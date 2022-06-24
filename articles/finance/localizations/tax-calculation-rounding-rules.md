---
title: Verolaskennan pyöristyssäännöt
description: Tässä artikkelissa on tietoja verolaskentapalvelun verolaskentaparametrien pyöristyssäännöistä.
author: kailiang
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 0f6182ab18a5a408a6e526feec7014ccdfce8af0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858298"
---
# <a name="tax-calculation-rounding-rules"></a>Verolaskennan pyöristyssäännöt

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja verolaskentapalvelun verolaskentaparametrien pyöristyssääntöjen toiminnasta.

> [!NOTE] 
> Kun verolaskentapalvelu otetaan käyttöön, **Arvonlisäverokoodi**- ja **Arvonlisäveroryhmä**-sivujen pyöristyssäännöt eivät ole käytössä.

Verolaskentapalvelun pyöristyssääntöjen määrityksiä voi tarkastella **Verolaskentaparametrit**-sivun **Yleiset**-välilehden **Laskenta**-pikavälilehden **Arvonlisäveron pyöristyssääntö** -osassa (**Vero** \> **Asetukset** \> **Veromääritykset** \> **Verolaskentaparametrit**).

[![Pyöristyssääntömääritykset Verolaskentaparametrit-sivulla](./media/tax-calculation-parameters-calculation-1.png)](./media/tax-calculation-parameters-calculation-1.png)

**Pyöristystarkkuus**- ja **Pyöristysmenetelmä**-kentät määrittävät, miten verolaskentapalvelujen tiedoissa olevat lasketut summat pyöristetään.

## <a name="rounding-precision"></a>Pyöristystarkkuus

**Pyöristystarkkuus**-kentät tukevat arvoa, jossa on enintään kuusi desimaalia. Jos **Pyöristystarkkuus**-kentän arvoksi määritetään esimerkiksi **0,000000**, lasketut summat pyöristetään kuuteen desimaaliin ja lähetetään sitten Microsoft Dynamics 365 Financeen. Jos pyöristysmenetelmänä on käytössä esimerkiksi **Normaali**, summa **987,1234567** pyöristetään summaksi **987,123457**.

> [!NOTE]
> Finance pyöristää summat valuutan pyöristyssääntöjen mukaisesti. Niinpä sekä verolaskennan että valuutan pyöristyssäännöt koskevat tapahtumissa näkyviä ja niihin kirjattuja veron määriä.

## <a name="rounding-method"></a>Pyöristysmenetelmä

Kullekin yritykselle voidaan määrittää verolaskennassa käytettävä pyöristysmenetelmä. **Pyöristysmenetelmä**-kentässä on valittavana kolme vaihtoehtoa: **Normaali**, **Alaspäin** ja **Pyöristys ylös**.

### <a name="rounding-example"></a>Pyöristysesimerkki

Seuraavan taulukon esimerkki osoittaa, miten summa **987,345** pyöristetään erilaisilla pyöristystarkkuuden ja -menetelmien yhdistelmillä.

<table>
<thead>
<tr>
<th rowspan="2">Pyöristysmenetelmä</th>
<th colspan="8">Pyöristystarkkuus</th>
</tr>
<tr>
<th>0,00</th>
<th>0.01</th>
<th>0.10</th>
<th>1.00</th>
<th>10.00</th>
<th>0.02</th>
<th>0.05</th>
<th>0.25</th>
</tr>
</thead>
<tbody>
<tr>
<td>Normaali</td>
<td>987.35</td>
<td>987.35</td>
<td>987.30</td>
<td>987.00</td>
<td>990.00</td>
<td>987.34</td>
<td>987.35</td>
<td>987.25</td>
</tr>
<tr>
<td>Alaspäin</td>
<td>987.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.00</td>
<td>980.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.25</td>
</tr>
<tr>
<td>Ylöspäin</td>
<td>988.00</td>
<td>987.35</td>
<td>987.40</td>
<td>988.00</td>
<td>990.00</td>
<td>987.36</td>
<td>987.35</td>
<td>987.50</td>
</tr>
</tbody>
</table>

Veron määrän laskenta- ja pyöristyslogiikka voidaan määrittää verotussääntöjen mukaisesti.

## <a name="rounding-by"></a>Pyöristys 

Valitse **Pyöristys:**-kentässä veroja koskeva pyöristysperiaate. Käytettävissä ovat seuraavat asetukset:

- **Verokoodit** – veron määrä pyöristetään kussakin verokoodissa.
- **Verokoodiyhdistelmät** – veron määrä pyöristetään rivillä olevassa verokoodiyhdistelmässä.

## <a name="calculation-method"></a>Laskentatapa

**Laskentatapa**-kentässä valitaan, lasketaanko verot laskuissa jokaisella rivillä vai yhteisesti kaikille riveille. Käytettävissä ovat seuraavat asetukset:

- **Rivi** – Veron määrä lasketaan kullakin rivillä. Muiden rivien veron määrä ei vaikuta rivin veron määrään.
- **Yhteensä** – veron määrä lasketaan kaikilta yhden asiakirjan riveiltä.

### <a name="rounding-calculation-example"></a>Pyöristyksen laskentaesimerkki

Tässä esimerkissä näytetään yhdessä laskussa tehtävät erilaiset laskennat, kun käytössä on erilaiset **Pyöritys:**- ja **Laskentatapa**-arvojen yhdistelmät. Tässä esimerkissä on käytössä seuraavat määritykset:

- Laskussa on neljä riviä.
- Verokoodeja on kaksi: **ALV1** (10 prosenttia) ja **ALV2** (10 prosenttia).
- Pyöristystarkkuus on **0,01**.
- Pyöristysmenetelmäksi on määritetty **Pyöristys:**.

#### <a name="rounding-by--tax-codes-and-calculation-method--line"></a>Pyöristys: = Verokoodit ja Laskentatapa = Rivi

| Rivinumero | Rivin nettosumma | Määritetyt verokoodit | Veron määrä ennen pyöristystä | Pyöristetty veron määrä |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | ALV1                 | 1.111                      | 1.12               |
| 2           | 22.22           | ALV1; ALV2           | 2,222; 2,222               | 2,23; 2,23         |
| 3           | 33.33           | ALV1                 | 3.333                      | 3.34               |
| 4           | 44.44           | ALV1; ALV2           | 4,444; 4,444               | 4,45; 4,45         |

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--line"></a>Pyöristys: = Verokoodiyhdistelmä ja Laskentatapa = Rivi

| Rivinumero | Rivin nettosumma | Määritetyt verokoodit | Veron määrä ennen pyöristystä | Pyöristetty veron määrä |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | ALV1                 | 1.111                      | 1.12               |
| 2\*         | 22.22           | ALV1; ALV2           | 2,222; 2,222               | 2,23; 2,22         |
| 3           | 33.33           | ALV1                 | 3.333                      | 3.34               |
| 4\*\*       | 44.44           | ALV1; ALV2           | 4,444; 4,444               | 4,45; 4,44         |

\* Rivi 2 = Pyöristys\[22,22 × (10 prosenttia + 10 prosenttia)\] = 2,23 + 2,22

\*\* Rivi 4 = Pyöristys\[44,44 × (10 prosenttia + 10 prosenttia)\] = 4,45 + 4,44

#### <a name="rounding-by--tax-codes-and-calculation-method--total"></a>Pyöristys: = Verokoodit ja Laskentatapa = Yhteensä

| Rivinumero | Rivin nettosumma | Määritetyt verokoodit | Veron määrä ennen pyöristystä | Pyöristetty veron määrä |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | ALV1\*               | 1.111                      | 1.12               |
| 2           | 22.22           | ALV1\*; ALV2\*\*     | 2,222; 2,222               | 2,22; 2,23         |
| 3           | 33.33           | ALV1\*               | 3.333                      | 3.33               |
| 4           | 44.44           | ALV1\*; ALV2\*\*     | 4,444; 4,444               | 4,44; 4,44         |

\* ALV1(Rivi 1, Rivi 2, Rivi 3, Rivi 4) = Pyöristys\[(11,11 + 22,22 + 33,33 + 44,44) × 10 prosenttia\] = 1,12 + 2,22 + 3,33 + 4,44

\*\* ALV2(Rivi 2, Rivi 4) = Pyöristys\[(22,22 + 44,44) × 10 prosenttia\] = 2,23 + 4,44

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--total"></a>Pyöristys: = Verokoodiyhdistelmä ja Laskentatapa = Yhteensä

| Rivinumero | Rivin nettosumma | Määritetyt verokoodit | Veron määrä ennen pyöristystä | Pyöristetty veron määrä |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1\*         | 11.11           | ALV1                 | 1.111                      | 1.12               |
| 2\*\*       | 22.22           | ALV1; ALV2           | 2,222; 2,222               | 2,23; 2,22         |
| 3\*         | 33.33           | ALV1                 | 3.333                      | 3.33               |
| 4\*\*       | 44.44           | ALV1; ALV2           | 4,444; 4,444               | 4,44; 4,45         |

\* Rivi 1, Rivi 3 = Pyöristys\[(11,11 + 33,33) × 10 prosenttia\] = 1,12 + 3,33

\*\* Rivi 2, Rivi 4 = Pyöristys\[(22,22 + 44,44) × (10 prosenttia + 10 prosenttia)\] = 2,23 + 2,22 + 4,44 + 4,45

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
