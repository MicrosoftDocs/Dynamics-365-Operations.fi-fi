---
title: IF ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) IF-funktiota käytetään.
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
ms.openlocfilehash: a69675e3c743154e8119ba6c04da5897f23a8422
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565901"
---
# <a name="if-er-function"></a>IF ER -funktio

[!include [banner](../includes/banner.md)]

`IF`- funktio palauttaa ensimmäisen määritetyn arvon, jos määritetyt ehdot täyttyvät. Muussa tapauksessa se palauttaa toisen määritetyn arvon. Palautettava arvo voi olla minkä tahansa tuettujen tietotyyppien arvo.

## <a name="syntax"></a>Syntaksi

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a>Argumentit

`condition`: *Totuusarvo*

Kelvollinen ehdollinen lauseke, joka on testattava.

`first value`: *Jokin tuetuista tietotyypeistä*

Tulos, joka palautetaan, jos ehto täyttyy.

`second value`: *Jokin tuetuista tietotyypeistä*

Tulos, joka palautetaan, jos ehto ei täyty.

## <a name="return-values"></a>Palautusarvot

*Jokin tuetuista tietotyypeistä*

Minkä tahansa tuettujen tietotyyppien tulokseksi saatava arvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

`first value` ja `second value` -argumentit on määritettävä käyttämällä samaa tietotyyppiä. Poikkeus on heitetty suunnittelun aikana, jos määritettyjen arvojen tietotyypit eivät vastaa toisiaan.

Jos ensimmäinen arvo ja toinen arvo ovat *Säilön (tietueen)* tai *Tietueluettelon* tietotyypin arvoja, tuloksessa on vain kentät, jotka ovat molemmissa arvoissa.

## <a name="example"></a>Esimerkki

`IF (1=2, "condition is met", "condition is not met")` palauttaa merkkijonon **"ehto ei täyty"**.

## <a name="additional-resources"></a>Lisäresurssit

[Loogiset toiminnot](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]