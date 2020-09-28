---
title: ABS ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ABS-funktiota käytetään.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b53535d1a000b72577be5c6284cc4676c43d591b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744596"
---
# <a name="abs-er-function"></a>ABS ER -funktio

[!include [banner](../includes/banner.md)]

`ABS`-funktio palauttaa määritetyn luvun absoluuttisen arvon (jakojäännös) *todelliseksi* arvoksi. Toisin sanoen, se palauttaa luvun ilman etumerkkiä.

## <a name="syntax"></a>Syntaksi

```vb
ABS (number)
```

## <a name="arguments"></a>Argumentit

`number`: *Todellinen*

Numeerinen arvo, jonka jakojäännöksen haluat.

## <a name="return-values"></a>Palautusarvot

*Reaaliluku*

Tuloksena oleva numeroarvo.

## <a name="example"></a>Esimerkki

`ABS (-1)` palauttaa **1**.

## <a name="additional-resources"></a>Lisäresurssit

[Matemaattinen toiminto](er-functions-category-mathematical.md)
