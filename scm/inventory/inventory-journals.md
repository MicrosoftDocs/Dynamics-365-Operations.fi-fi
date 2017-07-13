---
title: Varastokirjauskansiot
description: "Tässä artikkelissa kuvataan, miten varastokirjauskansioita voidaan käyttää erityyppisten varastotilannetapahtumien kirjaamisessa."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalBOM, InventJournalCount, InventJournalCountTag, InventJournalLossProfit, InventJournalMovement, InventJournalTransfer, WMSJournalTable
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 51631
ms.assetid: 3fedeaaf-502f-483c-93d2-ab266828189e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: fa629b4b8f7fcbd15ee89bc66cbc0bd7ca45215c
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# Varastokirjauskansiot
<a id="inventory-journals" class="xliff"></a>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Tässä artikkelissa kuvataan, miten varastokirjauskansioita voidaan käyttää erityyppisten varastotilannetapahtumien kirjaamisessa. 

Microsoft Dynamics 365 for Finance and Operationsin varastokirjauskansioihin kirjataan erityyppisiä fyysisiä varastotapahtumia, kuten varasto-ottoja ja -vastaanottoja, varastosiirtoja, tuoterakenteiden luonteja ja fyysisen varaston täsmäytys. Kaikki varastokirjauskansioita käytetään samalla tavalla, mutta ne on jaettu eri tyyppeihin.

## Varastokirjauskansiotyypit
<a id="types-of-inventory-journals" class="xliff"></a>
Käytössä on seuraavat varastokirjauskansiotyypit:

-   Varastotapahtuma
-   Varaston oikaisu
-   Varastosiirto
-   Tuoterakenne
-   Nimikkeen saapuminen
-   Tuotannon varastointi
-   Inventointi
-   Inventointi tunnisteiden perusteella

### Varastotapahtuma
<a id="movement" class="xliff"></a>

Kun käytät varastokirjauskansiota, voit lisätä kustannuksen nimikkeeseen varastoa lisättäessä, mutta lisäkustannus tiettyyn kirjanpidon kirjauskansioon on kohdistettava manuaalisesti määrittämällä kirjanpidon vastatili kirjauskansiota luotaessa. Tämä varastokirjauskansio on kätevä, jos haluat lisätä nimikkeen kuluna toiselle osastolle tai jos haluat poistaa nimikkeitä varastosta kulutarkoituksessa.

### Varaston oikaisu
<a id="inventory-adjustment" class="xliff"></a>

Kun käytä varaston oikaisukirjauskansion, voit lisätä kustannuksen nimikkeen varastossa lisättäessä. Lisäkustannus kirjataan automaattisesti tietylle kirjanpitotilille nimikeryhmän kirjausprofiilin asetusten perusteella. Käytä tätä varastokirjauskansiotyyppiä päivittämään varastomäärien voitot ja tappiot, kun nimike on pidettävä oletuskirjanpidon vastatilillä. Kun kirjaat varaston oikaisukirjauskansion, varastovastaanotto tai varasto-otto kirjataan, varastoarvot muuttuvat ja kirjanpitotapahtumat luodaan.

### Varastosiirto
<a id="transfer" class="xliff"></a>

Voit siirtää nimikkeitä siirtokirjauskansioiden avulla varastointisijainnin, erien tai tuotevarianttien välillä kustannusvaikutuksia liittämättä. Voit esimerkiksi siirtää nimikkeitä saman yrityksen varastosta toiseen. Siirtokirjauskansiota käytettäessä on määritettävä sekä alkuperäinen varastodimensio että uusi varastodimensio (kuten sijainti ja varasto). Määritetyn varastodimension käytettävissä olevan varasto muuttuu vastaavasti. Varastosiirrot ilmaisevat materiaalin välitöntä liikkumista. Kuljetettavaa varastoa ei seurata. Jos kuljetettavaa varasto on seurattava, käytä siirtotilausta. Kun kirjaat siirtokirjauskansioon, kullekin kirjauskansioriville luodaan kaksi varastotapahtumaa:

-   Varasto-otto alkuperäisestä sijainnista
-   Varasto-vastaanotto uudessa sijainnissa

### Tuoterakenne
<a id="bom" class="xliff"></a>

Kun ilmoitat tuoterakenteen valmiiksi, voit luoda tuoterakennekirjauskansion. Tuoterakennekirjauskansion avulla voit kirjata tuoterakenteen suoraan. Tämä kirjaus muodostaa tuotteen varastovastaanoton yhdessä liitetyn tuoterakenteen ja tuoterakenteeseen sisältyvän tuotteiden varasto-ottojen kanssa. Tämä varastokirjauskansiotyyppi on kätevä yksinkertaisissa tai määrältään suurissa tuotantoskenaarioissa, joissa reitityksiä ei tarvita.

### Nimikkeen saapuminen
<a id="item-arrival" class="xliff"></a>

Voit käyttää nimikkeen saapumisen kirjauskansiota nimikkeiden vastaanoton rekisteröintiin (esimerkiksi ostotilauksista). Nimikkeen saapumisen kirjauskansio voidaan luoda osana saapumisen hallintaa **Saapumisten yhteenveto** -sivulla. Voit myös luoda kirjauskansioviennin manuaalisesti **Nimikkeen saapuminen**-sivulla. Jos otat nimikkeen saapumisen kirjauskansion nimessä käyttöön keräyssijaintien tarkistuksen, Finance and Operations etsii sijainnin vastaanotettaville nimikkeille ja, jos tilaa on, muodostaa saapuville nimikkeille sijaintikohteet.

### Tuotannon varastointi
<a id="production-input" class="xliff"></a>

Tuotannon varastoinnin kirjauskansiot toimivat kuten nimikkeen saapumisen kirjauskansiot, mutta niitä käytetään tuotantotilauksille.

### Inventointi
<a id="counting" class="xliff"></a>

Voit korjata inventointikirjauskansioiden avulla nimikkeille tai nimikeryhmille rekisteröidyn käytettävissä olevan varaston ja kirjata sitten todellisen fyysisen määrän. Tällä tavoin tehdä oikaisut, joita tarvitaan erojen täsmäyttämiseen. Voit liittää inventointikäytännöt inventointiryhmiin, mikä auttaa ryhmittämään erilaisia ominaisuuksia sisältävät nimikkeet, jotta ne voidaan sisällyttää inventointikirjauskansioon. Voit esimerkiksi määrittää inventointiryhmät inventoimaan tietyn tiheyden nimikkeet tai inventoimaan nimikkeet, kun varasto laskee tietylle tasolle. Lisätietoja inventointiryhmien määrittämisestä on artikkelissa [Varaston inventointiprosessien määrittäminen (tehtäväopas)](http://ax.help.dynamics.com/en/wiki/define-inventory-counting-processes/).

### Inventointi tunnisteiden perusteella
<a id="tag-counting" class="xliff"></a>

Kirjauskansioita, jotka liittyvät inventointiin tunnisteiden perusteella, käytetään määrittämään numeroitu tunniste inventointierään. Tunnisteessa on oltava tunnistenumero, nimiketunnus ja nimikkeen määrä. Voit varmistaa, että tunnistetta käytetään vain kerran että kaikki tunnisteet käytetään, kun jokaisella nimiketunnuksella yksilöllinen tunnistejoukko, jolla on oma numerosarja. Kullekin tunnisteelle voidaan määrittää kolme arvoa:

-   **Käytetty** – nimiketunnus on laskettu tunnisteelle.
-   **Mitätöity** – tämän tunnisteen nimiketunnus on mitätöity.
-   **Puuttuu** – tämän tunnisteen nimiketunnus puuttuu.

Kun kirjaat tunnisteiden inventointikirjauskansion, uusi inventointikirjauskansio luodaan tunnisteiden inventointikirjauskansioiden rivien perusteella. Lisätietoja inventoinnin tunnisteista on artikkelissa [Varaston inventoinnin tunnisteet](inventory-tag-counting.md).

## Kirjauskansioiden käsittely
<a id="working-with-journals" class="xliff"></a>
Vain yksi käyttäjä kerrallaan voi käsitellä kirjauskansiota. Jos useiden käyttäjien on päästävä kirjautumaan kirjauskansioihin samanaikaisesti luomaan kirjauskansiorivejä, näiden käyttäjien on valittava kirjauskansiot, jotka eivät ole käytössä, jotta tietoja ei korvattaisi. Tilanteissa, joissa useat osastot käyttävät samaa kirjauskansiotyyppiä, kannattaa luoda useita kirjauskansion nimiä (esimerkiksi yksi jokaiselle osastolle). Kannattaa myös jakaa kirjauskansiot niin, että kukin kirjausrutiini on omassa yksilöllisessä varastokirjauskansiossaan. Postitusrutiineille, jotka on yhdistetty inventaariotransaktioihin, luo päiväkirja säännöllisille inventaariosovituksille ja toinen inventaariolaskennalle.

## Kirjauskansioluettelorivit
<a id="posting-journal-lines" class="xliff"></a>
Voit kirjata luomiasi kirjauskansiorivejä koska tahansa siihen saakka, että nimike lisätään lisätapahtumille. Kirjauskansioon annetut tiedot pysyvät kirjauskansiossa, vaikka suljet kirjauskansion kirjaamatta rivejä.




