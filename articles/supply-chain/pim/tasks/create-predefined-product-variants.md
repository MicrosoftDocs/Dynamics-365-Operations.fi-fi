---
title: Luo ennalta määritetyt tuotevariantit
description: Tässä menettelyssä selvitetään tuotevariantien luonti päätuotteelle käyttämällä tuotedimensioiden yhdistelmiä.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6fa9c6d4862a49bbf0b5ecbb8c0c3d573e0f49e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427073"
---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="36dcf-103">Luo ennalta määritetyt tuotevariantit</span><span class="sxs-lookup"><span data-stu-id="36dcf-103">Create predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="36dcf-104">Tässä menettelyssä selvitetään tuotevariantien luonti päätuotteelle käyttämällä tuotedimensioiden yhdistelmiä.</span><span class="sxs-lookup"><span data-stu-id="36dcf-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="36dcf-105">Tämän menettelyn luomiseen on käytetty USMF-demoyritystä.</span><span class="sxs-lookup"><span data-stu-id="36dcf-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="36dcf-106">Luo päätuote</span><span class="sxs-lookup"><span data-stu-id="36dcf-106">Create a product master</span></span>
1. <span data-ttu-id="36dcf-107">Siirry kohtaan Tuotetietojen hallinta > Tuotteet > Päätuotteet.</span><span class="sxs-lookup"><span data-stu-id="36dcf-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="36dcf-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="36dcf-108">Click New.</span></span>
3. <span data-ttu-id="36dcf-109">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="36dcf-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="36dcf-110">Tuotetunnuksen antaminen manuaalisesti on pakollista vain, jos tuotetunnuskenttään ei ole määritetty numerosarjaa.</span><span class="sxs-lookup"><span data-stu-id="36dcf-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="36dcf-111">Toisin sanoen, tämän vaiheen voi ohittaa, jos kentälle on määritetty numerosarja.</span><span class="sxs-lookup"><span data-stu-id="36dcf-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="36dcf-112">Kirjoita arvo Tuotteen nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="36dcf-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="36dcf-113">Syötä tai valitse arvo Tuotedimension ryhmä -kentässä.</span><span class="sxs-lookup"><span data-stu-id="36dcf-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="36dcf-114">Valitse tuotedimensioryhmäksi SizeCol (koko ja väri).</span><span class="sxs-lookup"><span data-stu-id="36dcf-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="36dcf-115">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="36dcf-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="36dcf-116">Lisää tuotedimensiot</span><span class="sxs-lookup"><span data-stu-id="36dcf-116">Add product dimensions</span></span>
1. <span data-ttu-id="36dcf-117">Valitse Tuotedimensiot.</span><span class="sxs-lookup"><span data-stu-id="36dcf-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="36dcf-118">Tässä esimerkissä havainnollistetaan, kuinka tuotedimensiot voi antaa käsin.</span><span class="sxs-lookup"><span data-stu-id="36dcf-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="36dcf-119">Voit myös valita koko-, väri- tai tyyliryhmän, joka sisältää haluamasi tuotedimension arvot.</span><span class="sxs-lookup"><span data-stu-id="36dcf-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="36dcf-120">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="36dcf-120">Click New.</span></span>
3. <span data-ttu-id="36dcf-121">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="36dcf-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="36dcf-122">Syötä tai valitse arvo Koko-kenttään.</span><span class="sxs-lookup"><span data-stu-id="36dcf-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="36dcf-123">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="36dcf-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="36dcf-124">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="36dcf-124">Click New.</span></span>
7. <span data-ttu-id="36dcf-125">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="36dcf-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="36dcf-126">Syötä tai valitse arvo Koko-kenttään.</span><span class="sxs-lookup"><span data-stu-id="36dcf-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="36dcf-127">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="36dcf-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="36dcf-128">Valitse Värit-välilehti.</span><span class="sxs-lookup"><span data-stu-id="36dcf-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="36dcf-129">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="36dcf-129">Click New.</span></span>
12. <span data-ttu-id="36dcf-130">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="36dcf-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="36dcf-131">Syötä tai valitse Väri-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="36dcf-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="36dcf-132">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="36dcf-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="36dcf-133">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="36dcf-133">Click New.</span></span>
16. <span data-ttu-id="36dcf-134">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="36dcf-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="36dcf-135">Syötä tai valitse Väri-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="36dcf-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="36dcf-136">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="36dcf-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="36dcf-137">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="36dcf-137">Click Save.</span></span>
20. <span data-ttu-id="36dcf-138">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="36dcf-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="36dcf-139">Luo tuotevariantit</span><span class="sxs-lookup"><span data-stu-id="36dcf-139">Generate product variants</span></span>
1. <span data-ttu-id="36dcf-140">Valitse Tuotevariantin koot.</span><span class="sxs-lookup"><span data-stu-id="36dcf-140">Click Product variants.</span></span>
2. <span data-ttu-id="36dcf-141">Valitse Muuttujaehdotukset.</span><span class="sxs-lookup"><span data-stu-id="36dcf-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="36dcf-142">Valitse Valitse kaikki.</span><span class="sxs-lookup"><span data-stu-id="36dcf-142">Click Select all.</span></span>
    * <span data-ttu-id="36dcf-143">Tässä esimerkissä kaikki mahdolliset muuttujat on valittu.</span><span class="sxs-lookup"><span data-stu-id="36dcf-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="36dcf-144">Jos ainoastaan saatavilla olevien tuotedimensioyhdistelmien alijoukkoa käytetään varianttien luomiseen, voit valita yksittäisiä merkintöjä.</span><span class="sxs-lookup"><span data-stu-id="36dcf-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="36dcf-145">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="36dcf-145">Click Create.</span></span>
    * <span data-ttu-id="36dcf-146">Voit luoda kuvaukset kaikille varianteille tuotedimensioarvojen yhdistelmien perusteella.</span><span class="sxs-lookup"><span data-stu-id="36dcf-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="36dcf-147">Kuvaukset ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="36dcf-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="36dcf-148">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="36dcf-148">Click Save.</span></span>

