---
title: ROUND ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ROUND-funktiota käytetään.
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
ms.openlocfilehash: 6751c1321fc71419fa8b153145a057371e0f7af5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041604"
---
# <span data-ttu-id="abf07-103"><a name="ROUND">ROUND ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="abf07-103"><a name="ROUND">ROUND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="abf07-104">`ROUND`-funktio palauttaa määritetyn numeron *Todellisen* arvon sen jälkeen, kun se on pyöristetty määritettyyn määrään desimaaleja.</span><span class="sxs-lookup"><span data-stu-id="abf07-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="abf07-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="abf07-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="abf07-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="abf07-106">Arguments</span></span>

<span data-ttu-id="abf07-107">`number`: *Todellinen*</span><span class="sxs-lookup"><span data-stu-id="abf07-107">`number`: *Real*</span></span>

<span data-ttu-id="abf07-108">Numeerinen arvo, joka on pyöristettävä.</span><span class="sxs-lookup"><span data-stu-id="abf07-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="abf07-109">`decimals`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="abf07-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="abf07-110">Numeerinen arvo, joka vastaa desimaalien määrää.</span><span class="sxs-lookup"><span data-stu-id="abf07-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="abf07-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="abf07-111">Return values</span></span>

<span data-ttu-id="abf07-112">*Reaaliluku*</span><span class="sxs-lookup"><span data-stu-id="abf07-112">*Real*</span></span>

<span data-ttu-id="abf07-113">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="abf07-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="abf07-114">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="abf07-114">Usage notes</span></span>

<span data-ttu-id="abf07-115">Jos `decimals`-argumentin arvo on yli 0 (nolla), numero pyöristetään kyseiseen määrään desimaaleja.</span><span class="sxs-lookup"><span data-stu-id="abf07-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="abf07-116">Jos `decimals`-argumentin arvo on **0** (nolla), numero pyöristetään lähimpään kokonaislukuun.</span><span class="sxs-lookup"><span data-stu-id="abf07-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="abf07-117">Jos `decimals`-argumentin arvo on vähemmän kuin 0 (nolla), numero pyöristetään desimaalipilkusta vasemmalle.</span><span class="sxs-lookup"><span data-stu-id="abf07-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="abf07-118">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="abf07-118">Example 1</span></span>

<span data-ttu-id="abf07-119">`ROUND (1200.767, 2)` pyöristää kahteen desimaaliin ja palauttaa arvon **1200,77**.</span><span class="sxs-lookup"><span data-stu-id="abf07-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="abf07-120">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="abf07-120">Example 2</span></span>

<span data-ttu-id="abf07-121">`ROUND (1200.767, -3)` pyöristää lähimpään tuhanteen ja palauttaa arvon **1000**.</span><span class="sxs-lookup"><span data-stu-id="abf07-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="abf07-122">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="abf07-122">Additional resources</span></span>

[<span data-ttu-id="abf07-123">Matemaattinen toiminto</span><span class="sxs-lookup"><span data-stu-id="abf07-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
