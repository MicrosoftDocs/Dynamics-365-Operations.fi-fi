---
title: Yhdistämisvälin toiminto
description: Tässä ohje aiheessa on tietoja, joiden avulla voit valita kuukausittaisten, neljännesvuosittaisten, puolivuosittaisten ja vuosittaisten yhdistämisvälin.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c37da09f50448c27b20dfacccf2e7134b828f13b
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442976"
---
# <a name="compounding-interval-functionality"></a>Yhdistämisvälin toiminto

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä ohje aiheessa on tietoja, joiden avulla voit valita kuukausittaisten, neljännesvuosittaisten, puolivuosittaisten ja vuosittaisten yhdistämisvälin. Yhdistämisvälin toimintoa käytetään määritettäessä yhdistämiskausien määrä vuodessa vuokrasopimuksen maksuaikataulussa. Tämän ohjeaiheen kaikki neljä esimerkkiä osoittavat, miltä vuokrasopimuksen maksuaikataulu näyttää eri väleissä.

Et voi valita yhdistämisväliä, joka toistuu vuokrasopimuksen maksutiheyttä harvemmin. Esimerkiksi neljännesvuosittaista yhdistämisväliä ei voi käyttää kuukausittaisen maksutiheyden kanssa, eikä vuosittaista yhdistämisväliä puolivuosittaisen maksutiheyden kanssa. Jos yrität valita yhdistämisvälin, joka toistuu vuokrasopimuksen maksutiheyttä harvemmin, näyttöön tulee virhesanoma.

> [!NOTE]
> Tämän ohjeaiheen neljässä esimerkissä yhdistämisväli vastaa maksutiheyttä.

## <a name="examples"></a>Esimerkkejä

### <a name="setup-for-all-four-leases"></a>Kaikkien neljän vuokrasopimuksen määrittäminen

Seuraavissa taulukoissa ovat arvot, jotka on määritetty **Yleistiedot**- ja **Maksuaikataulun rivit** -välilehdille neljässä vuokrasopimuksessa, joita käytetään esimerkeissä.

**Yleinen-välilehti**

| Kenttä                      | Arvo                        |
|----------------------------|------------------------------|
| Inkrementaalinen lainakorko | **5 %**                       |
| Annuiteetin tyyppi               | **Tavallinen annuiteetti**         |
| Yhdistämisväli       | Katso yksilölliset esimerkit. |
| Maksun toistuvuus          | **Kuukausittain**                  |
| Aloituspäivämäärä          | **1.1.2020**                 |

**Maksusuunnitelmarivit-välilehti**

| Kenttä             | Arvo                        |
|-------------------|------------------------------|
| Aloituspäivä        | **1.1.2020**                 |
| Kaudet           | **120**                      |
| Kausiväli   | **Kuukautta**                   |
| Päättymispäivämäärä          | **31.12.2029**               |
| Maksun toistuvuus | Katso yksilölliset esimerkit. |
| Maksun summa    | **50,000**                   |

### <a name="lease-1-monthly-compounding-interval-and-monthly-payment-frequency"></a>Vuokrasopimus 1: Kuukausittainen yhdistämisväli ja kuukausittainen maksutiheys

Seuraavassa taulukossa ovat maksuaikataulun ensimmäiset 12 kuukautta. Ota seuraavat seikat huomioon:

- Kausi-sarakkeen arvo lisääntyy yhdellä joka kuukausi, koska jokainen kuukausi on uusi yhdistämisväli.
- Nykyinen arvo -sarakkeen kaavassa määrä jaetaan luvulla 12, koska vuodessa on 12 yhdistämiskautta. Eksponentti (eli yläindeksinumero) on sama kuin Kausi-sarakkeen arvo.

| Jakso | Kuukausi | Päivämäärä       | Maksun summa | Nykyinen arvo                                       |
|--------|-------|------------|----------------|-----------------------------------------------------|
| 1      | 1     | 31.1.2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>1</sup> = 49 792,53  |
| 2      | 2     | 29.2.2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>2</sup> = 49 585,92  |
| 3      | 3     | 31.3.2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>3</sup> = 49 380,17  |
| 4      | 4     | 30.4.2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>4</sup> = 49 175,28  |
| 5      | 5     | 31.5.2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>5</sup> = 48 971,23  |
| 6      | 6     | 30.6.2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>6</sup> = 48 768,03  |
| 7      | 7     | 31.7.2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>7</sup> = 48 565,67  |
| 8      | 8     | 31.8.2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>8</sup> = 48 364,15  |
| 9      | 9     | 30.9.2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>9</sup> = 48 163,47  |
| 10     | 10    | 31.10.2020 | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>10</sup> = 47 963,62 |
| 11     | 11    | 30.11.2020 | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>11</sup> = 47 764,61 |
| 12     | 12    | 31.12.2020 | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>12</sup> = 47 566,41 |

### <a name="lease-2-quarterly-compounding-interval-and-quarterly-payment-frequency"></a>Vuokrasopimus 2: Neljännesvuosittainen yhdistämisväli ja neljännesvuosittainen maksutiheys

Seuraavassa taulukossa ovat maksuaikataulun ensimmäiset 12 kuukautta. Ota seuraavat seikat huomioon:

- Kausi-sarakkeen arvo lisääntyy yhdellä joka kolmas kuukausi (neljännesvuosittain), koska jokainen neljännesvuosi on uusi yhdistämisväli.
- Nykyinen arvo -sarakkeen kaavassa määrä jaetaan luvulla 4, koska vuodessa on 4 yhdistämiskautta. Eksponentti vastaa Kausi-sarakkeen arvoa.

| Jakso | Kuukausi | Päivämäärä       | Maksun summa | Nykyinen arvo                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31.1.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>1</sup> = 0           |
| 1      | 2     | 29.2.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>1</sup> = 0           |
| 1      | 3     | 31.3.2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 4\])<sup>1</sup> = 49 382,72 |
| 2      | 4     | 30.4.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>2</sup> = 0           |
| 2      | 5     | 31.5.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>2</sup> = 0           |
| 2      | 6     | 30.6.2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 4\])<sup>2</sup> = 48 773,05 |
| 3      | 7     | 31.7.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>3</sup> = 0           |
| 3      | 8     | 31.8.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>3</sup> = 0           |
| 3      | 9     | 30.9.2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 4\])<sup>3</sup> = 48 170,92 |
| 4      | 10    | 31.10.2020 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>4</sup> = 0           |
| 4      | 11    | 30.11.2020 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>4</sup> = 0           |
| 4      | 12    | 31.12.2020 | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 4\])<sup>4</sup> = 47 576,21 |

> [!NOTE]
> Jos annuiteetin tyypiksi muutetaan **Erääntyvä annuiteetti**, maksu suoritetaan neljännesvuoden alussa neljännesvuoden lopun sijaan.

### <a name="lease-3-semiannual-compounding-interval-and-semiannual-payment-frequency"></a>Vuokrasopimus 3: Puolivuosittainen yhdistämisväli ja puolivuosittainen maksutiheys

Seuraavassa taulukossa ovat maksuaikataulun ensimmäiset 12 kuukautta. Ota seuraavat seikat huomioon:

- Kausi-sarakkeen arvo lisääntyy yhdellä joka kuudes kuukausi (puolivuosittain), koska puoli vuotta on uusi yhdistämisväli.
- Nykyinen arvo -sarakkeen kaavassa määrä jaetaan luvulla 2, koska vuodessa on 2 yhdistämiskautta. Eksponentti vastaa Kausi-sarakkeen arvoa.

| Jakso | Kuukausi | Päivämäärä       | Maksun summa | Nykyinen arvo                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31.1.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 2     | 29.2.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 3     | 31.3.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 4     | 30.4.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 5     | 31.5.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 6     | 30.6.2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 48 780,49 |
| 2      | 7     | 31.7.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 8     | 31.8.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 9     | 30.9.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 10    | 31.10.2020 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 11    | 30.11.2020 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 12    | 31.12.2020 | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 47 590,72 |

> [!NOTE]
> Jos annuiteettityypiksi muutetaan **Erääntyvä annuiteetti**, maksu suoritetaan tammikuussa ja heinäkuussa kesäkuun ja joulukuun sijaan.

### <a name="lease-4-annual-compounding-interval-and-annual-payment-frequency"></a>Vuokrasopimus 4: Vuosittainen yhdistämisväli ja vuosittainen maksutiheys

Seuraavassa taulukossa ovat maksuaikataulun ensimmäiset 12 kuukautta. Ota seuraavat seikat huomioon:

- Kausi-sarakkeen arvo lisääntyy yhdellä joka 12 kuukausi (vuosittain), koska jokainen vuosi on uusi yhdistämisväli.
- Nykyinen arvo -sarakkeen kaavassa määrä jaetaan luvulla 1, koska vuodessa on yksi yhdistämiskausi. Eksponentti vastaa Kausi-sarakkeen arvoa.

| Jakso | Kuukausi | Päivämäärä       | Maksun summa | Nykyinen arvo                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31.1.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 2     | 29.2.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 3     | 31.3.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 4     | 30.4.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 5     | 31.5.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 6     | 30.6.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 7     | 31.7.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 8     | 31.8.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 9     | 30.9.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 10    | 31.10.2020 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 11    | 30.11.2020 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 12    | 31.12.2020 | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 47 619,05 |

> [!NOTE]
> Jos annuiteettityypiksi muutetaan **Erääntyvä annuiteetti**, maksu suoritetaan tammikuussa joulukuun sijaan.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]