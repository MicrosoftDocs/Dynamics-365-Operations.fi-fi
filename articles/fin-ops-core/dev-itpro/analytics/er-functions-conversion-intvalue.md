---
title: INTVALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) INTVALUE-funktiota käytetään.
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
ms.openlocfilehash: 98b91a983c60bb99280763f7f7a944d08f535e60
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686000"
---
# <a name="intvalue-er-function"></a><span data-ttu-id="74f86-103">INTVALUE ER -funktio</span><span class="sxs-lookup"><span data-stu-id="74f86-103">INTVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74f86-104">`INTVALUE`-funktio palauttaa *Int*-arvon, joka edustaa määritettyä merkkijonoa.</span><span class="sxs-lookup"><span data-stu-id="74f86-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="74f86-105">Syntaksi 1</span><span class="sxs-lookup"><span data-stu-id="74f86-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="74f86-106">Syntaksi 2</span><span class="sxs-lookup"><span data-stu-id="74f86-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="74f86-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="74f86-107">Arguments</span></span>

<span data-ttu-id="74f86-108">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="74f86-108">`text`: *String*</span></span>

<span data-ttu-id="74f86-109">Tekstiarvo, jota ei pidä muuntaa *Int*-numeroksi.</span><span class="sxs-lookup"><span data-stu-id="74f86-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="74f86-110">`number`: *Todellinen* tai *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="74f86-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="74f86-111">Numeerinen *todellinen* tai *kokonaisluku*-arvo, jota ei pidä muuntaa *Int*-numeroksi.</span><span class="sxs-lookup"><span data-stu-id="74f86-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="74f86-112">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="74f86-112">Return values</span></span>

<span data-ttu-id="74f86-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="74f86-113">*Int*</span></span>

<span data-ttu-id="74f86-114">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="74f86-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="74f86-115">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="74f86-115">Usage notes</span></span>

<span data-ttu-id="74f86-116">Kaikki desimaalit lyhennetään.</span><span class="sxs-lookup"><span data-stu-id="74f86-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="74f86-117">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="74f86-117">Example 1</span></span>

<span data-ttu-id="74f86-118">`INTVALUE ("100.77")` palauttaa *Int*-arvon **100**.</span><span class="sxs-lookup"><span data-stu-id="74f86-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="74f86-119">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="74f86-119">Example 2</span></span>

<span data-ttu-id="74f86-120">`INTVALUE (-100.77)` palauttaa *Int*-arvon **-100**.</span><span class="sxs-lookup"><span data-stu-id="74f86-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="74f86-121">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="74f86-121">Additional resources</span></span>

[<span data-ttu-id="74f86-122">Tyypin muuntamisen toiminnot</span><span class="sxs-lookup"><span data-stu-id="74f86-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
