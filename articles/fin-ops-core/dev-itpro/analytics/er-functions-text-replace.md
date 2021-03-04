---
title: REPLACE ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) REPLACE-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 3c9d3b6748ecb1680586a2d47a425b5ef98551f1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682915"
---
# <a name="replace-er-function"></a>REPLACE ER-funktio

[!include [banner](../includes/banner.md)]

`REPLACE`-funktio palauttaa määritetyn tekstimerkkijonon *merkkijonona*, kun se kokonaan tai osa siitä on korvattu toisella merkkijonolla.

## <a name="syntax"></a>Syntaksi

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a>Argumentit

`text`: *Merkkijono*

*Merkkijono*-tietotyypin tietolähteen kelvollinen polku.

`pattern`: *Merkkijono*

Jos `regular expression flag` -argumentti on **EPÄTOSI**, tämä argumentti sisältää tekstin, joka on korvattava.

Jos `regular expression flag` -argumentti on **TOSI**, tämä argumentti sisältää säännöllisen lausekkeen, joka määrittää sekä hakukuvion että korvaavan tekstin.

`replacement`: *Merkkijono*

Jos `regular expression flag` -argumentti on **EPÄTOSI**, tämä argumentti sisältää tekstin, jota täytyy käyttää korvaavana tekstinä.

Jos `regular expression flag` -argumentti on **TOSI**, tätä argumenttia ei käytetä.

`regular expression flag`: *Totuusarvo*

*Totuusarvo* , joka ilmaisee, käytetäänkö korvauksena säännöllistä lauseketta.

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Jos `regular expression flag` -argumentti on **TOSI**, funktio palauttaa määritetyn merkkijonon sen jälkeen, kun se on muutettu, käyttämällä `pattern`-argumentilla määritettyä säännöllistä lauseketta. Säännöllistä lauseketta käytetään etsittäessä korvattavia merkkejä.

Jos `regular expression flag` -argumentti on **EPÄTOSI**, tämä funktio palauttaa määritetyn merkkijonon sen jälkeen, kun argumentissa määritetty `pattern`-argumentin merkkijoukko on korvattu `replacement`-argumentin merkeillä. 

## <a name="example-1"></a>Esimerkki 1

`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` on käytössä säännöllisessä lausekkeessa, joka poistaa kaikki muut kuin numeeriset merkit ja se palauttaa arvon **19234564971**. 

## <a name="example-2"></a>Esimerkki 2

`REPLACE ("abcdef", "cd", "GH", false)` korvaa mallin **cd** merkkijonolla **GH** ja palauttaa arvon **abGHef**.

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]