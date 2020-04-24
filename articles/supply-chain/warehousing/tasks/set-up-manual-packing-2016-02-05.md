---
title: Manuaalisen pakkaamisen määrittäminen (helmikuu 2016 ja toukokuu 2016)
description: Pakkaamisprosessin avulla voit vahvistaa ja pakata tuotteita kontteihin.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8486ca90da44bb4c05c71a2babfc79445ed2dd12
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216893"
---
# <a name="set-up-manual-packing-february-2016--may-2016"></a><span data-ttu-id="9cd14-103">Manuaalisen pakkaamisen määrittäminen (helmikuu 2016 ja toukokuu 2016)</span><span class="sxs-lookup"><span data-stu-id="9cd14-103">Set up manual packing (February 2016 & May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9cd14-104">Pakkaamisprosessin avulla voit vahvistaa ja pakata tuotteita kontteihin.</span><span class="sxs-lookup"><span data-stu-id="9cd14-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="9cd14-105">Tässä prosessissa varastotyöntekijät poimivat tuotteita varastopaikoista ja siirtävät ne pakkausasemalle, jossa nimikemäärät ja -tyypit tarkistetaan ja tuotteet liitetään asianmukaisiin kontteihin.</span><span class="sxs-lookup"><span data-stu-id="9cd14-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="9cd14-106">Kun kontti on täysin pakattu, sen voi sulkea ja siirtää lähtevien tuotteiden laiturille – tuotteet ovat valmiina toimitettavaksi.</span><span class="sxs-lookup"><span data-stu-id="9cd14-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="9cd14-107">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="9cd14-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="9cd14-108">Tämä ohje koskee vain helmikuun 2016 ja toukokuun 2016 Dynamics 365 for Operationsin versioita.</span><span class="sxs-lookup"><span data-stu-id="9cd14-108">This procedure is for the February 2016 & May 2016 versions of Dynamics 365 for Operations only.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="9cd14-109">Määritä sijaintiprofiilit</span><span class="sxs-lookup"><span data-stu-id="9cd14-109">Set up location profiles</span></span>
1. <span data-ttu-id="9cd14-110">Valitse Varastonhallinta > Asetukset > Varasto > Sijaintiprofiilit.</span><span class="sxs-lookup"><span data-stu-id="9cd14-110">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="9cd14-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9cd14-111">Click New.</span></span>
    * <span data-ttu-id="9cd14-112">Sijaintiprofiilia käytetään pakkausasemilla ja se sisältää toimipaikan tietoja ja säännöt.</span><span class="sxs-lookup"><span data-stu-id="9cd14-112">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="9cd14-113">Kirjoita Sijainnin profiilitunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="9cd14-113">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="9cd14-114">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cd14-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9cd14-115">Syötä tai valitse arvo Sijainnin muoto -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cd14-115">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="9cd14-116">Anna tai valitse Sijainnin tyyppi -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="9cd14-116">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="9cd14-117">Valitse Salli yhdistetyt nimikkeet -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="9cd14-117">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="9cd14-118">Valitse Salli yhdistetyt varastotilat -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="9cd14-118">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="9cd14-119">Valitse Erän käsittelypäivien ohitussäännöt -kentän arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="9cd14-119">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="9cd14-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9cd14-120">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="9cd14-121">Määritä varastonhallinnan parametrit</span><span class="sxs-lookup"><span data-stu-id="9cd14-121">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="9cd14-122">Valitse Varastonhallinta > Asetukset > Varastonhallinnan parametrit.</span><span class="sxs-lookup"><span data-stu-id="9cd14-122">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="9cd14-123">Napsauta Pakkaus-välilehteä.</span><span class="sxs-lookup"><span data-stu-id="9cd14-123">Click the Packing tab.</span></span>
3. <span data-ttu-id="9cd14-124">Syötä tai valitse arvo Pakkauksen sijainnin profiilitunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cd14-124">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="9cd14-125">Valitse sijaintiprofiili, joita haluat käyttää pakkaukseen.</span><span class="sxs-lookup"><span data-stu-id="9cd14-125">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="9cd14-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9cd14-126">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="9cd14-127">Määritä konttityypit</span><span class="sxs-lookup"><span data-stu-id="9cd14-127">Set up container types</span></span>
1. <span data-ttu-id="9cd14-128">Valitse Varastonhallinta > Asetukset > Kontit > Konttityypit.</span><span class="sxs-lookup"><span data-stu-id="9cd14-128">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="9cd14-129">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9cd14-129">Click New.</span></span>
    * <span data-ttu-id="9cd14-130">Voit määrittää käytettävät kontit.</span><span class="sxs-lookup"><span data-stu-id="9cd14-130">You can define the types of containers to use.</span></span> <span data-ttu-id="9cd14-131">Voit määrittää konttien fyysiset dimensiot, kuten taarapainon, enimmäispainon, enimmäistilavuuden, pituuden, leveyden ja painon.</span><span class="sxs-lookup"><span data-stu-id="9cd14-131">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="9cd14-132">Määritteet ovat mukautettuja kenttiä, joiden avulla voit lisätä konttityyppiin ylimääräisiä dimensioita.</span><span class="sxs-lookup"><span data-stu-id="9cd14-132">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="9cd14-133">Kirjoita arvo Konttityyppi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cd14-133">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="9cd14-134">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cd14-134">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9cd14-135">Syötä Taarapaino-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="9cd14-135">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="9cd14-136">Lisää Enimmäispaino-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="9cd14-136">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="9cd14-137">Syötä Tilavuus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="9cd14-137">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="9cd14-138">Lisää Pituus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="9cd14-138">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="9cd14-139">Kirjoita Leveys-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="9cd14-139">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="9cd14-140">Kirjoita Korkeus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="9cd14-140">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="9cd14-141">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9cd14-141">Click Save.</span></span>
12. <span data-ttu-id="9cd14-142">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9cd14-142">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="9cd14-143">Määritä pakkausprofiilit</span><span class="sxs-lookup"><span data-stu-id="9cd14-143">Set up packing profiles</span></span>
1. <span data-ttu-id="9cd14-144">Valitse Varastonhallinta > Asetukset > Pakkaus > Pakkausprofiilit.</span><span class="sxs-lookup"><span data-stu-id="9cd14-144">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="9cd14-145">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9cd14-145">Click New.</span></span>
3. <span data-ttu-id="9cd14-146">Kirjoita arvo Pakkausprofiilin tunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cd14-146">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="9cd14-147">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cd14-147">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9cd14-148">Syötä tai valitse arvo Kontin sulkemisprofiilin tunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cd14-148">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="9cd14-149">Kontin sulkemisprofiilin tunnus on valinnainen ja on suljetun kontin oletusprofiili tälle pakkausprofiilille.</span><span class="sxs-lookup"><span data-stu-id="9cd14-149">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="9cd14-150">Valitse Kontin tunnuksen tila -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="9cd14-150">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="9cd14-151">Tämä asetus määrittää, luodaanko kontin tunnus automaattisesti kontin luomisen yhteydessä, vai luodaanko kontin tunnus manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="9cd14-151">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="9cd14-152">Anna tai valitse arvo Konttityyppi -kentässä.</span><span class="sxs-lookup"><span data-stu-id="9cd14-152">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="9cd14-153">Kontin tyyppiä käytetään oletusarvon uutta konttia luotaessa.</span><span class="sxs-lookup"><span data-stu-id="9cd14-153">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="9cd14-154">Merkitse Luo kontti automaattisesti kontin sulkemisessa -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="9cd14-154">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="9cd14-155">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9cd14-155">Click Save.</span></span>
10. <span data-ttu-id="9cd14-156">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9cd14-156">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="9cd14-157">Määritä kontin sulkemisprofiilit</span><span class="sxs-lookup"><span data-stu-id="9cd14-157">Set up container closing profiles</span></span>
1. <span data-ttu-id="9cd14-158">Valitse Varastonhallinta > Asetukset > Kontit > Kontin sulkemisprofiilit.</span><span class="sxs-lookup"><span data-stu-id="9cd14-158">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="9cd14-159">Kontin sulkemisprofiili määrittää, mitä tapahtuu, kun kontti suljetaan.</span><span class="sxs-lookup"><span data-stu-id="9cd14-159">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="9cd14-160">Voit määrittää useita suljetun kontin profiileja.</span><span class="sxs-lookup"><span data-stu-id="9cd14-160">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="9cd14-161">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9cd14-161">Click New.</span></span>
3. <span data-ttu-id="9cd14-162">Kirjoita arvo Kontin sulkemisprofiilin tunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cd14-162">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="9cd14-163">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cd14-163">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9cd14-164">Valitse vaihtoehto Luettelo kohteessa -kentässä .</span><span class="sxs-lookup"><span data-stu-id="9cd14-164">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="9cd14-165">Määritä, tapahtuuko luettelointi kontteja suljettaessa vai lähetystä vahvistettaessa.</span><span class="sxs-lookup"><span data-stu-id="9cd14-165">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="9cd14-166">Huomaa, että luettelointi edellyttää, että Kuljetustenhallinta on käytössä.</span><span class="sxs-lookup"><span data-stu-id="9cd14-166">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="9cd14-167">Luettelointi on toteutettava kuljetusmoottoreissa, jotta se toimii.</span><span class="sxs-lookup"><span data-stu-id="9cd14-167">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="9cd14-168">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="9cd14-168">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="9cd14-169">Syötä tai valitse arvo Lopullisen lähetyksen oletussijainti -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cd14-169">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="9cd14-170">Tämä on toimipaikka, johon tuotteet siirretään konttien sulkemisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="9cd14-170">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="9cd14-171">Toimipaikalle on määritettävä sijaintiprofiili varaston parametreissa.</span><span class="sxs-lookup"><span data-stu-id="9cd14-171">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="9cd14-172">Syötä tai valitse arvo kentässä Painoyksikkö.</span><span class="sxs-lookup"><span data-stu-id="9cd14-172">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="9cd14-173">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9cd14-173">Click Save.</span></span>

