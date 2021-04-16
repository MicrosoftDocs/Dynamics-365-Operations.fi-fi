---
title: NOT ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NOT-funktiota käytetään.
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
ms.openlocfilehash: 7c10ed61b97dcd4d4a66a530bb3d08c539659233
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751706"
---
# <a name="not-er-function"></a><span data-ttu-id="635a9-103">NOT ER -funktio</span><span class="sxs-lookup"><span data-stu-id="635a9-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="635a9-104">`NOT`-funktio palauttaa määritetyn ehdon käänteisen loogisen arvon *totuusarvoksi*.</span><span class="sxs-lookup"><span data-stu-id="635a9-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="635a9-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="635a9-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="635a9-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="635a9-106">Arguments</span></span>

<span data-ttu-id="635a9-107">`condition`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="635a9-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="635a9-108">Kelvollinen ehdollinen lauseke, joka on käännettävä.</span><span class="sxs-lookup"><span data-stu-id="635a9-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="635a9-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="635a9-109">Return values</span></span>

<span data-ttu-id="635a9-110">*Boolen arvo*</span><span class="sxs-lookup"><span data-stu-id="635a9-110">*Boolean*</span></span>

<span data-ttu-id="635a9-111">Tuloksena oleva *Totuusarvo*-arvo.</span><span class="sxs-lookup"><span data-stu-id="635a9-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="635a9-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="635a9-112">Example</span></span>

<span data-ttu-id="635a9-113">`NOT (TRUE)` palauttaa arvon **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="635a9-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="635a9-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="635a9-114">Additional resources</span></span>

[<span data-ttu-id="635a9-115">Loogiset toiminnot</span><span class="sxs-lookup"><span data-stu-id="635a9-115">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]