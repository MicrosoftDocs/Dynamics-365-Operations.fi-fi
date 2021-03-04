---
title: FIRSTORNULL ER-funktio
description: Tämä ohjeaihe kertoo, miten sähköisen raportoinnin (ER) FIRSTORNULL-funktiota käytetään
author: NickSelin
manager: kfend
ms.date: 11/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 3547eeea3c6fef5cca0699002cc0c35cffd940b3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688040"
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