---
title: RIGHT ER-toiminto
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) RIGHT-funktiota käytetään.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: f59b12f0b3f7b100b953b2072677c83c836746ff
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746120"
---
# <a name="right-er-function"></a><span data-ttu-id="76ca8-103">RIGHT ER-toiminto</span><span class="sxs-lookup"><span data-stu-id="76ca8-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76ca8-104">`RIGHT`-funktio palauttaa määritetystä luettelosta *merkkijono*-arvon, joka esittää määritetyn määrän merkkejä määritetyn merkkijonon lopusta.</span><span class="sxs-lookup"><span data-stu-id="76ca8-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="76ca8-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="76ca8-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="76ca8-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="76ca8-106">Arguments</span></span>

<span data-ttu-id="76ca8-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="76ca8-107">`text`: *String*</span></span>

<span data-ttu-id="76ca8-108">*Merkkijono*-arvo, joka esittelee alkuperäisen tekstin.</span><span class="sxs-lookup"><span data-stu-id="76ca8-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="76ca8-109">`number`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="76ca8-109">`number`: *Integer*</span></span>

<span data-ttu-id="76ca8-110">Merkkien määrä, joka on palautettava alkuperäisen tekstin lopusta.</span><span class="sxs-lookup"><span data-stu-id="76ca8-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="76ca8-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="76ca8-111">Return values</span></span>

<span data-ttu-id="76ca8-112">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="76ca8-112">*String*</span></span>

<span data-ttu-id="76ca8-113">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="76ca8-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="76ca8-114">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="76ca8-114">Example</span></span>

<span data-ttu-id="76ca8-115">`RIGHT ("Sample", 3)` palauttaa arvon **ple**.</span><span class="sxs-lookup"><span data-stu-id="76ca8-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="76ca8-116">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="76ca8-116">Additional resources</span></span>

[<span data-ttu-id="76ca8-117">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="76ca8-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]