---
title: UPPER ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) UPPER-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: c3e594138ef8e28f1b3aaf333026fa8f9e55cca0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688338"
---
# <a name="upper-er-function"></a>UPPER ER-funktio

[!include [banner](../includes/banner.md)]

`UPPER`-funktio palauttaa määritetyn tekstimerkkijonon *Merkkijono*-arvona sen jälkeen, kun se on muunnettu isoiksi kirjaimiksi.

## <a name="syntax"></a>Syntaksi

```vb
UPPER (text )
```

## <a name="arguments"></a>Argumentit

`text`: *Merkkijono*

*Merkkijono*-tietotyypin tietolähteen kelvollinen polku.

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="example"></a>Esimerkki

`UPPER ("Sample")` palauttaa arvon **MALLI**.

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]