---
title: LEFT ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) LEFT-funktiota käytetään.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 6f1ec7a21a16c3a34bed9779b05f20f21815ab9d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569989"
---
# <a name="left-er-function"></a><span data-ttu-id="2c337-103">LEFT ER -funktio</span><span class="sxs-lookup"><span data-stu-id="2c337-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c337-104">`LEFT`-funktio palauttaa määritetystä luettelosta *merkkijono*-arvon, joka esittää määritetyn määrän merkkejä määritetyn merkkijonon alusta.</span><span class="sxs-lookup"><span data-stu-id="2c337-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c337-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="2c337-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="2c337-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="2c337-106">Arguments</span></span>

<span data-ttu-id="2c337-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="2c337-107">`text`: *String*</span></span>

<span data-ttu-id="2c337-108">*Merkkijono*-arvo, joka esittelee alkuperäisen tekstin.</span><span class="sxs-lookup"><span data-stu-id="2c337-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="2c337-109">`number`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="2c337-109">`number`: *Integer*</span></span>

<span data-ttu-id="2c337-110">Merkkien määrä, joka on palautettava alkuperäisen tekstin alusta.</span><span class="sxs-lookup"><span data-stu-id="2c337-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="2c337-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="2c337-111">Return values</span></span>

<span data-ttu-id="2c337-112">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="2c337-112">*String*</span></span>

<span data-ttu-id="2c337-113">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="2c337-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="2c337-114">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="2c337-114">Example</span></span>

<span data-ttu-id="2c337-115">`LEFT ("Sample", 3)` palauttaa arvon **Sam**.</span><span class="sxs-lookup"><span data-stu-id="2c337-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c337-116">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2c337-116">Additional resources</span></span>

[<span data-ttu-id="2c337-117">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="2c337-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]