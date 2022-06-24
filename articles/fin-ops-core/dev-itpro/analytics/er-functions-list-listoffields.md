---
title: LISTOFFIELDS ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) LISTOFFIELDS-funktiota käytetään.
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
ms.openlocfilehash: c36630280ed351048022bafd4c6f634afd1b1319
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877093"
---
# <a name="listoffields-er-function"></a>LISTOFFIELDS ER-funktio

[!include [banner](../includes/banner.md)]

`LISTOFFIELDS`-funktio palauttaa *Tietueluettelon* arvon, joka luodaan *luettelointi*- tai *säilö (tietue)* -tyypin määritetyn argumentin rakenteen perusteella.

## <a name="syntax-1"></a>Syntaksi 1

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a>Syntaksi 2

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a>Argumentit

`path`: Tietolähdeviite

Tieto lähteen kelvollinen viitepolku, joka on jokin seuraavista tietotyypeistä:

- Mallin luettelointi
- Muodon luettelointi
- Sovellusten luettelointi
- Kontti (tietue)

`language`: *Merkkijono*

Kielikoodia edustava teksti.

## <a name="return-values"></a>Palautusarvot

*Tietueluettelo*

Tuloksena oleva tietueluettelo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Luotu luettelo koostuu tietueista, jossa on seuraavat kentät:

- **Nimi** (*Merkkijono* tietotyyppi)
- **Otsikko** (*Merkkijono* tietotyyppi)
- **Kuvaus** (*Merkkijono* tietotyyppi)
- **IsTranslated** (*Totuusarvo* tietotyyppi)

Jos `path`-argumentti viittaa *säilön (tietue)* -tyypin tietolähteeseen viitatun säilötietueen jokaiseen kenttään, luotavaan luetteloon lisätään uusi tietue. Jokaisen luodun tietueen **Nimi**-kenttä palauttaa viitatun säilötietueen kentän nimen, jolle nykyinen tietue luotiin.

Jos `path`-argumentti viittaa johonkin *luettelointi*-tyyppiin, jokaiselle viitatun luettelon arvolle lisätään uusi luettelo luotavaan luetteloon. Jokaisen luodun tietueen **Nimi**-kenttä palauttaa viitatun luetteloinnin arvon, jolle nykyinen tietue luotiin, **Kuvaus**-kenttä palauttaa kyseisen luetteloinnin kuvauksen ja **Selite**-kenttä palauttaa kyseisen luetteloinnin otsikon.

Suorituksen aikana, kun käytetään syntaksia 1, **Selite**- ja **Kuvaus**-kenttien on palautettava arvot, jotka perustuvat käynnissä olevan sähköisen raportoinnin (ER) muodon kieliasetuksiin:

- Jos pyydetyn kielen otsikot ja kuvaukset ovat saatavilla, **Otsikko**- ja **Kuvaus** -kentät palauttavat kyseiseen kieleen perustuvat arvot, ja **IsTranslated**-kenttä palauttaa arvon **Tosi**.
- Jos pyydetyn kielen otsikot ja kuvaukset eivät ole saatavilla, **Otsikko**- ja **Kuvaus** -kentät palauttavat oletuksena olevaan kieleen **EN-US** perustuvat arvot, ja **IsTranslated**-kenttä palauttaa arvon **Epätosi**.

Suorituksen aikana, kun käytetään syntaksia 2, **Selite**- ja **Kuvaus**-kenttien on palautettava arvot, jotka perustuvat kieleen, joka määritetään kutsutun funktion toisena argumenttina:

- Jos pyydetyn kielen otsikot ja kuvaukset ovat saatavilla, **Otsikko**- ja **Kuvaus** -kentät palauttavat kyseiseen kieleen perustuvat arvot, ja **IsTranslated**-kenttä palauttaa arvon **Tosi**.
- Jos pyydetyn kielen otsikot ja kuvaukset eivät ole saatavilla, **Otsikko**- ja **Kuvaus** -kentät palauttavat kieleen **EN-US** perustuvat arvot, ja **IsTranslated**-kenttä palauttaa arvon **Epätosi**.

## <a name="example-1"></a>Esimerkki 1

Seuraavassa kuvan on ER-tietomallin luettelointi.

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

Seuraavassa kuvassa on nämä tiedot:

- Mallin luettelointi lisätään raporttiin tietolähteenä.
- ER-lauseke käyttää mallin luettelointia `LISTOFFIELDS`-funktion parametrina.
- *Tietueluettelon* tyypin tietolähde lisätään raporttiin luodun ER-lausekkeen avulla.

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

Seuraavassa esimerkissä on ER-lomakkeen elementit, jotka on sidottu `LISTOFFIELDS`-funktiolla luotuun *Tietueluettelo*-tyypin tietolähteeseen.

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

Seuraavassa kuvassa on tulos, kun suunniteltu muoto suoritetaan.

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> Selitteiden ja kuvausten käännetty teksti annetaan ER-lomakkeeseen **FILE**- ja **FOLDER**-päälomake-elementeille määritettyjen kieliasetusten perusteella

## <a name="example-2"></a>Esimerkki 2

Voit esimerkiksi määrittää *Laskettu kenttä*-tietolähdetyypin määrittämään **enumType\_de**- ja **enumType\_deCH**-tietolähteet **enumType**-tietomallin luettelointia varten:

- **enumType\_de** = `LISTOFFIELDS (enumType, "de")`
- **enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`

Voit hakea tässä tapauksessa otsikon sveitsinsaksan luettelointiarvon, jos tämä käännös on käytettävissä, käyttämällä seuraavaa lauseketta. Jos sveitsinsaksan käännös ei ole käytettävissä, otsikko on saksankielinen.

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]