---
title: AND ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) AND-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 1836d25ad07ad1ce735fda5e008a3315626b62bb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041811"
---
# <a name="AND">AND ER -funktio</a>

[!include [banner](../includes/banner.md)]

`AND`-funktio palauttaa *totuusarvon* **TOSI**, jos kaikki määritetyt ehdot toteutuvat. Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**.

## <a name="syntax"></a>Syntaksi

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Argumentit

`condition 1`: *Totuusarvo*

Kelvollinen ehdollinen lauseke, joka on testattava. Tämä argumentti on pakollinen.

`condition N`: *Totuusarvo*

Kelvollinen ehdollinen lauseke, joka on testattava. Nämä lisäargumentit ovat valinnaisia.

## <a name="return-values"></a>Palautusarvot

*Boolen arvo*

Tuloksena oleva *Totuusarvo*-arvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Loogisten funktioiden argumenteissa voit käyttää tietolähdeviittauksia, numeerisia ja tekstiarvoja, totuusarvoja, vertailuoperaattoreita ja muita sähköisen raportoinnin (ER) funktioita. Kaikki argumentit on kuitenkin arvioitava *totuusarvoiksi* **TOSI** tai **EPÄTOSI**.

## <a name="example"></a>Esimerkki

`AND (1=1, "a"="a")` palauttaa arvon **TOSI**.

`AND (1=2, "a"="a")` palauttaa arvon **EPÄTOSI**.

## <a name="additional-resources"></a>Lisäresurssit

[Loogiset toiminnot](er-functions-category-logical.md)
