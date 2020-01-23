---
title: CN_GBT_ADDITIONALDIMENSIONID ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) CN_GBT_ADDITIONALDIMENSIONID-funktiota käytetään.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df693d745d1fe74b4500dd3fda0cc0c4be21142d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917025"
---
# <span data-ttu-id="9a6c3-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="9a6c3-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a6c3-104">`CN_GBT_ADDITIONALDIMENSIONID`-funktio palauttaa *merkkijono* arvon, joka edustaa yksittäistä taloushallinnon dimension tunnusta, joka on otettu määritetystä merkkijonosta.</span><span class="sxs-lookup"><span data-stu-id="9a6c3-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="9a6c3-105">Määrätty merkkijono näyttää kaikki ulottuvuudet pilkulla erotettuna tunnusten luettelona.</span><span class="sxs-lookup"><span data-stu-id="9a6c3-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a6c3-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="9a6c3-106">Syntax</span></span>

```
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="9a6c3-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="9a6c3-107">Arguments</span></span>

<span data-ttu-id="9a6c3-108">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="9a6c3-108">`text`: *String*</span></span>

<span data-ttu-id="9a6c3-109">*Merkkijono*-arvo, joka näyttää kaikki ulottuvuudet pilkulla erotettuna tunnusten luettelona.</span><span class="sxs-lookup"><span data-stu-id="9a6c3-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="9a6c3-110">`number`: Kokonaisluku</span><span class="sxs-lookup"><span data-stu-id="9a6c3-110">`number`: Integer</span></span>

<span data-ttu-id="9a6c3-111">*Kokonaisluku*-arvo, joka määrittää pyydetyn dimension järjestyskoodin tietyssä merkkijonossa.</span><span class="sxs-lookup"><span data-stu-id="9a6c3-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="9a6c3-112">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="9a6c3-112">Return values</span></span>

<span data-ttu-id="9a6c3-113">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="9a6c3-113">*String*</span></span>

<span data-ttu-id="9a6c3-114">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="9a6c3-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9a6c3-115">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="9a6c3-115">Example</span></span>

<span data-ttu-id="9a6c3-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` palauttaa arvon **CC**.</span><span class="sxs-lookup"><span data-stu-id="9a6c3-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9a6c3-117">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="9a6c3-117">Additional resources</span></span>

[<span data-ttu-id="9a6c3-118">Muut (liiketoiminnan toimialuekohtaiset) toiminnot</span><span class="sxs-lookup"><span data-stu-id="9a6c3-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
