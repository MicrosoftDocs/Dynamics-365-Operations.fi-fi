---
title: "Talousraportoinnin tietovaraston palauttaminen tietokannan palauttamisen jälkeen"
description: "Tässä ohjeaiheessa kerrotaan, miten talousraportoinnin tietovaraston palautetaan Microsoft Dynamics 365 for Finance and Operations -tietokannan palauttamisen jälkeen."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: c132c04bc64f02201252f03830d3f8309306f19c
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Talousraportoinnin tietovaraston palauttaminen tietokannan palauttamisen jälkeen

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa kerrotaan, miten talousraportoinnin tietovaraston palautetaan Microsoft Dynamics 365 for Finance and Operations -tietokannan palauttamisen jälkeen. 

Finance and Operations -tietokanta voidaan joutua palauttamaan useissa eri tilanteissa, kuten tietokannan varmuuskopioinnin tai toisesta ympäristöstä kopioinnin yhteydessä. Tällöin on noudatettava tiettyjä vaiheita, joiden avulla varmistetaan, että talousraportoinnin tietovarasto käyttää palautettua Finance and Operations -tietokantaa oikein. Lisätietoja talousraportoinnin tietovaraston palauttamisesta, kun palauttamisessa ei ole kyse Finance and Operations -tietokannan palauttamisesta on ohjeaiheessa [Management Reporter -tietovaraston palauttaminen](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/). Ota huomioon, että tämän prosessin vaiheita tuetaan Dynamics 365 for Operations -ohjelman toukokuu 2016 -versiossa (sovelluksen versio 7.0.1265.23014 ja talousraportoinnin versio 7.0.10000.4) ja uudemmissa versioissa. Jos käytössä on Finance and Operationsin vanha versio, ota yhteys tukiryhmään.

## <a name="export-report-definitions"></a>Raporttimääritysten vieminen
Vie aluksi Report Designerin raporttirakenteet seuraavasti:

1.  Siirry Report Designerissa kohtaan **Yritys** &gt; **Rakenneosaryhmät**.
2.  Valitse vietävä rakenneosaryhmä ja valitse sitten **Vie**. **Huomautus:** Finance and Operations tukee vain yhtä **oletusarvoista** rakenneosaryhmää.
3.  Valitse vietävät raporttimääritykset seuraavasti:
    -   Voit viedä kaikki raporttien määritykset ja liittyvät rakenneosat valitsemalla **Valitse kaikki**.
    -   Voit viedä tiettyjä raportti-, rivi-, sarake-, puu- ja dimensioyhdistelmiä valitsemalla kyseisen välilehden ja valitsemalla sitten vietävät kohteet. Voit valita useita välilehden kohteita pitämällä Ctrl-näppäintä alhaalla. Kun valitset vietävät raportit, liittyvät rivi-, sarake-, puu- ja dimensioyhdistelmät valitaan myös.

4.  Valitse **Vie**.
5.  Anna tiedostonimi ja valitse turvallinen paikka, jonne viedyt raporttimääritykset tallennetaan.
6.  Valitse **Tallenna**.

Tiedosto voidaan kopioida tai ladata turvalliseen paikkaan. Tämän jälkeen se voidaan tuoda toiseen ympäristöön haluttuna ajankohtana. Lisätietoja Microsoft Azure -tallennustilistä on kohdassa [Tietojen siirtäminen AzCopy-komentorivin apuohjelman avulla](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). 
> [!NOTE]
> Microsoft ei tarjoa tallennustiliä Finance and Operations -sopimuksen osana. Osta tallennustili tai käytä erillisen Azure-tilauksen tallennustiliä. 
> [!WARNING]
> Ota huomioon Azuren virtuaalikoneiden D-aseman toiminta. Älä säilytä vietyjä rakenneosaryhmiä täällä pysyvästi. Lisätietoja väliaikaisista asemista on kohdassa [Tietoja Windows Azuren virtuaalikoneiden väliaikaisesta asemasta](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Palveluiden pysäyttäminen
Muodosta yhteys kaikkiin ympäristön tietokoneisiin etätyöpöydän avulla. Pysäytä seuraavat Windows-palvelut services.msc:n avulla:

-   WWW-julkaisupalvelu (kaikissa AOS-tietokoneissa)
-   Microsoft Dynamics 365 for Finance and Operationsin erähallintapalvelu (vain muissa kuin yksityisissä AOS-tietokoneissa)
-   Management Reporter 2012 Process Service (vain BI-tietokoneissa)

Näillä palveluilla on avoimet yhteydet Finance and Operations -tietokantaan.

## <a name="reset"></a>Palauta
#### <a name="locate-the-latest-dataupgradezip-package"></a>Uusimman DataUpgrade.zip-paketin etsiminen

Etsi uusin DataUpgrade.zip-paketti kohdan [DataUpgrade.zip-komentosarjan lataaminen](..\migration-upgrade\upgrade-data-to-latest-update.md) ohjeilla. Ohjeissa kerrotaan, miten löydät tietojen päivityksen paketin oikean version ympäristöäsi varten.

#### <a name="execute-scripts-against-finance-and-operations-database"></a>Komentosarjojen suorittaminen Finance and Operations -tietokannassa

Suorita seuraavat komentosarjat Finance and Operations -tietokannassa (ei raportointitietokannassa).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Nämä komentosarjat varmistavat, että käyttäjien, roolien ja muutosten seurannan asetukset on määritetty oikein.

#### <a name="execute-powershell-command-to-reset-database"></a>PowerShell-komennon suorittaminen tietokannan palauttamista varten

Suorita seuraava komento suoraan AOS-tietokoneessa, jos haluat palauttaa Finance and Operationsin ja raportoinnin väliset integrointiasetukset:

1.  Avaa Windows PowerShell järjestelmänvalvojana.
2.  Suorita: F:
3.  Suorita: cd F:\\MRApplicationService\\MRInstallDirectory
4.  Suorita: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1
5.  Suorita: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”
    -   Vahvista syöttämällä kirjain Y.

Parametrien selitys:

-   Reason-parametrin sallitut arvot ovat SERVICING, BADDATA, OTHER.
-   ReasonDetail-parametri on vapaatekstikenttä.
-   Sekä reason että reasonDetail tallennetaan telemetria-/ympäristövalvonnassa.

## <a name="start-services"></a>Palveluiden käynnistäminen
Käynnistä aiemmin pysäyttämäsi palvelut uudelleen services.msc:n avulla:

-   WWW-julkaisupalvelu (kaikissa AOS-tietokoneissa)
-   Microsoft Dynamics 365 for Finance and Operationsin erähallintapalvelu (vain muissa kuin yksityisissä AOS-tietokoneissa)
-   Management Reporter 2012 Process Service (vain BI-tietokoneissa)

## <a name="import-report-definitions"></a>Raporttimääritysten tuominen
Tuo raporttimallit Report Designerista viennin aikana luotua tiedostoa seuraavasti:

1.  Siirry Report Designerissa kohtaan **Yritys** &gt; **Rakenneosaryhmät**.
2.  Valitse vietävä rakenneosaryhmä ja valitse sitten **Vie**. 
    > [!NOTE]
    > Finance and Operations tukee vain yhtä **oletusarvoista** rakenneosaryhmää.
3.  Valitse **oletusrakenneosa** ja valitse sitten **Tuo**.
4.  Valitse viedyt raporttimääritykset sisältävä tiedosto ja valitse sitten **Avaa**.
5.  Valitse Tuo-valintaikkunassa tuotavat raporttien määritykset.
    -   Voit tuoda kaikki raporttien määritykset ja niitä tukevat rakenneosat valitsemalla **Valitse kaikki**.
    -   Voit tuoda tiettyjä raportti-, rivi-, sarake-, puu- tai dimensioyhdistelmiä valitsemalla tuotavat raportti-, rivi-, sarake-, puu- tai dimensioyhdistelmät.

6.  Valitse **Tuo**.





