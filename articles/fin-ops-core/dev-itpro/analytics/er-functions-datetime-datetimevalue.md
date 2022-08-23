---
title: DATETIMEVALUE ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) DATETIMEVALUE-funktiota käytetään.
author: kfend
ms.date: 09/08/2021
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
ms.openlocfilehash: 591c707ae7f57236386de0b4ef85d428c9ae31fd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287335"
---
# <a name="datetimevalue-er-function"></a>DATETIMEVALUE ER-funktio

[!include [banner](../includes/banner.md)]

`DATETIMEVALUE` -funktio palauttaa *[Päivämäärä/aika](er-formula-supported-data-types-primitive.md#datetime)* -arvon, joka muunnetaan tietystä tekstiarvosta tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä [kulttuurissa](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) päivämäärä-/aika-arvoksi. Lisätietoja tuetuista muodoista on kohdassa [vakio](/dotnet/standard/base-types/standard-date-and-time-format-strings) ja [mukautettu](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Syntaksi 1

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a>Syntaksi 2

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumentit

`text`: *[Merkkijono](er-formula-supported-data-types-primitive.md#string)*

Teksti, joka vastaa muokattavaa arvoa.

`format`: *Merkkijono*

Annetun tekstin muoto. Lisätietoja tuetuista muodoista on kohdassa [vakio](/dotnet/standard/base-types/standard-date-and-time-format-strings) ja [mukautettu](/dotnet/standard/base-types/custom-date-and-time-format-strings).

`culture`: *Merkkijono*

Tietyn tekstin muotoilussa käytettävä kulttuuri. Lisätietoja tuetuista kulttuureista on kohdassa [kulttuuri](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Palautusarvot

*Päivämäärä ja aika*

Tulokseksi saatava päivämäärä-/aika-arvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Kun kulttuuria ei ole määritetty kutsutun funktion argumentiksi, kutsuvan kontekstin määrittämä arvo `culture` määritetään. Jos `DATETIMEVALUE`-funktiota kutsutaan esimerkiksi käyttämällä syntaksia 1 sähköisen raportoinnin (ER) muodossa **TIEDOSTO**-elementille, joka on määritetty käyttämään Saksan kulttuuria, muuntaminen tehdään Saksan kulttuurin avulla. `culture`-arvon oletusarvo on **FI-FI**.

## <a name="example-1"></a>Esimerkki 1

`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` palauttaa arvon **2:55:00 am 21. joulukuuta 2016**, joka perustuu määritettyyn mukautettuun muotoon ja oletussovelluksen **EN-US** -kulttuuriin.

## <a name="example-2"></a>Esimerkki 2

`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` palauttaa arvon **2:55:00 AM 21. joulukuuta 2016** perustuen määritettyyn mukautettuun muotoon ja kulttuuriin.

Kuitenkin `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` aiheuttaa poikkeuksen, joka ilmoittaa käyttäjälle, että määritettyä merkkijonoa ei tunnisteta kelvolliseksi päivämäärä-/aika-arvoksi tietylle kulttuurille.

## <a name="additional-resources"></a>Lisäresurssit

[Päivämäärä- ja aikatoiminnot](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
