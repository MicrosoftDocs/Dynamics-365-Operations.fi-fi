---
title: VALUEINLARGE ER -funktio
description: Tässä ohjeaiheessa käsitellään sähköisen raportoinnin (ER) VALUEINLARGE-funktion käyttämistä.
author: NickSelin
ms.date: 08/17/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 57b2246631b31cce10d086da29e76b729059a64aa6a3c2d8cf864dd70085dbfd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725257"
---
# <a name="valueinlarge-er-function"></a>VALUEINLARGE ER -funktio

[!include [banner](../includes/banner.md)]

`VALUEINLARGE`-funktio määrittää, vastaako määritetty *Int64*- tai *Kokonaisluku*-tyyppi määritetyn luettelokohteen tiettyä arvoa. Funktio *totuusarvon* arvon **TOSI**, jos määritetty syöte vastaa määritetyn lausekkeen suorittamisen tulosta vähintään yhdelle määritetyn luettelon tietueelle. Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**. Lisätietoja erosta `VALUEIN`-funktioon on jäljempänä tässä ohjeaiheessa kohdassa [Käyttötiedote](#usage_note).

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