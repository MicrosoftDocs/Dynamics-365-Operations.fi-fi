---
title: JSONVALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) JSONVALUE-funktiota käytetään.
author: NickSelin
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
ms.openlocfilehash: e8336e43a236e3f3b875fb3cb81bc139507673c2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746360"
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