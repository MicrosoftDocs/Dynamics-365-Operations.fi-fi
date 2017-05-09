---
title: "Talousraportoinnin tietovaraston palauttaminen tietokannan palauttamisen jälkeen"
description: "Tässä aiheessa kerrotaan, miten talousraportoinnin tietovaraston palautetaan Microsoft Dynamics 365 for Operations -tietokannan palauttamisen jälkeen."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-08 16 - 20 - 13
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 3967cbb869fbb23d5d7716f619e4c22b4a273921
ms.lasthandoff: 03/29/2017


---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Talousraportoinnin tietovaraston palauttaminen tietokannan palauttamisen jälkeen

Tässä aiheessa kerrotaan, miten talousraportoinnin tietovaraston palautetaan Microsoft Dynamics 365 for Operations -tietokannan palauttamisen jälkeen. 

Dynamics 365 for Operations -tietokanta voidaan joutua palauttamaan useissa eri tilanteissa, kuten esimerkiksi tietokannan varmuuskopioinnin tai toisesta ympäristöstä kopioinnin yhteydessä. Tällöin on noudatettava tiettyjä vaiheita, joiden avulla varmistetaan, että talousraportoinnin tietovarasto käyttää palautettua Dynamics 365 for Operations -tietokantaa oikein. Lisätietoja talousraportoinnin tietovaraston palauttamisesta, kun palauttamisen syy ei ole Dynamics 365 for Operations -tietokannan palauttaminen, on kohdassa [Management Reporter -tietovaraston palauttaminen](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/). Ota huomioon, että tämän prosessin vaiheita tuetaan Dynamics 365 for Operations -ohjelman toukokuu 2016 -versiossa (sovelluksen versio 7.0.1265.23014 ja talousraportoinnin versio 7.0.10000.4) ja uudemmissa versioissa. Jos käytössä on vanhempi Dynamics 365 for Operations -versio, ota yhteys tukiryhmään.

## <a name="export-report-definitions"></a>Raporttimääritysten vieminen
Vie aluksi Report Designerin raporttirakenteet seuraavasti:

1.  Siirry Report Designerissa kohtaan **Yritys** &gt; **Rakenneosaryhmät**.
2.  Valitse vietävä rakenneosaryhmä ja valitse sitten **Vie**. **Huomautus:** Dynamics 365 for Operations tukee vain yhtä **oletusarvoista** rakenneosaryhmää.
3.  Valitse vietävät raporttimääritykset seuraavasti:
    -   Voit viedä kaikki raporttien määritykset ja liittyvät rakenneosat valitsemalla **Valitse kaikki**.
    -   Voit viedä tiettyjä raportti-, rivi-, sarake-, puu- ja dimensioyhdistelmiä valitsemalla kyseisen välilehden ja valitsemalla sitten vietävät kohteet. Voit valita useita välilehden kohteita pitämällä Ctrl-näppäintä alhaalla. Kun valitset vietävät raportit, liittyvät rivi-, sarake-, puu- ja dimensioyhdistelmät valitaan myös.

4.  Valitse **Vie**.
5.  Anna tiedostonimi ja valitse turvallinen paikka, jonne viedyt raporttimääritykset tallennetaan.
6.  Valitse **Tallenna**.

Tiedosto voidaan kopioida tai ladata turvalliseen paikkaan. Tämän jälkeen se voidaan tuoda toiseen ympäristöön haluttuna ajankohtana. Lisätietoja Microsoft Azure -tallennustilistä on kohdassa [Tietojen siirtäminen AzCopy-komentorivin apuohjelman avulla](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). **Huomautus:** Microsoft ei tarjoa tallennustiliä Dynamics 365 for Operations -sopimuksen osana. Osta tallennustili tai käytä erillisen Azure-tilauksen tallennustiliä. **Tärkeää:** Ota huomioon Azuren virtuaalikoneiden D-aseman toiminta. Älä säilytä vietyjä rakenneosaryhmiä täällä pysyvästi. Lisätietoja väliaikaisista asemista on kohdassa [Tietoja Windows Azuren virtuaalikoneiden väliaikaisesta asemasta](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Palveluiden pysäyttäminen
Muodosta yhteys kaikkiin ympäristön tietokoneisiin etätyöpöydän avulla. Pysäytä seuraavat Windows-palvelut services.msc:n avulla:

-   WWW-julkaisupalvelu (kaikissa AOS-tietokoneissa)
-   Microsoft Dynamics 365 for Operations -ohjelman erähallintapalvelu (vain muissa kuin yksityisissä AOS-tietokoneissa)
-   Management Reporter 2012 Process Service (vain BI-tietokoneissa)

Näillä palveluilla on avoimet yhteydet Dynamics 365 for Operations -tietokantaan.

## <a name="reset"></a>Palauta
#### <a name="locate-the-latest-dataupgradezip-package"></a>Uusimman DataUpgrade.zip-paketin etsiminen

Etsi uusin DataUpgrade.zip-paketti kohdan [DataUpgrade.zip-komentosarjan lataaminen](..\migration-upgrade\upgrade-data-to-latest-update.md) ohjeilla. Ohjeissa kerrotaan, miten löydät tietojen päivityksen paketin oikean version ympäristöäsi varten.

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>Komentosarjojen suorittaminen Dynamics 365 for Operations -tietokannassa

Suorita seuraavat komentosarjat Dynamics 365 for Operations -tietokannassa (ei talousraportoinnin tietokannassa).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Nämä komentosarjat varmistavat, että käyttäjien, roolien ja muutosten seurannan asetukset on määritetty oikein.

#### <a name="execute-powershell-command-to-reset-database"></a>PowerShell-komennon suorittaminen tietokannan palauttamista varten

Suorita seuraava komento suoraan AOS-tietokoneessa, kun haluat palauttaa Dynamics 365 for Operations -ohjelman ja talousraportoinnin välisen integroinnin asetukset:

1.  Avaa Windows PowerShell järjestelmänvalvojana.
2.  Suorita: F:
3.  Suorita: cd F:\\MRApplicationService\\MRInstallDirectory
4.  Suorita: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1
5.  Suorita: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”
    -   Vahvista syöttämällä kirjain Y.

Parametrien selitys:

-   -Reason-parametrin sallitut arvot ovat SERVICING, BADDATA, OTHER.
-   -ReasonDetail-parametri on vapaatekstikenttä.
-   Sekä reason että reasonDetail tallennetaan telemetria-/ympäristövalvonnassa.

## <a name="start-services"></a>Palveluiden käynnistäminen
Käynnistä aiemmin pysäyttämäsi palvelut uudelleen services.msc:n avulla:

-   WWW-julkaisupalvelu (kaikissa AOS-tietokoneissa)
-   Microsoft Dynamics 365 for Operations -ohjelman erähallintapalvelu (vain muissa kuin yksityisissä AOS-tietokoneissa)
-   Management Reporter 2012 Process Service (vain BI-tietokoneissa)

## <a name="import-report-definitions"></a>Raporttimääritysten tuominen
Tuo raporttimallit Report Designerista viennin aikana luotua tiedostoa seuraavasti:

1.  Siirry Report Designerissa kohtaan **Yritys** &gt; **Rakenneosaryhmät**.
2.  Valitse vietävä rakenneosaryhmä ja valitse sitten **Vie**. **Huomautus:** Dynamics 365 for Operations tukee vain yhtä **oletusarvoista** rakenneosaryhmää.
3.  Valitse **oletusrakenneosa** ja valitse sitten **Tuo**.
4.  Valitse viedyt raporttimääritykset sisältävä tiedosto ja valitse sitten **Avaa**.
5.  Valitse Tuo-valintaikkunassa tuotavat raporttien määritykset.
    -   Voit tuoda kaikki raporttien määritykset ja niitä tukevat rakenneosat valitsemalla **Valitse kaikki**.
    -   Voit tuoda tiettyjä raportti-, rivi-, sarake-, puu- tai dimensioyhdistelmiä valitsemalla tuotavat raportti-, rivi-, sarake-, puu- tai dimensioyhdistelmät.

6.  Valitse **Tuo**.



