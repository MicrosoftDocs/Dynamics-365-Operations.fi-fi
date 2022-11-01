---
title: Pankin kirjauskansioiden yhdistelmäyksikön päivittäminen
description: Tässä artikkelissa on luettelo vaiheista, joita tarvitaan BankTransactionType-lisäkentän lisäämiseen BankJournalEntity-yhdistelmäyksikköön.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1855f9680ba6bcf8eb46608882a128b4a21f0dac
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715200"
---
# <a name="update-the-bank-journal-composite-entity"></a>Pankin kirjauskansioiden yhdistelmäyksikön päivittäminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on luettelo vaiheista, joita tarvitaan BankTransactionType-lisäkentän lisäämiseen BankJournalEntity-yhdistelmäyksikköön.

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
