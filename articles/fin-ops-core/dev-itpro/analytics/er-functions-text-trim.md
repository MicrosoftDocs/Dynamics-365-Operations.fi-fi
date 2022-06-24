---
title: TRIM ER -funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) TRIM-funktiota käytetään.
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
ms.openlocfilehash: deadf89641771efa864e701af9dad57c5e62ea37
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864641"
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
