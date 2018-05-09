--- 
title: "Lean-valmistuksen siirtotehtävien luominen"
description: "Luo Lean-valmistuksen siirtotehtävä."
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 11e37d5a2da33d14d691fa8408aac443fb7a6dfa
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="create-transfer-activities-for-lean-manufacturing"></a><span data-ttu-id="c88c8-103">Lean-valmistuksen siirtotehtävien luominen</span><span class="sxs-lookup"><span data-stu-id="c88c8-103">Create transfer activities for lean manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c88c8-104">Luo Lean-valmistuksen siirtotehtävä.</span><span class="sxs-lookup"><span data-stu-id="c88c8-104">Create a transfer activity for lean manufacturing.</span></span> 

<span data-ttu-id="c88c8-105">Edellytykset:</span><span class="sxs-lookup"><span data-stu-id="c88c8-105">Prerequisites:</span></span> 

1. <span data-ttu-id="c88c8-106">On välttämätöntä luoda tuotantovirta ja versio, jotka eivät ole aktiivisia.</span><span class="sxs-lookup"><span data-stu-id="c88c8-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="c88c8-107">Lähtö- ja kohdevarasto ja sijainnit on luotava.</span><span class="sxs-lookup"><span data-stu-id="c88c8-107">The from and to warehouse and locations must be created.</span></span> <span data-ttu-id="c88c8-108">Työsolun täydentäminen tai täydennetyn työsolun luominen on valinnaista.</span><span class="sxs-lookup"><span data-stu-id="c88c8-108">Optionally, the replenishing or the replenished work cell should be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="c88c8-109">Etsi tuotantovirran versio</span><span class="sxs-lookup"><span data-stu-id="c88c8-109">Find the production flow version</span></span>
1. <span data-ttu-id="c88c8-110">Valitse Tuotannonhallinta > Asetukset > Lean-tuotantovirta > Tuotantovirrat.</span><span class="sxs-lookup"><span data-stu-id="c88c8-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="c88c8-111">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="c88c8-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c88c8-112">Huomaa, että tuotantovirran version on oltava luonnostilassa.</span><span class="sxs-lookup"><span data-stu-id="c88c8-112">Note that the production flow must have a version in draft status.</span></span>  
3. <span data-ttu-id="c88c8-113">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="c88c8-113">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="c88c8-114">Luo uusi tehtävä</span><span class="sxs-lookup"><span data-stu-id="c88c8-114">Create a new activity</span></span>
1. <span data-ttu-id="c88c8-115">Valitse Tehtävät.</span><span class="sxs-lookup"><span data-stu-id="c88c8-115">Click Activities.</span></span>
    * <span data-ttu-id="c88c8-116">Varmista, että valitulla tuotantovirralla on luonnostilassa oleva versio ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="c88c8-116">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="c88c8-117">Valitse Luo uusi suunnitelman tehtävä.</span><span class="sxs-lookup"><span data-stu-id="c88c8-117">Click Create new plan activity.</span></span>
3. <span data-ttu-id="c88c8-118">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="c88c8-118">Click Next.</span></span>
4. <span data-ttu-id="c88c8-119">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c88c8-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c88c8-120">Valitse Tehtävätyyppi-kentässä Siirto.</span><span class="sxs-lookup"><span data-stu-id="c88c8-120">In the Activity type field, select 'Transfer'.</span></span>
6. <span data-ttu-id="c88c8-121">Lisää Prosessin määrä -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c88c8-121">In the Process quantity field, enter a number.</span></span>
7. <span data-ttu-id="c88c8-122">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="c88c8-122">Click Next.</span></span>

## <a name="select-the-work-cells"></a><span data-ttu-id="c88c8-123">Valitse Työsolut</span><span class="sxs-lookup"><span data-stu-id="c88c8-123">Select the Work cells</span></span>
1. <span data-ttu-id="c88c8-124">Avaa haku napsauttamalla Täydennetään-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="c88c8-124">In the Replenishing field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c88c8-125">Valitse työsolu, jos haluat käyttää työsolun tuotossijaintia siirtotehtävän lähtösijaintina.</span><span class="sxs-lookup"><span data-stu-id="c88c8-125">To use the work cell output location as the from location in the transfer activity, select a work cell.</span></span> <span data-ttu-id="c88c8-126">Sama voidaan tehdä täydennetyllä työsolulla, joka määrittää siirtotehtävän kohdesijainnin.</span><span class="sxs-lookup"><span data-stu-id="c88c8-126">The same can be done with the replenished work cell, which sets the target location of the transfer activity.</span></span>  
2. <span data-ttu-id="c88c8-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="c88c8-127">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="c88c8-128">Määritä varastopäivitykset</span><span class="sxs-lookup"><span data-stu-id="c88c8-128">Define the inventory updates</span></span>
1. <span data-ttu-id="c88c8-129">Valitse vaihtoehto Tuotetyyppi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="c88c8-129">In the Product type field, select an option.</span></span>
    * <span data-ttu-id="c88c8-130">Huomaa, että siirto ei vaihda tuotteen tyyppiä.</span><span class="sxs-lookup"><span data-stu-id="c88c8-130">Note that a transfer does not change the type of product.</span></span> <span data-ttu-id="c88c8-131">Voit siirtää valmiita tai puolivalmiita tuotteita (kahden tuotantovirran tehtävän ja mahdollisen kanban-työnkulun välisen siirto).</span><span class="sxs-lookup"><span data-stu-id="c88c8-131">You can transfer finished products or semi-finished products (transfer between two activities of a production flow and possibly a kanban flow).</span></span>     <span data-ttu-id="c88c8-132">Voit valita valmiita tuotteita siirrettäessä, jos tulosten kerääminen tai vastaanottaminen on varastotapahtuma.</span><span class="sxs-lookup"><span data-stu-id="c88c8-132">When transferring finished products, you can select if picking or receiving results in an inventory transaction.</span></span>  

## <a name="define-the-transfer-locations"></a><span data-ttu-id="c88c8-133">Määritä siirtosijainnit</span><span class="sxs-lookup"><span data-stu-id="c88c8-133">Define the transfer locations</span></span>
1. <span data-ttu-id="c88c8-134">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="c88c8-134">Click Next.</span></span>
2. <span data-ttu-id="c88c8-135">Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="c88c8-135">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="c88c8-136">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="c88c8-136">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="c88c8-137">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="c88c8-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c88c8-138">Avaa haku valitsemalla Sijainnit-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="c88c8-138">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="c88c8-139">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="c88c8-139">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="c88c8-140">Valitse Rahdinkuljettaja-kentässä Huolitsija.</span><span class="sxs-lookup"><span data-stu-id="c88c8-140">In the Freighted by field, select 'Shipper'.</span></span>
    * <span data-ttu-id="c88c8-141">Vaihtoehdot: Huolitsija – lähetysvarastoa käyttävä organisaatio, Vastaanottaja – vastaanottovarastoa käyttävä organisaatio ja Rahdinkuljettaja – ulkopuolinen toimittaja.</span><span class="sxs-lookup"><span data-stu-id="c88c8-141">Options include: Shipper - the organization operating the shipping warehouse, Recipient -  the organization operating the receiving warehouse, Carrier - a third party vendor.</span></span> <span data-ttu-id="c88c8-142">Jos käyttävä organisaatio on toimittaja, siirtotehtävä edellyttää alihankintasopimuksen.</span><span class="sxs-lookup"><span data-stu-id="c88c8-142">If the operating organization is a vendor, the transfer activity requires a subcontracting agreement.</span></span>  
8. <span data-ttu-id="c88c8-143">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="c88c8-143">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="c88c8-144">Määritä tehtäväajat</span><span class="sxs-lookup"><span data-stu-id="c88c8-144">Define the activity times</span></span>
1. <span data-ttu-id="c88c8-145">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="c88c8-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c88c8-146">Suorituksenaikainen kohde on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="c88c8-146">The definition of a Runtime is required.</span></span> <span data-ttu-id="c88c8-147">Suorituksenaikaisella kohteella lasketaan kanban-töiden kustannukset ja läpimenoajat.</span><span class="sxs-lookup"><span data-stu-id="c88c8-147">The Runtime is used to calculate cost and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="c88c8-148">Suorituksenaikaisia kohteita ei käytetä kapasiteetin kuormituksen ja kulutuksen laskentaan, sillä ne lasketaan tuotantovirran versiotehtävästä johdetusta syklin kestosta.</span><span class="sxs-lookup"><span data-stu-id="c88c8-148">Runtimes are not used to calculate capacity load and consumption, which is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="c88c8-149">Lisää Aika-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c88c8-149">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="c88c8-150">Kirjoita arvo Yksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c88c8-150">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="c88c8-151">Valitse Aikayksikkö.</span><span class="sxs-lookup"><span data-stu-id="c88c8-151">Select the Time unit.</span></span>
5. <span data-ttu-id="c88c8-152">Lisää Määrää kohden -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c88c8-152">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="c88c8-153">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="c88c8-153">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c88c8-154">Jonotusajat ovat valinnaisia</span><span class="sxs-lookup"><span data-stu-id="c88c8-154">Queue times are optional.</span></span>  
7. <span data-ttu-id="c88c8-155">Lisää Aika-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c88c8-155">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="c88c8-156">Kirjoita arvo Yksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c88c8-156">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="c88c8-157">Valitse Aikayksikkö.</span><span class="sxs-lookup"><span data-stu-id="c88c8-157">Select the Time unit.</span></span>
10. <span data-ttu-id="c88c8-158">Lisää Määrää kohden -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c88c8-158">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="c88c8-159">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="c88c8-159">Click Next.</span></span>
12. <span data-ttu-id="c88c8-160">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="c88c8-160">Click Finish.</span></span>
13. <span data-ttu-id="c88c8-161">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c88c8-161">Close the page.</span></span>


