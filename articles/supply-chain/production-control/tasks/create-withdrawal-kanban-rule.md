---
title: Luo oton kanban-sääntö
description: Seuraavassa menettelyssä kuvataan tarvittavat määritykset ottamisen kanban-säännön luomiseen materiaalin siirtämiseksi lean-ympäristössä.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1694472e20c28a0b0f94c1ced8544b7258c22b40
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007088"
---
# <a name="create-a-withdrawal-kanban-rule"></a><span data-ttu-id="8b71a-103">Luo oton kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="8b71a-103">Create a withdrawal kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8b71a-104">Seuraavassa menettelyssä kuvataan tarvittavat määritykset ottamisen kanban-säännön luomiseen materiaalin siirtämiseksi lean-ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="8b71a-104">This procedure shows the setup that is needed to create a withdrawal kanban rule for transferring material in a lean environment.</span></span> <span data-ttu-id="8b71a-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="8b71a-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8b71a-106">Menettely on tarkoitettu prosessiteknikolle tai arvovirtaa hallitsevalle työntekijälle uuden tai muokatun materiaalin täydennyksen valmisteluun.</span><span class="sxs-lookup"><span data-stu-id="8b71a-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare replenishment of new or modified material.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="8b71a-107">Luo uusi kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="8b71a-107">Create new kanban rule</span></span>
1. <span data-ttu-id="8b71a-108">Valitse Kanban-säännöt.</span><span class="sxs-lookup"><span data-stu-id="8b71a-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="8b71a-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8b71a-109">Click New.</span></span>
3. <span data-ttu-id="8b71a-110">Valitse Tyyppi-kentän arvoksi "Otto".</span><span class="sxs-lookup"><span data-stu-id="8b71a-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="8b71a-111">Otto-tyyppiä käytetään kanban-säännössä tuotteiden tai materiaalin siirtoon.</span><span class="sxs-lookup"><span data-stu-id="8b71a-111">The Withdrawal type is used for kanban rules to transfer material or goods.</span></span>  
4. <span data-ttu-id="8b71a-112">Anna tai valitse Ensimmäinen suunnitelman tehtävä -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="8b71a-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="8b71a-113">Valitse ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="8b71a-113">Select ReplenishSpeakerComponents.</span></span>   <span data-ttu-id="8b71a-114">Tehtävä on määritetty siirtämään komponentteja varaston 11 toimipaikasta 11 varaston 12 toimipaikkaan 12.</span><span class="sxs-lookup"><span data-stu-id="8b71a-114">This activity is set up to move components from warehouse 11, location 11 to warehouse 12, and location 12.</span></span>  
5. <span data-ttu-id="8b71a-115">Anna tai valitse Tuote-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="8b71a-115">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="8b71a-116">Valitse M0007.</span><span class="sxs-lookup"><span data-stu-id="8b71a-116">Select M0007.</span></span>  
6. <span data-ttu-id="8b71a-117">Lisää Läpimenoaika-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="8b71a-117">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="8b71a-118">Esimerkki: 60.</span><span class="sxs-lookup"><span data-stu-id="8b71a-118">For example, 60.</span></span>  
7. <span data-ttu-id="8b71a-119">Anna tai valitse Mittayksikkö-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="8b71a-119">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="8b71a-120">Esimerkiksi minuutteja.</span><span class="sxs-lookup"><span data-stu-id="8b71a-120">For example, Minutes.</span></span>  

## <a name="set-quantities-for-kanban"></a><span data-ttu-id="8b71a-121">Määritä kanban-määrät</span><span class="sxs-lookup"><span data-stu-id="8b71a-121">Set quantities for kanban</span></span>
1. <span data-ttu-id="8b71a-122">Määritä Oletusmäärä-arvoksi 5.</span><span class="sxs-lookup"><span data-stu-id="8b71a-122">Set Default quantity to '5'.</span></span>
    * <span data-ttu-id="8b71a-123">Tämä määrä siirretään kullekin kanbanille.</span><span class="sxs-lookup"><span data-stu-id="8b71a-123">This is the quantity that will be transferred for each kanban.</span></span>  
2. <span data-ttu-id="8b71a-124">Syötä Kiinteä kanban-määrä -kentän arvoksi 2.</span><span class="sxs-lookup"><span data-stu-id="8b71a-124">In the Fixed kanban quantity field, enter '2'.</span></span>
    * <span data-ttu-id="8b71a-125">Tämä on sellaisten kanbanien määrä, joiden pitäisi olla aktiivisia.</span><span class="sxs-lookup"><span data-stu-id="8b71a-125">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="8b71a-126">Tällä tapauksessa jokainen 2 kanbanista siirtää 5.</span><span class="sxs-lookup"><span data-stu-id="8b71a-126">In this case, 2 kanbans transferring 5 each.</span></span>  
3. <span data-ttu-id="8b71a-127">Lisää Vähimmäisrajan hälytys -kenttään 1.</span><span class="sxs-lookup"><span data-stu-id="8b71a-127">In the Alert boundary minimum field, enter '1'.</span></span>
    * <span data-ttu-id="8b71a-128">Käytetään seuraamaan sellaisten täysien kanbanien vähimmäismäärää, joiden pitäisi olla päämäärässä.</span><span class="sxs-lookup"><span data-stu-id="8b71a-128">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="8b71a-129">Tätä käytetään esimerkiksi kanban-määrän yhteenvedossa.</span><span class="sxs-lookup"><span data-stu-id="8b71a-129">For example, this is used on the kanban quantity overview.</span></span>  
4. <span data-ttu-id="8b71a-130">Lisää Enimmäisrajan hälytys -kenttään 2.</span><span class="sxs-lookup"><span data-stu-id="8b71a-130">In the Alert boundary maximum field, enter '2'.</span></span>
    * <span data-ttu-id="8b71a-131">Käytetään seuraamaan sellaisten täysien kanbanien enimmäismäärää, joiden pitäisi olla päämäärässä.</span><span class="sxs-lookup"><span data-stu-id="8b71a-131">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="8b71a-132">Tätä käytetään esimerkiksi kanban-määrän yhteenvedossa.</span><span class="sxs-lookup"><span data-stu-id="8b71a-132">For example, this is used on the kanban quantity overview.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="8b71a-133">Luo kanbaneita</span><span class="sxs-lookup"><span data-stu-id="8b71a-133">Create kanbans</span></span>
1. <span data-ttu-id="8b71a-134">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8b71a-134">Click Save.</span></span>
    * <span data-ttu-id="8b71a-135">Kanban-sääntö on tallennettava ennen kanbanien luomista.</span><span class="sxs-lookup"><span data-stu-id="8b71a-135">The kanban rule needs to be saved before kanbans can be created.</span></span>  
2. <span data-ttu-id="8b71a-136">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="8b71a-136">Click Add.</span></span>
    * <span data-ttu-id="8b71a-137">Huomaa, että yksikään kanban ei ole aktiivinen, koska ehdotettu Uusien kanbanien määrä on 2. Tämä vastaa Kiinteä kanban-määrä -asetusta.</span><span class="sxs-lookup"><span data-stu-id="8b71a-137">Note that there are no active kanbans because the suggested 'Number of new kanbans' is 2, which is equal to the 'Fixed kanban quantity'.</span></span>  
3. <span data-ttu-id="8b71a-138">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="8b71a-138">Click Create.</span></span>
    * <span data-ttu-id="8b71a-139">Tämä luo kaksi kanbania.</span><span class="sxs-lookup"><span data-stu-id="8b71a-139">This will create two kanbans.</span></span>  
    * <span data-ttu-id="8b71a-140">Huomaa, että tälle ottamisen kanban-säännölle luotiin 2 kanbania, joista kunkin arvo on 5.</span><span class="sxs-lookup"><span data-stu-id="8b71a-140">Note that 2 kanbans, for 5 each, was created for this withdrawal kanban rule.</span></span>  <span data-ttu-id="8b71a-141">Tämä on tämän menettelyn viimeinen vaihe.</span><span class="sxs-lookup"><span data-stu-id="8b71a-141">This is the last step in this procedure.</span></span>  

