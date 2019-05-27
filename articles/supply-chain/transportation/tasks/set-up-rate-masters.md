---
title: Määritä päätiedot
description: Tässä menettelyssä näytetään, miten hinnan päätiedot määritetään.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 462bfce89fa77c8830a93a22b0dd6c8c8fb2cde6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555303"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="336d5-103">Määritä päätiedot</span><span class="sxs-lookup"><span data-stu-id="336d5-103">Set up rate masters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="336d5-104">Tässä menettelyssä näytetään, miten hinnan päätiedot määritetään.</span><span class="sxs-lookup"><span data-stu-id="336d5-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="336d5-105">Logistiikkapäällikkö määrittää yleensä hinnan päätiedot rahdinkuljettajien kanssa tehtyjen sopimusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="336d5-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="336d5-106">Tässä skenaariossa määritetään lentoyhtiön hinnan päätiedot.</span><span class="sxs-lookup"><span data-stu-id="336d5-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="336d5-107">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="336d5-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-rate-master"></a><span data-ttu-id="336d5-108">Hinnan päätietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="336d5-108">Set up rate master</span></span>
1. <span data-ttu-id="336d5-109">Valitse Kuljetustenhallinta > Asetukset > Luokitus > Hinnan päätiedot.</span><span class="sxs-lookup"><span data-stu-id="336d5-109">Go to Transportation management > Setup > Rating > Rate master.</span></span>
2. <span data-ttu-id="336d5-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="336d5-110">Click New.</span></span>
3. <span data-ttu-id="336d5-111">Syötä Hinnan päätiedot -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="336d5-111">In the Rate master field, type a value.</span></span>
4. <span data-ttu-id="336d5-112">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="336d5-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="336d5-113">Avaa haku valitsemalla Luokituksen metatietojen tunnus -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="336d5-113">In the Rating metadata ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="336d5-114">Luokituksen metatietojen tunnus määrittää hinnan päätiedoissa tarvittavat tiedot. Se määrittää näitä hinnan päätietoja käyttävän TMS-laskennan odottamat metatiedot.</span><span class="sxs-lookup"><span data-stu-id="336d5-114">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the TMS engine using this rate master.</span></span>  
6. <span data-ttu-id="336d5-115">Tässä esimerkissä valitaan P2P-asetus.</span><span class="sxs-lookup"><span data-stu-id="336d5-115">For this example, select the P2P option</span></span>
7. <span data-ttu-id="336d5-116">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="336d5-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="336d5-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="336d5-117">Click Save.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="336d5-118">Hintaperusteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="336d5-118">Set up rate base</span></span>
1. <span data-ttu-id="336d5-119">Valitse Hintaperuste.</span><span class="sxs-lookup"><span data-stu-id="336d5-119">Click Rate base.</span></span>
    * <span data-ttu-id="336d5-120">Hintaperuste määrittää rahdinkuljettajan hinnan. Sitä voidaan käyttää tariffirakenteen määrittämisessä, koska se muodostaa tauon päätietojen keskeytyskohdissa määritettyjen hintojen rakenteet.</span><span class="sxs-lookup"><span data-stu-id="336d5-120">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="336d5-121">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="336d5-121">Click New.</span></span>
3. <span data-ttu-id="336d5-122">Syötä Hintaperuste-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="336d5-122">In the Rate base field, type a value.</span></span>
4. <span data-ttu-id="336d5-123">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="336d5-123">In the Name field, type a value.</span></span>
5. <span data-ttu-id="336d5-124">Avaa haku valitsemalla Tauon päätiedot -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="336d5-124">In the Break master field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="336d5-125">Tauon päätietoja käytetään hinnoittelurakenteen ja sen keskeytyskohtien määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="336d5-125">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="336d5-126">Hinnoittelurakenteessa käytetään fyysisiin dimensioihin perustuvia hinnoittelutasoja.</span><span class="sxs-lookup"><span data-stu-id="336d5-126">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="336d5-127">Tässä esimerkissä käytetään painoa</span><span class="sxs-lookup"><span data-stu-id="336d5-127">For this example, use weight</span></span>
7. <span data-ttu-id="336d5-128">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="336d5-128">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="336d5-129">Ota käyttöön Tiedot-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="336d5-129">Toggle the expansion of the Details section.</span></span>
9. <span data-ttu-id="336d5-130">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="336d5-130">Click New.</span></span>
10. <span data-ttu-id="336d5-131">Syötä Jättöpaikan postinumero kohteesta -kenttään 30301.</span><span class="sxs-lookup"><span data-stu-id="336d5-131">In the Drop-off Postal Code From field, type '30301'.</span></span>
11. <span data-ttu-id="336d5-132">Syötä Jättöpaikan postinumero kohteelle -kenttään 30318.</span><span class="sxs-lookup"><span data-stu-id="336d5-132">In the Drop-off Postal Code To field, type '30318'.</span></span>
12. <span data-ttu-id="336d5-133">Syötä Jättömaa/-alue-kenttään Suomi.</span><span class="sxs-lookup"><span data-stu-id="336d5-133">In the Drop-off Country Region field, type 'USA'.</span></span>
13. <span data-ttu-id="336d5-134">Kirjoita Alle 1,00 kg -kenttään 100.</span><span class="sxs-lookup"><span data-stu-id="336d5-134">In the <1.00 Lbs field, type '100'.</span></span>
    * <span data-ttu-id="336d5-135">Lisää hinta per kilo, jos kuorman kokonaispaino on alle 1 kilo.</span><span class="sxs-lookup"><span data-stu-id="336d5-135">Insert the rate per lbs if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="336d5-136">Kirjoita < 5,00 kg -kenttään 300.</span><span class="sxs-lookup"><span data-stu-id="336d5-136">In the <5.00 Lbs field, type '300'.</span></span>
    * <span data-ttu-id="336d5-137">Lisää hinta per kilo, jos kuorman kokonaispaino on alle 5 kiloa.</span><span class="sxs-lookup"><span data-stu-id="336d5-137">Insert the rate per lbs if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="336d5-138">Kirjoita < 20,00 kg -kenttään 500.</span><span class="sxs-lookup"><span data-stu-id="336d5-138">In the <20.00 Lbs field, type '500'.</span></span>
    * <span data-ttu-id="336d5-139">Lisää hinta per kilo, jos kuorman kokonaispaino on alle 20 kiloa.</span><span class="sxs-lookup"><span data-stu-id="336d5-139">Insert the rate per lbs if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="336d5-140">Kirjoita < 100,00 kg -kenttään 1000.</span><span class="sxs-lookup"><span data-stu-id="336d5-140">In the <100.00 Lbs field, type '1000'.</span></span>
    * <span data-ttu-id="336d5-141">Lisää hinta per kilo, jos kuorman kokonaispaino on alle 100 kiloa.</span><span class="sxs-lookup"><span data-stu-id="336d5-141">Insert the rate per lbs if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="336d5-142">Kirjoita < 1.000,00 kg -kenttään 3000.</span><span class="sxs-lookup"><span data-stu-id="336d5-142">In the <1,000.00 Lbs field, type '3000'.</span></span>
    * <span data-ttu-id="336d5-143">Lisää hinta per kilo, jos kuorman kokonaispaino on alle 1 000 kiloa.</span><span class="sxs-lookup"><span data-stu-id="336d5-143">Insert the rate per lbs if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="336d5-144">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="336d5-144">Click Save.</span></span>
19. <span data-ttu-id="336d5-145">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="336d5-145">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="336d5-146">Hintaperusteen liittäminen</span><span class="sxs-lookup"><span data-stu-id="336d5-146">Assign rate base</span></span>
1. <span data-ttu-id="336d5-147">Ota käyttöön Hintaan perustuvat määritykset -osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="336d5-147">Toggle the expansion of the Rate base assignments section.</span></span>
2. <span data-ttu-id="336d5-148">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="336d5-148">Click New.</span></span>
    * <span data-ttu-id="336d5-149">Kaikissa hinnan päätiedoissa voi olla useita hintaan perustuvia määrityksiä.</span><span class="sxs-lookup"><span data-stu-id="336d5-149">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="336d5-150">Näin jokaiselle rahdinkuljettajalle voidaan luoda useita eri hintapisteitä kohteista, palveluista ja eri hintaperusteista riippuen.</span><span class="sxs-lookup"><span data-stu-id="336d5-150">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="336d5-151">Tässä menettelyssä luodaan vain yksi hintaan perustuvan määritys.</span><span class="sxs-lookup"><span data-stu-id="336d5-151">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="336d5-152">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="336d5-152">In the Name field, type a value.</span></span>
4. <span data-ttu-id="336d5-153">Avaa haku valitsemalla Hintaperuste-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="336d5-153">In the Rate base field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="336d5-154">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="336d5-154">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="336d5-155">Avaa haku valitsemalla Palvelu-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="336d5-155">In the Service field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="336d5-156">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="336d5-156">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="336d5-157">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="336d5-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="336d5-158">Kirjoita Noudon postinumero -kenttään 98052.</span><span class="sxs-lookup"><span data-stu-id="336d5-158">In the Pick-up Postal Code field, type '98052'.</span></span>
    * <span data-ttu-id="336d5-159">Määritä postinumero, josta alkaen tämä hintaan perustuva määritys on voimassa.</span><span class="sxs-lookup"><span data-stu-id="336d5-159">Specify which postal code this rate base assignment should be valid from.</span></span>    
10. <span data-ttu-id="336d5-160">Syötä Noutomaa/-alue-kenttään Suomi.</span><span class="sxs-lookup"><span data-stu-id="336d5-160">In the Pick-up Country Region field, type 'USA'.</span></span>
11. <span data-ttu-id="336d5-161">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="336d5-161">Click Save.</span></span>

