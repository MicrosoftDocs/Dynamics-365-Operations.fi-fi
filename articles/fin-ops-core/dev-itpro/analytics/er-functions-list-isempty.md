---
title: ISEMPTY ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ISEMPTY-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: b689e6d4bb849f07db5d00cf8a9dc5c16646a927
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563869"
---
# <a name="isempty-er-function"></a><span data-ttu-id="87eb9-103">ISEMPTY ER-funktio</span><span class="sxs-lookup"><span data-stu-id="87eb9-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87eb9-104">`ISEMPTY` funktio palauttaa *totuusarvon* **TOSI**, jos määritetty luettelo ei sisällä tietueita.</span><span class="sxs-lookup"><span data-stu-id="87eb9-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="87eb9-105">Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="87eb9-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="87eb9-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="87eb9-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="87eb9-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="87eb9-107">Arguments</span></span>

<span data-ttu-id="87eb9-108">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="87eb9-108">`list`: *Record list*</span></span>

<span data-ttu-id="87eb9-109">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="87eb9-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="87eb9-110">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="87eb9-110">Return values</span></span>

<span data-ttu-id="87eb9-111">*Boolen arvo*</span><span class="sxs-lookup"><span data-stu-id="87eb9-111">*Boolean*</span></span>

<span data-ttu-id="87eb9-112">Tuloksena oleva *Totuusarvo*-arvo.</span><span class="sxs-lookup"><span data-stu-id="87eb9-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="87eb9-113">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="87eb9-113">Example 1</span></span>

<span data-ttu-id="87eb9-114">Jos syötät *Lasketun kenttä*-tyypin **DS**-tietolähteen, ja se sisältää lausekkeen `SPLIT ("A|B|C", "|")`, lauseke `ISEMPTY(DS)` palauttaa arvon **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="87eb9-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="87eb9-115">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="87eb9-115">Example 2</span></span>

<span data-ttu-id="87eb9-116">Lauseke `ISEMPTY (SPLIT ("",1))` palauttaa arvon **TOSI**.</span><span class="sxs-lookup"><span data-stu-id="87eb9-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87eb9-117">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="87eb9-117">Additional resources</span></span>

[<span data-ttu-id="87eb9-118">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="87eb9-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]