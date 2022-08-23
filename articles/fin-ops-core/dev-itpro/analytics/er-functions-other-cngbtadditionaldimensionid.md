---
title: CN_GBT_ADDITIONALDIMENSIONID ER -funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) CN_GBT_ADDITIONALDIMENSIONID-funktiota käytetään.
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
ms.openlocfilehash: 0ed2593f865a4764b1c6172722d701a0a10ba5f8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281749"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a>CN_GBT_ADDITIONALDIMENSIONID ER -funktio

[!include [banner](../includes/banner.md)]

`CN_GBT_ADDITIONALDIMENSIONID`-funktio palauttaa *merkkijono* arvon, joka edustaa yksittäistä taloushallinnon dimension tunnusta, joka on otettu määritetystä merkkijonosta. Määrätty merkkijono näyttää kaikki ulottuvuudet pilkulla erotettuna tunnusten luettelona.

## <a name="syntax"></a>Syntaksi

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a>Argumentit

`text`: *Merkkijono*

*Merkkijono*-arvo, joka näyttää kaikki ulottuvuudet pilkulla erotettuna tunnusten luettelona.

`number`: Kokonaisluku

*Kokonaisluku*-arvo, joka määrittää pyydetyn dimension järjestyskoodin tietyssä merkkijonossa.

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="example"></a>Esimerkki

`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` palauttaa arvon **CC**.

## <a name="additional-resources"></a>Lisäresurssit

[Muut (liiketoiminnan toimialuekohtaiset) toiminnot](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
