---
title: WEEKNUM ER -funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) WEEKNUM-funktiota käytetään.
author: kfend
ms.date: 01/15/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.custom: 58771
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 4658f88b7e353e651177fad0c8636c5403be1256
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268143"
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
