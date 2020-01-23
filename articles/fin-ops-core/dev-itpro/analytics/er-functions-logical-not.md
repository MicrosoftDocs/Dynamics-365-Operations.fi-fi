---
title: NOT ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NOT-funktiota käytetään.
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
ms.openlocfilehash: b15277dba26dc7864193b11a127944daca6b989f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916036"
---
# <span data-ttu-id="73933-103"><a name="NOT">NOT ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="73933-103"><a name="NOT">NOT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73933-104">`NOT`-funktio palauttaa määritetyn ehdon käänteisen loogisen arvon *totuusarvoksi*.</span><span class="sxs-lookup"><span data-stu-id="73933-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="73933-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="73933-105">Syntax</span></span>

```
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="73933-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="73933-106">Arguments</span></span>

<span data-ttu-id="73933-107">`condition`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="73933-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="73933-108">Kelvollinen ehdollinen lauseke, joka on käännettävä.</span><span class="sxs-lookup"><span data-stu-id="73933-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="73933-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="73933-109">Return values</span></span>

<span data-ttu-id="73933-110">*Boolen arvo*</span><span class="sxs-lookup"><span data-stu-id="73933-110">*Boolean*</span></span>

<span data-ttu-id="73933-111">Tuloksena oleva *Totuusarvo*-arvo.</span><span class="sxs-lookup"><span data-stu-id="73933-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="73933-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="73933-112">Example</span></span>

<span data-ttu-id="73933-113">`NOT (TRUE)` palauttaa arvon **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="73933-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73933-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="73933-114">Additional resources</span></span>

[<span data-ttu-id="73933-115">Loogiset toiminnot</span><span class="sxs-lookup"><span data-stu-id="73933-115">Logical functions</span></span>](er-functions-category-logical.md)
