--- 
title: "Kanban-töiden ajoitus"
description: "Tässä menettelyssä keskitytään tietyn työsolun aikataulutusprosessin kanban-töihin."
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f36544993a9280ae10489a19252bc105abd40ac9
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="schedule-kanban-jobs"></a><span data-ttu-id="337b0-103">Kanban-töiden ajoitus</span><span class="sxs-lookup"><span data-stu-id="337b0-103">Schedule kanban jobs</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="337b0-104">Tässä menettelyssä keskitytään tietyn työsolun aikataulutusprosessin kanban-töihin.</span><span class="sxs-lookup"><span data-stu-id="337b0-104">This procedure focuses on scheduling process kanban jobs for a specific work cell.</span></span> <span data-ttu-id="337b0-105">Valmistele kanban-työn kun materiaalit eivät ole käytettävissä työsolulle -menettely on tämän menettelyn luomisen edellytys.</span><span class="sxs-lookup"><span data-stu-id="337b0-105">The procedure "Prepare a process kanban job when materials are not available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="337b0-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="337b0-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="337b0-107">Tämä tehtävä on tarkoitettu työnohjauksen esimiehelle ja tuotannon suunnittelijalle, jotka käsittelevät kanbaneita.</span><span class="sxs-lookup"><span data-stu-id="337b0-107">This task is intended for the shop floor supervisor and production planner working with kanbans.</span></span>


## <a name="select-kanban-jobs-for-a-work-cell"></a><span data-ttu-id="337b0-108">Työsolun kanban-töiden valitseminen</span><span class="sxs-lookup"><span data-stu-id="337b0-108">Select kanban jobs for a work cell</span></span>
1. <span data-ttu-id="337b0-109">Siirry kohtaan Tuotannonhallinta > Kanban > Kanban-työn aikataulutus.</span><span class="sxs-lookup"><span data-stu-id="337b0-109">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="337b0-110">Laajenna Kauden kapasiteetti -tietokenttä.</span><span class="sxs-lookup"><span data-stu-id="337b0-110">Expand the Period capacity fact box</span></span>
    * <span data-ttu-id="337b0-111">Laajenna Kanban-tietoruutu.</span><span class="sxs-lookup"><span data-stu-id="337b0-111">Expand the Kanban FactBox.</span></span>  
3. <span data-ttu-id="337b0-112">Avaa haku valitsemalla Työsolu-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="337b0-112">In the Work cell field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="337b0-113">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="337b0-113">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="337b0-114">Valitse työsolu 1250.</span><span class="sxs-lookup"><span data-stu-id="337b0-114">Select work cell 1250.</span></span> <span data-ttu-id="337b0-115">Nyt näkymä suodatetaan niin, että se näyttää vain työsolun 1250 työt.</span><span class="sxs-lookup"><span data-stu-id="337b0-115">This will filter the view to display only the jobs for work cell 1250.</span></span>  
5. <span data-ttu-id="337b0-116">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="337b0-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="337b0-117">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="337b0-117">Click Select.</span></span>

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a><span data-ttu-id="337b0-118">Kanban-työn aikatauluttaminen ensimmäiselle käytettävissä olevalle kaudelle</span><span class="sxs-lookup"><span data-stu-id="337b0-118">Schedule a kanban job in the first available period</span></span>
1. <span data-ttu-id="337b0-119">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="337b0-119">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="337b0-120">Valitse luettelon ensimmäinen rivi, jonka tila on Ei suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="337b0-120">Select the first row in the list that has the Not planned status.</span></span> <span data-ttu-id="337b0-121">Työn tila -kentän pisteviivakuvake osoittaa, että tila on Ei suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="337b0-121">The dotted icon in the Job status field indicates not planned.</span></span>  
2. <span data-ttu-id="337b0-122">Valitse Aikatauluta.</span><span class="sxs-lookup"><span data-stu-id="337b0-122">Click Schedule.</span></span>
    * <span data-ttu-id="337b0-123">Tämä aikatauluttaa kanban-työn ensimmäisellä käytettävissä olevalla kaudella.</span><span class="sxs-lookup"><span data-stu-id="337b0-123">This will schedule the kanban job in the first available period.</span></span>  
    * <span data-ttu-id="337b0-124">Huomioi, että kanban-työ siirretään luettelon loppuun, koska se on lisätty tänään alkavalle kaudelle.</span><span class="sxs-lookup"><span data-stu-id="337b0-124">Notice that the kanban job is moved to the end of the list because it has been added to the period starting from today.</span></span>  
    * <span data-ttu-id="337b0-125">Jos kuluvasta päivästä alkava kausi on kokonaan varattu, työ siirretään ensimmäiseen käytettävissä olevaan kauteen.</span><span class="sxs-lookup"><span data-stu-id="337b0-125">If the period starting from today is fully booked, the job will be moved to the first available period.</span></span>  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a><span data-ttu-id="337b0-126">Kahden kanban-työn aikatauluttaminen tietylle päivälle</span><span class="sxs-lookup"><span data-stu-id="337b0-126">Schedule two kanban jobs for a specific day</span></span>
1. <span data-ttu-id="337b0-127">Valitse luettelosta rivi 1.</span><span class="sxs-lookup"><span data-stu-id="337b0-127">In the list, select row 1.</span></span>
    * <span data-ttu-id="337b0-128">Ensimmäisen rivin Työn tila -kentässä tulisi olla Ei suunniteltu -tila.</span><span class="sxs-lookup"><span data-stu-id="337b0-128">You should see that the first row has the Not planned status in the Job status field.</span></span>  
2. <span data-ttu-id="337b0-129">Valitse luettelosta rivi 2.</span><span class="sxs-lookup"><span data-stu-id="337b0-129">In the list, select row 2.</span></span>
    * <span data-ttu-id="337b0-130">Toisen rivin Työn tila -kentässä tulisi olla Ei suunniteltu -tila.</span><span class="sxs-lookup"><span data-stu-id="337b0-130">You should see that the second row has the Not planned status in the Job status field.</span></span> <span data-ttu-id="337b0-131">Nyt kaksi ensimmäistä työtä on valittu.</span><span class="sxs-lookup"><span data-stu-id="337b0-131">Now you have the first two jobs selected.</span></span>  
3. <span data-ttu-id="337b0-132">Avaa valintaikkuna valitsemalla Aikataulun alkupäivä.</span><span class="sxs-lookup"><span data-stu-id="337b0-132">Click Schedule from date to open the drop dialog.</span></span>
4. <span data-ttu-id="337b0-133">Valitse Ohita kapasiteetin puutteen aiheuttama reaktio -ruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="337b0-133">Check or uncheck the Override capacity shortage reaction box.</span></span>
    * <span data-ttu-id="337b0-134">Tämän asetuksen avulla voit korvata kapasiteetin puutteen aiheuttaman oletusreaktion.</span><span class="sxs-lookup"><span data-stu-id="337b0-134">This option allows you to override the default capacity shortage reaction.</span></span>  
5. <span data-ttu-id="337b0-135">Valitse Kapasiteetin puutteen aiheuttama reaktio -kentässä Lisää pyydetty kausi.</span><span class="sxs-lookup"><span data-stu-id="337b0-135">In the Capacity shortage reaction field, select 'Add to the requested period'.</span></span>
    * <span data-ttu-id="337b0-136">Tämä asetus varmistaa, että työ lisätään pyydetylle kaudelle myös silloin, jos työsolu on ylikuormittunut.</span><span class="sxs-lookup"><span data-stu-id="337b0-136">This option will ensure that the job is added to the requested period, regardless if the work cell might be overloaded.</span></span>  
6. <span data-ttu-id="337b0-137">Valitse Aikatauluta.</span><span class="sxs-lookup"><span data-stu-id="337b0-137">Click Schedule.</span></span>
    * <span data-ttu-id="337b0-138">Huomioi myös se, että molemmat työt lisätään haluttuun kauteen.</span><span class="sxs-lookup"><span data-stu-id="337b0-138">Notice that both jobs are added to the desired period.</span></span>  
    * <span data-ttu-id="337b0-139">Kauden kapasiteetti -osassa näkyy kunkin kauden kuormitus.</span><span class="sxs-lookup"><span data-stu-id="337b0-139">In the Period capacity section, you can see the load for each period.</span></span> <span data-ttu-id="337b0-140">Kulutus-kentässä näkyy tämän kauden suunniteltu kulutus.</span><span class="sxs-lookup"><span data-stu-id="337b0-140">The Consumption field shows the scheduled consumption in this period.</span></span> <span data-ttu-id="337b0-141">Jos suunniteltu kulutus on korkeampi kuin tämän kauden käytettävissä oleva kapasiteetti, valitaan ylikuormitettu kulutus.</span><span class="sxs-lookup"><span data-stu-id="337b0-141">If the scheduled consumption is higher than the available capacity in this period, the overloaded consumption will be selected.</span></span>  


