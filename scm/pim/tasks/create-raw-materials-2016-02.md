--- 
title: Luo raaka-aineet (vain helmikuu 2016)
description: "Tämä tehtävä keskittyy valmiiden ja puolivalmiiden tuotteiden osien luomiseen."
author: BibiSp
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f1c10e0f8275d928c1455cd99105aece8780e7f0
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="ce34d-103">Luo raaka-aineet (vain helmikuu 2016)</span><span class="sxs-lookup"><span data-stu-id="ce34d-103">Create raw materials (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ce34d-104">Tämä tehtävä keskittyy valmiiden ja puolivalmiiden tuotteiden osien luomiseen.</span><span class="sxs-lookup"><span data-stu-id="ce34d-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="ce34d-105">Se on tuoterakenteen laskentasarjan kolmas tehtävä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="ce34d-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="ce34d-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="ce34d-107">Ensimmäisen materiaalin luonti</span><span class="sxs-lookup"><span data-stu-id="ce34d-107">Create the first material</span></span>
1. <span data-ttu-id="ce34d-108">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="ce34d-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="ce34d-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ce34d-109">Click New.</span></span>
3. <span data-ttu-id="ce34d-110">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ce34d-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="ce34d-111">Anna tässä esimerkissä ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="ce34d-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="ce34d-112">Syötä tai valitse arvo Nimikemalliryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-113">Valitse STD.</span><span class="sxs-lookup"><span data-stu-id="ce34d-113">Select STD.</span></span> <span data-ttu-id="ce34d-114">STD standardikustannusta ja on kustannuslaskennassa yleisimmin käytetty malli.</span><span class="sxs-lookup"><span data-stu-id="ce34d-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="ce34d-115">Anna tai valitse arvo Nimikeryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-116">Valitse esimerkiksi Audio.</span><span class="sxs-lookup"><span data-stu-id="ce34d-116">For example, select Audio.</span></span> <span data-ttu-id="ce34d-117">Se ei vaikuta kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="ce34d-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="ce34d-118">Syötä tai valitse arvo Varastodimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-119">Valitse SiteWH.</span><span class="sxs-lookup"><span data-stu-id="ce34d-119">Select SiteWH.</span></span> <span data-ttu-id="ce34d-120">Esimerkissä käytetään vain toimipaikkaa ja varastoa.</span><span class="sxs-lookup"><span data-stu-id="ce34d-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="ce34d-121">Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-122">Tässä esimerkissä ei käytetä seurantadimensioita.</span><span class="sxs-lookup"><span data-stu-id="ce34d-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="ce34d-123">Valitse Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="ce34d-123">Select None.</span></span>  
8. <span data-ttu-id="ce34d-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ce34d-124">Click OK.</span></span>
9. <span data-ttu-id="ce34d-125">Valitse toimintoruudussa Varastonhallinta.</span><span class="sxs-lookup"><span data-stu-id="ce34d-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="ce34d-126">Valitse Tilauksen oletusasetukset.</span><span class="sxs-lookup"><span data-stu-id="ce34d-126">Click Default order settings.</span></span>
11. <span data-ttu-id="ce34d-127">Anna tai valitse arvo Ostotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-128">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="ce34d-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="ce34d-129">Anna tai valitse arvo Varastotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-130">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="ce34d-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="ce34d-131">Anna tai valitse arvo Myyntitoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-132">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="ce34d-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="ce34d-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ce34d-133">Close the page.</span></span>
15. <span data-ttu-id="ce34d-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ce34d-134">Close the page.</span></span>
16. <span data-ttu-id="ce34d-135">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ce34d-136">Valitse ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="ce34d-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="ce34d-137">Laajenna Kustannusten hallinta -osa.</span><span class="sxs-lookup"><span data-stu-id="ce34d-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="ce34d-138">Kirjoita Kustannusryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ce34d-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="ce34d-139">Kirjoita tässä esimerkissä M2.</span><span class="sxs-lookup"><span data-stu-id="ce34d-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="ce34d-140">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="ce34d-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="ce34d-141">Valitse Nimikkeen hinta.</span><span class="sxs-lookup"><span data-stu-id="ce34d-141">Click Item price.</span></span>
21. <span data-ttu-id="ce34d-142">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ce34d-142">Click New.</span></span>
22. <span data-ttu-id="ce34d-143">Anna tai valitse arvo Versio-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-144">Valitse tässä esimerkissä 10, mikä on standardikustannuksen kustannuslaskentatyyppi.</span><span class="sxs-lookup"><span data-stu-id="ce34d-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="ce34d-145">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ce34d-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-146">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="ce34d-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="ce34d-147">Syötä Hinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="ce34d-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="ce34d-148">Kirjoita tässä esimerkissä 10.</span><span class="sxs-lookup"><span data-stu-id="ce34d-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="ce34d-149">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="ce34d-149">Click Save.</span></span>
26. <span data-ttu-id="ce34d-150">Valitse Aktivoi odottavat hinnat.</span><span class="sxs-lookup"><span data-stu-id="ce34d-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="ce34d-151">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ce34d-151">Close the page.</span></span>
28. <span data-ttu-id="ce34d-152">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ce34d-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="ce34d-153">Toisen materiaalin luonti</span><span class="sxs-lookup"><span data-stu-id="ce34d-153">Create the second material</span></span>
1. <span data-ttu-id="ce34d-154">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ce34d-154">Click New.</span></span>
2. <span data-ttu-id="ce34d-155">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ce34d-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="ce34d-156">Kirjoita tässä esimerkissä ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="ce34d-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="ce34d-157">Syötä tai valitse arvo Nimikemalliryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-158">Valitse STD.</span><span class="sxs-lookup"><span data-stu-id="ce34d-158">Select STD.</span></span> <span data-ttu-id="ce34d-159">STD standardikustannusta ja on kustannuslaskennassa yleisimmin käytetty malli.</span><span class="sxs-lookup"><span data-stu-id="ce34d-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="ce34d-160">Anna tai valitse arvo Nimikeryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-161">Valitse esimerkiksi Audio.</span><span class="sxs-lookup"><span data-stu-id="ce34d-161">For example, select Audio.</span></span> <span data-ttu-id="ce34d-162">Se ei vaikuta kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="ce34d-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="ce34d-163">Syötä tai valitse arvo Varastodimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-164">Valitse SiteWH.</span><span class="sxs-lookup"><span data-stu-id="ce34d-164">Select SiteWH.</span></span> <span data-ttu-id="ce34d-165">Tässä esimerkissä käytetään vain toimipaikkaa ja varastoa.</span><span class="sxs-lookup"><span data-stu-id="ce34d-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="ce34d-166">Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-167">Tässä esimerkissä ei käytetä seurantadimensioita.</span><span class="sxs-lookup"><span data-stu-id="ce34d-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="ce34d-168">Valitse Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="ce34d-168">Select None.</span></span>  
7. <span data-ttu-id="ce34d-169">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ce34d-169">Click OK.</span></span>
8. <span data-ttu-id="ce34d-170">Valitse toimintoruudussa Varastonhallinta.</span><span class="sxs-lookup"><span data-stu-id="ce34d-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="ce34d-171">Valitse Tilauksen oletusasetukset.</span><span class="sxs-lookup"><span data-stu-id="ce34d-171">Click Default order settings.</span></span>
10. <span data-ttu-id="ce34d-172">Anna tai valitse arvo Ostotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-173">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="ce34d-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="ce34d-174">Anna tai valitse arvo Varastotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-175">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="ce34d-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="ce34d-176">Anna tai valitse arvo Myyntitoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-177">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="ce34d-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="ce34d-178">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ce34d-178">Close the page.</span></span>
14. <span data-ttu-id="ce34d-179">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ce34d-179">Close the page.</span></span>
15. <span data-ttu-id="ce34d-180">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ce34d-181">Valitse ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="ce34d-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="ce34d-182">Laajenna Kustannusten hallinta -osa.</span><span class="sxs-lookup"><span data-stu-id="ce34d-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="ce34d-183">Kirjoita Kustannusryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ce34d-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="ce34d-184">Kirjoita tässä esimerkissä M2.</span><span class="sxs-lookup"><span data-stu-id="ce34d-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="ce34d-185">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="ce34d-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="ce34d-186">Valitse Nimikkeen hinta.</span><span class="sxs-lookup"><span data-stu-id="ce34d-186">Click Item price.</span></span>
20. <span data-ttu-id="ce34d-187">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ce34d-187">Click New.</span></span>
21. <span data-ttu-id="ce34d-188">Anna tai valitse arvo Versio-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-189">Valitse tässä esimerkissä 10.</span><span class="sxs-lookup"><span data-stu-id="ce34d-189">For this example, select 10.</span></span> <span data-ttu-id="ce34d-190">Tämä on standardikustannuksen kustannuslaskentatyyppi.</span><span class="sxs-lookup"><span data-stu-id="ce34d-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="ce34d-191">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ce34d-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-192">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="ce34d-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="ce34d-193">Syötä Hinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="ce34d-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="ce34d-194">Kirjoita esimerkkiä varten 10.</span><span class="sxs-lookup"><span data-stu-id="ce34d-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="ce34d-195">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="ce34d-195">Click Save.</span></span>
25. <span data-ttu-id="ce34d-196">Valitse Aktivoi odottavat hinnat.</span><span class="sxs-lookup"><span data-stu-id="ce34d-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="ce34d-197">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ce34d-197">Close the page.</span></span>
27. <span data-ttu-id="ce34d-198">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ce34d-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="ce34d-199">Kolmannen materiaalin luonti</span><span class="sxs-lookup"><span data-stu-id="ce34d-199">Create the third material</span></span>
1. <span data-ttu-id="ce34d-200">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ce34d-200">Click New.</span></span>
2. <span data-ttu-id="ce34d-201">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ce34d-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="ce34d-202">Kirjoita esimerkkiä varten ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="ce34d-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="ce34d-203">Syötä tai valitse arvo Nimikemalliryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-204">Valitse STD.</span><span class="sxs-lookup"><span data-stu-id="ce34d-204">Select STD.</span></span> <span data-ttu-id="ce34d-205">STD standardikustannusta ja on kustannuslaskennassa yleisimmin käytetty malli.</span><span class="sxs-lookup"><span data-stu-id="ce34d-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="ce34d-206">Anna tai valitse arvo Nimikeryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-207">Valitse esimerkiksi Audio.</span><span class="sxs-lookup"><span data-stu-id="ce34d-207">For example, select Audio.</span></span> <span data-ttu-id="ce34d-208">Se ei vaikuta kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="ce34d-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="ce34d-209">Syötä tai valitse arvo Varastodimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-210">Valitse SiteWH.</span><span class="sxs-lookup"><span data-stu-id="ce34d-210">Select SiteWH.</span></span> <span data-ttu-id="ce34d-211">Esimerkissä käytetään vain toimipaikkaa ja varastoa.</span><span class="sxs-lookup"><span data-stu-id="ce34d-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="ce34d-212">Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-213">Tässä esimerkissä ei käytetä seurantadimensioita.</span><span class="sxs-lookup"><span data-stu-id="ce34d-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="ce34d-214">Valitse Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="ce34d-214">Select None.</span></span>  
7. <span data-ttu-id="ce34d-215">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ce34d-215">Click OK.</span></span>
8. <span data-ttu-id="ce34d-216">Valitse toimintoruudussa Varastonhallinta.</span><span class="sxs-lookup"><span data-stu-id="ce34d-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="ce34d-217">Valitse Tilauksen oletusasetukset.</span><span class="sxs-lookup"><span data-stu-id="ce34d-217">Click Default order settings.</span></span>
10. <span data-ttu-id="ce34d-218">Anna tai valitse arvo Ostotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-219">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="ce34d-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="ce34d-220">Anna tai valitse arvo Varastotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-221">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="ce34d-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="ce34d-222">Anna tai valitse arvo Myyntitoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-223">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="ce34d-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="ce34d-224">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ce34d-224">Close the page.</span></span>
14. <span data-ttu-id="ce34d-225">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ce34d-225">Close the page.</span></span>
15. <span data-ttu-id="ce34d-226">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ce34d-227">Valitse ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="ce34d-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="ce34d-228">Laajenna Kustannusten hallinta -osa.</span><span class="sxs-lookup"><span data-stu-id="ce34d-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="ce34d-229">Kirjoita Kustannusryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ce34d-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="ce34d-230">Kirjoita tässä esimerkissä M1.</span><span class="sxs-lookup"><span data-stu-id="ce34d-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="ce34d-231">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="ce34d-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="ce34d-232">Valitse Nimikkeen hinta.</span><span class="sxs-lookup"><span data-stu-id="ce34d-232">Click Item price.</span></span>
20. <span data-ttu-id="ce34d-233">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ce34d-233">Click New.</span></span>
21. <span data-ttu-id="ce34d-234">Anna tai valitse arvo Versio-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce34d-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-235">Valitse tässä esimerkissä 10.</span><span class="sxs-lookup"><span data-stu-id="ce34d-235">For this example, select 10.</span></span> <span data-ttu-id="ce34d-236">Tämä on standardikustannuksen kustannuslaskentatyyppi.</span><span class="sxs-lookup"><span data-stu-id="ce34d-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="ce34d-237">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ce34d-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce34d-238">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="ce34d-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="ce34d-239">Syötä Hinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="ce34d-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="ce34d-240">Kirjoita tässä esimerkissä 10.</span><span class="sxs-lookup"><span data-stu-id="ce34d-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="ce34d-241">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="ce34d-241">Click Save.</span></span>
25. <span data-ttu-id="ce34d-242">Valitse Aktivoi odottavat hinnat.</span><span class="sxs-lookup"><span data-stu-id="ce34d-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="ce34d-243">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ce34d-243">Close the page.</span></span>
27. <span data-ttu-id="ce34d-244">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ce34d-244">Close the page.</span></span>


