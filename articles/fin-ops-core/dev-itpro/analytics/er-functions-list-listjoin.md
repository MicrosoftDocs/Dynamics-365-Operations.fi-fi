---
title: LISTJOIN ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) LISTJOIN-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6713823d8d089a677c39bc2a8b5cfe1d1b23b459
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563773"
---
# <a name="listjoin-er-function"></a>LISTJOIN ER-funktio

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

![ER-mallimäärityksen suunnittelun sivu](./media/er-functions-list-listjoin-image1.gif)

Tässä tapauksessa lauseke `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` palauttaa uuden luettelon, joka sisältää kaksi tietuetta.

![Sähköisen raportoinnin mallivastaavuusmäärityksen suunnittelun sivu ja kaksi tietuetta](./media/er-functions-list-listjoin-image2.gif)

Tämän luettelon rakenne koostuu `Real`-tyypistä, joka on yksittäisessä **Summa**-kentässä, koska tämä kenttä on ainoa kenttä, joka esitetään kutsutun funktion jokaisessa argumentissa.

![Sähköisen raportoinnin malliyhdistämismäärityksen suunnittelun sivun summakenttä](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)

[Suoritettavan ER-muodon tietolähteiden vianmääritys tiedonkulun ja muunnoksen analysointia varten](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]