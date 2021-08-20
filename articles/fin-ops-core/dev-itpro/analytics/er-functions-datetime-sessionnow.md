---
title: SESSIONNOW ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) SESSIONNOW-funktiota käytetään.
author: NickSelin
ms.date: 12/04/2019
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc532a96c7e52e6a12877ae88d1a6183829a1282d43c7df52dd90e536a7e3d75
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734813"
---
# <a name="sessionnow-er-function"></a>SESSIONNOW ER -funktio

[!include [banner](../includes/banner.md)]

`SESSIONNOW`-funktio palauttaa *DateTime*-arvon, joka edustaa nykyistä sovellusistunnon päivämäärää ja aikaa.

## <a name="syntax"></a>Syntaksi

```vb
SESSIONNOW ()
```

## <a name="return-values"></a>Palautusarvot

*DateTime*

Tulokseksi saatava päivämäärä-/aika-arvo.

## <a name="example"></a>Esimerkki

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` palauttaa nykyisen sovellusistunnon päivämäärä-/aika-arvon, 24. joulukuuta 2015, merkkijonona **"24.12.2015"**, joka perustuu valittuun Saksan kulttuuriin ja määritettyyn muotoon.

## <a name="additional-resources"></a>Lisäresurssit

[Päivämäärä- ja aikatoiminnot](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]