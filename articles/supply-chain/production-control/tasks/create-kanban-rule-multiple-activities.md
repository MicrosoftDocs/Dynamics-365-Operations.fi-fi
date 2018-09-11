--- 
title: "Luo kanban-sääntö usealle tehtävälle"
description: "Seuraavassa menettelyssä kuvataan, miten luot kanban-säännön, joka sisältää useita tuotantovirran toimenpiteitä."
author: ChristianRytt
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 16aac6301b6534c4bf95184097ff5fc1b95fe795
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="82212-103">Luo kanban-sääntö usealle tehtävälle</span><span class="sxs-lookup"><span data-stu-id="82212-103">Create a kanban rule for multiple activities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="82212-104">Seuraavassa menettelyssä kuvataan, miten luot kanban-säännön, joka sisältää useita tuotantovirran toimenpiteitä.</span><span class="sxs-lookup"><span data-stu-id="82212-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="82212-105">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="82212-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="82212-106">Tämä tehtävä on tarkoitettu prosessiteknikolle tai arvovirtaa hallitsevalle työntekijälle uuden tai muokatun tuotteen tuotannon valmisteluun lean-ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="82212-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="82212-107">Luo uusi kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="82212-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="82212-108">Siirry kohtaan Tuotetietojen hallinta > Lean-valmistus > Kanban-säännöt.</span><span class="sxs-lookup"><span data-stu-id="82212-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="82212-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="82212-109">Click New.</span></span>
3. <span data-ttu-id="82212-110">Valitse Täydennysstrategia-kentässä Ajoitettu.</span><span class="sxs-lookup"><span data-stu-id="82212-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="82212-111">Anna tai valitse Ensimmäinen suunnitelman tehtävä -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="82212-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="82212-112">Valitse SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="82212-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="82212-113">Valitse useiden tehtävien valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="82212-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="82212-114">Kanban-sääntöön on tarkoitus sisällyttää useampi kuin yksi tehtävä.</span><span class="sxs-lookup"><span data-stu-id="82212-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="82212-115">Valitset polun tuotantovirrassa, kun valitset viimeisen suunnitelman tehtävän.</span><span class="sxs-lookup"><span data-stu-id="82212-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="82212-116">Anna tai valitse Viimeinen suunnitelman tehtävä -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="82212-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="82212-117">Valitse SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="82212-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="82212-118">Sivu aukeaa automaattisesti, kun olet valinnut arvon.</span><span class="sxs-lookup"><span data-stu-id="82212-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="82212-119">Valitse kanban-työnkulku SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="82212-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="82212-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="82212-120">Click OK.</span></span>  
7. <span data-ttu-id="82212-121">Laajenna Tiedot-osa.</span><span class="sxs-lookup"><span data-stu-id="82212-121">Expand the Details section.</span></span>
8. <span data-ttu-id="82212-122">Anna tai valitse Tuote-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="82212-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="82212-123">Valitse nimike L0006.</span><span class="sxs-lookup"><span data-stu-id="82212-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="82212-124">Luo kanban ja näytä työt</span><span class="sxs-lookup"><span data-stu-id="82212-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="82212-125">Laajenna Kanbanit-osa.</span><span class="sxs-lookup"><span data-stu-id="82212-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="82212-126">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="82212-126">Click Add.</span></span>
3. <span data-ttu-id="82212-127">Syötä Uusien kanbanien määrä -kenttän arvoksi "1".</span><span class="sxs-lookup"><span data-stu-id="82212-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="82212-128">Tämä luo yhden kanbanin.</span><span class="sxs-lookup"><span data-stu-id="82212-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="82212-129">Määritä tuotemääräksi 3.</span><span class="sxs-lookup"><span data-stu-id="82212-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="82212-130">Kanban käsittelee 3 tuotetta.</span><span class="sxs-lookup"><span data-stu-id="82212-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="82212-131">Syötä päivämäärä ja kellonaika Eräpäivä/-kellonaika -kenttään.</span><span class="sxs-lookup"><span data-stu-id="82212-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="82212-132">Voit antaa arvoksi Tänään.</span><span class="sxs-lookup"><span data-stu-id="82212-132">You can enter Today.</span></span>  
6. <span data-ttu-id="82212-133">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="82212-133">Click Create.</span></span>
7. <span data-ttu-id="82212-134">Valitse Erittely.</span><span class="sxs-lookup"><span data-stu-id="82212-134">Click Details.</span></span>
    * <span data-ttu-id="82212-135">Huomaa, että kanbanilla on kaksi tuotantovirran prosessityötä.</span><span class="sxs-lookup"><span data-stu-id="82212-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="82212-136">Ensimmäinen on SpeakerAssemblyAndPolish ja toinen SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="82212-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="82212-137">Tämä on viimeinen vaihe!</span><span class="sxs-lookup"><span data-stu-id="82212-137">This is the last step!</span></span>  


