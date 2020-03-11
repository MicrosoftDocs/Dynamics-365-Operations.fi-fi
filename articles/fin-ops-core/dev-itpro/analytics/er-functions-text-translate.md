---
title: TRANSLATE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) TRANSLATE-funktiota käytetään.
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
ms.openlocfilehash: 07fe19c5f66c33e336f76f3a72d3bbda0c7e8d86
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040914"
---
# <span data-ttu-id="6419c-103"><a name="TRANSLATE">TRANSLATE ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="6419c-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6419c-104">`TRANSLATE`-funktio palauttaa määritetyn tekstimerkkijonon *merkkijonona*, kun se kokonaan tai osa siitä on korvattu toisella merkkijonolla.</span><span class="sxs-lookup"><span data-stu-id="6419c-104">The `TRANSLATE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="6419c-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="6419c-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="6419c-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="6419c-106">Arguments</span></span>

<span data-ttu-id="6419c-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="6419c-107">`text`: *String*</span></span>

<span data-ttu-id="6419c-108">*Merkkijono*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="6419c-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="6419c-109">`pattern`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="6419c-109">`pattern`: *String*</span></span>

<span data-ttu-id="6419c-110">Teksti, joka tulee korvata.</span><span class="sxs-lookup"><span data-stu-id="6419c-110">The text that must be replaced.</span></span>

<span data-ttu-id="6419c-111">`replacement`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="6419c-111">`replacement`: *String*</span></span>

<span data-ttu-id="6419c-112">Korvaava teksti.</span><span class="sxs-lookup"><span data-stu-id="6419c-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="6419c-113">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="6419c-113">Return values</span></span>

<span data-ttu-id="6419c-114">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="6419c-114">*String*</span></span>

<span data-ttu-id="6419c-115">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="6419c-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="6419c-116">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="6419c-116">Example</span></span>

<span data-ttu-id="6419c-117">`TRANSLATE ("abcdef", "cd", "GH")` korvaa mallin **cd** merkkijonolla **GH** ja palauttaa arvon **abGHef**.</span><span class="sxs-lookup"><span data-stu-id="6419c-117">`TRANSLATE ("abcdef", "cd", "GH")` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6419c-118">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6419c-118">Additional resources</span></span>

[<span data-ttu-id="6419c-119">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="6419c-119">Text functions</span></span>](er-functions-category-text.md)
