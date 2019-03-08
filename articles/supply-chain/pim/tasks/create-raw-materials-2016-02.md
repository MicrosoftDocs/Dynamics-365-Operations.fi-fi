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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 091b6edaf43e86e6e3665bf79871648473e284c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "351053"
---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="3fed4-103">Raaka-aineiden luominen (helmikuu 2016)</span><span class="sxs-lookup"><span data-stu-id="3fed4-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3fed4-104">Tämä tehtävä keskittyy valmiiden ja puolivalmiiden tuotteiden osien luomiseen.</span><span class="sxs-lookup"><span data-stu-id="3fed4-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="3fed4-105">Se on tuoterakenteen laskentasarjan kolmas tehtävä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="3fed4-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="3fed4-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="3fed4-107">Ensimmäisen materiaalin luonti</span><span class="sxs-lookup"><span data-stu-id="3fed4-107">Create the first material</span></span>
1. <span data-ttu-id="3fed4-108">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="3fed4-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="3fed4-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3fed4-109">Click New.</span></span>
3. <span data-ttu-id="3fed4-110">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3fed4-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="3fed4-111">Anna tässä esimerkissä ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="3fed4-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="3fed4-112">Syötä tai valitse arvo Nimikemalliryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-113">Valitse STD.</span><span class="sxs-lookup"><span data-stu-id="3fed4-113">Select STD.</span></span> <span data-ttu-id="3fed4-114">STD standardikustannusta ja on kustannuslaskennassa yleisimmin käytetty malli.</span><span class="sxs-lookup"><span data-stu-id="3fed4-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="3fed4-115">Anna tai valitse arvo Nimikeryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-116">Valitse esimerkiksi Audio.</span><span class="sxs-lookup"><span data-stu-id="3fed4-116">For example, select Audio.</span></span> <span data-ttu-id="3fed4-117">Se ei vaikuta kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="3fed4-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="3fed4-118">Syötä tai valitse arvo Varastodimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-119">Valitse SiteWH.</span><span class="sxs-lookup"><span data-stu-id="3fed4-119">Select SiteWH.</span></span> <span data-ttu-id="3fed4-120">Esimerkissä käytetään vain toimipaikkaa ja varastoa.</span><span class="sxs-lookup"><span data-stu-id="3fed4-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="3fed4-121">Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-122">Tässä esimerkissä ei käytetä seurantadimensioita.</span><span class="sxs-lookup"><span data-stu-id="3fed4-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="3fed4-123">Valitse Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="3fed4-123">Select None.</span></span>  
8. <span data-ttu-id="3fed4-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="3fed4-124">Click OK.</span></span>
9. <span data-ttu-id="3fed4-125">Valitse toimintoruudussa Varastonhallinta.</span><span class="sxs-lookup"><span data-stu-id="3fed4-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="3fed4-126">Valitse Tilauksen oletusasetukset.</span><span class="sxs-lookup"><span data-stu-id="3fed4-126">Click Default order settings.</span></span>
11. <span data-ttu-id="3fed4-127">Anna tai valitse arvo Ostotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-128">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="3fed4-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="3fed4-129">Anna tai valitse arvo Varastotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-130">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="3fed4-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="3fed4-131">Anna tai valitse arvo Myyntitoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-132">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="3fed4-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="3fed4-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3fed4-133">Close the page.</span></span>
15. <span data-ttu-id="3fed4-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3fed4-134">Close the page.</span></span>
16. <span data-ttu-id="3fed4-135">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3fed4-136">Valitse ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="3fed4-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="3fed4-137">Laajenna Kustannusten hallinta -osa.</span><span class="sxs-lookup"><span data-stu-id="3fed4-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="3fed4-138">Kirjoita Kustannusryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="3fed4-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="3fed4-139">Kirjoita tässä esimerkissä M2.</span><span class="sxs-lookup"><span data-stu-id="3fed4-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="3fed4-140">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="3fed4-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="3fed4-141">Valitse Nimikkeen hinta.</span><span class="sxs-lookup"><span data-stu-id="3fed4-141">Click Item price.</span></span>
21. <span data-ttu-id="3fed4-142">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3fed4-142">Click New.</span></span>
22. <span data-ttu-id="3fed4-143">Anna tai valitse arvo Versio-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-144">Valitse tässä esimerkissä 10, mikä on standardikustannuksen kustannuslaskentatyyppi.</span><span class="sxs-lookup"><span data-stu-id="3fed4-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="3fed4-145">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3fed4-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-146">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="3fed4-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="3fed4-147">Syötä Hinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="3fed4-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="3fed4-148">Kirjoita tässä esimerkissä 10.</span><span class="sxs-lookup"><span data-stu-id="3fed4-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="3fed4-149">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3fed4-149">Click Save.</span></span>
26. <span data-ttu-id="3fed4-150">Valitse Aktivoi odottavat hinnat.</span><span class="sxs-lookup"><span data-stu-id="3fed4-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="3fed4-151">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3fed4-151">Close the page.</span></span>
28. <span data-ttu-id="3fed4-152">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3fed4-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="3fed4-153">Toisen materiaalin luonti</span><span class="sxs-lookup"><span data-stu-id="3fed4-153">Create the second material</span></span>
1. <span data-ttu-id="3fed4-154">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3fed4-154">Click New.</span></span>
2. <span data-ttu-id="3fed4-155">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3fed4-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="3fed4-156">Kirjoita tässä esimerkissä ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="3fed4-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="3fed4-157">Syötä tai valitse arvo Nimikemalliryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-158">Valitse STD.</span><span class="sxs-lookup"><span data-stu-id="3fed4-158">Select STD.</span></span> <span data-ttu-id="3fed4-159">STD standardikustannusta ja on kustannuslaskennassa yleisimmin käytetty malli.</span><span class="sxs-lookup"><span data-stu-id="3fed4-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="3fed4-160">Anna tai valitse arvo Nimikeryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-161">Valitse esimerkiksi Audio.</span><span class="sxs-lookup"><span data-stu-id="3fed4-161">For example, select Audio.</span></span> <span data-ttu-id="3fed4-162">Se ei vaikuta kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="3fed4-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="3fed4-163">Syötä tai valitse arvo Varastodimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-164">Valitse SiteWH.</span><span class="sxs-lookup"><span data-stu-id="3fed4-164">Select SiteWH.</span></span> <span data-ttu-id="3fed4-165">Tässä esimerkissä käytetään vain toimipaikkaa ja varastoa.</span><span class="sxs-lookup"><span data-stu-id="3fed4-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="3fed4-166">Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-167">Tässä esimerkissä ei käytetä seurantadimensioita.</span><span class="sxs-lookup"><span data-stu-id="3fed4-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="3fed4-168">Valitse Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="3fed4-168">Select None.</span></span>  
7. <span data-ttu-id="3fed4-169">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="3fed4-169">Click OK.</span></span>
8. <span data-ttu-id="3fed4-170">Valitse toimintoruudussa Varastonhallinta.</span><span class="sxs-lookup"><span data-stu-id="3fed4-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="3fed4-171">Valitse Tilauksen oletusasetukset.</span><span class="sxs-lookup"><span data-stu-id="3fed4-171">Click Default order settings.</span></span>
10. <span data-ttu-id="3fed4-172">Anna tai valitse arvo Ostotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-173">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="3fed4-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="3fed4-174">Anna tai valitse arvo Varastotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-175">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="3fed4-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="3fed4-176">Anna tai valitse arvo Myyntitoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-177">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="3fed4-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="3fed4-178">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3fed4-178">Close the page.</span></span>
14. <span data-ttu-id="3fed4-179">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3fed4-179">Close the page.</span></span>
15. <span data-ttu-id="3fed4-180">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3fed4-181">Valitse ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="3fed4-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="3fed4-182">Laajenna Kustannusten hallinta -osa.</span><span class="sxs-lookup"><span data-stu-id="3fed4-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="3fed4-183">Kirjoita Kustannusryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="3fed4-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="3fed4-184">Kirjoita tässä esimerkissä M2.</span><span class="sxs-lookup"><span data-stu-id="3fed4-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="3fed4-185">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="3fed4-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="3fed4-186">Valitse Nimikkeen hinta.</span><span class="sxs-lookup"><span data-stu-id="3fed4-186">Click Item price.</span></span>
20. <span data-ttu-id="3fed4-187">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3fed4-187">Click New.</span></span>
21. <span data-ttu-id="3fed4-188">Anna tai valitse arvo Versio-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-189">Valitse tässä esimerkissä 10.</span><span class="sxs-lookup"><span data-stu-id="3fed4-189">For this example, select 10.</span></span> <span data-ttu-id="3fed4-190">Tämä on standardikustannuksen kustannuslaskentatyyppi.</span><span class="sxs-lookup"><span data-stu-id="3fed4-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="3fed4-191">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3fed4-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-192">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="3fed4-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="3fed4-193">Syötä Hinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="3fed4-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="3fed4-194">Kirjoita esimerkkiä varten 10.</span><span class="sxs-lookup"><span data-stu-id="3fed4-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="3fed4-195">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3fed4-195">Click Save.</span></span>
25. <span data-ttu-id="3fed4-196">Valitse Aktivoi odottavat hinnat.</span><span class="sxs-lookup"><span data-stu-id="3fed4-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="3fed4-197">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3fed4-197">Close the page.</span></span>
27. <span data-ttu-id="3fed4-198">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3fed4-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="3fed4-199">Kolmannen materiaalin luonti</span><span class="sxs-lookup"><span data-stu-id="3fed4-199">Create the third material</span></span>
1. <span data-ttu-id="3fed4-200">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3fed4-200">Click New.</span></span>
2. <span data-ttu-id="3fed4-201">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3fed4-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="3fed4-202">Kirjoita esimerkkiä varten ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="3fed4-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="3fed4-203">Syötä tai valitse arvo Nimikemalliryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-204">Valitse STD.</span><span class="sxs-lookup"><span data-stu-id="3fed4-204">Select STD.</span></span> <span data-ttu-id="3fed4-205">STD standardikustannusta ja on kustannuslaskennassa yleisimmin käytetty malli.</span><span class="sxs-lookup"><span data-stu-id="3fed4-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="3fed4-206">Anna tai valitse arvo Nimikeryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-207">Valitse esimerkiksi Audio.</span><span class="sxs-lookup"><span data-stu-id="3fed4-207">For example, select Audio.</span></span> <span data-ttu-id="3fed4-208">Se ei vaikuta kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="3fed4-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="3fed4-209">Syötä tai valitse arvo Varastodimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-210">Valitse SiteWH.</span><span class="sxs-lookup"><span data-stu-id="3fed4-210">Select SiteWH.</span></span> <span data-ttu-id="3fed4-211">Esimerkissä käytetään vain toimipaikkaa ja varastoa.</span><span class="sxs-lookup"><span data-stu-id="3fed4-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="3fed4-212">Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-213">Tässä esimerkissä ei käytetä seurantadimensioita.</span><span class="sxs-lookup"><span data-stu-id="3fed4-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="3fed4-214">Valitse Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="3fed4-214">Select None.</span></span>  
7. <span data-ttu-id="3fed4-215">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="3fed4-215">Click OK.</span></span>
8. <span data-ttu-id="3fed4-216">Valitse toimintoruudussa Varastonhallinta.</span><span class="sxs-lookup"><span data-stu-id="3fed4-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="3fed4-217">Valitse Tilauksen oletusasetukset.</span><span class="sxs-lookup"><span data-stu-id="3fed4-217">Click Default order settings.</span></span>
10. <span data-ttu-id="3fed4-218">Anna tai valitse arvo Ostotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-219">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="3fed4-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="3fed4-220">Anna tai valitse arvo Varastotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-221">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="3fed4-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="3fed4-222">Anna tai valitse arvo Myyntitoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-223">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="3fed4-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="3fed4-224">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3fed4-224">Close the page.</span></span>
14. <span data-ttu-id="3fed4-225">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3fed4-225">Close the page.</span></span>
15. <span data-ttu-id="3fed4-226">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3fed4-227">Valitse ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="3fed4-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="3fed4-228">Laajenna Kustannusten hallinta -osa.</span><span class="sxs-lookup"><span data-stu-id="3fed4-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="3fed4-229">Kirjoita Kustannusryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="3fed4-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="3fed4-230">Kirjoita tässä esimerkissä M1.</span><span class="sxs-lookup"><span data-stu-id="3fed4-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="3fed4-231">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="3fed4-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="3fed4-232">Valitse Nimikkeen hinta.</span><span class="sxs-lookup"><span data-stu-id="3fed4-232">Click Item price.</span></span>
20. <span data-ttu-id="3fed4-233">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3fed4-233">Click New.</span></span>
21. <span data-ttu-id="3fed4-234">Anna tai valitse arvo Versio-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3fed4-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-235">Valitse tässä esimerkissä 10.</span><span class="sxs-lookup"><span data-stu-id="3fed4-235">For this example, select 10.</span></span> <span data-ttu-id="3fed4-236">Tämä on standardikustannuksen kustannuslaskentatyyppi.</span><span class="sxs-lookup"><span data-stu-id="3fed4-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="3fed4-237">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3fed4-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="3fed4-238">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="3fed4-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="3fed4-239">Syötä Hinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="3fed4-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="3fed4-240">Kirjoita tässä esimerkissä 10.</span><span class="sxs-lookup"><span data-stu-id="3fed4-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="3fed4-241">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3fed4-241">Click Save.</span></span>
25. <span data-ttu-id="3fed4-242">Valitse Aktivoi odottavat hinnat.</span><span class="sxs-lookup"><span data-stu-id="3fed4-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="3fed4-243">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3fed4-243">Close the page.</span></span>
27. <span data-ttu-id="3fed4-244">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3fed4-244">Close the page.</span></span>

