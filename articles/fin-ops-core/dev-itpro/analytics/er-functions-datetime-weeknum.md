---
title: WEEKNUM ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) WEEKNUM-funktiota käytetään.
author: NickSelin
ms.date: 01/15/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: 37e62b32896e2030b3322a89ac4acdd6c18d5e3c
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982174"
---
# <a name="weeknum-er-function"></a>WEEKNUM ER -funktio

[!include [banner](../includes/banner.md)]

`WEEKNUM`-funktio palauttaa *[Kokonaisluku](er-formula-supported-data-types-primitive.md#integer)*-arvon, joka kuvaa vuoden viikkoa, johon kuuluu määritetty *[Päivämäärä](er-formula-supported-data-types-primitive.md#date)*-arvo. Laskenta perustuu kulttuurisidonnaisiin sääntöihin, jotka määrittävät kalenteriviikkoa ja viikon ensimmäistä päivää.

## <a name="syntax"></a>Syntaksi

```vb
WEEKNUM (date, culture) as Integer
```

## <a name=""></a><a name="arguments">Argumentit</a>

`date`: *Päivämäärä*

Päivämääräarvo, joka ilmaisee päivämäärän, jota käytetään päivien määrän laskennassa.

`culture`: *[Merkkijono](er-formula-supported-data-types-primitive.md#string)*

Laskennassa käytettävä kulttuuri. Voit käyttää kielikoodeja, joita tuetaan .NET-[standardien](/dotnet/api/system.globalization.cultureinfo.getcultures?view=net-5.0) mukaisesti.

## <a name="return-values"></a>Palautusarvot

*Kokonaisluku*

Tuloksena oleva numeroarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Vuoden viikko lasketaan [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) -standardin perusteella, jos maa tai alue on hyväksynyt tämän standardin ajon aikana. Muussa tapauksessa laskenta perustuu maa-/aluekohtaisiin kansallisiin standardeihin.

Jos `WEEKNUM`-funktion argumenttina annetaan suorituksen aikana [kulttuuri](#arguments)-koodi, jota ei tueta, poikkeus näytetään. Jos tyhjä merkkijono annetaan kielikoodina, viikon numeron laskemiseen käytetään englanninkielistä maan ja ranskankielistä kalenteria.

## <a name="examples"></a>Esimerkkejä

`WEEKNUM (DATEVALUE ("01-01-2020", "de"))` palauttaa **1**.

`WEEKNUM (DATEVALUE ("01-01-2021", "de"))` palauttaa **53**.

`WEEKNUM (DATEVALUE ("01-01-2022", "de"))` palauttaa **52**.

`WEEKNUM (DATEVALUE ("01-01-2022", "ar"))` palauttaa **21**.

## <a name="additional-resources"></a>Lisäresurssit

[Päivämäärä- ja aikatoiminnot](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
