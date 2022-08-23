---
title: DAYOFYEAR ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) DAYOFYEAR-funktiota käytetään.
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: e49a80b2ef3c7defcfc23e868374cec5832dc913
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292553"
---
# <a name="dayofyear-er-function"></a>DAYOFYEAR ER-funktio

[!include [banner](../includes/banner.md)]

`DAYOFYEAR`-toiminto palauttaa tammikuun 1. päivän ja määritetyn päivämäärän välisten päivien määrää kuvaavan arvon *kokonaislukuna*.

## <a name="syntax"></a>Syntaksi

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a>Argumentit

`date`: *Päivämäärä*

Päivämääräarvo, joka ilmaisee päivien määrän laskennassa käytettävää päivämäärä.

## <a name="return-values"></a>Palautusarvot

*Kokonaisluku*

Tuloksena oleva numeroarvo.

## <a name="example-1"></a>Esimerkki 1

`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` palauttaa **61**.

## <a name="example-2"></a>Esimerkki 2

`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` palauttaa **1**.

## <a name="additional-resources"></a>Lisäresurssit

[Päivämäärä- ja aikatoiminnot](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
