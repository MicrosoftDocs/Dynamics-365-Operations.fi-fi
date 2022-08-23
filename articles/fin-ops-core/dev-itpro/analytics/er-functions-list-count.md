---
title: COUNT ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) COUNT-funktiota käytetään.
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
ms.openlocfilehash: 64c8be659b564d612f3127d46e54535c73ae21ce
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287245"
---
# <a name="count-er-function"></a>COUNT ER-funktio

[!include [banner](../includes/banner.md)]

`COUNT`-funktio palauttaa *kokonaisluku*-arvon, joka vastaa määritetyn luettelon tietueiden määrää, jos luettelo ei ole tyhjä. Jos luettelo on tyhjä, funktio palauttaa arvon **0** (nolla).

## <a name="syntax"></a>Syntaksi

```vb
COUNT (list)
```

## <a name="arguments"></a>Argumentit

`list`: *Tietueluettelo*

*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.

## <a name="return-values"></a>Palautusarvot

*Kokonaisluku*

Tuloksena oleva numeroarvo.

## <a name="example"></a>Esimerkki

`COUNT (SPLIT("abcd" , 3))` palauttaa arvon **2**, koska tässä esimerkissä käytetty `SPLIT`-funktio luo luettelon, joka koostuu kahdesta tietueesta.

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
