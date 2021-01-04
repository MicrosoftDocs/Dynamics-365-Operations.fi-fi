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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13884182cb986564e81f310993747997341ffc07
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682939"
---
# <a name="right-er-function"></a><span data-ttu-id="fb620-103">RIGHT ER-toiminto</span><span class="sxs-lookup"><span data-stu-id="fb620-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb620-104">`RIGHT`-funktio palauttaa määritetystä luettelosta *merkkijono*-arvon, joka esittää määritetyn määrän merkkejä määritetyn merkkijonon lopusta.</span><span class="sxs-lookup"><span data-stu-id="fb620-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb620-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="fb620-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="fb620-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="fb620-106">Arguments</span></span>

<span data-ttu-id="fb620-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="fb620-107">`text`: *String*</span></span>

<span data-ttu-id="fb620-108">*Merkkijono*-arvo, joka esittelee alkuperäisen tekstin.</span><span class="sxs-lookup"><span data-stu-id="fb620-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="fb620-109">`number`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="fb620-109">`number`: *Integer*</span></span>

<span data-ttu-id="fb620-110">Merkkien määrä, joka on palautettava alkuperäisen tekstin lopusta.</span><span class="sxs-lookup"><span data-stu-id="fb620-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="fb620-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="fb620-111">Return values</span></span>

<span data-ttu-id="fb620-112">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="fb620-112">*String*</span></span>

<span data-ttu-id="fb620-113">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="fb620-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="fb620-114">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="fb620-114">Example</span></span>

<span data-ttu-id="fb620-115">`RIGHT ("Sample", 3)` palauttaa arvon **ple**.</span><span class="sxs-lookup"><span data-stu-id="fb620-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fb620-116">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="fb620-116">Additional resources</span></span>

[<span data-ttu-id="fb620-117">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="fb620-117">Text functions</span></span>](er-functions-category-text.md)
