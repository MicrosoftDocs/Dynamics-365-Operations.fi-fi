---
title: INT64VALUE ER -funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) INT64VALUE-funktiota käytetään.
author: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 4af6cd4ba8b08fe00f53e9dfb1a9156354ec17fc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292583"
---
# <a name="int64value-er-function"></a>INT64VALUE ER -funktio

[!include [banner](../includes/banner.md)]

`INT64VALUE`-funktio palauttaa *Int64*-arvon, joka edustaa määritettyä merkkijonoa.

## <a name="syntax-1"></a>Syntaksi 1

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a>Syntaksi 2

```vb
INT64VALUE (number)
```

## <a name="arguments"></a>Argumentit

`text`: *Merkkijono*

Tekstiarvo, jota ei pidä muuntaa *Int64*-numeroksi.

`number`: *Todellinen* tai *Kokonaisluku*

Numeerinen *todellinen* tai *kokonaisluku*-arvo, jota ei pidä muuntaa *Int64*-numeroksi.

## <a name="return-values"></a>Palautusarvot

*Int64*

Tuloksena oleva numeroarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Kaikki desimaalit lyhennetään.

## <a name="example-1"></a>Esimerkki 1

`INT64VALUE ("22565422744")` palauttaa *Int64*-arvon **22565422744**.

## <a name="example-2"></a>Esimerkki 2

`INT64VALUE ( VALUE("22565422744.77"))` palauttaa *Int64*-arvon **22565422744**.

## <a name="additional-resources"></a>Lisäresurssit

[Tyypin muuntamisen toiminnot](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
