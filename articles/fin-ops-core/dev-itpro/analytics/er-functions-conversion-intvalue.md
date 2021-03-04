---
title: INTVALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) INTVALUE-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 98b91a983c60bb99280763f7f7a944d08f535e60
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686000"
---
# <a name="intvalue-er-function"></a>INTVALUE ER -funktio

[!include [banner](../includes/banner.md)]

`INTVALUE`-funktio palauttaa *Int*-arvon, joka edustaa määritettyä merkkijonoa.

## <a name="syntax-1"></a>Syntaksi 1

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a>Syntaksi 2

```vb
INTVALUE (number)
```

## <a name="arguments"></a>Argumentit

`text`: *Merkkijono*

Tekstiarvo, jota ei pidä muuntaa *Int*-numeroksi.

`number`: *Todellinen* tai *Kokonaisluku*

Numeerinen *todellinen* tai *kokonaisluku*-arvo, jota ei pidä muuntaa *Int*-numeroksi.

## <a name="return-values"></a>Palautusarvot

*Int*

Tuloksena oleva numeroarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Kaikki desimaalit lyhennetään.

## <a name="example-1"></a>Esimerkki 1

`INTVALUE ("100.77")` palauttaa *Int*-arvon **100**.

## <a name="example-2"></a>Esimerkki 2

`INTVALUE (-100.77)` palauttaa *Int*-arvon **-100**.

## <a name="additional-resources"></a>Lisäresurssit

[Tyypin muuntamisen toiminnot](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]