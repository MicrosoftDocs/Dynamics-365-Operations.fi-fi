---
title: Arvonlisäveron laskenta ja pyöristys
description: Tässä artikkelissa on yhteenveto arvonlisäveron laskennasta ja pyöristyksestä sekä tietoja arvonlisäveron laskennan ja pyöristyksen asetusten parametreista.
author: wangchen
ms.date: 06/01/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom:
- "13111"
- intro-internal
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2022-05-31
ms.dyn365.ops.version: AX 10.0.28
ms.openlocfilehash: aa3564f0fcf4a958637ba4a5cdcc497bffc50000
ms.sourcegitcommit: 8b716849707ec96d1cb4cac85b9e782dc25f5a70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/07/2022
ms.locfileid: "8939230"
---
# <a name="sales-tax-calculation-and-rounding"></a>Arvonlisäveron laskenta ja pyöristys

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on yhteenveto arvonlisäveron laskennasta ja pyöristyksestä Microsoft Dynamics 365 Financessa. Artikkelissa kerrotaan myös parametrit, joita käytetään arvonlisäveron laskennan ja pyöristyksen asetuksissa sekä määritetään, miten nämä parametrit toimivat yhdessä.

## <a name="parameters"></a>Parametrit

Arvonlisäveron laskentaa ja pyöristystä ohjaavat seuraavat parametrit:

- **Laskentatapa** – Tämä parametri määritetään **Kirjanpitoparametrit** -sivulla. Se määrittää, lasketaanko veron perussumma asiakirjaa vai riviä kohti. Jos arvonlisäverokoodin **Alv-rajan peruste** -parametrin arvoksi on määritetty **Laskun saldon nettosumma**, veron perussumma lasketaan aina asiakirjaa kohti tämän parametrin asetuksesta huolimatta.
- **Pyöristys** – Tämä parametri määritetään arvonlisäveroryhmälle. Se määrittää, pyöristetäänkö verosumma arvonlisäverokoodin vai arvonlisäverokoodin yhdistelmän mukaan.
- **Alkuperä** – Tämä parametri määritetään arvonlisäverokoodille. Se määrittää, miten verosumma lasketaan. Lisätietoja on kohdassa [Arvonlisäveron laskentatavat Alkuperä-kentässä](sales-tax-calculation-methods-origin-field.md).
- **Alv-rajan peruste** – Tämä parametri määritetään arvonlisäverokoodille. Se määrittää, mitä summaa käytetään valittaessa soveltuvat veroprosentit **Arvonlisäverokoodin arvot** -sivulla. Lisätietoja on kohdassa [Alv-rajan perusteeseen ja Laskentatapoihin perustuva arvonlisäveroprosentti](marginal-base-field.md).
- **Arvonlisäveron pyöristyssääntö** – Tämä parametri on määritetty arvonlisäverokoodille. Se määrittää, miten määritetty arvonlisäverosumma pyöristetään, mukaan lukien pyöristyksen tarkkuus ja pyöristystapa.

Tämän artikkelin loppuosassa esitellään joitakin edellisten parametrien yhdistelmää käyttävän arvonlisäveron laskennan ja pyöristyksen tyypillisiä esimerkkejä.

## <a name="scenario-for-the-examples"></a>Esimerkkiskenaario

- Verotettavassa asiakirjassa on kaksi riviä. Kunkin rivin veron perussumma on 42,42.
- Kullekin riville määritetään kaksi arvonlisäverokoodia, jotka ovat arvonlisäverokoodi 1 ja arvonlisäverokoodi 2.
- Sekä verokoodin 1 että verokoodin 2 veroprosentti on 10.
- Hinta ei sisällä veroa.
- Pyöristystarkkuus on 0,01.
- Pyöristysmenetelmäksi on määritetty **Pyöristä ylöspäin**.

## <a name="example-1"></a>Esimerkki 1

### <a name="parameter-values"></a>Parametrin arvot

| Laskentatapa | Pyöristys    | Peruste                   | Alv-rajan peruste       |
| ------------------ | -------------- | ------------------------ | ------------------- |
| Rivi               | Arvonlisäverokoodi | Prosenttia nettosummasta | Rivikohtainen nettosumma |

### <a name="calculation-and-rounding-behavior"></a>Laskennan ja pyöristyksen toiminta

| Rivinumero | Arvonlisäverokoodi | Alkuperäinen summa | Arvonlisäveron summa |
| ------------| ---------------| --------------| -----------------|
| 1           | Koodi 1         | 42.42         | 4.25             |
| 1           | Koodi 2         | 42.42         | 4.25             |
| 2           | Koodi 1         | 42.42         | 4.25             |
| 2           | Koodi 2         | 42.42         | 4.25             |

Veron perussumma lasketaan riviä kohti:

- **Rivi 1:** 42,42
- **Rivi 2:** 42,42

Verosumma lasketaan arvonlisäverokoodia kohti:

- **Rivi 1:**

    - Verosumma arvonlisäverokoodille 1 = 42,42 &times; 10 prosenttia = 4,242
    - Verosumma arvonlisäverokoodille 2 = 42,42 &times; 10 prosenttia = 4,242

- **Rivi 2:**

    - Verosumma arvonlisäverokoodille 1 = 42,42 &times; 10 prosenttia = 4,242
    - Verosumma arvonlisäverokoodille 2 = 42,42 &times; 10 prosenttia = 4,242

Verosumma pyöristetään arvonlisäverokoodia kohti:

- **Rivi 1:**

    - Pyöristetty verosumma arvonlisäverokoodille 1 = 4,25
    - Pyöristetty verosumma arvonlisäverokoodille 2 = 4,25

- **Rivi 2:**

    - Pyöristetty verosumma arvonlisäverokoodille 1 = 4,25
    - Pyöristetty verosumma arvonlisäverokoodille 2 = 4,25

## <a name="example-2"></a>Esimerkki 2

### <a name="parameter-values"></a>Parametrin arvot

| Laskentatapa | Pyöristys    | Peruste                   | Alv-rajan peruste                 |
| ------------------ | -------------- | ------------------------ | ----------------------------- |
| Rivi/yhteensä         | Arvonlisäverokoodi | Prosenttia nettosummasta | Laskun saldon nettosumma |

### <a name="calculation-and-rounding-behavior"></a>Laskennan ja pyöristyksen toiminta

| Rivinumero | Arvonlisäverokoodi | Alkuperäinen summa | Arvonlisäveron summa |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Koodi 1         | 42.42         | 4.25             |
| 1           | Koodi 2         | 42.42         | 4.25             |
| 2           | Koodi 1         | 42.42         | 4.24             |
| 2           | Koodi 2         | 42.42         | 4.24             |

Veron perussumma lasketaan asiakirjaa kohti:

- Veron perussumma = 42,42 + 42,42 = 84,84

Verosumma lasketaan arvonlisäverokoodia kohti:

- Verosumma arvonlisäverokoodille 1 = 84,84 &times; 10 prosenttia = 8,484
- Verosumma arvonlisäverokoodille 2 = 84,84 &times; 10 prosenttia = 8,484

Verosumma pyöristetään arvonlisäverokoodia kohti:

- Pyöristetty verosumma arvonlisäverokoodille 1 = 8,49
- Pyöristetty verosumma arvonlisäverokoodille 2 = 8,49

Pyöristetty verosumma kohdistetaan kullekin riville arvonlisäverokoodia kohti:

- Kohdista pyöristetty verosumma arvonlisäverokoodille 1 (8,49) riville 1 (4,25) ja riville 2 (4,24).
- Kohdista pyöristetty verosumma arvonlisäverokoodille 2 (8,49) riville 1 (4,25) ja riville 2 (4,24).

## <a name="example-3"></a>Esimerkki 3

### <a name="parameter-values"></a>Parametrin arvot

| Laskentatapa | Pyöristys    | Peruste                              | Alv-rajan peruste       |
| ------------------ | -------------- | ----------------------------------- | ------------------- |
| Rivi               | Arvonlisäverokoodi | Laskettu nettosummaprosentti | Rivikohtainen nettosumma |

### <a name="calculation-and-rounding-behavior"></a>Laskennan ja pyöristyksen toiminta

| Rivinumero | Arvonlisäverokoodi | Alkuperäinen summa | Arvonlisäveron summa |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Koodi 1         | 42.42         | 4.72             |
| 1           | Koodi 2         | 42.42         | 4.72             |
| 2           | Koodi 1         | 42.42         | 4.72             |
| 2           | Koodi 2         | 42.42         | 4.72             |

Veron perussumma lasketaan riviä kohti:

- **Rivi 1:** 42,42
- **Rivi 2:** 42,42

Verosumma lasketaan arvonlisäverokoodia kohti:

- **Rivi 1:**

    - Verosumma arvonlisäverokoodille 1 = 42,42 &times; 10 prosenttia &divide; (1 – 10 prosenttia) = 4,7133
    - Verosumma arvonlisäverokoodille 2 = 42,42 &times; 10 prosenttia &divide; (1 – 10 prosenttia) = 4,7133

- **Rivi 2:**

    - Verosumma arvonlisäverokoodille 1 = 42,42 &times; 10 prosenttia &divide; (1 – 10 prosenttia) = 4,7133
    - Verosumma arvonlisäverokoodille 2 = 42,42 &times; 10 prosenttia &divide; (1 – 10 prosenttia) = 4,7133

Verosumma pyöristetään arvonlisäverokoodia kohti:

- **Rivi 1:**

    - Pyöristetty verosumma arvonlisäverokoodille 1 = 4,72
    - Pyöristetty verosumma arvonlisäverokoodille 2 = 4,72

- **Rivi 2:**

    - Pyöristetty verosumma arvonlisäverokoodille 1 = 4,72
    - Pyöristetty verosumma arvonlisäverokoodille 2 = 4,72

## <a name="example-4"></a>Esimerkki 4

### <a name="parameter-values"></a>Parametrin arvot

| Laskentatapa | Pyöristys    | Peruste                              | Alv-rajan peruste                 |
| ------------------ | -------------- | ----------------------------------- | ----------------------------- |
| Rivi/yhteensä         | Arvonlisäverokoodi | Laskettu nettosummaprosentti | Laskun saldon nettosumma |

### <a name="calculation-and-rounding-behavior"></a>Laskennan ja pyöristyksen toiminta

| Rivinumero | Arvonlisäverokoodi | Alkuperäinen summa | Arvonlisäveron summa |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Koodi 1         | 42.42         | 4.72             |
| 1           | Koodi 2         | 42.42         | 4.72             |
| 2           | Koodi 1         | 42.42         | 4.71             |
| 2           | Koodi 2         | 42.42         | 4.71             |

Veron perussumma lasketaan asiakirjaa kohti:

- Veron perussumma = 42,42 + 42,42 = 84,84

Verosumma lasketaan arvonlisäverokoodia kohti:

- Verosumma arvonlisäverokoodille 1 = 84,84 &times; 10 prosenttia &divide; (1 – 10 prosenttia) = 9,4267
- Verosumma arvonlisäverokoodille 2 = 84,84 &times; 10 prosenttia &divide; (1 – 10 prosenttia) = 9,4267

Verosumma pyöristetään arvonlisäverokoodia kohti:

- Pyöristetty verosumma arvonlisäverokoodille 1 = 9,43
- Pyöristetty verosumma arvonlisäverokoodille 2 = 9,43

Pyöristetty verosumma kohdistetaan kullekin riville arvonlisäverokoodia kohti:

- Kohdista verosumma arvonlisäverokoodille 1 (9,43) riville 1 (4,72) ja riville 2 (4,71).
- Kohdista verosumma arvonlisäverokoodille 2 (9,43) riville 1 (4,72) ja riville 2 (4,71).

## <a name="example-5"></a>Esimerkki 5

### <a name="parameter-values"></a>Parametrin arvot

| Laskentatapa | Pyöristys                | Peruste                   | Alv-rajan peruste       |
| ------------------ | -------------------------- | ------------------------ | ------------------- |
| Rivi               | Arvonlisäverokoodiyhdistelmä | Prosenttia nettosummasta | Rivikohtainen nettosumma |

### <a name="calculation-and-rounding-behavior"></a>Laskennan ja pyöristyksen toiminta

| Rivinumero | Arvonlisäverokoodi | Alkuperäinen summa | Arvonlisäveron summa |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Koodi 1         | 42.42         | 4.25             |
| 1           | Koodi 2         | 42.42         | 4.24             |
| 2           | Koodi 1         | 42.42         | 4.24             |
| 2           | Koodi 2         | 42.42         | 4.24             |

Veron perussumma lasketaan riviä kohti:

- **Rivi 1:** 42,42
- **Rivi 2:** 42,42

Verosumma lasketaan arvonlisäverokoodia kohti:

- **Rivi 1:**

    - Verosumma arvonlisäverokoodille 1 = 42,42 &times; 10 prosenttia = 4,242
    - verosumma arvonlisäverokoodille 2 = 42,42 &times; 10 prosenttia = 4,242

- **Rivi 2:**

    - Verosumma arvonlisäverokoodille 1 = 42,42 &times; 10 prosenttia = 4,242
    - Verosumma arvonlisäverokoodille 2 = 42,42 &times; 10 prosenttia = 4,242

Verosumma pyöristetään arvonlisäverokoodin yhdistelmää kohti:

- Arvonlisäveron summa yhteensä = 4,242 + 4,242 + 4,242 + 4,242 = 16,968, joka pyöristetään summaksi 16,97

Pyöristetty verosumma kohdistetaan kullekin riville arvonlisäverokoodia kohti:

- Kohdista arvonlisäverosumma (16,97) riville 1 ja riville 2:

    - **Rivi 1:**

        - Verosumma arvonlisäverokoodille 1 = 4,25
        - Verosumma arvonlisäverokoodille 2 = 4,24

    - **Rivi 2:**

        - Verosumma arvonlisäverokoodille 1 = 4,24
        - Verosumma arvonlisäverokoodille 2 = 4,24

## <a name="example-6"></a>Esimerkki 6

### <a name="parameter-values"></a>Parametrin arvot

| Laskentatapa | Pyöristys                | Peruste                   | Alv-rajan peruste                 |
| ------------------ | -------------------------- | ------------------------ | ----------------------------- |
| Rivi/yhteensä         | Arvonlisäverokoodiyhdistelmä | Prosenttia nettosummasta | Laskun saldon nettosumma |

### <a name="calculation-and-rounding-behavior"></a>Laskennan ja pyöristyksen toiminta

| Rivinumero | Arvonlisäverokoodi | Alkuperäinen summa | Arvonlisäveron summa |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Koodi 1         | 42.42         | 4.25             |
| 1           | Koodi 2         | 42.42         | 4.24             |
| 2           | Koodi 1         | 42.42         | 4.24             |
| 2           | Koodi 2         | 42.42         | 4.24             |

Veron perussumma lasketaan asiakirjaa kohti:

- Veron perussumma = 42,42 + 42,42 = 84,84

Verosumma lasketaan arvonlisäverokoodia kohti:

- Verosumma arvonlisäverokoodille 1 = 84,84 &times; 10 prosenttia = 8,484
- Verosumma arvonlisäverokoodille 2 = 84,84 &times; 10 prosenttia = 8,484

Verosumma pyöristetään arvonlisäverokoodin yhdistelmää kohti:

- Arvonlisäveron summa yhteensä = 8,484 + 8,484 = 16,968, joka pyöristetään summaksi 16,97

Pyöristetty verosumma kohdistetaan kullekin riville arvonlisäverokoodia kohti:

- Kohdista arvonlisäverosumma (16,97) riville 1 ja riville 2:

    - **Rivi 1:**

        - Verosumma arvonlisäverokoodille 1 = 4,25
        - Verosumma arvonlisäverokoodille 2 = 4,24

    - **Rivi 2:**

        - Verosumma arvonlisäverokoodille 1 = 4,24
        - Verosumma arvonlisäverokoodille 2 = 4,24

## <a name="example-7"></a>Esimerkki 7

### <a name="parameter-values"></a>Parametrin arvot

| Laskentatapa | Pyöristys                | Peruste                              | Alv-rajan peruste       |
| ------------------ | -------------------------- | ----------------------------------- | ------------------- |
| Rivi               | Arvonlisäverokoodiyhdistelmä | Laskettu nettosummaprosentti | Rivikohtainen nettosumma |

### <a name="calculation-and-rounding-behavior"></a>Laskennan ja pyöristyksen toiminta

| Rivinumero | Arvonlisäverokoodi | Alkuperäinen summa | Arvonlisäveron summa |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Koodi 1         | 42.42         | 4.72             |
| 1           | Koodi 2         | 42.42         | 4.71             |
| 2           | Koodi 1         | 42.42         | 4.71             |
| 2           | Koodi 2         | 42.42         | 4.72             |

Veron perussumma lasketaan riviä kohti:

- **Rivi 1:** 42,42
- **Rivi 2:** 42,42

Verosumma lasketaan arvonlisäverokoodia kohti:

- **Rivi 1:**

    - Verosumma arvonlisäverokoodille 1 = 42,42 &times; 10 prosenttia &divide; (1 – 10 prosenttia) = 4,7133
    - Verosumma arvonlisäverokoodille 2 = 42,42 &times; 10 prosenttia &divide; (1 – 10 prosenttia) = 4,7133

- **Rivi 2:**

    - Verosumma arvonlisäverokoodille 1 = 42,42 &times; 10 prosenttia &divide; (1 – 10 prosenttia) = 4,7133
    - Verosumma arvonlisäverokoodille 2 = 42,42 &times; 10 prosenttia &divide; (1 – 10 prosenttia) = 4,7133

Verosumma pyöristetään arvonlisäverokoodin yhdistelmää kohti:

- Arvonlisäveron summa yhteensä = 4,7133 + 4,7133 + 4,7133 + 4,7133 = 18,8532, joka pyöristetään summaksi 18,86

Pyöristetty verosumma kohdistetaan kullekin riville arvonlisäverokoodia kohti:

- Kohdista arvonlisäverosumma (18,86) riville 1 ja riville 2:

    - **Rivi 1:**

        - Verosumma arvonlisäverokoodille 1 = 4,72
        - Verosumma arvonlisäverokoodille 2 = 4,71

    - **Rivi 2:**

        - Verosumma arvonlisäverokoodille 1 = 4,71
        - Verosumma arvonlisäverokoodille 2 = 4,72

## <a name="example-8"></a>Esimerkki 8

### <a name="parameter-values"></a>Parametrin arvot

| Laskentatapa | Pyöristys                | Peruste                              | Alv-rajan peruste                 |
| ------------------ | -------------------------- | ----------------------------------- | ----------------------------- |
| Rivi/yhteensä         | Arvonlisäverokoodiyhdistelmä | Laskettu nettosummaprosentti | Laskun saldon nettosumma |

### <a name="calculation-and-rounding-behavior"></a>Laskennan ja pyöristyksen toiminta

| Rivinumero | Arvonlisäverokoodi | Alkuperäinen summa | Arvonlisäveron summa |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Koodi 1         | 42.42         | 4.72             |
| 1           | Koodi 2         | 42.42         | 4.71             |
| 2           | Koodi 1         | 42.42         | 4.71             |
| 2           | Koodi 2         | 42.42         | 4.72             |

Veron perussumma lasketaan asiakirjaa kohti:

- Veron perussumma = 42,42 + 42,42 = 84,84

Verosumma lasketaan arvonlisäverokoodia kohti:

- Verosumma arvonlisäverokoodille 1 = 84,84 &times; 10 prosenttia &divide; (1 – 10 prosenttia) = 9,4267
- Verosumma arvonlisäverokoodille 2 = 84,84 &times; 10 prosenttia &divide; (1 – 10 prosenttia) = 9,4267

Verosumma pyöristetään arvonlisäverokoodin yhdistelmää kohti:

- Arvonlisäveron summa yhteensä = 9,4267 + 9,4267 = 18,8534, joka pyöristetään summaksi 18,86

Pyöristetty verosumma kohdistetaan kullekin riville arvonlisäverokoodia kohti:

- Kohdista arvonlisäverosumma (18,86) riville 1 ja riville 2:

    - **Rivi 1:**

        - Verosumma arvonlisäverokoodille 1 = 4,72
        - Verosumma arvonlisäverokoodille 2 = 4,71

    - **Rivi 2:**

        - Verosumma arvonlisäverokoodille 1 = 4,71
        - Verosumma arvonlisäverokoodille 2 = 4,72

## <a name="additional-resources"></a>Lisäresurssit

- [Arvonlisäveron laskentatavat Alkuperä-kentässä](sales-tax-calculation-methods-origin-field.md)
- [Arvonlisäveroprosentit Alv-rajan peruste- ja Laskentatapa-kenttien perusteella](marginal-base-field.md)
- [Arvonlisäverokoodien koko summan ja välin laskentavaihtoehdot](whole-amount-interval-options-sales-tax-codes.md)
