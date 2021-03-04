---
title: FILTER ER-toiminto
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) FILTER-funktiota käytetään.
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
ms.openlocfilehash: 55fa3d4ad4427e2a45f7c5fce679c50a91c40b6d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679435"
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

## <a name="usage-notes"></a>Käyttöhuomautukset

Funktio eroaa [WHERE](er-functions-list-where.md)-funktiosta, koska määritettyä ehtoa käytetään tietokannan tasolla kaikkiin *Taulukkotietue*-tyypin elektronisen raportoinnin (ER) tietolähteisiin. Luettelo ja ehto voidaan määrittää tauluja ja suhteita käyttämällä.

Jos jompikumpi tai molemmat tälle toiminnolle määritetyt argumentit (`list` ja `condition`) eivät salli tämän pyynnön kääntyä suoraan SQL-puheluun, suunnitteluaikaan tulee poikkeus. Tämä poikkeus ilmoittaa käyttäjälle, että joko `list` tai `condition` ei voi käyttää tietokannan kyselyä.

## <a name="example-1"></a>Esimerkki 1

Jos **Toimittaja** on määritetty VendTable-tauluun viittaavaksi ER-tietolähteeksi, lauseke `FILTER (Vendors, Vendors.VendGroup = "40")` palauttaa luettelon toimittajista, jotka kuuluvat vain toimittajaryhmään 40.

## <a name="example-2"></a>Esimerkki 2

Jos **Toimittaja** määritetään VendTable-tauluun viittaavaksi ER-tietolähteeksi ja ER-tietolähteeksi määritetty **parmVendorBankGroup** palauttaa *String*-tietotyypin arvon, `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` palauttaa luettelon vain niistä toimittajatileistä, jotka kuuluvat tiettyyn pankkiryhmään.

## <a name="example-3"></a>Esimerkki 3

Syötät *Lasketun kenttä*-tyypin **DS**-tietolähteen, ja se sisältää lausekkeen `SPLIT ("A,B,C", ",")`. Kirjoita sitten toinen lauseke `FILTER( DS, DS.Value = "B")`. Kun yrität tallentaa lausekkeen ER-kaavan suunnittelutoimintoon, seuraava poikkeus hylätään: "Vahvistusvirhe: suodatusfunktion luettelolauseke ei ole kyseltävä."

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]