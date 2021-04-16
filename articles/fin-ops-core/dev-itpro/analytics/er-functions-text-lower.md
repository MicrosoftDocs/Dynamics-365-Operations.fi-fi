---
title: LOWER ER-toiminto
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) LOWER-funktiota käytetään.
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: e684883d4262e4c3cd8a84d0a1c6f1d685bb650b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746288"
---
# <a name="lower-er-function"></a><span data-ttu-id="2d222-103">LOWER ER-toiminto</span><span class="sxs-lookup"><span data-stu-id="2d222-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d222-104">`LOWER`-funktio palauttaa määritetyn tekstimerkkijonon *Merkkijono*-arvona sen jälkeen, kun se on muunnettu pieniksi kirjaimiksi.</span><span class="sxs-lookup"><span data-stu-id="2d222-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d222-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="2d222-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="2d222-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="2d222-106">Arguments</span></span>

<span data-ttu-id="2d222-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="2d222-107">`text`: *String*</span></span>

<span data-ttu-id="2d222-108">*Merkkijono*-arvo, joka määrittää tekstin.</span><span class="sxs-lookup"><span data-stu-id="2d222-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="2d222-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="2d222-109">Return values</span></span>

<span data-ttu-id="2d222-110">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="2d222-110">*String*</span></span>

<span data-ttu-id="2d222-111">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="2d222-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="2d222-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="2d222-112">Example</span></span>

<span data-ttu-id="2d222-113">`LOWER ("Sample")` palauttaa arvon **Malli**.</span><span class="sxs-lookup"><span data-stu-id="2d222-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2d222-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2d222-114">Additional resources</span></span>

[<span data-ttu-id="2d222-115">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="2d222-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]