---
title: NUMBERVALUE ER -funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) NUMBERVALUE-funktiota käytetään.
author: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 2e39cf59cabd44583e78ff2c35a7ae4d6edbd7ee
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282588"
---
# <a name="numbervalue-er-function"></a>NUMBERVALUE ER -funktio

[!include [banner](../includes/banner.md)]

`NUMBERVALUE`-funktio palauttaa *todellisen* arvon, joka muunnetaan määritetystä *merkkiarvosta*. Muuntamisen aikana otetaan huomioon määritetyt desimaali- ja numeroryhmittelyerottimet.

## <a name="syntax"></a>Syntaksi

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a>Argumentit

`text`: *Merkkijono*

Tekstiarvo, jota ei pidä muuntaa *todelliseksi* numeroksi.

`decimal separator`: Merkkijono

Desimaalierotin. Sitä käytetään erottamaan desimaaliluvun kokonaisluku ja murto-osat.

`digit grouping separator`: *Merkkijono*

Numeroiden ryhmittelyerotin. Sitä käytetään tuhaterottimena.

## <a name="return-values"></a>Palautusarvot

*Reaaliluku*

Tuloksena oleva numeroarvo.

## <a name="example"></a>Esimerkki

`NUMBERVALUE( "1 234,56", ",", " ")` palauttaa **1234.56**.

## <a name="additional-resources"></a>Lisäresurssit

[Tyypin muuntamisen toiminnot](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
