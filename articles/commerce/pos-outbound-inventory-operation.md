---
title: Myyntipisteen lähtevä varastotoiminto
description: Tässä ohjeaiheessa kuvataan myyntipisteen lähtevä varastotoiminto.
author: hhaines
ms.date: 07/30/2020
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
ms.openlocfilehash: 3cfe144f7bba2bbc4b25024b68155045271f6366
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795642"
---
# <a name="outbound-inventory-operation-in-pos"></a>Myyntipisteen lähtevä varastotoiminto

[!include [banner](includes/banner.md)]


Microsoft Dynamics 365 Commercen versiossa 10.0.10 ja myöhemmissä versioissa myyntipisteen saapuvat ja lähtevät toiminnot korvaavat keräys- ja vastaanottotoiminnon.

> [!NOTE]
> Versiossa 10.0.10 ja myöhemmissä versioissa kaikki myyntipistesovelluksen uudet myymälän varaston vastaanoton ja osto- ja siirtotilausten ominaisuudet lisätään saapuvien toimintojen toimintoon. Jos käytät tällä hetkellä myyntipisteen keräily- ja vastaanottotoimintoa, on suositeltavaa kehittää strategia, jonka avulla siirrytään kyseisen toiminnon käyttämisestä uuden saapuvien ja lähtevien toimintojen käyttämiseen. Vaikka keräily- ja vastaanottotoimintoa ei poisteta tuotteesta, sitä ei enää kehitetä toiminnallisesti eikä suorituskyvyn osalta version 10.0.9 jälkeen.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Edellytys: Asynkronisen asiakirjakehyksen määrittäminen

Lähtevä toiminto sisältää suorituskyvyn parantamisen. Näin varmistetaan, että suuria määriä vastaanottokirjauksia käyttävät käyttäjät eri myymälöissä tai yrityksissä ja suurissa varastoasiakirjoissa voivat käsitellä näitä asiakirjoja Commercen pääkonttorisovelluksessa ilman aikakatkaisuja ja virheitä. Nämä parannukset edellyttävät asynkronisen asiakirjakehyksen käyttämistä.

Kun käytössä on asynkroninen asiakirjakehys, myyntipisteestä lähtevän asiakirjan muutokset voidaan ottaa käyttöön Commercen pääkonttorisovelluksessa ja siirtää sitten muille tehtäville samalla, kun Commercen pääkonttorisovellus on taustalla. Voit tarkistaa asiakirjan tilan **Lähtevä toiminto** -asiakirjaluettelosivun avulla myyntipisteessä. Näin voit varmistaa, että kirjaus onnistui. Myyntipistesovelluksessa voidaan käyttää myös lähtevän toiminnon aktiivista asiakirjaluetteloa. Näin nähdään asiakirjat, joita ei voi kirjata Commercen pääkonttorisovellukseen. Jos asiakirja epäonnistuu, myyntipisteen käyttäjät voivat tehdä korjauksia siihen ja yrittää sen käsittelyä uudelleen Commercen pääkonttorisovelluksessa.

> [!IMPORTANT]
> Asynkroninen asiakirjakehys on määritettävä ennen kuin yritys yrittää käyttää lähtevää toimintoa myyntipisteessä.

Voit määrittää asynkronisen asiakirjakehyksen suorittamalla seuraavat toiminnot.

### <a name="create-and-configure-a-number-sequence"></a>Numerosarjan luominen ja määrittäminen

1. Siirry kohtaan **Organisaation hallinta \> Numerosarjat \> Numerosarjat**.
2. Luo **Numerosarjat**-sivulla numerosarja.
3. Anna **Numerosarjan koodi** ja **Nimi**-kenttiin käyttäjän määrittämät arvot.
4. Valitse **Viitteet**-pikavälilehdessä **Lisää**.
5. Valitse **Alue**-kentässä **Kaupan parametrit**.
6. Valitse **Viite**-kentässä **Vähittäismyyntiasiakirjatoiminnon tunniste**.
7. Määritä **Yleistä**-pikavälilehden **Asetukset**-osassa **Jatkuva**-asetuksen arvoksi **Ei**, jos haluat varmistaa, että suorituskykyongelmia ei ole.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Tehtäviä käsittelevän ja valvovan asiakirjan kahden erätyön luominen ja aikatauluttaminen

> [!NOTE]
> Commercen versiossa 10.0.13 ja sitä uudemmassa versiossa erätöitä ei tarvitse määrittää erätyökehikossa. Eräprosessit voidaan määrittää **Retail ja Commerce > Retail ja Commerce IT** -valikossa. Määritä erätyöt **Vähittäismyynnin asiakirjatoiminnon seuranta**- ja **Vähittäismyynnin asiakirjatoiminnon käsittely** -valikkovaihtoehdoissa.

Luotuja erätöitä käytetään epäonnistuneiden tai aikakatkaistujen asiakirjojen käsittelyssä. Niitä käytetään myös silloin, kun myyntipisteessä käsiteltävien aktiivisten varastoasiakirjojen määrä ylittää järjestelmän määrittämän arvon.

1. Siirry kohtaa **Järjestelmänhallinta \> Kyselyt \> Erätyöt**.
2. Luo **Erätyö**-sivulla kaksi erätyötä seuraavasti:

    - Määritä yksi työ **RetailDocumentOperationMonitorBatch**-luokan suorittamista varten.
    - Määritä toinen työ **RetailDocumentOperationProcessingBatch**-luokan suorittamista varten.

3. Ajoita uudet erätyöt toistuvasti suoritettaviksi. Voit esimerkiksi määrittää ajoituksen niin, että työt suoritetaan viiden minuutin välein.

## <a name="prerequisite-add-outbound-operation-to-the-pos-screen-layout"></a>Edellytys: Lähtevän toiminnon lisääminen myyntipisteen näyttöasetteluun

Ennen kuin organisaatio voi käyttää lähtevää toimintoa, se on määritettävä **lähtevän toiminnon** myyntipistetoiminnossa vähintään yhdessä [myyntipisteen näyttöasettelussa](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts). Ennen kuin otat uuden toiminnon käyttöön tuotantoympäristössä, varmista, että se on testattu kunnolla ja käyttäjät on koulutettu käyttämään sitä.

## <a name="overview"></a>Yleiskatsaus

Lähtevän toiminnon avulla myyntipisteen käyttäjät voivat suorittaa seuraavat tehtävät:

- Kirjaa lähetykset siirtotilausasiakirjoille silloin, kun käyttäjän myymälä on määritetty lähteväksi varastoksi.
- Tarkastele myymälässä kirjattujen aiempien siirtotilausten lähetysten tietoja.
- Luo uusia lähteviä siirtotilauspyyntöjä.

Kun lähtevä toiminto käynnistetään myyntipistesovelluksesta, näkyviin tulee luettelosivu. Tämä näkymä sisältää sellaisia varastorivejä sisältävät avoimet siirtotilausasiakirjat, jotka käyttäjän nykyinen myymälä aikoo lähettää ja täyttää. Jos käyttäjät haluavat etsiä ja valita asiakirjan, he voivat selata luetteloa tai käyttää hakutoimintoa.

Lähtevien varastoasiakirjojen luettelossa on kolme välilehteä.

- **Aktiivinen** – Tässä välilehdessä ovat siirtotilaukset, joiden tila on **Pyydetty** tai **Osittain lähetetty**. Tilaukset sisältävät rivejä tai rivien määriä, jotka käyttäjän nykyisen myymälän on lähetettävä. Tämä välilehti sisältää myös tilaukset, joiden tila on **Käsitellään HQ:ssa** (eli ne odottavat onnistuneen kirjauksen vahvistusta Commercen pääkonttorisovelluksesta) tai **Käsittely epäonnistui** (eli kirjaaminen Commercen pääkonttorisovellukseen ei onnistunut, joten käyttäjän on korjattava tiedot ja yritettävä lähettää tilaukset uudelleen).
- **Luonnos** – Tässä välilehdessä ovat käyttäjän luomat uudet lähtevät siirtotilauspyynnöt. Asiakirjat on kuitenkin tallennettu vain paikallisesti. Niitä ei ole vielä lähetetty Commercen pääkonttorisovellukseen käsittelyä varten.
- **Valmis** – Tässä välilehdessä on niiden siirtotilausasiakirjojen luettelo, jotka on lähetetty kokonaan edellisten seitsemän päivän aikana. Tämä välilehti on tarkoitettu vain tiedoksi. Kaikki asiakirjoja koskevat tiedot ovat vain lukumuodossa myymälää varten.

Kun tarkastelet asiakirjoja muilla välilehdillä, **Tila**-kentän avulla saat tietoja asiakirjan vaiheesta.

- **Luonnos** – Siirtotilausasiakirja on tallennettu vain paikallisesti myymälän kanavan tietokantaan. Siirtotilauspyyntöä koskevia tietoja ei ole vielä lähetetty Commercen pääkonttorisovellukseen.
- **Pyydetty** – Ostotilaus tai siirtotilaus on luotu Commercen pääkonttorisovellukseen ja se on täysin avoinna. Käyttäjän nykyinen myymälä ei ole vielä käsitellyt asiakirjojen lähetyksiä.
- **Osittain lähetetty** – Siirtotilausasiakirjassa on yksi rivi tai useita rivejä tai osittaisia rivimääriä, jotka on kirjattu lähtevän varaston lähettämiksi. Nämä lähetetyt rivit ovat vastaanotettavissa saapuvan toiminnon kautta.
- **Kokonaan lähetetty** – Siirtotilauksen kaikki rivit ja kaikki rivimäärät on kirjattu lähtevän varaston lähettämiksi.
- **Käsittelyssä** – Tämän tilan avulla ilmoitetaan laitteen käyttäjille, että toinen käyttäjä käsittelee asiakirjaa parhaillaan.
- **Keskeytetty** – Tämä tila näkyy sen jälkeen, kun **Keskeytä vastaanotto** on valittu ja vastaanottoprosessi on pysäytetty väliaikaisesti.
- **Käsitellään HQ:ssa** – Asiakirja on lähetetty Commercen pääkonttorisovellukseen myyntipistesovelluksesta, mutta sen kirjaaminen Commercen pääkonttorisovellukseen ei onnistunut. Asiakirjaa käsitellään asynkronisen asiakirjan kirjausprosessissa. Kun asiakirjan kirjaaminen Commercen pääkonttorisovellukseen onnistuu, sen tilaksi päivitetään **Kokonaan vastaanotettu** tai **Osittain vastaanotettu**.
- **Käsittely epäonnistui** – Asiakirja kirjattiin Commercen pääkonttorisovellukseen ja hylättiin. **Tiedot**-ruudussa näkyy kirjaamisen epäonnistumisen syy. Asiakirjaa on muokattava, jotta tietojen virheet voidaan korjata. Tämän jälkeen se lähetetään uudelleen Commercen pääkonttorisovellukseen käsittelyä varten.

Kun valitset asiakirjarivin luettelosta, näkyviin tulee **Tiedot**-ruutu. Tässä ruudussa näkyvät asiakirjaa koskevat lisätiedot, kuten lähetys- ja päivämäärätiedot. Tilanneilmaisin osoittaa, miten monta nimikettä on vielä käsiteltävä. Jos asiakirjan käsitteleminen Commercen pääkonttorisovelluksessa ei onnistunut, **Tiedot**-ruudussa näkyy myös virheeseen liittyvät virhesanomat.

Asiakirjaluettelosivun näkymässä voit valita sovelluspalkissa **Tilauksen tiedot**, jos haluat tarkastella asiakirjan tietoja. Voit myös aktivoida vastaanottokäsittelyn sallituilla asiakirjariveillä.

Asiakirjaluettelosivun näkymässä voit luoda uuden lähtevän siirtotilauksen myymälää varten.

## <a name="transfer-order-shipping-process"></a>Siirtotilauksen lähetysprosessi

Kun olet valinnut siirtotilausasiakirjan **Aktiivinen**-välilehdessä, voit valita **Tilauksen tiedot** ja aloittaa täyttämisprosessin. Näyttöön tulee **Täydellinen tilausluettelo** -näkymä. Tällä sivulla näkyvät kaikki nimikkeen sisältämät asiakirjarivit. Sivulla näkyvät myös tilatun määrän tiedot.

Jokainen viivakoodin skannaus päivittää määrän **Lähetys nyt** -kentässä yhdellä yksiköllä. Vaihtoehtoisesti voit syöttää lähetysmäärän valitsemalla **Lähetä tuote** sovelluspalkissa, syöttämällä nimikkeen tunnuksen ja syöttämällä sitten määrän. Jos nimike on sijaintiohjattu, voit vahvistaa tai määrittää asiakirjarivin lähetyssijainnin.

**Täydellinen tilausluettelo** -näkymässä voit manuaalisesti valita rivin luettelosta ja päivittää sitten **Lähetys nyt** -määrän valitulle riville **Tiedot**-ruudussa.

### <a name="over-delivery-shipping-validations"></a>Ylitoimituksen lähetyksen tarkistukset

Tarkistukset tapahtuvat asiakirjarivien vastaanottoprosessin aikana. Ne sisältävät ylitoimituksen tarkistukset. Jos käyttäjä yrittää vastaanottaa enemmän varastoa kuin ostotilauksen mukaan on tilattu, mutta ylitoimitusta ei ole määritetty tai vastaanotettu määrä ylittää ostotilausrivillä määritetyn ylitoimitustoleranssin, käyttäjä vastaanottaa virheen, koska ylimääräistä määrää ei voi vastaanottaa.

### <a name="underdelivery-close-lines"></a>Alitoimituksen sulkemisrivit

Commerce-versioon 10.0.12 lisättiin toimintoja, joilla myyntipisteen käyttäjät voivat sulkea tai peruuttaa jäljellä olevat määrät lähtevän tilauksen lähetyksessä, jos lähtevä varasto määrittää, ettei se voi lähettää koko pyydettyä määrää. Määrät voidaan sulkea tai peruuttaa myös myöhemmin. Tämän ominaisuuden käyttäminen edellyttää, että yritys on määritettävä sallimaan siirtotilausten alitoimitus. Lisäksi siirtotilausriville on määritettävä alitoimitusprosentti.

Yritys voidaan määrittää sallimaan siirtotilausten alitoimitus valitsemalla Commercen pääkonttorisovelluksessa **Varastonhallinta \> Asetukset \> Varasto ja varastonhallinnan parametrit**. Ota **Varasto ja varastonhallinnan parametrit** -sivun **Siirtotilaukset**-välilehdessä käyttöön **Hyväksy alitoimitus** -parametri. Synkronoi sitten parametrimuutokset myymäläkanavaa suorittamalla jakelun ajastustyö **1070**.

Siirtotilausrivin alitoimitusprosentti voidaan määrittää tuotteissa ennalta tuotteen määrityksen osana Commerce Headquartersissa. Vaihtoehtoisesti ne voidaan määrittää tai korvata tietyllä siirtotilausrivillä Commercen pääkonttorisovelluksessa.

Kun organisaatio on määrittänyt siirtotilauksen alitoimituksen, myyntipisteen käyttäjät näkevät **Sulje jäljellä oleva määrä** -vaihtoehdon **Tiedot**-ruudussa, kun he valitsevat lähtevän siirtotilausrivin **Lähtevä toiminto** -toiminnon. Kun käyttäjä viimeistee lähetyksen **Viimeistele täyttäminen** -toiminnon, he voivat sitten lähettää Commercen pääkonttorisovellukseen jäljellä olevan lähettämättömän määrän peruutuspyynnön. Jos käyttäjä sulkee jäljellä olevan määrän, Commerce suorittaa vahvistuksen ja tarkistaa, että peruutettava määrä on siirtotilausrivillä määritetyn alitoimitusprosentin toleranssin mukainen. Jos alitoimituksen toleranssi ylittyy, käyttäjä saa virhesanoman eikä voi sulkea jäljellä olevaa määrää, ennen kuin aiemmin lähetetty ja nyt lähetettävä määrä on alitoimituksen toleranssin mukainen tai sitä suurempi.

Kun lähetys on synkronoitu Commercen pääkonttorisovellukseen, myyntipisteessä siirtotilausrivin **Lähetä nyt** -kentässä määritetyt määrät päivitetään Commercen pääkonttorisovelluksessa lähetettyyn tilaan. Kaikkia lähettämättömiä määriä, joita olisi aiemmin pidetty lähetettävänä jäljellä olevana määränä (eli myöhemmin lähetettävänä määränä), pidetään sen sijaan peruutettuina määrinä. Siirtotilausrivin lähetettävän jäljellä olevan määrän arvo on **0** (nolla), ja rivi katsotaan kokonaisuudessaan lähetetyksi.

### <a name="shipping-location-controlled-items"></a>Lähetyksen sijaintiohjatut nimikkeet

Jos lähetettävät nimikkeet ovat sijaintiohjattuja, käyttäjät voivat valita sijainnin, josta he haluavat ottaa varaston lähetysprosessin aikana. Myymälän varastolle kannattaa määrittää oletusvarasto-ottosijainti. Tällöin prosessi on aiempaa tehokkaampi. Vaikka oletusvarasto-ottosijainti olisi määritetty, käyttäjät voivat korvata sen halutessaan valituilla riveillä.

Toiminto noudattaa **Tyhjä vastaanotto sallitaan** -määritystä **sijainnin** varastodimensiossa. Sijainnin dimensiota ei tarvitse syöttää, jos tyhjä vastaanotto on määritetty. Jos tyhjät vastaanottosijainnit eivät ole sallittuja nimikkeelle, myyntipistesovellus näyttää virheen ja vaatii sijainnin syöttämisen ennen vastaanoton kirjaamista.

### <a name="ship-all"></a>Lähetä kaikki

Voit halutessasi valita **Lähetä kaikki** sovelluspalkissa ja päivittää kaikkien asiakirjarivien **Lähetä nyt** -määrän nopeasti enimmäisarvoksi, joka on täytettävissä näille riveille.

### <a name="cancel-fulfillment"></a>Peruuta toimitus

Käytä **Peruuta täyttäminen** -toiminto sovelluspalkissa vain, jos haluat peruuttaa asiakirjan, etkä halua tallentaa muutoksia. Tee niin esimerkiksi silloin, kun valitsit alussa väärän asiakirjan, etkä halua tallentaa aiempia lähetystietoja.

### <a name="pause-fulfillment"></a>Keskeytä toimitus

Jos olet täyttämässä siirtotilausta, voit käyttää **Keskeytä täyttäminen** -toimintoa ja keskeyttää prosessin. Voit esimerkiksi haluta suorittaa myyntipisteessä toisen toiminnon, kuten soittaa asiakasmyyntiin, tai tehdä lähetyksen kirjauksen Commercen pääkonttorisovellukseen myöhemmin.

Kun valitset **Keskeytä täyttäminen** -vaihtoehdon, asiakirjan tilaksi muutetaan **Keskeytetty**. Näin käyttäjä tietää, mitä tietoja asiakirjaan on syötetty ja että asiakirjaa ei ole vielä vahvistettu. Kun olet valmis jatkamaan täyttämisprosessia, valitse keskeytetty asiakirja ja valitse sitten **Tilauksen tiedot**. Kaikki aiemmin tallennetut **Lähetys nyt** -määrät säilytetään. Ne näkyvät **Täydellinen tilausluettelo** -näkymässä.

### <a name="review"></a>Tarkista

Ennen lopullista sitoutumista Commercen pääkonttorisovellukseen toimituksesta, voit käyttää **Tarkista**-toimintoa ja vahvistaa lähtevän asiakirjan. Tämä toiminto kertoo mahdollisista puuttuvista tai virheellisistä tiedoista, jotka saattavat aiheuttaa käsittelyvirheen, sekä antaa mahdollisuuden korjata ongelmia ennen täydennyspyynnön lähettämistä. Jos haluat ottaa käyttöön **Tarkista**-toiminnon sovelluspalkissa, ota käyttöön **Ota käyttöön vahvistus myyntipisteen saapuvissa ja lähtevissä varastotoiminnoissa** -ominaisuus ominaisuuksien hallinnassa Commercen pääkonttorisovelluksessa.

**Tarkista**-toiminto vahvistaa seuraavat ongelmat lähtevässä asiakirjassa:
- **Ylilähetys** - lähetyksen määrä on suurempi kuin tilattu määrä. Commercen pääkonttorisovelluksen ylitoimituksen määritys määrittää tämän ongelman vakavuuden.
- **Alilähetys** - lähetyksen määrä on pienempi kuin tilattu määrä. Commercen pääkonttorisovelluksen alitoimituksen määritys määrittää tämän ongelman vakavuuden.
- **Sarjanumero** – sarjanumeroa ei ole annettu tai se ei ole käytettävissä sarjoitetulle nimikkeelle, joka vaatii sarjanumeron rekisteröimisen varastossa.
- **Sijaintia ei ole määritetty** – sijaintia ei ole määritetty sijaintiohjatulle nimikkeelle, jossa sijainti ei saa olla tyhjä.
- **Poistetut rivit** – Commercen pääkonttorisovelluksen käyttäjä, joka myyntipistesovellus ei tunne, on poistanut tilauksen rivejä.

Jos määrität **Ota käyttöön automaattinen vahvistus** -parametrin arvoksi **Kyllä** kohdassa **Commerce-parametrit** > **Varasto** > **Myymälän varastotoiminnot**, vahvistus tehdään automaattisesti, kun valitset **Viimeistele toimitus** -toiminnon.

### <a name="finish-fulfillment"></a>Viimeistele toimitus

Kun olet syöttänyt kaikki **Lähetä nyt** -määrät tuotteille, valitse sovelluspalkissa **Tee täyttäminen valmiiksi**.

Kun käytetään asynkronista asiakirjojen käsittelyä, kuitti lähetetään asynkronisen asiakirjakehyksen kautta. Asiakirjan kirjaamiseen kuluva aika riippuu asiakirjan koosta (rivien määrä) ja palvelimella tapahtuvasta yleisen tietoliikenteen määrästä. Yleensä tämä prosessi tapahtuu muutamassa sekunnissa. Jos asiakirjan kirjaaminen epäonnistuu, käyttäjälle lähetetään ilmoitus **Lähtevä toiminto** -asiakirjaluettelon kautta **Aktiivinen**-välilehdessä. Siellä asiakirjan tilaksi päivitetään **Käsittely epäonnistui**. Käyttäjä voi sitten valita epäonnistuneen asiakirjan myyntipisteessä ja tarkastella virhesanomaa ja virheen syytä **Tiedot**-ruudussa. Epäonnistunut asiakirja säilyy kirjaamattomana. Käyttäjän on palattava asiakirjariveille valitsemalla **Tilauksen tiedot** myyntipisteessä. Käyttäjän on tämän jälkeen päivitettävä asiakirjaan korjaukset virheiden perusteella. Kun asiakirja on korjattu, käyttäjä voi yrittää sen käsittelyä uudelleen valitsemalla **Tee täyttäminen valmiiksi** sovelluspalkissa.

## <a name="create-an-outbound-transfer-order"></a>Lähtevän siirtotilauksen luominen

Käyttäjät voivat luoda myyntipisteessä uusia siirtotilausasiakirjoja. Aloita prosessi valitsemalla **Uusi** sovelluspalkissa, kun olet **Lähtevä toiminto** -pääasiakirjaluettelossa. Tämän jälkeen sinua pyydetään valitsemaan **Siirron kohde** -varasto, tai myymälä, johon nykyinen myymälä lähettää varaston. Mahdollisia arvoja ovat myymälän täyttämisryhmän kokoonpanossa määritetyt arvot. Nykyinen myymälä on aina lähtevän siirtopyynnön **Siirron lähde** -varasto siirtotilauksessa. Arvoa ei voi muuttaa.

Voit syöttää arvot **Lähetyspäivä**-, **Vastaanottopäivä**- ja **Toimitustapa** -kenttiin haluamallasi tavalla. Voit myös lisätä muistiinpanon, joka tallennetaan yhdessä siirtotilauksen otsikon kanssa liitteenä asiakirjaan Commercen pääkonttorisovelluksessa.

Kun otsikon tiedot on luotu, voit lisätä siirtotilaukseen tuotteita. Aloita nimikkeiden ja pyydettyjen määrien lisääminen skannaamalla viivakoodit tai valitsemalla **Lisää tuote**.

Kun lähtevän siirtotilauksen rivit on syötetty, valitse **Tallenna** ja tallenna asiakirjan muutokset paikallisesti tai valitse **Lähetä pyyntö** ja lähetä tilauksen tiedot Commercen pääkonttorisovellukseen lisäkäsittelyä varten. Jos valitset **Tallenna**, oletusasiakirja tallennetaan kanavan tietokantaan. Lähtevä varasto voi suorittaa asiakirjan vasta, kun se on käsitelty onnistuneesti **Lähetä pyyntö** -kohdassa. Valitse **Tallenna** vain, jos et ole valmis vahvistamaan pyyntöä Commercen pääkonttorisovelluksessa käsittelyä varten.

Jos asiakirja tallennetaan paikallisesti, se löytyy **Luonnokset**-välilehdestä **Saapuva toiminto** -asiakirjaluettelosta. Kun asiakirjan tila on **Luonnos**, voit muokata sitä valitsemalla **Muokkaa**. Voit päivittää, lisätä tai poistaa rivejä tarvittaessa. Voit myös poistaa koko asiakirjan, kun sen tila on **Luonnos**, valitsemalla **Poista** **Luonnokset**-välilehdessä.

Kun luonnosasiakirjan lähettäminen Commercen pääkonttorisovellukseen onnistuu, se näkyy **Aktiivinen**-välilehdessä ja sen tila on **Pyydetty**. Tässä vaiheessa vain lähtevän varaston käyttäjät voivat muokata asiakirjaa valitsemalla myyntipisteessä **Lähtevä toiminto** -kohdan. Saapuvan varaston käyttäjät voivat tarkastella siirtotilausta **Aktiivinen**-välilehdessä **Saapuva toiminto** -asiakirjaluettelossa, mutta he eivät voi muokata tai poistaa sitä. Muokkauksen lukituksen avulla voidaan välttää ristiriidat, koska saapuva pyytäjä muuttaa siirtotilausta samalla kuin lähtevien huolitsija keräilee ja lähettää tilausta aktiivisesti. Jos saapuvasta myymälästä tai varastosta on saatava muutoksia siirtotilauksen lähettämisen jälkeen, lähtevien huolitsijaan on otettava yhteyttä ja pyydettävä muutosten käyttöönottoa.

Kun asiakirjan tila on **Pyydetty**, se on valmis lähtevän varaston täyttämiskäsittelyä varten. Kun lähetystä käsitellään käyttämällä lähtevää toimintoa, siirtotilausasiakirjojen tila päivitetään **Pyydetty**-tilasta **Kokonaan lähetetty**- tai **Osittain lähetetty** -tilaksi. Kun asiakirjojen tila on **Kokonaan lähetetty** tai **Osittain lähetetty**, saapuva myymälä tai varasto voi kirjata vastanotot niiden avulla käyttämällä saapuvan toiminnon vastaanottoprosessia.

Kokonaan lähetetyt siirtotilaukset siirretään **Valmis**-välilehteen **Lähtevä toiminto** -asiakirjaluettelossa. Ne näkyvät siellä lähtevän myymälän tai varaston käyttäjille vain luku -tilassa seitsemän päivän ajan.

## <a name="related-topics"></a>Liittyvät aiheet

[Myyntipisteen saapuva varastotoiminto](pos-inbound-inventory-operation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]