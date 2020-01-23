---
title: ROUND ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ROUND-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: c9384d5975e4a25d18ff741f87431daa4b0bbd7e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917071"
---
# <span data-ttu-id="7bfef-103"><a name="ROUND">ROUND ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="7bfef-103"><a name="ROUND">ROUND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7bfef-104">`ROUND`-funktio palauttaa määritetyn numeron *Todellisen* arvon sen jälkeen, kun se on pyöristetty määritettyyn määrään desimaaleja.</span><span class="sxs-lookup"><span data-stu-id="7bfef-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bfef-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="7bfef-105">Syntax</span></span>

```
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="7bfef-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="7bfef-106">Arguments</span></span>

<span data-ttu-id="7bfef-107">`number`: *Todellinen*</span><span class="sxs-lookup"><span data-stu-id="7bfef-107">`number`: *Real*</span></span>

<span data-ttu-id="7bfef-108">Numeerinen arvo, joka on pyöristettävä.</span><span class="sxs-lookup"><span data-stu-id="7bfef-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="7bfef-109">`decimals`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="7bfef-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="7bfef-110">Numeerinen arvo, joka vastaa desimaalien määrää.</span><span class="sxs-lookup"><span data-stu-id="7bfef-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="7bfef-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="7bfef-111">Return values</span></span>

<span data-ttu-id="7bfef-112">*Reaaliluku*</span><span class="sxs-lookup"><span data-stu-id="7bfef-112">*Real*</span></span>

<span data-ttu-id="7bfef-113">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="7bfef-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7bfef-114">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="7bfef-114">Usage notes</span></span>

<span data-ttu-id="7bfef-115">Jos `decimals`-argumentin arvo on yli 0 (nolla), numero pyöristetään kyseiseen määrään desimaaleja.</span><span class="sxs-lookup"><span data-stu-id="7bfef-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="7bfef-116">Jos `decimals`-argumentin arvo on **0** (nolla), numero pyöristetään lähimpään kokonaislukuun.</span><span class="sxs-lookup"><span data-stu-id="7bfef-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="7bfef-117">Jos `decimals`-argumentin arvo on vähemmän kuin 0 (nolla), numero pyöristetään desimaalipilkusta vasemmalle.</span><span class="sxs-lookup"><span data-stu-id="7bfef-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="7bfef-118">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="7bfef-118">Example 1</span></span>

<span data-ttu-id="7bfef-119">`ROUND (1200.767, 2)` pyöristää kahteen desimaaliin ja palauttaa arvon **1200,77**.</span><span class="sxs-lookup"><span data-stu-id="7bfef-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="7bfef-120">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="7bfef-120">Example 2</span></span>

<span data-ttu-id="7bfef-121">`ROUND (1200.767, -3)` pyöristää lähimpään tuhanteen ja palauttaa arvon **1000**.</span><span class="sxs-lookup"><span data-stu-id="7bfef-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7bfef-122">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="7bfef-122">Additional resources</span></span>

[<span data-ttu-id="7bfef-123">Matemaattinen toiminto</span><span class="sxs-lookup"><span data-stu-id="7bfef-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
