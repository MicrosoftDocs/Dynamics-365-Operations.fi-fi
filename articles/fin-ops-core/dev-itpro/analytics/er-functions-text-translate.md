---
title: TRANSLATE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) TRANSLATE-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 51b9a2e25a9f1dfc08e9e0f7fc3ad84b359a6d1b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744236"
---
# <a name="translate-er-function"></a><span data-ttu-id="43b35-103">TRANSLATE ER -funktio</span><span class="sxs-lookup"><span data-stu-id="43b35-103">TRANSLATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43b35-104">`TRANSLATE`-funktio palauttaa *Merkkijono*-arvon, joka sisältää määritetyn tekstin merkkien korvaamisen tuloksen toisen toimitetun joukon merkkeinä.</span><span class="sxs-lookup"><span data-stu-id="43b35-104">The `TRANSLATE` function returns a *String* value that contains the result of the character replacement of specified text in characters of another provided set.</span></span>

## <a name="syntax"></a><span data-ttu-id="43b35-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="43b35-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="43b35-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="43b35-106">Arguments</span></span>

<span data-ttu-id="43b35-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="43b35-107">`text`: *String*</span></span>

<span data-ttu-id="43b35-108">*Merkkijono*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="43b35-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="43b35-109">`pattern`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="43b35-109">`pattern`: *String*</span></span>

<span data-ttu-id="43b35-110">Teksti, joka tulee korvata.</span><span class="sxs-lookup"><span data-stu-id="43b35-110">The text that must be replaced.</span></span>

<span data-ttu-id="43b35-111">`replacement`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="43b35-111">`replacement`: *String*</span></span>

<span data-ttu-id="43b35-112">Korvaava teksti.</span><span class="sxs-lookup"><span data-stu-id="43b35-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="43b35-113">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="43b35-113">Return values</span></span>

<span data-ttu-id="43b35-114">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="43b35-114">*String*</span></span>

<span data-ttu-id="43b35-115">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="43b35-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="43b35-116">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="43b35-116">Usage notes</span></span>

<span data-ttu-id="43b35-117">`TRANSLATE`-toiminto korvaa yhden merkin kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="43b35-117">The `TRANSLATE` function replaces one character at a time.</span></span> <span data-ttu-id="43b35-118">Funktio korvaa `text`-argumentin ensimmäisen merkin `pattern`-argumentin ensimmäisellä merkillä ja sitten toisen merkin ja noudattaa samaa virtausarvoa, kunnes se on valmis.</span><span class="sxs-lookup"><span data-stu-id="43b35-118">The function replaces the first character of the `text` argument with the first character of the `pattern` argument and then the second character and follows the same flow until finished.</span></span> <span data-ttu-id="43b35-119">Kun `text`- ja `pattern`-argumenttien merkit ovat samat, ne korvataan `replacement`-argumentilla, joka sijaitsee samassa sijainnissa kuin `pattern`-argumentin merkki.</span><span class="sxs-lookup"><span data-stu-id="43b35-119">When a character from the `text` and `pattern` arguments match, it is replaced by a character from the `replacement` argument that is located in the same position as the character from the `pattern` argument.</span></span> <span data-ttu-id="43b35-120">Jos merkki esiintyy `pattern`-argumenttina useita kertoja, käytetään tämän merkin ensimmäistä esiintymää vastaavaa `replacement`-argumenttimääritystä.</span><span class="sxs-lookup"><span data-stu-id="43b35-120">If a character appears multiple times in the `pattern` argument, the `replacement` argument mapping that corresponds to the first occurrence of this character is used.</span></span>

## <a name="example-1"></a><span data-ttu-id="43b35-121">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="43b35-121">Example 1</span></span>

<span data-ttu-id="43b35-122">`TRANSLATE ("abcdef", "cd", "GH")` korvaa määritetyn **abcde**- tekstin **c**-merkin `replacement`-tekstin **G**-merkillä seuraavien seikkojen vuoksi:</span><span class="sxs-lookup"><span data-stu-id="43b35-122">`TRANSLATE ("abcdef", "cd", "GH")` replaces the **"c"** character of the specified  **“abcdef”** text with the **"G"** character of the `replacement` text due to the following:</span></span>
-   <span data-ttu-id="43b35-123">**c**-merkki esitetään ensimmäisessä kohdassa olevassa `pattern`-tekstissä.</span><span class="sxs-lookup"><span data-stu-id="43b35-123">The **"c"** character is presented in the `pattern` text in the first position.</span></span>
-   <span data-ttu-id="43b35-124">`replacement`-tekstin ensimmäinen kohta sisältää **G**-merkin.</span><span class="sxs-lookup"><span data-stu-id="43b35-124">The first position of the `replacement` text contains the **"G"** character.</span></span>

## <a name="example-2"></a><span data-ttu-id="43b35-125">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="43b35-125">Example 2</span></span>

<span data-ttu-id="43b35-126">`TRANSLATE ("abcdef", "ccd", "GH")`-funktio palauttaa arvon **abGdef**.</span><span class="sxs-lookup"><span data-stu-id="43b35-126">`TRANSLATE ("abcdef", "ccd", "GH")` returns **"abGdef"**.</span></span>

## <a name="example-3"></a><span data-ttu-id="43b35-127">Esimerkki 3</span><span class="sxs-lookup"><span data-stu-id="43b35-127">Example 3</span></span>

<span data-ttu-id="43b35-128">`TRANSLATE ("abccba", "abc", "123")` palauttaa **"123321"**.</span><span class="sxs-lookup"><span data-stu-id="43b35-128">`TRANSLATE ("abccba", "abc", "123")` returns **"123321"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="43b35-129">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="43b35-129">Additional resources</span></span>

[<span data-ttu-id="43b35-130">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="43b35-130">Text functions</span></span>](er-functions-category-text.md)
