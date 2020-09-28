---
title: DATEVALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) DATEVALUE-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1970682db9a2278464aeff572599f0bfa6533e7d
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743588"
---
# <a name="datevalue-er-function"></a>DATEVALUE ER -funktio

[!include [banner](../includes/banner.md)]

`DATEVALUE`-funktio palauttaa *Date*-arvon, joka muunnetaan annetusta tekstiarvosta määrätyssä muodossa ja valinnaisesti määritellyssä [kulttuurissa](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) päivämääräarvoksi. Lisätietoja tuetuista muodoista on kohdassa [vakio](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ja [mukautettu](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>Syntaksi 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>Syntaksi 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumentit

`text`: *Merkkijono*

Teksti, joka vastaa muokattavaa arvoa.

`format`: *Merkkijono*

Annetun tekstin muoto.

`culture`: *Merkkijono*

Tietyn tekstin muotoilussa käytettävä kulttuuri.

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
