---
title: ROUNDDOWN ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ROUNDDOWN-funktiota käytetään.
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
ms.openlocfilehash: 7ac559983609d4fdb80c9ac70d84031e4a231889
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744524"
---
# <a name="rounddown-er-function"></a>ROUNDDOWN ER-funktio

[!include [banner](../includes/banner.md)]

`ROUNDDOWN`-funktio palauttaa määritetyn numeron *Todellisen* arvon sen jälkeen, kun se on pyöristetty alaspäin määritettyyn määrään desimaaleja.

## <a name="syntax"></a>Syntaksi

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Argumentit

`number`: *Todellinen*

Numeerinen arvo, joka on pyöristettävä alaspäin.

`decimals`: *Kokonaisluku*

Numeerinen arvo, joka vastaa desimaalien määrää.

## <a name="return-values"></a>Palautusarvot

*Reaaliluku*

Tuloksena oleva numeroarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Tämä funktio toimii kuin [ROUND](er-functions-mathematical-round.md), mutta se pyöristää määritetyn numeron aina alaspäin (kohti nollaa).

## <a name="example-1"></a>Esimerkki 1

`ROUNDDOWN (1200.767, 2)` pyöristää alaspäin kahteen desimaaliin ja palauttaa arvon **1200,76**. 

## <a name="example-2"></a>Esimerkki 2

`ROUNDDOWN (1700.767, -3)` pyöristää alaspäin lähimpään tuhanteen ja palauttaa arvon **1000**.

## <a name="additional-resources"></a>Lisäresurssit

[Matemaattinen toiminto](er-functions-category-mathematical.md)
