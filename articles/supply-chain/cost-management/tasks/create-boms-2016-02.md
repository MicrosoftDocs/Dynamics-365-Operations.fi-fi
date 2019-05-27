---
title: Tuoterakenteiden luonti (vain helmikuu 2016)
description: Tässä tehtävässä keskitytään valmiin ja puolivalmiin tuotteen tuoterakenteen luomiseen.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f132a3865b180a74d328ebc76ca29b2fc8aee85f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563247"
---
# <a name="create-boms-february-2016-only"></a><span data-ttu-id="26684-103">Tuoterakenteiden luonti (vain helmikuu 2016)</span><span class="sxs-lookup"><span data-stu-id="26684-103">Create BOMs (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="26684-104">Tässä tehtävässä keskitytään valmiin ja puolivalmiin tuotteen tuoterakenteen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="26684-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="26684-105">Se on tuoterakenteen laskentasarjan neljäs tehtävä.</span><span class="sxs-lookup"><span data-stu-id="26684-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="26684-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="26684-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="26684-107">Puolivalmiin tuotteen tuoterakenteen luominen</span><span class="sxs-lookup"><span data-stu-id="26684-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="26684-108">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="26684-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="26684-109">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="26684-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="26684-110">Valitse nimiketunnus BOM_2.</span><span class="sxs-lookup"><span data-stu-id="26684-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="26684-111">Valitse toimintoruudussa Suunnittele.</span><span class="sxs-lookup"><span data-stu-id="26684-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="26684-112">Valitse Tuoterakenneversiot.</span><span class="sxs-lookup"><span data-stu-id="26684-112">Click BOM versions.</span></span>
5. <span data-ttu-id="26684-113">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="26684-113">Click New.</span></span>
6. <span data-ttu-id="26684-114">Napsauta kohtia Tuoterakenne ja Tuoterakenneversio.</span><span class="sxs-lookup"><span data-stu-id="26684-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="26684-115">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="26684-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="26684-116">Kirjoita esimerkiksi BOM_2.</span><span class="sxs-lookup"><span data-stu-id="26684-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="26684-117">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="26684-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="26684-118">Anna tai valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="26684-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="26684-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="26684-119">Click OK.</span></span>
10. <span data-ttu-id="26684-120">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="26684-120">Click New.</span></span>
11. <span data-ttu-id="26684-121">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="26684-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="26684-122">Kirjoita tässä esimerkissä ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="26684-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="26684-123">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="26684-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="26684-124">Anna tai valitse tässä esimerkissä 11.</span><span class="sxs-lookup"><span data-stu-id="26684-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="26684-125">Napsauta otsikkoa.</span><span class="sxs-lookup"><span data-stu-id="26684-125">Click Header.</span></span>
14. <span data-ttu-id="26684-126">Hyväksy tuoterakenteen valitsemalla Hyväksyminen.</span><span class="sxs-lookup"><span data-stu-id="26684-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="26684-127">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="26684-127">Click OK.</span></span>
16. <span data-ttu-id="26684-128">Valitse Hyväksy.</span><span class="sxs-lookup"><span data-stu-id="26684-128">Click Approve.</span></span>
    * <span data-ttu-id="26684-129">Hyväksymispainike on työkalurivillä tuoterakenneversioiden osassa.</span><span class="sxs-lookup"><span data-stu-id="26684-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="26684-130">Jos se ei ole näkyvissä, tuo Hyväksy näkyviin napsauttamalla ylätunnistetta Tuoterakenne-sivun oikeassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="26684-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="26684-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="26684-131">Click OK.</span></span>
18. <span data-ttu-id="26684-132">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="26684-132">Click Activate.</span></span>
19. <span data-ttu-id="26684-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="26684-133">Close the page.</span></span>
20. <span data-ttu-id="26684-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="26684-134">Close the page.</span></span>
21. <span data-ttu-id="26684-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="26684-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="26684-136">Valmiin tuotteen tuoterakenteen luominen</span><span class="sxs-lookup"><span data-stu-id="26684-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="26684-137">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="26684-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="26684-138">Valitse nimiketunnus BOM_1.</span><span class="sxs-lookup"><span data-stu-id="26684-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="26684-139">Valitse toimintoruudussa Suunnittele.</span><span class="sxs-lookup"><span data-stu-id="26684-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="26684-140">Valitse Tuoterakenneversiot.</span><span class="sxs-lookup"><span data-stu-id="26684-140">Click BOM versions.</span></span>
4. <span data-ttu-id="26684-141">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="26684-141">Click New.</span></span>
5. <span data-ttu-id="26684-142">Napsauta kohtia Tuoterakenne ja Tuoterakenneversio.</span><span class="sxs-lookup"><span data-stu-id="26684-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="26684-143">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="26684-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="26684-144">Kirjoita esimerkiksi BOM_1.</span><span class="sxs-lookup"><span data-stu-id="26684-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="26684-145">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="26684-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="26684-146">Anna tai valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="26684-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="26684-147">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="26684-147">Click OK.</span></span>
9. <span data-ttu-id="26684-148">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="26684-148">Click New.</span></span>
10. <span data-ttu-id="26684-149">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="26684-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="26684-150">Kirjoita tässä esimerkissä ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="26684-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="26684-151">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="26684-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="26684-152">Valitse tässä esimerkissä 11.</span><span class="sxs-lookup"><span data-stu-id="26684-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="26684-153">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="26684-153">Click New.</span></span>
13. <span data-ttu-id="26684-154">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="26684-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="26684-155">Kirjoita tässä esimerkissä ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="26684-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="26684-156">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="26684-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="26684-157">Anna tai valitse tässä esimerkissä 11.</span><span class="sxs-lookup"><span data-stu-id="26684-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="26684-158">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="26684-158">Click New.</span></span>
16. <span data-ttu-id="26684-159">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="26684-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="26684-160">Kirjoita tässä esimerkissä BOM_2.</span><span class="sxs-lookup"><span data-stu-id="26684-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="26684-161">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="26684-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="26684-162">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="26684-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="26684-163">Anna tai valitse tässä esimerkissä varasto 11.</span><span class="sxs-lookup"><span data-stu-id="26684-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="26684-164">Napsauta otsikkoa.</span><span class="sxs-lookup"><span data-stu-id="26684-164">Click Header.</span></span>
20. <span data-ttu-id="26684-165">Hyväksy tuoterakenteen valitsemalla Hyväksyminen.</span><span class="sxs-lookup"><span data-stu-id="26684-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="26684-166">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="26684-166">Click OK.</span></span>
22. <span data-ttu-id="26684-167">Valitse Hyväksy.</span><span class="sxs-lookup"><span data-stu-id="26684-167">Click Approve.</span></span>
    * <span data-ttu-id="26684-168">Hyväksymispainike on työkalurivillä tuoterakenneversioiden osassa.</span><span class="sxs-lookup"><span data-stu-id="26684-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="26684-169">Jos se ei ole näkyvissä, tuo Hyväksy näkyviin napsauttamalla ylätunnistetta Tuoterakenne-sivun oikeassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="26684-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="26684-170">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="26684-170">Click OK.</span></span>
24. <span data-ttu-id="26684-171">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="26684-171">Click Activate.</span></span>
25. <span data-ttu-id="26684-172">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="26684-172">Close the page.</span></span>
26. <span data-ttu-id="26684-173">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="26684-173">Close the page.</span></span>
27. <span data-ttu-id="26684-174">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="26684-174">Close the page.</span></span>

