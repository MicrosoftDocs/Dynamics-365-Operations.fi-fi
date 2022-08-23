---
title: INTVALUE ER -funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) INTVALUE-funktiota käytetään.
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
ms.openlocfilehash: eccee60c40bfc96f1fd93e7177207a1dd1888dc6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282618"
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
