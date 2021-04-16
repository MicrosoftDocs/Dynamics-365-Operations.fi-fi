---
title: ROUNDUP ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ROUNDUP-funktiota käytetään.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 4898f596108ff3c563da55a567a10da987d62d33
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744436"
---
# <a name="roundup-er-function"></a>ROUNDUP ER-funktio

[!include [banner](../includes/banner.md)]

`ROUNDUP`-funktio palauttaa määritetyn numeron *Todellisen* arvon sen jälkeen, kun se on pyöristetty ylöspäin määritettyyn määrään desimaaleja.

## <a name="syntax"></a>Syntaksi

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Argumentit

`number`: *Todellinen*

Numeerinen arvo, joka on pyöristettävä ylöspäin.

`decimals`: *Kokonaisluku*

Numeerinen arvo, joka vastaa desimaalien määrää.

## <a name="return-values"></a>Palautusarvot

*Reaaliluku*

Tuloksena oleva numeroarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Tämä funktio toimii kuin [ROUND](er-functions-mathematical-round.md), mutta se pyöristää määritetyn numeron aina ylöspäin (pois päin nollasta).

## <a name="example-1"></a>Esimerkki 1

`ROUNDUP (1200.763, 2)` pyöristää ylöspäin kahteen desimaaliin ja palauttaa arvon **1200,77**.

## <a name="example-2"></a>Esimerkki 2

`ROUNDUP (1200.767, -3)` pyöristää ylöspäin lähimpään tuhanteen ja palauttaa arvon **1,000**.

## <a name="additional-resources"></a>Lisäresurssit

[Matemaattinen toiminto](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]