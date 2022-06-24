---
title: Osamaksun tilittäminen ennen alennuspäivämäärää, kun viimeinen maksu suoritetaan alennuspäivämäärän jälkeen
description: Tässä artikkelissa käydään läpi skenaario, jossa suoritetaan useita osittaisia maksuja, joista osa on käteisalennuskaudella ja osa käteisalennuskauden ulkopuolella.
author: abruer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14411
ms.assetid: 302ad6ae-28ee-4899-9f6b-f74424a5f50c
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e249be4024ee6581060e3890795770054c6ab67
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871359"
---
# <a name="settle-partial-payment-before-discount-date-and-final-payment-after-discount-date"></a>Osamaksun tilittäminen ennen alennuspäivämäärää, kun viimeinen maksu suoritetaan alennuspäivämäärän jälkeen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käydään läpi skenaario, jossa suoritetaan useita osittaisia maksuja, joista osa on käteisalennuskaudella ja osa käteisalennuskauden ulkopuolella.

Fabrikam ostaa tavaraa toimittajalta 3057. Fabrikam saa 1 prosentin käteisalennuksen, jos lasku maksetaan 14 päivän kuluessa. Laskut on maksettava 30 päivän kuluessa. Lisäksi toimittaja antaa Fabrikamille käteisalennukset osamaksuista. Tilityksen parametrit sijaitsevat **Ostoreskontran parametrit** -sivulla.

## <a name="invoice-on-june-25"></a>Lasku 25.6.
April syöttää ja kirjaa 25. kesäkuuta laskun toimittajalle 3057, jonka arvo on 1.000,00. April voi tarkastella tapahtumia **Toimittajatapahtumat**-sivulla.

| Tosite   | Tapahtumatyyppi | Päivämäärä      | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo   | Valuutta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Lku-10020 | Lasku          | 25.6.2015 | 10020   |                                      | 1 000,00                              | -1 000,00 | USD      |

## <a name="partial-payment-on-july-2"></a>Osamaksu 2.7.
2. heinäkuuta April haluaa tilittää 300,00 tästä laskusta. Maksu on oikeutettu alennukseen, koska saa alennuksen osamaksuista. Siksi April maksaa 297,00 ja käyttää 3,00:n alennuksen. Hän luo maksun kirjauskansion ja lisää rivin toimittajalle 3057. Tämän jälkeen hän avaa **Selvitä tapahtumat** -sivun, jotta hän voi merkitä laskun tilitettäväksi.

| Merkitse     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valittu | Normaali            | Lku-10020 | 3057    | 25.6.2015 | 25.7.2015 | 10020   | -1 000,00                      | USD      | -297,00          |

Alennustiedot näkyvät **Tilitä avoimet tapahtumat**-sivun alaosassa.

| Kenttä                        | Arvo     |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 9.7.2015 |
| Käteisalennussumma         | -10,00    |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | 0,00      |
| Käytettävä käteisalennussumma | -3,00     |

April kirjaa sitten maksun. Lasku saldo on nyt 700,00. April voi tarkastella tapahtumia **Toimittajatapahtumat**-sivulla.

| Tosite    | Tapahtumatyyppi | Päivämäärä      | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo | Valuutta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Lku-10020  | Lasku          | 25.6.2015 | 10020   |                                      | 1 000,00                              | -700,00 | USD      |
| HYV-10020  | Maksu          | 7.1.2015  |         | 297,00                               |                                       | 0,00    | USD      |
| ALE-10020 | Käteisalennus    | 7.1.2015  |         | 3,00                                 |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--normal"></a>Jäljellä oleva maksu 15.7. käytössä käteisalennus = normaali
April maksaa loput laskusta 15.7, joka on alennuskauden jälkeen. Alennussummaa ei näy **Tilitä avoimet tapahtumat** -sivun **Arvioitu käteisalennus** -kentässä, ja **Käteisalennussumma**-kentässä arvona on **0,00**. Kun April maksaa jäljellä olevan summan 700,00, lisäalennusta ei myönnetä.

| Merkitse     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valittu | Normaali            | Lku-10020 | 3057    | 25.6.2015 | 25.7.2015 | 10020   | -700,00                        | USD      | -700,00          |

Alennustiedot näkyvät **Selvitä tapahtumat** -sivun alaosassa. April näkee, että hän on jo käyttänyt 3,00:n alennuksen.

| Kenttä                        | Arvo     |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 9.7.2015 |
| Käteisalennussumma         | 0,00      |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | -3,00     |
| Käytettävä käteisalennussumma | 0,00      |

April kirjaa sitten maksun. Kun hän avaa **Toimittajatapahtumat**-sivun, hän näkee, että laskun saldo on 0,00. Hän näkee myös, että maksuja on kaksi. Toisen summa on 297,00, ja siinä on alennus 3,00, ja toisen summa on 700,00.

| Tosite    | Tapahtumatyyppi | Päivämäärä      | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo | Valuutta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Lku-10020  | Lasku          | 25.6.2015 | 10020   |                                      | 1 000,00                              | 0,00    | USD      |
| HYV-10020  | Maksu          | 1.7.2015  |         | 297,00                               |                                       | 0,00    | USD      |
| ALE-10020 | Käteisalennus    | 7.1.2015  |         | 3,00                                 |                                       | 0,00    | USD      |
| HYV-10021  | Maksu          | 15.7.2015 |         | 700,00                               |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--always"></a>Jäljellä oleva maksu 15.7. käytössä käteisalennus = aina
Jos toimittaja sallii alennuksen käyttämisen, vaikka April on maksamassa laskun alennuspäivämäärän jälkeen, hän voi muuttaa **Käytä käteisalennusta** kentän arvoksi **Aina**. **Laske käteisalennukset osamaksulle** -asetus ohitetaan ja alennus otetaan käyttöön. Maksusumma on 693,00 ja alennus on jäljellä oleva 7,00.

| Merkitse     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Valuutta | Täsmäytettävä summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valittu | Aina            | Lku-10020 | 3057    | 25.6.2015 | 25.7.2015 | 10020   | 700,00                               |                                       | USD      | -693,00          |

Alennustiedot näkyvät **Selvitä tapahtumat** -sivun alaosassa.

| Kenttä                        | Arvo     |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 9.7.2015 |
| Käteisalennussumma         | 7.00      |
| Käytä käteisalennusta            | Aina    |
| Käytetty käteisalennus          | -3,00     |
| Käytettävä käteisalennussumma | -7,00     |

April kirjaa sitten maksun. Kun hän avaa **Toimittajatapahtumat**-sivun, hän näkee, että laskun saldo on 0,00. Hän näkee myös, että maksuja on kaksi. Toinen maksu on 297,00 ja siinä on alennus 3,00, kun taas toinen maksu on 693,00 ja siinä on alennus 7,00.

| Tosite    | Tapahtumatyyppi | Päivämäärä      | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo | Valuutta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Lku-10020  | Lasku          | 25.6.2015 | 10020   |                                      | 1 000,00                              | 0,00    | USD      |
| HYV-10020  | Maksu          | 1.7.2015  |         | 297,00                               |                                       | 0,00    | USD      |
| ALE-10020 | Käteisalennus    | 1.7.2015  |         | 3,00                                 |                                       | 0,00    | USD      |
| HYV-10021  | Maksu          | 15.7.2015 |         | 693,00                               |                                       | 0,00    | USD      |
| ALE-10021 | Käteisalennus    | 15.7.2015 |         | 7:00                                 |                                       | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
