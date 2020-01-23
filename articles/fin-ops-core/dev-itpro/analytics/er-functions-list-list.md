---
title: LIST ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) LIST-funktiota käytetään.
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
ms.openlocfilehash: 6848fe535a6a588eaf06f96e93f28db9ef304940
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917278"
---
# <a name="LIST">LIST ER -funktio</a>

[!include [banner](../includes/banner.md)]

`LIST`-funktio palauttaa *Tietueluettelon* arvon, joka sisältää uuden tietueluettelon, joka luodaan määritetyistä argumenteista.

## <a name="syntax"></a>Syntaksi

```
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