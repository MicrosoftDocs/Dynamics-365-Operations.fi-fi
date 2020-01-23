---
title: UPPER ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) UPPER-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: ed862ab823cfc3539c420d3066c9397e1e6d870e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916680"
---
# <span data-ttu-id="882c8-103"><a name="UPPER">UPPER ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="882c8-103"><a name="UPPER">UPPER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="882c8-104">`UPPER`-funktio palauttaa määritetyn tekstimerkkijonon *Merkkijono*-arvona sen jälkeen, kun se on muunnettu isoiksi kirjaimiksi.</span><span class="sxs-lookup"><span data-stu-id="882c8-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="882c8-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="882c8-105">Syntax</span></span>

```
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="882c8-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="882c8-106">Arguments</span></span>

<span data-ttu-id="882c8-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="882c8-107">`text`: *String*</span></span>

<span data-ttu-id="882c8-108">*Merkkijono*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="882c8-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="882c8-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="882c8-109">Return values</span></span>

<span data-ttu-id="882c8-110">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="882c8-110">*String*</span></span>

<span data-ttu-id="882c8-111">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="882c8-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="882c8-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="882c8-112">Example</span></span>

<span data-ttu-id="882c8-113">`UPPER ("Sample")` palauttaa arvon **MALLI**.</span><span class="sxs-lookup"><span data-stu-id="882c8-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="882c8-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="882c8-114">Additional resources</span></span>

[<span data-ttu-id="882c8-115">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="882c8-115">Text functions</span></span>](er-functions-category-text.md)
