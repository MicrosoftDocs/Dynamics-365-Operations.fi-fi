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
ms.openlocfilehash: 3e0ba19e762574dde4f9038b87ce352d13f714f4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041052"
---
# <span data-ttu-id="93071-103"><a name="LEN">LEN ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="93071-103"><a name="LEN">LEN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93071-104">`LEN`-funktio palauttaa määritetystä luettelosta *Kokonaisluku*-arvon, joka esittää merkkien määrän määritetyssä merkkijonossa.</span><span class="sxs-lookup"><span data-stu-id="93071-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="93071-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="93071-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="93071-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="93071-106">Arguments</span></span>

<span data-ttu-id="93071-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="93071-107">`text`: *String*</span></span>

<span data-ttu-id="93071-108">*Merkkijono*-arvo, joka määrittää tekstin.</span><span class="sxs-lookup"><span data-stu-id="93071-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="93071-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="93071-109">Return values</span></span>

<span data-ttu-id="93071-110">*Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="93071-110">*Integer*</span></span>

<span data-ttu-id="93071-111">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="93071-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="93071-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="93071-112">Example</span></span>

<span data-ttu-id="93071-113">`LEN ("Sample")` palauttaa **6**.</span><span class="sxs-lookup"><span data-stu-id="93071-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="93071-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="93071-114">Additional resources</span></span>

[<span data-ttu-id="93071-115">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="93071-115">Text functions</span></span>](er-functions-category-text.md)
