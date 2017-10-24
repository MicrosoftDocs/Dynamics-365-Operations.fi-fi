---
title: Manuaalinen poisto
description: "Tämä artikkeli sisältää manuaalisen poistomenetelmän yleiskatsauksen."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e43b9397dd4e362eff9d78f302732e6bcc53d1db
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="manual-depreciation"></a><span data-ttu-id="35057-103">Manuaalinen poisto</span><span class="sxs-lookup"><span data-stu-id="35057-103">Manual depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="35057-104">Tämä artikkeli sisältää manuaalisen poistomenetelmän yleiskatsauksen.</span><span class="sxs-lookup"><span data-stu-id="35057-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="35057-105">Kun määrität käyttöomaisuuden poistoprofiilin ja valitset **Poistoprofiilit**-sivun **Menetelmä**-kentässä **Manuaalinen**, poistoprofiiliin määritetty käyttöomaisuuden poisto määräytyy sen prosentin mukaan, joka annetaan kalenterivuoden kullekin aikavälille.</span><span class="sxs-lookup"><span data-stu-id="35057-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="35057-106">Aikavälit, joille määrität prosenttiosuuden, kirjataan **Poistoprofiilit**-sivun **Yleinen**-pikavälilehden **Kausifrekvenssi**-kentässä valitun arvon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="35057-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="35057-107">Valittavana on seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="35057-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="35057-108">Vuosittain</span><span class="sxs-lookup"><span data-stu-id="35057-108">Yearly</span></span>
-   <span data-ttu-id="35057-109">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="35057-109">Monthly</span></span>
-   <span data-ttu-id="35057-110">Neljännesvuosittain</span><span class="sxs-lookup"><span data-stu-id="35057-110">Quarterly</span></span>
-   <span data-ttu-id="35057-111">Puolivuosittain</span><span class="sxs-lookup"><span data-stu-id="35057-111">Half-Yearly</span></span>
-   <span data-ttu-id="35057-112">Päivittäin</span><span class="sxs-lookup"><span data-stu-id="35057-112">Daily</span></span>

<span data-ttu-id="35057-113">Valitse kausifrekvenssin valinnan jälkeen **Manuaalinen aikataulu** ja määritä kunkin kirjausvälin prosenttiosuudet.</span><span class="sxs-lookup"><span data-stu-id="35057-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="35057-114">Manuaaliset aikataulut ja kirjausvälit määrittävät yhdessä poistosumman, kuten artikkelissa myöhemmin käsiteltävissä esimerkeissä.</span><span class="sxs-lookup"><span data-stu-id="35057-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="35057-115">Manuaalinen poisto lasketaan aina prosenttina hankintahinnasta.</span><span class="sxs-lookup"><span data-stu-id="35057-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="35057-116">Manuaalisissa poistoissa poistoväleille annettavien prosenttien summan ei tarvitse olla 100 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="35057-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="35057-117">Manuaalinen poisti on joustava poistomenetelmä, jota käytetään usein määritettäessä **Kirjat**-sivulla lisäpoistoprofiili, esimerkiksi muu kuin kausittainen poisto jotain erityistarkoitusta (esimerkiksi verotusta) varten.</span><span class="sxs-lookup"><span data-stu-id="35057-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="35057-118">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="35057-118">Examples</span></span>
<span data-ttu-id="35057-119">Hankintahinta: 11 000,00 Odotettavissa oleva jäännösarvo: 1 000,00 Seuraavassa taulukossa on aikavälit ja prosentit, jotka määritetään **Käyttöomaisuuserän poistoprofiilisuunnitelma** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="35057-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="35057-120">Aikavälin numero</span><span class="sxs-lookup"><span data-stu-id="35057-120">Interval number</span></span> | <span data-ttu-id="35057-121">Prosentti</span><span class="sxs-lookup"><span data-stu-id="35057-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="35057-122">1</span><span class="sxs-lookup"><span data-stu-id="35057-122">1</span></span>               | <span data-ttu-id="35057-123">10,00</span><span class="sxs-lookup"><span data-stu-id="35057-123">10.00</span></span>      |
| <span data-ttu-id="35057-124">2</span><span class="sxs-lookup"><span data-stu-id="35057-124">2</span></span>               | <span data-ttu-id="35057-125">50,00</span><span class="sxs-lookup"><span data-stu-id="35057-125">50.00</span></span>      |
| <span data-ttu-id="35057-126">3</span><span class="sxs-lookup"><span data-stu-id="35057-126">3</span></span>               | <span data-ttu-id="35057-127">8,00</span><span class="sxs-lookup"><span data-stu-id="35057-127">8.00</span></span>       |

<span data-ttu-id="35057-128">Seuraavassa taulukossa esitetään, miten kunkin aikavälin poisto lasketaan.</span><span class="sxs-lookup"><span data-stu-id="35057-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="35057-129">Aikavälin numero</span><span class="sxs-lookup"><span data-stu-id="35057-129">Interval number</span></span> | <span data-ttu-id="35057-130">Vuotuisen poistomäärän laskeminen</span><span class="sxs-lookup"><span data-stu-id="35057-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="35057-131">Nettokirjanpitoarvo aikavälin lopussa</span><span class="sxs-lookup"><span data-stu-id="35057-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="35057-132">1</span><span class="sxs-lookup"><span data-stu-id="35057-132">1</span></span>                | <span data-ttu-id="35057-133">(11 000 – 1 000) × 10 % = 1 000</span><span class="sxs-lookup"><span data-stu-id="35057-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="35057-134">10 000 (11 000 – 1 000)</span><span class="sxs-lookup"><span data-stu-id="35057-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="35057-135">2</span><span class="sxs-lookup"><span data-stu-id="35057-135">2</span></span>                | <span data-ttu-id="35057-136">(11 000 – 1 000) × 50 % = 5 000</span><span class="sxs-lookup"><span data-stu-id="35057-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="35057-137">5 000 (10 000 – 5 000)</span><span class="sxs-lookup"><span data-stu-id="35057-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="35057-138">3</span><span class="sxs-lookup"><span data-stu-id="35057-138">3</span></span>                | <span data-ttu-id="35057-139">(11 000 – 1 000) × 8 % = 800</span><span class="sxs-lookup"><span data-stu-id="35057-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="35057-140">4 200 (5 000 – 800)</span><span class="sxs-lookup"><span data-stu-id="35057-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="35057-141">Jos valitset **Kausifrekvenssi**-kentässä **Kuukausittain**, määrität 12 manuaalisen aikataulun aikaväliä.</span><span class="sxs-lookup"><span data-stu-id="35057-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="35057-142">Seuraavassa taulukossa esitellään kahden ensimmäisen aikavälin poistosummat.</span><span class="sxs-lookup"><span data-stu-id="35057-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="35057-143">Väli</span><span class="sxs-lookup"><span data-stu-id="35057-143">Interval</span></span> | <span data-ttu-id="35057-144">Poiston määrä</span><span class="sxs-lookup"><span data-stu-id="35057-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="35057-145">Tammikuu</span><span class="sxs-lookup"><span data-stu-id="35057-145">January</span></span>  | <span data-ttu-id="35057-146">(11 000 – 1 000) × 10 % = 1 000</span><span class="sxs-lookup"><span data-stu-id="35057-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="35057-147">Helmikuu</span><span class="sxs-lookup"><span data-stu-id="35057-147">February</span></span> | <span data-ttu-id="35057-148">(11 000 – 1 000) × 50 % = 5 000</span><span class="sxs-lookup"><span data-stu-id="35057-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="35057-149">Jos valitset ****Kausifrekvenssi**-kentässä** **Puolivuosittain**, määrität kaksi manuaalisen aikataulun aikaväliä.</span><span class="sxs-lookup"><span data-stu-id="35057-149">If you select **Half-Yearly** in the ****Period frequency** field**, you set up two manual schedule intervals.</span></span> <span data-ttu-id="35057-150">Seuraavassa taulukossa esitellään näiden kahden aikavälin poistosummat.</span><span class="sxs-lookup"><span data-stu-id="35057-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="35057-151">Väli</span><span class="sxs-lookup"><span data-stu-id="35057-151">Interval</span></span>    | <span data-ttu-id="35057-152">Poiston määrä</span><span class="sxs-lookup"><span data-stu-id="35057-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="35057-153">30. kesäkuuta</span><span class="sxs-lookup"><span data-stu-id="35057-153">June 30</span></span>     | <span data-ttu-id="35057-154">(11 000 – 1 000) × 10 % = 1 000</span><span class="sxs-lookup"><span data-stu-id="35057-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="35057-155">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="35057-155">December 31</span></span> | <span data-ttu-id="35057-156">(11 000 – 1 000) × 50 % = 5 000</span><span class="sxs-lookup"><span data-stu-id="35057-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="35057-157">Aikavälien prosenttien yhteissumman ei tarvitse olla 100.</span><span class="sxs-lookup"><span data-stu-id="35057-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="35057-158">Näyttöön avautuu kuitenkin sanoma, jos **Käyttöomaisuuserän poistoprofiilisuunnitelma** -sivun **Kumulatiivinen prosentti** -kentän arvo ei ole **100**.</span><span class="sxs-lookup"><span data-stu-id="35057-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>




