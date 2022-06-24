---
title: FILTER ER-toiminto
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) FILTER-funktiota käytetään.
author: NickSelin
ms.date: 12/14/2021
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
ms.openlocfilehash: dfa4afdcfad8c1855a10e1fa37c36cc5b20682ef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884514"
---
# <a name="filter-er-function"></a>FILTER ER-toiminto

[!include [banner](../includes/banner.md)]

`FILTER` funktio palauttaa määritetyn luettelon *tietueluettelon* arvoksi sen jälkeen, kun kyselyä on muutettu niin, että se suodattaa määritetyn ehdon.

## <a name="syntax"></a>Syntaksi

```vb
FILTER (list, condition)
```

## <a name="arguments"></a>Argumentit

`list`: *Tietueluettelo*

*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.

`condition`: *Totuusarvo*

Kelvollinen ehtolauseke, jota käytetään määritetyn luettelon tietueiden suodattamiseen.

## <a name="return-values"></a>Palautusarvot

*Tietueluettelo*

Tuloksena oleva tietueluettelo.

## <a name="usage-notes"></a><a name="usage-notes"></a>Käyttöhuomautukset

Funktio eroaa [WHERE](er-functions-list-where.md)-funktiosta, koska määritettyä ehtoa käytetään tietokannan tasolla kaikkiin *Taulukkotietue*-tyypin elektronisen raportoinnin (ER) tietolähteisiin. Luettelo ja ehto voidaan määrittää tauluja ja suhteita käyttämällä.

Jos jompikumpi tai molemmat tälle toiminnolle määritetyt argumentit (`list` ja `condition`) eivät salli tämän pyynnön kääntyä suoraan SQL-puheluun, suunnitteluaikaan tulee poikkeus. Tämä poikkeus ilmoittaa käyttäjälle, että joko `list` tai `condition` ei voi käyttää tietokannan kyselyä.

> [!NOTE]
> `FILTER`-toiminnon toiminta eroaa `WHERE`-funktiosta, kun valintaehdot määritetään [`VALUEIN`](er-functions-logical-valuein.md)-toiminnon avulla.
> 
> - Jos `VALUEIN`-toimintoa käytetään `WHERE`-toiminnon käyttöalueessa ja `VALUEIN`-funktion toinen argumentti viittaa tietolähteeseen, joka ei palauta tietueita, `VALUEIN`-funktion palauttama *[False](er-formula-supported-data-types-primitive.md#boolean)*-totuusarvo otetaan huomioon. Lauseke `WHERE(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` ei siis palauta toimittajatietueita, jos **VendGroups**-tietolähde ei palauta toimittajaryhmätietueita.
> - Jos `VALUEIN`-toimintoa käytetään `FILTER`-toiminnon käyttöalueessa ja `VALUEIN`-funktion toinen argumentti viittaa tietolähteeseen, joka ei palauta tietueita, `VALUEIN`-funktion palauttama *[False](er-formula-supported-data-types-primitive.md#boolean)*-totuusarvo ohitetaan. Lauseke `FILTER(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` palauttaa siis kaikki toimittajatietueet **Vendors**-tietolähteestä, vaikka **VendGroups**-tietolähde ei palauta toimittajaryhmätietueita.

## <a name="example-1"></a>Esimerkki 1

Jos **Toimittaja** on määritetty VendTable-tauluun viittaavaksi ER-tietolähteeksi, lauseke `FILTER (Vendors, Vendors.VendGroup = "40")` palauttaa luettelon toimittajista, jotka kuuluvat vain toimittajaryhmään 40.

## <a name="example-2"></a>Esimerkki 2

Jos **Toimittaja** määritetään VendTable-tauluun viittaavaksi ER-tietolähteeksi ja ER-tietolähteeksi määritetty **parmVendorBankGroup** palauttaa *String*-tietotyypin arvon, `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` palauttaa luettelon vain niistä toimittajatileistä, jotka kuuluvat tiettyyn pankkiryhmään.

## <a name="example-3"></a>Esimerkki 3

Syötät *Lasketun kenttä*-tyypin **DS**-tietolähteen, ja se sisältää lausekkeen `SPLIT ("A,B,C", ",")`. Kirjoita sitten toinen lauseke `FILTER( DS, DS.Value = "B")`. Kun yrität tallentaa lausekkeen ER-kaavan suunnittelutoimintoon, seuraava poikkeus hylätään: "Vahvistusvirhe: suodatusfunktion luettelolauseke ei ole kyseltävä."

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
