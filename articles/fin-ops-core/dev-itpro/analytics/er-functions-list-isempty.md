---
title: ISEMPTY ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) ISEMPTY-funktiota käytetään.
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: e1f1ac1cc1729ef6d0f0301f12cc3f4b07fc6110
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273215"
---
# <a name="isempty-er-function"></a>ISEMPTY ER-funktio

[!include [banner](../includes/banner.md)]

`ISEMPTY` funktio palauttaa *totuusarvon* **TOSI**, jos määritetty luettelo ei sisällä tietueita. Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**.

## <a name="syntax"></a>Syntaksi

```vb
ISEMPTY (list)
```

## <a name="arguments"></a>Argumentit

`list`: *Tietueluettelo*

*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.

## <a name="return-values"></a>Palautusarvot

*Boolen arvo*

Tuloksena oleva *Totuusarvo*-arvo.

## <a name="example-1"></a>Esimerkki 1

Jos syötät *Lasketun kenttä*-tyypin **DS**-tietolähteen, ja se sisältää lausekkeen `SPLIT ("A|B|C", "|")`, lauseke `ISEMPTY(DS)` palauttaa arvon **EPÄTOSI**.

## <a name="example-2"></a>Esimerkki 2

Lauseke `ISEMPTY (SPLIT ("",1))` palauttaa arvon **TOSI**.

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
