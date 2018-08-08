--- 
title: "Määritä manuaalinen pakkaus (vain helmikuu ja toukokuu 2016)"
description: Pakkaamisprosessin avulla voit vahvistaa ja pakata tuotteita kontteihin.
author: ShylaThompson
manager: AnnBe
ms.date: 11/04/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 7e776a08ec2adc48b77c86c16e1f291e524a8d00
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-manual-packing-february--may-2016-only"></a><span data-ttu-id="60d33-103">Määritä manuaalinen pakkaus (vain helmikuu ja toukokuu 2016)</span><span class="sxs-lookup"><span data-stu-id="60d33-103">Set up manual packing (February & May 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="60d33-104">Pakkaamisprosessin avulla voit vahvistaa ja pakata tuotteita kontteihin.</span><span class="sxs-lookup"><span data-stu-id="60d33-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="60d33-105">Tässä prosessissa varastotyöntekijät poimivat tuotteita varastopaikoista ja siirtävät ne pakkausasemalle, jossa nimikemäärät ja -tyypit tarkistetaan ja tuotteet liitetään asianmukaisiin kontteihin.</span><span class="sxs-lookup"><span data-stu-id="60d33-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="60d33-106">Kun kontti on täysin pakattu, sen voi sulkea ja siirtää lähtevien tuotteiden laiturille – tuotteet ovat valmiina toimitettavaksi.</span><span class="sxs-lookup"><span data-stu-id="60d33-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="60d33-107">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="60d33-107">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="60d33-108">Määritä sijaintiprofiilit</span><span class="sxs-lookup"><span data-stu-id="60d33-108">Set up location profiles</span></span>
1. <span data-ttu-id="60d33-109">Valitse Varastonhallinta > Asetukset > Varasto > Sijaintiprofiilit.</span><span class="sxs-lookup"><span data-stu-id="60d33-109">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="60d33-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="60d33-110">Click New.</span></span>
    * <span data-ttu-id="60d33-111">Sijaintiprofiilia käytetään pakkausasemilla ja se sisältää toimipaikan tietoja ja säännöt.</span><span class="sxs-lookup"><span data-stu-id="60d33-111">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="60d33-112">Kirjoita Sijainnin profiilitunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="60d33-112">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="60d33-113">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="60d33-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="60d33-114">Syötä tai valitse arvo Sijainnin muoto -kenttään.</span><span class="sxs-lookup"><span data-stu-id="60d33-114">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="60d33-115">Anna tai valitse Sijainnin tyyppi -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="60d33-115">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="60d33-116">Valitse Salli yhdistetyt nimikkeet -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="60d33-116">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="60d33-117">Valitse Salli yhdistetyt varastotilat -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="60d33-117">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="60d33-118">Valitse Erän käsittelypäivien ohitussäännöt -kentän arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="60d33-118">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="60d33-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="60d33-119">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="60d33-120">Määritä varastonhallinnan parametrit</span><span class="sxs-lookup"><span data-stu-id="60d33-120">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="60d33-121">Valitse Varastonhallinta > Asetukset > Varastonhallinnan parametrit.</span><span class="sxs-lookup"><span data-stu-id="60d33-121">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="60d33-122">Napsauta Pakkaus-välilehteä.</span><span class="sxs-lookup"><span data-stu-id="60d33-122">Click the Packing tab.</span></span>
3. <span data-ttu-id="60d33-123">Syötä tai valitse arvo Pakkauksen sijainnin profiilitunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="60d33-123">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="60d33-124">Valitse sijaintiprofiili, joita haluat käyttää pakkaukseen.</span><span class="sxs-lookup"><span data-stu-id="60d33-124">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="60d33-125">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="60d33-125">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="60d33-126">Määritä konttityypit</span><span class="sxs-lookup"><span data-stu-id="60d33-126">Set up container types</span></span>
1. <span data-ttu-id="60d33-127">Valitse Varastonhallinta > Asetukset > Kontit > Konttityypit.</span><span class="sxs-lookup"><span data-stu-id="60d33-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="60d33-128">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="60d33-128">Click New.</span></span>
    * <span data-ttu-id="60d33-129">Voit määrittää käytettävät kontit.</span><span class="sxs-lookup"><span data-stu-id="60d33-129">You can define the types of containers to use.</span></span> <span data-ttu-id="60d33-130">Voit määrittää konttien fyysiset dimensiot, kuten taarapainon, enimmäispainon, enimmäistilavuuden, pituuden, leveyden ja painon.</span><span class="sxs-lookup"><span data-stu-id="60d33-130">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="60d33-131">Määritteet ovat mukautettuja kenttiä, joiden avulla voit lisätä konttityyppiin ylimääräisiä dimensioita.</span><span class="sxs-lookup"><span data-stu-id="60d33-131">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="60d33-132">Kirjoita arvo Konttityyppi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="60d33-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="60d33-133">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="60d33-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="60d33-134">Syötä Taarapaino-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="60d33-134">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="60d33-135">Lisää Enimmäispaino-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="60d33-135">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="60d33-136">Syötä Tilavuus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="60d33-136">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="60d33-137">Lisää Pituus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="60d33-137">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="60d33-138">Kirjoita Leveys-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="60d33-138">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="60d33-139">Kirjoita Korkeus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="60d33-139">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="60d33-140">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="60d33-140">Click Save.</span></span>
12. <span data-ttu-id="60d33-141">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="60d33-141">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="60d33-142">Määritä pakkausprofiilit</span><span class="sxs-lookup"><span data-stu-id="60d33-142">Set up packing profiles</span></span>
1. <span data-ttu-id="60d33-143">Valitse Varastonhallinta > Asetukset > Pakkaus > Pakkausprofiilit.</span><span class="sxs-lookup"><span data-stu-id="60d33-143">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="60d33-144">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="60d33-144">Click New.</span></span>
3. <span data-ttu-id="60d33-145">Kirjoita arvo Pakkausprofiilin tunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="60d33-145">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="60d33-146">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="60d33-146">In the Description field, type a value.</span></span>
5. <span data-ttu-id="60d33-147">Syötä tai valitse arvo Kontin sulkemisprofiilin tunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="60d33-147">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="60d33-148">Kontin sulkemisprofiilin tunnus on valinnainen ja on suljetun kontin oletusprofiili tälle pakkausprofiilille.</span><span class="sxs-lookup"><span data-stu-id="60d33-148">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="60d33-149">Valitse Kontin tunnuksen tila -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="60d33-149">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="60d33-150">Tämä asetus määrittää, luodaanko kontin tunnus automaattisesti kontin luomisen yhteydessä, vai luodaanko kontin tunnus manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="60d33-150">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="60d33-151">Anna tai valitse arvo Konttityyppi -kentässä.</span><span class="sxs-lookup"><span data-stu-id="60d33-151">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="60d33-152">Kontin tyyppiä käytetään oletusarvon uutta konttia luotaessa.</span><span class="sxs-lookup"><span data-stu-id="60d33-152">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="60d33-153">Merkitse Luo kontti automaattisesti kontin sulkemisessa -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="60d33-153">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="60d33-154">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="60d33-154">Click Save.</span></span>
10. <span data-ttu-id="60d33-155">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="60d33-155">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="60d33-156">Määritä kontin sulkemisprofiilit</span><span class="sxs-lookup"><span data-stu-id="60d33-156">Set up container closing profiles</span></span>
1. <span data-ttu-id="60d33-157">Valitse Varastonhallinta > Asetukset > Kontit > Kontin sulkemisprofiilit.</span><span class="sxs-lookup"><span data-stu-id="60d33-157">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="60d33-158">Kontin sulkemisprofiili määrittää, mitä tapahtuu, kun kontti suljetaan.</span><span class="sxs-lookup"><span data-stu-id="60d33-158">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="60d33-159">Voit määrittää useita suljetun kontin profiileja.</span><span class="sxs-lookup"><span data-stu-id="60d33-159">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="60d33-160">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="60d33-160">Click New.</span></span>
3. <span data-ttu-id="60d33-161">Kirjoita arvo Kontin sulkemisprofiilin tunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="60d33-161">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="60d33-162">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="60d33-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="60d33-163">Valitse vaihtoehto Luettelo kohteessa -kentässä .</span><span class="sxs-lookup"><span data-stu-id="60d33-163">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="60d33-164">Määritä, tapahtuuko luettelointi kontteja suljettaessa vai lähetystä vahvistettaessa.</span><span class="sxs-lookup"><span data-stu-id="60d33-164">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="60d33-165">Huomaa, että luettelointi edellyttää, että Kuljetustenhallinta on käytössä.</span><span class="sxs-lookup"><span data-stu-id="60d33-165">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="60d33-166">Luettelointi on toteutettava kuljetusmoottoreissa, jotta se toimii.</span><span class="sxs-lookup"><span data-stu-id="60d33-166">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="60d33-167">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="60d33-167">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="60d33-168">Syötä tai valitse arvo Lopullisen lähetyksen oletussijainti -kenttään.</span><span class="sxs-lookup"><span data-stu-id="60d33-168">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="60d33-169">Tämä on toimipaikka, johon tuotteet siirretään konttien sulkemisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="60d33-169">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="60d33-170">Toimipaikalle on määritettävä sijaintiprofiili varaston parametreissa.</span><span class="sxs-lookup"><span data-stu-id="60d33-170">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="60d33-171">Syötä tai valitse arvo kentässä Painoyksikkö.</span><span class="sxs-lookup"><span data-stu-id="60d33-171">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="60d33-172">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="60d33-172">Click Save.</span></span>


