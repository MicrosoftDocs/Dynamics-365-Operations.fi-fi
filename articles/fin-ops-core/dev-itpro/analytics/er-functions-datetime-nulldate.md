---
title: NULLDATE ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NULLDATE-funktiota käytetään.
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
ms.openlocfilehash: 6ac8da3f18c7793512685d52dd64a9bd55bfb8fc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746840"
---
# <a name="nulldate-er-function"></a>NULLDATE ER-funktio

[!include [banner](../includes/banner.md)]

`NULLDATE`-funktio palauttaa *päivämäärän* arvon, joka vastaa **Null**-arvoa (1. tammikuuta 1900).

## <a name="syntax"></a>Syntaksi

```vb
NULLDATE () as 
```

## <a name="return-values"></a>Palautusarvot

*Päivämäärä*

Tulokseksi saatava päivämääräarvo.

## <a name="example-1"></a>Esimerkki 1

`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` palauttaa **null**-arvon, 1. tammikuuta 1900, muodossa **"1900-01-01"** määritetyn mukautetun muodon perusteella.

## <a name="example-2"></a>Esimerkki 2

Lauseke `IF( Invoice.DocumentDate = NULLDATE(), true, false)` palauttaa arvon **Tosi**, kun **DocumentDate**-kentän arvo on **Null**-päivämäärä. Tässä esimerkissä **Lasku** on **Finance/taulutietueet**-tyypin sähköisen raportoinnin ER-tietolähde, joka viittaa CustInvoiceJour-tauluun.

## <a name="additional-resources"></a>Lisäresurssit

[Päivämäärä- ja aikatoiminnot](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]