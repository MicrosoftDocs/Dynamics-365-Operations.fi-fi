---
title: "Tarjouspyynnöt"
description: "Tässä aiheessa on tarjouspyyntöjen yleiskuvaus. Organisaatiot tekevät tarjouspyyntöjä, kun ne haluavat ostaa tarvitsemiaan nimikkeitä tai palveluita ja haluavat saada kilpailukykyisiä tarjouksia useilta toimittajilta."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: 42ab7beb8a269cd37fd9100385bd302e4945c1e0
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---

# <a name="requests-for-quotation-rfqs"></a>Tarjouspyynnöt

[!include[banner](../includes/banner.md)]

Tässä aiheessa on tarjouspyyntöjen yleiskuvaus. Organisaatiot tekevät tarjouspyyntöjä, kun ne haluavat ostaa tarvitsemiaan nimikkeitä tai palveluita ja haluavat saada kilpailukykyisiä tarjouksia useilta toimittajilta. Tarjouspyynnössä pyydät toimittajilta hinnat ja toimitusaikoja nimikkeiden määrille, jotka määrität. Voit myös pyytää toimittajia määrittämään, liittyykö tarjoukseen satunnaisia kuluja, esimerkiksi lähetyskustannuksia, tai tarjoaako toimittaja alennuksia suurista tilauksista tai toimittajalaskun maksamisesta aikaisin.

Tarjouspyyntöprosessi muodostuu seuraavista tehtävistä:

1. Tarjouspyynnön luominen ja lähettäminen vähintään yhdelle toimittajalle.
2. Tarjouspyyntövastausten (tarjousten) vastaanottaminen ja rekisteröiminen.
3. Hyväksyttyjen tarjousten siirtäminen ostotilaukseen, ostosopimukseen tai ostoehdotukseen.

Seuraavassa kuvassa on yhteenveto tarjouspyyntöprosessista.

[![Tarjouspyyntöprosessi](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

Voit luoda tarjouspyynnön suunnitelluista tilauksista, ostoehdotuksesta tai manuaalisesta kirjauksesta. Luotua tarjouspyyntöä kutsutaan tarjouspyyntötapaukseksi. Tarjouspyyntötapaus on perusasiakirja, jonka perusteella tarjouspyyntö tehdään kullekin toimittajalle.

Kun olet valmistellut tarjouspyyntötapauksen ja lisännyt toimittajia, valitse **Lähetä** tarjouspyyntötapauksessa. Tarjouspyynnön kirjauskansio luodaan jokaiselle toimittajalle, jolle lähetät tarjouspyynnön. Voit määrittää Lähetä-toiminnon tulostuksenhallinta-asetukset joko tulostamaan raportin jokaisesta toimittajasta arkistoon vai lähettämään raportin kunkin toimittajan sähköpostiosoitteeseen. Voit lisäksi luoda kunkin toimittajan tarjouspyynnön kirjauskansiossa raportin, jonka voit lähettää toimittajalle tai lähettää sen myöhemmin uudelleen. Voit myös määrittää Lähetä-toiminnon luomaan vastauslomakkeen, jonka toimittaja voi täyttää.

Tässä aiheessa käsitellään tarjouspyyntöjen käsittelyprosessi silloin, kun toimittajayhteistyö ei ole käytössä. Jos järjestelmään on määritetty toimittajayhteistyö, toimittajat voivat antaa tarjouksia suoraan Microsoft Dynamics 365 for Finance and Operations, Enterprise editionissa. Lisätietoja on kohdassa [Toimittajayhteistyö asiakkaiden kanssa](vendor-collaboration-work-customers-dynamics-365-operations.md)
 
Jos tarjouspyyntöä on muutettava lähettämisen jälkeen, voit lähettää tarjouspyynnön uudelleen toimittajille, kun olet käyttänyt kahta muutostoimintoa: luontia ja viimeistelyä.

Kun vastaanotetut tarjouksia sähköpostitse, ne on kirjattava **Tarjouspyynnön vastaukset** -sivulla. Jos valitset **Kopioi tiedot vastaukseen** -vaihtoehdon, vastaukseen kopioidaan tarjouspyyntötapauksesta tietyt tiedot, kuten määrä ja päivämäärät. Voit muuttaa nämä tiedot toimittajan tarjousta vastaavasti.

Jos tietylle toimittajalle tarvitaan vastauksen toinen iteraatio, valitse **Tarjouspyynnön vastaus** -sivulla **Palauta**. Palautustoiminto luo uuden kirjauskansion ja raportin, joka tulostetaan, arkistoidaan ja lähetetään tulostuksenhallinta-asetusten mukaisesti.

Jos olet lisännyt tarjouspyyntötapahtumaan pisteytysehtoja, tarjouspyyntövastauksessa on pisteytyspaneeli, johon voit lisätä pisteet. Kokonaispisteytys on näkyvissä, kun vertailet vastauksia **Vertaa vastauksia** -sivulla. Voit verrata tällä sivulla myös muita vastaustietoja, kuten rivihintaa, toimituspäivämäärää ja kokonaishintaa.

Kun olet valinnut jonkin tarjouksen tai osittaisia tarjouksia, voit hyväksyä ne ja hylätä muut. Luotavat hyväksymiskirjauskansiot, hylkäämiskirjauskansiot ja vastaavat raportit tulostetaan, arkistoidaan ja lähetetään tulostuksenhallinta-asetusten mukaisesti. Kun hyväksyt tarjouksen tai tietyt tarjouksen rivit, järjestelmä luo joko ostosopimuksen tai ostotilauksen tai päivittää ostoehdotuksen tarjouspyynnön ostotyypin mukaan. Voit luoda haluamistasi vastauksista kauppasopimuksen käytettäväksi myöhemmin huolimatta siitä, oletko hyväksynyt tai hylännyt kyseiset vastaukset.

Tarjouspyynnön tila näkyy sen otsikossa, ja se määräytyy tarjouspyynnön rivien tilan mukaan. Tila ilmaisee, kuinka paljon tarjouspyyntöä on käsitelty. Jokaisen tarjouspyynnön tilalla on kaksi arvoa: alhaisin ja korkein tila. Alin tila on minkä tahansa tarjouspyynnön rivin vähiten edistynyt vaihe, ja korkein tila on minkä tahansa tarjouspyynnön rivin kaikkein edistynein vaihe. Jos esimerkiksi tarjouspyynnön vähiten edennyt vaihe koskee luotua riviä, tarjouspyynnön alin tila on **Luotu**. Jos tarjouspyynnön eniten edennyt vaihe koskee toimittajille lähetettyä riviä, tarjouspyynnön korkein tila on **Lähetetty**. Tilat päivitetään automaattisesti, kun tarjouspyynnön.

Voit tarkastella tarjouspyynnön otsikon alinta ja ylintä tilaa **Kaikki tarjouspyynnöt** -sivulla. Voit tarkastella tarjouspyynnön rivin alinta ja ylintä tilaa **Tarjouspyynnöt** -sivulla **Rivit**-välilehdessä.

Tarjouspyyntöjen tilat käsitellään seuraavassa järjestyksessä:

1. **Luotu**
2. **Lähetetty**
3. **Vastaanotettu**
4. **Hyväksytty**, **Peruutettu** tai **Hylätty**

Näitä tiloja käsitellään tarkemmin jäljempänä tässä aiheessa.

## <a name="setting-up-rfq-functionality"></a>Tarjouspyyntötoimintojen asetukset

Ennen tarjouspyyntötapauksen luomista sinun täytyy määrittää tarjouspyynnön tiedot **Hankintaparametrit**-sivulla. Tarjouspyyntötapausta luodessasi voit määrittää oletusarvot, jotka kopioidaan tarjouspyyntöön. Voit määrittää seuraavat oletusarvot:

- Uusien tarjouspyyntöjen ostotyyppi: **Ostotilaus** tai **Ostosopimus**
- Vanhentumispäivämäärä ja -aika
- Toimitustiedot ja maksuehdot
- Tarjouspyynnön vastaukseen sisällytettävät kentät

Nämä arvot voi ohittaa tietyissä tarjouspyyntötapauksissa.

Myös muutosprosessi täytyy määrittää. Tämän määrityksen yhteydessä voit ottaa käyttöön kentän lukituksen. Kun kentän lukitus on käytössä ja hankinta-asiantuntija haluaa tehdä tarjouspyyntöön muutoksia, hänen on ensin valittava **Tarjous**-välilehden **Muutos**-osassa **Luo**. Kun tarjouspyyntö on päivitetty muutoksen avulla, hankinta-asiantuntijan on viimeisteltävä prosessi valitsemalla **Viimeistele**. Viimeistelytoiminto luo sähköpostiviestin, joka ilmoittaa toimittajille tarjouspyynnön muutoksesta.

Valitse **Hankintaparametrit**-sivulla toimittajille lähetettävän sähköposti-ilmoituksen malli. Luotava malli voi sisältää seuraavia korvattavia tunnisteita:

- %Tarjouspyyntötapaus%
- %Tarjouksen palautuksen syy%
- %Muutoksen syy%
- %Muutoksen valmistelija%
- %Yritys%
- %Tarjouspyyntötapauksen nimi%
- %ExpiryDateTime%
- %Päivämäärä%

%Tarjouksen palautuksen syy%- ja %Muutoksen syy% -tunnisteet korvataan tekstillä, jonka hankinta-asiantuntija voi täyttää viimeistellessään muutoksia ohjatussa **Muutos**-toiminnossa. %Muutoksen valmistelija%- ja %Yritys%-tunnisteet korvataan automaattisesti tarjouspyynnön tiedoilla. %Päivämäärä%-tunniste korvataan nykyisellä päivämäärällä.

Sähköpostimallia tarvitaan myös, jos peruutat lähetetyn tarjouspyynnön. Tätä sähköpostimallia käytetään lähetettäessä peruutusilmoitus toimittajan yhteyshenkilöille. Malli on oltava valittuna **Hankintaparametrit**-sivulla. Luotava malli voi sisältää seuraavat korvattavat tunnisteet:

- %Peruutuksen syys%
- %Tarjouspyyntötapaus% 
- %Tarjouspyynnön peruuttaja%
- %Yritys%
- %Tarjouspyyntötapauksen nimi%
- %Päivämäärä%

%Peruutuksen syy% -tunniste korvataan tekstillä, jonka hankinta-asiantuntija voi antaa ohjatussa **Peruutus**-toiminnossa. %Päivämäärä%-tunniste korvataan nykyisellä päivämäärällä.

Jos haluat osoittaa tarjouspyynnön vastauksessa tarjouksen hylkäämisen tai hyväksymisen syyn syykoodeilla, määritä syykoodit **Toimittajan syyt** -sivulla.

Voit määrittää hankinnan **Lomakeasetukset**-sivulla tulostettujen tai tallennettujen tarjouspyyntöasiakirjojen ulkoasun.

> [!NOTE]
> Julkisen sektorin määrityksessä jo lähetettyyn tarjouspyyntöön tehdyt muutokset edellyttävät muutosprosessin käyttöä. Kun tarjouspyyntö on lähetetty, kentät lukitaan. Niinpä tarjouspyyntöön tehtävät muutokset edellyttävät edellä kuvatun muutosprosessin aloittamista valitsemalla **Luo**. Lukitustoimintaa ohjataan **Hankintaparametrit**-sivun **Lukitse tarjouspyynnöt, kun ne on lähetetty** -asetuksella. Parametrin arvoksi määritetään oletusarvoisesti **Kyllä**. Julkisen sektorin määrityksissä tämä on oletusasetus, jota ei voi muuttaa. Vaikka muutosprosessia voidaankin käsitellä manuaalisesti muissa kuin julkisen sektorin määrityksissä, sitä on käytettävä julkisen sektorin määrityksissä.

Kun luot ostotilaukselle tarjouspyynnön ja lisäät tarjouspyyntöön varastonimikkeen, luodaan varastotapahtuma, jossa vastaanoton tila on **Tarjouksen vastaanotto**. Vain tarjouspyyntörivit, joilla on tämä tila, otetaan huomioon, kun lasket toimituksia pääsuunnitelmaa käyttämällä. Jos haluat, että pääsuunnitelma sisältää tarjouspyynnön rivejä odotettuna vastaanottona, tämä on määritettävä pääsuunnittelun asetuksissa.

Ostopäällikkö tai edustaja voi luoda ja ylläpitää pyyntötyyppejä, jotka vastaavat organisaation hankintavaatimuksia. Kukin pyyntötyyppi voidaan liittää pisteytystapaan. Pisteytysmenetelmät koostuvat ehdoista, joita voi käyttää tarjouksia pisteytettäessä. Pyyntötyypit, pisteytysmenetelmät ja pisteytysehdot määritellään **Pyyntötyyppi**- ja **Pisteytystapa**-sivuilla.

## <a name="creating-and-sending-an-rfq"></a>Tarjouspyynnön luominen ja lähettäminen

Voit luoda tarjouspyynnön ja valita toimittajat, joiden haluat lähettävän tarjouksia, ja lähettää sitten tarjouspyynnön toimittajille. Voit lähettää tarjouspyyntöraportin ja vastauslomakeraportit tulostuksenhallinnan avulla ensisijaiseen sijaintiisi.

Voit luoda tarjouspyynnön joko **Ostotilaus**- tai **Ostosopimus**-ostotyypeille.

Jos tarjouspyynnön tyyppi on **Ostotilaus**, toimitaan seuraavasti:

- Kun tarjouspyynnön rivejä luodaan, järjestelmä luo varastotapahtumia, joiden vastaanottotila on **Tarjouksen vastaanotto**.
- Kun hyväksyt tarjouksen, ostotilaus luodaan.

Jos tarjouspyynnön tyyppi on **Ostosopimus**, toimitaan seuraavasti:

- Tarjouspyyntöä käytetään sopimuksessa, kun tuotetta halutaan ostaa tietty määrä tai arvo tiettynä aikana. Valitse tällöin ostosopimusta koskeva päivämääräalue ja ostosopimusta hallinnoivan henkilön nimi.
- Kun hyväksyt tarjouksen, ostosopimus luodaan.

Jos tarjouspyyntö luodaan ostoehdotuksesta, **Ostoehdotus**-tyyppi määritetään automaattisesti. Tarjouspyyntöä, jonka tyyppi on **Ostoehdotus**, ei voi luoda manuaalisesti.

Voit luoda tarjouspyynnön ostoehdotuksesta vain, jos ostoehdotuksen tila on **Tarkistuksessa** ja sinut on määritetty suorittamaan seuraava työnkulkutehtävä. Ostoehdotuksen rivit päivittyvät automaattisesti, kun hyväksyt toimittajilta saamiasi tarjouspyynnön vastauksia (tarjouksia). Ostoehdotukselle ei voi suorittaa loppuun, hylätä, hyväksyä tai suorittaa mitään muita toimintoja tarjouspyynnön ollessa kesken.

Kun luot tarjouspyynnön, voit valita pyyntötyypin. Pyyntötyyppi määrittää pisteytysehdot, joilla tarjouspyynnön vastauksia pisteytetään.

Voit lisätä tarjouspyyntötapaukseen kyselylomakkeen. Kyselylomake näkyy tämän jälkeen kaikissa vastauksissa, kun tarjouspyyntö on lähetetty.

Tarjouspyyntötapahtumaan lisättäviä toimittajia voi valita kolmella tavalla:

- Voit lisätä toimittajia yksitellen.
- Voit hakea kaikkia toimittajia, jotka täyttävät tietyt ehdot.
- Voit lisätä automaattisesti kaikki toimittajat, jotka on hyväksytty tarjouspyynnön riveillä käytettyihin hankintaluokkiin.

Kun tarjouspyyntötapaus on valmis, valitse **Lähetä**. Lähetystoiminto luo kirjauskansiot ja raportit, jotka tulostetaan, arkistoidaan ja lähetetään tulostuksenhallinta-asetusten mukaisesti.

Jos valitset **Käytä toimittajaa hintojen uudelleenlaskemiseen**- ja **Käytä toimittajakohtaisia nimiketietoja** -asetukseksi **Kyllä** **Lähetetään tarjouspyyntöä** -sivulla, kun lähetät tarjouspyynnön toimittajille, jotkin toimittajakohtaiset tiedot täytetään automaattisesti. Voit muokata näitä tietoja **Tarjouspyynnön vastaus** -sivulla.

Seuraavassa taulukossa näkyvät tarjouspyynnön tilan muutokset, kun luot tarjouspyynnön ja lähetät sen toimittajille.

| Toimi                             | Alhaisin tarjouspyyntöotsikon tila | Suurimman tarjouspyyntöotsikon tila on                        | Alhaisin tarjouspyyntörivin tila | Ylimmän tarjouspyynnön tila |
|------------------------------------|--------------------------|--------------------------------------------------|------------------------|-------------------------|
| Luo tarjouspyynnön otsikko ja rivi.    | Luotu                  | Luotu                                          | Luotu                | Luotu |
| Lähetä tietylle toimittajalle Tarjouspyyntö. | Lähetetty                     | Lähetetty                                             | Lähetetty                   | Lähetetty |
| Lisää toinen toimittaja.                | Luotu                  | Lähetetty (Tarjouspyyntö on lähetetty vain yhdelle toimittajalle.) | Luotu                | Lähetetty |
| Lähetä tarjouspyyntö toiselle toimittajalle. | Lähetetty                     | Lähetetty                                             | Lähetetty                   | Lähetetty |

> [!NOTE]
> Voit lisätä toimittajia tarjouspyyntöön milloin tahansa, ja alimmat ja ylimmät tilat päivitetään uusien toimittajien mukaan. Jos esimerkiksi sait tarjoukset kaikilta toimittajilta ja hyväksyit vähintään yhden tarjousrivin, tarjouspyynnön otsikon alin tila on **Hylätty** ja ylin tila on **Hyväksytty**. Jos lisäät uuden toimittajan, minkä tahansa rivin alin tila on nyt **Luotu**. Tämän vuoksi tarjouspyynnön otsikon alin tila päivitetään tilaksi **Luotu**, mutta ylimmän tila on edelleen **Hyväksytty**.

## <a name="amending-an-rfq"></a>Tarjouspyynnön muuttaminen

Tarjouspyyntöä voi joutua muuttamaan vielä senkin jälkeen, kun se on lähetetty. Tarjouspyyntöä on muutettava ehkä siksi, että toimituspäivämäärät ovat muuttuneet tai tuotteita tarvitaan lisää tai eri määrinä. Voit määrittää muutosprosessin rajoittavammaksi tai joustavammaksi.

Jos määrität muutosprosessin rajoittavammaksi, aloita muutos valitsemalla tarjouspyyntötapauksessa **Luo** ennen lähetetyn tarjouspyyntötapauksen kenttien muokkaamista. Kun olet tehnyt haluamasi muutokset, valitse **Viimeistele**. Tämän jälkeen saat ohjeet tietojen lisäämisestä sähköpostiviestiin, jolla muutoksesta ilmoitetaan toimittajille. Viestiin liitetään automaattisesti päivitetty tarjouspyyntöraportti, jossa on muutosta koskeva huomautus.

Jos määrität joustavan muutosprosessin, sinun ei tarvitse valita **Luo** ennen jo lähetetyn tarjouspyyntötapauksen kenttien muokkaamista. Muutoshuomautus on kuitenkin lisättävä tarjouspyyntöön manuaalisesti ja tapaus on lähetettävä uudelleen. Huomaa, että tätä menettelyä voi käyttää vain, jos yhtäkään vastausta (tarjousta) ei ole muokattu. Jos olet kirjannut vastauksen ja sen tila on **Vastaanotettu**, **Lähetä**-painike ei ole käytettävissä. Siinä tapauksessa sinun on valittava ensin **Luo** ja sitten **Viimeistele** samoin kuin rajoittavassa prosessissa. Vastaus palautetaan sitten vastaamaan tarjouspyyntötapauksen muutoksia. 

Jos toimittajat kirjaavat tarjoukset toimittajayhteistyöliittymässä, sinun on ilmoitettava tarjouspyyntötapauksen muutokset käyttämällä muutosprosessia. Tämä vaatimus auttaa estämään tilanteen, jossa toimittajat tekevät tarjouksen vanhentuneesta tarjouspyynnöstä, kun heidän tarjouksensa on kesken. Lisätietoja siitä toimittajayhteistyöstä on kohdassa [Toimittajayhteistyö ulkoisten toimittajien kanssa](vendor-collaboration-work-external-vendors.md). 

Jos haluat kutsua tarjouksia muilta toimittajilta eikä tarjouspyyntötapaukseen ole tehty muutoksia, voit käyttää **Lähetä**-painiketta. Lisäämäsi toimittajat näkyvät **Lähetä**-sivulla, ja he vastaanottavat sähköpostikutsun.

## <a name="receiving-and-registering-rfq-replies"></a>Tarjouspyyntövastausten vastaanottaminen ja rekisteröiminen

Kun lähetät tarjouspyynnön, ohjelma luo automaattisesti vastauslomakkeen. Kun saat vastauksia tarjouspyyntöön (eli tarjouksia), sinun täytyy syöttää kutakin toimittajaa koskevat tiedot toimittajakohtaiselle tarjouspyynnön vastauslomakkeelle. Jos olet lisännyt pisteytysehdot, voit pisteyttää vastaukset. Sen jälkeen voit vertailla toimittajien tarjouksia ja asettaa ne järjestykseen pisteytysehtojen mukaan, esimerkiksi parhaan kokonaishinnan tai toimitusajan perusteella.

Jos tarjouspyyntötapahtumaan on liitetty kyselylomake, kysymysten vastaukset on annettava manuaalisesti vastauslomakkeeseen.

Voit antaa myös vaihtoehtoisia rivejä, jos tarjouspyyntötapaus sallii vaihtoehtoiset rivit. Valitse **Ostotarjousrivit**-pikavälilehdessä **Lisää rivi**. Kirjoita sitten tuotteen tiedot, kuten nimikkeen numero tai hankintaluokka, määrä, hinta ja alennus.

Jos olet kirjoittanut vastauksen mutta vaadit toimittajalta uutta tarjousta, voit lähettää tarjouspyynnön uudelleen. Voit pyytää luotavalla uudella kirjauskansiolla ja raportilla muutoksia toimittajalta.

Kaikkien tarjouspyyntöjen ja niiden vastaustilojen yhteenveto on nähtävissä **Tarjouspyynnön seuranta** -sivulla.

Seuraavassa taulukossa näkyy, miten tarjouspyynnön tila muuttuu, kun vastaanotat tarjouksia ja rekisteröit tiedot tarjouspyynnön vastauslomakkeeseen.

| Toimenpide                                         | Alhaisimman tarjouksen tila | Ylin tarjoustila | Alhaisin tarjouspyyntöotsikon tila | Suurimman tarjouspyyntöotsikon tila on | Alhaisin tarjouspyyntörivin tila | Ylimmän tarjouspyynnön tila |
|------------------------------------------------|-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Rekisteröi yhden toimittajan tarjous ja tallenna se.        | Lähetetty              | Vastaanotettu           | Lähetetty                     | Vastaanotettu                  | Lähetetty                   | Vastaanotettu |
| Rekisteröi toisen toimittajan tarjous ja tallenna se. | Vastaanotettu          | Vastaanotettu           | Vastaanotettu                 | Vastaanotettu                  | Vastaanotettu               | Vastaanotettu |

> [!NOTE]
> Jos palautat tarjouksen toimittajalle lisäneuvotteluja varten, alin ja ylin tila on edelleen **Vastaanotettu**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Tarjousten hyväksyminen ja hylkääminen sekä hyväksyttyjen tarjousten siirtäminen alatason asiakirjoihin

Kun olet löytänyt parhaan tarjouksen, esimerkiksi sellaisen, jonka kokonaishinta on paras, voit hyväksyä sen. Voit hyväksyä joitakin tarjouksen rivejä ja hylätä muut. Voit myös hyväksyä rivejä eri toimittajilta. Huomaa, että jos hyväksyt joitakin rivejä, sinua pyydetään hylkäämään kaikki muut rivit. Jos siis haluat hyväksyä muitakin rivejä, valitse kysyttäessä **Peruuta**. Kunkin sellaisen toimittajan tarjouspyynnön vastauksen tilaksi, jonka tarjouksia tai rivejä hyväksyt, päivitetään **Hyväksytty**. 

Kun hyväksyt tarjouksen tai sen tietyt rivit, ostotilaus tai -sopimus luodaan automaattisesti. Voit sitten hylätä muilta toimittajilta saadut tarjoukset.

Voit lisätä vastaukseen syykoodin, joka selittää, miksi tarjous on hyväksytty tai hylätty.

Kun hyväksyt tarjouspyynnön vastauksen, jonka tyyppi on **Ostoehdotus**, ostoehdotusriveille päivittyvät tarjouspyynnön vastausrivien perusteella seuraavat tiedot:

- Yksikköhinta
- Alennusprosentti
- Alennussumma
- Oston kulut
- Rivin kulut
- Toimittaja
- ulkoinen tunnus
- Ulkoinen kuvaus

Seuraavassa taulukossa näkyy, miten tarjouspyynnön tila muuttuu, kun hyväksyt ja hylkäät toimittajien tarjouksia.

| Toimenpide                      | Alin tarjoustila | Ylin tarjoustila | Alhaisin tarjouspyyntöotsikon tila | Suurimman tarjouspyyntöotsikon tila on | Alhaisin tarjouspyyntörivin tila | Ylimmän tarjouspyynnön tila |
|-------------------------    |-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Hyväksy yksi tarjouksista.     | Vastaanotettu          | Hyv.           | Vastaanotettu                 | Hyv.                  | Vastaanotettu               | Hyv. |
| Hylkää kaikki muut tarjoukset.  | Hylätty          | Hyv.           | Hylätty                 | Hyv.                  | Hylätty               | Hyväksytty |

