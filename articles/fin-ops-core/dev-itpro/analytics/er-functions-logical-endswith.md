---
title: ER:n ENDSWITH-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ENDSWITH-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 2470bd8c75cf690d701957c4c79009659d61f7a5
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557514"
---
# <a name="endswith-er-function"></a>ER:n ENDSWITH-funktio

[!include [banner](../includes/banner.md)]

`ENDSWITH`-funktio määrittää, loppuuko määritetty syöte määritettyyn tekstiin. Se palauttaa *totuus*-arvon **TOSI**, jos määritetty syöte loppuu määritetyllä tekstillä. Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**.

## <a name="syntax"></a>Syntaksi

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a>Argumentit

`input`: *Merkkijono*

*Merkkijono*-tyypin tai merkkijonovakion tietolähteen kohteen kelvollinen polku, jonka arvo voi päättyä toiseen argumenttiin.

`start text`: *Merkkijono*

*Merkkijono*-tietotyypin tai merkkijonovakion tietolähteen kelvollinen polku, jonka arvo voi olla ensimmäisen argumentin lopussa.

## <a name="return-values"></a>Palautusarvot

*Boolen arvo*

Tuloksena oleva *Totuusarvo*-arvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Tätä toimintoa voidaan käyttää [FILTER](er-functions-list-filter.md)-toiminnon ehtolausekkeen määrittämiseen vain, kun asianmukainen määritys on konfiguroitu [Regulatory Configuration Servicesissä](../../../finance/localizations/rcs-globalization-feature.md), jotta voidaan käyttää [Microsoft Dataversea](../data-entities/data-integration-cds.md). Muussa tapauksessa tuotetaan poikkeus suunnittelun aikana. Vastaanotettu sanoma suosittelee [WHERE](er-functions-list-where.md)-funktion käyttöä `FILTER`-funktion asemesta suorituskyvyn parantamiseksi.

## <a name="example-1"></a>Esimerkki 1

Lauseke `ENDSWITH ("abc", "d")` palauttaa arvon **EPÄTOSI** ja lauseke `ENDSWITH ("abc", "C")` palauttaa arvon **TOSI**.

## <a name="example-2"></a>Esimerkki 2

Lauseke `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` palauttaa arvon **TOSI**, jos **malli**-tietolähteen **Address**-kentän arvo päättyy merkkijonolla **USA**. Muussa tapauksessa se palauttaa **EPÄTOSI**-arvon.

## <a name="additional-resources"></a>Lisäresurssit

[Loogiset toiminnot](er-functions-category-logical.md)
