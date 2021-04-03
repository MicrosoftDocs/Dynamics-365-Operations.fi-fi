---
title: STRINGJOIN ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) STRINGJOIN-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 755e6481abb65dfecc8ddb6bceb032c8110095e2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568167"
---
# <a name="stringjoin-er-function"></a>STRINGJOIN ER-funktio

[!include [banner](../includes/banner.md)]

`STRINGJOIN`-funktio palauttaa määritetystä luettelosta *merkkijonon*, joka koostuu määritetyn kentän ketjutetuista arvoista tietystä luettelosta. Arvot voidaan erottaa määritetyllä erottimella.

## <a name="syntax"></a>Syntaksi

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a>Argumentit

`list`: *Tietueluettelo*

*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.

`field`: *Kenttä*

*Merkkijono*-tietotyypin kentän kelvollinen polku on määritetyssä luettelossa.

`delimiter`: *Merkkijono*

Erotin, jota käytetään erottelemaan alimerkkijonoja.

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="example"></a>Esimerkki

Jos syötät `SPLIT("abc" , 1)` tietolähteeksi **DS**, lauseke `STRINGJOIN (DS, DS.Value, "-")` palauttaa arvon **a-b-c**.

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]