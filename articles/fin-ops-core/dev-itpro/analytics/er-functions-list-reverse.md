---
title: REVERSE ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) REVERSE-funktiota käytetään.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 360878319bfa29395ae5deabec2e25e52d9e0fdc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284145"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
