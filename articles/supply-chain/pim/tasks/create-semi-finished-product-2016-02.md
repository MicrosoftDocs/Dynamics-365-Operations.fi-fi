--- 
title: Puolivalmiin tuotteen luominen (helmikuu 2016)
description: "Tämä tehtävä keskittyy puolivalmiin tuotteen luomiseen."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 9caeae552471eed1cb1d8630f387ca31107fcece
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-semi-finished-product-february-2016"></a><span data-ttu-id="338c4-103">Puolivalmiin tuotteen luominen (helmikuu 2016)</span><span class="sxs-lookup"><span data-stu-id="338c4-103">Create a semi-finished product (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="338c4-104">Tämä tehtävä keskittyy puolivalmiin tuotteen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="338c4-104">This task focuses on creating a semi-finished product.</span></span> <span data-ttu-id="338c4-105">Se on tuoterakenteen laskentasarjan toinen tehtävä.</span><span class="sxs-lookup"><span data-stu-id="338c4-105">It is the second task in the BOM calculation series.</span></span> <span data-ttu-id="338c4-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="338c4-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="338c4-107">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="338c4-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="338c4-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="338c4-108">Click New.</span></span>
3. <span data-ttu-id="338c4-109">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="338c4-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="338c4-110">Kirjoita tässä esimerkissä BOM_2.</span><span class="sxs-lookup"><span data-stu-id="338c4-110">For this example, type BOM_2.</span></span>  
4. <span data-ttu-id="338c4-111">Syötä tai valitse arvo Nimikemalliryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="338c4-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="338c4-112">Valitse STD.</span><span class="sxs-lookup"><span data-stu-id="338c4-112">Select STD.</span></span> <span data-ttu-id="338c4-113">STD standardikustannusta ja on kustannuslaskennassa yleisimmin käytetty malli.</span><span class="sxs-lookup"><span data-stu-id="338c4-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="338c4-114">Anna tai valitse arvo Nimikeryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="338c4-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="338c4-115">Valitse esimerkiksi Audio.</span><span class="sxs-lookup"><span data-stu-id="338c4-115">For example, select Audio.</span></span> <span data-ttu-id="338c4-116">Se ei vaikuta kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="338c4-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="338c4-117">Syötä tai valitse arvo Varastodimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="338c4-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="338c4-118">Valitse SiteWH.</span><span class="sxs-lookup"><span data-stu-id="338c4-118">Select SiteWH.</span></span> <span data-ttu-id="338c4-119">Tässä esimerkissä käytetään vain toimipaikkaa ja varastoa.</span><span class="sxs-lookup"><span data-stu-id="338c4-119">Only Site and Warehouse will be used for this example.</span></span>  
7. <span data-ttu-id="338c4-120">Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="338c4-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="338c4-121">Tässä esimerkissä ei käytetä seurantadimensioita. Valitse Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="338c4-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="338c4-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="338c4-122">Click OK.</span></span>
9. <span data-ttu-id="338c4-123">Valitse toimintoruudussa Varastonhallinta.</span><span class="sxs-lookup"><span data-stu-id="338c4-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="338c4-124">Valitse Tilauksen oletusasetukset.</span><span class="sxs-lookup"><span data-stu-id="338c4-124">Click Default order settings.</span></span>
11. <span data-ttu-id="338c4-125">Valitse Oletusarvoinen tilaustyyppi -kentässä Tuotanto.</span><span class="sxs-lookup"><span data-stu-id="338c4-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="338c4-126">Koska kyse on puolivalmiista tuotantoon tulevasta tuotteesta, valitse Tuotanto.</span><span class="sxs-lookup"><span data-stu-id="338c4-126">Because this is a semi-finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="338c4-127">Anna tai valitse arvo Ostotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="338c4-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="338c4-128">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="338c4-128">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="338c4-129">Anna tai valitse arvo Varastotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="338c4-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="338c4-130">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="338c4-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="338c4-131">Anna tai valitse arvo Myyntitoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="338c4-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="338c4-132">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="338c4-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="338c4-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="338c4-133">Close the page.</span></span>
16. <span data-ttu-id="338c4-134">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="338c4-134">On the Action Pane, click Manage costs.</span></span>
17. <span data-ttu-id="338c4-135">Valitse Nimikkeen hinta.</span><span class="sxs-lookup"><span data-stu-id="338c4-135">Click Item price.</span></span>
18. <span data-ttu-id="338c4-136">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="338c4-136">Click New.</span></span>
19. <span data-ttu-id="338c4-137">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="338c4-137">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="338c4-138">Anna tai valitse arvo Versio-kentässä.</span><span class="sxs-lookup"><span data-stu-id="338c4-138">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="338c4-139">Valitse tässä esimerkissä Versio 10.</span><span class="sxs-lookup"><span data-stu-id="338c4-139">For this example, select Version 10.</span></span>  
21. <span data-ttu-id="338c4-140">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="338c4-140">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="338c4-141">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="338c4-141">For this example, select Site 1.</span></span>  
22. <span data-ttu-id="338c4-142">Määritä hinnaksi 10.</span><span class="sxs-lookup"><span data-stu-id="338c4-142">Set Price to '10'.</span></span>
    * <span data-ttu-id="338c4-143">Kirjoita tässä esimerkissä kustannushinnaksi 10.</span><span class="sxs-lookup"><span data-stu-id="338c4-143">For this example, type a cost price of 10.</span></span>  
23. <span data-ttu-id="338c4-144">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="338c4-144">Click Save.</span></span>
24. <span data-ttu-id="338c4-145">Valitse Aktivoi odottavat hinnat.</span><span class="sxs-lookup"><span data-stu-id="338c4-145">Click Activate pending price(s).</span></span>
25. <span data-ttu-id="338c4-146">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="338c4-146">Close the page.</span></span>
26. <span data-ttu-id="338c4-147">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="338c4-147">Close the page.</span></span>
27. <span data-ttu-id="338c4-148">Avaa se valitsemalla BOM_2.</span><span class="sxs-lookup"><span data-stu-id="338c4-148">Click BOM_2 to open it.</span></span>
28. <span data-ttu-id="338c4-149">Laajenna Kustannusten hallinta -osa.</span><span class="sxs-lookup"><span data-stu-id="338c4-149">Expand the Manage costs section.</span></span>
29. <span data-ttu-id="338c4-150">Anna tai valitse arvo Kustannusryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="338c4-150">In the Cost group field, enter or select a value.</span></span>
    * <span data-ttu-id="338c4-151">Valitse tässä esimerkissä Kustannusryhmä M1.</span><span class="sxs-lookup"><span data-stu-id="338c4-151">For this example, select Cost group M1.</span></span>  
30. <span data-ttu-id="338c4-152">Tallenna tietue tällä pikanäppäimellä.</span><span class="sxs-lookup"><span data-stu-id="338c4-152">Use the shortcut for saving a record.</span></span>
31. <span data-ttu-id="338c4-153">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="338c4-153">Close the page.</span></span>


