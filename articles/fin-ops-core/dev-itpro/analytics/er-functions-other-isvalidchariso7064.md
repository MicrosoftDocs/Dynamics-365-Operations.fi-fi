---
title: ISVALIDCHARACTERISO7064 ER -funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) ISVALIDCHARACTERISO7064-funktiota käytetään.
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
ms.openlocfilehash: 26ee54d1c3cd5673ec573e2df688780d3902b69d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275372"
---
# <a name="isvalidcharacteriso7064-er-function"></a>ISVALIDCHARACTERISO7064 ER -funktio

[!include [banner](../includes/banner.md)]

`ISVALIDCHARACTERISO7064`-funktio palauttaa *totuusarvon* **TOSI**, jos määritetty merkkijono vastaa kelvollista kansainvälistä tilinumeroa (IBAN). Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**.

## <a name="syntax"></a>Syntaksi

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a>Argumentit

`text`: *Merkkijono*

Tekstiarvo, joka edustaa IBAN-arvoa.

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="example"></a>Esimerkki

`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` palauttaa arvon **TOSI**. 

`ISVALIDCHARACTERISO7064 ("AT61")` palauttaa arvon **EPÄTOSI**.

## <a name="additional-resources"></a>Lisäresurssit

[Muut (liiketoiminnan toimialuekohtaiset) toiminnot](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
