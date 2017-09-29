--- 
title: "Luo valmistuksen vakiomäärän kanban-sääntö"
description: "Tässä menettelyssä käsitellään määrityksiä, joita tarvitaan luotaessa kiinteää valmistuksen kanban-sääntöä, jolla käynnistetään muuntotehtävät Lean-ympäristön työsolussa."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8020a37bf0c725fc260574cfe87861aeb017519e
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a><span data-ttu-id="080ca-103">Luo valmistuksen vakiomäärän kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="080ca-103">Create a fixed quantity kanban rule for manufacturing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="080ca-104">Tässä menettelyssä käsitellään määrityksiä, joita tarvitaan luotaessa kiinteää valmistuksen kanban-sääntöä, jolla käynnistetään muuntotehtävät Lean-ympäristön työsolussa.</span><span class="sxs-lookup"><span data-stu-id="080ca-104">This procedure focuses on the setup needed to create a fixed manufacturing kanban rule for triggering transforming activities, at a work cell, in a lean environment.</span></span> <span data-ttu-id="080ca-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="080ca-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="080ca-106">Menettely on tarkoitettu prosessiteknikolle tai arvovirtaa hallitsevalle työntekijälle uuden tai muokatun tuotteen tuotannon valmisteluun.</span><span class="sxs-lookup"><span data-stu-id="080ca-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="080ca-107">Luo uusi kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="080ca-107">Create new kanban rule</span></span>
1. <span data-ttu-id="080ca-108">Valitse Kanban-säännöt.</span><span class="sxs-lookup"><span data-stu-id="080ca-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="080ca-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="080ca-109">Click New.</span></span>
    * <span data-ttu-id="080ca-110">Huomaa, että oletustyyppi on Valmistus ja Täydennysstrategia on Kiinteä.</span><span class="sxs-lookup"><span data-stu-id="080ca-110">Notice that the default Type is Manufacturing and Replenishment strategy is Fixed.</span></span> <span data-ttu-id="080ca-111">Näitä parametreja ei tarvitse muuttaa.</span><span class="sxs-lookup"><span data-stu-id="080ca-111">You do not have to change these parameters.</span></span>  
3. <span data-ttu-id="080ca-112">Anna tai valitse Ensimmäinen suunnitelman tehtävä -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="080ca-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="080ca-113">Tämä tehtävä tehdään tämän kanban-säännön perusteella luoduissa kanbaneissa.</span><span class="sxs-lookup"><span data-stu-id="080ca-113">This is the activity that will be performed for kanbans created based on this kanban rule.</span></span>  <span data-ttu-id="080ca-114">Valitse SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="080ca-114">Select 'SpeakerTestAndPackaging'.</span></span>  
4. <span data-ttu-id="080ca-115">Laajenna Tiedot-osa.</span><span class="sxs-lookup"><span data-stu-id="080ca-115">Expand the Details section.</span></span>
5. <span data-ttu-id="080ca-116">Anna tai valitse Tuote-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="080ca-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="080ca-117">Valitse L0050.</span><span class="sxs-lookup"><span data-stu-id="080ca-117">Select L0050.</span></span>  
6. <span data-ttu-id="080ca-118">Anna tai valitse Mittayksikkö-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="080ca-118">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="080ca-119">Valitse minuutit.</span><span class="sxs-lookup"><span data-stu-id="080ca-119">Select minutes.</span></span>  
7. <span data-ttu-id="080ca-120">Lisää Läpimenoaika-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="080ca-120">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="080ca-121">Anna 5.</span><span class="sxs-lookup"><span data-stu-id="080ca-121">Enter 5.</span></span>  

## <a name="set-quantities"></a><span data-ttu-id="080ca-122">Määritä määrät</span><span class="sxs-lookup"><span data-stu-id="080ca-122">Set quantities</span></span>
1. <span data-ttu-id="080ca-123">Laajenna Määrät-osa.</span><span class="sxs-lookup"><span data-stu-id="080ca-123">Expand the Quantities section.</span></span>
2. <span data-ttu-id="080ca-124">Määritä Oletusmäärä-arvoksi 10.</span><span class="sxs-lookup"><span data-stu-id="080ca-124">Set Default quantity to '10'.</span></span>
    * <span data-ttu-id="080ca-125">Tämä määrä siirretään kullekin kanbanille.</span><span class="sxs-lookup"><span data-stu-id="080ca-125">This is the quantity that will be transferred for each kanban.</span></span>  
3. <span data-ttu-id="080ca-126">Valitse Tuotemäärän varianssi -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="080ca-126">Select the Product quantity variance check box.</span></span>
    * <span data-ttu-id="080ca-127">Valitut kanbanit voidaan toteuttaa tämän avulla oletusmäärän varianssilla.</span><span class="sxs-lookup"><span data-stu-id="080ca-127">With this, selected kanbans can be completed with a variance from the default quantity.</span></span>  <span data-ttu-id="080ca-128">Jotta kanbanit voitaisiin toteuttaa määrällä 8–12, määritä molempien varianssien arvoksi 2.</span><span class="sxs-lookup"><span data-stu-id="080ca-128">To allow kanbans to be completed with a quantity from 8 to 12, set both variances to 2.</span></span>  
4. <span data-ttu-id="080ca-129">Määritä Poikkeaman alla -arvoksi 2.</span><span class="sxs-lookup"><span data-stu-id="080ca-129">Set Variance below to '2'.</span></span>
    * <span data-ttu-id="080ca-130">Tällöin myös pienempi toteutus on mahdollinen 10–2=8</span><span class="sxs-lookup"><span data-stu-id="080ca-130">This will allow completing down to 10 - 2 = 8</span></span>  
5. <span data-ttu-id="080ca-131">Määritä Poikkeaman yllä -arvoksi 2.</span><span class="sxs-lookup"><span data-stu-id="080ca-131">Set Variance above to '2'.</span></span>
    * <span data-ttu-id="080ca-132">Tällöin myös suurempi toteutus on mahdollinen 10+2=12</span><span class="sxs-lookup"><span data-stu-id="080ca-132">This will allow completing up to 10 + 2 = 12</span></span>  
6. <span data-ttu-id="080ca-133">Lisää Kiinteä kanban-määrä -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="080ca-133">In the Fixed kanban quantity field, enter a number.</span></span>
    * <span data-ttu-id="080ca-134">Tämä on sellaisten kanbanien määrä, joiden pitäisi olla aktiivisia.</span><span class="sxs-lookup"><span data-stu-id="080ca-134">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="080ca-135">Tällä tapauksessa jokainen 5 kanbanista käsittelee 10.</span><span class="sxs-lookup"><span data-stu-id="080ca-135">In this case, 5 kanbans processing 10 each.</span></span>  
7. <span data-ttu-id="080ca-136">Lisää Vähimmäisrajan hälytys -kenttään 2.</span><span class="sxs-lookup"><span data-stu-id="080ca-136">In the Alert boundary minimum field, enter '2'.</span></span>
    * <span data-ttu-id="080ca-137">Käytetään seuraamaan sellaisten täysien kanbanien vähimmäismäärää, joiden pitäisi olla päämäärässä.</span><span class="sxs-lookup"><span data-stu-id="080ca-137">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="080ca-138">Tätä käytetään esimerkiksi kanban-määrän yhteenvedossa.</span><span class="sxs-lookup"><span data-stu-id="080ca-138">For example, this is used on the kanban quantity overview.</span></span>  
8. <span data-ttu-id="080ca-139">Lisää Enimmäisrajan hälytys -kenttään 4.</span><span class="sxs-lookup"><span data-stu-id="080ca-139">In the Alert boundary maximum field, enter '4'.</span></span>
    * <span data-ttu-id="080ca-140">Käytetään seuraamaan sellaisten täysien kanbanien enimmäismäärää, joiden pitäisi olla päämäärässä.</span><span class="sxs-lookup"><span data-stu-id="080ca-140">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="080ca-141">Tätä käytetään esimerkiksi kanban-määrän yhteenvedossa.</span><span class="sxs-lookup"><span data-stu-id="080ca-141">For example, this is used on the kanban quantity overview.</span></span>  
9. <span data-ttu-id="080ca-142">Lisää Automaattisen suunnittelun määrä -kenttään 1.</span><span class="sxs-lookup"><span data-stu-id="080ca-142">In the Automatic planning quantity field, enter '1'.</span></span>
    * <span data-ttu-id="080ca-143">Kun arvoksi on määritetty 1, jokainen kanban suunnitellaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="080ca-143">Setting this to 1 means that every kanban will be automatically planned.</span></span>   <span data-ttu-id="080ca-144">Jos arvoksi annetaan 3, kanbaneja ei suunnitella, ennen kuin 3 tyhjää kanbania on valmiita suunnitteluun.</span><span class="sxs-lookup"><span data-stu-id="080ca-144">If we entered 3, the kanbans would not be planned until 3 empty kanbans are ready for planning.</span></span> <span data-ttu-id="080ca-145">Tämä on kätevää töiden ryhmittelyssä, ja sillä vältetään liialliset asetukset.</span><span class="sxs-lookup"><span data-stu-id="080ca-145">This is useful for grouping work and avoiding too much setup.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="080ca-146">Luo kanbaneita</span><span class="sxs-lookup"><span data-stu-id="080ca-146">Create Kanbans</span></span>
1. <span data-ttu-id="080ca-147">Laajenna Kanbanit-osa.</span><span class="sxs-lookup"><span data-stu-id="080ca-147">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="080ca-148">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="080ca-148">Click Save.</span></span>
    * <span data-ttu-id="080ca-149">Kanban-sääntö on tallennettava ennen kanbanien luomista.</span><span class="sxs-lookup"><span data-stu-id="080ca-149">The kanban rule needs to be saved before kanbans can be created.</span></span>  
3. <span data-ttu-id="080ca-150">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="080ca-150">Click Add.</span></span>
    * <span data-ttu-id="080ca-151">Huomaa, että yksikään kanban ei ole aktiivinen, minkä vuoksi ehdotettu uusien kanbanien määrä on 5.</span><span class="sxs-lookup"><span data-stu-id="080ca-151">Note that there are no active kanbans, due to this the suggested 'Number of new kanbans' are 5.</span></span> <span data-ttu-id="080ca-152">Tämä vastaa Kiinteä kanban-määrä -asetusta.</span><span class="sxs-lookup"><span data-stu-id="080ca-152">This is equal to the 'Fixed kanban quantity'.</span></span>  
4. <span data-ttu-id="080ca-153">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="080ca-153">Click Create.</span></span>
    * <span data-ttu-id="080ca-154">Tämä luo 5 kanbania.</span><span class="sxs-lookup"><span data-stu-id="080ca-154">This will create 5 kanbans.</span></span>  
    * <span data-ttu-id="080ca-155">Huomaa, että tälle valmistuksen kanban-säännölle luotiin 5 kanbania, joista kunkin arvo on 10.</span><span class="sxs-lookup"><span data-stu-id="080ca-155">Note that 5 kanbans, for 10 each, was created for this manufacturing kanban rule.</span></span> <span data-ttu-id="080ca-156">Tämä on tämän menettelyn viimeinen vaihe.</span><span class="sxs-lookup"><span data-stu-id="080ca-156">This is the last step in this procedure.</span></span>  


