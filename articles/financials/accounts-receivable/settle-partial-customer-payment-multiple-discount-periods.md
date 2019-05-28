---
title: Useita alennuskausia sisältävän asiakkaan osamaksun tilittäminen
description: Tässä artikkelissa kerrotaan, miten osittaiset asiakkaan maksut tilitetään, kun alennuskausia on useita.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14471
ms.assetid: b633a7c4-c18d-42e7-91cc-adcdc8a3ba98
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 60c8b9b3a5aebed7e1a999335aab0baf83ea952a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558761"
---
# <a name="settle-a-partial-customer-payment-that-has-multiple-discount-periods"></a>Useita alennuskausia sisältävän asiakkaan osamaksun tilittäminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten osittaiset asiakkaan maksut tilitetään, kun alennuskausia on useita.

Fabrikam tarjoaa asiakkaalle 4031 kaksi käteisalennuskautta. Asiakas saa 2 prosentin käteisalennuksen, jos lasku maksetaan viiden päivän kuluessa, ja 1 prosentin käteisalennuksen, jos lasku maksetaan 14 päivän kuluessa. Fabrikam myöntää käteisalennukset myös osamaksuista. Tilityksen parametrit sijaitsevat **Myyntireskontran parametrit** -sivulla.

## <a name="invoice"></a>Lasku
Erik syöttää ja kirjaa 25. kesäkuuta laskun asiakkaalle 4031, jonka arvo on 1.000,00. Kun hän tarkastaa tämän laskun käteisalennukset, Erik näkee, että asiakas 4031 saa 20,00 arvoisen alennuksen, jos lasku maksetaan viimeistään 30. päivänä kesäkuuta. Jos lasku maksetaan viimeistään 9. päivänä heinäkuuta, asiakas saa 10,00 arvoisen alennuksen.

| Käteisalennuksen päivämäärä | Käteisalennussumma | Summa tapahtuman valuuttana |
|--------------------|----------------------|--------------------------------|
| 30.6.2015          | 20,00                | 980,00                         |
| 9.7.2015           | 10,00                | 990,00                         |
| 25.7.2015          | 0,00                 | 1 000,00                       |

Arnie voi tarkastella tapahtumaa **Asiakastapahtumat**-sivulla.

| Tosite   | Tapahtumatyyppi | Päivämäärä      | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo  | Valuutta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10030 | Lasku          | 25.6.2015 | 10030   | 1 000,00                             |                                       | 1 000,00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Osamaksu ennen käteisalennuspäivämäärää
Asiakas 4031 suorittaa 28. kesäkuuta 294,00 arvoisen osamaksun. Koska 28. kesäkuuta on ensimmäisen käteisalennuskauden aikana, asiakas saa alennusta 6,00 arvosta. **Selvitä tapahtumat** -sivun **Käteisalennussumma**-arvo on 20,00 ja **Käytettävä käteisalennussumma** on 6,00.

| Merkitse     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valittu | Normaali            | FTI-10030 | 4031    | 25.6.2015 | 25.7.2015 | 10030   | 1 000,00                       | USD      | 294,00           |

Alennustiedot näkyvät **Tilitä avoimet tapahtumat** -sivun alaosassa. Ellet muuta **Täsmäytettävä summa** -arvoksi **294,00**, **Käteisalennussumma** -kentän arvot vaihtelevat. Käteisalennuksena käytetään kuitenkin arvoa 6,00 maksun kirjaamisen yhteydessä, koska tilitys muuttaa **Täsmäytettävä summa** -arvon automaattisesti.

|                              |           |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 30.6.2015 |
| Käteisalennussumma         | 20,00     |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | 0,00      |
| Käytettävä käteisalennussumma | 6,00      |

Kun Arnie on kirjannut maksun, laskun saldo on 700,00.

## <a name="partial-payment-before-the-second-cash-discount-date"></a>Osamaksu ennen toista käteisalennuspäivämäärää
Asiakas maksaa laskun loppusumman 8. heinäkuuta. Koska maksu suoritetaan toisella käteisalennusjaksolla, siitä vähennetään 7,00:n arvoinen alennus (1 prosentti).

| Merkitse     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Valuutta | Täsmäytettävä summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valittu | Normaali            | FTI-10030 | 4031    | 25.6.2015 | 25.7.2015 | 10030   | 700,00                               |                                       | USD      | 693,00           |

Alennustiedot näkyvät **Tilitä avoimet tapahtumat** -sivun alaosassa.

|                              |           |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 9.7.2015 |
| Käteisalennussumma         | 30,00     |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | 6,00      |
| Käytettävä käteisalennussumma | 7:00      |

Laskun saldo on nyt 0,00. Arnie tarkastelee tietoja **Asiakastapahtumat**-sivulla.

| Tosite    | Tapahtumatyyppi | Päivämäärä      | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo | Valuutta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10030  | Lasku          | 25.6.2015 | 10030   | 1 000,00                             |                                       | 0,00    | USD      |
| ARP-10030  |  Maksu         | 28.6.2015 |         |                                      | 294,00                                | 0,00    | USD      |
| ALE-10030 |  Käteisalennus   | 28.6.2015 |         |                                      | 6,00                                  | 0,00    | USD      |
| ARP-10031  |  Maksu         | 8.7.2015  |         |                                      | 693,00                                | 0,00    | USD      |
| ALE-1031  |  Käteisalennus   | 8.7.2015  |         |                                      | 7:00                                  | 0,00    | USD      |





