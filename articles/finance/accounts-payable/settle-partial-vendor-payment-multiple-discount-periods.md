---
title: Useita alennuskausia sisältävän toimittajan osamaksun tilittäminen
description: Tämä artikkeli opastaa sinua skenaariossa, jossa useita osittaisia maksuja suoritetaan toimittajalle, jolla on useita käteisalennuksia.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14262
ms.assetid: af95c48a-afd1-476c-978d-e34995100be4
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56e2b3a8dadd824fa0170a1db19fffeaecb47775
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827863"
---
# <a name="settle-a-partial-vendor-payment-that-has-multiple-discount-periods"></a>Useita alennuskausia sisältävän toimittajan osamaksun tilittäminen

[!include [banner](../includes/banner.md)]

Tämä artikkeli opastaa sinua skenaariossa, jossa useita osittaisia maksuja suoritetaan toimittajalle, jolla on useita käteisalennuksia. 

Toimittaja 3054 myöntää Fabrikamille 2 prosentin käteisalennuksen, jos lasku maksetaan viiden päivän kuluessa, ja 1 prosentin käteisalennuksen, jos lasku maksetaan 14 päivän kuluessa.

## <a name="invoice"></a>Lasku
April luo 28. kesäkuuta 1 000,00 arvoisen laskun toimittajalle 3054. April voi tarkastella tapahtumia **Toimittajatapahtumat**-sivulla.

| Tosite   | Päivämäärä      | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo   | Valuutta |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Var-10060 | 28.6.2015 | 10060   |                                      | 1 000,00                              | -1 000,00 | USD      |

Laskuun voidaan liittää seuraavat käteisalennuspäivämäärät ja -summat.

| Käteisalennuksen päivämäärä | Käteisalennussumma | Summa tapahtuman valuuttana |
|--------------------|----------------------|--------------------------------|
| 3.7.2015           | 20,00                | 980,00                         |
| 12.7.2015          | 10,00                | 990,00                         |
| 25.7.2015          | 0,00                 | 1 000,00                       |

## <a name="payment-on-july-2"></a>Maksu 2. heinäkuuta
2. heinäkuuta April haluaa maksaa 300,00 tästä laskusta. Hän luo kertamaksun käyttämällä ostoreskontran **Maksukirjauskansio**-sivua. Hän lisää rivin toimittajalle 3054 ja syöttää maksusummaksi **300,00**. Tämän jälkeen April avaa **Selvitä tapahtumat** -sivun, jotta hän voi merkitä tilitettävän laskun. Hän päivittää **Tilitettävä summa** -kenttään arvoksi **300,00** ja huomaa, että **Käytettävä käteisalennussumma** -kentän arvoksi muuttuu **6,12**. Koska maksu suoritetaan ensimmäisellä alennusjaksolla, siitä vähennetään 2 prosentin alennus.

| Merkitse | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normaali            | Var-10060 | 3054    | 28.6.2015 | 28.7.2015 | 10060   | 1 000,00                       | USD      | 300,00           |

Alennustiedot näkyvät **Tilitä avoimet tapahtumat**-sivun alaosassa.

| Kenttä                        | Arvo     |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 2.7.2015 |
| Käteisalennussumma         | -20,00    |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | 0,00      |
| Käytettävä käteisalennussumma | -6,12     |

Koska käteisalennus on käytettävissä, April haluaa muuttaa maksusummaa siten, että sekä maksun että käteisalennuksen tilitetty summa on yhteensä 300,00. Hän muuttaa **Tilitettävä summa** -kentän arvoksi **294,00** ja huomaa, että **Käytettävä käteisalennussumma** -kentän arvoksi muuttuu **6,00**.

| Merkitse | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normaali            | Var-10060 | 3054    | 28.6.2015 | 28.7.2015 | 10060   | 1 000,00                       | USD      | 294,00           |

Alennustiedot näkyvät **Tilitä avoimet tapahtumat**-sivun alaosassa.

| Kenttä                        | Arvo     |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 2.7.2015 |
| Käteisalennussumma         | -20,00    |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | 0,00      |
| Käytettävä käteisalennussumma | -6,00     |

April kirjaa maksun. Hän voi tarkastella tapahtumia **Toimittajatapahtumat**-sivulla. Hän näkee, että laskuun on kohdistettu summa 300,00. Summa sisältää alennuksen, jonka arvo on 6,00. Niinpä jäljelle jäävä saldo on 700,00.

| Tosite    | Päivämäärä      | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo | Valuutta |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Var-10060  | 28.6.2015 | 10060   |                                      | 1 000,00                              | -700,00 | USD      |
| HYV-10060  | 2.7.2015  |         | 294,00                               |                                       | 0,00    | USD      |
| ALE-10060 | 2.7.2015  |         | 6,00                                 |                                       | 0,00    | USD      |

## <a name="payment-on-july-8"></a>Maksu 8. heinäkuuta
April suorittaa 8. heinäkuuta lisämaksun laskulle. Hän avaa **Selvitä tapahtumat** -sivun ja napsauttaa **Käteisalennus**-välilehteä, jotta hän voi syöttää summan. Hän näkee kahden käytettävissä olevan käteisalennuksen päivämäärät ja summat. Koska maksu suoritetaan toisella alennusjaksolla, siitä vähennetään 1 prosentin alennus (5,00). Summaksi lasketaan puolet 1 prosentin alennuksesta summalle 1 000,00 tai puolet arvosta 10,00.

| Käteisalennuksen päivämäärä | Käteisalennussumma | Summa tapahtuman valuuttana |
|--------------------|----------------------|--------------------------------|
| 3.7.2015           | 20,00                | 680,00                         |
| 12.7.2015          | 10,00                | 690,00                         |
| 25.7.2015          | 0,00                 | 700,00                         |

April päättää maksaa 495,00 ja käyttää käteisalennuksen 5,00. Niinpä tilitettävä summa on yhteensä 500,00.

| Merkitse | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normaali            | Var-10060 | 3054    | 28.6.2015 | 28.7.2015 | 10060   | 1 000,00                       | USD      | 495,00           |

Alennustiedot näkyvät **Tilitä avoimet tapahtumat**-sivun alaosassa.

| Kenttä                        | Arvo     |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 12.7.2015 |
| Käteisalennussumma         | -10,00    |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | -6,00     |
| Käytettävä käteisalennussumma | -5,00     |

April näkee **Toimittajatapahtumat**-sivulla, että uusi saldo on 200,00.

| Tosite    | Päivämäärä      | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo | Valuutta |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Var-10060  | 28.6.2015 | 10060   |                                      | 1 000,00                              | -200,00 | USD      |
| HYV-10060  | 2.7.2015  |         | 294,00                               |                                       | 0,00    | USD      |
| ALE-10060 | 2.7.2015  |         | 6,00                                 |                                       | 0,00    | USD      |
| HYV-10061  | 12.7.2015 |         | 495,00                               |                                       | 0,00    | USD      |
| ALE-10061 | 12.7.2015 |         | 5,00                                 |                                       | 0,00    | USD      |

## <a name="payment-on-july-20"></a>Maksu 20. heinäkuuta
April luo 20. heinäkuuta lopullisen maksun, jonka summa on 200,00. Alennusta ei käytetä, koska maksu suoritetaan molempien alennusjaksojen jälkeen. Laskun saldo on 0,00.

| Tosite    | Päivämäärä      | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo | Valuutta |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Var-10060  | 28.6.2015 | 10060   |                                      | 1 000,00                              | -200,00 | USD      |
| HYV-10060  | 2.7.2015  |         | 294,00                               |                                       | 0,00    | USD      |
| ALE-10060 | 2.7.2015  |         | 6,00                                 |                                       | 0,00    | USD      |
| HYV-10061  | 12.7.2015 |         | 495,00                               |                                       | 0,00    | USD      |
| ALE-10061 | 12.7.2015 |         | 5,00                                 |                                       | 0,00    | USD      |
| HYV-10062  | 20.7.2015 |         | 200,00                               |                                       | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]