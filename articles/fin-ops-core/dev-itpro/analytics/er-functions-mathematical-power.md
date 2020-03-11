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
ms.openlocfilehash: c57222d7fcc133faa679bab43431272c984c9d8b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041627"
---
# <span data-ttu-id="70e17-103"><a name="POWER">POWER ER-toiminto</a></span><span class="sxs-lookup"><span data-stu-id="70e17-103"><a name="POWER">POWER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70e17-104">`POWER`-funktio palauttaa *todellisen* arvon, joka ilmaisee määritetyn positiivisen luvun nostamisesta määritettyyn tehoon.</span><span class="sxs-lookup"><span data-stu-id="70e17-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="70e17-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="70e17-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="70e17-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="70e17-106">Arguments</span></span>

<span data-ttu-id="70e17-107">`number`: *Todellinen* tai *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="70e17-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="70e17-108">Numeerinen arvo, joka on nostettava määritettyyn tehoon.</span><span class="sxs-lookup"><span data-stu-id="70e17-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="70e17-109">`power`: *Todellinen* tai *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="70e17-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="70e17-110">Numeerinen arvo, joka edustaa tiettyä tehoa.</span><span class="sxs-lookup"><span data-stu-id="70e17-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="70e17-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="70e17-111">Return values</span></span>

<span data-ttu-id="70e17-112">*Reaaliluku*</span><span class="sxs-lookup"><span data-stu-id="70e17-112">*Real*</span></span>

<span data-ttu-id="70e17-113">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="70e17-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="70e17-114">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="70e17-114">Example 1</span></span>

<span data-ttu-id="70e17-115">`POWER (10, 2)` palauttaa **100**.</span><span class="sxs-lookup"><span data-stu-id="70e17-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="70e17-116">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="70e17-116">Example 2</span></span>

<span data-ttu-id="70e17-117">`POWER (4, 0.5)` palauttaa **2**.</span><span class="sxs-lookup"><span data-stu-id="70e17-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="70e17-118">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="70e17-118">Additional resources</span></span>

[<span data-ttu-id="70e17-119">Matemaattinen toiminto</span><span class="sxs-lookup"><span data-stu-id="70e17-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
