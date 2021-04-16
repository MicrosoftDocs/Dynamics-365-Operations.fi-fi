---
title: Määritä päätiedot
description: Tässä menettelyssä näytetään, miten hinnan päätiedot määritetään.
author: ShylaThompson
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cb25726e05f11420c7355c39f7e262abca5da62
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808987"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="a5aa0-103">Määritä päätiedot</span><span class="sxs-lookup"><span data-stu-id="a5aa0-103">Set up rate masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a5aa0-104">Tässä menettelyssä näytetään, miten hinnan päätiedot määritetään.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="a5aa0-105">Logistiikkapäällikkö määrittää yleensä hinnan päätiedot rahdinkuljettajien kanssa tehtyjen sopimusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="a5aa0-106">Tässä skenaariossa määritetään lentoyhtiön hinnan päätiedot.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="a5aa0-107">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-break-master"></a><span data-ttu-id="a5aa0-108">Tauon päätietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a5aa0-108">Set up break master</span></span>

1. <span data-ttu-id="a5aa0-109">Valitse **Kuljetustenhallinta > Määritys > Luokitus > Tauon päätiedot**.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-109">Go to **Transportation management > Setup > Rating > Break master**.</span></span> <span data-ttu-id="a5aa0-110">Tauon päätietoja käytetään hinnoittelurakenteen ja sen keskeytyskohtien määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-110">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="a5aa0-111">Hinnoittelurakenteessa käytetään fyysisiin dimensioihin perustuvia hinnoittelutasoja.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-111">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
1. <span data-ttu-id="a5aa0-112">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-112">Select **New**.</span></span>
1. <span data-ttu-id="a5aa0-113">Anna arvo **Tauon päätiedot** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-113">In the **Break master** field, enter a value.</span></span>
1. <span data-ttu-id="a5aa0-114">Anna **Nimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="a5aa0-115">Valitse **Tietotyyppi**-kentässä tietotyyppi.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-115">In the **Data type** field, select the data type.</span></span>
1. <span data-ttu-id="a5aa0-116">Anna **Vertailu**-kentässä pyydetty vertailulaji (operaattorien avulla).</span><span class="sxs-lookup"><span data-stu-id="a5aa0-116">In the **Comparison** field, enter the kind of comparison requested (using operators).</span></span>
1. <span data-ttu-id="a5aa0-117">Anna **Hajota yksikkö** -kentässä jakoyksikkö.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-117">In the **Break unit** field, enter the break unit.</span></span>
1. <span data-ttu-id="a5aa0-118">Luo **Tiedot**-osassa hinnoittelurakenteeseen tarvittava määrä jakoja.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-118">In the **Details** section, create as many breaks as needed for the pricing structure.</span></span>
1. <span data-ttu-id="a5aa0-119">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-119">Select **Save**.</span></span>

## <a name="set-up-rate-master"></a><span data-ttu-id="a5aa0-120">Hinnan päätietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a5aa0-120">Set up rate master</span></span>

1. <span data-ttu-id="a5aa0-121">Valitse **Kuljetustenhallinta > Asetukset > Luokitus > Hinnan päätiedot**.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-121">Go to **Transportation management > Setup > Rating > Rate master**.</span></span>
1. <span data-ttu-id="a5aa0-122">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-122">Select **New**.</span></span>
1. <span data-ttu-id="a5aa0-123">Anna arvo **Hinnan päätiedot** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-123">In the **Rate master** field, type a value.</span></span>
1. <span data-ttu-id="a5aa0-124">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-124">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="a5aa0-125">Avaa haku valitsemalla **Luokituksen metatietojen tunnus** -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-125">In the **Rating metadata ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="a5aa0-126">Luokituksen metatietojen tunnus määrittää hinnan päätiedoissa tarvittavat tiedot. Se määrittää näitä hinnan päätietoja käyttävän kuljetuksen hallintamoduulin odottamat metatiedot.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-126">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the transportation management engine using this rate master.</span></span>  
1. <span data-ttu-id="a5aa0-127">Tässä esimerkissä valitaan P2P-asetus.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-127">For this example, select the P2P option.</span></span> <span data-ttu-id="a5aa0-128">Tämä on jo määritetty esittelytiedoissa.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-128">This is already defined in the demo data.</span></span>
1. <span data-ttu-id="a5aa0-129">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-129">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="a5aa0-130">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-130">Select **Save**.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="a5aa0-131">Hintaperusteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a5aa0-131">Set up rate base</span></span>

1. <span data-ttu-id="a5aa0-132">Valitse **Hintaperuste**.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-132">Select **Rate base**.</span></span>
    * <span data-ttu-id="a5aa0-133">Hintaperuste määrittää rahdinkuljettajan hinnan. Sitä voidaan käyttää tariffirakenteen määrittämisessä, koska se muodostaa tauon päätietojen keskeytyskohdissa määritettyjen hintojen rakenteet.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-133">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="a5aa0-134">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-134">Select **New**.</span></span>
3. <span data-ttu-id="a5aa0-135">Anna arvo **Hintaperuste**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-135">In the **Rate base** field, type a value.</span></span>
4. <span data-ttu-id="a5aa0-136">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-136">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="a5aa0-137">Avaa haku valitsemalla **Tauon päätiedot** -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-137">In the **Break master** field, select the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a5aa0-138">Tauon päätietoja käytetään hinnoittelurakenteen ja sen keskeytyskohtien määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-138">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="a5aa0-139">Hinnoittelurakenteessa käytetään fyysisiin dimensioihin perustuvia hinnoittelutasoja.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-139">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="a5aa0-140">Tässä esimerkissä käytetään painoa.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-140">For this example, use weight.</span></span> <span data-ttu-id="a5aa0-141">Tämä on jo määritetty esittelytiedoissa.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-141">This is already defined in the demo data.</span></span>
7. <span data-ttu-id="a5aa0-142">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-142">In the list, select the link in the highlighted row.</span></span>
8. <span data-ttu-id="a5aa0-143">Laajenna **Tiedot**-osa.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-143">Expand the **Details** section.</span></span>
9. <span data-ttu-id="a5aa0-144">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-144">Select **New**.</span></span>
10. <span data-ttu-id="a5aa0-145">Anna **Jättöpaikan postinumero kohteesta** -kentässä 30301.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-145">In the **Drop-off Postal Code From** field, type "30301".</span></span>
11. <span data-ttu-id="a5aa0-146">Anna **Jättöpaikan postinumero kohteelle** -kentässä 30318.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-146">In the **Drop-off Postal Code To** field, type "30318".</span></span>
12. <span data-ttu-id="a5aa0-147">Anna **Jättömaa/-alue**-kentässä Suomi.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-147">In the **Drop-off Country Region** field, type "USA".</span></span>
13. <span data-ttu-id="a5aa0-148">Anna **Alle 1,00 kg** -kentässä 100.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-148">In the **<1.00 Lbs** field, type "100".</span></span>
    * <span data-ttu-id="a5aa0-149">Lisää hinta per kilo, jos kuorman kokonaispaino on alle 1 kilo.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-149">Insert the rate per pounds if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="a5aa0-150">Anna **Alle 5,00 kg** -kentässä 300.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-150">In the **<5.00 Lbs** field, type "300".</span></span>
    * <span data-ttu-id="a5aa0-151">Lisää hinta per kilo, jos kuorman kokonaispaino on alle 5 kiloa.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-151">Insert the rate per pounds if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="a5aa0-152">Anna **Alle 20,00 kg** -kentässä 500.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-152">In the **<20.00 Lbs** field, type "500".</span></span>
    * <span data-ttu-id="a5aa0-153">Lisää hinta per kilo, jos kuorman kokonaispaino on alle 20 kiloa.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-153">Insert the rate per pounds if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="a5aa0-154">Anna **Alle 100,00 kg** -kentässä 1000.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-154">In the **<100.00 Lbs** field, type "1000".</span></span>
    * <span data-ttu-id="a5aa0-155">Lisää hinta per kilo, jos kuorman kokonaispaino on alle 100 kiloa.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-155">Insert the rate per pounds if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="a5aa0-156">Anna **Alle 1000,00 kg** -kentässä 3000.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-156">In the **<1,000.00 Lbs** field, type "3000".</span></span>
    * <span data-ttu-id="a5aa0-157">Lisää hinta per kilo, jos kuorman kokonaispaino on alle 1000 kiloa.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-157">Insert the rate per pounds if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="a5aa0-158">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-158">Select **Save**.</span></span>
19. <span data-ttu-id="a5aa0-159">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-159">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="a5aa0-160">Hintaperusteen liittäminen</span><span class="sxs-lookup"><span data-stu-id="a5aa0-160">Assign rate base</span></span>

1. <span data-ttu-id="a5aa0-161">Laajenna **Hintaan perustuvat määritykset** -osa.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-161">Expand the **Rate base assignments** section.</span></span>
2. <span data-ttu-id="a5aa0-162">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-162">Select **New**.</span></span>
    * <span data-ttu-id="a5aa0-163">Kaikissa hinnan päätiedoissa voi olla useita hintaan perustuvia määrityksiä.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-163">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="a5aa0-164">Näin jokaiselle rahdinkuljettajalle voidaan luoda useita eri hintapisteitä kohteista, palveluista ja eri hintaperusteista riippuen.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-164">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="a5aa0-165">Tässä menettelyssä luodaan vain yksi hintaan perustuvan määritys.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-165">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="a5aa0-166">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-166">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="a5aa0-167">Avaa haku valitsemalla **Hintaperuste**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-167">In the **Rate base** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a5aa0-168">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-168">In the list, select the link in the highlighted row.</span></span>
6. <span data-ttu-id="a5aa0-169">Avaa haku valitsemalla **Palvelu**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-169">In the **Service** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="a5aa0-170">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-170">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="a5aa0-171">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-171">In the list, select the link in the highlighted row.</span></span>
9. <span data-ttu-id="a5aa0-172">Anna **Noudon postinumero** -kentässä 98052.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-172">In the **Pick-up Postal Code** field, type "98052".</span></span>
    * <span data-ttu-id="a5aa0-173">Määritä postinumero, josta alkaen tämä hintaan perustuva määritys on voimassa.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-173">Specify which postal code this rate base assignment should be valid from.</span></span>
10. <span data-ttu-id="a5aa0-174">Anna **Noutomaa/-alue**-kentässä Suomi.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-174">In the **Pick-up Country Region** field, type "USA".</span></span>
11. <span data-ttu-id="a5aa0-175">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a5aa0-175">Select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]