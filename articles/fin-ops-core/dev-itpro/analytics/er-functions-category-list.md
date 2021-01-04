---
title: Luettelo ER-funktioista luetteloluokassa
description: Tässä ohjeaiheessa on tietoja sähköisen raportoinnin (ER) tukemista luettelofunktioista.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
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
ms.openlocfilehash: e2e708c59bceebf845ee78c98057133bb2892cf9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686170"
---
# <a name="list-of-er-functions-in-the-list-category"></a>Luettelo ER-funktioista luetteloluokassa

[!include [banner](../includes/banner.md)]

Sähköisen raportoinnin (ER) luettelofunktioiden avulla voidaan poimia tietoja *Tietueluettelosta* ja *Säilö (tietue)* -tietotyypin tietolähteistä ja suorittaa niitä. Tässä aiheessa on yhteenveto näistä funktioista.

## <a name="list-of-supported-functions"></a>Luettelo tuetuista toiminnoista

| Toiminto | Kuvaus |
|----------|-------------|
| [AllItems](er-functions-list-allitems.md)                 | Tämä toiminto suoritetaan muistin sisäisenä valintana. Se palauttaa uuden litistetyn *Tietueluettelo*-arvon, joka sisältää luettelon kaikista kohteista, jotka vastaavat määritettyä polkua. |
| [AllItemsQuery](er-functions-list-allitemsquery.md)       | Tämä toiminto suoritetaan liitettynä SQL-kyselynä. Se palauttaa uuden litistetyn *Tietueluettelo*-arvon, joka sisältää luettelon kaikista kohteista, jotka vastaavat määritettyä polkua. |
| [Lukumäärä](er-functions-list-count.md)                       | Tämä funktio palauttaa *kokonaislukuarvon*, joka vastaa määritetyn luettelon tietueiden määrää, jos luettelo ei ole tyhjä. Jos luettelo on tyhjä, funktio palauttaa arvon **0** (nolla). |
| [EmptyList](er-functions-list-emptylist.md)               | Tämä funktio palauttaa tyhjän *Tietueluettelon* arvon käyttämällä määritettyä luetteloa luettelorakenteen lähteenä.|
| [Valintalista](er-functions-list-enumerate.md)               | Tämä funktio palauttaa uuden *Tietueluettelon* arvon, joka koostuu määritetyn luettelon valintalistan tietueista. |
| [Suodatus](er-functions-list-filter.md)                     | Tämä funktio palauttaa määritetyn luettelon *tietueluettelon* arvoksi sen jälkeen, kun kyselyä on muutettu niin, että se suodattaa määritetyn ehdon. |
| [Ensimmäinen](er-functions-list-first.md)                       | Tämä funktio palauttaa ensimmäisen tietueen, joka on määritetty *Säilön (tietueen)* arvona, jos luettelo ei ole tyhjä. Jos luettelo on tyhjä, funktio heittää poikkeuksen. |
| [FirstOrNull](er-functions-list-firstornull.md)           | Tämä funktio palauttaa ensimmäisen tietueen, joka on määritetty *Säilön (tietueen)* arvona, jos tietue ei ole tyhjä. Jos tietue on tyhjä, funktio palauttaa Null *Säilö (tietue)*-arvon. |
| [Index](er-functions-list-index.md)                       | Tämä funktio palauttaa *Säilö (tietue)*-arvon, joka on valittu määritetyn numeroindeksin avulla määritetyssä luettelossa. Jos hakemisto on määritellyn luettelon tietueiden ulkopuolella, tämä toiminto antaa poikkeuksen. |
| [IsEmpty](er-functions-list-isempty.md)                   | Tämä funktio palauttaa *totuusarvon* **TOSI**, jos määritetty luettelo ei sisällä tietueita. Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**. |
| [Luettelo](er-functions-list-list.md)                         | Tämä funktio palauttaa *Tietueluettelon* arvon, joka sisältää uuden luettelon, joka luodaan määritetyistä argumenteista.|
| [ListDistinct](er-functions-list-listdistinct.md)         | Tämä funktio laskee määritetyn lausekkeen valitun luettelon jokaisen tietueen valitsimena. Se palauttaa uuden *tietueluettelon* arvon, joka sisältää yhden tietueen kutakin yksilöllistä valitsinarvoa kohden.|
| [ListJoin](er-functions-list-listjoin.md)                 | Tämä funktio palauttaa *Tietueluettelon* arvon, joka edustaa uutta liitettyä luetteloa, joka luodaan määritetyistä argumenteista.|
| [ListOfFields](er-functions-list-listoffields.md)         | Tämä funktio palauttaa *Tietueluettelon* arvon, joka luodaan *luettelointi*- tai *säilö (tietue)* -tyypin määritetyn argumentin rakenteen perusteella. |
| [ListOfFirstItem](er-functions-list-listoffirstitem.md)   | Tämä funktio palauttaa uuden *Tietueluettelon* arvon, joka koostuu vain määritetyn luettelon ensimmäisestä tietueesta.|
| [OrderBy](er-functions-list-orderby.md)                   | Tämä funktio palauttaa määritetyn luettelon *Tietueluettelon* arvoksi sen jälkeen, kun se on lajiteltu määritettyjen argumenttien mukaan. Nämä argumentit voivaan määrittää lausekkeina. |
| [Käänteinen](er-functions-list-reverse.md)                   | Tämä funktio palauttaa määritetyn luettelon *Tietueluettelon* arvoksi käänteisen lajittelujärjestyksen. |
| [Jako](er-functions-list-split.md)                       | Tämä funktio jakaa määritetyn syötemerkkijonon arvon alimerkkijonoiksi ja palauttaa tuloksen uudeksi *Tietueluettelon* arvoksi. |
| [SplitList](er-functions-list-splitlist.md)               | Tämä funktio jakaa määritetyn luettelon aliluetteloiksi (tai eriksi), joissa on tietty määrä tietueita. Sitten se palauttaa tuloksen uutena *Tietueluettelon* arvona, joka koostuu eristä. |
| [SplitListByLimit](er-functions-list-splitlistbylimit.md) | Tämä funktio jakaa määritetyn luettelon uuteen aliluetteloon (erät). Kunkin erän tietueiden määrä lasketaan dynaamisesti. Sitten funktio palauttaa tuloksen uutena *Tietueluettelon* arvona, joka koostuu eristä. |
| [StringJoin](er-functions-list-stringjoin.md)             | Tämä funktio palauttaa määritetystä luettelosta *merkkijonon*, joka koostuu määritetyn kentän ketjutetuista arvoista tietystä luettelosta. Arvot voidaan erottaa määritetyllä erottimella. |
| [Missä](er-functions-list-where.md)                       | Tämä funktio palauttaa määritetyn luettelon *Tietueluettelon* arvoksi sen jälkeen, kun se on suodatettu määritettyjen ehtojen mukaan. |

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Sähköisen raportoinnin kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)

[Sähköisen raportoinnin kaavakieli](er-formula-language.md)
