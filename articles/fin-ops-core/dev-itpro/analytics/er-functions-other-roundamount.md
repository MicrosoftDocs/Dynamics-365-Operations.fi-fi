---
title: ROUNDAMOUNT ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) ROUNDAMOUNT-funktiota käytetään.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 623024f4ee6ac0d237ec45d50d9678195d6c6cd0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905167"
---
# <a name="roundamount-er-function"></a>ROUNDAMOUNT ER-funktio

[!include [banner](../includes/banner.md)]

`ROUNDAMOUNT`-Funktio palauttaa *todellisen* arvon määritetyn numeron pyöristyksen tuloksena lähimpään toiseen useaan numeroon määritetyn pyöristyssäännön mukaisesti.

## <a name="syntax"></a>Syntaksi

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a>Argumentit

`number`: *Int* tai *Todellinen*

Numeerinen arvo, joka on pyöristettävä.

`decimals`: *Int* tai *Todellinen*

Numero, joka `number`-parametrin arvon on pyöristettävä useaan.

`round rule`: *Enum-arvo*

**RoundOffType**-luetteloinnin luettelointiarvo, joka määrittää pyöristyssäännön. Tämä luettelointi tarjoaa seuraavat arvot:

- Normaali (tavallinen)
- Alaspäin (RoundDown)
- Pyöristys ylös (RoundUp)

## <a name="return-values"></a>Palautusarvot

*Reaaliluku*

Tulokseksi saatava numeerinen arvo on moninkertaisesti `decimals`-parametrin määrittämän arvo, ja se on lähimpänä `number`-parametrin määrittämää arvoa.

## <a name="usage-notes"></a>Käyttöhuomautukset

Kun `number`-parametri on nolla, funktio palauttaa aina nollan.

Kun `decimals`-parametri on nolla, funktio pyöristää oletusarvoisen pyöristysarvon. Kun `round rule`-parametrin arvoksi on asetettu **RoundOffType.Ordinary**, oletuspyöristysarvo on **0,01**. Muussa tapauksessa pyöristysarvon oletusarvo on **1,0**.

Kun `round rule` -parametrin arvoksi on asetettu **RoundOffType.Ordinary**, tämä funktio pyöristää lähimpään pyöristysmäärään.

Kun `round rule` -parametrin arvoksi on asetettu **RoundOffType.RoundDown**, tämä funktio pyöristää kohti nollaa lähimpään pyöristysmäärään.

Kun `round rule` -parametrin arvoksi on asetettu **RoundOffType.RoundUp**, tämä funktio pyöristää pois nollasta lähimpään pyöristysmäärään.

Kun `round rule`-parametrin arvoksi on asetettu **RoundOffType.Ordinary**, tämä funktio käyttäytyy kuten [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel-funktio ja [ROUND](../dev-ref/xpp-math-run-time-functions.md#round) X + +-funktio.

## <a name="remarks"></a>Huomautukset

Jos haluat pyöristää numeerisen arvon määritettyyn desimaalien määrään, käytä [ROUND](er-functions-mathematical-round.md)-funktiota.

## <a name="example"></a>Esimerkki

Jos **model.RoundOff**-parametrin arvoksi on asetettu **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` palauttaa arvon 7,35. 

Jos **model.RoundOff**-parametrin arvoksi on asetettu **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` palauttaa arvon 7,35. 

Jos **model.RoundOff**-parametrin arvoksi on asetettu **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` palauttaa arvon 8,4.

## <a name="additional-resources"></a>Lisäresurssit

[Muut (liiketoiminnan toimialuekohtaiset) toiminnot](er-functions-category-other.md)

[Matemaattinen toiminto](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]