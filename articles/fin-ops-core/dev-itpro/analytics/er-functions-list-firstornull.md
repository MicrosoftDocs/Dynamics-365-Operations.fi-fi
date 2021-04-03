---
title: FIRSTORNULL ER-funktio
description: Tämä ohjeaihe kertoo, miten sähköisen raportoinnin (ER) FIRSTORNULL-funktiota käytetään
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 53284333507ef1264d3eb66b0c7141eb69f32392
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564622"
---
# <a name="firstornull-er-function"></a>FIRSTORNULL ER-funktio

[!include [banner](../includes/banner.md)]

`FIRSTORNULL` funktio palauttaa ensimmäisen tietueen, joka on määritetty *Säilön (tietueen)* arvona, jos tietue ei ole tyhjä. Jos tietue on tyhjä, funktio palauttaa Null *Säilö (tietue)*-arvon.

## <a name="syntax"></a>Syntaksi

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a>Argumentit

`list`: *Tietueluettelo*

*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.

## <a name="return-values"></a>Palautusarvot

*Kontti (tietue)*

Tuloksena oleva tietueen arvo.

## <a name="example"></a>Esimerkki

Lauseke `FIRSTORNULL(SPLIT("",1)).Value` palauttaa tyhjän merkkijonon (**""**).

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]