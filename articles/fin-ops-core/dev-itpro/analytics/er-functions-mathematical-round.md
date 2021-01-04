---
title: ROUND ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ROUND-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 10/21/2020
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
ms.openlocfilehash: 83fb5c04938e0aba1277f2d6017d4b66208a8858
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683253"
---
# <a name="round-er-function"></a><span data-ttu-id="b4b95-103">ROUND ER-funktio</span><span class="sxs-lookup"><span data-stu-id="b4b95-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4b95-104">`ROUND`-funktio palauttaa määritetyn numeron *Todellisen* arvon sen jälkeen, kun se on pyöristetty määritettyyn määrään desimaaleja.</span><span class="sxs-lookup"><span data-stu-id="b4b95-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4b95-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="b4b95-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="b4b95-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="b4b95-106">Arguments</span></span>

<span data-ttu-id="b4b95-107">`number`: *Todellinen*</span><span class="sxs-lookup"><span data-stu-id="b4b95-107">`number`: *Real*</span></span>

<span data-ttu-id="b4b95-108">Numeerinen arvo, joka on pyöristettävä.</span><span class="sxs-lookup"><span data-stu-id="b4b95-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="b4b95-109">`decimals`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="b4b95-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="b4b95-110">Numeerinen arvo, joka vastaa desimaalien määrää.</span><span class="sxs-lookup"><span data-stu-id="b4b95-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="b4b95-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="b4b95-111">Return values</span></span>

<span data-ttu-id="b4b95-112">*Reaaliluku*</span><span class="sxs-lookup"><span data-stu-id="b4b95-112">*Real*</span></span>

<span data-ttu-id="b4b95-113">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="b4b95-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b4b95-114">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="b4b95-114">Usage notes</span></span>

<span data-ttu-id="b4b95-115">Jos `decimals`-argumentin arvo on yli 0 (nolla), numero pyöristetään kyseiseen määrään desimaaleja.</span><span class="sxs-lookup"><span data-stu-id="b4b95-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="b4b95-116">Jos `decimals`-argumentin arvo on **0** (nolla), numero pyöristetään lähimpään parilliseen kokonaislukuun.</span><span class="sxs-lookup"><span data-stu-id="b4b95-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest even integer.</span></span>

<span data-ttu-id="b4b95-117">Jos `decimals`-argumentin arvo on vähemmän kuin 0 (nolla), numero pyöristetään desimaalipilkusta vasemmalle.</span><span class="sxs-lookup"><span data-stu-id="b4b95-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="b4b95-118">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="b4b95-118">Example 1</span></span>

<span data-ttu-id="b4b95-119">`ROUND (1200.767, 2)` pyöristää kahteen desimaaliin ja palauttaa arvon **1200,77**.</span><span class="sxs-lookup"><span data-stu-id="b4b95-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b4b95-120">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="b4b95-120">Example 2</span></span>

<span data-ttu-id="b4b95-121">`ROUND (1200.767, -3)` pyöristää lähimpään tuhanteen ja palauttaa arvon **1000**.</span><span class="sxs-lookup"><span data-stu-id="b4b95-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="example-3"></a><span data-ttu-id="b4b95-122">Esimerkki 3</span><span class="sxs-lookup"><span data-stu-id="b4b95-122">Example 3</span></span>

<span data-ttu-id="b4b95-123">`ROUND (1200.5, 0)` pyöristää lähimpään parilliseen kokonaislukuun ja palauttaa arvon **1200**, mutta `ROUND (1201.5, 0)` tekee saman ja palauttaa arvon **1202**.</span><span class="sxs-lookup"><span data-stu-id="b4b95-123">`ROUND (1200.5, 0)` rounds to the nearest even integer and returns **1200**, while `ROUND (1201.5, 0)` does the same and returns **1202**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4b95-124">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b4b95-124">Additional resources</span></span>

[<span data-ttu-id="b4b95-125">Matemaattinen toiminto</span><span class="sxs-lookup"><span data-stu-id="b4b95-125">Mathematical functions</span></span>](er-functions-category-mathematical.md)
