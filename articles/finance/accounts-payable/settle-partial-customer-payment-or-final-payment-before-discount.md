---
title: Osamaksun ja viimeisen maksun tilittäminen kokonaan ennen alennuspäivämäärää
description: Tässä artikkelissa on skenaarioita, jotka kuvaavat osittaisten maksujen kirjaamista asiakkaalle ja käteisalennusten käyttämistä käteisalennusjaksolla.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 14491
ms.assetid: 0f07d3ce-a439-43ed-a22e-957ccd36a37b
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
ms.openlocfilehash: a8da366b1e770ea649603ae85d4acc5e377ed9fb
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780496"
---
# <a name="settle-partial-and-final-payments-in-full-before-the-discount-date"></a>Osamaksun ja viimeisen maksun tilittäminen kokonaan ennen alennuspäivämäärää

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on skenaarioita, jotka kuvaavat osittaisten maksujen kirjaamista asiakkaalle ja käteisalennusten käyttämistä käteisalennusjaksolla.

Fabrikam myy tavaroita asiakkaalle 4028. Fabrikam tarjoaa 1 prosentin käteisalennuksen, jos lasku maksetaan 14 päivän kuluessa. Laskut on maksettava 30 päivän kuluessa. Fabrikam myöntää käteisalennukset myös osamaksuista. Tilityksen parametrit sijaitsevat **Myyntireskontran parametrit** -sivulla.

## <a name="customer-invoice"></a>Myyntilasku
Erik syöttää ja kirjaa 25. kesäkuuta laskun asiakkaalle 4028, jonka arvo on 1.000,00. Arnie voi tarkastella tapahtumaa **Asiakastapahtumat**-sivulla.

| Tosite   | Tapahtumatyyppi | Päivämäärä      | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo  | Valuutta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10010 | Lasku          | 25.6.2020 | 10010   | 1,000.00                             |                                       | 1,000.00 | USD      |

Arnie avaa **Selvitä tapahtumat** -sivun **Asiakas**- tai **Asiakastapahtumat**-sivulta tarkastellakseen päivämääriä sekä laskulle saatavilla olevia käteisalennuksia. Eräpäivä on 25. heinäkuuta ja 10,00:n arvoinen käteisalennus on käytettävissä, jos lasku maksetaan viimeistään 9. heinäkuuta.

| Merkitse     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valittu | Normaali            | FTI-10010 | 4028    | 25.6.2020 | 25.7.2020 | 10010   | 1,000.00                       | USD      | 990.00           |

Hyvityslaskun alennustiedot näkyvät merkityn laskun **Selvitä tapahtumat** -sivun alaosassa.

|    &nbsp;                    |  &nbsp;   |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 9.7.2020 |
| Käteisalennussumma         | 10.00     |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | 0,00      |
| Käytettävä käteisalennussumma | 10,00     |

Arnie napsauttaa **Käteisalennus**-välilehteä tarkastellakseen alennussummaa.

| Käteisalennuksen päivämäärä | Käteisalennussumma | Summa tapahtuman valuuttana |
|--------------------|----------------------|--------------------------------|
| 9.7.2020           | 10.00                | 990.00                         |
| 25.7.2020          | 0,00                 | 1,000.00                       |

## <a name="partial-payment-by-using-the-enter-customer-payments-page"></a>Osamaksu Lisää asiakkaan maksuja -sivun avulla
Asiakas 4028 lähettää 500,00 arvoisen maksun 1. heinäkuuta. Erik ei napsauta **Rivit**-kohtaa kirjatakseen tämän maksun. Sen sijaan, Erik kirjaa maksun luomalla uuden maksukirjauskansion ja avaamalla sitten **Lisää asiakkaan maksuja** -sivun. Erik syöttää maksutiedot ja merkitsee kirjaamansa laskun. Kun Erik kirjaa summaksi **500,00**, hän kirjoittaa myös **500,00** ruudukon **Maksettava summa** -kenttään. Koska Fabrikam voi antaa käteisalennuksen osamaksuille, Erik huomaa, että maksulle käytetään myös osittaista, 5,05:n arvoista käteisalennusta. Tämä alennus lasketaan seuraavasti: 500,00 / 0,99 × 0,01 = 5,05. (Tässä laskutoimituksessa 500,00 jaetaan 0,99:llä, koska alennus on 1 prosentti. Tällöin asiakas maksaa laskusta 99 prosenttia. Tulos kerrotaan sitten alennusprosentilla eli 1 prosentilla – 0,01. Jos asiakkaalle käytetään 10,00:n arvoista alennusta kokonaisuudessaan, selvitettävä summa olisi 990,00.) Alennustiedot tulevat **Lisää asiakkaan maksuja** -sivun alalaidan ruudukkoon.

| Käytettävä käteisalennussumma | Käytetty käteisalennus | Maksettava summa |
|------------------------------|---------------------|---------------|
| 5,05                         | 0,00                | 500,00        |

## <a name="partial-payment-by-using-the-journal-lines"></a>Osamaksu kirjauskansiorivien avulla
**Lisää asiakkaan maksuja** -sivun avaamisen sijaan Arnie voi napsauttaa kirjauskansiossa **Rivit** -kohtaa kirjatakseen maksun. Näyttöön tulee maksujen kirjauskansio, jossa Erik voi syöttää rivin asiakkaalle 4028. Tämän jälkeen Arnie avaa **Selvitä tapahtumat** -sivun, jotta hän voi merkitä laskun tilitettäväksi. Arnie merkitsee laskun ja muuttaa **Tilitettävä summa** -kentän arvoksi **500,00**. Erik huomaa jälleen, että **Tilitettävä summa** -kentän arvo koko laskulle on **10,00** ja että **Käytettävä käteisalennussumma** -kentän arvo on **5,05**. Arnie selvittää siis tämän laskun summaksi 505,05.

| Merkitse     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valittu | Normaali            | FTI-10010 | 4028    | 25.6.2020 | 25.7.2020 | 10010   | 1,000.00                       | USD      | 500.00           |

Alennustiedot näkyvät **Tilitä avoimet tapahtumat**-sivun alaosassa.

|        &nbsp;                | &nbsp;    |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 9.7.2020 |
| Käteisalennussumma         | 10.00     |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | 0,00      |
| Käytettävä käteisalennussumma | 5,05      |

Jos asiakas haluaa selvittää tasan puolet laskusta, asiakkaan on suoritettava maksu summalla 495,00. Tässä tapauksessa Arnie syöttää **495,00** summaksi **Tilitettävä summa** -kenttään. Summalle käytetään myös 5,00:n käteisalennusta, jotta selvitettävä kokonaissumma olisi 500,00.

| Merkitse     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valittu | Normaali            | FTI-10010 | 4028    | 25.6.2020 | 25.7.2020 | 10010   | 1,000.00                       | USD      | 495,00           |

Alennustiedot näkyvät **Tilitä avoimet tapahtumat**-sivun alaosassa.

|     &nbsp;                   | &nbsp;    |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 9.7.2020 |
| Käteisalennussumma         | 10.00     |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | 0,00      |
| Käytettävä käteisalennussumma | 5,00      |

Arnie sulkee **Selvitä tapahtumat** -sivun. Kirjauskansioon luodaan maksurivi summalle 495,00, jonka jälkeen Arnie kirjaa kirjauskansion. Erik voi tarkastella asiakastapahtumia **Asiakastapahtumat**-sivulla. Tällä sivulla Arnie näkee, että laskun saldo on 500,00. Näkyvillä ovat myös maksu (495,00) ja käteisalennus (5,00).

| Tosite    | Tapahtumatyyppi | Päivämäärä      | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo | Valuutta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | Lasku          | 25.6.2020 | 10010   | 1,000.00                             |                                       | 500.00  | USD      |
| ARP-10010  |  Maksu         | 7/1/2020  |         |                                      | 495,00                                | 0,00    | USD      |
| ALE-10010 |  Käteisalennus   | 7/1/2020  |         |                                      | 5.00                                  | 0,00    | USD      |

## <a name="payment-for-the-remaining-amount"></a>Jäljellä olevan määrän maksaminen
Asiakas 4028 maksaa jäljellä olevan summan, 495,00 8. heinäkuuta, joka on käteisalennuskaudella. Arnie luo maksukirjauskansion 8. heinäkuuta ja merkitsee tapahtuman selvitettäväksi. Erik näkee, että selvitettävä summa on 495,00. **Arvioitu käteisalennus** -kentän arvo on **5,00**, koska alennuksesta on jo aiemmin käytetty 5,00.

|   &nbsp;                | &nbsp; |
|-------------------------|--------|
| Merkitty kokonaissumma            | 495,00 |
| Arvioitu käteisalennus | 5,00   |

Valittua tapahtumaa koskevat tiedot näkyvät **Tilitä avoimet tapahtumat** -sivun ruudukossa.

| Merkitse     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valittu | Normaali            | FTI-10010 | 4028    | 25.6.2020 | 25.7.2020 | 10010   | 1,000.00                       | USD      | 495,00           |

Alennustiedot näkyvät **Tilitä avoimet tapahtumat**-sivun alaosassa.

|  &nbsp;                      |  &nbsp;   |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 9.7.2020 |
| Käteisalennussumma         | 10.00     |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | 5,00      |
| Käytettävä käteisalennussumma | 5,00      |

Arnie kirjaa maksukirjauskansion ja tarkistaa asiakkaan tapahtumat **Asiakastapahtumat**-sivulta. Laskun saldo on nyt 0,00, ja Arnie näkee kaksi maksua ja kaksi käteisalennusta.

| Tosite    | Tapahtumatyyppi | Päivämäärä      | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo | Valuutta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | Lasku          | 25.6.2020 | 10010   | 1,000.00                             |                                       | 0,00    | USD      |
| ARP-10010  | Maksu          | 7/1/2020  |         |                                      | 495,00                                | 0,00    | USD      |
| ALE-10010 | Käteisalennus    | 7/1/2020  |         |                                      | 5.00                                  | 0,00    | USD      |
| ARP-10011  | Maksu          | 8.7.2020  |         |                                      | 495,00                                | 0,00    | USD      |
| ALE-10011 | Käteisalennus    | 8.7.2020  |         |                                      | 5.00                                  | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
