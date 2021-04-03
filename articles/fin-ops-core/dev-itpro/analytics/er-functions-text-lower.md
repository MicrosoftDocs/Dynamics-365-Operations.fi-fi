---
title: LOWER ER-toiminto
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) LOWER-funktiota käytetään.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: e507a17f5125a3cba0d2434a1aaec0f04f0cd388
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562780"
---
# <a name="lower-er-function"></a><span data-ttu-id="75e59-103">LOWER ER-toiminto</span><span class="sxs-lookup"><span data-stu-id="75e59-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75e59-104">`LOWER`-funktio palauttaa määritetyn tekstimerkkijonon *Merkkijono*-arvona sen jälkeen, kun se on muunnettu pieniksi kirjaimiksi.</span><span class="sxs-lookup"><span data-stu-id="75e59-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="75e59-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="75e59-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="75e59-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="75e59-106">Arguments</span></span>

<span data-ttu-id="75e59-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="75e59-107">`text`: *String*</span></span>

<span data-ttu-id="75e59-108">*Merkkijono*-arvo, joka määrittää tekstin.</span><span class="sxs-lookup"><span data-stu-id="75e59-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="75e59-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="75e59-109">Return values</span></span>

<span data-ttu-id="75e59-110">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="75e59-110">*String*</span></span>

<span data-ttu-id="75e59-111">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="75e59-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="75e59-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="75e59-112">Example</span></span>

<span data-ttu-id="75e59-113">`LOWER ("Sample")` palauttaa arvon **Malli**.</span><span class="sxs-lookup"><span data-stu-id="75e59-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="75e59-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="75e59-114">Additional resources</span></span>

[<span data-ttu-id="75e59-115">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="75e59-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]