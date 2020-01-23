---
title: POWER ER-toiminto
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) POWER-funktiota käytetään.
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
ms.openlocfilehash: cb768b400e3ddb99e7c8b05905d7a2dd9e4392de
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915898"
---
# <span data-ttu-id="c0f2f-103"><a name="POWER">POWER ER-toiminto</a></span><span class="sxs-lookup"><span data-stu-id="c0f2f-103"><a name="POWER">POWER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0f2f-104">`POWER`-funktio palauttaa *todellisen* arvon, joka ilmaisee määritetyn positiivisen luvun nostamisesta määritettyyn tehoon.</span><span class="sxs-lookup"><span data-stu-id="c0f2f-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0f2f-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="c0f2f-105">Syntax</span></span>

```
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="c0f2f-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="c0f2f-106">Arguments</span></span>

<span data-ttu-id="c0f2f-107">`number`: *Todellinen* tai *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="c0f2f-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="c0f2f-108">Numeerinen arvo, joka on nostettava määritettyyn tehoon.</span><span class="sxs-lookup"><span data-stu-id="c0f2f-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="c0f2f-109">`power`: *Todellinen* tai *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="c0f2f-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="c0f2f-110">Numeerinen arvo, joka edustaa tiettyä tehoa.</span><span class="sxs-lookup"><span data-stu-id="c0f2f-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="c0f2f-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="c0f2f-111">Return values</span></span>

<span data-ttu-id="c0f2f-112">*Reaaliluku*</span><span class="sxs-lookup"><span data-stu-id="c0f2f-112">*Real*</span></span>

<span data-ttu-id="c0f2f-113">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="c0f2f-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="c0f2f-114">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="c0f2f-114">Example 1</span></span>

<span data-ttu-id="c0f2f-115">`POWER (10, 2)` palauttaa **100**.</span><span class="sxs-lookup"><span data-stu-id="c0f2f-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="c0f2f-116">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="c0f2f-116">Example 2</span></span>

<span data-ttu-id="c0f2f-117">`POWER (4, 0.5)` palauttaa **2**.</span><span class="sxs-lookup"><span data-stu-id="c0f2f-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c0f2f-118">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c0f2f-118">Additional resources</span></span>

[<span data-ttu-id="c0f2f-119">Matemaattinen toiminto</span><span class="sxs-lookup"><span data-stu-id="c0f2f-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
