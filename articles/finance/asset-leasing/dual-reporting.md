---
title: Kaksoisraportointi
description: Tämä ohjeaihe sisältää esimerkin sekä International Financial Reporting Standard (IFRS) -raportoinnin että resurssin vuokrauksen lakisääteisen raportoinnin vaatimusten täyttämisestä.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d6daa43178625316a40427728e7e4186691cc13c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229547"
---
# <a name="dual-reporting"></a><span data-ttu-id="59d0f-103">Kaksoisraportointi</span><span class="sxs-lookup"><span data-stu-id="59d0f-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59d0f-104">Tämä ohjeaihe sisältää esimerkin sekä International Financial Reporting Standard (IFRS) -raportoinnin että resurssin vuokrauksen lakisääteisen raportoinnin vaatimusten täyttämisestä.</span><span class="sxs-lookup"><span data-stu-id="59d0f-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="59d0f-105">Vaatimuksena on Microsoft Dynamics 365 Financen kirjanpitotasojen käyttökokemus. Sen avulla esimerkki on helpompi ymmärtää.</span><span class="sxs-lookup"><span data-stu-id="59d0f-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="59d0f-106">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="59d0f-106">Example</span></span>

<span data-ttu-id="59d0f-107">Seuraavassa esimerkissä otetaan huomioon vuokraus Italian lakisääteisessä raportoinnissa käyttämällä sekä käteisvaroihin perustuvaa menetelmää että IFRS-raportointimenetelmiä.</span><span class="sxs-lookup"><span data-stu-id="59d0f-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="59d0f-108">Yrityksen on muodostettava kolme kirjaa, joiden avulla sekä Italian lakisääteiset vaatimukset että IFRS 16 -vaatimukset otetaan huomioon.</span><span class="sxs-lookup"><span data-stu-id="59d0f-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="59d0f-109">Yksi kirja vaaditaan IFRS 16:lle, toinen lakisääteisille vaatimuksille ja kolmas lakisääteisten kirjausten automaattista käänteistä kirjausta varten.</span><span class="sxs-lookup"><span data-stu-id="59d0f-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="59d0f-110">Kirjat määritetään seuraavissa taulukoissa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="59d0f-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="59d0f-111">**IFRS 16 -kirja**</span><span class="sxs-lookup"><span data-stu-id="59d0f-111">**IFRS 16 book**</span></span>

<span data-ttu-id="59d0f-112">IFRS 16 -kirja määritetään niin, että se on yhdenmukainen IFRS 16 -kirjanpitostandardin kanssa.</span><span class="sxs-lookup"><span data-stu-id="59d0f-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="59d0f-113">Kaikki tähän kirjaan kirjatut tapahtumat kirjataan mukautettuun tasoon.</span><span class="sxs-lookup"><span data-stu-id="59d0f-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="59d0f-114">Nimi</span><span class="sxs-lookup"><span data-stu-id="59d0f-114">Name</span></span>                                    | <span data-ttu-id="59d0f-115">kuvaus</span><span class="sxs-lookup"><span data-stu-id="59d0f-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="59d0f-116">Kirjan tyyppi</span><span class="sxs-lookup"><span data-stu-id="59d0f-116">Book type</span></span>                               | <span data-ttu-id="59d0f-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="59d0f-117">IFRS 16</span></span>        |
| <span data-ttu-id="59d0f-118">Kirjan kuvaus</span><span class="sxs-lookup"><span data-stu-id="59d0f-118">Book description</span></span>                        | <span data-ttu-id="59d0f-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="59d0f-119">IFRS 16</span></span>        |
| <span data-ttu-id="59d0f-120">Kirjanpitotaso</span><span class="sxs-lookup"><span data-stu-id="59d0f-120">Posting Layer</span></span>                           | <span data-ttu-id="59d0f-121">Mukautettu kerros 1</span><span class="sxs-lookup"><span data-stu-id="59d0f-121">Custom layer 1</span></span> |
| <span data-ttu-id="59d0f-122">Vuokran tyyppi</span><span class="sxs-lookup"><span data-stu-id="59d0f-122">Lease Type</span></span>                              | <span data-ttu-id="59d0f-123">Finance</span><span class="sxs-lookup"><span data-stu-id="59d0f-123">Finance</span></span>        |
| <span data-ttu-id="59d0f-124">Kirjanpitokehys</span><span class="sxs-lookup"><span data-stu-id="59d0f-124">Accounting Framework</span></span>                    | <span data-ttu-id="59d0f-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="59d0f-125">IFRS 16</span></span>        |
| <span data-ttu-id="59d0f-126">Vuokra-/käyttöajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="59d0f-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="59d0f-127">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-127">0.00</span></span>           |
| <span data-ttu-id="59d0f-128">Nykyinen arvo / resurssin käyvän arvon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="59d0f-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="59d0f-129">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-129">0.00</span></span>           |
| <span data-ttu-id="59d0f-130">Lyhytaikainen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="59d0f-130">Short-term threshold</span></span>                    | <span data-ttu-id="59d0f-131">12</span><span class="sxs-lookup"><span data-stu-id="59d0f-131">12</span></span>             |
| <span data-ttu-id="59d0f-132">Arvoltaan vähäinen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="59d0f-132">Low Value Threshold</span></span>                     | <span data-ttu-id="59d0f-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-133">5,000.00</span></span>       |
| <span data-ttu-id="59d0f-134">Maksu toimittajalle</span><span class="sxs-lookup"><span data-stu-id="59d0f-134">Pay to Vendor</span></span>                           | <span data-ttu-id="59d0f-135">Nro</span><span class="sxs-lookup"><span data-stu-id="59d0f-135">No</span></span>             |

<span data-ttu-id="59d0f-136">**Lakisääteinen kirja**</span><span class="sxs-lookup"><span data-stu-id="59d0f-136">**Statutory book**</span></span>

<span data-ttu-id="59d0f-137">Lakisääteinen kirja on käteisvaroihin perustuva kirja, jonne yritys kirjaa vuokrauksen kulut käteisvarojen summana, joka maksetaan joka kuukausi vuokrana.</span><span class="sxs-lookup"><span data-stu-id="59d0f-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="59d0f-138">Tämä kirja ei tuota käyttöoikeusomaisuuserää tai vuokrasopimusvelkaa.</span><span class="sxs-lookup"><span data-stu-id="59d0f-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="59d0f-139">Nimi</span><span class="sxs-lookup"><span data-stu-id="59d0f-139">Name</span></span>                                    | <span data-ttu-id="59d0f-140">kuvaus</span><span class="sxs-lookup"><span data-stu-id="59d0f-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="59d0f-141">Kirjan tyyppi</span><span class="sxs-lookup"><span data-stu-id="59d0f-141">Book type</span></span>                               | <span data-ttu-id="59d0f-142">Lakisääteinen</span><span class="sxs-lookup"><span data-stu-id="59d0f-142">Statutory</span></span>   |
| <span data-ttu-id="59d0f-143">Kirjan kuvaus</span><span class="sxs-lookup"><span data-stu-id="59d0f-143">Book description</span></span>                        | <span data-ttu-id="59d0f-144">Paikallinen GAAP</span><span class="sxs-lookup"><span data-stu-id="59d0f-144">Local GAAP</span></span>  |
| <span data-ttu-id="59d0f-145">Kirjanpitotaso</span><span class="sxs-lookup"><span data-stu-id="59d0f-145">Posting Layer</span></span>                           | <span data-ttu-id="59d0f-146">Valittu</span><span class="sxs-lookup"><span data-stu-id="59d0f-146">Current</span></span>     |
| <span data-ttu-id="59d0f-147">Vuokran tyyppi</span><span class="sxs-lookup"><span data-stu-id="59d0f-147">Lease Type</span></span>                              | <span data-ttu-id="59d0f-148">Automaattinen</span><span class="sxs-lookup"><span data-stu-id="59d0f-148">Automatic</span></span>   |
| <span data-ttu-id="59d0f-149">Kirjanpitokehys</span><span class="sxs-lookup"><span data-stu-id="59d0f-149">Accounting Framework</span></span>                    | <span data-ttu-id="59d0f-150">Maksuperuste</span><span class="sxs-lookup"><span data-stu-id="59d0f-150">Cash basis</span></span>  |
| <span data-ttu-id="59d0f-151">Vuokra-/käyttöajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="59d0f-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="59d0f-152">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-152">0.00</span></span>        |
| <span data-ttu-id="59d0f-153">Nykyinen arvo / resurssin käyvän arvon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="59d0f-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="59d0f-154">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-154">0.00</span></span>        |
| <span data-ttu-id="59d0f-155">Lyhytaikainen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="59d0f-155">Short-term threshold</span></span>                    | <span data-ttu-id="59d0f-156">0</span><span class="sxs-lookup"><span data-stu-id="59d0f-156">0</span></span>           |
| <span data-ttu-id="59d0f-157">Arvoltaan vähäinen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="59d0f-157">Low Value Threshold</span></span>                     | <span data-ttu-id="59d0f-158">0</span><span class="sxs-lookup"><span data-stu-id="59d0f-158">0</span></span>           |
| <span data-ttu-id="59d0f-159">Maksu toimittajalle</span><span class="sxs-lookup"><span data-stu-id="59d0f-159">Pay to Vendor</span></span>                           | <span data-ttu-id="59d0f-160">Nro</span><span class="sxs-lookup"><span data-stu-id="59d0f-160">No</span></span>          |

<span data-ttu-id="59d0f-161">**Lakisääteinen palautuskirja**</span><span class="sxs-lookup"><span data-stu-id="59d0f-161">**Statutory reversal book**</span></span>

<span data-ttu-id="59d0f-162">Lakisääteinen palautuskirja määritetään samalla tavalla kuin lakisääteinen kirja.</span><span class="sxs-lookup"><span data-stu-id="59d0f-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="59d0f-163">Nimi</span><span class="sxs-lookup"><span data-stu-id="59d0f-163">Name</span></span>                                    | <span data-ttu-id="59d0f-164">kuvaus</span><span class="sxs-lookup"><span data-stu-id="59d0f-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="59d0f-165">Kirjan tyyppi</span><span class="sxs-lookup"><span data-stu-id="59d0f-165">Book type</span></span>                               | <span data-ttu-id="59d0f-166">Lakisääteinen – palautus</span><span class="sxs-lookup"><span data-stu-id="59d0f-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="59d0f-167">Kirjan kuvaus</span><span class="sxs-lookup"><span data-stu-id="59d0f-167">Book description</span></span>                        | <span data-ttu-id="59d0f-168">Kirjaa käänteiseen lakisääteiseen kirjaan</span><span class="sxs-lookup"><span data-stu-id="59d0f-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="59d0f-169">Kirjanpitotaso</span><span class="sxs-lookup"><span data-stu-id="59d0f-169">Posting Layer</span></span>                           | <span data-ttu-id="59d0f-170">Mukautettu kerros 1</span><span class="sxs-lookup"><span data-stu-id="59d0f-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="59d0f-171">Vuokran tyyppi</span><span class="sxs-lookup"><span data-stu-id="59d0f-171">Lease Type</span></span>                              | <span data-ttu-id="59d0f-172">Automaattinen</span><span class="sxs-lookup"><span data-stu-id="59d0f-172">Automatic</span></span>                      |
| <span data-ttu-id="59d0f-173">Kirjanpitokehys</span><span class="sxs-lookup"><span data-stu-id="59d0f-173">Accounting Framework</span></span>                    | <span data-ttu-id="59d0f-174">Maksuperuste</span><span class="sxs-lookup"><span data-stu-id="59d0f-174">Cash basis</span></span>                     |
| <span data-ttu-id="59d0f-175">Vuokra-/käyttöajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="59d0f-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="59d0f-176">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-176">0.00</span></span>                           |
| <span data-ttu-id="59d0f-177">Nykyinen arvo / resurssin käyvän arvon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="59d0f-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="59d0f-178">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-178">0.00</span></span>                           |
| <span data-ttu-id="59d0f-179">Lyhytaikainen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="59d0f-179">Short-term threshold</span></span>                    | <span data-ttu-id="59d0f-180">0</span><span class="sxs-lookup"><span data-stu-id="59d0f-180">0</span></span>                              |
| <span data-ttu-id="59d0f-181">Arvoltaan vähäinen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="59d0f-181">Low Value Threshold</span></span>                     | <span data-ttu-id="59d0f-182">0</span><span class="sxs-lookup"><span data-stu-id="59d0f-182">0</span></span>                              |
| <span data-ttu-id="59d0f-183">Maksu toimittajalle</span><span class="sxs-lookup"><span data-stu-id="59d0f-183">Pay to Vendor</span></span>                           | <span data-ttu-id="59d0f-184">Nro</span><span class="sxs-lookup"><span data-stu-id="59d0f-184">No</span></span>                             |

<span data-ttu-id="59d0f-185">Tässä esimerkissä on luotu vuokraus, jolla on seuraavat asetukset **Yleistä**- ja **Maksuaikataulurivit**-välilehdissä.</span><span class="sxs-lookup"><span data-stu-id="59d0f-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="59d0f-186">**Yleinen-välilehti**</span><span class="sxs-lookup"><span data-stu-id="59d0f-186">**General tab**</span></span>

| <span data-ttu-id="59d0f-187">Kenttä</span><span class="sxs-lookup"><span data-stu-id="59d0f-187">Field</span></span>                      | <span data-ttu-id="59d0f-188">Arvo</span><span class="sxs-lookup"><span data-stu-id="59d0f-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="59d0f-189">Inkrementaalinen lainakorko</span><span class="sxs-lookup"><span data-stu-id="59d0f-189">Incremental borrowing rate</span></span> | <span data-ttu-id="59d0f-190">5 %</span><span class="sxs-lookup"><span data-stu-id="59d0f-190">5%</span></span>               |
| <span data-ttu-id="59d0f-191">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="59d0f-191">Commencement date</span></span>          | <span data-ttu-id="59d0f-192">1.1.2020</span><span class="sxs-lookup"><span data-stu-id="59d0f-192">1/1/2020</span></span>         |
| <span data-ttu-id="59d0f-193">Vuokraryhmä</span><span class="sxs-lookup"><span data-stu-id="59d0f-193">Lease group</span></span>                | <span data-ttu-id="59d0f-194">Rakennukset</span><span class="sxs-lookup"><span data-stu-id="59d0f-194">Buildings</span></span>        |
| <span data-ttu-id="59d0f-195">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="59d0f-195">Vendor</span></span>                     | <span data-ttu-id="59d0f-196">1001</span><span class="sxs-lookup"><span data-stu-id="59d0f-196">1001</span></span>             |
| <span data-ttu-id="59d0f-197">Resurssin käypä arvo</span><span class="sxs-lookup"><span data-stu-id="59d0f-197">Fair value of the asset</span></span>    | <span data-ttu-id="59d0f-198">245,000</span><span class="sxs-lookup"><span data-stu-id="59d0f-198">245,000</span></span>          |
| <span data-ttu-id="59d0f-199">Käyttöomaisuuden käyttöikä</span><span class="sxs-lookup"><span data-stu-id="59d0f-199">Asset useful life</span></span>          | <span data-ttu-id="59d0f-200">120</span><span class="sxs-lookup"><span data-stu-id="59d0f-200">120</span></span>              |
| <span data-ttu-id="59d0f-201">Annuiteetin tyyppi</span><span class="sxs-lookup"><span data-stu-id="59d0f-201">Annuity type</span></span>               | <span data-ttu-id="59d0f-202">Tavallinen annuiteetti</span><span class="sxs-lookup"><span data-stu-id="59d0f-202">Ordinary annuity</span></span> |
| <span data-ttu-id="59d0f-203">Yhdistämisväli</span><span class="sxs-lookup"><span data-stu-id="59d0f-203">Compounding interval</span></span>       | <span data-ttu-id="59d0f-204">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="59d0f-204">Monthly</span></span>          |

<span data-ttu-id="59d0f-205">**Maksusuunnitelmarivit-välilehti**</span><span class="sxs-lookup"><span data-stu-id="59d0f-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="59d0f-206">Kenttä</span><span class="sxs-lookup"><span data-stu-id="59d0f-206">Field</span></span>             | <span data-ttu-id="59d0f-207">Arvo</span><span class="sxs-lookup"><span data-stu-id="59d0f-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="59d0f-208">Aloituspäivä</span><span class="sxs-lookup"><span data-stu-id="59d0f-208">Start date</span></span>        | <span data-ttu-id="59d0f-209">1.1.2020</span><span class="sxs-lookup"><span data-stu-id="59d0f-209">1/1/2020</span></span>   |
| <span data-ttu-id="59d0f-210">Kausiväli</span><span class="sxs-lookup"><span data-stu-id="59d0f-210">Period interval</span></span>   | <span data-ttu-id="59d0f-211">Kuukautta</span><span class="sxs-lookup"><span data-stu-id="59d0f-211">Months</span></span>     |
| <span data-ttu-id="59d0f-212">Kaudet</span><span class="sxs-lookup"><span data-stu-id="59d0f-212">Periods</span></span>           | <span data-ttu-id="59d0f-213">24</span><span class="sxs-lookup"><span data-stu-id="59d0f-213">24</span></span>         |
| <span data-ttu-id="59d0f-214">Päättymispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="59d0f-214">End date</span></span>          | <span data-ttu-id="59d0f-215">31.12.2020</span><span class="sxs-lookup"><span data-stu-id="59d0f-215">12/31/2020</span></span> |
| <span data-ttu-id="59d0f-216">Maksun toistuvuus</span><span class="sxs-lookup"><span data-stu-id="59d0f-216">Payment frequency</span></span> | <span data-ttu-id="59d0f-217">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="59d0f-217">Monthly</span></span>    |
| <span data-ttu-id="59d0f-218">Maksun summa</span><span class="sxs-lookup"><span data-stu-id="59d0f-218">Payment amount</span></span>    | <span data-ttu-id="59d0f-219">1 000</span><span class="sxs-lookup"><span data-stu-id="59d0f-219">1,000</span></span>      |

<span data-ttu-id="59d0f-220">Jotta tämä vuokraus voidaan ottaa huomioon kahdessa kehyksessä, käytetään sekä nykyistä että mukautettua kirjaustasoa.</span><span class="sxs-lookup"><span data-stu-id="59d0f-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="59d0f-221">Seuraavassa taulukossa on esimerkki jokaisesta kirjauskansiomerkinnästä, joka vaaditaan vastaamaan tasapuolisesti kunkin raportointistandardin mukaisia taloustietoja.</span><span class="sxs-lookup"><span data-stu-id="59d0f-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="59d0f-222">Kunkin vuokrauksen ensimmäisen kuukauden kirjauskansiomerkinnän yksityiskohtainen kuvaus annetaan jälkikäteen.</span><span class="sxs-lookup"><span data-stu-id="59d0f-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="59d0f-223">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="59d0f-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="59d0f-224">kuvaus</span><span class="sxs-lookup"><span data-stu-id="59d0f-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="59d0f-225">Lakisääteinen kirja (nykyinen taso)</span><span class="sxs-lookup"><span data-stu-id="59d0f-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="59d0f-226">Nykyinen taso yhteensä</span><span class="sxs-lookup"><span data-stu-id="59d0f-226">Current layer total</span></span></th>
<th><span data-ttu-id="59d0f-227">Palautuskirja (mukautettu taso)</span><span class="sxs-lookup"><span data-stu-id="59d0f-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="59d0f-228">IFRS 16 -kirja (mukautettu taso)</span><span class="sxs-lookup"><span data-stu-id="59d0f-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="59d0f-229">Nykyinen taso + mukautettu taso yhteensä</span><span class="sxs-lookup"><span data-stu-id="59d0f-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="59d0f-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="59d0f-230">JE-100</span></span></th>
<th><span data-ttu-id="59d0f-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="59d0f-231">JE-110</span></span></th>
<th><span data-ttu-id="59d0f-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="59d0f-232">JE-120</span></span></th>
<th><span data-ttu-id="59d0f-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="59d0f-233">JE-130</span></span></th>
<th><span data-ttu-id="59d0f-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="59d0f-234">JE-140</span></span></th>
<th><span data-ttu-id="59d0f-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="59d0f-235">JE-150</span></span></th>
<th><span data-ttu-id="59d0f-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="59d0f-236">JE-160</span></span></th>
<th><span data-ttu-id="59d0f-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="59d0f-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="59d0f-238">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="59d0f-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="59d0f-239">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="59d0f-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="59d0f-240">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="59d0f-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="59d0f-241">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="59d0f-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="59d0f-242">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="59d0f-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="59d0f-243">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="59d0f-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="59d0f-244">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="59d0f-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="59d0f-245">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="59d0f-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="59d0f-246">1</span><span class="sxs-lookup"><span data-stu-id="59d0f-246">1</span></span></td>
<td><span data-ttu-id="59d0f-247">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="59d0f-247">Lease expense</span></span></td>
<td><span data-ttu-id="59d0f-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-249">1,000.00</span></span></td>
<td><span data-ttu-id="59d0f-250">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-251">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59d0f-252">2</span><span class="sxs-lookup"><span data-stu-id="59d0f-252">2</span></span></td>
<td><span data-ttu-id="59d0f-253">Pankkikulu</span><span class="sxs-lookup"><span data-stu-id="59d0f-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="59d0f-254">3.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="59d0f-255">3.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-256">3.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59d0f-257">3</span><span class="sxs-lookup"><span data-stu-id="59d0f-257">3</span></span></td>
<td><span data-ttu-id="59d0f-258">ALV-kulu</span><span class="sxs-lookup"><span data-stu-id="59d0f-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="59d0f-259">5.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="59d0f-260">5.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-261">5.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59d0f-262">4</span><span class="sxs-lookup"><span data-stu-id="59d0f-262">4</span></span></td>
<td><span data-ttu-id="59d0f-263">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="59d0f-263">Clearing account</span></span></td>
<td><span data-ttu-id="59d0f-264">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-264">-1,000.00</span></span></td>
<td><span data-ttu-id="59d0f-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="59d0f-266">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-266">0.00</span></span></td>
<td><span data-ttu-id="59d0f-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="59d0f-268">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-269">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59d0f-270">5</span><span class="sxs-lookup"><span data-stu-id="59d0f-270">5</span></span></td>
<td><span data-ttu-id="59d0f-271">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="59d0f-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="59d0f-272">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-272">-1,008.00</span></span></td>
<td><span data-ttu-id="59d0f-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-273">1,008.00</span></span></td>
<td><span data-ttu-id="59d0f-274">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-275">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59d0f-276">6</span><span class="sxs-lookup"><span data-stu-id="59d0f-276">6</span></span></td>
<td><span data-ttu-id="59d0f-277">Käyttöoikeusomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="59d0f-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-278">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="59d0f-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="59d0f-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59d0f-281">7</span><span class="sxs-lookup"><span data-stu-id="59d0f-281">7</span></span></td>
<td><span data-ttu-id="59d0f-282">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="59d0f-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-283">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="59d0f-284">-22 794,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-284">-22,794.00</span></span></td>
<td><span data-ttu-id="59d0f-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-285">1,000.00</span></span></td>
<td><span data-ttu-id="59d0f-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="59d0f-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="59d0f-287">-21 888,87</span><span class="sxs-lookup"><span data-stu-id="59d0f-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59d0f-288">8</span><span class="sxs-lookup"><span data-stu-id="59d0f-288">8</span></span></td>
<td><span data-ttu-id="59d0f-289">Korkokustannus</span><span class="sxs-lookup"><span data-stu-id="59d0f-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-290">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-291">94.97</span><span class="sxs-lookup"><span data-stu-id="59d0f-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="59d0f-292">94.97</span><span class="sxs-lookup"><span data-stu-id="59d0f-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59d0f-293">9</span><span class="sxs-lookup"><span data-stu-id="59d0f-293">9</span></span></td>
<td><span data-ttu-id="59d0f-294">Maksu</span><span class="sxs-lookup"><span data-stu-id="59d0f-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-295">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-295">-1,008.00</span></span></td>
<td><span data-ttu-id="59d0f-296">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-297">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59d0f-298">10</span><span class="sxs-lookup"><span data-stu-id="59d0f-298">10</span></span></td>
<td><span data-ttu-id="59d0f-299">Poistokulu</span><span class="sxs-lookup"><span data-stu-id="59d0f-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-300">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-301">949.75</span><span class="sxs-lookup"><span data-stu-id="59d0f-301">949.75</span></span></td>
<td><span data-ttu-id="59d0f-302">949.75</span><span class="sxs-lookup"><span data-stu-id="59d0f-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59d0f-303">11</span><span class="sxs-lookup"><span data-stu-id="59d0f-303">11</span></span></td>
<td><span data-ttu-id="59d0f-304">Kertynyt poisto</span><span class="sxs-lookup"><span data-stu-id="59d0f-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-305">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="59d0f-306">-949.75</span></span></td>
<td><span data-ttu-id="59d0f-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="59d0f-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="59d0f-308">Kuten edellä olevasta taulukosta ilmenee, sekä lakisääteinen raportointi että IFRS-raportointi edellyttävät kolmen kirjan käyttämistä.</span><span class="sxs-lookup"><span data-stu-id="59d0f-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="59d0f-309">Lakisääteinen kirja tallentaa vuokrat nykyisen tason käteisvaroihin perustuvan kirjanpidon sääntöjen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="59d0f-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="59d0f-310">Lakisääteinen palautuskirja kumoaa lakisääteiset kirjauskansiomerkinnät.</span><span class="sxs-lookup"><span data-stu-id="59d0f-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="59d0f-311">IFRS 16 -kirja luo IFRS 16:n pakolliset kirjauskansiomerkinnät.</span><span class="sxs-lookup"><span data-stu-id="59d0f-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="59d0f-312">Sinun on syötettävä vuokraus vain kerran.</span><span class="sxs-lookup"><span data-stu-id="59d0f-312">You must enter a lease only one time.</span></span> <span data-ttu-id="59d0f-313">Tämän jälkeen voit avata **Kirjat**-sivun, ja näet kaikki vuokraukseen liittyvät kirjat.</span><span class="sxs-lookup"><span data-stu-id="59d0f-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="59d0f-314">Kun luot kirjoja, kaikkien kolmen on liityttävä samaan vuokraustietueeseen.</span><span class="sxs-lookup"><span data-stu-id="59d0f-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="59d0f-315">Ensimmäinen kirjauskansiomerkintä tallentaa vuokrauksen lakisääteiseen kirjaan.</span><span class="sxs-lookup"><span data-stu-id="59d0f-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="59d0f-316">Voit luoda maksut eränä tai valitsemalla maksusuunnitelman lakisääteisestä kirjasta.</span><span class="sxs-lookup"><span data-stu-id="59d0f-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="59d0f-317">Tässä esimerkissä maksusuunnitelmasta luodaan seuraava kirjauskansiomerkintä lakisääteistä kirjaa varten.</span><span class="sxs-lookup"><span data-stu-id="59d0f-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="59d0f-318">Vuokra – 31.1.2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="59d0f-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="59d0f-319">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="59d0f-319">Account type</span></span> | <span data-ttu-id="59d0f-320">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="59d0f-320">Account number</span></span> | <span data-ttu-id="59d0f-321">Taso</span><span class="sxs-lookup"><span data-stu-id="59d0f-321">Layer</span></span>   | <span data-ttu-id="59d0f-322">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="59d0f-322">Account description</span></span> | <span data-ttu-id="59d0f-323">Veloitus</span><span class="sxs-lookup"><span data-stu-id="59d0f-323">Debit</span></span>    | <span data-ttu-id="59d0f-324">Luotto</span><span class="sxs-lookup"><span data-stu-id="59d0f-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="59d0f-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="59d0f-325">Ledger</span></span>       | <span data-ttu-id="59d0f-326">1</span><span class="sxs-lookup"><span data-stu-id="59d0f-326">1</span></span>              | <span data-ttu-id="59d0f-327">Valittu</span><span class="sxs-lookup"><span data-stu-id="59d0f-327">Current</span></span> | <span data-ttu-id="59d0f-328">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="59d0f-328">Lease expense</span></span>       | <span data-ttu-id="59d0f-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-329">1,000.00</span></span> |          |
| <span data-ttu-id="59d0f-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="59d0f-330">Ledger</span></span>       | <span data-ttu-id="59d0f-331">4</span><span class="sxs-lookup"><span data-stu-id="59d0f-331">4</span></span>              | <span data-ttu-id="59d0f-332">Valittu</span><span class="sxs-lookup"><span data-stu-id="59d0f-332">Current</span></span> | <span data-ttu-id="59d0f-333">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="59d0f-333">Clearing account</span></span>    |          | <span data-ttu-id="59d0f-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-334">1,000.00</span></span> |

<span data-ttu-id="59d0f-335">Ostoreskontran käsittelijä käyttää Dynamics 365:n vakiotoimintoa luodessaan resurssin vuokrauksen ulkopuoliselle vuokraukselle laskun maksamista varten.</span><span class="sxs-lookup"><span data-stu-id="59d0f-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="59d0f-336">Sen sijaan, että debettiliksi valittaisiin **Vuokran kulu** ostoreskontran käsittelijä valitsee selvitystilin seuraavan merkinnän luomiseksi.</span><span class="sxs-lookup"><span data-stu-id="59d0f-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="59d0f-337">Ostoreskontran prosessi – 31.1.2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="59d0f-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="59d0f-338">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="59d0f-338">Account type</span></span> | <span data-ttu-id="59d0f-339">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="59d0f-339">Account number</span></span> | <span data-ttu-id="59d0f-340">Taso</span><span class="sxs-lookup"><span data-stu-id="59d0f-340">Layer</span></span>   | <span data-ttu-id="59d0f-341">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="59d0f-341">Account description</span></span> | <span data-ttu-id="59d0f-342">Veloitus</span><span class="sxs-lookup"><span data-stu-id="59d0f-342">Debit</span></span>    | <span data-ttu-id="59d0f-343">Luotto</span><span class="sxs-lookup"><span data-stu-id="59d0f-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="59d0f-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="59d0f-344">Ledger</span></span>       | <span data-ttu-id="59d0f-345">4</span><span class="sxs-lookup"><span data-stu-id="59d0f-345">4</span></span>              | <span data-ttu-id="59d0f-346">Valittu</span><span class="sxs-lookup"><span data-stu-id="59d0f-346">Current</span></span> | <span data-ttu-id="59d0f-347">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="59d0f-347">Clearing account</span></span>    | <span data-ttu-id="59d0f-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-348">1,000.00</span></span> |          |
| <span data-ttu-id="59d0f-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="59d0f-349">Ledger</span></span>       | <span data-ttu-id="59d0f-350">2</span><span class="sxs-lookup"><span data-stu-id="59d0f-350">2</span></span>              | <span data-ttu-id="59d0f-351">Valittu</span><span class="sxs-lookup"><span data-stu-id="59d0f-351">Current</span></span> | <span data-ttu-id="59d0f-352">Pankkikulu</span><span class="sxs-lookup"><span data-stu-id="59d0f-352">Bank fee</span></span>            | <span data-ttu-id="59d0f-353">3.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-353">3.00</span></span>     |          |
| <span data-ttu-id="59d0f-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="59d0f-354">Ledger</span></span>       | <span data-ttu-id="59d0f-355">3</span><span class="sxs-lookup"><span data-stu-id="59d0f-355">3</span></span>              | <span data-ttu-id="59d0f-356">Valittu</span><span class="sxs-lookup"><span data-stu-id="59d0f-356">Current</span></span> | <span data-ttu-id="59d0f-357">ALV-kulu</span><span class="sxs-lookup"><span data-stu-id="59d0f-357">VAT expense</span></span>         | <span data-ttu-id="59d0f-358">5.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-358">5.00</span></span>     |          |
| <span data-ttu-id="59d0f-359">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="59d0f-359">Vendor</span></span>       | <span data-ttu-id="59d0f-360">5</span><span class="sxs-lookup"><span data-stu-id="59d0f-360">5</span></span>              | <span data-ttu-id="59d0f-361">Valittu</span><span class="sxs-lookup"><span data-stu-id="59d0f-361">Current</span></span> | <span data-ttu-id="59d0f-362">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="59d0f-362">Accounts payable</span></span>    |          | <span data-ttu-id="59d0f-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-363">1,008.00</span></span> |

<span data-ttu-id="59d0f-364">Kun toimittajalle annetaan ilmoitus, seuraat säännöllistä maksuprosessia.</span><span class="sxs-lookup"><span data-stu-id="59d0f-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="59d0f-365">Tämän prosessin aikana luodaan seuraava kirjauskansiomerkintä.</span><span class="sxs-lookup"><span data-stu-id="59d0f-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="59d0f-366">Käteismaksu – 31.1.2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="59d0f-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="59d0f-367">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="59d0f-367">Account type</span></span> | <span data-ttu-id="59d0f-368">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="59d0f-368">Account number</span></span> | <span data-ttu-id="59d0f-369">Taso</span><span class="sxs-lookup"><span data-stu-id="59d0f-369">Layer</span></span>   | <span data-ttu-id="59d0f-370">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="59d0f-370">Account description</span></span> | <span data-ttu-id="59d0f-371">Veloitus</span><span class="sxs-lookup"><span data-stu-id="59d0f-371">Debit</span></span>    | <span data-ttu-id="59d0f-372">Luotto</span><span class="sxs-lookup"><span data-stu-id="59d0f-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="59d0f-373">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="59d0f-373">Vendor</span></span>       | <span data-ttu-id="59d0f-374">5</span><span class="sxs-lookup"><span data-stu-id="59d0f-374">5</span></span>              | <span data-ttu-id="59d0f-375">Valittu</span><span class="sxs-lookup"><span data-stu-id="59d0f-375">Current</span></span> | <span data-ttu-id="59d0f-376">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="59d0f-376">Accounts Payable</span></span>    | <span data-ttu-id="59d0f-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-377">1,008.00</span></span> |          |
| <span data-ttu-id="59d0f-378">Pankki</span><span class="sxs-lookup"><span data-stu-id="59d0f-378">Bank</span></span>         | <span data-ttu-id="59d0f-379">9</span><span class="sxs-lookup"><span data-stu-id="59d0f-379">9</span></span>              | <span data-ttu-id="59d0f-380">Valittu</span><span class="sxs-lookup"><span data-stu-id="59d0f-380">Current</span></span> | <span data-ttu-id="59d0f-381">Maksu</span><span class="sxs-lookup"><span data-stu-id="59d0f-381">Cash</span></span>                |          | <span data-ttu-id="59d0f-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-382">1,008.00</span></span> |

<span data-ttu-id="59d0f-383">Nyt tämä vuokraus on otettu kokonaan huomioon lakisääteisen raportoinnin vaatimusten mukaisesti, ja voit luoda pääkirjan nykyisen tason mukaan.</span><span class="sxs-lookup"><span data-stu-id="59d0f-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="59d0f-384">Järjestelmä palauttaa pääkirjan, jossa ovat seuraavat luvut.</span><span class="sxs-lookup"><span data-stu-id="59d0f-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="59d0f-385">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="59d0f-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="59d0f-386">kuvaus</span><span class="sxs-lookup"><span data-stu-id="59d0f-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="59d0f-387">Lakisääteinen kirja (nykyinen taso)</span><span class="sxs-lookup"><span data-stu-id="59d0f-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="59d0f-388">Nykyinen taso yhteensä</span><span class="sxs-lookup"><span data-stu-id="59d0f-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="59d0f-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="59d0f-389">JE-100</span></span></th>
<th><span data-ttu-id="59d0f-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="59d0f-390">JE-110</span></span></th>
<th><span data-ttu-id="59d0f-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="59d0f-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="59d0f-392">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="59d0f-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="59d0f-393">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="59d0f-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="59d0f-394">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="59d0f-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="59d0f-395">1</span><span class="sxs-lookup"><span data-stu-id="59d0f-395">1</span></span></td>
<td><span data-ttu-id="59d0f-396">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="59d0f-396">Lease expense</span></span></td>
<td><span data-ttu-id="59d0f-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59d0f-399">2</span><span class="sxs-lookup"><span data-stu-id="59d0f-399">2</span></span></td>
<td><span data-ttu-id="59d0f-400">Pankkikulu</span><span class="sxs-lookup"><span data-stu-id="59d0f-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="59d0f-401">3.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="59d0f-402">3.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59d0f-403">3</span><span class="sxs-lookup"><span data-stu-id="59d0f-403">3</span></span></td>
<td><span data-ttu-id="59d0f-404">ALV-kulu</span><span class="sxs-lookup"><span data-stu-id="59d0f-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="59d0f-405">5.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="59d0f-406">5.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59d0f-407">4</span><span class="sxs-lookup"><span data-stu-id="59d0f-407">4</span></span></td>
<td><span data-ttu-id="59d0f-408">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="59d0f-408">Clearing account</span></span></td>
<td><span data-ttu-id="59d0f-409">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-409">-1,000.00</span></span></td>
<td><span data-ttu-id="59d0f-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="59d0f-411">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59d0f-412">5</span><span class="sxs-lookup"><span data-stu-id="59d0f-412">5</span></span></td>
<td><span data-ttu-id="59d0f-413">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="59d0f-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="59d0f-414">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-414">-1,008.00</span></span></td>
<td><span data-ttu-id="59d0f-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-415">1,008.00</span></span></td>
<td><span data-ttu-id="59d0f-416">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59d0f-417">6</span><span class="sxs-lookup"><span data-stu-id="59d0f-417">6</span></span></td>
<td><span data-ttu-id="59d0f-418">Käyttöoikeusomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="59d0f-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-419">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59d0f-420">7</span><span class="sxs-lookup"><span data-stu-id="59d0f-420">7</span></span></td>
<td><span data-ttu-id="59d0f-421">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="59d0f-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-422">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59d0f-423">8</span><span class="sxs-lookup"><span data-stu-id="59d0f-423">8</span></span></td>
<td><span data-ttu-id="59d0f-424">Korkokustannus</span><span class="sxs-lookup"><span data-stu-id="59d0f-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-425">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59d0f-426">9</span><span class="sxs-lookup"><span data-stu-id="59d0f-426">9</span></span></td>
<td><span data-ttu-id="59d0f-427">Maksu</span><span class="sxs-lookup"><span data-stu-id="59d0f-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-428">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-428">-1,008.00</span></span></td>
<td><span data-ttu-id="59d0f-429">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59d0f-430">10</span><span class="sxs-lookup"><span data-stu-id="59d0f-430">10</span></span></td>
<td><span data-ttu-id="59d0f-431">Poistokulu</span><span class="sxs-lookup"><span data-stu-id="59d0f-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-432">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59d0f-433">11</span><span class="sxs-lookup"><span data-stu-id="59d0f-433">11</span></span></td>
<td><span data-ttu-id="59d0f-434">Kertynyt poisto</span><span class="sxs-lookup"><span data-stu-id="59d0f-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="59d0f-435">0,00</span><span class="sxs-lookup"><span data-stu-id="59d0f-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="59d0f-436">Jos haluat käyttää IFRS 16 -lukuja ja suorittaa saman pääkirjan, lakisääteisen kirjapidon kirjauskansioviennit on palautettava ja IFRS 16 -kirjauskansioviennit kirjattava.</span><span class="sxs-lookup"><span data-stu-id="59d0f-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="59d0f-437">Tässä esimerkissä on myös lakisääteinen palautuskirja siltä varalta, että haluat palauttaa lakisääteiset kirjauskansioviennit. Palautuskirjassa on samat asetukset kuin lakisääteisessä kirjassa, mutta vastakkainen kirjausprofiili.</span><span class="sxs-lookup"><span data-stu-id="59d0f-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="59d0f-438">Esimerkiksi lakisääteinen kirja *veloitti* vuokrauksen kulutilin, mutta palautuskirja *hyvittää* tämän tilin.</span><span class="sxs-lookup"><span data-stu-id="59d0f-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="59d0f-439">Nämä suhteet on helppo määrittää resurssin vuokrauksen kirjaustileillä **Resurssin vuokrauksen parametrit** -sivulla (**Resurssin vuokraus \> Asetukset \> Resurssin vuokrauksen parametrit**).</span><span class="sxs-lookup"><span data-stu-id="59d0f-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="59d0f-440">Kun lakisääteisessä kirjassa käytettyä prosessia käytetään palautuskirjassa, luodaan seuraava kirjauskansiovienti.</span><span class="sxs-lookup"><span data-stu-id="59d0f-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="59d0f-441">Erona on se, että palautuskirja kirjaa vastakirjaukset lakisääteisestä kirjasta.</span><span class="sxs-lookup"><span data-stu-id="59d0f-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="59d0f-442">Vastakirjaukset tehdään myös mukautetussa tasossa.</span><span class="sxs-lookup"><span data-stu-id="59d0f-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="59d0f-443">Kun pääkirja suoritetaan nykyisellä tasolla, palautuskirjauskansiovientejä ei sisällytetä.</span><span class="sxs-lookup"><span data-stu-id="59d0f-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="59d0f-444">Vuokra – 31.1.2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="59d0f-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="59d0f-445">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="59d0f-445">Account type</span></span> | <span data-ttu-id="59d0f-446">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="59d0f-446">Account number</span></span> | <span data-ttu-id="59d0f-447">Taso</span><span class="sxs-lookup"><span data-stu-id="59d0f-447">Layer</span></span>  | <span data-ttu-id="59d0f-448">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="59d0f-448">Account description</span></span> | <span data-ttu-id="59d0f-449">Veloitus</span><span class="sxs-lookup"><span data-stu-id="59d0f-449">Debit</span></span>    | <span data-ttu-id="59d0f-450">Luotto</span><span class="sxs-lookup"><span data-stu-id="59d0f-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="59d0f-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="59d0f-451">Ledger</span></span>       | <span data-ttu-id="59d0f-452">4</span><span class="sxs-lookup"><span data-stu-id="59d0f-452">4</span></span>              | <span data-ttu-id="59d0f-453">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="59d0f-453">Custom</span></span> | <span data-ttu-id="59d0f-454">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="59d0f-454">Clearing account</span></span>    | <span data-ttu-id="59d0f-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-455">1,000.00</span></span> |          |
| <span data-ttu-id="59d0f-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="59d0f-456">Ledger</span></span>       | <span data-ttu-id="59d0f-457">1</span><span class="sxs-lookup"><span data-stu-id="59d0f-457">1</span></span>              | <span data-ttu-id="59d0f-458">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="59d0f-458">Custom</span></span> | <span data-ttu-id="59d0f-459">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="59d0f-459">Lease expense</span></span>       |          | <span data-ttu-id="59d0f-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-460">1,000.00</span></span> |

<span data-ttu-id="59d0f-461">Nyt lakisääteiset kirjauskansioviennit on eliminoitu, ja voit kirjata kaikki IFRS 16:n edellyttämät kirjauskansioviennit IFRS 16 -kirjaan.</span><span class="sxs-lookup"><span data-stu-id="59d0f-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="59d0f-462">Nämä viennit sisältävät käyttöoikeusomaisuuserän ja velan alkuperäisen kirjauksen sekä koron ja poiston tietueen.</span><span class="sxs-lookup"><span data-stu-id="59d0f-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="59d0f-463">Alkuperäinen kirjaus – 1.1.2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="59d0f-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="59d0f-464">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="59d0f-464">Account type</span></span> | <span data-ttu-id="59d0f-465">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="59d0f-465">Account number</span></span> | <span data-ttu-id="59d0f-466">Taso</span><span class="sxs-lookup"><span data-stu-id="59d0f-466">Layer</span></span>  | <span data-ttu-id="59d0f-467">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="59d0f-467">Account description</span></span>      | <span data-ttu-id="59d0f-468">Veloitus</span><span class="sxs-lookup"><span data-stu-id="59d0f-468">Debit</span></span>     | <span data-ttu-id="59d0f-469">Luotto</span><span class="sxs-lookup"><span data-stu-id="59d0f-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="59d0f-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="59d0f-470">Ledger</span></span>       | <span data-ttu-id="59d0f-471">6</span><span class="sxs-lookup"><span data-stu-id="59d0f-471">6</span></span>              | <span data-ttu-id="59d0f-472">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="59d0f-472">Custom</span></span> | <span data-ttu-id="59d0f-473">Käyttöoikeusomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="59d0f-473">ROU Asset</span></span>                | <span data-ttu-id="59d0f-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="59d0f-474">22,793.90</span></span> |           |
| <span data-ttu-id="59d0f-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="59d0f-475">Ledger</span></span>       | <span data-ttu-id="59d0f-476">7</span><span class="sxs-lookup"><span data-stu-id="59d0f-476">7</span></span>              | <span data-ttu-id="59d0f-477">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="59d0f-477">Custom</span></span> | <span data-ttu-id="59d0f-478">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="59d0f-478">Finance lease obligation</span></span> |           | <span data-ttu-id="59d0f-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="59d0f-479">22,793.90</span></span> |

<span data-ttu-id="59d0f-480">Vuokra kirjataan kuten muut vuokrat.</span><span class="sxs-lookup"><span data-stu-id="59d0f-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="59d0f-481">Selvitystiliä käytetään, jotta voidaan varmistaa käteisen hyvitys vain kerran.</span><span class="sxs-lookup"><span data-stu-id="59d0f-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="59d0f-482">Vuokra – 31.1.2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="59d0f-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="59d0f-483">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="59d0f-483">Account type</span></span> | <span data-ttu-id="59d0f-484">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="59d0f-484">Account number</span></span> | <span data-ttu-id="59d0f-485">Taso</span><span class="sxs-lookup"><span data-stu-id="59d0f-485">Layer</span></span>  | <span data-ttu-id="59d0f-486">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="59d0f-486">Account description</span></span>      | <span data-ttu-id="59d0f-487">Veloitus</span><span class="sxs-lookup"><span data-stu-id="59d0f-487">Debit</span></span>    | <span data-ttu-id="59d0f-488">Luotto</span><span class="sxs-lookup"><span data-stu-id="59d0f-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="59d0f-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="59d0f-489">Ledger</span></span>       | <span data-ttu-id="59d0f-490">7</span><span class="sxs-lookup"><span data-stu-id="59d0f-490">7</span></span>              | <span data-ttu-id="59d0f-491">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="59d0f-491">Custom</span></span> | <span data-ttu-id="59d0f-492">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="59d0f-492">Finance lease obligation</span></span> | <span data-ttu-id="59d0f-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-493">1,000.00</span></span> |          |
| <span data-ttu-id="59d0f-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="59d0f-494">Ledger</span></span>       | <span data-ttu-id="59d0f-495">4</span><span class="sxs-lookup"><span data-stu-id="59d0f-495">4</span></span>              | <span data-ttu-id="59d0f-496">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="59d0f-496">Custom</span></span> | <span data-ttu-id="59d0f-497">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="59d0f-497">Clearing account</span></span>         |          | <span data-ttu-id="59d0f-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-498">1,000.00</span></span> |

<span data-ttu-id="59d0f-499">Korkokulun kirjauskansiovienti luodaan velan kuoletusaikataulusta.</span><span class="sxs-lookup"><span data-stu-id="59d0f-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="59d0f-500">Korkokustannus – 31.1.2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="59d0f-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="59d0f-501">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="59d0f-501">Account type</span></span> | <span data-ttu-id="59d0f-502">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="59d0f-502">Account number</span></span> | <span data-ttu-id="59d0f-503">Taso</span><span class="sxs-lookup"><span data-stu-id="59d0f-503">Layer</span></span>  | <span data-ttu-id="59d0f-504">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="59d0f-504">Account description</span></span>      | <span data-ttu-id="59d0f-505">Veloitus</span><span class="sxs-lookup"><span data-stu-id="59d0f-505">Debit</span></span> | <span data-ttu-id="59d0f-506">Luotto</span><span class="sxs-lookup"><span data-stu-id="59d0f-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="59d0f-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="59d0f-507">Ledger</span></span>       | <span data-ttu-id="59d0f-508">8</span><span class="sxs-lookup"><span data-stu-id="59d0f-508">8</span></span>              | <span data-ttu-id="59d0f-509">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="59d0f-509">Custom</span></span> | <span data-ttu-id="59d0f-510">Korkokustannus</span><span class="sxs-lookup"><span data-stu-id="59d0f-510">Interest expense</span></span>         | <span data-ttu-id="59d0f-511">94.97</span><span class="sxs-lookup"><span data-stu-id="59d0f-511">94.97</span></span> |        |
| <span data-ttu-id="59d0f-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="59d0f-512">Ledger</span></span>       | <span data-ttu-id="59d0f-513">7</span><span class="sxs-lookup"><span data-stu-id="59d0f-513">7</span></span>              | <span data-ttu-id="59d0f-514">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="59d0f-514">Custom</span></span> | <span data-ttu-id="59d0f-515">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="59d0f-515">Finance lease obligation</span></span> |       | <span data-ttu-id="59d0f-516">94.97</span><span class="sxs-lookup"><span data-stu-id="59d0f-516">94.97</span></span>  |

<span data-ttu-id="59d0f-517">Poistokulun kirjauskansiovienti luodaan resurssin poistoaikataulusta.</span><span class="sxs-lookup"><span data-stu-id="59d0f-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="59d0f-518">Poistokulu – 31.1.2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="59d0f-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="59d0f-519">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="59d0f-519">Account type</span></span> | <span data-ttu-id="59d0f-520">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="59d0f-520">Account number</span></span> | <span data-ttu-id="59d0f-521">Taso</span><span class="sxs-lookup"><span data-stu-id="59d0f-521">Layer</span></span>  | <span data-ttu-id="59d0f-522">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="59d0f-522">Account description</span></span>      | <span data-ttu-id="59d0f-523">Veloitus</span><span class="sxs-lookup"><span data-stu-id="59d0f-523">Debit</span></span>  | <span data-ttu-id="59d0f-524">Luotto</span><span class="sxs-lookup"><span data-stu-id="59d0f-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="59d0f-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="59d0f-525">Ledger</span></span>       | <span data-ttu-id="59d0f-526">10</span><span class="sxs-lookup"><span data-stu-id="59d0f-526">10</span></span>             | <span data-ttu-id="59d0f-527">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="59d0f-527">Custom</span></span> | <span data-ttu-id="59d0f-528">Poistokulu</span><span class="sxs-lookup"><span data-stu-id="59d0f-528">Depreciation expense</span></span>     | <span data-ttu-id="59d0f-529">949.75</span><span class="sxs-lookup"><span data-stu-id="59d0f-529">949.75</span></span> |        |
| <span data-ttu-id="59d0f-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="59d0f-530">Ledger</span></span>       | <span data-ttu-id="59d0f-531">11</span><span class="sxs-lookup"><span data-stu-id="59d0f-531">11</span></span>             | <span data-ttu-id="59d0f-532">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="59d0f-532">Custom</span></span> | <span data-ttu-id="59d0f-533">Kertynyt poisto</span><span class="sxs-lookup"><span data-stu-id="59d0f-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="59d0f-534">949.75</span><span class="sxs-lookup"><span data-stu-id="59d0f-534">949.75</span></span> |

<span data-ttu-id="59d0f-535">Kun kaikki nämä kirjauskansioviennit on luotu ja kirjattu, näkyvissä ovat seuraavat mukautetun tason 1 arvot.</span><span class="sxs-lookup"><span data-stu-id="59d0f-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="59d0f-536">Huomaa, että viimeinen sarake sisältää pankkikulun, ALV-kulun ja käteisvähennyksen edelliseltä tasolta, mutta ei lakisääteisen raportoinnin kirjauskansiovientejä.</span><span class="sxs-lookup"><span data-stu-id="59d0f-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="59d0f-537">Näin saavutetaan todelliset kaksoisraportoinnin ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="59d0f-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="59d0f-538">Tässä vaiheessa yritys on juuri suorittanut pääkirjan ja yhdistää nykyisen tason mukautettuun tasoon IFRS-pääkirjan luomista varten.</span><span class="sxs-lookup"><span data-stu-id="59d0f-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="59d0f-539">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="59d0f-539">Account No</span></span> | <span data-ttu-id="59d0f-540">kuvaus</span><span class="sxs-lookup"><span data-stu-id="59d0f-540">Description</span></span>              | <span data-ttu-id="59d0f-541">Lakisääteinen kirja\-Nykyinen taso\-JE\-100\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="59d0f-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="59d0f-542">Lakisääteinen kirja\-Nykyinen taso\-JE\-110\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="59d0f-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="59d0f-543">Lakisääteinen kirja\-Nykyinen taso\-JE\-120\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="59d0f-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="59d0f-544">Nykyinen taso \- Kokonaissummat</span><span class="sxs-lookup"><span data-stu-id="59d0f-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="59d0f-545">Palautuskirja\-Mukautettu taso\-JE\-130\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="59d0f-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="59d0f-546">IFRS 16 -kirja\-Mukautettu taso\-JE\-140\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="59d0f-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="59d0f-547">IFRS 16 -kirja\-Mukautettu taso\-JE\-150\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="59d0f-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="59d0f-548">IFRS 16 -kirja\-Mukautettu taso\-JE\-160\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="59d0f-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="59d0f-549">IFRS 16 -kirja\-Mukautettu taso\-JE\-170\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="59d0f-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="59d0f-550">Mukautettu taso \+ Nykyinen taso \- Kokonaissummat</span><span class="sxs-lookup"><span data-stu-id="59d0f-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="59d0f-551">1</span><span class="sxs-lookup"><span data-stu-id="59d0f-551">1</span></span>          | <span data-ttu-id="59d0f-552">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="59d0f-552">Lease expense</span></span>            | <span data-ttu-id="59d0f-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="59d0f-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-554">1,000\.00</span></span>               |   | <span data-ttu-id="59d0f-555">\-1 000</span><span class="sxs-lookup"><span data-stu-id="59d0f-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="59d0f-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-556">0\.00</span></span>                                   |
| <span data-ttu-id="59d0f-557">2</span><span class="sxs-lookup"><span data-stu-id="59d0f-557">2</span></span>          | <span data-ttu-id="59d0f-558">Pankkikulu</span><span class="sxs-lookup"><span data-stu-id="59d0f-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="59d0f-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="59d0f-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="59d0f-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-561">3\.00</span></span>                                   |
| <span data-ttu-id="59d0f-562">3</span><span class="sxs-lookup"><span data-stu-id="59d0f-562">3</span></span>          | <span data-ttu-id="59d0f-563">ALV-kulu</span><span class="sxs-lookup"><span data-stu-id="59d0f-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="59d0f-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="59d0f-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="59d0f-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-566">5\.00</span></span>                                   |
| <span data-ttu-id="59d0f-567">4</span><span class="sxs-lookup"><span data-stu-id="59d0f-567">4</span></span>          | <span data-ttu-id="59d0f-568">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="59d0f-568">Clearing account</span></span>         | <span data-ttu-id="59d0f-569">\-1 000\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="59d0f-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="59d0f-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-571">0\.00</span></span>                   |   | <span data-ttu-id="59d0f-572">1 000</span><span class="sxs-lookup"><span data-stu-id="59d0f-572">1,000</span></span>                                           |                                                | <span data-ttu-id="59d0f-573">\-1 000</span><span class="sxs-lookup"><span data-stu-id="59d0f-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="59d0f-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-574">0\.00</span></span>                                   |
| <span data-ttu-id="59d0f-575">5</span><span class="sxs-lookup"><span data-stu-id="59d0f-575">5</span></span>          | <span data-ttu-id="59d0f-576">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="59d0f-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="59d0f-577">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="59d0f-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-578">1,008\.00</span></span>                                         | <span data-ttu-id="59d0f-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="59d0f-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-580">0\.00</span></span>                                   |
| <span data-ttu-id="59d0f-581">6</span><span class="sxs-lookup"><span data-stu-id="59d0f-581">6</span></span>          | <span data-ttu-id="59d0f-582">Käyttöoikeusomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="59d0f-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="59d0f-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="59d0f-584">22,794</span><span class="sxs-lookup"><span data-stu-id="59d0f-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="59d0f-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="59d0f-585">22,793\.90</span></span>                              |
| <span data-ttu-id="59d0f-586">7</span><span class="sxs-lookup"><span data-stu-id="59d0f-586">7</span></span>          | <span data-ttu-id="59d0f-587">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="59d0f-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="59d0f-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="59d0f-589">\-22 794</span><span class="sxs-lookup"><span data-stu-id="59d0f-589">\-22,794</span></span>                                       | <span data-ttu-id="59d0f-590">1 000</span><span class="sxs-lookup"><span data-stu-id="59d0f-590">1,000</span></span>                                          | <span data-ttu-id="59d0f-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="59d0f-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="59d0f-592">\-21,888\.87</span><span class="sxs-lookup"><span data-stu-id="59d0f-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="59d0f-593">8</span><span class="sxs-lookup"><span data-stu-id="59d0f-593">8</span></span>          | <span data-ttu-id="59d0f-594">Korkokustannus</span><span class="sxs-lookup"><span data-stu-id="59d0f-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="59d0f-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="59d0f-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="59d0f-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="59d0f-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="59d0f-597">94\.97</span></span>                                  |
| <span data-ttu-id="59d0f-598">9</span><span class="sxs-lookup"><span data-stu-id="59d0f-598">9</span></span>          | <span data-ttu-id="59d0f-599">Maksu</span><span class="sxs-lookup"><span data-stu-id="59d0f-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="59d0f-600">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="59d0f-601">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="59d0f-602">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="59d0f-603">10</span><span class="sxs-lookup"><span data-stu-id="59d0f-603">10</span></span>         | <span data-ttu-id="59d0f-604">Poistokulu</span><span class="sxs-lookup"><span data-stu-id="59d0f-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="59d0f-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="59d0f-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="59d0f-606">949\.75</span></span>                                        | <span data-ttu-id="59d0f-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="59d0f-607">949\.75</span></span>                                 |
| <span data-ttu-id="59d0f-608">11</span><span class="sxs-lookup"><span data-stu-id="59d0f-608">11</span></span>         | <span data-ttu-id="59d0f-609">Kertynyt poisto</span><span class="sxs-lookup"><span data-stu-id="59d0f-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="59d0f-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="59d0f-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="59d0f-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="59d0f-611">\-949\.75</span></span>                                      | <span data-ttu-id="59d0f-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="59d0f-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]