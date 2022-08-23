---
title: LOWER ER-toiminto
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) LOWER-funktiota käytetään.
author: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 7a633c8cf68b611fcaa3f216823ef9b19cac16f5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288015"
---
# <a name="lower-er-function"></a>LOWER ER-toiminto

[!include [banner](../includes/banner.md)]

`LOWER`-funktio palauttaa määritetyn tekstimerkkijonon *Merkkijono*-arvona sen jälkeen, kun se on muunnettu pieniksi kirjaimiksi.

## <a name="syntax"></a>Syntaksi

```vb
LOWER (text)
```

## <a name="arguments"></a>Argumentit

`text`: *Merkkijono*

*Merkkijono*-arvo, joka määrittää tekstin.

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="example"></a>Esimerkki

`LOWER ("Sample")` palauttaa arvon **Malli**.

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
