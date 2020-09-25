---
title: ROUNDDOWN ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ROUNDDOWN-funktiota käytetään.
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
ms.openlocfilehash: 7ac559983609d4fdb80c9ac70d84031e4a231889
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744524"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="fabd9-103">ROUNDDOWN ER-funktio</span><span class="sxs-lookup"><span data-stu-id="fabd9-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fabd9-104">`ROUNDDOWN`-funktio palauttaa määritetyn numeron *Todellisen* arvon sen jälkeen, kun se on pyöristetty alaspäin määritettyyn määrään desimaaleja.</span><span class="sxs-lookup"><span data-stu-id="fabd9-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="fabd9-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="fabd9-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="fabd9-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="fabd9-106">Arguments</span></span>

<span data-ttu-id="fabd9-107">`number`: *Todellinen*</span><span class="sxs-lookup"><span data-stu-id="fabd9-107">`number`: *Real*</span></span>

<span data-ttu-id="fabd9-108">Numeerinen arvo, joka on pyöristettävä alaspäin.</span><span class="sxs-lookup"><span data-stu-id="fabd9-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="fabd9-109">`decimals`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="fabd9-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="fabd9-110">Numeerinen arvo, joka vastaa desimaalien määrää.</span><span class="sxs-lookup"><span data-stu-id="fabd9-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="fabd9-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="fabd9-111">Return values</span></span>

<span data-ttu-id="fabd9-112">*Reaaliluku*</span><span class="sxs-lookup"><span data-stu-id="fabd9-112">*Real*</span></span>

<span data-ttu-id="fabd9-113">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="fabd9-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fabd9-114">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="fabd9-114">Usage notes</span></span>

<span data-ttu-id="fabd9-115">Tämä funktio toimii kuin [ROUND](er-functions-mathematical-round.md), mutta se pyöristää määritetyn numeron aina alaspäin (kohti nollaa).</span><span class="sxs-lookup"><span data-stu-id="fabd9-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="fabd9-116">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="fabd9-116">Example 1</span></span>

<span data-ttu-id="fabd9-117">`ROUNDDOWN (1200.767, 2)` pyöristää alaspäin kahteen desimaaliin ja palauttaa arvon **1200,76**.</span><span class="sxs-lookup"><span data-stu-id="fabd9-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="fabd9-118">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="fabd9-118">Example 2</span></span>

<span data-ttu-id="fabd9-119">`ROUNDDOWN (1700.767, -3)` pyöristää alaspäin lähimpään tuhanteen ja palauttaa arvon **1000**.</span><span class="sxs-lookup"><span data-stu-id="fabd9-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fabd9-120">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="fabd9-120">Additional resources</span></span>

[<span data-ttu-id="fabd9-121">Matemaattinen toiminto</span><span class="sxs-lookup"><span data-stu-id="fabd9-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
