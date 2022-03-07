---
title: GETENUMVALUEBYNAME ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) GETENUMVALUEBYNAME-funktiota käytetään.
author: NickSelin
ms.date: 09/23/2020
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
ms.openlocfilehash: 03759852e5ceb13b79b0df4592bdcef76eb0a82865725c00df40b9cc5f786240
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774434"
---
# <a name="getenumvaluebyname-er-function"></a>GETENUMVALUEBYNAME ER-funktio

[!include [banner](../includes/banner.md)]

`GETENUMVALUEBYNAME`-funktio etsii määritetystä luettelointitietolähteestä tiettyä *Enum*-arvoa käyttämällä *merkkijono*-arvona määritettyä luetteloinnin nimeä. Jos *Enum*-arvo löytyy, funktio palauttaa sen. Muussa tapauksessa funktio palauttaa **Null**-luettelointiarvon.

## <a name="syntax"></a>Syntaksi

```vb
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

## <a name="example-1"></a>Esimerkki 1

Seuraavassa kuvassa on tietomallin **ReportDirection**-luettelointi. Huomaa, että luettelointiarvoille on määritetty otsikot.

![Tieto mallin luetteloinnissa käytettävissä olevat arvot.](./media/ER-data-model-enumeration-values.PNG)

Seuraavassa kuvassa on nämä tiedot:

- **$Direction**-tietolähde määritetään ER-raportissa. Tämä tietolähde määritetään **ReportDirection**-mallin luetteloinnin perusteella.
- `$IsArrivals`-lauseke on suunniteltu käyttämään mallin luettelointiin perustuvaa **$Direction**-tietolähdettä tämän toiminnon parametrina.
- Tämän vertailulausekkeen arvo on **TOSI**.

![Esimerkki tietomallin luetteloinnista.](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a>Esimerkki 2

Funktioiden `GETENUMVALUEBYNAME` ja [`LISTOFFIELDS`](er-functions-list-listoffields.md) avulla voit tuettujen luettelointien arvoja ja otsikoita tekstiarvoina. (Tuettuja luettelointeja ovat sovellusluetteloinnit, tietomalliluetteloinnit ja muotoluetteloinnit.)

Seuraavassa kuvassa **TransType**-tietolähde lisätään mallin yhdistämismääritykseen. Tämä tietolähde viittaa **LedgerTransType**-sovellusluettelointiin.

![Mallin yhdistämismäärityksen tietolähde, joka viittaa sovellusluettelointiin.](./media/er-functions-text-getenumvaluebyname-example2-1.png)

Seuraavassa kuvassa on **TransTypeList**-tietolähde, joka määritetään mallin yhdistämismäärityksessä. Tämä tietolähde määritetään **TransType**-sovellusluetteloinnin perusteella. `LISTOFFIELDS`-funktion avulla palautetaan kaikki luettelointiarvot kenttiä sisältävien tietueiden luettelona. Näin jokaisen luettelointiarvon tiedot tulevat näkyviin.

> [!NOTE]
> **EnumValue**-kenttä määritetään **TransTypeList**-tietolähdettä varten käyttämällä lauseketta `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)`. Tämä kenttä palauttaa luettelointiarvon jokaiselle tämän luettelon tietueelle.

![Valitun luetteloinnin kaikki luettelointiarvot tietueluettelona palauttavan mallin yhdistämismäärityksen tietolähde.](./media/er-functions-text-getenumvaluebyname-example2-2.png)

Seuraavassa kuvassa on **VendTrans**-tietolähde, joka määritetään mallin yhdistämismäärityksessä. Tämä tietolähde palauttaa toimittajan tapahtumatietueita **VendTrans**-sovellustaulukosta. Kunkin tapahtuman kirjanpitotyyppi määräytyy **TransType**-kentän arvon mukaan.

> [!NOTE]
> **TransTypeTitle**-kenttä määritetään **VendTrans**-tietolähdettä varten käyttämällä lauseketta `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label`. Tämä kenttä palauttaa nykyisen tapahtuman luettelointiarvon otsikon tekstinä, jos tämä luettelointiarvo on käytettävissä. Muussa tapauksessa se palauttaa tyhjän merkkijonoarvon.
>
> **TransTypeTitle**-kenttä on sidottu sellaisen tietomallin **LedgerType**-kenttään, joka mahdollistaa näiden tietojen käytön kaikissa ER-muodoissa, joissa tätä tietomallia käytetään tietolähteenä.

![Toimittajatapahtumia palauttavan mallin yhdistämismäärityksen tietolähde.](./media/er-functions-text-getenumvaluebyname-example2-3.png)

Seuraavassa kuvassa näkyy, miten voit käyttää [tietolähteen virheenkorjausta](er-debug-data-sources.md) määritetyn mallin yhdistämismäärityksen testaamiseen.

![Määritetyn mallin yhdistämismärityksen testaaminen tietolähteen virheenkorjauksen avulla.](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

Tietomallin **LedgerType** näyttää tapahtumatyyppien otsikkoja odotetulla tavalla.

Jos aiot käyttää tätä menetelmää suureen määrään tapahtumatietoja, sinun on otettava huomioon suorituksen suorituskyky. Lisätietoja: [Sähköisen raportoinnin muotojen suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi](trace-execution-er-troubleshoot-perf.md).

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)

[Sähköisen raportoinnin muotojen suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi](trace-execution-er-troubleshoot-perf.md)

[LISTOFFIELDS ER-funktio](er-functions-list-listoffields.md)

[FIRSTORNULL ER-funktio](er-functions-list-firstornull.md)

[WHERE ER-funktio](er-functions-list-where.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]