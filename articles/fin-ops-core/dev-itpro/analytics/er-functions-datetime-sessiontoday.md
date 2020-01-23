---
title: SESSIONTODAY ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) SESSIONTODAY-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: bcfb36d6e3fb8475546f7cfb420c4aca848ac896
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917462"
---
# <span data-ttu-id="bfb6c-103"><a name="SESSIONTODAY">SESSIONTODAY ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="bfb6c-103"><a name="SESSIONTODAY">SESSIONTODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bfb6c-104">`SESSIONTODAY`-funktio palauttaa *Date*-arvon, joka edustaa nykyistä sovellusistunnon päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="bfb6c-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfb6c-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="bfb6c-105">Syntax</span></span>

```
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="bfb6c-106">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="bfb6c-106">Return values</span></span>

<span data-ttu-id="bfb6c-107">*Päivämäärä*</span><span class="sxs-lookup"><span data-stu-id="bfb6c-107">*Date*</span></span>

<span data-ttu-id="bfb6c-108">Tulokseksi saatava päivämääräarvo.</span><span class="sxs-lookup"><span data-stu-id="bfb6c-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="bfb6c-109">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="bfb6c-109">Example</span></span>

<span data-ttu-id="bfb6c-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` palauttaa nykyisen sovellusistunnon päivämäärän, 24. joulukuuta 2015, merkkijonona **"24-12-2015"**, joka perustuu valittuun Saksan kulttuuriin ja määritettyyn muotoon.</span><span class="sxs-lookup"><span data-stu-id="bfb6c-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bfb6c-111">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="bfb6c-111">Additional resources</span></span>

[<span data-ttu-id="bfb6c-112">Päivämäärä- ja aikatoiminnot</span><span class="sxs-lookup"><span data-stu-id="bfb6c-112">Date and time functions</span></span>](er-functions-category-datetime.md)
