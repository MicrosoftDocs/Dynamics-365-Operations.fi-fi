---
title: CN_GBT_ADDITIONALDIMENSIONID ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) CN_GBT_ADDITIONALDIMENSIONID-funktiota käytetään.
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
ms.openlocfilehash: 9217b70076a369c18a94f820f19ca371c2d8aca61ab72b6be762592f39fa1160
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731542"
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