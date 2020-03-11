---
title: SPLITLIST ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) SPLITLIST-funktiota käytetään.
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
ms.openlocfilehash: 56ef02e3ea0ca2207ccdc79468a9ea4c1fbe8f95
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041880"
---
# <span data-ttu-id="12b92-103"><a name="SPLITLIST">SPLITLIST ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="12b92-103"><a name="SPLITLIST">SPLITLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12b92-104">`SPLITLIST`-funktio jakaa määritetyn luettelon aliluetteloiksi (tai eriksi), joissa on tietty määrä tietueita.</span><span class="sxs-lookup"><span data-stu-id="12b92-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="12b92-105">Sitten se palauttaa tuloksen uutena *Tietueluettelon* arvona, joka koostuu eristä.</span><span class="sxs-lookup"><span data-stu-id="12b92-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="12b92-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="12b92-106">Syntax</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="12b92-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="12b92-107">Arguments</span></span>

<span data-ttu-id="12b92-108">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="12b92-108">`list`: *Record list*</span></span>

<span data-ttu-id="12b92-109">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="12b92-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="12b92-110">`number`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="12b92-110">`number`: *Integer*</span></span>

<span data-ttu-id="12b92-111">Tietueiden enimmäismäärä erää kohti.</span><span class="sxs-lookup"><span data-stu-id="12b92-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="12b92-112">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="12b92-112">Return values</span></span>

<span data-ttu-id="12b92-113">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="12b92-113">*Record list*</span></span>

<span data-ttu-id="12b92-114">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="12b92-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="12b92-115">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="12b92-115">Usage notes</span></span>

<span data-ttu-id="12b92-116">Palautettu eräluettelo, joka sisältää seuraavat elementit:</span><span class="sxs-lookup"><span data-stu-id="12b92-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="12b92-117">**Arvo:** *Luettelo*</span><span class="sxs-lookup"><span data-stu-id="12b92-117">**Value:** *List*</span></span>

    <span data-ttu-id="12b92-118">Nykyiseen erään kuuluvien tietueiden luettelo.</span><span class="sxs-lookup"><span data-stu-id="12b92-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="12b92-119">**BatchNumber:** *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="12b92-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="12b92-120">Palautetun luettelon nykyisen erän numero.</span><span class="sxs-lookup"><span data-stu-id="12b92-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="12b92-121">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="12b92-121">Example</span></span>

<span data-ttu-id="12b92-122">Seuraavassa kuvassa **Rivit**-tietolähde luodaan tietueluettelo, jossa on kolme tietuetta.</span><span class="sxs-lookup"><span data-stu-id="12b92-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="12b92-123">Tämä luettelo on jaettu eriin, joista kussakin on enintään kaksi tietuetta.</span><span class="sxs-lookup"><span data-stu-id="12b92-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="12b92-124">Seuraavassa kuvassa on suunnitellun muodon asettelu.</span><span class="sxs-lookup"><span data-stu-id="12b92-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="12b92-125">Tässä muodon asettelussa sidonnat **Rivit**-tietolähde luodaan muodostamaan tulos XML-muodossa.</span><span class="sxs-lookup"><span data-stu-id="12b92-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="12b92-126">Tämä tulos esittää kunkin erän erilliset solmut ja sen tietueet.</span><span class="sxs-lookup"><span data-stu-id="12b92-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="12b92-127">Seuraavassa kuvassa on tulos, kun suunniteltu muoto suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="12b92-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="12b92-128">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="12b92-128">Additional resources</span></span>

[<span data-ttu-id="12b92-129">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="12b92-129">List functions</span></span>](er-functions-category-list.md)
