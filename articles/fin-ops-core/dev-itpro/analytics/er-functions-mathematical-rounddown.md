---
title: ROUNDDOWN ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) ROUNDDOWN-funktiota käytetään.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: e0fa2c92fe63c3c89548b5cc23dd714d3d7589af
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286086"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
