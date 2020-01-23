---
title: CH_BANK_MOD_10 ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) CH_BANK_MOD_10-funktiota käytetään.
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
ms.openlocfilehash: 42a345fc48b0d87b353308060903a6b5156c0e62
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915875"
---
# <span data-ttu-id="c3f19-103"><a name="CH_BANK_MOD_10">CH_BANK_MOD_10 ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="c3f19-103"><a name="CH_BANK_MOD_10">CH_BANK_MOD_10 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3f19-104">`CH_BANK_MOD_10`-funktio palauttaa *merkkijono*-arvon, joka vastaa velkojan viittausta MOD10-lausekkeena määritetyn laskunumeron numeroiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="c3f19-104">The `CH_BANK_MOD_10` function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3f19-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="c3f19-105">Syntax</span></span>

```
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="c3f19-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="c3f19-106">Arguments</span></span>

<span data-ttu-id="c3f19-107">`invoice number digits`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="c3f19-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="c3f19-108">Tekstiarvo, joka edustaa laskunumeron numeroita.</span><span class="sxs-lookup"><span data-stu-id="c3f19-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="c3f19-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="c3f19-109">Return values</span></span>

<span data-ttu-id="c3f19-110">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="c3f19-110">*String*</span></span>

<span data-ttu-id="c3f19-111">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="c3f19-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c3f19-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="c3f19-112">Example</span></span>

<span data-ttu-id="c3f19-113">`CH_BANK_MOD_10 ("VEND-200002")` palauttaa **3**.</span><span class="sxs-lookup"><span data-stu-id="c3f19-113">`CH_BANK_MOD_10 ("VEND-200002")` returns **3**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3f19-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c3f19-114">Additional resources</span></span>

[<span data-ttu-id="c3f19-115">Muut (liiketoiminnan toimialuekohtaiset) toiminnot</span><span class="sxs-lookup"><span data-stu-id="c3f19-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
