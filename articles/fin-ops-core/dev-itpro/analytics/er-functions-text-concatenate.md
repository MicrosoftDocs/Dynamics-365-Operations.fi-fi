---
title: CONCATENATE ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) CONCATENATE-funktiota käytetään
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 6e4800ce44d9da07818acec55c50224a9a000fe6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569602"
---
# <a name="concatenate-er-function"></a>CONCATENATE ER-funktio

[!include [banner](../includes/banner.md)]

`CONCATENATE`-funktio palauttaa kaikki määritetyt tekstimerkkijonot *Merkkijono*-arvona sen jälkeen, kun ne on liitetty yhdeksi merkkijonoksi.

## <a name="syntax"></a>Syntaksi

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a>Argumentit

`text 1`: *Merkkijono*

Viittaus *Merkkijonon* tietotyypin tietolähteeseen. Tämä argumentti on pakollinen.

`text N`: *Merkkijono*

Viittaus *Merkkijonon* tietotyypin tietolähteeseen. Nämä lisäargumentit ovat valinnaisia.

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="example"></a>Esimerkki

`CONCATENATE ("abc", "def")`-funktio palauttaa arvon **abcdef**.

## <a name="usage-notes"></a>Käyttöhuomautukset

Myös lauseke `"abc" & "def"` palauttaa lausekkeen **abcdef**.

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]