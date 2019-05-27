---
title: Laajennettu pankkitäsmäytys MT940 tuonti - yhdistelmätietoyksikkö päivitys
description: Järjestysnumero täytyy lisätä tiliotteen tuonnin yksikköön tukemaan MT940-muotoa.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6c0eeb59726422177ed1122767b9d3142a1311a2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554848"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>Laajennettu pankkitäsmäytys MT940 tuonti - yhdistelmätietoyksikkö päivitys

[!include [banner](../includes/banner.md)]

Järjestysnumero täytyy lisätä tiliotteen tuonnin yksikköön tukemaan MT940-muotoa. 

Seuraavien vaiheiden avulla voit lisätä tiliotteen tuonnin entiteetin tukemaan MT940 muotoa.

1.  Käännä ja synkronoi seuraavasti:
    -   Composite Entity\\BankStatementImportEntity
    -   Entity\\BankStatementBalanceEntity
    -   Entity\\BankStatementDocumentEntity
    -   Entity\\BankStatementEntity
    -   Entity\\BankStatementLineEntity
    -   Tables\\BankStatementStaging

2.  Tietojen hallinta\\tietoprojektit
    1.  Lataa MT940 tuontiprojektit
        1.  Vaihda XSLT.
            -   Valitse **Näytä yhdistämismääritykset**.
            -   Valitse **Näytä yhdistämismääritykset** tiliote-asiakirjassa.
            -   Valitse **Muunnokset**
            -   Poista BankReconiliation-to-Composite.xslt -tiedosto.
            -   Lisää uusi versio tiedostosta BankReconiliation-to-Composite.xsl.

        2.  Näytä **järjestysnumero** kohdassa **Lähdetiedot** asettelu.
            1.  Lähdetietojen muoto = XML-Element.
            2.  Yksikön nimi = tiliotteet.
            3.  Lataa datatiedosto = SampleBankCompositeEntity.xml uusi versio.
            4.  Korvaa aiemmin luotu tiedosto napsauttamalla **Kyllä**.
            5.  Valitse **Kyllä** jolloin luodaan uusi yhdistämismääritys.
            6.  Varmista, että S**equenceNumber** on yhdistetty.
                -   Valitse **Näytä yhdistämismääritykset** tiliote-yksikössä.
                -   Varmista, että **SequenceNumber** liitetään lähteestä väliaikaiseen alueeseen.

3.  Tuo uusi tilinpäätös.




