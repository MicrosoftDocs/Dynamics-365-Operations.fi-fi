---
title: GETENUMVALUEBYNAME ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) GETENUMVALUEBYNAME-funktiota käytetään.
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
ms.openlocfilehash: 4ded0c62b4556b21e731cd9b98db2863ec6ec442
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916841"
---
# <a name="GETENUMVALUEBYNAME">GETENUMVALUEBYNAME ER-funktio</a>

[!include [banner](../includes/banner.md)]

`GETENUMVALUEBYNAME`-funktio etsii määritetystä luettelointitietolähteestä tiettyä *Enum*-arvoa käyttämällä *merkkijono*-arvona määritettyä luetteloinnin nimeä. Jos *Enum*-arvo löytyy, funktio palauttaa sen. Muussa tapauksessa funktio palauttaa **Null**-luettelointiarvon.

## <a name="syntax"></a>Syntaksi

```
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>Argumentit

`enumeration data source path`: *Luettelointi*

Tieto lähteen kelvollinen polku, joka on jokin seuraavista luettelointityypeistä:

- Sähköisen raportointimallin (ER) numerointi
- ER-muodon numerointi
- Microsoft Dynamics 365 Financen numerointi

`enumeration value text`: *Merkkijono*

Merkkijonoarvo, joka edustaa yksittäisen luettelointiarvon nimeä.

## <a name="return-values"></a>Palautusarvot

Tyhjäarvot salliva *Enum*

Tulokseksi saatava luettelointiarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Poikkeusta ei heitetä, jos *Enum*-arvoa ei löydy *merkkijono*-arvona määritetyn luettelointiarvon nimen avulla.

## <a name="example"></a>Esimerkki

Seuraavassa kuvassa on tietomallin **ReportDirection**-luettelointi. Huomaa, että luettelointiarvoille on määritetty otsikot.

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Seuraavassa kuvassa on nämä tiedot:

- **$Direction**-tietolähde määritetään ER-raportissa. Tämä tietolähde määritetään **ReportDirection**-mallin luetteloinnin perusteella.
- `$IsArrivals`-lauseke on suunniteltu käyttämään mallin luettelointiin perustuvaa **$Direction**-tietolähdettä tämän toiminnon parametrina.
- Tämän vertailulausekkeen arvo on **TOSI**.

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)
