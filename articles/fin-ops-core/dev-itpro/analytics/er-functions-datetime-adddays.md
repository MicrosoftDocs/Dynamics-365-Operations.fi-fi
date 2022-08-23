---
title: ADDDAYS ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) ADDDAYS-funktiota käytetään.
author: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 69273794def0dc52dc8e31615c319ccf5067fa77
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274136"
---
# <a name="adddays-er-function"></a>ADDDAYS ER-funktio

[!include [banner](../includes/banner.md)]

`ADDDAYS`-funktio laskee *DateTime*-arvon, joka on määritetty päivien määrä ennen määritettyä alkamispäivää tai sen jälkeen.

## <a name="syntax"></a>Syntaksi

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a>Argumentit

`datetime`: *DateTime*

Päivämäärä-/aika-arvo, joka vastaa alkamispäivämäärää.

`days`: *Kokonaisluku*

Päivien lukumäärä ennen tai jälkeen `datetime`.

## <a name="return-values"></a>Palautusarvot

*DateTime*

Tulokseksi saatava päivämäärä-/aika-arvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Positiivinen arvo tuotoille `days` viittaa tulevaan päivään. Negatiivinen arvo tuottaa kuluneen päivämäärän.

## <a name="example-1"></a>Esimerkki 1

`ADDDAYS (NOW(), 7)` palauttaa päivämäärän ja ajan seitsemän päivän kuluttua.

## <a name="example-2"></a>Esimerkki 2

`ADDDAYS (NOW(), -3)` palauttaa päivämäärän ja ajan kolme päivää sitten.

## <a name="additional-resources"></a>Lisäresurssit

[Päivämäärä- ja aikatoiminnot](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
