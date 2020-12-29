---
title: Luo tuoterakennerivitapahtuman kanban-sääntö
description: Tehtävässä keskitytään määrityksiin, jotka tarvitaan tapahtuman kanban-säännön luomiseen, jotta voidaan varmistaa toimitukset tuotannon tuoterakenneriveille lean-menetelmiä ja perinteisiä menetelmiä yhdistävässä tuotantoympäristössä.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdTable, ProdBOM, ProdParmCostEstimation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 698b7af3bc8e2146aaf86fb5e04dd123ea6d5153
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426797"
---
# <a name="create-a-bom-line-event-kanban-rule"></a><span data-ttu-id="9aa86-103">Luo tuoterakennerivitapahtuman kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="9aa86-103">Create a BOM line event kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9aa86-104">Tehtävässä keskitytään määrityksiin, jotka tarvitaan tapahtuman kanban-säännön luomiseen, jotta voidaan varmistaa toimitukset tuotannon tuoterakenneriveille lean-menetelmiä ja perinteisiä menetelmiä yhdistävässä tuotantoympäristössä.</span><span class="sxs-lookup"><span data-stu-id="9aa86-104">This task focuses on the setup needed to create an event kanban rule to ensure supply for production BOM lines in a mixed lean and classic production environment.</span></span> <span data-ttu-id="9aa86-105">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="9aa86-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="9aa86-106">Tehtävä on tarkoitettu prosessiteknikolle tai arvovirtaa hallitsevalle työntekijälle uuden tai muokatun tuotteen tuotannon valmisteluun.</span><span class="sxs-lookup"><span data-stu-id="9aa86-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="9aa86-107">Luo uusi kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="9aa86-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="9aa86-108">Valitse Tuotannonhallinta > Kausittaiset tehtävät > Kanban-määrän laskeminen > Kanban-säännöt.</span><span class="sxs-lookup"><span data-stu-id="9aa86-108">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban rules.</span></span>
2. <span data-ttu-id="9aa86-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9aa86-109">Click New.</span></span>
3. <span data-ttu-id="9aa86-110">Valitse Tyyppi-kentän arvoksi "Otto".</span><span class="sxs-lookup"><span data-stu-id="9aa86-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="9aa86-111">Otto-tyyppiä käytetään siirtokanbanien luomiseen.</span><span class="sxs-lookup"><span data-stu-id="9aa86-111">The Withdrawal type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="9aa86-112">Valitse Täydennysstrategia-kentässä Tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="9aa86-112">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="9aa86-113">Tapahtumastategia valitaan, jotta kanbanien siirto voidaan tehdä tapahtuman perusteella.</span><span class="sxs-lookup"><span data-stu-id="9aa86-113">The Event strategy is selected to create the transfer of kanbans based on an event.</span></span> <span data-ttu-id="9aa86-114">Strategia käynnistetään myöhemmin tehtäväoppaassa tuotantotilauksen arvioinnilla.</span><span class="sxs-lookup"><span data-stu-id="9aa86-114">Later in the task guide, we will trigger it by estimating a production order.</span></span>  
5. <span data-ttu-id="9aa86-115">Anna tai valitse Ensimmäinen suunnitelman tehtävä -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="9aa86-115">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="9aa86-116">Anna tai valitse ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="9aa86-116">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="9aa86-117">Siirtotehtävällä on vastaanottava (tulos-)varasto ja toimipaikka 12, minkä vuoksi materiaalin siirretään varaston 12 toimipaikkaan 12.</span><span class="sxs-lookup"><span data-stu-id="9aa86-117">This transfer activity has receipt (output) warehouse and location 12, which means that material will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="9aa86-118">Laajenna Tiedot-osa.</span><span class="sxs-lookup"><span data-stu-id="9aa86-118">Expand the Details section.</span></span>
7. <span data-ttu-id="9aa86-119">Anna tai valitse Tuote-kenttän arvoksi M0001.</span><span class="sxs-lookup"><span data-stu-id="9aa86-119">In the Product field, enter or select M0001.</span></span>
8. <span data-ttu-id="9aa86-120">Laajenna Tapahtumat-osa.</span><span class="sxs-lookup"><span data-stu-id="9aa86-120">Expand the Events section.</span></span>
9. <span data-ttu-id="9aa86-121">Valitse Tuotantotilausrivin tapahtuma -kentässä Automaattinen.</span><span class="sxs-lookup"><span data-stu-id="9aa86-121">In the BOM line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="9aa86-122">Kun tuoterakennerivin tapahtumakentän arvo on Automaattinen, kanban luodaan täyttämään tuotantotilauksen tuoterakennerivien materiaalitarpeet.</span><span class="sxs-lookup"><span data-stu-id="9aa86-122">With the BOM line event field set to Automatic, kanban will be created to fulfill material needs for production order BOM lines.</span></span>  
10. <span data-ttu-id="9aa86-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9aa86-123">Close the page.</span></span>

## <a name="create-and-modify-a-new-production-order"></a><span data-ttu-id="9aa86-124">Luo ja muokkaa uusi tuotantotilaus</span><span class="sxs-lookup"><span data-stu-id="9aa86-124">Create and modify a new production order</span></span>
1. <span data-ttu-id="9aa86-125">Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="9aa86-125">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="9aa86-126">Valitse Uusi tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="9aa86-126">Click New production order.</span></span>
3. <span data-ttu-id="9aa86-127">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="9aa86-127">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="9aa86-128">Kirjoita tai valitse L0001.</span><span class="sxs-lookup"><span data-stu-id="9aa86-128">Enter or select 'L0001'.</span></span> <span data-ttu-id="9aa86-129">Nimikettä L0001 käytetään, koska nimike M0001 sisältyy nimikkeen L0001 nimikkeen tuoterakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="9aa86-129">We use item L0001 because item M0001 is included in the BOM for item L0001.</span></span>  
4. <span data-ttu-id="9aa86-130">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="9aa86-130">Click Create.</span></span>
5. <span data-ttu-id="9aa86-131">Napsauta luettelossa L0001-rivillä olevaa linkkiä</span><span class="sxs-lookup"><span data-stu-id="9aa86-131">In the list, click the link in the row for L0001</span></span>
6. <span data-ttu-id="9aa86-132">Valitse Tuoterakenne.</span><span class="sxs-lookup"><span data-stu-id="9aa86-132">Click BOM.</span></span>
7. <span data-ttu-id="9aa86-133">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="9aa86-133">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9aa86-134">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="9aa86-134">Click Edit.</span></span>
9. <span data-ttu-id="9aa86-135">Valitse Rivin tyyppi -kenttään "Tarvekohdistuksen tarjonta".</span><span class="sxs-lookup"><span data-stu-id="9aa86-135">In the Line type field, select 'Pegged supply'.</span></span>
    * <span data-ttu-id="9aa86-136">Tarvekohdistuksen tarjonta valitaan käynnistämään kanbanin toimitusten luonti.</span><span class="sxs-lookup"><span data-stu-id="9aa86-136">Pegged supply is selected to trigger the supply creation of a kanban.</span></span>  
10. <span data-ttu-id="9aa86-137">Valitse Resurssin kulutus -kentässä Ei.</span><span class="sxs-lookup"><span data-stu-id="9aa86-137">Select No in the Resource consumption field.</span></span>
    * <span data-ttu-id="9aa86-138">Resurrsin kulutus -valintaruudun merkinnän poistamalla voit vaihtaa varastoa.</span><span class="sxs-lookup"><span data-stu-id="9aa86-138">Clearing the check box of Resource consumption lets us change the warehouse.</span></span>  
11. <span data-ttu-id="9aa86-139">Laajenna Varaston dimensiot -osa.</span><span class="sxs-lookup"><span data-stu-id="9aa86-139">Expand the Inventory dimensions section.</span></span>
12. <span data-ttu-id="9aa86-140">Syötä Varasto-kenttään 12.</span><span class="sxs-lookup"><span data-stu-id="9aa86-140">In the Warehouse field, type '12'.</span></span>
    * <span data-ttu-id="9aa86-141">Varastoksi on määritetty 12, koska se on ottotehtävän tulosvarasto.</span><span class="sxs-lookup"><span data-stu-id="9aa86-141">Warehouse is set to 12 because this is the output warehouse for the withdrawal activity.</span></span>  
13. <span data-ttu-id="9aa86-142">Syötä Toimipaikka-kenttään arvo 12.</span><span class="sxs-lookup"><span data-stu-id="9aa86-142">In the Location field, type '12'.</span></span>
    * <span data-ttu-id="9aa86-143">Toimipaikaksi on määritetty 12, koska se on ottotehtävän tulostoimipaikka.</span><span class="sxs-lookup"><span data-stu-id="9aa86-143">Location is set to 12 because this is the output location of the withdrawal activity.</span></span>  
14. <span data-ttu-id="9aa86-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9aa86-144">Close the page.</span></span>
15. <span data-ttu-id="9aa86-145">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9aa86-145">Close the page.</span></span>

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a><span data-ttu-id="9aa86-146">Arvioi tuotantotilaus ja näytä luotu kanban</span><span class="sxs-lookup"><span data-stu-id="9aa86-146">Estimate the production order and view the kanban created</span></span>
1. <span data-ttu-id="9aa86-147">Valitse Arvio.</span><span class="sxs-lookup"><span data-stu-id="9aa86-147">Click Estimate.</span></span>
    * <span data-ttu-id="9aa86-148">Tuotantotilauksen arviointi käynnistää liittyvässä kanbanissa nimikkeen M0001 toimituksen luonnin.</span><span class="sxs-lookup"><span data-stu-id="9aa86-148">Estimating the production order will trigger the creation of the associated kanban to supply item M0001.</span></span>  
2. <span data-ttu-id="9aa86-149">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9aa86-149">Click OK.</span></span>
3. <span data-ttu-id="9aa86-150">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9aa86-150">Close the page.</span></span>
4. <span data-ttu-id="9aa86-151">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9aa86-151">Close the page.</span></span>
5. <span data-ttu-id="9aa86-152">Siirry kohtaan Tuotetietojen hallinta > Lean-valmistus > Kanban-säännöt.</span><span class="sxs-lookup"><span data-stu-id="9aa86-152">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
6. <span data-ttu-id="9aa86-153">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="9aa86-153">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9aa86-154">Valitse nimikkeelle M0001 luotu tapahtuman kanban-sääntö.</span><span class="sxs-lookup"><span data-stu-id="9aa86-154">Select the event kanban rule created for item M0001.</span></span>  
7. <span data-ttu-id="9aa86-155">Laajenna Kanbanit-osa.</span><span class="sxs-lookup"><span data-stu-id="9aa86-155">Expand the Kanbans section.</span></span>
8. <span data-ttu-id="9aa86-156">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="9aa86-156">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9aa86-157">Huomaa kanban, joka on luotu toimittamaan M0001 arvioituun tuotantotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="9aa86-157">Notice the kanban created to supply M0001 for the estimated production order.</span></span>  
    * <span data-ttu-id="9aa86-158">Tämä on viimeinen vaihe!</span><span class="sxs-lookup"><span data-stu-id="9aa86-158">This is the last step!</span></span>  

