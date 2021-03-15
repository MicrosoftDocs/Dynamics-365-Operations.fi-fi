---
title: Toimittajan osamaksun ja lopullisen maksun täydellinen tilittäminen ennen alennuspäivämäärää
description: Tämä artikkeli opastaa sinua skenaariossa, jossa osittaisia maksuja suoritetaan toimittajan laskulle ja käytetään käteisalennusta.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14431
ms.assetid: 6b8e3420-b4c9-4e02-9588-598fe6d3df0d
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1aaedddae59b1a4883ac737d30436d8d7268103f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979410"
---
# <a name="settle-a-partial-vendor-payment-and-the-final-payment-in-full-before-the-discount-date"></a>Toimittajan osamaksun ja lopullisen maksun täydellinen tilittäminen ennen alennuspäivämäärää

[!include [banner](../includes/banner.md)]

Tämä artikkeli opastaa sinua skenaariossa, jossa osittaisia maksuja suoritetaan toimittajan laskulle ja käytetään käteisalennusta.

Fabrikam ostaa tavaraa toimittajalta 3064. Toimittaja antaa Fabrikamille 1 prosentin käteisalennuksen, jos lasku maksetaan 14 päivän kuluessa. Laskut on maksettava 30 päivän kuluessa. Lisäksi toimittaja antaa Fabrikamille käteisalennukset osamaksuista. Tilityksen parametrit sijaitsevat **Ostoreskontran parametrit** -sivulla. April syöttää 25. kesäkuuta 1 000,00 arvoisen laskun toimittajalle 3064.

## <a name="vendor-invoice-on-june-25"></a>Toimittajan lasku 25. kesäkuuta
April syöttää ja kirjaa 25. kesäkuuta laskun toimittajalle 3064, jonka arvo on 1.000,00. April voi tarkastella tapahtumia **Toimittajatapahtumat**-sivulla.

| Tosite   | Päivämäärä      | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo   | Valuutta |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Var-10010 | 25.6.2015 | 10010   |                                      | 1 000,00                              | -1 000,00 | USD      |

**Toimittajat**-sivulla April avaa **Selvitä tapahtumat** -sivun. Hän voi käyttää **Selvitä tapahtumat** -sivua tarkastellakseen käteisalennusten päivämääriä ja summia. Eräpäivä on 25. heinäkuuta ja -10,00:n arvoinen käteisalennus on käytettävissä, jos lasku maksetaan viimeistään 9. heinäkuuta.

| Merkitse | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normaali            | Var-10010 | 3064    | 25.6.2015 | 25.7.2015 | 10010   | 1 000,00                       | USD      | 990,00           |

Alennustiedot näkyvät **Tilitä avoimet tapahtumat**-sivun alaosassa.

|       &nbsp;                 | &nbsp;    |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 9.7.2015 |
| Käteisalennussumma         | –10,00    |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | 0,00      |
| Käytettävä käteisalennussumma | –10,00    |

April napsauttaa **Käteisalennus**-välilehteä tarkastellakseen alennussummaa.

| Käteisalennuksen päivämäärä | Käteisalennussumma | Summa tapahtuman valuuttana |
|--------------------|----------------------|--------------------------------|
| 9.7.2015           | 10,00                | 990,00                         |
| 25.7.2015          | 0,00                 | 1 000,00                       |

## <a name="partial-payment-on-july-1-by-using-the-settle-transactions-page"></a>Osamaksu 1. heinäkuuta käyttäen Selvitä tapahtumat -sivua
April voi luoda maksulle kirjauskansion avaamalla **Maksukirjauskansio**-sivun ostoreskontrasta. Hän luo uuden maksun kirjauskansion ja lisää rivin toimittajalle 3064. Tämän jälkeen hän avaa **Selvitä tapahtumat** -sivun, jotta hän voi merkitä laskun tilitettäväksi. April merkitsee laskun ja muuttaa **Tilitettävä summa** -kentän arvoksi **-500.00**. Hän huomaa, että **Tilitettävä summa** -kentän arvo koko laskulle on **-10,00** ja että **Käytettävä käteisalennussumma** -kentän arvo on **-5,05**. April selvittää siis tämän laskun summaksi -505,05.

| Merkitse     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valittu | Normaali            | FTI-10010 | 4028    | 25.6.2015 | 25.7.2015 | 10010   | 1 000,00                       | USD      | -500,00          |

Alennustiedot näkyvät **Tilitä avoimet tapahtumat** -sivun alaosassa.

|  &nbsp;                      |  &nbsp;   |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 9.7.2015 |
| Käteisalennussumma         | –10,00    |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | 0,00      |
| Käytettävä käteisalennussumma | -5,05     |

April haluaa selvittää täsmälleen puolet laskusta. Hän muuttaa siis laskun **Tilitettävä summa** -kentän arvoksi **-495.00**. Niinpä tilitettävä summa on nyt yhteensä 500,00. Summa sisältää käteisalennuksen, jonka arvo on -5,00.

| Merkitse     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valittu | Normaali            | FTI-10010 | 4028    | 25.6.2015 | 25.7.2015 | 10010   | 1 000,00                       | USD      | -495,00          |

Alennustiedot näkyvät **Tilitä avoimet tapahtumat** -sivun alaosassa.

|  &nbsp;                      |  &nbsp;   |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 9.7.2015 |
| Käteisalennussumma         | –10,00    |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | 0,00      |
| Käytettävä käteisalennussumma | -5,00     |

April sulkee **Selvitä tapahtumat** -sivun. Kirjauskansioon luodaan maksurivi summalle 495,00, jonka jälkeen April kirjaa kirjauskansion. April voi tarkastella toimittajan tapahtumia **Toimittajatapahtumat**-sivulla. Hän näkee, että laskun saldo on -500,00. Näkyvillä ovat myös maksu (495,00) ja käteisalennus (5,00).

| Tosite    | Tapahtumatyyppi | Päivämäärä      | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo | Valuutta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Var-10010  | Lasku          | 25.6.2015 | 10010   |                                      | 1 000,00                              | -500,00 | USD      |
| HYV-10010  | Maksu          | 1.7.2015  |         | 495,00                               |                                       | 0,00    | USD      |
| ALE-10010 | Käteisalennus    | 7.1.2015  |         | 5,00                                 |                                       | 0,00    | USD      |

## <a name="remaining-amount-paid-on-july-8"></a>Jäljellä oleva summa maksettu 8. heinäkuuta
April maksaa loput toimittajan 3064 laskusta 8. heinäkuuta, joka on vielä käteisalennuskaudella. April luo maksukirjauskansion 8. heinäkuuta ja merkitsee tapahtuman selvitettäväksi. Hän näkee, että selvitettävä summa on 495,00. **Arvioitu käteisalennus** -kentän arvo on **-5,00**, alennuksesta on jo aiemmin käytetty 5,00.

|  &nbsp;                 |  &nbsp; |
|-------------------------|--------|
| Merkitty kokonaissumma            | 495,00 |
| Arvioitu käteisalennus | -5,00  |

Valittua tapahtumaa koskevat tiedot näkyvät **Tilitä avoimet tapahtumat** -sivun ruudukossa.

| Merkitse     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valittu | Normaali            | FTI-10010 | 4028    | 25.6.2015 | 25.7.2015 | 10010   | 1 000,00                       | USD      | 495,00           |

Alennustiedot näkyvät **Tilitä avoimet tapahtumat** -sivun alaosassa.

|  &nbsp;                      | &nbsp;    |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 9.7.2015 |
| Käteisalennussumma         | 10,00     |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | 5,00      |
| Käytettävä käteisalennussumma | 5,00      |

April kirjaa maksukirjauskansion ja tarkistaa toimittajan tapahtumat **Toimittajatapahtumat**-sivulta. Laskun saldo on nyt 0,00, ja April näkee kaksi maksua ja kaksi käteisalennusta.

| Tosite    | Tapahtumatyyppi | Päivämäärä      | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo | Valuutta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Var-10010  | Lasku          | 25.6.2015 | 10010   |                                      | 1 000,00                              | 0,00    | USD      |
| HYV-10010  |  Maksu         | 7.1.2015  |         | 495,00                               |                                       | 0,00    | USD      |
| ALE-10010 | Käteisalennus    | 7.1.2015  |         | 5,00                                 |                                       | 0,00    | USD      |
| HYV-10011  | Maksu          | 8.7.2015  |         | 495,00                               |                                       | 0,00    | USD      |
| ALE-10011 | Käteisalennus    | 8.7.2015  |         | 5,00                                 |                                       | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]