---
title: REPLACE ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) REPLACE-funktiota käytetään.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: c9f1abe397e05f816fcf226df76362d872819f57
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570261"
---
# <a name="replace-er-function"></a><span data-ttu-id="ca28b-103">REPLACE ER-funktio</span><span class="sxs-lookup"><span data-stu-id="ca28b-103">REPLACE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca28b-104">`REPLACE`-funktio palauttaa määritetyn tekstimerkkijonon *merkkijonona*, kun se kokonaan tai osa siitä on korvattu toisella merkkijonolla.</span><span class="sxs-lookup"><span data-stu-id="ca28b-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca28b-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="ca28b-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="ca28b-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="ca28b-106">Arguments</span></span>

<span data-ttu-id="ca28b-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="ca28b-107">`text`: *String*</span></span>

<span data-ttu-id="ca28b-108">*Merkkijono*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="ca28b-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="ca28b-109">`pattern`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="ca28b-109">`pattern`: *String*</span></span>

<span data-ttu-id="ca28b-110">Jos `regular expression flag` -argumentti on **EPÄTOSI**, tämä argumentti sisältää tekstin, joka on korvattava.</span><span class="sxs-lookup"><span data-stu-id="ca28b-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="ca28b-111">Jos `regular expression flag` -argumentti on **TOSI**, tämä argumentti sisältää säännöllisen lausekkeen, joka määrittää sekä hakukuvion että korvaavan tekstin.</span><span class="sxs-lookup"><span data-stu-id="ca28b-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="ca28b-112">`replacement`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="ca28b-112">`replacement`: *String*</span></span>

<span data-ttu-id="ca28b-113">Jos `regular expression flag` -argumentti on **EPÄTOSI**, tämä argumentti sisältää tekstin, jota täytyy käyttää korvaavana tekstinä.</span><span class="sxs-lookup"><span data-stu-id="ca28b-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="ca28b-114">Jos `regular expression flag` -argumentti on **TOSI**, tätä argumenttia ei käytetä.</span><span class="sxs-lookup"><span data-stu-id="ca28b-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="ca28b-115">`regular expression flag`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="ca28b-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="ca28b-116">*Totuusarvo* , joka ilmaisee, käytetäänkö korvauksena säännöllistä lauseketta.</span><span class="sxs-lookup"><span data-stu-id="ca28b-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="ca28b-117">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="ca28b-117">Return values</span></span>

<span data-ttu-id="ca28b-118">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="ca28b-118">*String*</span></span>

<span data-ttu-id="ca28b-119">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="ca28b-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ca28b-120">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="ca28b-120">Usage notes</span></span>

<span data-ttu-id="ca28b-121">Jos `regular expression flag` -argumentti on **TOSI**, funktio palauttaa määritetyn merkkijonon sen jälkeen, kun se on muutettu, käyttämällä `pattern`-argumentilla määritettyä säännöllistä lauseketta.</span><span class="sxs-lookup"><span data-stu-id="ca28b-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="ca28b-122">Säännöllistä lauseketta käytetään etsittäessä korvattavia merkkejä.</span><span class="sxs-lookup"><span data-stu-id="ca28b-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="ca28b-123">Jos `regular expression flag` -argumentti on **EPÄTOSI**, tämä funktio palauttaa määritetyn merkkijonon sen jälkeen, kun argumentissa määritetty `pattern`-argumentin merkkijoukko on korvattu `replacement`-argumentin merkeillä.</span><span class="sxs-lookup"><span data-stu-id="ca28b-123">If the `regular expression flag` argument is **FALSE**, this function returns the specified string after the set of characters that are defined in the `pattern` argument have been replaced by characters of the `replacement` argument.</span></span> 

## <a name="example-1"></a><span data-ttu-id="ca28b-124">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="ca28b-124">Example 1</span></span>

<span data-ttu-id="ca28b-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` on käytössä säännöllisessä lausekkeessa, joka poistaa kaikki muut kuin numeeriset merkit ja se palauttaa arvon **19234564971**.</span><span class="sxs-lookup"><span data-stu-id="ca28b-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="ca28b-126">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="ca28b-126">Example 2</span></span>

<span data-ttu-id="ca28b-127">`REPLACE ("abcdef", "cd", "GH", false)` korvaa mallin **cd** merkkijonolla **GH** ja palauttaa arvon **abGHef**.</span><span class="sxs-lookup"><span data-stu-id="ca28b-127">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ca28b-128">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="ca28b-128">Additional resources</span></span>

[<span data-ttu-id="ca28b-129">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="ca28b-129">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]