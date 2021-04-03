---
title: STRINGJOIN ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) STRINGJOIN-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 755e6481abb65dfecc8ddb6bceb032c8110095e2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568167"
---
# <a name="stringjoin-er-function"></a><span data-ttu-id="95e75-103">STRINGJOIN ER-funktio</span><span class="sxs-lookup"><span data-stu-id="95e75-103">STRINGJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95e75-104">`STRINGJOIN`-funktio palauttaa määritetystä luettelosta *merkkijonon*, joka koostuu määritetyn kentän ketjutetuista arvoista tietystä luettelosta.</span><span class="sxs-lookup"><span data-stu-id="95e75-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="95e75-105">Arvot voidaan erottaa määritetyllä erottimella.</span><span class="sxs-lookup"><span data-stu-id="95e75-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="95e75-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="95e75-106">Syntax</span></span>

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="95e75-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="95e75-107">Arguments</span></span>

<span data-ttu-id="95e75-108">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="95e75-108">`list`: *Record list*</span></span>

<span data-ttu-id="95e75-109">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="95e75-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="95e75-110">`field`: *Kenttä*</span><span class="sxs-lookup"><span data-stu-id="95e75-110">`field`: *Field*</span></span>

<span data-ttu-id="95e75-111">*Merkkijono*-tietotyypin kentän kelvollinen polku on määritetyssä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="95e75-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="95e75-112">`delimiter`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="95e75-112">`delimiter`: *String*</span></span>

<span data-ttu-id="95e75-113">Erotin, jota käytetään erottelemaan alimerkkijonoja.</span><span class="sxs-lookup"><span data-stu-id="95e75-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="95e75-114">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="95e75-114">Return values</span></span>

<span data-ttu-id="95e75-115">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="95e75-115">*String*</span></span>

<span data-ttu-id="95e75-116">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="95e75-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="95e75-117">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="95e75-117">Example</span></span>

<span data-ttu-id="95e75-118">Jos syötät `SPLIT("abc" , 1)` tietolähteeksi **DS**, lauseke `STRINGJOIN (DS, DS.Value, "-")` palauttaa arvon **a-b-c**.</span><span class="sxs-lookup"><span data-stu-id="95e75-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="95e75-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="95e75-119">Additional resources</span></span>

[<span data-ttu-id="95e75-120">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="95e75-120">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]