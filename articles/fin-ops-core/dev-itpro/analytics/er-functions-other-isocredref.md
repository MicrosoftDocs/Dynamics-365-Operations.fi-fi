---
title: ISOCREDREF ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ISOCREDREF-funktiota käytetään.
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
ms.openlocfilehash: ea72d824d3a98d7685a965e981d057991f012a0e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916956"
---
# <span data-ttu-id="6ee42-103"><a name="ISOCREDREF">ISOCREDREF ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="6ee42-103"><a name="ISOCREDREF">ISOCREDREF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ee42-104">`ISOCREDREF`-funktio palauttaa *merkkijono*-arvon, joka edustaa laskuttajan ISO (International Organization for Standardization) -viitettä määritetyn laskunumeron lukujen ja kirjainmerkkien perusteella.</span><span class="sxs-lookup"><span data-stu-id="6ee42-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ee42-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="6ee42-105">Syntax</span></span>

```
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="6ee42-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="6ee42-106">Arguments</span></span>

<span data-ttu-id="6ee42-107">`invoice number digits`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="6ee42-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="6ee42-108">Tekstiarvo, joka edustaa laskunumeron numeroita.</span><span class="sxs-lookup"><span data-stu-id="6ee42-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="6ee42-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="6ee42-109">Return values</span></span>

<span data-ttu-id="6ee42-110">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="6ee42-110">*String*</span></span>

<span data-ttu-id="6ee42-111">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="6ee42-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6ee42-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="6ee42-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="6ee42-113">Voit poistaa ne aakkosmerkit, jotka eivät ole ISO-yhteensopivia, jos `invoice number digits`-argumentti on käännetty ennen kuin se välitetään tälle toiminnolle.</span><span class="sxs-lookup"><span data-stu-id="6ee42-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="6ee42-114">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="6ee42-114">Example</span></span>

<span data-ttu-id="6ee42-115">`ISOCredRef ("VEND-200002")` palauttaa arvon **"RF23VEND-200002"**.</span><span class="sxs-lookup"><span data-stu-id="6ee42-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ee42-116">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6ee42-116">Additional resources</span></span>

[<span data-ttu-id="6ee42-117">Muut (liiketoiminnan toimialuekohtaiset) toiminnot</span><span class="sxs-lookup"><span data-stu-id="6ee42-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
