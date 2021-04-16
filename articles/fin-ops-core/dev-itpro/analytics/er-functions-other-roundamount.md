---
title: ROUNDAMOUNT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ROUNDAMOUNT-funktiota käytetään.
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
ms.openlocfilehash: cce35a33ca179ad85bbde879122d3afbeefe5ee7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745660"
---
# <a name="roundamount-er-function"></a><span data-ttu-id="8071c-103">ROUNDAMOUNT ER-funktio</span><span class="sxs-lookup"><span data-stu-id="8071c-103">ROUNDAMOUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8071c-104">`ROUNDAMOUNT`-Funktio palauttaa *todellisen* arvon määritetyn numeron pyöristyksen tuloksena lähimpään toiseen useaan numeroon määritetyn pyöristyssäännön mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8071c-104">The `ROUNDAMOUNT` function returns a *Real* value as the result of the rounding of the specified number to the nearest multiple of another number according to the specified rounding rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="8071c-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="8071c-105">Syntax</span></span>

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a><span data-ttu-id="8071c-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="8071c-106">Arguments</span></span>

<span data-ttu-id="8071c-107">`number`: *Int* tai *Todellinen*</span><span class="sxs-lookup"><span data-stu-id="8071c-107">`number`: *Int* or *Real*</span></span>

<span data-ttu-id="8071c-108">Numeerinen arvo, joka on pyöristettävä.</span><span class="sxs-lookup"><span data-stu-id="8071c-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="8071c-109">`decimals`: *Int* tai *Todellinen*</span><span class="sxs-lookup"><span data-stu-id="8071c-109">`decimals`: *Int* or *Real*</span></span>

<span data-ttu-id="8071c-110">Numero, joka `number`-parametrin arvon on pyöristettävä useaan.</span><span class="sxs-lookup"><span data-stu-id="8071c-110">The number that the value of the `number` parameter must be rounded to a multiple of.</span></span>

<span data-ttu-id="8071c-111">`round rule`: *Enum-arvo*</span><span class="sxs-lookup"><span data-stu-id="8071c-111">`round rule`: *Enum value*</span></span>

<span data-ttu-id="8071c-112">**RoundOffType**-luetteloinnin luettelointiarvo, joka määrittää pyöristyssäännön.</span><span class="sxs-lookup"><span data-stu-id="8071c-112">An enumeration value of the **RoundOffType** enumeration that defines the rounding rule.</span></span> <span data-ttu-id="8071c-113">Tämä luettelointi tarjoaa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="8071c-113">This enumeration offers the following values:</span></span>

- <span data-ttu-id="8071c-114">Normaali (tavallinen)</span><span class="sxs-lookup"><span data-stu-id="8071c-114">Normal (Ordinary)</span></span>
- <span data-ttu-id="8071c-115">Alaspäin (RoundDown)</span><span class="sxs-lookup"><span data-stu-id="8071c-115">Downward (RoundDown)</span></span>
- <span data-ttu-id="8071c-116">Pyöristys ylös (RoundUp)</span><span class="sxs-lookup"><span data-stu-id="8071c-116">Rounding-up (RoundUp)</span></span>

## <a name="return-values"></a><span data-ttu-id="8071c-117">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="8071c-117">Return values</span></span>

<span data-ttu-id="8071c-118">*Reaaliluku*</span><span class="sxs-lookup"><span data-stu-id="8071c-118">*Real*</span></span>

<span data-ttu-id="8071c-119">Tulokseksi saatava numeerinen arvo on moninkertaisesti `decimals`-parametrin määrittämän arvo, ja se on lähimpänä `number`-parametrin määrittämää arvoa.</span><span class="sxs-lookup"><span data-stu-id="8071c-119">The resulting numeric value is a multiple of the value specified by the `decimals` parameter and is closest to the value specified by the `number` parameter.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8071c-120">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="8071c-120">Usage notes</span></span>

<span data-ttu-id="8071c-121">Kun `number`-parametri on nolla, funktio palauttaa aina nollan.</span><span class="sxs-lookup"><span data-stu-id="8071c-121">When the `number` parameter is zero, this function always returns zero.</span></span>

<span data-ttu-id="8071c-122">Kun `decimals`-parametri on nolla, funktio pyöristää oletusarvoisen pyöristysarvon.</span><span class="sxs-lookup"><span data-stu-id="8071c-122">When the `decimals` parameter is zero, this function rounds to the default round-off value.</span></span> <span data-ttu-id="8071c-123">Kun `round rule`-parametrin arvoksi on asetettu **RoundOffType.Ordinary**, oletuspyöristysarvo on **0,01**.</span><span class="sxs-lookup"><span data-stu-id="8071c-123">When the `round rule` parameter is set to **RoundOffType.Ordinary**, the default round-off value is **0.01**.</span></span> <span data-ttu-id="8071c-124">Muussa tapauksessa pyöristysarvon oletusarvo on **1,0**.</span><span class="sxs-lookup"><span data-stu-id="8071c-124">Otherwise, the default round-off value is **1.0**.</span></span>

<span data-ttu-id="8071c-125">Kun `round rule` -parametrin arvoksi on asetettu **RoundOffType.Ordinary**, tämä funktio pyöristää lähimpään pyöristysmäärään.</span><span class="sxs-lookup"><span data-stu-id="8071c-125">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function rounds to the nearest round-off amount.</span></span>

<span data-ttu-id="8071c-126">Kun `round rule` -parametrin arvoksi on asetettu **RoundOffType.RoundDown**, tämä funktio pyöristää kohti nollaa lähimpään pyöristysmäärään.</span><span class="sxs-lookup"><span data-stu-id="8071c-126">When the `round rule` parameter is set to **RoundOffType.RoundDown**, this function rounds towards zero to the nearest round-off amount.</span></span>

<span data-ttu-id="8071c-127">Kun `round rule` -parametrin arvoksi on asetettu **RoundOffType.RoundUp**, tämä funktio pyöristää pois nollasta lähimpään pyöristysmäärään.</span><span class="sxs-lookup"><span data-stu-id="8071c-127">When the `round rule` parameter is set to **RoundOffType.RoundUp**, this function rounds away from zero to the nearest round-off amount.</span></span>

<span data-ttu-id="8071c-128">Kun `round rule`-parametrin arvoksi on asetettu **RoundOffType.Ordinary**, tämä funktio käyttäytyy kuten [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel-funktio ja [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X + +-funktio.</span><span class="sxs-lookup"><span data-stu-id="8071c-128">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function behaves like the [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel function and the [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ function.</span></span>

## <a name="remarks"></a><span data-ttu-id="8071c-129">Huomautukset</span><span class="sxs-lookup"><span data-stu-id="8071c-129">Remarks</span></span>

<span data-ttu-id="8071c-130">Jos haluat pyöristää numeerisen arvon määritettyyn desimaalien määrään, käytä [ROUND](er-functions-mathematical-round.md)-funktiota.</span><span class="sxs-lookup"><span data-stu-id="8071c-130">To round a numeric value to a specified number of decimal places, use the [ROUND](er-functions-mathematical-round.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="8071c-131">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="8071c-131">Example</span></span>

<span data-ttu-id="8071c-132">Jos **model.RoundOff**-parametrin arvoksi on asetettu **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` palauttaa arvon 7,35.</span><span class="sxs-lookup"><span data-stu-id="8071c-132">If the **model.RoundOff** parameter is set to **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="8071c-133">Jos **model.RoundOff**-parametrin arvoksi on asetettu **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` palauttaa arvon 7,35.</span><span class="sxs-lookup"><span data-stu-id="8071c-133">If the **model.RoundOff** parameter is set to **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="8071c-134">Jos **model.RoundOff**-parametrin arvoksi on asetettu **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` palauttaa arvon 8,4.</span><span class="sxs-lookup"><span data-stu-id="8071c-134">If the **model.RoundOff** parameter is set to **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 8.4.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8071c-135">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8071c-135">Additional resources</span></span>

[<span data-ttu-id="8071c-136">Muut (liiketoiminnan toimialuekohtaiset) toiminnot</span><span class="sxs-lookup"><span data-stu-id="8071c-136">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

[<span data-ttu-id="8071c-137">Matemaattinen toiminto</span><span class="sxs-lookup"><span data-stu-id="8071c-137">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]