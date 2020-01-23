---
title: LEN ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) LEN-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: d6f2a661dd3a85c658ff85f5886d98f665e28718
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915576"
---
# <span data-ttu-id="7d3c9-103"><a name="LEN">LEN ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="7d3c9-103"><a name="LEN">LEN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d3c9-104">`LEN`-funktio palauttaa määritetystä luettelosta *Kokonaisluku*-arvon, joka esittää merkkien määrän määritetyssä merkkijonossa.</span><span class="sxs-lookup"><span data-stu-id="7d3c9-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d3c9-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="7d3c9-105">Syntax</span></span>

```
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="7d3c9-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="7d3c9-106">Arguments</span></span>

<span data-ttu-id="7d3c9-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="7d3c9-107">`text`: *String*</span></span>

<span data-ttu-id="7d3c9-108">*Merkkijono*-arvo, joka määrittää tekstin.</span><span class="sxs-lookup"><span data-stu-id="7d3c9-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="7d3c9-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="7d3c9-109">Return values</span></span>

<span data-ttu-id="7d3c9-110">*Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="7d3c9-110">*Integer*</span></span>

<span data-ttu-id="7d3c9-111">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="7d3c9-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="7d3c9-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="7d3c9-112">Example</span></span>

<span data-ttu-id="7d3c9-113">`LEN ("Sample")` palauttaa **6**.</span><span class="sxs-lookup"><span data-stu-id="7d3c9-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d3c9-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="7d3c9-114">Additional resources</span></span>

[<span data-ttu-id="7d3c9-115">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="7d3c9-115">Text functions</span></span>](er-functions-category-text.md)
