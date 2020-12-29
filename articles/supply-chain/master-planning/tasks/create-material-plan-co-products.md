---
title: Oheistuotteiden materiaalisuunnitelman luominen
description: Tuotannon suunnittelija suunnittelee materiaalitarpeet nimikkeille, jotka ovat reseptin oheistuotteita.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14de9a1085ac1cae88ad93c35385dd43c60ed4d1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427093"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="b23ea-103">Oheistuotteiden materiaalisuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="b23ea-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b23ea-104">Tuotannon suunnittelija suunnittelee materiaalitarpeet nimikkeille, jotka ovat reseptin oheistuotteita.</span><span class="sxs-lookup"><span data-stu-id="b23ea-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="b23ea-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USP2.</span><span class="sxs-lookup"><span data-stu-id="b23ea-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="b23ea-106">Oheistuotteen tarpeen luominen</span><span class="sxs-lookup"><span data-stu-id="b23ea-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="b23ea-107">Siirry oletuskoontinäyttöön.</span><span class="sxs-lookup"><span data-stu-id="b23ea-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="b23ea-108">Valitse Myyntitilausten käsittely ja kysely.</span><span class="sxs-lookup"><span data-stu-id="b23ea-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="b23ea-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b23ea-109">Click New.</span></span>
4. <span data-ttu-id="b23ea-110">Valitse Myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="b23ea-110">Click Sales order.</span></span>
5. <span data-ttu-id="b23ea-111">Kirjoita arvo Asiakastili-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b23ea-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="b23ea-112">Esimerkki: US-001</span><span class="sxs-lookup"><span data-stu-id="b23ea-112">Example: US-001</span></span>  
6. <span data-ttu-id="b23ea-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="b23ea-113">Click OK.</span></span>
7. <span data-ttu-id="b23ea-114">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b23ea-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="b23ea-115">Esimerkki: P6003</span><span class="sxs-lookup"><span data-stu-id="b23ea-115">Example: P6003</span></span>  
8. <span data-ttu-id="b23ea-116">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b23ea-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="b23ea-117">Esimerkki: 50 000</span><span class="sxs-lookup"><span data-stu-id="b23ea-117">Example: 50000</span></span>  
9. <span data-ttu-id="b23ea-118">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="b23ea-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="b23ea-119">Rinnakkaistuotteiden materiaalisuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="b23ea-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="b23ea-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b23ea-120">Close the page.</span></span>
2. <span data-ttu-id="b23ea-121">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b23ea-121">Close the page.</span></span>
3. <span data-ttu-id="b23ea-122">Valitse Pääsuunnittelu.</span><span class="sxs-lookup"><span data-stu-id="b23ea-122">Click Master planning.</span></span>
4. <span data-ttu-id="b23ea-123">Avaa haku valitsemalla Suunnitelma-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="b23ea-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b23ea-124">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="b23ea-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b23ea-125">Esimerkki: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="b23ea-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="b23ea-126">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="b23ea-126">Click Run.</span></span>
7. <span data-ttu-id="b23ea-127">Laajenna tai tiivistä Sisällytettävät tietueet -osa.</span><span class="sxs-lookup"><span data-stu-id="b23ea-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="b23ea-128">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="b23ea-128">Click Filter.</span></span>
9. <span data-ttu-id="b23ea-129">Valitse luettelosta rivi Nimiketunnus-kentälle.</span><span class="sxs-lookup"><span data-stu-id="b23ea-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="b23ea-130">Kirjoita arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b23ea-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="b23ea-131">Esimerkki: P6003</span><span class="sxs-lookup"><span data-stu-id="b23ea-131">Example: P6003</span></span>  
11. <span data-ttu-id="b23ea-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="b23ea-132">Click OK.</span></span>
12. <span data-ttu-id="b23ea-133">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="b23ea-133">Click OK.</span></span>
13. <span data-ttu-id="b23ea-134">Valitse Suunnitellut tilaukset.</span><span class="sxs-lookup"><span data-stu-id="b23ea-134">Click Planned orders.</span></span>
14. <span data-ttu-id="b23ea-135">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="b23ea-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b23ea-136">Voit esimerkiksi suodattaa Nimiketunnus-kenttää arvolla P6000.</span><span class="sxs-lookup"><span data-stu-id="b23ea-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="b23ea-137">Suodata sellaisen reseptinimikkeen perusteella, jolla on sen nimikkeen oheistuote, jolle myyntitilaus luotiin.</span><span class="sxs-lookup"><span data-stu-id="b23ea-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="b23ea-138">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b23ea-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b23ea-139">Valitse mikä tahansa suodattimen palauttamista riveistä.</span><span class="sxs-lookup"><span data-stu-id="b23ea-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="b23ea-140">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="b23ea-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="b23ea-141">Laajenna tai tiivistä Tarvekohdistus-osa.</span><span class="sxs-lookup"><span data-stu-id="b23ea-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="b23ea-142">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="b23ea-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b23ea-143">Suunniteltu tilaus on tarvekohdistettu oheistuotteen myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="b23ea-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="b23ea-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b23ea-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="b23ea-145">Oheistuotteen tarpeen luominen</span><span class="sxs-lookup"><span data-stu-id="b23ea-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="b23ea-146">Siirry oletuskoontinäyttöön.</span><span class="sxs-lookup"><span data-stu-id="b23ea-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="b23ea-147">Valitse Myyntitilausten käsittely ja kysely.</span><span class="sxs-lookup"><span data-stu-id="b23ea-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="b23ea-148">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b23ea-148">Click New.</span></span>
4. <span data-ttu-id="b23ea-149">Valitse Myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="b23ea-149">Click Sales order.</span></span>
5. <span data-ttu-id="b23ea-150">Kirjoita arvo Asiakastili-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b23ea-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="b23ea-151">Esimerkki: US-001</span><span class="sxs-lookup"><span data-stu-id="b23ea-151">Example: US-001</span></span>  
6. <span data-ttu-id="b23ea-152">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="b23ea-152">Click OK.</span></span>
7. <span data-ttu-id="b23ea-153">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b23ea-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="b23ea-154">Esimerkki: P6003</span><span class="sxs-lookup"><span data-stu-id="b23ea-154">Example: P6003</span></span>  
8. <span data-ttu-id="b23ea-155">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b23ea-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="b23ea-156">Esimerkki: 50 000</span><span class="sxs-lookup"><span data-stu-id="b23ea-156">Example: 50000</span></span>  
9. <span data-ttu-id="b23ea-157">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="b23ea-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="b23ea-158">Rinnakkaistuotteiden materiaalisuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="b23ea-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="b23ea-159">Avaa haku valitsemalla Suunnitelma-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="b23ea-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="b23ea-160">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="b23ea-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b23ea-161">Esimerkki: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="b23ea-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="b23ea-162">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="b23ea-162">Click Run.</span></span>
4. <span data-ttu-id="b23ea-163">Laajenna tai tiivistä Sisällytettävät tietueet -osa.</span><span class="sxs-lookup"><span data-stu-id="b23ea-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="b23ea-164">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="b23ea-164">Click Filter.</span></span>
6. <span data-ttu-id="b23ea-165">Valitse luettelosta rivi Nimiketunnus-kentälle.</span><span class="sxs-lookup"><span data-stu-id="b23ea-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="b23ea-166">Kirjoita arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b23ea-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="b23ea-167">Esimerkki: P6003</span><span class="sxs-lookup"><span data-stu-id="b23ea-167">Example: P6003</span></span>  
8. <span data-ttu-id="b23ea-168">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="b23ea-168">Click OK.</span></span>
9. <span data-ttu-id="b23ea-169">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="b23ea-169">Click OK.</span></span>
10. <span data-ttu-id="b23ea-170">Valitse Suunnitellut tilaukset.</span><span class="sxs-lookup"><span data-stu-id="b23ea-170">Click Planned orders.</span></span>
11. <span data-ttu-id="b23ea-171">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="b23ea-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b23ea-172">Voit esimerkiksi suodattaa Nimiketunnus-kenttää arvolla P6000.</span><span class="sxs-lookup"><span data-stu-id="b23ea-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="b23ea-173">Suodata sellaisen reseptinimikkeen perusteella, jolla on sen nimikkeen oheistuote, jolle myyntitilaus luotiin.</span><span class="sxs-lookup"><span data-stu-id="b23ea-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="b23ea-174">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b23ea-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b23ea-175">Valitse mikä tahansa suodattimen palauttamista riveistä.</span><span class="sxs-lookup"><span data-stu-id="b23ea-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="b23ea-176">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="b23ea-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="b23ea-177">Laajenna tai tiivistä Tarvekohdistus-osa.</span><span class="sxs-lookup"><span data-stu-id="b23ea-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="b23ea-178">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="b23ea-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b23ea-179">Suunniteltu tilaus on tarvekohdistettu oheistuotteen myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="b23ea-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="b23ea-180">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b23ea-180">Close the page.</span></span>
17. <span data-ttu-id="b23ea-181">Valitse Pääsuunnittelu.</span><span class="sxs-lookup"><span data-stu-id="b23ea-181">Click Master planning.</span></span>
18. <span data-ttu-id="b23ea-182">Valitse Pääsuunnittelu > Määritys > Pääsuunnittelun parametrit.</span><span class="sxs-lookup"><span data-stu-id="b23ea-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="b23ea-183">Valitse Ei-vaihtoehto Poista käytöstä kaikki suunnitteluprosessit -kentässä.</span><span class="sxs-lookup"><span data-stu-id="b23ea-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="b23ea-184">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b23ea-184">Close the page.</span></span>

