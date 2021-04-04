---
title: VALUEIN ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) VALUEIN-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 08/18/2020
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
ms.openlocfilehash: e5a0ac314a61abce610407550e65479cbf5a6b5b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565829"
---
# <a name="valuein-er-function"></a>VALUEIN ER -funktio

[!include [banner](../includes/banner.md)]

`VALUEIN`-funktio määrittää, vastaako määritetty syöte määritetyn luettelokohteen tiettyä arvoa. Se palauttaa *totuusarvon* arvon **TOSI**, jos määritetty syöte vastaa määritetyn lausekkeen suorittamisen tulosta vähintään yhdelle määritetyn luettelon tietueelle. Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**.

## <a name="syntax"></a>Syntaksi

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a>Argumentit

`input`: *Kenttä*

*Tietueluettelo*-tyypin tietolähteen kelvollinen polku. Tämän nimikkeen arvon vastaavuus määritetään.

`list`: *Tietueluettelo*

*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.

`list item expression`: *Totuusarvo*

Kelvollinen ehdollinen lauseke, joka joko osoittaa tai sisältää määritetyn luettelon yhden kentän, jota olisi käytettävä vastaavuuteen.

## <a name="return-values"></a>Palautusarvot

*Boolen arvo*

Tuloksena oleva *Totuusarvo*-arvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Yleensä `VALUEIN`-funktio muunnetaan **OR**-ehtojoukoksi. Jos **TAI**-ehtojen luettelo on suuri ja SQL-lausekkeen enimmäispituus voi ylittyä, harkitse [`VALUEINLARGE`](er-functions-logical-valueinlarge.md)-funktion käyttöä.

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

Joissakin tapauksissa se voidaan kääntää tietokannan SQL-lauseessa `EXISTS JOIN`-operaattoria käyttämällä.

## <a name="example-1"></a>Esimerkki 1

Mallikartoituksessa määrität *Laskettu kenttä*-tyypin **Luettelo**-tietolähteen. Tässä tietolähteessä on lauseke `SPLIT ("a,b,c", ",")`.

Jos tietolähde on kutsuttaessa määritetty `VALUEIN ("B", List, List.Value)`-lausekkeeksi, funktio palauttaa arvon **TOSI**. Tässä tapauksessa `VALUEIN`-funktio muunnetaan seuraavaksi ehtojoukoksi: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, jossa `("B" = "b")` on yhtä kuin **TOSI**.

Jos tietolähde on kutsuttaessa määritetty `VALUEIN ("B", List, LEFT(List.Value, 0))`-lausekkeeksi, funktio palauttaa arvon **EPÄTOSI**. Tässä tapauksessa `VALUEIN`-funktio muunnetaan seuraavaksi ehdoksi: `("B" = "")` ei ole yhtä kuin **TOSI**.

Kyseisen ehdon tekstin suurin merkkimäärä on 32 768 merkkiä. Älä tämän vuoksi luo tietolähteitä, jotka voivat ylittää suorituksen aikana tämän rajan. Jos raja ylitetään, sovellus pysähtyy ja annetaan poikkeus. Tämä tilanne voi esiintyä esimerkiksi silloin, jos tietolähteeksi on määritetty `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` ja **List1**- ja **List2**-luetteloissa on suuria määriä tietueita.

Joissakin tapauksissa `VALUEIN`-funktio muunnetaan tietokantalausekkeeksi `EXISTS JOIN` -operaattorin avulla. Näin tapahtuu, kun käytetään [`FILTER`](er-functions-list-filter.md)-funktiota ja seuraavat ehdot täyttyvät:

- **KYSY KYSELYÄ** -asetus on poistettu käytöstä siinä `VALUEIN`-funktion tietolähteessä, joka viittaa tietueluetteloon. Tässä tietolähteessä ei käytetä suorituksen aikana mitään lisäehtoja.
- Tietueluetteloon viittaavaan `VALUEIN`-funktion tietolähteeseen ei ole määritetty upotettuja lausekkeita.
- `VALUEIN`-funktion luettelokohde viittaa määritetyn tietolähteen kenttään eikä tämän tietolähteen lausekkeeseen tai menetelmään.

Harkitse tämän vaihtoehdon käyttöä [`WHERE`](er-functions-list-where.md)-funktion sijaan, joka on kuvattu aiemmin tässä esimerkissä.

## <a name="example-2"></a>Esimerkki 2

Määritä seuraavat tietolähteet omassa mallimäärityksessäsi:

- *Taulukon tietueet* -tyypin **Sisällä**-tietolähde. Tämä tietolähde viittaa Intrastat-tauluun.
- *Taulukon tietueet* -tyypin **Portti**-tietolähde. Tämä tietolähde viittaa IntrastatPort-tauluun.

Kun `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` -lausekkeena määritetty tietolähde kutsutaan, luodaan seuraava SQL-lauseke palauttamaan Intrastat-taulun suodatetut tietueet.

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

**dataAreaId**-kenttien lopullinen SQL-lauseke luodaan käyttämällä `IN`-operaattoria.

## <a name="example-3"></a>Esimerkki 3

Määritä seuraavat tietolähteet omassa mallimäärityksessäsi:

- *Laskettu kenttä* -tyypin **Le**-tietolähde. Tässä tietolähteessä on lauseke `SPLIT ("DEMF,GBSI,USMF", ",")`.
- *Taulukon tietueet* -tyypin **Sisällä**-tietolähde. Tämä tietolähde viittaa Intrastat-tauluun ja **Yritysten väliset** -vaihtoehto on otettu käyttöön.

Kun `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` -lausekkeena määritetty tietolähde kutsutaan, lopullinen SQL-lauseke sisältää seuraavan ehdon.

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a>Lisäresurssit

[Loogiset toiminnot](er-functions-category-logical.md)

[VALUEINLARGE-funktiot](er-functions-logical-valueinlarge.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]