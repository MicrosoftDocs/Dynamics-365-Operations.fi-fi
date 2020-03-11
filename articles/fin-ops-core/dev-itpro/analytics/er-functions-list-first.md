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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d10abcf15b93961bd2ba4aec22914825d9ac38c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042087"
---
# <span data-ttu-id="fd949-103"><a name="FIRST">FIRST ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="fd949-103"><a name="FIRST">FIRST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd949-104">`FIRST`-funktio palauttaa ensimmäisen tietueen, joka on määritetty *Säilön (tietueen)* arvona, jos luettelo ei ole tyhjä.</span><span class="sxs-lookup"><span data-stu-id="fd949-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="fd949-105">Jos luettelo on tyhjä, funktio heittää poikkeuksen.</span><span class="sxs-lookup"><span data-stu-id="fd949-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd949-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="fd949-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="fd949-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="fd949-107">Arguments</span></span>

<span data-ttu-id="fd949-108">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="fd949-108">`list`: *Record list*</span></span>

<span data-ttu-id="fd949-109">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="fd949-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="fd949-110">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="fd949-110">Return values</span></span>

<span data-ttu-id="fd949-111">*Kontti (tietue)*</span><span class="sxs-lookup"><span data-stu-id="fd949-111">*Container (record)*</span></span>

<span data-ttu-id="fd949-112">Tuloksena oleva tietueen arvo.</span><span class="sxs-lookup"><span data-stu-id="fd949-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="fd949-113">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="fd949-113">Example 1</span></span>

<span data-ttu-id="fd949-114">Lauseke `FIRST(SPLIT("ABC",1)).Value` palauttaa tekstiarvon **"A"**.</span><span class="sxs-lookup"><span data-stu-id="fd949-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="fd949-115">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="fd949-115">Example 2</span></span>

<span data-ttu-id="fd949-116">Lauseke `FIRST(SPLIT("",1)).Value` heittää poikkeuksen suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="fd949-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd949-117">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="fd949-117">Additional resources</span></span>

[<span data-ttu-id="fd949-118">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="fd949-118">List functions</span></span>](er-functions-category-list.md)
