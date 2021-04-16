---
title: UPPER ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) UPPER-funktiota käytetään.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 0e0e9837765914c657a72c5ce04c6f565fa13788
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749138"
---
# <a name="upper-er-function"></a><span data-ttu-id="f11a5-103">UPPER ER-funktio</span><span class="sxs-lookup"><span data-stu-id="f11a5-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f11a5-104">`UPPER`-funktio palauttaa määritetyn tekstimerkkijonon *Merkkijono*-arvona sen jälkeen, kun se on muunnettu isoiksi kirjaimiksi.</span><span class="sxs-lookup"><span data-stu-id="f11a5-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="f11a5-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="f11a5-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="f11a5-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="f11a5-106">Arguments</span></span>

<span data-ttu-id="f11a5-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="f11a5-107">`text`: *String*</span></span>

<span data-ttu-id="f11a5-108">*Merkkijono*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="f11a5-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f11a5-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="f11a5-109">Return values</span></span>

<span data-ttu-id="f11a5-110">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="f11a5-110">*String*</span></span>

<span data-ttu-id="f11a5-111">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="f11a5-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="f11a5-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="f11a5-112">Example</span></span>

<span data-ttu-id="f11a5-113">`UPPER ("Sample")` palauttaa arvon **MALLI**.</span><span class="sxs-lookup"><span data-stu-id="f11a5-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f11a5-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f11a5-114">Additional resources</span></span>

[<span data-ttu-id="f11a5-115">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="f11a5-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]