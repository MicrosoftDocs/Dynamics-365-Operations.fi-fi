---
title: TRANSLATE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) TRANSLATE-funktiota käytetään.
author: NickSelin
ms.date: 04/02/2020
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
ms.openlocfilehash: 7e4d6417757e27190ab7cabf2bf01243bb87b55c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746070"
---
# <a name="translate-er-function"></a><span data-ttu-id="db7e7-103">TRANSLATE ER -funktio</span><span class="sxs-lookup"><span data-stu-id="db7e7-103">TRANSLATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db7e7-104">`TRANSLATE`-funktio palauttaa *Merkkijono*-arvon, joka sisältää määritetyn tekstin merkkien korvaamisen tuloksen toisen toimitetun joukon merkkeinä.</span><span class="sxs-lookup"><span data-stu-id="db7e7-104">The `TRANSLATE` function returns a *String* value that contains the result of the character replacement of specified text in characters of another provided set.</span></span>

## <a name="syntax"></a><span data-ttu-id="db7e7-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="db7e7-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="db7e7-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="db7e7-106">Arguments</span></span>

<span data-ttu-id="db7e7-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="db7e7-107">`text`: *String*</span></span>

<span data-ttu-id="db7e7-108">*Merkkijono*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="db7e7-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="db7e7-109">`pattern`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="db7e7-109">`pattern`: *String*</span></span>

<span data-ttu-id="db7e7-110">Teksti, joka tulee korvata.</span><span class="sxs-lookup"><span data-stu-id="db7e7-110">The text that must be replaced.</span></span>

<span data-ttu-id="db7e7-111">`replacement`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="db7e7-111">`replacement`: *String*</span></span>

<span data-ttu-id="db7e7-112">Korvaava teksti.</span><span class="sxs-lookup"><span data-stu-id="db7e7-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="db7e7-113">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="db7e7-113">Return values</span></span>

<span data-ttu-id="db7e7-114">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="db7e7-114">*String*</span></span>

<span data-ttu-id="db7e7-115">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="db7e7-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="db7e7-116">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="db7e7-116">Usage notes</span></span>

<span data-ttu-id="db7e7-117">`TRANSLATE`-toiminto korvaa yhden merkin kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="db7e7-117">The `TRANSLATE` function replaces one character at a time.</span></span> <span data-ttu-id="db7e7-118">Funktio korvaa `text`-argumentin ensimmäisen merkin `pattern`-argumentin ensimmäisellä merkillä ja sitten toisen merkin ja noudattaa samaa virtausarvoa, kunnes se on valmis.</span><span class="sxs-lookup"><span data-stu-id="db7e7-118">The function replaces the first character of the `text` argument with the first character of the `pattern` argument and then the second character and follows the same flow until finished.</span></span> <span data-ttu-id="db7e7-119">Kun `text`- ja `pattern`-argumenttien merkit ovat samat, ne korvataan `replacement`-argumentilla, joka sijaitsee samassa sijainnissa kuin `pattern`-argumentin merkki.</span><span class="sxs-lookup"><span data-stu-id="db7e7-119">When a character from the `text` and `pattern` arguments match, it is replaced by a character from the `replacement` argument that is located in the same position as the character from the `pattern` argument.</span></span> <span data-ttu-id="db7e7-120">Jos merkki esiintyy `pattern`-argumenttina useita kertoja, käytetään tämän merkin ensimmäistä esiintymää vastaavaa `replacement`-argumenttimääritystä.</span><span class="sxs-lookup"><span data-stu-id="db7e7-120">If a character appears multiple times in the `pattern` argument, the `replacement` argument mapping that corresponds to the first occurrence of this character is used.</span></span>

## <a name="example-1"></a><span data-ttu-id="db7e7-121">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="db7e7-121">Example 1</span></span>

<span data-ttu-id="db7e7-122">`TRANSLATE ("abcdef", "cd", "GH")` korvaa määritetyn **abcde**- tekstin **c**-merkin `replacement`-tekstin **G**-merkillä seuraavien seikkojen vuoksi:</span><span class="sxs-lookup"><span data-stu-id="db7e7-122">`TRANSLATE ("abcdef", "cd", "GH")` replaces the **"c"** character of the specified  **“abcdef”** text with the **"G"** character of the `replacement` text due to the following:</span></span>
-   <span data-ttu-id="db7e7-123">**c**-merkki esitetään ensimmäisessä kohdassa olevassa `pattern`-tekstissä.</span><span class="sxs-lookup"><span data-stu-id="db7e7-123">The **"c"** character is presented in the `pattern` text in the first position.</span></span>
-   <span data-ttu-id="db7e7-124">`replacement`-tekstin ensimmäinen kohta sisältää **G**-merkin.</span><span class="sxs-lookup"><span data-stu-id="db7e7-124">The first position of the `replacement` text contains the **"G"** character.</span></span>

## <a name="example-2"></a><span data-ttu-id="db7e7-125">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="db7e7-125">Example 2</span></span>

<span data-ttu-id="db7e7-126">`TRANSLATE ("abcdef", "ccd", "GH")`-funktio palauttaa arvon **abGdef**.</span><span class="sxs-lookup"><span data-stu-id="db7e7-126">`TRANSLATE ("abcdef", "ccd", "GH")` returns **"abGdef"**.</span></span>

## <a name="example-3"></a><span data-ttu-id="db7e7-127">Esimerkki 3</span><span class="sxs-lookup"><span data-stu-id="db7e7-127">Example 3</span></span>

<span data-ttu-id="db7e7-128">`TRANSLATE ("abccba", "abc", "123")` palauttaa **"123321"**.</span><span class="sxs-lookup"><span data-stu-id="db7e7-128">`TRANSLATE ("abccba", "abc", "123")` returns **"123321"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db7e7-129">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="db7e7-129">Additional resources</span></span>

[<span data-ttu-id="db7e7-130">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="db7e7-130">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]