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
ms.openlocfilehash: b51e4b4d00da2babb5128d8c4c22139b0c1853d4
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920726"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="18f80-103">Oheistuotteiden materiaalisuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="18f80-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="18f80-104">Tuotannon suunnittelija suunnittelee materiaalitarpeet nimikkeille, jotka ovat reseptin oheistuotteita.</span><span class="sxs-lookup"><span data-stu-id="18f80-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="18f80-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USP2.</span><span class="sxs-lookup"><span data-stu-id="18f80-105">The demo data company used to create this procedure is USP2.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="18f80-106">Oheistuotteen tarpeen luominen</span><span class="sxs-lookup"><span data-stu-id="18f80-106">Create requirement for a co-product</span></span>

1. <span data-ttu-id="18f80-107">Valitse **Myynti ja markkinointi \> Työtilat \> Myyntitilausten käsittely ja kysely**.</span><span class="sxs-lookup"><span data-stu-id="18f80-107">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="18f80-108">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="18f80-108">Select **New**.</span></span>
1. <span data-ttu-id="18f80-109">Valitse **Myyntitilaus**.</span><span class="sxs-lookup"><span data-stu-id="18f80-109">Select **Sales order**.</span></span>
1. <span data-ttu-id="18f80-110">Kirjoita arvo **Asiakastili**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="18f80-110">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="18f80-111">Esimerkki: US-001</span><span class="sxs-lookup"><span data-stu-id="18f80-111">Example: US-001</span></span>  
1. <span data-ttu-id="18f80-112">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="18f80-112">Select **OK**.</span></span>
1. <span data-ttu-id="18f80-113">Kirjoita arvo **Nimiketunnus**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="18f80-113">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="18f80-114">Esimerkki: P6003</span><span class="sxs-lookup"><span data-stu-id="18f80-114">Example: P6003</span></span>  
1. <span data-ttu-id="18f80-115">Anna **Määrä**-kentässä numero.</span><span class="sxs-lookup"><span data-stu-id="18f80-115">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="18f80-116">Esimerkki: 50 000</span><span class="sxs-lookup"><span data-stu-id="18f80-116">Example: 50000</span></span>  
1. <span data-ttu-id="18f80-117">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="18f80-117">Select **Save**.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="18f80-118">Rinnakkaistuotteiden materiaalisuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="18f80-118">Create a material plan for co-products</span></span>

1. <span data-ttu-id="18f80-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="18f80-119">Close the page.</span></span>
1. <span data-ttu-id="18f80-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="18f80-120">Close the page.</span></span>
1. <span data-ttu-id="18f80-121">Valitse **Pääsuunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="18f80-121">Select **Master planning**.</span></span>
1. <span data-ttu-id="18f80-122">Avaa haku valitsemalla **Suunnitelma**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="18f80-122">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
1. <span data-ttu-id="18f80-123">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="18f80-123">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="18f80-124">Esimerkki: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="18f80-124">Example: MasterPlan</span></span>  
1. <span data-ttu-id="18f80-125">Valitse **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="18f80-125">Select **Run**.</span></span>
1. <span data-ttu-id="18f80-126">Laajenna tai tiivistä **Sisällytettävät tietueet** -osa.</span><span class="sxs-lookup"><span data-stu-id="18f80-126">Expand or collapse the **Records to include** section.</span></span>
1. <span data-ttu-id="18f80-127">Valitse **Suodata**.</span><span class="sxs-lookup"><span data-stu-id="18f80-127">Select **Filter**.</span></span>
1. <span data-ttu-id="18f80-128">Valitse luettelosta rivi kohdalle **Kenttä** = *Nimiketunnus*.</span><span class="sxs-lookup"><span data-stu-id="18f80-128">In the list, select the row for **Field** = *Item number*.</span></span>
1. <span data-ttu-id="18f80-129">Kirjoita arvo **Ehdot**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="18f80-129">In the **Criteria** field, type a value.</span></span>
    * <span data-ttu-id="18f80-130">Esimerkki: P6003</span><span class="sxs-lookup"><span data-stu-id="18f80-130">Example: P6003</span></span>  
1. <span data-ttu-id="18f80-131">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="18f80-131">Select **OK**.</span></span>
1. <span data-ttu-id="18f80-132">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="18f80-132">Select **OK**.</span></span>
1. <span data-ttu-id="18f80-133">Valitse **Suunnitellut tilaukset**.</span><span class="sxs-lookup"><span data-stu-id="18f80-133">Select **Planned orders**.</span></span>
1. <span data-ttu-id="18f80-134">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="18f80-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="18f80-135">Voit esimerkiksi suodattaa **Nimiketunnus**-kenttää arvolla P6000.</span><span class="sxs-lookup"><span data-stu-id="18f80-135">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="18f80-136">Suodata sellaisen reseptinimikkeen perusteella, jolla on sen nimikkeen oheistuote, jolle myyntitilaus luotiin.</span><span class="sxs-lookup"><span data-stu-id="18f80-136">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
1. <span data-ttu-id="18f80-137">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="18f80-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="18f80-138">Valitse mikä tahansa suodattimen palauttamista riveistä.</span><span class="sxs-lookup"><span data-stu-id="18f80-138">Select any of the rows returned by the filter.</span></span>  
1. <span data-ttu-id="18f80-139">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="18f80-139">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="18f80-140">Laajenna **Tarvekohdistus**-osa.</span><span class="sxs-lookup"><span data-stu-id="18f80-140">Expand the **Pegging** section.</span></span>
1. <span data-ttu-id="18f80-141">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="18f80-141">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="18f80-142">Suunniteltu tilaus on tarvekohdistettu oheistuotteen myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="18f80-142">The planned order is pegged to the sales order for the co-product.</span></span>  
1. <span data-ttu-id="18f80-143">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="18f80-143">Close the page.</span></span>

## <a name="create-a-second-requirement-for-a-co-product"></a><span data-ttu-id="18f80-144">Oheistuotteen toisen tarpeen luominen</span><span class="sxs-lookup"><span data-stu-id="18f80-144">Create a second requirement for a co-product</span></span>

1. <span data-ttu-id="18f80-145">Valitse **Myynti ja markkinointi \> Työtilat \> Myyntitilausten käsittely ja kysely**.</span><span class="sxs-lookup"><span data-stu-id="18f80-145">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="18f80-146">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="18f80-146">Select **New**.</span></span>
1. <span data-ttu-id="18f80-147">Valitse **Myyntitilaus**.</span><span class="sxs-lookup"><span data-stu-id="18f80-147">Select **Sales order**.</span></span>
1. <span data-ttu-id="18f80-148">Kirjoita arvo **Asiakastili**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="18f80-148">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="18f80-149">Esimerkki: US-001</span><span class="sxs-lookup"><span data-stu-id="18f80-149">Example: US-001</span></span>  
1. <span data-ttu-id="18f80-150">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="18f80-150">Select **OK**.</span></span>
1. <span data-ttu-id="18f80-151">Kirjoita arvo **Nimiketunnus**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="18f80-151">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="18f80-152">Esimerkki: P6003</span><span class="sxs-lookup"><span data-stu-id="18f80-152">Example: P6003</span></span>  
1. <span data-ttu-id="18f80-153">Anna **Määrä**-kentässä numero.</span><span class="sxs-lookup"><span data-stu-id="18f80-153">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="18f80-154">Esimerkki: 50 000</span><span class="sxs-lookup"><span data-stu-id="18f80-154">Example: 50000</span></span>  
1. <span data-ttu-id="18f80-155">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="18f80-155">Select **Save**.</span></span>

## <a name="create-a-second-material-plan-for-co-products"></a><span data-ttu-id="18f80-156">Rinnakkaistuotteiden toisen materiaalisuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="18f80-156">Create a second material plan for co-products</span></span>

1. <span data-ttu-id="18f80-157">Avaa haku valitsemalla **Suunnitelma**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="18f80-157">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="18f80-158">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="18f80-158">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="18f80-159">Esimerkki: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="18f80-159">Example: MasterPlan</span></span>  
3. <span data-ttu-id="18f80-160">Valitse **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="18f80-160">Select **Run**.</span></span>
4. <span data-ttu-id="18f80-161">Laajenna tai tiivistä **Sisällytettävät tietueet** -osa.</span><span class="sxs-lookup"><span data-stu-id="18f80-161">Expand or collapse the **Records to include** section.</span></span>
5. <span data-ttu-id="18f80-162">Valitse **Suodata**.</span><span class="sxs-lookup"><span data-stu-id="18f80-162">Select **Filter**.</span></span>
6. <span data-ttu-id="18f80-163">Valitse luettelosta rivi kohdalle **Kenttä** = *Nimiketunnus*.</span><span class="sxs-lookup"><span data-stu-id="18f80-163">In the list, select the row for **Field** = *Item number*.</span></span>
7. <span data-ttu-id="18f80-164">Kirjoita arvo *Ehdot*-kenttään.</span><span class="sxs-lookup"><span data-stu-id="18f80-164">In the *Criteria* field, type a value.</span></span>
    * <span data-ttu-id="18f80-165">Esimerkki: P6003</span><span class="sxs-lookup"><span data-stu-id="18f80-165">Example: P6003</span></span>  
8. <span data-ttu-id="18f80-166">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="18f80-166">Select **OK**.</span></span>
9. <span data-ttu-id="18f80-167">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="18f80-167">Select **OK**.</span></span>
10. <span data-ttu-id="18f80-168">Valitse **Suunnitellut tilaukset**.</span><span class="sxs-lookup"><span data-stu-id="18f80-168">Select **Planned orders**.</span></span>
11. <span data-ttu-id="18f80-169">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="18f80-169">Use the Quick Filter to find records.</span></span> <span data-ttu-id="18f80-170">Voit esimerkiksi suodattaa **Nimiketunnus**-kenttää arvolla P6000.</span><span class="sxs-lookup"><span data-stu-id="18f80-170">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="18f80-171">Suodata sellaisen reseptinimikkeen perusteella, jolla on sen nimikkeen oheistuote, jolle myyntitilaus luotiin.</span><span class="sxs-lookup"><span data-stu-id="18f80-171">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="18f80-172">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="18f80-172">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="18f80-173">Valitse mikä tahansa suodattimen palauttamista riveistä.</span><span class="sxs-lookup"><span data-stu-id="18f80-173">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="18f80-174">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="18f80-174">In the list, select the link in the selected row.</span></span>
14. <span data-ttu-id="18f80-175">Laajenna tai tiivistä **Tarvekohdistus**-osa.</span><span class="sxs-lookup"><span data-stu-id="18f80-175">Expand or collapse the **Pegging** section.</span></span>
15. <span data-ttu-id="18f80-176">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="18f80-176">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="18f80-177">Suunniteltu tilaus on tarvekohdistettu oheistuotteen myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="18f80-177">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="18f80-178">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="18f80-178">Close the page.</span></span>
17. <span data-ttu-id="18f80-179">Valitse **Pääsuunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="18f80-179">Select **Master planning**.</span></span>
18. <span data-ttu-id="18f80-180">Valitse **Pääsuunnittelu \> Määritys \> Pääsuunnittelun parametrit**.</span><span class="sxs-lookup"><span data-stu-id="18f80-180">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
19. <span data-ttu-id="18f80-181">Valitse *Ei*-vaihtoehto **Poista käytöstä kaikki suunnitteluprosessit** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="18f80-181">Select *No* in the **Disable all planning processes** field.</span></span>
20. <span data-ttu-id="18f80-182">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="18f80-182">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]