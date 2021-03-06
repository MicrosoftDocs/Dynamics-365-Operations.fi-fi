---
title: WHERE ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) WHERE-funktiota käytetään.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: bdf5c658fda83399c7bcffeaaf07005164c53f8a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745494"
---
# <a name="where-er-function"></a>WHERE ER-funktio

[!include [banner](../includes/banner.md)]

`WHERE`-funktio palauttaa määritetyn luettelon *Tietueluettelon* arvoksi sen jälkeen, kun se on suodatettu määritettyjen ehtojen mukaan.

## <a name="syntax"></a>Syntaksi

```vb
WHERE (list, condition)
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

Funktio eroaa [FILTER](er-functions-list-filter.md)-funktiosta, koska määritettyä ehtoa käytetään muistissa oleviin kaikkiin *Tietueluettelo*-tyypin elektronisen raportoinnin (ER) tietolähteisiin.

Jos toiminnolle määritetyt argumentit (`list` ja `condition`) sallivat tämän pyynnön kääntyä suoraan SQL-puheluun, suunnitteluaikaan tulee varoitusviesti. Tämä sanoma ilmoittaa käyttäjälle, että suorituskykyä voidaan parantaa, jos [FILTER](er-functions-list-filter.md)-toimintoa käytetään `WHERE`-funktion asemesta.

## <a name="example-1"></a>Esimerkki 1

Jos **Toimittaja** on määritetty VendTable-tauluun viittaavaksi ER-tietolähteeksi, lauseke `WHERE (Vendors, Vendors.VendGroup = "40")` palauttaa luettelon toimittajista, jotka kuuluvat vain toimittajaryhmään 40.

## <a name="example-2"></a>Esimerkki 2

Jos syötät tietolähteen **DS** *laskettuun kenttätyyppiin* ja se sisältää lausekkeen `SPLIT ("A|B|C", "|")`, lauseke `WHERE( DS, DS.Value = "B")` palauttaa ainoastaan yhden tietueen luettelon, joka sisältää tekstiarvon **B** **Arvo**-kentässä.

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]