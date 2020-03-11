---
title: ISEMPTY ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ISEMPTY-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 6adca3c95c10e7d4b3287561925a9d9fe8a74121
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042041"
---
# <span data-ttu-id="26191-103"><a name="ISEMPTY">ISEMPTY ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="26191-103"><a name="ISEMPTY">ISEMPTY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26191-104">`ISEMPTY` funktio palauttaa *totuusarvon* **TOSI**, jos määritetty luettelo ei sisällä tietueita.</span><span class="sxs-lookup"><span data-stu-id="26191-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="26191-105">Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="26191-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="26191-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="26191-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="26191-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="26191-107">Arguments</span></span>

<span data-ttu-id="26191-108">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="26191-108">`list`: *Record list*</span></span>

<span data-ttu-id="26191-109">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="26191-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="26191-110">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="26191-110">Return values</span></span>

<span data-ttu-id="26191-111">*Boolen arvo*</span><span class="sxs-lookup"><span data-stu-id="26191-111">*Boolean*</span></span>

<span data-ttu-id="26191-112">Tuloksena oleva *Totuusarvo*-arvo.</span><span class="sxs-lookup"><span data-stu-id="26191-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="26191-113">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="26191-113">Example 1</span></span>

<span data-ttu-id="26191-114">Jos syötät *Lasketun kenttä*-tyypin **DS**-tietolähteen, ja se sisältää lausekkeen `SPLIT ("A|B|C", "|")`, lauseke `ISEMPTY(DS)` palauttaa arvon **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="26191-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="26191-115">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="26191-115">Example 2</span></span>

<span data-ttu-id="26191-116">Lauseke `ISEMPTY (SPLIT ("",1))` palauttaa arvon **TOSI**.</span><span class="sxs-lookup"><span data-stu-id="26191-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26191-117">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="26191-117">Additional resources</span></span>

[<span data-ttu-id="26191-118">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="26191-118">List functions</span></span>](er-functions-category-list.md)
