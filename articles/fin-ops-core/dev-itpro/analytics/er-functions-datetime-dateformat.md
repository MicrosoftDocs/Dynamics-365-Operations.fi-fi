---
title: DATEFORMAT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) DATEFORMAT-funktiota käytetään.
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
ms.openlocfilehash: 4a6c113f5f8147cbeaab103e86a44d4c66272c13
ms.sourcegitcommit: e7eeca05d738e9e46d6185d1ba349836ebafc1a4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485489"
---
# <a name="dateformat-er-function"></a>DATEFORMAT ER-funktio

[!include [banner](../includes/banner.md)]

`DATEFORMAT`-funktio palauttaa *[Merkkijono](er-formula-supported-data-types-primitive.md#string)*-arvon, joka esittää tietyn päivämääräarvon tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä [kulttuurissa](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Lisätietoja tuetuista muodoista on kohdassa [vakio](/dotnet/standard/base-types/standard-date-and-time-format-strings) ja [mukautettu](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Syntaksi 1

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a>Syntaksi 2

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a>Argumentit

`date`: *[Päivämäärä](er-formula-supported-data-types-primitive.md#date)*

Päivämääräarvo, joka vastaa muokattavaa päivämäärää.

`format`: *Merkkijono*

Tulostusmerkkijonon muoto Lisätietoja tuetuista muodoista on kohdassa [vakio](/dotnet/standard/base-types/standard-date-and-time-format-strings) ja [mukautettu](/dotnet/standard/base-types/custom-date-and-time-format-strings).

> [!NOTE]
> Muodon merkkijono ottaa kirjainkoon huomioon, kun käytössä joko vakiomuoto tai mukautettu muoto. Esimerkiksi [vakiomuotoinen](/dotnet/standard/base-types/standard-date-and-time-format-strings) d-määrite palauttaa päivämäärän käyttämällä lyhyt päivämäärämalli, kun taas vakiomuotoinen D-määrite palauttaa pitkää päivämäärämallia käyttävän päivämäärän. Lisäksi [mukautetun](/dotnet/standard/base-types/custom-date-and-time-format-strings) muodon M-määrite palauttaa kuukaudet 1–12, kun taas mukautetun muodon m-määrite palauttaa minuutit 0–59.

`culture`: *Merkkijono*

Muotoilussa käytettävä kulttuuri. Lisätietoja tuetuista kulttuureista on kohdassa [kulttuuri](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Palautusarvot

*Merkkijono*

Tuloksena oleva merkkijonoarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Jos kulttuuria ei ole määritetty kutsutun funktion argumentiksi, kutsuvan kontekstin määrittämä arvo `culture` määritetään. Jos `DATEFORMAT`-funktiota kutsutaan esimerkiksi käyttämällä syntaksia 1 sähköisen raportoinnin (ER) muodossa **TIEDOSTO**-elementille, joka on määritetty käyttämään Saksan kulttuuria, muuntaminen tehdään Saksan kulttuurin avulla. `culture`-arvon oletusarvo on **FI-FI**.

## <a name="example-1"></a>Esimerkki 1

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` palauttaa nykyisen sovelluspalvelimen päivämäärän 24. joulukuuta 2015 merkkirivinä **24-12-2015** määritetyn mukautetun muodon mukaisesti.

## <a name="example-2"></a>Esimerkki 2

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` palauttaa nykyisen sovellusistunnon päivämäärän, 24. joulukuuta 2015, merkkijonona **"24-12-2015"**, joka perustuu valittuun Saksan kulttuuriin ja määritettyyn muotoon.

## <a name="additional-resources"></a>Lisäresurssit

[Päivämäärä- ja aikatoiminnot](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
