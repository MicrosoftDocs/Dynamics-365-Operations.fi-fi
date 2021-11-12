---
title: ER-funktio NEWGUID
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NEWGUID-funktiota käytetään.
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: 5856a4d765f5136ecb11a34e0255c1ba88818f2c
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647932"
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
