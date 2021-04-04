---
title: NUMBERVALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NUMBERVALUE-funktiota käytetään.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: f542621c4bcc29e03d8c92b0c700e2c80c9846f6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561419"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="f06dd-103">NUMBERVALUE ER -funktio</span><span class="sxs-lookup"><span data-stu-id="f06dd-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f06dd-104">`NUMBERVALUE`-funktio palauttaa *todellisen* arvon, joka muunnetaan määritetystä *merkkiarvosta*.</span><span class="sxs-lookup"><span data-stu-id="f06dd-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="f06dd-105">Muuntamisen aikana otetaan huomioon määritetyt desimaali- ja numeroryhmittelyerottimet.</span><span class="sxs-lookup"><span data-stu-id="f06dd-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="f06dd-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="f06dd-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="f06dd-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="f06dd-107">Arguments</span></span>

<span data-ttu-id="f06dd-108">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="f06dd-108">`text`: *String*</span></span>

<span data-ttu-id="f06dd-109">Tekstiarvo, jota ei pidä muuntaa *todelliseksi* numeroksi.</span><span class="sxs-lookup"><span data-stu-id="f06dd-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="f06dd-110">`decimal separator`: Merkkijono</span><span class="sxs-lookup"><span data-stu-id="f06dd-110">`decimal separator`: String</span></span>

<span data-ttu-id="f06dd-111">Desimaalierotin.</span><span class="sxs-lookup"><span data-stu-id="f06dd-111">A decimal separator.</span></span> <span data-ttu-id="f06dd-112">Sitä käytetään erottamaan desimaaliluvun kokonaisluku ja murto-osat.</span><span class="sxs-lookup"><span data-stu-id="f06dd-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="f06dd-113">`digit grouping separator`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="f06dd-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="f06dd-114">Numeroiden ryhmittelyerotin.</span><span class="sxs-lookup"><span data-stu-id="f06dd-114">A digit grouping separator.</span></span> <span data-ttu-id="f06dd-115">Sitä käytetään tuhaterottimena.</span><span class="sxs-lookup"><span data-stu-id="f06dd-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="f06dd-116">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="f06dd-116">Return values</span></span>

<span data-ttu-id="f06dd-117">*Reaaliluku*</span><span class="sxs-lookup"><span data-stu-id="f06dd-117">*Real*</span></span>

<span data-ttu-id="f06dd-118">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="f06dd-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="f06dd-119">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="f06dd-119">Example</span></span>

<span data-ttu-id="f06dd-120">`NUMBERVALUE( "1 234,56", ",", " ")` palauttaa **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="f06dd-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f06dd-121">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f06dd-121">Additional resources</span></span>

[<span data-ttu-id="f06dd-122">Tyypin muuntamisen toiminnot</span><span class="sxs-lookup"><span data-stu-id="f06dd-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]