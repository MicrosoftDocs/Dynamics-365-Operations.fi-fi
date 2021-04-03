---
title: POWER ER-toiminto
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) POWER-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 9c45e7f9b47a3f0ff4445b1dd160def0ada3a56e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570419"
---
# <a name="power-er-function"></a><span data-ttu-id="b9860-103">POWER ER-toiminto</span><span class="sxs-lookup"><span data-stu-id="b9860-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9860-104">`POWER`-funktio palauttaa *todellisen* arvon, joka ilmaisee määritetyn positiivisen luvun nostamisesta määritettyyn tehoon.</span><span class="sxs-lookup"><span data-stu-id="b9860-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9860-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="b9860-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="b9860-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="b9860-106">Arguments</span></span>

<span data-ttu-id="b9860-107">`number`: *Todellinen* tai *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="b9860-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="b9860-108">Numeerinen arvo, joka on nostettava määritettyyn tehoon.</span><span class="sxs-lookup"><span data-stu-id="b9860-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="b9860-109">`power`: *Todellinen* tai *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="b9860-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="b9860-110">Numeerinen arvo, joka edustaa tiettyä tehoa.</span><span class="sxs-lookup"><span data-stu-id="b9860-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="b9860-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="b9860-111">Return values</span></span>

<span data-ttu-id="b9860-112">*Reaaliluku*</span><span class="sxs-lookup"><span data-stu-id="b9860-112">*Real*</span></span>

<span data-ttu-id="b9860-113">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="b9860-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="b9860-114">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="b9860-114">Example 1</span></span>

<span data-ttu-id="b9860-115">`POWER (10, 2)` palauttaa **100**.</span><span class="sxs-lookup"><span data-stu-id="b9860-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b9860-116">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="b9860-116">Example 2</span></span>

<span data-ttu-id="b9860-117">`POWER (4, 0.5)` palauttaa **2**.</span><span class="sxs-lookup"><span data-stu-id="b9860-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9860-118">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b9860-118">Additional resources</span></span>

[<span data-ttu-id="b9860-119">Matemaattinen toiminto</span><span class="sxs-lookup"><span data-stu-id="b9860-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]