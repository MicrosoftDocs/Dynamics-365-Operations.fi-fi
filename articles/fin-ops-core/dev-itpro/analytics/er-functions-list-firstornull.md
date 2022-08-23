---
title: FIRSTORNULL ER-funktio
description: Tämä artikkeli kertoo, miten sähköisen raportoinnin (ER) FIRSTORNULL-funktiota käytetään
author: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 7ee1a5c1b6ac13581608f9adbda42fae0706d225
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273185"
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
