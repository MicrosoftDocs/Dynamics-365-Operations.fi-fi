--- 
title: Tuoterakenteiden luonti (vain helmikuu 2016)
description: "Tässä tehtävässä keskitytään valmiin ja puolivalmiin tuotteen tuoterakenteen luomiseen."
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6c5473a0786ba0348701e8e106de46f811571f07
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="create-boms-february-2016-only"></a><span data-ttu-id="aeb08-103">Tuoterakenteiden luonti (vain helmikuu 2016)</span><span class="sxs-lookup"><span data-stu-id="aeb08-103">Create BOMs (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aeb08-104">Tässä tehtävässä keskitytään valmiin ja puolivalmiin tuotteen tuoterakenteen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="aeb08-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="aeb08-105">Se on tuoterakenteen laskentasarjan neljäs tehtävä.</span><span class="sxs-lookup"><span data-stu-id="aeb08-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="aeb08-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="aeb08-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="aeb08-107">Puolivalmiin tuotteen tuoterakenteen luominen</span><span class="sxs-lookup"><span data-stu-id="aeb08-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="aeb08-108">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="aeb08-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="aeb08-109">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="aeb08-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="aeb08-110">Valitse nimiketunnus BOM_2.</span><span class="sxs-lookup"><span data-stu-id="aeb08-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="aeb08-111">Valitse toimintoruudussa Suunnittele.</span><span class="sxs-lookup"><span data-stu-id="aeb08-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="aeb08-112">Valitse Tuoterakenneversiot.</span><span class="sxs-lookup"><span data-stu-id="aeb08-112">Click BOM versions.</span></span>
5. <span data-ttu-id="aeb08-113">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="aeb08-113">Click New.</span></span>
6. <span data-ttu-id="aeb08-114">Napsauta kohtia Tuoterakenne ja Tuoterakenneversio.</span><span class="sxs-lookup"><span data-stu-id="aeb08-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="aeb08-115">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aeb08-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="aeb08-116">Kirjoita esimerkiksi BOM_2.</span><span class="sxs-lookup"><span data-stu-id="aeb08-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="aeb08-117">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aeb08-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb08-118">Anna tai valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="aeb08-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="aeb08-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="aeb08-119">Click OK.</span></span>
10. <span data-ttu-id="aeb08-120">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="aeb08-120">Click New.</span></span>
11. <span data-ttu-id="aeb08-121">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aeb08-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="aeb08-122">Kirjoita tässä esimerkissä ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="aeb08-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="aeb08-123">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="aeb08-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb08-124">Anna tai valitse tässä esimerkissä 11.</span><span class="sxs-lookup"><span data-stu-id="aeb08-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="aeb08-125">Napsauta otsikkoa.</span><span class="sxs-lookup"><span data-stu-id="aeb08-125">Click Header.</span></span>
14. <span data-ttu-id="aeb08-126">Hyväksy tuoterakenteen valitsemalla Hyväksyminen.</span><span class="sxs-lookup"><span data-stu-id="aeb08-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="aeb08-127">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="aeb08-127">Click OK.</span></span>
16. <span data-ttu-id="aeb08-128">Valitse Hyväksy.</span><span class="sxs-lookup"><span data-stu-id="aeb08-128">Click Approve.</span></span>
    * <span data-ttu-id="aeb08-129">Hyväksymispainike on työkalurivillä tuoterakenneversioiden osassa.</span><span class="sxs-lookup"><span data-stu-id="aeb08-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="aeb08-130">Jos se ei ole näkyvissä, tuo Hyväksy näkyviin napsauttamalla ylätunnistetta Tuoterakenne-sivun oikeassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="aeb08-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="aeb08-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="aeb08-131">Click OK.</span></span>
18. <span data-ttu-id="aeb08-132">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="aeb08-132">Click Activate.</span></span>
19. <span data-ttu-id="aeb08-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aeb08-133">Close the page.</span></span>
20. <span data-ttu-id="aeb08-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aeb08-134">Close the page.</span></span>
21. <span data-ttu-id="aeb08-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aeb08-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="aeb08-136">Valmiin tuotteen tuoterakenteen luominen</span><span class="sxs-lookup"><span data-stu-id="aeb08-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="aeb08-137">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="aeb08-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="aeb08-138">Valitse nimiketunnus BOM_1.</span><span class="sxs-lookup"><span data-stu-id="aeb08-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="aeb08-139">Valitse toimintoruudussa Suunnittele.</span><span class="sxs-lookup"><span data-stu-id="aeb08-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="aeb08-140">Valitse Tuoterakenneversiot.</span><span class="sxs-lookup"><span data-stu-id="aeb08-140">Click BOM versions.</span></span>
4. <span data-ttu-id="aeb08-141">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="aeb08-141">Click New.</span></span>
5. <span data-ttu-id="aeb08-142">Napsauta kohtia Tuoterakenne ja Tuoterakenneversio.</span><span class="sxs-lookup"><span data-stu-id="aeb08-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="aeb08-143">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aeb08-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="aeb08-144">Kirjoita esimerkiksi BOM_1.</span><span class="sxs-lookup"><span data-stu-id="aeb08-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="aeb08-145">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aeb08-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb08-146">Anna tai valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="aeb08-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="aeb08-147">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="aeb08-147">Click OK.</span></span>
9. <span data-ttu-id="aeb08-148">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="aeb08-148">Click New.</span></span>
10. <span data-ttu-id="aeb08-149">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aeb08-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="aeb08-150">Kirjoita tässä esimerkissä ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="aeb08-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="aeb08-151">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="aeb08-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb08-152">Valitse tässä esimerkissä 11.</span><span class="sxs-lookup"><span data-stu-id="aeb08-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="aeb08-153">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="aeb08-153">Click New.</span></span>
13. <span data-ttu-id="aeb08-154">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aeb08-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="aeb08-155">Kirjoita tässä esimerkissä ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="aeb08-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="aeb08-156">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="aeb08-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb08-157">Anna tai valitse tässä esimerkissä 11.</span><span class="sxs-lookup"><span data-stu-id="aeb08-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="aeb08-158">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="aeb08-158">Click New.</span></span>
16. <span data-ttu-id="aeb08-159">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aeb08-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="aeb08-160">Kirjoita tässä esimerkissä BOM_2.</span><span class="sxs-lookup"><span data-stu-id="aeb08-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="aeb08-161">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="aeb08-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="aeb08-162">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="aeb08-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="aeb08-163">Anna tai valitse tässä esimerkissä varasto 11.</span><span class="sxs-lookup"><span data-stu-id="aeb08-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="aeb08-164">Napsauta otsikkoa.</span><span class="sxs-lookup"><span data-stu-id="aeb08-164">Click Header.</span></span>
20. <span data-ttu-id="aeb08-165">Hyväksy tuoterakenteen valitsemalla Hyväksyminen.</span><span class="sxs-lookup"><span data-stu-id="aeb08-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="aeb08-166">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="aeb08-166">Click OK.</span></span>
22. <span data-ttu-id="aeb08-167">Valitse Hyväksy.</span><span class="sxs-lookup"><span data-stu-id="aeb08-167">Click Approve.</span></span>
    * <span data-ttu-id="aeb08-168">Hyväksymispainike on työkalurivillä tuoterakenneversioiden osassa.</span><span class="sxs-lookup"><span data-stu-id="aeb08-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="aeb08-169">Jos se ei ole näkyvissä, tuo Hyväksy näkyviin napsauttamalla ylätunnistetta Tuoterakenne-sivun oikeassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="aeb08-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="aeb08-170">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="aeb08-170">Click OK.</span></span>
24. <span data-ttu-id="aeb08-171">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="aeb08-171">Click Activate.</span></span>
25. <span data-ttu-id="aeb08-172">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aeb08-172">Close the page.</span></span>
26. <span data-ttu-id="aeb08-173">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aeb08-173">Close the page.</span></span>
27. <span data-ttu-id="aeb08-174">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aeb08-174">Close the page.</span></span>


