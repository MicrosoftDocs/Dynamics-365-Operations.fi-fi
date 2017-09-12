--- 
title: Tuoterakenteiden luonti (vain helmikuu 2016)
description: "Tässä tehtävässä keskitytään valmiin ja puolivalmiin tuotteen tuoterakenteen luomiseen."
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
ms.openlocfilehash: f8ad4b0e230fb0f018355e486e3b898895a61f28
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="create-boms-february-2016-only"></a><span data-ttu-id="fa16d-103">Tuoterakenteiden luonti (vain helmikuu 2016)</span><span class="sxs-lookup"><span data-stu-id="fa16d-103">Create BOMs (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fa16d-104">Tässä tehtävässä keskitytään valmiin ja puolivalmiin tuotteen tuoterakenteen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="fa16d-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="fa16d-105">Se on tuoterakenteen laskentasarjan neljäs tehtävä.</span><span class="sxs-lookup"><span data-stu-id="fa16d-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="fa16d-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="fa16d-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="fa16d-107">Puolivalmiin tuotteen tuoterakenteen luominen</span><span class="sxs-lookup"><span data-stu-id="fa16d-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="fa16d-108">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="fa16d-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="fa16d-109">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="fa16d-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="fa16d-110">Valitse nimiketunnus BOM_2.</span><span class="sxs-lookup"><span data-stu-id="fa16d-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="fa16d-111">Valitse toimintoruudussa Suunnittele.</span><span class="sxs-lookup"><span data-stu-id="fa16d-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="fa16d-112">Valitse Tuoterakenneversiot.</span><span class="sxs-lookup"><span data-stu-id="fa16d-112">Click BOM versions.</span></span>
5. <span data-ttu-id="fa16d-113">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="fa16d-113">Click New.</span></span>
6. <span data-ttu-id="fa16d-114">Napsauta kohtia Tuoterakenne ja Tuoterakenneversio.</span><span class="sxs-lookup"><span data-stu-id="fa16d-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="fa16d-115">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fa16d-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="fa16d-116">Kirjoita esimerkiksi BOM_2.</span><span class="sxs-lookup"><span data-stu-id="fa16d-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="fa16d-117">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fa16d-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="fa16d-118">Anna tai valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="fa16d-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="fa16d-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="fa16d-119">Click OK.</span></span>
10. <span data-ttu-id="fa16d-120">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="fa16d-120">Click New.</span></span>
11. <span data-ttu-id="fa16d-121">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fa16d-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="fa16d-122">Kirjoita tässä esimerkissä ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="fa16d-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="fa16d-123">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="fa16d-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="fa16d-124">Anna tai valitse tässä esimerkissä 11.</span><span class="sxs-lookup"><span data-stu-id="fa16d-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="fa16d-125">Napsauta otsikkoa.</span><span class="sxs-lookup"><span data-stu-id="fa16d-125">Click Header.</span></span>
14. <span data-ttu-id="fa16d-126">Hyväksy tuoterakenteen valitsemalla Hyväksyminen.</span><span class="sxs-lookup"><span data-stu-id="fa16d-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="fa16d-127">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="fa16d-127">Click OK.</span></span>
16. <span data-ttu-id="fa16d-128">Valitse Hyväksy.</span><span class="sxs-lookup"><span data-stu-id="fa16d-128">Click Approve.</span></span>
    * <span data-ttu-id="fa16d-129">Hyväksymispainike on työkalurivillä tuoterakenneversioiden osassa.</span><span class="sxs-lookup"><span data-stu-id="fa16d-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="fa16d-130">Jos se ei ole näkyvissä, tuo Hyväksy näkyviin napsauttamalla ylätunnistetta Tuoterakenne-sivun oikeassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="fa16d-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="fa16d-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="fa16d-131">Click OK.</span></span>
18. <span data-ttu-id="fa16d-132">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="fa16d-132">Click Activate.</span></span>
19. <span data-ttu-id="fa16d-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="fa16d-133">Close the page.</span></span>
20. <span data-ttu-id="fa16d-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="fa16d-134">Close the page.</span></span>
21. <span data-ttu-id="fa16d-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="fa16d-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="fa16d-136">Valmiin tuotteen tuoterakenteen luominen</span><span class="sxs-lookup"><span data-stu-id="fa16d-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="fa16d-137">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="fa16d-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="fa16d-138">Valitse nimiketunnus BOM_1.</span><span class="sxs-lookup"><span data-stu-id="fa16d-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="fa16d-139">Valitse toimintoruudussa Suunnittele.</span><span class="sxs-lookup"><span data-stu-id="fa16d-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="fa16d-140">Valitse Tuoterakenneversiot.</span><span class="sxs-lookup"><span data-stu-id="fa16d-140">Click BOM versions.</span></span>
4. <span data-ttu-id="fa16d-141">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="fa16d-141">Click New.</span></span>
5. <span data-ttu-id="fa16d-142">Napsauta kohtia Tuoterakenne ja Tuoterakenneversio.</span><span class="sxs-lookup"><span data-stu-id="fa16d-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="fa16d-143">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fa16d-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="fa16d-144">Kirjoita esimerkiksi BOM_1.</span><span class="sxs-lookup"><span data-stu-id="fa16d-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="fa16d-145">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fa16d-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="fa16d-146">Anna tai valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="fa16d-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="fa16d-147">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="fa16d-147">Click OK.</span></span>
9. <span data-ttu-id="fa16d-148">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="fa16d-148">Click New.</span></span>
10. <span data-ttu-id="fa16d-149">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fa16d-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="fa16d-150">Kirjoita tässä esimerkissä ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="fa16d-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="fa16d-151">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="fa16d-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="fa16d-152">Valitse tässä esimerkissä 11.</span><span class="sxs-lookup"><span data-stu-id="fa16d-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="fa16d-153">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="fa16d-153">Click New.</span></span>
13. <span data-ttu-id="fa16d-154">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fa16d-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="fa16d-155">Kirjoita tässä esimerkissä ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="fa16d-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="fa16d-156">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="fa16d-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="fa16d-157">Anna tai valitse tässä esimerkissä 11.</span><span class="sxs-lookup"><span data-stu-id="fa16d-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="fa16d-158">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="fa16d-158">Click New.</span></span>
16. <span data-ttu-id="fa16d-159">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fa16d-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="fa16d-160">Kirjoita tässä esimerkissä BOM_2.</span><span class="sxs-lookup"><span data-stu-id="fa16d-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="fa16d-161">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="fa16d-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="fa16d-162">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="fa16d-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="fa16d-163">Anna tai valitse tässä esimerkissä varasto 11.</span><span class="sxs-lookup"><span data-stu-id="fa16d-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="fa16d-164">Napsauta otsikkoa.</span><span class="sxs-lookup"><span data-stu-id="fa16d-164">Click Header.</span></span>
20. <span data-ttu-id="fa16d-165">Hyväksy tuoterakenteen valitsemalla Hyväksyminen.</span><span class="sxs-lookup"><span data-stu-id="fa16d-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="fa16d-166">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="fa16d-166">Click OK.</span></span>
22. <span data-ttu-id="fa16d-167">Valitse Hyväksy.</span><span class="sxs-lookup"><span data-stu-id="fa16d-167">Click Approve.</span></span>
    * <span data-ttu-id="fa16d-168">Hyväksymispainike on työkalurivillä tuoterakenneversioiden osassa.</span><span class="sxs-lookup"><span data-stu-id="fa16d-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="fa16d-169">Jos se ei ole näkyvissä, tuo Hyväksy näkyviin napsauttamalla ylätunnistetta Tuoterakenne-sivun oikeassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="fa16d-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="fa16d-170">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="fa16d-170">Click OK.</span></span>
24. <span data-ttu-id="fa16d-171">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="fa16d-171">Click Activate.</span></span>
25. <span data-ttu-id="fa16d-172">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="fa16d-172">Close the page.</span></span>
26. <span data-ttu-id="fa16d-173">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="fa16d-173">Close the page.</span></span>
27. <span data-ttu-id="fa16d-174">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="fa16d-174">Close the page.</span></span>


