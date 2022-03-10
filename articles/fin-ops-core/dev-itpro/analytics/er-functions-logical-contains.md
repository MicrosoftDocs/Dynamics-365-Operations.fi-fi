---
title: ER:n CONTAINS-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) CONTAINS-funktiota käytetään.
author: NickSelin
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: ae6c96b5754946ee971a8f47d4c618751d25f7e86fb9fb115861e97c5e6f536e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765143"
---
# <a name="contains-er-function"></a>ER:n CONTAINS-funktio

[!include [banner](../includes/banner.md)]

`CONTAINS`-funktio määrittää, sisältääkö määritetty syöte määritetyn tekstin. Se palauttaa *totuus*-arvon **TOSI**, jos määritetty syöte sisältää määritetyn tekstin. Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**.

## <a name="syntax"></a>Syntaksi

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a>Argumentit

`input`: *Merkkijono*

*Merkkijono*-tyypin tai merkkijonovakion tietolähteen kohteen kelvollinen polku, jonka arvo voi sisältää toisen argumentin.

`search text`: *Merkkijono*

*Merkkijono*-tietotyypin tai merkkijonovakion tietolähteen kelvollinen polku, jonka arvo voi sisältyä ensimmäiseen argumenttiin.

## <a name="return-values"></a>Palautusarvot

*Boolen arvo*

Tuloksena oleva *Totuusarvo*-arvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Tätä toimintoa voidaan käyttää [FILTER](er-functions-list-filter.md)-toiminnon ehtolausekkeen määrittämiseen vain, kun asianmukainen määritys on konfiguroitu [Regulatory Configuration Servicesissä](../../../finance/localizations/rcs-globalization-feature.md), jotta voidaan käyttää [Microsoft Dataversea](/power-platform/admin/data-integrator). Muussa tapauksessa tuotetaan poikkeus suunnittelun aikana. Vastaanotettu sanoma suosittelee [WHERE](er-functions-list-where.md)-funktion käyttöä `FILTER`-funktion asemesta suorituskyvyn parantamiseksi.

## <a name="example-1"></a>Esimerkki 1

Lauseke `CONTAINS ("abc", "d")` palauttaa arvon **EPÄTOSI** ja lauseke `CONTAINS ("abc", "C")` palauttaa arvon **TOSI**.

## <a name="example-2"></a>Esimerkki 2

Lauseke `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` palauttaa arvon **TOSI**, jos **malli**-tietolähteen **Address**-kentän arvo sisältäää merkkijonon **DEU**. Muussa tapauksessa se palauttaa **EPÄTOSI**-arvon.

## <a name="additional-resources"></a>Lisäresurssit

[Loogiset toiminnot](er-functions-category-logical.md)
