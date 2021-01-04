---
title: INT64VALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) INT64VALUE-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: bb750116312df82448f5a0048e380f9e5274f8e9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686047"
---
# <a name="int64value-er-function"></a><span data-ttu-id="489e0-103">INT64VALUE ER -funktio</span><span class="sxs-lookup"><span data-stu-id="489e0-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="489e0-104">`INT64VALUE`-funktio palauttaa *Int64*-arvon, joka edustaa määritettyä merkkijonoa.</span><span class="sxs-lookup"><span data-stu-id="489e0-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="489e0-105">Syntaksi 1</span><span class="sxs-lookup"><span data-stu-id="489e0-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="489e0-106">Syntaksi 2</span><span class="sxs-lookup"><span data-stu-id="489e0-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="489e0-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="489e0-107">Arguments</span></span>

<span data-ttu-id="489e0-108">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="489e0-108">`text`: *String*</span></span>

<span data-ttu-id="489e0-109">Tekstiarvo, jota ei pidä muuntaa *Int64*-numeroksi.</span><span class="sxs-lookup"><span data-stu-id="489e0-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="489e0-110">`number`: *Todellinen* tai *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="489e0-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="489e0-111">Numeerinen *todellinen* tai *kokonaisluku*-arvo, jota ei pidä muuntaa *Int64*-numeroksi.</span><span class="sxs-lookup"><span data-stu-id="489e0-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="489e0-112">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="489e0-112">Return values</span></span>

<span data-ttu-id="489e0-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="489e0-113">*Int64*</span></span>

<span data-ttu-id="489e0-114">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="489e0-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="489e0-115">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="489e0-115">Usage notes</span></span>

<span data-ttu-id="489e0-116">Kaikki desimaalit lyhennetään.</span><span class="sxs-lookup"><span data-stu-id="489e0-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="489e0-117">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="489e0-117">Example 1</span></span>

<span data-ttu-id="489e0-118">`INT64VALUE ("22565422744")` palauttaa *Int64*-arvon **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="489e0-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="489e0-119">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="489e0-119">Example 2</span></span>

<span data-ttu-id="489e0-120">`INT64VALUE ( VALUE("22565422744.77"))` palauttaa *Int64*-arvon **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="489e0-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="489e0-121">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="489e0-121">Additional resources</span></span>

[<span data-ttu-id="489e0-122">Tyypin muuntamisen toiminnot</span><span class="sxs-lookup"><span data-stu-id="489e0-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
