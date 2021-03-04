---
title: CHAR ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) CHAR-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: a9f0f70c250592bf74b1a1df823e66803e853a64
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682988"
---
# <a name="char-er-function"></a>CHAR ER -funktio

[!include [banner](../includes/banner.md)]

`CHAR`-funktio palauttaa *Merkkijono*-arvon, joka edustaa yksittäistä merkkiä, johon viitataan määritetyllä Unicode-numerolla.

## <a name="syntax"></a>Syntaksi

```vb
CHAR (number)
```

## <a name="arguments"></a>Argumentit

`number`: *Kokonaisluku*

Numero, joka vastaa odotettua yksittäistä merkkiä.

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Tämän funktion palauttama merkkijono määräytyy koodauksen mukaan, joka on valittu ylemmän tason **FILE**-muotoisessa elementissä. Luettelo tuetuista koodauksista on kohdassa [Koodausluokka](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).

## <a name="example"></a>Esimerkki

`CHAR (255)` palauttaa arvon **"ÿ"**.

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]