---
title: LEFT ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) LEFT-funktiota käytetään.
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: 69b1d95ea0e82b1947b665b0724cff6c5b319633
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746336"
---
# <a name="left-er-function"></a><span data-ttu-id="44cb1-103">LEFT ER -funktio</span><span class="sxs-lookup"><span data-stu-id="44cb1-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44cb1-104">`LEFT`-funktio palauttaa määritetystä luettelosta *merkkijono*-arvon, joka esittää määritetyn määrän merkkejä määritetyn merkkijonon alusta.</span><span class="sxs-lookup"><span data-stu-id="44cb1-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="44cb1-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="44cb1-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="44cb1-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="44cb1-106">Arguments</span></span>

<span data-ttu-id="44cb1-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="44cb1-107">`text`: *String*</span></span>

<span data-ttu-id="44cb1-108">*Merkkijono*-arvo, joka esittelee alkuperäisen tekstin.</span><span class="sxs-lookup"><span data-stu-id="44cb1-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="44cb1-109">`number`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="44cb1-109">`number`: *Integer*</span></span>

<span data-ttu-id="44cb1-110">Merkkien määrä, joka on palautettava alkuperäisen tekstin alusta.</span><span class="sxs-lookup"><span data-stu-id="44cb1-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="44cb1-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="44cb1-111">Return values</span></span>

<span data-ttu-id="44cb1-112">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="44cb1-112">*String*</span></span>

<span data-ttu-id="44cb1-113">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="44cb1-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="44cb1-114">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="44cb1-114">Example</span></span>

<span data-ttu-id="44cb1-115">`LEFT ("Sample", 3)` palauttaa arvon **Sam**.</span><span class="sxs-lookup"><span data-stu-id="44cb1-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="44cb1-116">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="44cb1-116">Additional resources</span></span>

[<span data-ttu-id="44cb1-117">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="44cb1-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]