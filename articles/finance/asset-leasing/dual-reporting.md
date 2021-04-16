---
title: Kaksoisraportointi
description: Tämä ohjeaihe sisältää esimerkin sekä International Financial Reporting Standard (IFRS) -raportoinnin että resurssin vuokrauksen lakisääteisen raportoinnin vaatimusten täyttämisestä.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: c9f2bae330e688e1e941277d46ddcbd38916f8c8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815977"
---
# <a name="dual-reporting"></a><span data-ttu-id="50dd3-103">Kaksoisraportointi</span><span class="sxs-lookup"><span data-stu-id="50dd3-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50dd3-104">Tämä ohjeaihe sisältää esimerkin sekä International Financial Reporting Standard (IFRS) -raportoinnin että resurssin vuokrauksen lakisääteisen raportoinnin vaatimusten täyttämisestä.</span><span class="sxs-lookup"><span data-stu-id="50dd3-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="50dd3-105">Vaatimuksena on Microsoft Dynamics 365 Financen kirjanpitotasojen käyttökokemus. Sen avulla esimerkki on helpompi ymmärtää.</span><span class="sxs-lookup"><span data-stu-id="50dd3-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="50dd3-106">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="50dd3-106">Example</span></span>

<span data-ttu-id="50dd3-107">Seuraavassa esimerkissä otetaan huomioon vuokraus Italian lakisääteisessä raportoinnissa käyttämällä sekä käteisvaroihin perustuvaa menetelmää että IFRS-raportointimenetelmiä.</span><span class="sxs-lookup"><span data-stu-id="50dd3-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="50dd3-108">Yrityksen on muodostettava kolme kirjaa, joiden avulla sekä Italian lakisääteiset vaatimukset että IFRS 16 -vaatimukset otetaan huomioon.</span><span class="sxs-lookup"><span data-stu-id="50dd3-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="50dd3-109">Yksi kirja vaaditaan IFRS 16:lle, toinen lakisääteisille vaatimuksille ja kolmas lakisääteisten kirjausten automaattista käänteistä kirjausta varten.</span><span class="sxs-lookup"><span data-stu-id="50dd3-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="50dd3-110">Kirjat määritetään seuraavissa taulukoissa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="50dd3-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="50dd3-111">**IFRS 16 -kirja**</span><span class="sxs-lookup"><span data-stu-id="50dd3-111">**IFRS 16 book**</span></span>

<span data-ttu-id="50dd3-112">IFRS 16 -kirja määritetään niin, että se on yhdenmukainen IFRS 16 -kirjanpitostandardin kanssa.</span><span class="sxs-lookup"><span data-stu-id="50dd3-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="50dd3-113">Kaikki tähän kirjaan kirjatut tapahtumat kirjataan mukautettuun tasoon.</span><span class="sxs-lookup"><span data-stu-id="50dd3-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="50dd3-114">Nimi</span><span class="sxs-lookup"><span data-stu-id="50dd3-114">Name</span></span>                                    | <span data-ttu-id="50dd3-115">kuvaus</span><span class="sxs-lookup"><span data-stu-id="50dd3-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="50dd3-116">Kirjan tyyppi</span><span class="sxs-lookup"><span data-stu-id="50dd3-116">Book type</span></span>                               | <span data-ttu-id="50dd3-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="50dd3-117">IFRS 16</span></span>        |
| <span data-ttu-id="50dd3-118">Kirjan kuvaus</span><span class="sxs-lookup"><span data-stu-id="50dd3-118">Book description</span></span>                        | <span data-ttu-id="50dd3-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="50dd3-119">IFRS 16</span></span>        |
| <span data-ttu-id="50dd3-120">Kirjanpitotaso</span><span class="sxs-lookup"><span data-stu-id="50dd3-120">Posting Layer</span></span>                           | <span data-ttu-id="50dd3-121">Mukautettu kerros 1</span><span class="sxs-lookup"><span data-stu-id="50dd3-121">Custom layer 1</span></span> |
| <span data-ttu-id="50dd3-122">Vuokran tyyppi</span><span class="sxs-lookup"><span data-stu-id="50dd3-122">Lease Type</span></span>                              | <span data-ttu-id="50dd3-123">Finance</span><span class="sxs-lookup"><span data-stu-id="50dd3-123">Finance</span></span>        |
| <span data-ttu-id="50dd3-124">Kirjanpitokehys</span><span class="sxs-lookup"><span data-stu-id="50dd3-124">Accounting Framework</span></span>                    | <span data-ttu-id="50dd3-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="50dd3-125">IFRS 16</span></span>        |
| <span data-ttu-id="50dd3-126">Vuokra-/käyttöajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="50dd3-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="50dd3-127">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-127">0.00</span></span>           |
| <span data-ttu-id="50dd3-128">Nykyinen arvo / resurssin käyvän arvon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="50dd3-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="50dd3-129">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-129">0.00</span></span>           |
| <span data-ttu-id="50dd3-130">Lyhytaikainen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="50dd3-130">Short-term threshold</span></span>                    | <span data-ttu-id="50dd3-131">12</span><span class="sxs-lookup"><span data-stu-id="50dd3-131">12</span></span>             |
| <span data-ttu-id="50dd3-132">Arvoltaan vähäinen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="50dd3-132">Low Value Threshold</span></span>                     | <span data-ttu-id="50dd3-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-133">5,000.00</span></span>       |
| <span data-ttu-id="50dd3-134">Maksu toimittajalle</span><span class="sxs-lookup"><span data-stu-id="50dd3-134">Pay to Vendor</span></span>                           | <span data-ttu-id="50dd3-135">Nro</span><span class="sxs-lookup"><span data-stu-id="50dd3-135">No</span></span>             |

<span data-ttu-id="50dd3-136">**Lakisääteinen kirja**</span><span class="sxs-lookup"><span data-stu-id="50dd3-136">**Statutory book**</span></span>

<span data-ttu-id="50dd3-137">Lakisääteinen kirja on käteisvaroihin perustuva kirja, jonne yritys kirjaa vuokrauksen kulut käteisvarojen summana, joka maksetaan joka kuukausi vuokrana.</span><span class="sxs-lookup"><span data-stu-id="50dd3-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="50dd3-138">Tämä kirja ei tuota käyttöoikeusomaisuuserää tai vuokrasopimusvelkaa.</span><span class="sxs-lookup"><span data-stu-id="50dd3-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="50dd3-139">Nimi</span><span class="sxs-lookup"><span data-stu-id="50dd3-139">Name</span></span>                                    | <span data-ttu-id="50dd3-140">kuvaus</span><span class="sxs-lookup"><span data-stu-id="50dd3-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="50dd3-141">Kirjan tyyppi</span><span class="sxs-lookup"><span data-stu-id="50dd3-141">Book type</span></span>                               | <span data-ttu-id="50dd3-142">Lakisääteinen</span><span class="sxs-lookup"><span data-stu-id="50dd3-142">Statutory</span></span>   |
| <span data-ttu-id="50dd3-143">Kirjan kuvaus</span><span class="sxs-lookup"><span data-stu-id="50dd3-143">Book description</span></span>                        | <span data-ttu-id="50dd3-144">Paikallinen GAAP</span><span class="sxs-lookup"><span data-stu-id="50dd3-144">Local GAAP</span></span>  |
| <span data-ttu-id="50dd3-145">Kirjanpitotaso</span><span class="sxs-lookup"><span data-stu-id="50dd3-145">Posting Layer</span></span>                           | <span data-ttu-id="50dd3-146">Valittu</span><span class="sxs-lookup"><span data-stu-id="50dd3-146">Current</span></span>     |
| <span data-ttu-id="50dd3-147">Vuokran tyyppi</span><span class="sxs-lookup"><span data-stu-id="50dd3-147">Lease Type</span></span>                              | <span data-ttu-id="50dd3-148">Automaattinen</span><span class="sxs-lookup"><span data-stu-id="50dd3-148">Automatic</span></span>   |
| <span data-ttu-id="50dd3-149">Kirjanpitokehys</span><span class="sxs-lookup"><span data-stu-id="50dd3-149">Accounting Framework</span></span>                    | <span data-ttu-id="50dd3-150">Maksuperuste</span><span class="sxs-lookup"><span data-stu-id="50dd3-150">Cash basis</span></span>  |
| <span data-ttu-id="50dd3-151">Vuokra-/käyttöajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="50dd3-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="50dd3-152">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-152">0.00</span></span>        |
| <span data-ttu-id="50dd3-153">Nykyinen arvo / resurssin käyvän arvon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="50dd3-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="50dd3-154">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-154">0.00</span></span>        |
| <span data-ttu-id="50dd3-155">Lyhytaikainen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="50dd3-155">Short-term threshold</span></span>                    | <span data-ttu-id="50dd3-156">0</span><span class="sxs-lookup"><span data-stu-id="50dd3-156">0</span></span>           |
| <span data-ttu-id="50dd3-157">Arvoltaan vähäinen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="50dd3-157">Low Value Threshold</span></span>                     | <span data-ttu-id="50dd3-158">0</span><span class="sxs-lookup"><span data-stu-id="50dd3-158">0</span></span>           |
| <span data-ttu-id="50dd3-159">Maksu toimittajalle</span><span class="sxs-lookup"><span data-stu-id="50dd3-159">Pay to Vendor</span></span>                           | <span data-ttu-id="50dd3-160">Nro</span><span class="sxs-lookup"><span data-stu-id="50dd3-160">No</span></span>          |

<span data-ttu-id="50dd3-161">**Lakisääteinen palautuskirja**</span><span class="sxs-lookup"><span data-stu-id="50dd3-161">**Statutory reversal book**</span></span>

<span data-ttu-id="50dd3-162">Lakisääteinen palautuskirja määritetään samalla tavalla kuin lakisääteinen kirja.</span><span class="sxs-lookup"><span data-stu-id="50dd3-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="50dd3-163">Nimi</span><span class="sxs-lookup"><span data-stu-id="50dd3-163">Name</span></span>                                    | <span data-ttu-id="50dd3-164">kuvaus</span><span class="sxs-lookup"><span data-stu-id="50dd3-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="50dd3-165">Kirjan tyyppi</span><span class="sxs-lookup"><span data-stu-id="50dd3-165">Book type</span></span>                               | <span data-ttu-id="50dd3-166">Lakisääteinen – palautus</span><span class="sxs-lookup"><span data-stu-id="50dd3-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="50dd3-167">Kirjan kuvaus</span><span class="sxs-lookup"><span data-stu-id="50dd3-167">Book description</span></span>                        | <span data-ttu-id="50dd3-168">Kirjaa käänteiseen lakisääteiseen kirjaan</span><span class="sxs-lookup"><span data-stu-id="50dd3-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="50dd3-169">Kirjanpitotaso</span><span class="sxs-lookup"><span data-stu-id="50dd3-169">Posting Layer</span></span>                           | <span data-ttu-id="50dd3-170">Mukautettu kerros 1</span><span class="sxs-lookup"><span data-stu-id="50dd3-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="50dd3-171">Vuokran tyyppi</span><span class="sxs-lookup"><span data-stu-id="50dd3-171">Lease Type</span></span>                              | <span data-ttu-id="50dd3-172">Automaattinen</span><span class="sxs-lookup"><span data-stu-id="50dd3-172">Automatic</span></span>                      |
| <span data-ttu-id="50dd3-173">Kirjanpitokehys</span><span class="sxs-lookup"><span data-stu-id="50dd3-173">Accounting Framework</span></span>                    | <span data-ttu-id="50dd3-174">Maksuperuste</span><span class="sxs-lookup"><span data-stu-id="50dd3-174">Cash basis</span></span>                     |
| <span data-ttu-id="50dd3-175">Vuokra-/käyttöajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="50dd3-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="50dd3-176">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-176">0.00</span></span>                           |
| <span data-ttu-id="50dd3-177">Nykyinen arvo / resurssin käyvän arvon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="50dd3-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="50dd3-178">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-178">0.00</span></span>                           |
| <span data-ttu-id="50dd3-179">Lyhytaikainen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="50dd3-179">Short-term threshold</span></span>                    | <span data-ttu-id="50dd3-180">0</span><span class="sxs-lookup"><span data-stu-id="50dd3-180">0</span></span>                              |
| <span data-ttu-id="50dd3-181">Arvoltaan vähäinen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="50dd3-181">Low Value Threshold</span></span>                     | <span data-ttu-id="50dd3-182">0</span><span class="sxs-lookup"><span data-stu-id="50dd3-182">0</span></span>                              |
| <span data-ttu-id="50dd3-183">Maksu toimittajalle</span><span class="sxs-lookup"><span data-stu-id="50dd3-183">Pay to Vendor</span></span>                           | <span data-ttu-id="50dd3-184">Nro</span><span class="sxs-lookup"><span data-stu-id="50dd3-184">No</span></span>                             |

<span data-ttu-id="50dd3-185">Tässä esimerkissä on luotu vuokraus, jolla on seuraavat asetukset **Yleistä**- ja **Maksuaikataulurivit**-välilehdissä.</span><span class="sxs-lookup"><span data-stu-id="50dd3-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="50dd3-186">**Yleinen-välilehti**</span><span class="sxs-lookup"><span data-stu-id="50dd3-186">**General tab**</span></span>

| <span data-ttu-id="50dd3-187">Kenttä</span><span class="sxs-lookup"><span data-stu-id="50dd3-187">Field</span></span>                      | <span data-ttu-id="50dd3-188">Arvo</span><span class="sxs-lookup"><span data-stu-id="50dd3-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="50dd3-189">Inkrementaalinen lainakorko</span><span class="sxs-lookup"><span data-stu-id="50dd3-189">Incremental borrowing rate</span></span> | <span data-ttu-id="50dd3-190">5 %</span><span class="sxs-lookup"><span data-stu-id="50dd3-190">5%</span></span>               |
| <span data-ttu-id="50dd3-191">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="50dd3-191">Commencement date</span></span>          | <span data-ttu-id="50dd3-192">1.1.2020</span><span class="sxs-lookup"><span data-stu-id="50dd3-192">1/1/2020</span></span>         |
| <span data-ttu-id="50dd3-193">Vuokraryhmä</span><span class="sxs-lookup"><span data-stu-id="50dd3-193">Lease group</span></span>                | <span data-ttu-id="50dd3-194">Rakennukset</span><span class="sxs-lookup"><span data-stu-id="50dd3-194">Buildings</span></span>        |
| <span data-ttu-id="50dd3-195">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="50dd3-195">Vendor</span></span>                     | <span data-ttu-id="50dd3-196">1001</span><span class="sxs-lookup"><span data-stu-id="50dd3-196">1001</span></span>             |
| <span data-ttu-id="50dd3-197">Resurssin käypä arvo</span><span class="sxs-lookup"><span data-stu-id="50dd3-197">Fair value of the asset</span></span>    | <span data-ttu-id="50dd3-198">245,000</span><span class="sxs-lookup"><span data-stu-id="50dd3-198">245,000</span></span>          |
| <span data-ttu-id="50dd3-199">Käyttöomaisuuden käyttöikä</span><span class="sxs-lookup"><span data-stu-id="50dd3-199">Asset useful life</span></span>          | <span data-ttu-id="50dd3-200">120</span><span class="sxs-lookup"><span data-stu-id="50dd3-200">120</span></span>              |
| <span data-ttu-id="50dd3-201">Annuiteetin tyyppi</span><span class="sxs-lookup"><span data-stu-id="50dd3-201">Annuity type</span></span>               | <span data-ttu-id="50dd3-202">Tavallinen annuiteetti</span><span class="sxs-lookup"><span data-stu-id="50dd3-202">Ordinary annuity</span></span> |
| <span data-ttu-id="50dd3-203">Yhdistämisväli</span><span class="sxs-lookup"><span data-stu-id="50dd3-203">Compounding interval</span></span>       | <span data-ttu-id="50dd3-204">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="50dd3-204">Monthly</span></span>          |

<span data-ttu-id="50dd3-205">**Maksusuunnitelmarivit-välilehti**</span><span class="sxs-lookup"><span data-stu-id="50dd3-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="50dd3-206">Kenttä</span><span class="sxs-lookup"><span data-stu-id="50dd3-206">Field</span></span>             | <span data-ttu-id="50dd3-207">Arvo</span><span class="sxs-lookup"><span data-stu-id="50dd3-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="50dd3-208">Aloituspäivä</span><span class="sxs-lookup"><span data-stu-id="50dd3-208">Start date</span></span>        | <span data-ttu-id="50dd3-209">1.1.2020</span><span class="sxs-lookup"><span data-stu-id="50dd3-209">1/1/2020</span></span>   |
| <span data-ttu-id="50dd3-210">Kausiväli</span><span class="sxs-lookup"><span data-stu-id="50dd3-210">Period interval</span></span>   | <span data-ttu-id="50dd3-211">Kuukautta</span><span class="sxs-lookup"><span data-stu-id="50dd3-211">Months</span></span>     |
| <span data-ttu-id="50dd3-212">Kaudet</span><span class="sxs-lookup"><span data-stu-id="50dd3-212">Periods</span></span>           | <span data-ttu-id="50dd3-213">24</span><span class="sxs-lookup"><span data-stu-id="50dd3-213">24</span></span>         |
| <span data-ttu-id="50dd3-214">Päättymispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="50dd3-214">End date</span></span>          | <span data-ttu-id="50dd3-215">31.12.2020</span><span class="sxs-lookup"><span data-stu-id="50dd3-215">12/31/2020</span></span> |
| <span data-ttu-id="50dd3-216">Maksun toistuvuus</span><span class="sxs-lookup"><span data-stu-id="50dd3-216">Payment frequency</span></span> | <span data-ttu-id="50dd3-217">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="50dd3-217">Monthly</span></span>    |
| <span data-ttu-id="50dd3-218">Maksun summa</span><span class="sxs-lookup"><span data-stu-id="50dd3-218">Payment amount</span></span>    | <span data-ttu-id="50dd3-219">1 000</span><span class="sxs-lookup"><span data-stu-id="50dd3-219">1,000</span></span>      |

<span data-ttu-id="50dd3-220">Jotta tämä vuokraus voidaan ottaa huomioon kahdessa kehyksessä, käytetään sekä nykyistä että mukautettua kirjaustasoa.</span><span class="sxs-lookup"><span data-stu-id="50dd3-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="50dd3-221">Seuraavassa taulukossa on esimerkki jokaisesta kirjauskansiomerkinnästä, joka vaaditaan vastaamaan tasapuolisesti kunkin raportointistandardin mukaisia taloustietoja.</span><span class="sxs-lookup"><span data-stu-id="50dd3-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="50dd3-222">Kunkin vuokrauksen ensimmäisen kuukauden kirjauskansiomerkinnän yksityiskohtainen kuvaus annetaan jälkikäteen.</span><span class="sxs-lookup"><span data-stu-id="50dd3-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="50dd3-223">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="50dd3-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="50dd3-224">kuvaus</span><span class="sxs-lookup"><span data-stu-id="50dd3-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="50dd3-225">Lakisääteinen kirja (nykyinen taso)</span><span class="sxs-lookup"><span data-stu-id="50dd3-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="50dd3-226">Nykyinen taso yhteensä</span><span class="sxs-lookup"><span data-stu-id="50dd3-226">Current layer total</span></span></th>
<th><span data-ttu-id="50dd3-227">Palautuskirja (mukautettu taso)</span><span class="sxs-lookup"><span data-stu-id="50dd3-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="50dd3-228">IFRS 16 -kirja (mukautettu taso)</span><span class="sxs-lookup"><span data-stu-id="50dd3-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="50dd3-229">Nykyinen taso + mukautettu taso yhteensä</span><span class="sxs-lookup"><span data-stu-id="50dd3-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="50dd3-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="50dd3-230">JE-100</span></span></th>
<th><span data-ttu-id="50dd3-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="50dd3-231">JE-110</span></span></th>
<th><span data-ttu-id="50dd3-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="50dd3-232">JE-120</span></span></th>
<th><span data-ttu-id="50dd3-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="50dd3-233">JE-130</span></span></th>
<th><span data-ttu-id="50dd3-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="50dd3-234">JE-140</span></span></th>
<th><span data-ttu-id="50dd3-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="50dd3-235">JE-150</span></span></th>
<th><span data-ttu-id="50dd3-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="50dd3-236">JE-160</span></span></th>
<th><span data-ttu-id="50dd3-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="50dd3-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="50dd3-238">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="50dd3-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="50dd3-239">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="50dd3-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="50dd3-240">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="50dd3-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="50dd3-241">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="50dd3-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="50dd3-242">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="50dd3-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="50dd3-243">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="50dd3-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="50dd3-244">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="50dd3-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="50dd3-245">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="50dd3-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="50dd3-246">1</span><span class="sxs-lookup"><span data-stu-id="50dd3-246">1</span></span></td>
<td><span data-ttu-id="50dd3-247">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="50dd3-247">Lease expense</span></span></td>
<td><span data-ttu-id="50dd3-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-249">1,000.00</span></span></td>
<td><span data-ttu-id="50dd3-250">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-251">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50dd3-252">2</span><span class="sxs-lookup"><span data-stu-id="50dd3-252">2</span></span></td>
<td><span data-ttu-id="50dd3-253">Pankkikulu</span><span class="sxs-lookup"><span data-stu-id="50dd3-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="50dd3-254">3.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="50dd3-255">3.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-256">3.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50dd3-257">3</span><span class="sxs-lookup"><span data-stu-id="50dd3-257">3</span></span></td>
<td><span data-ttu-id="50dd3-258">ALV-kulu</span><span class="sxs-lookup"><span data-stu-id="50dd3-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="50dd3-259">5.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="50dd3-260">5.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-261">5.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50dd3-262">4</span><span class="sxs-lookup"><span data-stu-id="50dd3-262">4</span></span></td>
<td><span data-ttu-id="50dd3-263">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="50dd3-263">Clearing account</span></span></td>
<td><span data-ttu-id="50dd3-264">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-264">-1,000.00</span></span></td>
<td><span data-ttu-id="50dd3-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="50dd3-266">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-266">0.00</span></span></td>
<td><span data-ttu-id="50dd3-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="50dd3-268">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-269">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50dd3-270">5</span><span class="sxs-lookup"><span data-stu-id="50dd3-270">5</span></span></td>
<td><span data-ttu-id="50dd3-271">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="50dd3-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="50dd3-272">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-272">-1,008.00</span></span></td>
<td><span data-ttu-id="50dd3-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-273">1,008.00</span></span></td>
<td><span data-ttu-id="50dd3-274">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-275">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50dd3-276">6</span><span class="sxs-lookup"><span data-stu-id="50dd3-276">6</span></span></td>
<td><span data-ttu-id="50dd3-277">Käyttöoikeusomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="50dd3-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-278">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="50dd3-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="50dd3-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50dd3-281">7</span><span class="sxs-lookup"><span data-stu-id="50dd3-281">7</span></span></td>
<td><span data-ttu-id="50dd3-282">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="50dd3-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-283">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="50dd3-284">-22 794,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-284">-22,794.00</span></span></td>
<td><span data-ttu-id="50dd3-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-285">1,000.00</span></span></td>
<td><span data-ttu-id="50dd3-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="50dd3-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="50dd3-287">-21 888,87</span><span class="sxs-lookup"><span data-stu-id="50dd3-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50dd3-288">8</span><span class="sxs-lookup"><span data-stu-id="50dd3-288">8</span></span></td>
<td><span data-ttu-id="50dd3-289">Korkokustannus</span><span class="sxs-lookup"><span data-stu-id="50dd3-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-290">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-291">94.97</span><span class="sxs-lookup"><span data-stu-id="50dd3-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="50dd3-292">94.97</span><span class="sxs-lookup"><span data-stu-id="50dd3-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50dd3-293">9</span><span class="sxs-lookup"><span data-stu-id="50dd3-293">9</span></span></td>
<td><span data-ttu-id="50dd3-294">Maksu</span><span class="sxs-lookup"><span data-stu-id="50dd3-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-295">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-295">-1,008.00</span></span></td>
<td><span data-ttu-id="50dd3-296">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-297">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50dd3-298">10</span><span class="sxs-lookup"><span data-stu-id="50dd3-298">10</span></span></td>
<td><span data-ttu-id="50dd3-299">Poistokulu</span><span class="sxs-lookup"><span data-stu-id="50dd3-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-300">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-301">949.75</span><span class="sxs-lookup"><span data-stu-id="50dd3-301">949.75</span></span></td>
<td><span data-ttu-id="50dd3-302">949.75</span><span class="sxs-lookup"><span data-stu-id="50dd3-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50dd3-303">11</span><span class="sxs-lookup"><span data-stu-id="50dd3-303">11</span></span></td>
<td><span data-ttu-id="50dd3-304">Kertynyt poisto</span><span class="sxs-lookup"><span data-stu-id="50dd3-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-305">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="50dd3-306">-949.75</span></span></td>
<td><span data-ttu-id="50dd3-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="50dd3-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="50dd3-308">Kuten edellä olevasta taulukosta ilmenee, sekä lakisääteinen raportointi että IFRS-raportointi edellyttävät kolmen kirjan käyttämistä.</span><span class="sxs-lookup"><span data-stu-id="50dd3-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="50dd3-309">Lakisääteinen kirja tallentaa vuokrat nykyisen tason käteisvaroihin perustuvan kirjanpidon sääntöjen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="50dd3-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="50dd3-310">Lakisääteinen palautuskirja kumoaa lakisääteiset kirjauskansiomerkinnät.</span><span class="sxs-lookup"><span data-stu-id="50dd3-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="50dd3-311">IFRS 16 -kirja luo IFRS 16:n pakolliset kirjauskansiomerkinnät.</span><span class="sxs-lookup"><span data-stu-id="50dd3-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="50dd3-312">Sinun on syötettävä vuokraus vain kerran.</span><span class="sxs-lookup"><span data-stu-id="50dd3-312">You must enter a lease only one time.</span></span> <span data-ttu-id="50dd3-313">Tämän jälkeen voit avata **Kirjat**-sivun, ja näet kaikki vuokraukseen liittyvät kirjat.</span><span class="sxs-lookup"><span data-stu-id="50dd3-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="50dd3-314">Kun luot kirjoja, kaikkien kolmen on liityttävä samaan vuokraustietueeseen.</span><span class="sxs-lookup"><span data-stu-id="50dd3-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="50dd3-315">Ensimmäinen kirjauskansiomerkintä tallentaa vuokrauksen lakisääteiseen kirjaan.</span><span class="sxs-lookup"><span data-stu-id="50dd3-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="50dd3-316">Voit luoda maksut eränä tai valitsemalla maksusuunnitelman lakisääteisestä kirjasta.</span><span class="sxs-lookup"><span data-stu-id="50dd3-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="50dd3-317">Tässä esimerkissä maksusuunnitelmasta luodaan seuraava kirjauskansiomerkintä lakisääteistä kirjaa varten.</span><span class="sxs-lookup"><span data-stu-id="50dd3-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="50dd3-318">Vuokra – 31.1.2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="50dd3-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="50dd3-319">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="50dd3-319">Account type</span></span> | <span data-ttu-id="50dd3-320">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="50dd3-320">Account number</span></span> | <span data-ttu-id="50dd3-321">Taso</span><span class="sxs-lookup"><span data-stu-id="50dd3-321">Layer</span></span>   | <span data-ttu-id="50dd3-322">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="50dd3-322">Account description</span></span> | <span data-ttu-id="50dd3-323">Veloitus</span><span class="sxs-lookup"><span data-stu-id="50dd3-323">Debit</span></span>    | <span data-ttu-id="50dd3-324">Luotto</span><span class="sxs-lookup"><span data-stu-id="50dd3-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="50dd3-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="50dd3-325">Ledger</span></span>       | <span data-ttu-id="50dd3-326">1</span><span class="sxs-lookup"><span data-stu-id="50dd3-326">1</span></span>              | <span data-ttu-id="50dd3-327">Valittu</span><span class="sxs-lookup"><span data-stu-id="50dd3-327">Current</span></span> | <span data-ttu-id="50dd3-328">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="50dd3-328">Lease expense</span></span>       | <span data-ttu-id="50dd3-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-329">1,000.00</span></span> |          |
| <span data-ttu-id="50dd3-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="50dd3-330">Ledger</span></span>       | <span data-ttu-id="50dd3-331">4</span><span class="sxs-lookup"><span data-stu-id="50dd3-331">4</span></span>              | <span data-ttu-id="50dd3-332">Valittu</span><span class="sxs-lookup"><span data-stu-id="50dd3-332">Current</span></span> | <span data-ttu-id="50dd3-333">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="50dd3-333">Clearing account</span></span>    |          | <span data-ttu-id="50dd3-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-334">1,000.00</span></span> |

<span data-ttu-id="50dd3-335">Ostoreskontran käsittelijä käyttää Dynamics 365:n vakiotoimintoa luodessaan resurssin vuokrauksen ulkopuoliselle vuokraukselle laskun maksamista varten.</span><span class="sxs-lookup"><span data-stu-id="50dd3-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="50dd3-336">Sen sijaan, että debettiliksi valittaisiin **Vuokran kulu** ostoreskontran käsittelijä valitsee selvitystilin seuraavan merkinnän luomiseksi.</span><span class="sxs-lookup"><span data-stu-id="50dd3-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="50dd3-337">Ostoreskontran prosessi – 31.1.2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="50dd3-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="50dd3-338">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="50dd3-338">Account type</span></span> | <span data-ttu-id="50dd3-339">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="50dd3-339">Account number</span></span> | <span data-ttu-id="50dd3-340">Taso</span><span class="sxs-lookup"><span data-stu-id="50dd3-340">Layer</span></span>   | <span data-ttu-id="50dd3-341">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="50dd3-341">Account description</span></span> | <span data-ttu-id="50dd3-342">Veloitus</span><span class="sxs-lookup"><span data-stu-id="50dd3-342">Debit</span></span>    | <span data-ttu-id="50dd3-343">Luotto</span><span class="sxs-lookup"><span data-stu-id="50dd3-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="50dd3-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="50dd3-344">Ledger</span></span>       | <span data-ttu-id="50dd3-345">4</span><span class="sxs-lookup"><span data-stu-id="50dd3-345">4</span></span>              | <span data-ttu-id="50dd3-346">Valittu</span><span class="sxs-lookup"><span data-stu-id="50dd3-346">Current</span></span> | <span data-ttu-id="50dd3-347">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="50dd3-347">Clearing account</span></span>    | <span data-ttu-id="50dd3-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-348">1,000.00</span></span> |          |
| <span data-ttu-id="50dd3-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="50dd3-349">Ledger</span></span>       | <span data-ttu-id="50dd3-350">2</span><span class="sxs-lookup"><span data-stu-id="50dd3-350">2</span></span>              | <span data-ttu-id="50dd3-351">Valittu</span><span class="sxs-lookup"><span data-stu-id="50dd3-351">Current</span></span> | <span data-ttu-id="50dd3-352">Pankkikulu</span><span class="sxs-lookup"><span data-stu-id="50dd3-352">Bank fee</span></span>            | <span data-ttu-id="50dd3-353">3.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-353">3.00</span></span>     |          |
| <span data-ttu-id="50dd3-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="50dd3-354">Ledger</span></span>       | <span data-ttu-id="50dd3-355">3</span><span class="sxs-lookup"><span data-stu-id="50dd3-355">3</span></span>              | <span data-ttu-id="50dd3-356">Valittu</span><span class="sxs-lookup"><span data-stu-id="50dd3-356">Current</span></span> | <span data-ttu-id="50dd3-357">ALV-kulu</span><span class="sxs-lookup"><span data-stu-id="50dd3-357">VAT expense</span></span>         | <span data-ttu-id="50dd3-358">5.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-358">5.00</span></span>     |          |
| <span data-ttu-id="50dd3-359">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="50dd3-359">Vendor</span></span>       | <span data-ttu-id="50dd3-360">5</span><span class="sxs-lookup"><span data-stu-id="50dd3-360">5</span></span>              | <span data-ttu-id="50dd3-361">Valittu</span><span class="sxs-lookup"><span data-stu-id="50dd3-361">Current</span></span> | <span data-ttu-id="50dd3-362">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="50dd3-362">Accounts payable</span></span>    |          | <span data-ttu-id="50dd3-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-363">1,008.00</span></span> |

<span data-ttu-id="50dd3-364">Kun toimittajalle annetaan ilmoitus, seuraat säännöllistä maksuprosessia.</span><span class="sxs-lookup"><span data-stu-id="50dd3-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="50dd3-365">Tämän prosessin aikana luodaan seuraava kirjauskansiomerkintä.</span><span class="sxs-lookup"><span data-stu-id="50dd3-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="50dd3-366">Käteismaksu – 31.1.2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="50dd3-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="50dd3-367">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="50dd3-367">Account type</span></span> | <span data-ttu-id="50dd3-368">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="50dd3-368">Account number</span></span> | <span data-ttu-id="50dd3-369">Taso</span><span class="sxs-lookup"><span data-stu-id="50dd3-369">Layer</span></span>   | <span data-ttu-id="50dd3-370">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="50dd3-370">Account description</span></span> | <span data-ttu-id="50dd3-371">Veloitus</span><span class="sxs-lookup"><span data-stu-id="50dd3-371">Debit</span></span>    | <span data-ttu-id="50dd3-372">Luotto</span><span class="sxs-lookup"><span data-stu-id="50dd3-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="50dd3-373">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="50dd3-373">Vendor</span></span>       | <span data-ttu-id="50dd3-374">5</span><span class="sxs-lookup"><span data-stu-id="50dd3-374">5</span></span>              | <span data-ttu-id="50dd3-375">Valittu</span><span class="sxs-lookup"><span data-stu-id="50dd3-375">Current</span></span> | <span data-ttu-id="50dd3-376">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="50dd3-376">Accounts Payable</span></span>    | <span data-ttu-id="50dd3-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-377">1,008.00</span></span> |          |
| <span data-ttu-id="50dd3-378">Pankki</span><span class="sxs-lookup"><span data-stu-id="50dd3-378">Bank</span></span>         | <span data-ttu-id="50dd3-379">9</span><span class="sxs-lookup"><span data-stu-id="50dd3-379">9</span></span>              | <span data-ttu-id="50dd3-380">Valittu</span><span class="sxs-lookup"><span data-stu-id="50dd3-380">Current</span></span> | <span data-ttu-id="50dd3-381">Maksu</span><span class="sxs-lookup"><span data-stu-id="50dd3-381">Cash</span></span>                |          | <span data-ttu-id="50dd3-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-382">1,008.00</span></span> |

<span data-ttu-id="50dd3-383">Nyt tämä vuokraus on otettu kokonaan huomioon lakisääteisen raportoinnin vaatimusten mukaisesti, ja voit luoda pääkirjan nykyisen tason mukaan.</span><span class="sxs-lookup"><span data-stu-id="50dd3-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="50dd3-384">Järjestelmä palauttaa pääkirjan, jossa ovat seuraavat luvut.</span><span class="sxs-lookup"><span data-stu-id="50dd3-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="50dd3-385">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="50dd3-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="50dd3-386">kuvaus</span><span class="sxs-lookup"><span data-stu-id="50dd3-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="50dd3-387">Lakisääteinen kirja (nykyinen taso)</span><span class="sxs-lookup"><span data-stu-id="50dd3-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="50dd3-388">Nykyinen taso yhteensä</span><span class="sxs-lookup"><span data-stu-id="50dd3-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="50dd3-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="50dd3-389">JE-100</span></span></th>
<th><span data-ttu-id="50dd3-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="50dd3-390">JE-110</span></span></th>
<th><span data-ttu-id="50dd3-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="50dd3-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="50dd3-392">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="50dd3-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="50dd3-393">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="50dd3-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="50dd3-394">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="50dd3-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="50dd3-395">1</span><span class="sxs-lookup"><span data-stu-id="50dd3-395">1</span></span></td>
<td><span data-ttu-id="50dd3-396">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="50dd3-396">Lease expense</span></span></td>
<td><span data-ttu-id="50dd3-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50dd3-399">2</span><span class="sxs-lookup"><span data-stu-id="50dd3-399">2</span></span></td>
<td><span data-ttu-id="50dd3-400">Pankkikulu</span><span class="sxs-lookup"><span data-stu-id="50dd3-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="50dd3-401">3.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="50dd3-402">3.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50dd3-403">3</span><span class="sxs-lookup"><span data-stu-id="50dd3-403">3</span></span></td>
<td><span data-ttu-id="50dd3-404">ALV-kulu</span><span class="sxs-lookup"><span data-stu-id="50dd3-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="50dd3-405">5.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="50dd3-406">5.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50dd3-407">4</span><span class="sxs-lookup"><span data-stu-id="50dd3-407">4</span></span></td>
<td><span data-ttu-id="50dd3-408">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="50dd3-408">Clearing account</span></span></td>
<td><span data-ttu-id="50dd3-409">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-409">-1,000.00</span></span></td>
<td><span data-ttu-id="50dd3-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="50dd3-411">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50dd3-412">5</span><span class="sxs-lookup"><span data-stu-id="50dd3-412">5</span></span></td>
<td><span data-ttu-id="50dd3-413">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="50dd3-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="50dd3-414">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-414">-1,008.00</span></span></td>
<td><span data-ttu-id="50dd3-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-415">1,008.00</span></span></td>
<td><span data-ttu-id="50dd3-416">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50dd3-417">6</span><span class="sxs-lookup"><span data-stu-id="50dd3-417">6</span></span></td>
<td><span data-ttu-id="50dd3-418">Käyttöoikeusomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="50dd3-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-419">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50dd3-420">7</span><span class="sxs-lookup"><span data-stu-id="50dd3-420">7</span></span></td>
<td><span data-ttu-id="50dd3-421">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="50dd3-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-422">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50dd3-423">8</span><span class="sxs-lookup"><span data-stu-id="50dd3-423">8</span></span></td>
<td><span data-ttu-id="50dd3-424">Korkokustannus</span><span class="sxs-lookup"><span data-stu-id="50dd3-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-425">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50dd3-426">9</span><span class="sxs-lookup"><span data-stu-id="50dd3-426">9</span></span></td>
<td><span data-ttu-id="50dd3-427">Maksu</span><span class="sxs-lookup"><span data-stu-id="50dd3-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-428">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-428">-1,008.00</span></span></td>
<td><span data-ttu-id="50dd3-429">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50dd3-430">10</span><span class="sxs-lookup"><span data-stu-id="50dd3-430">10</span></span></td>
<td><span data-ttu-id="50dd3-431">Poistokulu</span><span class="sxs-lookup"><span data-stu-id="50dd3-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-432">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50dd3-433">11</span><span class="sxs-lookup"><span data-stu-id="50dd3-433">11</span></span></td>
<td><span data-ttu-id="50dd3-434">Kertynyt poisto</span><span class="sxs-lookup"><span data-stu-id="50dd3-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="50dd3-435">0,00</span><span class="sxs-lookup"><span data-stu-id="50dd3-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="50dd3-436">Jos haluat käyttää IFRS 16 -lukuja ja suorittaa saman pääkirjan, lakisääteisen kirjapidon kirjauskansioviennit on palautettava ja IFRS 16 -kirjauskansioviennit kirjattava.</span><span class="sxs-lookup"><span data-stu-id="50dd3-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="50dd3-437">Tässä esimerkissä on myös lakisääteinen palautuskirja siltä varalta, että haluat palauttaa lakisääteiset kirjauskansioviennit. Palautuskirjassa on samat asetukset kuin lakisääteisessä kirjassa, mutta vastakkainen kirjausprofiili.</span><span class="sxs-lookup"><span data-stu-id="50dd3-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="50dd3-438">Esimerkiksi lakisääteinen kirja *veloitti* vuokrauksen kulutilin, mutta palautuskirja *hyvittää* tämän tilin.</span><span class="sxs-lookup"><span data-stu-id="50dd3-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="50dd3-439">Nämä suhteet on helppo määrittää resurssin vuokrauksen kirjaustileillä **Resurssin vuokrauksen parametrit** -sivulla (**Resurssin vuokraus \> Asetukset \> Resurssin vuokrauksen parametrit**).</span><span class="sxs-lookup"><span data-stu-id="50dd3-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="50dd3-440">Kun lakisääteisessä kirjassa käytettyä prosessia käytetään palautuskirjassa, luodaan seuraava kirjauskansiovienti.</span><span class="sxs-lookup"><span data-stu-id="50dd3-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="50dd3-441">Erona on se, että palautuskirja kirjaa vastakirjaukset lakisääteisestä kirjasta.</span><span class="sxs-lookup"><span data-stu-id="50dd3-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="50dd3-442">Vastakirjaukset tehdään myös mukautetussa tasossa.</span><span class="sxs-lookup"><span data-stu-id="50dd3-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="50dd3-443">Kun pääkirja suoritetaan nykyisellä tasolla, palautuskirjauskansiovientejä ei sisällytetä.</span><span class="sxs-lookup"><span data-stu-id="50dd3-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="50dd3-444">Vuokra – 31.1.2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="50dd3-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="50dd3-445">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="50dd3-445">Account type</span></span> | <span data-ttu-id="50dd3-446">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="50dd3-446">Account number</span></span> | <span data-ttu-id="50dd3-447">Taso</span><span class="sxs-lookup"><span data-stu-id="50dd3-447">Layer</span></span>  | <span data-ttu-id="50dd3-448">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="50dd3-448">Account description</span></span> | <span data-ttu-id="50dd3-449">Veloitus</span><span class="sxs-lookup"><span data-stu-id="50dd3-449">Debit</span></span>    | <span data-ttu-id="50dd3-450">Luotto</span><span class="sxs-lookup"><span data-stu-id="50dd3-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="50dd3-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="50dd3-451">Ledger</span></span>       | <span data-ttu-id="50dd3-452">4</span><span class="sxs-lookup"><span data-stu-id="50dd3-452">4</span></span>              | <span data-ttu-id="50dd3-453">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="50dd3-453">Custom</span></span> | <span data-ttu-id="50dd3-454">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="50dd3-454">Clearing account</span></span>    | <span data-ttu-id="50dd3-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-455">1,000.00</span></span> |          |
| <span data-ttu-id="50dd3-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="50dd3-456">Ledger</span></span>       | <span data-ttu-id="50dd3-457">1</span><span class="sxs-lookup"><span data-stu-id="50dd3-457">1</span></span>              | <span data-ttu-id="50dd3-458">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="50dd3-458">Custom</span></span> | <span data-ttu-id="50dd3-459">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="50dd3-459">Lease expense</span></span>       |          | <span data-ttu-id="50dd3-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-460">1,000.00</span></span> |

<span data-ttu-id="50dd3-461">Nyt lakisääteiset kirjauskansioviennit on eliminoitu, ja voit kirjata kaikki IFRS 16:n edellyttämät kirjauskansioviennit IFRS 16 -kirjaan.</span><span class="sxs-lookup"><span data-stu-id="50dd3-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="50dd3-462">Nämä viennit sisältävät käyttöoikeusomaisuuserän ja velan alkuperäisen kirjauksen sekä koron ja poiston tietueen.</span><span class="sxs-lookup"><span data-stu-id="50dd3-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="50dd3-463">Alkuperäinen kirjaus – 1.1.2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="50dd3-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="50dd3-464">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="50dd3-464">Account type</span></span> | <span data-ttu-id="50dd3-465">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="50dd3-465">Account number</span></span> | <span data-ttu-id="50dd3-466">Taso</span><span class="sxs-lookup"><span data-stu-id="50dd3-466">Layer</span></span>  | <span data-ttu-id="50dd3-467">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="50dd3-467">Account description</span></span>      | <span data-ttu-id="50dd3-468">Veloitus</span><span class="sxs-lookup"><span data-stu-id="50dd3-468">Debit</span></span>     | <span data-ttu-id="50dd3-469">Luotto</span><span class="sxs-lookup"><span data-stu-id="50dd3-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="50dd3-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="50dd3-470">Ledger</span></span>       | <span data-ttu-id="50dd3-471">6</span><span class="sxs-lookup"><span data-stu-id="50dd3-471">6</span></span>              | <span data-ttu-id="50dd3-472">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="50dd3-472">Custom</span></span> | <span data-ttu-id="50dd3-473">Käyttöoikeusomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="50dd3-473">ROU Asset</span></span>                | <span data-ttu-id="50dd3-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="50dd3-474">22,793.90</span></span> |           |
| <span data-ttu-id="50dd3-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="50dd3-475">Ledger</span></span>       | <span data-ttu-id="50dd3-476">7</span><span class="sxs-lookup"><span data-stu-id="50dd3-476">7</span></span>              | <span data-ttu-id="50dd3-477">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="50dd3-477">Custom</span></span> | <span data-ttu-id="50dd3-478">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="50dd3-478">Finance lease obligation</span></span> |           | <span data-ttu-id="50dd3-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="50dd3-479">22,793.90</span></span> |

<span data-ttu-id="50dd3-480">Vuokra kirjataan kuten muut vuokrat.</span><span class="sxs-lookup"><span data-stu-id="50dd3-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="50dd3-481">Selvitystiliä käytetään, jotta voidaan varmistaa käteisen hyvitys vain kerran.</span><span class="sxs-lookup"><span data-stu-id="50dd3-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="50dd3-482">Vuokra – 31.1.2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="50dd3-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="50dd3-483">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="50dd3-483">Account type</span></span> | <span data-ttu-id="50dd3-484">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="50dd3-484">Account number</span></span> | <span data-ttu-id="50dd3-485">Taso</span><span class="sxs-lookup"><span data-stu-id="50dd3-485">Layer</span></span>  | <span data-ttu-id="50dd3-486">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="50dd3-486">Account description</span></span>      | <span data-ttu-id="50dd3-487">Veloitus</span><span class="sxs-lookup"><span data-stu-id="50dd3-487">Debit</span></span>    | <span data-ttu-id="50dd3-488">Luotto</span><span class="sxs-lookup"><span data-stu-id="50dd3-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="50dd3-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="50dd3-489">Ledger</span></span>       | <span data-ttu-id="50dd3-490">7</span><span class="sxs-lookup"><span data-stu-id="50dd3-490">7</span></span>              | <span data-ttu-id="50dd3-491">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="50dd3-491">Custom</span></span> | <span data-ttu-id="50dd3-492">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="50dd3-492">Finance lease obligation</span></span> | <span data-ttu-id="50dd3-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-493">1,000.00</span></span> |          |
| <span data-ttu-id="50dd3-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="50dd3-494">Ledger</span></span>       | <span data-ttu-id="50dd3-495">4</span><span class="sxs-lookup"><span data-stu-id="50dd3-495">4</span></span>              | <span data-ttu-id="50dd3-496">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="50dd3-496">Custom</span></span> | <span data-ttu-id="50dd3-497">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="50dd3-497">Clearing account</span></span>         |          | <span data-ttu-id="50dd3-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-498">1,000.00</span></span> |

<span data-ttu-id="50dd3-499">Korkokulun kirjauskansiovienti luodaan velan kuoletusaikataulusta.</span><span class="sxs-lookup"><span data-stu-id="50dd3-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="50dd3-500">Korkokustannus – 31.1.2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="50dd3-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="50dd3-501">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="50dd3-501">Account type</span></span> | <span data-ttu-id="50dd3-502">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="50dd3-502">Account number</span></span> | <span data-ttu-id="50dd3-503">Taso</span><span class="sxs-lookup"><span data-stu-id="50dd3-503">Layer</span></span>  | <span data-ttu-id="50dd3-504">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="50dd3-504">Account description</span></span>      | <span data-ttu-id="50dd3-505">Veloitus</span><span class="sxs-lookup"><span data-stu-id="50dd3-505">Debit</span></span> | <span data-ttu-id="50dd3-506">Luotto</span><span class="sxs-lookup"><span data-stu-id="50dd3-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="50dd3-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="50dd3-507">Ledger</span></span>       | <span data-ttu-id="50dd3-508">8</span><span class="sxs-lookup"><span data-stu-id="50dd3-508">8</span></span>              | <span data-ttu-id="50dd3-509">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="50dd3-509">Custom</span></span> | <span data-ttu-id="50dd3-510">Korkokustannus</span><span class="sxs-lookup"><span data-stu-id="50dd3-510">Interest expense</span></span>         | <span data-ttu-id="50dd3-511">94.97</span><span class="sxs-lookup"><span data-stu-id="50dd3-511">94.97</span></span> |        |
| <span data-ttu-id="50dd3-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="50dd3-512">Ledger</span></span>       | <span data-ttu-id="50dd3-513">7</span><span class="sxs-lookup"><span data-stu-id="50dd3-513">7</span></span>              | <span data-ttu-id="50dd3-514">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="50dd3-514">Custom</span></span> | <span data-ttu-id="50dd3-515">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="50dd3-515">Finance lease obligation</span></span> |       | <span data-ttu-id="50dd3-516">94.97</span><span class="sxs-lookup"><span data-stu-id="50dd3-516">94.97</span></span>  |

<span data-ttu-id="50dd3-517">Poistokulun kirjauskansiovienti luodaan resurssin poistoaikataulusta.</span><span class="sxs-lookup"><span data-stu-id="50dd3-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="50dd3-518">Poistokulu – 31.1.2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="50dd3-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="50dd3-519">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="50dd3-519">Account type</span></span> | <span data-ttu-id="50dd3-520">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="50dd3-520">Account number</span></span> | <span data-ttu-id="50dd3-521">Taso</span><span class="sxs-lookup"><span data-stu-id="50dd3-521">Layer</span></span>  | <span data-ttu-id="50dd3-522">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="50dd3-522">Account description</span></span>      | <span data-ttu-id="50dd3-523">Veloitus</span><span class="sxs-lookup"><span data-stu-id="50dd3-523">Debit</span></span>  | <span data-ttu-id="50dd3-524">Luotto</span><span class="sxs-lookup"><span data-stu-id="50dd3-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="50dd3-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="50dd3-525">Ledger</span></span>       | <span data-ttu-id="50dd3-526">10</span><span class="sxs-lookup"><span data-stu-id="50dd3-526">10</span></span>             | <span data-ttu-id="50dd3-527">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="50dd3-527">Custom</span></span> | <span data-ttu-id="50dd3-528">Poistokulu</span><span class="sxs-lookup"><span data-stu-id="50dd3-528">Depreciation expense</span></span>     | <span data-ttu-id="50dd3-529">949.75</span><span class="sxs-lookup"><span data-stu-id="50dd3-529">949.75</span></span> |        |
| <span data-ttu-id="50dd3-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="50dd3-530">Ledger</span></span>       | <span data-ttu-id="50dd3-531">11</span><span class="sxs-lookup"><span data-stu-id="50dd3-531">11</span></span>             | <span data-ttu-id="50dd3-532">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="50dd3-532">Custom</span></span> | <span data-ttu-id="50dd3-533">Kertynyt poisto</span><span class="sxs-lookup"><span data-stu-id="50dd3-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="50dd3-534">949.75</span><span class="sxs-lookup"><span data-stu-id="50dd3-534">949.75</span></span> |

<span data-ttu-id="50dd3-535">Kun kaikki nämä kirjauskansioviennit on luotu ja kirjattu, näkyvissä ovat seuraavat mukautetun tason 1 arvot.</span><span class="sxs-lookup"><span data-stu-id="50dd3-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="50dd3-536">Huomaa, että viimeinen sarake sisältää pankkikulun, ALV-kulun ja käteisvähennyksen edelliseltä tasolta, mutta ei lakisääteisen raportoinnin kirjauskansiovientejä.</span><span class="sxs-lookup"><span data-stu-id="50dd3-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="50dd3-537">Näin saavutetaan todelliset kaksoisraportoinnin ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="50dd3-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="50dd3-538">Tässä vaiheessa yritys on juuri suorittanut pääkirjan ja yhdistää nykyisen tason mukautettuun tasoon IFRS-pääkirjan luomista varten.</span><span class="sxs-lookup"><span data-stu-id="50dd3-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="50dd3-539">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="50dd3-539">Account No</span></span> | <span data-ttu-id="50dd3-540">kuvaus</span><span class="sxs-lookup"><span data-stu-id="50dd3-540">Description</span></span>              | <span data-ttu-id="50dd3-541">Lakisääteinen kirja\-Nykyinen taso\-JE\-100\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="50dd3-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="50dd3-542">Lakisääteinen kirja\-Nykyinen taso\-JE\-110\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="50dd3-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="50dd3-543">Lakisääteinen kirja\-Nykyinen taso\-JE\-120\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="50dd3-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="50dd3-544">Nykyinen taso \- Kokonaissummat</span><span class="sxs-lookup"><span data-stu-id="50dd3-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="50dd3-545">Palautuskirja\-Mukautettu taso\-JE\-130\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="50dd3-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="50dd3-546">IFRS 16 -kirja\-Mukautettu taso\-JE\-140\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="50dd3-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="50dd3-547">IFRS 16 -kirja\-Mukautettu taso\-JE\-150\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="50dd3-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="50dd3-548">IFRS 16 -kirja\-Mukautettu taso\-JE\-160\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="50dd3-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="50dd3-549">IFRS 16 -kirja\-Mukautettu taso\-JE\-170\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="50dd3-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="50dd3-550">Mukautettu taso \+ Nykyinen taso \- Kokonaissummat</span><span class="sxs-lookup"><span data-stu-id="50dd3-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="50dd3-551">1</span><span class="sxs-lookup"><span data-stu-id="50dd3-551">1</span></span>          | <span data-ttu-id="50dd3-552">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="50dd3-552">Lease expense</span></span>            | <span data-ttu-id="50dd3-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="50dd3-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-554">1,000\.00</span></span>               |   | <span data-ttu-id="50dd3-555">\-1 000</span><span class="sxs-lookup"><span data-stu-id="50dd3-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="50dd3-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-556">0\.00</span></span>                                   |
| <span data-ttu-id="50dd3-557">2</span><span class="sxs-lookup"><span data-stu-id="50dd3-557">2</span></span>          | <span data-ttu-id="50dd3-558">Pankkikulu</span><span class="sxs-lookup"><span data-stu-id="50dd3-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="50dd3-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="50dd3-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="50dd3-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-561">3\.00</span></span>                                   |
| <span data-ttu-id="50dd3-562">3</span><span class="sxs-lookup"><span data-stu-id="50dd3-562">3</span></span>          | <span data-ttu-id="50dd3-563">ALV-kulu</span><span class="sxs-lookup"><span data-stu-id="50dd3-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="50dd3-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="50dd3-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="50dd3-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-566">5\.00</span></span>                                   |
| <span data-ttu-id="50dd3-567">4</span><span class="sxs-lookup"><span data-stu-id="50dd3-567">4</span></span>          | <span data-ttu-id="50dd3-568">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="50dd3-568">Clearing account</span></span>         | <span data-ttu-id="50dd3-569">\-1 000\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="50dd3-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="50dd3-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-571">0\.00</span></span>                   |   | <span data-ttu-id="50dd3-572">1 000</span><span class="sxs-lookup"><span data-stu-id="50dd3-572">1,000</span></span>                                           |                                                | <span data-ttu-id="50dd3-573">\-1 000</span><span class="sxs-lookup"><span data-stu-id="50dd3-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="50dd3-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-574">0\.00</span></span>                                   |
| <span data-ttu-id="50dd3-575">5</span><span class="sxs-lookup"><span data-stu-id="50dd3-575">5</span></span>          | <span data-ttu-id="50dd3-576">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="50dd3-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="50dd3-577">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="50dd3-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-578">1,008\.00</span></span>                                         | <span data-ttu-id="50dd3-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="50dd3-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-580">0\.00</span></span>                                   |
| <span data-ttu-id="50dd3-581">6</span><span class="sxs-lookup"><span data-stu-id="50dd3-581">6</span></span>          | <span data-ttu-id="50dd3-582">Käyttöoikeusomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="50dd3-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="50dd3-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="50dd3-584">22,794</span><span class="sxs-lookup"><span data-stu-id="50dd3-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="50dd3-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="50dd3-585">22,793\.90</span></span>                              |
| <span data-ttu-id="50dd3-586">7</span><span class="sxs-lookup"><span data-stu-id="50dd3-586">7</span></span>          | <span data-ttu-id="50dd3-587">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="50dd3-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="50dd3-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="50dd3-589">\-22 794</span><span class="sxs-lookup"><span data-stu-id="50dd3-589">\-22,794</span></span>                                       | <span data-ttu-id="50dd3-590">1 000</span><span class="sxs-lookup"><span data-stu-id="50dd3-590">1,000</span></span>                                          | <span data-ttu-id="50dd3-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="50dd3-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="50dd3-592">\-21,888\.87</span><span class="sxs-lookup"><span data-stu-id="50dd3-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="50dd3-593">8</span><span class="sxs-lookup"><span data-stu-id="50dd3-593">8</span></span>          | <span data-ttu-id="50dd3-594">Korkokustannus</span><span class="sxs-lookup"><span data-stu-id="50dd3-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="50dd3-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="50dd3-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="50dd3-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="50dd3-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="50dd3-597">94\.97</span></span>                                  |
| <span data-ttu-id="50dd3-598">9</span><span class="sxs-lookup"><span data-stu-id="50dd3-598">9</span></span>          | <span data-ttu-id="50dd3-599">Maksu</span><span class="sxs-lookup"><span data-stu-id="50dd3-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="50dd3-600">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="50dd3-601">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="50dd3-602">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="50dd3-603">10</span><span class="sxs-lookup"><span data-stu-id="50dd3-603">10</span></span>         | <span data-ttu-id="50dd3-604">Poistokulu</span><span class="sxs-lookup"><span data-stu-id="50dd3-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="50dd3-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="50dd3-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="50dd3-606">949\.75</span></span>                                        | <span data-ttu-id="50dd3-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="50dd3-607">949\.75</span></span>                                 |
| <span data-ttu-id="50dd3-608">11</span><span class="sxs-lookup"><span data-stu-id="50dd3-608">11</span></span>         | <span data-ttu-id="50dd3-609">Kertynyt poisto</span><span class="sxs-lookup"><span data-stu-id="50dd3-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="50dd3-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="50dd3-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="50dd3-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="50dd3-611">\-949\.75</span></span>                                      | <span data-ttu-id="50dd3-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="50dd3-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]