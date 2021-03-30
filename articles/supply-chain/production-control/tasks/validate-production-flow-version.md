---
title: Vahvista tuotantovirta ja versio
description: Tässä menettelyssä käsitellään, miten Lean-valmistuksen uusi tuotantovirta ja ensimmäinen versio luodaan.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2bceb5b61fea55c78cb2bb65b8d7cde66679ef01
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254260"
---
# <a name="validate-a-production-flow-and-version"></a><span data-ttu-id="78f79-103">Vahvista tuotantovirta ja versio</span><span class="sxs-lookup"><span data-stu-id="78f79-103">Validate a production flow and version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="78f79-104">Tässä menettelyssä käsitellään, miten Lean-valmistuksen uusi tuotantovirta ja ensimmäinen versio luodaan.</span><span class="sxs-lookup"><span data-stu-id="78f79-104">This procedure shows how to create a new production flow and a first version for lean manufacturing.</span></span> <span data-ttu-id="78f79-105">Edellytykset: Lean-valmistuksen tuotantoparametrit ja luokka-ajan mittayksiköt on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="78f79-105">Prerequisites: The production parameters for Lean manufacturing and the units of measure for class time must be defined.</span></span> <span data-ttu-id="78f79-106">Sinun on määritettävä arvovirta ja tuotantoryhmä.</span><span class="sxs-lookup"><span data-stu-id="78f79-106">You need to define a Value stream and a Production group.</span></span> <span data-ttu-id="78f79-107">Lisätietoja Lean-valmistuksesta on teknisissä raporteissa, joissa voit tutustua tuotantovirta- ja tehtäväkäsitteisiin.</span><span class="sxs-lookup"><span data-stu-id="78f79-107">Refer to the white papers on Lean manufacturing to familiarize yourself with the concepts of production flows and activities.</span></span> <span data-ttu-id="78f79-108">Tämä menettely viittaa demotiedoissa USMF-yritykseen.</span><span class="sxs-lookup"><span data-stu-id="78f79-108">This procedure refers to the legal entity USMF in demo data.</span></span> <span data-ttu-id="78f79-109">Olettaen, että yritys on määritetty Lean-valmistukseen, muita yrityksiä voidaan käyttää.</span><span class="sxs-lookup"><span data-stu-id="78f79-109">However, assuming that the legal entity is configured for Lean manufacturing, other legal entities can be used.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="78f79-110">Luo tuotantovirta</span><span class="sxs-lookup"><span data-stu-id="78f79-110">Create a production flow</span></span>
1. <span data-ttu-id="78f79-111">Valitse Tuotannonhallinta > Asetukset > Lean-tuotantovirta > Tuotantovirrat.</span><span class="sxs-lookup"><span data-stu-id="78f79-111">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="78f79-112">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="78f79-112">Click New.</span></span>
3. <span data-ttu-id="78f79-113">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="78f79-113">In the Name field, type a value.</span></span>
4. <span data-ttu-id="78f79-114">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="78f79-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="78f79-115">Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="78f79-115">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="78f79-116">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="78f79-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="78f79-117">Arvovirta on toimintayksikkö, joka kattaa kaikki arvovirran toiminnot ja työnkulut.</span><span class="sxs-lookup"><span data-stu-id="78f79-117">A value stream is an operating unit that spans over all activities and flows of the value stream.</span></span>   <span data-ttu-id="78f79-118">Tässä vaiheessa toimintayksiköt on rajoitettu yritykseen eikä niillä ole muita toimintoja.</span><span class="sxs-lookup"><span data-stu-id="78f79-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="78f79-119">Avaa haku napsauttamalla Tuotantoryhmä-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="78f79-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="78f79-120">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="78f79-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="78f79-121">Tuotantoryhmien avulla voi määrittää tuotantoprosessin materiaalin, työn ja KET-tilit.</span><span class="sxs-lookup"><span data-stu-id="78f79-121">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="78f79-122">Tuotantovirran liittäminen kirjanpitokontekstiin edellyttää tuotantoryhmän valintaa.</span><span class="sxs-lookup"><span data-stu-id="78f79-122">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="78f79-123">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="78f79-123">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="78f79-124">Luo tuotantovirran versio</span><span class="sxs-lookup"><span data-stu-id="78f79-124">Create a production flow version</span></span>
1. <span data-ttu-id="78f79-125">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="78f79-125">Click Add.</span></span>
2. <span data-ttu-id="78f79-126">Anna päivämäärä ja kellonaika Vanhentumispäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="78f79-126">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="78f79-127">Voit päivittää version, myös aktiivisten versioiden, vanhentumispäivän koska tahansa.</span><span class="sxs-lookup"><span data-stu-id="78f79-127">You can update the Expiration date of the version at any given time, even for active versions.</span></span> <span data-ttu-id="78f79-128">Käytä version vanhentumista version käytöstäpoiston suunnitteluun.</span><span class="sxs-lookup"><span data-stu-id="78f79-128">Use the expiration of the version to plan for a phase out of a version.</span></span>  
3. <span data-ttu-id="78f79-129">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="78f79-129">Click OK.</span></span>
4. <span data-ttu-id="78f79-130">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="78f79-130">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="78f79-131">Kirjoita arvo Yksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="78f79-131">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="78f79-132">Valitse tahtiyksikkö.</span><span class="sxs-lookup"><span data-stu-id="78f79-132">Select the Takt unit.</span></span>
7. <span data-ttu-id="78f79-133">Lisää Keskimääräinen tahtiaika -kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="78f79-133">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="78f79-134">Tuotantovirran tahtiohjausta varten on määritettävä keskimääräinen tavoitetahtiaika.</span><span class="sxs-lookup"><span data-stu-id="78f79-134">For the takt control of the production flow version, define a targeted average takt time.</span></span>   <span data-ttu-id="78f79-135">Tahdin määritys on määrä/ajanjakso.</span><span class="sxs-lookup"><span data-stu-id="78f79-135">The takt is defined as quantity  per time period.</span></span>  <span data-ttu-id="78f79-136">Esimerkissä tahtiaika on 10 kappaletta 0,2 tunnissa.</span><span class="sxs-lookup"><span data-stu-id="78f79-136">In the given example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="78f79-137">Jos työaika on kahdeksan tuntia, päivittäinen työteho on silloin 400 kappaletta.</span><span class="sxs-lookup"><span data-stu-id="78f79-137">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="78f79-138">Lisää Määrä sykliä kohden -kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="78f79-138">In the Quantity per cycle field, enter a number.</span></span>
9. <span data-ttu-id="78f79-139">Laajenna tai tiivistä Versiotiedot-osa.</span><span class="sxs-lookup"><span data-stu-id="78f79-139">Expand or collapse the Version details section.</span></span>
10. <span data-ttu-id="78f79-140">Lisää Vähimmäistahtiaika-kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="78f79-140">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="78f79-141">Vähimmäistahtiajan on oltava pienempi tai yhtä suuri kuin keskimääräinen tahtiaika.</span><span class="sxs-lookup"><span data-stu-id="78f79-141">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="78f79-142">Lisää Enimmäistahtiaika-kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="78f79-142">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="78f79-143">Enimmäistahtiajan on oltava suurempi tai yhtä suuri kuin keskimääräinen tahtiaika.</span><span class="sxs-lookup"><span data-stu-id="78f79-143">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="78f79-144">Anna toteutuneen syklin keston päivinä.</span><span class="sxs-lookup"><span data-stu-id="78f79-144">Enter a number of days in the Period for actual cycle time</span></span>
    * <span data-ttu-id="78f79-145">Toteutunut syklin kesto on se määrä päiviä, jolloin töitä koostetaan toteutuneesta ajasta taaksepäin, jotta toteutunut syklin kesto voidaan laskea.</span><span class="sxs-lookup"><span data-stu-id="78f79-145">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="78f79-146">Arvoa voidaan muuttaa koska tahansa ja sitä käytetään vain toteutuneiden syklien keston laskentaan.</span><span class="sxs-lookup"><span data-stu-id="78f79-146">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="78f79-147">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="78f79-147">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]