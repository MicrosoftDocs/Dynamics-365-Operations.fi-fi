---
title: INTVALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) INTVALUE-funktiota käytetään.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 71eedde5a22f36a8a827824087633de32c00cc7d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755369"
---
# <a name="intvalue-er-function"></a><span data-ttu-id="af65e-103">INTVALUE ER -funktio</span><span class="sxs-lookup"><span data-stu-id="af65e-103">INTVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af65e-104">`INTVALUE`-funktio palauttaa *Int*-arvon, joka edustaa määritettyä merkkijonoa.</span><span class="sxs-lookup"><span data-stu-id="af65e-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="af65e-105">Syntaksi 1</span><span class="sxs-lookup"><span data-stu-id="af65e-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="af65e-106">Syntaksi 2</span><span class="sxs-lookup"><span data-stu-id="af65e-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="af65e-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="af65e-107">Arguments</span></span>

<span data-ttu-id="af65e-108">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="af65e-108">`text`: *String*</span></span>

<span data-ttu-id="af65e-109">Tekstiarvo, jota ei pidä muuntaa *Int*-numeroksi.</span><span class="sxs-lookup"><span data-stu-id="af65e-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="af65e-110">`number`: *Todellinen* tai *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="af65e-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="af65e-111">Numeerinen *todellinen* tai *kokonaisluku*-arvo, jota ei pidä muuntaa *Int*-numeroksi.</span><span class="sxs-lookup"><span data-stu-id="af65e-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="af65e-112">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="af65e-112">Return values</span></span>

<span data-ttu-id="af65e-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="af65e-113">*Int*</span></span>

<span data-ttu-id="af65e-114">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="af65e-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="af65e-115">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="af65e-115">Usage notes</span></span>

<span data-ttu-id="af65e-116">Kaikki desimaalit lyhennetään.</span><span class="sxs-lookup"><span data-stu-id="af65e-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="af65e-117">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="af65e-117">Example 1</span></span>

<span data-ttu-id="af65e-118">`INTVALUE ("100.77")` palauttaa *Int*-arvon **100**.</span><span class="sxs-lookup"><span data-stu-id="af65e-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="af65e-119">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="af65e-119">Example 2</span></span>

<span data-ttu-id="af65e-120">`INTVALUE (-100.77)` palauttaa *Int*-arvon **-100**.</span><span class="sxs-lookup"><span data-stu-id="af65e-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="af65e-121">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="af65e-121">Additional resources</span></span>

[<span data-ttu-id="af65e-122">Tyypin muuntamisen toiminnot</span><span class="sxs-lookup"><span data-stu-id="af65e-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]