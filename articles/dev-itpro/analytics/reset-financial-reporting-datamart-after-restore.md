---
title: "Talousraportoinnin tietovaraston palauttaminen tietokannan palauttamisen jälkeen"
description: "Tässä ohjeaiheessa kerrotaan, miten talousraportoinnin tietovaraston palautetaan Microsoft Dynamics 365 for Finance and Operations -tietokannan palauttamisen jälkeen."
author: ShylaThompson
manager: AnnBe
ms.date: 08/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6e3f78fb2f6528449d2a411225cd0e14ca33443e
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Talousraportoinnin tietovaraston palauttaminen tietokannan palauttamisen jälkeen

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa kerrotaan, miten talousraportoinnin tietovaraston palautetaan Microsoft Dynamics 365 for Finance and Operations -tietokannan palauttamisen jälkeen.

Jos joskus palautat Finance and Operations -tietokannan varmuuskopiosta tai toisen ympäristön tietokannasta, sinun noudatettava tämän ohjeaiheen ohjeita. Tällä tavoin voit varmistaa, että raportin tietovarasto käyttää oikein palautettua Finance and Operations -tietokantaa. 
> [!Note] 
> Tämän prosessin vaiheita tuetaan Dynamics 365 for Operationsin toukokuun 2016 -versiossa (sovelluksen koontiversio 7.0.1265.23014 ja raportoinnin koontiversio 7.0.10000.4) ja uudemmissa versioissa. Jos käytössä on Finance and Operationsin vanha versio, ota yhteys tukiryhmään.

## <a name="export-report-definitions"></a>Raporttimääritysten vieminen
Vie aluksi Report Designerin raporttirakenteet seuraavasti:

1.  Siirry Report Designerissa kohtaan **Yritys** &gt; **Rakenneosaryhmät**.
2.  Valitse vietävä rakenneosaryhmä ja valitse sitten **Vie**. 

    > [!Note] 
    > Finance and Operations tukee vain yhtä **oletusarvoista** rakenneosaryhmää.
    
3.  Valitse vietävät raporttimääritykset seuraavasti:
    -   Voit viedä kaikki raporttien määritykset ja liittyvät rakenneosat valitsemalla **Valitse kaikki**.
    -   Voit viedä tiettyjä raportti-, rivi-, sarake-, puu- ja dimensioyhdistelmiä valitsemalla kyseisen välilehden ja valitsemalla sitten vietävät kohteet. Voit valita välilehdessä useita kohteita pitämällä Ctrl-näppäintä alhaalla. Kun valitset vietävät raportit, niihin liittyvät rivit, sarakkeet, puut ja dimensioyhdistelmät tulevat valituiksi.

4.  Valitse **Vie**.
5.  Anna tiedostonimi ja valitse turvallinen paikka, jonne viedyt raporttimääritykset tallennetaan.
6.  Valitse **Tallenna**.

Tiedosto voidaan kopioida tai ladata turvalliseen paikkaan. Tämän jälkeen se voidaan tuoda toiseen ympäristöön haluttuna ajankohtana. Lisätietoja Microsoft Azure -tallennustilistä on kohdassa [Tietojen siirtäminen AzCopy-komentorivin apuohjelman avulla](/azure/storage/storage-use-azcopy). 
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
### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a>Uusimman MinorVersionDataUpgrade.zip-paketin etsiminen ja lataaminen

Etsi uudin MinorVersionDataUpgrade.zip-paketti ohjeaiheessa [Uusimman tietojen päivityksen käyttöönotettavan paketin lataaminen](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages) annettujen ohjeiden mukaisesti. Ohjeissa kerrotaan, miten tietojen päivityspaketin oikea versio etsitään ja ladataan. Päivitystä ei tarvita MinorVersionDataUpgrade.zip-paketin lataamiseen. MinorVersionDataUpgrade.zip-paketin noutamista varten tarvitsee tehdä vain Uusimman tietojen päivityksen käyttöönotettavan paketin lataaminen -osan vaiheet, ja muut ohjeaiheessa mainitut vaiheet voi jättää tekemättä.

### <a name="execute-scripts-against-finance-and-operations-database"></a>Komentosarjojen suorittaminen Finance and Operations -tietokannassa

Suorita seuraavat komentosarjat Finance and Operations -tietokannassa (ei raportointitietokannassa).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Nämä komentosarjat varmistavat, että käyttäjien, roolien ja muutosten seurannan asetukset on määritetty oikein.

### <a name="execute-powershell-command-to-reset-database"></a>PowerShell-komennon suorittaminen tietokannan palauttamista varten

Suorita seuraava PowerShell-komento järjstelmänvalvojana suoraan AOS-tietokoneessa, jos haluat palauttaa Finance and Operationsin ja raportoinnin väliset integrointiasetukset:

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail “<my reason for resetting>”

```
> [!NOTE]
> Vahvista syöttämällä kirjain Y komennon suorittamisen jälkeen.

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





