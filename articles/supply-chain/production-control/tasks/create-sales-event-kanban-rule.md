--- 
title: "Luo myyntitapahtuman kanban-sääntö"
description: "Tässä menettelyssä käsitellään asetuksia, joita tarvitaan myyntitilauksen luonnin aikana käynnistettävän kanban-säännön luomiseen."
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: d2bee6e81acd029406c95237f0b4ba4ab2565ea1
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-sales-event-kanban-rule"></a><span data-ttu-id="ac421-103">Luo myyntitapahtuman kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="ac421-103">Create a sales event kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ac421-104">Tässä menettelyssä käsitellään asetuksia, joita tarvitaan myyntitilauksen luonnin aikana käynnistettävän kanban-säännön luomiseen.</span><span class="sxs-lookup"><span data-stu-id="ac421-104">This procedure focuses on the setup needed to create a kanban rule that is triggered during sales order creation.</span></span> <span data-ttu-id="ac421-105">Tapahtuman kanban-sääntö täydentää myyntitilausriveiltä lähtevät vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="ac421-105">The event kanban rule replenishes requirements that originate from sales order lines.</span></span> <span data-ttu-id="ac421-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="ac421-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ac421-107">Se on tarkoitettu prosessiteknikolle tai arvovirtaa hallitsevalle työntekijälle uuden tai muokatun tuotteen tuotannon valmisteluun.</span><span class="sxs-lookup"><span data-stu-id="ac421-107">It is intended for the process engineer or the value stream manager as they prepare production of a new or modified product.</span></span>




## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="ac421-108">Luo uusi kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="ac421-108">Create a new kanban rule</span></span>
1. <span data-ttu-id="ac421-109">Valitse Kanban-säännöt.</span><span class="sxs-lookup"><span data-stu-id="ac421-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="ac421-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ac421-110">Click New.</span></span>
3. <span data-ttu-id="ac421-111">Valitse Täydennysstrategia-kentässä Tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="ac421-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="ac421-112">Tapahtuman valitseminen tarkoittaa, että tapahtuma, kuten myyntitilausrivin luonti, käynnistää kanban-säännön.</span><span class="sxs-lookup"><span data-stu-id="ac421-112">Selecting Event means that the kanban rule is triggered by an event, for example, creation of a sales order line.</span></span>   <span data-ttu-id="ac421-113">Tätä käytetään alueilla, jossa kunkin kanbanin pitäisi kattaa tietty tarve.</span><span class="sxs-lookup"><span data-stu-id="ac421-113">This is applied to areas where each kanban should cover a specific demand.</span></span>  
4. <span data-ttu-id="ac421-114">Anna tai valitse Ensimmäinen suunnitelman tehtävä -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="ac421-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="ac421-115">Valitse Lopullinen kokoonpano.</span><span class="sxs-lookup"><span data-stu-id="ac421-115">Select Final assembly.</span></span>  
5. <span data-ttu-id="ac421-116">Laajenna Tiedot-osa.</span><span class="sxs-lookup"><span data-stu-id="ac421-116">Expand the Details section.</span></span>
6. <span data-ttu-id="ac421-117">Anna tai valitse Tuote-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="ac421-117">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="ac421-118">Valitse L0050.</span><span class="sxs-lookup"><span data-stu-id="ac421-118">Select L0050.</span></span>  

## <a name="define-an-event"></a><span data-ttu-id="ac421-119">Määritä tapahtuma</span><span class="sxs-lookup"><span data-stu-id="ac421-119">Define an event</span></span>
1. <span data-ttu-id="ac421-120">Laajenna Tapahtumat-osa.</span><span class="sxs-lookup"><span data-stu-id="ac421-120">Expand the Events section.</span></span>
2. <span data-ttu-id="ac421-121">Valitse Myyntitapahtuma-kentässä Automaattinen.</span><span class="sxs-lookup"><span data-stu-id="ac421-121">In the Sales event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="ac421-122">Kun automaattinen myyntitapahtuma valitaan, tämä kanban-sääntö käynnistetään automaattisesti, kun myyntirivi vastaa tuotetta ja vastaanottosijaintia.</span><span class="sxs-lookup"><span data-stu-id="ac421-122">By selecting the sales event Automatic, this kanban rule will be triggered automatically when a sales line matches the product and receipt location.</span></span> <span data-ttu-id="ac421-123">Tässä menettelyssä tuote L0050 on varastossa 13.</span><span class="sxs-lookup"><span data-stu-id="ac421-123">In this procedure, it is product L0050 on warehouse 13.</span></span>  
3. <span data-ttu-id="ac421-124">Määritä tapahtuman vähimmäismääräksi 50.</span><span class="sxs-lookup"><span data-stu-id="ac421-124">Set Minimum event quantity to '50'.</span></span>
    * <span data-ttu-id="ac421-125">Kun tapahtuman vähimmäismäärä on 50, vain tapahtumat, joiden määrä on vähintään 50, käynnistävät kanban-säännön.</span><span class="sxs-lookup"><span data-stu-id="ac421-125">With a minimum event quantity of 50, the kanban rule will only be triggered by events with a quantity of 50 or more.</span></span>  
4. <span data-ttu-id="ac421-126">Laajenna Tuotantovirta-osa.</span><span class="sxs-lookup"><span data-stu-id="ac421-126">Expand the Production flow section.</span></span>
    * <span data-ttu-id="ac421-127">Huomaa, vastaanottosijainti on varasto 13.</span><span class="sxs-lookup"><span data-stu-id="ac421-127">Notice that the Receipt location is warehouse 13.</span></span> <span data-ttu-id="ac421-128">Tämä tarkoittaa, että kanban-sääntö käynnistetään tässä sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="ac421-128">This means that this kanban rule will be triggered for this location.</span></span>  
    * <span data-ttu-id="ac421-129">Tässä esimerkissä myyntirivi tuotteelle L0050, jonka määrä varastossa 13 on vähintään 50, käynnistää tämän kanban-säännön.</span><span class="sxs-lookup"><span data-stu-id="ac421-129">In this example, a sales line for product L0050, with a quantity of 50 or more, on warehouse 13, will trigger this kanban rule.</span></span>  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a><span data-ttu-id="ac421-130">Luo tapahtuman kanban-säännön käynnistävä myyntirivi</span><span class="sxs-lookup"><span data-stu-id="ac421-130">Create sales line to trigger event kanban rule</span></span>
1. <span data-ttu-id="ac421-131">Siirry Kaikki myyntitilaukset -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="ac421-131">Go to All sales orders.</span></span>
    * <span data-ttu-id="ac421-132">Varoitus näytetään, kun kanban-sääntö tallennetaan, joten kanbanit luodaan reaaliaikaisesti myyntitilauksen luonnin aikana.</span><span class="sxs-lookup"><span data-stu-id="ac421-132">A warning is shown when the kanban rule is saved, which means that kanbans will be created in real-time during sales order creation.</span></span>  
2. <span data-ttu-id="ac421-133">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ac421-133">Click New.</span></span>
3. <span data-ttu-id="ac421-134">Syötä tai valitse arvo Asiakastili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ac421-134">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="ac421-135">Valitse esimerkiksi arvo US-003.</span><span class="sxs-lookup"><span data-stu-id="ac421-135">For example, select US-003.</span></span>  
4. <span data-ttu-id="ac421-136">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ac421-136">Click OK.</span></span>
5. <span data-ttu-id="ac421-137">Kirjoita Nimiketunnus-kenttään L0050.</span><span class="sxs-lookup"><span data-stu-id="ac421-137">In the Item number field, type 'L0050'.</span></span>
6. <span data-ttu-id="ac421-138">Kirjoita Toimipaikka-kenttään 1.</span><span class="sxs-lookup"><span data-stu-id="ac421-138">In the Site field, type '1'.</span></span>
    * <span data-ttu-id="ac421-139">Valitse toimipaikka 1, koska varasto 13 on toimipaikassa 1.</span><span class="sxs-lookup"><span data-stu-id="ac421-139">Select Site 1 because Warehouse 13 is on Site 1.</span></span>  
7. <span data-ttu-id="ac421-140">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="ac421-140">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="ac421-141">Määritä Varasto-arvoksi 13.</span><span class="sxs-lookup"><span data-stu-id="ac421-141">Set Warehouse to 13.</span></span>  
8. <span data-ttu-id="ac421-142">Valitse määräksi 75.</span><span class="sxs-lookup"><span data-stu-id="ac421-142">Set Quantity to '75'.</span></span>
    * <span data-ttu-id="ac421-143">Anna määräksi vähintään 50, jotta luotu kanban-sääntö luodaan.</span><span class="sxs-lookup"><span data-stu-id="ac421-143">Enter a quantity of 50 or greater, to trigger the created kanban rule.</span></span>  

## <a name="verify-that-kanban-is-created"></a><span data-ttu-id="ac421-144">Varmista, että kanban on luotu</span><span class="sxs-lookup"><span data-stu-id="ac421-144">Verify that kanban is created</span></span>
1. <span data-ttu-id="ac421-145">Valitse Tuote ja toimitus.</span><span class="sxs-lookup"><span data-stu-id="ac421-145">Click Product and supply.</span></span>
2. <span data-ttu-id="ac421-146">Valitse Näytä tarvekohdistuspuu.</span><span class="sxs-lookup"><span data-stu-id="ac421-146">Click View pegging tree.</span></span>
    * <span data-ttu-id="ac421-147">Huomaa, että luotavalla kanbanilla on sama määrä kuin myyntirivillä.</span><span class="sxs-lookup"><span data-stu-id="ac421-147">Notice that a kanban with the same quantity as the sales line is created.</span></span> <span data-ttu-id="ac421-148">Näet myös mitä materiaaliottoja L0050:n tuotantoon tarvitaan.</span><span class="sxs-lookup"><span data-stu-id="ac421-148">You can also see the material issues needed to produce L0050.</span></span> <span data-ttu-id="ac421-149">Tämä on tämän menettelyn viimeinen vaihe.</span><span class="sxs-lookup"><span data-stu-id="ac421-149">This is the last step in this procedure.</span></span>  


