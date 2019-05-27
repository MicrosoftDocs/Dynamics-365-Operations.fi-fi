---
title: Myyntireskontran keskitetyt maksut
description: Organisaatiot, joihin kuuluu useita yrityksiä, voivat luoda ja hallita maksuja käsittelemällä kaikki yhdessä yrityksessä. Näin samoja tapahtumia ei tarvitse lisätä useisiin yrityksiin. Tässä artikkelissa on esimerkkejä, jotka osoittavat, miten keskitettyjen maksujen kirjaus toteutetaan eri tilanteissa.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 02/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6b8b1548bf70363431ad58482ba82cf11017332
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552008"
---
# <a name="centralized-payments-for-accounts-receivable"></a>Myyntireskontran keskitetyt maksut

[!include [banner](../includes/banner.md)]

Organisaatiot, joihin kuuluu useita yrityksiä, voivat luoda ja hallita maksuja käsittelemällä kaikki yhdessä yrityksessä. Näin samoja tapahtumia ei tarvitse lisätä useisiin yrityksiin. Tässä artikkelissa on esimerkkejä, jotka osoittavat, miten keskitettyjen maksujen kirjaus toteutetaan eri tilanteissa.

Organisaatiot, joihin kuuluu useita yrityksiä, voivat luoda ja hallita maksuja käsittelemällä kaikki yhdessä yrityksessä. Näin samoja tapahtumia ei tarvitse lisätä useisiin yrityksiin. Organisaatio säästää myös aikaa, koska maksuehdotusten, tilitysten sekä avoimien ja suljettujen tapahtumien keskitetyt maksuprosessit ovat tehokkaita. 

Maksujen keskittämiseen tarkoitetussa organisaatiossa on useita toimintaa harjoittavia yrityksiä, ja jokainen toimintaa harjoittava yritys hallitsee omien saatavien laskujen tietojaan. Maksut kaikille toimintaa harjoittaville yrityksille vastaanotetaan yhdestä yrityksestä, joka toimii maksun yrityksenä. Selvitysprosessin aikana sovellettavissa olevat erääntymiskohteen ja -lähteen tapahtumat muodostetaan. Voit määrittää, mikä organisaatioon kuuluva yritys vastaanottaa toteutuneet voitto- tai tappiotapahtumat ja kuinka keskitettyihin maksuihin liittyvät käteisalennustapahtumat käsitellään. Keskitetyn maksukirjauskansion rivin **tilityypiksi** on määritettävä asiakas. **Vastatilin tapahtumalajiksi** on määritettävä pankki tai kirjanpito. Pankkitilin on oltava nykyisessä yrityksessä. 

Seuraavissa esimerkeissä näytetään, kuinka kirjaus toteutetaan eri tilanteissa. Lähtötilanne on kaikissa esimerkeissä sama:

-   Yritykset ovat Fabrikam, Fabrikam East ja Fabrikam West. Asiakasmaksut lisätään Fabrikamiin.
-   **Konsernin sisäinen laskenta** -sivun **Käteisalennuksen jälkeen** -kentän arvoksi on valittu **Laskun oikeushenkilö**.
-   **Konsernin sisäinen laskenta** -sivun **Valuutanvaihdon voiton tai tappion jälkeen** -kentän arvoksi on valittu **Maksun oikeushenkilö**.
-   Asiakas Northwind Traders on määritetty kunkin yrityksen asiakkaaksi. Eri yritysten asiakkaat tunnistetaan samaksi asiakkaaksi, koska niillä on yhteinen yleisen osoitekirjan tunnus.

| Osoitekirjan tunnus | Asiakastili | Nimi              | Oikeushenkilö  |
|-----------------|------------------|-------------------|---------------|
| 4050            | 4 000             | Northwind Traders | Fabrikam:      |
| 4050            | 4 000             | Northwind Traders | Fabrikam East: |
| 4050            | 10 000            | Northwind Traders | Fabrikam West: |

## <a name="example-1-customer-payment-of-invoice-from-another-legal-entity"></a>Esimerkki 1: Asiakkaan laskun maksaminen toisesta yrityksestä
Fabrikam vastaanottaa maksun, jonka summa on 600,00, Fabrikamin asiakastilille 4000, Northwind Traders. Maksu selvitetään asiakastilin 4000 (Fabrikam East) avoimen laskun kanssa.

### <a name="invoice-is-posted-in-fabrikam-east-for-customer-4000"></a>Lasku kirjataan Fabrikam Eastiin asiakkaalle 4000

| Tili:                             | Veloitussumma: | Hyvityssumma: |
|-------------------------------------|--------------|---------------|
| Myyntireskontra (Fabrikam East) | 600,00       |               |
| Myynti (Fabrikam East)               |              | 600,00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>Maksu vastaanotetaan ja kirjataan Fabrikamiin asiakkaalle 4000

| Tili:                        | Veloitussumma: | Hyvityssumma: |
|--------------------------------|--------------|---------------|
| Käteinen (Fabrikam)                | 600,00       |               |
| Myyntireskontra (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikamin maksu selvitetään Fabrikam Eastin laskun kanssa

**Kirjaus Fabrikamiin**

| Tili:                         | Veloitussumma: | Hyvityssumma: |
|---------------------------------|--------------|---------------|
| Myyntireskontra (Fabrikam)  | 600,00       |               |
| Saaja Fabrikam East (Fabrikam) |              | 600,00        |

**Kirjaus Fabrikam Eastiin**

| Tili:                             | Veloitussumma | Hyvityssumma |
|-------------------------------------|--------------|---------------|
| Maksaja Fabrikam (Fabrikam East)   | 600,00       |               |
| Myyntireskontra (Fabrikam East) |              | 600,00        |

## <a name="example-2-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>Esimerkki 2: Asiakkaan laskun ja käteisalennuksen maksaminen toisesta yrityksestä
Fabrikam vastaanottaa maksun, jonka summa on 580,00, Fabrikamin asiakkaalle 4000, Northwind Traders. Fabrikam Eastilla on avoin lasku asiakkaalle 4000. Laskussa on käytettävissä käteisalennus, jonka summa on 20,00. Maksu selvitetään Fabrikam Eastin avointen laskujen kanssa. Käteisalennus kirjataan laskun yritykseen, joka on Fabrikam East.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Lasku kirjataan Fabrikam Eastiin Fabrikam Westin asiakkaalle 4000

| Tili:                             | Veloitussumma: | Hyvityssumma: |
|-------------------------------------|--------------|---------------|
| Myyntireskontra (Fabrikam East) | 600,00       |               |
| Myynti (Fabrikam East)               |              | 600,00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Maksu vastaanotetaan ja kirjataan Fabrikamiin Fabrikamin asiakkaalle 4000

| Tili:                        | Veloitussumma: | Hyvityssumma: |
|--------------------------------|--------------|---------------|
| Käteinen (Fabrikam)                | 600,00       |               |
| Myyntireskontra (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikamin maksu selvitetään Fabrikam Eastin laskun kanssa

**Kirjaus Fabrikamiin**

| Tili:                         | Veloitussumma: | Hyvityssumma: |
|---------------------------------|--------------|---------------|
| Myyntireskontra (Fabrikam)  | 580,00       |               |
| Saaja Fabrikam East (Fabrikam) |              | 580,00        |

**Kirjaus Fabrikam Eastiin**

| Tili:                             | Veloitussumma: | Hyvityssumma: |
|-------------------------------------|--------------|---------------|
| Maksaja Fabrikam (Fabrikam East)   | 580,00       |               |
| Myyntireskontra (Fabrikam East) |              | 580,00        |
| Käteisalennus (Fabrikam East)       | 20,00        |               |
| Myyntireskontra (Fabrikam East) |              | 20,00         |

## <a name="example-3-customer-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-gain"></a>Esimerkki 3: Asiakkaan laskun ja toteutuneen vaihtokurssivoiton maksaminen toisesta yrityksestä
Fabrikam vastaanottaa 600,00 euron (EUR) maksun Fabrikamin asiakkaalle 4000, Northwind Traders. Maksu selvitetään asiakkaan 4000 (Fabrikam East) avoimen laskun kanssa. Valuuttakurssivoittotapahtuma muodostetaan selvitysprosessin aikana.

-   Euron (EUR) ja Yhdysvaltain dollarin (USD) vaihtokurssi laskun päivämääränä: 1,2062
-   Euron ja Yhdysvaltain dollarin vaihtokurssi maksun päivämääränä: 1,2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Lasku kirjataan Fabrikam Eastiin Fabrikam Westin asiakkaalle 4000

| Tili:                             | Veloitussumma:            | Hyvityssumma:           |
|-------------------------------------|-------------------------|-------------------------|
| Myyntireskontra (Fabrikam East) | 600,00 (EUR) / 723,72 (USD) |                         |
| Myynti (Fabrikam East)               |                         | 600,00 (EUR) / 723,72 (USD) |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Maksu vastaanotetaan ja kirjataan Fabrikamiin Fabrikamin asiakkaalle 4000

| Tili:                        | Veloitussumma:            | Hyvityssumma:           |
|--------------------------------|-------------------------|-------------------------|
| Käteinen (Fabrikam)                | 600,00 (EUR) / 736,62 (USD) |                         |
| Myyntireskontra (Fabrikam) |                         | 600,00 (EUR) / 736,62 (USD) |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikamin maksu selvitetään Fabrikam Eastin laskun kanssa

**Kirjaus Fabrikamiin**

| Tili:                         | Veloitussumma:            | Hyvityssumma:           |
|---------------------------------|-------------------------|-------------------------|
| Myyntireskontra (Fabrikam)  | 600,00 (EUR) / 736,62 (USD) |                         |
| Saaja Fabrikam East (Fabrikam) |                         | 600,00 (EUR) / 736,62 (USD) |
| Saaja Fabrikam East (Fabrikam) | 0,00 (EUR) / 12,90 (USD)    |                         |
| Realisoitunut voitto (Fabrikam)        |                         | 0,00 (EUR) / 12,90 (USD)    |

**Kirjaus Fabrikam Eastiin**

| Tili:                             | Veloitussumma:            | Hyvityssumma:           |
|-------------------------------------|-------------------------|-------------------------|
| Maksaja Fabrikam (Fabrikam East)   | 600,00 (EUR) / 736,62 (USD) |                         |
| Myyntireskontra (Fabrikam East) |                         | 600,00 (EUR) / 736,62 (USD) |
| Myyntireskontra (Fabrikam East) | 0,00 (EUR) / 12,90 (USD)    |                         |
| Maksaja Fabrikam (Fabrikam East)   |                         | 0,00 (EUR) / 12,90 (USD)    |

## <a name="example-4-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-gain"></a>Esimerkki 4: Asiakkaan laskun, käteisalennuksen ja toteutuneen vaihtokurssivoiton maksaminen toisesta yrityksestä
Fabrikam kirjaa Fabrikamin asiakkaan 4000, Northwind Traders, maksun Fabrikam Eastin avoimelle laskulle. Laskussa on käytettävissä käteisalennus, ja arvonlisäverotapahtuma muodostetaan. Maksu selvitetään Fabrikam Eastin avoimen laskun kanssa. Valuuttakurssivoittotapahtuma muodostetaan selvitysprosessin aikana. Käteisalennus kirjataan laskutusyritykseen (Fabrikam Eastiin) ja vaihtokurssivoitto maksutapahtuman yritykseen (Fabrikamiin).

-   Euron ja Yhdysvaltain dollarin vaihtokurssi laskun päivämääränä: 1,2062
-   Euron ja Yhdysvaltain dollarin vaihtokurssi maksun päivämääränä: 1,2277

### <a name="free-text-invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-customer-4000"></a>Vapaatekstilasku kirjataan ja verotapahtuma muodostetaan Fabrikam Eastiin asiakkaalle 4000

| Tili:                             | Veloitussumma:            | Hyvityssumma:           |
|-------------------------------------|-------------------------|-------------------------|
| Myyntireskontra (Fabrikam East) | 638,22 (EUR) / 769,82 (USD) |                         |
| Myynti (Fabrikam East)               |                         | 600,00 (EUR) / 723,72 (USD) |
| Arvonlisävero (Fabrikam East)           |                         | 38,22 (EUR) / 46,10 (USD)   |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>Maksu vastaanotetaan ja kirjataan Fabrikamiin asiakkaalle 4000

| Tili:                        | Veloitussumma:            | Hyvityssumma:           |
|--------------------------------|-------------------------|-------------------------|
| Käteinen (Fabrikam)                | 626,22 (EUR) / 768,81 (USD) |                         |
| Myyntireskontra (Fabrikam) |                         | 626,22 (EUR) / 768,81 (USD) |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikamin maksu selvitetään Fabrikam Eastin laskun kanssa

**Kirjaus Fabrikamiin**

| Tili:                         | Veloitussumma:            | Hyvityssumma:           |
|---------------------------------|-------------------------|-------------------------|
| Myyntireskontra (Fabrikam)  | 626,22 (EUR) / 768,81 (USD) |                         |
| Saaja Fabrikam East (Fabrikam) |                         | 626,22 (EUR) / 768,81 (USD) |
| Saaja Fabrikam East (Fabrikam) | 0,00 (EUR) / 13,46 (USD)    |                         |
| Realisoitunut voitto (Fabrikam)        |                         | 0,00 (EUR) / 13,46 (USD)    |

**Kirjaus Fabrikam Eastiin**

| Tili:                             | Veloitussumma:            | Hyvityssumma:           |
|-------------------------------------|-------------------------|-------------------------|
| Maksaja Fabrikam (Fabrikam East)   | 626,22 (EUR) / 768,81 (USD) |                         |
| Myyntireskontra (Fabrikam East) |                         | 626,22 (EUR) / 768,81 (USD) |
| Myyntireskontra (Fabrikam East)  | 0,00 (EUR) / 13,46 (USD)    |                         |
| Maksaja Fabrikam (Fabrikam East)   |                         | 0,00 (EUR) / 13,46 (USD)    |
| Käteisalennus (Fabrikam East)       | 12,00 (EUR) / 14,47 (USD)   |                         |
| Myyntireskontra (Fabrikam East) |                         | 12,00 (EUR) / 14,47 (USD)   |

## <a name="example-5-customer-credit-note-with-primary-payment"></a>Esimerkki 5: Asiakkaan hyvityslasku ja ensisijainen maksu
Fabrikam vastaanottaa maksun, jonka summa on 75,00, asiakkaalta 4000, Northwind Traders. Maksu selvitetään Fabrikam Westin asiakkaan 10000 avoimen laskun ja Fabrikam Eastin asiakkaan 4000 avoimen hyvityslaskun kanssa. Maksu valitaan ensisijaiseksi maksuksi **Selvitä tapahtumat** -sivulla.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>Lasku kirjataan Fabrikam Westiin asiakkaalle 10000

| Tili                             | Veloitussumma: | Hyvityssumma: |
|-------------------------------------|--------------|---------------|
| Myyntireskontra (Fabrikam West) | 100,00       |               |
| Myynti (Fabrikam West)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>Hyvityslasku kirjataan Fabrikam Eastiin asiakkaalle 4000

| Tili:                             | Veloitussumma: | Hyvityssumma: |
|-------------------------------------|--------------|---------------|
| Myyntipalautukset (Fabrikam East)       | 25,00        |               |
| Myyntireskontra (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>Maksu kirjataan Fabrikamiin asiakkaalle 4000

| Tili:                        | Veloitussumma: | Hyvityssumma: |
|--------------------------------|--------------|---------------|
| Käteinen (Fabrikam)                | 75,00        |               |
| Myyntireskontra (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikamin maksu selvitetään Fabrikam Westin laskun ja Fabrikam Eastin hyvityslaskun kanssa

**Kirjaus Fabrikamiin**

| Tili:                           | Veloitussumma: | Hyvityssumma: |
|-----------------------------------|--------------|---------------|
| Maksaja Fabrikam East (Fabrikam) | 25,00        |               |
| Myyntireskontra (Fabrikam)    |              | 25,00         |
| Myyntireskontra (Fabrikam)    | 100,00       |               |
| Saaja Fabrikam West (Fabrikam)   |              | 100,00        |

**Kirjaus Fabrikam Eastiin**

| Tili:                             | Veloitussumma: | Hyvityssumma: |
|-------------------------------------|--------------|---------------|
| Myyntireskontra (Fabrikam East) | 25,00        |               |
| Saaja Fabrikam (Fabrikam East)     |              | 25,00         |

**Kirjaus Fabrikam Westiin**

| Tili:                             | Veloitussumma: | Hyvityssumma: |
|-------------------------------------|--------------|---------------|
| Maksaja Fabrikam (Fabrikam West)   | 100,00       |               |
| Myyntireskontra (Fabrikam West) |              | 100,00        |

## <a name="example-6-customer-credit-note-without-primary-payment"></a>Esimerkki 6: Asiakkaan hyvityslasku ilman ensisijaista maksua
Fabrikam vastaanottaa maksun, jonka summa on 75,00, asiakkaalta 4000, Northwind Traders. Maksu selvitetään Fabrikam Westin asiakkaan 10000 avoimen laskun ja Fabrikam Eastin asiakkaan 4000 avoimen hyvityslaskun kanssa. Maksu ei valita ensisijaiseksi maksuksi **Selvitä tapahtumat** -sivulla.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>Lasku kirjataan Fabrikam Westiin asiakkaalle 10000

| Tili                             | Veloitussumma: | Hyvityssumma: |
|-------------------------------------|--------------|---------------|
| Myyntireskontra (Fabrikam West) | 100,00       |               |
| Myynti (Fabrikam West)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>Hyvityslasku kirjataan Fabrikam Eastiin asiakkaalle 4000

| Tili:                             | Veloitussumma: | Hyvityssumma: |
|-------------------------------------|--------------|---------------|
| Myyntipalautukset (Fabrikam East)       | 25,00        |               |
| Myyntireskontra (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>Maksu kirjataan Fabrikamiin asiakkaalle 4000

| Tili:                        | Veloitussumma: | Hyvityssumma: |
|--------------------------------|--------------|---------------|
| Käteinen (Fabrikam)                | 75,00        |               |
| Myyntireskontra (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikamin maksu selvitetään Fabrikam Westin laskun ja Fabrikam Eastin hyvityslaskun kanssa

**Kirjaus Fabrikamiin**

| Tili:                         | Veloitussumma: | Hyvityssumma: |
|---------------------------------|--------------|---------------|
| Myyntireskontra (Fabrikam)  | 75,00        |               |
| Saaja Fabrikam West (Fabrikam) |              | 75,00         |

**Kirjaus Fabrikam Eastiin**

| Tili:                              | Veloitussumma: | Hyvityssumma: |
|--------------------------------------|--------------|---------------|
| Myyntireskontra (Fabrikam East)  | 25,00        |               |
| Saaja Fabrikam West (Fabrikam East) |              | 25,00         |

**Kirjaus Fabrikam Westiin**

| Tili:                                | Veloitussumma: | Hyvityssumma: |
|----------------------------------------|--------------|---------------|
| Maksaja Fabrikam (Fabrikam West)      | 75,00        |               |
| Myyntireskontra (Fabrikam West)    |              | 75,00         |
| Maksaja Fabrikam East (Fabrikam West) | 25,00        |               |
| Myyntireskontra (Fabrikam West)    |              | 25,00         |
