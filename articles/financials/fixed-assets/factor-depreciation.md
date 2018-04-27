---
title: Kerroinpoisto
description: "Tämä artikkeli sisältää kerroinpoistomenetelmän yleiskatsauksen."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 44fa540c31e5302ccf0a65b44b3c45a4c1e1fd1f
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="factor-depreciation"></a>Kerroinpoisto

[!INCLUDE [banner](../includes/banner.md)]

Tämä artikkeli sisältää kerroinpoistomenetelmän yleiskatsauksen.

Kertoimet ovat käyttöomaisuuserien poistamiseen käytettäviä prosenttiosuuksia. Kun määrität käyttöomaisuuden poistoprofiilin ja valitset **Poistoprofiilit**-sivulla **Tapa**-kentästä **Kerroin**-vaihtoehdon, voit määrittää nousevan poiston, laskevan poiston tai tasapoiston:

-   Nousevassa poistossa poiston määrä kasvaa jokaisella poistokaudella.
-   Laskevassa poistossa poiston määrä pienenee ajan kuluessa.
-   Tasapoistossa poisto on sama jokaisella kaudella.

Seuraavassa on sääntöjä ja esimerkkejä, jotka osoittavat, miten eri poistotyyppien kertoimet voidaan määrittää. 

> [!NOTE] 
> Kun valitset **Tapa**-kentästä **Kerroin**-vaihtoehdon, näkyviin tulevat **Kerroin**- ja **Väli**-kenttä.

## <a name="progressive-depreciation"></a>Nouseva poisto
**Kerroin**-kentän arvo on suurempi kuin **50**.

### <a name="example"></a>Esimerkki

Hankintahinta on 100 000, kerroin on 70, käyttöikä on 10 vuotta ja poisto alkaa 1.1. Poistosummat ja nettokirjanpitoarvon summat näytetään vain ensimmäisen kuuden vuoden käyttöiän osalta.

| Vuosi(a) | Kausi      | Poiston määrä | Nettokirjanpitoarvo |
|------|-------------|---------------------|-----------------------|
| 1    | 31. joulukuuta | 307,69              | 99 692,31             |
| 2    | 31. joulukuuta | 1 447,21            | 98 245,10             |
| 3    | 31. joulukuuta | 3 104,50            | 95 140,60             |
| 4    | 31. joulukuuta | 5 150,21            | 89 990,39             |
| 5    | 31. joulukuuta | 7 522,95            | 82 467,44             |
| 6    | 31. joulukuuta | 10 184,06           | 72 283,38             |

## <a name="digressive-depreciation"></a>Laskeva poisto
**Kerroin**-kentän arvo on pienempi kuin **50**.

### <a name="example"></a>Esimerkki

Hankintahinta on 100 000, kerroin on 20, käyttöikä on 10 vuotta ja poisto alkaa 1.1. Poistosummat ja nettokirjanpitoarvon summat näytetään vain ensimmäisen kuuden vuoden käyttöiän osalta.

| Vuosi(a) | Kausi      | Poiston määrä | Nettokirjanpitoarvo |
|------|-------------|---------------------|-----------------------|
| 1    | 31. joulukuuta | 56 080,43           | 43 919,57             |
| 2    | 31. joulukuuta | 10 665,70           | 33 253,87             |
| 3    | 31. joulukuuta | 7 156,22            | 26 097,65             |
| 4    | 31. joulukuuta | 5 538,06            | 20 559,59             |
| 5    | 31. joulukuuta | 4 579,89            | 15 979,70             |
| 6    | 31. joulukuuta | 3 937,36            | 12 042,34             |

## <a name="straight-line-depreciation"></a>Tasapoisto
**Kerroin**-kentän arvo on yhtä suuri kuin **50**. Poistosumma on tällöin sama jokaisella kaudella. Muiden kenttien valintojen merkitykset tulisi ottaa huomioon. Nämä on kuvattu ohjeaiheessa [Käyttöikään perustuva tasapoisto](straight-line-service-life-depreciation.md).




