---
title: LIST ER -funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) LIST-funktiota käytetään.
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
ms.openlocfilehash: 7a5f27baa248ec84c75725cf32a1f482841424c2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277629"
---
# <a name="list-er-function"></a>LIST ER -funktio

[!include [banner](../includes/banner.md)]

`LIST`-funktio palauttaa *Tietueluettelon* arvon, joka sisältää uuden tietueluettelon, joka luodaan määritetyistä argumenteista.

## <a name="syntax"></a>Syntaksi

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a>Argumentit

`record 1`: *Kontti (tietue)*

Viittaus *Tietueen* tietotyypin tietolähteeseen. Tämä argumentti on pakollinen.

`record N`: *Kontti (tietue)*

Viittaus *Tietueen* tietotyypin tietolähteeseen. Nämä lisäargumentit ovat valinnaisia.

## <a name="return-values"></a>Palautusarvot

*Tietueluettelo*

Tuloksena oleva tietueluettelo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Luodun luettelon rakenne sisältää vain kentät, jotka on esitetty jokaisessa argumentissa mainitun tietueen rakenteessa.

## <a name="example"></a>Esimerkki

Syötät *Säilö*-tyypin **Tietueen 1**:n tietolähteen. Tämä tietolähde sisältää seuraavat *Lasketun kentän* tyypin sisäkkäiset kentät:

- **Koodi:** Tässä kentässä on lauseke, joka palauttaa *merkkijono*-tyypin arvon.
- **Määrä:** Tässä kentässä on lauseke, joka palauttaa *Todellisen* tyypin arvon.

Syötät sitten *Säilö*-tyypin **Tietueen 2**:n tietolähteen. Tämä tietolähde sisältää seuraavat *Lasketun kentän* tyypin sisäkkäiset kentät:

- **Määrä:** Tässä kentässä on lauseke, joka palauttaa *Todellisen* tyypin arvon.
- **IsValid:** Tässä kentässä on lauseke, joka palauttaa *Totuusarvon* tyypin arvon.

Tässä tapauksessa lauseke `LIST('Record 1', 'Record 2')` palauttaa uuden luettelon, joka sisältää kaksi tietuetta. Tämän luettelon rakenne koostuu *todellisesta* tyypistä, joka on yksittäisessä **summa**-kentässä, koska tämä kenttä on ainoa kenttä, joka esitetään kutsutun funktion jokaisessa argumentissa.

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
