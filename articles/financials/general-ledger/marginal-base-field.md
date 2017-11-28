---
title: "Arvonlisäveroprosentit Alv-rajan peruste- ja Laskentatapa-kenttien perusteella"
description: "Tässä ohjeaiheessa kerrotaan, miten Alv-rajan peruste- ja Laskentatapa-kenttien arvot määrittävät myynti- ja ostotapahtumien veroprosentit."
author: twheeloc
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bf0f8f2e3f553ea181e8cc9ab5b712fce64a89d4
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a>Arvonlisäveroprosentit Alv-rajan peruste- ja Laskentatapa-kenttien perusteella

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa kerrotaan, miten Alv-rajan peruste- ja Laskentatapa-kenttien arvot määrittävät myynti- ja ostotapahtumien veroprosentit.

ALV-rajan peruste Arvonlisäverokoodit-sivun Laskenta-pikavälilehdessä määrittää, millä summalla sopiva veroprosentti valitaan Arvonlisäverokoodin arvot -sivulla olevista prosenteista. Alv-rajan peruste -kentän summatyyppi yhdessä Laskentatapa-kentässä valitun menetelmän kanssa määrittää logiikan, jolla tapahtumalle etsitään oikea veroprosentti. 

Seuraavat esimerkit osoittavat, että syöttämällä näihin kenttiin erilaisia yhdistelmiä saadaan hyvin erilaisia arvonlisäverolaskutuloksia. Esimerkeissä käytetään samoja verovälin arvoja, jotka määritetään jokaiselle verokoodille Arvonlisäverokoodin arvot -sivulla. Voit avata sivun valitsemalla Arvonlisäverokoodi &gt; Arvonlisäverokoodit arvot -sivu.

> [!Important]                                                                                                                  
> Jos vähintään yhden arvolisäverokoodin Alv-rajan peruste perustuu rivin summiin tai yksiköihin, Kirjanpitoparametrit-sivun Laskentapa-kentän arvoksi on määritettävä Rivi. |

## <a name="net-amount-per-line"></a> Rivikohtainen nettosumma
Valitsemalla tämän asetuksen voit määrittää arvonlisäveroprosentit laskurivien nettosumman perusteella ilman muita veroja.

### <a name="example"></a>Esimerkki

Arvonlisäveroprosentit määritetään seuraavilla väleillä.

| Summaväli    | Veroprosentti |
|--------------------|----------|
| 0–50             | 30 %      |
| 50–100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

> [!NOTE]                                                                                                             
> Viimeisen välin yläraja nolla (0) tarkoittaa sitä, että väliin sisällytetään kaikki summat, jotka ovat yli 100.

Alv-rajan peruste: **Nettosumma riveittäin** 

Laskentatapa: **Väli** 

Ostat 8 lamppua, joista jokaisen hinta on 25,00. 

Laskurivin nettosumma on 200,00. 

Vero lasketaan seuraavasti: 

Arvonlisävero yhteensä = 50 x 30 % + 50 x 20 % + 100 x 10 % = 15 + 10 + 10 = 35,00. 

Laskun kokonaissumma = 200,00 + 35,00 = 235,00. 

**Vaihtelu** 

Jos laskussa on kaksi riviä ja kumpikin rivi sisältää 4 nimikettä, kunkin rivin nettosumma on 100,00 ja arvonlisävero lasketaan seuraavasti: 

Arvonlisäverorivi 1 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00. 

Arvonlisäverorivi 2 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00. 

Arvonlisävero yhteensä = 25,00 + 25,00 = 50,00 

Laskun kokonaissumma = 200,00 + 50,00 = 250,00

## <a name="net-amount-per-unit"></a> Yksikkökohtainen nettosumma
Valitsemalla tämän asetuksen voit määrittää arvonlisäveroprosentit kunkin yksikön arvon perusteella ilman muita veroja. Jos yksikköperusteinen ALV-rajan peruste valitaan, myös arvonlisäverokoodille on määritettävä myös yksikkö.

### <a name="example"></a>Esimerkki

Arvonlisäveroprosentit määritetään seuraavilla väleillä.

| Summa             | Veroprosentti |
|--------------------|----------|
| 0–50             | 30 %      |
| 50–100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

Alv-rajan peruste: **Yksikkökohtainen nettosumma** 

Laskentatapa: **Koko summa** 

Ostat 8 lamppua, joista jokaisen hinta on 25,00. 

Laskurivin nettosumma on 200,00. 

Vero lasketaan seuraavasti: Yksikkökohtainen arvonlisävero = 25,00 x 30 % = 7,50 Arvonlisävero yhteensä = 7,50 x 8 yksikköä = 60,00 Laskun kokonaissumma = 200,00 + 60,00 = 260,00

## <a name="net-amount-of-invoice-balance"></a> Laskun saldon nettosumma

Valitsemalla tämän asetuksen voit määrittää arvonlisäveroprosentit laskun kokonaisarvon perusteella ilman muita veroja.

### <a name="example"></a>Esimerkki

Arvonlisäveroprosentit määritetään seuraavilla väleillä.

| Summa            | Veroprosentti |
|-------------------|----------|
| 0–50            | 30 %      |
| 50–100          | 20 %      |
| 100 -0 (&gt; 100) | 10 %      |

Alv-rajan peruste: **Laskun saldon nettosumma** 

Laskentatapa: **Väli** Myyntilaskussa on 2 riviä ja kummallakin rivillä 4 lamppua, joiden hinta on 25,00. Laskun saldon nettosumma on 4 x 25,00 + 4 x 25,00 = 200,00. Vero lasketaan seuraavasti: Arvonlisävero yhteensä = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 + 10 = 35,00 Laskun kokonaissumma = 200,00 + 35,00 = 235,00

## <a name="gross-amount-per-line"></a> Rivikohtainen bruttosumma

Valitsemalla tämän asetuksen voit määrittää arvonlisäveroprosentit rivin arvon perusteella. Rivin arvo sisältää myös muut kyseisen rivin verot.

> [!NOTE]
> Arvonlisäveroryhmässä voi olla vain yksi arvonlisäverokoodi, jossa tämä valinta on tehty Alv-rajan peruste -kentässä.

### <a name="example"></a>Esimerkki

Arvonlisäveroprosentit määritetään seuraavilla väleillä.

| Summa             | Veroprosentti |
|--------------------|----------|
| 0–50             | 30 %      |
| 50–100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

ALV-rajan peruste: **Rivikohtainen bruttosumma** Laskentatapa: **Väli** Kullakin lampulla on myös erikoismaksu, jonka suuruus on 5,00 ja jolle lasketaan toinen verokoodi. Erikoismaksu lisätään nettosummaan ennen arvonlisäveron laskemista. Ostat 8 lamppua, joista jokaisen hinta on 25,00. Laskurivin nettosumma on 200,00. Laskurivin bruttosumma on 8 x 25,00 + 8 x 5,00 = 240,00. Vero lasketaan seuraavasti: Arvonlisävero yhteensä = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 Erikoismaksut yhteensä = 5,00 x 8 = 40,00 Laskun kokonaissumma = 200,00 + 39,00 + 40,00 = 279,00

**Vaihtelu** 

Jos lasku luodaan käyttämällä kahta laskuriviä ja kumpikin rivi sisältää 4 nimikettä, laskurivin nettosumma on 100. Laskurivikohtainen bruttosumma (mukaan lukien vero 4 x 5,00) olisi 120,00 ja arvonlisävero luodaan seuraavasti: Arvonlisävero laskun rivi 1 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Arvonlisävero laskun rivi 2 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Arvonlisävero yhteensä = 27,00 + 27,00 = 54,00 Erikoismaksut yhteensä = 5,00 x 8 = 40,00 Laskun kokonaissumma = 200,00 + 54,00 + 40,00 = 294,00

## <a name="gross-amount-per-unit"></a> Yksikkökohtainen bruttosumma

Valitsemalla tämän asetuksen voit määrittää arvonlisäveroprosentit kunkin yksikön arvon perusteella mukaan lukien muut verot.

> [!NOTE]
> Arvonlisäveroryhmässä voi olla vain yksi arvonlisäverokoodi, jossa tämä valinta on tehty Alv-rajan peruste -kentässä.

### <a name="example"></a>Esimerkki

Arvonlisäveroprosentit määritetään seuraavilla väleillä.

| Summa             | Veroprosentti |
|--------------------|----------|
| 0–50             | 30 %      |
| 50–100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

ALV-rajan peruste: **Yksikkökohtainen bruttosumma** Kullakin lampulla on erikoismaksu, jonka suuruus on 5,00. Erikoismaksu lisätään nettosummaan ennen arvonlisäveron laskemista. Ostat 8 lamppua, joista jokaisen hinta on 25,00. Yksikkökohtainen bruttosumma on 30,00. Vero lasketaan seuraavasti: Yksikkökohtainen arvonlisävero = 30 x 30 % = 9,00 Arvonlisävero yhteensä 9,00 + 8 = 72,00 Erikoismaksu yhteensä = 5,00 + 8 = 40,00 Laskun kokonaissumma = 200,00 + 72,00 + 40,00 = 312,00

## <a name="invoice-total-incl-other-sales-tax-amounts"></a> Laskun loppusumma muut arvonlisäverosummat mukaan luettuna

Valitsemalla tämän asetuksen voit määrittää arvonlisäveroprosentit laskun kokonaisarvon perusteella mukaan lukien muut verot.
> [!NOTE]
> Arvonlisäveroryhmässä voi olla vain yksi arvonlisäverokoodi, jossa tämä valinta on tehty Alv-rajan peruste -kentässä

### <a name="example"></a>Esimerkki

Arvonlisäveroprosentit määritetään seuraavilla väleillä.

| Summa             | Veroprosentti |
|--------------------|----------|
| 0–50             | 30 %      |
| 50–100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

Alv-rajan peruste: **Laskun loppusumma muut arvonlisäverosummat mukaan luettuna** Laskentatapa: **Väli**   
Jokaisella lampulla on erikoismaksu 5,00. Erikoismaksu lisätään nettosummaan ennen arvonlisäveron laskemista. Ostat 8 lamppua, joista jokaisen hinta on 25,00. Laskun nettosumma on 200,00. Laskun bruttosumma on 200,00 + (8 x 5,00) = 240,00. Vero lasketaan seuraavasti: Arvonlisävero yhteensä = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Erikoismaksut yhteensä = 5,00 x 8 = 40,00 Laskun kokonaissumma = 200,00 + 39,00 + 40,00 = 279,00

Lisätietoja: [Alv-koodien koko summa- ja väli-laskentavaihtoehdot](whole-amount-interval-options-sales-tax-codes.md) [Arvonlisäveron laskentatavat Alkuperä-kentässä](sales-tax-calculation-methods-origin-field.md)




