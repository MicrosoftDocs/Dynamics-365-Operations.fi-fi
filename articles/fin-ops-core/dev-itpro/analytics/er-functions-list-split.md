---
title: SPLIT ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) SPLIT-funktiota käytetään.
author: kfend
ms.date: 04/01/2021
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
ms.openlocfilehash: e95ecaae46ee73899736b1d5729d7f9639fc6803
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274046"
---
# <a name="split-er-function"></a>SPLIT ER-funktio

[!include [banner](../includes/banner.md)]

`SPLIT`-funktio jakaa määritetyn syötemerkkijonon arvon alimerkkijonoiksi ja palauttaa tuloksen uudeksi *Tietueluettelon* arvoksi.

## <a name="syntax-1"></a>Syntaksi 1

```vb
SPLIT (input, length)
```

Tätä syntaksia käytetään jakamaan määritetty syötemerkkijono alimerkkijonoiksi, joilla on tietty pituus.

## <a name="syntax-2"></a>Syntaksi 2

```vb
SPLIT (input, delimiter)
```

Tätä syntaksia käytetään jakamaan määritetty syötemerkkijono alimerkkijonoiksi määritetyn erottimen perusteella.

## <a name="arguments"></a>Argumentit

`input`: *Merkkijono*

Jaettava teksti.

`length`: *Kokonaisluku*

Yksittäisen alimerkkijonon enimmäispituus.

`delimiter`: *Merkkijono*

Erotin, jota käytetään erottelemaan alimerkkijonoja.

## <a name="return-values"></a>Palautusarvot

*Tietueluettelo*

Tuloksena oleva tietueluettelo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Palautettavan luettelon tietuerakenne koostuu *Merkkijono*-tyypin **Arvo**-kentästä. Jokainen palautettavan luettelon tietue sisältää tämän kentän luotuja alimerkkijonoja.

Jos `delimiter`-argumentti on tyhjä, palautettu uusi luettelo koostuu yhdestä tietueesta, jolla on *merkkijono*-tyypin **Arvo**-kenttä. Tässä kentässä on syöteteksti.

Jos `input`-argumentti on tyhjä, palautettava uusi luettelo on tyhjä. Jos `input`- tai `delimiter`-argumentti on määrittämättä (tyhjäarvo), sovellus antaa poikkeuksen.

## <a name="example-1"></a>Esimerkki 1

`SPLIT ("abcd", 3)` palauttaa uuden luettelon, joka sisältää kaksi tietuetta, joilla on *Merkkijono*-tyypin **Arvo**-kenttä. Ensimmäisen tietueen **Arvo**-kenttä sisältää tekstin **abc** ja toisen tietueen **Arvo**-kenttä tekstin **d**.

## <a name="example-2"></a>Esimerkki 2

`SPLIT ("XAb aBy", "aB")` palauttaa uuden luettelon, joka sisältää kolme tietuetta, joilla on *Merkkijono*-tyypin **Arvo**-kenttä. Ensimmäisen tietueen **Arvo**-kentässä on teksti **X**, toisen tietueen **Arvo**-kentässä teksti **&nbsp;** ja kolmannen tietueen **Arvo**-kentässä teksti **y**. 

## <a name="example-3"></a>Esimerkki 3

[INDEX](er-functions-list-index.md)-toiminnolla voit käyttää määritetyn syötemerkkijonon yksittäisiä elementtejä. Jos syötät **laskettu kenttä**-tyyppin **MyList**-tietolähteen ja määrität sen `SPLIT("abc", 1)`-lausekkeelle `INDEX(MyList,2).Value`-lauseke palauttaa tekstiarvon **b**.

## <a name="example-4"></a>Esimerkki 4

[ERITTELE](er-functions-list-enumerate.md)-toiminto voi auttaa sinua myös käyttämään määritetyn syötemerkkijonon yksittäisiä elementtejä. Jos syötät ensin **Lasketun kentän** tyypin **MyList**-tietolähteen ja konfiguroit sen lausekkeelle `SPLIT("abc", 1)` ja syötät sitten **Lasketun kentän** tyypin **Valintalista**-tietolähteen ja konfiguroit sen lausekkeelle `ENUMERATE(MyList)`, `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value`-lauseke palauttaa tekstin **b**.

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
