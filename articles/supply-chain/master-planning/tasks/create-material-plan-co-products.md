---
title: Oheistuotteiden materiaalisuunnitelman luominen
description: Tuotannon suunnittelija suunnittelee materiaalitarpeet nimikkeille, jotka ovat reseptin oheistuotteita.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e59ff769685677b0970dbc7d4c9d4d2c1e5b63d1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835955"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="8ed08-103">Oheistuotteiden materiaalisuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="8ed08-103">Create a material plan for co products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8ed08-104">Tuotannon suunnittelija suunnittelee materiaalitarpeet nimikkeille, jotka ovat reseptin oheistuotteita.</span><span class="sxs-lookup"><span data-stu-id="8ed08-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="8ed08-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USP2.</span><span class="sxs-lookup"><span data-stu-id="8ed08-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="8ed08-106">Oheistuotteen tarpeen luominen</span><span class="sxs-lookup"><span data-stu-id="8ed08-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="8ed08-107">Siirry oletuskoontinäyttöön.</span><span class="sxs-lookup"><span data-stu-id="8ed08-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="8ed08-108">Valitse Myyntitilausten käsittely ja kysely.</span><span class="sxs-lookup"><span data-stu-id="8ed08-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="8ed08-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8ed08-109">Click New.</span></span>
4. <span data-ttu-id="8ed08-110">Valitse Myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="8ed08-110">Click Sales order.</span></span>
5. <span data-ttu-id="8ed08-111">Kirjoita arvo Asiakastili-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8ed08-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="8ed08-112">Esimerkki: US-001</span><span class="sxs-lookup"><span data-stu-id="8ed08-112">Example: US-001</span></span>  
6. <span data-ttu-id="8ed08-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8ed08-113">Click OK.</span></span>
7. <span data-ttu-id="8ed08-114">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8ed08-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="8ed08-115">Esimerkki: P6003</span><span class="sxs-lookup"><span data-stu-id="8ed08-115">Example: P6003</span></span>  
8. <span data-ttu-id="8ed08-116">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8ed08-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="8ed08-117">Esimerkki: 50 000</span><span class="sxs-lookup"><span data-stu-id="8ed08-117">Example: 50000</span></span>  
9. <span data-ttu-id="8ed08-118">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8ed08-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="8ed08-119">Rinnakkaistuotteiden materiaalisuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="8ed08-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="8ed08-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8ed08-120">Close the page.</span></span>
2. <span data-ttu-id="8ed08-121">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8ed08-121">Close the page.</span></span>
3. <span data-ttu-id="8ed08-122">Valitse Pääsuunnittelu.</span><span class="sxs-lookup"><span data-stu-id="8ed08-122">Click Master planning.</span></span>
4. <span data-ttu-id="8ed08-123">Avaa haku valitsemalla Suunnitelma-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="8ed08-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="8ed08-124">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8ed08-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8ed08-125">Esimerkki: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="8ed08-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="8ed08-126">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="8ed08-126">Click Run.</span></span>
7. <span data-ttu-id="8ed08-127">Laajenna tai tiivistä Sisällytettävät tietueet -osa.</span><span class="sxs-lookup"><span data-stu-id="8ed08-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="8ed08-128">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="8ed08-128">Click Filter.</span></span>
9. <span data-ttu-id="8ed08-129">Valitse luettelosta rivi Nimiketunnus-kentälle.</span><span class="sxs-lookup"><span data-stu-id="8ed08-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="8ed08-130">Kirjoita arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8ed08-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="8ed08-131">Esimerkki: P6003</span><span class="sxs-lookup"><span data-stu-id="8ed08-131">Example: P6003</span></span>  
11. <span data-ttu-id="8ed08-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8ed08-132">Click OK.</span></span>
12. <span data-ttu-id="8ed08-133">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8ed08-133">Click OK.</span></span>
13. <span data-ttu-id="8ed08-134">Valitse Suunnitellut tilaukset.</span><span class="sxs-lookup"><span data-stu-id="8ed08-134">Click Planned orders.</span></span>
14. <span data-ttu-id="8ed08-135">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="8ed08-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="8ed08-136">Voit esimerkiksi suodattaa Nimiketunnus-kenttää arvolla P6000.</span><span class="sxs-lookup"><span data-stu-id="8ed08-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="8ed08-137">Suodata sellaisen reseptinimikkeen perusteella, jolla on sen nimikkeen oheistuote, jolle myyntitilaus luotiin.</span><span class="sxs-lookup"><span data-stu-id="8ed08-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="8ed08-138">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="8ed08-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8ed08-139">Valitse mikä tahansa suodattimen palauttamista riveistä.</span><span class="sxs-lookup"><span data-stu-id="8ed08-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="8ed08-140">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8ed08-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="8ed08-141">Laajenna tai tiivistä Tarvekohdistus-osa.</span><span class="sxs-lookup"><span data-stu-id="8ed08-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="8ed08-142">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8ed08-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8ed08-143">Suunniteltu tilaus on tarvekohdistettu oheistuotteen myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="8ed08-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="8ed08-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8ed08-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="8ed08-145">Oheistuotteen tarpeen luominen</span><span class="sxs-lookup"><span data-stu-id="8ed08-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="8ed08-146">Siirry oletuskoontinäyttöön.</span><span class="sxs-lookup"><span data-stu-id="8ed08-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="8ed08-147">Valitse Myyntitilausten käsittely ja kysely.</span><span class="sxs-lookup"><span data-stu-id="8ed08-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="8ed08-148">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8ed08-148">Click New.</span></span>
4. <span data-ttu-id="8ed08-149">Valitse Myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="8ed08-149">Click Sales order.</span></span>
5. <span data-ttu-id="8ed08-150">Kirjoita arvo Asiakastili-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8ed08-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="8ed08-151">Esimerkki: US-001</span><span class="sxs-lookup"><span data-stu-id="8ed08-151">Example: US-001</span></span>  
6. <span data-ttu-id="8ed08-152">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8ed08-152">Click OK.</span></span>
7. <span data-ttu-id="8ed08-153">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8ed08-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="8ed08-154">Esimerkki: P6003</span><span class="sxs-lookup"><span data-stu-id="8ed08-154">Example: P6003</span></span>  
8. <span data-ttu-id="8ed08-155">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8ed08-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="8ed08-156">Esimerkki: 50 000</span><span class="sxs-lookup"><span data-stu-id="8ed08-156">Example: 50000</span></span>  
9. <span data-ttu-id="8ed08-157">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8ed08-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="8ed08-158">Rinnakkaistuotteiden materiaalisuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="8ed08-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="8ed08-159">Avaa haku valitsemalla Suunnitelma-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="8ed08-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="8ed08-160">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8ed08-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8ed08-161">Esimerkki: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="8ed08-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="8ed08-162">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="8ed08-162">Click Run.</span></span>
4. <span data-ttu-id="8ed08-163">Laajenna tai tiivistä Sisällytettävät tietueet -osa.</span><span class="sxs-lookup"><span data-stu-id="8ed08-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="8ed08-164">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="8ed08-164">Click Filter.</span></span>
6. <span data-ttu-id="8ed08-165">Valitse luettelosta rivi Nimiketunnus-kentälle.</span><span class="sxs-lookup"><span data-stu-id="8ed08-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="8ed08-166">Kirjoita arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8ed08-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="8ed08-167">Esimerkki: P6003</span><span class="sxs-lookup"><span data-stu-id="8ed08-167">Example: P6003</span></span>  
8. <span data-ttu-id="8ed08-168">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8ed08-168">Click OK.</span></span>
9. <span data-ttu-id="8ed08-169">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8ed08-169">Click OK.</span></span>
10. <span data-ttu-id="8ed08-170">Valitse Suunnitellut tilaukset.</span><span class="sxs-lookup"><span data-stu-id="8ed08-170">Click Planned orders.</span></span>
11. <span data-ttu-id="8ed08-171">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="8ed08-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="8ed08-172">Voit esimerkiksi suodattaa Nimiketunnus-kenttää arvolla P6000.</span><span class="sxs-lookup"><span data-stu-id="8ed08-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="8ed08-173">Suodata sellaisen reseptinimikkeen perusteella, jolla on sen nimikkeen oheistuote, jolle myyntitilaus luotiin.</span><span class="sxs-lookup"><span data-stu-id="8ed08-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="8ed08-174">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="8ed08-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8ed08-175">Valitse mikä tahansa suodattimen palauttamista riveistä.</span><span class="sxs-lookup"><span data-stu-id="8ed08-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="8ed08-176">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8ed08-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="8ed08-177">Laajenna tai tiivistä Tarvekohdistus-osa.</span><span class="sxs-lookup"><span data-stu-id="8ed08-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="8ed08-178">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8ed08-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8ed08-179">Suunniteltu tilaus on tarvekohdistettu oheistuotteen myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="8ed08-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="8ed08-180">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8ed08-180">Close the page.</span></span>
17. <span data-ttu-id="8ed08-181">Valitse Pääsuunnittelu.</span><span class="sxs-lookup"><span data-stu-id="8ed08-181">Click Master planning.</span></span>
18. <span data-ttu-id="8ed08-182">Valitse Pääsuunnittelu > Määritys > Pääsuunnittelun parametrit.</span><span class="sxs-lookup"><span data-stu-id="8ed08-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="8ed08-183">Valitse Ei-vaihtoehto Poista käytöstä kaikki suunnitteluprosessit -kentässä.</span><span class="sxs-lookup"><span data-stu-id="8ed08-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="8ed08-184">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8ed08-184">Close the page.</span></span>

