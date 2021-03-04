---
title: NUMBERVALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NUMBERVALUE-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: d3eec6dc5a472f366c9029456fe05cf1e431e1c5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685976"
---
# <a name="numbervalue-er-function"></a>NUMBERVALUE ER -funktio

[!include [banner](../includes/banner.md)]

`NUMBERVALUE`-funktio palauttaa *todellisen* arvon, joka muunnetaan määritetystä *merkkiarvosta*. Muuntamisen aikana otetaan huomioon määritetyt desimaali- ja numeroryhmittelyerottimet.

## <a name="syntax"></a>Syntaksi

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a>Argumentit

`text`: *Merkkijono*

Tekstiarvo, jota ei pidä muuntaa *todelliseksi* numeroksi.

`decimal separator`: Merkkijono

Desimaalierotin. Sitä käytetään erottamaan desimaaliluvun kokonaisluku ja murto-osat.

`digit grouping separator`: *Merkkijono*

Numeroiden ryhmittelyerotin. Sitä käytetään tuhaterottimena.

## <a name="return-values"></a>Palautusarvot

*Reaaliluku*

Tuloksena oleva numeroarvo.

## <a name="example"></a>Esimerkki

`NUMBERVALUE( "1 234,56", ",", " ")` palauttaa **1234.56**.

## <a name="additional-resources"></a>Lisäresurssit

[Tyypin muuntamisen toiminnot](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]