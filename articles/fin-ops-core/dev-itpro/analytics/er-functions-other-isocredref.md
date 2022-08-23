---
title: ISOCREDREF ER -funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) ISOCREDREF-funktiota käytetään.
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
ms.openlocfilehash: 189843d608cc00ac51a284b163553da6d821150e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277583"
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
