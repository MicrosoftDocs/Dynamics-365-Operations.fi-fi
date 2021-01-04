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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3e594138ef8e28f1b3aaf333026fa8f9e55cca0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688338"
---
# <a name="upper-er-function"></a><span data-ttu-id="54506-103">UPPER ER-funktio</span><span class="sxs-lookup"><span data-stu-id="54506-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54506-104">`UPPER`-funktio palauttaa määritetyn tekstimerkkijonon *Merkkijono*-arvona sen jälkeen, kun se on muunnettu isoiksi kirjaimiksi.</span><span class="sxs-lookup"><span data-stu-id="54506-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="54506-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="54506-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="54506-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="54506-106">Arguments</span></span>

<span data-ttu-id="54506-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="54506-107">`text`: *String*</span></span>

<span data-ttu-id="54506-108">*Merkkijono*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="54506-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="54506-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="54506-109">Return values</span></span>

<span data-ttu-id="54506-110">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="54506-110">*String*</span></span>

<span data-ttu-id="54506-111">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="54506-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="54506-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="54506-112">Example</span></span>

<span data-ttu-id="54506-113">`UPPER ("Sample")` palauttaa arvon **MALLI**.</span><span class="sxs-lookup"><span data-stu-id="54506-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="54506-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="54506-114">Additional resources</span></span>

[<span data-ttu-id="54506-115">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="54506-115">Text functions</span></span>](er-functions-category-text.md)
