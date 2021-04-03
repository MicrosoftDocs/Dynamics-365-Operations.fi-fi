---
title: MID ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) MID-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: e0520bc54465f00d36e88787933b291847dee852
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562730"
---
# <a name="mid-er-function"></a>MID ER -funktio

[!include [banner](../includes/banner.md)]

`MID`-funktio palauttaa määritetystä luettelosta *merkkijono*-arvon, joka esittää määritetyn määrän merkkejä määrätystä merkkijonosta, alkaen määritellystä kohdasta.

## <a name="syntax"></a>Syntaksi

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a>Argumentit

`text`: *Merkkijono*

*Merkkijono*-arvo, joka määrittää tekstin, josta merkit palautetaan.

`starting position`: *Kokonaisluku*

*Kokonaislukuarvo*, joka määrittää sen ensimmäisen merkin sijainnin, joka on palautettava määritetystä tekstistä.

`number of characters`: *Kokonaisluku*

*Kokonaislukuarvo*, joka määrittelee palautettavien merkkien lukumäärän määritetystä aloituspaikasta alkaen.

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Jos `starting position` -argumentin arvo on pienempi kuin 0 (nolla), palautetut merkit lasketaan määritetyn merkkijonon ensimmäisestä kohdasta.

Jos `starting position` -argumentin arvo ylittää määritetyn merkkijonon pituuden, funktio palauttaa tyhjän merkkijonon.

## <a name="example"></a>Esimerkki

`MID ("Sample", 2, 3)` palauttaa arvon **amp**.

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]