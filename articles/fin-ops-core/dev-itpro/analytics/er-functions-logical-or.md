---
title: OR ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) OR-funktiota käytetään.
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
ms.openlocfilehash: 81a596f5206b23001feea553adcdf6c904572775
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917117"
---
# <span data-ttu-id="0a23f-103"><a name="OR">OR ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="0a23f-103"><a name="OR">OR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a23f-104">`OR`-funktio palauttaa *totuusarvon* **EPÄTOSI**, jos mikään määritetty ehto ei toteudu.</span><span class="sxs-lookup"><span data-stu-id="0a23f-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="0a23f-105">Jos joku määritetty ehto toteutuu, tämä funktio palauttaa *totuusarvon* **TOSI**.</span><span class="sxs-lookup"><span data-stu-id="0a23f-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a23f-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="0a23f-106">Syntax</span></span>

```
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="0a23f-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="0a23f-107">Arguments</span></span>

<span data-ttu-id="0a23f-108">`condition 1`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="0a23f-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="0a23f-109">Kelvollinen ehdollinen lauseke, joka on testattava.</span><span class="sxs-lookup"><span data-stu-id="0a23f-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="0a23f-110">Tämä argumentti on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="0a23f-110">This argument is required.</span></span>

<span data-ttu-id="0a23f-111">`condition N`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="0a23f-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="0a23f-112">Kelvollinen ehdollinen lauseke, joka on testattava.</span><span class="sxs-lookup"><span data-stu-id="0a23f-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="0a23f-113">Nämä lisäargumentit ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="0a23f-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="0a23f-114">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="0a23f-114">Return values</span></span>

<span data-ttu-id="0a23f-115">*Boolen arvo*</span><span class="sxs-lookup"><span data-stu-id="0a23f-115">*Boolean*</span></span>

<span data-ttu-id="0a23f-116">Tuloksena oleva *Totuusarvo*-arvo.</span><span class="sxs-lookup"><span data-stu-id="0a23f-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="0a23f-117">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="0a23f-117">Example</span></span>

<span data-ttu-id="0a23f-118">`OR (1=2, "a"="a")` palauttaa arvon **TOSI**.</span><span class="sxs-lookup"><span data-stu-id="0a23f-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0a23f-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0a23f-119">Additional resources</span></span>

[<span data-ttu-id="0a23f-120">Loogiset toiminnot</span><span class="sxs-lookup"><span data-stu-id="0a23f-120">Logical functions</span></span>](er-functions-category-logical.md)
