---
title: DAYS ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) DAYS-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 66398e624e4b9d69d4dc3ccf3ee8f97758f4f861
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682338"
---
# <a name="days-er-function"></a>DAYS ER -funktio

[!include [banner](../includes/banner.md)]

`DAYS`-funktio palauttaa ensimmäisen määritetyn päivämäärän ja toisen määritetyn päivämäärän välisten päivien määrää kuvaavan arvon *kokonaislukuna*.

## <a name="syntax"></a>Syntaksi

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a>Argumentit

`date 1`: *Päivämäärä*

Päivämääräarvo, joka ilmaisee päivien määrän laskennassa käytettävää aloituspäivämäärää.

`date 2`: *Päivämäärä*

Päivämääräarvo, joka ilmaisee päivien määrän laskennassa käytettävää lopetuspäivämäärää.

## <a name="return-values"></a>Palautusarvot

*Kokonaisluku*

Tuloksena oleva numeroarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

`DAYS`-funktio palauttaa positiivisen arvon, kun ensimmäinen päivämäärä on myöhemmin kuin toinen päivämäärä, se palauttaa arvon **0** (nolla), kun ensimmäinen päivämäärä on sama kuin toinen päivämäärä ja palauttaa negatiivisen arvon, kun ensimmäinen päivämäärä on aikaisempi kuin toinen päivämäärä.

## <a name="example"></a>Esimerkki

`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.

## <a name="additional-resources"></a>Lisäresurssit

[Päivämäärä- ja aikatoiminnot](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]