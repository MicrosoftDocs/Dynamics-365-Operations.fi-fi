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
ms.openlocfilehash: a7d9b3ea3d4f1d48b8a7326bd5a01d3119310c62
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003178"
---
# <a name="dual-reporting"></a><span data-ttu-id="764b1-103">Kaksoisraportointi</span><span class="sxs-lookup"><span data-stu-id="764b1-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="764b1-104">Tämä ohjeaihe sisältää esimerkin sekä International Financial Reporting Standard (IFRS) -raportoinnin että resurssin vuokrauksen lakisääteisen raportoinnin vaatimusten täyttämisestä.</span><span class="sxs-lookup"><span data-stu-id="764b1-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="764b1-105">Vaatimuksena on Microsoft Dynamics 365 Financen kirjanpitotasojen käyttökokemus. Sen avulla esimerkki on helpompi ymmärtää.</span><span class="sxs-lookup"><span data-stu-id="764b1-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="764b1-106">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="764b1-106">Example</span></span>

<span data-ttu-id="764b1-107">Seuraavassa esimerkissä otetaan huomioon vuokraus Italian lakisääteisessä raportoinnissa käyttämällä sekä käteisvaroihin perustuvaa menetelmää että IFRS-raportointimenetelmiä.</span><span class="sxs-lookup"><span data-stu-id="764b1-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="764b1-108">Yrityksen on muodostettava kolme kirjaa, joiden avulla sekä Italian lakisääteiset vaatimukset että IFRS 16 -vaatimukset otetaan huomioon.</span><span class="sxs-lookup"><span data-stu-id="764b1-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="764b1-109">Yksi kirja vaaditaan IFRS 16:lle, toinen lakisääteisille vaatimuksille ja kolmas lakisääteisten kirjausten automaattista käänteistä kirjausta varten.</span><span class="sxs-lookup"><span data-stu-id="764b1-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="764b1-110">Kirjat määritetään seuraavissa taulukoissa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="764b1-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="764b1-111">**IFRS 16 -kirja**</span><span class="sxs-lookup"><span data-stu-id="764b1-111">**IFRS 16 book**</span></span>

<span data-ttu-id="764b1-112">IFRS 16 -kirja määritetään niin, että se on yhdenmukainen IFRS 16 -kirjanpitostandardin kanssa.</span><span class="sxs-lookup"><span data-stu-id="764b1-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="764b1-113">Kaikki tähän kirjaan kirjatut tapahtumat kirjataan mukautettuun tasoon.</span><span class="sxs-lookup"><span data-stu-id="764b1-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="764b1-114">Nimi</span><span class="sxs-lookup"><span data-stu-id="764b1-114">Name</span></span>                                    | <span data-ttu-id="764b1-115">kuvaus</span><span class="sxs-lookup"><span data-stu-id="764b1-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="764b1-116">Kirjan tyyppi</span><span class="sxs-lookup"><span data-stu-id="764b1-116">Book type</span></span>                               | <span data-ttu-id="764b1-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="764b1-117">IFRS 16</span></span>        |
| <span data-ttu-id="764b1-118">Kirjan kuvaus</span><span class="sxs-lookup"><span data-stu-id="764b1-118">Book description</span></span>                        | <span data-ttu-id="764b1-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="764b1-119">IFRS 16</span></span>        |
| <span data-ttu-id="764b1-120">Kirjanpitotaso</span><span class="sxs-lookup"><span data-stu-id="764b1-120">Posting Layer</span></span>                           | <span data-ttu-id="764b1-121">Mukautettu kerros 1</span><span class="sxs-lookup"><span data-stu-id="764b1-121">Custom layer 1</span></span> |
| <span data-ttu-id="764b1-122">Vuokran tyyppi</span><span class="sxs-lookup"><span data-stu-id="764b1-122">Lease Type</span></span>                              | <span data-ttu-id="764b1-123">Finance</span><span class="sxs-lookup"><span data-stu-id="764b1-123">Finance</span></span>        |
| <span data-ttu-id="764b1-124">Kirjanpitokehys</span><span class="sxs-lookup"><span data-stu-id="764b1-124">Accounting Framework</span></span>                    | <span data-ttu-id="764b1-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="764b1-125">IFRS 16</span></span>        |
| <span data-ttu-id="764b1-126">Vuokra-/käyttöajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="764b1-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="764b1-127">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-127">0.00</span></span>           |
| <span data-ttu-id="764b1-128">Nykyinen arvo / resurssin käyvän arvon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="764b1-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="764b1-129">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-129">0.00</span></span>           |
| <span data-ttu-id="764b1-130">Lyhytaikainen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="764b1-130">Short-term threshold</span></span>                    | <span data-ttu-id="764b1-131">12</span><span class="sxs-lookup"><span data-stu-id="764b1-131">12</span></span>             |
| <span data-ttu-id="764b1-132">Arvoltaan vähäinen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="764b1-132">Low Value Threshold</span></span>                     | <span data-ttu-id="764b1-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="764b1-133">5,000.00</span></span>       |
| <span data-ttu-id="764b1-134">Maksu toimittajalle</span><span class="sxs-lookup"><span data-stu-id="764b1-134">Pay to Vendor</span></span>                           | <span data-ttu-id="764b1-135">Nro</span><span class="sxs-lookup"><span data-stu-id="764b1-135">No</span></span>             |

<span data-ttu-id="764b1-136">**Lakisääteinen kirja**</span><span class="sxs-lookup"><span data-stu-id="764b1-136">**Statutory book**</span></span>

<span data-ttu-id="764b1-137">Lakisääteinen kirja on käteisvaroihin perustuva kirja, jonne yritys kirjaa vuokrauksen kulut käteisvarojen summana, joka maksetaan joka kuukausi vuokrana.</span><span class="sxs-lookup"><span data-stu-id="764b1-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="764b1-138">Tämä kirja ei tuota käyttöoikeusomaisuuserää tai vuokrasopimusvelkaa.</span><span class="sxs-lookup"><span data-stu-id="764b1-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="764b1-139">Nimi</span><span class="sxs-lookup"><span data-stu-id="764b1-139">Name</span></span>                                    | <span data-ttu-id="764b1-140">kuvaus</span><span class="sxs-lookup"><span data-stu-id="764b1-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="764b1-141">Kirjan tyyppi</span><span class="sxs-lookup"><span data-stu-id="764b1-141">Book type</span></span>                               | <span data-ttu-id="764b1-142">Lakisääteinen</span><span class="sxs-lookup"><span data-stu-id="764b1-142">Statutory</span></span>   |
| <span data-ttu-id="764b1-143">Kirjan kuvaus</span><span class="sxs-lookup"><span data-stu-id="764b1-143">Book description</span></span>                        | <span data-ttu-id="764b1-144">Paikallinen GAAP</span><span class="sxs-lookup"><span data-stu-id="764b1-144">Local GAAP</span></span>  |
| <span data-ttu-id="764b1-145">Kirjanpitotaso</span><span class="sxs-lookup"><span data-stu-id="764b1-145">Posting Layer</span></span>                           | <span data-ttu-id="764b1-146">Valittu</span><span class="sxs-lookup"><span data-stu-id="764b1-146">Current</span></span>     |
| <span data-ttu-id="764b1-147">Vuokran tyyppi</span><span class="sxs-lookup"><span data-stu-id="764b1-147">Lease Type</span></span>                              | <span data-ttu-id="764b1-148">Automaattinen</span><span class="sxs-lookup"><span data-stu-id="764b1-148">Automatic</span></span>   |
| <span data-ttu-id="764b1-149">Kirjanpitokehys</span><span class="sxs-lookup"><span data-stu-id="764b1-149">Accounting Framework</span></span>                    | <span data-ttu-id="764b1-150">Maksuperuste</span><span class="sxs-lookup"><span data-stu-id="764b1-150">Cash basis</span></span>  |
| <span data-ttu-id="764b1-151">Vuokra-/käyttöajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="764b1-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="764b1-152">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-152">0.00</span></span>        |
| <span data-ttu-id="764b1-153">Nykyinen arvo / resurssin käyvän arvon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="764b1-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="764b1-154">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-154">0.00</span></span>        |
| <span data-ttu-id="764b1-155">Lyhytaikainen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="764b1-155">Short-term threshold</span></span>                    | <span data-ttu-id="764b1-156">0</span><span class="sxs-lookup"><span data-stu-id="764b1-156">0</span></span>           |
| <span data-ttu-id="764b1-157">Arvoltaan vähäinen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="764b1-157">Low Value Threshold</span></span>                     | <span data-ttu-id="764b1-158">0</span><span class="sxs-lookup"><span data-stu-id="764b1-158">0</span></span>           |
| <span data-ttu-id="764b1-159">Maksu toimittajalle</span><span class="sxs-lookup"><span data-stu-id="764b1-159">Pay to Vendor</span></span>                           | <span data-ttu-id="764b1-160">Nro</span><span class="sxs-lookup"><span data-stu-id="764b1-160">No</span></span>          |

<span data-ttu-id="764b1-161">**Lakisääteinen palautuskirja**</span><span class="sxs-lookup"><span data-stu-id="764b1-161">**Statutory reversal book**</span></span>

<span data-ttu-id="764b1-162">Lakisääteinen palautuskirja määritetään samalla tavalla kuin lakisääteinen kirja.</span><span class="sxs-lookup"><span data-stu-id="764b1-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="764b1-163">Nimi</span><span class="sxs-lookup"><span data-stu-id="764b1-163">Name</span></span>                                    | <span data-ttu-id="764b1-164">kuvaus</span><span class="sxs-lookup"><span data-stu-id="764b1-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="764b1-165">Kirjan tyyppi</span><span class="sxs-lookup"><span data-stu-id="764b1-165">Book type</span></span>                               | <span data-ttu-id="764b1-166">Lakisääteinen – palautus</span><span class="sxs-lookup"><span data-stu-id="764b1-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="764b1-167">Kirjan kuvaus</span><span class="sxs-lookup"><span data-stu-id="764b1-167">Book description</span></span>                        | <span data-ttu-id="764b1-168">Kirjaa käänteiseen lakisääteiseen kirjaan</span><span class="sxs-lookup"><span data-stu-id="764b1-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="764b1-169">Kirjanpitotaso</span><span class="sxs-lookup"><span data-stu-id="764b1-169">Posting Layer</span></span>                           | <span data-ttu-id="764b1-170">Mukautettu kerros 1</span><span class="sxs-lookup"><span data-stu-id="764b1-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="764b1-171">Vuokran tyyppi</span><span class="sxs-lookup"><span data-stu-id="764b1-171">Lease Type</span></span>                              | <span data-ttu-id="764b1-172">Automaattinen</span><span class="sxs-lookup"><span data-stu-id="764b1-172">Automatic</span></span>                      |
| <span data-ttu-id="764b1-173">Kirjanpitokehys</span><span class="sxs-lookup"><span data-stu-id="764b1-173">Accounting Framework</span></span>                    | <span data-ttu-id="764b1-174">Maksuperuste</span><span class="sxs-lookup"><span data-stu-id="764b1-174">Cash basis</span></span>                     |
| <span data-ttu-id="764b1-175">Vuokra-/käyttöajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="764b1-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="764b1-176">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-176">0.00</span></span>                           |
| <span data-ttu-id="764b1-177">Nykyinen arvo / resurssin käyvän arvon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="764b1-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="764b1-178">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-178">0.00</span></span>                           |
| <span data-ttu-id="764b1-179">Lyhytaikainen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="764b1-179">Short-term threshold</span></span>                    | <span data-ttu-id="764b1-180">0</span><span class="sxs-lookup"><span data-stu-id="764b1-180">0</span></span>                              |
| <span data-ttu-id="764b1-181">Arvoltaan vähäinen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="764b1-181">Low Value Threshold</span></span>                     | <span data-ttu-id="764b1-182">0</span><span class="sxs-lookup"><span data-stu-id="764b1-182">0</span></span>                              |
| <span data-ttu-id="764b1-183">Maksu toimittajalle</span><span class="sxs-lookup"><span data-stu-id="764b1-183">Pay to Vendor</span></span>                           | <span data-ttu-id="764b1-184">Nro</span><span class="sxs-lookup"><span data-stu-id="764b1-184">No</span></span>                             |

<span data-ttu-id="764b1-185">Tässä esimerkissä on luotu vuokraus, jolla on seuraavat asetukset **Yleistä**- ja **Maksuaikataulurivit**-välilehdissä.</span><span class="sxs-lookup"><span data-stu-id="764b1-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="764b1-186">**Yleinen-välilehti**</span><span class="sxs-lookup"><span data-stu-id="764b1-186">**General tab**</span></span>

| <span data-ttu-id="764b1-187">Kenttä</span><span class="sxs-lookup"><span data-stu-id="764b1-187">Field</span></span>                      | <span data-ttu-id="764b1-188">Arvo</span><span class="sxs-lookup"><span data-stu-id="764b1-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="764b1-189">Inkrementaalinen lainakorko</span><span class="sxs-lookup"><span data-stu-id="764b1-189">Incremental borrowing rate</span></span> | <span data-ttu-id="764b1-190">5 %</span><span class="sxs-lookup"><span data-stu-id="764b1-190">5%</span></span>               |
| <span data-ttu-id="764b1-191">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="764b1-191">Commencement date</span></span>          | <span data-ttu-id="764b1-192">1.1.2020</span><span class="sxs-lookup"><span data-stu-id="764b1-192">1/1/2020</span></span>         |
| <span data-ttu-id="764b1-193">Vuokraryhmä</span><span class="sxs-lookup"><span data-stu-id="764b1-193">Lease group</span></span>                | <span data-ttu-id="764b1-194">Rakennukset</span><span class="sxs-lookup"><span data-stu-id="764b1-194">Buildings</span></span>        |
| <span data-ttu-id="764b1-195">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="764b1-195">Vendor</span></span>                     | <span data-ttu-id="764b1-196">1001</span><span class="sxs-lookup"><span data-stu-id="764b1-196">1001</span></span>             |
| <span data-ttu-id="764b1-197">Resurssin käypä arvo</span><span class="sxs-lookup"><span data-stu-id="764b1-197">Fair value of the asset</span></span>    | <span data-ttu-id="764b1-198">245,000</span><span class="sxs-lookup"><span data-stu-id="764b1-198">245,000</span></span>          |
| <span data-ttu-id="764b1-199">Käyttöomaisuuden käyttöikä</span><span class="sxs-lookup"><span data-stu-id="764b1-199">Asset useful life</span></span>          | <span data-ttu-id="764b1-200">120</span><span class="sxs-lookup"><span data-stu-id="764b1-200">120</span></span>              |
| <span data-ttu-id="764b1-201">Annuiteetin tyyppi</span><span class="sxs-lookup"><span data-stu-id="764b1-201">Annuity type</span></span>               | <span data-ttu-id="764b1-202">Tavallinen annuiteetti</span><span class="sxs-lookup"><span data-stu-id="764b1-202">Ordinary annuity</span></span> |
| <span data-ttu-id="764b1-203">Yhdistämisväli</span><span class="sxs-lookup"><span data-stu-id="764b1-203">Compounding interval</span></span>       | <span data-ttu-id="764b1-204">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="764b1-204">Monthly</span></span>          |

<span data-ttu-id="764b1-205">**Maksusuunnitelmarivit-välilehti**</span><span class="sxs-lookup"><span data-stu-id="764b1-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="764b1-206">Kenttä</span><span class="sxs-lookup"><span data-stu-id="764b1-206">Field</span></span>             | <span data-ttu-id="764b1-207">Arvo</span><span class="sxs-lookup"><span data-stu-id="764b1-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="764b1-208">Aloituspäivä</span><span class="sxs-lookup"><span data-stu-id="764b1-208">Start date</span></span>        | <span data-ttu-id="764b1-209">1.1.2020</span><span class="sxs-lookup"><span data-stu-id="764b1-209">1/1/2020</span></span>   |
| <span data-ttu-id="764b1-210">Kausiväli</span><span class="sxs-lookup"><span data-stu-id="764b1-210">Period interval</span></span>   | <span data-ttu-id="764b1-211">Kuukautta</span><span class="sxs-lookup"><span data-stu-id="764b1-211">Months</span></span>     |
| <span data-ttu-id="764b1-212">Kaudet</span><span class="sxs-lookup"><span data-stu-id="764b1-212">Periods</span></span>           | <span data-ttu-id="764b1-213">24</span><span class="sxs-lookup"><span data-stu-id="764b1-213">24</span></span>         |
| <span data-ttu-id="764b1-214">Päättymispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="764b1-214">End date</span></span>          | <span data-ttu-id="764b1-215">31.12.2020</span><span class="sxs-lookup"><span data-stu-id="764b1-215">12/31/2020</span></span> |
| <span data-ttu-id="764b1-216">Maksun toistuvuus</span><span class="sxs-lookup"><span data-stu-id="764b1-216">Payment frequency</span></span> | <span data-ttu-id="764b1-217">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="764b1-217">Monthly</span></span>    |
| <span data-ttu-id="764b1-218">Maksun summa</span><span class="sxs-lookup"><span data-stu-id="764b1-218">Payment amount</span></span>    | <span data-ttu-id="764b1-219">1 000</span><span class="sxs-lookup"><span data-stu-id="764b1-219">1,000</span></span>      |

<span data-ttu-id="764b1-220">Jotta tämä vuokraus voidaan ottaa huomioon kahdessa kehyksessä, käytetään sekä nykyistä että mukautettua kirjaustasoa.</span><span class="sxs-lookup"><span data-stu-id="764b1-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="764b1-221">Seuraavassa taulukossa on esimerkki jokaisesta kirjauskansiomerkinnästä, joka vaaditaan vastaamaan tasapuolisesti kunkin raportointistandardin mukaisia taloustietoja.</span><span class="sxs-lookup"><span data-stu-id="764b1-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="764b1-222">Kunkin vuokrauksen ensimmäisen kuukauden kirjauskansiomerkinnän yksityiskohtainen kuvaus annetaan jälkikäteen.</span><span class="sxs-lookup"><span data-stu-id="764b1-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="764b1-223">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="764b1-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="764b1-224">kuvaus</span><span class="sxs-lookup"><span data-stu-id="764b1-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="764b1-225">Lakisääteinen kirja (nykyinen taso)</span><span class="sxs-lookup"><span data-stu-id="764b1-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="764b1-226">Nykyinen taso yhteensä</span><span class="sxs-lookup"><span data-stu-id="764b1-226">Current layer total</span></span></th>
<th><span data-ttu-id="764b1-227">Palautuskirja (mukautettu taso)</span><span class="sxs-lookup"><span data-stu-id="764b1-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="764b1-228">IFRS 16 -kirja (mukautettu taso)</span><span class="sxs-lookup"><span data-stu-id="764b1-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="764b1-229">Nykyinen taso + mukautettu taso yhteensä</span><span class="sxs-lookup"><span data-stu-id="764b1-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="764b1-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="764b1-230">JE-100</span></span></th>
<th><span data-ttu-id="764b1-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="764b1-231">JE-110</span></span></th>
<th><span data-ttu-id="764b1-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="764b1-232">JE-120</span></span></th>
<th><span data-ttu-id="764b1-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="764b1-233">JE-130</span></span></th>
<th><span data-ttu-id="764b1-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="764b1-234">JE-140</span></span></th>
<th><span data-ttu-id="764b1-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="764b1-235">JE-150</span></span></th>
<th><span data-ttu-id="764b1-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="764b1-236">JE-160</span></span></th>
<th><span data-ttu-id="764b1-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="764b1-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="764b1-238">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="764b1-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="764b1-239">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="764b1-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="764b1-240">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="764b1-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="764b1-241">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="764b1-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="764b1-242">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="764b1-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="764b1-243">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="764b1-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="764b1-244">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="764b1-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="764b1-245">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="764b1-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="764b1-246">1</span><span class="sxs-lookup"><span data-stu-id="764b1-246">1</span></span></td>
<td><span data-ttu-id="764b1-247">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="764b1-247">Lease expense</span></span></td>
<td><span data-ttu-id="764b1-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="764b1-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="764b1-249">1,000.00</span></span></td>
<td><span data-ttu-id="764b1-250">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="764b1-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-251">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="764b1-252">2</span><span class="sxs-lookup"><span data-stu-id="764b1-252">2</span></span></td>
<td><span data-ttu-id="764b1-253">Pankkikulu</span><span class="sxs-lookup"><span data-stu-id="764b1-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="764b1-254">3.00</span><span class="sxs-lookup"><span data-stu-id="764b1-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="764b1-255">3.00</span><span class="sxs-lookup"><span data-stu-id="764b1-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-256">3.00</span><span class="sxs-lookup"><span data-stu-id="764b1-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="764b1-257">3</span><span class="sxs-lookup"><span data-stu-id="764b1-257">3</span></span></td>
<td><span data-ttu-id="764b1-258">ALV-kulu</span><span class="sxs-lookup"><span data-stu-id="764b1-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="764b1-259">5.00</span><span class="sxs-lookup"><span data-stu-id="764b1-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="764b1-260">5.00</span><span class="sxs-lookup"><span data-stu-id="764b1-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-261">5.00</span><span class="sxs-lookup"><span data-stu-id="764b1-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="764b1-262">4</span><span class="sxs-lookup"><span data-stu-id="764b1-262">4</span></span></td>
<td><span data-ttu-id="764b1-263">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="764b1-263">Clearing account</span></span></td>
<td><span data-ttu-id="764b1-264">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="764b1-264">-1,000.00</span></span></td>
<td><span data-ttu-id="764b1-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="764b1-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="764b1-266">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-266">0.00</span></span></td>
<td><span data-ttu-id="764b1-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="764b1-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="764b1-268">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="764b1-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-269">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="764b1-270">5</span><span class="sxs-lookup"><span data-stu-id="764b1-270">5</span></span></td>
<td><span data-ttu-id="764b1-271">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="764b1-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="764b1-272">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="764b1-272">-1,008.00</span></span></td>
<td><span data-ttu-id="764b1-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="764b1-273">1,008.00</span></span></td>
<td><span data-ttu-id="764b1-274">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-275">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="764b1-276">6</span><span class="sxs-lookup"><span data-stu-id="764b1-276">6</span></span></td>
<td><span data-ttu-id="764b1-277">Käyttöoikeusomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="764b1-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-278">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="764b1-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="764b1-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="764b1-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="764b1-281">7</span><span class="sxs-lookup"><span data-stu-id="764b1-281">7</span></span></td>
<td><span data-ttu-id="764b1-282">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="764b1-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-283">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="764b1-284">-22 794,00</span><span class="sxs-lookup"><span data-stu-id="764b1-284">-22,794.00</span></span></td>
<td><span data-ttu-id="764b1-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="764b1-285">1,000.00</span></span></td>
<td><span data-ttu-id="764b1-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="764b1-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="764b1-287">-21 888,87</span><span class="sxs-lookup"><span data-stu-id="764b1-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="764b1-288">8</span><span class="sxs-lookup"><span data-stu-id="764b1-288">8</span></span></td>
<td><span data-ttu-id="764b1-289">Korkokustannus</span><span class="sxs-lookup"><span data-stu-id="764b1-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-290">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-291">94.97</span><span class="sxs-lookup"><span data-stu-id="764b1-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="764b1-292">94.97</span><span class="sxs-lookup"><span data-stu-id="764b1-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="764b1-293">9</span><span class="sxs-lookup"><span data-stu-id="764b1-293">9</span></span></td>
<td><span data-ttu-id="764b1-294">Maksu</span><span class="sxs-lookup"><span data-stu-id="764b1-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-295">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="764b1-295">-1,008.00</span></span></td>
<td><span data-ttu-id="764b1-296">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="764b1-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-297">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="764b1-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="764b1-298">10</span><span class="sxs-lookup"><span data-stu-id="764b1-298">10</span></span></td>
<td><span data-ttu-id="764b1-299">Poistokulu</span><span class="sxs-lookup"><span data-stu-id="764b1-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-300">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-301">949.75</span><span class="sxs-lookup"><span data-stu-id="764b1-301">949.75</span></span></td>
<td><span data-ttu-id="764b1-302">949.75</span><span class="sxs-lookup"><span data-stu-id="764b1-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="764b1-303">11</span><span class="sxs-lookup"><span data-stu-id="764b1-303">11</span></span></td>
<td><span data-ttu-id="764b1-304">Kertynyt poisto</span><span class="sxs-lookup"><span data-stu-id="764b1-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-305">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="764b1-306">-949.75</span></span></td>
<td><span data-ttu-id="764b1-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="764b1-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="764b1-308">Kuten edellä olevasta taulukosta ilmenee, sekä lakisääteinen raportointi että IFRS-raportointi edellyttävät kolmen kirjan käyttämistä.</span><span class="sxs-lookup"><span data-stu-id="764b1-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="764b1-309">Lakisääteinen kirja tallentaa vuokrat nykyisen tason käteisvaroihin perustuvan kirjanpidon sääntöjen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="764b1-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="764b1-310">Lakisääteinen palautuskirja kumoaa lakisääteiset kirjauskansiomerkinnät.</span><span class="sxs-lookup"><span data-stu-id="764b1-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="764b1-311">IFRS 16 -kirja luo IFRS 16:n pakolliset kirjauskansiomerkinnät.</span><span class="sxs-lookup"><span data-stu-id="764b1-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="764b1-312">Sinun on syötettävä vuokraus vain kerran.</span><span class="sxs-lookup"><span data-stu-id="764b1-312">You must enter a lease only one time.</span></span> <span data-ttu-id="764b1-313">Tämän jälkeen voit avata **Kirjat**-sivun, ja näet kaikki vuokraukseen liittyvät kirjat.</span><span class="sxs-lookup"><span data-stu-id="764b1-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="764b1-314">Kun luot kirjoja, kaikkien kolmen on liityttävä samaan vuokraustietueeseen.</span><span class="sxs-lookup"><span data-stu-id="764b1-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="764b1-315">Ensimmäinen kirjauskansiomerkintä tallentaa vuokrauksen lakisääteiseen kirjaan.</span><span class="sxs-lookup"><span data-stu-id="764b1-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="764b1-316">Voit luoda maksut eränä tai valitsemalla maksusuunnitelman lakisääteisestä kirjasta.</span><span class="sxs-lookup"><span data-stu-id="764b1-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="764b1-317">Tässä esimerkissä maksusuunnitelmasta luodaan seuraava kirjauskansiomerkintä lakisääteistä kirjaa varten.</span><span class="sxs-lookup"><span data-stu-id="764b1-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="764b1-318">Vuokra – 31.1.2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="764b1-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="764b1-319">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="764b1-319">Account type</span></span> | <span data-ttu-id="764b1-320">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="764b1-320">Account number</span></span> | <span data-ttu-id="764b1-321">Taso</span><span class="sxs-lookup"><span data-stu-id="764b1-321">Layer</span></span>   | <span data-ttu-id="764b1-322">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="764b1-322">Account description</span></span> | <span data-ttu-id="764b1-323">Veloitus</span><span class="sxs-lookup"><span data-stu-id="764b1-323">Debit</span></span>    | <span data-ttu-id="764b1-324">Luotto</span><span class="sxs-lookup"><span data-stu-id="764b1-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="764b1-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="764b1-325">Ledger</span></span>       | <span data-ttu-id="764b1-326">1</span><span class="sxs-lookup"><span data-stu-id="764b1-326">1</span></span>              | <span data-ttu-id="764b1-327">Valittu</span><span class="sxs-lookup"><span data-stu-id="764b1-327">Current</span></span> | <span data-ttu-id="764b1-328">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="764b1-328">Lease expense</span></span>       | <span data-ttu-id="764b1-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="764b1-329">1,000.00</span></span> |          |
| <span data-ttu-id="764b1-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="764b1-330">Ledger</span></span>       | <span data-ttu-id="764b1-331">4</span><span class="sxs-lookup"><span data-stu-id="764b1-331">4</span></span>              | <span data-ttu-id="764b1-332">Valittu</span><span class="sxs-lookup"><span data-stu-id="764b1-332">Current</span></span> | <span data-ttu-id="764b1-333">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="764b1-333">Clearing account</span></span>    |          | <span data-ttu-id="764b1-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="764b1-334">1,000.00</span></span> |

<span data-ttu-id="764b1-335">Ostoreskontran käsittelijä käyttää Dynamics 365:n vakiotoimintoa luodessaan resurssin vuokrauksen ulkopuoliselle vuokraukselle laskun maksamista varten.</span><span class="sxs-lookup"><span data-stu-id="764b1-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="764b1-336">Sen sijaan, että debettiliksi valittaisiin **Vuokran kulu** ostoreskontran käsittelijä valitsee selvitystilin seuraavan merkinnän luomiseksi.</span><span class="sxs-lookup"><span data-stu-id="764b1-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="764b1-337">Ostoreskontran prosessi – 31.1.2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="764b1-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="764b1-338">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="764b1-338">Account type</span></span> | <span data-ttu-id="764b1-339">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="764b1-339">Account number</span></span> | <span data-ttu-id="764b1-340">Taso</span><span class="sxs-lookup"><span data-stu-id="764b1-340">Layer</span></span>   | <span data-ttu-id="764b1-341">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="764b1-341">Account description</span></span> | <span data-ttu-id="764b1-342">Veloitus</span><span class="sxs-lookup"><span data-stu-id="764b1-342">Debit</span></span>    | <span data-ttu-id="764b1-343">Luotto</span><span class="sxs-lookup"><span data-stu-id="764b1-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="764b1-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="764b1-344">Ledger</span></span>       | <span data-ttu-id="764b1-345">4</span><span class="sxs-lookup"><span data-stu-id="764b1-345">4</span></span>              | <span data-ttu-id="764b1-346">Valittu</span><span class="sxs-lookup"><span data-stu-id="764b1-346">Current</span></span> | <span data-ttu-id="764b1-347">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="764b1-347">Clearing account</span></span>    | <span data-ttu-id="764b1-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="764b1-348">1,000.00</span></span> |          |
| <span data-ttu-id="764b1-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="764b1-349">Ledger</span></span>       | <span data-ttu-id="764b1-350">2</span><span class="sxs-lookup"><span data-stu-id="764b1-350">2</span></span>              | <span data-ttu-id="764b1-351">Valittu</span><span class="sxs-lookup"><span data-stu-id="764b1-351">Current</span></span> | <span data-ttu-id="764b1-352">Pankkikulu</span><span class="sxs-lookup"><span data-stu-id="764b1-352">Bank fee</span></span>            | <span data-ttu-id="764b1-353">3.00</span><span class="sxs-lookup"><span data-stu-id="764b1-353">3.00</span></span>     |          |
| <span data-ttu-id="764b1-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="764b1-354">Ledger</span></span>       | <span data-ttu-id="764b1-355">3</span><span class="sxs-lookup"><span data-stu-id="764b1-355">3</span></span>              | <span data-ttu-id="764b1-356">Valittu</span><span class="sxs-lookup"><span data-stu-id="764b1-356">Current</span></span> | <span data-ttu-id="764b1-357">ALV-kulu</span><span class="sxs-lookup"><span data-stu-id="764b1-357">VAT expense</span></span>         | <span data-ttu-id="764b1-358">5.00</span><span class="sxs-lookup"><span data-stu-id="764b1-358">5.00</span></span>     |          |
| <span data-ttu-id="764b1-359">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="764b1-359">Vendor</span></span>       | <span data-ttu-id="764b1-360">5</span><span class="sxs-lookup"><span data-stu-id="764b1-360">5</span></span>              | <span data-ttu-id="764b1-361">Valittu</span><span class="sxs-lookup"><span data-stu-id="764b1-361">Current</span></span> | <span data-ttu-id="764b1-362">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="764b1-362">Accounts payable</span></span>    |          | <span data-ttu-id="764b1-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="764b1-363">1,008.00</span></span> |

<span data-ttu-id="764b1-364">Kun toimittajalle annetaan ilmoitus, seuraat säännöllistä maksuprosessia.</span><span class="sxs-lookup"><span data-stu-id="764b1-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="764b1-365">Tämän prosessin aikana luodaan seuraava kirjauskansiomerkintä.</span><span class="sxs-lookup"><span data-stu-id="764b1-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="764b1-366">Käteismaksu – 31.1.2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="764b1-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="764b1-367">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="764b1-367">Account type</span></span> | <span data-ttu-id="764b1-368">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="764b1-368">Account number</span></span> | <span data-ttu-id="764b1-369">Taso</span><span class="sxs-lookup"><span data-stu-id="764b1-369">Layer</span></span>   | <span data-ttu-id="764b1-370">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="764b1-370">Account description</span></span> | <span data-ttu-id="764b1-371">Veloitus</span><span class="sxs-lookup"><span data-stu-id="764b1-371">Debit</span></span>    | <span data-ttu-id="764b1-372">Luotto</span><span class="sxs-lookup"><span data-stu-id="764b1-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="764b1-373">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="764b1-373">Vendor</span></span>       | <span data-ttu-id="764b1-374">5</span><span class="sxs-lookup"><span data-stu-id="764b1-374">5</span></span>              | <span data-ttu-id="764b1-375">Valittu</span><span class="sxs-lookup"><span data-stu-id="764b1-375">Current</span></span> | <span data-ttu-id="764b1-376">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="764b1-376">Accounts Payable</span></span>    | <span data-ttu-id="764b1-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="764b1-377">1,008.00</span></span> |          |
| <span data-ttu-id="764b1-378">Pankki</span><span class="sxs-lookup"><span data-stu-id="764b1-378">Bank</span></span>         | <span data-ttu-id="764b1-379">9</span><span class="sxs-lookup"><span data-stu-id="764b1-379">9</span></span>              | <span data-ttu-id="764b1-380">Valittu</span><span class="sxs-lookup"><span data-stu-id="764b1-380">Current</span></span> | <span data-ttu-id="764b1-381">Maksu</span><span class="sxs-lookup"><span data-stu-id="764b1-381">Cash</span></span>                |          | <span data-ttu-id="764b1-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="764b1-382">1,008.00</span></span> |

<span data-ttu-id="764b1-383">Nyt tämä vuokraus on otettu kokonaan huomioon lakisääteisen raportoinnin vaatimusten mukaisesti, ja voit luoda pääkirjan nykyisen tason mukaan.</span><span class="sxs-lookup"><span data-stu-id="764b1-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="764b1-384">Järjestelmä palauttaa pääkirjan, jossa ovat seuraavat luvut.</span><span class="sxs-lookup"><span data-stu-id="764b1-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="764b1-385">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="764b1-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="764b1-386">kuvaus</span><span class="sxs-lookup"><span data-stu-id="764b1-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="764b1-387">Lakisääteinen kirja (nykyinen taso)</span><span class="sxs-lookup"><span data-stu-id="764b1-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="764b1-388">Nykyinen taso yhteensä</span><span class="sxs-lookup"><span data-stu-id="764b1-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="764b1-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="764b1-389">JE-100</span></span></th>
<th><span data-ttu-id="764b1-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="764b1-390">JE-110</span></span></th>
<th><span data-ttu-id="764b1-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="764b1-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="764b1-392">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="764b1-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="764b1-393">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="764b1-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="764b1-394">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="764b1-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="764b1-395">1</span><span class="sxs-lookup"><span data-stu-id="764b1-395">1</span></span></td>
<td><span data-ttu-id="764b1-396">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="764b1-396">Lease expense</span></span></td>
<td><span data-ttu-id="764b1-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="764b1-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="764b1-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="764b1-399">2</span><span class="sxs-lookup"><span data-stu-id="764b1-399">2</span></span></td>
<td><span data-ttu-id="764b1-400">Pankkikulu</span><span class="sxs-lookup"><span data-stu-id="764b1-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="764b1-401">3.00</span><span class="sxs-lookup"><span data-stu-id="764b1-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="764b1-402">3.00</span><span class="sxs-lookup"><span data-stu-id="764b1-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="764b1-403">3</span><span class="sxs-lookup"><span data-stu-id="764b1-403">3</span></span></td>
<td><span data-ttu-id="764b1-404">ALV-kulu</span><span class="sxs-lookup"><span data-stu-id="764b1-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="764b1-405">5.00</span><span class="sxs-lookup"><span data-stu-id="764b1-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="764b1-406">5.00</span><span class="sxs-lookup"><span data-stu-id="764b1-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="764b1-407">4</span><span class="sxs-lookup"><span data-stu-id="764b1-407">4</span></span></td>
<td><span data-ttu-id="764b1-408">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="764b1-408">Clearing account</span></span></td>
<td><span data-ttu-id="764b1-409">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="764b1-409">-1,000.00</span></span></td>
<td><span data-ttu-id="764b1-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="764b1-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="764b1-411">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="764b1-412">5</span><span class="sxs-lookup"><span data-stu-id="764b1-412">5</span></span></td>
<td><span data-ttu-id="764b1-413">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="764b1-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="764b1-414">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="764b1-414">-1,008.00</span></span></td>
<td><span data-ttu-id="764b1-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="764b1-415">1,008.00</span></span></td>
<td><span data-ttu-id="764b1-416">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="764b1-417">6</span><span class="sxs-lookup"><span data-stu-id="764b1-417">6</span></span></td>
<td><span data-ttu-id="764b1-418">Käyttöoikeusomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="764b1-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-419">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="764b1-420">7</span><span class="sxs-lookup"><span data-stu-id="764b1-420">7</span></span></td>
<td><span data-ttu-id="764b1-421">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="764b1-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-422">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="764b1-423">8</span><span class="sxs-lookup"><span data-stu-id="764b1-423">8</span></span></td>
<td><span data-ttu-id="764b1-424">Korkokustannus</span><span class="sxs-lookup"><span data-stu-id="764b1-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-425">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="764b1-426">9</span><span class="sxs-lookup"><span data-stu-id="764b1-426">9</span></span></td>
<td><span data-ttu-id="764b1-427">Maksu</span><span class="sxs-lookup"><span data-stu-id="764b1-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-428">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="764b1-428">-1,008.00</span></span></td>
<td><span data-ttu-id="764b1-429">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="764b1-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="764b1-430">10</span><span class="sxs-lookup"><span data-stu-id="764b1-430">10</span></span></td>
<td><span data-ttu-id="764b1-431">Poistokulu</span><span class="sxs-lookup"><span data-stu-id="764b1-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-432">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="764b1-433">11</span><span class="sxs-lookup"><span data-stu-id="764b1-433">11</span></span></td>
<td><span data-ttu-id="764b1-434">Kertynyt poisto</span><span class="sxs-lookup"><span data-stu-id="764b1-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="764b1-435">0,00</span><span class="sxs-lookup"><span data-stu-id="764b1-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="764b1-436">Jos haluat käyttää IFRS 16 -lukuja ja suorittaa saman pääkirjan, lakisääteisen kirjapidon kirjauskansioviennit on palautettava ja IFRS 16 -kirjauskansioviennit kirjattava.</span><span class="sxs-lookup"><span data-stu-id="764b1-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="764b1-437">Tässä esimerkissä on myös lakisääteinen palautuskirja siltä varalta, että haluat palauttaa lakisääteiset kirjauskansioviennit. Palautuskirjassa on samat asetukset kuin lakisääteisessä kirjassa, mutta vastakkainen kirjausprofiili.</span><span class="sxs-lookup"><span data-stu-id="764b1-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="764b1-438">Esimerkiksi lakisääteinen kirja *veloitti* vuokrauksen kulutilin, mutta palautuskirja *hyvittää* tämän tilin.</span><span class="sxs-lookup"><span data-stu-id="764b1-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="764b1-439">Nämä suhteet on helppo määrittää resurssin vuokrauksen kirjaustileillä **Resurssin vuokrauksen parametrit** -sivulla (**Resurssin vuokraus \> Asetukset \> Resurssin vuokrauksen parametrit**).</span><span class="sxs-lookup"><span data-stu-id="764b1-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="764b1-440">Kun lakisääteisessä kirjassa käytettyä prosessia käytetään palautuskirjassa, luodaan seuraava kirjauskansiovienti.</span><span class="sxs-lookup"><span data-stu-id="764b1-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="764b1-441">Erona on se, että palautuskirja kirjaa vastakirjaukset lakisääteisestä kirjasta.</span><span class="sxs-lookup"><span data-stu-id="764b1-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="764b1-442">Vastakirjaukset tehdään myös mukautetussa tasossa.</span><span class="sxs-lookup"><span data-stu-id="764b1-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="764b1-443">Kun pääkirja suoritetaan nykyisellä tasolla, palautuskirjauskansiovientejä ei sisällytetä.</span><span class="sxs-lookup"><span data-stu-id="764b1-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="764b1-444">Vuokra – 31.1.2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="764b1-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="764b1-445">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="764b1-445">Account type</span></span> | <span data-ttu-id="764b1-446">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="764b1-446">Account number</span></span> | <span data-ttu-id="764b1-447">Taso</span><span class="sxs-lookup"><span data-stu-id="764b1-447">Layer</span></span>  | <span data-ttu-id="764b1-448">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="764b1-448">Account description</span></span> | <span data-ttu-id="764b1-449">Veloitus</span><span class="sxs-lookup"><span data-stu-id="764b1-449">Debit</span></span>    | <span data-ttu-id="764b1-450">Luotto</span><span class="sxs-lookup"><span data-stu-id="764b1-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="764b1-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="764b1-451">Ledger</span></span>       | <span data-ttu-id="764b1-452">4</span><span class="sxs-lookup"><span data-stu-id="764b1-452">4</span></span>              | <span data-ttu-id="764b1-453">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="764b1-453">Custom</span></span> | <span data-ttu-id="764b1-454">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="764b1-454">Clearing account</span></span>    | <span data-ttu-id="764b1-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="764b1-455">1,000.00</span></span> |          |
| <span data-ttu-id="764b1-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="764b1-456">Ledger</span></span>       | <span data-ttu-id="764b1-457">1</span><span class="sxs-lookup"><span data-stu-id="764b1-457">1</span></span>              | <span data-ttu-id="764b1-458">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="764b1-458">Custom</span></span> | <span data-ttu-id="764b1-459">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="764b1-459">Lease expense</span></span>       |          | <span data-ttu-id="764b1-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="764b1-460">1,000.00</span></span> |

<span data-ttu-id="764b1-461">Nyt lakisääteiset kirjauskansioviennit on eliminoitu, ja voit kirjata kaikki IFRS 16:n edellyttämät kirjauskansioviennit IFRS 16 -kirjaan.</span><span class="sxs-lookup"><span data-stu-id="764b1-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="764b1-462">Nämä viennit sisältävät käyttöoikeusomaisuuserän ja velan alkuperäisen kirjauksen sekä koron ja poiston tietueen.</span><span class="sxs-lookup"><span data-stu-id="764b1-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="764b1-463">Alkuperäinen kirjaus – 1.1.2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="764b1-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="764b1-464">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="764b1-464">Account type</span></span> | <span data-ttu-id="764b1-465">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="764b1-465">Account number</span></span> | <span data-ttu-id="764b1-466">Taso</span><span class="sxs-lookup"><span data-stu-id="764b1-466">Layer</span></span>  | <span data-ttu-id="764b1-467">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="764b1-467">Account description</span></span>      | <span data-ttu-id="764b1-468">Veloitus</span><span class="sxs-lookup"><span data-stu-id="764b1-468">Debit</span></span>     | <span data-ttu-id="764b1-469">Luotto</span><span class="sxs-lookup"><span data-stu-id="764b1-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="764b1-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="764b1-470">Ledger</span></span>       | <span data-ttu-id="764b1-471">6</span><span class="sxs-lookup"><span data-stu-id="764b1-471">6</span></span>              | <span data-ttu-id="764b1-472">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="764b1-472">Custom</span></span> | <span data-ttu-id="764b1-473">Käyttöoikeusomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="764b1-473">ROU Asset</span></span>                | <span data-ttu-id="764b1-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="764b1-474">22,793.90</span></span> |           |
| <span data-ttu-id="764b1-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="764b1-475">Ledger</span></span>       | <span data-ttu-id="764b1-476">7</span><span class="sxs-lookup"><span data-stu-id="764b1-476">7</span></span>              | <span data-ttu-id="764b1-477">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="764b1-477">Custom</span></span> | <span data-ttu-id="764b1-478">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="764b1-478">Finance lease obligation</span></span> |           | <span data-ttu-id="764b1-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="764b1-479">22,793.90</span></span> |

<span data-ttu-id="764b1-480">Vuokra kirjataan kuten muut vuokrat.</span><span class="sxs-lookup"><span data-stu-id="764b1-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="764b1-481">Selvitystiliä käytetään, jotta voidaan varmistaa käteisen hyvitys vain kerran.</span><span class="sxs-lookup"><span data-stu-id="764b1-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="764b1-482">Vuokra – 31.1.2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="764b1-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="764b1-483">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="764b1-483">Account type</span></span> | <span data-ttu-id="764b1-484">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="764b1-484">Account number</span></span> | <span data-ttu-id="764b1-485">Taso</span><span class="sxs-lookup"><span data-stu-id="764b1-485">Layer</span></span>  | <span data-ttu-id="764b1-486">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="764b1-486">Account description</span></span>      | <span data-ttu-id="764b1-487">Veloitus</span><span class="sxs-lookup"><span data-stu-id="764b1-487">Debit</span></span>    | <span data-ttu-id="764b1-488">Luotto</span><span class="sxs-lookup"><span data-stu-id="764b1-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="764b1-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="764b1-489">Ledger</span></span>       | <span data-ttu-id="764b1-490">7</span><span class="sxs-lookup"><span data-stu-id="764b1-490">7</span></span>              | <span data-ttu-id="764b1-491">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="764b1-491">Custom</span></span> | <span data-ttu-id="764b1-492">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="764b1-492">Finance lease obligation</span></span> | <span data-ttu-id="764b1-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="764b1-493">1,000.00</span></span> |          |
| <span data-ttu-id="764b1-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="764b1-494">Ledger</span></span>       | <span data-ttu-id="764b1-495">4</span><span class="sxs-lookup"><span data-stu-id="764b1-495">4</span></span>              | <span data-ttu-id="764b1-496">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="764b1-496">Custom</span></span> | <span data-ttu-id="764b1-497">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="764b1-497">Clearing account</span></span>         |          | <span data-ttu-id="764b1-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="764b1-498">1,000.00</span></span> |

<span data-ttu-id="764b1-499">Korkokulun kirjauskansiovienti luodaan velan kuoletusaikataulusta.</span><span class="sxs-lookup"><span data-stu-id="764b1-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="764b1-500">Korkokustannus – 31.1.2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="764b1-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="764b1-501">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="764b1-501">Account type</span></span> | <span data-ttu-id="764b1-502">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="764b1-502">Account number</span></span> | <span data-ttu-id="764b1-503">Taso</span><span class="sxs-lookup"><span data-stu-id="764b1-503">Layer</span></span>  | <span data-ttu-id="764b1-504">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="764b1-504">Account description</span></span>      | <span data-ttu-id="764b1-505">Veloitus</span><span class="sxs-lookup"><span data-stu-id="764b1-505">Debit</span></span> | <span data-ttu-id="764b1-506">Luotto</span><span class="sxs-lookup"><span data-stu-id="764b1-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="764b1-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="764b1-507">Ledger</span></span>       | <span data-ttu-id="764b1-508">8</span><span class="sxs-lookup"><span data-stu-id="764b1-508">8</span></span>              | <span data-ttu-id="764b1-509">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="764b1-509">Custom</span></span> | <span data-ttu-id="764b1-510">Korkokustannus</span><span class="sxs-lookup"><span data-stu-id="764b1-510">Interest expense</span></span>         | <span data-ttu-id="764b1-511">94.97</span><span class="sxs-lookup"><span data-stu-id="764b1-511">94.97</span></span> |        |
| <span data-ttu-id="764b1-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="764b1-512">Ledger</span></span>       | <span data-ttu-id="764b1-513">7</span><span class="sxs-lookup"><span data-stu-id="764b1-513">7</span></span>              | <span data-ttu-id="764b1-514">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="764b1-514">Custom</span></span> | <span data-ttu-id="764b1-515">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="764b1-515">Finance lease obligation</span></span> |       | <span data-ttu-id="764b1-516">94.97</span><span class="sxs-lookup"><span data-stu-id="764b1-516">94.97</span></span>  |

<span data-ttu-id="764b1-517">Poistokulun kirjauskansiovienti luodaan resurssin poistoaikataulusta.</span><span class="sxs-lookup"><span data-stu-id="764b1-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="764b1-518">Poistokulu – 31.1.2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="764b1-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="764b1-519">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="764b1-519">Account type</span></span> | <span data-ttu-id="764b1-520">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="764b1-520">Account number</span></span> | <span data-ttu-id="764b1-521">Taso</span><span class="sxs-lookup"><span data-stu-id="764b1-521">Layer</span></span>  | <span data-ttu-id="764b1-522">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="764b1-522">Account description</span></span>      | <span data-ttu-id="764b1-523">Veloitus</span><span class="sxs-lookup"><span data-stu-id="764b1-523">Debit</span></span>  | <span data-ttu-id="764b1-524">Luotto</span><span class="sxs-lookup"><span data-stu-id="764b1-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="764b1-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="764b1-525">Ledger</span></span>       | <span data-ttu-id="764b1-526">10</span><span class="sxs-lookup"><span data-stu-id="764b1-526">10</span></span>             | <span data-ttu-id="764b1-527">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="764b1-527">Custom</span></span> | <span data-ttu-id="764b1-528">Poistokulu</span><span class="sxs-lookup"><span data-stu-id="764b1-528">Depreciation expense</span></span>     | <span data-ttu-id="764b1-529">949.75</span><span class="sxs-lookup"><span data-stu-id="764b1-529">949.75</span></span> |        |
| <span data-ttu-id="764b1-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="764b1-530">Ledger</span></span>       | <span data-ttu-id="764b1-531">11</span><span class="sxs-lookup"><span data-stu-id="764b1-531">11</span></span>             | <span data-ttu-id="764b1-532">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="764b1-532">Custom</span></span> | <span data-ttu-id="764b1-533">Kertynyt poisto</span><span class="sxs-lookup"><span data-stu-id="764b1-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="764b1-534">949.75</span><span class="sxs-lookup"><span data-stu-id="764b1-534">949.75</span></span> |

<span data-ttu-id="764b1-535">Kun kaikki nämä kirjauskansioviennit on luotu ja kirjattu, näkyvissä ovat seuraavat mukautetun tason 1 arvot.</span><span class="sxs-lookup"><span data-stu-id="764b1-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="764b1-536">Huomaa, että viimeinen sarake sisältää pankkikulun, ALV-kulun ja käteisvähennyksen edelliseltä tasolta, mutta ei lakisääteisen raportoinnin kirjauskansiovientejä.</span><span class="sxs-lookup"><span data-stu-id="764b1-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="764b1-537">Näin saavutetaan todelliset kaksoisraportoinnin ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="764b1-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="764b1-538">Tässä vaiheessa yritys on juuri suorittanut pääkirjan ja yhdistää nykyisen tason mukautettuun tasoon IFRS-pääkirjan luomista varten.</span><span class="sxs-lookup"><span data-stu-id="764b1-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="764b1-539">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="764b1-539">Account No</span></span> | <span data-ttu-id="764b1-540">kuvaus</span><span class="sxs-lookup"><span data-stu-id="764b1-540">Description</span></span>              | <span data-ttu-id="764b1-541">Lakisääteinen kirja\-Nykyinen taso\-JE\-100\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="764b1-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="764b1-542">Lakisääteinen kirja\-Nykyinen taso\-JE\-110\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="764b1-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="764b1-543">Lakisääteinen kirja\-Nykyinen taso\-JE\-120\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="764b1-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="764b1-544">Nykyinen taso \- Kokonaissummat</span><span class="sxs-lookup"><span data-stu-id="764b1-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="764b1-545">Palautuskirja\-Mukautettu taso\-JE\-130\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="764b1-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="764b1-546">IFRS 16 -kirja\-Mukautettu taso\-JE\-140\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="764b1-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="764b1-547">IFRS 16 -kirja\-Mukautettu taso\-JE\-150\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="764b1-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="764b1-548">IFRS 16 -kirja\-Mukautettu taso\-JE\-160\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="764b1-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="764b1-549">IFRS 16 -kirja\-Mukautettu taso\-JE\-170\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="764b1-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="764b1-550">Mukautettu taso \+ Nykyinen taso \- Kokonaissummat</span><span class="sxs-lookup"><span data-stu-id="764b1-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="764b1-551">1</span><span class="sxs-lookup"><span data-stu-id="764b1-551">1</span></span>          | <span data-ttu-id="764b1-552">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="764b1-552">Lease expense</span></span>            | <span data-ttu-id="764b1-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="764b1-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-554">1,000\.00</span></span>               |   | <span data-ttu-id="764b1-555">\-1 000</span><span class="sxs-lookup"><span data-stu-id="764b1-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="764b1-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-556">0\.00</span></span>                                   |
| <span data-ttu-id="764b1-557">2</span><span class="sxs-lookup"><span data-stu-id="764b1-557">2</span></span>          | <span data-ttu-id="764b1-558">Pankkikulu</span><span class="sxs-lookup"><span data-stu-id="764b1-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="764b1-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="764b1-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="764b1-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-561">3\.00</span></span>                                   |
| <span data-ttu-id="764b1-562">3</span><span class="sxs-lookup"><span data-stu-id="764b1-562">3</span></span>          | <span data-ttu-id="764b1-563">ALV-kulu</span><span class="sxs-lookup"><span data-stu-id="764b1-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="764b1-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="764b1-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="764b1-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-566">5\.00</span></span>                                   |
| <span data-ttu-id="764b1-567">4</span><span class="sxs-lookup"><span data-stu-id="764b1-567">4</span></span>          | <span data-ttu-id="764b1-568">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="764b1-568">Clearing account</span></span>         | <span data-ttu-id="764b1-569">\-1 000\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="764b1-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="764b1-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-571">0\.00</span></span>                   |   | <span data-ttu-id="764b1-572">1 000</span><span class="sxs-lookup"><span data-stu-id="764b1-572">1,000</span></span>                                           |                                                | <span data-ttu-id="764b1-573">\-1 000</span><span class="sxs-lookup"><span data-stu-id="764b1-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="764b1-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-574">0\.00</span></span>                                   |
| <span data-ttu-id="764b1-575">5</span><span class="sxs-lookup"><span data-stu-id="764b1-575">5</span></span>          | <span data-ttu-id="764b1-576">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="764b1-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="764b1-577">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="764b1-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-578">1,008\.00</span></span>                                         | <span data-ttu-id="764b1-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="764b1-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-580">0\.00</span></span>                                   |
| <span data-ttu-id="764b1-581">6</span><span class="sxs-lookup"><span data-stu-id="764b1-581">6</span></span>          | <span data-ttu-id="764b1-582">Käyttöoikeusomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="764b1-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="764b1-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="764b1-584">22,794</span><span class="sxs-lookup"><span data-stu-id="764b1-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="764b1-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="764b1-585">22,793\.90</span></span>                              |
| <span data-ttu-id="764b1-586">7</span><span class="sxs-lookup"><span data-stu-id="764b1-586">7</span></span>          | <span data-ttu-id="764b1-587">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="764b1-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="764b1-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="764b1-589">\-22 794</span><span class="sxs-lookup"><span data-stu-id="764b1-589">\-22,794</span></span>                                       | <span data-ttu-id="764b1-590">1 000</span><span class="sxs-lookup"><span data-stu-id="764b1-590">1,000</span></span>                                          | <span data-ttu-id="764b1-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="764b1-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="764b1-592">\-21,888\.87</span><span class="sxs-lookup"><span data-stu-id="764b1-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="764b1-593">8</span><span class="sxs-lookup"><span data-stu-id="764b1-593">8</span></span>          | <span data-ttu-id="764b1-594">Korkokustannus</span><span class="sxs-lookup"><span data-stu-id="764b1-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="764b1-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="764b1-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="764b1-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="764b1-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="764b1-597">94\.97</span></span>                                  |
| <span data-ttu-id="764b1-598">9</span><span class="sxs-lookup"><span data-stu-id="764b1-598">9</span></span>          | <span data-ttu-id="764b1-599">Maksu</span><span class="sxs-lookup"><span data-stu-id="764b1-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="764b1-600">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="764b1-601">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="764b1-602">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="764b1-603">10</span><span class="sxs-lookup"><span data-stu-id="764b1-603">10</span></span>         | <span data-ttu-id="764b1-604">Poistokulu</span><span class="sxs-lookup"><span data-stu-id="764b1-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="764b1-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="764b1-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="764b1-606">949\.75</span></span>                                        | <span data-ttu-id="764b1-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="764b1-607">949\.75</span></span>                                 |
| <span data-ttu-id="764b1-608">11</span><span class="sxs-lookup"><span data-stu-id="764b1-608">11</span></span>         | <span data-ttu-id="764b1-609">Kertynyt poisto</span><span class="sxs-lookup"><span data-stu-id="764b1-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="764b1-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="764b1-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="764b1-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="764b1-611">\-949\.75</span></span>                                      | <span data-ttu-id="764b1-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="764b1-612">\-949\.75</span></span>                               |


