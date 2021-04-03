---
title: RIGHT ER-toiminto
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) RIGHT-funktiota käytetään.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 75255eccf4da468b0946253f7570b1621f905cd7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570237"
---
# <a name="right-er-function"></a><span data-ttu-id="310ea-103">RIGHT ER-toiminto</span><span class="sxs-lookup"><span data-stu-id="310ea-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="310ea-104">`RIGHT`-funktio palauttaa määritetystä luettelosta *merkkijono*-arvon, joka esittää määritetyn määrän merkkejä määritetyn merkkijonon lopusta.</span><span class="sxs-lookup"><span data-stu-id="310ea-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="310ea-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="310ea-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="310ea-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="310ea-106">Arguments</span></span>

<span data-ttu-id="310ea-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="310ea-107">`text`: *String*</span></span>

<span data-ttu-id="310ea-108">*Merkkijono*-arvo, joka esittelee alkuperäisen tekstin.</span><span class="sxs-lookup"><span data-stu-id="310ea-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="310ea-109">`number`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="310ea-109">`number`: *Integer*</span></span>

<span data-ttu-id="310ea-110">Merkkien määrä, joka on palautettava alkuperäisen tekstin lopusta.</span><span class="sxs-lookup"><span data-stu-id="310ea-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="310ea-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="310ea-111">Return values</span></span>

<span data-ttu-id="310ea-112">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="310ea-112">*String*</span></span>

<span data-ttu-id="310ea-113">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="310ea-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="310ea-114">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="310ea-114">Example</span></span>

<span data-ttu-id="310ea-115">`RIGHT ("Sample", 3)` palauttaa arvon **ple**.</span><span class="sxs-lookup"><span data-stu-id="310ea-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="310ea-116">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="310ea-116">Additional resources</span></span>

[<span data-ttu-id="310ea-117">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="310ea-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]