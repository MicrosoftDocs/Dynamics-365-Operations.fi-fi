---
title: POWER ER-toiminto
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) POWER-funktiota käytetään.
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
ms.openlocfilehash: da3ae988b57cb5588de1e2fd8ee962b77b5534ff
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864685"
---
# <a name="power-er-function"></a>POWER ER-toiminto

[!include [banner](../includes/banner.md)]

`POWER`-funktio palauttaa *todellisen* arvon, joka ilmaisee määritetyn positiivisen luvun nostamisesta määritettyyn tehoon.

## <a name="syntax"></a>Syntaksi

```vb
POWER (number, power)
```

## <a name="arguments"></a>Argumentit

`number`: *Todellinen* tai *Kokonaisluku*

Numeerinen arvo, joka on nostettava määritettyyn tehoon.

`power`: *Todellinen* tai *Kokonaisluku*

Numeerinen arvo, joka edustaa tiettyä tehoa.

## <a name="return-values"></a>Palautusarvot

*Reaaliluku*

Tuloksena oleva numeroarvo.

## <a name="example-1"></a>Esimerkki 1

`POWER (10, 2)` palauttaa **100**.

## <a name="example-2"></a>Esimerkki 2

`POWER (4, 0.5)` palauttaa **2**.

## <a name="additional-resources"></a>Lisäresurssit

[Matemaattinen toiminto](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]