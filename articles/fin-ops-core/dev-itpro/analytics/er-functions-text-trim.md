---
title: TRIM ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) TRIM-funktiota käytetään.
author: NickSelin
ms.date: 02/28/2022
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
ms.openlocfilehash: 816f6d6623bb778c9186d294c9b67db7edddd671
ms.sourcegitcommit: 753714ac0dabc4b7ce91509757cd19f7be4a4793
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/01/2022
ms.locfileid: "8367789"
---
# <a name="trim-er-function"></a>TRIM ER -funktio

[!include [banner](../includes/banner.md)]

`TRIM`-toiminto palauttaa määritetyn tekstimerkkijonon *merkkijonona*, kun sarkain-, rivinvaihto-, rivisyöte- ja lomakesyötemerkit on korvattu yhdellä välilyönnillä, kun alun ja lopun välilyönnit on lyhennetty ja kun sanojen välistä on poistettu useat välilyönnit.

## <a name="syntax"></a>Syntaksi

```vb
TRIM (text)
```

## <a name="arguments"></a>Argumentit

`text`: *Merkkijono*

*Merkkijono*-tietotyypin tietolähteen kelvollinen polku.

## <a name="return-values"></a>Palautusarvot

*Merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Joissain tapauksissa alun ja lopun välit halutaan poistaa, mutta haluat säilyttää muotoilun määritetyssä tekstissä. Jos tämä teksti edustaa esimerkiksi osoitetta, joka voidaan syöttää moniriviseen tekstiruutuun ja joka voi sisältää rivisyötteen ja rivinvaihdon muotoilun. Käytä tässä tapauksessa seuraavaa lauseketta: `REPLACE(text,"^[ \t]+|[ \t]+$","", true)`, missä se `text` on argumentti, joka viittaa määritettyyn tekstimerkkijonoon.

## <a name="example-1"></a>Esimerkki 1

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` palauttaa arvon **Malliteksti**.

## <a name="example-2"></a>Esimerkki 2

`TRIM (CONCATENATE (CHAR(10), "`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(9),"`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(13)))` palauttaa **"Sample text"**.

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)

[REPLACE ER-funktio](er-functions-text-replace.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
