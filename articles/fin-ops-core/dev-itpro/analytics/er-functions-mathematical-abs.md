---
title: ABS ER -funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) ABS-funktiota käytetään.
author: NickSelin
ms.date: 12/17/2019
ms.prod: ''
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
ms.openlocfilehash: 90fbff223be5c195feb66b9ea72ee0688e60697b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886875"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]