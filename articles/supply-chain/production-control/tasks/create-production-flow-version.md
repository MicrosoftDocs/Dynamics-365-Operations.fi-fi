---
title: Luo tuotantovirran versio
description: Tässä menettelyssä selvitetään uuden tuotantovirtaversion luomista.
author: cvocph
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a4b4847046af541644338157d95e6fcba315f9c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828991"
---
# <a name="create-a-production-flow-version"></a><span data-ttu-id="8a266-103">Luo tuotantovirran versio</span><span class="sxs-lookup"><span data-stu-id="8a266-103">Create a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8a266-104">Tässä menettelyssä selvitetään uuden tuotantovirtaversion luomista.</span><span class="sxs-lookup"><span data-stu-id="8a266-104">This procedure focuses on creating a new production flow version.</span></span> <span data-ttu-id="8a266-105">Tässä menettelyssä Lean-valmistuksen tuotantoparametrit ja luokka-ajan mittayksiköt on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="8a266-105">For this procedure, the production parameters for lean manufacturing and the units of measurement for class time must be defined.</span></span> <span data-ttu-id="8a266-106">Myös arvovirta ja tuotantoryhmä on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="8a266-106">You also need to define a value stream and a production group.</span></span> <span data-ttu-id="8a266-107">Lisätietoja Lean-valmistuksen tuotantovirroista ja tehtävistä on Microsoft Dynamics AX:n Lean-valmistusta käsittelevissä teknisissä raporteissa.</span><span class="sxs-lookup"><span data-stu-id="8a266-107">To learn more about production flows and activities in lean manufacturing, see the white papers on Lean manufacturing for Microsoft Dynamics AX.</span></span> <span data-ttu-id="8a266-108">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="8a266-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="8a266-109">Luo tuotantovirta</span><span class="sxs-lookup"><span data-stu-id="8a266-109">Create a production flow</span></span>
1. <span data-ttu-id="8a266-110">Valitse Tuotannonhallinta > Asetukset > Lean-tuotantovirta > Tuotantovirrat.</span><span class="sxs-lookup"><span data-stu-id="8a266-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="8a266-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8a266-111">Click New.</span></span>
3. <span data-ttu-id="8a266-112">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8a266-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="8a266-113">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8a266-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8a266-114">Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="8a266-114">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="8a266-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8a266-115">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8a266-116">Valitse toimintayksikön tyypiksi arvovirta.</span><span class="sxs-lookup"><span data-stu-id="8a266-116">Select an operating unit of type value stream.</span></span> <span data-ttu-id="8a266-117">Arvovirta on toimintayksikkö, joka kattaa kaikki arvovirran toiminnot ja työnkulut.</span><span class="sxs-lookup"><span data-stu-id="8a266-117">A value stream is an operating unit that spans all activities and flows of the value stream.</span></span> <span data-ttu-id="8a266-118">Tässä vaiheessa toimintayksiköt on rajoitettu yritykseen eikä niillä ole muita toimintoja.</span><span class="sxs-lookup"><span data-stu-id="8a266-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="8a266-119">Avaa haku napsauttamalla Tuotantoryhmä-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="8a266-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="8a266-120">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8a266-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8a266-121">Valitse tuotantovirran tuotantoryhmä.</span><span class="sxs-lookup"><span data-stu-id="8a266-121">Select a production group for the production flow.</span></span> <span data-ttu-id="8a266-122">Tuotantoryhmien avulla voi määrittää tuotantoprosessin materiaalin, työn ja KET-tilit.</span><span class="sxs-lookup"><span data-stu-id="8a266-122">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="8a266-123">Tuotantovirran liittäminen kirjanpitokontekstiin edellyttää tuotantoryhmän valintaa.</span><span class="sxs-lookup"><span data-stu-id="8a266-123">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="8a266-124">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8a266-124">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="8a266-125">Luo tuotantovirran versio</span><span class="sxs-lookup"><span data-stu-id="8a266-125">Create a production flow version</span></span>
1. <span data-ttu-id="8a266-126">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="8a266-126">Click Add.</span></span>
2. <span data-ttu-id="8a266-127">Anna päivämäärä ja kellonaika Vanhentumispäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8a266-127">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="8a266-128">Määritä tarvittaessa version vanhentumispäivä.</span><span class="sxs-lookup"><span data-stu-id="8a266-128">If required, define an Expiration date for the version.</span></span> <span data-ttu-id="8a266-129">Voit päivittää sen koska tahansa myös aktiivisissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="8a266-129">You can update it at any given time, even for active versions.</span></span> <span data-ttu-id="8a266-130">Voit suunnitella sen avulla version käytöstä poistamisen.</span><span class="sxs-lookup"><span data-stu-id="8a266-130">You can use it to plan to phase out a version.</span></span>  
3. <span data-ttu-id="8a266-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8a266-131">Click OK.</span></span>
4. <span data-ttu-id="8a266-132">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="8a266-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="8a266-133">Kirjoita arvo Yksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8a266-133">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="8a266-134">Ratkaise muutokset tahtiyksikössä</span><span class="sxs-lookup"><span data-stu-id="8a266-134">ResolveChanges the Takt unit.</span></span>
7. <span data-ttu-id="8a266-135">Lisää Keskimääräinen tahtiaika -kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="8a266-135">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="8a266-136">Määritä version keskimääräinen tahtiaika.</span><span class="sxs-lookup"><span data-stu-id="8a266-136">Define the Average takt time of the version.</span></span> <span data-ttu-id="8a266-137">Tuotantovirran tahtiohjausta varten on määritettävä keskimääräinen tavoitetahtiaika.</span><span class="sxs-lookup"><span data-stu-id="8a266-137">For the takt control of the production flow version, define a targeted average takt time.</span></span> <span data-ttu-id="8a266-138">Tahdin määritys on määrä/ajanjakso.</span><span class="sxs-lookup"><span data-stu-id="8a266-138">The takt is defined as quantity per time period.</span></span> <span data-ttu-id="8a266-139">Esimerkissä tahtiaika on 10 kappaletta 0,2 tunnissa.</span><span class="sxs-lookup"><span data-stu-id="8a266-139">In the example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="8a266-140">Jos työaika on kahdeksan tuntia, päivittäinen työteho on silloin 400 kappaletta.</span><span class="sxs-lookup"><span data-stu-id="8a266-140">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="8a266-141">Lisää Määrä sykliä kohden -kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="8a266-141">In the Quantity per cycle field, enter a number.</span></span>
    * <span data-ttu-id="8a266-142">Määritä keskimääräiseen tahtiaikaan liittyvä jaksottainen määrä.</span><span class="sxs-lookup"><span data-stu-id="8a266-142">Define the quantity per cycle related to the Average takt time.</span></span>  
9. <span data-ttu-id="8a266-143">Ota käyttöön Versiotiedot-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="8a266-143">Toggle the expansion of the Version details section.</span></span>
10. <span data-ttu-id="8a266-144">Lisää Vähimmäistahtiaika-kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="8a266-144">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="8a266-145">Määritä vähimmäistahtiaika.</span><span class="sxs-lookup"><span data-stu-id="8a266-145">Define the minimum takt time.</span></span> <span data-ttu-id="8a266-146">Vähimmäistahtiajan on oltava pienempi tai yhtä suuri kuin keskimääräinen tahtiaika.</span><span class="sxs-lookup"><span data-stu-id="8a266-146">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="8a266-147">Lisää Enimmäistahtiaika-kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="8a266-147">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="8a266-148">Enimmäistahtiajan on oltava suurempi tai yhtä suuri kuin keskimääräinen tahtiaika.</span><span class="sxs-lookup"><span data-stu-id="8a266-148">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="8a266-149">Lisää Toteutunut syklin kesto (päivinä) -kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="8a266-149">In the Period for actual cycle time (days) field, enter a number.</span></span>
    * <span data-ttu-id="8a266-150">Anna toteutuneen syklin keston päivien määrä.</span><span class="sxs-lookup"><span data-stu-id="8a266-150">Enter the number of days in the Period for actual cycle time.</span></span> <span data-ttu-id="8a266-151">Toteutunut syklin kesto on se määrä päiviä, jolloin töitä koostetaan toteutuneesta ajasta taaksepäin, jotta toteutunut syklin kesto voidaan laskea.</span><span class="sxs-lookup"><span data-stu-id="8a266-151">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="8a266-152">Arvoa voidaan muuttaa koska tahansa ja sitä käytetään vain toteutuneiden syklien keston laskentaan.</span><span class="sxs-lookup"><span data-stu-id="8a266-152">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="8a266-153">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8a266-153">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]