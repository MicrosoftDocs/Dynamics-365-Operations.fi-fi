---
title: AND ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) AND-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ccb7feb1d0f6836e7e8001870034900f6a1f598
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687071"
---
# <a name="and-er-function"></a><span data-ttu-id="180c1-103">AND ER -funktio</span><span class="sxs-lookup"><span data-stu-id="180c1-103">AND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="180c1-104">`AND`-funktio palauttaa *totuusarvon* **TOSI**, jos kaikki määritetyt ehdot toteutuvat.</span><span class="sxs-lookup"><span data-stu-id="180c1-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="180c1-105">Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="180c1-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="180c1-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="180c1-106">Syntax</span></span>

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="180c1-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="180c1-107">Arguments</span></span>

<span data-ttu-id="180c1-108">`condition 1`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="180c1-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="180c1-109">Kelvollinen ehdollinen lauseke, joka on testattava.</span><span class="sxs-lookup"><span data-stu-id="180c1-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="180c1-110">Tämä argumentti on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="180c1-110">This argument is required.</span></span>

<span data-ttu-id="180c1-111">`condition N`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="180c1-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="180c1-112">Kelvollinen ehdollinen lauseke, joka on testattava.</span><span class="sxs-lookup"><span data-stu-id="180c1-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="180c1-113">Nämä lisäargumentit ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="180c1-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="180c1-114">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="180c1-114">Return values</span></span>

<span data-ttu-id="180c1-115">*Boolen arvo*</span><span class="sxs-lookup"><span data-stu-id="180c1-115">*Boolean*</span></span>

<span data-ttu-id="180c1-116">Tuloksena oleva *Totuusarvo*-arvo.</span><span class="sxs-lookup"><span data-stu-id="180c1-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="180c1-117">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="180c1-117">Usage notes</span></span>

<span data-ttu-id="180c1-118">Loogisten funktioiden argumenteissa voit käyttää tietolähdeviittauksia, numeerisia ja tekstiarvoja, totuusarvoja, vertailuoperaattoreita ja muita sähköisen raportoinnin (ER) funktioita.</span><span class="sxs-lookup"><span data-stu-id="180c1-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="180c1-119">Kaikki argumentit on kuitenkin arvioitava *totuusarvoiksi* **TOSI** tai **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="180c1-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="180c1-120">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="180c1-120">Example</span></span>

<span data-ttu-id="180c1-121">`AND (1=1, "a"="a")` palauttaa arvon **TOSI**.</span><span class="sxs-lookup"><span data-stu-id="180c1-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="180c1-122">`AND (1=2, "a"="a")` palauttaa arvon **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="180c1-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="180c1-123">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="180c1-123">Additional resources</span></span>

[<span data-ttu-id="180c1-124">Loogiset toiminnot</span><span class="sxs-lookup"><span data-stu-id="180c1-124">Logical functions</span></span>](er-functions-category-logical.md)
