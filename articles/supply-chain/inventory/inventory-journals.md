---
title: Varastokirjauskansiot
description: "Tässä artikkelissa kuvataan, miten varastokirjauskansioita voidaan käyttää erityyppisten varastotilannetapahtumien kirjaamisessa."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalBOM, InventJournalCount, InventJournalCountTag, InventJournalLossProfit, InventJournalMovement, InventJournalTransfer, WMSJournalTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 51631
ms.assetid: 3fedeaaf-502f-483c-93d2-ab266828189e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 968bf9a243d0c0cc9f0dfec474cb207ca32f9eeb
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="inventory-journals"></a>Varastokirjauskansiot

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Tässä artikkelissa kuvataan, miten varastokirjauskansioita voidaan käyttää erityyppisten varastotilannetapahtumien kirjaamisessa.

Microsoft Dynamics 365 for Finance and Operationsin varastokirjauskansioihin kirjataan erityyppisiä fyysisiä varastotapahtumia, kuten varasto-ottoja ja -vastaanottoja, varastosiirtoja, tuoterakenteiden luonteja ja fyysisen varaston täsmäytys. Kaikki varastokirjauskansioita käytetään samalla tavalla, mutta ne on jaettu eri tyyppeihin.

## <a name="types-of-inventory-journals"></a>Varastokirjauskansiotyypit
Käytössä on seuraavat varastokirjauskansiotyypit:

-   Varastotapahtuma
-   Varaston oikaisu
-   Varastosiirto
-   Tuoterakenne
-   Nimikkeen saapuminen
-   Tuotannon varastointi
-   Inventointi
-   Inventointi tunnisteiden perusteella

### <a name="movement"></a>Varastotapahtuma

Kun käytät varastokirjauskansiota, voit lisätä kustannuksen nimikkeeseen varastoa lisättäessä, mutta lisäkustannus tiettyyn kirjanpidon kirjauskansioon on kohdistettava manuaalisesti määrittämällä kirjanpidon vastatili kirjauskansiota luotaessa. Tämä varastokirjauskansio on kätevä, jos haluat lisätä nimikkeen kuluna toiselle osastolle tai jos haluat poistaa nimikkeitä varastosta kulutarkoituksessa.

### <a name="inventory-adjustment"></a>Varaston oikaisu

Kun käytä varaston oikaisukirjauskansion, voit lisätä kustannuksen nimikkeen varastossa lisättäessä. Lisäkustannus kirjataan automaattisesti tietylle kirjanpitotilille nimikeryhmän kirjausprofiilin asetusten perusteella. Käytä tätä varastokirjauskansiotyyppiä päivittämään varastomäärien voitot ja tappiot, kun nimike on pidettävä oletuskirjanpidon vastatilillä. Kun kirjaat varaston oikaisukirjauskansion, varastovastaanotto tai varasto-otto kirjataan, varastoarvot muuttuvat ja kirjanpitotapahtumat luodaan.

### <a name="transfer"></a>Varastosiirto

Voit siirtää nimikkeitä siirtokirjauskansioiden avulla varastointisijainnin, erien tai tuotevarianttien välillä kustannusvaikutuksia liittämättä. Voit esimerkiksi siirtää nimikkeitä saman yrityksen varastosta toiseen. Siirtokirjauskansiota käytettäessä on määritettävä sekä alkuperäinen varastodimensio että uusi varastodimensio (kuten sijainti ja varasto). Määritetyn varastodimension käytettävissä olevan varasto muuttuu vastaavasti. Varastosiirrot ilmaisevat materiaalin välitöntä liikkumista. Kuljetettavaa varastoa ei seurata. Jos kuljetettavaa varasto on seurattava, käytä siirtotilausta. Kun kirjaat siirtokirjauskansioon, kullekin kirjauskansioriville luodaan kaksi varastotapahtumaa:

-   Varasto-otto alkuperäisestä sijainnista
-   Varasto-vastaanotto uudessa sijainnissa

### <a name="bom"></a>Tuoterakenne

Kun ilmoitat tuoterakenteen valmiiksi, voit luoda tuoterakennekirjauskansion. Tuoterakennekirjauskansion avulla voit kirjata tuoterakenteen suoraan. Tämä kirjaus muodostaa tuotteen varastovastaanoton yhdessä liitetyn tuoterakenteen ja tuoterakenteeseen sisältyvän tuotteiden varasto-ottojen kanssa. Tämä varastokirjauskansiotyyppi on kätevä yksinkertaisissa tai määrältään suurissa tuotantoskenaarioissa, joissa reitityksiä ei tarvita.

### <a name="item-arrival"></a>Nimikkeen saapuminen

Voit käyttää nimikkeen saapumisen kirjauskansiota nimikkeiden vastaanoton rekisteröintiin (esimerkiksi ostotilauksista). Nimikkeen saapumisen kirjauskansio voidaan luoda osana saapumisen hallintaa **Saapumisten yhteenveto** -sivulla. Voit myös luoda kirjauskansioviennin manuaalisesti **Nimikkeen saapuminen**-sivulla. Jos otat nimikkeen saapumisen kirjauskansion nimessä käyttöön keräyssijaintien tarkistuksen, Finance and Operations etsii sijainnin vastaanotettaville nimikkeille ja, jos tilaa on, muodostaa saapuville nimikkeille sijaintikohteet.

### <a name="production-input"></a>Tuotannon varastointi

Tuotannon varastoinnin kirjauskansiot toimivat kuten nimikkeen saapumisen kirjauskansiot, mutta niitä käytetään tuotantotilauksille.

### <a name="counting"></a>Inventointi

Voit korjata inventointikirjauskansioiden avulla nimikkeille tai nimikeryhmille rekisteröidyn käytettävissä olevan varaston ja kirjata sitten todellisen fyysisen määrän. Tällä tavoin tehdä oikaisut, joita tarvitaan erojen täsmäyttämiseen. Voit liittää inventointikäytännöt inventointiryhmiin, mikä auttaa ryhmittämään erilaisia ominaisuuksia sisältävät nimikkeet, jotta ne voidaan sisällyttää inventointikirjauskansioon. Voit esimerkiksi määrittää inventointiryhmät inventoimaan tietyn tiheyden nimikkeet tai inventoimaan nimikkeet, kun varasto laskee tietylle tasolle. Lisätietoja inventointiryhmien määrittämisestä on artikkelissa [Varaston inventointiprosessien määrittäminen (tehtäväopas)](tasks/define-inventory-counting-processes.md).

### <a name="tag-counting"></a>Inventointi tunnisteiden perusteella

Kirjauskansioita, jotka liittyvät inventointiin tunnisteiden perusteella, käytetään määrittämään numeroitu tunniste inventointierään. Tunnisteessa on oltava tunnistenumero, nimiketunnus ja nimikkeen määrä. Voit varmistaa, että tunnistetta käytetään vain kerran että kaikki tunnisteet käytetään, kun jokaisella nimiketunnuksella yksilöllinen tunnistejoukko, jolla on oma numerosarja. Kullekin tunnisteelle voidaan määrittää kolme arvoa:

-   **Käytetty** – nimiketunnus on laskettu tunnisteelle.
-   **Mitätöity** – tämän tunnisteen nimiketunnus on mitätöity.
-   **Puuttuu** – tämän tunnisteen nimiketunnus puuttuu.

Kun kirjaat tunnisteiden inventointikirjauskansion, uusi inventointikirjauskansio luodaan tunnisteiden inventointikirjauskansioiden rivien perusteella. Lisätietoja inventoinnin tunnisteista on artikkelissa [Varaston inventoinnin tunnisteet](inventory-tag-counting.md).

## <a name="working-with-journals"></a>Kirjauskansioiden käsittely
Vain yksi käyttäjä kerrallaan voi käsitellä kirjauskansiota. Jos useiden käyttäjien on päästävä kirjautumaan kirjauskansioihin samanaikaisesti luomaan kirjauskansiorivejä, näiden käyttäjien on valittava kirjauskansiot, jotka eivät ole käytössä, jotta tietoja ei korvattaisi. Tilanteissa, joissa useat osastot käyttävät samaa kirjauskansiotyyppiä, kannattaa luoda useita kirjauskansion nimiä (esimerkiksi yksi jokaiselle osastolle). Kannattaa myös jakaa kirjauskansiot niin, että kukin kirjausrutiini on omassa yksilöllisessä varastokirjauskansiossaan. Postitusrutiineille, jotka on yhdistetty inventaariotransaktioihin, luo päiväkirja säännöllisille inventaariosovituksille ja toinen inventaariolaskennalle.

## <a name="posting-journal-lines"></a>Kirjauskansioluettelorivit
Voit kirjata luomiasi kirjauskansiorivejä koska tahansa siihen saakka, että nimike lisätään lisätapahtumille. Kirjauskansioon annetut tiedot pysyvät kirjauskansiossa, vaikka suljet kirjauskansion kirjaamatta rivejä.

