---
title: Määritä konttiinpakkaus
description: Tässä menettelyssä kuvataan, kuinka voit automatisoida kuormien konttiinpakkauksen Varastonhallinnassa.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 56fc6adc2a0eeb5b824089ff4b1b781f3a99a34c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558053"
---
# <a name="set-up-containerization"></a><span data-ttu-id="c5874-103">Määritä konttiinpakkaus</span><span class="sxs-lookup"><span data-stu-id="c5874-103">Set up containerization</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c5874-104">Tässä menettelyssä kuvataan, kuinka voit automatisoida kuormien konttiinpakkauksen Varastonhallinnassa.</span><span class="sxs-lookup"><span data-stu-id="c5874-104">This procedure describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="c5874-105">Automaattinen konttiinpakkaus luo lähetyksille kontit ja keräilytyöt kun aalto käsitellään, ja työrivit voidaan jakaa määriin, jotka sopivat kontteihin.</span><span class="sxs-lookup"><span data-stu-id="c5874-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="c5874-106">Tämän avulla varastotyöntekijän voivat keräillä nimikkeet suoraan valittuun konttiin.</span><span class="sxs-lookup"><span data-stu-id="c5874-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="c5874-107">Manuaaliseen pakkauskäsittelyyn verrattuna järjestelmä automatisoi tehtäviä, kuten konttien luonnin, nimikkeiden liittämisen ja konttien sulkemisen.</span><span class="sxs-lookup"><span data-stu-id="c5874-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="c5874-108">Tässä menettelyssä käytetään esittely-yritystä USMF, ja sen suorittaa varastopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="c5874-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="c5874-109">Aaltomallin asetuksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c5874-109">Set up a wave template</span></span>
1. <span data-ttu-id="c5874-110">Valitse Varastonhallinta > Asetukset > Aallot > Aaltomallit.</span><span class="sxs-lookup"><span data-stu-id="c5874-110">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="c5874-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c5874-111">Click New.</span></span>
3. <span data-ttu-id="c5874-112">Syötä Aaltomallin nimi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="c5874-112">In the Wave template name field, type a value.</span></span>
4. <span data-ttu-id="c5874-113">Kirjoita Aaltomallin kuvaus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="c5874-113">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="c5874-114">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c5874-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="c5874-115">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="c5874-115">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="c5874-116">Laajenna Menetelmät-osa.</span><span class="sxs-lookup"><span data-stu-id="c5874-116">Expand the Methods section.</span></span>
    * <span data-ttu-id="c5874-117">Valitut menetelmät -ruudussa näkyvät valitun aaltomallin tyypin menetelmät.</span><span class="sxs-lookup"><span data-stu-id="c5874-117">The Selected methods pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="c5874-118">Aaltomallin on sisällettävä pakkaa konttiin -menetelmä.</span><span class="sxs-lookup"><span data-stu-id="c5874-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="c5874-119">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="c5874-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="c5874-120">Kirjoita arvo Aallon vaihekoodi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c5874-120">In the Wave step code field, type a value.</span></span>
    * <span data-ttu-id="c5874-121">Kirjoita aaltovaiheen koodi lisätylle menetelmälle, joka voi olla mikä tahansa koodi.</span><span class="sxs-lookup"><span data-stu-id="c5874-121">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="c5874-122">Voit lisätä menetelmän useammin kuin kerran ja määrittää sille eri aaltovaiheen koodit.</span><span class="sxs-lookup"><span data-stu-id="c5874-122">It’s possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="c5874-123">Valitse tällöin Toistettava-asetus tälle menetelmälle Aallon käsittelymenetelmät -sivulla</span><span class="sxs-lookup"><span data-stu-id="c5874-123">To do this, select Repeatable for this method in the Wave process methods page.</span></span>  
10. <span data-ttu-id="c5874-124">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c5874-124">Click Save.</span></span>
11. <span data-ttu-id="c5874-125">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c5874-125">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="c5874-126">Määritä konttityyppi</span><span class="sxs-lookup"><span data-stu-id="c5874-126">Set up a container type</span></span>
1. <span data-ttu-id="c5874-127">Valitse Varastonhallinta > Asetukset > Kontit > Konttityypit.</span><span class="sxs-lookup"><span data-stu-id="c5874-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
    * <span data-ttu-id="c5874-128">Voit määrittää haluamasi kontit Konttityypit-sivulla.</span><span class="sxs-lookup"><span data-stu-id="c5874-128">You can define your containers in the Container types page.</span></span> <span data-ttu-id="c5874-129">Voit määrittää konttien fyysiset dimensiot, kuten taarapainon, enimmäispainon, enimmäistilavuuden, pituuden, leveyden ja korkeuden.</span><span class="sxs-lookup"><span data-stu-id="c5874-129">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="c5874-130">Tässä esimerkissä on kolmea eri kokoista laatikkoa.</span><span class="sxs-lookup"><span data-stu-id="c5874-130">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="c5874-131">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c5874-131">Click New.</span></span>
3. <span data-ttu-id="c5874-132">Kirjoita arvo Konttityyppi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c5874-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="c5874-133">Syötä Taarapaino-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c5874-133">In the Tare weight field, enter a number.</span></span>
5. <span data-ttu-id="c5874-134">Lisää Enimmäispaino-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c5874-134">In the Maximum weight field, enter a number.</span></span>
6. <span data-ttu-id="c5874-135">Syötä Tilavuus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c5874-135">In the Volume field, enter a number.</span></span>
7. <span data-ttu-id="c5874-136">Lisää Pituus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c5874-136">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="c5874-137">Kirjoita Leveys-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c5874-137">In the Width field, enter a number.</span></span>
9. <span data-ttu-id="c5874-138">Kirjoita Korkeus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c5874-138">In the Height field, enter a number.</span></span>
10. <span data-ttu-id="c5874-139">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c5874-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="c5874-140">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c5874-140">Click Save.</span></span>
12. <span data-ttu-id="c5874-141">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c5874-141">Click New.</span></span>
13. <span data-ttu-id="c5874-142">Kirjoita arvo Konttityyppi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c5874-142">In the Container type code field, type a value.</span></span>
14. <span data-ttu-id="c5874-143">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c5874-143">In the Description field, type a value.</span></span>
15. <span data-ttu-id="c5874-144">Syötä Taarapaino-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c5874-144">In the Tare weight field, enter a number.</span></span>
16. <span data-ttu-id="c5874-145">Lisää Enimmäispaino-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c5874-145">In the Maximum weight field, enter a number.</span></span>
17. <span data-ttu-id="c5874-146">Syötä Tilavuus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c5874-146">In the Volume field, enter a number.</span></span>
18. <span data-ttu-id="c5874-147">Lisää Pituus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c5874-147">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="c5874-148">Kirjoita Leveys-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c5874-148">In the Width field, enter a number.</span></span>
20. <span data-ttu-id="c5874-149">Kirjoita Korkeus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c5874-149">In the Height field, enter a number.</span></span>
21. <span data-ttu-id="c5874-150">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c5874-150">Click Save.</span></span>
22. <span data-ttu-id="c5874-151">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c5874-151">Click New.</span></span>
23. <span data-ttu-id="c5874-152">Kirjoita arvo Konttityyppi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c5874-152">In the Container type code field, type a value.</span></span>
24. <span data-ttu-id="c5874-153">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c5874-153">In the Description field, type a value.</span></span>
25. <span data-ttu-id="c5874-154">Syötä Taarapaino-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c5874-154">In the Tare weight field, enter a number.</span></span>
26. <span data-ttu-id="c5874-155">Lisää Enimmäispaino-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c5874-155">In the Maximum weight field, enter a number.</span></span>
27. <span data-ttu-id="c5874-156">Syötä Tilavuus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c5874-156">In the Volume field, enter a number.</span></span>
28. <span data-ttu-id="c5874-157">Lisää Pituus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c5874-157">In the Length field, enter a number.</span></span>
29. <span data-ttu-id="c5874-158">Kirjoita Leveys-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c5874-158">In the Width field, enter a number.</span></span>
30. <span data-ttu-id="c5874-159">Kirjoita Korkeus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c5874-159">In the Height field, enter a number.</span></span>
31. <span data-ttu-id="c5874-160">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c5874-160">Click Save.</span></span>
32. <span data-ttu-id="c5874-161">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c5874-161">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="c5874-162">Määritä konttiryhmä</span><span class="sxs-lookup"><span data-stu-id="c5874-162">Set up a container group</span></span>
1. <span data-ttu-id="c5874-163">Valitse Varastonhallinta > Asetukset > Kontit > Konttiryhmät.</span><span class="sxs-lookup"><span data-stu-id="c5874-163">Go to Warehouse management > Setup > Containers > Container groups.</span></span>
2. <span data-ttu-id="c5874-164">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c5874-164">Click New.</span></span>
    * <span data-ttu-id="c5874-165">Voit määrittää konttityyppien loogiset ryhmät.</span><span class="sxs-lookup"><span data-stu-id="c5874-165">You can set up logical groups of container types.</span></span> <span data-ttu-id="c5874-166">Voit määrittää kullekin ryhmälle konttien pakkausjärjestyksen ja prosenttiosuuden, jonka perusteella kontit täytetään. Nimikkeen kokodimensiota käytetään määrittämään, onko kontissa tilaa.</span><span class="sxs-lookup"><span data-stu-id="c5874-166">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="c5874-167">Järjestelmä valitsee kontin, jonka kokodimensiot ovat lähimpänä nimikettä.</span><span class="sxs-lookup"><span data-stu-id="c5874-167">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="c5874-168">Jos ryhmässä on useita konttityyppejä, suosittelemme, että järjestät järjestyksen koon mukaan niin, että suurin kontti on ensimmäinen, numero 1 sarjassa, ja pienin kontti on viimeinen.</span><span class="sxs-lookup"><span data-stu-id="c5874-168">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="c5874-169">Kirjoita Konttiryhmän tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="c5874-169">In the Container group ID field, type a value.</span></span>
4. <span data-ttu-id="c5874-170">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c5874-170">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c5874-171">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c5874-171">Click New.</span></span>
6. <span data-ttu-id="c5874-172">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c5874-172">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="c5874-173">Anna tai valitse arvo Konttityyppi -kentässä.</span><span class="sxs-lookup"><span data-stu-id="c5874-173">In the Container type field, enter or select a value.</span></span>
8. <span data-ttu-id="c5874-174">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c5874-174">Click New.</span></span>
9. <span data-ttu-id="c5874-175">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c5874-175">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="c5874-176">Anna tai valitse arvo Konttityyppi -kentässä.</span><span class="sxs-lookup"><span data-stu-id="c5874-176">In the Container type field, enter or select a value.</span></span>
11. <span data-ttu-id="c5874-177">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c5874-177">Click New.</span></span>
12. <span data-ttu-id="c5874-178">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c5874-178">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="c5874-179">Anna tai valitse arvo Konttityyppi -kentässä.</span><span class="sxs-lookup"><span data-stu-id="c5874-179">In the Container type field, enter or select a value.</span></span>
14. <span data-ttu-id="c5874-180">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c5874-180">Click Save.</span></span>
15. <span data-ttu-id="c5874-181">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c5874-181">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="c5874-182">Aseta kontin muodostusmalli</span><span class="sxs-lookup"><span data-stu-id="c5874-182">Set up a container build template</span></span>
1. <span data-ttu-id="c5874-183">Valitse Varastonhallinta > Asetukset > Kontit > Kontin rakennusmallit.</span><span class="sxs-lookup"><span data-stu-id="c5874-183">Go to Warehouse management > Setup > Containers > Container build templates.</span></span>
2. <span data-ttu-id="c5874-184">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c5874-184">Click New.</span></span>
    * <span data-ttu-id="c5874-185">Kontin rakennusmalli perustuu suoritettavaan konttiinpakkauksen prosessiin.</span><span class="sxs-lookup"><span data-stu-id="c5874-185">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="c5874-186">Kukin kontin rakennusmalli määrittää yhden konttiinpakkauksen prosessin, jota käytetään aaltomallissa.</span><span class="sxs-lookup"><span data-stu-id="c5874-186">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="c5874-187">Muokkaa kyselyä -komennon avulla voit määrittää ehdot, jonka perusteella valittu malli käsitellään.</span><span class="sxs-lookup"><span data-stu-id="c5874-187">The Edit query option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="c5874-188">Voit esimerkiksi haluta suorittaa konttiinpakkauksen vain tietyille asiakkaille, tuotteille tai varastoille, tai voit lisätä vastaavan kyselyalueen malliin.</span><span class="sxs-lookup"><span data-stu-id="c5874-188">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="c5874-189">Kontin rakennusmalli linkitetään aaltomallin vaiheisiin Aallon vaihekoodi -kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="c5874-189">The Wave step code field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="c5874-190">Kun aalto suoritetaan, se määrittää, mitä kontin rakennusmalleja käytetään konttiinpakkauksen aloittamiseen.</span><span class="sxs-lookup"><span data-stu-id="c5874-190">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="c5874-191">Peruskyselytyyppi-kenttä määrittää pakattavat kohteet ja suodattimen perusteen.</span><span class="sxs-lookup"><span data-stu-id="c5874-191">The Base query type field determines what to pack and what to base the filter query on.</span></span>  
3. <span data-ttu-id="c5874-192">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c5874-192">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c5874-193">Kirjoita Konttimallin tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="c5874-193">In the Container template ID field, type a value.</span></span>
5. <span data-ttu-id="c5874-194">Anna tai valitse Konttiryhmän tunnus -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="c5874-194">In the Container group ID field, enter or select a value.</span></span>
6. <span data-ttu-id="c5874-195">Kirjoita arvo Aallon vaihekoodi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c5874-195">In the Wave step code field, type a value.</span></span>
7. <span data-ttu-id="c5874-196">Merkitse Salli jaetut keräilyt -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="c5874-196">Select the Allow split picks check box.</span></span>
8. <span data-ttu-id="c5874-197">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c5874-197">Click Save.</span></span>
9. <span data-ttu-id="c5874-198">Napsauta Säilön yhdistämisrajoitukset -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="c5874-198">Click Containier mixing constraints.</span></span>
    * <span data-ttu-id="c5874-199">Yhdistämislogiikan keskeytysten avulla voit määrittää sääntöjä pakkauksen kohdistusriveille konteissa.</span><span class="sxs-lookup"><span data-stu-id="c5874-199">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="c5874-200">Jos esimerkiksi lisäät Nimiketunnus-kentän, kun nimikkeet on liitetty kontteihin, luodaan uusi kontti aina silloin, kun kohdataan uusi nimiketunnus.</span><span class="sxs-lookup"><span data-stu-id="c5874-200">For example, if you add the Item number field, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="c5874-201">Tämä estää työntekijöitä pakkaamasta kahden eri asiakkaan kohdistusrivejä samaan konttiin.</span><span class="sxs-lookup"><span data-stu-id="c5874-201">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
10. <span data-ttu-id="c5874-202">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c5874-202">Click New.</span></span>
11. <span data-ttu-id="c5874-203">Valitse vaihtoehto Taulukko-kentässä.</span><span class="sxs-lookup"><span data-stu-id="c5874-203">In the Table field, select an option.</span></span>
12. <span data-ttu-id="c5874-204">Syötä tai valitse arvo Kentän valinta -kentässä.</span><span class="sxs-lookup"><span data-stu-id="c5874-204">In the Field Select field, enter or select a value.</span></span>
13. <span data-ttu-id="c5874-205">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c5874-205">Click OK.</span></span>

