---
title: PADLEFT ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) PADLEFT-funktiota käytetään.
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: dac1f9142a381238bf116c4bce65958da8afc4db
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278885"
---
# <a name="padleft-er-function"></a>PADLEFT ER-funktio

[!include [banner](../includes/banner.md)]

`PADLEFT`-funktio palauttaa määritetyn pituisen *merkkijonon* arvon, jossa määritetyn merkkijonon alkua on täydennetty määritetyillä merkeillä.

## <a name="syntax"></a>Syntaksi

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a>Argumentit

`text`: *Merkkijono*

*Merkkijono*-arvo, joka esittelee alkuperäisen tekstin.

`length`: *Kokonaisluku*

*Kokonaislukuarvo*, joka vastaa täydennetyn merkkijonon lopullista merkkien määrää.

`padding chars`: *Merkkijono*

Täydennyskäyttöön käytettävät merkit.

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="example"></a>Esimerkki

`PADLEFT ("1234", 10, "`&nbsp;`")` palauttaa tekstimerkkijonon **&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234**

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
