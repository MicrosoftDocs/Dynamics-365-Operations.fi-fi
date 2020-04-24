---
title: REPLACE ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) REPLACE-funktiota käytetään.
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
ms.openlocfilehash: 83d5095620a938f1ac4b8428fff9209fda7a7831
ms.sourcegitcommit: fb8ad8e2b142441a6530b364f3258bbcc0c724d2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201063"
---
# <a name=""></a><span data-ttu-id="7d230-103"><a name="REPLACE">REPLACE ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="7d230-103"><a name="REPLACE">REPLACE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d230-104">`REPLACE`-funktio palauttaa määritetyn tekstimerkkijonon *merkkijonona*, kun se kokonaan tai osa siitä on korvattu toisella merkkijonolla.</span><span class="sxs-lookup"><span data-stu-id="7d230-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d230-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="7d230-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="7d230-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="7d230-106">Arguments</span></span>

<span data-ttu-id="7d230-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="7d230-107">`text`: *String*</span></span>

<span data-ttu-id="7d230-108">*Merkkijono*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="7d230-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="7d230-109">`pattern`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="7d230-109">`pattern`: *String*</span></span>

<span data-ttu-id="7d230-110">Jos `regular expression flag` -argumentti on **EPÄTOSI**, tämä argumentti sisältää tekstin, joka on korvattava.</span><span class="sxs-lookup"><span data-stu-id="7d230-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="7d230-111">Jos `regular expression flag` -argumentti on **TOSI**, tämä argumentti sisältää säännöllisen lausekkeen, joka määrittää sekä hakukuvion että korvaavan tekstin.</span><span class="sxs-lookup"><span data-stu-id="7d230-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="7d230-112">`replacement`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="7d230-112">`replacement`: *String*</span></span>

<span data-ttu-id="7d230-113">Jos `regular expression flag` -argumentti on **EPÄTOSI**, tämä argumentti sisältää tekstin, jota täytyy käyttää korvaavana tekstinä.</span><span class="sxs-lookup"><span data-stu-id="7d230-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="7d230-114">Jos `regular expression flag` -argumentti on **TOSI**, tätä argumenttia ei käytetä.</span><span class="sxs-lookup"><span data-stu-id="7d230-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="7d230-115">`regular expression flag`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="7d230-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="7d230-116">*Totuusarvo* , joka ilmaisee, käytetäänkö korvauksena säännöllistä lauseketta.</span><span class="sxs-lookup"><span data-stu-id="7d230-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="7d230-117">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="7d230-117">Return values</span></span>

<span data-ttu-id="7d230-118">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="7d230-118">*String*</span></span>

<span data-ttu-id="7d230-119">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="7d230-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7d230-120">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="7d230-120">Usage notes</span></span>

<span data-ttu-id="7d230-121">Jos `regular expression flag` -argumentti on **TOSI**, funktio palauttaa määritetyn merkkijonon sen jälkeen, kun se on muutettu, käyttämällä `pattern`-argumentilla määritettyä säännöllistä lauseketta.</span><span class="sxs-lookup"><span data-stu-id="7d230-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="7d230-122">Säännöllistä lauseketta käytetään etsittäessä korvattavia merkkejä.</span><span class="sxs-lookup"><span data-stu-id="7d230-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="7d230-123">Jos `regular expression flag` -argumentti on **EPÄTOSI**, tämä funktio palauttaa määritetyn merkkijonon sen jälkeen, kun argumentissa määritetty `pattern`-argumentin merkkijoukko on korvattu `replacement`-argumentin merkeillä.</span><span class="sxs-lookup"><span data-stu-id="7d230-123">If the `regular expression flag` argument is **FALSE**, this function returns the specified string after the set of characters that are defined in the `pattern` argument have been replaced by characters of the `replacement` argument.</span></span> 

## <a name="example-1"></a><span data-ttu-id="7d230-124">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="7d230-124">Example 1</span></span>

<span data-ttu-id="7d230-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` on käytössä säännöllisessä lausekkeessa, joka poistaa kaikki muut kuin numeeriset merkit ja se palauttaa arvon **19234564971**.</span><span class="sxs-lookup"><span data-stu-id="7d230-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="7d230-126">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="7d230-126">Example 2</span></span>

<span data-ttu-id="7d230-127">`REPLACE ("abcdef", "cd", "GH", false)` korvaa mallin **cd** merkkijonolla **GH** ja palauttaa arvon **abGHef**.</span><span class="sxs-lookup"><span data-stu-id="7d230-127">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d230-128">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="7d230-128">Additional resources</span></span>

[<span data-ttu-id="7d230-129">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="7d230-129">Text functions</span></span>](er-functions-category-text.md)
