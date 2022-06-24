---
title: DATEVALUE ER -funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) DATEVALUE-funktiota käytetään.
author: NickSelin
ms.date: 09/08/2021
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
ms.openlocfilehash: 396d6823531d8bf2c5b5f61f2483422c84e54c62
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883785"
---
# <a name="datevalue-er-function"></a>DATEVALUE ER -funktio

[!include [banner](../includes/banner.md)]

`DATEVALUE`-funktio palauttaa *[Date](er-formula-supported-data-types-primitive.md#date)* arvon, joka muunnetaan annetusta tekstiarvosta määrätyssä muodossa ja valinnaisesti määritellyssä [kulttuurissa](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) päivämääräarvoksi. Lisätietoja tuetuista muodoista on kohdassa [vakio](/dotnet/standard/base-types/standard-date-and-time-format-strings) ja [mukautettu](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Syntaksi 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>Syntaksi 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumentit

`text`: *[Merkkijono](er-formula-supported-data-types-primitive.md#string)*

Teksti, joka vastaa muokattavaa arvoa.

`format`: *Merkkijono*

Annetun tekstin muoto. Lisätietoja tuetuista muodoista on kohdassa [vakio](/dotnet/standard/base-types/standard-date-and-time-format-strings) ja [mukautettu](/dotnet/standard/base-types/custom-date-and-time-format-strings).

`culture`: *Merkkijono*

Tietyn tekstin muotoilussa käytettävä kulttuuri. Lisätietoja tuetuista kulttuureista on kohdassa [kulttuuri](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Palautusarvot

*Päivämäärä*

Tulokseksi saatava päivämääräarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Kun kulttuuria ei ole määritetty kutsutun funktion argumentiksi, kutsuvan kontekstin määrittämä arvo `culture` määritetään. Jos `DATEVALUE`-funktiota kutsutaan esimerkiksi käyttämällä syntaksia 1 sähköisen raportoinnin (ER) muodossa **TIEDOSTO**-elementille, joka on määritetty käyttämään Saksan kulttuuria, muuntaminen tehdään Saksan kulttuurin avulla. `culture`-arvon oletusarvo on **FI-FI**.

## <a name="example-1"></a>Esimerkki 1

`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` palauttaa päivämääräarvon **2:55:00 am 21. joulukuuta 2016**, joka perustuu määritettyyn mukautettuun muotoon ja oletussovelluksen **EN-US** -kulttuuriin.

## <a name="example-2"></a>Esimerkki 2

`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` palauttaa päivämääräarvon **21. tammikuuta 2016** perustuen määritettyyn mukautettuun muotoon ja kulttuuriin.

Kuitenkin `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` aiheuttaa poikkeuksen, joka ilmoittaa käyttäjälle, että määritettyä merkkijonoa ei tunnisteta kelvolliseksi päivämääräarvoksi tietylle kulttuurille.

## <a name="additional-resources"></a>Lisäresurssit

[Päivämäärä- ja aikatoiminnot](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
