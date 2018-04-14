--- 
title: "Lean-valmistuksen prosessitehtävien luominen"
description: "Luo Lean-valmistuksen prosessitehtävä."
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 977856385cd6170e141884320b8f8c7226d206cf
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="create-process-activities-for-lean-manufacturing"></a><span data-ttu-id="2a3ef-103">Lean-valmistuksen prosessitehtävien luominen</span><span class="sxs-lookup"><span data-stu-id="2a3ef-103">Create process activities for lean manufacturing</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2a3ef-104">Luo Lean-valmistuksen prosessitehtävä.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-104">Create a process activity for lean manufacturing.</span></span> 

<span data-ttu-id="2a3ef-105">Edellytykset:</span><span class="sxs-lookup"><span data-stu-id="2a3ef-105">Prerequisites:</span></span> 

1. <span data-ttu-id="2a3ef-106">On välttämätöntä luoda tuotantovirta ja versio, jotka eivät ole aktiivisia.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="2a3ef-107">Työsolu on luotava.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-107">A work cell must be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="2a3ef-108">Etsi tuotantovirran versio</span><span class="sxs-lookup"><span data-stu-id="2a3ef-108">Find the production flow version</span></span>
1. <span data-ttu-id="2a3ef-109">Valitse Tuotannonhallinta > Asetukset > Lean-tuotantovirta > Tuotantovirrat.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="2a3ef-110">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2a3ef-111">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-111">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="2a3ef-112">Luo uusi tehtävä</span><span class="sxs-lookup"><span data-stu-id="2a3ef-112">Create a new activity</span></span>
1. <span data-ttu-id="2a3ef-113">Valitse Tehtävät.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-113">Click Activities.</span></span>
    * <span data-ttu-id="2a3ef-114">Varmista, että valitulla tuotantovirralla on luonnostilassa oleva versio ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-114">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="2a3ef-115">Valitse Luo uusi suunnitelman tehtävä.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-115">Click Create new plan activity.</span></span>
3. <span data-ttu-id="2a3ef-116">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-116">Click Next.</span></span>
4. <span data-ttu-id="2a3ef-117">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="2a3ef-118">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="2a3ef-119">Huomaa, että tietyn tuotantovirran kaikilla versioilla on oltava yksilöllinen nimi.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-119">Note that the name must be unique for a given production flow for all versions.</span></span>  
6. <span data-ttu-id="2a3ef-120">Lisää Prosessin määrä -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-120">In the Process quantity field, enter a number.</span></span>
    * <span data-ttu-id="2a3ef-121">Huomaa, että käsiteltävästä työmäärästä riippumatta tämä on työkohtainen vähimmäismäärä työkustannusten laskentaan.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-121">Note that no matter what job quantity will be processed, this is the minimum quantity per job to calculate the labor cost.</span></span> <span data-ttu-id="2a3ef-122">Jos työmäärät poikkeavat tästä määrästä, työkustannuspoikkeama luodaan.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-122">If job quantities deviate from this quantity, labor cost variance will be created.</span></span>  
7. <span data-ttu-id="2a3ef-123">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-123">Click Next.</span></span>

## <a name="select-the-work-cell"></a><span data-ttu-id="2a3ef-124">Valitse työsolu</span><span class="sxs-lookup"><span data-stu-id="2a3ef-124">Select the work cell</span></span>
1. <span data-ttu-id="2a3ef-125">Avaa haku valitsemalla Työsolu-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-125">In the Work cell field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="2a3ef-126">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-126">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="2a3ef-127">Määritä varastopäivitykset</span><span class="sxs-lookup"><span data-stu-id="2a3ef-127">Define the inventory updates</span></span>
1. <span data-ttu-id="2a3ef-128">Valitse Päivitä käytettävissä olevan varaston vastaanotto -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-128">Select or clear the Update on hand receipt check box.</span></span>
    * <span data-ttu-id="2a3ef-129">Jos Päivitä käytettävissä oleva varasto -arvona on Ei, voit määrittää tehtävän vastaanottamaan puolivalmiin tuotteen. (Tehtävä ei tavoita seuraavaa tuoterakennetasoa.)</span><span class="sxs-lookup"><span data-stu-id="2a3ef-129">If Update On hand = No, you can define the activity to receive a semi-finished product (the activity does not reach the next BOM level).</span></span>    <span data-ttu-id="2a3ef-130">Voit myös valita puolivalmiiden tuotteiden kulutuksen.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-130">You can also select to consume semi-finished products.</span></span>  

## <a name="define-the-picking-activities"></a><span data-ttu-id="2a3ef-131">Määritä keräystehtävät</span><span class="sxs-lookup"><span data-stu-id="2a3ef-131">Define the picking activities</span></span>
1. <span data-ttu-id="2a3ef-132">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-132">Click Next.</span></span>
2. <span data-ttu-id="2a3ef-133">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-133">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2a3ef-134">Oletuskeräystehtävä luodaan valitun työsolun syöttösijaintiin.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-134">A default picking activity is created for the input location of the selected work cell.</span></span>  
3. <span data-ttu-id="2a3ef-135">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-135">Click Add.</span></span>
    * <span data-ttu-id="2a3ef-136">Voit luoda tietyille tuotteille lisäkeräystehtäviä, joita ei vaiheisteta työsolun syöttötehtävässä.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-136">You can create additional picking activities for specific products, that are not staged at the work cell input activity.</span></span>  
4. <span data-ttu-id="2a3ef-137">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="2a3ef-138">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-138">In the Item number field, type a value.</span></span>
6. <span data-ttu-id="2a3ef-139">Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-139">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2a3ef-140">Tällä määrityksellä kaikki tehtävässä kulutetut materiaalit kerätään oletussyöttövarastosta ja -sijainnista lukuun ottamatta toisessa keräystehtävässä määritettyä nimikettä.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-140">With this definition, all materials consumed in the activity are picked from the default input warehouse and location except the item that is defined in the second picking activity.</span></span> <span data-ttu-id="2a3ef-141">Tämä nimike kerätään eri varastoista ja sijainnista.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-141">This item will be picked from a different warehouse and location.</span></span>  
7. <span data-ttu-id="2a3ef-142">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-142">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="2a3ef-143">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-143">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="2a3ef-144">Valitse Rekisteröi hävikki -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-144">Select or clear the Register scrap check box.</span></span>
10. <span data-ttu-id="2a3ef-145">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-145">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="2a3ef-146">Määritä tehtäväajat</span><span class="sxs-lookup"><span data-stu-id="2a3ef-146">Define the activity times</span></span>
1. <span data-ttu-id="2a3ef-147">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-147">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2a3ef-148">Suorituksenaikainen kohde on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-148">The definition of a Runtime is required.</span></span> <span data-ttu-id="2a3ef-149">Suorituksenaikaisella kohteella lasketaan kanban-töiden kustannukset ja läpimenoajat.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-149">The Runtime is used to calculate costs and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="2a3ef-150">Suorituksenaikaisia kohteita ei käytetä kapasiteetin kuormituksen ja kulutuksen laskentaan, sillä ne lasketaan tuotantovirran versiotehtävästä johdetusta syklin kestosta.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-150">Runtimes are not used to calculate capacity load and consumption, this is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="2a3ef-151">Lisää Aika-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-151">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="2a3ef-152">Kirjoita arvo Yksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-152">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="2a3ef-153">Valitse Aikayksikkö.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-153">Select the Time unit.</span></span>
5. <span data-ttu-id="2a3ef-154">Lisää Määrää kohden -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-154">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="2a3ef-155">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-155">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2a3ef-156">Jonotusajat ovat valinnaisia</span><span class="sxs-lookup"><span data-stu-id="2a3ef-156">Queue times are optional.</span></span>  
7. <span data-ttu-id="2a3ef-157">Lisää Aika-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-157">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="2a3ef-158">Kirjoita arvo Yksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-158">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="2a3ef-159">Valitse Aikayksikkö.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-159">Select the Time unit.</span></span>
10. <span data-ttu-id="2a3ef-160">Lisää Määrää kohden -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-160">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="2a3ef-161">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-161">Click Next.</span></span>
12. <span data-ttu-id="2a3ef-162">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-162">Click Finish.</span></span>
13. <span data-ttu-id="2a3ef-163">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2a3ef-163">Close the page.</span></span>


