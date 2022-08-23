---
title: POWER ER-toiminto
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) POWER-funktiota käytetään.
author: kfend
ms.date: 12/17/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 9b6693d7c1afebcf9c30d1bf8d72950053c305bd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273992"
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
