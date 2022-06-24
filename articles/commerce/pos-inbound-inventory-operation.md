---
title: Myyntipisteen saapuva varastotoiminto
description: Tässä artikkelissa kuvataan myyntipisteen saapuva varastotoiminto.
author: hhaines
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: fbabcaafee74b4d0a1ca8ef79de94376a7764aa3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858879"
---
# <a name="inbound-inventory-operation-in-pos"></a>Myyntipisteen saapuva varastotoiminto

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commercen versiossa 10.0.10 ja myöhemmissä versioissa myyntipisteen saapuvat ja lähtevät toiminnot korvaavat keräys- ja vastaanottotoiminnon.

> [!NOTE]
> Commercen versiossa 10.0.10 ja myöhemmissä versioissa kaikki myyntipistesovelluksen uudet myymälän varaston vastaanoton ja osto- ja siirtotilausten ominaisuudet lisätään **saapuva toiminnon** myyntipistetoimintoon. Jos käytät tällä hetkellä myyntipisteen keräily- ja vastaanottotoimintoa, on suositeltavaa kehittää strategia, jonka avulla siirrytään kyseisen toiminnon käyttämisestä uuden saapuvien ja lähtevien toimintojen käyttämiseen. Vaikka keräily- ja vastaanottotoimintoa ei poisteta tuotteesta, sitä ei enää kehitetä toiminnallisesti eikä suorituskyvyn osalta version 10.0.9 jälkeen.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Edellytys: Asynkronisen asiakirjakehyksen määrittäminen

Saapuva toiminto sisältää suorituskyvyn parantamisen. Näin varmistetaan, että suuria määriä vastaanottokirjauksia käyttävät käyttäjät eri myymälöissä tai yrityksissä ja suurissa varastoasiakirjoissa voivat käsitellä näitä asiakirjoja Commerce Headquarters -sovelluksessa ilman aikakatkaisuja ja virheitä. Nämä parannukset edellyttävät asynkronisen asiakirjakehyksen käyttämistä.

Kun käytössä on asynkroninen asiakirjakehys, myyntipisteestä saapuvan asiakirjan muutokset voidaan ottaa käyttöön Commerce Headquarters -sovelluksessa ja siirtää sitten muille tehtäville samalla, kun Commerce Headquarters -käsittelyä tehdään taustalla. Voit tarkistaa asiakirjan tilan **Saapuva toiminto** -asiakirjaluettelosivun avulla myyntipisteessä. Näin voit varmistaa, että kirjaus onnistui. Myyntipistesovelluksessa voidaan käyttää myös saapuvan toiminnon aktiivista asiakirjaluetteloa. Näin nähdään asiakirjat, joita ei voi kirjata Commerce Headquarters -sovellukseen. Jos asiakirja epäonnistuu, myyntipisteen käyttäjät voivat tehdä korjauksia siihen ja yrittää sen käsittelyä uudelleen Commerce Headquarters -sovelluksessa.

> [!IMPORTANT]
> Asynkroninen asiakirjakehys on määritettävä ennen kuin yritys yrittää käyttää saapuvaa toimintoa myyntipisteessä.

Voit määrittää asynkronisen asiakirjakehyksen suorittamalla seuraavat toiminnot.

### <a name="create-and-configure-a-number-sequence"></a>Numerosarjan luominen ja määrittäminen

1. Siirry kohtaan **Organisaation hallinta \> Numerosarjat \> Numerosarjat**.
2. Luo **Numerosarjat**-sivulla numerosarja.
3. Anna **Numerosarjan koodi** ja **Nimi**-kenttiin käyttäjän määrittämät arvot.
4. Valitse **Viitteet**-pikavälilehdessä **Lisää**.
5. Valitse **Alue**-kentässä **Kaupan parametrit**.
4. Valitse **Viite**-kentässä **Vähittäismyyntiasiakirjatoiminnon tunniste**.
5. Määritä **Yleistä**-pikavälilehden **Asetukset**-osassa **Jatkuva**-asetuksen arvoksi **Ei**, jos haluat varmistaa, että suorituskykyongelmia ei ole.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Tehtäviä käsittelevän ja valvovan asiakirjan kahden erätyön luominen ja aikatauluttaminen

> [!NOTE]
> Commercen versiossa 10.0.13 ja sitä uudemmassa versiossa näitä erätöitä ei tarvitse määrittää erätyökehikossa. Eräprosessit voidaan määrittää **Retail ja Commerce > Retail ja Commerce IT** -valikossa. Määritä erätyöt **Vähittäismyynnin asiakirjatoiminnon seuranta**- ja **Vähittäismyynnin asiakirjatoiminnon käsittely** -valikkovaihtoehdoissa.

Luotuja erätöitä käytetään epäonnistuneiden tai aikakatkaistujen asiakirjojen käsittelyssä. Niitä käytetään myös silloin, kun myyntipisteessä käsiteltävien aktiivisten varastoasiakirjojen määrä ylittää järjestelmän määrittämän arvon.

1. Siirry kohtaa **Järjestelmänhallinta \> Kyselyt \> Erätyöt**.
2. Luo **Erätyö**-sivulla kaksi erätyötä seuraavasti:

    - Määritä yksi työ **RetailDocumentOperationMonitorBatch**-luokan suorittamista varten.
    - Määritä toinen työ **RetailDocumentOperationProcessingBatch**-luokan suorittamista varten.

2. Ajoita uudet erätyöt toistuvasti suoritettaviksi. Voit esimerkiksi määrittää ajoituksen niin, että työt suoritetaan viiden minuutin välein.

## <a name="prerequisite-add-inbound-operation-to-the-pos-screen-layout"></a>Edellytys: Saapuvan toiminnon lisääminen myyntipisteen näyttöasetteluun

Ennen kuin organisaatio voi käyttää saapuvaa toimintoa, se on määritettävä **saapuvan toiminnon** myyntipistetoiminnossa vähintään yhdessä [myyntipisteen näyttöasettelussa](/dynamics365/unified-operations/retail/pos-screen-layouts). Ennen kuin otat uuden toiminnon käyttöön tuotantoympäristössä, varmista, että se on testattu kunnolla ja käyttäjät on koulutettu käyttämään sitä.

## <a name="overview"></a>Yleiskatsaus

Saapuvan toiminnon avulla myyntipisteen käyttäjät voivat suorittaa seuraavat tehtävät:

- Vastaanota varasto myymälän varastosta vahvistetuista ostotilausasiakirjoista tai lähetetyistä siirtotilausasiakirjoista.
- Näytä aiempien varastovastaaottojen tiedot seitsemän päivän ajalta sen jälkeen, kun asiakirja on vastaanotettu kokonaan.
- Luo uusia saapuvia siirtotilauspyyntöjä.

Kun saapuva toiminto käynnistetään myyntipistesovelluksesta, näkyviin tulee luettelosivu. Tämä näkymä sisältää sellaisia varastorivejä sisältävät avoimet ostotilaus- ja siirtotilausasiakirjat, jotka on ajoitettu vastaanotettaviksi nykyiseen myymälään. Jos käyttäjät haluavat etsiä ja valita tietyn asiakirjan, he voivat selata luetteloa tai käyttää hakutoimintoa.

Saapuvien varastoasiakirjojen luettelossa on seuraavat kolme välilehteä:

- **Aktiivinen** – Tässä välilehdessä näkyvät kokonaan tai osittain avoimet asiakirjat, jotka sisältävät vielä vastaanotettavia rivejä tai määriä.
- **Luonnos** – Tässä välilehdessä ovat käyttäjän luomat uudet saapuvat siirtotilauspyynnöt. Asiakirjat on kuitenkin tallennettu vain paikallisesti. Niitä ei ole vielä lähetetty Commerce Headquarters -sovellukseen käsittelyä varten.
- **Valmis** – Tässä välilehdessä on niiden ostotilaus- tai siirtotilausasiakirjojen luettelo, jotka on vastaanotettu kokonaan edellisten seitsemän päivän aikana. Tämä välilehti on tarkoitettu vain tiedoksi. Kaikki asiakirjoja koskevat tiedot ovat vain lukumuodossa myymälää varten.

Kun tarkastelet asiakirjoja muilla välilehdillä, **Tila**-kentän avulla saat tietoja asiakirjan vaiheesta.

- **Luonnos** – Siirtotilausasiakirja on tallennettu vain paikallisesti myymälän kanavan tietokantaan. Siirtotilauspyyntöä koskevia tietoja ei ole vielä lähetetty Commerce Headquarters -sovellukseen.
- **Pyydetty** – Ostotilaus tai siirtotilaus on luotu Commerce Headquarters -sovelluksessa ja se on täysin avoinna. Vastaanottoja ei ole vielä käsitelty asiakirjan avulla. Jos asiakirjan tyyppi on Ostotilaus, vastaanotto voidaan tehdä milloin tahansa, jos tila on **Pyydetty**.
- **Osittain lähetetty** – Siirtotilausasiakirjassa on yksi rivi tai useita rivejä tai osittaisia rivimääriä, jotka on kirjattu lähtevän varaston lähettämiksi. Nämä lähetetyt rivit ovat vastaanotettavissa saapuvan toiminnon kautta.
- **Kokonaan lähetetty** – Siirtotilauksen kaikki rivit ja kaikki rivimäärät on kirjattu lähtevän varaston lähettämiksi. Koko asiakirja on vastaanotettavissa saapuvan toiminnon kautta.
- **Osittain vastaanotettu** – Myymälä on vastaanottanut osan ostotilaus- tai siirtotilausasiakirjan riveistä tai rivimääristä. Jotkin rivit jäävät kuitenkin avoimiksi.
- **Täysin vastaanotettu** – Kaikki ostotilaus- tai siirtotilausasiakirjan rivit ja määrät on vastaanotettu kokonaan. Asiakirjat ovat käytettävissä vain **Valmis**-välilehdessä. Myymälän käyttäjät voivat lukea niitä.
- **Käsittelyssä** – Tämän tilan avulla ilmoitetaan laitteen käyttäjille, että toinen käyttäjä käsittelee asiakirjaa parhaillaan.
- **Keskeytetty** – Tämä tila näkyy sen jälkeen, kun **Keskeytä vastaanotto** on valittu ja vastaanottoprosessi on pysäytetty väliaikaisesti.
- **Käsitellään HQ:ssa** – Asiakirja on lähetetty Commerce Headquarters -sovellukseen myyntipistesovelluksesta, mutta sen kirjaaminen Commerce Headquarters -sovellukseen ei onnistunut. Asiakirjaa käsitellään asynkronisen asiakirjan kirjausprosessissa. Kun asiakirjan kirjaaminen Commerce Headquarters -sovellukseen onnistuu, sen tilaksi päivitetään **Kokonaan vastaanotettu** tai **Osittain vastaanotettu**.
- **Käsittely epäonnistui** – Asiakirja kirjattiin Commerce Headquarters -sovellukseen ja hylättiin. **Tiedot**-ruudussa näkyy kirjaamisen epäonnistumisen syy. Asiakirjaa on muokattava, jotta tietojen virheet voidaan korjata. Tämän jälkeen se lähetetään uudelleen Commerce Headquarters -sovellukseen käsittelyä varten.

Kun valitset asiakirjarivin luettelosta, näkyviin tulee **Tiedot**-ruutu. Tässä ruudussa näkyvät asiakirjaa koskevat lisätiedot, kuten lähetys- ja päivämäärätiedot. Tilanneilmaisin osoittaa, miten monta nimikettä on vielä käsiteltävä. Jos asiakirjan käsitteleminen Commerce Headquarters -sovelluksessa ei onnistunut, **Tiedot**-ruudussa näkyy myös virheeseen liittyvät virhesanomat.

Asiakirjaluettelosivun näkymässä voit valita sovelluspalkissa **Tilauksen tiedot**, jos haluat tarkastella asiakirjan tietoja. Voit myös aktivoida vastaanottokäsittelyn sallituilla asiakirjariveillä.

Asiakirjaluettelosivun näkymässä voit luoda uuden saapuvan siirtotilauspyynnön myymälää varten. Asiakirjojen tilana pysyy **Luonnos**. Niitä voi muokata tai ne voi poistaa niin kauan, kunnes ne lähetetään Commerce Headquarters -sovellukseen käsittelyä varten. Kun ne on lähetetty Commerce Headquarters -sovellukseen siirtotilausrivejä ei enää voi muuttaa myyntipistesovelluksessa.

## <a name="receiving-process"></a>Vastaanottoprosessi

Kun olet valinnut ostotilaus- tai siirtotilausasiakirjan **Aktiivinen**-välilehdessä, voit valita **Tilauksen tiedot** ja aloittaa vastaanottoprosessin.

Oletusarvon mukaan näkyviin tulee **Vastaanotto nyt** -näkymä. Tämä näkymä on optimoitu viivakoodin skannausta varten. Sen avulla voidaan luoda luettelo skannatuista nimikkeistä. Tämän jälkeen kyseiset nimikkeet voidaan vastaanottaa. Voit aloittaa vastaanottoprosessin skannaamalla nimikkeen viivakoodit.

Kun nimikkeen viivakoodit skannataan **Vastaanotto nyt** -näkymässä, sovellus tarkistaa nimikkeet valitun osto- tai siirtotilausasiakirjan perusteella ja varmistaa, että kukin skannattu nimike vastaa asiakirjan sallittua nimikettä. **Vastaanotto nyt** -näkymässä kunkin viivakoodin skannauksen oletetaan edustavan yhden yksikön määrän vastaanottoa, ellei määrää ole upotettu viivakoodiin. Voit skannata viivakoodeja toistuvasti tässä näkymässä, jos haluat luoda luettelon kaikista vastaanoton nimikkeistä ja määristä.

### <a name="example-scenario"></a>Esimerkkiskenaario

Käyttäjä vastaanottaa ostotilauksen, joka sisältää 10 yksikköä viivakoodilla 5657900266. Käyttäjä voi skannata viivakoodin 10 times kertaa ja päivittää **Vastaanotto nyt** -kentän yhdellä yksiköllä per skannaus. Kun käyttäjä on tehnyt skannaukset valmiiksi, nimikkeen rivin **Vastaanotto nyt** -kentässä on vastaanotettu 10 yksikön määrä.

Vaihtoehtoisesti skenaariossa, jossa nimikemäärä on suuri, käyttäjä voi halutessaan syöttää määrän manuaalisesti kunkin vastaanotetun nimikkeen viivakoodin skannaamisen sijaan. Tässä tapauksessa käyttäjä voi skannata viivakoodin kerran, jolloin nimike lisätään **Vastaanotto nyt** -luetteloon. Käyttäjä voi sitten valita liittyvän rivin **Vastaanotto nyt** -näkymässä ja päivittää sivun oikealla puolella näkyvässä **Tiedot**-ruudussa nimikkeen **Vastaanoton määrä** -kentän.

Vaikka **Vastaanotto nyt** -näkymä on optimoitu viivakoodin skannaamista varten, käyttäjät voivat valita sovelluspalkissa myös **Vastaanota tuote** -kohdan ja syöttää nimikkeen tunnuksen tai viivakoodin tiedot tässä valintaikkunassa. Kun syötetty nimike on tarkistettu, käyttää pyydetään antamaan vastaanottomäärä.

**Vastaanotto nyt** -näkymän avulla käyttäjät näkevät, mitä tuotteita vastaanotetaan. Vaihtoehtoisesti voidaan käyttää **Täydellinen tilausluettelo** -näkymää. Tässä näkymässä on valitun osto- tai siirtotilausasiakirjan asiakirjarivien täydellinen luettelo. Käyttäjät voivat valita rivit luettelosta manuaalisesti ja päivittää tämän jälkeen **Tiedot**-ruudussa valitun rivin **Vastaanottomäärä**-kentän. **Täydellinen tilausluettelo** -näkymässä käyttäjät voivat skannata viivakoodeja. **Vastaanota tuote** -toiminnon avulla he voivat syöttää nimikkeen tunnuksen tai viivakoodin ja vastaanotetun määrän tiedot ilman, että luettelosta pitää valita vastaava nimikerivi.

### <a name="over-receiving-validations"></a>Ylivastaanoton tarkistukset

Tarkistukset tapahtuvat asiakirjarivien vastaanottoprosessin aikana. Ne sisältävät ylitoimituksen tarkistukset. Jos käyttäjä yrittää vastaanottaa enemmän varastoa kuin ostotilauksen mukaan on tilattu, mutta ylitoimitusta ei ole määritetty tai vastaanotettu summa ylittää ostotilausrivillä määritetyn ylitoimitustoleranssin, käyttäjä vastaanottaa virheen, koska ylimääräistä määrää ei voi vastaanottaa.

Ylivastaanotto ei ole sallittu siirtotilausasiakirjoille Käyttäjät vastaanottavat aina virheitä, jos he vastaanottavat enemmän kuin siirtotilausrivin mukaan on lähetetty.

### <a name="close-purchase-order-lines"></a>Ostotilausrivien sulkeminen

Voit sulkea saapuvan ostotilauksen jäljellä olevan määrän vastaanottoprosessin aikana, jos lähettäjä on vahvistanut, etteivät he lähetä koko pyydettyä määrää. Sitä varten yritys on määritettävä sallimaan ostotilausten alitoimitus. Lisäksi ostotilausriville on määritettävä alitoimituksen toleranssiprosentti.

Yritys määritetään sallimaan ostotilausten alitoimitus valitsemalla Commerce Headquartersissa **Hankinta** > **Asetukset** > **Hankintaparametrit**. Ota **Hyväksy alitoimitus** -parametri käyttöön **Toimitus**-välilehdessä. Synkronoi asetuksen muutokset kanaviin suorittamalla **1070** (**Kananvan määritys**) -jakelun ajoitustehtävä.

Ostotilausrivin alitoimituksen toleranssiprosentti voidaan määrittää tuotteissa ennalta tuotteen määritysten osana Commerce Headquartersissa. Vaihtoehtoisesti ne voidaan määrittää tai korvata tietyllä ostotilauksella Commerce Headquartersissa.

Kun organisaatio on määrittänyt ostotilauksen alitoimituksen, myyntipisteen käyttäjät näkevät **Sulje jäljellä oleva määrä** -vaihtoehdon **Tiedot**-ruudussa, kun saapuva ostotilausrivi valitaan **Saapuva varasto** -toiminnossa. Jos käyttäjä sulkee jäljellä olevan määrän, myyntipiste vahvistaa, onko suljettava määrä ostotilausrivillä määritetyn alitoimituksen toleranssiprosentin mukainen. Jos alitoimitustoleranssi ylittyy, virhesanoma avautuu eikä käyttäjä voi sulkea jäljillä olevaa määrää, ennen kuin aiemmin vastaanotettu määrä ja siihen lisätty **Vastaanotto nyt** -määrä vastaavat tai ylittävät vastaanotettavan alitoimituksen toleranssiprosenttiin perustuvan vähimmäismäärän. 

Kun **Sulje jäljellä oleva määrä** -vaihtoehto on otettu käyttöön ostotilausrivillä ja käyttäjä suorittaa vastaanoton loppuun **Viimeistele vastaanotto** -toiminnon, sulkemispyyntö lähetetään myös Commerce Headquartersiin ja tämän tilauksen vielä vastaanottamaton määrä peruutetaan. Tässä vaiheessa rivi katsotaan täysin vastaanotetuksi. 

### <a name="receiving-location-controlled-items"></a>Vastaanoton sijaintiohjatut nimikkeet

Jos vastaanotettavat nimikkeet ovat sijaintiohjattuja, käyttäjät voivat valita sijainnin, jossa he haluavat vastaanottaa nimikkeet vastaanottoprosessin aikana. Myymälän varastolle kannattaa määrittää oletusvastaanottosijainti. Tällöin prosessi on aiempaa tehokkaampi. Vaikka oletusvastaanottosijainti olisi määritetty, käyttäjät voivat korvata sen halutessaan valituilla riveillä.

Toiminto noudattaa **Tyhjä vastaanotto sallitaan** -määritystä **sijainnin** varastodimensiossa. Sijainnin dimensiota ei tarvitse syöttää, jos tyhjä vastaanotto on määritetty. Jos tyhjät vastaanottosijainnit eivät ole sallittuja nimikkeelle, myyntipistesovellus näyttää virheen ja vaatii sijainnin syöttämisen ennen vastaanoton kirjaamista.

### <a name="receive-all"></a>Vastaanota kaikki

Voit halutessasi valita **Vastaanota kaikki** sovelluspalkissa ja päivittää kaikkien asiakirjarivien **Vastaanotto nyt** -määrän nopeasti enimmäisarvoksi, joka on vastaanotettavissa näille riveille.

### <a name="receipt-of-unplanned-items-on-purchase-orders"></a>Suunnittelemattomien nimikkeiden vastaanotto ostotilauksissa

Käyttäjät voivat vastaanottaa Commercessa versiosta 10.0.14 alkaen tuotteen, jota ei ollut alun perin ostotilauksessa. Tämä toiminto otetaan käyttöön ottamalla **Lisää rivejä ostotilaukseen myyntipisteen vastaanoton aikana**.  

Tämä toiminto toimii vain ostotilauksen vastaanottamisessa. Nimikkeitä ei voi vastaanottaa siirtotilausten perusteella, jos nimikkeitä ei ole tilattu aiemmin ja lähetetty lähtevästä varastosta.

Käyttäjät eivät voi lisätä uusia tuotteita ostotilaukseen myyntipisteen vastaanoton aikana, jos ostotilauksen [muutosten hallinnan työnkulku](../supply-chain/procurement/purchase-order-approval-confirmation.md) on otettu käyttöön Commercen pääkonttoriversiossa (HQ). Muutosten hallinnan käyttöönotto edellyttää, että kaikki ostotilauksen muutokset on hyväksyttävä, ennen kuin vastaanotto sallitaan. Koska vastaanottaja voi tämän prosessin myötä lisätä uusia rivejä ostotilaukseen, vastaanotto epäonnistuu, jos muutosten hallinnan työnkulku on otettu käyttöön. Jos muutosten hallinta on otettu käyttöön kaikissa ostotilauksissa tai toimittaja on linkitetty ostotilaukseen, jota vastaanotetaan aktiivisesti myyntipisteessä, käyttäjä ei voi lisätä myyntipisteessä uusia tuotteita ostotilaukseen vastaanoton aikana.

Rivien lisäämisen mahdollistavaa toimintoa ei voi käyttää keinona vastaanottaa lisää ostotilauksessa jo olevia tuotteita. Ylivastaanottoa hallitaan ostotilauksen tuoterivin [ylivastaanoton](#over-receiving-validations) vakioasetuksilla.

Jos **Lisää rivejä ostotilaukseen myyntipisteen vastaanoton aikana** on otettu käyttöön ja käyttäjä käyttää myyntipisteessä vastaanottoon **saapuvaa toimintoa** ja jos käyttäjä lukee tai näppäilee tuotteen viivakoodin tai tuotenumeron, jota ei tunnisteta nykyisen ostotilauksen nimikkeeksi mutta joka tunnistetaan kelvolliseksi nimikkeeksi, käyttäjä vastaanottaa ilmoituksen nimikkeen lisäämisestä ostotilaukseen. Jos käyttäjä lisää nimikkeen ostotilaukseen, **Vastaanotto nyt** -kohdassa annettua arvoa pidetään ostotilausrivin tilattuna määränä.

Kun ostotilaus on vastaanotettu ja lähetetty käsiteltäväksi pääkonttoriversioon, lisätyt rivit luodaan ostotilauksen pääasiakirjaan. Pääkonttoriversion ostotilausrivillä on **Myyntipiste lisännyt** -merkintä ostotilausrivin **Yleiset**-välilehdessä. **Myyntipiste lisännyt** -merkintä ilmaisee, että myyntipisteen vastaanottoprosessi lisäsi ostotilausrivin ja että rivi ei ollut ostotilauksessa ennen vastaanottoa.

### <a name="cancel-receiving"></a>Peruuta vastaanotto

Käytä **Peruuta vastaanotto** -toiminto sovelluspalkissa vain, jos haluat peruuttaa asiakirjan, etkä halua tallentaa muutoksia. Tee niin esimerkiksi silloin, kun valitsit alussa väärän asiakirjan, etkä halua tallentaa aiempia vastaanottotietoja.

### <a name="pause-receiving"></a>Keskeytä vastaanotto

Jos olet vastaanottamassa varastoa, voit käyttää **Keskeytä vastaanotto** -toimintoa ja keskeyttää vastaanottoprosessin. Voit esimerkiksi haluta suorittaa myyntipisteessä toisen toiminnon, kuten soittaa asiakasmyyntiin, tai tehdä vastaanoton kirjauksen myöhemmin.

Kun valitset **Keskeytä vastaanotto** -vaihtoehdon, asiakirjan tilaksi muutetaan **Keskeytetty**. Näin käyttäjät tietävät, mitä tietoja asiakirjaan on syötetty ja että asiakirjaa ei ole vielä vahvistettu. Kun olet valmis jatkamaan vastaanottoprosessia, valitse keskeytetty asiakirja ja valitse sitten **Tilauksen tiedot**. Kaikki aiemmin tallennetut **Vastaanotto nyt** -määrät säilytetään. Ne näkyvät **Täydellinen tilausluettelo** -näkymässä.

### <a name="review"></a>Tarkista

Ennen lopullista sitoutumista Commercen pääkonttorisovellukseen vastaanotosta, voit käyttää Tarkista-toimintoa ja vahvistaa saapuvan asiakirjan. Tarkistustoiminto kertoo mahdollisista puuttuvista tai virheellisistä tiedoista, jotka saattavat aiheuttaa käsittelyvirheen, sekä antaa mahdollisuuden korjata ongelmia ennen vastaanottopyynnön lähettämistä. Jos haluat ottaa käyttöön **Tarkista**-toiminnon sovelluspalkissa, ota käyttöön **Ota käyttöön vahvistus myyntipisteen saapuvissa ja lähtevissä varastotoiminnoissa** -ominaisuus **Ominaisuuksien hallinta** -työtilassa Commercen pääkonttorisovelluksessa.

**Tarkista**-toiminto vahvistaa seuraavat ongelmat saapuvassa asiakirjassa:

- **Ylivastaanotto** - vastaanoton määrä on suurempi kuin tilattu määrä. Commercen pääkonttorisovelluksen ylitoimituksen määritys määrittää tämän ongelman vakavuuden.
- **Elivastaanotto** - vastaanoton määrä on pienempi kuin tilattu määrä. Commercen pääkonttorisovelluksen alitoimituksen määritys määrittää tämän ongelman vakavuuden.
- **Sarjanumero** – sarjanumeroa ei ole annettu tai sitä ei ole vahvistettu sarjoitetulle nimikkeelle, joka vaatii sarjanumeron rekisteröimisen varastossa.
- **Sijaintia ei ole määritetty** – sijaintia ei ole määritetty sijaintiohjatulle nimikkeelle, jossa sijainti ei saa olla tyhjä.
- **Poistetut rivit** – Commercen pääkonttorisovelluksen käyttäjä, joka myyntipistesovellus ei tunne, on poistanut tilauksen rivejä.

Määritä **Ota käyttöön automaattinen vahvistus** -parametrin arvoksi **Kyllä** kohdassa **Commerce-parametrit** > **Varasto** > **Myymälän varasto**, jos haluat, että vahvistus tehdään automaattisesti, kun **Lopeta vastaanotto** on valittuna.

### <a name="finish-receiving"></a>Viimeistele vastaanotto

Kun olet syöttänyt kaikki **Vastaanotto nyt** -määrät tuotteille, valitse sovelluspalkissa **Tee vastaanotto valmiiksi** vastaanoton käsittelemiseksi.

Kun käyttäjä tekee ostotilauksen vastaanoton valmiiksi, häntä pyydetään antamaan arvo **Vastaanottonumero**-kenttään, jos tämä toiminto on määritetty. Yleensä tämä arvo on sama kuin toimittajan pakkausluettelon tunniste. **Vastaanottonumeron** tiedot tallennetaan Commerce Headquarters -sovelluksen tuotteen vastaanoton kirjauskansioon. Siirtotilausten vastaanottojen vastaanottonumeroita ei tallenneta.

Kun käytetään asynkronista asiakirjojen käsittelyä, kuitti lähetetään asynkronisen asiakirjakehyksen kautta. Asiakirjan kirjaamiseen kuluva aika riippuu asiakirjan koosta (rivien määrä) ja palvelimella tapahtuvasta yleisen tietoliikenteen määrästä. Yleensä tämä prosessi tapahtuu muutamassa sekunnissa. Jos asiakirjan kirjaaminen epäonnistuu, käyttäjälle lähetetään ilmoitus **Saapuva toiminto** -asiakirjaluettelon kautta Aktiivinen-välilehdessä. Siellä asiakirjan tilaksi päivitetään **Käsittely epäonnistui**. Käyttäjä voi sitten valita epäonnistuneen asiakirjan myyntipisteessä ja tarkastella virhesanomaa ja virheen syytä **Tiedot**-ruudussa. Epäonnistunut asiakirja säilyy kirjaamattomana. Käyttäjän on palattava asiakirjariveille valitsemalla **Tilauksen tiedot** myyntipisteessä. Käyttäjän on tämän jälkeen päivitettävä asiakirjaan korjaukset virheiden perusteella. Kun asiakirja on korjattu, käyttäjä voi yrittää sen käsittelyä uudelleen valitsemalla **Tee täyttäminen valmiiksi** sovelluspalkissa.

## <a name="create-an-inbound-transfer-order"></a>Saapuvan siirtotilauksen luominen

Käyttäjät voivat luoda myyntipisteessä uusia siirtotilausasiakirjoja. Aloita prosessi valitsemalla **Uusi** sovelluspalkissa, kun olet **Saapuva toiminto** -pääasiakirjaluettelossa. Tämän jälkeen sinua pyydetään valitsemaan **Siirron lähde** -varasto, tai myymälä, jossa myymälän sijainnin varasto on. Mahdollisia arvoja ovat myymälän täyttämisryhmän kokoonpanossa määritetyt arvot. Nykyinen myymälä on aina saapuvan siirtopyynnön **Siirron kohde** -varasto siirtotilauksessa. Arvoa ei voi muuttaa.

Voit syöttää arvot **Lähetyspäivä**-, **Vastaanottopäivä**- ja **Toimitustapa** -kenttiin haluamallasi tavalla. Voit myös lisätä muistiinpanon, joka tallennetaan yhdessä siirtotilauksen otsikon kanssa liitteenä asiakirjaan Commerce Headquarters -sovelluksessa.

Kun otsikon tiedot on luotu, voit lisätä siirtotilaukseen tuotteita. Aloita nimikkeiden ja pyydettyjen määrien lisääminen valitsemalla **Lisää tuote**. **Tiedot**-ruudussa voit myös lisätä rivikohtaisen huomautuksen kirjauskansion riveille. Nämä huomautukset tallennetaan rivin liitteenä.

Kun saapuvan siirtotilauksen rivit on syötetty, valitse **Tallenna** ja tallenna asiakirjan muutokset paikallisesti tai valitse **Lähetä pyyntö** ja lähetä tilauksen tiedot Commerce Headquarters -sovellukseen lisäkäsittelyä varten. Jos valitset **Tallenna**, oletusasiakirja tallennetaan kanavan tietokantaan. Lähtevä varasto voi suorittaa asiakirjan vasta, kun se on käsitelty onnistuneesti **Lähetä pyyntö** -kohdassa. Valitse **Tallenna** vain, jos et ole valmis vahvistamaan pyyntöä Commerce Headquarters -sovelluksessa käsittelyä varten.

Jos asiakirja tallennetaan paikallisesti, se löytyy **Luonnokset**-välilehdestä **Saapuva toiminto** -asiakirjaluettelosta. Kun asiakirjan tila on **Luonnos**, voit muokata sitä valitsemalla **Muokkaa**. Voit päivittää, lisätä tai poistaa rivejä tarvittaessa. Voit myös poistaa koko asiakirjan, kun sen tila on **Luonnos**, valitsemalla **Poista** **Luonnokset**-välilehdessä.

Kun luonnosasiakirjan lähettäminen Commerce Headquarters -sovellukseen onnistuu, se näkyy **Aktiivinen**-välilehdessä ja sen tila on **Pyydetty**. Tässä vaiheessa saapuvan myymälän tai varaston käyttäjät eivät voi enää muokata pyydettyä saapuvaa siirtotilausasiakirjaa. Vain lähtevän varaston käyttäjät voivat muokata asiakirjaa valitsemalla myyntipisteessä **Lähtevä toiminto** -kohdan. Muokkauksen lukituksen avulla voidaan välttää ristiriidat, koska saapuva pyytäjä muuttaa siirtotilausta samalla kuin lähtevien huolitsija keräilee ja lähettää tilausta aktiivisesti. Jos saapuvasta myymälästä tai varastosta on saatava muutoksia siirtotilauksen lähettämisen jälkeen, lähtevien huolitsijaan on otettava yhteyttä ja pyydettävä muutosten käyttöönottoa.

Kun asiakirjan tila on **Pyydetty**, se näkyy **Aktiivinen**-välilehdessä. Saapuva myymälä tai varasto ei voi kuitenkaan vielä vastaanottaa sitä. Kun lähtevä varasto on lähettänyt osan siirtotilauksesta tai sen kokonaan, saapuva myymälä tai varasto voi kirjata vastaanotot myyntipisteessä. Kun lähtevä toiminto käsittelee siirtotilausasiakirjoja, niiden tilaus päivitetään **Pyydetty**-tilasta **Lähetetty**- tai **Osittain lähetetty** -tilaksi. Kun asiakirjojen tila on **Lähetetty** tai **Osittain lähetetty**, saapuva myymälä tai varasto voi kirjata vastanotot niiden avulla käyttämällä saapuvan toiminnon vastaanottoprosessia.

## <a name="related-articles"></a>Liittyvät artikkelit

[Myyntipisteen lähtevä varastotoiminto](pos-outbound-inventory-operation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]