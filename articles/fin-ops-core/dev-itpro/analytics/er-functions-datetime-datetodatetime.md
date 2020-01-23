---
title: DATETODATETIME ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) DATETODATETIME-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: f9ce977b36cd96a27a228dba1bc8c8445bafd879
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916381"
---
# <a name="DATETODATETIME">DATETODATETIME ER-funktio</a>

[!include [banner](../includes/banner.md)]

`DATETODATETIME`-funktio palauttaa *DateTime*-arvon , joka muunnetaan tietyn päivämäärän arvosta päivämäärä- ja aika-arvoksi koordinoidussa yleisajassa (Greenwichin aika \[GMT\]).

## <a name="syntax"></a>Syntaksi

```
DATETODATETIME (date)
```

## <a name="arguments"></a>Argumentit

`date`: *Päivämäärä*

Päivämääräarvo, joka vastaa muunnettavaa päivämäärää.

## <a name="return-values"></a>Palautusarvot

*DateTime*

Tulokseksi saatava päivämäärä-/aika-arvo.

## <a name="example-1"></a>Esimerkki 1

`DATETODATETIME (CompInfo. 'getCurrentDate()')` palauttaa nykyisen Microsoft Dynamics 365 Finance -istunnon päivämäärän, 24. joulukuuta 2015, muodossa **12/24/2015 12:00:00 AM**. Tässä esimerkissä **CompInfo** on **Finance and Operations/taulu** -tyypin sähköisen raportoinnin ER-tietolähde, joka viittaa CompanyInfo-tauluun.

## <a name="example-2"></a>Esimerkki 2

`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` palauttaa päivämäärän ja kellonajan arvon **11/12/2019 12:00:00 AM**.

## <a name="additional-resources"></a>Lisäresurssit

[Päivämäärä- ja aikatoiminnot](er-functions-category-datetime.md)