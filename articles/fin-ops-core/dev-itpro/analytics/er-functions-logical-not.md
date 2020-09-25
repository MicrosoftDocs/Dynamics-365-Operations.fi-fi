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
ms.openlocfilehash: af588c3714069040fa339d3121e6eb404b9be979
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744644"
---
# <a name="not-er-function"></a><span data-ttu-id="3920e-103">NOT ER -funktio</span><span class="sxs-lookup"><span data-stu-id="3920e-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3920e-104">`NOT`-funktio palauttaa määritetyn ehdon käänteisen loogisen arvon *totuusarvoksi*.</span><span class="sxs-lookup"><span data-stu-id="3920e-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3920e-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="3920e-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="3920e-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="3920e-106">Arguments</span></span>

<span data-ttu-id="3920e-107">`condition`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="3920e-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="3920e-108">Kelvollinen ehdollinen lauseke, joka on käännettävä.</span><span class="sxs-lookup"><span data-stu-id="3920e-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="3920e-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="3920e-109">Return values</span></span>

<span data-ttu-id="3920e-110">*Boolen arvo*</span><span class="sxs-lookup"><span data-stu-id="3920e-110">*Boolean*</span></span>

<span data-ttu-id="3920e-111">Tuloksena oleva *Totuusarvo*-arvo.</span><span class="sxs-lookup"><span data-stu-id="3920e-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="3920e-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="3920e-112">Example</span></span>

<span data-ttu-id="3920e-113">`NOT (TRUE)` palauttaa arvon **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="3920e-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3920e-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="3920e-114">Additional resources</span></span>

[<span data-ttu-id="3920e-115">Loogiset toiminnot</span><span class="sxs-lookup"><span data-stu-id="3920e-115">Logical functions</span></span>](er-functions-category-logical.md)
