---
title: Kohdistuspäiväskenaariot
description: Tässä ohjeaiheessa on esimerkkejä, jotka näyttävät, kuinka kohdistuspäivämäärät toimivat tilauslaskutuksen yhteydessä.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 91480fecd16cf8417722df73c28bbd81d029fb07
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690470"
---
# <a name="alignment-date-scenarios"></a>Kohdistuspäiväskenaariot

Tässä ohjeaiheessa on esimerkkejä, jotka näyttävät, kuinka kohdistuspäivämäärät toimivat tilauslaskutuksen yhteydessä.

Näissä esimerkeissä laskutusaikataulun laskutustietojen kohdistuspäivämäärä on 31.10.2019. Rivin ensimmäiset laskutustiedot päättyvät 31.10.2019, ja on jaettu suhteellisesti vastaavasti. Rivi uusitaan automaattisesti käyttäen uusinnan alkamispäivämäärää 11.11.

> [!NOTE]
> Vuosi on tärkeä, koska kohdistuspäivämäärä voi olla suurempi tai pienempi kuin vuosi. Näissä esimerkeissä suhteellisen jaon laskennassa käytettäväksi menetelmäksi määritetään **Kuukausittain** **Toistuvat sopimuksen laskutusparametrit** -sivulla. Jos arvoksi on määritetty **Päivittäin**, jotkin osasummista poikkeaa toisistaan.

## <a name="scenario-1-no-alignment"></a>Skenaario 1: Ei kohdistusta

Laskutusaikataulu määritetään seuraavilla tiedoilla:

- **Alkamispäivä:** 1.5.2019
- **Päättymispäivä:** 31.12.2024
- **Summa:** 1 000 $

| Laskutuksen aloituspäivä | Laskutuksen päättymispäivä | Edellinen lukema | Nykyinen lukema | Määritetty määrä | Vapaa määrä | Laskutettava määrä | Yksikköhinta |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 30.4.2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2020 | 4/30/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2021 | 4/30/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2022 | 4/30/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2023 | 4/30/2024 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 666.67 |

## <a name="scenario-2-shortened-alignment"></a>Skenaario 2: Lyhennetty kohdistus

Laskutusaikataulu määritetään seuraavilla tiedoilla:

- **Alkamispäivä:** 1.5.2019
- **Päättymispäivä:** 31.12.2024
- **Summa:** 1 000 $
- **Kohdistuspäivä:** 31.12.2019

Ensimmäinen uusimissumma koskee alle yhtä vuotta.

| Laskutuksen aloituspäivä | Laskutuksen päättymispäivä | Edellinen lukema | Nykyinen lukema | Määritetty määrä | Vapaa määrä | Laskutettava määrä | Yksikköhinta |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2019 | | | 1.00 | | 1.00 | 666.67 |
| 1.1.2020 | 31.12.2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2021 | 12/31/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.1.2022 | 12/31/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-3-extended-alignment"></a>Skenaario 3: Pidennetty kohdistus

Laskutusaikataulu määritetään seuraavilla tiedoilla:

- **Alkamispäivä:** 1.5.2019
- **Päättymispäivä:** 31.12.2024
- **Summa:** 1 000 $
- **Kohdistuspäivä:** 31.12.2020

Ensimmäinen uusimissumma koskee yli yhtä vuotta.

| Laskutuksen aloituspäivä | Laskutuksen päättymispäivä | Edellinen lukema | Nykyinen lukema | Määritetty määrä | Vapaa määrä | Laskutettava määrä | Yksikköhinta |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 31.12.2020 | | | 1.00 | | 1.00 | 1,666.67 |
| 1/1/2021 | 12/31/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.1.2022 | 12/31/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-4-alignment-with-a-different-end-month"></a>Skenaario 4: Kohdistus eri päättymiskuukaudella

Laskutusaikataulu määritetään seuraavilla tiedoilla:

- **Alkamispäivä:** 1.5.2019
- **Päättymispäivä:** 31.10.2024
- **Summa:** 1 000 $
- **Kohdistuspäivä:** 31.12.2019

> [!NOTE]
> Tämä skenaario ei ole yleinen.

| Laskutuksen aloituspäivä | Laskutuksen päättymispäivä | Edellinen lukema | Nykyinen lukema | Määritetty määrä | Vapaa määrä | Laskutettava määrä | Yksikköhinta |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2019 | | | 1.00 | | 1.00 | 666.67 |
| 1.1.2020 | 31.12.2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2021 | 12/31/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.1.2022 | 12/31/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2024 | 10/31/2024 | | | 1.00 | | 1.00 | 833.33 |

## <a name="scenario-5-single-partial-year"></a>Skenaario 5: Yksi osittainen vuosi

Laskutusaikataulu määritetään seuraavilla tiedoilla:

- **Alkamispäivä:** 1.5.2019
- **Päättymispäivä:** 31.12.2019
- **Summa:** 1 000 $
- **Kohdistuspäivä**: 31.12.2019

Tässä skenaariossa kohdistuspäivää ei tarvita. Tämä skenaario on yleinen automaattisissa uusinnoissa.

| Laskutuksen aloituspäivä | Laskutuksen päättymispäivä | Edellinen lukema | Nykyinen lukema | Määritetty määrä | Vapaa määrä | Laskutettava määrä | Yksikköhinta |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2019 | | | 1.00 | | 1.00 | 666.67 |

## <a name="scenario-6-calculated-dates"></a>Skenaario 6: Lasketut päivämäärät

Tuki ja uusiminen määritetään seuraavilla tiedoilla:

- **Ohituksen alkamispäivä:** Ei
- **Tuen ja uusinnan aloituspäivät:** Seuraavan kuukauden alku
- **Laskun kirjauspäivä:** 22.6.2019
- **Kohdistuspäivä:** 31.12.2020

| Laskutuksen aloituspäivä | Laskutuksen päättymispäivä | Edellinen lukema | Nykyinen lukema | Määritetty määrä | Vapaa määrä | Laskutettava määrä | Yksikköhinta |
|---|---|---|---|---|---|---|---|
| 7/1/2019 | 7/31/2019 | | | 1.00 | | 1.00 | 297.60 |
| 8/1/2019 | 31.12.2020 | | | 1.00 | | 1.00 | 6,936.00 |

## <a name="scenario-7-calculated-dates-and-future-posting"></a>Skenaario 7: Lasketut päivämäärät ja tulevat kirjaukset

Tuki ja uusiminen määritetään seuraavilla tiedoilla:

- **Ohituksen alkamispäivä:** Ei
- **Tuen ja uusinnan aloituspäivät:** Seuraavan kuukauden alku
- **Laskun kirjauspäivä:** 22.6.2019
- **Kohdistuspäivä:** 31.12.2020

Tässä skenaariossa kohdistuspäivämääräksi muutetaan 31.12.2021.

| Laskutuksen aloituspäivä | Laskutuksen päättymispäivä | Edellinen lukema | Nykyinen lukema | Määritetty määrä | Vapaa määrä | Laskutettava määrä | Yksikköhinta |
|---|---|---|---|---|---|---|---|
| 6/22/2019 | 6/22/2019 | | | 1.00 | | 1.00 | 0,00 |
| 8/1/2019 | 31.12.2020 | | | 1.00 | | 1.00 | 4,250.00 |

## <a name="scenario-8-manual-dates-and-multiple-years"></a>Esimerkki 8: Manuaaliset päivämäärät ja useita vuosia

Tuki ja uusiminen määritetään seuraavilla tiedoilla:

- **Ohituksen alkamispäivä:** Kyllä
- **Uusimisen alkamispäivä:** 1.7.2020
- **Uusinnan päättymispäivä:** 31.12.2024
- **Kohdistuspäivä:** 31.12.2021

| Laskutuksen aloituspäivä | Laskutuksen päättymispäivä | Edellinen lukema | Nykyinen lukema | Määritetty määrä | Vapaa määrä | Laskutettava määrä | Yksikköhinta |
|---|---|---|---|---|---|---|---|
| 6/22/2019 | 6/22/2019 | | | 1.00 | | 1.00 | 0,00 |
| 7/1/2020 | 12/31/2021 | | | 1.00 | | 1.00 | 375.00 |
| 1.1.2022 | 12/31/2022 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 250,00 |

## <a name="scenario-9-manual-dates-multiple-years-and-a-different-end-month"></a>Skenaario 9: Manuaaliset päivämäärät, useita vuosia ja eri päättymiskuukausi

Tuki ja uusiminen määritetään seuraavilla tiedoilla:

- **Ohituksen alkamispäivä:** Kyllä
- **Uusimisen alkamispäivä:** 1.7.2020
- **Uusinnan päättymispäivä:** 31.10.2024
- **Kohdistuspäivä:** 31.12.2021

| Laskutuksen aloituspäivä | Laskutuksen päättymispäivä | Edellinen lukema | Nykyinen lukema | Määritetty määrä | Vapaa määrä | Laskutettava määrä | Yksikköhinta |
|---|---|---|---|---|---|---|---|
| 6/22/2019 | 6/22/2019 | | | 1.00 | | 1.00 | 0,00 |
| 7/1/2020 | 12/31/2021 | | | 1.00 | | 1.00 | 375.00 |
| 1.1.2022 | 12/31/2022 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2024 | 10/31/2024 | | | 1.00 | | 1.00 | 208.33 |

## <a name="scenario-10-alignment-without-proration"></a>Skenaario 10: Kohdistus ilman suhteellista jakamista

Tuki ja uusiminen määritetään seuraavilla tiedoilla:

- **Ohituksen alkamispäivä:** Ei
- **Laskun kirjauspäivä:** 22.6.2019
- **Kohdistuspäivä:** 31.12.2019

Uusinnan alkamispäivämäärää ja kohdistuspäivämääriä muutetaan niin, että molemmat aloituspäivät ovat kirjauspäivän jälkeen.

- **Uusinnan aloituspäivä:** 1.1.2020.
- **Uusinnan päättymispäivä:** 31.12.2020
