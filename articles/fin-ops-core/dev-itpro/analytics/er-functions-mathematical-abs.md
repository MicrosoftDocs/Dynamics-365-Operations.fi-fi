---
title: ABS ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ABS-funktiota käytetään.
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
ms.openlocfilehash: b53535d1a000b72577be5c6284cc4676c43d591b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744596"
---
# <a name="abs-er-function"></a><span data-ttu-id="5fece-103">ABS ER -funktio</span><span class="sxs-lookup"><span data-stu-id="5fece-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5fece-104">`ABS`-funktio palauttaa määritetyn luvun absoluuttisen arvon (jakojäännös) *todelliseksi* arvoksi.</span><span class="sxs-lookup"><span data-stu-id="5fece-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="5fece-105">Toisin sanoen, se palauttaa luvun ilman etumerkkiä.</span><span class="sxs-lookup"><span data-stu-id="5fece-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fece-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="5fece-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="5fece-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="5fece-107">Arguments</span></span>

<span data-ttu-id="5fece-108">`number`: *Todellinen*</span><span class="sxs-lookup"><span data-stu-id="5fece-108">`number`: *Real*</span></span>

<span data-ttu-id="5fece-109">Numeerinen arvo, jonka jakojäännöksen haluat.</span><span class="sxs-lookup"><span data-stu-id="5fece-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="5fece-110">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="5fece-110">Return values</span></span>

<span data-ttu-id="5fece-111">*Reaaliluku*</span><span class="sxs-lookup"><span data-stu-id="5fece-111">*Real*</span></span>

<span data-ttu-id="5fece-112">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="5fece-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="5fece-113">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="5fece-113">Example</span></span>

<span data-ttu-id="5fece-114">`ABS (-1)` palauttaa **1**.</span><span class="sxs-lookup"><span data-stu-id="5fece-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5fece-115">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="5fece-115">Additional resources</span></span>

[<span data-ttu-id="5fece-116">Matemaattinen toiminto</span><span class="sxs-lookup"><span data-stu-id="5fece-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
