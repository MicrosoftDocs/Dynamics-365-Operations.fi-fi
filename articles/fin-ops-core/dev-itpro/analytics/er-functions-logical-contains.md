---
title: ER:n CONTAINS-funktio
description: Tässä artikkelissa on tietoja siitä, miten sähköisen raportoinnin (ER) CONTAINS-funktiota käytetään.
author: kfend
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 0b2831f8aec4847279953ebcea583c9218d214a7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273125"
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
