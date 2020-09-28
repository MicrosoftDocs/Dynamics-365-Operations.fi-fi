---
title: STRINGJOIN ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) STRINGJOIN-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f5d6b9a0f43902160d1ff7fa91b86a7e2c3422d
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743491"
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
