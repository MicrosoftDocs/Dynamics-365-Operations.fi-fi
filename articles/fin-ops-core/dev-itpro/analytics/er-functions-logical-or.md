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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 107241dbf9a5127d61343fc1cf42c3bab577adb3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686975"
---
# <a name="or-er-function"></a><span data-ttu-id="61aff-103">OR ER -funktio</span><span class="sxs-lookup"><span data-stu-id="61aff-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61aff-104">`OR`-funktio palauttaa *totuusarvon* **EPÄTOSI**, jos mikään määritetty ehto ei toteudu.</span><span class="sxs-lookup"><span data-stu-id="61aff-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="61aff-105">Jos joku määritetty ehto toteutuu, tämä funktio palauttaa *totuusarvon* **TOSI**.</span><span class="sxs-lookup"><span data-stu-id="61aff-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="61aff-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="61aff-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="61aff-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="61aff-107">Arguments</span></span>

<span data-ttu-id="61aff-108">`condition 1`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="61aff-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="61aff-109">Kelvollinen ehdollinen lauseke, joka on testattava.</span><span class="sxs-lookup"><span data-stu-id="61aff-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="61aff-110">Tämä argumentti on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="61aff-110">This argument is required.</span></span>

<span data-ttu-id="61aff-111">`condition N`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="61aff-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="61aff-112">Kelvollinen ehdollinen lauseke, joka on testattava.</span><span class="sxs-lookup"><span data-stu-id="61aff-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="61aff-113">Nämä lisäargumentit ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="61aff-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="61aff-114">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="61aff-114">Return values</span></span>

<span data-ttu-id="61aff-115">*Boolen arvo*</span><span class="sxs-lookup"><span data-stu-id="61aff-115">*Boolean*</span></span>

<span data-ttu-id="61aff-116">Tuloksena oleva *Totuusarvo*-arvo.</span><span class="sxs-lookup"><span data-stu-id="61aff-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="61aff-117">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="61aff-117">Example</span></span>

<span data-ttu-id="61aff-118">`OR (1=2, "a"="a")` palauttaa arvon **TOSI**.</span><span class="sxs-lookup"><span data-stu-id="61aff-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61aff-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="61aff-119">Additional resources</span></span>

[<span data-ttu-id="61aff-120">Loogiset toiminnot</span><span class="sxs-lookup"><span data-stu-id="61aff-120">Logical functions</span></span>](er-functions-category-logical.md)
