---
title: LISTJOIN ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) LISTJOIN-funktiota käytetään.
author: kfend
ms.date: 04/01/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: ec8a5985277de8036ec8ad51b947a8bab098a1c3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291201"
---
# <a name="listjoin-er-function"></a>LISTJOIN ER-funktio

[!include [banner](../includes/banner.md)]

`LISTJOIN`-funktio palauttaa *Tietueluettelon* arvon, joka edustaa uutta liitettyä tietueluetteloa, joka luodaan määritetyistä argumenteista.

## <a name="syntax"></a>Syntaksi

```vb
LISTJOIN (list 1 [, list 2, …, list N])
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

![ER-mallimäärityksen suunnittelun sivu.](./media/er-functions-list-listjoin-image1.gif)

Tässä tapauksessa lauseke `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` palauttaa uuden luettelon, joka sisältää kaksi tietuetta.

![Sähköisen raportoinnin mallivastaavuusmäärityksen suunnittelun sivu ja kaksi tietuetta.](./media/er-functions-list-listjoin-image2.gif)

Tämän luettelon rakenne koostuu `Real`-tyypistä, joka on yksittäisessä **Summa**-kentässä, koska tämä kenttä on ainoa kenttä, joka esitetään kutsutun funktion jokaisessa argumentissa.

![Sähköisen raportoinnin malliyhdistämismäärityksen suunnittelun sivun summakenttä.](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)

[Suoritettavan ER-muodon tietolähteiden vianmääritys tiedonkulun ja muunnoksen analysointia varten](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
