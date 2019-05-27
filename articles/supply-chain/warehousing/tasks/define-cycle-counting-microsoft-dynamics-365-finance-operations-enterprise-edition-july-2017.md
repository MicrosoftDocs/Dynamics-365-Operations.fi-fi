---
title: Inventoinnin määrittäminen
description: Inventointi on varastoprosessi, jota voit käyttää käytettävissä olevien varastonimikkeiden tarkastamiseen.
author: MarkusFogelberg
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
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2832547f81b0153d42ac4664184f18bd66f1acdd
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571669"
---
# <a name="define-cycle-counting"></a><span data-ttu-id="9a286-103">Inventoinnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9a286-103">Define cycle counting</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9a286-104">Inventointi on varastoprosessi, jota voit käyttää käytettävissä olevien varastonimikkeiden tarkastamiseen.</span><span class="sxs-lookup"><span data-stu-id="9a286-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="9a286-105">Tämän tehtävän tallenne osoittaa, miten oletusinventointityön prioriteetti määritetään, miten mobiililaitteen valikkovaihtoehto otetaan käyttöön käsittelemään keräys- ja inventointitoimintoja, miten tyhjäksi tulevasta sijainnista käynnistyvä inventointiraja otetaan käyttöön ja miten tietyn nimikkeen inventointisuunnitelma otetaan käyttöön tietyssä varastossa.</span><span class="sxs-lookup"><span data-stu-id="9a286-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="9a286-106">Varastopäällikkö tekee yleensä nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="9a286-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="9a286-107">Voit käyttää tässä menettelyssä USMF-yrityksen demotietoja tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="9a286-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="9a286-108">Määritä inventointityön prioriteetti</span><span class="sxs-lookup"><span data-stu-id="9a286-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="9a286-109">Valitse Varastonhallinta > Asetukset > Varastonhallinnan parametrit.</span><span class="sxs-lookup"><span data-stu-id="9a286-109">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="9a286-110">Valitse Inventointi-välilehti.</span><span class="sxs-lookup"><span data-stu-id="9a286-110">Click the Cycle counting tab.</span></span>
3. <span data-ttu-id="9a286-111">Lisää Inventointityön oletusprioriteetti -kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="9a286-111">In the Default cycle count work priority field, enter a number.</span></span>
    * <span data-ttu-id="9a286-112">Tämä vaihe muuttaa inventointityön prioriteettia verrattuna varaston muihin työtyyppeihin.</span><span class="sxs-lookup"><span data-stu-id="9a286-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="9a286-113">Kun syötät luvun, joka on alhaisempi kuin muiden työtyyppien luku, inventointityön prioriteetti nousee.</span><span class="sxs-lookup"><span data-stu-id="9a286-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="9a286-114">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9a286-114">Click Save.</span></span>
5. <span data-ttu-id="9a286-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9a286-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="9a286-116">Ota mobiililaite käyttöön</span><span class="sxs-lookup"><span data-stu-id="9a286-116">Enable the mobile device</span></span>
1. <span data-ttu-id="9a286-117">Valitse Varastonhallinta > Asetukset > Mobiililaite > Mobiililaitteen valikkovaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="9a286-117">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="9a286-118">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9a286-118">Click New.</span></span>
3. <span data-ttu-id="9a286-119">Kirjoita arvo Valikkovaihtoehdon nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9a286-119">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="9a286-120">Kirjoita Otsikko-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="9a286-120">In the Title field, type a value.</span></span>
5. <span data-ttu-id="9a286-121">Valitse Tila-kentässä Työ.</span><span class="sxs-lookup"><span data-stu-id="9a286-121">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="9a286-122">Valitse Käytä nykyistä työtä -vaihtoehdossa Kyllä.</span><span class="sxs-lookup"><span data-stu-id="9a286-122">Set the Use existing work option to Yes.</span></span>
    * <span data-ttu-id="9a286-123">Kun määrität tämän vaihtoehdon arvoksi Kyllä, järjestelmä etsii aiemmin luotua työtä, kun mobiililaitteen valikkovaihtoehtoa käytetään.</span><span class="sxs-lookup"><span data-stu-id="9a286-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="9a286-124">Valitse Ohjaaja-kentässä Järjestelmäohjattu.</span><span class="sxs-lookup"><span data-stu-id="9a286-124">In the Directed by field, select 'System directed'.</span></span>
    * <span data-ttu-id="9a286-125">Jos valitaan Järjestelmäohjattu, varastotyöntekijä ohjataan määritetyissä luokissa olevaan avoimeen työhön.</span><span class="sxs-lookup"><span data-stu-id="9a286-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="9a286-126">(Nämä työluokat luodaan seuraavaksi.)</span><span class="sxs-lookup"><span data-stu-id="9a286-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="9a286-127">Laajenna tai tiivistä Työluokat-osa.</span><span class="sxs-lookup"><span data-stu-id="9a286-127">Expand or collapse the Work classes section.</span></span>
    * <span data-ttu-id="9a286-128">Seuraavaksi luodaan kaksi työluokkaa, joita käytetään mobiililaitteen valikkovaihtoehdon kanssa.</span><span class="sxs-lookup"><span data-stu-id="9a286-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="9a286-129">Kun valikkovaihtoehtoa käytetään, näissä työluokissa voidaan tehdä kyselyjä ja käyttäjälle näytetään työ, jolla on suurin prioriteetti.</span><span class="sxs-lookup"><span data-stu-id="9a286-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="9a286-130">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9a286-130">Click New.</span></span>
10. <span data-ttu-id="9a286-131">Valitse Työluokan tunnus -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="9a286-131">In the Work class ID field, select a value.</span></span>
11. <span data-ttu-id="9a286-132">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9a286-132">Click New.</span></span>
12. <span data-ttu-id="9a286-133">Valitse Työluokan tunnus -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="9a286-133">In the Work class ID field, select a value.</span></span>
13. <span data-ttu-id="9a286-134">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9a286-134">Click Save.</span></span>
14. <span data-ttu-id="9a286-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9a286-135">Close the page.</span></span>
15. <span data-ttu-id="9a286-136">Valitse Varastonhallinta > Asetukset > Mobiililaite > Mobiililaitteen valikko.</span><span class="sxs-lookup"><span data-stu-id="9a286-136">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
16. <span data-ttu-id="9a286-137">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="9a286-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="9a286-138">Valitse puusta juuri luotu valikkovaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="9a286-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="9a286-139">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="9a286-139">Click Edit.</span></span>
19. <span data-ttu-id="9a286-140">Lisää valikkovaihtoehto valikkoon nuolen avulla.</span><span class="sxs-lookup"><span data-stu-id="9a286-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="9a286-141">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9a286-141">Click Save.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="9a286-142">Luo inventointiraja</span><span class="sxs-lookup"><span data-stu-id="9a286-142">Create a counting threshold</span></span>
1. <span data-ttu-id="9a286-143">Valitse Varastonhallinta > Asetukset > Inventointi > Inventointirajat.</span><span class="sxs-lookup"><span data-stu-id="9a286-143">Go to Warehouse management > Setup > Cycle counting > Cycle count thresholds.</span></span>
2. <span data-ttu-id="9a286-144">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9a286-144">Click New.</span></span>
3. <span data-ttu-id="9a286-145">Kirjoita Inventointirajan tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="9a286-145">In the Cycle counting threshold ID field, type a value.</span></span>
4. <span data-ttu-id="9a286-146">Valitse Käsittele inventointi heti -asetukseksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="9a286-146">Set the Process cycle counting immediately option to Yes.</span></span>
5. <span data-ttu-id="9a286-147">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9a286-147">In the Description field, type a value.</span></span>
6. <span data-ttu-id="9a286-148">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9a286-148">Click Save.</span></span>
7. <span data-ttu-id="9a286-149">Valitse Valitse sijainnit.</span><span class="sxs-lookup"><span data-stu-id="9a286-149">Click Select locations.</span></span>
8. <span data-ttu-id="9a286-150">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="9a286-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="9a286-151">Valitse Ehdot-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="9a286-151">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="9a286-152">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9a286-152">Click OK.</span></span>
11. <span data-ttu-id="9a286-153">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9a286-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="9a286-154">Luo inventointisuunnitelma</span><span class="sxs-lookup"><span data-stu-id="9a286-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="9a286-155">Valitse Varastonhallinta > Asetukset > Inventointi > Inventointisuunnitelmat.</span><span class="sxs-lookup"><span data-stu-id="9a286-155">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="9a286-156">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9a286-156">Click New.</span></span>
3. <span data-ttu-id="9a286-157">Kirjoita Inventointisuunnitelman tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="9a286-157">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="9a286-158">Kirjoita Kuvaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="9a286-158">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9a286-159">Lisää Inventointien enimmäismäärä -kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="9a286-159">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="9a286-160">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9a286-160">Click Save.</span></span>
7. <span data-ttu-id="9a286-161">Valitse Valitse sijainnit.</span><span class="sxs-lookup"><span data-stu-id="9a286-161">Click Select locations.</span></span>
8. <span data-ttu-id="9a286-162">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="9a286-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="9a286-163">Valitse Ehdot-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="9a286-163">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="9a286-164">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9a286-164">Click OK.</span></span>
11. <span data-ttu-id="9a286-165">Lisää Inventointien välissä olevat päivät -kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="9a286-165">In the Days between cycle counting field, enter a number.</span></span>
    * <span data-ttu-id="9a286-166">Jos esimerkiksi jos Inventointien välissä olevat päivät -kentän arvoksi määritetään 5, inventointityö luodaan viiden päivän välein.</span><span class="sxs-lookup"><span data-stu-id="9a286-166">For example, if the Days between cycle counting field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="9a286-167">Jos inventointityöt käsitellään kolmantena päivänä, seuraava inventointityö luodaan viiden päivän jälkeen viimeisestä inventoinnista eli kahdeksantena päivänä.</span><span class="sxs-lookup"><span data-stu-id="9a286-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="9a286-168">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9a286-168">Click Save.</span></span>
13. <span data-ttu-id="9a286-169">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9a286-169">Click New.</span></span>
14. <span data-ttu-id="9a286-170">Syötä Järjestysnumero-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="9a286-170">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="9a286-171">Lajittelujärjestys on pienimmästä numerosta suurimpaan.</span><span class="sxs-lookup"><span data-stu-id="9a286-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="9a286-172">Arvon on oltava suurempi kuin 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="9a286-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="9a286-173">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="9a286-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="9a286-174">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9a286-174">In the Description field, type a value.</span></span>
17. <span data-ttu-id="9a286-175">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9a286-175">Click Save.</span></span>
18. <span data-ttu-id="9a286-176">Valitse Määritä tuotekysely.</span><span class="sxs-lookup"><span data-stu-id="9a286-176">Click Define product query.</span></span>
19. <span data-ttu-id="9a286-177">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="9a286-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="9a286-178">Syötä tai valitse arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9a286-178">In the Criteria field, enter or select a value.</span></span>
21. <span data-ttu-id="9a286-179">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9a286-179">Click OK.</span></span>
22. <span data-ttu-id="9a286-180">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9a286-180">Close the page.</span></span>

