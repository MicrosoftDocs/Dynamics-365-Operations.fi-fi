---
title: Luo valmistuksen vakiomäärän kanban-sääntö
description: Tässä menettelyssä käsitellään määrityksiä, joita tarvitaan luotaessa kiinteää valmistuksen kanban-sääntöä, jolla käynnistetään muuntotehtävät Lean-ympäristön työsolussa.
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
ms.openlocfilehash: ff38ba2ed1d513d6b64cf5a64e021cbb08d69b21
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3161751"
---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a><span data-ttu-id="c81d8-103">Luo valmistuksen vakiomäärän kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="c81d8-103">Create a fixed quantity kanban rule for manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c81d8-104">Tässä menettelyssä käsitellään määrityksiä, joita tarvitaan luotaessa kiinteää valmistuksen kanban-sääntöä, jolla käynnistetään muuntotehtävät Lean-ympäristön työsolussa.</span><span class="sxs-lookup"><span data-stu-id="c81d8-104">This procedure focuses on the setup needed to create a fixed manufacturing kanban rule for triggering transforming activities, at a work cell, in a lean environment.</span></span> <span data-ttu-id="c81d8-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="c81d8-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c81d8-106">Menettely on tarkoitettu prosessiteknikolle tai arvovirtaa hallitsevalle työntekijälle uuden tai muokatun tuotteen tuotannon valmisteluun.</span><span class="sxs-lookup"><span data-stu-id="c81d8-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="c81d8-107">Luo uusi kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="c81d8-107">Create new kanban rule</span></span>
1. <span data-ttu-id="c81d8-108">Valitse Kanban-säännöt.</span><span class="sxs-lookup"><span data-stu-id="c81d8-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="c81d8-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c81d8-109">Click New.</span></span>
    * <span data-ttu-id="c81d8-110">Huomaa, että oletustyyppi on Valmistus ja Täydennysstrategia on Kiinteä.</span><span class="sxs-lookup"><span data-stu-id="c81d8-110">Notice that the default Type is Manufacturing and Replenishment strategy is Fixed.</span></span> <span data-ttu-id="c81d8-111">Näitä parametreja ei tarvitse muuttaa.</span><span class="sxs-lookup"><span data-stu-id="c81d8-111">You do not have to change these parameters.</span></span>  
3. <span data-ttu-id="c81d8-112">Anna tai valitse Ensimmäinen suunnitelman tehtävä -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="c81d8-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="c81d8-113">Tämä tehtävä tehdään tämän kanban-säännön perusteella luoduissa kanbaneissa.</span><span class="sxs-lookup"><span data-stu-id="c81d8-113">This is the activity that will be performed for kanbans created based on this kanban rule.</span></span>  <span data-ttu-id="c81d8-114">Valitse SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="c81d8-114">Select 'SpeakerTestAndPackaging'.</span></span>  
4. <span data-ttu-id="c81d8-115">Laajenna Tiedot-osa.</span><span class="sxs-lookup"><span data-stu-id="c81d8-115">Expand the Details section.</span></span>
5. <span data-ttu-id="c81d8-116">Anna tai valitse Tuote-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="c81d8-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="c81d8-117">Valitse L0050.</span><span class="sxs-lookup"><span data-stu-id="c81d8-117">Select L0050.</span></span>  
6. <span data-ttu-id="c81d8-118">Anna tai valitse Mittayksikkö-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="c81d8-118">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="c81d8-119">Valitse minuutit.</span><span class="sxs-lookup"><span data-stu-id="c81d8-119">Select minutes.</span></span>  
7. <span data-ttu-id="c81d8-120">Lisää Läpimenoaika-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c81d8-120">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="c81d8-121">Anna 5.</span><span class="sxs-lookup"><span data-stu-id="c81d8-121">Enter 5.</span></span>  

## <a name="set-quantities"></a><span data-ttu-id="c81d8-122">Määritä määrät</span><span class="sxs-lookup"><span data-stu-id="c81d8-122">Set quantities</span></span>
1. <span data-ttu-id="c81d8-123">Laajenna Määrät-osa.</span><span class="sxs-lookup"><span data-stu-id="c81d8-123">Expand the Quantities section.</span></span>
2. <span data-ttu-id="c81d8-124">Määritä Oletusmäärä-arvoksi 10.</span><span class="sxs-lookup"><span data-stu-id="c81d8-124">Set Default quantity to '10'.</span></span>
    * <span data-ttu-id="c81d8-125">Tämä määrä siirretään kullekin kanbanille.</span><span class="sxs-lookup"><span data-stu-id="c81d8-125">This is the quantity that will be transferred for each kanban.</span></span>  
3. <span data-ttu-id="c81d8-126">Valitse Tuotemäärän varianssi -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="c81d8-126">Select the Product quantity variance check box.</span></span>
    * <span data-ttu-id="c81d8-127">Valitut kanbanit voidaan toteuttaa tämän avulla oletusmäärän varianssilla.</span><span class="sxs-lookup"><span data-stu-id="c81d8-127">With this, selected kanbans can be completed with a variance from the default quantity.</span></span>  <span data-ttu-id="c81d8-128">Jotta kanbanit voitaisiin toteuttaa määrällä 8–12, määritä molempien varianssien arvoksi 2.</span><span class="sxs-lookup"><span data-stu-id="c81d8-128">To allow kanbans to be completed with a quantity from 8 to 12, set both variances to 2.</span></span>  
4. <span data-ttu-id="c81d8-129">Määritä Poikkeaman alla -arvoksi 2.</span><span class="sxs-lookup"><span data-stu-id="c81d8-129">Set Variance below to '2'.</span></span>
    * <span data-ttu-id="c81d8-130">Tällöin myös pienempi toteutus on mahdollinen 10–2=8</span><span class="sxs-lookup"><span data-stu-id="c81d8-130">This will allow completing down to 10 - 2 = 8</span></span>  
5. <span data-ttu-id="c81d8-131">Määritä Poikkeaman yllä -arvoksi 2.</span><span class="sxs-lookup"><span data-stu-id="c81d8-131">Set Variance above to '2'.</span></span>
    * <span data-ttu-id="c81d8-132">Tällöin myös suurempi toteutus on mahdollinen 10+2=12</span><span class="sxs-lookup"><span data-stu-id="c81d8-132">This will allow completing up to 10 + 2 = 12</span></span>  
6. <span data-ttu-id="c81d8-133">Lisää Kiinteä kanban-määrä -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c81d8-133">In the Fixed kanban quantity field, enter a number.</span></span>
    * <span data-ttu-id="c81d8-134">Tämä on sellaisten kanbanien määrä, joiden pitäisi olla aktiivisia.</span><span class="sxs-lookup"><span data-stu-id="c81d8-134">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="c81d8-135">Tällä tapauksessa jokainen 5 kanbanista käsittelee 10.</span><span class="sxs-lookup"><span data-stu-id="c81d8-135">In this case, 5 kanbans processing 10 each.</span></span>  
7. <span data-ttu-id="c81d8-136">Lisää Vähimmäisrajan hälytys -kenttään 2.</span><span class="sxs-lookup"><span data-stu-id="c81d8-136">In the Alert boundary minimum field, enter '2'.</span></span>
    * <span data-ttu-id="c81d8-137">Käytetään seuraamaan sellaisten täysien kanbanien vähimmäismäärää, joiden pitäisi olla päämäärässä.</span><span class="sxs-lookup"><span data-stu-id="c81d8-137">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="c81d8-138">Tätä käytetään esimerkiksi kanban-määrän yhteenvedossa.</span><span class="sxs-lookup"><span data-stu-id="c81d8-138">For example, this is used on the kanban quantity overview.</span></span>  
8. <span data-ttu-id="c81d8-139">Lisää Enimmäisrajan hälytys -kenttään 4.</span><span class="sxs-lookup"><span data-stu-id="c81d8-139">In the Alert boundary maximum field, enter '4'.</span></span>
    * <span data-ttu-id="c81d8-140">Käytetään seuraamaan sellaisten täysien kanbanien enimmäismäärää, joiden pitäisi olla päämäärässä.</span><span class="sxs-lookup"><span data-stu-id="c81d8-140">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="c81d8-141">Tätä käytetään esimerkiksi kanban-määrän yhteenvedossa.</span><span class="sxs-lookup"><span data-stu-id="c81d8-141">For example, this is used on the kanban quantity overview.</span></span>  
9. <span data-ttu-id="c81d8-142">Lisää Automaattisen suunnittelun määrä -kenttään 1.</span><span class="sxs-lookup"><span data-stu-id="c81d8-142">In the Automatic planning quantity field, enter '1'.</span></span>
    * <span data-ttu-id="c81d8-143">Kun arvoksi on määritetty 1, jokainen kanban suunnitellaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="c81d8-143">Setting this to 1 means that every kanban will be automatically planned.</span></span>   <span data-ttu-id="c81d8-144">Jos arvoksi annetaan 3, kanbaneja ei suunnitella, ennen kuin 3 tyhjää kanbania on valmiita suunnitteluun.</span><span class="sxs-lookup"><span data-stu-id="c81d8-144">If we entered 3, the kanbans would not be planned until 3 empty kanbans are ready for planning.</span></span> <span data-ttu-id="c81d8-145">Tämä on kätevää töiden ryhmittelyssä, ja sillä vältetään liialliset asetukset.</span><span class="sxs-lookup"><span data-stu-id="c81d8-145">This is useful for grouping work and avoiding too much setup.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="c81d8-146">Luo kanbaneita</span><span class="sxs-lookup"><span data-stu-id="c81d8-146">Create Kanbans</span></span>
1. <span data-ttu-id="c81d8-147">Laajenna Kanbanit-osa.</span><span class="sxs-lookup"><span data-stu-id="c81d8-147">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="c81d8-148">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c81d8-148">Click Save.</span></span>
    * <span data-ttu-id="c81d8-149">Kanban-sääntö on tallennettava ennen kanbanien luomista.</span><span class="sxs-lookup"><span data-stu-id="c81d8-149">The kanban rule needs to be saved before kanbans can be created.</span></span>  
3. <span data-ttu-id="c81d8-150">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="c81d8-150">Click Add.</span></span>
    * <span data-ttu-id="c81d8-151">Huomaa, että yksikään kanban ei ole aktiivinen, minkä vuoksi ehdotettu uusien kanbanien määrä on 5.</span><span class="sxs-lookup"><span data-stu-id="c81d8-151">Note that there are no active kanbans, due to this the suggested 'Number of new kanbans' are 5.</span></span> <span data-ttu-id="c81d8-152">Tämä vastaa Kiinteä kanban-määrä -asetusta.</span><span class="sxs-lookup"><span data-stu-id="c81d8-152">This is equal to the 'Fixed kanban quantity'.</span></span>  
4. <span data-ttu-id="c81d8-153">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="c81d8-153">Click Create.</span></span>
    * <span data-ttu-id="c81d8-154">Tämä luo 5 kanbania.</span><span class="sxs-lookup"><span data-stu-id="c81d8-154">This will create 5 kanbans.</span></span>  
    * <span data-ttu-id="c81d8-155">Huomaa, että tälle valmistuksen kanban-säännölle luotiin 5 kanbania, joista kunkin arvo on 10.</span><span class="sxs-lookup"><span data-stu-id="c81d8-155">Note that 5 kanbans, for 10 each, was created for this manufacturing kanban rule.</span></span> <span data-ttu-id="c81d8-156">Tämä on tämän menettelyn viimeinen vaihe.</span><span class="sxs-lookup"><span data-stu-id="c81d8-156">This is the last step in this procedure.</span></span>  

