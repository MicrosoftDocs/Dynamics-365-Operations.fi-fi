---
title: ISOCREDREF ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ISOCREDREF-funktiota käytetään.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c9a75cedcf543b318df2850df3e4a60bac2dc6b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680683"
---
# <a name="isocredref-er-function"></a>ISOCREDREF ER -funktio

[!include [banner](../includes/banner.md)]

`ISOCREDREF`-funktio palauttaa *merkkijono*-arvon, joka edustaa laskuttajan ISO (International Organization for Standardization) -viitettä määritetyn laskunumeron lukujen ja kirjainmerkkien perusteella.

## <a name="syntax"></a>Syntaksi

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a>Argumentit

`invoice number digits`: *Merkkijono*

Tekstiarvo, joka edustaa laskunumeron numeroita.

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

> [!NOTE] 
> Voit poistaa ne aakkosmerkit, jotka eivät ole ISO-yhteensopivia, jos `invoice number digits`-argumentti on käännetty ennen kuin se välitetään tälle toiminnolle.

## <a name="example"></a>Esimerkki

`ISOCredRef ("VEND-200002")` palauttaa arvon **"RF23VEND-200002"**.

## <a name="additional-resources"></a>Lisäresurssit

[Muut (liiketoiminnan toimialuekohtaiset) toiminnot](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]