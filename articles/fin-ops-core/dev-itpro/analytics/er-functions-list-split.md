---
title: SPLIT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) SPLIT-funktiota käytetään.
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
ms.openlocfilehash: e1f11d68b697fdd363f429e60a79f1e1f97bab5b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686389"
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

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]