---
title: Pankin kirjauskansioiden yhdistelmäyksikön päivittäminen
description: Tässä aiheessa on luettelo vaiheista, joita tarvitaan BankTransactionType-lisäkentän lisäämiseen BankJournalEntity-yhdistelmäyksikköön.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 730e6bd10b0cdd1587c915bb9ec8d6a4792435d9
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727255"
---
# <a name="update-the-bank-journal-composite-entity"></a>Pankin kirjauskansioiden yhdistelmäyksikön päivittäminen

[!include [banner](../includes/banner.md)]

Tässä aiheessa on luettelo vaiheista, joita tarvitaan BankTransactionType-lisäkentän lisäämiseen BankJournalEntity-yhdistelmäyksikköön.

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
