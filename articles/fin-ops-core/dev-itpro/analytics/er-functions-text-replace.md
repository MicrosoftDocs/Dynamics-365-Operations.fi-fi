---
title: REPLACE ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) REPLACE-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: ba2590635ba465dae9ea50d3e4da989365548f3b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040983"
---
# <span data-ttu-id="a0ea7-103"><a name="REPLACE">REPLACE ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="a0ea7-103"><a name="REPLACE">REPLACE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0ea7-104">`REPLACE`-funktio palauttaa määritetyn tekstimerkkijonon *merkkijonona*, kun se kokonaan tai osa siitä on korvattu toisella merkkijonolla.</span><span class="sxs-lookup"><span data-stu-id="a0ea7-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0ea7-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="a0ea7-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="a0ea7-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="a0ea7-106">Arguments</span></span>

<span data-ttu-id="a0ea7-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="a0ea7-107">`text`: *String*</span></span>

<span data-ttu-id="a0ea7-108">*Merkkijono*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="a0ea7-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="a0ea7-109">`pattern`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="a0ea7-109">`pattern`: *String*</span></span>

<span data-ttu-id="a0ea7-110">Jos `regular expression flag` -argumentti on **EPÄTOSI**, tämä argumentti sisältää tekstin, joka on korvattava.</span><span class="sxs-lookup"><span data-stu-id="a0ea7-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="a0ea7-111">Jos `regular expression flag` -argumentti on **TOSI**, tämä argumentti sisältää säännöllisen lausekkeen, joka määrittää sekä hakukuvion että korvaavan tekstin.</span><span class="sxs-lookup"><span data-stu-id="a0ea7-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="a0ea7-112">`replacement`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="a0ea7-112">`replacement`: *String*</span></span>

<span data-ttu-id="a0ea7-113">Jos `regular expression flag` -argumentti on **EPÄTOSI**, tämä argumentti sisältää tekstin, jota täytyy käyttää korvaavana tekstinä.</span><span class="sxs-lookup"><span data-stu-id="a0ea7-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="a0ea7-114">Jos `regular expression flag` -argumentti on **TOSI**, tätä argumenttia ei käytetä.</span><span class="sxs-lookup"><span data-stu-id="a0ea7-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="a0ea7-115">`regular expression flag`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="a0ea7-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="a0ea7-116">*Totuusarvo* , joka ilmaisee, käytetäänkö korvauksena säännöllistä lauseketta.</span><span class="sxs-lookup"><span data-stu-id="a0ea7-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="a0ea7-117">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="a0ea7-117">Return values</span></span>

<span data-ttu-id="a0ea7-118">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="a0ea7-118">*String*</span></span>

<span data-ttu-id="a0ea7-119">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="a0ea7-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a0ea7-120">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="a0ea7-120">Usage notes</span></span>

<span data-ttu-id="a0ea7-121">Jos `regular expression flag` -argumentti on **TOSI**, funktio palauttaa määritetyn merkkijonon sen jälkeen, kun se on muutettu, käyttämällä `pattern`-argumentilla määritettyä säännöllistä lauseketta.</span><span class="sxs-lookup"><span data-stu-id="a0ea7-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="a0ea7-122">Säännöllistä lauseketta käytetään etsittäessä korvattavia merkkejä.</span><span class="sxs-lookup"><span data-stu-id="a0ea7-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="a0ea7-123">Jos `regular expression flag`-argumentti on **EPÄTOSI**, tämä funktio käyttäytyy kuten [TRANSLATE](er-functions-text-translate.md).</span><span class="sxs-lookup"><span data-stu-id="a0ea7-123">If the `regular expression flag` argument is **FALSE**, this function behaves like [TRANSLATE](er-functions-text-translate.md).</span></span> <span data-ttu-id="a0ea7-124">`replacement`-argumentin määritettyjä merkkejä käytetään löydettyjen merkkien korvaamisessa.</span><span class="sxs-lookup"><span data-stu-id="a0ea7-124">The characters that are specified by the `replacement` argument are used to replace the characters that are found.</span></span> 

## <a name="example-1"></a><span data-ttu-id="a0ea7-125">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="a0ea7-125">Example 1</span></span>

<span data-ttu-id="a0ea7-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` on käytössä säännöllisessä lausekkeessa, joka poistaa kaikki muut kuin numeeriset merkit ja se palauttaa arvon **19234564971**.</span><span class="sxs-lookup"><span data-stu-id="a0ea7-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="a0ea7-127">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="a0ea7-127">Example 2</span></span>

<span data-ttu-id="a0ea7-128">`REPLACE ("abcdef", "cd", "GH", false)` korvaa mallin **cd** merkkijonolla **GH** ja palauttaa arvon **abGHef**.</span><span class="sxs-lookup"><span data-stu-id="a0ea7-128">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a0ea7-129">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a0ea7-129">Additional resources</span></span>

[<span data-ttu-id="a0ea7-130">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="a0ea7-130">Text functions</span></span>](er-functions-category-text.md)
