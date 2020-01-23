---
title: Loman ja poissaolon käsitteet
description: Tässä ohjeaiheessa käsitellään loman ja poissaolon käsitteitä sekä poissaolosaldojen määrittämistä.
author: andreabichsel
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 03e2557e29194f17a9a586470ced5b352408b07c
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898639"
---
# <a name="leave-and-absence-concepts"></a>Loman ja poissaolon käsitteet

Tässä ohjeaiheessa käsitellyt käsitteet ja termit auttavat määrittämään, miten työntekijälle myönnetään palkkioksi vapaa-aikaa ja miten työntekijän aikasaldot lasketaan. Lisätietoja lomien ja poissaolojen hallinnasta on kohdassa [Lomien ja poissaolojen hallinta](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).

## <a name="leave-plan-details"></a>Lomasuunnitelman tiedot

### <a name="start-date"></a>Aloituspäivämäärä

Aloituspäivämäärä on päivämäärä, jolloin kertymän käsittely alkaa. Aloituspäivämäärä on myös vuosipäivä, jonka mukaan siirtokirjaussummat lasketaan.

## <a name="accruals"></a>Jaksotukset

Kertymät määrittävät, milloin ja miten usein työntekijälle myönnetään palkkiona vapaa-aikaa. Kertymisten myöntämisajankohtaa ja suhteellista jakoa koskevat käytännöt määritetään **Jaksotukset**-osassa, kun loma- ja poissaolosuunnitelma määritetään.

### <a name="accrual-frequency"></a>Kertymäväli

Kertymäväli määrittää, kuinka usein loma kerätään tai myönnetään palkkioksi. Käytettävissä ovat seuraavat asetukset:

- Päivittäin
- Viikoittain
- Kaksi kertaa viikossa
- Kaksi kertaa kuussa
- Kuukausittain
- Neljännesvuosittain
- Puolivuosittain
- Vuosittain
- Ei mitään

### <a name="accrual-period-basis"></a>Kertymäkauden perusta

Kertymäkauden perusta määrittää päivämäärän, jonka avulla kertymäkaudet lasketaan. Käytettävissä ovat seuraavat asetukset:

- **Suunnitelman aloituspäivämäärä**
- **Työntekijäkohtainen päivämäärä** – Kun tämä asetus on valittu, arvo määrittää alkuperäisen päivämääräarvon, jonka avulla kertymäkaudet lasketaan. Käytettävissä ovat seuraavat asetukset:

    - Mukautettu
    - Vuosipäivän päivämäärä
    - Alkuperäinen työsuhteen alkamispäivämäärä
    - Ikälisäpäivä
    - Työntekijän muutettu aloituspäivämäärä
    - Työntekijän aloituspäivämäärä

### <a name="accrual-award-date"></a>Palkkion jaksotuspäivämäärä

Palkkion kertymäpäivämäärä määrittää, milloin työntekijälle myönnetään palkkiona vapaa-aikaa. Käytettävissä ovat seuraavat asetukset:

- **Jaksotuskauden loppupäivämäärä** – työntekijälle myönnetään palkkiona vapaa-aikaa palkkiokauden viimeisenä päivänä.

    Oikean määrän kertyminen edellyttää, että kertymisprosessi sisältää koko kauden. Esimerkki: Kertymäkausi on 1.1.–31.1.2018. Jos tammikuu halutaan tässä tapauksessa sisällyttää, kertymä on suoritettava 1.2.2018.

- **Jaksotuskauden aloituspäivämäärä** – työntekijälle myönnetään palkkiona vapaa-aikaa palkkiokauden ensimmäisenä päivänä.

### <a name="accrual-policy-on-enrollment"></a>Kertymäkäytäntö rekisteröinnin yhteydessä

Rekisteröitymiseen liittyvä kertymäkäytäntö määrittää, miten kertymä lasketaan, kun työntekijä rekisteröidään kertymäkauden aikana. Käytettävissä ovat seuraavat asetukset:

- **Suhteellisesti jaettu** – Päivien välinen ero määritetään rekisteröitymis- ja aloituspäivämäärän välisen eron perusteella. Kyseistä eroa käytetään, kun kertymiä käsitellään.
- **Täysi kertymä** – tasoon perustuva täysi kertymä myönnetään palkkiona ensimmäisen kertymäkäsittelyn aikana.
- **Ei kertymää** – jaksotusta ei myönnetä palkkiona ennen seuraavaa kertymäkautta.

### <a name="accrual-policy-on-unenrollment"></a>Kertymäkäytäntö rekisteröitymisen poiston yhteydessä

Kertymäkäytännön rekisteröinnin poisto määrittää, miten kertymä lasketaan, kun työntekijän rekisteröinti poistetaan kertymäkauden aikana. Käytettävissä ovat seuraavat asetukset:

- **Suhteellisesti jaettu** – Päivien välinen ero määritetään rekisteröitymis- ja aloituspäivämäärän välisen eron perusteella. Kyseistä eroa käytetään, kun kertymiä käsitellään.
- **Täysi kertymä** – tasoon perustuva täysi kertymä myönnetään palkkiona ensimmäisen kertymäkäsittelyn aikana.
- **Ei kertymää** – jaksotusta ei myönnetä palkkiona ennen seuraavaa kertymäkautta.

## <a name="accrual-schedule"></a>Kertymäaikataulu

Kertymäaikataulu määrittää, miten työntekijälle kertyy vapaa-aikaa, sekä työntekijälle kertyvät määrät, joille tehdään siirtokirjaus. Luotujen tasojen avulla vapaa-aikaa voidaan myöntää palkkiona eri perustein.

### <a name="months-of-service"></a>Työkuukaudet

**Työkuukaudet**-arvo määrittää, kuinka monta kuukautta työntekijän on vähintään oltava töissä, jotta heille voi syntyä kertymiä. Jos työntekijöille ei määritetä vähimmäisarvoa, arvoksi määritetään **0**.

### <a name="hours-worked"></a>Työtunnit

**Työtunnit**-arvo määrittää, kuinka monta tuntia työntekijän on tehtävä töitä kertymäkaudella, jotta hänelle voi syntyä kertymiä. Jos työntekijöille ei määritetä vähimmäisarvoa, arvoksi määritetään **0**.

### <a name="accrual-amount"></a>Jaksotussumma

Kertymäsumma on se tuntien tai päivien määrä, joka työntekijöille kertyy kunkin kauden aikana. Kausi perustuu kertymäväliin.

### <a name="minimum-balance"></a>Vähimmäissaldo

Vähimmäissaldolla voi olla negatiivinen arvo, jos työntekijät pyytämä loma-aika ylittää heidän käytössään olevan loma-ajan.

### <a name="maximum-carry-forward"></a>Enimmäissiirtokirjaus

Kertymäprosessi oikaisee enimmäissiirtokirjauksen saldon ylittävät lomasaldot aloituspäivämäärän vuosipäivänä.

### <a name="grant-amount"></a>Myönnetty summa

Myönnetty summa on työntekijöille aluksi myönnetty tuntien tai päivien määrä, kun rekisteröityvät lomasuunnitelmaan ensimmäisen kerran. Summaa ei jaksoteta kullekin kertymäkaudelle.

## <a name="enrollments-and-balances"></a>Rekisteröitymiset ja saldot

### <a name="enrollment-date"></a>Rekisteröintipäivä

Rekisteröintipäivä määrittää, milloin työntekijä voi aloittaa vapaa-ajan keräämisen. Jos työntekijä esimerkiksi on rekisteröitynyt lomasuunnitelmaan 15.6.2018, hän voi aloittaa vapaa-ajan keräämisen vasta 15.6.2018.

### <a name="current-balance"></a>Nykyinen saldo

Nykyisen saldo on se loman määrä, joka on vapaa-aikapyyntöjen käytettävissä. Tämä määrä sisältää kertymät, hyväksytyt pyynnöt ja oikaisut kuluvaan päivämäärään mennessä.

### <a name="current-balance-examples"></a>Nykyiseen saldoon liittyviä esimerkkejä

#### <a name="annual-plan"></a>Vuosisuunnitelma

**Suunnitelman asetukset**

| Suunnitelman aloituspäivämäärä | Rekisteröintipäivä | Kertymäväli | Kertymäkauden perusta | Palkkion jaksotuspäivämäärä    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Vuosittainen            | Suunnitelman aloituspäivämäärä      | Kertymäkauden loppupäivämäärä |

Kertymät käsitellään 1. tammikuuta 2019 (1.1.2019), joten siihen sisältyy koko kausi.

**Tulokset**

| Jaksotussumma | Vähimmäissaldo | Enimmäissiirtokirjaus | Pyydetty määrä | Nykyinen saldo (1.1.2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 200            | 0               | 120                   | 40             | 160                              |

Nykyinen saldo (160) = kertynyt määrä (200) – pyydetty määrä (40)

#### <a name="semimonthly-plan"></a>Kaksi kertaa kuussa -suunnitelma

**Suunnitelman asetukset**

| Suunnitelman aloituspäivämäärä | Rekisteröintipäivä | Kertymäväli | Kertymäkauden perusta | Palkkion jaksotuspäivämäärä    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kaksi kertaa kuussa       | Suunnitelman aloituspäivämäärä      | Kertymäkauden loppupäivämäärä |

Kertymät käsitellään 1. toukokuuta 2018 (1.5.2018), joten siihen sisältyy koko kausi.

**Tulokset**

| Jaksotussumma | Vähimmäissaldo | Enimmäissiirtokirjaus | Pyydetty määrä | Nykyinen saldo (1.1.2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 22                               |

Nykyinen saldo (22) = kertynyt määrä (5 × 6) – pyydetty määrä (8)

#### <a name="monthly-plan"></a>Kuukausisuunnitelma

**Suunnitelman asetukset**

| Suunnitelman aloituspäivämäärä | Rekisteröintipäivä | Kertymäväli | Kertymäkauden perusta | Palkkion jaksotuspäivämäärä    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kaksi kertaa kuussa       | Suunnitelman aloituspäivämäärä      | Kertymäkauden loppupäivämäärä |

Kertymät käsitellään 1. toukokuuta 2018 (1.5.2018), joten siihen sisältyy koko kausi.

**Tulokset**

| Jaksotussumma | Vähimmäissaldo | Enimmäissiirtokirjaus | Pyydetty määrä | Nykyinen saldo (1.1.2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 7                                |

Nykyinen saldo (7) = kertynyt määrä (5 × 3) – pyydetty määrä (8)

### <a name="forecasted-balance"></a>Ennustettu saldo

*Ennustettu saldo* on se loman määrä, joka on käytettävissä tulevana ajankohtana. Kertymät ja siirtokirjausten oikaisut ennustetaan kyseiseen päivämäärään saakka.

Seuraavaa kaavaa käytetään:

Maanantain ennustettu saldo = nykyinen saldo – pyynnöt + kertymät – siirtokirjausoikaisu

### <a name="forecasted-balance-examples"></a>Esimerkkejä ennustetusta saldosta

#### <a name="annual-plan"></a>Vuosisuunnitelma

**Suunnitelman asetukset**

| Suunnitelman aloituspäivämäärä | Rekisteröintipäivä | Kertymäväli | Kertymäkauden perusta | Palkkion jaksotuspäivämäärä    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Vuosittainen            | Suunnitelman aloituspäivämäärä      | Kertymäkauden loppupäivämäärä |

Kertymät käsitellään 15. helmikuuta 2019 (15.2.2019), joten siihen sisältyy koko kausi.

**Tulokset**

| Jaksotussumma | Vähimmäissaldo | Enimmäissiirtokirjaus | Nykyinen saldo | Ennustettu saldo (15.2.2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 20             | 0               | 20                    | 40              | 40                                   |

Ennustettu saldo (40) = kertynyt määrä (20) + nykyinen saldo (40) – siirtokirjausoikaisu (20)

#### <a name="semimonthly-plan"></a>Kaksi kertaa kuussa -suunnitelma

**Suunnitelman asetukset**

| Suunnitelman aloituspäivämäärä | Rekisteröintipäivä | Kertymäväli | Kertymäkauden perusta | Palkkion jaksotuspäivämäärä    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kaksi kertaa kuussa       | Suunnitelman aloituspäivämäärä      | Kertymäkauden loppupäivämäärä |

Kertymät käsitellään 15. helmikuuta 2019 (15.2.2019), joten siihen sisältyy koko kausi.

**Tulokset**

| Jaksotussumma | Vähimmäissaldo | Enimmäissiirtokirjaus | Nykyinen saldo | Ennustettu saldo (15.2.2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 5              | 0               | 20                    | 40              | 35                                   |

Ennustettu saldo (35) = kertynyt määrä (5 × 3) + nykyinen saldo (40) – siirtokirjausoikaisu (20)

#### <a name="monthly-plan"></a>Kuukausisuunnitelma

**Suunnitelman asetukset**

| Suunnitelman aloituspäivämäärä | Rekisteröintipäivä | Kertymäväli | Kertymäkauden perusta | Palkkion jaksotuspäivämäärä    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kaksi kertaa kuussa       | Suunnitelman aloituspäivämäärä      | Kertymäkauden loppupäivämäärä |

Kertymät käsitellään 15. helmikuuta 2019 (15.2.2019), joten siihen sisältyy koko kausi.

**Tulokset**

| Jaksotussumma | Vähimmäissaldo | Enimmäissiirtokirjaus | Nykyinen saldo | Ennustettu saldo (15.2.2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 10             | 0               | 20                    | 40              | 30                                   |

Ennustettu saldo (30) = kertynyt määrä (10 × 1) + nykyinen saldo (40) – siirtokirjausoikaisu (20)

### <a name="proration-balance-examples"></a>Esimerkkejä jaetusta saldosta

#### <a name="prorated-monthly-plan"></a>Jaettu kuukausisuunnitelma

**Suunnitelman asetukset**

| Suunnitelman aloituspäivämäärä | Kertymäväli | Kertymäkauden perusta |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Kuukausittain           | Suunnitelman aloituspäivämäärä      |

**Tulokset**

| Työntekijä             | Työkuukaudet | Rekisteröintipäivä | Aloituspäivämäärä | Jaksotussumma | Kertymän käsittely | Tase |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 2,53    |

#### <a name="full-accrual-monthly-plan"></a>Täyden kertymän kuukausisuunnitelma

**Suunnitelman asetukset**

| Suunnitelman aloituspäivämäärä | Kertymäväli | Kertymäkauden perusta |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Kuukausittain           | Suunnitelman aloituspäivämäärä      |

**Tulokset**

| Työntekijä             | Työkuukaudet | Rekisteröintipäivä | Aloituspäivämäärä | Jaksotussumma | Kertymän käsittely | Tase |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 3,00    |

#### <a name="no-accrual-monthly-plan"></a>Ei kertymää kuukausisuunnitelmassa

**Suunnitelman asetukset**

| Suunnitelman aloituspäivämäärä | Kertymäväli | Kertymäkauden perusta |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Kuukausittain           | Suunnitelman aloituspäivämäärä      |

**Tulokset**

| Työntekijä             | Työkuukaudet | Rekisteröintipäivä | Aloituspäivämäärä | Jaksotussumma | Kertymän käsittely | Tase |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 2,00    |
