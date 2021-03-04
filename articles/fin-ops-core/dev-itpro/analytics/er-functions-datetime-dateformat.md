---
title: DATEFORMAT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) DATEFORMAT-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 1fa6bdef2168112aeb17e0edb9f9a6d1b3bd45c0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684928"
---
# <a name="dateformat-er-function"></a>DATEFORMAT ER-funktio

[!include [banner](../includes/banner.md)]

`DATEFORMAT`-funktio palauttaa *Merkkijono*-arvon, joka esittää tietyn päivämääräarvon tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä [kulttuurissa](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Lisätietoja tuetuista muodoista on kohdassa [vakio](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ja [mukautettu](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>Syntaksi 1

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a>Syntaksi 2

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a>Argumentit

`date`: *Päivämäärä*

Päivämääräarvo, joka vastaa muokattavaa päivämäärää.

`format`: *Merkkijono*

Tulostusmerkkijonon muoto

`culture`: *Merkkijono*

Muotoilussa käytettävä kulttuuri.

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tuloksena oleva merkkijonoarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Kun kulttuuria ei ole määritetty kutsutun funktion argumentiksi, kutsuvan kontekstin määrittämä arvo `culture` määritetään. Jos `DATEFORMAT`-funktiota kutsutaan esimerkiksi käyttämällä syntaksia 1 sähköisen raportoinnin (ER) muodossa **TIEDOSTO**-elementille, joka on määritetty käyttämään Saksan kulttuuria, muuntaminen tehdään Saksan kulttuurin avulla. `culture`-arvon oletusarvo on **FI-FI**.

## <a name="example-1"></a>Esimerkki 1

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` palauttaa nykyisen sovelluspalvelimen päivämäärän 24. joulukuuta 2015 merkkirivinä **24-12-2015** määritetyn mukautetun muodon mukaisesti.

## <a name="example-2"></a>Esimerkki 2

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` palauttaa nykyisen sovellusistunnon päivämäärän, 24. joulukuuta 2015, merkkijonona **"24-12-2015"**, joka perustuu valittuun Saksan kulttuuriin ja määritettyyn muotoon.

## <a name="additional-resources"></a>Lisäresurssit

[Päivämäärä- ja aikatoiminnot](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]