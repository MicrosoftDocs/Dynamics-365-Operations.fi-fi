---
title: MID ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) MID-funktiota käytetään.
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
ms.openlocfilehash: e2addace5c5606ebaae56ca658700347978a805b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744716"
---
# <a name="mid-er-function"></a><span data-ttu-id="c9f78-103">MID ER -funktio</span><span class="sxs-lookup"><span data-stu-id="c9f78-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9f78-104">`MID`-funktio palauttaa määritetystä luettelosta *merkkijono*-arvon, joka esittää määritetyn määrän merkkejä määrätystä merkkijonosta, alkaen määritellystä kohdasta.</span><span class="sxs-lookup"><span data-stu-id="c9f78-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9f78-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="c9f78-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="c9f78-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="c9f78-106">Arguments</span></span>

<span data-ttu-id="c9f78-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="c9f78-107">`text`: *String*</span></span>

<span data-ttu-id="c9f78-108">*Merkkijono*-arvo, joka määrittää tekstin, josta merkit palautetaan.</span><span class="sxs-lookup"><span data-stu-id="c9f78-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="c9f78-109">`starting position`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="c9f78-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="c9f78-110">*Kokonaislukuarvo*, joka määrittää sen ensimmäisen merkin sijainnin, joka on palautettava määritetystä tekstistä.</span><span class="sxs-lookup"><span data-stu-id="c9f78-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="c9f78-111">`number of characters`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="c9f78-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="c9f78-112">*Kokonaislukuarvo*, joka määrittelee palautettavien merkkien lukumäärän määritetystä aloituspaikasta alkaen.</span><span class="sxs-lookup"><span data-stu-id="c9f78-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="c9f78-113">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="c9f78-113">Return values</span></span>

<span data-ttu-id="c9f78-114">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="c9f78-114">*String*</span></span>

<span data-ttu-id="c9f78-115">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="c9f78-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c9f78-116">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="c9f78-116">Usage notes</span></span>

<span data-ttu-id="c9f78-117">Jos `starting position` -argumentin arvo on pienempi kuin 0 (nolla), palautetut merkit lasketaan määritetyn merkkijonon ensimmäisestä kohdasta.</span><span class="sxs-lookup"><span data-stu-id="c9f78-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="c9f78-118">Jos `starting position` -argumentin arvo ylittää määritetyn merkkijonon pituuden, funktio palauttaa tyhjän merkkijonon.</span><span class="sxs-lookup"><span data-stu-id="c9f78-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="c9f78-119">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="c9f78-119">Example</span></span>

<span data-ttu-id="c9f78-120">`MID ("Sample", 2, 3)` palauttaa arvon **amp**.</span><span class="sxs-lookup"><span data-stu-id="c9f78-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c9f78-121">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c9f78-121">Additional resources</span></span>

[<span data-ttu-id="c9f78-122">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="c9f78-122">Text functions</span></span>](er-functions-category-text.md)
