---
title: LISTJOIN ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) LISTJOIN-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b5b82917e3083b5ffe4546a6a15fd14938383a
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249032"
---
# <a name=""></a><a name="LISTJOIN">LISTJOIN ER-funktio</a>

[!include [banner](../includes/banner.md)]

`LISTJOIN`-funktio palauttaa *Tietueluettelon* arvon, joka edustaa uutta liitettyä tietueluetteloa, joka luodaan määritetyistä argumenteista.

## <a name="syntax"></a>Syntaksi

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a>Argumentit

`list 1`: *Tietueluettelo*

Viittaus *Tietueluettelon* tietotyypin tietolähteeseen. Tämä argumentti on pakollinen.

`list N`: *Tietueluettelo*

Viittaus *Tietueluettelon* tietotyypin tietolähteeseen. Nämä lisäargumentit ovat valinnaisia.

## <a name="return-values"></a>Palautusarvot

*Tietueluettelo*

Tuloksena oleva tietueluettelo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Luodun luettelon rakenne sisältää vain kentät, jotka ovat läsnä jokaisessa argumentissa mainitun tietueluettelon rakenteessa.

## <a name="example"></a>Esimerkki

Syötät `Container`-tyypin **Tietue 1**:n tietolähteen. Tämä tietolähde sisältää seuraavat `Calculated field` -tyypin sisäkkäiset kentät:

- **Koodi**: Tässä kentässä on lauseke, joka palauttaa `String`-tyypin arvon.
- **Summa**: Tässä kentässä on lauseke, joka palauttaa `Real`-tyypin arvon.

Syötä sitten `Container`-tyypin **Tietue 2**:n tietolähde. Tämä tietolähde sisältää seuraavat `Calculated field` -tyypin sisäkkäiset kentät:

- **Summa**: Tässä kentässä on lauseke, joka palauttaa `Real`-tyypin arvon.
- **IsValid**: Tässä kentässä on lauseke, joka palauttaa `Boolean`-tyypin arvon.

Tässä tapauksessa lauseke `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` palauttaa uuden luettelon, joka sisältää kaksi tietuetta. Tämän luettelon rakenne koostuu `Real`-tyypistä, joka on yksittäisessä **Summa**-kentässä, koska tämä kenttä on ainoa kenttä, joka esitetään kutsutun funktion jokaisessa argumentissa.

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)
