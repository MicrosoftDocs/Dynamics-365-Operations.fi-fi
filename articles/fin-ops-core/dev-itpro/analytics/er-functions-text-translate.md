---
title: TRANSLATE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) TRANSLATE-funktiota käytetään.
author: NickSelin
ms.date: 04/02/2020
ms.topic: article
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
ms.openlocfilehash: 7e4d6417757e27190ab7cabf2bf01243bb87b55c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746070"
---
# <a name="translate-er-function"></a>TRANSLATE ER -funktio

[!include [banner](../includes/banner.md)]

`TRANSLATE`-funktio palauttaa *Merkkijono*-arvon, joka sisältää määritetyn tekstin merkkien korvaamisen tuloksen toisen toimitetun joukon merkkeinä.

## <a name="syntax"></a>Syntaksi

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>Argumentit

`text`: *Merkkijono*

*Merkkijono*-tietotyypin tietolähteen kelvollinen polku.

`pattern`: *Merkkijono*

Teksti, joka tulee korvata.

`replacement`: *Merkkijono*

Korvaava teksti.

## <a name="return-values"></a>Palautusarvot

*Merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

`TRANSLATE`-toiminto korvaa yhden merkin kerrallaan. Funktio korvaa `text`-argumentin ensimmäisen merkin `pattern`-argumentin ensimmäisellä merkillä ja sitten toisen merkin ja noudattaa samaa virtausarvoa, kunnes se on valmis. Kun `text`- ja `pattern`-argumenttien merkit ovat samat, ne korvataan `replacement`-argumentilla, joka sijaitsee samassa sijainnissa kuin `pattern`-argumentin merkki. Jos merkki esiintyy `pattern`-argumenttina useita kertoja, käytetään tämän merkin ensimmäistä esiintymää vastaavaa `replacement`-argumenttimääritystä.

## <a name="example-1"></a>Esimerkki 1

`TRANSLATE ("abcdef", "cd", "GH")` korvaa määritetyn **abcde**- tekstin **c**-merkin `replacement`-tekstin **G**-merkillä seuraavien seikkojen vuoksi:
-   **c**-merkki esitetään ensimmäisessä kohdassa olevassa `pattern`-tekstissä.
-   `replacement`-tekstin ensimmäinen kohta sisältää **G**-merkin.

## <a name="example-2"></a>Esimerkki 2

`TRANSLATE ("abcdef", "ccd", "GH")`-funktio palauttaa arvon **abGdef**.

## <a name="example-3"></a>Esimerkki 3

`TRANSLATE ("abccba", "abc", "123")` palauttaa **"123321"**.

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]