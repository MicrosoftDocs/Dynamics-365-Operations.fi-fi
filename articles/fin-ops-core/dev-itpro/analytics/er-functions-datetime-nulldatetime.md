---
title: NULLDATETIME ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NULLDATETIME-funktiota käytetään.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: f7282b7c161b6e183186ba81e6bcf7b34ce6e612
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746816"
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