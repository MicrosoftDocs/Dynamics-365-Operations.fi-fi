---
title: ISVALIDCHARACTERISO7064 ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ISVALIDCHARACTERISO7064-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: c3bceb15bbe1dc65abc88c1229459707a6166482
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680659"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="5a71a-103">ISVALIDCHARACTERISO7064 ER -funktio</span><span class="sxs-lookup"><span data-stu-id="5a71a-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a71a-104">`ISVALIDCHARACTERISO7064`-funktio palauttaa *totuusarvon* **TOSI**, jos määritetty merkkijono vastaa kelvollista kansainvälistä tilinumeroa (IBAN).</span><span class="sxs-lookup"><span data-stu-id="5a71a-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="5a71a-105">Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="5a71a-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a71a-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="5a71a-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="5a71a-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="5a71a-107">Arguments</span></span>

<span data-ttu-id="5a71a-108">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="5a71a-108">`text`: *String*</span></span>

<span data-ttu-id="5a71a-109">Tekstiarvo, joka edustaa IBAN-arvoa.</span><span class="sxs-lookup"><span data-stu-id="5a71a-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="5a71a-110">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="5a71a-110">Return values</span></span>

<span data-ttu-id="5a71a-111">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="5a71a-111">*String*</span></span>

<span data-ttu-id="5a71a-112">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="5a71a-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="5a71a-113">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="5a71a-113">Example</span></span>

<span data-ttu-id="5a71a-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` palauttaa arvon **TOSI**.</span><span class="sxs-lookup"><span data-stu-id="5a71a-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="5a71a-115">`ISVALIDCHARACTERISO7064 ("AT61")` palauttaa arvon **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="5a71a-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5a71a-116">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="5a71a-116">Additional resources</span></span>

[<span data-ttu-id="5a71a-117">Muut (liiketoiminnan toimialuekohtaiset) toiminnot</span><span class="sxs-lookup"><span data-stu-id="5a71a-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
