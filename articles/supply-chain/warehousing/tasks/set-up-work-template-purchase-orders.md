--- 
title: "Määritä työmalli ostotilauksia varten"
description: "Tässä menettelyssä käsitellään vastaanotettujen nimikkeiden poispanossa käytettävän yksinkertaisen työmallin määrittämistä."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: fbbe019bdca2d5182466a20370418a14032fe63d
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="d3921-103">Määritä työmalli ostotilauksia varten</span><span class="sxs-lookup"><span data-stu-id="d3921-103">Set up a work template for purchase orders</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d3921-104">Tässä menettelyssä käsitellään vastaanotettujen nimikkeiden poispanossa käytettävän yksinkertaisen työmallin määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="d3921-104">This procedure focuses on the set up of a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="d3921-105">Työmallit määrittävät varastotyöntekijälle mobiililaitteessa näytettävät ohjeet, kun nimikkeitä siirretään vastaanotosta.</span><span class="sxs-lookup"><span data-stu-id="d3921-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="d3921-106">Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoissa mainituilla tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="d3921-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="d3921-107">Luo työpoolin tunnus ennen tämän opastuksen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="d3921-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="d3921-108">Tässä esimerkissä käytetään Saapuva-asetuksessa kutsuttua työpoolin tunnusta.</span><span class="sxs-lookup"><span data-stu-id="d3921-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="d3921-109">Tämä menettely on tarkoitettu varastopäällikölle.</span><span class="sxs-lookup"><span data-stu-id="d3921-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="d3921-110">Valitse Varastonhallinta > Asetukset > Työ > Työmallit.</span><span class="sxs-lookup"><span data-stu-id="d3921-110">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="d3921-111">Valitse Työtilaustyyppi-kentässä Ostotilaukset.</span><span class="sxs-lookup"><span data-stu-id="d3921-111">In the Work order type field, select 'Purchase orders'.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="d3921-112">Luo työmallin otsikko</span><span class="sxs-lookup"><span data-stu-id="d3921-112">Create a work template header</span></span>
1. <span data-ttu-id="d3921-113">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d3921-113">Click New.</span></span>
2. <span data-ttu-id="d3921-114">Syötä Järjestysnumero-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="d3921-114">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="d3921-115">Työmallit arvioidaan tässä järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="d3921-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="d3921-116">Voit tarvittaessa muuttaa järjestystä.</span><span class="sxs-lookup"><span data-stu-id="d3921-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="d3921-117">Kirjoita Työmalli-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="d3921-117">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="d3921-118">Tämä on mallin yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="d3921-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="d3921-119">Kirjoita Työmallin kuvaus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="d3921-119">In the Work template description field, type a value.</span></span>
    * <span data-ttu-id="d3921-120">Voimassaoleva-asetusta ei voi valita, ennen kuin mallin tarvitsevat tiedot on annettu ja Tallenna on valittu.</span><span class="sxs-lookup"><span data-stu-id="d3921-120">The Valid option will not be checked until you’ve completed all the information that's needed by the template and have then clicked Save.</span></span>  
    * <span data-ttu-id="d3921-121">Ostotilaus-tyypin työtilausta ei voi käsitellä automaattisesti, joten jätä Käsittele automaattisesti -asetuksen valinnaksi Ei.</span><span class="sxs-lookup"><span data-stu-id="d3921-121">A work order of type Purchase order cannot be automatically processed, so leave the  Automatically process option set to No.</span></span>  
5. <span data-ttu-id="d3921-122">Kirjoita Työpoolin tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="d3921-122">In the Work pool ID field, type a value.</span></span>
    * <span data-ttu-id="d3921-123">Työpoolin tunnuksilla voi järjestää työt ryhmiksi.</span><span class="sxs-lookup"><span data-stu-id="d3921-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="d3921-124">Tässä määritetty arvo on tällä mallilla luotavien töiden oletusarvo.</span><span class="sxs-lookup"><span data-stu-id="d3921-124">The value that you set here will be the default value for any work that’s created using this template.</span></span>  
6. <span data-ttu-id="d3921-125">Lisää Työn prioriteetti -kenttään 1.</span><span class="sxs-lookup"><span data-stu-id="d3921-125">In the Work priority field, enter '1'.</span></span>
    * <span data-ttu-id="d3921-126">Tämä ilmaisee työn tärkeyden ja tässä määritetty arvo on tällä mallilla luotavien töiden oletusarvo.</span><span class="sxs-lookup"><span data-stu-id="d3921-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="d3921-127">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d3921-127">Click Save.</span></span>
    * <span data-ttu-id="d3921-128">Muokkaa kyselyä -painike tulee käytettäväksi, kun työmallin otsikko on tallennettu.</span><span class="sxs-lookup"><span data-stu-id="d3921-128">You must save the work template header before the Edit Query button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="d3921-129">Määritä työmallin kysely</span><span class="sxs-lookup"><span data-stu-id="d3921-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="d3921-130">Valitse Muokkaa kyselyä.</span><span class="sxs-lookup"><span data-stu-id="d3921-130">Click Edit query.</span></span>
    * <span data-ttu-id="d3921-131">Määritettävä rajoitus aiheuttaa sen, että mallia voi käyttää vain tietyssä varastossa.</span><span class="sxs-lookup"><span data-stu-id="d3921-131">We’ll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="d3921-132">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="d3921-132">Click Add.</span></span>
3. <span data-ttu-id="d3921-133">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="d3921-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="d3921-134">Kirjoita Kenttä-kenttään varasto.</span><span class="sxs-lookup"><span data-stu-id="d3921-134">In the Field field, type 'warehouse'.</span></span>
5. <span data-ttu-id="d3921-135">Kirjoita arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d3921-135">In the Criteria field, type a value.</span></span>
6. <span data-ttu-id="d3921-136">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="d3921-136">Click OK.</span></span>
7. <span data-ttu-id="d3921-137">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="d3921-137">Click Yes.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="d3921-138">Määritä työmallin tiedot</span><span class="sxs-lookup"><span data-stu-id="d3921-138">Set work template details</span></span>
1. <span data-ttu-id="d3921-139">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d3921-139">Click New.</span></span>
2. <span data-ttu-id="d3921-140">Valitse Työtyyppi-kentässä Keräilyt.</span><span class="sxs-lookup"><span data-stu-id="d3921-140">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="d3921-141">Kirjoita Työluokan tunnus -kenttään osto.</span><span class="sxs-lookup"><span data-stu-id="d3921-141">In the Work class ID field, type 'purchase'.</span></span>
    * <span data-ttu-id="d3921-142">Tässä määritetty työluokka on kaikkien tällä mallilla luotujen Keräily-tyypin työrivien oletus.</span><span class="sxs-lookup"><span data-stu-id="d3921-142">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="d3921-143">Työluokkaa ei voi ohittaa työtilausriveiltä.</span><span class="sxs-lookup"><span data-stu-id="d3921-143">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="d3921-144">Työluokilla ohjataan ja/tai rajoitetaan työtilausrivityyppejä, joita varastotyötekijä voi käsitellä mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="d3921-144">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="d3921-145">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d3921-145">Click New.</span></span>
5. <span data-ttu-id="d3921-146">Valitse Työtyyppi-kentässä Määritä.</span><span class="sxs-lookup"><span data-stu-id="d3921-146">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="d3921-147">Kirjoita Työluokan tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="d3921-147">In the Work class ID field, type a value.</span></span>
    * <span data-ttu-id="d3921-148">Keräily- ja määritysohjeet kuuluvat yhteen.</span><span class="sxs-lookup"><span data-stu-id="d3921-148">The pick and put instructions are a set.</span></span> <span data-ttu-id="d3921-149">Jokaisella keräily/määritys-joukolla on oltava sama työluokka.</span><span class="sxs-lookup"><span data-stu-id="d3921-149">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="d3921-150">Käytä samaa, keräilyohjeessa ilmoitettua työluokkaa.</span><span class="sxs-lookup"><span data-stu-id="d3921-150">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="d3921-151">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d3921-151">Click Save.</span></span>
    * <span data-ttu-id="d3921-152">Huomaa, että Voimassaoleva-valinta on nyt valittuna.</span><span class="sxs-lookup"><span data-stu-id="d3921-152">Note that the Valid checkbox is now checked.</span></span>  


