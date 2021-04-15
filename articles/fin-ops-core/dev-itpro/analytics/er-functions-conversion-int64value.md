---
title: INT64VALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) INT64VALUE-funktiota käytetään.
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
ms.openlocfilehash: 89a26e867579bcb34a9bae33fa0b98e1ecfe9995
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755393"
---
# <a name="int64value-er-function"></a><span data-ttu-id="190fc-103">INT64VALUE ER -funktio</span><span class="sxs-lookup"><span data-stu-id="190fc-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="190fc-104">`INT64VALUE`-funktio palauttaa *Int64*-arvon, joka edustaa määritettyä merkkijonoa.</span><span class="sxs-lookup"><span data-stu-id="190fc-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="190fc-105">Syntaksi 1</span><span class="sxs-lookup"><span data-stu-id="190fc-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="190fc-106">Syntaksi 2</span><span class="sxs-lookup"><span data-stu-id="190fc-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="190fc-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="190fc-107">Arguments</span></span>

<span data-ttu-id="190fc-108">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="190fc-108">`text`: *String*</span></span>

<span data-ttu-id="190fc-109">Tekstiarvo, jota ei pidä muuntaa *Int64*-numeroksi.</span><span class="sxs-lookup"><span data-stu-id="190fc-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="190fc-110">`number`: *Todellinen* tai *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="190fc-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="190fc-111">Numeerinen *todellinen* tai *kokonaisluku*-arvo, jota ei pidä muuntaa *Int64*-numeroksi.</span><span class="sxs-lookup"><span data-stu-id="190fc-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="190fc-112">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="190fc-112">Return values</span></span>

<span data-ttu-id="190fc-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="190fc-113">*Int64*</span></span>

<span data-ttu-id="190fc-114">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="190fc-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="190fc-115">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="190fc-115">Usage notes</span></span>

<span data-ttu-id="190fc-116">Kaikki desimaalit lyhennetään.</span><span class="sxs-lookup"><span data-stu-id="190fc-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="190fc-117">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="190fc-117">Example 1</span></span>

<span data-ttu-id="190fc-118">`INT64VALUE ("22565422744")` palauttaa *Int64*-arvon **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="190fc-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="190fc-119">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="190fc-119">Example 2</span></span>

<span data-ttu-id="190fc-120">`INT64VALUE ( VALUE("22565422744.77"))` palauttaa *Int64*-arvon **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="190fc-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="190fc-121">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="190fc-121">Additional resources</span></span>

[<span data-ttu-id="190fc-122">Tyypin muuntamisen toiminnot</span><span class="sxs-lookup"><span data-stu-id="190fc-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]