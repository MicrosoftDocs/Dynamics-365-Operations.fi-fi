---
title: ADDDAYS ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ADDDAYS-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 998cf2c0dac67040814d4a32e433b465ec51f88c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743372"
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
