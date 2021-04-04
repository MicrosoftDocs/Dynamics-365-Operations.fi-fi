---
title: INDEX ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) INDEX-funktiota käytetään.
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
ms.openlocfilehash: 88be8f8bdc82bf3eab5c99e72046c794d8fac361
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566922"
---
# <a name="index-er-function"></a><span data-ttu-id="e4a8d-103">INDEX ER-funktio</span><span class="sxs-lookup"><span data-stu-id="e4a8d-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4a8d-104">`INDEX`-funktio palauttaa *Säilö (tietue)*-arvon, joka on valittu määritetyn numeroindeksin avulla määritetyssä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="e4a8d-105">Jos indeksi on määritellyn luettelon tietueiden ulkopuolella, poikkeus heitetään.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4a8d-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="e4a8d-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="e4a8d-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="e4a8d-107">Arguments</span></span>

<span data-ttu-id="e4a8d-108">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="e4a8d-108">`list`: *Record list*</span></span>

<span data-ttu-id="e4a8d-109">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="e4a8d-110">`index`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="e4a8d-110">`index`: *Integer*</span></span>

<span data-ttu-id="e4a8d-111">Numeerinen indeksi, joka ilmaisee halutun tietueen sijainnin määritetyssä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="e4a8d-112">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="e4a8d-112">Return values</span></span>

<span data-ttu-id="e4a8d-113">*Kontti (tietue)*</span><span class="sxs-lookup"><span data-stu-id="e4a8d-113">*Container (record)*</span></span>

<span data-ttu-id="e4a8d-114">Tuloksena oleva tietueen arvo.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="e4a8d-115">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="e4a8d-115">Example 1</span></span>

<span data-ttu-id="e4a8d-116">Jos syötät tietolähteen **DS** *laskettuun kenttätyyppiin* ja se sisältää lausekkeen `SPLIT ("A|B|C", "|")`, lauseke `DS.Value`, palauttaa tekstiarvon **B** tämän tietueluettelon toiselle tietueelle.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="e4a8d-117">Lauseke `INDEX (SPLIT ("A|B|C", "|"), 2).Value` palauttaa myös tekstiarvon **B**.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="e4a8d-118">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="e4a8d-118">Example 2</span></span>

<span data-ttu-id="e4a8d-119">Jos syötät *Lasketun kenttä* -tyypin **DS**-tietolähteen, ja se sisältää lausekkeen `SPLIT ("A|B|C", "|")`, lauseke `INDEX (SPLIT ("A|B|C", "|"), 4).Value` heittää poikkeuksen suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e4a8d-120">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e4a8d-120">Additional resources</span></span>

[<span data-ttu-id="e4a8d-121">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="e4a8d-121">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]