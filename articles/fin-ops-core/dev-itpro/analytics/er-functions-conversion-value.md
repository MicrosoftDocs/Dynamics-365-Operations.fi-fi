---
title: VALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) VALUE-funktiota käytetään.
author: NickSelin
ms.date: 12/05/2019
ms.topic: article
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
ms.openlocfilehash: 2252823d98b63d36d9bb195696abef34ac9c98b6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752577"
---
# <a name="value-er-function"></a>VALUE ER -funktio

[!include [banner](../includes/banner.md)]

`VALUE`-funktio palauttaa *todellisen* arvon, joka muunnetaan määritetystä merkkijonosta.

## <a name="syntax"></a>Syntaksi

```vb
VALUE (text)
```

## <a name="arguments"></a>Argumentit

`text`: *Merkkijono*

Merkkijonon arvo, jota ei pidä muuntaa numeroarvoon.

## <a name="return-values"></a>Palautusarvot

*Reaaliluku*

Tuloksena oleva numeroarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Pilkkuja ja pisteitä (.) pidetään desimaalierottimina. Alussa olevaa tavuviivaa (-) pidetään miinusmerkkinä. Poikkeus annetaan suorituksen aikana, jos määritetyssä merkkijonossa on muita kuin numeerisia merkkejä.

## <a name="example-1"></a>Esimerkki 1

`VALUE ("1 234,56")` antaa poikkeuksen.

## <a name="example-2"></a>Esimerkki 2

`VALUE ("1234,56")` palauttaa **1234.56**.

## <a name="additional-resources"></a>Lisäresurssit

[Tyypin muuntamisen toiminnot](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]