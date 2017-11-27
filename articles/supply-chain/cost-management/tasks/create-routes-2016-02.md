--- 
title: Reititysten luonti (vain helmikuu 2016)
description: "Tässä tehtävässä keskitytään valmiin ja puolivalmiin tuotteen tuotantoreitityksen luomiseen."
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
ms.sourcegitcommit: 273ced77a61d485426c0830556e4401e782e86c4
ms.openlocfilehash: 1ba2ae3ad92149636714701448d4dac8296d6613
ms.contentlocale: fi-fi
ms.lasthandoff: 10/24/2017

---
# <a name="create-routes-february-2016-only"></a><span data-ttu-id="39ad5-103">Reititysten luonti (vain helmikuu 2016)</span><span class="sxs-lookup"><span data-stu-id="39ad5-103">Create routes (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="39ad5-104">Tässä tehtävässä keskitytään valmiin ja puolivalmiin tuotteen tuotantoreitityksen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="39ad5-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="39ad5-105">Se on tuoterakenteen laskentasarjan viides tehtävä.</span><span class="sxs-lookup"><span data-stu-id="39ad5-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="39ad5-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="39ad5-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="39ad5-107">Puolivalmiin tuotteen reitin luominen</span><span class="sxs-lookup"><span data-stu-id="39ad5-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="39ad5-108">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="39ad5-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="39ad5-109">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="39ad5-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="39ad5-110">Valitse nimiketunnus BOM_2.</span><span class="sxs-lookup"><span data-stu-id="39ad5-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="39ad5-111">Valitse toimintoruudussa Suunnittele.</span><span class="sxs-lookup"><span data-stu-id="39ad5-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="39ad5-112">Valitse Reitti.</span><span class="sxs-lookup"><span data-stu-id="39ad5-112">Click Route.</span></span>
5. <span data-ttu-id="39ad5-113">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="39ad5-113">Click New.</span></span>
6. <span data-ttu-id="39ad5-114">Valitse Reitti ja reittiversio.</span><span class="sxs-lookup"><span data-stu-id="39ad5-114">Click Route and route version.</span></span>
7. <span data-ttu-id="39ad5-115">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="39ad5-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="39ad5-116">Kirjoita tässä esimerkissä ROUTE_2.</span><span class="sxs-lookup"><span data-stu-id="39ad5-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="39ad5-117">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="39ad5-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="39ad5-118">Anna tai valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="39ad5-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="39ad5-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="39ad5-119">Click OK.</span></span>
10. <span data-ttu-id="39ad5-120">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="39ad5-120">Click New.</span></span>
11. <span data-ttu-id="39ad5-121">Anna tai valitse Toiminto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="39ad5-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="39ad5-122">Valitse tässä esimerkissä Kokoonpano.</span><span class="sxs-lookup"><span data-stu-id="39ad5-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="39ad5-123">Lisää Ajoaika-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="39ad5-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="39ad5-124">Kirjoita esimerkiksi 1.</span><span class="sxs-lookup"><span data-stu-id="39ad5-124">For example, type 1.</span></span> <span data-ttu-id="39ad5-125">Suoritusajat sisältyvät usein nimikkeelle laskettavaan hintaan.</span><span class="sxs-lookup"><span data-stu-id="39ad5-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="39ad5-126">Anna tai valitse arvo Reititysryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="39ad5-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="39ad5-127">Valitse tässä esimerkissä Std.</span><span class="sxs-lookup"><span data-stu-id="39ad5-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="39ad5-128">Valitse Asetukset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="39ad5-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="39ad5-129">Syötä tai valitse arvo Asetusluokka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="39ad5-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="39ad5-130">Valitse tässä esimerkissä Kokoonpano.</span><span class="sxs-lookup"><span data-stu-id="39ad5-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="39ad5-131">Valitse Ajat-välilehti.</span><span class="sxs-lookup"><span data-stu-id="39ad5-131">Click the Times tab.</span></span>
17. <span data-ttu-id="39ad5-132">Anna Asetusaika-kentässä luku.</span><span class="sxs-lookup"><span data-stu-id="39ad5-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="39ad5-133">Kirjoita tässä esimerkissä 1.</span><span class="sxs-lookup"><span data-stu-id="39ad5-133">For this example, type 1.</span></span> <span data-ttu-id="39ad5-134">Asetusajat sisältyvät usein nimikkeelle laskettavaan hintaan.</span><span class="sxs-lookup"><span data-stu-id="39ad5-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="39ad5-135">Valitse toimintoruudussa Reittiversio.</span><span class="sxs-lookup"><span data-stu-id="39ad5-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="39ad5-136">Valitse Hyväksy.</span><span class="sxs-lookup"><span data-stu-id="39ad5-136">Click Approve.</span></span>
20. <span data-ttu-id="39ad5-137">Valitse Kyllä Haluatko hyväksyä myös reitin? -kentässä.</span><span class="sxs-lookup"><span data-stu-id="39ad5-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="39ad5-138">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="39ad5-138">Click OK.</span></span>
22. <span data-ttu-id="39ad5-139">Valitse toimintoruudussa Reittiversio.</span><span class="sxs-lookup"><span data-stu-id="39ad5-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="39ad5-140">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="39ad5-140">Click Activate.</span></span>
24. <span data-ttu-id="39ad5-141">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="39ad5-141">Close the page.</span></span>
25. <span data-ttu-id="39ad5-142">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="39ad5-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="39ad5-143">Valmiin tuotteen reitin luominen</span><span class="sxs-lookup"><span data-stu-id="39ad5-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="39ad5-144">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="39ad5-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="39ad5-145">Valitse nimiketunnus BOM_1.</span><span class="sxs-lookup"><span data-stu-id="39ad5-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="39ad5-146">Valitse toimintoruudussa Suunnittele.</span><span class="sxs-lookup"><span data-stu-id="39ad5-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="39ad5-147">Valitse Reitti.</span><span class="sxs-lookup"><span data-stu-id="39ad5-147">Click Route.</span></span>
4. <span data-ttu-id="39ad5-148">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="39ad5-148">Click New.</span></span>
5. <span data-ttu-id="39ad5-149">Valitse Reitti ja reittiversio.</span><span class="sxs-lookup"><span data-stu-id="39ad5-149">Click Route and route version.</span></span>
6. <span data-ttu-id="39ad5-150">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="39ad5-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="39ad5-151">Kirjoita tässä esimerkissä ROUTE_1.</span><span class="sxs-lookup"><span data-stu-id="39ad5-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="39ad5-152">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="39ad5-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="39ad5-153">Anna tai valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="39ad5-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="39ad5-154">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="39ad5-154">Click OK.</span></span>
9. <span data-ttu-id="39ad5-155">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="39ad5-155">Click New.</span></span>
10. <span data-ttu-id="39ad5-156">Anna tai valitse Toiminto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="39ad5-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="39ad5-157">Valitse tässä esimerkissä Pakkaus.</span><span class="sxs-lookup"><span data-stu-id="39ad5-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="39ad5-158">Lisää Ajoaika-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="39ad5-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="39ad5-159">Kirjoita tässä esimerkissä 1.</span><span class="sxs-lookup"><span data-stu-id="39ad5-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="39ad5-160">Anna tai valitse arvo Reititysryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="39ad5-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="39ad5-161">Valitse tässä esimerkissä Std.</span><span class="sxs-lookup"><span data-stu-id="39ad5-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="39ad5-162">Valitse Asetukset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="39ad5-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="39ad5-163">Syötä tai valitse arvo Asetusluokka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="39ad5-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="39ad5-164">Valitse tässä esimerkissä Pakkaus.</span><span class="sxs-lookup"><span data-stu-id="39ad5-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="39ad5-165">Valitse Ajat-välilehti.</span><span class="sxs-lookup"><span data-stu-id="39ad5-165">Click the Times tab.</span></span>
16. <span data-ttu-id="39ad5-166">Anna Asetusaika-kentässä luku.</span><span class="sxs-lookup"><span data-stu-id="39ad5-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="39ad5-167">Kirjoita tässä esimerkissä 1.</span><span class="sxs-lookup"><span data-stu-id="39ad5-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="39ad5-168">Valitse toimintoruudussa Reittiversio.</span><span class="sxs-lookup"><span data-stu-id="39ad5-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="39ad5-169">Valitse Hyväksy.</span><span class="sxs-lookup"><span data-stu-id="39ad5-169">Click Approve.</span></span>
19. <span data-ttu-id="39ad5-170">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="39ad5-170">Click OK.</span></span>
20. <span data-ttu-id="39ad5-171">Valitse toimintoruudussa Reittiversio.</span><span class="sxs-lookup"><span data-stu-id="39ad5-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="39ad5-172">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="39ad5-172">Click Activate.</span></span>
22. <span data-ttu-id="39ad5-173">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="39ad5-173">Close the page.</span></span>
23. <span data-ttu-id="39ad5-174">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="39ad5-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="39ad5-175">Asetusajan automaattisen kulutuksen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="39ad5-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="39ad5-176">Valitse Tuotannonhallinta > Asetukset > Reitit > Reititysryhmät.</span><span class="sxs-lookup"><span data-stu-id="39ad5-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="39ad5-177">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="39ad5-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="39ad5-178">Valitse luettelossa Std.</span><span class="sxs-lookup"><span data-stu-id="39ad5-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="39ad5-179">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="39ad5-179">Click Edit.</span></span>
4. <span data-ttu-id="39ad5-180">Valitse Asetusaika-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="39ad5-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="39ad5-181">Asetusajat sisältyvät usein nimikkeelle laskettavaan hintaan.</span><span class="sxs-lookup"><span data-stu-id="39ad5-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="39ad5-182">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="39ad5-182">Click Save.</span></span>
6. <span data-ttu-id="39ad5-183">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="39ad5-183">Close the page.</span></span>


