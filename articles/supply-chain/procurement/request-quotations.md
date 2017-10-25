---
title: "Tarjouspyynnöt"
description: "Tämä ohjeaihe sisältää yleistietoja tarjouspyynnöistä. Organisaatiot luovat tarjouspyyntöjä silloin, kun niiden on ostettava nimikkeitä tai palveluita, ja halutaan saada kilpailukykyisiä tarjouksia useilta toimittajilta."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8b817ffd905f1d3e99befc149416006e1a51f5e2
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="request-for-quotations-rfqs"></a>Tarjouspyynnöt

[!include[banner](../includes/banner.md)]


Tämä ohjeaihe sisältää yleistietoja tarjouspyynnöistä. Organisaatiot luovat tarjouspyyntöjä silloin, kun niiden on ostettava nimikkeitä tai palveluita, ja halutaan saada kilpailukykyisiä tarjouksia useilta toimittajilta. Tarjouspyynnössä pyydät toimittajilta hinnat ja toimitusaikoja nimikkeiden määrille, jotka määrität. Voit myös pyytää toimittajia määrittämään, liittyykö tarjoukseen satunnaisia kuluja, esimerkiksi lähetyskustannuksia, tai tarjoaako toimittaja alennuksia suurista tilauksista tai toimittajalaskun maksamisesta aikaisin.

Tarjouspyyntöprosessiin sisältyvät seuraavat tehtävät:

-   Tarjouspyynnön luominen ja lähettäminen yhdelle tai useammalle toimittajalle.
-   Tarjouspyyntövastausten (tarjousten) vastaanottaminen ja rekisteröiminen.
-   Hyväksyttyjen tarjousten siirtäminen ostotilaukseen, ostosopimukseen tai ostoehdotukseen.

Seuraavassa kuvassa on yhteenveto tarjouspyyntöprosessista.  

[![Tarjouspyyntöprosessi](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)  

Tarjouspyynnön voi luoda suunnitelluista tilauksista, ostoehdotuksesta tai manuaalisesta kirjauksesta. Luotavaa tarjouspyyntöä kutsutaan tarjouspyyntötapaukseksi, ja se on perusasiakirja, jolla tarjouspyyntö lähetetään kullekin toimittajalle. Kun olet laatinut tarjouspyyntötapauksen ja lisännyt toimittajat, valitse tarjouspyyntötapahtumassa **Lähetä**, niin tarjouspyynnön kirjauskansio luodaan kullekin toimittajalle, jolle tarjouspyyntö on lähetetty. Voit määrittää Lähetä-toiminnon tulostuksenhallinta-asetukset sen mukaan, haluatko tulostaa kustakin toimittajasta raportin arkistoon vai lähettää raportin kunkin toimittajan sähköpostiosoitteeseen. Lisäksi voit luoda kunkin toimittajan tarjouspyynnön kirjauskansiossa raportin, jonka voit lähettää toimittajalle myöhemmin tai uudelleen. Voit myös määrittää Lähetä-toiminnon luomaan vastauslomakkeen, jonka toimittaja voi täyttää.  

Jos jo lähetettyä tarjouspyyntöä on muokattava, voit lähettää tarjouspyynnön toimittajille uudelleen tehtyäsi tarvittavat muutokset.  

Vastaanotetut tarjoukset on syötettävä **Tarjouspyynnön vastaukset** -sivulle. Jos valitset **Kopioi tiedot vastaukseen** -vaihtoehdon, vastaukseen kopioidaan tarjouspyyntötapauksesta tietyt tiedot, kuten määrä ja päivämäärät. Voit muuttaa nämä tiedot toimittajan tarjousta vastaavasti.  

Jos tietylle toimittajalle tarvitaan vastauksen toinen iteraatio, valitse **Tarjouspyynnön vastaus** -sivulta **Palauta**. Palautustoimenpide luo uuden kirjauskansion sekä raportin, joka tulostetaan, arkistoidaan ja lähetetään tulostuksenhallinta-asetusten mukaisesti.  

Jos olet lisännyt tarjouspyyntötapahtumaan pisteytysehtoja, tarjouspyyntövastauksessa on pisteytyspaneeli, johon voit lisätä pisteet. Yhteispistemäärä tulee näkyviin, kun vertailet vastauksia **Vertaa vastauksia** -sivulla, jolla voit myös verrata muita vastauksen sisältämiä tietoja, kuten rivihintaa, toimituspäivää ja kokonaishintaa.  

Kun olet valinnut jonkin tarjouksen tai osittaiset tarjoukset, voit hyväksyä ne ja hylätä muut. Järjestelmä luo kirjauskansiot hyväksymisille ja hylkäämisille sekä vastaavat raportit. Nämä tulostetaan, arkistoidaan ja lähetetään tulostuksenhallinta-asetusten mukaisesti. Kun hyväksyt tarjouksen tai tietyt tarjouksen rivit, järjestelmä luo joko ostosopimuksen tai ostotilauksen tai päivittää ostoehdotuksen tarjouspyynnön ostotyypistä riippuen. Voit luoda haluamistasi vastauksista kauppasopimuksen käytettäväksi myöhemmin huolimatta siitä, oletko hyväksynyt tai hylännyt kyseiset vastaukset.  

Tarjouspyynnön tila näkyy sen otsikosta ja riippuu tarjouspyynnön rivien tilasta. Tila ilmaisee tarjouspyynnön käsittelyn laajuuden. Jokaisella tarjouspyynnöllä on tilalle kaksi arvoa: alhaisin ja korkein. Alin tila on minkä tahansa tarjouspyynnön rivin vähiten edistynyt vaihe, ja korkein tila on minkä tahansa tarjouspyynnön rivin kaikkein edistynein vaihe. Jos esimerkiksi tarjouspyynnön vähiten edennyt vaihe koskee luotua riviä, tarjouspyynnön alin tila on **Luotu**. Jos tarjouspyynnön eniten edennyt vaihe koskee toimittajille lähetettyä riviä, tarjouspyynnön korkein tila on **Lähetetty**. Tilat päivitetään automaattisesti, kun tarjouspyynnön.  

Voit tarkastella tarjouspyynnön otsikon alinta ja ylintä tilaa **Kaikki tarjouspyynnöt** -sivulla. Voit tarkastella tarjouspyynnön rivin alinta ja ylintä tilaa **Tarjouspyynnöt** -sivulla **Rivit**-välilehdessä.  

Tilojen järjestys tarjouspyyntöjen käsittelylle on seuraava:

1.  **Luotu**
2.  **Lähetetty**
3.  **Vastaanotettu**
4.  **Hyväksytty**/**Peruutettu**/**Hylätty**

Tiloja on kuvattu tarkemmin tämän ohjeaiheen seuraavissa osissa.

## <a name="setting-up-rfq-functionality"></a>Tarjouspyyntötoimintojen asetukset
Ennen tarjouspyyntötapauksen luomista sinun täytyy määrittää tarjouspyynnön tiedot **Hankintaparametrit**-sivulla. Tarjouspyyntötapausta luodessasi voit määrittää oletusarvot, jotka kopioidaan tarjouspyyntöön. Voit määrittää seuraavat oletusarvot:

-   Uusien tarjouspyyntöjen ostotyyppi: **Ostotilaus** tai **Ostosopimus**.
-   Vanhentumispäivämäärän ja -ajan asetukset.
-   Toimitustiedot ja maksuehdot.
-   Tarjouspyynnön vastaukseen sisällytettävät kentät.

Nämä arvot voi ohittaa tietyissä tarjouspyyntötapauksissa. Myös muutosprosessi täytyy määrittää. Tämän määrityksen yhteydessä voit ottaa käyttöön kentän lukituksen. Kun kentän lukitus on käytössä ja hankinta-asiantuntija haluaa tehdä tarjouspyyntöön muutoksia, hänen on ensin valittava **Tarjous**-välilehden **Muutos**-osasta **Luo**. Kun tarjouspyyntö on päivitetty lisäyksellä, hankinta-asiantuntijan on viimeisteltävä prosessi valitsemalla **Viimeistele**. **Viimeistele**-toiminto luo sähköpostiviestin, joka ilmoittaa toimittajille muutetusta tarjouspyynnöstä. Toimittajille lähetettävän sähköposti-ilmoituksen malli valitaan **Hankintaparametrit**-sivulta. Luotava malli voi sisältää seuraavia korvattavia tunnisteita:

-   %Tarjouksen palautuksen syy%
-   %Muutoksen syy%
-   %Muutoksen valmistelija%
-   %Yritys%

%Tarjouksen palautuksen syy%- ja %Muutoksen syy% -tunnisteet korvataan tekstillä, jonka hankinta-asiantuntija voi täyttää viimeistellessään muutoksia ohjatussa **Muutos**-toiminnossa. %Muutoksen valmistelija%- ja %Yritys%-tunnisteet korvataan automaattisesti tarjouspyynnön tiedoilla.  

Jos haluat osoittaa tarjouspyynnön vastauksessa tarjouksen hylkäämisen tai hyväksymisen syyn syykoodeilla, määritä syykoodit **Toimittajan syyt** -sivulla.  

Voit määrittää tulostettujen tai tallennettujen tarjouspyyntöasiakirjojen ulkoasun hankinnan **Lomakeasetukset**-sivulla. 

**Huomautus:** Julkisen sektorin määrityksessä jo lähetettyyn tarjouspyyntöön tehdyt muutokset edellyttävät muutosprosessin käyttöä. Kun tarjouspyyntö on lähetetty, kentät on lukittu, joten edellä mainitun muutosprosessin käyttäminen valitsemalla **Luo** on pakollinen vaihe tehtäessä muutoksia tarjouspyyntöön.
Tätä ohjataan kentän lukitusparametrilla **Lukitse tarjouspyynnöt, kun ne on lähetetty** kohdassa **Lukitse tarjouspyynnöt, kun ne on lähetetty**. Parametrin arvoksi määritetään **Kyllä**. Julkisen sektorin määrityksissä tämä on oletusasetus, jota ei voi muuttaa. Tämä tarkoittaa, että siinä missä muutosprosessi voidaan käsitellä manuaalisesti muissa kuin julkisen sektorin määrityksessä, julkisella sektorilla muutoksia käsitellään lukitsemalla kentät tarjouspyynnön lähettämisen jälkeen.

Kun luot ostotilaukselle tarjouspyynnön ja lisäät tarjouspyyntöön varastonimikkeen, luodaan varastotapahtuma, jossa vastaanoton tila on **Tarjouksen vastaanotto**. Vain tarjouspyyntörivit, joilla on tämä tila, otetaan huomioon, kun lasket toimituksia pääsuunnitelmaa käyttämällä. Jos haluat, että pääsuunnitelma sisältää tarjouspyynnön rivejä odotettuna vastaanottona, tämä on määritettävä pääsuunnittelun asetuksissa.  

Ostopäällikkönä tai -edustajana voit luoda ja ylläpitää pyyntötyyppejä, jotka vastaavat organisaatiosi hankintavaatimuksia. Kukin pyyntötyyppi voi ohjata pisteytysmenetelmiä. Pisteytysmenetelmät koostuvat ehdoista, joita voi käyttää tarjouksia pisteytettäessä. Pyyntötyypit, pisteytysmenetelmät ja pisteytysehdot määritellään **Pyyntötyyppi**- ja **Pisteytystapa**-sivuilla.

## <a name="creating-and-sending-an-rfq"></a>Tarjouspyynnön luominen ja lähettäminen
Voit luoda tarjouspyynnön ja valita toimittajat, joiden haluat lähettävän tarjouksia, ja lähettää sitten tarjouspyynnön toimittajille. Tulostuksenhallinnan avulla voit lähettää tarjouspyyntöraportin ja vastauslomakeraportit haluamaasi sijaintiin.  

Voit luoda tarjouspyynnön **Ostotilaus**- tai **Ostosopimus**-ostotyypeille.  

Jos tarjouspyyntö luodaan ostoehdotuksesta, **Ostoehdotus**-tyyppi määritetään automaattisesti. Tarjouspyyntöä, jonka tyyppi on **Ostoehdotus**, ei voi luoda manuaalisesti. Jos tarjouspyynnön tyyppi on **Ostotilaus**:

-   Kun tarjouspyynnön rivejä luodaan, järjestelmä luo varastotapahtumia, joiden vastaanottotila on **Tarjouksen vastaanotto**.
-   Kun hyväksyt tarjouksen, ostotilaus luodaan.

Jos tarjouspyynnön tyyppi on **Ostosopimus**:

-   Tarjouspyyntöä käytetään sopimuksessa, kun tuotetta halutaan ostaa tietty määrä tai arvo tiettynä aikana. Valitse tällöin ostosopimusta koskeva päivämääräalue ja ostosopimusta hallinnoivan henkilön nimi.
-   Kun hyväksyt tarjouksen, ostosopimus luodaan.

Voit luoda tarjouspyynnön ostoehdotuksesta vain, jos ostoehdotuksen tilana on **Tarkistuksessa** ja sinut on määritetty suorittamaan seuraava työnkulkutehtävä. Ostoehdotuksen rivit päivittyvät automaattisesti, kun hyväksyt toimittajilta saamiasi tarjouspyynnön vastauksia (tarjouksia). Ostoehdotukselle ei voi suorittaa loppuun, hylätä, hyväksyä tai suorittaa mitään muita toimintoja tarjouspyynnön ollessa kesken.  

Kun luot tarjouspyynnön, voit valita tietyn pyyntötyypin. Pyyntötyyppi määrittää pisteytysehdot, joilla tarjouspyynnön vastauksia pisteytetään.  

Voit lisätä tarjouspyyntötapaukseen kyselylomakkeen. Kyselylomake näkyy tämän jälkeen kaikissa vastauksissa, kun tarjouspyyntö on lähetetty.  

Tarjouspyyntötapahtumaan lisättäviä toimittajia voi valita kolmella tavalla:

-   Voit lisätä toimittajia yksitellen.
-   Voit hakea kaikkia toimittajia, jotka täyttävät tietyt ehdot.
-   Voit lisätä automaattisesti kaikki toimittajat, jotka on hyväksytty tarjouspyynnön riveillä käytettyihin hankintaluokkiin.

Kun tarjouspyyntötapaus on valmis, valitse **Lähetä**. Lähetys luo kirjauskansiot ja raportit, jotka tulostetaan, arkistoidaan ja lähetetään tulostuksenhallinta-asetusten mukaisesti.  

Jos valitsit **Käytä toimittajaa hintojen uudelleenlaskemiseen**- ja **Käytä toimittajakohtaisia nimiketietoja** -valintaruudut **Lähetetään tarjouspyyntöä** -sivulta lähettäessäsi pyynnöt toimittajille, jotkin toimittajakohtaiset tiedot täytetään automaattisesti. Voit muokata näitä tietoja **Tarjouspyynnön vastaus** -sivulla.  

Seuraavassa taulukossa näkyvät tarjouspyynnön tilan muutokset, kun luot tarjouspyynnön ja lähetät sen toimittajille.

|                                    |                              |                                                 |                            |                             |
|------------------------------------|------------------------------|-------------------------------------------------|----------------------------|-----------------------------|
| **Toiminto**                         | **Alhaisin tarjouspyyntöotsikon tila** | **Korkein tarjouspyyntöotsikon tila**                   | **Alhaisin tarjouspyyntörivin tila** | **Korkein tarjouspyyntörivin tila** |
| Luo tarjouspyynnön otsikko ja rivi.    | Luotu                      | Luotu                                         | Luotu                    | Luotu                     |
| Lähetä tietylle toimittajalle Tarjouspyyntö. | Lähetetty                         | Lähetetty                                            | Lähetetty                       | Lähetetty                        |
| Lisää toinen toimittaja.                | Luotu                      | Lähetetty (Tarjouspyyntö on lähetetty vain yhdelle toimittajalle.) | Luotu                    | Lähetetty                        |
| Lähetä tarjouspyyntö toiselle toimittajalle. | Lähetetty                         | Lähetetty                                            | Lähetetty                       | Lähetetty                        |

**Huomautus:** Voit lisätä toimittajia tarjouspyyntöön milloin tahansa, ja alimmat ja ylimmät tilat muuttuvat uusien toimittajien mukaan. Jos esimerkiksi sait tarjoukset kaikilta toimittajilta ja hyväksyit vähintään yhden tarjousrivin, tarjouspyynnön otsikon alin tila on **Hylätty** ja ylin tila on **Hyväksytty**. Jos lisäät uuden toimittajan, minkä tahansa rivin alin tila on nyt **Luotu**. Tämän vuoksi tarjouspyynnön otsikon alin tila muuttuu arvoon **Luotu**, ja ylin tila on edelleen **Hyväksytty**.

## <a name="amending-an-rfq"></a>Tarjouspyynnön muuttaminen
Tarjouspyyntöä voi joutua muuttamaan vielä senkin jälkeen, kun se on lähetetty. Syynä voi olla vaikkapa se, että toimituspäivämäärät ovat muuttuneet tai tuotteita tarvitaan lisää tai eri määrinä. Voit määrittää muutosprosessin rajoittavammaksi tai joustavammaksi.  

Jos käytät rajoittavampaa muutosprosessia, tarjouspyyntötapauksessa täytyy valita **Luo**, jotta tarjouspyyntötapauksen kenttiä voi muokata. Kun olet tehnyt haluamasi muutokset, valitse **Viimeistele**. Tämän jälkeen sinua opastetaan lisäämään tiedot sähköpostiviestiin, jolla muutoksesta ilmoitetaan toimittajille. Viestiin liitetään automaattisesti päivitetty tarjouspyyntöraportti, jossa on muutosta koskeva huomautus.  

Jos käytät joustavampaa muutosprosessia, sinun ei tarvitse luoda muutosta, ennen kuin voit muokata jo lähetetyn tarjouspyyntötapauksen kenttiä. Muutoshuomautus on kuitenkin lisättävä tarjouspyyntöön manuaalisesti.

## <a name="receiving-and-registering-rfq-replies"></a>Tarjouspyyntövastausten vastaanottaminen ja rekisteröiminen
Kun lähetät tarjouspyynnön, ohjelma luo automaattisesti vastauslomakkeen. Kun saat vastauksia tarjouspyyntöön (eli tarjouksia), sinun täytyy syöttää kutakin toimittajaa koskevat tiedot toimittajakohtaiselle tarjouspyynnön vastauslomakkeelle. Jos olet lisännyt pisteytysehtoja, voit pisteyttää vastaukset. Sen jälkeen voit vertailla toimittajien tarjouksia ja asettaa ne järjestykseen pisteytysehtojen mukaan, esimerkiksi parhaan kokonaishinnan tai toimitusajan perusteella.  

Jos tarjouspyyntötapahtumaan on liitetty kyselylomake, kysymysten vastaukset on syötettävä manuaalisesti vastauslomakkeeseen.  

Jos haluat syöttää vaihtoehtoisia rivejä ja se on kyseisessä tarjouspyyntötapahtumassa mahdollista, valitse **Ostotarjousrivit**-pikavälilehdestä **Lisää rivi**. Kirjoita sitten tuotteen tiedot, kuten nimikkeen numero tai hankintaluokka, määrä, hinta ja alennus.  

Jos olet kirjoittanut vastauksen mutta vaadit toimittajalta uutta tarjousta, voit lähettää tarjouspyynnön uudelleen. Tämä luo uuden kirjauskansion ja raportin, jolla voit pyytää muutoksia toimittajalta.  

Kaikkien tarjouspyyntöjen ja niiden vastaustilojen yhteenveto on nähtävissä **Tarjouspyynnön seuranta** -sivulla.  

Seuraavassa taulukossa näkyy, miten tarjouspyynnön tila muuttuu, kun vastaanotat tarjouksia ja rekisteröit tiedot tarjouspyynnön vastauslomakkeeseen.

|                                                |                       |                        |                              |                               |                            |                             |
|------------------------------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Toiminto**                                     | **Alin tarjoustila** | **Ylin tarjoustila** | **Alhaisin tarjouspyyntöotsikon tila** | **Korkein tarjouspyyntöotsikon tila** | **Alhaisin tarjouspyyntörivin tila** | **Korkein tarjouspyyntörivin tila** |
| Rekisteröi yhden toimittajan tarjous ja tallenna se.        | Lähetetty                  | Vastaanotettu               | Lähetetty                         | Vastaanotettu                      | Lähetetty                       | Vastaanotettu                    |
| Rekisteröi toisen toimittajan tarjous ja tallenna se. | Vastaanotettu              | Vastaanotettu               | Vastaanotettu                     | Vastaanotettu                      | Vastaanotettu                   | Vastaanotettu                    |

**Huomautus:** Jos palautat tarjouksen toimittajalle lisäneuvotteluja varten, alin ja ylin tila on edelleen **Vastaanotettu**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Tarjousten hyväksyminen ja hylkääminen sekä hyväksyttyjen tarjousten siirtäminen alatason asiakirjoihin

Kun olet löytänyt parhaan tarjouksen, esimerkiksi sellaisen, jonka kokonaishinta on paras, voit hyväksyä sen. Kyseisen toimittajan tarjouspyynnön vastauksen tilaksi päivittyy **Hyväksytty**. Kun hyväksyt tarjouksen tai sen tietyt rivit, ostotilaus tai -sopimus luodaan automaattisesti ja voit hylätä muilta toimittajilta saadut tarjoukset.  

Kun hyväksyt tarjouspyynnön vastauksen, jonka tyyppi on **Ostoehdotus**, ostoehdotusriveille päivittyvät tarjouspyynnön vastausrivien perusteella seuraavat tiedot:

-   Yksikköhinta
-   Alennusprosentti
-   Alennussumma
-   Oston kulut
-   Rivin kulut
-   Toimittaja
-   ulkoinen tunnus
-   Ulkoinen kuvaus

Voit lisätä vastaukseen syykoodin, joka selittää, miksi tarjous on hyväksytty tai hylätty.  

Voit hyväksyä joitakin tarjouksen rivejä ja hylätä muut. Voit myös hyväksyä rivejä eri toimittajilta. Huomaa, että jos hyväksyt joitakin rivejä, näkyviin tulee kehote, jossa kysytään, haluatko hylätä kaikki muut rivit. Jos siis haluat hyväksyä muitakin rivejä, valitse **Peruuta**, kun kehote tulee näyttöön.  

Seuraavassa taulukossa näkyy, miten tarjouspyynnön tila muuttuu, kun hyväksyt ja hylkäät toimittajien tarjouksia.

|                         |                       |                        |                              |                               |                            |                             |
|-------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Toiminto**              | **Alin tarjoustila** | **Ylin tarjoustila** | **Alhaisin tarjouspyyntöotsikon tila** | **Korkein tarjouspyyntöotsikon tila** | **Alhaisin tarjouspyyntörivin tila** | **Korkein tarjouspyyntörivin tila** |
| Hyväksy yksi tarjouksista. | Vastaanotettu              | Hyväksytty               | Vastaanotettu                     | Hyväksytty                      | Vastaanotettu                   | Hyväksytty                    |
| Hylkää muut tarjoukset.  | Hylätty              | Hyväksytty               | Hylätty                     | Hyväksytty                      | Hylätty                   | Hyväksytty                    |





