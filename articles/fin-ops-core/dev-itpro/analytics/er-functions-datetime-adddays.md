---
title: ADDDAYS ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ADDDAYS-funktiota käytetään.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: 0c420daa04b8e22504d25d317c75826f1d1914b7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747056"
---
# <a name="adddays-er-function"></a>ADDDAYS ER-funktio

[!include [banner](../includes/banner.md)]

`ADDDAYS`-funktio laskee *DateTime*-arvon, joka on määritetty päivien määrä ennen määritettyä alkamispäivää tai sen jälkeen.

## <a name="syntax"></a>Syntaksi

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a>Argumentit

`datetime`: *DateTime*

Päivämäärä-/aika-arvo, joka vastaa alkamispäivämäärää.

`days`: *Kokonaisluku*

Päivien lukumäärä ennen tai jälkeen `datetime`.

## <a name="return-values"></a>Palautusarvot

*DateTime*

Tulokseksi saatava päivämäärä-/aika-arvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Positiivinen arvo tuotoille `days` viittaa tulevaan päivään. Negatiivinen arvo tuottaa kuluneen päivämäärän.

## <a name="example-1"></a>Esimerkki 1

`ADDDAYS (NOW(), 7)` palauttaa päivämäärän ja ajan seitsemän päivän kuluttua.

## <a name="example-2"></a>Esimerkki 2

`ADDDAYS (NOW(), -3)` palauttaa päivämäärän ja ajan kolme päivää sitten.

## <a name="additional-resources"></a>Lisäresurssit

[Päivämäärä- ja aikatoiminnot](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]