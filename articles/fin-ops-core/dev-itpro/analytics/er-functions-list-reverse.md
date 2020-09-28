---
title: REVERSE ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) REVERSE-funktiota käytetään.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab953136b7500665bdb13e6ff585e3b76896c9ee
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744982"
---
# <a name="reverse-er-function"></a>REVERSE ER-funktio

[!include [banner](../includes/banner.md)]

`REVERSE`-funktio palauttaa määritetyn luettelon *Tietueluettelon* arvoksi käänteisen lajittelujärjestyksen.

## <a name="syntax"></a>Syntaksi

```vb
REVERSE (list)
```

## <a name="arguments"></a>Argumentit

`list`: *Tietueluettelo*

*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.

## <a name="return-values"></a>Palautusarvot

*Tietueluettelo*

Tuloksena oleva tietueluettelo.

## <a name="example-1"></a>Esimerkki 1

Jos syötät *Lasketun kenttä*-tyypin **DS**-tietolähteen, ja se sisältää lausekkeen `SPLIT ("C|B|A", "|")`, lauseke `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` palauttaa tekstiarvon **C**.

## <a name="example-2"></a>Esimerkki 2

Jos **Toimittaja** on määritetty sähköisen raportoinnin (ER) tietolähteeksi, joka viittaa VendTable-tauluun, lauseke `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` palauttaa toimittajaluettelon, joka on lajiteltu nimen mukaan laskevassa järjestyksessä.

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)
