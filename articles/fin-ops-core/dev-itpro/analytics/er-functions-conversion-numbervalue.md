---
title: NUMBERVALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NUMBERVALUE-funktiota käytetään.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6eeb66f4206eb39141a5b2573fcb9d15428ae52a
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042649"
---
# <span data-ttu-id="28b38-103"><a name="NUMBERVALUE">NUMBERVALUE ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="28b38-103"><a name="NUMBERVALUE">NUMBERVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28b38-104">`NUMBERVALUE`-funktio palauttaa *todellisen* arvon, joka muunnetaan määritetystä *merkkiarvosta*.</span><span class="sxs-lookup"><span data-stu-id="28b38-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="28b38-105">Muuntamisen aikana otetaan huomioon määritetyt desimaali- ja numeroryhmittelyerottimet.</span><span class="sxs-lookup"><span data-stu-id="28b38-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="28b38-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="28b38-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="28b38-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="28b38-107">Arguments</span></span>

<span data-ttu-id="28b38-108">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="28b38-108">`text`: *String*</span></span>

<span data-ttu-id="28b38-109">Tekstiarvo, jota ei pidä muuntaa *todelliseksi* numeroksi.</span><span class="sxs-lookup"><span data-stu-id="28b38-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="28b38-110">`decimal separator`: Merkkijono</span><span class="sxs-lookup"><span data-stu-id="28b38-110">`decimal separator`: String</span></span>

<span data-ttu-id="28b38-111">Desimaalierotin.</span><span class="sxs-lookup"><span data-stu-id="28b38-111">A decimal separator.</span></span> <span data-ttu-id="28b38-112">Sitä käytetään erottamaan desimaaliluvun kokonaisluku ja murto-osat.</span><span class="sxs-lookup"><span data-stu-id="28b38-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="28b38-113">`digit grouping separator`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="28b38-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="28b38-114">Numeroiden ryhmittelyerotin.</span><span class="sxs-lookup"><span data-stu-id="28b38-114">A digit grouping separator.</span></span> <span data-ttu-id="28b38-115">Sitä käytetään tuhaterottimena.</span><span class="sxs-lookup"><span data-stu-id="28b38-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="28b38-116">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="28b38-116">Return values</span></span>

<span data-ttu-id="28b38-117">*Reaaliluku*</span><span class="sxs-lookup"><span data-stu-id="28b38-117">*Real*</span></span>

<span data-ttu-id="28b38-118">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="28b38-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="28b38-119">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="28b38-119">Example</span></span>

<span data-ttu-id="28b38-120">`NUMBERVALUE( "1 234,56", ",", " ")` palauttaa **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="28b38-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="28b38-121">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="28b38-121">Additional resources</span></span>

[<span data-ttu-id="28b38-122">Tyypin muuntamisen toiminnot</span><span class="sxs-lookup"><span data-stu-id="28b38-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
