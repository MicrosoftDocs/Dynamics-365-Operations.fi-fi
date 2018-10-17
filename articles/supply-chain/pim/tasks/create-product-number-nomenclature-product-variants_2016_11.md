--- 
title: "Luo tuotenumeroiden nimikkeistö määritetyille tuotevarianteille"
description: "Tässä aiheessa kuvataan, miten tuotenumeroiden nimikkeistö määritetään konfiguroiduille tuotevarianteille ja miten se voidaan liittää konfiguroitavaan päätuotteeseen."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 800afdf075f0675185514158f3b712a0fe7675e3
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="54b50-103">Luo tuotenumeroiden nimikkeistö määritetyille tuotevarianteille</span><span class="sxs-lookup"><span data-stu-id="54b50-103">Create a product number nomenclature for configured product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54b50-104">Tässä aiheessa kuvataan, miten tuotenumeroiden nimikkeistö määritetään konfiguroiduille tuotevarianteille ja miten se voidaan liittää konfiguroitavaan päätuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="54b50-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="54b50-105">Tässä ohjeaiheessa kerrotaan myös, miten tuotteen kokoonpanomallin osan konfiguraationimikkeistö rakennetaan.</span><span class="sxs-lookup"><span data-stu-id="54b50-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="54b50-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="54b50-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="54b50-107">Uusi tuotenumeroiden nimikkeistö on määritetty päätuotteelle D0004.</span><span class="sxs-lookup"><span data-stu-id="54b50-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="54b50-108">Tuotesuunnittelija tekee yleensä tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="54b50-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="54b50-109">Tuotenumeroiden nimikkeistön luominen</span><span class="sxs-lookup"><span data-stu-id="54b50-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="54b50-110">Valitse Tuotevarianttimallin määritys.</span><span class="sxs-lookup"><span data-stu-id="54b50-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="54b50-111">Valitse Tuotenimikkeistö.</span><span class="sxs-lookup"><span data-stu-id="54b50-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="54b50-112">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="54b50-112">Click New.</span></span>
4. <span data-ttu-id="54b50-113">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="54b50-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="54b50-114">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="54b50-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="54b50-115">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="54b50-115">Click Add.</span></span>
7. <span data-ttu-id="54b50-116">Valitse Päätuotteen numero.</span><span class="sxs-lookup"><span data-stu-id="54b50-116">Click Product master number.</span></span>
8. <span data-ttu-id="54b50-117">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="54b50-117">Click Add.</span></span>
9. <span data-ttu-id="54b50-118">Valitse Tekstivakio.</span><span class="sxs-lookup"><span data-stu-id="54b50-118">Click Text constant.</span></span>
10. <span data-ttu-id="54b50-119">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="54b50-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="54b50-120">Kirjoita arvo Teksti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="54b50-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="54b50-121">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="54b50-121">Click Add.</span></span>
13. <span data-ttu-id="54b50-122">Valitse Konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="54b50-122">Click Configuration.</span></span>
14. <span data-ttu-id="54b50-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="54b50-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="54b50-124">Tuotenumeroiden nimikkeistön määrittäminen päätuotteelle</span><span class="sxs-lookup"><span data-stu-id="54b50-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="54b50-125">Valitse Päätuotteet.</span><span class="sxs-lookup"><span data-stu-id="54b50-125">Click Product masters.</span></span>
2. <span data-ttu-id="54b50-126">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="54b50-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="54b50-127">Voit esimerkiksi suodattaa Tuotenumero-kenttää arvolla D.</span><span class="sxs-lookup"><span data-stu-id="54b50-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="54b50-128">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="54b50-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="54b50-129">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="54b50-129">Click Edit.</span></span>
5. <span data-ttu-id="54b50-130">Valitse Käytä nimikkeistöä -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="54b50-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="54b50-131">Syötä tai valitse arvo Tuotevariantin numeron nimikkeistö -kentässä.</span><span class="sxs-lookup"><span data-stu-id="54b50-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="54b50-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="54b50-132">Close the page.</span></span>
8. <span data-ttu-id="54b50-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="54b50-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="54b50-134">Nimikkeistön luominen tuotemääritysmallin osalle</span><span class="sxs-lookup"><span data-stu-id="54b50-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="54b50-135">Valitse Tuotekonfiguraation mallit.</span><span class="sxs-lookup"><span data-stu-id="54b50-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="54b50-136">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="54b50-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="54b50-137">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="54b50-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="54b50-138">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="54b50-138">Click Edit.</span></span>
5. <span data-ttu-id="54b50-139">Valitse Käytä konfiguraationimikkeistöä -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="54b50-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="54b50-140">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="54b50-140">Click Add.</span></span>
7. <span data-ttu-id="54b50-141">Valitse Määritteen arvo.</span><span class="sxs-lookup"><span data-stu-id="54b50-141">Click Attribute value.</span></span>
8. <span data-ttu-id="54b50-142">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="54b50-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="54b50-143">Syötä tai valitse arvo kentässä Määrite.</span><span class="sxs-lookup"><span data-stu-id="54b50-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="54b50-144">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="54b50-144">Click Add.</span></span>
11. <span data-ttu-id="54b50-145">Valitse Tekstivakio.</span><span class="sxs-lookup"><span data-stu-id="54b50-145">Click Text constant.</span></span>
12. <span data-ttu-id="54b50-146">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="54b50-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="54b50-147">Kirjoita arvo Teksti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="54b50-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="54b50-148">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="54b50-148">Click Add.</span></span>
15. <span data-ttu-id="54b50-149">Valitse Määritteen arvo.</span><span class="sxs-lookup"><span data-stu-id="54b50-149">Click Attribute value.</span></span>
16. <span data-ttu-id="54b50-150">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="54b50-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="54b50-151">Syötä tai valitse arvo kentässä Määrite.</span><span class="sxs-lookup"><span data-stu-id="54b50-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="54b50-152">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="54b50-152">Click Add.</span></span>
19. <span data-ttu-id="54b50-153">Valitse Tekstivakio.</span><span class="sxs-lookup"><span data-stu-id="54b50-153">Click Text constant.</span></span>
20. <span data-ttu-id="54b50-154">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="54b50-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="54b50-155">Kirjoita arvo Teksti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="54b50-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="54b50-156">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="54b50-156">Click Add.</span></span>
23. <span data-ttu-id="54b50-157">Valitse Määritteen arvo.</span><span class="sxs-lookup"><span data-stu-id="54b50-157">Click Attribute value.</span></span>
24. <span data-ttu-id="54b50-158">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="54b50-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="54b50-159">Syötä tai valitse arvo kentässä Määrite.</span><span class="sxs-lookup"><span data-stu-id="54b50-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="54b50-160">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="54b50-160">Click Add.</span></span>
27. <span data-ttu-id="54b50-161">Valitse Tekstivakio.</span><span class="sxs-lookup"><span data-stu-id="54b50-161">Click Text constant.</span></span>
28. <span data-ttu-id="54b50-162">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="54b50-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="54b50-163">Kirjoita arvo Teksti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="54b50-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="54b50-164">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="54b50-164">Click Add.</span></span>
31. <span data-ttu-id="54b50-165">Valitse Määritteen arvo.</span><span class="sxs-lookup"><span data-stu-id="54b50-165">Click Attribute value.</span></span>
32. <span data-ttu-id="54b50-166">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="54b50-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="54b50-167">Syötä tai valitse arvo kentässä Määrite.</span><span class="sxs-lookup"><span data-stu-id="54b50-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="54b50-168">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="54b50-168">Click Add.</span></span>
35. <span data-ttu-id="54b50-169">Valitse Tekstivakio.</span><span class="sxs-lookup"><span data-stu-id="54b50-169">Click Text constant.</span></span>
36. <span data-ttu-id="54b50-170">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="54b50-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="54b50-171">Kirjoita arvo Teksti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="54b50-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="54b50-172">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="54b50-172">Click Add.</span></span>
39. <span data-ttu-id="54b50-173">Valitse Numerosarjan arvo.</span><span class="sxs-lookup"><span data-stu-id="54b50-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="54b50-174">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="54b50-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="54b50-175">Anna tai valitse Numerojärjestys-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="54b50-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="54b50-176">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="54b50-176">Close the page.</span></span>
43. <span data-ttu-id="54b50-177">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="54b50-177">Close the page.</span></span>
44. <span data-ttu-id="54b50-178">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="54b50-178">Close the page.</span></span>


