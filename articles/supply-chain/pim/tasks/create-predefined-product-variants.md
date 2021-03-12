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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d07a090dbd41eb17e8d604887435bbb8b07e8d9e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966927"
---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="ffe11-103">Luo ennalta määritetyt tuotevariantit</span><span class="sxs-lookup"><span data-stu-id="ffe11-103">Create predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ffe11-104">Tässä menettelyssä selvitetään tuotevariantien luonti päätuotteelle käyttämällä tuotedimensioiden yhdistelmiä.</span><span class="sxs-lookup"><span data-stu-id="ffe11-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="ffe11-105">Tämän menettelyn luomiseen on käytetty USMF-demoyritystä.</span><span class="sxs-lookup"><span data-stu-id="ffe11-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="ffe11-106">Luo päätuote</span><span class="sxs-lookup"><span data-stu-id="ffe11-106">Create a product master</span></span>
1. <span data-ttu-id="ffe11-107">Siirry kohtaan Tuotetietojen hallinta > Tuotteet > Päätuotteet.</span><span class="sxs-lookup"><span data-stu-id="ffe11-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="ffe11-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ffe11-108">Click New.</span></span>
3. <span data-ttu-id="ffe11-109">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ffe11-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="ffe11-110">Tuotetunnuksen antaminen manuaalisesti on pakollista vain, jos tuotetunnuskenttään ei ole määritetty numerosarjaa.</span><span class="sxs-lookup"><span data-stu-id="ffe11-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="ffe11-111">Toisin sanoen, tämän vaiheen voi ohittaa, jos kentälle on määritetty numerosarja.</span><span class="sxs-lookup"><span data-stu-id="ffe11-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="ffe11-112">Kirjoita arvo Tuotteen nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ffe11-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="ffe11-113">Syötä tai valitse arvo Tuotedimension ryhmä -kentässä.</span><span class="sxs-lookup"><span data-stu-id="ffe11-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ffe11-114">Valitse tuotedimensioryhmäksi SizeCol (koko ja väri).</span><span class="sxs-lookup"><span data-stu-id="ffe11-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="ffe11-115">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ffe11-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="ffe11-116">Lisää tuotedimensiot</span><span class="sxs-lookup"><span data-stu-id="ffe11-116">Add product dimensions</span></span>
1. <span data-ttu-id="ffe11-117">Valitse Tuotedimensiot.</span><span class="sxs-lookup"><span data-stu-id="ffe11-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="ffe11-118">Tässä esimerkissä havainnollistetaan, kuinka tuotedimensiot voi antaa käsin.</span><span class="sxs-lookup"><span data-stu-id="ffe11-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="ffe11-119">Voit myös valita koko-, väri- tai tyyliryhmän, joka sisältää haluamasi tuotedimension arvot.</span><span class="sxs-lookup"><span data-stu-id="ffe11-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="ffe11-120">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ffe11-120">Click New.</span></span>
3. <span data-ttu-id="ffe11-121">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ffe11-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ffe11-122">Syötä tai valitse arvo Koko-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ffe11-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="ffe11-123">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ffe11-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="ffe11-124">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ffe11-124">Click New.</span></span>
7. <span data-ttu-id="ffe11-125">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ffe11-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="ffe11-126">Syötä tai valitse arvo Koko-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ffe11-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="ffe11-127">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ffe11-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="ffe11-128">Valitse Värit-välilehti.</span><span class="sxs-lookup"><span data-stu-id="ffe11-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="ffe11-129">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ffe11-129">Click New.</span></span>
12. <span data-ttu-id="ffe11-130">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ffe11-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="ffe11-131">Syötä tai valitse Väri-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="ffe11-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="ffe11-132">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ffe11-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="ffe11-133">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ffe11-133">Click New.</span></span>
16. <span data-ttu-id="ffe11-134">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ffe11-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="ffe11-135">Syötä tai valitse Väri-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="ffe11-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="ffe11-136">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ffe11-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="ffe11-137">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="ffe11-137">Click Save.</span></span>
20. <span data-ttu-id="ffe11-138">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ffe11-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="ffe11-139">Luo tuotevariantit</span><span class="sxs-lookup"><span data-stu-id="ffe11-139">Generate product variants</span></span>
1. <span data-ttu-id="ffe11-140">Valitse Tuotevariantin koot.</span><span class="sxs-lookup"><span data-stu-id="ffe11-140">Click Product variants.</span></span>
2. <span data-ttu-id="ffe11-141">Valitse Muuttujaehdotukset.</span><span class="sxs-lookup"><span data-stu-id="ffe11-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="ffe11-142">Valitse Valitse kaikki.</span><span class="sxs-lookup"><span data-stu-id="ffe11-142">Click Select all.</span></span>
    * <span data-ttu-id="ffe11-143">Tässä esimerkissä kaikki mahdolliset muuttujat on valittu.</span><span class="sxs-lookup"><span data-stu-id="ffe11-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="ffe11-144">Jos ainoastaan saatavilla olevien tuotedimensioyhdistelmien alijoukkoa käytetään varianttien luomiseen, voit valita yksittäisiä merkintöjä.</span><span class="sxs-lookup"><span data-stu-id="ffe11-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="ffe11-145">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="ffe11-145">Click Create.</span></span>
    * <span data-ttu-id="ffe11-146">Voit luoda kuvaukset kaikille varianteille tuotedimensioarvojen yhdistelmien perusteella.</span><span class="sxs-lookup"><span data-stu-id="ffe11-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="ffe11-147">Kuvaukset ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="ffe11-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="ffe11-148">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="ffe11-148">Click Save.</span></span>

