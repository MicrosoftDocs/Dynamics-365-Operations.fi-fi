---
title: OR ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) OR-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: faf07c5d8b30cd3babe8a6a55ae7effe5ce457a0
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744620"
---
# <a name="or-er-function"></a>OR ER -funktio

[!include [banner](../includes/banner.md)]

`OR`-funktio palauttaa *totuusarvon* **EPÄTOSI**, jos mikään määritetty ehto ei toteudu. Jos joku määritetty ehto toteutuu, tämä funktio palauttaa *totuusarvon* **TOSI**.

## <a name="syntax"></a>Syntaksi

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Argumentit

`condition 1`: *Totuusarvo*

Kelvollinen ehdollinen lauseke, joka on testattava. Tämä argumentti on pakollinen.

`condition N`: *Totuusarvo*

Kelvollinen ehdollinen lauseke, joka on testattava. Nämä lisäargumentit ovat valinnaisia.

## <a name="return-values"></a>Palautusarvot

*Boolen arvo*

Tuloksena oleva *Totuusarvo*-arvo.

## <a name="example"></a>Esimerkki

`OR (1=2, "a"="a")` palauttaa arvon **TOSI**.

## <a name="additional-resources"></a>Lisäresurssit

[Loogiset toiminnot](er-functions-category-logical.md)
