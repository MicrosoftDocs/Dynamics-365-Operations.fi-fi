---
title: NULLDATETIME ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) NULLDATETIME-funktiota käytetään.
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 49b75a6cc1e2c1eee926ed8a235ae886d781ad3c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287275"
---
# <a name="nulldatetime-er-function"></a>NULLDATETIME ER-funktio

[!include [banner](../includes/banner.md)]

`NULLDATETIME`-funktio palauttaa *DateTime*-arvon, joka edustaa **Null**-arvoista päivämäärä- ja aika-arvoa (1. tammikuuta 1900) koordinoituun yleisaikaan (Greenwichin keskimääräinen aika \[GMT\]).

## <a name="syntax"></a>Syntaksi

```vb
NULLDATETIME ()
```

## <a name="return-values"></a>Palautusarvot

*DateTime*

Tulokseksi saatava päivämäärä-/aika-arvo.

## <a name="example"></a>Esimerkki

`DATETIMEFORMAT( NULLDATETIME(), "O")` palauttaa merkkijonon arvon **1900-01-01T00:00:00.0000000+00:00**, kun sitä kutsutaan prosessin aikana, jonka on käynnistänyt sovelluskäyttäjä, jolla on aikavyöhyke arvo **(GMT) koordinoituun yleisaikaan** **kieli ja maa/alue-asetukset** -osassa.

## <a name="additional-resources"></a>Lisäresurssit

[Päivämäärä- ja aikatoiminnot](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
