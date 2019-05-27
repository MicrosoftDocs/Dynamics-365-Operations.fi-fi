---
title: Lean-valmistuksen alihankintatyösolun luominen
description: Kun haluat mallintaa alihankkijalle annetun lean-valmistuksen työn, luo työsolu, joka on liitetty työn tarjoavaan toimittajaan.
author: cvocph
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58b725af456f1a5c7f158f01ffe48a2d8cdf056b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550534"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a><span data-ttu-id="4fcce-103">Lean-valmistuksen alihankintatyösolun luominen</span><span class="sxs-lookup"><span data-stu-id="4fcce-103">Create a subcontracted work cell for lean manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4fcce-104">Kun haluat mallintaa alihankkijalle annetun lean-valmistuksen työn, luo työsolu, joka on liitetty työn tarjoavaan toimittajaan.</span><span class="sxs-lookup"><span data-stu-id="4fcce-104">To model subcontracted work for lean manufacturing, you must create a work cell that is associated with the vendor that provides the work.</span></span> <span data-ttu-id="4fcce-105">Alihankinnan työsolu linkitetään toimittajaan Toimittaja-tyyppisen resurssin liitoksen kautta.</span><span class="sxs-lookup"><span data-stu-id="4fcce-105">A subcontracted work cell is linked to the vendor through the association of a resource of the Vendor type.</span></span> <span data-ttu-id="4fcce-106">Jos tämä tallenne toistetaan USMF-demoyrityksessä, voit valita toimittajan tilin, jonka tunnus on 1002, ja toimipaikan 1.</span><span class="sxs-lookup"><span data-stu-id="4fcce-106">If you play this recording in the USMF demo company, you can select vendor account ID 1002 and site 1.</span></span>


## <a name="create-a-vendor-resource"></a><span data-ttu-id="4fcce-107">Luo toimittajan resurssi</span><span class="sxs-lookup"><span data-stu-id="4fcce-107">Create a vendor resource</span></span>
1. <span data-ttu-id="4fcce-108">Siirry Resurssit-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="4fcce-108">Go to Resources.</span></span>
2. <span data-ttu-id="4fcce-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4fcce-109">Click New.</span></span>
3. <span data-ttu-id="4fcce-110">Kirjoita arvo Resurssi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4fcce-110">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="4fcce-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4fcce-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4fcce-112">Valitse Tyyppi-kenttään Toimittaja.</span><span class="sxs-lookup"><span data-stu-id="4fcce-112">In the Type field, select 'Vendor'.</span></span>
6. <span data-ttu-id="4fcce-113">Avaa haku valitsemalla Toimittaja-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="4fcce-113">In the Vendor field, click the drop-down button to open the lookup.</span></span>

## <a name="create-the-resource-group"></a><span data-ttu-id="4fcce-114">Luo resurssiryhmä</span><span class="sxs-lookup"><span data-stu-id="4fcce-114">Create the resource group</span></span>
1. <span data-ttu-id="4fcce-115">Siirry Resurssiryhmät-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="4fcce-115">Go to Resource groups.</span></span>
2. <span data-ttu-id="4fcce-116">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4fcce-116">Click New.</span></span>
3. <span data-ttu-id="4fcce-117">Kirjoita arvo Resurssiryhmä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4fcce-117">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="4fcce-118">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4fcce-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4fcce-119">Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="4fcce-119">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4fcce-120">Valitse toimipaikka, johon työsolu kohdistetaan.</span><span class="sxs-lookup"><span data-stu-id="4fcce-120">Select the site that the work cell should be allocated to.</span></span> <span data-ttu-id="4fcce-121">Teoriassa toimipaikka voi edustaa yksittäistä toimittajan toimipaikkaa.</span><span class="sxs-lookup"><span data-stu-id="4fcce-121">In theory, a site can represent a single site that is operated by a vendor.</span></span> <span data-ttu-id="4fcce-122">Kuitenkin suurimmassa osassa tapauksia alihankinnan resurssit kohdistetaan toimipaikkaan, joka on tilannut alihankkijalle annetun työn.</span><span class="sxs-lookup"><span data-stu-id="4fcce-122">However, in most cases, subcontracted resources are just allocated to the site that orders the subcontracted work.</span></span> <span data-ttu-id="4fcce-123">Ota huomioon, että alihankinnan työsolujen syöttö- ja tuotosvaraston on oltava samassa toimipaikassa.</span><span class="sxs-lookup"><span data-stu-id="4fcce-123">Note that the input and output warehouses of subcontracted work cells must be on the same site.</span></span>  
6. <span data-ttu-id="4fcce-124">Kirjoita arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4fcce-124">In the Site field, type a value.</span></span>
7. <span data-ttu-id="4fcce-125">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="4fcce-125">@SysTaskRecorder:_RequestClose</span></span>
8. <span data-ttu-id="4fcce-126">Valitse Työsolu-valintaruutu tai poista valintaruudun valinta.</span><span class="sxs-lookup"><span data-stu-id="4fcce-126">Select or clear the Work cell check box.</span></span>
9. <span data-ttu-id="4fcce-127">Avaa haku napsauttamalla Syöttövarasto-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="4fcce-127">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4fcce-128">Valitse varasto ja sijainti, joita käytetään materiaalin paikkana toimittajan hallitsemassa työsolussa.</span><span class="sxs-lookup"><span data-stu-id="4fcce-128">Select the warehouse and location that are used to stage the material for the vendor-managed work cell.</span></span> <span data-ttu-id="4fcce-129">Useissa tapauksissa varasto ja sijainti voidaan mallintaa käyttämällä erillistä varastoa toimittajaa kohti ja yhtä sijaintia työsolua kohti.</span><span class="sxs-lookup"><span data-stu-id="4fcce-129">In many cases, the warehouse and location are modeled by using a separate warehouse per vendor and one location per work cell.</span></span>  
10. <span data-ttu-id="4fcce-130">Avaa haku napsauttamalla Syöttösijainti-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="4fcce-130">In the Input location field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="4fcce-131">Avaa haku napsauttamalla Tuotosvarasto-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="4fcce-131">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4fcce-132">Määritä varasto ja sijainti, jonne materiaali kirjataan, kun työsolun alihankintatehtävät kirjataan.</span><span class="sxs-lookup"><span data-stu-id="4fcce-132">Define the warehouse and location where the material is posted when the subcontracted activities of the work cell are posted.</span></span> <span data-ttu-id="4fcce-133">Varasto ja sijainti voivat olla toimittajan toimipaikassa, jos toimittaja raportoi kanban-työt.</span><span class="sxs-lookup"><span data-stu-id="4fcce-133">The warehouse and location can be at the vendor site if the vendor reports the kanban jobs.</span></span> <span data-ttu-id="4fcce-134">Vaihtoehtoisesti varasto ja sijainti voivat olla vastaanottosijainnissa, joka on liitetty tuotantovirran seuraavaan vaiheeseen.</span><span class="sxs-lookup"><span data-stu-id="4fcce-134">Alternatively, the warehouse and location can be the receiving location that is associated with the next step of the production flow.</span></span>  
12. <span data-ttu-id="4fcce-135">Avaa haku napsauttamalla Tuotossijainti-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="4fcce-135">In the Output location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="4fcce-136">Laajenna tai tiivistä Kalenterit-osa.</span><span class="sxs-lookup"><span data-stu-id="4fcce-136">Expand or collapse the Calendars section.</span></span>
14. <span data-ttu-id="4fcce-137">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4fcce-137">Click Add.</span></span>
15. <span data-ttu-id="4fcce-138">Avaa haku valitsemalla Kalenteri-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="4fcce-138">In the Calendar field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4fcce-139">Liitä työsolun työaikakalenteri resurssiryhmään.</span><span class="sxs-lookup"><span data-stu-id="4fcce-139">Associate the working time calendar of the work cell with the resource group.</span></span> <span data-ttu-id="4fcce-140">Kriittisiä resursseja varten kannattaa määrittää erityiset kalenterit, jotka edustavat tarkkoja työaikoja ja työsolun tai toimittajan toimipaikan liittyviä kapasiteetteja.</span><span class="sxs-lookup"><span data-stu-id="4fcce-140">For critical resources, we recommend that you define specific calendars that represent the exact working times and related capacities of the work cell or vendor site.</span></span>  
16. <span data-ttu-id="4fcce-141">Laajenna tai tiivistä Resurssit-osa.</span><span class="sxs-lookup"><span data-stu-id="4fcce-141">Expand or collapse the Resources section.</span></span>
17. <span data-ttu-id="4fcce-142">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4fcce-142">Click Add.</span></span>
    * <span data-ttu-id="4fcce-143">Alihankinnan resurssiryhmällä on oltava liitetty resurssi, jonka tyyppi on Toimittaja. Se linkittää resurssiryhmän toimittajan tiliin.</span><span class="sxs-lookup"><span data-stu-id="4fcce-143">A subcontracted resource group must have an associated resource of the Vendor type that links the resource group to the vendor account.</span></span>  
18. <span data-ttu-id="4fcce-144">Avaa haku valitsemalla Resurssi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="4fcce-144">In the Resource field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4fcce-145">Valitse tai syötä edellisessä alitehtävässä luotu toimittajan resurssi.</span><span class="sxs-lookup"><span data-stu-id="4fcce-145">Select or enter the vendor resource that you created in the previous sub-task.</span></span>  
19. <span data-ttu-id="4fcce-146">Laajenna tai tiivistä Työsolun kapasiteetti -osa.</span><span class="sxs-lookup"><span data-stu-id="4fcce-146">Expand or collapse the Work cell capacity section.</span></span>
20. <span data-ttu-id="4fcce-147">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4fcce-147">Click Add.</span></span>
    * <span data-ttu-id="4fcce-148">Työsolulle on määritettävä kapasiteetti.</span><span class="sxs-lookup"><span data-stu-id="4fcce-148">A work cell must have a defined capacity.</span></span> <span data-ttu-id="4fcce-149">Tässä esimerkissä luodaan 100 kappaleen tuotantoteho tavallista työpäivää kohti.</span><span class="sxs-lookup"><span data-stu-id="4fcce-149">In this example, we create a throughput capacity of 100 pieces per standard workday.</span></span>  
21. <span data-ttu-id="4fcce-150">Avaa haku napsauttamalla Tuotantovirtamalli-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="4fcce-150">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="4fcce-151">Valitse vaihtoehto Kapasiteettikausi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="4fcce-151">In the Capacity period field, select an option.</span></span>
23. <span data-ttu-id="4fcce-152">Lisää Tuotantokapasiteetin keskimääräinen määrä -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="4fcce-152">In the Average throughput quantity field, enter a number.</span></span>
24. <span data-ttu-id="4fcce-153">Avaa haku napsauttamalla Yksikkö -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="4fcce-153">In the Unit field, click the drop-down button to open the lookup.</span></span>
25. <span data-ttu-id="4fcce-154">Ratkaise muutokset yksikössä.</span><span class="sxs-lookup"><span data-stu-id="4fcce-154">ResolveChanges the Unit.</span></span>

