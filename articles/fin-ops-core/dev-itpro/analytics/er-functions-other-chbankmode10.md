---
title: CH_BANK_MOD_10 ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) CH_BANK_MOD_10-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 21942fa47b968fa10bfc9b07f269d44e495139fe
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564837"
---
# <a name="ch_bank_mod_10-er-function"></a>CH_BANK_MOD_10 ER -funktio

[!include [banner](../includes/banner.md)]

`CH_BANK_MOD_10`-funktio palauttaa *merkkijono*-arvon, joka vastaa velkojan viittausta MOD10-lausekkeena määritetyn laskunumeron numeroiden perusteella.

## <a name="syntax"></a>Syntaksi

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a>Argumentit

`invoice number digits`: *Merkkijono*

Tekstiarvo, joka edustaa laskunumeron numeroita.

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="example"></a>Esimerkki

`CH_BANK_MOD_10 ("VEND-200002")` palauttaa **3**.

## <a name="additional-resources"></a>Lisäresurssit

[Muut (liiketoiminnan toimialuekohtaiset) toiminnot](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]