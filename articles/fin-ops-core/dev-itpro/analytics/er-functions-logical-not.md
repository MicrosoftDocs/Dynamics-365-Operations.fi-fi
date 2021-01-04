---
title: NOT ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NOT-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 2308ab4d222863312441b3f17559ac4d3afbfb29
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686951"
---
# <a name="not-er-function"></a>NOT ER -funktio

[!include [banner](../includes/banner.md)]

`NOT`-funktio palauttaa määritetyn ehdon käänteisen loogisen arvon *totuusarvoksi*.

## <a name="syntax"></a>Syntaksi

```vb
NOT (condition)
```

## <a name="arguments"></a>Argumentit

`condition`: *Totuusarvo*

Kelvollinen ehdollinen lauseke, joka on käännettävä.

## <a name="return-values"></a>Palautusarvot

*Boolen arvo*

Tuloksena oleva *Totuusarvo*-arvo.

## <a name="example"></a>Esimerkki

`NOT (TRUE)` palauttaa arvon **EPÄTOSI**.

## <a name="additional-resources"></a>Lisäresurssit

[Loogiset toiminnot](er-functions-category-logical.md)
