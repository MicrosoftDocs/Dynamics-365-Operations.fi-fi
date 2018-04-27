--- 
title: Luo puolivalmis tuote (vain helmikuu 2016)
description: "Tämä tehtävä keskittyy puolivalmiin tuotteen luomiseen."
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
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1311e27b4080832c6e1aa2b879308f518d2ab001
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-semi-finished-product-february-2016-only"></a><span data-ttu-id="21d96-103">Luo puolivalmis tuote (vain helmikuu 2016)</span><span class="sxs-lookup"><span data-stu-id="21d96-103">Create a semi-finished product (February 2016 only)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="21d96-104">Tämä tehtävä keskittyy puolivalmiin tuotteen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="21d96-104">This task focuses on creating a semi-finished product.</span></span> <span data-ttu-id="21d96-105">Se on tuoterakenteen laskentasarjan toinen tehtävä.</span><span class="sxs-lookup"><span data-stu-id="21d96-105">It is the second task in the BOM calculation series.</span></span> <span data-ttu-id="21d96-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="21d96-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="21d96-107">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="21d96-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="21d96-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="21d96-108">Click New.</span></span>
3. <span data-ttu-id="21d96-109">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="21d96-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="21d96-110">Kirjoita tässä esimerkissä BOM_2.</span><span class="sxs-lookup"><span data-stu-id="21d96-110">For this example, type BOM_2.</span></span>  
4. <span data-ttu-id="21d96-111">Syötä tai valitse arvo Nimikemalliryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="21d96-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="21d96-112">Valitse STD.</span><span class="sxs-lookup"><span data-stu-id="21d96-112">Select STD.</span></span> <span data-ttu-id="21d96-113">STD standardikustannusta ja on kustannuslaskennassa yleisimmin käytetty malli.</span><span class="sxs-lookup"><span data-stu-id="21d96-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="21d96-114">Anna tai valitse arvo Nimikeryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="21d96-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="21d96-115">Valitse esimerkiksi Audio.</span><span class="sxs-lookup"><span data-stu-id="21d96-115">For example, select Audio.</span></span> <span data-ttu-id="21d96-116">Se ei vaikuta kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="21d96-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="21d96-117">Syötä tai valitse arvo Varastodimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="21d96-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="21d96-118">Valitse SiteWH.</span><span class="sxs-lookup"><span data-stu-id="21d96-118">Select SiteWH.</span></span> <span data-ttu-id="21d96-119">Tässä esimerkissä käytetään vain toimipaikkaa ja varastoa.</span><span class="sxs-lookup"><span data-stu-id="21d96-119">Only Site and Warehouse will be used for this example.</span></span>  
7. <span data-ttu-id="21d96-120">Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="21d96-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="21d96-121">Tässä esimerkissä ei käytetä seurantadimensioita. Valitse Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="21d96-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="21d96-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="21d96-122">Click OK.</span></span>
9. <span data-ttu-id="21d96-123">Valitse toimintoruudussa Varastonhallinta.</span><span class="sxs-lookup"><span data-stu-id="21d96-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="21d96-124">Valitse Tilauksen oletusasetukset.</span><span class="sxs-lookup"><span data-stu-id="21d96-124">Click Default order settings.</span></span>
11. <span data-ttu-id="21d96-125">Valitse Oletusarvoinen tilaustyyppi -kentässä Tuotanto.</span><span class="sxs-lookup"><span data-stu-id="21d96-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="21d96-126">Koska kyse on puolivalmiista tuotantoon tulevasta tuotteesta, valitse Tuotanto.</span><span class="sxs-lookup"><span data-stu-id="21d96-126">Because this is a semi-finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="21d96-127">Anna tai valitse arvo Ostotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="21d96-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="21d96-128">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="21d96-128">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="21d96-129">Anna tai valitse arvo Varastotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="21d96-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="21d96-130">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="21d96-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="21d96-131">Anna tai valitse arvo Myyntitoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="21d96-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="21d96-132">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="21d96-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="21d96-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="21d96-133">Close the page.</span></span>
16. <span data-ttu-id="21d96-134">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="21d96-134">On the Action Pane, click Manage costs.</span></span>
17. <span data-ttu-id="21d96-135">Valitse Nimikkeen hinta.</span><span class="sxs-lookup"><span data-stu-id="21d96-135">Click Item price.</span></span>
18. <span data-ttu-id="21d96-136">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="21d96-136">Click New.</span></span>
19. <span data-ttu-id="21d96-137">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="21d96-137">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="21d96-138">Anna tai valitse arvo Versio-kentässä.</span><span class="sxs-lookup"><span data-stu-id="21d96-138">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="21d96-139">Valitse tässä esimerkissä Versio 10.</span><span class="sxs-lookup"><span data-stu-id="21d96-139">For this example, select Version 10.</span></span>  
21. <span data-ttu-id="21d96-140">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="21d96-140">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="21d96-141">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="21d96-141">For this example, select Site 1.</span></span>  
22. <span data-ttu-id="21d96-142">Määritä hinnaksi 10.</span><span class="sxs-lookup"><span data-stu-id="21d96-142">Set Price to '10'.</span></span>
    * <span data-ttu-id="21d96-143">Kirjoita tässä esimerkissä kustannushinnaksi 10.</span><span class="sxs-lookup"><span data-stu-id="21d96-143">For this example, type a cost price of 10.</span></span>  
23. <span data-ttu-id="21d96-144">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="21d96-144">Click Save.</span></span>
24. <span data-ttu-id="21d96-145">Valitse Aktivoi odottavat hinnat.</span><span class="sxs-lookup"><span data-stu-id="21d96-145">Click Activate pending price(s).</span></span>
25. <span data-ttu-id="21d96-146">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="21d96-146">Close the page.</span></span>
26. <span data-ttu-id="21d96-147">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="21d96-147">Close the page.</span></span>
27. <span data-ttu-id="21d96-148">Avaa se valitsemalla BOM_2.</span><span class="sxs-lookup"><span data-stu-id="21d96-148">Click BOM_2 to open it.</span></span>
28. <span data-ttu-id="21d96-149">Laajenna Kustannusten hallinta -osa.</span><span class="sxs-lookup"><span data-stu-id="21d96-149">Expand the Manage costs section.</span></span>
29. <span data-ttu-id="21d96-150">Anna tai valitse arvo Kustannusryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="21d96-150">In the Cost group field, enter or select a value.</span></span>
    * <span data-ttu-id="21d96-151">Valitse tässä esimerkissä Kustannusryhmä M1.</span><span class="sxs-lookup"><span data-stu-id="21d96-151">For this example, select Cost group M1.</span></span>  
30. <span data-ttu-id="21d96-152">Tallenna tietue tällä pikanäppäimellä.</span><span class="sxs-lookup"><span data-stu-id="21d96-152">Use the shortcut for saving a record.</span></span>
31. <span data-ttu-id="21d96-153">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="21d96-153">Close the page.</span></span>


