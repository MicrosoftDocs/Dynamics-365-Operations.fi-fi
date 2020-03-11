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
ms.openlocfilehash: 10a98e98d913b0b4fe36690f7effd5d8d9a3faf4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041788"
---
# <span data-ttu-id="87e90-103"><a name="STRINGJOIN">STRINGJOIN ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="87e90-103"><a name="STRINGJOIN">STRINGJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87e90-104">`STRINGJOIN`-funktio palauttaa määritetystä luettelosta *merkkijonon*, joka koostuu määritetyn kentän ketjutetuista arvoista tietystä luettelosta.</span><span class="sxs-lookup"><span data-stu-id="87e90-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="87e90-105">Arvot voidaan erottaa määritetyllä erottimella.</span><span class="sxs-lookup"><span data-stu-id="87e90-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="87e90-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="87e90-106">Syntax</span></span>

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="87e90-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="87e90-107">Arguments</span></span>

<span data-ttu-id="87e90-108">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="87e90-108">`list`: *Record list*</span></span>

<span data-ttu-id="87e90-109">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="87e90-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="87e90-110">`field`: *Kenttä*</span><span class="sxs-lookup"><span data-stu-id="87e90-110">`field`: *Field*</span></span>

<span data-ttu-id="87e90-111">*Merkkijono*-tietotyypin kentän kelvollinen polku on määritetyssä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="87e90-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="87e90-112">`delimiter`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="87e90-112">`delimiter`: *String*</span></span>

<span data-ttu-id="87e90-113">Erotin, jota käytetään erottelemaan alimerkkijonoja.</span><span class="sxs-lookup"><span data-stu-id="87e90-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="87e90-114">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="87e90-114">Return values</span></span>

<span data-ttu-id="87e90-115">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="87e90-115">*String*</span></span>

<span data-ttu-id="87e90-116">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="87e90-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="87e90-117">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="87e90-117">Example</span></span>

<span data-ttu-id="87e90-118">Jos syötät `SPLIT("abc" , 1)` tietolähteeksi **DS**, lauseke `STRINGJOIN (DS, DS.Value, "-")` palauttaa arvon **a-b-c**.</span><span class="sxs-lookup"><span data-stu-id="87e90-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87e90-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="87e90-119">Additional resources</span></span>

[<span data-ttu-id="87e90-120">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="87e90-120">List functions</span></span>](er-functions-category-list.md)
