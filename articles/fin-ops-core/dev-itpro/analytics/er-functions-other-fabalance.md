---
title: FA_BALANCE ER-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) FA_BALANCE-funktiota käytetään.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: f9bb52643b60fd1b9423d798c08d731565c70f81
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285242"
---
# <a name="fa_balance-er-function"></a>FA_BALANCE ER-funktio

[!include [banner](../includes/banner.md)]

`FA_BALANCE`-funktio palauttaa *Säilö (tietue)*-arvon, joka koostuu määritetyn käyttöomaisuuserän, arvomallin koodin, raportointivuoden ja raportointipäivämäärän käyttöomaisuussaldon tiedoista.

## <a name="syntax"></a>Syntaksi

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a>Argumentit

`fixed asset code`: *Merkkijono*

*Merkkijono*-arvo, joka edustaa sen käyttöomaisuuserän koodia, jolle saldo on laskettu.

`value model code`: *Merkkijono*

*Merkkijono*-arvo, joka edustaa sen arvomallin koodia, jolle saldo on laskettu.

`reporting year`: *Luettelointiarvo*

**AssetYear**-sovelluksen luetteloinnin luettelointiarvo, joka määrittää saldon laskennan kauden.

`reporting date`: *Päivämäärä*

*Päivämäärä*-arvo, joka määrittää saldon laskennan päivämäärän.

## <a name="return-values"></a>Palautusarvot

*Kontti (tietue)*

Tuloksena oleva tietueen arvo.

## <a name="example"></a>Esimerkki

`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` palauttaa käyttöomaisuuden **COMP-000001**-saldojen valmistellun tietosäilön, jonka arvomalli on **Current** kyseisenä sovellusistunnon päivämääränä.

## <a name="additional-resources"></a>Lisäresurssit

[Muut (liiketoiminnan toimialuekohtaiset) toiminnot](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
