---
title: "Arvonlisäveroprosentit ALV-rajan peruste-ja laskentamenetelmiä"
description: "Tässä artikkelissa kerrotaan, miten Alv-rajan peruste- ja Laskentatapa-kenttien arvot määrittävät myynti- ja ostotapahtumien veroprosentit."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: ad731401fe553cdc50665cc87aaac64dc48813f2
ms.lasthandoff: 03/31/2017


---

# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a>Arvonlisäveroprosentit ALV-rajan peruste-ja laskentamenetelmiä

Tässä artikkelissa kerrotaan, miten Alv-rajan peruste- ja Laskentatapa-kenttien arvot määrittävät myynti- ja ostotapahtumien veroprosentit.

ALV-rajan peruste Arvonlisäverokoodit-sivun Laskenta-pikavälilehdessä määrittää, millä summalla sopiva veroprosentti valitaan Arvonlisäverokoodin arvot -sivulla olevista prosenteista. Alv-rajan peruste -kentän summatyyppi yhdessä Laskentatapa-kentässä valitun menetelmän kanssa määrittää logiikan, jolla tapahtumalle etsitään oikea veroprosentti. 

Seuraavat esimerkit osoittavat, että syöttämällä näihin kenttiin erilaisia yhdistelmiä saadaan hyvin erilaisia arvonlisäverolaskutuloksia. Esimerkeissä käytetään samoja verovälin arvoja, jotka määritetään jokaiselle verokoodille Arvonlisäverokoodin arvot -sivulla. Jos haluat avata tämän sivun, valitse arvonlisäverokoodi &gt;ALV-koodit sivulla arvoja.

> [!Important]                                                                                                                  
> Jos vähintään yhden arvolisäverokoodin Alv-rajan peruste perustuu rivin summiin tai yksiköihin, Kirjanpitoparametrit-sivun Laskentapa-kentän arvoksi on määritettävä Rivi. |

## <a name="net-amount-per-line"></a>Rivikohtainen nettosumma
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

ALV-rajan peruste: **yhden rivin nettosumma** 

Laskutapa: **aikaväli** 

Ostat 8 lamppua, joista jokaisen hinta on 25,00. 

Laskurivin nettosumma on 200,00. 

Vero lasketaan seuraavasti: 

Arvonlisävero yhteensä = 50 x 30 % + 50 x 20 % + 10 % x 100 = 15 + 10 + 10 = 35,00 

Laskutussumma 200,00 + 35,00 = 235.00 = 

**Variation** 

Jos lasku on kaksi riviä, jossa on neljä osaa kullekin riville, kunkin rivin nettosumma on 100,00 ja arvonlisävero lasketaan seuraavasti: 

Arvonlisäveron rivi 1 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00 

Arvonlisäveron rivi 2 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00 

Arvonlisävero yhteensä = 25,00 + 25,00 = 50,00 

Laskun loppusumma = 200,00 + 50,00 = 250,00

## <a name="net-amount-per-unit"></a> Yksikkökohtainen nettosumma
Valitsemalla tämän asetuksen voit määrittää arvonlisäveroprosentit kunkin yksikön arvon perusteella ilman muita veroja. Jos yksikköperusteinen ALV-rajan peruste valitaan, myös arvonlisäverokoodille on määritettävä myös yksikkö.

### <a name="example"></a>Esimerkki

Arvonlisäveroprosentit määritetään seuraavilla väleillä.

| Summa             | Veroprosentti |
|--------------------|----------|
| 0–50             | 30 %      |
| 50–100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

ALV-rajan peruste: **Net summa per yksikkö** 

Laskutapa: **koko summa** 

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

ALV-rajan peruste: **laskun saldon nettosumma** 

Laskentatapa: **aikaväli** myyntilasku on kunkin komentorivit ollessa 25,00 2 rivit 4 valaisimien kanssa. Laskun saldon nettosumma on 4 x 25,00 + 4 x 25,00 = 200,00. Vero lasketaan seuraavasti: Arvonlisävero yhteensä = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 + 10 = 35,00 Laskun kokonaissumma = 200,00 + 35,00 = 235,00

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

ALV-rajan peruste: **Rivikohtainen bruttosumma** Laskentatapa: **Väli** Kullakin lampulla on myös erikoismaksu, jonka suuruus on 5,00 ja jolle lasketaan toinen verokoodi. Erikoismaksu lisätään nettosummaan ennen arvonlisäveron laskemista. Ostat 8 lamppua, joista jokaisen hinta on 25,00. Laskurivin nettosumma on 200,00. Laskurivin bruttosumma on 8 x 25,00 + 8 x 5,00 = 240,00. Vero lasketaan seuraavasti: arvonlisävero yhteensä = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 yhteensä tullin 5.00 x 8 = 40,00 = laskun loppusumma = 200,00 + 39,00 + 40,00 = 279,00

**Variation** 

Jos lasku luodaan käyttämällä Huoltolaskun rivit 2 ja 4 kullakin rivillä oleville nimikkeille, laskurivin nettosumma on 100,00. Laskurivikohtainen bruttosumma (mukaan lukien vero 4 x 5,00) olisi 120,00 ja arvonlisävero luodaan seuraavasti: Arvonlisävero laskun rivi 1 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Arvonlisävero laskun rivi 2 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Arvonlisävero yhteensä = 27,00 + 27,00 = 54,00 Erikoismaksut yhteensä = 5,00 x 8 = 40,00 Laskun kokonaissumma = 200,00 + 54,00 + 40,00 = 294,00

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
> Valitse alv-ryhmä voi olla vain yksi arvonlisäverokoodi tämän valinnan kanssa rajan peruste-kentässä

### <a name="example"></a>Esimerkki

Arvonlisäveroprosentit määritetään seuraavilla väleillä.

| Summa             | Veroprosentti |
|--------------------|----------|
| 0–50             | 30 %      |
| 50–100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

ALV-rajan peruste: **laskun summa sisältäen muut arvonlisäverosummat** laskentatapaa: **aikaväli**   
On erityinen velvollisuus Jokaisella lampulla 5,00. Erikoismaksu lisätään nettosummaan ennen arvonlisäveron laskemista. Ostat 8 lamppua, joista jokaisen hinta on 25,00. Laskun nettosumma on 200,00. Laskun bruttosumma on 200,00 + (8 x 5,00) = 240,00. Vero lasketaan seuraavasti: Arvonlisävero yhteensä = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Erikoismaksut yhteensä = 5,00 x 8 = 40,00 Laskun kokonaissumma = 200,00 + 39,00 + 40,00 = 279,00

Lisätietoja on ohjeaiheessa [koko summan ja arvonlisäverokoodien aikavälin laskenta-asetukset](whole-amount-interval-options-sales-tax-codes.md) ja [laskentamenetelmät arvonlisäveron Alkuperä-kentässä](sales-tax-calculation-methods-origin-field.md).


