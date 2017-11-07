---
title: "Asiakkaan osamaksun tilittäminen ennen alennuspäivämäärää, kun lopullinen maksu suoritetaan alennuspäivämäärän jälkeen"
description: "Tässä artikkelissa käsitellään maksujen laskuille tilittämisen vaikutusta asiakkaille. Skenaariossa keskitytään vaikutuksiin alareskontrassa (ei kirjanpidossa)."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14584
ms.assetid: e54936f5-053b-4ed3-b778-42c7e9aeb7cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cc71e9257462983d42fd71bf19728add359e261d
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="settle-a-partial-customer-payment-before-the-discount-date-with-a-final-payment-after-the-discount-date"></a>Asiakkaan osamaksun tilittäminen ennen alennuspäivämäärää, kun lopullinen maksu suoritetaan alennuspäivämäärän jälkeen

[!include[banner](../includes/banner.md)]


Tässä artikkelissa käsitellään maksujen laskuille tilittämisen vaikutusta asiakkaille. Skenaariossa keskitytään vaikutuksiin alareskontrassa (ei kirjanpidossa).

Fabrikam myy tavaroita asiakkaalle 4027. Fabrikam tarjoaa 1 prosentin käteisalennuksen, jos lasku maksetaan 14 päivän kuluessa. Laskut on maksettava 30 päivän kuluessa. Fabrikam myöntää käteisalennukset myös osamaksuista. Tilityksen parametrit sijaitsevat **Myyntireskontran parametrit** -sivulla.

## <a name="invoice"></a>Lasku
Erik syöttää ja kirjaa 25. kesäkuuta laskun asiakkaalle 4027, jonka arvo on 1000,00. Erik voi tarkastella tätä laskua käyttämällä **Tapahtumat**-painiketta, joka on **Asiakkaat**-sivulla.

| Tosite   | Tapahtumatyyppi | Päivämäärä      | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo  | Valuutta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10020 | Lasku          | 25.6.2015 | 10020   | 1 000,00                             |                                       | 1 000,00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Osamaksu ennen käteisalennuspäivämäärää
Asiakas 4027 maksaa 2. heinäkuuta laskusta osamaksuerän, jonka suuruus on 297,00. Maksu on oikeutettu käteisalennukseen, koska Fabrikam myöntää käteisalennuksia osamaksuista ja osamaksu suoritetaan ennen käteisalennuspäivämäärää. Siten asiakas 4027 käyttää käteisalennuksen, jonka suuruus on 3,00. Arnie tallentaa asiakkaan 4027 maksun maksukirjauskansion avulla. Tämän jälkeen Arnie avaa **Selvitä tapahtumat** -sivun, jotta hän voi merkitä laskun tilitettäväksi.

| Merkitse     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana debet | Valuutta | Täsmäytettävä summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Valittu | Normaali            | FTI-10020 | 4027    | 25.6.2015 | 25.7.2015 | 10020   | 1 000,00                             | USD      | 297,00           |

Alennustiedot näkyvät **Tilitä avoimet tapahtumat** -sivun alaosassa. Ellet muuta **Täsmäytettävä summa** -arvoksi 297,00, näkyviin tulevat **Käteisalennussumma**-arvot vaihtelevat. Käteisalennuksena käytetään kuitenkin arvoa 3,00 maksun kirjaamisen yhteydessä, koska tilitys muuttaa **Täsmäytettävä summa** -arvon automaattisesti.

|                              |           |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 9.7.2015 |
| Käteisalennussumma         | 10,00     |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | 0,00      |
| Käytettävä käteisalennussumma | 3,00      |

Arnie kirjaa tämän maksun. Lasku saldo on nyt 700,00. Seuraavat tapahtumat näkyvät asiakkaalle.

| Tosite    | Tapahtumatyyppi | Päivämäärä      | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo | Valuutta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10020  | Lasku          | 25.6.2015 | 10020   | 1 000,00                             |                                       | 700,00  | USD      |
| ARP-10020  |  Maksu         | 1.7.2015  |         |                                      | 297,00                                | 0,00    | USD      |
| ALE-10020 |  Käteisalennus   | 1.7.2015  |         |                                      | 3,00                                  | 0,00    | USD      |

## <a name="remaining-payment-after-the-cash-discount-date"></a>Jäljellä oleva maksu käteisalennuspäivämäärän jälkeen
Asiakas 4027 maksaa loppulaskun 11. heinäkuuta, joka on alennusjakson jälkeen. Alennussummaa ei näy **Selvitä tapahtumat** -sivun **Arvioitu käteisalennus** -kentässä, ja **Käteisalennussumma**-kentässä arvona on **0,00**. Kun asiakas 4027 maksaa jäljellä olevan summan 700,00, lisäalennusta ei myönnetä.

| Merkitse     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana debet | Valuutta | Täsmäytettävä summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Valittu | Normaali            | FTI-10020 | 4027    | 25.6.2015 | 25.7.2015 | 10020   | 700,00                               | USD      | 700,00           |

Alennustiedot näkyvät **Tilitä avoimet tapahtumat** -sivun alaosassa.

|                              |           |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 9.7.2015 |
| Käteisalennussumma         | 0,00      |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | 3,00      |
| Käytettävä käteisalennussumma | 0,00      |

Jos Arnie muuttaa **Käytä käteisalennusta** -kentän arvoksi **Aina**, **Laske käteisalennukset osamaksuille** -asetus ohitetaan ja käteisalennus käytetään. Maksusummaksi muuttuu 693,00 ja käteisalennus on jäljellä oleva 7,00.

| Merkitse     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Valuutta | Täsmäytettävä summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valittu | Aina            | FTI-10020 | 4027    | 25.6.2015 | 25.7.2015 | 10020   | 700,00                               |                                       | USD      | 693,00           |

Alennustiedot näkyvät **Tilitä avoimet tapahtumat** -sivun alaosassa.

|                              |           |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 9.7.2015 |
| Käteisalennussumma         | 7:00      |
| Käytä käteisalennusta            | Aina    |
| Käytetty käteisalennus          | 3,00      |
| Käytettävä käteisalennussumma | 7:00      |

Arnie palauttaa **Käytä käteisalennusta** -kentän arvoksi **Normaali**, sillä hän ei anna asiakkaan käyttää jäljellä olevaa käteisalennusta 7,00. Tämän jälkeen Arnie kirjaa maksun. Kun Arnie avaa **Asiakastapahtumat**-sivun, hän näkee, että laskun saldo on 0,00. Hän näkee myös, että maksuja on kaksi. Toisen summa on 297,00 ja käteisalennus 3,00, ja toisen summa on 700,00.

| Tosite    | Tapahtumatyyppi | Päivämäärä      | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo | Valuutta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10020  | Lasku          | 25.6.2015 | 10020   | 1 000,00                             |                                       | 0,00    | USD      |
| ARP-10020  |                  | 1.7.2015  |         |                                      | 297,00                                | 0,00    | USD      |
| ALE-10020 |                  | 1.7.2015  |         |                                      | 3,00                                  | 0,00    | USD      |
| ARP-10021  |                  | 11.7.2015 |         |                                      | 700,00                                | 0,00    | USD      |






