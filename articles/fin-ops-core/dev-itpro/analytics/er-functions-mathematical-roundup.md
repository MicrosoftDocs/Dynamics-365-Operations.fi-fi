---
title: ROUNDUP ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ROUNDUP-funktiota käytetään.
author: NickSelin
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
ms.openlocfilehash: 4898f596108ff3c563da55a567a10da987d62d33
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744436"
---
# <a name="roundup-er-function"></a><span data-ttu-id="61d31-103">ROUNDUP ER-funktio</span><span class="sxs-lookup"><span data-stu-id="61d31-103">ROUNDUP ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61d31-104">`ROUNDUP`-funktio palauttaa määritetyn numeron *Todellisen* arvon sen jälkeen, kun se on pyöristetty ylöspäin määritettyyn määrään desimaaleja.</span><span class="sxs-lookup"><span data-stu-id="61d31-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="61d31-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="61d31-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="61d31-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="61d31-106">Arguments</span></span>

<span data-ttu-id="61d31-107">`number`: *Todellinen*</span><span class="sxs-lookup"><span data-stu-id="61d31-107">`number`: *Real*</span></span>

<span data-ttu-id="61d31-108">Numeerinen arvo, joka on pyöristettävä ylöspäin.</span><span class="sxs-lookup"><span data-stu-id="61d31-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="61d31-109">`decimals`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="61d31-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="61d31-110">Numeerinen arvo, joka vastaa desimaalien määrää.</span><span class="sxs-lookup"><span data-stu-id="61d31-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="61d31-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="61d31-111">Return values</span></span>

<span data-ttu-id="61d31-112">*Reaaliluku*</span><span class="sxs-lookup"><span data-stu-id="61d31-112">*Real*</span></span>

<span data-ttu-id="61d31-113">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="61d31-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="61d31-114">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="61d31-114">Usage notes</span></span>

<span data-ttu-id="61d31-115">Tämä funktio toimii kuin [ROUND](er-functions-mathematical-round.md), mutta se pyöristää määritetyn numeron aina ylöspäin (pois päin nollasta).</span><span class="sxs-lookup"><span data-stu-id="61d31-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="61d31-116">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="61d31-116">Example 1</span></span>

<span data-ttu-id="61d31-117">`ROUNDUP (1200.763, 2)` pyöristää ylöspäin kahteen desimaaliin ja palauttaa arvon **1200,77**.</span><span class="sxs-lookup"><span data-stu-id="61d31-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="61d31-118">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="61d31-118">Example 2</span></span>

<span data-ttu-id="61d31-119">`ROUNDUP (1200.767, -3)` pyöristää ylöspäin lähimpään tuhanteen ja palauttaa arvon **1,000**.</span><span class="sxs-lookup"><span data-stu-id="61d31-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61d31-120">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="61d31-120">Additional resources</span></span>

[<span data-ttu-id="61d31-121">Matemaattinen toiminto</span><span class="sxs-lookup"><span data-stu-id="61d31-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]