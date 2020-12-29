---
title: Määritä työmalli ostotilauksia varten
description: Tässä aiheessa käsitellään vastaanotettujen nimikkeiden poispanossa käytettävän yksinkertaisen työmallin määrittämistä.
author: ShylaThompson
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6628936a56619de255ca7dc7b332b5819918c310
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427284"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="5a8a1-103">Määritä työmalli ostotilauksia varten</span><span class="sxs-lookup"><span data-stu-id="5a8a1-103">Set up a work template for purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5a8a1-104">Tässä aiheessa käsitellään vastaanotettujen nimikkeiden poispanossa käytettävän yksinkertaisen työmallin määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-104">This topic describes how to set up a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="5a8a1-105">Työmallit määrittävät varastotyöntekijälle mobiililaitteessa näytettävät ohjeet, kun nimikkeitä siirretään vastaanotosta.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="5a8a1-106">Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoissa mainituilla tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="5a8a1-107">Luo työpoolin tunnus ennen tämän opastuksen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="5a8a1-108">Tässä esimerkissä käytetään Saapuva-asetuksessa kutsuttua työpoolin tunnusta.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="5a8a1-109">Tämä menettely on tarkoitettu varastopäällikölle.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="5a8a1-110">Siirry kohtaan **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Työ > Työmallit**.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-110">In the navigation pane, go to **Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="5a8a1-111">Valitse **Työtilaustyyppi**-kentässä **Ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-111">In the **Work order type** field, select **Purchase orders**.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="5a8a1-112">Luo työmallin otsikko</span><span class="sxs-lookup"><span data-stu-id="5a8a1-112">Create a work template header</span></span>
1. <span data-ttu-id="5a8a1-113">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-113">Select **New**.</span></span>
2. <span data-ttu-id="5a8a1-114">Syötä **Järjestysnumero**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-114">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="5a8a1-115">Työmallit arvioidaan tässä järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="5a8a1-116">Voit tarvittaessa muuttaa järjestystä.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="5a8a1-117">Kirjoita **Työmalli**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-117">In the **Work template** field, type a value.</span></span> <span data-ttu-id="5a8a1-118">Tämä on mallin yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="5a8a1-119">Kirjoita **Työmallin kuvaus** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-119">In the **Work template description** field, type a value.</span></span>
    - <span data-ttu-id="5a8a1-120">**Voimassaoleva**-asetusta ei voi valita, ennen kuin mallin tarvitsevat tiedot on annettu ja **Tallenna** on valittu.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-120">The **Valid** option will not be checked until you've completed all the information that's needed by the template and have then selected **Save**.</span></span>  
    - <span data-ttu-id="5a8a1-121">**Ostotilaus**-tyypin työtilausta ei voi käsitellä automaattisesti, joten jätä **Käsittele automaattisesti** -asetukseksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-121">A work order of type **Purchase order** cannot be automatically processed, so leave the **Automatically process** option set to **No**.</span></span>  
5. <span data-ttu-id="5a8a1-122">Kirjoita **Työpoolin tunnus** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-122">In the **Work pool ID** field, type a value.</span></span> <span data-ttu-id="5a8a1-123">Työpoolin tunnuksilla voi järjestää työt ryhmiksi.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="5a8a1-124">Tässä määritetty arvo on tällä mallilla luotavien töiden oletusarvo.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-124">The value that you set here will be the default value for any work that's created using this template.</span></span>  
6. <span data-ttu-id="5a8a1-125">Lisää **Työn prioriteetti** -kenttään `1`.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-125">In the **Work priority** field, enter `1`.</span></span> <span data-ttu-id="5a8a1-126">Tämä ilmaisee työn tärkeyden ja tässä määritetty arvo on tällä mallilla luotavien töiden oletusarvo.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="5a8a1-127">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-127">Select **Save**.</span></span> <span data-ttu-id="5a8a1-128">**Muokkaa kyselyä** -painike tulee käytettäväksi, kun työmallin otsikko on tallennettu.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-128">You must save the work template header before the **Edit Query** button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="5a8a1-129">Määritä työmallin kysely</span><span class="sxs-lookup"><span data-stu-id="5a8a1-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="5a8a1-130">Valitse **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-130">Select **Edit query**.</span></span> <span data-ttu-id="5a8a1-131">Määritettävä rajoitus aiheuttaa sen, että mallia voi käyttää vain tietyssä varastossa.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-131">We'll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="5a8a1-132">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-132">Select **Add**.</span></span>
3. <span data-ttu-id="5a8a1-133">Kirjoita uuden rivin **Kenttä**-kenttään `warehouse`.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-133">In the **Field** field of the new row, type `warehouse`.</span></span>
4. <span data-ttu-id="5a8a1-134">Kirjoita arvo **Ehdot**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-134">In the **Criteria** field, type a value.</span></span>
5. <span data-ttu-id="5a8a1-135">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-135">Select **OK**.</span></span>
6. <span data-ttu-id="5a8a1-136">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-136">Select **Yes**.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="5a8a1-137">Määritä työmallin tiedot</span><span class="sxs-lookup"><span data-stu-id="5a8a1-137">Set work template details</span></span>
1. <span data-ttu-id="5a8a1-138">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-138">Select **New**.</span></span>
2. <span data-ttu-id="5a8a1-139">Valitse **Työtyyppi**-kentässä **Keräilyt**.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-139">In the **Work type** field, select **Pick**.</span></span>
3. <span data-ttu-id="5a8a1-140">Kirjoita **Työluokan tunnus** -kenttään `purchase`.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-140">In the **Work class ID** field, type `purchase`.</span></span> <span data-ttu-id="5a8a1-141">Tässä määritetty työluokka on kaikkien tällä mallilla luotujen Keräily-tyypin työrivien oletus.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-141">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="5a8a1-142">Työluokkaa ei voi ohittaa työtilausriveiltä.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-142">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="5a8a1-143">Työluokilla ohjataan ja/tai rajoitetaan työtilausrivityyppejä, joita varastotyötekijä voi käsitellä mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-143">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="5a8a1-144">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-144">Select **New**.</span></span>
5. <span data-ttu-id="5a8a1-145">Valitse **Työtyyppi**-kentässä **Määritä**.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-145">In the **Work type** field, select **Put**.</span></span>
6. <span data-ttu-id="5a8a1-146">Kirjoita **Työluokan tunnus** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-146">In the **Work class ID** field, type a value.</span></span> <span data-ttu-id="5a8a1-147">Keräily- ja määritysohjeet kuuluvat yhteen.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-147">The pick and put instructions are a set.</span></span> <span data-ttu-id="5a8a1-148">Jokaisella keräily/määritys-joukolla on oltava sama työluokka.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-148">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="5a8a1-149">Käytä samaa, keräilyohjeessa ilmoitettua työluokkaa.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-149">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="5a8a1-150">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-150">Select **Save**.</span></span> <span data-ttu-id="5a8a1-151">Huomaa, että **Voimassaoleva**-valinta on nyt valittuna.</span><span class="sxs-lookup"><span data-stu-id="5a8a1-151">Note that the **Valid** checkbox is now checked.</span></span>  

