---
title: ISEMPTY ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ISEMPTY-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 5dbba375104b57f9fb09ed4e330d85181ec0dff8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684880"
---
# <a name="isempty-er-function"></a><span data-ttu-id="512d8-103">ISEMPTY ER-funktio</span><span class="sxs-lookup"><span data-stu-id="512d8-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="512d8-104">`ISEMPTY` funktio palauttaa *totuusarvon* **TOSI**, jos määritetty luettelo ei sisällä tietueita.</span><span class="sxs-lookup"><span data-stu-id="512d8-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="512d8-105">Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="512d8-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="512d8-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="512d8-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="512d8-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="512d8-107">Arguments</span></span>

<span data-ttu-id="512d8-108">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="512d8-108">`list`: *Record list*</span></span>

<span data-ttu-id="512d8-109">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="512d8-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="512d8-110">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="512d8-110">Return values</span></span>

<span data-ttu-id="512d8-111">*Boolen arvo*</span><span class="sxs-lookup"><span data-stu-id="512d8-111">*Boolean*</span></span>

<span data-ttu-id="512d8-112">Tuloksena oleva *Totuusarvo*-arvo.</span><span class="sxs-lookup"><span data-stu-id="512d8-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="512d8-113">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="512d8-113">Example 1</span></span>

<span data-ttu-id="512d8-114">Jos syötät *Lasketun kenttä*-tyypin **DS**-tietolähteen, ja se sisältää lausekkeen `SPLIT ("A|B|C", "|")`, lauseke `ISEMPTY(DS)` palauttaa arvon **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="512d8-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="512d8-115">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="512d8-115">Example 2</span></span>

<span data-ttu-id="512d8-116">Lauseke `ISEMPTY (SPLIT ("",1))` palauttaa arvon **TOSI**.</span><span class="sxs-lookup"><span data-stu-id="512d8-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="512d8-117">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="512d8-117">Additional resources</span></span>

[<span data-ttu-id="512d8-118">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="512d8-118">List functions</span></span>](er-functions-category-list.md)
