---
title: Luo ennalta määritetyt tuotevariantit
description: Tässä menettelyssä selvitetään tuotevariantien luonti päätuotteelle käyttämällä tuotedimensioiden yhdistelmiä.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab4f43957f7c661349714dbb0933ac3c1d19ab0e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550649"
---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="79c73-103">Luo ennalta määritetyt tuotevariantit</span><span class="sxs-lookup"><span data-stu-id="79c73-103">Create predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="79c73-104">Tässä menettelyssä selvitetään tuotevariantien luonti päätuotteelle käyttämällä tuotedimensioiden yhdistelmiä.</span><span class="sxs-lookup"><span data-stu-id="79c73-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="79c73-105">Tämän menettelyn luomiseen on käytetty USMF-demoyritystä.</span><span class="sxs-lookup"><span data-stu-id="79c73-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="79c73-106">Luo päätuote</span><span class="sxs-lookup"><span data-stu-id="79c73-106">Create a product master</span></span>
1. <span data-ttu-id="79c73-107">Siirry kohtaan Tuotetietojen hallinta > Tuotteet > Päätuotteet.</span><span class="sxs-lookup"><span data-stu-id="79c73-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="79c73-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="79c73-108">Click New.</span></span>
3. <span data-ttu-id="79c73-109">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="79c73-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="79c73-110">Tuotetunnuksen antaminen manuaalisesti on pakollista vain, jos tuotetunnuskenttään ei ole määritetty numerosarjaa.</span><span class="sxs-lookup"><span data-stu-id="79c73-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="79c73-111">Toisin sanoen, tämän vaiheen voi ohittaa, jos kentälle on määritetty numerosarja.</span><span class="sxs-lookup"><span data-stu-id="79c73-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="79c73-112">Kirjoita arvo Tuotteen nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="79c73-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="79c73-113">Syötä tai valitse arvo Tuotedimension ryhmä -kentässä.</span><span class="sxs-lookup"><span data-stu-id="79c73-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="79c73-114">Valitse tuotedimensioryhmäksi SizeCol (koko ja väri).</span><span class="sxs-lookup"><span data-stu-id="79c73-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="79c73-115">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="79c73-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="79c73-116">Lisää tuotedimensiot</span><span class="sxs-lookup"><span data-stu-id="79c73-116">Add product dimensions</span></span>
1. <span data-ttu-id="79c73-117">Valitse Tuotedimensiot.</span><span class="sxs-lookup"><span data-stu-id="79c73-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="79c73-118">Tässä esimerkissä havainnollistetaan, kuinka tuotedimensiot voi antaa käsin.</span><span class="sxs-lookup"><span data-stu-id="79c73-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="79c73-119">Voit myös valita koko-, väri- tai tyyliryhmän, joka sisältää haluamasi tuotedimension arvot.</span><span class="sxs-lookup"><span data-stu-id="79c73-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="79c73-120">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="79c73-120">Click New.</span></span>
3. <span data-ttu-id="79c73-121">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="79c73-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="79c73-122">Syötä tai valitse arvo Koko-kenttään.</span><span class="sxs-lookup"><span data-stu-id="79c73-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="79c73-123">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="79c73-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="79c73-124">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="79c73-124">Click New.</span></span>
7. <span data-ttu-id="79c73-125">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="79c73-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="79c73-126">Syötä tai valitse arvo Koko-kenttään.</span><span class="sxs-lookup"><span data-stu-id="79c73-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="79c73-127">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="79c73-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="79c73-128">Valitse Värit-välilehti.</span><span class="sxs-lookup"><span data-stu-id="79c73-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="79c73-129">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="79c73-129">Click New.</span></span>
12. <span data-ttu-id="79c73-130">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="79c73-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="79c73-131">Syötä tai valitse Väri-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="79c73-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="79c73-132">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="79c73-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="79c73-133">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="79c73-133">Click New.</span></span>
16. <span data-ttu-id="79c73-134">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="79c73-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="79c73-135">Syötä tai valitse Väri-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="79c73-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="79c73-136">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="79c73-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="79c73-137">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="79c73-137">Click Save.</span></span>
20. <span data-ttu-id="79c73-138">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="79c73-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="79c73-139">Luo tuotevariantit</span><span class="sxs-lookup"><span data-stu-id="79c73-139">Generate product variants</span></span>
1. <span data-ttu-id="79c73-140">Valitse Tuotevariantin koot.</span><span class="sxs-lookup"><span data-stu-id="79c73-140">Click Product variants.</span></span>
2. <span data-ttu-id="79c73-141">Valitse Muuttujaehdotukset.</span><span class="sxs-lookup"><span data-stu-id="79c73-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="79c73-142">Valitse Valitse kaikki.</span><span class="sxs-lookup"><span data-stu-id="79c73-142">Click Select all.</span></span>
    * <span data-ttu-id="79c73-143">Tässä esimerkissä kaikki mahdolliset muuttujat on valittu.</span><span class="sxs-lookup"><span data-stu-id="79c73-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="79c73-144">Jos ainoastaan saatavilla olevien tuotedimensioyhdistelmien alijoukkoa käytetään varianttien luomiseen, voit valita yksittäisiä merkintöjä.</span><span class="sxs-lookup"><span data-stu-id="79c73-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="79c73-145">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="79c73-145">Click Create.</span></span>
    * <span data-ttu-id="79c73-146">Voit luoda kuvaukset kaikille varianteille tuotedimensioarvojen yhdistelmien perusteella.</span><span class="sxs-lookup"><span data-stu-id="79c73-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="79c73-147">Kuvaukset ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="79c73-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="79c73-148">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="79c73-148">Click Save.</span></span>

