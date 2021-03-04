---
title: ROUND ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ROUND-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 10/21/2020
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
ms.openlocfilehash: 83fb5c04938e0aba1277f2d6017d4b66208a8858
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683253"
---
# <a name="round-er-function"></a>ROUND ER-funktio

[!include [banner](../includes/banner.md)]

`ROUND`-funktio palauttaa määritetyn numeron *Todellisen* arvon sen jälkeen, kun se on pyöristetty määritettyyn määrään desimaaleja.

## <a name="syntax"></a>Syntaksi

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a>Argumentit

`number`: *Todellinen*

Numeerinen arvo, joka on pyöristettävä.

`decimals`: *Kokonaisluku*

Numeerinen arvo, joka vastaa desimaalien määrää.

## <a name="return-values"></a>Palautusarvot

*Reaaliluku*

Tuloksena oleva numeroarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Jos `decimals`-argumentin arvo on yli 0 (nolla), numero pyöristetään kyseiseen määrään desimaaleja.

Jos `decimals`-argumentin arvo on **0** (nolla), numero pyöristetään lähimpään parilliseen kokonaislukuun.

Jos `decimals`-argumentin arvo on vähemmän kuin 0 (nolla), numero pyöristetään desimaalipilkusta vasemmalle.

## <a name="example-1"></a>Esimerkki 1

`ROUND (1200.767, 2)` pyöristää kahteen desimaaliin ja palauttaa arvon **1200,77**.

## <a name="example-2"></a>Esimerkki 2

`ROUND (1200.767, -3)` pyöristää lähimpään tuhanteen ja palauttaa arvon **1000**.

## <a name="example-3"></a>Esimerkki 3

`ROUND (1200.5, 0)` pyöristää lähimpään parilliseen kokonaislukuun ja palauttaa arvon **1200**, mutta `ROUND (1201.5, 0)` tekee saman ja palauttaa arvon **1202**.

## <a name="additional-resources"></a>Lisäresurssit

[Matemaattinen toiminto](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]