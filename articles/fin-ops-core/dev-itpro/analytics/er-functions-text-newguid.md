---
title: ER-funktio NEWGUID
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) NEWGUID-funktiota käytetään.
author: kfend
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 381dbcbe816c189c1966ffe962020d5aa2b1f3eb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274769"
---
# <a name="newguid-er-function"></a>ER-funktio NEWGUID

[!include [banner](../includes/banner.md)]

`NEWGUID`-funktio luo uuden GUID-tunnuksen ja palauttaa sen *[GUID](er-formula-supported-data-types-primitive.md#guid)*-arvona.

## <a name="syntax"></a>Syntaksi

```vb
NEWGUID ()
```

## <a name="return-values"></a>Palautusarvot

*GUID*

Tulokseksi saatava GUID-arvo.

## <a name="example"></a>Esimerkki

`NEWGUID()` palauttaa aina *GUID*-arvon, kuten **3afcf7ff-af10-ec11-b6e6-000d3a13209e**.

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
