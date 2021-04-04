---
title: JSONVALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) JSONVALUE-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 203fe1b1616f724ddf3015258306e0d9e8d4f599
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570013"
---
# <a name="jsonvalue-er-function"></a>JSONVALUE ER -funktio

[!include [banner](../includes/banner.md)]

`JSONVALUE`-funktio jäsentää tiedot JavaScript Object Notation (JSON) -muodossa, jota käytettään tietyssä polussa, ja se purkaa skalaariarvon, jolla on tietty tunnus. Sen jälkeen se palauttaa puretut skalaariarvot *merkkijono*-arvona.

## <a name="syntax"></a>Syntaksi

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>Argumentit

`input`: *Merkkijono*

JSON-tietoja sisältävän *Merkkijono*-tyypin tietolähteen kelvollinen polku.

`path`: *Merkkijono*

JSON-tietojen skaalariarvon tunniste.

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="example"></a>Esimerkki

**$JsonField**-tietolähde sisältää seuraavat tiedot JSON-muodossa: **{BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**. Tässä tapauksessa `JSONVALUE (JsonField, "BuildNumber")`-lauseke palauttaa *merkkijonon* tietotyypin seuraavan arvon: **"7.3.1234.1"**.

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]