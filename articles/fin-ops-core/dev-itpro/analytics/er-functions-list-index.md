---
title: INDEX ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) INDEX-funktiota käytetään.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a49def8aaa5398fbc7e0f06cc26df8a745207c93
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687988"
---
# <a name="index-er-function"></a>INDEX ER-funktio

[!include [banner](../includes/banner.md)]

`INDEX`-funktio palauttaa *Säilö (tietue)*-arvon, joka on valittu määritetyn numeroindeksin avulla määritetyssä luettelossa. Jos indeksi on määritellyn luettelon tietueiden ulkopuolella, poikkeus heitetään.

## <a name="syntax"></a>Syntaksi

```vb
INDEX (list, index)
```

## <a name="arguments"></a>Argumentit

`list`: *Tietueluettelo*

*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.

`index`: *Kokonaisluku*

Numeerinen indeksi, joka ilmaisee halutun tietueen sijainnin määritetyssä luettelossa.

## <a name="return-values"></a>Palautusarvot

*Kontti (tietue)*

Tuloksena oleva tietueen arvo.

## <a name="example-1"></a>Esimerkki 1

Jos syötät tietolähteen **DS** *laskettuun kenttätyyppiin* ja se sisältää lausekkeen `SPLIT ("A|B|C", "|")`, lauseke `DS.Value`, palauttaa tekstiarvon **B** tämän tietueluettelon toiselle tietueelle. Lauseke `INDEX (SPLIT ("A|B|C", "|"), 2).Value` palauttaa myös tekstiarvon **B**.

## <a name="example-2"></a>Esimerkki 2

Jos syötät *Lasketun kenttä* -tyypin **DS**-tietolähteen, ja se sisältää lausekkeen `SPLIT ("A|B|C", "|")`, lauseke `INDEX (SPLIT ("A|B|C", "|"), 4).Value` heittää poikkeuksen suorituksen aikana.

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]