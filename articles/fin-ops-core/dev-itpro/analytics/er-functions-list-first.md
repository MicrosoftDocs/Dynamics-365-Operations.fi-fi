---
title: FIRST ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) FIRST-funktiota käytetään.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: a1f841fe11f025be95ffee2750da74ad7be51624
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906573"
---
# <a name="first-er-function"></a>FIRST ER-funktio

[!include [banner](../includes/banner.md)]

`FIRST`-funktio palauttaa ensimmäisen tietueen, joka on määritetty *Säilön (tietueen)* arvona, jos luettelo ei ole tyhjä. Jos luettelo on tyhjä, funktio heittää poikkeuksen.

## <a name="syntax"></a>Syntaksi

```vb
FIRST (list)
```

## <a name="arguments"></a>Argumentit

`list`: *Tietueluettelo*

*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.

## <a name="return-values"></a>Palautusarvot

*Kontti (tietue)*

Tuloksena oleva tietueen arvo.

## <a name="example-1"></a>Esimerkki 1

Lauseke `FIRST(SPLIT("ABC",1)).Value` palauttaa tekstiarvon **"A"**.

## <a name="example-2"></a>Esimerkki 2

Lauseke `FIRST(SPLIT("",1)).Value` heittää poikkeuksen suorituksen aikana.

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]