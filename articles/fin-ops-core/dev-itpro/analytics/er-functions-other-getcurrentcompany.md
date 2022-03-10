---
title: GETCURRENTCOMPANY ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) GETCURRENTCOMPANY-funktiota käytetään.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: c74ffaf1ee134da8d962e054656301d5e99827ff53f560f5d93f9dcb51819c13
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760771"
---
# <a name="getcurrentcompany-er-function"></a>GETCURRENTCOMPANY ER-funktio

[!include [banner](../includes/banner.md)]

`GETCURRENTCOMPANY`-funktio palauttaa *Merkkijono*-arvon siltä yritykseltä, johon käyttäjä on tällä hetkellä kirjautunut.

## <a name="syntax"></a>Syntaksi

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="example"></a>Esimerkki

`GETCURRENTCOMPANY ()` palauttaa arvon **USMF** käyttäjälle, joka kirjautui **Contoso Entertainment System USA** -yritykseen.

## <a name="additional-resources"></a>Lisäresurssit

[Muut (liiketoiminnan toimialuekohtaiset) toiminnot](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]