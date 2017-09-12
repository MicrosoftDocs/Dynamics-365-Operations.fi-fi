--- 
title: "Määritä manuaalinen pakkaus (vain helmikuu ja toukokuu 2016)"
description: Pakkaamisprosessin avulla voit vahvistaa ja pakata tuotteita kontteihin.
author: BibiSp
manager: AnnBe
ms.date: 11/04/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: c8cec376bcc8c50fb9a78bed039505608cd7782d
ms.contentlocale: fi-fi
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-manual-packing-february--may-2016-only"></a><span data-ttu-id="7d3d1-103">Määritä manuaalinen pakkaus (vain helmikuu ja toukokuu 2016)</span><span class="sxs-lookup"><span data-stu-id="7d3d1-103">Set up manual packing (February & May 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7d3d1-104">Pakkaamisprosessin avulla voit vahvistaa ja pakata tuotteita kontteihin.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="7d3d1-105">Tässä prosessissa varastotyöntekijät poimivat tuotteita varastopaikoista ja siirtävät ne pakkausasemalle, jossa nimikemäärät ja -tyypit tarkistetaan ja tuotteet liitetään asianmukaisiin kontteihin.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="7d3d1-106">Kun kontti on täysin pakattu, sen voi sulkea ja siirtää lähtevien tuotteiden laiturille – tuotteet ovat valmiina toimitettavaksi.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="7d3d1-107">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="7d3d1-108">Tämä ohje koskee vain Dynamics 365 for Operations -järjestelmän helmikuu 2016- ja toukokuu 2016 -versioita.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-108">This procedure is for the February 2016 & May 2016 versions of Dynamics 365 for Operations only.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="7d3d1-109">Määritä sijaintiprofiilit</span><span class="sxs-lookup"><span data-stu-id="7d3d1-109">Set up location profiles</span></span>
1. <span data-ttu-id="7d3d1-110">Valitse Varastonhallinta > Asetukset > Varasto > Sijaintiprofiilit.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-110">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="7d3d1-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-111">Click New.</span></span>
    * <span data-ttu-id="7d3d1-112">Sijaintiprofiilia käytetään pakkausasemilla ja se sisältää toimipaikan tietoja ja säännöt.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-112">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="7d3d1-113">Kirjoita Sijainnin profiilitunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-113">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="7d3d1-114">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="7d3d1-115">Syötä tai valitse arvo Sijainnin muoto -kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-115">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="7d3d1-116">Anna tai valitse Sijainnin tyyppi -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-116">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="7d3d1-117">Valitse Salli yhdistetyt nimikkeet -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-117">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="7d3d1-118">Valitse Salli yhdistetyt varastotilat -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-118">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="7d3d1-119">Valitse Erän käsittelypäivien ohitussäännöt -kentän arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-119">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="7d3d1-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-120">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="7d3d1-121">Määritä varastonhallinnan parametrit</span><span class="sxs-lookup"><span data-stu-id="7d3d1-121">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="7d3d1-122">Valitse Varastonhallinta > Asetukset > Varastonhallinnan parametrit.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-122">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="7d3d1-123">Napsauta Pakkaus-välilehteä.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-123">Click the Packing tab.</span></span>
3. <span data-ttu-id="7d3d1-124">Syötä tai valitse arvo Pakkauksen sijainnin profiilitunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-124">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="7d3d1-125">Valitse sijaintiprofiili, joita haluat käyttää pakkaukseen.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-125">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="7d3d1-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-126">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="7d3d1-127">Määritä konttityypit</span><span class="sxs-lookup"><span data-stu-id="7d3d1-127">Set up container types</span></span>
1. <span data-ttu-id="7d3d1-128">Valitse Varastonhallinta > Asetukset > Kontit > Konttityypit.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-128">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="7d3d1-129">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-129">Click New.</span></span>
    * <span data-ttu-id="7d3d1-130">Voit määrittää käytettävät kontit.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-130">You can define the types of containers to use.</span></span> <span data-ttu-id="7d3d1-131">Voit määrittää konttien fyysiset dimensiot, kuten taarapainon, enimmäispainon, enimmäistilavuuden, pituuden, leveyden ja painon.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-131">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="7d3d1-132">Määritteet ovat mukautettuja kenttiä, joiden avulla voit lisätä konttityyppiin ylimääräisiä dimensioita.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-132">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="7d3d1-133">Kirjoita arvo Konttityyppi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-133">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="7d3d1-134">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-134">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7d3d1-135">Syötä Taarapaino-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-135">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="7d3d1-136">Lisää Enimmäispaino-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-136">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="7d3d1-137">Syötä Tilavuus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-137">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="7d3d1-138">Lisää Pituus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-138">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="7d3d1-139">Kirjoita Leveys-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-139">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="7d3d1-140">Kirjoita Korkeus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-140">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="7d3d1-141">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-141">Click Save.</span></span>
12. <span data-ttu-id="7d3d1-142">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-142">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="7d3d1-143">Määritä pakkausprofiilit</span><span class="sxs-lookup"><span data-stu-id="7d3d1-143">Set up packing profiles</span></span>
1. <span data-ttu-id="7d3d1-144">Valitse Varastonhallinta > Asetukset > Pakkaus > Pakkausprofiilit.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-144">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="7d3d1-145">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-145">Click New.</span></span>
3. <span data-ttu-id="7d3d1-146">Kirjoita arvo Pakkausprofiilin tunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-146">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="7d3d1-147">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-147">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7d3d1-148">Syötä tai valitse arvo Kontin sulkemisprofiilin tunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-148">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="7d3d1-149">Kontin sulkemisprofiilin tunnus on valinnainen ja on suljetun kontin oletusprofiili tälle pakkausprofiilille.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-149">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="7d3d1-150">Valitse Kontin tunnuksen tila -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-150">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="7d3d1-151">Tämä asetus määrittää, luodaanko kontin tunnus automaattisesti kontin luomisen yhteydessä, vai luodaanko kontin tunnus manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-151">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="7d3d1-152">Anna tai valitse arvo Konttityyppi -kentässä.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-152">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="7d3d1-153">Kontin tyyppiä käytetään oletusarvon uutta konttia luotaessa.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-153">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="7d3d1-154">Merkitse Luo kontti automaattisesti kontin sulkemisessa -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-154">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="7d3d1-155">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-155">Click Save.</span></span>
10. <span data-ttu-id="7d3d1-156">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-156">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="7d3d1-157">Määritä kontin sulkemisprofiilit</span><span class="sxs-lookup"><span data-stu-id="7d3d1-157">Set up container closing profiles</span></span>
1. <span data-ttu-id="7d3d1-158">Valitse Varastonhallinta > Asetukset > Kontit > Kontin sulkemisprofiilit.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-158">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="7d3d1-159">Kontin sulkemisprofiili määrittää, mitä tapahtuu, kun kontti suljetaan.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-159">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="7d3d1-160">Voit määrittää useita suljetun kontin profiileja.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-160">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="7d3d1-161">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-161">Click New.</span></span>
3. <span data-ttu-id="7d3d1-162">Kirjoita arvo Kontin sulkemisprofiilin tunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-162">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="7d3d1-163">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-163">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7d3d1-164">Valitse vaihtoehto Luettelo kohteessa -kentässä .</span><span class="sxs-lookup"><span data-stu-id="7d3d1-164">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="7d3d1-165">Määritä, tapahtuuko luettelointi kontteja suljettaessa vai lähetystä vahvistettaessa.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-165">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="7d3d1-166">Huomaa, että luettelointi edellyttää, että Kuljetustenhallinta on käytössä.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-166">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="7d3d1-167">Luettelointi on toteutettava kuljetusmoottoreissa, jotta se toimii.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-167">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="7d3d1-168">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-168">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="7d3d1-169">Syötä tai valitse arvo Lopullisen lähetyksen oletussijainti -kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-169">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="7d3d1-170">Tämä on toimipaikka, johon tuotteet siirretään konttien sulkemisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-170">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="7d3d1-171">Toimipaikalle on määritettävä sijaintiprofiili varaston parametreissa.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-171">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="7d3d1-172">Syötä tai valitse arvo kentässä Painoyksikkö.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-172">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="7d3d1-173">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7d3d1-173">Click Save.</span></span>


