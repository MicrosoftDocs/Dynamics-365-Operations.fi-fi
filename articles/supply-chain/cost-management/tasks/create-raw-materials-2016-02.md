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
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3d77dcc20fe7402af83dd724e7fef848977e5bf8
ms.openlocfilehash: f6af7b93d8d1d9a6f7474f24177b16e5295e90d6
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="aeb97-103">Luo raaka-aineet (vain helmikuu 2016)</span><span class="sxs-lookup"><span data-stu-id="aeb97-103">Create raw materials (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aeb97-104">Tämä tehtävä keskittyy valmiiden ja puolivalmiiden tuotteiden osien luomiseen.</span><span class="sxs-lookup"><span data-stu-id="aeb97-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="aeb97-105">Se on tuoterakenteen laskentasarjan kolmas tehtävä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="aeb97-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="aeb97-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="aeb97-107">Ensimmäisen materiaalin luonti</span><span class="sxs-lookup"><span data-stu-id="aeb97-107">Create the first material</span></span>
1. <span data-ttu-id="aeb97-108">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="aeb97-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="aeb97-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="aeb97-109">Click New.</span></span>
3. <span data-ttu-id="aeb97-110">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aeb97-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="aeb97-111">Anna tässä esimerkissä ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="aeb97-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="aeb97-112">Syötä tai valitse arvo Nimikemalliryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-113">Valitse STD.</span><span class="sxs-lookup"><span data-stu-id="aeb97-113">Select STD.</span></span> <span data-ttu-id="aeb97-114">STD standardikustannusta ja on kustannuslaskennassa yleisimmin käytetty malli.</span><span class="sxs-lookup"><span data-stu-id="aeb97-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="aeb97-115">Anna tai valitse arvo Nimikeryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-116">Valitse esimerkiksi Audio.</span><span class="sxs-lookup"><span data-stu-id="aeb97-116">For example, select Audio.</span></span> <span data-ttu-id="aeb97-117">Se ei vaikuta kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="aeb97-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="aeb97-118">Syötä tai valitse arvo Varastodimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-119">Valitse SiteWH.</span><span class="sxs-lookup"><span data-stu-id="aeb97-119">Select SiteWH.</span></span> <span data-ttu-id="aeb97-120">Esimerkissä käytetään vain toimipaikkaa ja varastoa.</span><span class="sxs-lookup"><span data-stu-id="aeb97-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="aeb97-121">Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-122">Tässä esimerkissä ei käytetä seurantadimensioita.</span><span class="sxs-lookup"><span data-stu-id="aeb97-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="aeb97-123">Valitse Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="aeb97-123">Select None.</span></span>  
8. <span data-ttu-id="aeb97-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="aeb97-124">Click OK.</span></span>
9. <span data-ttu-id="aeb97-125">Valitse toimintoruudussa Varastonhallinta.</span><span class="sxs-lookup"><span data-stu-id="aeb97-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="aeb97-126">Valitse Tilauksen oletusasetukset.</span><span class="sxs-lookup"><span data-stu-id="aeb97-126">Click Default order settings.</span></span>
11. <span data-ttu-id="aeb97-127">Anna tai valitse arvo Ostotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-128">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="aeb97-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="aeb97-129">Anna tai valitse arvo Varastotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-130">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="aeb97-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="aeb97-131">Anna tai valitse arvo Myyntitoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-132">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="aeb97-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="aeb97-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aeb97-133">Close the page.</span></span>
15. <span data-ttu-id="aeb97-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aeb97-134">Close the page.</span></span>
16. <span data-ttu-id="aeb97-135">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="aeb97-136">Valitse ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="aeb97-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="aeb97-137">Laajenna Kustannusten hallinta -osa.</span><span class="sxs-lookup"><span data-stu-id="aeb97-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="aeb97-138">Kirjoita Kustannusryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="aeb97-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="aeb97-139">Kirjoita tässä esimerkissä M2.</span><span class="sxs-lookup"><span data-stu-id="aeb97-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="aeb97-140">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="aeb97-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="aeb97-141">Valitse Nimikkeen hinta.</span><span class="sxs-lookup"><span data-stu-id="aeb97-141">Click Item price.</span></span>
21. <span data-ttu-id="aeb97-142">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="aeb97-142">Click New.</span></span>
22. <span data-ttu-id="aeb97-143">Anna tai valitse arvo Versio-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-144">Valitse tässä esimerkissä 10, mikä on standardikustannuksen kustannuslaskentatyyppi.</span><span class="sxs-lookup"><span data-stu-id="aeb97-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="aeb97-145">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aeb97-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-146">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="aeb97-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="aeb97-147">Syötä Hinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="aeb97-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="aeb97-148">Kirjoita tässä esimerkissä 10.</span><span class="sxs-lookup"><span data-stu-id="aeb97-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="aeb97-149">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="aeb97-149">Click Save.</span></span>
26. <span data-ttu-id="aeb97-150">Valitse Aktivoi odottavat hinnat.</span><span class="sxs-lookup"><span data-stu-id="aeb97-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="aeb97-151">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aeb97-151">Close the page.</span></span>
28. <span data-ttu-id="aeb97-152">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aeb97-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="aeb97-153">Toisen materiaalin luonti</span><span class="sxs-lookup"><span data-stu-id="aeb97-153">Create the second material</span></span>
1. <span data-ttu-id="aeb97-154">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="aeb97-154">Click New.</span></span>
2. <span data-ttu-id="aeb97-155">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aeb97-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="aeb97-156">Kirjoita tässä esimerkissä ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="aeb97-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="aeb97-157">Syötä tai valitse arvo Nimikemalliryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-158">Valitse STD.</span><span class="sxs-lookup"><span data-stu-id="aeb97-158">Select STD.</span></span> <span data-ttu-id="aeb97-159">STD standardikustannusta ja on kustannuslaskennassa yleisimmin käytetty malli.</span><span class="sxs-lookup"><span data-stu-id="aeb97-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="aeb97-160">Anna tai valitse arvo Nimikeryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-161">Valitse esimerkiksi Audio.</span><span class="sxs-lookup"><span data-stu-id="aeb97-161">For example, select Audio.</span></span> <span data-ttu-id="aeb97-162">Se ei vaikuta kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="aeb97-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="aeb97-163">Syötä tai valitse arvo Varastodimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-164">Valitse SiteWH.</span><span class="sxs-lookup"><span data-stu-id="aeb97-164">Select SiteWH.</span></span> <span data-ttu-id="aeb97-165">Tässä esimerkissä käytetään vain toimipaikkaa ja varastoa.</span><span class="sxs-lookup"><span data-stu-id="aeb97-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="aeb97-166">Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-167">Tässä esimerkissä ei käytetä seurantadimensioita.</span><span class="sxs-lookup"><span data-stu-id="aeb97-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="aeb97-168">Valitse Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="aeb97-168">Select None.</span></span>  
7. <span data-ttu-id="aeb97-169">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="aeb97-169">Click OK.</span></span>
8. <span data-ttu-id="aeb97-170">Valitse toimintoruudussa Varastonhallinta.</span><span class="sxs-lookup"><span data-stu-id="aeb97-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="aeb97-171">Valitse Tilauksen oletusasetukset.</span><span class="sxs-lookup"><span data-stu-id="aeb97-171">Click Default order settings.</span></span>
10. <span data-ttu-id="aeb97-172">Anna tai valitse arvo Ostotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-173">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="aeb97-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="aeb97-174">Anna tai valitse arvo Varastotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-175">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="aeb97-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="aeb97-176">Anna tai valitse arvo Myyntitoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-177">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="aeb97-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="aeb97-178">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aeb97-178">Close the page.</span></span>
14. <span data-ttu-id="aeb97-179">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aeb97-179">Close the page.</span></span>
15. <span data-ttu-id="aeb97-180">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="aeb97-181">Valitse ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="aeb97-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="aeb97-182">Laajenna Kustannusten hallinta -osa.</span><span class="sxs-lookup"><span data-stu-id="aeb97-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="aeb97-183">Kirjoita Kustannusryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="aeb97-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="aeb97-184">Kirjoita tässä esimerkissä M2.</span><span class="sxs-lookup"><span data-stu-id="aeb97-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="aeb97-185">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="aeb97-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="aeb97-186">Valitse Nimikkeen hinta.</span><span class="sxs-lookup"><span data-stu-id="aeb97-186">Click Item price.</span></span>
20. <span data-ttu-id="aeb97-187">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="aeb97-187">Click New.</span></span>
21. <span data-ttu-id="aeb97-188">Anna tai valitse arvo Versio-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-189">Valitse tässä esimerkissä 10.</span><span class="sxs-lookup"><span data-stu-id="aeb97-189">For this example, select 10.</span></span> <span data-ttu-id="aeb97-190">Tämä on standardikustannuksen kustannuslaskentatyyppi.</span><span class="sxs-lookup"><span data-stu-id="aeb97-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="aeb97-191">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aeb97-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-192">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="aeb97-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="aeb97-193">Syötä Hinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="aeb97-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="aeb97-194">Kirjoita esimerkkiä varten 10.</span><span class="sxs-lookup"><span data-stu-id="aeb97-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="aeb97-195">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="aeb97-195">Click Save.</span></span>
25. <span data-ttu-id="aeb97-196">Valitse Aktivoi odottavat hinnat.</span><span class="sxs-lookup"><span data-stu-id="aeb97-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="aeb97-197">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aeb97-197">Close the page.</span></span>
27. <span data-ttu-id="aeb97-198">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aeb97-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="aeb97-199">Kolmannen materiaalin luonti</span><span class="sxs-lookup"><span data-stu-id="aeb97-199">Create the third material</span></span>
1. <span data-ttu-id="aeb97-200">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="aeb97-200">Click New.</span></span>
2. <span data-ttu-id="aeb97-201">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aeb97-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="aeb97-202">Kirjoita esimerkkiä varten ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="aeb97-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="aeb97-203">Syötä tai valitse arvo Nimikemalliryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-204">Valitse STD.</span><span class="sxs-lookup"><span data-stu-id="aeb97-204">Select STD.</span></span> <span data-ttu-id="aeb97-205">STD standardikustannusta ja on kustannuslaskennassa yleisimmin käytetty malli.</span><span class="sxs-lookup"><span data-stu-id="aeb97-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="aeb97-206">Anna tai valitse arvo Nimikeryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-207">Valitse esimerkiksi Audio.</span><span class="sxs-lookup"><span data-stu-id="aeb97-207">For example, select Audio.</span></span> <span data-ttu-id="aeb97-208">Se ei vaikuta kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="aeb97-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="aeb97-209">Syötä tai valitse arvo Varastodimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-210">Valitse SiteWH.</span><span class="sxs-lookup"><span data-stu-id="aeb97-210">Select SiteWH.</span></span> <span data-ttu-id="aeb97-211">Esimerkissä käytetään vain toimipaikkaa ja varastoa.</span><span class="sxs-lookup"><span data-stu-id="aeb97-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="aeb97-212">Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-213">Tässä esimerkissä ei käytetä seurantadimensioita.</span><span class="sxs-lookup"><span data-stu-id="aeb97-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="aeb97-214">Valitse Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="aeb97-214">Select None.</span></span>  
7. <span data-ttu-id="aeb97-215">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="aeb97-215">Click OK.</span></span>
8. <span data-ttu-id="aeb97-216">Valitse toimintoruudussa Varastonhallinta.</span><span class="sxs-lookup"><span data-stu-id="aeb97-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="aeb97-217">Valitse Tilauksen oletusasetukset.</span><span class="sxs-lookup"><span data-stu-id="aeb97-217">Click Default order settings.</span></span>
10. <span data-ttu-id="aeb97-218">Anna tai valitse arvo Ostotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-219">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="aeb97-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="aeb97-220">Anna tai valitse arvo Varastotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-221">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="aeb97-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="aeb97-222">Anna tai valitse arvo Myyntitoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-223">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="aeb97-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="aeb97-224">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aeb97-224">Close the page.</span></span>
14. <span data-ttu-id="aeb97-225">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aeb97-225">Close the page.</span></span>
15. <span data-ttu-id="aeb97-226">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="aeb97-227">Valitse ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="aeb97-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="aeb97-228">Laajenna Kustannusten hallinta -osa.</span><span class="sxs-lookup"><span data-stu-id="aeb97-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="aeb97-229">Kirjoita Kustannusryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="aeb97-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="aeb97-230">Kirjoita tässä esimerkissä M1.</span><span class="sxs-lookup"><span data-stu-id="aeb97-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="aeb97-231">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="aeb97-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="aeb97-232">Valitse Nimikkeen hinta.</span><span class="sxs-lookup"><span data-stu-id="aeb97-232">Click Item price.</span></span>
20. <span data-ttu-id="aeb97-233">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="aeb97-233">Click New.</span></span>
21. <span data-ttu-id="aeb97-234">Anna tai valitse arvo Versio-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aeb97-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-235">Valitse tässä esimerkissä 10.</span><span class="sxs-lookup"><span data-stu-id="aeb97-235">For this example, select 10.</span></span> <span data-ttu-id="aeb97-236">Tämä on standardikustannuksen kustannuslaskentatyyppi.</span><span class="sxs-lookup"><span data-stu-id="aeb97-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="aeb97-237">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aeb97-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb97-238">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="aeb97-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="aeb97-239">Syötä Hinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="aeb97-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="aeb97-240">Kirjoita tässä esimerkissä 10.</span><span class="sxs-lookup"><span data-stu-id="aeb97-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="aeb97-241">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="aeb97-241">Click Save.</span></span>
25. <span data-ttu-id="aeb97-242">Valitse Aktivoi odottavat hinnat.</span><span class="sxs-lookup"><span data-stu-id="aeb97-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="aeb97-243">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aeb97-243">Close the page.</span></span>
27. <span data-ttu-id="aeb97-244">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aeb97-244">Close the page.</span></span>


