---
title: EMPTYRECORD ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) EMPTYRECORD-funktiota käytetään.
author: NickSelin
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
ms.openlocfilehash: e614c06b4cfad628bbd8a966719ed994ce05b792
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746528"
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