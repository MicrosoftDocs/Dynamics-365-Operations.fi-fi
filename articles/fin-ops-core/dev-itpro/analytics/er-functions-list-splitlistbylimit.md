---
title: SPLITLISTBYLIMIT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) SPLITLISTBYLIMIT-funktiota käytetään.
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
ms.openlocfilehash: f9b740b7d46fcfdf0d0b08d03411017cf909265d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916174"
---
# <span data-ttu-id="f69b7-103"><a name="SPLITLISTBYLIMIT">SPLITLISTBYLIMIT ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="f69b7-103"><a name="SPLITLISTBYLIMIT">SPLITLISTBYLIMIT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f69b7-104">`SPLITLISTBYLIMIT`-funktio jakaa määritetyn luettelon uuteen aliluetteloon (erät).</span><span class="sxs-lookup"><span data-stu-id="f69b7-104">The `SPLITLISTBYLIMIT` function splits the specified list into a new list of sublists (batches).</span></span> <span data-ttu-id="f69b7-105">Kunkin erän tietueiden määrä lasketaan dynaamisesti.</span><span class="sxs-lookup"><span data-stu-id="f69b7-105">The number of records in each batch is dynamically calculated.</span></span> <span data-ttu-id="f69b7-106">Sitten funktio palauttaa tuloksen uutena *Tietueluettelon* arvona, joka koostuu eristä.</span><span class="sxs-lookup"><span data-stu-id="f69b7-106">The function then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="f69b7-107">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="f69b7-107">Syntax</span></span>

```
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a><span data-ttu-id="f69b7-108">Argumentit</span><span class="sxs-lookup"><span data-stu-id="f69b7-108">Arguments</span></span>

<span data-ttu-id="f69b7-109">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="f69b7-109">`list`: *Record list*</span></span>

<span data-ttu-id="f69b7-110">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="f69b7-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="f69b7-111">`limit value`: *Kokonaisluku* tai *Todellinen*</span><span class="sxs-lookup"><span data-stu-id="f69b7-111">`limit value`: *Integer* or *Real*</span></span>

<span data-ttu-id="f69b7-112">Enimmäisarvo, jonka avulla alkuperäinen luettelo jaetaan eriin.</span><span class="sxs-lookup"><span data-stu-id="f69b7-112">The maximum value of the limit that is used to split the original list into batches.</span></span>

<span data-ttu-id="f69b7-113">`limit source`: *Kenttä*</span><span class="sxs-lookup"><span data-stu-id="f69b7-113">`limit source`: *Field*</span></span>

<span data-ttu-id="f69b7-114">*Kokonaisluku*- tai *Todellinen*-tyypin kentän kelvollinen polku on määritetyssä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="f69b7-114">The valid path of a field of the *Integer* or *Real* type in the specified list.</span></span> <span data-ttu-id="f69b7-115">Tämän kentän arvo määrittää vaiheen, jonka kokonaissumma on kasvanut.</span><span class="sxs-lookup"><span data-stu-id="f69b7-115">The value of this field defines the step that the total sum is increased on.</span></span>

## <a name="return-values"></a><span data-ttu-id="f69b7-116">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="f69b7-116">Return values</span></span>

<span data-ttu-id="f69b7-117">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="f69b7-117">*Record list*</span></span>

<span data-ttu-id="f69b7-118">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="f69b7-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f69b7-119">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="f69b7-119">Usage notes</span></span>

<span data-ttu-id="f69b7-120">Palautettu eräluettelo, joka sisältää seuraavat elementit:</span><span class="sxs-lookup"><span data-stu-id="f69b7-120">The list of batches that is returned contains the following elements:</span></span>

- <span data-ttu-id="f69b7-121">**Arvo**: *Luettelo*</span><span class="sxs-lookup"><span data-stu-id="f69b7-121">**Value**: *List*</span></span>

    <span data-ttu-id="f69b7-122">Nykyiseen erään kuuluvien tietueiden luettelo.</span><span class="sxs-lookup"><span data-stu-id="f69b7-122">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="f69b7-123">**BatchNumber**: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="f69b7-123">**BatchNumber**: *Integer*</span></span>

    <span data-ttu-id="f69b7-124">Palautetun luettelon nykyisen erän numero.</span><span class="sxs-lookup"><span data-stu-id="f69b7-124">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="f69b7-125">Rajaa ei käytetä tietyn alkuperäisen luettelon yhteen nimikkeeseen, jos lähderaja ylittää määritetyn rajan.</span><span class="sxs-lookup"><span data-stu-id="f69b7-125">The limit isn't applied to a single item of the original list if the limit source exceeds the defined limit.</span></span>

## <a name="example"></a><span data-ttu-id="f69b7-126">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="f69b7-126">Example</span></span>

<span data-ttu-id="f69b7-127">Seuraavassa kuvassa on sähköisen raportoinnin (ER) muodon.</span><span class="sxs-lookup"><span data-stu-id="f69b7-127">The following illustration shows an Electronic reporting (ER) format.</span></span>

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

<span data-ttu-id="f69b7-128">Seuraavissa kuvissa näkyvät muodossa käytetyt tietolähteet.</span><span class="sxs-lookup"><span data-stu-id="f69b7-128">The following illustration shows the data sources that are used for the format.</span></span>

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

<span data-ttu-id="f69b7-129">Seuraavassa kuvassa on tulos, kun muoto suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="f69b7-129">The following illustration shows the result when the format is run.</span></span> <span data-ttu-id="f69b7-130">Tässä tapauksessa tuloksena muoto, joka on kauppatavaroiden jäsentämätön luettelo.</span><span class="sxs-lookup"><span data-stu-id="f69b7-130">In this case, the output is a flat list of commodity items.</span></span>

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

<span data-ttu-id="f69b7-131">Seuraavissa kuvissa sama muoto on säädetty ilmaisemaan kauppatavarat erinä, jos yhdessä erässä on oltava kauppatavaroita, joiden kokonaispaino ei saa olla suurempi kuin 9.</span><span class="sxs-lookup"><span data-stu-id="f69b7-131">In the following illustrations, the same format has been adjusted so that it presents the list of commodity items in batches if a single batch must include commodities and the total weight should not exceed a limit of 9.</span></span>

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

<span data-ttu-id="f69b7-132">Seuraavassa kuvassa on tulos, kun säädetty muoto suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="f69b7-132">The following illustration shows the result when the adjusted format is run.</span></span>

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> <span data-ttu-id="f69b7-133">Rajaa ei sovellettu alkuperäisen luettelon viimeiseen nimikkeeseen, koska arvo (**11**) ylittää lähteen (**painon**) määritetyn raja-arvon (**9**).</span><span class="sxs-lookup"><span data-stu-id="f69b7-133">The limit isn't applied to the last item of the original list, because the value (**11**) of the limit source (**weight**) exceeds the defined limit (**9**).</span></span> <span data-ttu-id="f69b7-134">Ohita alaluettelot raportin luomisen aikana käyttämällä joko `WHERE`-funktiota tai vastaavan muodon elementin **Käytössä**-lauseketta tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="f69b7-134">To ignore sublists during report generation, use either the `WHERE` function or the **Enabled** expression of the corresponding format element, as you require.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f69b7-135">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f69b7-135">Additional resources</span></span>

[<span data-ttu-id="f69b7-136">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="f69b7-136">List functions</span></span>](er-functions-category-list.md)
