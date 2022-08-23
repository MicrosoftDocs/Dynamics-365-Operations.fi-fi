---
title: NUMBERFORMAT ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) NUMBERFORMAT-funktiota käytetään.
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 5519f549c10ba5c02e249592d040582c3f8dc44f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274792"
---
# <a name="numberformat-er-function"></a>NUMBERFORMAT ER-funktio

[!include [banner](../includes/banner.md)]

`NUMBERFORMAT`-funktio palauttaa *Merkkijonoarvon*, joka edustaa määritetyn numeron määritetyssä muodossa ja valinnaisesti määritetyssä [kulttuurissa](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Lisätietoja tuetuista muodoista on kohdassa [vakio](/dotnet/standard/base-types/standard-numeric-format-strings) ja [mukautettu](/dotnet/standard/base-types/custom-numeric-format-strings).

## <a name="syntax-1"></a>Syntaksi 1

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a>Syntaksi 2

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a>Argumentit

`number`: *Kokonaisluku* tai *Todellinen*

Numeerinen arvo, joka määrittää muotoiltava lukumäärän.

`format` : *Merkkijono*

*Merkkijono*-arvo, joka esittelee alkuperäisen muodon.

`culture`: *Merkkijono*

*Merkkijono*-arvo, joka edustaa muotoilussa käytettävää kulttuuria.

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Jos kulttuuria ei ole määritetty kutsuttujen funktioiden argumentiksi, sen konteksti, jossa tämä funktio suoritetaan, määrittää lukujen muotoilussa käytettävän kulttuurin.

## <a name="example-1"></a>Esimerkki 1

Jos maa-asetukset ovat **EN-US**, `NUMBERFORMAT (0.45, "p")` palauttaa arvon **45.00 %** ja `NUMBERFORMAT (10.45, "#")` palauttaa arvon **10**.

## <a name="example-2"></a>Esimerkki 2

`NUMBERFORMAT (10/3, "F2", "de")`-funktio palauttaa arvon **3,33**, kun `NUMBERFORMAT (10/3, "F2", "en-us")` palauttaa arvon **3.33**.

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
