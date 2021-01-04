---
title: LEN ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) LEN-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 8d766b8effa9d6936de7a3def252536603330965
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680358"
---
# <a name="len-er-function"></a><span data-ttu-id="7ff24-103">LEN ER -funktio</span><span class="sxs-lookup"><span data-stu-id="7ff24-103">LEN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ff24-104">`LEN`-funktio palauttaa määritetystä luettelosta *Kokonaisluku*-arvon, joka esittää merkkien määrän määritetyssä merkkijonossa.</span><span class="sxs-lookup"><span data-stu-id="7ff24-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ff24-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="7ff24-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="7ff24-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="7ff24-106">Arguments</span></span>

<span data-ttu-id="7ff24-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="7ff24-107">`text`: *String*</span></span>

<span data-ttu-id="7ff24-108">*Merkkijono*-arvo, joka määrittää tekstin.</span><span class="sxs-lookup"><span data-stu-id="7ff24-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="7ff24-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="7ff24-109">Return values</span></span>

<span data-ttu-id="7ff24-110">*Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="7ff24-110">*Integer*</span></span>

<span data-ttu-id="7ff24-111">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="7ff24-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="7ff24-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="7ff24-112">Example</span></span>

<span data-ttu-id="7ff24-113">`LEN ("Sample")` palauttaa **6**.</span><span class="sxs-lookup"><span data-stu-id="7ff24-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7ff24-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="7ff24-114">Additional resources</span></span>

[<span data-ttu-id="7ff24-115">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="7ff24-115">Text functions</span></span>](er-functions-category-text.md)
