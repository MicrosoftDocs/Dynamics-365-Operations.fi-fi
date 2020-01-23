---
title: FA_BALANCE ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) FA_BALANCE-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 0907cb8cb4bc1e90b9fb59eccedb699a894b5cc9
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916013"
---
# <a name="FA_BALANCE">FA_BALANCE ER-funktio</a>

[!include [banner](../includes/banner.md)]

`FA_BALANCE`-funktio palauttaa *Säilö (tietue)*-arvon, joka koostuu määritetyn käyttöomaisuuserän, arvomallin koodin, raportointivuoden ja raportointipäivämäärän käyttöomaisuussaldon tiedoista.

## <a name="syntax"></a>Syntaksi

```
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
