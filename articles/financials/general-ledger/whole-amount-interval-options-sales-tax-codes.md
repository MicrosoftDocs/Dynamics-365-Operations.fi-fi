---
title: "Alv-koodien koko summa- ja väli-laskentavaihtoehdot"
description: "Tässä artikkelissa kuvataan arvonlisäverokoodien Laskentatapa-kentän asetuksia ja sitä, miten arvonlisävero lasketaan välejä ja koko summia varten."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 093047d43a39fa723eb99e3daf34cf33fa81a099
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a>Alv-koodien koko summa- ja väli-laskentavaihtoehdot

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]



Tässä artikkelissa kuvataan arvonlisäverokoodien Laskentatapa-kentän asetuksia ja sitä, miten arvonlisävero lasketaan välejä ja koko summia varten.

Voit määrittää, että alv-koodi lasketaan koko summan tai välisumman perusteella. Valitse Arvonlisäverokoodit-sivulla alv-koodin laskentatapa Laskenta-pikavälilehden Laskentatapa-kentässä.
-   Koko summa – veroprosentti kohdistetaan koko verotettavaan summaan.
-   Väli – Verotettava summa on jaettu osiin, joista jokainen kuuluu tietyn alv-prosentin alueeseen. Määritetylle välille osuvan summan vero lasketaan kyseistä väliä koskevan prosentin mukaan. Arvonlisävero on kullekin summavälille laskettavien verosummien yhteissumma.
> [!NOTE]                                                                                                                              
> Väli-vaihtoehto on käytettävissä vain, jos valitset Kirjanpitoparametrit-sivulla Arvonlisävero-alueen Laskentatapa-kentästä Rivi-vaihtoehdon. 

Välit määritetään Arvonlisäverokoodin arvot -sivulla syöttämällä kunkin veroprosentin vähimmäis- ja enimmäisrajasummat. Jotta verot voidaan laskea kaikille verotettaville summille valitusta laskentatavasta riippumatta, välien on noudatettava seuraavia sääntöjä:
-   Ensimmäisen välin vähimmäisraja on oltava 0.
-   Viimeisen välin enimmäisrajan on oltava nolla, joka tarkoittaa ääretöntä.
-   Välin enimmäisrajan on oltava seuraavan välin vähimmäisraja.

Jos summa on edellisen välin enimmäisraja ja seuraavan välin vähimmäisraja, summaan käytetään ensimmäisen välin arvonlisäveroprosenttia. Jos summa jää enimmäis- ja vähimmäisrajojen määrittämien välien ulkopuolelle, alv-prosentti on 0.

## <a name="example-whole-amount-method-of-calculation"></a>Esimerkki: Koko summa -laskutapa
Arvonlisäveron koodi -sivulla arvonlisäveroprosentit määritetään seuraavin välein:
|                   |                   |              |
|-------------------|-------------------|--------------|
| **Vähimmäisraja** | **Enimmäisraja** | **Veroprosentti** |
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

|                   |                   |              |
|-------------------|-------------------|--------------|
| **Vähimmäisraja** | **Enimmäisraja** | **Veroprosentti** |
| 0,00              | 50,00             | 30 %          |
| 50,00             | 100,00            | 20 %          |
| 100,00            | 0,00              | 10 %          |

Arvonlisävero on kullekin summavälille laskettavien verosummien yhteissumma.

| Verotettava summa (hinta) | Laskelma                                                               | Arvonlisävero |
|------------------------|---------------------------------------------------------------------------|-----------|
| 35,00                  | 35,00 \* 0,30                                                             | 10,50     |
| 50,00                  | 50,00 \* 0,30                                                             | 15,00     |
| 85,00                  | (50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)                          | 22,00     |
| 305,00                 | (50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50) | 45,50     |

 

Lisätietoja on kohdassa [Arvonlisäveroprosenttien määrittäminen Alv-rajan peruste- ja Laskentatapa-kenttien perusteella](marginal-base-field.md).





