---
title: AND ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) AND-funktiota käytetään.
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9851321137b4c7744634df30f85aa3a0b1a0a588
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745470"
---
# <a name="and-er-function"></a><span data-ttu-id="c38aa-103">AND ER -funktio</span><span class="sxs-lookup"><span data-stu-id="c38aa-103">AND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c38aa-104">`AND`-funktio palauttaa *totuusarvon* **TOSI**, jos kaikki määritetyt ehdot toteutuvat.</span><span class="sxs-lookup"><span data-stu-id="c38aa-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="c38aa-105">Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="c38aa-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c38aa-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="c38aa-106">Syntax</span></span>

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="c38aa-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="c38aa-107">Arguments</span></span>

<span data-ttu-id="c38aa-108">`condition 1`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="c38aa-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="c38aa-109">Kelvollinen ehdollinen lauseke, joka on testattava.</span><span class="sxs-lookup"><span data-stu-id="c38aa-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="c38aa-110">Tämä argumentti on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="c38aa-110">This argument is required.</span></span>

<span data-ttu-id="c38aa-111">`condition N`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="c38aa-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="c38aa-112">Kelvollinen ehdollinen lauseke, joka on testattava.</span><span class="sxs-lookup"><span data-stu-id="c38aa-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="c38aa-113">Nämä lisäargumentit ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="c38aa-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="c38aa-114">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="c38aa-114">Return values</span></span>

<span data-ttu-id="c38aa-115">*Boolen arvo*</span><span class="sxs-lookup"><span data-stu-id="c38aa-115">*Boolean*</span></span>

<span data-ttu-id="c38aa-116">Tuloksena oleva *Totuusarvo*-arvo.</span><span class="sxs-lookup"><span data-stu-id="c38aa-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c38aa-117">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="c38aa-117">Usage notes</span></span>

<span data-ttu-id="c38aa-118">Loogisten funktioiden argumenteissa voit käyttää tietolähdeviittauksia, numeerisia ja tekstiarvoja, totuusarvoja, vertailuoperaattoreita ja muita sähköisen raportoinnin (ER) funktioita.</span><span class="sxs-lookup"><span data-stu-id="c38aa-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="c38aa-119">Kaikki argumentit on kuitenkin arvioitava *totuusarvoiksi* **TOSI** tai **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="c38aa-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="c38aa-120">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="c38aa-120">Example</span></span>

<span data-ttu-id="c38aa-121">`AND (1=1, "a"="a")` palauttaa arvon **TOSI**.</span><span class="sxs-lookup"><span data-stu-id="c38aa-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="c38aa-122">`AND (1=2, "a"="a")` palauttaa arvon **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="c38aa-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c38aa-123">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c38aa-123">Additional resources</span></span>

[<span data-ttu-id="c38aa-124">Loogiset toiminnot</span><span class="sxs-lookup"><span data-stu-id="c38aa-124">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]