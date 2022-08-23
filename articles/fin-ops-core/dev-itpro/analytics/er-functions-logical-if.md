---
title: IF ER -funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) IF-funktiota käytetään.
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
ms.openlocfilehash: b674a6f3e86af3763a251cbdc7c30fb8c5ed0f55
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275546"
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
