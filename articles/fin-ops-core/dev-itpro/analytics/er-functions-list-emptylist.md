---
title: EMPTYLIST ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) EMPTYLIST-funktiota käytetään.
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 5fd14456a615d5dc6fb565f4bed523db5432c871
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268113"
---
# <a name="emptylist-er-function"></a>EMPTYLIST ER-funktio

[!include [banner](../includes/banner.md)]

`EMPTYLIST` funktio palauttaa tyhjän *Tietueluettelon* arvon käyttämällä määritettyä luetteloa luettelorakenteen lähteenä.

## <a name="syntax"></a>Syntaksi

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a>Argumentit

`list`: *Tietueluettelo*

*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.

## <a name="return-values"></a>Palautusarvot

*Tietueluettelo*

Tuloksena oleva tietueluettelo.

## <a name="example"></a>Esimerkki

`EMPTYLIST (SPLIT ("abc", 1))` palauttaa uuden tyhjän luettelon, jonka rakenne on sama kuin `SPLIT`-toiminnon palauttamalla luettelolla.

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
