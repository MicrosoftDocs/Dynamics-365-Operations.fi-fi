---
title: MID ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) MID-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: e0520bc54465f00d36e88787933b291847dee852
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562730"
---
# <a name="mid-er-function"></a><span data-ttu-id="70c1d-103">MID ER -funktio</span><span class="sxs-lookup"><span data-stu-id="70c1d-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70c1d-104">`MID`-funktio palauttaa määritetystä luettelosta *merkkijono*-arvon, joka esittää määritetyn määrän merkkejä määrätystä merkkijonosta, alkaen määritellystä kohdasta.</span><span class="sxs-lookup"><span data-stu-id="70c1d-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="70c1d-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="70c1d-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="70c1d-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="70c1d-106">Arguments</span></span>

<span data-ttu-id="70c1d-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="70c1d-107">`text`: *String*</span></span>

<span data-ttu-id="70c1d-108">*Merkkijono*-arvo, joka määrittää tekstin, josta merkit palautetaan.</span><span class="sxs-lookup"><span data-stu-id="70c1d-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="70c1d-109">`starting position`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="70c1d-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="70c1d-110">*Kokonaislukuarvo*, joka määrittää sen ensimmäisen merkin sijainnin, joka on palautettava määritetystä tekstistä.</span><span class="sxs-lookup"><span data-stu-id="70c1d-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="70c1d-111">`number of characters`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="70c1d-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="70c1d-112">*Kokonaislukuarvo*, joka määrittelee palautettavien merkkien lukumäärän määritetystä aloituspaikasta alkaen.</span><span class="sxs-lookup"><span data-stu-id="70c1d-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="70c1d-113">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="70c1d-113">Return values</span></span>

<span data-ttu-id="70c1d-114">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="70c1d-114">*String*</span></span>

<span data-ttu-id="70c1d-115">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="70c1d-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="70c1d-116">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="70c1d-116">Usage notes</span></span>

<span data-ttu-id="70c1d-117">Jos `starting position` -argumentin arvo on pienempi kuin 0 (nolla), palautetut merkit lasketaan määritetyn merkkijonon ensimmäisestä kohdasta.</span><span class="sxs-lookup"><span data-stu-id="70c1d-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="70c1d-118">Jos `starting position` -argumentin arvo ylittää määritetyn merkkijonon pituuden, funktio palauttaa tyhjän merkkijonon.</span><span class="sxs-lookup"><span data-stu-id="70c1d-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="70c1d-119">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="70c1d-119">Example</span></span>

<span data-ttu-id="70c1d-120">`MID ("Sample", 2, 3)` palauttaa arvon **amp**.</span><span class="sxs-lookup"><span data-stu-id="70c1d-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="70c1d-121">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="70c1d-121">Additional resources</span></span>

[<span data-ttu-id="70c1d-122">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="70c1d-122">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]