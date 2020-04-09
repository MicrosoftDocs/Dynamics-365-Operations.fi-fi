---
title: Luo oton kanban-sääntö
description: Seuraavassa menettelyssä kuvataan tarvittavat määritykset ottamisen kanban-säännön luomiseen materiaalin siirtämiseksi lean-ympäristössä.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: afc927fbc77f2120678fdf856b47d7c0e1b5a37d
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149190"
---
# <a name="create-a-withdrawal-kanban-rule"></a><span data-ttu-id="e8f32-103">Luo oton kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="e8f32-103">Create a withdrawal kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e8f32-104">Seuraavassa menettelyssä kuvataan tarvittavat määritykset ottamisen kanban-säännön luomiseen materiaalin siirtämiseksi lean-ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="e8f32-104">This procedure shows the setup that is needed to create a withdrawal kanban rule for transferring material in a lean environment.</span></span> <span data-ttu-id="e8f32-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="e8f32-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e8f32-106">Menettely on tarkoitettu prosessiteknikolle tai arvovirtaa hallitsevalle työntekijälle uuden tai muokatun materiaalin täydennyksen valmisteluun.</span><span class="sxs-lookup"><span data-stu-id="e8f32-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare replenishment of new or modified material.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="e8f32-107">Luo uusi kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="e8f32-107">Create new kanban rule</span></span>
1. <span data-ttu-id="e8f32-108">Valitse Kanban-säännöt.</span><span class="sxs-lookup"><span data-stu-id="e8f32-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="e8f32-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="e8f32-109">Click New.</span></span>
3. <span data-ttu-id="e8f32-110">Valitse Tyyppi-kentän arvoksi "Otto".</span><span class="sxs-lookup"><span data-stu-id="e8f32-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="e8f32-111">Otto-tyyppiä käytetään kanban-säännössä tuotteiden tai materiaalin siirtoon.</span><span class="sxs-lookup"><span data-stu-id="e8f32-111">The Withdrawal type is used for kanban rules to transfer material or goods.</span></span>  
4. <span data-ttu-id="e8f32-112">Anna tai valitse Ensimmäinen suunnitelman tehtävä -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="e8f32-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="e8f32-113">Valitse ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="e8f32-113">Select ReplenishSpeakerComponents.</span></span>   <span data-ttu-id="e8f32-114">Tehtävä on määritetty siirtämään komponentteja varaston 11 toimipaikasta 11 varaston 12 toimipaikkaan 12.</span><span class="sxs-lookup"><span data-stu-id="e8f32-114">This activity is set up to move components from warehouse 11, location 11 to warehouse 12, and location 12.</span></span>  
5. <span data-ttu-id="e8f32-115">Anna tai valitse Tuote-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="e8f32-115">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="e8f32-116">Valitse M0007.</span><span class="sxs-lookup"><span data-stu-id="e8f32-116">Select M0007.</span></span>  
6. <span data-ttu-id="e8f32-117">Lisää Läpimenoaika-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="e8f32-117">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="e8f32-118">Esimerkki: 60.</span><span class="sxs-lookup"><span data-stu-id="e8f32-118">For example, 60.</span></span>  
7. <span data-ttu-id="e8f32-119">Anna tai valitse Mittayksikkö-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="e8f32-119">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="e8f32-120">Esimerkiksi minuutteja.</span><span class="sxs-lookup"><span data-stu-id="e8f32-120">For example, Minutes.</span></span>  

## <a name="set-quantities-for-kanban"></a><span data-ttu-id="e8f32-121">Määritä kanban-määrät</span><span class="sxs-lookup"><span data-stu-id="e8f32-121">Set quantities for kanban</span></span>
1. <span data-ttu-id="e8f32-122">Määritä Oletusmäärä-arvoksi 5.</span><span class="sxs-lookup"><span data-stu-id="e8f32-122">Set Default quantity to '5'.</span></span>
    * <span data-ttu-id="e8f32-123">Tämä määrä siirretään kullekin kanbanille.</span><span class="sxs-lookup"><span data-stu-id="e8f32-123">This is the quantity that will be transferred for each kanban.</span></span>  
2. <span data-ttu-id="e8f32-124">Syötä Kiinteä kanban-määrä -kentän arvoksi 2.</span><span class="sxs-lookup"><span data-stu-id="e8f32-124">In the Fixed kanban quantity field, enter '2'.</span></span>
    * <span data-ttu-id="e8f32-125">Tämä on sellaisten kanbanien määrä, joiden pitäisi olla aktiivisia.</span><span class="sxs-lookup"><span data-stu-id="e8f32-125">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="e8f32-126">Tällä tapauksessa jokainen 2 kanbanista siirtää 5.</span><span class="sxs-lookup"><span data-stu-id="e8f32-126">In this case, 2 kanbans transferring 5 each.</span></span>  
3. <span data-ttu-id="e8f32-127">Lisää Vähimmäisrajan hälytys -kenttään 1.</span><span class="sxs-lookup"><span data-stu-id="e8f32-127">In the Alert boundary minimum field, enter '1'.</span></span>
    * <span data-ttu-id="e8f32-128">Käytetään seuraamaan sellaisten täysien kanbanien vähimmäismäärää, joiden pitäisi olla päämäärässä.</span><span class="sxs-lookup"><span data-stu-id="e8f32-128">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="e8f32-129">Tätä käytetään esimerkiksi kanban-määrän yhteenvedossa.</span><span class="sxs-lookup"><span data-stu-id="e8f32-129">For example, this is used on the kanban quantity overview.</span></span>  
4. <span data-ttu-id="e8f32-130">Lisää Enimmäisrajan hälytys -kenttään 2.</span><span class="sxs-lookup"><span data-stu-id="e8f32-130">In the Alert boundary maximum field, enter '2'.</span></span>
    * <span data-ttu-id="e8f32-131">Käytetään seuraamaan sellaisten täysien kanbanien enimmäismäärää, joiden pitäisi olla päämäärässä.</span><span class="sxs-lookup"><span data-stu-id="e8f32-131">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="e8f32-132">Tätä käytetään esimerkiksi kanban-määrän yhteenvedossa.</span><span class="sxs-lookup"><span data-stu-id="e8f32-132">For example, this is used on the kanban quantity overview.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="e8f32-133">Luo kanbaneita</span><span class="sxs-lookup"><span data-stu-id="e8f32-133">Create kanbans</span></span>
1. <span data-ttu-id="e8f32-134">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="e8f32-134">Click Save.</span></span>
    * <span data-ttu-id="e8f32-135">Kanban-sääntö on tallennettava ennen kanbanien luomista.</span><span class="sxs-lookup"><span data-stu-id="e8f32-135">The kanban rule needs to be saved before kanbans can be created.</span></span>  
2. <span data-ttu-id="e8f32-136">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e8f32-136">Click Add.</span></span>
    * <span data-ttu-id="e8f32-137">Huomaa, että yksikään kanban ei ole aktiivinen, koska ehdotettu Uusien kanbanien määrä on 2. Tämä vastaa Kiinteä kanban-määrä -asetusta.</span><span class="sxs-lookup"><span data-stu-id="e8f32-137">Note that there are no active kanbans because the suggested 'Number of new kanbans' is 2, which is equal to the 'Fixed kanban quantity'.</span></span>  
3. <span data-ttu-id="e8f32-138">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="e8f32-138">Click Create.</span></span>
    * <span data-ttu-id="e8f32-139">Tämä luo kaksi kanbania.</span><span class="sxs-lookup"><span data-stu-id="e8f32-139">This will create two kanbans.</span></span>  
    * <span data-ttu-id="e8f32-140">Huomaa, että tälle ottamisen kanban-säännölle luotiin 2 kanbania, joista kunkin arvo on 5.</span><span class="sxs-lookup"><span data-stu-id="e8f32-140">Note that 2 kanbans, for 5 each, was created for this withdrawal kanban rule.</span></span>  <span data-ttu-id="e8f32-141">Tämä on tämän menettelyn viimeinen vaihe.</span><span class="sxs-lookup"><span data-stu-id="e8f32-141">This is the last step in this procedure.</span></span>  

