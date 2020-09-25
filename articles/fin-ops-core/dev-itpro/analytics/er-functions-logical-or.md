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
ms.openlocfilehash: faf07c5d8b30cd3babe8a6a55ae7effe5ce457a0
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744620"
---
# <a name="or-er-function"></a><span data-ttu-id="66369-103">OR ER -funktio</span><span class="sxs-lookup"><span data-stu-id="66369-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66369-104">`OR`-funktio palauttaa *totuusarvon* **EPÄTOSI**, jos mikään määritetty ehto ei toteudu.</span><span class="sxs-lookup"><span data-stu-id="66369-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="66369-105">Jos joku määritetty ehto toteutuu, tämä funktio palauttaa *totuusarvon* **TOSI**.</span><span class="sxs-lookup"><span data-stu-id="66369-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="66369-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="66369-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="66369-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="66369-107">Arguments</span></span>

<span data-ttu-id="66369-108">`condition 1`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="66369-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="66369-109">Kelvollinen ehdollinen lauseke, joka on testattava.</span><span class="sxs-lookup"><span data-stu-id="66369-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="66369-110">Tämä argumentti on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="66369-110">This argument is required.</span></span>

<span data-ttu-id="66369-111">`condition N`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="66369-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="66369-112">Kelvollinen ehdollinen lauseke, joka on testattava.</span><span class="sxs-lookup"><span data-stu-id="66369-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="66369-113">Nämä lisäargumentit ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="66369-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="66369-114">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="66369-114">Return values</span></span>

<span data-ttu-id="66369-115">*Boolen arvo*</span><span class="sxs-lookup"><span data-stu-id="66369-115">*Boolean*</span></span>

<span data-ttu-id="66369-116">Tuloksena oleva *Totuusarvo*-arvo.</span><span class="sxs-lookup"><span data-stu-id="66369-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="66369-117">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="66369-117">Example</span></span>

<span data-ttu-id="66369-118">`OR (1=2, "a"="a")` palauttaa arvon **TOSI**.</span><span class="sxs-lookup"><span data-stu-id="66369-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="66369-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="66369-119">Additional resources</span></span>

[<span data-ttu-id="66369-120">Loogiset toiminnot</span><span class="sxs-lookup"><span data-stu-id="66369-120">Logical functions</span></span>](er-functions-category-logical.md)
