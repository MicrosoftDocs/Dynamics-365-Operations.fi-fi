---
title: DAYOFYEAR ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) DAYOFYEAR-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: b9b937e7fae3e90d1a87196fab653dfac8e94179
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682386"
---
# <a name="dayofyear-er-function"></a><span data-ttu-id="b088d-103">DAYOFYEAR ER-funktio</span><span class="sxs-lookup"><span data-stu-id="b088d-103">DAYOFYEAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b088d-104">`DAYOFYEAR`-toiminto palauttaa tammikuun 1. päivän ja määritetyn päivämäärän välisten päivien määrää kuvaavan arvon *kokonaislukuna*.</span><span class="sxs-lookup"><span data-stu-id="b088d-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="b088d-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="b088d-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="b088d-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="b088d-106">Arguments</span></span>

<span data-ttu-id="b088d-107">`date`: *Päivämäärä*</span><span class="sxs-lookup"><span data-stu-id="b088d-107">`date`: *Date*</span></span>

<span data-ttu-id="b088d-108">Päivämääräarvo, joka ilmaisee päivien määrän laskennassa käytettävää päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="b088d-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="b088d-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="b088d-109">Return values</span></span>

<span data-ttu-id="b088d-110">*Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="b088d-110">*Integer*</span></span>

<span data-ttu-id="b088d-111">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="b088d-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="b088d-112">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="b088d-112">Example 1</span></span>

<span data-ttu-id="b088d-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` palauttaa **61**.</span><span class="sxs-lookup"><span data-stu-id="b088d-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b088d-114">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="b088d-114">Example 2</span></span>

<span data-ttu-id="b088d-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` palauttaa **1**.</span><span class="sxs-lookup"><span data-stu-id="b088d-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b088d-116">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b088d-116">Additional resources</span></span>

[<span data-ttu-id="b088d-117">Päivämäärä- ja aikatoiminnot</span><span class="sxs-lookup"><span data-stu-id="b088d-117">Date and time functions</span></span>](er-functions-category-datetime.md)
