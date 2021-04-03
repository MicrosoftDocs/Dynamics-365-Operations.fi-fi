---
title: SESSIONTODAY ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) SESSIONTODAY-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
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
ms.openlocfilehash: e6ad28e642fcfae3cfa2692a4e41b99fae7fc9df
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561346"
---
# <a name="sessiontoday-er-function"></a>SESSIONTODAY ER -funktio

[!include [banner](../includes/banner.md)]

`SESSIONTODAY`-funktio palauttaa *Date*-arvon, joka edustaa nykyistä sovellusistunnon päivämäärää.

## <a name="syntax"></a>Syntaksi

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a>Palautusarvot

*Päivämäärä*

Tulokseksi saatava päivämääräarvo.

## <a name="example"></a>Esimerkki

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` palauttaa nykyisen sovellusistunnon päivämäärän, 24. joulukuuta 2015, merkkijonona **"24-12-2015"**, joka perustuu valittuun Saksan kulttuuriin ja määritettyyn muotoon.

## <a name="additional-resources"></a>Lisäresurssit

[Päivämäärä- ja aikatoiminnot](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]