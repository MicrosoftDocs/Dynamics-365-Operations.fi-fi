---
title: Raaka-aineiden luominen (helmikuu 2016)
description: Tämä tehtävä keskittyy valmiiden ja puolivalmiiden tuotteiden osien luomiseen.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e20abf8a1b211bff2bc73d1a36a1e5c917ffaab
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844582"
---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="36edf-103">Raaka-aineiden luominen (helmikuu 2016)</span><span class="sxs-lookup"><span data-stu-id="36edf-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="36edf-104">Tämä tehtävä keskittyy valmiiden ja puolivalmiiden tuotteiden osien luomiseen.</span><span class="sxs-lookup"><span data-stu-id="36edf-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="36edf-105">Se on tuoterakenteen laskentasarjan kolmas tehtävä.</span><span class="sxs-lookup"><span data-stu-id="36edf-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="36edf-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="36edf-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="36edf-107">Ensimmäisen materiaalin luonti</span><span class="sxs-lookup"><span data-stu-id="36edf-107">Create the first material</span></span>
1. <span data-ttu-id="36edf-108">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="36edf-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="36edf-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="36edf-109">Click New.</span></span>
3. <span data-ttu-id="36edf-110">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="36edf-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="36edf-111">Anna tässä esimerkissä ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="36edf-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="36edf-112">Syötä tai valitse arvo Nimikemalliryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-113">Valitse STD.</span><span class="sxs-lookup"><span data-stu-id="36edf-113">Select STD.</span></span> <span data-ttu-id="36edf-114">STD standardikustannusta ja on kustannuslaskennassa yleisimmin käytetty malli.</span><span class="sxs-lookup"><span data-stu-id="36edf-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="36edf-115">Anna tai valitse arvo Nimikeryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-116">Valitse esimerkiksi Audio.</span><span class="sxs-lookup"><span data-stu-id="36edf-116">For example, select Audio.</span></span> <span data-ttu-id="36edf-117">Se ei vaikuta kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="36edf-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="36edf-118">Syötä tai valitse arvo Varastodimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-119">Valitse SiteWH.</span><span class="sxs-lookup"><span data-stu-id="36edf-119">Select SiteWH.</span></span> <span data-ttu-id="36edf-120">Esimerkissä käytetään vain toimipaikkaa ja varastoa.</span><span class="sxs-lookup"><span data-stu-id="36edf-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="36edf-121">Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-122">Tässä esimerkissä ei käytetä seurantadimensioita.</span><span class="sxs-lookup"><span data-stu-id="36edf-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="36edf-123">Valitse Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="36edf-123">Select None.</span></span>  
8. <span data-ttu-id="36edf-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="36edf-124">Click OK.</span></span>
9. <span data-ttu-id="36edf-125">Valitse toimintoruudussa Varastonhallinta.</span><span class="sxs-lookup"><span data-stu-id="36edf-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="36edf-126">Valitse Tilauksen oletusasetukset.</span><span class="sxs-lookup"><span data-stu-id="36edf-126">Click Default order settings.</span></span>
11. <span data-ttu-id="36edf-127">Anna tai valitse arvo Ostotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-128">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="36edf-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="36edf-129">Anna tai valitse arvo Varastotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-130">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="36edf-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="36edf-131">Anna tai valitse arvo Myyntitoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-132">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="36edf-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="36edf-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="36edf-133">Close the page.</span></span>
15. <span data-ttu-id="36edf-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="36edf-134">Close the page.</span></span>
16. <span data-ttu-id="36edf-135">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="36edf-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="36edf-136">Valitse ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="36edf-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="36edf-137">Laajenna Kustannusten hallinta -osa.</span><span class="sxs-lookup"><span data-stu-id="36edf-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="36edf-138">Kirjoita Kustannusryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="36edf-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="36edf-139">Kirjoita tässä esimerkissä M2.</span><span class="sxs-lookup"><span data-stu-id="36edf-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="36edf-140">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="36edf-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="36edf-141">Valitse Nimikkeen hinta.</span><span class="sxs-lookup"><span data-stu-id="36edf-141">Click Item price.</span></span>
21. <span data-ttu-id="36edf-142">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="36edf-142">Click New.</span></span>
22. <span data-ttu-id="36edf-143">Anna tai valitse arvo Versio-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-144">Valitse tässä esimerkissä 10, mikä on standardikustannuksen kustannuslaskentatyyppi.</span><span class="sxs-lookup"><span data-stu-id="36edf-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="36edf-145">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="36edf-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-146">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="36edf-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="36edf-147">Syötä Hinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="36edf-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="36edf-148">Kirjoita tässä esimerkissä 10.</span><span class="sxs-lookup"><span data-stu-id="36edf-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="36edf-149">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="36edf-149">Click Save.</span></span>
26. <span data-ttu-id="36edf-150">Valitse Aktivoi odottavat hinnat.</span><span class="sxs-lookup"><span data-stu-id="36edf-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="36edf-151">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="36edf-151">Close the page.</span></span>
28. <span data-ttu-id="36edf-152">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="36edf-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="36edf-153">Toisen materiaalin luonti</span><span class="sxs-lookup"><span data-stu-id="36edf-153">Create the second material</span></span>
1. <span data-ttu-id="36edf-154">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="36edf-154">Click New.</span></span>
2. <span data-ttu-id="36edf-155">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="36edf-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="36edf-156">Kirjoita tässä esimerkissä ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="36edf-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="36edf-157">Syötä tai valitse arvo Nimikemalliryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-158">Valitse STD.</span><span class="sxs-lookup"><span data-stu-id="36edf-158">Select STD.</span></span> <span data-ttu-id="36edf-159">STD standardikustannusta ja on kustannuslaskennassa yleisimmin käytetty malli.</span><span class="sxs-lookup"><span data-stu-id="36edf-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="36edf-160">Anna tai valitse arvo Nimikeryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-161">Valitse esimerkiksi Audio.</span><span class="sxs-lookup"><span data-stu-id="36edf-161">For example, select Audio.</span></span> <span data-ttu-id="36edf-162">Se ei vaikuta kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="36edf-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="36edf-163">Syötä tai valitse arvo Varastodimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-164">Valitse SiteWH.</span><span class="sxs-lookup"><span data-stu-id="36edf-164">Select SiteWH.</span></span> <span data-ttu-id="36edf-165">Tässä esimerkissä käytetään vain toimipaikkaa ja varastoa.</span><span class="sxs-lookup"><span data-stu-id="36edf-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="36edf-166">Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-167">Tässä esimerkissä ei käytetä seurantadimensioita.</span><span class="sxs-lookup"><span data-stu-id="36edf-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="36edf-168">Valitse Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="36edf-168">Select None.</span></span>  
7. <span data-ttu-id="36edf-169">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="36edf-169">Click OK.</span></span>
8. <span data-ttu-id="36edf-170">Valitse toimintoruudussa Varastonhallinta.</span><span class="sxs-lookup"><span data-stu-id="36edf-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="36edf-171">Valitse Tilauksen oletusasetukset.</span><span class="sxs-lookup"><span data-stu-id="36edf-171">Click Default order settings.</span></span>
10. <span data-ttu-id="36edf-172">Anna tai valitse arvo Ostotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-173">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="36edf-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="36edf-174">Anna tai valitse arvo Varastotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-175">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="36edf-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="36edf-176">Anna tai valitse arvo Myyntitoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-177">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="36edf-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="36edf-178">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="36edf-178">Close the page.</span></span>
14. <span data-ttu-id="36edf-179">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="36edf-179">Close the page.</span></span>
15. <span data-ttu-id="36edf-180">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="36edf-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="36edf-181">Valitse ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="36edf-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="36edf-182">Laajenna Kustannusten hallinta -osa.</span><span class="sxs-lookup"><span data-stu-id="36edf-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="36edf-183">Kirjoita Kustannusryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="36edf-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="36edf-184">Kirjoita tässä esimerkissä M2.</span><span class="sxs-lookup"><span data-stu-id="36edf-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="36edf-185">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="36edf-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="36edf-186">Valitse Nimikkeen hinta.</span><span class="sxs-lookup"><span data-stu-id="36edf-186">Click Item price.</span></span>
20. <span data-ttu-id="36edf-187">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="36edf-187">Click New.</span></span>
21. <span data-ttu-id="36edf-188">Anna tai valitse arvo Versio-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-189">Valitse tässä esimerkissä 10.</span><span class="sxs-lookup"><span data-stu-id="36edf-189">For this example, select 10.</span></span> <span data-ttu-id="36edf-190">Tämä on standardikustannuksen kustannuslaskentatyyppi.</span><span class="sxs-lookup"><span data-stu-id="36edf-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="36edf-191">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="36edf-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-192">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="36edf-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="36edf-193">Syötä Hinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="36edf-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="36edf-194">Kirjoita esimerkkiä varten 10.</span><span class="sxs-lookup"><span data-stu-id="36edf-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="36edf-195">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="36edf-195">Click Save.</span></span>
25. <span data-ttu-id="36edf-196">Valitse Aktivoi odottavat hinnat.</span><span class="sxs-lookup"><span data-stu-id="36edf-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="36edf-197">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="36edf-197">Close the page.</span></span>
27. <span data-ttu-id="36edf-198">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="36edf-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="36edf-199">Kolmannen materiaalin luonti</span><span class="sxs-lookup"><span data-stu-id="36edf-199">Create the third material</span></span>
1. <span data-ttu-id="36edf-200">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="36edf-200">Click New.</span></span>
2. <span data-ttu-id="36edf-201">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="36edf-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="36edf-202">Kirjoita esimerkkiä varten ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="36edf-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="36edf-203">Syötä tai valitse arvo Nimikemalliryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-204">Valitse STD.</span><span class="sxs-lookup"><span data-stu-id="36edf-204">Select STD.</span></span> <span data-ttu-id="36edf-205">STD standardikustannusta ja on kustannuslaskennassa yleisimmin käytetty malli.</span><span class="sxs-lookup"><span data-stu-id="36edf-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="36edf-206">Anna tai valitse arvo Nimikeryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-207">Valitse esimerkiksi Audio.</span><span class="sxs-lookup"><span data-stu-id="36edf-207">For example, select Audio.</span></span> <span data-ttu-id="36edf-208">Se ei vaikuta kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="36edf-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="36edf-209">Syötä tai valitse arvo Varastodimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-210">Valitse SiteWH.</span><span class="sxs-lookup"><span data-stu-id="36edf-210">Select SiteWH.</span></span> <span data-ttu-id="36edf-211">Esimerkissä käytetään vain toimipaikkaa ja varastoa.</span><span class="sxs-lookup"><span data-stu-id="36edf-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="36edf-212">Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-213">Tässä esimerkissä ei käytetä seurantadimensioita.</span><span class="sxs-lookup"><span data-stu-id="36edf-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="36edf-214">Valitse Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="36edf-214">Select None.</span></span>  
7. <span data-ttu-id="36edf-215">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="36edf-215">Click OK.</span></span>
8. <span data-ttu-id="36edf-216">Valitse toimintoruudussa Varastonhallinta.</span><span class="sxs-lookup"><span data-stu-id="36edf-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="36edf-217">Valitse Tilauksen oletusasetukset.</span><span class="sxs-lookup"><span data-stu-id="36edf-217">Click Default order settings.</span></span>
10. <span data-ttu-id="36edf-218">Anna tai valitse arvo Ostotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-219">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="36edf-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="36edf-220">Anna tai valitse arvo Varastotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-221">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="36edf-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="36edf-222">Anna tai valitse arvo Myyntitoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-223">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="36edf-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="36edf-224">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="36edf-224">Close the page.</span></span>
14. <span data-ttu-id="36edf-225">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="36edf-225">Close the page.</span></span>
15. <span data-ttu-id="36edf-226">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="36edf-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="36edf-227">Valitse ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="36edf-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="36edf-228">Laajenna Kustannusten hallinta -osa.</span><span class="sxs-lookup"><span data-stu-id="36edf-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="36edf-229">Kirjoita Kustannusryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="36edf-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="36edf-230">Kirjoita tässä esimerkissä M1.</span><span class="sxs-lookup"><span data-stu-id="36edf-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="36edf-231">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="36edf-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="36edf-232">Valitse Nimikkeen hinta.</span><span class="sxs-lookup"><span data-stu-id="36edf-232">Click Item price.</span></span>
20. <span data-ttu-id="36edf-233">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="36edf-233">Click New.</span></span>
21. <span data-ttu-id="36edf-234">Anna tai valitse arvo Versio-kentässä.</span><span class="sxs-lookup"><span data-stu-id="36edf-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-235">Valitse tässä esimerkissä 10.</span><span class="sxs-lookup"><span data-stu-id="36edf-235">For this example, select 10.</span></span> <span data-ttu-id="36edf-236">Tämä on standardikustannuksen kustannuslaskentatyyppi.</span><span class="sxs-lookup"><span data-stu-id="36edf-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="36edf-237">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="36edf-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="36edf-238">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="36edf-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="36edf-239">Syötä Hinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="36edf-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="36edf-240">Kirjoita tässä esimerkissä 10.</span><span class="sxs-lookup"><span data-stu-id="36edf-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="36edf-241">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="36edf-241">Click Save.</span></span>
25. <span data-ttu-id="36edf-242">Valitse Aktivoi odottavat hinnat.</span><span class="sxs-lookup"><span data-stu-id="36edf-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="36edf-243">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="36edf-243">Close the page.</span></span>
27. <span data-ttu-id="36edf-244">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="36edf-244">Close the page.</span></span>

