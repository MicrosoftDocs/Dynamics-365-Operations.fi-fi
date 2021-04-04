---
title: LEN ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) LEN-funktiota käytetään.
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
ms.openlocfilehash: fce4b5311d84364310b76545a775f1cc8db2fd70
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569965"
---
# <a name="len-er-function"></a><span data-ttu-id="b7d31-103">LEN ER -funktio</span><span class="sxs-lookup"><span data-stu-id="b7d31-103">LEN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7d31-104">`LEN`-funktio palauttaa määritetystä luettelosta *Kokonaisluku*-arvon, joka esittää merkkien määrän määritetyssä merkkijonossa.</span><span class="sxs-lookup"><span data-stu-id="b7d31-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7d31-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="b7d31-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="b7d31-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="b7d31-106">Arguments</span></span>

<span data-ttu-id="b7d31-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="b7d31-107">`text`: *String*</span></span>

<span data-ttu-id="b7d31-108">*Merkkijono*-arvo, joka määrittää tekstin.</span><span class="sxs-lookup"><span data-stu-id="b7d31-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="b7d31-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="b7d31-109">Return values</span></span>

<span data-ttu-id="b7d31-110">*Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="b7d31-110">*Integer*</span></span>

<span data-ttu-id="b7d31-111">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="b7d31-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="b7d31-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="b7d31-112">Example</span></span>

<span data-ttu-id="b7d31-113">`LEN ("Sample")` palauttaa **6**.</span><span class="sxs-lookup"><span data-stu-id="b7d31-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b7d31-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b7d31-114">Additional resources</span></span>

[<span data-ttu-id="b7d31-115">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="b7d31-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]