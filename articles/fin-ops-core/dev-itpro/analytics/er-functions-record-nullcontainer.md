---
title: NULLCONTAINER ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) NULLCONTAINER-funktiota käytetään.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 8da2a30cf2839adabf7b5ea4916f44999aa05758
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850955"
---
# <a name="nullcontainer-er-function"></a>NULLCONTAINER ER-funktio

[!include [banner](../includes/banner.md)]

`NULLCONTAINER`-funktio palauttaa tyhjäarvo-*säilön (tietueen)* arvon, jolla on sama rakenne kuin määritetyllä tietueluettelolla tai tietueella.

## <a name="syntax"></a>Syntaksi

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a>Argumentit

`list`: *Tietueluettelo* tai *Säilö (tietue)*

Tietolähteen kelvollinen polku on joko *Tietueluettelo* tai *Säilö (tietue)*-tyyppi.

## <a name="return-values"></a>Palautusarvot

*Kontti (tietue)*

Tuloksena oleva tietueen arvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

> [!NOTE] 
> Tämä toiminto on vanhentunut. Käytä sen sijaan `EMPTYRECORD`-funktiota. Lisätietoja on kohdassa [EMPTYRECORD](er-functions-record-emptyrecord.md)

## <a name="example"></a>Esimerkki

`NULLCONTAINER (SPLIT ("abc", 1))` palauttaa uuden tyhjän tietueen, jonka rakenne on sama kuin `SPLIT`-toiminnon palauttamalla luettelolla. Lisätietoja on kohdassa [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Lisäresurssit

[Tallennustoiminnot](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]