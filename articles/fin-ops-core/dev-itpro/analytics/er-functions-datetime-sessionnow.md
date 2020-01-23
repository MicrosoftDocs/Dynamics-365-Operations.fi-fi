---
title: SESSIONNOW ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) SESSIONNOW-funktiota käytetään.
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
ms.openlocfilehash: 4dff6daa8fbd60ef1fc84d783e428d69477aac6d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916266"
---
# <span data-ttu-id="72b30-103"><a name="">SESSIONNOW ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="72b30-103"><a name="">SESSIONNOW ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72b30-104">`SESSIONNOW`-funktio palauttaa *DateTime*-arvon, joka edustaa nykyistä sovellusistunnon päivämäärää ja aikaa.</span><span class="sxs-lookup"><span data-stu-id="72b30-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="72b30-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="72b30-105">Syntax</span></span>

```
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="72b30-106">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="72b30-106">Return values</span></span>

<span data-ttu-id="72b30-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="72b30-107">*DateTime*</span></span>

<span data-ttu-id="72b30-108">Tulokseksi saatava päivämäärä-/aika-arvo.</span><span class="sxs-lookup"><span data-stu-id="72b30-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="72b30-109">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="72b30-109">Example</span></span>

<span data-ttu-id="72b30-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` palauttaa nykyisen sovellusistunnon päivämäärä-/aika-arvon, 24. joulukuuta 2015, merkkijonona **"24.12.2015"**, joka perustuu valittuun Saksan kulttuuriin ja määritettyyn muotoon.</span><span class="sxs-lookup"><span data-stu-id="72b30-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="72b30-111">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="72b30-111">Additional resources</span></span>

[<span data-ttu-id="72b30-112">Päivämäärä- ja aikatoiminnot</span><span class="sxs-lookup"><span data-stu-id="72b30-112">Date and time functions</span></span>](er-functions-category-datetime.md)
