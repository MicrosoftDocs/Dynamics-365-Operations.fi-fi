---
title: LIST ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) LIST-funktiota käytetään.
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
ms.openlocfilehash: 50cb8858301c030df07ad4af9fe2a9513f41fead
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750409"
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