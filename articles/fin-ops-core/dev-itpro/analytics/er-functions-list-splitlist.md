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
ms.openlocfilehash: 950fc711f0e28eaee7fabc437ee16a022e1b705e
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744788"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="861ae-103">SPLITLIST ER-funktio</span><span class="sxs-lookup"><span data-stu-id="861ae-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="861ae-104">`SPLITLIST`-funktio jakaa määritetyn luettelon aliluetteloiksi (tai eriksi), joissa on tietty määrä tietueita.</span><span class="sxs-lookup"><span data-stu-id="861ae-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="861ae-105">Sitten se palauttaa tuloksen uutena *Tietueluettelon* arvona, joka koostuu eristä.</span><span class="sxs-lookup"><span data-stu-id="861ae-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="861ae-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="861ae-106">Syntax</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="861ae-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="861ae-107">Arguments</span></span>

<span data-ttu-id="861ae-108">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="861ae-108">`list`: *Record list*</span></span>

<span data-ttu-id="861ae-109">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="861ae-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="861ae-110">`number`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="861ae-110">`number`: *Integer*</span></span>

<span data-ttu-id="861ae-111">Tietueiden enimmäismäärä erää kohti.</span><span class="sxs-lookup"><span data-stu-id="861ae-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="861ae-112">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="861ae-112">Return values</span></span>

<span data-ttu-id="861ae-113">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="861ae-113">*Record list*</span></span>

<span data-ttu-id="861ae-114">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="861ae-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="861ae-115">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="861ae-115">Usage notes</span></span>

<span data-ttu-id="861ae-116">Palautettu eräluettelo, joka sisältää seuraavat elementit:</span><span class="sxs-lookup"><span data-stu-id="861ae-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="861ae-117">**Arvo:** *Luettelo*</span><span class="sxs-lookup"><span data-stu-id="861ae-117">**Value:** *List*</span></span>

    <span data-ttu-id="861ae-118">Nykyiseen erään kuuluvien tietueiden luettelo.</span><span class="sxs-lookup"><span data-stu-id="861ae-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="861ae-119">**BatchNumber:** *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="861ae-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="861ae-120">Palautetun luettelon nykyisen erän numero.</span><span class="sxs-lookup"><span data-stu-id="861ae-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="861ae-121">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="861ae-121">Example</span></span>

<span data-ttu-id="861ae-122">Seuraavassa kuvassa **Rivit**-tietolähde luodaan tietueluettelo, jossa on kolme tietuetta.</span><span class="sxs-lookup"><span data-stu-id="861ae-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="861ae-123">Tämä luettelo on jaettu eriin, joista kussakin on enintään kaksi tietuetta.</span><span class="sxs-lookup"><span data-stu-id="861ae-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="861ae-124">Seuraavassa kuvassa on suunnitellun muodon asettelu.</span><span class="sxs-lookup"><span data-stu-id="861ae-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="861ae-125">Tässä muodon asettelussa sidonnat **Rivit**-tietolähde luodaan muodostamaan tulos XML-muodossa.</span><span class="sxs-lookup"><span data-stu-id="861ae-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="861ae-126">Tämä tulos esittää kunkin erän erilliset solmut ja sen tietueet.</span><span class="sxs-lookup"><span data-stu-id="861ae-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="861ae-127">Seuraavassa kuvassa on tulos, kun suunniteltu muoto suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="861ae-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="861ae-128">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="861ae-128">Additional resources</span></span>

[<span data-ttu-id="861ae-129">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="861ae-129">List functions</span></span>](er-functions-category-list.md)
