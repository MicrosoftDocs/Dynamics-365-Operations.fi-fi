---
title: ER:n STARTSWITH-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) STARTSWITH-funktiota käytetään.
author: NickSelin
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
ms.openlocfilehash: ef7e9c88abff2b4b58ecb8abf1e69f7853f9b3fa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751677"
---
# <a name="startswith-er-function"></a>ER:n STARTSWITH-funktio

[!include [banner](../includes/banner.md)]

`STARTSWITH`-funktio määrittää, alkaako määritetty syöte määritetyllä tekstillä. Se palauttaa *totuus*-arvon **TOSI**, jos määritetty syöte alkaa määritetyllä tekstillä. Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**.

## <a name="syntax"></a>Syntaksi

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a>Argumentit

`input`: *Merkkijono*

*Merkkijono*-tyypin tai merkkijonovakion tietolähteen kohteen kelvollinen polku, jonka arvo voi alkaa toisella argumentilla.

`start text`: *Merkkijono*

*Merkkijono*-tietotyypin tai merkkijonovakion tietolähteen kelvollinen polku, jonka arvo voi olla ensimmäisen argumentin alussa.

## <a name="return-values"></a>Palautusarvot

*Boolen arvo*

Tuloksena oleva *Totuusarvo*-arvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Tätä toimintoa voidaan käyttää [FILTER](er-functions-list-filter.md)-toiminnon ehtolausekkeen määrittämiseen vain, kun asianmukainen määritys on konfiguroitu [Regulatory Configuration Servicesissä](../../../finance/localizations/rcs-globalization-feature.md), jotta voidaan käyttää [Microsoft Dataversea](../data-entities/data-integration-cds.md). Muussa tapauksessa tuotetaan poikkeus suunnittelun aikana. Vastaanotettu sanoma suosittelee [WHERE](er-functions-list-where.md)-funktion käyttöä `FILTER`-funktion asemesta suorituskyvyn parantamiseksi.

## <a name="example-1"></a>Esimerkki 1

Lauseke `STARTSWITH ("abc", "d")` palauttaa arvon **EPÄTOSI** ja lauseke `STARTSWITH ("abc", "A")` palauttaa arvon **TOSI**.

## <a name="example-2"></a>Esimerkki 2

Lauseke `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` palauttaa arvon **TOSI**, jos **malli**-tietolähteen **Address**-kentän arvo alkaa merkkijonolla **123 Coffee Street**. Muussa tapauksessa se palauttaa **EPÄTOSI**-arvon.

## <a name="additional-resources"></a>Lisäresurssit

[Loogiset toiminnot](er-functions-category-logical.md)
