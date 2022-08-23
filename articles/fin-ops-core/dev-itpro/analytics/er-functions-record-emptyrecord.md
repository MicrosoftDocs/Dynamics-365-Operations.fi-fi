---
title: EMPTYRECORD ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) EMPTYRECORD-funktiota käytetään.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 5046a1cb43f12863ddbdf241e8ba72071d1016ce
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280152"
---
# <a name="emptyrecord-er-function"></a>EMPTYRECORD ER-funktio

[!include [banner](../includes/banner.md)]

`EMPTYRECORD`-funktio palauttaa tyhjäarvo-*säilön (tietueen)* arvon, jolla on sama rakenne kuin määritetyllä tietueluettelolla tai tietueella.

## <a name="syntax"></a>Syntaksi

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a>Argumentit

`list`: *Tietueluettelo* tai *Säilö (tietue)*

Tietolähteen kelvollinen polku on joko *Tietueluettelo* tai *Säilö (tietue)*-tyyppi.

## <a name="return-values"></a>Palautusarvot

*Kontti (tietue)*

Tuloksena oleva tietueen arvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

> [!NOTE] 
> Tyhjä-tietue on tietue, jossa kaikissa kentissä on tyhjä arvo. Tyhjä arvo numeroilla **0** (nolla), merkkijonoilla tyhjä merkkijono jne.

## <a name="example"></a>Esimerkki

`EMPTYRECORD (SPLIT ("abc", 1))` palauttaa uuden tyhjän tietueen, jonka rakenne on sama kuin `SPLIT`-toiminnon palauttamalla luettelolla. Lisätietoja on kohdassa [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Lisäresurssit

[Tallennustoiminnot](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
