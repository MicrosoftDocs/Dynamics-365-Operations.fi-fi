---
title: CONVERTCURRENCY ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) CONVERTCURRENCY-funktiota käytetään.
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
ms.openlocfilehash: 0f0d5bace9b62cf6f0d7576744a6cc271666bf73
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567637"
---
# <a name="convertcurrency-er-function"></a>CONVERTCURRENCY ER-funktio

[!include [banner](../includes/banner.md)]

`CONVERTCURRENCY`-funktio palauttaa *todellisen* arvon, joka edustaa tulosta muuntamalla määritetty rahasumma määritetystä lähdevaluutasta määritettyyn kohdevaluuttaan käyttämällä määritetyn yrityksen asetuksia tiettynä päivänä.

## <a name="syntax"></a>Syntaksi

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a>Argumentit

`amount`: *Kokonaisluku* tai *Todellinen*

Numeerinen arvo, joka edustaa muunnettavaa rahasummaa.

`source currency`: *Merkkijono*

Lähdevaluutan koodi.

`target currency`: *Merkkijono*

Kohdevaluutan koodi.

`date`: *Päivämäärä*

*Päivämäärä*-arvo, joka vastaa muunnoksen vaihtokurssin määrittämiseen käytettävää päivämäärää.

`company`: *Merkkijono*

*Merkkijono*-arvo, joka kuvaa konversiolle käytettäviä asetuksia käsittelevän yrityksen koodia.

## <a name="return-values"></a>Palautusarvot

*Reaaliluku*

Tuloksena oleva numeroarvo.

## <a name="example"></a>Esimerkki

`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` palauttaa yhden euron suuruisen määrän Yhdysvaltojen dollareita nykyisen istunnon päivämääränä **DEMF**-yrityksen asetusten perusteella.

## <a name="additional-resources"></a>Lisäresurssit

[Muut (liiketoiminnan toimialuekohtaiset) toiminnot](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]