---
title: NUMERALSTOTEXT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NUMERALSTOTEXT-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: e4af3926998d128f8269ab9af46caeb8be896509
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680215"
---
# <a name="numeralstotext-er-function"></a>NUMERALSTOTEXT ER-funktio

[!include [banner](../includes/banner.md)]

`NUMERALSTOTEXT`-funktio palauttaa määritetyn numeron *Merkkijono*-arvona sen jälkeen, kun se on kirjoitettu (muunnetaan tekstimerkkijonoiksi) määritetyllä kielellä.

## <a name="syntax"></a>Syntaksi

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a>Argumentit

`number`: *Kokonaisluku* tai *Todellinen*

Numeerinen arvo, joka määrittää lukumäärän, joka täytyy tavata.

`language`: *Merkkijono*

*Merkkijono*-arvo, joka esittelee kielikoodin.

`currency`: *Merkkijono*

*Merkkijono*-arvo, joka esittelee valuuttakoodin.

`print currency name flag`: *Totuusarvo*

*Totuusarvo*, joka ilmaisee, onko kirjoitettuun tekstin lisättävä valuutan nimi.

`decimal points`: *Kokonaisluku*

*Kokonaislukuarvo*, joka ilmaisee, kuinka monta desimaalia kirjoitetussa tekstissä pitäisi olla.

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Kielikoodi on valinnainen. Jos se on määritetty tyhjänä merkkijonona, suorituskontekstin kielikoodia käytetään. Oletuskielikoodi on **FI-FI**. Käynnissä olevan kontekstin kielikoodi määritetään käynnissä olevan sähköisen raportoinnin (ER) **Kansiossa** tai **Tiedosto**-elementissä.

Valuuttakoodi on valinnainen. Jos se on määritetty tyhjänä merkkijonona, suorituskontekstin yrityksen valuuttaa käytetään.

> [!NOTE] 
> `print currency name flag` ja `decimal points`-argumentit analysoidaan vain seuraaville kielikoodeille: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** ja **RU**. Lisäksi `print currency name flag`-argumentti analysoidaan vain niissä yrityksissä, joiden maa- tai alueyhteys tukee valuutan nimen taivutusta.

## <a name="example-1"></a>Esimerkki 1

`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` palauttaa arvon **Tuhat kaksisataa kolmekymmentä neljä ja 56**.

## <a name="example-2"></a>Esimerkki 2

`NUMERALSTOTEXT (120, "PL", "", false, 0)`-funktio palauttaa arvon **Sto dwadzieścia**. 

## <a name="example-3"></a>Esimerkki 3

`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` palauttaa arvon **сто двадцать евро 21 евроцент**.

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)
