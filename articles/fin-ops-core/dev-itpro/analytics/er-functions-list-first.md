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
ms.openlocfilehash: 211891a0ad5dc6152ce8d980bcd40a9a6bc7e3e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917347"
---
# <span data-ttu-id="ceeb2-103"><a name="FIRST">FIRST ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="ceeb2-103"><a name="FIRST">FIRST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ceeb2-104">`FIRST`-funktio palauttaa ensimmäisen tietueen, joka on määritetty *Säilön (tietueen)* arvona, jos luettelo ei ole tyhjä.</span><span class="sxs-lookup"><span data-stu-id="ceeb2-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="ceeb2-105">Jos luettelo on tyhjä, funktio heittää poikkeuksen.</span><span class="sxs-lookup"><span data-stu-id="ceeb2-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceeb2-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="ceeb2-106">Syntax</span></span>

```
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="ceeb2-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="ceeb2-107">Arguments</span></span>

<span data-ttu-id="ceeb2-108">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="ceeb2-108">`list`: *Record list*</span></span>

<span data-ttu-id="ceeb2-109">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="ceeb2-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="ceeb2-110">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="ceeb2-110">Return values</span></span>

<span data-ttu-id="ceeb2-111">*Kontti (tietue)*</span><span class="sxs-lookup"><span data-stu-id="ceeb2-111">*Container (record)*</span></span>

<span data-ttu-id="ceeb2-112">Tuloksena oleva tietueen arvo.</span><span class="sxs-lookup"><span data-stu-id="ceeb2-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="ceeb2-113">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="ceeb2-113">Example 1</span></span>

<span data-ttu-id="ceeb2-114">Lauseke `FIRST(SPLIT("ABC",1)).Value` palauttaa tekstiarvon **"A"**.</span><span class="sxs-lookup"><span data-stu-id="ceeb2-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="ceeb2-115">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="ceeb2-115">Example 2</span></span>

<span data-ttu-id="ceeb2-116">Lauseke `FIRST(SPLIT("",1)).Value` heittää poikkeuksen suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="ceeb2-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ceeb2-117">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="ceeb2-117">Additional resources</span></span>

[<span data-ttu-id="ceeb2-118">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="ceeb2-118">List functions</span></span>](er-functions-category-list.md)
