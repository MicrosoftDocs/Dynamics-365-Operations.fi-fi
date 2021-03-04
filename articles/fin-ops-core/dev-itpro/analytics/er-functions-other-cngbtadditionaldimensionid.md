---
title: CN_GBT_ADDITIONALDIMENSIONID ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) CN_GBT_ADDITIONALDIMENSIONID-funktiota käytetään.
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
ms.openlocfilehash: 38908c63c35465747505479bc983ada891f9e2bf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686807"
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