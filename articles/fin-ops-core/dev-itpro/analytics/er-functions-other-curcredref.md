---
title: CURCREDREF ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) CURCREDREF-funktiota käytetään.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3923126060963122634d90c2ba8a380f534e9178
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686759"
---
# <a name="curcredref-er-function"></a><span data-ttu-id="8d776-103">CURCREDREF ER-funktio</span><span class="sxs-lookup"><span data-stu-id="8d776-103">CURCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d776-104">`CURCREDREF`-funktio palauttaa *merkkijono*-arvon, joka vastaa velkojan viittausta määritetyn laskunumeron numeroiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="8d776-104">The `CURCREDREF` function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d776-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="8d776-105">Syntax</span></span>

```vb
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="8d776-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="8d776-106">Arguments</span></span>

<span data-ttu-id="8d776-107">`invoice number digits`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="8d776-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="8d776-108">Tekstiarvo, joka edustaa laskunumeron numeroita.</span><span class="sxs-lookup"><span data-stu-id="8d776-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="8d776-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="8d776-109">Return values</span></span>

<span data-ttu-id="8d776-110">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="8d776-110">*String*</span></span>

<span data-ttu-id="8d776-111">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="8d776-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="8d776-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="8d776-112">Example</span></span>

<span data-ttu-id="8d776-113">`CURCredRef ("VEND-200002")` palauttaa **"2200002"**.</span><span class="sxs-lookup"><span data-stu-id="8d776-113">`CURCredRef ("VEND-200002")` returns **"2200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8d776-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8d776-114">Additional resources</span></span>

[<span data-ttu-id="8d776-115">Muut (liiketoiminnan toimialuekohtaiset) toiminnot</span><span class="sxs-lookup"><span data-stu-id="8d776-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
