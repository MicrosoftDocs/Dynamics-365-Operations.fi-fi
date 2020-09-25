---
title: STRINGJOIN ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) STRINGJOIN-funktiota käytetään.
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
ms.openlocfilehash: 4f5d6b9a0f43902160d1ff7fa91b86a7e2c3422d
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743491"
---
# <a name="stringjoin-er-function"></a><span data-ttu-id="f1262-103">STRINGJOIN ER-funktio</span><span class="sxs-lookup"><span data-stu-id="f1262-103">STRINGJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1262-104">`STRINGJOIN`-funktio palauttaa määritetystä luettelosta *merkkijonon*, joka koostuu määritetyn kentän ketjutetuista arvoista tietystä luettelosta.</span><span class="sxs-lookup"><span data-stu-id="f1262-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="f1262-105">Arvot voidaan erottaa määritetyllä erottimella.</span><span class="sxs-lookup"><span data-stu-id="f1262-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1262-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="f1262-106">Syntax</span></span>

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="f1262-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="f1262-107">Arguments</span></span>

<span data-ttu-id="f1262-108">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="f1262-108">`list`: *Record list*</span></span>

<span data-ttu-id="f1262-109">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="f1262-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="f1262-110">`field`: *Kenttä*</span><span class="sxs-lookup"><span data-stu-id="f1262-110">`field`: *Field*</span></span>

<span data-ttu-id="f1262-111">*Merkkijono*-tietotyypin kentän kelvollinen polku on määritetyssä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="f1262-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="f1262-112">`delimiter`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="f1262-112">`delimiter`: *String*</span></span>

<span data-ttu-id="f1262-113">Erotin, jota käytetään erottelemaan alimerkkijonoja.</span><span class="sxs-lookup"><span data-stu-id="f1262-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="f1262-114">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="f1262-114">Return values</span></span>

<span data-ttu-id="f1262-115">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="f1262-115">*String*</span></span>

<span data-ttu-id="f1262-116">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="f1262-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="f1262-117">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="f1262-117">Example</span></span>

<span data-ttu-id="f1262-118">Jos syötät `SPLIT("abc" , 1)` tietolähteeksi **DS**, lauseke `STRINGJOIN (DS, DS.Value, "-")` palauttaa arvon **a-b-c**.</span><span class="sxs-lookup"><span data-stu-id="f1262-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f1262-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f1262-119">Additional resources</span></span>

[<span data-ttu-id="f1262-120">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="f1262-120">List functions</span></span>](er-functions-category-list.md)
