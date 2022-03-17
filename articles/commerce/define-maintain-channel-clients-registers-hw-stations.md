---
title: Yhdistä oheislaitteet myyntipisteeseen (POS)
description: Tässä aiheessa käsitellään oheislaitteiden liittämistä Retail POS:hon.
author: BrianShook
ms.date: 03/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable, RetailDevice
audience: Application User
ms.reviewer: josaw
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f1c53c7215d3a5a182f345d5e040274ae06f9b12
ms.sourcegitcommit: 116898def829c0f78bda8a117242aa308793465d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/01/2022
ms.locfileid: "8370948"
---
# <a name="connect-peripherals-to-the-point-of-sale-pos"></a>Yhdistä oheislaitteet myyntipisteeseen (POS)

[!include [banner](includes/banner.md)]

Tässä aiheessa käsitellään oheislaitteiden liittämistä Retail POS:hon.

> [!NOTE]
> Tarkat asennusohjeet ovat kohdissa [Retail Hardware Stationin määrittäminen ja asentaminen](retail-hardware-station-configuration-installation.md) ja [Moderni POS (MPOS) -ratkaisun määrittäminen, asentaminen ja aktivointi](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Tärkeimmät osat

Myymälän, myyntipisteen kassakoneiden tai myymälän kanavien sekä kyseisten kassakoneiden tai kanavien tapahtumien käsittelyyn käyttämien oheislaiteiden välisten suhteiden määrittämiseen tarvitaan useita osia. Tässä osassa käsitetään kutakin osaa ja kerrotaan, miten niitä käytetään myymälän käyttöönotossa.

### <a name="pos-registers"></a>Kassakoneet

Selaus: Valitse **Vähittäismyynti ja kauppa** &gt; **Kanavan määritys** &gt; **Myyntipisteen määritys** &gt; **Kassakoneet**.

Myyntipisteen kassakone on yksikkö, jolla määritetään tietyn POS-esiintymän ominaisuudet. Näitä ominaisuuksia ovat laiteprofiili tai kassakoneessa käytettävien oheislaitteiden asetukset, myymälä, johon kassakone on yhdistetty, ja kyseiseen kassakoneeseen kirjautuvan käyttäjän visuaalinen kokemus.

### <a name="devices"></a>Laitteet

Selaus: Valitse **Vähittäismyynti ja kauppa** &gt; **Kanavan määritys** &gt; **Myyntipisteen määritys** &gt; **Laitteet**.

Laite on yksikkö, joka ilmaisee myyntipisteen kassakoneeseen yhdistämismääritetyn laitteen fyysisen esiintymän. Kun laite on luotu, siitä muodostetaan yhdistämismääritys myyntipisteen kassakoneeseen. Laiteyksikkö seuraa seuraavia tietoja: myyntipisteen kassakoneen aktivoinnin ajankohta, käytettävän asiakasohjelman tyyppi ja tietyssä laitteessa käyttöönotettu sovelluspaketti. Laitetyyppejä on kaksi: **Retail modern POS** (MPOS) ja **Retail Cloud POS** (Cloud POS).

#### <a name="mpos"></a>MPOS

MPOS on myyntipisteen asiakasohjelma, joka asennettu Windows 8.1- tai sitä uudempaan PC-pohjaiseen käyttöjärjestelmään. Jos **Retail modern POS** -sovellustyyppi on yhdistämismääritetty laitteeseen, ladattava paketti voidaan määrittää tietylle laitteelle. Ladattava paketti voidaan mukauttaa sisältämään asennuspaketin eri versioita. Koska käyttöön voi ottaa erilaisia paketteja, joustavuus paranee tilanteissa, joissa myyntipisteen eri kassakoneissa on käytettävä erilaisia integrointeja. MPOS otetaan käyttöön yhdessä sisäisen laiteaseman kanssa.

#### <a name="cloud-pos"></a>Cloud POS

Cloud POS on selainpohjainen myyntipiste. Koska sitä käytetään selaimessa, Cloud POS:n käyttöä varten ei tarvita Windows 8.1- tai sitä uudempaa PC-pohjaista käyttöjärjestelmää. Jos **Retail Cloud POS** -sovellustyypistä on yhdistämismääritys tiettyyn Headquarters-laitteeseen, laitetta voidaan käyttää selaimella pakettia lataamatta tai asentamatta. Cloud POS tarvitsee laiteaseman, jotta laitetta voi käyttää muutenkin kuin näppäimistöliitokseen perustuvaan viivakoodin lukemiseen.

### <a name="hardware-profile"></a>Laiteprofiili

Siirtyminen: **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Laiteprofiilit**.

Laitteistoprofiili tunnistaa myyntipisteen kassakoneeseen integroidun tai jaetun laiteaseman kautta liitetyt laitteet. Laitteistoprofiililla määritetään myös maksun käsittelyprofiilit, joita käytetään tiedonsiirrossa maksuohjelmiston kehityspaketin (SDK) kanssa. Maksu-SDK otetaan käyttöön laiteaseman osana.

### <a name="hardware-station"></a>Laiteasema

Siirtyminen: Siirry kohtaan **Retail ja Commerce \> Kanavat \> Myymälät \> Kaikki myymälät**, valitse myymälä ja sitten **Hardware stations** -välilehti.

Laiteasema on liiketoimintalogiikan esiintymä, jolla POS-oheislaitteita käytetään. Laiteasema asennetaan automaattisesti yhdessä MPOS:n kanssa. Laiteasema voidaan vaihtoehtoisesti asentaa erillisenä osana, jota MPOS tai Cloud POS käyttävät verkkopalvelusta. Laiteasema on määritettävä kanavatasolla.

## <a name="scenarios"></a>Skenaariot

### <a name="mpos-with-connected-peripheral-devices"></a>MPOS, johon on liitetty oheislaitteita

[![Perinteinen kiinteä myyntipiste.](./media/traditional-300x279.png)](./media/traditional.png)

Jos haluat liittää MPOS:n myyntipisteen oheislaitteisiin perinteistä kiinteää myyntipistettä käytettäessä, siirry ensin kassakoneeseen ja määritä sille laiteprofiili. Pääset myyntipisteen kassakoneisiin valitsemalla **Vähittäismyynti ja kauppa** &gt; **Kanavan määritys** &gt; **Myyntipisteen määritykset** &gt; **Kassakoneet**. 

Synkronoi muutokset laiteprofiilin määrityksen jälkeen kanavatietokantaan käyttämällä **Kassakoneet**-jakeluaikataulua. Pääset jakeluaikatauluihin valitsemalla **Retail ja Commerce** &gt; **Retailin ja Commercen IT** &gt; **Jakeluaikataulu**. 

Määritä kanavaan seuraavaksi erillinen laiteasema. Mene kohtaan **Retail ja Commerce \> Kanavat \> Myymälät \> Kaikki myymälät** ja valitse sitten myymälä. 

Lisää sitten laiteasema valitsemalla **Laiteasemat**-pikavälilehdessä **Lisää**. Valitse laiteasematyypiksi **erillinen** ja kirjoita sitten kuvaus. **Laiteprofiili**-kentän voi jättää tyhjäksi, koska tässä skenaariossa käytettävä laiteprofiili tulee suoraan kassapäätteestä. Synkronoi sitten muutokset kanavaan suorittamalla **Kanavan määritys** -jakeluajoitusta. Pääset jakeluaikatauluihin valitsemalla **Retail ja Commerce \> Retailin ja Commercen IT \> Jakeluaikataulu**. 

Kun olet MPOS-päätteessä, valitse **Valitse laiteasema** -toiminnon avulla laiteasema, joka vastaa aiemmin kuvattua arvoa, ja määritä laiteaseman tilaksi **Aktiivinen**. 

> [!NOTE]
> - Osa laiteprofiilin muutoksia, kuten kassojen muutokset, edellyttää uuden vuoron avaamista sen jälkeen, kun muutokset on synkronoitu kanavaan.
> - Cloud POS:n on käytettävä erillistä laiteasemaa tiedonsiirtoon oheislaitteiden kanssa.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS tai Cloud POS ja erillinen laiteasema

[![Jaetut oheislaitteet.](./media/shared-300x254.png)](./media/shared.png)

Tässä skenaariossa MPOS- ja Cloud POS -asiakasohjelmat jakavat erillisen laiteaseman. Tämä skenaario edellyttää jaetun laiteaseman luontia ja määritä ladattava paketti, portti ja laiteaseman käyttämä laiteprofiili. Voit määrittää uuden laiteaseman valitsemalla **Laiteasemat**-välilehden tietyssä kanavassa (**Retail ja Commerce \> Kanavat \> Myymälät \> Kaikki myymälät**) ja lisäämällä uuden **Jaettu**-tyypin laiteaseman. 

Anna seuraavaksi kuvaus, jonka avulla kassa tunnistaa laiteaseman. Anna **Isännän nimi** -kenttään isäntäkoneen URL-osoite seuraavassa muodossa: `https://<MachineName:Port>/HardwareStation`. (Vaihda **&lt;MachineName:Port&gt;** -kohtaan laiteaseman fyysisen koneen nimi.) Jos kyse on erillisestä laite-asemasta, määritä myös sähköisen rahansiirron (EFT) päätetunnus. Tämä arvo yksilöi sen sähköisen rahansiirron päätteen, joka on liitettynä laiteasemaan, kun maksuyhdistin on yhteydessä maksupalveluun. 

Siirry seuraavaksi laiteasemaa isännöivästä koneesta kanavaan Headquartersissa ja valitse laiteasema. Valitse sitten **Lataa**, kun haluat ladata laiteaseman asennusohjelman ja asentaa laiteaseman. Lisätietoja laiteaseman asentamisesta on kohdassa [Retail Hardware Stationin määrittäminen ja asentaminen](retail-hardware-station-configuration-installation.md). 

Valitse MPOS:ssä tai Cloud POS:ssä seuraavaksi **Valitse laiteasema** -toiminnolla aiemmin asennettu laiteasema. Muodosta suojattu suhde myyntipisteen ja laiteaseman välille valitsemalla **Muodosta laitepari**. Tämä vaihe on suoritettava kerran kullekin myyntipiste- ja laiteasemayhdistelmälle. 

Kun laiteasemalle on muodostettu laitepari, laiteasema aktivoidaan samalla toiminnolla niin kauan kuin sitä käytetään. Tässä skenaariossa laiteprofiili on määritettävä jaetulle laiteasemalle eikä kassakoneelle. Jos laiteasemalle ei ole jostain syystä määritetty suoraan laiteprofiilia, käytetään kassakoneelle määritettyä laiteprofiilia.

## <a name="client-maintenance"></a>Asiakasohjelman ylläpito

### <a name="registers"></a>Kassakoneet

Myyntipuheen kassakoneita hallitaan ensisijaisesti kassakoneista sekä kassakoneisiin määritetyistä profiileista. Yksittäisiä kassakonekohtaisia määritteitä hallitaan kassakonetasolla. Näitä määritteitä ovat myymälä, jossa kassakonetta käytetään, kassakoneen numero, kuvaus ja kassakonekohtainen sähköisen rahansiirron päätetunnus.

### <a name="pos-profiles"></a>POS-profiilit

Pääset myyntipisteen profiileihin valitsemalla **Vähittäismyynti ja kauppa** &gt; **Kanavan määritys** &gt; **Myyntipisteen määritys** &gt; **Myyntipisteprofiilit**. Monia kassakoneen ominaisuuksia kannattaa hallita profiilien kautta, sillä profiileja voidaan jakaa useissa kassakoneissa. Profiileille voidaan tehdä yhdistämismääritys joko erilliseen kassakoneeseen tai, jos profiilia käytetään koko myymälässä, myymälään. Seuraavissa osissa käsitellään myyntipisteen profiileja ja niiden käyttöä.

#### <a name="offline-profile"></a>Offline-profiili

Offline-profiili määritetään myymälätasolla. Sillä määritetään myyntipisteen kassakoneessa suoritettujen tapahtumien latausasetukset palvelimeen tilanteessa, jossa kassakone ei ole yhteydessä kanavatietokantaan.

#### <a name="functionality-profile"></a>Toimintoprofiili

Toiminnon profiili määritetään myymälätasolla. Sillä määritetään myymäläkohtaiset asetukset toiminnoille, joita voidaan suorittaa myyntipisteessä. Seuraavia ominaisuuksia hallitaan toimintoprofiilin kautta. Nämä ominaisuudet järjestetään pikavälilehdessä.

- **Yleinen**-pikavälilehti:

    - International Organization for Standardization (ISO).
    - Luo asiakas offline-tilassa.
    - Sähköpostin vastaanottoprofiili.
    - Keskitetty henkilökunnan kirjautumisen todennus.

- **Toiminnot**-pikavälilehti:

    - Kirjautuminen ja laajennetun kirjautumisen hallinta.
    - Myyntipisteen taloushallintoon ja valuuttaan liittyvät ominaisuudet, kuten mahdollisuus näppäillä hinnat ja desimaalien käyttö pienessä valuutassa.
    - Aikarekisteröinnin ottaminen käyttöön myyntipisteestä.
    - Tuotteiden ja maksujen näkyminen myyntipisteessä ja kuiteissa.
    - Päivän lopun hallinta.
    - Kanavatietokannan tapahtumien pidätysparametrit.
    - Asiakkaiden haku ja luonti myyntipisteestä.
    - Alennusten laskenta.

- **Summa**-pikavälilehti:

    - Suurin ja pienin hinnat, jotka ovat sallittuja.
    - Alennus käyttö ja laskenta.

- **Tietokoodit**-pikavälilehti:

    - Kaikki tavat, joilla tietokoodeja hallitaan myyntipisteessä. Lisätietoja on kohdassa [Tietokoodit ja tietokoodiryhmät](info-codes-retail.md).

- **Kuitin numerointi** -pikavälilehti:

    - Määritä kuittien numeroinnin muodot, joissa voi olla segmentit myymälänumerolle, päätenumerolle ja vakioille, sekä tiedot tulostetaanko myynti, palautukset, myyntitilaukset ja tarjoukset erikseen järjestyksessä vai noudattavatko ne samaa järjestystä.

#### <a name="receipt-profiles"></a>Kuittiprofiilit

Kuittiprofiilit määritetään tulostimeen laiteprofiilissa. Niillä määritetään tietyssä tulostimessa tulostettavat kuittityypit. Näissä profiileissa on kuittimuotojen asetukset sekä asetukset, joilla määritetään, tulostetaanko kuitti aina vai pyydetäänkö kassaa päättämään kuitin tulostamisesta. Eri tulostimet voivat myös käyttää eri kuittiprofiileja. Jos esimerkiksi tulostin 1 on kuittien vakiolämpötulostin, joten siinä käytetään pienempiä kuittimuotoja. Tulostin 2 on kuitenkin täysikokoinen kuittitulostin, jolla tulostetaan vain enemmän tilaa tarvitsevat asiakastilauksen kuitit. Lisätietoja on kohdassa [Kuittiprofiilin määrittäminen](configure-emailed-receipt-formats.md#configure-a-receipt-profile).

#### <a name="hardware-profiles"></a>Laiteprofiilit

Laiteprofiilit on käsitelty aiemmin tässä aiheessa asiakasohjelman asetusten osana. Laiteprofiilit liitetään suoraan myyntipisteen kassakoneeseen tai jaettuun laiteasemaan, ja niiden avulla määritetään laitetyypit, joita tietty POS-kassapääte tai laiteasema käyttää. Laiteprofiileilla määritetään myös sähköisen rahansiirron asetukset, joita käytetään tiedonsiirtoon maksu-SDK:n kanssa.

#### <a name="visual-profiles"></a>Visuaaliset profiilit

Visuaaliset profiilit määrittävät tietyn kassakoneen teeman ja ne määritetään kassakoneen tasolla. Profiileissa on käytettävän sovellustyypin (MPOS tai Cloud POS), korostusväri ja -teeman, fonttimallin, kirjautumistaustan ja myyntipisteen taustan asetukset. Lisätietoja: [Myyntipisteen (POS) visuaalisten profiilien luominen](tasks/create-pos-visual-profile-2016-02.md). 

### <a name="custom-fields"></a>Mukautetut kentät

Voit luoda myyntipisteeseen lisättäväksi mukautettuja kenttiä, jotka eivät ole valmiina paketissa. Lisätietoja mukautettujen kenttien käytöstä on artikkelissa [Mukautettujen kenttien käyttöä käsittelevä blogikirjoitus](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Kieliteksti

Voit ohittaa myyntipisteen oletusmerkkijonot käyttämällä kielitekstimerkintöjä. Voit ohittaa myyntipisteen merkkijonon lisäämällä uuden kielitekstirivin. Määritä sitten tunnus, ohitettava oletusmerkkijono ja myyntipisteessä oletusmerkkijonon tilalla näytettävä teksti.

### <a name="channel-reports-configuration"></a>Kanavaraporttien konfigurointi

Määritä Kanavassa käytettävissä olevat raportit **Kanavan raporttien määritykset** -sivulla. Voit luoda uusia raportteja antamalla raportin XML-määrityksen ja määrittämällä raportin myyntipisteen tiettyyn käyttöoikeusryhmään.

### <a name="devices"></a>Laitteet

Laitteet käsiteltiin aiemmin tässä artikkelissa. Niitä hallitaan myyntipisteen tietyn kassakoneen aktivointi. Laitteilla määritetään myös tietyssä kassakoneessa käytettävä sovellus ja asennuspaketti, jolla MPOS-asiakasohjelma asennetaan. Laitteen aktivointitilat:

- **Odottaa** – laite on valmis aktivoitavaksi.
- **Aktivoitu** – laite on aktivoitu.
- **Aktivointi poistettu** – laitteen aktivointi on poistettu joko Headquarters -sovelluksessa tai myyntipisteessä.
- **Ei käytössä** – laite on poistettu käytöstä.

Muita aktivointiin liittyviä tietoja ovat laitteen aktivointitilan vaihtanut työntekijä, aktivoinnin aikaleima ja tieto siitä, onko laitteen määritykset vahvistettu.

### <a name="client-data-synchronization"></a>Asiakasohjelman tietojen synkronointi

Kaikki POS-asiakasohjelmaan tehdyt muutokset laitteen aktivointitilan muutoksia lukuun ottamatta on synkronoitava kanavatietokantaan, ennen kuin ne otetaan käyttöön. Voit synkronoida muutokset kanavatietokantaan valitsemalla **Vähittäismyynti ja kauppa** &gt; **Vähittäismyynnin ja kaupan IT** &gt; **Jakeluaikataulu** ja suorittamalla sitten tarvittavan jakeluaikataulun. Jos kyse on asiakasohjelman muutoksista, suorita **Kassakoneet**- ja **Kanavan määritys** -jakeluaikataulut.

## <a name="additional-resources"></a>Lisäresurssit

[Retail Hardware Stationin määrittäminen ja asentaminen](retail-hardware-station-configuration-installation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
