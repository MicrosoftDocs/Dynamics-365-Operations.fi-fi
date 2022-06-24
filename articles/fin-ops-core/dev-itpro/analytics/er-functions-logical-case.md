---
title: CASE ER -funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) CASE-funktiota käytetään.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: f8ce598315bfbf291fafc6c9c9d54133486fb352
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854753"
---
# <a name="case-er-function"></a>CASE ER -funktio

[!include [banner](../includes/banner.md)]

`CASE`-funktio arvioi määritetyn lausekkeen arvon määritettyjen vaihtoehtoisten asetusten mukaan ja palauttaa ensimmäisen vaihtoehdon tuloksen, joka on yhtä suuri kuin määritetyn lausekkeen arvo. Muussa tapauksessa se palauttaa valinnaisen oletustuloksen, jos oletustulos määritetään kutsutussa funktiossa viimeisenä argumenttina, jota ei edellä vaihtoehto. Palautettava arvo voi olla minkä tahansa tuettujen tietotyyppien arvo.

## <a name="syntax"></a>Syntaksi

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a>Argumentit

`expression`: *Primitiivinen tietotyyppi* (totuusarvo, numeerinen tai teksti)

Kelvollinen lauseke, joka palauttaa primitiivisen tietotyypin arvon.

`option 1`: *Primitiivinen tietotyyppi* (totuusarvo, numeerinen tai teksti)

Kelvollinen lauseke, joka palauttaa saman primitiivisen tietotyypin arvon kutsutun funktion `expression`-argumentiksi. Tämä argumentti on pakollinen.

`result 1`: *Jokin tuetuista tietotyypeistä*

Edellistä vaihtoehtoa vastaava palautettu tulos. Tämä argumentti on pakollinen.

`option N`: *Primitiivinen tietotyyppi* (totuusarvo, numeerinen tai teksti)

Kelvollinen lauseke, joka palauttaa saman primitiivisen tietotyypin arvon kutsutun funktion `expression`-argumentiksi. Tämä argumentti on valinnainen.

`result N`: *Jokin tuetuista tietotyypeistä*

Edellistä vaihtoehtoa vastaava palautettu tulos. Tämä argumentti on valinnainen.

`default result`: *Jokin tuetuista tietotyypeistä*

Tulos, joka tulisi palauttaa, jos vastaavuutta ei ole. Tämä argumentti on valinnainen.

## <a name="return-values"></a>Palautusarvot

*Jokin tuetuista tietotyypeistä*

Minkä tahansa tuettujen tietotyyppien tulokseksi saatava arvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Poikkeus on heitetty suorituksen aikana, jos vastaavuutta ei ole ja valinnaista oletustulosta ei ole määritetty.

Kaikki tulokset on määritettävä käyttämällä samaa tietotyyppiä. Poikkeus on heitetty suunnittelun aikana, jos määritettyjen tulosten tietotyypit eivät vastaa toisiaan.

Jos ensimmäinen tulosarvo ja *N*:s arvo ovat *Säilön (tietueen)* tai *Tietueluettelon* tietotyypin arvoja, tuloksessa on vain kentät, jotka ovat molemmissa arvoissa.

## <a name="example"></a>Esimerkki

`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` palauttaa merkkijonon **TALVI**, jos nykyinen sovellusistunnon päivämäärä on loka-joulukuun välissä. Muussa tapauksessa se palauttaa tyhjän merkkijonon.

## <a name="additional-resources"></a>Lisäresurssit

[Loogiset toiminnot](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]