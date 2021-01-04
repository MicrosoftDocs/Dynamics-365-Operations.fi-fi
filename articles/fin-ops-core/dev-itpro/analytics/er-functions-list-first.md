---
title: FIRST ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) FIRST-funktiota käytetään.
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
ms.openlocfilehash: a5c52d3f999b4c6fbdea0685977ab13fca1e8ffb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679411"
---
# <a name="first-er-function"></a><span data-ttu-id="0ca47-103">FIRST ER-funktio</span><span class="sxs-lookup"><span data-stu-id="0ca47-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ca47-104">`FIRST`-funktio palauttaa ensimmäisen tietueen, joka on määritetty *Säilön (tietueen)* arvona, jos luettelo ei ole tyhjä.</span><span class="sxs-lookup"><span data-stu-id="0ca47-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="0ca47-105">Jos luettelo on tyhjä, funktio heittää poikkeuksen.</span><span class="sxs-lookup"><span data-stu-id="0ca47-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ca47-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="0ca47-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="0ca47-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="0ca47-107">Arguments</span></span>

<span data-ttu-id="0ca47-108">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="0ca47-108">`list`: *Record list*</span></span>

<span data-ttu-id="0ca47-109">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="0ca47-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="0ca47-110">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="0ca47-110">Return values</span></span>

<span data-ttu-id="0ca47-111">*Kontti (tietue)*</span><span class="sxs-lookup"><span data-stu-id="0ca47-111">*Container (record)*</span></span>

<span data-ttu-id="0ca47-112">Tuloksena oleva tietueen arvo.</span><span class="sxs-lookup"><span data-stu-id="0ca47-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="0ca47-113">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="0ca47-113">Example 1</span></span>

<span data-ttu-id="0ca47-114">Lauseke `FIRST(SPLIT("ABC",1)).Value` palauttaa tekstiarvon **"A"**.</span><span class="sxs-lookup"><span data-stu-id="0ca47-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="0ca47-115">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="0ca47-115">Example 2</span></span>

<span data-ttu-id="0ca47-116">Lauseke `FIRST(SPLIT("",1)).Value` heittää poikkeuksen suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="0ca47-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0ca47-117">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0ca47-117">Additional resources</span></span>

[<span data-ttu-id="0ca47-118">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="0ca47-118">List functions</span></span>](er-functions-category-list.md)
