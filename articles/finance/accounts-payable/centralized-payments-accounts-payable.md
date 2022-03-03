---
title: Ostoreskontran keskitetyt maksut
description: Organisaatiot, joihin kuuluu useita yrityksiä, voivat luoda ja hallita maksuja käsittelemällä kaikki yhdessä yrityksessä. Näin samoja maksuja ei tarvitse lisätä useisiin yrityksiin. Tässä aiheessa on esimerkkejä, jotka osoittavat, miten keskitettyjen maksujen kirjaus toteutetaan eri tilanteissa.
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14341
ms.assetid: 7bd02e32-2416-4ac6-8a60-85525267fdb7
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3030bc7d2501e2162758c94c0dc1a073655c9c0f
ms.sourcegitcommit: 6102f70d4595d01b90afe5b23dfd8ec2ea030653
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/16/2022
ms.locfileid: "8182515"
---
# <a name="centralized-payments-for-accounts-payable"></a>Ostoreskontran keskitetyt maksut

[!include [banner](../includes/banner.md)]

Organisaatiot, joihin kuuluu useita yrityksiä, voivat luoda ja hallita maksuja käsittelemällä kaikki yhdessä yrityksessä. Näin samoja maksuja ei tarvitse lisätä useisiin yrityksiin. Tässä aiheessa on esimerkkejä, jotka osoittavat, miten keskitettyjen maksujen kirjaus toteutetaan eri tilanteissa.

Organisaatiot, joihin kuuluu useita yrityksiä, voivat luoda ja hallita maksuja käsittelemällä kaikki yhdessä yrityksessä. Näin samoja maksuja ei tarvitse lisätä useisiin yrityksiin. Lisäksi virtaviivaistettu maksuprosessi säästää organisaation aikaa.

Maksujen keskittämiseen tarkoitetussa organisaatiossa on useita toimintaa harjoittavia yrityksiä, ja jokainen toimintaa harjoittava yritys hallitsee omia toimittajalaskujaan. Maksut kaikille toimintaa harjoittaville yrityksille luodaan yhdestä yrityksestä, joka toimii maksun yrityksenä. Selvitysprosessin aikana sovellettavissa olevat erääntymiskohteen ja -lähteen tapahtumat muodostetaan. Voit määrittää, mikä organisaatioon kuuluva yritys vastaanottaa toteutuneet voitto- tai tappiotapahtumat ja kuinka yritysten välisiin maksuihin liittyvät käteisalennustapahtumat käsitellään. Keskitetyn maksukirjauskansion rivin **tilityypiksi** on määritettävä toimittaja. **Vastatilin tapahtumalajiksi** on määritettävä pankki tai kirjanpito. Pankkitilin on oltava nykyisessä yrityksessä. 

Seuraavissa esimerkeissä näytetään, kuinka kirjaus toteutetaan eri tilanteissa. Lähtötilanne on kaikissa esimerkeissä sama:

-   Yritykset ovat Fabrikam, Fabrikam East ja Fabrikam West. Maksut suoritetaan Fabrikamista.
-   **Konsernin sisäinen laskenta** -sivun **Käteisalennuksen jälkeen** -kentän arvoksi on valittu **Laskun oikeushenkilö**.
-   **Konsernin sisäinen laskenta** -sivun **Valuutanvaihdon voiton tai tappion jälkeen** -kentän arvoksi on valittu **Maksun oikeushenkilö**.
-   Fourth Coffee -toimittaja on määritetty kunkin yrityksen toimittajaksi. Eri yritysten toimittajat tunnistetaan samaksi toimittajaksi, koska niillä on yhteinen yleisen osoitekirjan tunnus.

| Hakemistotunnus | Toimittajatili | Nimi          | Oikeushenkilö  |
|--------------|----------------|---------------|---------------|
| 1 050         | 3004           | Fourth Coffee. | Fabrikam:      |
| 1 050         | 100            | Fourth Coffee. | Fabrikam East: |
| 1 050         | 3004           | Fourth Coffee. | Fabrikam West: |

## <a name="example-1-vendor-payment-of-invoice-from-another-legal-entity"></a>Esimerkki 1: Toimittajan laskun maksaminen toisesta yrityksestä
Fabrikam Eastilla on avoin lasku toimittajatilillä 100, Fourth Coffee. Fabrikam syöttää ja kirjaa maksun Fabrikamin toimittajatilille 3004, Fourth Coffee. Maksu selvitetään avoimen laskun kanssa.

### <a name="invoice-is-posted-in-fabrikam-east-for-vendor-100"></a>Lasku kirjataan Fabrikam Eastiin toimittajalle 100

| Tili                          | Veloitussumma | Hyvityssumma |
|----------------------------------|--------------|---------------|
| Kulu (Fabrikam East)          | 600,00       |               |
| Ostoreskontra (Fabrikam East) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Maksu muodostetaan ja kirjataan Fabrikamiin toimittajalle 3004

| Tili                     | Veloitussumma | Hyvityssumma |
|-----------------------------|--------------|---------------|
| Ostoreskontra (Fabrikam) | 600,00       |               |
| Käteinen (Fabrikam)             |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikamin maksu selvitetään Fabrikam Eastin laskun kanssa

**Kirjaus Fabrikamiin**

| Tili                           | Veloitussumma | Hyvityssumma |
|-----------------------------------|--------------|---------------|
| Maksaja Fabrikam East (Fabrikam) | 600,00       |               |
| Ostoreskontra (Fabrikam)       |              | 600,00        |

**Kirjaus Fabrikam Eastiin**

| Tili                          | Veloitussumma | Hyvityssumma |
|----------------------------------|--------------|---------------|
| Ostoreskontra (Fabrikam East) | 600,00       |               |
| Saaja Fabrikam (Fabrikam East)  |              | 600,00        |

## <a name="example-2-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>Esimerkki 2: Toimittajan laskun ja käteisalennuksen maksaminen toisesta yrityksestä
Fabrikam Eastilla on avoin lasku toimittajalle 100, Fourth Coffee. Laskussa on käytettävissä käteisalennus, jonka summa on 20,00. Fabrikam syöttää ja kirjaa maksun Fabrikamin toimittajalle 3004, Fourth Coffee. Maksu selvitetään Fabrikam Eastin avointen laskujen kanssa. Käteisalennus kirjataan laskun yritykseen, joka on Fabrikam East.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Lasku kirjataan Fabrikam Eastiin Fabrikam Westin toimittajalle 100

| Tili                          | Veloitussumma | Hyvityssumma |
|----------------------------------|--------------|---------------|
| Kulu (Fabrikam East)          | 600,00       |               |
| Ostoreskontra (Fabrikam East) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Maksu muodostetaan ja kirjataan Fabrikamiin Fabrikamin toimittajalle 3004

| Tili                     | Veloitussumma | Hyvityssumma |
|-----------------------------|--------------|---------------|
| Ostoreskontra (Fabrikam) | 580,00       |               |
| Käteinen (Fabrikam)             |              | 580,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikamin maksu selvitetään Fabrikam Eastin laskun kanssa

**Kirjaus Fabrikamiin**

| Tili                           | Veloitussumma | Hyvityssumma |
|-----------------------------------|--------------|---------------|
| Maksaja Fabrikam East (Fabrikam) | 580,00       |               |
| Ostoreskontra (Fabrikam)       |              | 580,00        |

**Kirjaus Fabrikam Eastiin**

| Tili                          | Veloitussumma | Hyvityssumma |
|----------------------------------|--------------|---------------|
| Ostoreskontra (Fabrikam East) | 580,00       |               |
| Saaja Fabrikam (Fabrikam East)  |              | 580,00        |
| Ostoreskontra (Fabrikam East) | 20,00        |               |
| Käteisalennus (Fabrikam East)    |              | 20,00         |

## <a name="example-3-vendor-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-loss"></a>Esimerkki 3: Toimittajan laskun ja toteutuneen vaihtokurssitappion maksaminen toisesta yrityksestä
Fabrikam Eastilla on avoin lasku toimittajalle 100, Fourth Coffee. Fabrikam syöttää ja kirjaa maksun Fabrikamin toimittajalle 3004, Fourth Coffee. Maksu selvitetään Fabrikam Eastin avoimen laskun kanssa. Valuuttakurssitappiotapahtuma muodostetaan selvitysprosessin aikana.

-   Euron (EUR) ja Yhdysvaltain dollarin (USD) vaihtokurssi laskun päivämääränä: 1,2062
-   Euron ja Yhdysvaltain dollarin vaihtokurssi maksun päivämääränä: 1,2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Lasku kirjataan Fabrikam Eastiin Fabrikam Westin toimittajalle 100

| Tili                          | Veloitussumma            | Hyvityssumma           |
|----------------------------------|-------------------------|-------------------------|
| Kulu (Fabrikam East)          | 600,00 (EUR) / 723, 72 (USD) |                         |
| Ostoreskontra (Fabrikam East) |                         | 600,00 (EUR) / 723, 72 (USD) |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Maksu muodostetaan ja kirjataan Fabrikamiin Fabrikamin toimittajalle 3004

| Tili                     | Veloitussumma            | Hyvityssumma           |
|-----------------------------|-------------------------|-------------------------|
| Ostoreskontra (Fabrikam) | 600,00 (EUR) / 736,62 (USD) |                         |
| Käteinen (Fabrikam)             |                         | 600,00 (EUR) / 736,62 (USD) |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikamin maksu selvitetään Fabrikam Eastin laskun kanssa

**Kirjaus Fabrikamiin**

| Tili                           | Veloitussumma            | Hyvityssumma           |
|-----------------------------------|-------------------------|-------------------------|
| Maksaja Fabrikam East (Fabrikam) | 600,00 (EUR) / 736,62 (USD) |                         |
| Ostoreskontra (Fabrikam)       |                         | 600,00 (EUR) / 736,62 (USD) |
| Realisoitunut tappio (Fabrikam)          | 0,00 (EUR) / 12,90 (USD)    |                         |
| Maksaja Fabrikam East (Fabrikam) |                         | 0,00 (EUR) / 12,90 (USD)    |

**Kirjaus Fabrikam Eastiin**

| Tili                          | Veloitussumma            | Hyvityssumma           |
|----------------------------------|-------------------------|-------------------------|
| Ostoreskontra (Fabrikam East) | 600,00 (EUR) / 736,62 (USD) |                         |
| Saaja Fabrikam (Fabrikam East)  |                         | 600,00 (EUR) / 736,62 (USD) |
| Saaja Fabrikam (Fabrikam East)  | 0,00 (EUR) / 12,90 (USD)    |                         |
| Ostoreskontra (Fabrikam East) |                         | 0,00 (EUR) / 12,90 (USD)    |

## <a name="example-4-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-loss"></a>Esimerkki 4: Toimittajan laskun, käteisalennuksen ja toteutuneen vaihtokurssitappion maksaminen toisesta yrityksestä
Fabrikam Eastilla on avoin lasku toimittajalle 100, Fourth Coffee. Laskussa on käytettävissä käteisalennus, ja arvonlisäverotapahtuma muodostetaan. Fabrikam kirjaa maksun Fabrikamin toimittajalle 3004, Fourth Coffee. Maksu selvitetään Fabrikam Eastin avoimen laskun kanssa. Valuuttakurssitappiotapahtuma muodostetaan selvitysprosessin aikana. Käteisalennus kirjataan laskutusyritykseen (Fabrikam Eastiin) ja vaihtokurssitappio maksutapahtuman yritykseen (Fabrikamiin).

-   Euron ja Yhdysvaltain dollarin vaihtokurssi laskun päivämääränä: 1,2062
-   Euron ja Yhdysvaltain dollarin vaihtokurssi maksun päivämääränä: 1,2277

### <a name="invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-vendor-100"></a>Lasku kirjataan ja verotapahtuma muodostetaan Fabrikam Eastiin toimittajalle 100

| Tili                          | Veloitussumma            | Hyvityssumma           |
|----------------------------------|-------------------------|-------------------------|
| Kulu (Fabrikam East)          | 564,07 (EUR) / 680,38 (USD) |                         |
| Arvonlisävero (Fabrikam East)        | 35,93 (EUR) / 43,34 (USD)   |                         |
| Ostoreskontra (Fabrikam East) |                         | 600,00 (EUR) / 723,72 (USD) |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Maksu muodostetaan ja kirjataan Fabrikamiin toimittajalle 3004

| Tili                     | Veloitussumma            | Hyvityssumma           |
|-----------------------------|-------------------------|-------------------------|
| Ostoreskontra (Fabrikam) | 588,72 (EUR) / 722,77 (USD) |                         |
| Käteinen (Fabrikam East)        |                         | 588,72 (EUR) / 722,77 (USD) |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikamin maksu selvitetään Fabrikam Eastin laskun kanssa

**Kirjaus Fabrikamiin**

| Tili                           | Veloitussumma            | Hyvityssumma           |
|-----------------------------------|-------------------------|-------------------------|
| Maksaja Fabrikam East (Fabrikam) | 588,72 (EUR) / 722,77 (USD) |                         |
| Ostoreskontra (Fabrikam)       |                         | 588,72 (EUR) / 722,77 (USD) |
| Realisoitunut tappio (Fabrikam)          | 0,00 (EUR) / 12,66 (USD)    |                         |
| Maksaja Fabrikam East (Fabrikam) |                         | 0,00 (EUR) / 12,66 (USD)    |

**Kirjaus Fabrikam Eastiin**

| Tili                          | Veloitussumma            | Hyvityssumma           |
|----------------------------------|-------------------------|-------------------------|
| Ostoreskontra (Fabrikam East) | 588,72 (EUR) / 722,77 (USD) |                         |
| Saaja Fabrikam (Fabrikam East)  |                         | 588,72 (EUR) / 722,77 (USD) |
| Saaja Fabrikam (Fabrikam East)   | 0,00 (EUR) / 12,66 (USD)    |                         |
| Ostoreskontra (Fabrikam East) |                         | 0,00 (EUR) / 12,66 (USD)    |
| Ostoreskontra (Fabrikam East) | 11,28 (EUR) / 13,61 (USD)   |                         |
| Käteisalennus (Fabrikam East)    |                         | 11,28 (EUR) / 13,61 (USD)   |

## <a name="example-5-vendor-credit-note-with-primary-payment"></a>Esimerkki 5: Toimittajan hyvityslasku ja ensisijainen maksu
Fabrikam muodostaa maksun, jonka summa on 75,00, toimittajalle 3004, Fourth Coffee. Maksu selvitetään Fabrikam Westin toimittajan 3004 avoimen laskun ja Fabrikam Eastin toimittajan 100 hyvityslaskun kanssa. Maksu valitaan ensisijaiseksi maksuksi **Selvitä tapahtumat** -sivulla.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Lasku kirjataan Fabrikam Westiin toimittajalle 3004

| Tili                          | Veloitussumma | Hyvityssumma |
|----------------------------------|--------------|---------------|
| Kulu (Fabrikam West)          | 100,00       |               |
| Ostoreskontra (Fabrikam West) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Hyvityslasku kirjataan Fabrikam Eastiin toimittajalle 100

| Tili                          | Veloitussumma | Hyvityssumma |
|----------------------------------|--------------|---------------|
| Ostoreskontra (Fabrikam East) | 25,00        |               |
| Ostopalautukset (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Maksu kirjataan Fabrikamiin toimittajalle 3004

| Tili                     | Veloitussumma | Hyvityssumma |
|-----------------------------|--------------|---------------|
| Ostoreskontra (Fabrikam) | 75,00        |               |
| Käteinen (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikamin maksu selvitetään Fabrikam Westin laskun ja Fabrikam Eastin hyvityslaskun kanssa

**Kirjaus Fabrikamiin**

| Tili                           | Veloitussumma | Hyvityssumma |
|-----------------------------------|--------------|---------------|
| Ostoreskontra (Fabrikam)       | 25,00        |               |
| Saaja Fabrikam East (Fabrikam)   |              | 25,00         |
| Maksaja Fabrikam West (Fabrikam) | 100,00       |               |
| Ostoreskontra (Fabrikam)       |              | 100,00        |

**Kirjaus Fabrikam Eastiin**

| Tili                           | Veloitussumma | Hyvityssumma |
|-----------------------------------|--------------|---------------|
| Maksaja Fabrikam (Fabrikam East) | 25,00        |               |
| Ostoreskontra (Fabrikam East)  |              | 25,00         |

**Kirjaus Fabrikam Westiin**

| Tili                          | Veloitussumma | Hyvityssumma |
|----------------------------------|--------------|---------------|
| Ostoreskontra (Fabrikam West) | 100,00       |               |
| Saaja Fabrikam (Fabrikam West)  |              | 100,00        |

## <a name="example-6-vendor-credit-note-without-primary-payment"></a>Esimerkki 6: Toimittajan hyvityslasku ilman ensisijaista maksua
Fabrikam muodostaa maksun, jonka summa on 75,00, toimittajalle 3004, Fourth Coffee. Maksu selvitetään Fabrikam Westin toimittajan 3004 avoimen laskun ja Fabrikam Eastin toimittajan 100 hyvityslaskun kanssa. Maksu ei valita ensisijaiseksi maksuksi **Selvitä tapahtumat** -sivulla.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Lasku kirjataan Fabrikam Westiin toimittajalle 3004

| Tili                          | Veloitussumma | Hyvityssumma |
|----------------------------------|--------------|---------------|
| Kulu (Fabrikam West)          | 100,00       |               |
| Ostoreskontra (Fabrikam West) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Hyvityslasku kirjataan Fabrikam Eastiin toimittajalle 100

| Tili                          | Veloitussumma | Hyvityssumma |
|----------------------------------|--------------|---------------|
| Ostoreskontra (Fabrikam East) | 25,00        |               |
| Ostopalautukset (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Maksu kirjataan Fabrikamiin toimittajalle 3004

| Tili                     | Veloitussumma | Hyvityssumma |
|-----------------------------|--------------|---------------|
| Ostoreskontra (Fabrikam) | 75,00        |               |
| Käteinen (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikamin maksu selvitetään Fabrikam Westin laskun ja Fabrikam Eastin hyvityslaskun kanssa

**Kirjaus Fabrikamiin**

| Tili                           | Veloitussumma | Hyvityssumma |
|-----------------------------------|--------------|---------------|
| Maksaja Fabrikam West (Fabrikam) | 75,00        |               |
| Ostoreskontra (Fabrikam)       |              | 75,00         |

**Kirjaus Fabrikam Eastiin**

| Tili                                | Veloitussumma | Hyvityssumma |
|----------------------------------------|--------------|---------------|
| Maksaja Fabrikam West (Fabrikam East) | 25,00        |               |
| Ostoreskontra (Fabrikam East)       |              | 25,00         |

**Kirjaus Fabrikam Westiin**

| Tili                              | Veloitussumma | Hyvityssumma |
|--------------------------------------|--------------|---------------|
| Ostoreskontra (Fabrikam West)     | 75,00        |               |
| Saaja Fabrikam (Fabrikam West)      |              | 75,00         |
| Ostoreskontra (Fabrikam West)     | 25,00        |               |
| Saaja Fabrikam East (Fabrikam West) |              | 25,00         |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
