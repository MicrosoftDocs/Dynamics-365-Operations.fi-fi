---
title: ER-funktio NEWGUID
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) NEWGUID-funktiota käytetään.
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
ms.openlocfilehash: 321e2eda4accf9c8fe33b5a4c092c7be55276f26
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861813"
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
