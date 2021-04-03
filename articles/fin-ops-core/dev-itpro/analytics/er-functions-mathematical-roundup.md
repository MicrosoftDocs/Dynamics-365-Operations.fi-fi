---
title: ROUNDUP ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ROUNDUP-funktiota käytetään.
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
ms.openlocfilehash: d23a984bd59c4d2d37c407e3fcfed9c7017dcc7f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569332"
---
# <a name="roundup-er-function"></a><span data-ttu-id="a2fb0-103">ROUNDUP ER-funktio</span><span class="sxs-lookup"><span data-stu-id="a2fb0-103">ROUNDUP ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2fb0-104">`ROUNDUP`-funktio palauttaa määritetyn numeron *Todellisen* arvon sen jälkeen, kun se on pyöristetty ylöspäin määritettyyn määrään desimaaleja.</span><span class="sxs-lookup"><span data-stu-id="a2fb0-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2fb0-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="a2fb0-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="a2fb0-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="a2fb0-106">Arguments</span></span>

<span data-ttu-id="a2fb0-107">`number`: *Todellinen*</span><span class="sxs-lookup"><span data-stu-id="a2fb0-107">`number`: *Real*</span></span>

<span data-ttu-id="a2fb0-108">Numeerinen arvo, joka on pyöristettävä ylöspäin.</span><span class="sxs-lookup"><span data-stu-id="a2fb0-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="a2fb0-109">`decimals`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="a2fb0-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="a2fb0-110">Numeerinen arvo, joka vastaa desimaalien määrää.</span><span class="sxs-lookup"><span data-stu-id="a2fb0-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="a2fb0-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="a2fb0-111">Return values</span></span>

<span data-ttu-id="a2fb0-112">*Reaaliluku*</span><span class="sxs-lookup"><span data-stu-id="a2fb0-112">*Real*</span></span>

<span data-ttu-id="a2fb0-113">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="a2fb0-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a2fb0-114">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="a2fb0-114">Usage notes</span></span>

<span data-ttu-id="a2fb0-115">Tämä funktio toimii kuin [ROUND](er-functions-mathematical-round.md), mutta se pyöristää määritetyn numeron aina ylöspäin (pois päin nollasta).</span><span class="sxs-lookup"><span data-stu-id="a2fb0-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="a2fb0-116">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="a2fb0-116">Example 1</span></span>

<span data-ttu-id="a2fb0-117">`ROUNDUP (1200.763, 2)` pyöristää ylöspäin kahteen desimaaliin ja palauttaa arvon **1200,77**.</span><span class="sxs-lookup"><span data-stu-id="a2fb0-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="a2fb0-118">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="a2fb0-118">Example 2</span></span>

<span data-ttu-id="a2fb0-119">`ROUNDUP (1200.767, -3)` pyöristää ylöspäin lähimpään tuhanteen ja palauttaa arvon **1,000**.</span><span class="sxs-lookup"><span data-stu-id="a2fb0-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a2fb0-120">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a2fb0-120">Additional resources</span></span>

[<span data-ttu-id="a2fb0-121">Matemaattinen toiminto</span><span class="sxs-lookup"><span data-stu-id="a2fb0-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]