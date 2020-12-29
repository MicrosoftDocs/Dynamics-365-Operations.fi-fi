---
title: Luo operatiivinen resurssi
description: Operatiivinen resurssi suorittaa projektin tai tuotantoprosessin aktiviteetit.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e2e59b1e6a83d902df98a0b40ee6c572a6567f05
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426791"
---
# <a name="create-an-operations-resource"></a><span data-ttu-id="3d528-103">Luo operatiivinen resurssi</span><span class="sxs-lookup"><span data-stu-id="3d528-103">Create an operations resource</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3d528-104">Operatiivinen resurssi suorittaa projektin tai tuotantoprosessin aktiviteetit.</span><span class="sxs-lookup"><span data-stu-id="3d528-104">An operations resource performs the activities of a project or a production process.</span></span> <span data-ttu-id="3d528-105">Tässä menettelyssä kerrotaan, miten operatiivinen resurssi määritetään.</span><span class="sxs-lookup"><span data-stu-id="3d528-105">This procedures shows you how to define an operations resource.</span></span> <span data-ttu-id="3d528-106">Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="3d528-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="3d528-107">Siirry Resurssit-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="3d528-107">Go to Resources.</span></span>
2. <span data-ttu-id="3d528-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3d528-108">Click New.</span></span>
3. <span data-ttu-id="3d528-109">Kirjoita arvo Resurssi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3d528-109">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="3d528-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3d528-110">In the Description field, type a value.</span></span>

## <a name="define-capacity-and-consumption-parameters"></a><span data-ttu-id="3d528-111">Kapasiteetin ja kulutuksen parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3d528-111">Define capacity and consumption parameters</span></span>
1. <span data-ttu-id="3d528-112">Laajenna Työvaihe-osa.</span><span class="sxs-lookup"><span data-stu-id="3d528-112">Expand the Operation section.</span></span>
2. <span data-ttu-id="3d528-113">Syötä numero Hävikkiprosentti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3d528-113">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="3d528-114">Syötä tai valitse arvo Asetusluokka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3d528-114">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="3d528-115">Määritä kustannusluokka, joka määrittää asetusten kustannusten tilitystavan.</span><span class="sxs-lookup"><span data-stu-id="3d528-115">Specify the cost category that defines how to account for the cost of setup.</span></span>  
4. <span data-ttu-id="3d528-116">Syötä tai valitse arvo Ajoaikaluokka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3d528-116">In the Run time category field, enter or select a value.</span></span>
    * <span data-ttu-id="3d528-117">Määritä kustannusluokka, joka määrittää ajoajan kustannusten tilitystavan.</span><span class="sxs-lookup"><span data-stu-id="3d528-117">Specify the cost category that defines how to account for the cost of run time.</span></span>  
5. <span data-ttu-id="3d528-118">Syötä tai valitse arvo Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3d528-118">In the Quantity category field, enter or select a value.</span></span>
    * <span data-ttu-id="3d528-119">Määritä kustannusluokka, joka määrittää tuotoksen määrään perustuvan resurssikustannusten tilitystavan.</span><span class="sxs-lookup"><span data-stu-id="3d528-119">Specify the cost category that defines how to account for the resource cost based on the output quantity.</span></span>  
6. <span data-ttu-id="3d528-120">Valitse Kapasiteettiyksikkö-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="3d528-120">In the Capacity unit field, select an option.</span></span>
    * <span data-ttu-id="3d528-121">Määritä yksikkö, jossa operatiivisen resurssin kapasiteetti ilmoitetaan.</span><span class="sxs-lookup"><span data-stu-id="3d528-121">Specify the unit in which to express the capacity of the operations resource.</span></span>  
7. <span data-ttu-id="3d528-122">Syötä Kapasiteetti-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="3d528-122">In the Capacity field, enter a number.</span></span>
8. <span data-ttu-id="3d528-123">Syötä Tehokkuusprosentti-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="3d528-123">In the Efficiency percentage field, enter a number.</span></span>
    * <span data-ttu-id="3d528-124">Määritä operatiiviselta resurssilta odotettava tehokkuus.</span><span class="sxs-lookup"><span data-stu-id="3d528-124">Specify the efficiency that you expect from the operations resource.</span></span> <span data-ttu-id="3d528-125">Tehokkuusprosentti muokkaa operatiivisen resurssin tuotantokapasiteettia ja vaikuttaa resurssille varattavaan aikaan.</span><span class="sxs-lookup"><span data-stu-id="3d528-125">The efficiency percentage adjusts the throughput of the operations resource and affects the time that is reserved for the resource.</span></span>  
9. <span data-ttu-id="3d528-126">Syötä numero Työvaiheen karkeasuunnittelun prosenttiosuus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3d528-126">In the Operations scheduling percentage field, enter a number.</span></span>
    * <span data-ttu-id="3d528-127">Määritä työvaiheiden ajoituksessa käytettävän operatiivisen resurssin kapasiteetin enimmäisprosentti.</span><span class="sxs-lookup"><span data-stu-id="3d528-127">Specify the maximum percentage of capacity of the operations resource that you want to use in operations scheduling.</span></span>  
10. <span data-ttu-id="3d528-128">Valitse Rajallinen kapasiteetti -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="3d528-128">Select Yes in the Finite capacity field.</span></span>
    * <span data-ttu-id="3d528-129">Määritä tämän vaihtoehdon arvoksi Kyllä, jos operatiivinen resurssi tulee ajoittaa käytettävissä olevan toteutuneen kapasiteetin perusteella ja aiemmin määritetyt kapasiteettivaraukset tulee ottaa huomioon.</span><span class="sxs-lookup"><span data-stu-id="3d528-129">Set this option to Yes if the operations resource should be scheduled based on the actual capacity that is available, and if existing capacity reservations should be considered.</span></span> <span data-ttu-id="3d528-130">Jos tämän asetuksen arvoksi on määritetty Ei, operatiivisella resurssin kapasiteetin oletetaan olevan rajaton, ja resurssi saatetaan ylivarata.</span><span class="sxs-lookup"><span data-stu-id="3d528-130">If this option is set to No, the operations resource is assumed to have infinite capacity, and the resource might be overbooked.</span></span>  
11. <span data-ttu-id="3d528-131">Valitse Pullonkaularesurssi-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="3d528-131">Select Yes in the Bottleneck resource field.</span></span>

## <a name="define-working-times"></a><span data-ttu-id="3d528-132">Työaikojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3d528-132">Define working times</span></span>
1. <span data-ttu-id="3d528-133">Laajenna Kalenterit-osa.</span><span class="sxs-lookup"><span data-stu-id="3d528-133">Expand the Calendars section.</span></span>
2. <span data-ttu-id="3d528-134">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="3d528-134">Click Add.</span></span>
3. <span data-ttu-id="3d528-135">Syötä tai valitse arvo Kalenteri-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3d528-135">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="3d528-136">Määritä työaikakalenteri, joka määrittää resurssin kapasiteetin (tunteina).</span><span class="sxs-lookup"><span data-stu-id="3d528-136">Specify the working time calendar that defines the capacity (in hours) of the resource.</span></span>  
4. <span data-ttu-id="3d528-137">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="3d528-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="3d528-138">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="3d528-138">In the list, click the link in the selected row.</span></span>

## <a name="define-resource-capabilities"></a><span data-ttu-id="3d528-139">Määritä resurssin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="3d528-139">Define resource capabilities</span></span>
1. <span data-ttu-id="3d528-140">Laajenna Ominaisuudet-osa.</span><span class="sxs-lookup"><span data-stu-id="3d528-140">Expand the Capabilities section.</span></span>
2. <span data-ttu-id="3d528-141">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="3d528-141">Click Add.</span></span>
    * <span data-ttu-id="3d528-142">Toiminto on operatiivisen resurssin kyky suorittaa tietty aktiviteetti.</span><span class="sxs-lookup"><span data-stu-id="3d528-142">A capability is the ability of an operations resource to perform a particular activity.</span></span> <span data-ttu-id="3d528-143">Ajoitusmoduuli kohdistaa resurssit kohdistamalla kunkin aktiviteetin resurssivaatimukset käytettävissä olevien operatiivisten resurssien ominaisuuksiin.</span><span class="sxs-lookup"><span data-stu-id="3d528-143">The scheduling engine allocates resources by matching the resource requirements of each activity to the capabilities of the available operations resources.</span></span>  
3. <span data-ttu-id="3d528-144">Syötä tai valitse arvo Ominaisuus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3d528-144">In the Capability field, enter or select a value.</span></span>
4. <span data-ttu-id="3d528-145">Syötä numero Taso-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3d528-145">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="3d528-146">Määritä pätevyystaso, jonka mukaan resurssi käsittelee ominaisuuden.</span><span class="sxs-lookup"><span data-stu-id="3d528-146">Specify the level of proficiency by which the resource processes the capability.</span></span>  
5. <span data-ttu-id="3d528-147">Syötä numero Prioriteetti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3d528-147">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="3d528-148">Määritä ominaisuuteen liittyvä operatiivisen resurssin prioriteetti.</span><span class="sxs-lookup"><span data-stu-id="3d528-148">Specify the priority of the operations resource with respect to the capability.</span></span> <span data-ttu-id="3d528-149">Kun ajoitus tehdään prioriteetin mukaan, ensimmäiseksi valitaan korkeimman prioriteetin omaava operatiivinen resurssi (pienin numeerinen arvo).</span><span class="sxs-lookup"><span data-stu-id="3d528-149">When scheduling by priority, the operations resource with the highest priority (lowest numeric value) is selected first.</span></span>  

## <a name="assign-resource-to-resource-group"></a><span data-ttu-id="3d528-150">Resurssin määrittäminen resurssiryhmään</span><span class="sxs-lookup"><span data-stu-id="3d528-150">Assign resource to resource group</span></span>
1. <span data-ttu-id="3d528-151">Laajenna Resurssiryhmät-osa.</span><span class="sxs-lookup"><span data-stu-id="3d528-151">Expand the Resource groups section.</span></span>
2. <span data-ttu-id="3d528-152">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="3d528-152">Click Add.</span></span>
    * <span data-ttu-id="3d528-153">Resurssiryhmä määrittää operatiivisten resurssien toimipaikan, tuotantoyksikön ja varaston kontekstin.</span><span class="sxs-lookup"><span data-stu-id="3d528-153">The resource group defines the site, production unit, and warehouse context for operations resources.</span></span> <span data-ttu-id="3d528-154">Operatiivinen resurssi voidaan ajoittaa vain, kun se on määritetty resurssiryhmään. Ajoitus voidaan tehdä vain resurssiryhmän toimipaikassa.</span><span class="sxs-lookup"><span data-stu-id="3d528-154">The operations resource can only be scheduled when assigned to a resource group, and only on the site where the resource group is located.</span></span>  
3. <span data-ttu-id="3d528-155">Syötä tai valitse arvo Resurssiryhmä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3d528-155">In the Resource group field, enter or select a value.</span></span>
4. <span data-ttu-id="3d528-156">Syötä tai valitse arvo Syötön sijainti -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3d528-156">In the Input location field, enter or select a value.</span></span>
    * <span data-ttu-id="3d528-157">Määritä varaston sijainti, josta operatiivinen resurssi käyttää materiaaleja.</span><span class="sxs-lookup"><span data-stu-id="3d528-157">Specify the warehouse location from where the operations resource is consuming materials.</span></span>  

