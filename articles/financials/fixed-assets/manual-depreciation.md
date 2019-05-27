---
title: Manuaalinen poisto
description: Tämä artikkeli sisältää manuaalisen poistomenetelmän yleiskatsauksen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14e385e60e10146a0855a467af57a0a31fcc53bd
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558732"
---
# <a name="manual-depreciation"></a><span data-ttu-id="ba445-103">Manuaalinen poisto</span><span class="sxs-lookup"><span data-stu-id="ba445-103">Manual depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba445-104">Tämä artikkeli sisältää manuaalisen poistomenetelmän yleiskatsauksen.</span><span class="sxs-lookup"><span data-stu-id="ba445-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="ba445-105">Kun määrität käyttöomaisuuden poistoprofiilin ja valitset **Poistoprofiilit**-sivun **Menetelmä**-kentässä **Manuaalinen**, poistoprofiiliin määritetty käyttöomaisuuden poisto määräytyy sen prosentin mukaan, joka annetaan kalenterivuoden kullekin aikavälille.</span><span class="sxs-lookup"><span data-stu-id="ba445-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="ba445-106">Aikavälit, joille määrität prosenttiosuuden, kirjataan **Poistoprofiilit**-sivun **Yleinen**-pikavälilehden **Kausifrekvenssi**-kentässä valitun arvon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="ba445-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="ba445-107">Valittavana on seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ba445-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="ba445-108">Vuosittain</span><span class="sxs-lookup"><span data-stu-id="ba445-108">Yearly</span></span>
-   <span data-ttu-id="ba445-109">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="ba445-109">Monthly</span></span>
-   <span data-ttu-id="ba445-110">Neljännesvuosittain</span><span class="sxs-lookup"><span data-stu-id="ba445-110">Quarterly</span></span>
-   <span data-ttu-id="ba445-111">Puolivuosittain</span><span class="sxs-lookup"><span data-stu-id="ba445-111">Half-Yearly</span></span>
-   <span data-ttu-id="ba445-112">Päivittäin</span><span class="sxs-lookup"><span data-stu-id="ba445-112">Daily</span></span>

<span data-ttu-id="ba445-113">Valitse kausifrekvenssin valinnan jälkeen **Manuaalinen aikataulu** ja määritä kunkin kirjausvälin prosenttiosuudet.</span><span class="sxs-lookup"><span data-stu-id="ba445-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="ba445-114">Manuaaliset aikataulut ja kirjausvälit määrittävät yhdessä poistosumman, kuten artikkelissa myöhemmin käsiteltävissä esimerkeissä.</span><span class="sxs-lookup"><span data-stu-id="ba445-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="ba445-115">Manuaalinen poisto lasketaan aina prosenttina hankintahinnasta.</span><span class="sxs-lookup"><span data-stu-id="ba445-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="ba445-116">Manuaalisissa poistoissa poistoväleille annettavien prosenttien summan ei tarvitse olla 100 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="ba445-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="ba445-117">Manuaalinen poisti on joustava poistomenetelmä, jota käytetään usein määritettäessä **Kirjat**-sivulla lisäpoistoprofiili, esimerkiksi muu kuin kausittainen poisto jotain erityistarkoitusta (esimerkiksi verotusta) varten.</span><span class="sxs-lookup"><span data-stu-id="ba445-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="ba445-118">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="ba445-118">Examples</span></span>
<span data-ttu-id="ba445-119">Hankintahinta: 11 000,00 Odotettavissa oleva jäännösarvo: 1 000,00 Seuraavassa taulukossa on aikavälit ja prosentit, jotka määritetään **Käyttöomaisuuserän poistoprofiilisuunnitelma** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="ba445-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="ba445-120">Aikavälin numero</span><span class="sxs-lookup"><span data-stu-id="ba445-120">Interval number</span></span> | <span data-ttu-id="ba445-121">Prosentti</span><span class="sxs-lookup"><span data-stu-id="ba445-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="ba445-122">1</span><span class="sxs-lookup"><span data-stu-id="ba445-122">1</span></span>               | <span data-ttu-id="ba445-123">10,00</span><span class="sxs-lookup"><span data-stu-id="ba445-123">10.00</span></span>      |
| <span data-ttu-id="ba445-124">2</span><span class="sxs-lookup"><span data-stu-id="ba445-124">2</span></span>               | <span data-ttu-id="ba445-125">50,00</span><span class="sxs-lookup"><span data-stu-id="ba445-125">50.00</span></span>      |
| <span data-ttu-id="ba445-126">3</span><span class="sxs-lookup"><span data-stu-id="ba445-126">3</span></span>               | <span data-ttu-id="ba445-127">8,00</span><span class="sxs-lookup"><span data-stu-id="ba445-127">8.00</span></span>       |

<span data-ttu-id="ba445-128">Seuraavassa taulukossa esitetään, miten kunkin aikavälin poisto lasketaan.</span><span class="sxs-lookup"><span data-stu-id="ba445-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="ba445-129">Aikavälin numero</span><span class="sxs-lookup"><span data-stu-id="ba445-129">Interval number</span></span> | <span data-ttu-id="ba445-130">Vuotuisen poistomäärän laskeminen</span><span class="sxs-lookup"><span data-stu-id="ba445-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="ba445-131">Nettokirjanpitoarvo aikavälin lopussa</span><span class="sxs-lookup"><span data-stu-id="ba445-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="ba445-132">1</span><span class="sxs-lookup"><span data-stu-id="ba445-132">1</span></span>                | <span data-ttu-id="ba445-133">(11 000 – 1 000) × 10 % = 1 000</span><span class="sxs-lookup"><span data-stu-id="ba445-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="ba445-134">10 000 (11 000 – 1 000)</span><span class="sxs-lookup"><span data-stu-id="ba445-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="ba445-135">2</span><span class="sxs-lookup"><span data-stu-id="ba445-135">2</span></span>                | <span data-ttu-id="ba445-136">(11 000 – 1 000) × 50 % = 5 000</span><span class="sxs-lookup"><span data-stu-id="ba445-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="ba445-137">5 000 (10 000 – 5 000)</span><span class="sxs-lookup"><span data-stu-id="ba445-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="ba445-138">3</span><span class="sxs-lookup"><span data-stu-id="ba445-138">3</span></span>                | <span data-ttu-id="ba445-139">(11 000 – 1 000) × 8 % = 800</span><span class="sxs-lookup"><span data-stu-id="ba445-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="ba445-140">4 200 (5 000 – 800)</span><span class="sxs-lookup"><span data-stu-id="ba445-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="ba445-141">Jos valitset **Kausifrekvenssi**-kentässä **Kuukausittain**, määrität 12 manuaalisen aikataulun aikaväliä.</span><span class="sxs-lookup"><span data-stu-id="ba445-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="ba445-142">Seuraavassa taulukossa esitellään kahden ensimmäisen aikavälin poistosummat.</span><span class="sxs-lookup"><span data-stu-id="ba445-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="ba445-143">Väli</span><span class="sxs-lookup"><span data-stu-id="ba445-143">Interval</span></span> | <span data-ttu-id="ba445-144">Poiston määrä</span><span class="sxs-lookup"><span data-stu-id="ba445-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="ba445-145">Tammikuu</span><span class="sxs-lookup"><span data-stu-id="ba445-145">January</span></span>  | <span data-ttu-id="ba445-146">(11 000 – 1 000) × 10 % = 1 000</span><span class="sxs-lookup"><span data-stu-id="ba445-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="ba445-147">Helmikuu</span><span class="sxs-lookup"><span data-stu-id="ba445-147">February</span></span> | <span data-ttu-id="ba445-148">(11 000 – 1 000) × 50 % = 5 000</span><span class="sxs-lookup"><span data-stu-id="ba445-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="ba445-149">Jos valitset *<strong><em>Kausifrekvenssi</em>*-kentässä</strong> <strong>Puolivuosittain</strong>, määrität kaksi manuaalisen aikataulun aikaväliä.</span><span class="sxs-lookup"><span data-stu-id="ba445-149">If you select <strong>Half-Yearly</strong> in the *<strong><em>Period frequency</em>* field</strong>, you set up two manual schedule intervals.</span></span> <span data-ttu-id="ba445-150">Seuraavassa taulukossa esitellään näiden kahden aikavälin poistosummat.</span><span class="sxs-lookup"><span data-stu-id="ba445-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="ba445-151">Väli</span><span class="sxs-lookup"><span data-stu-id="ba445-151">Interval</span></span>    | <span data-ttu-id="ba445-152">Poiston määrä</span><span class="sxs-lookup"><span data-stu-id="ba445-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="ba445-153">30. kesäkuuta</span><span class="sxs-lookup"><span data-stu-id="ba445-153">June 30</span></span>     | <span data-ttu-id="ba445-154">(11 000 – 1 000) × 10 % = 1 000</span><span class="sxs-lookup"><span data-stu-id="ba445-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="ba445-155">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="ba445-155">December 31</span></span> | <span data-ttu-id="ba445-156">(11 000 – 1 000) × 50 % = 5 000</span><span class="sxs-lookup"><span data-stu-id="ba445-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="ba445-157">Aikavälien prosenttien yhteissumman ei tarvitse olla 100.</span><span class="sxs-lookup"><span data-stu-id="ba445-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="ba445-158">Näyttöön avautuu kuitenkin sanoma, jos **Käyttöomaisuuserän poistoprofiilisuunnitelma** -sivun **Kumulatiivinen prosentti** -kentän arvo ei ole **100**.</span><span class="sxs-lookup"><span data-stu-id="ba445-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>



