---
title: FIRST ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) FIRST-funktiota käytetään.
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
ms.openlocfilehash: ec94a27776cf1069b50b5437f4d167019fdef120
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564732"
---
# <a name="first-er-function"></a><span data-ttu-id="d31c2-103">FIRST ER-funktio</span><span class="sxs-lookup"><span data-stu-id="d31c2-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d31c2-104">`FIRST`-funktio palauttaa ensimmäisen tietueen, joka on määritetty *Säilön (tietueen)* arvona, jos luettelo ei ole tyhjä.</span><span class="sxs-lookup"><span data-stu-id="d31c2-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="d31c2-105">Jos luettelo on tyhjä, funktio heittää poikkeuksen.</span><span class="sxs-lookup"><span data-stu-id="d31c2-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="d31c2-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="d31c2-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="d31c2-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="d31c2-107">Arguments</span></span>

<span data-ttu-id="d31c2-108">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="d31c2-108">`list`: *Record list*</span></span>

<span data-ttu-id="d31c2-109">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="d31c2-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d31c2-110">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="d31c2-110">Return values</span></span>

<span data-ttu-id="d31c2-111">*Kontti (tietue)*</span><span class="sxs-lookup"><span data-stu-id="d31c2-111">*Container (record)*</span></span>

<span data-ttu-id="d31c2-112">Tuloksena oleva tietueen arvo.</span><span class="sxs-lookup"><span data-stu-id="d31c2-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="d31c2-113">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="d31c2-113">Example 1</span></span>

<span data-ttu-id="d31c2-114">Lauseke `FIRST(SPLIT("ABC",1)).Value` palauttaa tekstiarvon **"A"**.</span><span class="sxs-lookup"><span data-stu-id="d31c2-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="d31c2-115">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="d31c2-115">Example 2</span></span>

<span data-ttu-id="d31c2-116">Lauseke `FIRST(SPLIT("",1)).Value` heittää poikkeuksen suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="d31c2-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d31c2-117">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d31c2-117">Additional resources</span></span>

[<span data-ttu-id="d31c2-118">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="d31c2-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]