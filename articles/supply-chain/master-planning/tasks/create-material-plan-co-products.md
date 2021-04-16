---
title: Oheistuotteiden materiaalisuunnitelman luominen
description: Tuotannon suunnittelija suunnittelee materiaalitarpeet nimikkeille, jotka ovat reseptin oheistuotteita.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d910b89330865b0bcf3f6cd05b761506f339a45f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841668"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="1aa2a-103">Oheistuotteiden materiaalisuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="1aa2a-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1aa2a-104">Tuotannon suunnittelija suunnittelee materiaalitarpeet nimikkeille, jotka ovat reseptin oheistuotteita.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="1aa2a-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USP2.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="1aa2a-106">Oheistuotteen tarpeen luominen</span><span class="sxs-lookup"><span data-stu-id="1aa2a-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="1aa2a-107">Siirry oletuskoontinäyttöön.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="1aa2a-108">Valitse Myyntitilausten käsittely ja kysely.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="1aa2a-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-109">Click New.</span></span>
4. <span data-ttu-id="1aa2a-110">Valitse Myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-110">Click Sales order.</span></span>
5. <span data-ttu-id="1aa2a-111">Kirjoita arvo Asiakastili-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="1aa2a-112">Esimerkki: US-001</span><span class="sxs-lookup"><span data-stu-id="1aa2a-112">Example: US-001</span></span>  
6. <span data-ttu-id="1aa2a-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-113">Click OK.</span></span>
7. <span data-ttu-id="1aa2a-114">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="1aa2a-115">Esimerkki: P6003</span><span class="sxs-lookup"><span data-stu-id="1aa2a-115">Example: P6003</span></span>  
8. <span data-ttu-id="1aa2a-116">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="1aa2a-117">Esimerkki: 50 000</span><span class="sxs-lookup"><span data-stu-id="1aa2a-117">Example: 50000</span></span>  
9. <span data-ttu-id="1aa2a-118">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="1aa2a-119">Rinnakkaistuotteiden materiaalisuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="1aa2a-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="1aa2a-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-120">Close the page.</span></span>
2. <span data-ttu-id="1aa2a-121">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-121">Close the page.</span></span>
3. <span data-ttu-id="1aa2a-122">Valitse Pääsuunnittelu.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-122">Click Master planning.</span></span>
4. <span data-ttu-id="1aa2a-123">Avaa haku valitsemalla Suunnitelma-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="1aa2a-124">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1aa2a-125">Esimerkki: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="1aa2a-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="1aa2a-126">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-126">Click Run.</span></span>
7. <span data-ttu-id="1aa2a-127">Laajenna tai tiivistä Sisällytettävät tietueet -osa.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="1aa2a-128">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-128">Click Filter.</span></span>
9. <span data-ttu-id="1aa2a-129">Valitse luettelosta rivi Nimiketunnus-kentälle.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="1aa2a-130">Kirjoita arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="1aa2a-131">Esimerkki: P6003</span><span class="sxs-lookup"><span data-stu-id="1aa2a-131">Example: P6003</span></span>  
11. <span data-ttu-id="1aa2a-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-132">Click OK.</span></span>
12. <span data-ttu-id="1aa2a-133">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-133">Click OK.</span></span>
13. <span data-ttu-id="1aa2a-134">Valitse Suunnitellut tilaukset.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-134">Click Planned orders.</span></span>
14. <span data-ttu-id="1aa2a-135">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1aa2a-136">Voit esimerkiksi suodattaa Nimiketunnus-kenttää arvolla P6000.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="1aa2a-137">Suodata sellaisen reseptinimikkeen perusteella, jolla on sen nimikkeen oheistuote, jolle myyntitilaus luotiin.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="1aa2a-138">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1aa2a-139">Valitse mikä tahansa suodattimen palauttamista riveistä.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="1aa2a-140">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="1aa2a-141">Laajenna tai tiivistä Tarvekohdistus-osa.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="1aa2a-142">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1aa2a-143">Suunniteltu tilaus on tarvekohdistettu oheistuotteen myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="1aa2a-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="1aa2a-145">Oheistuotteen tarpeen luominen</span><span class="sxs-lookup"><span data-stu-id="1aa2a-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="1aa2a-146">Siirry oletuskoontinäyttöön.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="1aa2a-147">Valitse Myyntitilausten käsittely ja kysely.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="1aa2a-148">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-148">Click New.</span></span>
4. <span data-ttu-id="1aa2a-149">Valitse Myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-149">Click Sales order.</span></span>
5. <span data-ttu-id="1aa2a-150">Kirjoita arvo Asiakastili-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="1aa2a-151">Esimerkki: US-001</span><span class="sxs-lookup"><span data-stu-id="1aa2a-151">Example: US-001</span></span>  
6. <span data-ttu-id="1aa2a-152">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-152">Click OK.</span></span>
7. <span data-ttu-id="1aa2a-153">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="1aa2a-154">Esimerkki: P6003</span><span class="sxs-lookup"><span data-stu-id="1aa2a-154">Example: P6003</span></span>  
8. <span data-ttu-id="1aa2a-155">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="1aa2a-156">Esimerkki: 50 000</span><span class="sxs-lookup"><span data-stu-id="1aa2a-156">Example: 50000</span></span>  
9. <span data-ttu-id="1aa2a-157">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="1aa2a-158">Rinnakkaistuotteiden materiaalisuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="1aa2a-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="1aa2a-159">Avaa haku valitsemalla Suunnitelma-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="1aa2a-160">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1aa2a-161">Esimerkki: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="1aa2a-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="1aa2a-162">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-162">Click Run.</span></span>
4. <span data-ttu-id="1aa2a-163">Laajenna tai tiivistä Sisällytettävät tietueet -osa.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="1aa2a-164">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-164">Click Filter.</span></span>
6. <span data-ttu-id="1aa2a-165">Valitse luettelosta rivi Nimiketunnus-kentälle.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="1aa2a-166">Kirjoita arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="1aa2a-167">Esimerkki: P6003</span><span class="sxs-lookup"><span data-stu-id="1aa2a-167">Example: P6003</span></span>  
8. <span data-ttu-id="1aa2a-168">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-168">Click OK.</span></span>
9. <span data-ttu-id="1aa2a-169">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-169">Click OK.</span></span>
10. <span data-ttu-id="1aa2a-170">Valitse Suunnitellut tilaukset.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-170">Click Planned orders.</span></span>
11. <span data-ttu-id="1aa2a-171">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1aa2a-172">Voit esimerkiksi suodattaa Nimiketunnus-kenttää arvolla P6000.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="1aa2a-173">Suodata sellaisen reseptinimikkeen perusteella, jolla on sen nimikkeen oheistuote, jolle myyntitilaus luotiin.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="1aa2a-174">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1aa2a-175">Valitse mikä tahansa suodattimen palauttamista riveistä.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="1aa2a-176">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="1aa2a-177">Laajenna tai tiivistä Tarvekohdistus-osa.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="1aa2a-178">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1aa2a-179">Suunniteltu tilaus on tarvekohdistettu oheistuotteen myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="1aa2a-180">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-180">Close the page.</span></span>
17. <span data-ttu-id="1aa2a-181">Valitse Pääsuunnittelu.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-181">Click Master planning.</span></span>
18. <span data-ttu-id="1aa2a-182">Valitse Pääsuunnittelu > Määritys > Pääsuunnittelun parametrit.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="1aa2a-183">Valitse Ei-vaihtoehto Poista käytöstä kaikki suunnitteluprosessit -kentässä.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="1aa2a-184">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1aa2a-184">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]