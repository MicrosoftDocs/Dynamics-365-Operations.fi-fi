---
title: Laajennettu pankkitäsmäytys MT940 tuonti - yhdistelmätietoyksikkö päivitys
description: Järjestysnumero täytyy lisätä tiliotteen tuonnin yksikköön tukemaan MT940-muotoa.
author: angelad116
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e0cf603e04be4f8f784a32b9ef98d748d4d28e5b
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151488"
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
            6.  Varmista, että S **equenceNumber** on yhdistetty.
                -   Valitse **Näytä yhdistämismääritykset** tiliote-yksikössä.
                -   Varmista, että **SequenceNumber** liitetään lähteestä väliaikaiseen alueeseen.

3.  Tuo uusi tilinpäätös.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
