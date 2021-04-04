---
title: FA_SUM ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) FA_SUM-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: c31722537e2a6bae502800953939ca01da4527b9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567565"
---
# <a name="fa_sum-er-function"></a>FA_SUM ER -funktio

[!include [banner](../includes/banner.md)]

`FA_SUM`-funktio palauttaa *Säilö (tietue)*-arvon, joka koostuu tietyn käyttöomaisuushyödykkeen kiinteän omaisuuden määrien tiedoista, arvomallikoodista ja päivämääräajanjaksosta.

## <a name="syntax"></a>Syntaksi

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a>Argumentit

`fixed asset code`: *Merkkijono*

*Merkkijono*-arvo, joka edustaa sen käyttöomaisuuserän koodia, jolle saldo on laskettu.

`value model code`: *Merkkijono*

*Merkkijono*-arvo, joka edustaa sen arvomallin koodia, jolle saldo on laskettu.

`start date`: *Päivämäärä*

*Päivämäärä*, joka ilmaisee alkamispäivämäärän kauden, jolle käyttöomaisuuserien summat lasketaan.

`end date`: *Päivämäärä*

*Päivämäärä*, joka ilmaisee loppumispäivämäärän kauden, jolle käyttöomaisuuserien summat lasketaan.

## <a name="return-values"></a>Palautusarvot

*Kontti (tietue)*

Tuloksena oleva tietueen arvo.

## <a name="example"></a>Esimerkki

`FA_SUM ("COMP-000001", "Current", Date1, Date2)` palauttaa käyttöomaisuuden **COMP-000001**-tieto säilön, joka on laadittu **nykyiselle** arvomallille ja ajanjaksolta **päivämäärä1** **päivämäärä2**.

## <a name="additional-resources"></a>Lisäresurssit

[Muut (liiketoiminnan toimialuekohtaiset) toiminnot](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]