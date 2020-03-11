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
ms.openlocfilehash: a518f255a4488c5ed6e007b1787e678fd88aff36
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041719"
---
# <span data-ttu-id="a0ed0-103"><a name="NOT">NOT ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="a0ed0-103"><a name="NOT">NOT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0ed0-104">`NOT`-funktio palauttaa määritetyn ehdon käänteisen loogisen arvon *totuusarvoksi*.</span><span class="sxs-lookup"><span data-stu-id="a0ed0-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0ed0-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="a0ed0-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="a0ed0-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="a0ed0-106">Arguments</span></span>

<span data-ttu-id="a0ed0-107">`condition`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="a0ed0-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="a0ed0-108">Kelvollinen ehdollinen lauseke, joka on käännettävä.</span><span class="sxs-lookup"><span data-stu-id="a0ed0-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="a0ed0-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="a0ed0-109">Return values</span></span>

<span data-ttu-id="a0ed0-110">*Boolen arvo*</span><span class="sxs-lookup"><span data-stu-id="a0ed0-110">*Boolean*</span></span>

<span data-ttu-id="a0ed0-111">Tuloksena oleva *Totuusarvo*-arvo.</span><span class="sxs-lookup"><span data-stu-id="a0ed0-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="a0ed0-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="a0ed0-112">Example</span></span>

<span data-ttu-id="a0ed0-113">`NOT (TRUE)` palauttaa arvon **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="a0ed0-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a0ed0-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a0ed0-114">Additional resources</span></span>

[<span data-ttu-id="a0ed0-115">Loogiset toiminnot</span><span class="sxs-lookup"><span data-stu-id="a0ed0-115">Logical functions</span></span>](er-functions-category-logical.md)
