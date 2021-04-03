---
title: CN_GBT_ADDITIONALDIMENSIONID ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) CN_GBT_ADDITIONALDIMENSIONID-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 5774bb6928ae321af923819d6b2cc609dbf35b99
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564139"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a><span data-ttu-id="99a3b-103">CN_GBT_ADDITIONALDIMENSIONID ER -funktio</span><span class="sxs-lookup"><span data-stu-id="99a3b-103">CN_GBT_ADDITIONALDIMENSIONID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99a3b-104">`CN_GBT_ADDITIONALDIMENSIONID`-funktio palauttaa *merkkijono* arvon, joka edustaa yksittäistä taloushallinnon dimension tunnusta, joka on otettu määritetystä merkkijonosta.</span><span class="sxs-lookup"><span data-stu-id="99a3b-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="99a3b-105">Määrätty merkkijono näyttää kaikki ulottuvuudet pilkulla erotettuna tunnusten luettelona.</span><span class="sxs-lookup"><span data-stu-id="99a3b-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="99a3b-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="99a3b-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="99a3b-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="99a3b-107">Arguments</span></span>

<span data-ttu-id="99a3b-108">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="99a3b-108">`text`: *String*</span></span>

<span data-ttu-id="99a3b-109">*Merkkijono*-arvo, joka näyttää kaikki ulottuvuudet pilkulla erotettuna tunnusten luettelona.</span><span class="sxs-lookup"><span data-stu-id="99a3b-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="99a3b-110">`number`: Kokonaisluku</span><span class="sxs-lookup"><span data-stu-id="99a3b-110">`number`: Integer</span></span>

<span data-ttu-id="99a3b-111">*Kokonaisluku*-arvo, joka määrittää pyydetyn dimension järjestyskoodin tietyssä merkkijonossa.</span><span class="sxs-lookup"><span data-stu-id="99a3b-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="99a3b-112">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="99a3b-112">Return values</span></span>

<span data-ttu-id="99a3b-113">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="99a3b-113">*String*</span></span>

<span data-ttu-id="99a3b-114">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="99a3b-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="99a3b-115">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="99a3b-115">Example</span></span>

<span data-ttu-id="99a3b-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` palauttaa arvon **CC**.</span><span class="sxs-lookup"><span data-stu-id="99a3b-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="99a3b-117">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="99a3b-117">Additional resources</span></span>

[<span data-ttu-id="99a3b-118">Muut (liiketoiminnan toimialuekohtaiset) toiminnot</span><span class="sxs-lookup"><span data-stu-id="99a3b-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]