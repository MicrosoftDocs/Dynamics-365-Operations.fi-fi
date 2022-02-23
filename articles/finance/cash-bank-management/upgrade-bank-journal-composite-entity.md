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
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ec196600a54a2aed4565cf422dc386d6646ff524
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442633"
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




