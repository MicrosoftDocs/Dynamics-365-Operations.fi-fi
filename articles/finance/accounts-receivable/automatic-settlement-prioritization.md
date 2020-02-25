---
title: Automaattinen tilitys ja priorisointi
description: Tässä ohjeaiheessa kuvataan tapahtumien tilitetään, jos Automaattinen tilitys -vaihtoehto on valittu Myyntireskontran parametrit -sivulla. Artikkelissa kerrotaan myös, miten automaattista tilitystä voi käyttää yhdessä maksun prioriteetin kanssa.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14531
ms.assetid: e7837cf6-ec69-44b4-8d47-eba38d5c7b1f
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b596557e80035e8d62d01f156a6678c75e4ae573
ms.sourcegitcommit: 9168621ca9b5061c65f3e05dbc5918b6a11d53d5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2020
ms.locfileid: "3000044"
---
# <a name="automatic-settlement-and-prioritization"></a>Automaattinen tilitys ja priorisointi

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan tapahtumien tilitetään, jos Automaattinen tilitys -vaihtoehto on valittu Myyntireskontran parametrit -sivulla. Artikkelissa kerrotaan myös, miten automaattista tilitystä voi käyttää yhdessä maksun prioriteetin kanssa.

Sinulla on kaksi vaihtoehtoa, kun täsmäytät maksuja laskujen ja muiden tapahtumien kanssa. Voit manuaalisesti valita täsmäytettävät tapahtumat, tai järjestelmä voi valita tapahtumat automaattisesti automaattisella tilitystoiminnolla. Voit myös mukauttaa automaattisten tilitysten käsittelyä **Priorisoi selvitys** -vaihtoehdon avulla. Nämä asetukset ovat osa tilityksen parametreja, joka on määritetty **Myyntireskontran parametrit** -sivulla. Tapahtumien automaattinen täsmäytystapa voi poiketa automaattiseen täsmäytykseen käyttämästäsi menetelmästä riippuen. Käytettävissä ovat seuraavat menetelmät:

-   Käyttäjän määrittämä tilitysprioriteetti
-   Oletusarvoinen automaattinen tilitys

Seuraavissa osissa kuvataan, kuinka tapahtumat täsmäytetään jokaiselle menetelmälle.

## <a name="example-transactions"></a>Esimerkkitapahtumat
Myöhemmin tässä artikkelissa kuvatut tilitysesimerkit perustuvat seuraaviin tapahtumiin. Kaikki tapahtumat koskevat asiakasta 2050.

| Tapahtuma   | Päivämäärä        | Summa | Käteisalennuksen ehdot | Käteisalennuksen päivämäärä | Huomautukset                                                                                                                                                                                      |
|---------------|-------------|--------|---------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lasku 1     | 15. elokuuta   | 100,00 | 2%14, netto 30        | 29. elokuuta          |                                                                                                                                                                                               |
| Lasku 2     | 1. syyskuuta | 250,00 | 2%14, netto 30        | 15. syyskuuta       |                                                                                                                                                                                               |
| Lasku 3     | 15. lokakuuta  | 500,00 | 2 % 14/netto 30        | 29. lokakuuta         |                                                                                                                                                                                               |
| Korkolasku | 15. lokakuuta  | 7:00   |                     |                    | Tämä korkolasku on laskulle 1 ja laskulle 2. Summa lasketaan 2 prosentin korkona summista, jotka ovat vähintään 30 päivää myöhässä. Esimerkki: 0,02 × (100,00 + 250,00) = 7,00. |

## <a name="user-defined-settlement-priority"></a>Käyttäjän määrittämä tilitysprioriteetti
Jos valitset **Käytä automaattisten selvitysten priorisointia** -asetukseksi **Kyllä** **Myyntireskontran parametrit** -sivulla, **Tilitysprioriteetti**-sivulla määritettyä tilitysprioriteettia käytetään, kun tapahtumia valitaan automaattiseen tilitykseen. Tässä esimerkissä määritetään seuraava tilitysjärjestys:

1.  Tapahtumatyyppi
    -   Toimitusmaksut
    -   Maksukehotukset
    -   Korkolaskut
    -   Laskut

2.  Tapahtumapäivä, nouseva
3.  Tosite

Jos kirjaat 700,00:n maksun 25. lokakuuta, maksu tilitetään tapahtumiin seuraavassa järjestyksessä.

| Tosite       | Päivämäärä       | Lasku | Summa tapahtuman valuuttana | Täsmäytettävä summa | Saldo | Valuutta |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Korkolasku | 15.10.2015 |         | 7:00                           | 7:00             | 0,00    | USD      |
| Lasku 1     | 15.8.2015  | 10 001   | 100,00                         | 100,00           | 0,00    | USD      |
| Lasku 2     | 1.9.2015   | 10 002   | 250,00                         | 250,00           | 0,00    | USD      |
| Lasku 3     | 15.10.2015 |         | 500,00                         | 343,00           | 157,00  | USD      |

## <a name="default-automatic-settlement"></a>Oletusarvoinen automaattinen tilitys
Jos käyttäjäkohtaista tilitysprioriteettia ei ole, tapahtumat valitaan tilitykseen eräpäivän perusteella. Täsmäytettävillä tapahtumilla on oltava sama valuutta kuin tapahtumilla, joiden kanssa ne täsmäytetään. Jos 700,00:n maksu kirjataan 25. lokakuuta, seuraavat tapahtumat valitaan tilitystä varten.

| Tosite       | Päivämäärä       | Lasku | Summa tapahtuman valuuttana | Täsmäytettävä summa | Saldo | Valuutta |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Lasku 1     | 15.8.2015  | 10 001   | 100,00                         | 100,00           | 0,00    | USD      |
| Lasku 2     | 1.9.2015   | 10 002   | 250,00                         | 250,00           | 0,00    | USD      |
| Lasku 3     | 15.10.2015 |         | 500.00                         | 350.00           | 150.00  | USD      |
| Korkolasku | 15.10.2015 |         | 7.00                           | 0,00             | 7.00    | USD      |





