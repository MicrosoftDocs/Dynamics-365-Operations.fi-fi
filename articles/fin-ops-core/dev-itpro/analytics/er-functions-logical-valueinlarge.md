---
title: VALUEINLARGE ER -funktio
description: Tässä artikkelissa käsitellään sähköisen raportoinnin (ER) VALUEINLARGE-funktion käyttämistä.
author: kfend
ms.date: 08/17/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 425dbce8f229acbb9c8d721c8f1a554989e0533c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288075"
---
# <a name="valueinlarge-er-function"></a>VALUEINLARGE ER -funktio

[!include [banner](../includes/banner.md)]

`VALUEINLARGE`-funktio määrittää, vastaako määritetty *Int64*- tai *Kokonaisluku*-tyyppi määritetyn luettelokohteen tiettyä arvoa. Funktio *totuusarvon* arvon **TOSI**, jos määritetty syöte vastaa määritetyn lausekkeen suorittamisen tulosta vähintään yhdelle määritetyn luettelon tietueelle. Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**. Lisätietoja erosta `VALUEIN`-funktioon on jäljempänä tässä artikkelissa kohdassa [Käyttötiedote](#usage_note).

## <a name="syntax"></a>Syntaksi

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a>Argumentit

`input`: *Kenttä*

*Tietueluettelo*-tyypin tietolähdenimikkeen kelvollinen polku. Tämän nimikkeen arvon vastaavuus määritetään.

`list`: *Tietueluettelo*

*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.

`list item expression`: *Lauseke*

Kelvollinen ehdollinen lauseke, joka joko osoittaa tai sisältää määritetyn luettelon yhden kentän, jota olisi käytettävä vastaavuuteen.

## <a name="return-values"></a>Palautusarvot

*Boolen arvo*

Tuloksena oleva *Totuusarvo*-arvo.

## <a name=""></a><a name="usage_note">Käyttöhuomautukset</a>

Kun määritetty syöte ilmaisee *Int64*- tai *Kokonaisluku*-tyyppisen tietolähdenimikkeen, suoraksi SQL-lausekkeeksi käännettävä kutsu, määritetty luettelo muunnetaan väliaikaiseksi SQL-taulukoksi ja vastaavuus suoritetaan tietokannassa suorittamalla yksi `EXISTS JOIN` -kysely. Muussa tapauksessa tämä funktio toimii kuten [`VALUEIN`](er-functions-logical-valuein.md)-funktio.

Kun määritetty syöte ilmaisee tietolähdenimikkeen, joka suunniteltiin muuna kuin *Int64*- ja *Kokonaisluku*-tyyppisenä nimikkeenä, suunnitteluvaiheessa tapahtuu virhe, joka ilmoittaa, että `VALUEINLARGE`-funktiota ei voi käytätä määritetyssä ER-lausekkeessa.

`VALUEINLARGE`-funktion lauseke suoritetaan ja suoritus koskee vähintään kahta väliaikaista taulukkoa, suorituspalveluvirhe tapahtuu.

## <a name="example"></a>Esimerkki

Määritä seuraavat tietolähteet omassa mallimäärityksessäsi:

- *Taulukon tietueet* -tyypin **Sisällä**-tietolähde.
    - Tämä tietolähde viittaa **Intrastat**-tauluun.
    - **Yritystenvälinen**-asetuksena on **Ei**.
- *Laskettu kenttä* -tyypin **InMemory**-tietolähde.
    - Tässä tietolähteessä on lauseke `WHERE (In, In.Port <> "")`.
- *Laskettu kenttä* -tyypin **InFiltered**-tietolähde.
    - Tässä tietolähteessä on lauseke `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.

Jos **InFiltered**-tietolähdettä kutsutaan **DEMF**-yrityskontekstissa, sovellustietokantaan luodaan uusi väliaikainen taulu, muistiluetteloon kerätyt tietueen tunnistuskoodit lisätään tähän tauluun ja seuraava SQL-lauseke luodaan palauttamaan **Intrastat**-taulun suodatetut tietueet.

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a>Lisäresurssit

[Loogiset toiminnot](er-functions-category-logical.md)

[VALUEIN-funktiot](er-functions-logical-valuein.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
