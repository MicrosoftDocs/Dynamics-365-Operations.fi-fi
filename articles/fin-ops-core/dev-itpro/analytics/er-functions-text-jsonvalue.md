---
title: JSONVALUE ER -funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) JSONVALUE-funktiota käytetään.
author: NickSelin
ms.date: 10/25/2021
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
ms.openlocfilehash: 7deaed83959f033d11333efb5a2b398cbe57076d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909497"
---
# <a name="jsonvalue-er-function"></a>JSONVALUE ER -funktio

[!include [banner](../includes/banner.md)]

`JSONVALUE`-funktio jäsentää tiedot JavaScript Object Notation (JSON) -muodossa, jota käytettään tietyssä polussa, ja se purkaa skalaariarvon, jolla on tietty tunnus. Sen jälkeen se palauttaa puretut skalaariarvot *merkkijono*-arvona.

## <a name="syntax"></a>Syntaksi

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>Argumentit

`input`: *Merkkijono*

JSON-tietoja sisältävän *Merkkijono*-tyypin tietolähteen kelvollinen polku.

`path`: *Merkkijono*

JSON-tietojen skaalariarvon tunniste. Erota toisiinsa liittyvien JSON-solmujen nimet vinoviivalla (/). Käytä hakasuljemerkintää (\[\]) tietyn arvon indeksin määrittämiseksi JSON-matriisissa. Huomaa, että tässä indeksissä käytetään nollaan perustuvaa numerointia.

## <a name="return-values"></a>Palautusarvot

*Merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="example-1"></a>Esimerkki 1

**$JsonField**-tietolähde sisältää seuraavat tiedot JSON-muodossa: **{BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**. Tässä tapauksessa `JSONVALUE (JsonField, "BuildNumber")`-lauseke palauttaa *merkkijonon* tietotyypin seuraavan arvon: **"7.3.1234.1"**.

## <a name="example-2"></a>Esimerkki 2

*Laskettu kenttä* -tyypin **JsonField**-tietolähde sisältää lausekkeen `"{""workers"": [ {""name"": ""Adam"", ""age"": 30, ""emails"": [""AdamS@Contoso.com"", ""AdamS@Hotmail.com"" ]}, { ""name"": ""John"", ""age"": 21, ""emails"": [""JohnS@Contoso.com"", ""JohnS@Aol.com""]}]}"`

Tämä lauseke on määritetty palauttamaan [*Merkkijono*](er-formula-supported-data-types-primitive.md#string)-arvo, joka edustaa seuraavia tietoja JSON-muodossa.

```json
{
    "workers": [
        {
            "name": "Adam",
            "age": 30,
            "emails": [ "AdamS@Contoso.com", "AdamS@Hotmail.com" ]
        },
        {
            "name": "John",
            "age": 21,
            "emails": [ "JohnS@Contoso.com", "JohnS@Aol.com" ]
        }
    ]
}
```

Tässä tapauksessa lauseke `JSONVALUE(json, "workers/[1]/emails/[0]")` palauttaa *Merkkijono*-tietotyypin seuraavan arvon: `JohnS@Contoso.com`.

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
