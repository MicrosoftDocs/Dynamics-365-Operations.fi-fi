---
title: ORDERBY ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ORDERBY-funktiota käytetään.
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
ms.openlocfilehash: 51da7f3766f5af901c8be6668bc2511cd8e2f9e9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753189"
---
# <a name="orderby-er-function"></a>ORDERBY ER-funktio

[!include [banner](../includes/banner.md)]

`ORDERBY`-funktio palauttaa määritetyn luettelon *Tietueluettelon* arvoksi sen jälkeen, kun se on lajiteltu määritettyjen argumenttien mukaan. Nämä argumentit voivaan määrittää lausekkeina.

## <a name="syntax"></a>Syntaksi

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a>Argumentit

`list`: *Tietueluettelo*

*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.

`expression 1`: *Kenttä*

Tietolähteen kentän kelvollinen polku, johon kutsutun funktion `list`-argumentti viittaa. Viitatun kentän on oltava primitiivisen tietotyypin kenttä. Tämä argumentti on pakollinen.

`expression N`: *Kenttä*

Tietolähteen kentän kelvollinen polku, johon kutsutun funktion `list`-argumentti viittaa. Viitatun kentän on oltava primitiivisen tietotyypin kenttä. Nämä lisäargumentit ovat valinnaisia.

## <a name="return-values"></a>Palautusarvot

*Tietueluettelo*

Tuloksena oleva tietueluettelo.

## <a name="example-1"></a>Esimerkki 1

Jos syötät *Lasketun kenttä*-tyypin **DS**-tietolähteen, ja se sisältää lausekkeen `SPLIT ("C|B|A", "|")`, lauseke `FIRST( ORDERBY( DS, DS. Value)).Value` palauttaa tekstiarvon **A**.

## <a name="example-2"></a>Esimerkki 2

Jos **Toimittaja** on määritetty sähköisen raportoinnin (ER) tietolähteeksi, joka viittaa VendTable-tauluun, lauseke `ORDERBY (Vendors, Vendors.'name()')` palauttaa toimittajaluettelon, joka on lajiteltu nimen mukaan nousevassa järjestyksessä.

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]