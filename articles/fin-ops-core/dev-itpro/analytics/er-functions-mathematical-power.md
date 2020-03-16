---
title: POWER ER-toiminto
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) POWER-funktiota käytetään.
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
ms.openlocfilehash: c57222d7fcc133faa679bab43431272c984c9d8b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041627"
---
# <a name="POWER">POWER ER-toiminto</a>

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
