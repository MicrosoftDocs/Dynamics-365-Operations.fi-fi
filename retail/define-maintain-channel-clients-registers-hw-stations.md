---
title: "Määritä ja Ylläpidä kanavan asiakkaiden, rekisterit ja laitteiston asemilla"
description: "Tässä wikissä käsitellään oheislaitteiden liittämistä Retail POS:hon."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: dee5745670ad86000795f2913f99f49c0f123a00
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-maintain-channel-clients-registers-and-hardware-stations"></a>Määritä ja Ylläpidä kanavan asiakkaiden, rekisterit ja laitteiston asemilla

Tässä wikissä käsitellään oheislaitteiden liittämistä Retail POS:hon.

**Huomautus:** lisätietoja asennusohjeista on artikkeleissa [Retail Hardware Stationin määritykset ja asennus](retail-hardware-station-configuration-installation.md) ja [Retail Modern POS:n omatoiminen lataus ja asennus sekä Modern POS- ja Cloud POS -laiteaktivointi](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Tärkeimmät osat
Myymälän, myyntipisteen kassakoneiden tai myymälän kanavien sekä kyseisten kassakoneiden tai kanavien tapahtumien käsittelyyn käyttämien myymälän oheislaiteiden välisten suhteiden määrittämiseen tarvitaan useita osia. Tässä osassa käsitetään kutakin osaa ja kerrotaan, miten niitä käytetään vähittäismyymälän käyttöönotossa.

### <a name="pos-registers"></a>Kassakoneet

Siirtyminen: Valitse **jälleenmyynti- ja commerce**&gt;**kanava-asetukset**&gt;**POS-asetukset**&gt;**Rekisteröi**. POS-rekisteri on kokonaisuus, jota käytetään tavaralta ilmentymän Myyntipiste. Nämä ominaisuudet ovat laitteistoprofiilin tai retail-oheislaitteet, jota käytetään rekisterin, myymälä, joka on yhdistetty rekisteriin ja visuaalisia ominaisuuksia käyttäjä, joka kirjautuu, joka rekisteröi asetukset.

### <a name="devices"></a>Laitteet

Siirtyminen: Valitse **jälleenmyynti- ja commerce**&gt;**kanava-asetukset**&gt;**POS-asetukset**&gt;**laitteet**. Laite on yksikkö, joka ilmaisee myyntipisteen kassakoneeseen yhdistämismääritetyn laitteen fyysisen esiintymän. Kun laite on luotu, siitä muodostetaan yhdistämismääritys myyntipisteen kassakoneeseen. Laiteyksikkö seuraa seuraavia tietoja: myyntipisteen kassakoneen aktivoinnin ajankohta, käytettävän asiakasohjelman tyyppi ja tietyssä laitteessa käyttöönotettu sovelluspaketti. Laitetyyppejä on kaksi: **Retail Modern POS** (MPOS) ja **Retail Cloud POS** (Cloud POS).

#### <a name="mpos"></a>MPOS

MPOS on myyntipisteen asiakasohjelma, joka asennettu Windows 8.1- tai sitä uudempaan PC-pohjaiseen käyttöjärjestelmään. Jos **Retail Modern POS** -sovellustyyppi on yhdistämismääritetty laitteeseen, ladattava paketti voidaan määrittää tietylle laitteelle. Ladattava paketti voidaan mukauttaa sisältämään asennuspaketin eri versioita. Koska käyttöön voi ottaa erilaisia paketteja, joustavuus paranee tilanteissa, joissa myyntipisteen eri kassakoneissa on käytettävä erilaisia integrointeja. MPOS otetaan käyttöön yhdessä sisäisen laiteaseman kanssa.

#### <a name="cloud-pos"></a>Cloud POS

Cloud POS on selain-pohjainen POS. Koska se toimii selaimessa, Cloud POS ei edellytä Windows 8.1 tai uudempi PC-pohjainen käyttöjärjestelmä. Jos **Retail Cloud POS** -sovellustyyppi on yhdistämismääritetty taustatoimintojen tiettyyn laitteeseen, laitetta voidaan käyttää selaimella pakettia lataamatta tai asentamatta. Cloud POS tarvitsee laiteaseman, jotta laitetta voi käyttää muutenkin kuin näppäimistöliitokseen perustuvaan viivakoodin lukemiseen.

### <a name="hardware-profile"></a>Laiteprofiili

Siirtyminen: Valitse **Commerce**&gt;**kanava-asetukset**&gt;**POS-asetukset**&gt;**POS-profiilit**&gt;**laitteistoprofiilien**. Laitteistoprofiili tunnistaa myyntipisteen kassakoneeseen tai laiteasemaan liitetyt laitteet. Laitteistoprofiililla määritetään myös maksun käsittelyprofiilit, joita käytetään tiedonsiirrossa maksuohjelmiston kehityspaketin (SDK) kanssa. (Maksu-SDK otetaan käyttöön laiteaseman osana.)

### <a name="hardware-station"></a>Laiteasema

Siirtyminen: Valitse **jälleenmyynti- ja commerce**&gt;**kanavia**&gt;**liikkeistä**&gt;**kaikki liikkeistä**. Valitse ensin myymälä ja sitten **Laiteasemat**-pikavälilehti. Laiteasema on liiketoimintalogiikan esiintymä, jolla POS-oheislaitteita käytetään. Laiteasema asennetaan automaattisesti yhdessä MPOS:n kanssa. Laiteasema voidaan vaihtoehtoisesti asentaa erillisenä osana, jota MPOS tai Cloud POS käyttävät verkkopalvelusta. Laiteasema on määritettävä kanavatasolla.

### <a name="hardware-station-profile"></a>Laiteaseman profiili

Siirtyminen: Valitse **Commerce**&gt;**kanava-asetukset**&gt;**POS-asetukset**&gt;**POS-profiilit**&gt;**asema laitteistoprofiilien**. Siinä missä kanavatasolla määritetty laiteasema sisältää esiintymäkohtaisia tietoja, kuten laiteaseman URL-osoitteen, laiteaseman profiili sisältää joko staattisia tietoja tai useiden laiteasemien kesken jaettuja tietoja. Staattisia tietoja ovat esimerkiksi käytettävä portti, laiteasemapaketti ja laiteaseman profiili. Staattisia tietoja ovat myös kuvaus käyttöönotettavan laiteaseman tyypistä, joka voi olla esimerkiksi **Siirry kassalle **tai **Palautukset**, sen mukaan minkälaista laitetta kukin laiteasema edellyttää.

## <a name="scenarios"></a>Skenaariot
### <a name="mpos-with-connected-peripheral-devices"></a>MPOS, johon on liitetty oheislaitteita

[![Perinteinen, kiinteä myyntipisteeseen](./media/traditional-300x279.png)](./media/traditional.png) muodostaa MPOS POS-oheislaitteiden perinteinen kiinteä POS-tilanteessa ensin Etsi rekisteröi itsensä ja laiteprofiilin siihen. Löydät kassakoneiden POS **jälleenmyynti- ja commerce**&gt;**kanava-asetukset**&gt;**POS-asetukset**&gt;**Rekisteröi**. Synkronoi muutokset laiteprofiilin määrityksen jälkeen kanavatietokantaan käyttämällä Kassakoneet-jakeluaikataulua. Jakelu, aikataulut löydät **jälleenmyynti- ja commerce**&gt;**vähittäismyynnin IT**&gt;**jakeluaikataulu**. Määritä kanavaan seuraavaksi paikallinen laiteasema. Valitse **jälleenmyynti- ja commerce**&gt;**kanavia**&gt;**liikkeistä**&gt;**kaikki liikkeistä**, ja valitse myymälä. Lisää sitten laiteasema valitsemalla **Laiteasemat**-pikavälilehdessä **Lisää**. Kirjoita kuvaus, anna isäntänimeksi **localhost** ja synkronoi sitten kanavan muutokset käyttämällä Kanavan konfigurointi -jakeluaikataulua. Jakelu, aikataulut löydät **jälleenmyynti- ja commerce**&gt;**vähittäismyynnin IT**&gt;**jakeluaikataulu**. Valitse lopuksi MPOS:ssä **Valitse laiteasema** -toiminnolla **localhost**-laiteasema. Valitse laiteaseman asetukseksi **Aktiivinen**. Tässä skenaariossa käytettävä laiteprofiili on haettava myyntipisteen kassakoneesta. Laiteaseman profiilia ei tarvita tässä skenaariossa. **Huomautus:** osa laiteprofiilin muutoksia, kuten kassojen muutokset, edellyttää uuden vuoron avaamista sen jälkeen, kun muutokset on synkronoitu kanavaan. **Huomautus:** Cloud POS:n on käytettävä erillistä laiteasemaa tiedonsiirtoon vähittäismyynnin oheislaitteiden kanssa.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS tai Cloud POS ja erillinen laiteasema

\[selosteen tunnus = "liitteen\_340041" Tasaa = "alignleft" width = "300"\][![jaettu oheislaitteiden](./media/shared-300x254.png)](./media/shared.png) jaettu oheislaitteiden\[/tekstitys\] tässä tilanteessa laitteiston itsenäinen asema on jaettu MPOS ja Cloud POS asiakkaiden kesken. Tämä skenaario edellyttää laiteaseman luontia määrittämään ladattavan paketti, portti ja laiteaseman käyttämä laiteprofiili. Station laitteistoprofiilin, voit etsiä **jälleenmyynti- ja commerce**&gt;**kanava-asetukset**&gt;**POS-asetukset**&gt;**POS-profiilit**&gt;**asema laitteistoprofiilien**. Kun olet luonut station laitteistoprofiilin, siirry tietyn vähittäismyyntikanavan (**jälleenmyynti- ja commerce**&gt;**kanavia**&gt;**liikkeistä**&gt;**kaikki liikkeistä**), ja Lisää uusi laite-asema. Tee tämän uuden laiteaseman yhdistämismääritys aiemmin luotuun laiteaseman profiiliin. Anna seuraavaksi kuvaus, jonka avulla kassa tunnistaa laiteaseman. - **Isännän nimi** -kenttään isännän tietokoneen URL-osoite seuraavassa muodossa: **https://&lt;MachineName:Port&gt;/HardwareStation**. (Korvaa **&lt;MachineName:Port&gt;** koneen varsinaisen nimen laitteisto-asema ja portti, joka on määritetty asema laitteistoprofiilissa.) Erillinen laite-asema olisi myös määritettävä sähköisen varojen siirron (EFT) päätteen tunnusta. Tämä arvo yksilöi sen sähköisen rahansiirron päätteen, joka on liitettynä laiteasemaan, kun maksuyhdistin on yhteydessä maksupalveluun. Siirry seuraavaksi laiteaseman fyysisestä koneesta kanavaan ja valitse laiteasema. Valitse sitten **Lataa** ja asenna laiteasema. Valitse MPOS:ssä tai Cloud POS:ssä seuraavaksi **Valitse laiteasema** -toiminnolla aiemmin asennettu laiteasema. Muodosta suojattu suhde myyntipisteen ja laiteaseman välille valitsemalla **Muodosta laitepari**. Tämä vaihe on suoritettava kerran kullekin myyntipiste- ja laiteasemayhdistelmälle. Kun laiteasemalle on muodostettu laitepari, laiteasema aktivoidaan samalla toiminnolla niin kauan kuin sitä käytetään. Tämän skenaarion laitteistoprofiili liitetään asema laitteistoprofiilin rekisteröi itsensä sijasta. Jos jostain syystä laitteisto-asema ei ole liitetty suoraan laitteistoprofiilin, on käyttää laitteistoprofiilin rekisterissä määritetyt

## <a name="client-maintenance"></a>Asiakasohjelman ylläpito
### <a name="registers"></a>Kassakoneet

Myyntipuheen kassakoneita hallitaan ensisijaisesti kassakoneista sekä kassakoneisiin määritetyistä profiileista. Yksittäisiä kassakonekohtaisia määritteitä hallitaan kassakonetasolla. Näitä määritteitä ovat myymälä, jossa kassakonetta käytetään, kassakoneen numero, kuvaus ja kassakonekohtainen sähköisen rahansiirron päätetunnus.

### <a name="pos-profiles"></a>POS-profiilit

POS-profiilit, löydät **jälleenmyynti- ja commerce**&gt;**kanava-asetukset**&gt;**POS-asetukset**&gt;**POS-profiilit**. Monia kassakoneen ominaisuuksia kannattaa hallita profiilien kautta, sillä profiileja voidaan jakaa useissa kassakoneissa. Profiileille voidaan tehdä yhdistämismääritys joko erilliseen kassakoneeseen tai, jos profiilia käytetään koko myymälässä, vähittäismyymälään. Seuraavissa osissa käsitellään myyntipisteen profiileja ja niiden käyttöä.

#### <a name="offline-profile"></a>Offline-profiili

Offline-profiili määritetään myymälätasolla. Sillä määritetään myyntipisteen kassakoneessa suoritettujen tapahtumien latausasetukset palvelimeen tilanteessa, jossa kassakone ei ole yhteydessä kanavatietokantaan.

#### <a name="functionality-profile"></a>Toimintoprofiili

Toiminnon profiili määritetään myymälätasolla. Sillä voidaan määrittää toiminnot, jotka voidaan suorittaa myyntipisteessä kampanjaa asetuksia. Seuraavat ominaisuudet, joita hallitaan toimintoprofiili. Nämä ominaisuudet järjestetään pikavälilehdessä.

-   **Yleinen**-pikavälilehti:
    -   International Organization for Standardization (ISO).
    -   Luo asiakas offline-tilassa.
    -   Sähköpostin vastaanottoprofiili.
    -   Keskitetty henkilökunnan kirjautumisen todennus.
-   **Toiminnot**-pikavälilehti:
    -   Kirjautuminen ja laajennetun kirjautumisen hallinta.
    -   Myyntipisteen taloushallintoon ja valuuttaan liittyvät ominaisuudet, kuten mahdollisuus näppäillä hinnat ja desimaalien käyttö pienessä valuutassa.
    -   Aikarekisteröinnin ottaminen käyttöön myyntipisteestä.
    -   Tuotteiden ja maksujen näkyminen myyntipisteessä ja kuiteissa.
    -   Päivän lopun hallinta.
    -   Kanavatietokannan tapahtumien pidätysparametrit.
    -   Asiakkaiden haku ja luonti myyntipisteestä.
    -   Alennusten laskenta.
-   **Summa**-pikavälilehti:
    -   Suurin ja pienin hinnat, jotka ovat sallittuja.
    -   Alennus käyttö ja laskenta.
-   **Tietokoodit**-pikavälilehti:
    -   Kaikista näkökohdista miten Tietokoodit hallitaan myyntipisteessä. Lisätietoja [Tietokoodit](info-codes-retail.md).
-   **Kuitin numerointi** -pikavälilehti:
    -   Määritä kuittien numeroinnin muodot, joissa voi olla segmentit myymälänumerolle, päätenumerolle ja vakioille, sekä tiedot tulostetaanko myynti, palautukset, myyntitilaukset ja tarjoukset erikseen järjestyksessä vai noudattavatko ne samaa järjestystä.

#### <a name="receipt-profiles"></a>Kuittiprofiilit

Kuittiprofiilit määritetään tulostimeen laiteprofiilissa. Niillä määritetään tietyssä tulostimessa tulostettavat kuittityypit. Näissä profiileissa on kuittimuotojen asetukset sekä asetukset, joilla määritetään, tulostetaanko kuitti aina vai pyydetäänkö kassaa päättämään kuitin tulostamisesta. Eri tulostimet voivat myös käyttää eri kuittiprofiileja. Jos esimerkiksi tulostin 1 on kuittien vakiolämpötulostin, joten siinä käytetään pienempiä kuittimuotoja. Tulostin 2 on kuitenkin täysikokoinen kuittitulostin, jolla tulostetaan vain enemmän tilaa tarvitsevat asiakastilauksen kuitit.

#### <a name="hardware-profiles"></a>Laiteprofiilit

Laiteprofiilit on käsitelty aiemmin tässä artikkelissa asiakasohjelman asetusten osana. Laiteprofiilit määritetään suoraan myyntipisteen kassakoneeseen tai laiteaseman profiiliin. Niillä määritetään tietyn myyntipisteen kassakoneen tai laiteaseman käyttämät laitetyypit. Laiteprofiileilla määritetään myös sähköisen rahansiirron asetukset, joita käytetään tiedonsiirtoon maksu-SDK:n kanssa.

#### <a name="visual-profiles"></a>Visuaaliset profiilit

Visuaaliset profiilit määritetään kassakonetasolla. Niitä määritetään tietyn kassakoneen teema. Profiileissa on käytettävän sovellustyypin (MPOS tai Cloud POS), korostusväri ja -teeman, fonttimallin, kirjautumistaustan ja myyntipisteen taustan asetukset.

### <a name="custom-fields"></a>Mukautetut kentät

Voit luoda mukautettuja kenttiä, voit lisätä kenttiä, jotka eivät ole tarkoitettu laatikosta Myyntipiste. Saat lisätietoja siitä, miten käyttää mukautettuja kenttiä [mukautettujen kenttien blogimerkintä parissa](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Kieliteksti

Voit ohittaa myyntipisteen oletusmerkkijonot käyttämällä kielitekstimerkintöjä. Voit ohittaa myyntipisteen merkkijonon lisäämällä uuden kielitekstirivin. Määritä sitten tunnus, ohitettava oletusmerkkijono ja myyntipisteessä oletusmerkkijonon tilalla näytettävä teksti.

### <a name="hardware-station-profiles"></a>Laiteaseman profiilit

Laiteaseman profiileja on käsitelty aiemmin tässä artikkelissa. Niillä määritetään ei-esiintymäkohtaisia tietoja laiteasemiin.

### <a name="channel-reports-configuration"></a>Kanavaraporttien konfigurointi

Määritä vähittäismyyntikanavassa käytettävissä olevat raportit **Vähittäismyyntikanavan raporttien määritykset** -sivulla. Voit luoda uusia raportteja antamalla raportin XML-määrityksen ja määrittämällä raportin myyntipisteen tiettyyn käyttöoikeusryhmään.

### <a name="devices"></a>Laitteet

Laitteet käsiteltiin aiemmin tässä artikkelissa. Niitä hallitaan myyntipisteen tietyn kassakoneen aktivointi. Laitteilla määritetään myös tietyssä kassakoneessa käytettävä sovellus ja asennuspaketti, jolla MPOS-asiakasohjelma asennetaan. Laitteen aktivointitilat:

-   **Odottaa** – laite on valmis aktivoitavaksi.
-   **Aktivoitu** – laite on aktivoitu.
-   **Aktivointi poistettu** – laitteen aktivointi on poistettu joko taustapalveluissa tai myyntipisteessä.
-   **Ei käytössä** – laite on poistettu käytöstä.

Muita aktivointiin liittyviä tietoja ovat laitteen aktivointitilan vaihtanut työntekijä, aktivoinnin aikaleima ja tieto siitä, onko laitteen määritykset vahvistettu.

### <a name="client-data-synchronization"></a>Asiakasohjelman tietojen synkronointi

Kaikki POS-asiakasohjelmaan tehdyt muutokset laitteen aktivointitilan muutoksia lukuun ottamatta on synkronoitava kanavatietokantaan, ennen kuin ne otetaan käyttöön. Kanavan tietokantaan tehdyt muutokset synkronoidaan, siirry **jälleenmyynti- ja commerce**&gt;**vähittäismyynnin IT**&gt;**aikataulun jakelu**, ja jakelu edellyttää ajoitus suoritetaan. Jos kyse on asiakasohjelman muutoksista, suorita Kassakoneet- ja Kanavan konfigurointi -jakeluaikataulut.


