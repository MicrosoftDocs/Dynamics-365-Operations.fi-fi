---
title: ADDDAYS ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) ADDDAYS-funktiota käytetään.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: 7cf2031c042ae93512cc85afe6a1b51558f6c8f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858738"
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