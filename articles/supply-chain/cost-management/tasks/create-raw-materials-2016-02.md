--- 
title: Luo raaka-aineet (vain helmikuu 2016)
description: "Tämä tehtävä keskittyy valmiiden ja puolivalmiiden tuotteiden osien luomiseen."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 8ed33e2e80915a80eb4c6de014091f1884799098
ms.contentlocale: fi-fi
ms.lasthandoff: 01/17/2018

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="63887-103">Luo raaka-aineet (vain helmikuu 2016)</span><span class="sxs-lookup"><span data-stu-id="63887-103">Create raw materials (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="63887-104">Tämä tehtävä keskittyy valmiiden ja puolivalmiiden tuotteiden osien luomiseen.</span><span class="sxs-lookup"><span data-stu-id="63887-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="63887-105">Se on tuoterakenteen laskentasarjan kolmas tehtävä.</span><span class="sxs-lookup"><span data-stu-id="63887-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="63887-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="63887-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="63887-107">Ensimmäisen materiaalin luonti</span><span class="sxs-lookup"><span data-stu-id="63887-107">Create the first material</span></span>
1. <span data-ttu-id="63887-108">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="63887-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="63887-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="63887-109">Click New.</span></span>
3. <span data-ttu-id="63887-110">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="63887-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="63887-111">Anna tässä esimerkissä ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="63887-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="63887-112">Syötä tai valitse arvo Nimikemalliryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-113">Valitse STD.</span><span class="sxs-lookup"><span data-stu-id="63887-113">Select STD.</span></span> <span data-ttu-id="63887-114">STD standardikustannusta ja on kustannuslaskennassa yleisimmin käytetty malli.</span><span class="sxs-lookup"><span data-stu-id="63887-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="63887-115">Anna tai valitse arvo Nimikeryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-116">Valitse esimerkiksi Audio.</span><span class="sxs-lookup"><span data-stu-id="63887-116">For example, select Audio.</span></span> <span data-ttu-id="63887-117">Se ei vaikuta kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="63887-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="63887-118">Syötä tai valitse arvo Varastodimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-119">Valitse SiteWH.</span><span class="sxs-lookup"><span data-stu-id="63887-119">Select SiteWH.</span></span> <span data-ttu-id="63887-120">Esimerkissä käytetään vain toimipaikkaa ja varastoa.</span><span class="sxs-lookup"><span data-stu-id="63887-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="63887-121">Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-122">Tässä esimerkissä ei käytetä seurantadimensioita.</span><span class="sxs-lookup"><span data-stu-id="63887-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="63887-123">Valitse Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="63887-123">Select None.</span></span>  
8. <span data-ttu-id="63887-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="63887-124">Click OK.</span></span>
9. <span data-ttu-id="63887-125">Valitse toimintoruudussa Varastonhallinta.</span><span class="sxs-lookup"><span data-stu-id="63887-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="63887-126">Valitse Tilauksen oletusasetukset.</span><span class="sxs-lookup"><span data-stu-id="63887-126">Click Default order settings.</span></span>
11. <span data-ttu-id="63887-127">Anna tai valitse arvo Ostotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-128">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="63887-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="63887-129">Anna tai valitse arvo Varastotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-130">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="63887-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="63887-131">Anna tai valitse arvo Myyntitoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-132">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="63887-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="63887-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="63887-133">Close the page.</span></span>
15. <span data-ttu-id="63887-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="63887-134">Close the page.</span></span>
16. <span data-ttu-id="63887-135">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="63887-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="63887-136">Valitse ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="63887-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="63887-137">Laajenna Kustannusten hallinta -osa.</span><span class="sxs-lookup"><span data-stu-id="63887-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="63887-138">Kirjoita Kustannusryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="63887-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="63887-139">Kirjoita tässä esimerkissä M2.</span><span class="sxs-lookup"><span data-stu-id="63887-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="63887-140">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="63887-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="63887-141">Valitse Nimikkeen hinta.</span><span class="sxs-lookup"><span data-stu-id="63887-141">Click Item price.</span></span>
21. <span data-ttu-id="63887-142">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="63887-142">Click New.</span></span>
22. <span data-ttu-id="63887-143">Anna tai valitse arvo Versio-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-144">Valitse tässä esimerkissä 10, mikä on standardikustannuksen kustannuslaskentatyyppi.</span><span class="sxs-lookup"><span data-stu-id="63887-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="63887-145">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="63887-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-146">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="63887-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="63887-147">Syötä Hinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="63887-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="63887-148">Kirjoita tässä esimerkissä 10.</span><span class="sxs-lookup"><span data-stu-id="63887-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="63887-149">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="63887-149">Click Save.</span></span>
26. <span data-ttu-id="63887-150">Valitse Aktivoi odottavat hinnat.</span><span class="sxs-lookup"><span data-stu-id="63887-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="63887-151">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="63887-151">Close the page.</span></span>
28. <span data-ttu-id="63887-152">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="63887-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="63887-153">Toisen materiaalin luonti</span><span class="sxs-lookup"><span data-stu-id="63887-153">Create the second material</span></span>
1. <span data-ttu-id="63887-154">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="63887-154">Click New.</span></span>
2. <span data-ttu-id="63887-155">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="63887-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="63887-156">Kirjoita tässä esimerkissä ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="63887-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="63887-157">Syötä tai valitse arvo Nimikemalliryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-158">Valitse STD.</span><span class="sxs-lookup"><span data-stu-id="63887-158">Select STD.</span></span> <span data-ttu-id="63887-159">STD standardikustannusta ja on kustannuslaskennassa yleisimmin käytetty malli.</span><span class="sxs-lookup"><span data-stu-id="63887-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="63887-160">Anna tai valitse arvo Nimikeryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-161">Valitse esimerkiksi Audio.</span><span class="sxs-lookup"><span data-stu-id="63887-161">For example, select Audio.</span></span> <span data-ttu-id="63887-162">Se ei vaikuta kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="63887-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="63887-163">Syötä tai valitse arvo Varastodimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-164">Valitse SiteWH.</span><span class="sxs-lookup"><span data-stu-id="63887-164">Select SiteWH.</span></span> <span data-ttu-id="63887-165">Tässä esimerkissä käytetään vain toimipaikkaa ja varastoa.</span><span class="sxs-lookup"><span data-stu-id="63887-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="63887-166">Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-167">Tässä esimerkissä ei käytetä seurantadimensioita.</span><span class="sxs-lookup"><span data-stu-id="63887-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="63887-168">Valitse Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="63887-168">Select None.</span></span>  
7. <span data-ttu-id="63887-169">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="63887-169">Click OK.</span></span>
8. <span data-ttu-id="63887-170">Valitse toimintoruudussa Varastonhallinta.</span><span class="sxs-lookup"><span data-stu-id="63887-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="63887-171">Valitse Tilauksen oletusasetukset.</span><span class="sxs-lookup"><span data-stu-id="63887-171">Click Default order settings.</span></span>
10. <span data-ttu-id="63887-172">Anna tai valitse arvo Ostotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-173">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="63887-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="63887-174">Anna tai valitse arvo Varastotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-175">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="63887-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="63887-176">Anna tai valitse arvo Myyntitoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-177">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="63887-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="63887-178">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="63887-178">Close the page.</span></span>
14. <span data-ttu-id="63887-179">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="63887-179">Close the page.</span></span>
15. <span data-ttu-id="63887-180">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="63887-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="63887-181">Valitse ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="63887-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="63887-182">Laajenna Kustannusten hallinta -osa.</span><span class="sxs-lookup"><span data-stu-id="63887-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="63887-183">Kirjoita Kustannusryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="63887-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="63887-184">Kirjoita tässä esimerkissä M2.</span><span class="sxs-lookup"><span data-stu-id="63887-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="63887-185">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="63887-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="63887-186">Valitse Nimikkeen hinta.</span><span class="sxs-lookup"><span data-stu-id="63887-186">Click Item price.</span></span>
20. <span data-ttu-id="63887-187">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="63887-187">Click New.</span></span>
21. <span data-ttu-id="63887-188">Anna tai valitse arvo Versio-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-189">Valitse tässä esimerkissä 10.</span><span class="sxs-lookup"><span data-stu-id="63887-189">For this example, select 10.</span></span> <span data-ttu-id="63887-190">Tämä on standardikustannuksen kustannuslaskentatyyppi.</span><span class="sxs-lookup"><span data-stu-id="63887-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="63887-191">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="63887-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-192">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="63887-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="63887-193">Syötä Hinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="63887-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="63887-194">Kirjoita esimerkkiä varten 10.</span><span class="sxs-lookup"><span data-stu-id="63887-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="63887-195">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="63887-195">Click Save.</span></span>
25. <span data-ttu-id="63887-196">Valitse Aktivoi odottavat hinnat.</span><span class="sxs-lookup"><span data-stu-id="63887-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="63887-197">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="63887-197">Close the page.</span></span>
27. <span data-ttu-id="63887-198">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="63887-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="63887-199">Kolmannen materiaalin luonti</span><span class="sxs-lookup"><span data-stu-id="63887-199">Create the third material</span></span>
1. <span data-ttu-id="63887-200">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="63887-200">Click New.</span></span>
2. <span data-ttu-id="63887-201">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="63887-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="63887-202">Kirjoita esimerkkiä varten ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="63887-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="63887-203">Syötä tai valitse arvo Nimikemalliryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-204">Valitse STD.</span><span class="sxs-lookup"><span data-stu-id="63887-204">Select STD.</span></span> <span data-ttu-id="63887-205">STD standardikustannusta ja on kustannuslaskennassa yleisimmin käytetty malli.</span><span class="sxs-lookup"><span data-stu-id="63887-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="63887-206">Anna tai valitse arvo Nimikeryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-207">Valitse esimerkiksi Audio.</span><span class="sxs-lookup"><span data-stu-id="63887-207">For example, select Audio.</span></span> <span data-ttu-id="63887-208">Se ei vaikuta kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="63887-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="63887-209">Syötä tai valitse arvo Varastodimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-210">Valitse SiteWH.</span><span class="sxs-lookup"><span data-stu-id="63887-210">Select SiteWH.</span></span> <span data-ttu-id="63887-211">Esimerkissä käytetään vain toimipaikkaa ja varastoa.</span><span class="sxs-lookup"><span data-stu-id="63887-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="63887-212">Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-213">Tässä esimerkissä ei käytetä seurantadimensioita.</span><span class="sxs-lookup"><span data-stu-id="63887-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="63887-214">Valitse Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="63887-214">Select None.</span></span>  
7. <span data-ttu-id="63887-215">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="63887-215">Click OK.</span></span>
8. <span data-ttu-id="63887-216">Valitse toimintoruudussa Varastonhallinta.</span><span class="sxs-lookup"><span data-stu-id="63887-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="63887-217">Valitse Tilauksen oletusasetukset.</span><span class="sxs-lookup"><span data-stu-id="63887-217">Click Default order settings.</span></span>
10. <span data-ttu-id="63887-218">Anna tai valitse arvo Ostotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-219">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="63887-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="63887-220">Anna tai valitse arvo Varastotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-221">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="63887-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="63887-222">Anna tai valitse arvo Myyntitoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-223">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="63887-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="63887-224">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="63887-224">Close the page.</span></span>
14. <span data-ttu-id="63887-225">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="63887-225">Close the page.</span></span>
15. <span data-ttu-id="63887-226">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="63887-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="63887-227">Valitse ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="63887-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="63887-228">Laajenna Kustannusten hallinta -osa.</span><span class="sxs-lookup"><span data-stu-id="63887-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="63887-229">Kirjoita Kustannusryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="63887-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="63887-230">Kirjoita tässä esimerkissä M1.</span><span class="sxs-lookup"><span data-stu-id="63887-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="63887-231">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="63887-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="63887-232">Valitse Nimikkeen hinta.</span><span class="sxs-lookup"><span data-stu-id="63887-232">Click Item price.</span></span>
20. <span data-ttu-id="63887-233">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="63887-233">Click New.</span></span>
21. <span data-ttu-id="63887-234">Anna tai valitse arvo Versio-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63887-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-235">Valitse tässä esimerkissä 10.</span><span class="sxs-lookup"><span data-stu-id="63887-235">For this example, select 10.</span></span> <span data-ttu-id="63887-236">Tämä on standardikustannuksen kustannuslaskentatyyppi.</span><span class="sxs-lookup"><span data-stu-id="63887-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="63887-237">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="63887-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="63887-238">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="63887-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="63887-239">Syötä Hinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="63887-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="63887-240">Kirjoita tässä esimerkissä 10.</span><span class="sxs-lookup"><span data-stu-id="63887-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="63887-241">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="63887-241">Click Save.</span></span>
25. <span data-ttu-id="63887-242">Valitse Aktivoi odottavat hinnat.</span><span class="sxs-lookup"><span data-stu-id="63887-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="63887-243">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="63887-243">Close the page.</span></span>
27. <span data-ttu-id="63887-244">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="63887-244">Close the page.</span></span>


