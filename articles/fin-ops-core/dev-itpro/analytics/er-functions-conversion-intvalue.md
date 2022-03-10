---
title: INTVALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) INTVALUE-funktiota käytetään.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 5d54543a6f9878feb3482c1c1e6c1f1f468718489fbc46aded84a5a84bdfb04e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745937"
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