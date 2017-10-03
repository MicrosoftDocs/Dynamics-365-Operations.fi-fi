---
title: "Arvonlisäveron laskentatavat Alkuperä-kentässä"
description: "Tässä artikkelissa käsitellään arvonlisäveron koodisivun Peruste-kentän vaihtoehtoja sekä sitä, miten arvonlisävero lasketaan valitun vaihtoehdon perusteella arvonlisäverokoodille."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f420341a7d5d12825a983ee96e814f0eedbc60c4
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017

---

# <a name="sales-tax-calculation-methods-in-the-origin-field"></a>Arvonlisäveron laskentatavat Alkuperä-kentässä

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Tässä artikkelissa käsitellään arvonlisäveron koodisivun Peruste-kentän vaihtoehtoja sekä sitä, miten arvonlisävero lasketaan valitun vaihtoehdon perusteella arvonlisäverokoodille.

Kun luot arvonlisäverokoodeja Arvonlisäverokoodit-sivulla, sinun täytyy valita laskentatapa, jota käytetään Alkuperä-kentässä olevaan veron perustesummaan.

## <a name="percentage-of-net-amount"></a>Prosenttia nettosummasta
Prosenttia nettosummasta -laskentatapa on Alkuperä-kentässä oletusarvona. Arvonlisävero lasketaan osto- tai myyntihinnan prosenttiarvona, kun hintaan ei sisälly muita veroja.
### <a name="example"></a>Esimerkki

Veroprosentti on 25 %. Laskurivillä näkyvä nimikemäärä on 10 ja hinta 1,00/nimike, ja asiakkaalle myönnetään 10 %:n rivialennus. Nettosumma: (10 x 1,00) -10 % = 9,00 Arvonlisävero: 9,00 x 25 % = 2,25 Kokonaissumma: 9,00 + 2,25 = 11,25

## <a name="percentage-of-gross-amount"></a> Prosenttia bruttosummasta
Jos valitset Prosenttia bruttosummasta -laskentatavan, arvonlisävero lasketaan bruttomyyntihinnan prosenttiosuutena. Bruttosumma on rivin nettosumma sekä kaikki rivin verot ja maksut, lukuun ottamatta veroa, jossa Alkuperä = Prosenttia bruttosummasta.
### <a name="example"></a>Esimerkki

Verottaja on säätänyt tätä kohdetta koskevia erikoismaksuja. Erikoismaksusummat lisätään nettosummaan ennen arvonlisäveron laskemista. Käytetään seuraavia arvonlisäverokoodeja:
-   MAKSU 1 = 10 %, Prosenttia nettosummasta -laskentatapa
-   MAKSU 2 = 20 %, Prosenttia nettosummasta -laskentatapa
-   ALV = 25 %, Prosenttia bruttosummasta -laskentatapa

Jos nettosumma on 10,00, niin MAKSU 1 on 1,00 (10,00 x 10 %) ja MAKSU 2 = 2,00 (10,00 x 20 %). Summat ovat seuraavat: Bruttosumma: Nettosumma + MAKSU 1 -summa + MAKSU 2 -summa (10,00 + 1,00 + 2,00) = 13,00 ALV = 13,00 x 25 % = 3,25 MAKSUT ja ALV yhteensä: 1,00 + 2,00 + 3,25 = 6,25 Kokonaissumma: 10,00 + 6,25 = 16,25
| **Huomautus**                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tapahtumassa voi käyttää vain yhtä verokoodia, jossa Alkuperä = Prosenttia bruttosummasta. Jos tapahtumalle määritetään useita tällaisia verokoodeja, näyttöön tulee virhesanoma, jonka mukaan arvonlisäveroa ei voi laskea. |

 
<a name="percentage-of-sales-tax"></a>Arvonlisäveroprosentti
-----------------------

Kun valitset Alkuperä-kentästä Arvonlisäveroprosentti-vaihtoehdon, arvonlisävero lasketaan prosenttina Arvonlisäveron arvonlisävero -kentässä valitusta arvonlisäverosta. Arvonlisäveron arvonlisävero -kentästä valittu arvonlisävero lasketaan ensin. Toinen arvonlisävero lasketaan sitten ensimmäisen arvonlisäverosumman perusteella.
### <a name="example"></a>Esimerkki

Käytetään seuraavia arvonlisäverokoodeja:
-   MAKSU 1 = 10 %, Prosenttia nettosummasta -laskentatapa
-   MAKSU 2 = 20 %, Arvonlisäveroprosentti-laskentatapa ja Maksu 1 Arvonlisäveron arvonlisävero -kentästä
-   ALV = 25 %, Prosenttia bruttosummasta -laskentatapa

Nettosumma: 10,00 MAKSU 1: 10,00 x 10 % = 1,00 MAKSU 2: 1,00 x 20 % = 0,20 Bruttosumma: 10,00 + 1,00 + 0,20 = 11,20 ALV: 11,20 x 25 % = 2,80 MAKSUT ja ALV yhteensä: 1,00 + 0,20 + 2,80 = 4,00 Kokonaissumma: 10,00 + 4,00 = 14,00
| **Huomautus**                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verolaskutoimituksissa ei voi käyttää monen tason veroja. Veroa ei voi laskea sellaisen veron perusteella, joka on jo laskettu toisen veron perusteella. Tapahtumalle voi laskea useita verokoodeihin perustuvia yhden tason veroja. |

## <a name="amount-per-unit"></a> Summa per yksikkö
Kun Alkuperä-kentästä valitaan Summa per yksikkö, arvonlisävero lasketaan kiinteänä summana yksikköä kohti kerrottuna asiakirjan riville syötetyllä määrällä. Yksikkö on valittava Yksikkö-kentästä. Yksikkökohtainen hinta määritetään Arvonlisäverokoodin arvot -sivulla.
### <a name="example"></a>Esimerkki

Arvonlisäverokoodiksi on määritetty: 1,20 USD / yksikkö = laatikko Myyntilaskurivillä nimikettä myydään 25 laatikkoa Arvonlisäveroksi lasketaan 25 x 1,20 = 30,00
| **Huomautus**                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jos tapahtumalla on eri yksikkö kuin arvonlisäverokoodissa määritetty, se muunnetaan automaattisesti Yksikkömuunnokset-sivulla määritettyjen yksikkömuunnosten perusteella. |

###  <a name="amount-per-unit-additional-option"></a> Summa per yksikkö, lisävaihtoehto

Laskenta-välilehdessä voit valita, lasketaanko yksikkökohtaiseen summaan perustuva vero ennen muita verokoodeja ja lisätäänkö se nettosummaan ennen muita verokoodeja, joille käytetty laskentatapa on Alkuperä = Prosenttia nettosummasta.

### <a name="examples"></a>Esimerkkejä

Oletetaan, että tapahtumalle lasketaan 2 verokoodia:

-   MAKSU: Alkuperä = Summa per yksikkö ja arvonlisävero, arvoksi määritetään 5,00 per yksikkö = kpl
-   ALV: Alkuperä = kuten alla olevissa esimerkeissä, arvoksi määritetään 25 %

Nimikettä myydään 1 kappale yksikköhintaan 10,00
#### <a name="example-1"></a>Esimerkki 1

ALV: Alkuperä = Prosenttia bruttosummasta -laskutapa Laske ennen arvonlisäveroa -vaihtoehdolla ei ole vaikutusta, koska ALV lasketaan prosenttina bruttosummasta. MAKSU: 1 x 5,00 = 5,00 Bruttosumma: 10,00 + 5,00 = 15,00 ALV: 15,00 x 25 % = 3,75 Arvonlisävero yhteensä: 5,00 + 3,75 = 8,75 Kokonaissumma: 10,00 + 8,75 = 18,75

#### <a name="example-2"></a>Esimerkki 2

ALV: Alkuperä = Prosenttia nettosummasta Laske ennen arvonlisäveroa -vaihtoehtoa ei valita MAKSU-laskennalle. Nettosumma: 10,00 MAKSU: 1 x 5,00 = 5,00 ALV: 10,00 x 25 % = 2,50 Arvonlisävero yhteensä: 5,00 + 2,50 = 7,50 Kokonaissumma: 10,00 + 7,50 = 17,50

#### <a name="example-3"></a>Esimerkki 3

ALV: Alkuperä = Prosenttia nettosummasta Laske ennen arvonlisäveroa -vaihtoehto valitaan MAKSU-laskennalle. Nettosumma: 10,00 MAKSU: 1 x 5,00 = 5,00 ALV: (10,00 + 5,00) x 25 % = 3,75 Arvonlisävero yhteensä: 5,00 + 3,75 = 8,75 Kokonaissumma: 10,00 + 8,75 = 18,75

#### <a name="example-4"></a>Esimerkki 4

Esimerkkien 3 ja 1 tulos on sama, koska erikoismaksuja on vain yksi. Oletetaan, että MAKSUJA on kaksi ja vain toinen niistä sisältyy arvonlisäveron laskennan nettosummaan: MAKSU 1: 5,00 käyttämällä Summa peri yksikkö -tapaa ja Laske ennen arvonlisävero -vaihtoehto on valittuna MAKSU 2: 2,50 käyttämällä Summa per yksikkö -tapaa ja Laske ennen arvonlisävero -vaihtoehtoa ei ole valittu Arvonlisävero: 25 % käyttämällä Prosenttia nettosummasta -tapaa Nettosumma: 10,00 MAKSU 1: 1 x 5,00 = 5,00 MAKSU 2: 1 x 2,50 = 2,50 Nettosumma, josta arvonlisäveroa maksetaan: 10,00 + 5,00 = 15,00 ALV: 15,00 x 25 % = 3.75 Arvonlisäverot yhteensä erikoismaksut mukaan lukien: 5,00 + 2,50 + 3,75 = 11,25 Kokonaissumma: 10,00 + 11,25 = 21,25 25 %:n ALV lasketaan nettosumman summalle (10,00) + MAKSU 1 (5,00) = 15,00. MAKSU 2 lisätään verosummaan, kun arvonlisävero on laskettu.

## <a name="calculated-percentage-of-net-amount"></a> Laskettu nettosummaprosentti
Laskettu nettosummaprosentti käsittelee verojen laskennan eri tavalla asiakirjan tai kirjauskansion Summat sisältävät arvonlisäveron -parametrin asetuksen mukaisesti.
### <a name="example-1"></a>Esimerkki 1

Asiakirjan/kirjauskansion asetukseksi on määritetty Summat sisältävät arvonlisäveron = Kyllä Tapahtuman rivisumma: 10,00 Veroprosentti: 25 % Arvonlisävero: Tapahtuman rivisumma x veroprosentti (10,00 x 25 %) = 2,50 Veron perustesumma (alkuperäinen määrä): Tapahtumarivin summa - Arvonlisävero (10,00 - 2,50) = 7,50

### <a name="example-2"></a>Esimerkki 2

Asiakirjan/kirjauskansion asetukseksi on määritetty Summat sisältävät arvonlisäveron = Ei Tapahtuman rivisumma: 10,00 Veroprosentti: 25 % Arvonlisävero: (Tapahtuman rivisumma x veroprosentti) / (100 - veroprosentti) (10,00 x 25 %) / (100 % - 25 %) = 3,33 Veron perustesumma (alkuperäinen määrä): Tapahtumarivin summa = 10,00



<a name="see-also"></a>Lisätietoja
--------

[Arvonlisäveroprosenttien määrittäminen Alv-rajan peruste- ja Laskentatapa-kenttien perusteella](marginal-base-field.md)

[Alv-koodien koko summa- ja väli-laskentavaihtoehdot](whole-amount-interval-options-sales-tax-codes.md)




