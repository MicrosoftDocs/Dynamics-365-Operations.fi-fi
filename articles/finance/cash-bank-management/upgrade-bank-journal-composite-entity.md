---
title: Pankin kirjauskansioiden yhdistelmäyksikön päivittäminen
description: Seuraavat vaiheet ovat välttämättömät, jotta voit lisätä BankTransactionType-lisäkentän BankJournalEntity-yhdistelmäyksikköön.
author: ShylaThompson
manager: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 18137ca8cecc43b4269f14b36df2eb8063192e52
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236344"
---
# <a name="update-the-bank-journal-composite-entity"></a>Pankin kirjauskansioiden yhdistelmäyksikön päivittäminen

[!include [banner](../includes/banner.md)]

Seuraavat vaiheet ovat välttämättömät, jotta voit lisätä BankTransactionType-lisäkentän BankJournalEntity-yhdistelmäyksikköön.

Seuraavien vaiheiden avulla voit lisätä BankTransactionType-lisäkentän BankJournalEntity-yhdistelmäyksikköön.

1.  Kääntää ja synkronoi seuraavat pankin kirjauskansion yhdistelmäyksiköt, yksiköt ja valmistelutaulut:
    -   Yhdistelmäyksikkö\\BankJournalEntity
    -   Yksikkö\\BankJournalHeaderEntity
    -   Yksikkö\\BankJournalLineEntity
    -   Taulu\\BankJournalHeaderStaging
    -   Taulu\\BankJournalLineStaging

2.  Tietojen hallinta\\tietoprojektit
    -   Näytä **pankkitapahtuma**-tyyppi **Lähdetiedot**-asettelussa.
        -   Lähdetietojen muoto = XML-elementti
        -   Yksikön nimi = pankin kirjauskansio
        -   Lataa datatiedosto = SampleBankJournalCompositeEntity.xml uusi versio.
        -   Korvaa aiemmin luotu tiedosto napsauttamalla **Kyllä**.
        -   Valitse **Kyllä** jolloin luodaan uusi yhdistämismääritys.
        -   Tarkista, että pankkitapahtuman laji on yhdistetty.
            -   Valitse **Näytä yhdistämismääritykset** rivi-yksikössä.
            -   Varmista, että pankkitapahtuman laji liitetään lähteestä väliaikaiseen alueeseen.

3.  Tuo uusi tilinpäätös.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]