---
title: RIGHT ER-toiminto
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) RIGHT-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 01718f9b153c1d6c46d50a9b17e899ccfba16915
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916726"
---
# <span data-ttu-id="c7c35-103"><a name="RIGHT">RIGHT ER-toiminto</a></span><span class="sxs-lookup"><span data-stu-id="c7c35-103"><a name="RIGHT">RIGHT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7c35-104">`RIGHT`-funktio palauttaa määritetystä luettelosta *merkkijono*-arvon, joka esittää määritetyn määrän merkkejä määritetyn merkkijonon lopusta.</span><span class="sxs-lookup"><span data-stu-id="c7c35-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c35-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="c7c35-105">Syntax</span></span>

```
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="c7c35-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="c7c35-106">Arguments</span></span>

<span data-ttu-id="c7c35-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="c7c35-107">`text`: *String*</span></span>

<span data-ttu-id="c7c35-108">*Merkkijono*-arvo, joka esittelee alkuperäisen tekstin.</span><span class="sxs-lookup"><span data-stu-id="c7c35-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="c7c35-109">`number`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="c7c35-109">`number`: *Integer*</span></span>

<span data-ttu-id="c7c35-110">Merkkien määrä, joka on palautettava alkuperäisen tekstin lopusta.</span><span class="sxs-lookup"><span data-stu-id="c7c35-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="c7c35-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="c7c35-111">Return values</span></span>

<span data-ttu-id="c7c35-112">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="c7c35-112">*String*</span></span>

<span data-ttu-id="c7c35-113">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="c7c35-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c7c35-114">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="c7c35-114">Example</span></span>

<span data-ttu-id="c7c35-115">`RIGHT ("Sample", 3)` palauttaa arvon **ple**.</span><span class="sxs-lookup"><span data-stu-id="c7c35-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c7c35-116">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c7c35-116">Additional resources</span></span>

[<span data-ttu-id="c7c35-117">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="c7c35-117">Text functions</span></span>](er-functions-category-text.md)
