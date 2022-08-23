---
title: TRIM ER -funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) TRIM-funktiota käytetään.
author: kfend
ms.date: 02/28/2022
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
ms.openlocfilehash: 95b8d2989d705c4998da0af8e683adf567edfe92
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273095"
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
