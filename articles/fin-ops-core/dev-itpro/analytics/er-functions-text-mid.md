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
ms.openlocfilehash: 6fbaf5952222d90a855956fb93713e0f9ef81305
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041026"
---
# <span data-ttu-id="54ac2-103"><a name="MID">MID ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="54ac2-103"><a name="MID">MID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54ac2-104">`MID`-funktio palauttaa määritetystä luettelosta *merkkijono*-arvon, joka esittää määritetyn määrän merkkejä määrätystä merkkijonosta, alkaen määritellystä kohdasta.</span><span class="sxs-lookup"><span data-stu-id="54ac2-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="54ac2-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="54ac2-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="54ac2-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="54ac2-106">Arguments</span></span>

<span data-ttu-id="54ac2-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="54ac2-107">`text`: *String*</span></span>

<span data-ttu-id="54ac2-108">*Merkkijono*-arvo, joka määrittää tekstin, josta merkit palautetaan.</span><span class="sxs-lookup"><span data-stu-id="54ac2-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="54ac2-109">`starting position`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="54ac2-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="54ac2-110">*Kokonaislukuarvo*, joka määrittää sen ensimmäisen merkin sijainnin, joka on palautettava määritetystä tekstistä.</span><span class="sxs-lookup"><span data-stu-id="54ac2-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="54ac2-111">`number of characters`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="54ac2-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="54ac2-112">*Kokonaislukuarvo*, joka määrittelee palautettavien merkkien lukumäärän määritetystä aloituspaikasta alkaen.</span><span class="sxs-lookup"><span data-stu-id="54ac2-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="54ac2-113">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="54ac2-113">Return values</span></span>

<span data-ttu-id="54ac2-114">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="54ac2-114">*String*</span></span>

<span data-ttu-id="54ac2-115">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="54ac2-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="54ac2-116">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="54ac2-116">Usage notes</span></span>

<span data-ttu-id="54ac2-117">Jos `starting position` -argumentin arvo on pienempi kuin 0 (nolla), palautetut merkit lasketaan määritetyn merkkijonon ensimmäisestä kohdasta.</span><span class="sxs-lookup"><span data-stu-id="54ac2-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="54ac2-118">Jos `starting position` -argumentin arvo ylittää määritetyn merkkijonon pituuden, funktio palauttaa tyhjän merkkijonon.</span><span class="sxs-lookup"><span data-stu-id="54ac2-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="54ac2-119">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="54ac2-119">Example</span></span>

<span data-ttu-id="54ac2-120">`MID ("Sample", 2, 3)` palauttaa arvon **amp**.</span><span class="sxs-lookup"><span data-stu-id="54ac2-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="54ac2-121">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="54ac2-121">Additional resources</span></span>

[<span data-ttu-id="54ac2-122">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="54ac2-122">Text functions</span></span>](er-functions-category-text.md)
