---
title: LOWER ER-toiminto
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) LOWER-funktiota käytetään.
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
ms.openlocfilehash: b016feb0c907ef384eae91840791c357d61cf634
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916818"
---
# <span data-ttu-id="30b8a-103"><a name="LOWER">LOWER ER-toiminto</a></span><span class="sxs-lookup"><span data-stu-id="30b8a-103"><a name="LOWER">LOWER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30b8a-104">`LOWER`-funktio palauttaa määritetyn tekstimerkkijonon *Merkkijono*-arvona sen jälkeen, kun se on muunnettu pieniksi kirjaimiksi.</span><span class="sxs-lookup"><span data-stu-id="30b8a-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="30b8a-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="30b8a-105">Syntax</span></span>

```
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="30b8a-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="30b8a-106">Arguments</span></span>

<span data-ttu-id="30b8a-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="30b8a-107">`text`: *String*</span></span>

<span data-ttu-id="30b8a-108">*Merkkijono*-arvo, joka määrittää tekstin.</span><span class="sxs-lookup"><span data-stu-id="30b8a-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="30b8a-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="30b8a-109">Return values</span></span>

<span data-ttu-id="30b8a-110">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="30b8a-110">*String*</span></span>

<span data-ttu-id="30b8a-111">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="30b8a-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="30b8a-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="30b8a-112">Example</span></span>

<span data-ttu-id="30b8a-113">`LOWER ("Sample")` palauttaa arvon **Malli**.</span><span class="sxs-lookup"><span data-stu-id="30b8a-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30b8a-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="30b8a-114">Additional resources</span></span>

[<span data-ttu-id="30b8a-115">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="30b8a-115">Text functions</span></span>](er-functions-category-text.md)
