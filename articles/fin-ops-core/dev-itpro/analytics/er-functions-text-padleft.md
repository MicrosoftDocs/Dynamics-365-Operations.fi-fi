---
title: PADLEFT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) PADLEFT-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 268941d8bc0bd4dc6de6d2597c05a11c1f530f15
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680143"
---
# <a name="padleft-er-function"></a>PADLEFT ER-funktio

[!include [banner](../includes/banner.md)]

`PADLEFT`-funktio palauttaa määritetyn pituisen *merkkijonon* arvon, jossa määritetyn merkkijonon alkua on täydennetty määritetyillä merkeillä.

## <a name="syntax"></a>Syntaksi

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a>Argumentit

`text`: *Merkkijono*

*Merkkijono*-arvo, joka esittelee alkuperäisen tekstin.

`length`: *Kokonaisluku*

*Kokonaislukuarvo*, joka vastaa täydennetyn merkkijonon lopullista merkkien määrää.

`padding chars`: *Merkkijono*

Täydennyskäyttöön käytettävät merkit.

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="example"></a>Esimerkki

`PADLEFT ("1234", 10, "`&nbsp;`")` palauttaa tekstimerkkijonon **&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234**

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]