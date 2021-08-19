---
title: Alv-koodien koko summa- ja väli-laskentavaihtoehdot
description: Tässä artikkelissa kuvataan arvonlisäverokoodien Laskentatapa-kentän asetuksia ja sitä, miten arvonlisävero lasketaan välejä ja koko summia varten.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb3d622f8a81c0eabc84fb165203aa193f5e7dd6ad148ff50a9f55c87453be9c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731473"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a>Alv-koodien koko summa- ja väli-laskentavaihtoehdot

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan arvonlisäverokoodien Laskentatapa-kentän asetuksia ja sitä, miten arvonlisävero lasketaan välejä ja koko summia varten.

Voit määrittää, että alv-koodi lasketaan koko summan tai välisumman perusteella. Valitse Arvonlisäverokoodit-sivulla alv-koodin laskentatapa Laskenta-pikavälilehden Laskentatapa-kentässä.
- Koko summa – veroprosentti kohdistetaan koko verotettavaan summaan.
- Väli – Verotettava summa on jaettu osiin, joista jokainen kuuluu tietyn alv-prosentin alueeseen. Määritetylle välille osuvan summan vero lasketaan kyseistä väliä koskevan prosentin mukaan. Arvonlisävero on kullekin summavälille laskettavien verosummien yhteissumma.
  > [!NOTE]                                                                                                                              
  > Väli-vaihtoehto on käytettävissä vain, jos valitset Kirjanpitoparametrit-sivulla Arvonlisävero-alueen Laskentatapa-kentästä Rivi-vaihtoehdon. 

Välit määritetään Arvonlisäverokoodin arvot -sivulla syöttämällä kunkin veroprosentin vähimmäis- ja enimmäisrajasummat. Jotta verot voidaan laskea kaikille verotettaville summille valitusta laskentatavasta riippumatta, välien on noudatettava seuraavia sääntöjä:
-   Ensimmäisen välin vähimmäisraja on oltava 0.
-   Viimeisen välin enimmäisrajan on oltava nolla, joka tarkoittaa ääretöntä.
-   Välin enimmäisrajan on oltava seuraavan välin vähimmäisraja.

Jos summa on edellisen välin enimmäisraja ja seuraavan välin vähimmäisraja, summaan käytetään ensimmäisen välin arvonlisäveroprosenttia. Jos summa jää enimmäis- ja vähimmäisrajojen määrittämien välien ulkopuolelle, alv-prosentti on 0.

## <a name="example-whole-amount-method-of-calculation"></a>Esimerkki: Koko summa -laskutapa
Arvonlisäveron koodi -sivulla arvonlisäveroprosentit määritetään seuraavin välein:

| Vähimmäisraja     | Enimmäisraja     | Veroprosentti     |
|-------------------|-------------------|--------------|
| 0,00              | 50,00             | 30 %          |
| 50,00             | 100,00            | 20 %          |
| 100,00            | 0,00              | 10 %          |

Arvonlisävero lasketaan koko verotettavasta summasta

| Verotettava summa (hinta) | Laskelma    | Arvonlisävero |
|------------------------|----------------|-----------|
| 35,00                  | 35,00 \* 0,30  | 10,50     |
| 50,00                  | 50,00 \* 0,30  | 15,00     |
| 85,00                  | 85,00 \* 0,20  | 17,00     |
| 305,00                 | 305,00 \* 0,10 | 30,50     |

## <a name="example-interval-method-of-calculation"></a> Esimerkki: Väli-laskentatapa
Arvonlisäveroprosentit määritetään Arvot-sivulla seuraavin välein:

| Vähimmäisraja     | Enimmäisraja     | Veroprosentti     |
|-------------------|-------------------|--------------|
| 0,00              | 50,00             | 30 %          |
| 50,00             | 100,00            | 20 %          |
| 100,00            | 0,00              | 10 %          |

Arvonlisävero on kullekin summavälille laskettavien verosummien yhteissumma.

| Verotettava summa (hinta) | Laskelma                                                               | Arvonlisävero |
|------------------------|---------------------------------------------------------------------------|-----------|
| 35,00                  | 35,00 \* 0,30                                                             | 10,50     |
| 50,00                  | 50,00 \* 0,30                                                             | 15,00     |
| 85,00                  | (50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)                          | 22,00     |
| 305,00                 | (50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50) | 45.50     |



Lisätietoja on kohdassa [Alv-rajan perusteeseen ja Laskentatapoihin perustuva arvonlisäveroprosentti](marginal-base-field.md).







[!INCLUDE[footer-include](../../includes/footer-banner.md)]