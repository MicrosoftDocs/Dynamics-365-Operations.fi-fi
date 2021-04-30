---
title: Kaksoisraportointi
description: Tämä ohjeaihe sisältää esimerkin sekä International Financial Reporting Standard (IFRS) -raportoinnin että resurssin vuokrauksen lakisääteisen raportoinnin vaatimusten täyttämisestä.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseBookMaster
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 86f42f8db707f3b8c62b9ec4c39ad6464f080748
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881153"
---
# <a name="dual-reporting"></a><span data-ttu-id="62fe6-103">Kaksoisraportointi</span><span class="sxs-lookup"><span data-stu-id="62fe6-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62fe6-104">Tämä ohjeaihe sisältää esimerkin sekä International Financial Reporting Standard (IFRS) -raportoinnin että resurssin vuokrauksen lakisääteisen raportoinnin vaatimusten täyttämisestä.</span><span class="sxs-lookup"><span data-stu-id="62fe6-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="62fe6-105">Vaatimuksena on Microsoft Dynamics 365 Financen kirjanpitotasojen käyttökokemus. Sen avulla esimerkki on helpompi ymmärtää.</span><span class="sxs-lookup"><span data-stu-id="62fe6-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="62fe6-106">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="62fe6-106">Example</span></span>

<span data-ttu-id="62fe6-107">Seuraavassa esimerkissä otetaan huomioon vuokraus Italian lakisääteisessä raportoinnissa käyttämällä sekä käteisvaroihin perustuvaa menetelmää että IFRS-raportointimenetelmiä.</span><span class="sxs-lookup"><span data-stu-id="62fe6-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="62fe6-108">Yrityksen on muodostettava kolme kirjaa, joiden avulla sekä Italian lakisääteiset vaatimukset että IFRS 16 -vaatimukset otetaan huomioon.</span><span class="sxs-lookup"><span data-stu-id="62fe6-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="62fe6-109">Yksi kirja vaaditaan IFRS 16:lle, toinen lakisääteisille vaatimuksille ja kolmas lakisääteisten kirjausten automaattista käänteistä kirjausta varten.</span><span class="sxs-lookup"><span data-stu-id="62fe6-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="62fe6-110">Kirjat määritetään seuraavissa taulukoissa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="62fe6-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="62fe6-111">**IFRS 16 -kirja**</span><span class="sxs-lookup"><span data-stu-id="62fe6-111">**IFRS 16 book**</span></span>

<span data-ttu-id="62fe6-112">IFRS 16 -kirja määritetään niin, että se on yhdenmukainen IFRS 16 -kirjanpitostandardin kanssa.</span><span class="sxs-lookup"><span data-stu-id="62fe6-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="62fe6-113">Kaikki tähän kirjaan kirjatut tapahtumat kirjataan mukautettuun tasoon.</span><span class="sxs-lookup"><span data-stu-id="62fe6-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="62fe6-114">Nimi</span><span class="sxs-lookup"><span data-stu-id="62fe6-114">Name</span></span>                                    | <span data-ttu-id="62fe6-115">kuvaus</span><span class="sxs-lookup"><span data-stu-id="62fe6-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="62fe6-116">Kirjan tyyppi</span><span class="sxs-lookup"><span data-stu-id="62fe6-116">Book type</span></span>                               | <span data-ttu-id="62fe6-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="62fe6-117">IFRS 16</span></span>        |
| <span data-ttu-id="62fe6-118">Kirjan kuvaus</span><span class="sxs-lookup"><span data-stu-id="62fe6-118">Book description</span></span>                        | <span data-ttu-id="62fe6-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="62fe6-119">IFRS 16</span></span>        |
| <span data-ttu-id="62fe6-120">Kirjanpitotaso</span><span class="sxs-lookup"><span data-stu-id="62fe6-120">Posting Layer</span></span>                           | <span data-ttu-id="62fe6-121">Mukautettu kerros 1</span><span class="sxs-lookup"><span data-stu-id="62fe6-121">Custom layer 1</span></span> |
| <span data-ttu-id="62fe6-122">Vuokran tyyppi</span><span class="sxs-lookup"><span data-stu-id="62fe6-122">Lease Type</span></span>                              | <span data-ttu-id="62fe6-123">Finance</span><span class="sxs-lookup"><span data-stu-id="62fe6-123">Finance</span></span>        |
| <span data-ttu-id="62fe6-124">Kirjanpitokehys</span><span class="sxs-lookup"><span data-stu-id="62fe6-124">Accounting Framework</span></span>                    | <span data-ttu-id="62fe6-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="62fe6-125">IFRS 16</span></span>        |
| <span data-ttu-id="62fe6-126">Vuokra-/käyttöajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="62fe6-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="62fe6-127">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-127">0.00</span></span>           |
| <span data-ttu-id="62fe6-128">Nykyinen arvo / resurssin käyvän arvon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="62fe6-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="62fe6-129">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-129">0.00</span></span>           |
| <span data-ttu-id="62fe6-130">Lyhytaikainen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="62fe6-130">Short-term threshold</span></span>                    | <span data-ttu-id="62fe6-131">12</span><span class="sxs-lookup"><span data-stu-id="62fe6-131">12</span></span>             |
| <span data-ttu-id="62fe6-132">Arvoltaan vähäinen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="62fe6-132">Low Value Threshold</span></span>                     | <span data-ttu-id="62fe6-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-133">5,000.00</span></span>       |
| <span data-ttu-id="62fe6-134">Maksu toimittajalle</span><span class="sxs-lookup"><span data-stu-id="62fe6-134">Pay to Vendor</span></span>                           | <span data-ttu-id="62fe6-135">Nro</span><span class="sxs-lookup"><span data-stu-id="62fe6-135">No</span></span>             |

<span data-ttu-id="62fe6-136">**Lakisääteinen kirja**</span><span class="sxs-lookup"><span data-stu-id="62fe6-136">**Statutory book**</span></span>

<span data-ttu-id="62fe6-137">Lakisääteinen kirja on käteisvaroihin perustuva kirja, jonne yritys kirjaa vuokrauksen kulut käteisvarojen summana, joka maksetaan joka kuukausi vuokrana.</span><span class="sxs-lookup"><span data-stu-id="62fe6-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="62fe6-138">Tämä kirja ei tuota käyttöoikeusomaisuuserää tai vuokrasopimusvelkaa.</span><span class="sxs-lookup"><span data-stu-id="62fe6-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="62fe6-139">Nimi</span><span class="sxs-lookup"><span data-stu-id="62fe6-139">Name</span></span>                                    | <span data-ttu-id="62fe6-140">kuvaus</span><span class="sxs-lookup"><span data-stu-id="62fe6-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="62fe6-141">Kirjan tyyppi</span><span class="sxs-lookup"><span data-stu-id="62fe6-141">Book type</span></span>                               | <span data-ttu-id="62fe6-142">Lakisääteinen</span><span class="sxs-lookup"><span data-stu-id="62fe6-142">Statutory</span></span>   |
| <span data-ttu-id="62fe6-143">Kirjan kuvaus</span><span class="sxs-lookup"><span data-stu-id="62fe6-143">Book description</span></span>                        | <span data-ttu-id="62fe6-144">Paikallinen GAAP</span><span class="sxs-lookup"><span data-stu-id="62fe6-144">Local GAAP</span></span>  |
| <span data-ttu-id="62fe6-145">Kirjanpitotaso</span><span class="sxs-lookup"><span data-stu-id="62fe6-145">Posting Layer</span></span>                           | <span data-ttu-id="62fe6-146">Valittu</span><span class="sxs-lookup"><span data-stu-id="62fe6-146">Current</span></span>     |
| <span data-ttu-id="62fe6-147">Vuokran tyyppi</span><span class="sxs-lookup"><span data-stu-id="62fe6-147">Lease Type</span></span>                              | <span data-ttu-id="62fe6-148">Automaattinen</span><span class="sxs-lookup"><span data-stu-id="62fe6-148">Automatic</span></span>   |
| <span data-ttu-id="62fe6-149">Kirjanpitokehys</span><span class="sxs-lookup"><span data-stu-id="62fe6-149">Accounting Framework</span></span>                    | <span data-ttu-id="62fe6-150">Maksuperuste</span><span class="sxs-lookup"><span data-stu-id="62fe6-150">Cash basis</span></span>  |
| <span data-ttu-id="62fe6-151">Vuokra-/käyttöajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="62fe6-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="62fe6-152">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-152">0.00</span></span>        |
| <span data-ttu-id="62fe6-153">Nykyinen arvo / resurssin käyvän arvon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="62fe6-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="62fe6-154">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-154">0.00</span></span>        |
| <span data-ttu-id="62fe6-155">Lyhytaikainen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="62fe6-155">Short-term threshold</span></span>                    | <span data-ttu-id="62fe6-156">0</span><span class="sxs-lookup"><span data-stu-id="62fe6-156">0</span></span>           |
| <span data-ttu-id="62fe6-157">Arvoltaan vähäinen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="62fe6-157">Low Value Threshold</span></span>                     | <span data-ttu-id="62fe6-158">0</span><span class="sxs-lookup"><span data-stu-id="62fe6-158">0</span></span>           |
| <span data-ttu-id="62fe6-159">Maksu toimittajalle</span><span class="sxs-lookup"><span data-stu-id="62fe6-159">Pay to Vendor</span></span>                           | <span data-ttu-id="62fe6-160">Nro</span><span class="sxs-lookup"><span data-stu-id="62fe6-160">No</span></span>          |

<span data-ttu-id="62fe6-161">**Lakisääteinen palautuskirja**</span><span class="sxs-lookup"><span data-stu-id="62fe6-161">**Statutory reversal book**</span></span>

<span data-ttu-id="62fe6-162">Lakisääteinen palautuskirja määritetään samalla tavalla kuin lakisääteinen kirja.</span><span class="sxs-lookup"><span data-stu-id="62fe6-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="62fe6-163">Nimi</span><span class="sxs-lookup"><span data-stu-id="62fe6-163">Name</span></span>                                    | <span data-ttu-id="62fe6-164">kuvaus</span><span class="sxs-lookup"><span data-stu-id="62fe6-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="62fe6-165">Kirjan tyyppi</span><span class="sxs-lookup"><span data-stu-id="62fe6-165">Book type</span></span>                               | <span data-ttu-id="62fe6-166">Lakisääteinen – palautus</span><span class="sxs-lookup"><span data-stu-id="62fe6-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="62fe6-167">Kirjan kuvaus</span><span class="sxs-lookup"><span data-stu-id="62fe6-167">Book description</span></span>                        | <span data-ttu-id="62fe6-168">Kirjaa käänteiseen lakisääteiseen kirjaan</span><span class="sxs-lookup"><span data-stu-id="62fe6-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="62fe6-169">Kirjanpitotaso</span><span class="sxs-lookup"><span data-stu-id="62fe6-169">Posting Layer</span></span>                           | <span data-ttu-id="62fe6-170">Mukautettu kerros 1</span><span class="sxs-lookup"><span data-stu-id="62fe6-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="62fe6-171">Vuokran tyyppi</span><span class="sxs-lookup"><span data-stu-id="62fe6-171">Lease Type</span></span>                              | <span data-ttu-id="62fe6-172">Automaattinen</span><span class="sxs-lookup"><span data-stu-id="62fe6-172">Automatic</span></span>                      |
| <span data-ttu-id="62fe6-173">Kirjanpitokehys</span><span class="sxs-lookup"><span data-stu-id="62fe6-173">Accounting Framework</span></span>                    | <span data-ttu-id="62fe6-174">Maksuperuste</span><span class="sxs-lookup"><span data-stu-id="62fe6-174">Cash basis</span></span>                     |
| <span data-ttu-id="62fe6-175">Vuokra-/käyttöajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="62fe6-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="62fe6-176">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-176">0.00</span></span>                           |
| <span data-ttu-id="62fe6-177">Nykyinen arvo / resurssin käyvän arvon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="62fe6-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="62fe6-178">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-178">0.00</span></span>                           |
| <span data-ttu-id="62fe6-179">Lyhytaikainen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="62fe6-179">Short-term threshold</span></span>                    | <span data-ttu-id="62fe6-180">0</span><span class="sxs-lookup"><span data-stu-id="62fe6-180">0</span></span>                              |
| <span data-ttu-id="62fe6-181">Arvoltaan vähäinen kynnysarvo</span><span class="sxs-lookup"><span data-stu-id="62fe6-181">Low Value Threshold</span></span>                     | <span data-ttu-id="62fe6-182">0</span><span class="sxs-lookup"><span data-stu-id="62fe6-182">0</span></span>                              |
| <span data-ttu-id="62fe6-183">Maksu toimittajalle</span><span class="sxs-lookup"><span data-stu-id="62fe6-183">Pay to Vendor</span></span>                           | <span data-ttu-id="62fe6-184">Nro</span><span class="sxs-lookup"><span data-stu-id="62fe6-184">No</span></span>                             |

<span data-ttu-id="62fe6-185">Tässä esimerkissä on luotu vuokraus, jolla on seuraavat asetukset **Yleistä**- ja **Maksuaikataulurivit**-välilehdissä.</span><span class="sxs-lookup"><span data-stu-id="62fe6-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="62fe6-186">**Yleinen-välilehti**</span><span class="sxs-lookup"><span data-stu-id="62fe6-186">**General tab**</span></span>

| <span data-ttu-id="62fe6-187">Kenttä</span><span class="sxs-lookup"><span data-stu-id="62fe6-187">Field</span></span>                      | <span data-ttu-id="62fe6-188">Arvo</span><span class="sxs-lookup"><span data-stu-id="62fe6-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="62fe6-189">Inkrementaalinen lainakorko</span><span class="sxs-lookup"><span data-stu-id="62fe6-189">Incremental borrowing rate</span></span> | <span data-ttu-id="62fe6-190">5 %</span><span class="sxs-lookup"><span data-stu-id="62fe6-190">5%</span></span>               |
| <span data-ttu-id="62fe6-191">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="62fe6-191">Commencement date</span></span>          | <span data-ttu-id="62fe6-192">1.1.2020</span><span class="sxs-lookup"><span data-stu-id="62fe6-192">1/1/2020</span></span>         |
| <span data-ttu-id="62fe6-193">Vuokraryhmä</span><span class="sxs-lookup"><span data-stu-id="62fe6-193">Lease group</span></span>                | <span data-ttu-id="62fe6-194">Rakennukset</span><span class="sxs-lookup"><span data-stu-id="62fe6-194">Buildings</span></span>        |
| <span data-ttu-id="62fe6-195">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="62fe6-195">Vendor</span></span>                     | <span data-ttu-id="62fe6-196">1001</span><span class="sxs-lookup"><span data-stu-id="62fe6-196">1001</span></span>             |
| <span data-ttu-id="62fe6-197">Resurssin käypä arvo</span><span class="sxs-lookup"><span data-stu-id="62fe6-197">Fair value of the asset</span></span>    | <span data-ttu-id="62fe6-198">245,000</span><span class="sxs-lookup"><span data-stu-id="62fe6-198">245,000</span></span>          |
| <span data-ttu-id="62fe6-199">Käyttöomaisuuden käyttöikä</span><span class="sxs-lookup"><span data-stu-id="62fe6-199">Asset useful life</span></span>          | <span data-ttu-id="62fe6-200">120</span><span class="sxs-lookup"><span data-stu-id="62fe6-200">120</span></span>              |
| <span data-ttu-id="62fe6-201">Annuiteetin tyyppi</span><span class="sxs-lookup"><span data-stu-id="62fe6-201">Annuity type</span></span>               | <span data-ttu-id="62fe6-202">Tavallinen annuiteetti</span><span class="sxs-lookup"><span data-stu-id="62fe6-202">Ordinary annuity</span></span> |
| <span data-ttu-id="62fe6-203">Yhdistämisväli</span><span class="sxs-lookup"><span data-stu-id="62fe6-203">Compounding interval</span></span>       | <span data-ttu-id="62fe6-204">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="62fe6-204">Monthly</span></span>          |

<span data-ttu-id="62fe6-205">**Maksusuunnitelmarivit-välilehti**</span><span class="sxs-lookup"><span data-stu-id="62fe6-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="62fe6-206">Kenttä</span><span class="sxs-lookup"><span data-stu-id="62fe6-206">Field</span></span>             | <span data-ttu-id="62fe6-207">Arvo</span><span class="sxs-lookup"><span data-stu-id="62fe6-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="62fe6-208">Aloituspäivä</span><span class="sxs-lookup"><span data-stu-id="62fe6-208">Start date</span></span>        | <span data-ttu-id="62fe6-209">1.1.2020</span><span class="sxs-lookup"><span data-stu-id="62fe6-209">1/1/2020</span></span>   |
| <span data-ttu-id="62fe6-210">Kausiväli</span><span class="sxs-lookup"><span data-stu-id="62fe6-210">Period interval</span></span>   | <span data-ttu-id="62fe6-211">Kuukautta</span><span class="sxs-lookup"><span data-stu-id="62fe6-211">Months</span></span>     |
| <span data-ttu-id="62fe6-212">Kaudet</span><span class="sxs-lookup"><span data-stu-id="62fe6-212">Periods</span></span>           | <span data-ttu-id="62fe6-213">24</span><span class="sxs-lookup"><span data-stu-id="62fe6-213">24</span></span>         |
| <span data-ttu-id="62fe6-214">Päättymispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="62fe6-214">End date</span></span>          | <span data-ttu-id="62fe6-215">31.12.2020</span><span class="sxs-lookup"><span data-stu-id="62fe6-215">12/31/2020</span></span> |
| <span data-ttu-id="62fe6-216">Maksun toistuvuus</span><span class="sxs-lookup"><span data-stu-id="62fe6-216">Payment frequency</span></span> | <span data-ttu-id="62fe6-217">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="62fe6-217">Monthly</span></span>    |
| <span data-ttu-id="62fe6-218">Maksun summa</span><span class="sxs-lookup"><span data-stu-id="62fe6-218">Payment amount</span></span>    | <span data-ttu-id="62fe6-219">1 000</span><span class="sxs-lookup"><span data-stu-id="62fe6-219">1,000</span></span>      |

<span data-ttu-id="62fe6-220">Jotta tämä vuokraus voidaan ottaa huomioon kahdessa kehyksessä, käytetään sekä nykyistä että mukautettua kirjaustasoa.</span><span class="sxs-lookup"><span data-stu-id="62fe6-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="62fe6-221">Seuraavassa taulukossa on esimerkki jokaisesta kirjauskansiomerkinnästä, joka vaaditaan vastaamaan tasapuolisesti kunkin raportointistandardin mukaisia taloustietoja.</span><span class="sxs-lookup"><span data-stu-id="62fe6-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="62fe6-222">Kunkin vuokrauksen ensimmäisen kuukauden kirjauskansiomerkinnän yksityiskohtainen kuvaus annetaan jälkikäteen.</span><span class="sxs-lookup"><span data-stu-id="62fe6-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="62fe6-223">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="62fe6-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="62fe6-224">kuvaus</span><span class="sxs-lookup"><span data-stu-id="62fe6-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="62fe6-225">Lakisääteinen kirja (nykyinen taso)</span><span class="sxs-lookup"><span data-stu-id="62fe6-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="62fe6-226">Nykyinen taso yhteensä</span><span class="sxs-lookup"><span data-stu-id="62fe6-226">Current layer total</span></span></th>
<th><span data-ttu-id="62fe6-227">Palautuskirja (mukautettu taso)</span><span class="sxs-lookup"><span data-stu-id="62fe6-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="62fe6-228">IFRS 16 -kirja (mukautettu taso)</span><span class="sxs-lookup"><span data-stu-id="62fe6-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="62fe6-229">Nykyinen taso + mukautettu taso yhteensä</span><span class="sxs-lookup"><span data-stu-id="62fe6-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="62fe6-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="62fe6-230">JE-100</span></span></th>
<th><span data-ttu-id="62fe6-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="62fe6-231">JE-110</span></span></th>
<th><span data-ttu-id="62fe6-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="62fe6-232">JE-120</span></span></th>
<th><span data-ttu-id="62fe6-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="62fe6-233">JE-130</span></span></th>
<th><span data-ttu-id="62fe6-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="62fe6-234">JE-140</span></span></th>
<th><span data-ttu-id="62fe6-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="62fe6-235">JE-150</span></span></th>
<th><span data-ttu-id="62fe6-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="62fe6-236">JE-160</span></span></th>
<th><span data-ttu-id="62fe6-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="62fe6-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="62fe6-238">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="62fe6-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="62fe6-239">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="62fe6-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="62fe6-240">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="62fe6-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="62fe6-241">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="62fe6-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="62fe6-242">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="62fe6-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="62fe6-243">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="62fe6-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="62fe6-244">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="62fe6-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="62fe6-245">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="62fe6-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="62fe6-246">1</span><span class="sxs-lookup"><span data-stu-id="62fe6-246">1</span></span></td>
<td><span data-ttu-id="62fe6-247">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="62fe6-247">Lease expense</span></span></td>
<td><span data-ttu-id="62fe6-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-249">1,000.00</span></span></td>
<td><span data-ttu-id="62fe6-250">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-251">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62fe6-252">2</span><span class="sxs-lookup"><span data-stu-id="62fe6-252">2</span></span></td>
<td><span data-ttu-id="62fe6-253">Pankkikulu</span><span class="sxs-lookup"><span data-stu-id="62fe6-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="62fe6-254">3.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="62fe6-255">3.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-256">3.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62fe6-257">3</span><span class="sxs-lookup"><span data-stu-id="62fe6-257">3</span></span></td>
<td><span data-ttu-id="62fe6-258">ALV-kulu</span><span class="sxs-lookup"><span data-stu-id="62fe6-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="62fe6-259">5.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="62fe6-260">5.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-261">5.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62fe6-262">4</span><span class="sxs-lookup"><span data-stu-id="62fe6-262">4</span></span></td>
<td><span data-ttu-id="62fe6-263">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="62fe6-263">Clearing account</span></span></td>
<td><span data-ttu-id="62fe6-264">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-264">-1,000.00</span></span></td>
<td><span data-ttu-id="62fe6-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="62fe6-266">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-266">0.00</span></span></td>
<td><span data-ttu-id="62fe6-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="62fe6-268">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-269">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62fe6-270">5</span><span class="sxs-lookup"><span data-stu-id="62fe6-270">5</span></span></td>
<td><span data-ttu-id="62fe6-271">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="62fe6-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="62fe6-272">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-272">-1,008.00</span></span></td>
<td><span data-ttu-id="62fe6-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-273">1,008.00</span></span></td>
<td><span data-ttu-id="62fe6-274">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-275">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62fe6-276">6</span><span class="sxs-lookup"><span data-stu-id="62fe6-276">6</span></span></td>
<td><span data-ttu-id="62fe6-277">Käyttöoikeusomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="62fe6-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-278">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="62fe6-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="62fe6-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62fe6-281">7</span><span class="sxs-lookup"><span data-stu-id="62fe6-281">7</span></span></td>
<td><span data-ttu-id="62fe6-282">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="62fe6-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-283">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="62fe6-284">-22 794,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-284">-22,794.00</span></span></td>
<td><span data-ttu-id="62fe6-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-285">1,000.00</span></span></td>
<td><span data-ttu-id="62fe6-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="62fe6-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="62fe6-287">-21 888,87</span><span class="sxs-lookup"><span data-stu-id="62fe6-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62fe6-288">8</span><span class="sxs-lookup"><span data-stu-id="62fe6-288">8</span></span></td>
<td><span data-ttu-id="62fe6-289">Korkokustannus</span><span class="sxs-lookup"><span data-stu-id="62fe6-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-290">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-291">94.97</span><span class="sxs-lookup"><span data-stu-id="62fe6-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="62fe6-292">94.97</span><span class="sxs-lookup"><span data-stu-id="62fe6-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62fe6-293">9</span><span class="sxs-lookup"><span data-stu-id="62fe6-293">9</span></span></td>
<td><span data-ttu-id="62fe6-294">Maksu</span><span class="sxs-lookup"><span data-stu-id="62fe6-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-295">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-295">-1,008.00</span></span></td>
<td><span data-ttu-id="62fe6-296">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-297">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62fe6-298">10</span><span class="sxs-lookup"><span data-stu-id="62fe6-298">10</span></span></td>
<td><span data-ttu-id="62fe6-299">Poistokulu</span><span class="sxs-lookup"><span data-stu-id="62fe6-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-300">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-301">949.75</span><span class="sxs-lookup"><span data-stu-id="62fe6-301">949.75</span></span></td>
<td><span data-ttu-id="62fe6-302">949.75</span><span class="sxs-lookup"><span data-stu-id="62fe6-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62fe6-303">11</span><span class="sxs-lookup"><span data-stu-id="62fe6-303">11</span></span></td>
<td><span data-ttu-id="62fe6-304">Kertynyt poisto</span><span class="sxs-lookup"><span data-stu-id="62fe6-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-305">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="62fe6-306">-949.75</span></span></td>
<td><span data-ttu-id="62fe6-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="62fe6-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="62fe6-308">Kuten edellä olevasta taulukosta ilmenee, sekä lakisääteinen raportointi että IFRS-raportointi edellyttävät kolmen kirjan käyttämistä.</span><span class="sxs-lookup"><span data-stu-id="62fe6-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="62fe6-309">Lakisääteinen kirja tallentaa vuokrat nykyisen tason käteisvaroihin perustuvan kirjanpidon sääntöjen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="62fe6-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="62fe6-310">Lakisääteinen palautuskirja kumoaa lakisääteiset kirjauskansiomerkinnät.</span><span class="sxs-lookup"><span data-stu-id="62fe6-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="62fe6-311">IFRS 16 -kirja luo IFRS 16:n pakolliset kirjauskansiomerkinnät.</span><span class="sxs-lookup"><span data-stu-id="62fe6-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="62fe6-312">Sinun on syötettävä vuokraus vain kerran.</span><span class="sxs-lookup"><span data-stu-id="62fe6-312">You must enter a lease only one time.</span></span> <span data-ttu-id="62fe6-313">Tämän jälkeen voit avata **Kirjat**-sivun, ja näet kaikki vuokraukseen liittyvät kirjat.</span><span class="sxs-lookup"><span data-stu-id="62fe6-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="62fe6-314">Kun luot kirjoja, kaikkien kolmen on liityttävä samaan vuokraustietueeseen.</span><span class="sxs-lookup"><span data-stu-id="62fe6-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="62fe6-315">Ensimmäinen kirjauskansiomerkintä tallentaa vuokrauksen lakisääteiseen kirjaan.</span><span class="sxs-lookup"><span data-stu-id="62fe6-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="62fe6-316">Voit luoda maksut eränä tai valitsemalla maksusuunnitelman lakisääteisestä kirjasta.</span><span class="sxs-lookup"><span data-stu-id="62fe6-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="62fe6-317">Tässä esimerkissä maksusuunnitelmasta luodaan seuraava kirjauskansiomerkintä lakisääteistä kirjaa varten.</span><span class="sxs-lookup"><span data-stu-id="62fe6-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="62fe6-318">Vuokra – 31.1.2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="62fe6-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="62fe6-319">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="62fe6-319">Account type</span></span> | <span data-ttu-id="62fe6-320">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="62fe6-320">Account number</span></span> | <span data-ttu-id="62fe6-321">Taso</span><span class="sxs-lookup"><span data-stu-id="62fe6-321">Layer</span></span>   | <span data-ttu-id="62fe6-322">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="62fe6-322">Account description</span></span> | <span data-ttu-id="62fe6-323">Veloitus</span><span class="sxs-lookup"><span data-stu-id="62fe6-323">Debit</span></span>    | <span data-ttu-id="62fe6-324">Luotto</span><span class="sxs-lookup"><span data-stu-id="62fe6-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="62fe6-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="62fe6-325">Ledger</span></span>       | <span data-ttu-id="62fe6-326">1</span><span class="sxs-lookup"><span data-stu-id="62fe6-326">1</span></span>              | <span data-ttu-id="62fe6-327">Valittu</span><span class="sxs-lookup"><span data-stu-id="62fe6-327">Current</span></span> | <span data-ttu-id="62fe6-328">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="62fe6-328">Lease expense</span></span>       | <span data-ttu-id="62fe6-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-329">1,000.00</span></span> |          |
| <span data-ttu-id="62fe6-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="62fe6-330">Ledger</span></span>       | <span data-ttu-id="62fe6-331">4</span><span class="sxs-lookup"><span data-stu-id="62fe6-331">4</span></span>              | <span data-ttu-id="62fe6-332">Valittu</span><span class="sxs-lookup"><span data-stu-id="62fe6-332">Current</span></span> | <span data-ttu-id="62fe6-333">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="62fe6-333">Clearing account</span></span>    |          | <span data-ttu-id="62fe6-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-334">1,000.00</span></span> |

<span data-ttu-id="62fe6-335">Ostoreskontran käsittelijä käyttää Dynamics 365:n vakiotoimintoa luodessaan resurssin vuokrauksen ulkopuoliselle vuokraukselle laskun maksamista varten.</span><span class="sxs-lookup"><span data-stu-id="62fe6-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="62fe6-336">Sen sijaan, että debettiliksi valittaisiin **Vuokran kulu** ostoreskontran käsittelijä valitsee selvitystilin seuraavan merkinnän luomiseksi.</span><span class="sxs-lookup"><span data-stu-id="62fe6-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="62fe6-337">Ostoreskontran prosessi – 31.1.2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="62fe6-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="62fe6-338">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="62fe6-338">Account type</span></span> | <span data-ttu-id="62fe6-339">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="62fe6-339">Account number</span></span> | <span data-ttu-id="62fe6-340">Taso</span><span class="sxs-lookup"><span data-stu-id="62fe6-340">Layer</span></span>   | <span data-ttu-id="62fe6-341">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="62fe6-341">Account description</span></span> | <span data-ttu-id="62fe6-342">Veloitus</span><span class="sxs-lookup"><span data-stu-id="62fe6-342">Debit</span></span>    | <span data-ttu-id="62fe6-343">Luotto</span><span class="sxs-lookup"><span data-stu-id="62fe6-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="62fe6-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="62fe6-344">Ledger</span></span>       | <span data-ttu-id="62fe6-345">4</span><span class="sxs-lookup"><span data-stu-id="62fe6-345">4</span></span>              | <span data-ttu-id="62fe6-346">Valittu</span><span class="sxs-lookup"><span data-stu-id="62fe6-346">Current</span></span> | <span data-ttu-id="62fe6-347">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="62fe6-347">Clearing account</span></span>    | <span data-ttu-id="62fe6-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-348">1,000.00</span></span> |          |
| <span data-ttu-id="62fe6-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="62fe6-349">Ledger</span></span>       | <span data-ttu-id="62fe6-350">2</span><span class="sxs-lookup"><span data-stu-id="62fe6-350">2</span></span>              | <span data-ttu-id="62fe6-351">Valittu</span><span class="sxs-lookup"><span data-stu-id="62fe6-351">Current</span></span> | <span data-ttu-id="62fe6-352">Pankkikulu</span><span class="sxs-lookup"><span data-stu-id="62fe6-352">Bank fee</span></span>            | <span data-ttu-id="62fe6-353">3.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-353">3.00</span></span>     |          |
| <span data-ttu-id="62fe6-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="62fe6-354">Ledger</span></span>       | <span data-ttu-id="62fe6-355">3</span><span class="sxs-lookup"><span data-stu-id="62fe6-355">3</span></span>              | <span data-ttu-id="62fe6-356">Valittu</span><span class="sxs-lookup"><span data-stu-id="62fe6-356">Current</span></span> | <span data-ttu-id="62fe6-357">ALV-kulu</span><span class="sxs-lookup"><span data-stu-id="62fe6-357">VAT expense</span></span>         | <span data-ttu-id="62fe6-358">5.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-358">5.00</span></span>     |          |
| <span data-ttu-id="62fe6-359">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="62fe6-359">Vendor</span></span>       | <span data-ttu-id="62fe6-360">5</span><span class="sxs-lookup"><span data-stu-id="62fe6-360">5</span></span>              | <span data-ttu-id="62fe6-361">Valittu</span><span class="sxs-lookup"><span data-stu-id="62fe6-361">Current</span></span> | <span data-ttu-id="62fe6-362">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="62fe6-362">Accounts payable</span></span>    |          | <span data-ttu-id="62fe6-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-363">1,008.00</span></span> |

<span data-ttu-id="62fe6-364">Kun toimittajalle annetaan ilmoitus, seuraat säännöllistä maksuprosessia.</span><span class="sxs-lookup"><span data-stu-id="62fe6-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="62fe6-365">Tämän prosessin aikana luodaan seuraava kirjauskansiomerkintä.</span><span class="sxs-lookup"><span data-stu-id="62fe6-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="62fe6-366">Käteismaksu – 31.1.2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="62fe6-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="62fe6-367">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="62fe6-367">Account type</span></span> | <span data-ttu-id="62fe6-368">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="62fe6-368">Account number</span></span> | <span data-ttu-id="62fe6-369">Taso</span><span class="sxs-lookup"><span data-stu-id="62fe6-369">Layer</span></span>   | <span data-ttu-id="62fe6-370">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="62fe6-370">Account description</span></span> | <span data-ttu-id="62fe6-371">Veloitus</span><span class="sxs-lookup"><span data-stu-id="62fe6-371">Debit</span></span>    | <span data-ttu-id="62fe6-372">Luotto</span><span class="sxs-lookup"><span data-stu-id="62fe6-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="62fe6-373">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="62fe6-373">Vendor</span></span>       | <span data-ttu-id="62fe6-374">5</span><span class="sxs-lookup"><span data-stu-id="62fe6-374">5</span></span>              | <span data-ttu-id="62fe6-375">Valittu</span><span class="sxs-lookup"><span data-stu-id="62fe6-375">Current</span></span> | <span data-ttu-id="62fe6-376">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="62fe6-376">Accounts Payable</span></span>    | <span data-ttu-id="62fe6-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-377">1,008.00</span></span> |          |
| <span data-ttu-id="62fe6-378">Pankki</span><span class="sxs-lookup"><span data-stu-id="62fe6-378">Bank</span></span>         | <span data-ttu-id="62fe6-379">9</span><span class="sxs-lookup"><span data-stu-id="62fe6-379">9</span></span>              | <span data-ttu-id="62fe6-380">Valittu</span><span class="sxs-lookup"><span data-stu-id="62fe6-380">Current</span></span> | <span data-ttu-id="62fe6-381">Maksu</span><span class="sxs-lookup"><span data-stu-id="62fe6-381">Cash</span></span>                |          | <span data-ttu-id="62fe6-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-382">1,008.00</span></span> |

<span data-ttu-id="62fe6-383">Nyt tämä vuokraus on otettu kokonaan huomioon lakisääteisen raportoinnin vaatimusten mukaisesti, ja voit luoda pääkirjan nykyisen tason mukaan.</span><span class="sxs-lookup"><span data-stu-id="62fe6-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="62fe6-384">Järjestelmä palauttaa pääkirjan, jossa ovat seuraavat luvut.</span><span class="sxs-lookup"><span data-stu-id="62fe6-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="62fe6-385">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="62fe6-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="62fe6-386">kuvaus</span><span class="sxs-lookup"><span data-stu-id="62fe6-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="62fe6-387">Lakisääteinen kirja (nykyinen taso)</span><span class="sxs-lookup"><span data-stu-id="62fe6-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="62fe6-388">Nykyinen taso yhteensä</span><span class="sxs-lookup"><span data-stu-id="62fe6-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="62fe6-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="62fe6-389">JE-100</span></span></th>
<th><span data-ttu-id="62fe6-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="62fe6-390">JE-110</span></span></th>
<th><span data-ttu-id="62fe6-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="62fe6-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="62fe6-392">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="62fe6-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="62fe6-393">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="62fe6-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="62fe6-394">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="62fe6-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="62fe6-395">1</span><span class="sxs-lookup"><span data-stu-id="62fe6-395">1</span></span></td>
<td><span data-ttu-id="62fe6-396">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="62fe6-396">Lease expense</span></span></td>
<td><span data-ttu-id="62fe6-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62fe6-399">2</span><span class="sxs-lookup"><span data-stu-id="62fe6-399">2</span></span></td>
<td><span data-ttu-id="62fe6-400">Pankkikulu</span><span class="sxs-lookup"><span data-stu-id="62fe6-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="62fe6-401">3.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="62fe6-402">3.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62fe6-403">3</span><span class="sxs-lookup"><span data-stu-id="62fe6-403">3</span></span></td>
<td><span data-ttu-id="62fe6-404">ALV-kulu</span><span class="sxs-lookup"><span data-stu-id="62fe6-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="62fe6-405">5.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="62fe6-406">5.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62fe6-407">4</span><span class="sxs-lookup"><span data-stu-id="62fe6-407">4</span></span></td>
<td><span data-ttu-id="62fe6-408">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="62fe6-408">Clearing account</span></span></td>
<td><span data-ttu-id="62fe6-409">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-409">-1,000.00</span></span></td>
<td><span data-ttu-id="62fe6-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="62fe6-411">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62fe6-412">5</span><span class="sxs-lookup"><span data-stu-id="62fe6-412">5</span></span></td>
<td><span data-ttu-id="62fe6-413">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="62fe6-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="62fe6-414">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-414">-1,008.00</span></span></td>
<td><span data-ttu-id="62fe6-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-415">1,008.00</span></span></td>
<td><span data-ttu-id="62fe6-416">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62fe6-417">6</span><span class="sxs-lookup"><span data-stu-id="62fe6-417">6</span></span></td>
<td><span data-ttu-id="62fe6-418">Käyttöoikeusomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="62fe6-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-419">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62fe6-420">7</span><span class="sxs-lookup"><span data-stu-id="62fe6-420">7</span></span></td>
<td><span data-ttu-id="62fe6-421">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="62fe6-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-422">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62fe6-423">8</span><span class="sxs-lookup"><span data-stu-id="62fe6-423">8</span></span></td>
<td><span data-ttu-id="62fe6-424">Korkokustannus</span><span class="sxs-lookup"><span data-stu-id="62fe6-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-425">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62fe6-426">9</span><span class="sxs-lookup"><span data-stu-id="62fe6-426">9</span></span></td>
<td><span data-ttu-id="62fe6-427">Maksu</span><span class="sxs-lookup"><span data-stu-id="62fe6-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-428">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-428">-1,008.00</span></span></td>
<td><span data-ttu-id="62fe6-429">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62fe6-430">10</span><span class="sxs-lookup"><span data-stu-id="62fe6-430">10</span></span></td>
<td><span data-ttu-id="62fe6-431">Poistokulu</span><span class="sxs-lookup"><span data-stu-id="62fe6-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-432">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62fe6-433">11</span><span class="sxs-lookup"><span data-stu-id="62fe6-433">11</span></span></td>
<td><span data-ttu-id="62fe6-434">Kertynyt poisto</span><span class="sxs-lookup"><span data-stu-id="62fe6-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="62fe6-435">0,00</span><span class="sxs-lookup"><span data-stu-id="62fe6-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="62fe6-436">Jos haluat käyttää IFRS 16 -lukuja ja suorittaa saman pääkirjan, lakisääteisen kirjapidon kirjauskansioviennit on palautettava ja IFRS 16 -kirjauskansioviennit kirjattava.</span><span class="sxs-lookup"><span data-stu-id="62fe6-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="62fe6-437">Tässä esimerkissä on myös lakisääteinen palautuskirja siltä varalta, että haluat palauttaa lakisääteiset kirjauskansioviennit. Palautuskirjassa on samat asetukset kuin lakisääteisessä kirjassa, mutta vastakkainen kirjausprofiili.</span><span class="sxs-lookup"><span data-stu-id="62fe6-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="62fe6-438">Esimerkiksi lakisääteinen kirja *veloitti* vuokrauksen kulutilin, mutta palautuskirja *hyvittää* tämän tilin.</span><span class="sxs-lookup"><span data-stu-id="62fe6-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="62fe6-439">Nämä suhteet on helppo määrittää resurssin vuokrauksen kirjaustileillä **Resurssin vuokrauksen parametrit** -sivulla (**Resurssin vuokraus \> Asetukset \> Resurssin vuokrauksen parametrit**).</span><span class="sxs-lookup"><span data-stu-id="62fe6-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="62fe6-440">Kun lakisääteisessä kirjassa käytettyä prosessia käytetään palautuskirjassa, luodaan seuraava kirjauskansiovienti.</span><span class="sxs-lookup"><span data-stu-id="62fe6-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="62fe6-441">Erona on se, että palautuskirja kirjaa vastakirjaukset lakisääteisestä kirjasta.</span><span class="sxs-lookup"><span data-stu-id="62fe6-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="62fe6-442">Vastakirjaukset tehdään myös mukautetussa tasossa.</span><span class="sxs-lookup"><span data-stu-id="62fe6-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="62fe6-443">Kun pääkirja suoritetaan nykyisellä tasolla, palautuskirjauskansiovientejä ei sisällytetä.</span><span class="sxs-lookup"><span data-stu-id="62fe6-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="62fe6-444">Vuokra – 31.1.2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="62fe6-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="62fe6-445">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="62fe6-445">Account type</span></span> | <span data-ttu-id="62fe6-446">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="62fe6-446">Account number</span></span> | <span data-ttu-id="62fe6-447">Taso</span><span class="sxs-lookup"><span data-stu-id="62fe6-447">Layer</span></span>  | <span data-ttu-id="62fe6-448">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="62fe6-448">Account description</span></span> | <span data-ttu-id="62fe6-449">Veloitus</span><span class="sxs-lookup"><span data-stu-id="62fe6-449">Debit</span></span>    | <span data-ttu-id="62fe6-450">Luotto</span><span class="sxs-lookup"><span data-stu-id="62fe6-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="62fe6-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="62fe6-451">Ledger</span></span>       | <span data-ttu-id="62fe6-452">4</span><span class="sxs-lookup"><span data-stu-id="62fe6-452">4</span></span>              | <span data-ttu-id="62fe6-453">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="62fe6-453">Custom</span></span> | <span data-ttu-id="62fe6-454">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="62fe6-454">Clearing account</span></span>    | <span data-ttu-id="62fe6-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-455">1,000.00</span></span> |          |
| <span data-ttu-id="62fe6-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="62fe6-456">Ledger</span></span>       | <span data-ttu-id="62fe6-457">1</span><span class="sxs-lookup"><span data-stu-id="62fe6-457">1</span></span>              | <span data-ttu-id="62fe6-458">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="62fe6-458">Custom</span></span> | <span data-ttu-id="62fe6-459">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="62fe6-459">Lease expense</span></span>       |          | <span data-ttu-id="62fe6-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-460">1,000.00</span></span> |

<span data-ttu-id="62fe6-461">Nyt lakisääteiset kirjauskansioviennit on eliminoitu, ja voit kirjata kaikki IFRS 16:n edellyttämät kirjauskansioviennit IFRS 16 -kirjaan.</span><span class="sxs-lookup"><span data-stu-id="62fe6-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="62fe6-462">Nämä viennit sisältävät käyttöoikeusomaisuuserän ja velan alkuperäisen kirjauksen sekä koron ja poiston tietueen.</span><span class="sxs-lookup"><span data-stu-id="62fe6-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="62fe6-463">Alkuperäinen kirjaus – 1.1.2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="62fe6-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="62fe6-464">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="62fe6-464">Account type</span></span> | <span data-ttu-id="62fe6-465">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="62fe6-465">Account number</span></span> | <span data-ttu-id="62fe6-466">Taso</span><span class="sxs-lookup"><span data-stu-id="62fe6-466">Layer</span></span>  | <span data-ttu-id="62fe6-467">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="62fe6-467">Account description</span></span>      | <span data-ttu-id="62fe6-468">Veloitus</span><span class="sxs-lookup"><span data-stu-id="62fe6-468">Debit</span></span>     | <span data-ttu-id="62fe6-469">Luotto</span><span class="sxs-lookup"><span data-stu-id="62fe6-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="62fe6-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="62fe6-470">Ledger</span></span>       | <span data-ttu-id="62fe6-471">6</span><span class="sxs-lookup"><span data-stu-id="62fe6-471">6</span></span>              | <span data-ttu-id="62fe6-472">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="62fe6-472">Custom</span></span> | <span data-ttu-id="62fe6-473">Käyttöoikeusomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="62fe6-473">ROU Asset</span></span>                | <span data-ttu-id="62fe6-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="62fe6-474">22,793.90</span></span> |           |
| <span data-ttu-id="62fe6-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="62fe6-475">Ledger</span></span>       | <span data-ttu-id="62fe6-476">7</span><span class="sxs-lookup"><span data-stu-id="62fe6-476">7</span></span>              | <span data-ttu-id="62fe6-477">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="62fe6-477">Custom</span></span> | <span data-ttu-id="62fe6-478">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="62fe6-478">Finance lease obligation</span></span> |           | <span data-ttu-id="62fe6-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="62fe6-479">22,793.90</span></span> |

<span data-ttu-id="62fe6-480">Vuokra kirjataan kuten muut vuokrat.</span><span class="sxs-lookup"><span data-stu-id="62fe6-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="62fe6-481">Selvitystiliä käytetään, jotta voidaan varmistaa käteisen hyvitys vain kerran.</span><span class="sxs-lookup"><span data-stu-id="62fe6-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="62fe6-482">Vuokra – 31.1.2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="62fe6-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="62fe6-483">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="62fe6-483">Account type</span></span> | <span data-ttu-id="62fe6-484">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="62fe6-484">Account number</span></span> | <span data-ttu-id="62fe6-485">Taso</span><span class="sxs-lookup"><span data-stu-id="62fe6-485">Layer</span></span>  | <span data-ttu-id="62fe6-486">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="62fe6-486">Account description</span></span>      | <span data-ttu-id="62fe6-487">Veloitus</span><span class="sxs-lookup"><span data-stu-id="62fe6-487">Debit</span></span>    | <span data-ttu-id="62fe6-488">Luotto</span><span class="sxs-lookup"><span data-stu-id="62fe6-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="62fe6-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="62fe6-489">Ledger</span></span>       | <span data-ttu-id="62fe6-490">7</span><span class="sxs-lookup"><span data-stu-id="62fe6-490">7</span></span>              | <span data-ttu-id="62fe6-491">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="62fe6-491">Custom</span></span> | <span data-ttu-id="62fe6-492">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="62fe6-492">Finance lease obligation</span></span> | <span data-ttu-id="62fe6-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-493">1,000.00</span></span> |          |
| <span data-ttu-id="62fe6-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="62fe6-494">Ledger</span></span>       | <span data-ttu-id="62fe6-495">4</span><span class="sxs-lookup"><span data-stu-id="62fe6-495">4</span></span>              | <span data-ttu-id="62fe6-496">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="62fe6-496">Custom</span></span> | <span data-ttu-id="62fe6-497">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="62fe6-497">Clearing account</span></span>         |          | <span data-ttu-id="62fe6-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-498">1,000.00</span></span> |

<span data-ttu-id="62fe6-499">Korkokulun kirjauskansiovienti luodaan velan kuoletusaikataulusta.</span><span class="sxs-lookup"><span data-stu-id="62fe6-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="62fe6-500">Korkokustannus – 31.1.2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="62fe6-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="62fe6-501">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="62fe6-501">Account type</span></span> | <span data-ttu-id="62fe6-502">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="62fe6-502">Account number</span></span> | <span data-ttu-id="62fe6-503">Taso</span><span class="sxs-lookup"><span data-stu-id="62fe6-503">Layer</span></span>  | <span data-ttu-id="62fe6-504">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="62fe6-504">Account description</span></span>      | <span data-ttu-id="62fe6-505">Veloitus</span><span class="sxs-lookup"><span data-stu-id="62fe6-505">Debit</span></span> | <span data-ttu-id="62fe6-506">Luotto</span><span class="sxs-lookup"><span data-stu-id="62fe6-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="62fe6-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="62fe6-507">Ledger</span></span>       | <span data-ttu-id="62fe6-508">8</span><span class="sxs-lookup"><span data-stu-id="62fe6-508">8</span></span>              | <span data-ttu-id="62fe6-509">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="62fe6-509">Custom</span></span> | <span data-ttu-id="62fe6-510">Korkokustannus</span><span class="sxs-lookup"><span data-stu-id="62fe6-510">Interest expense</span></span>         | <span data-ttu-id="62fe6-511">94.97</span><span class="sxs-lookup"><span data-stu-id="62fe6-511">94.97</span></span> |        |
| <span data-ttu-id="62fe6-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="62fe6-512">Ledger</span></span>       | <span data-ttu-id="62fe6-513">7</span><span class="sxs-lookup"><span data-stu-id="62fe6-513">7</span></span>              | <span data-ttu-id="62fe6-514">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="62fe6-514">Custom</span></span> | <span data-ttu-id="62fe6-515">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="62fe6-515">Finance lease obligation</span></span> |       | <span data-ttu-id="62fe6-516">94.97</span><span class="sxs-lookup"><span data-stu-id="62fe6-516">94.97</span></span>  |

<span data-ttu-id="62fe6-517">Poistokulun kirjauskansiovienti luodaan resurssin poistoaikataulusta.</span><span class="sxs-lookup"><span data-stu-id="62fe6-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="62fe6-518">Poistokulu – 31.1.2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="62fe6-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="62fe6-519">Tilityyppi</span><span class="sxs-lookup"><span data-stu-id="62fe6-519">Account type</span></span> | <span data-ttu-id="62fe6-520">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="62fe6-520">Account number</span></span> | <span data-ttu-id="62fe6-521">Taso</span><span class="sxs-lookup"><span data-stu-id="62fe6-521">Layer</span></span>  | <span data-ttu-id="62fe6-522">Tilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="62fe6-522">Account description</span></span>      | <span data-ttu-id="62fe6-523">Veloitus</span><span class="sxs-lookup"><span data-stu-id="62fe6-523">Debit</span></span>  | <span data-ttu-id="62fe6-524">Luotto</span><span class="sxs-lookup"><span data-stu-id="62fe6-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="62fe6-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="62fe6-525">Ledger</span></span>       | <span data-ttu-id="62fe6-526">10</span><span class="sxs-lookup"><span data-stu-id="62fe6-526">10</span></span>             | <span data-ttu-id="62fe6-527">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="62fe6-527">Custom</span></span> | <span data-ttu-id="62fe6-528">Poistokulu</span><span class="sxs-lookup"><span data-stu-id="62fe6-528">Depreciation expense</span></span>     | <span data-ttu-id="62fe6-529">949.75</span><span class="sxs-lookup"><span data-stu-id="62fe6-529">949.75</span></span> |        |
| <span data-ttu-id="62fe6-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="62fe6-530">Ledger</span></span>       | <span data-ttu-id="62fe6-531">11</span><span class="sxs-lookup"><span data-stu-id="62fe6-531">11</span></span>             | <span data-ttu-id="62fe6-532">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="62fe6-532">Custom</span></span> | <span data-ttu-id="62fe6-533">Kertynyt poisto</span><span class="sxs-lookup"><span data-stu-id="62fe6-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="62fe6-534">949.75</span><span class="sxs-lookup"><span data-stu-id="62fe6-534">949.75</span></span> |

<span data-ttu-id="62fe6-535">Kun kaikki nämä kirjauskansioviennit on luotu ja kirjattu, näkyvissä ovat seuraavat mukautetun tason 1 arvot.</span><span class="sxs-lookup"><span data-stu-id="62fe6-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="62fe6-536">Huomaa, että viimeinen sarake sisältää pankkikulun, ALV-kulun ja käteisvähennyksen edelliseltä tasolta, mutta ei lakisääteisen raportoinnin kirjauskansiovientejä.</span><span class="sxs-lookup"><span data-stu-id="62fe6-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="62fe6-537">Näin saavutetaan todelliset kaksoisraportoinnin ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="62fe6-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="62fe6-538">Tässä vaiheessa yritys on juuri suorittanut pääkirjan ja yhdistää nykyisen tason mukautettuun tasoon IFRS-pääkirjan luomista varten.</span><span class="sxs-lookup"><span data-stu-id="62fe6-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="62fe6-539">Tilinumero</span><span class="sxs-lookup"><span data-stu-id="62fe6-539">Account No</span></span> | <span data-ttu-id="62fe6-540">kuvaus</span><span class="sxs-lookup"><span data-stu-id="62fe6-540">Description</span></span>              | <span data-ttu-id="62fe6-541">Lakisääteinen kirja\-Nykyinen taso\-JE\-100\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="62fe6-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="62fe6-542">Lakisääteinen kirja\-Nykyinen taso\-JE\-110\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="62fe6-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="62fe6-543">Lakisääteinen kirja\-Nykyinen taso\-JE\-120\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="62fe6-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="62fe6-544">Nykyinen taso \- Kokonaissummat</span><span class="sxs-lookup"><span data-stu-id="62fe6-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="62fe6-545">Palautuskirja\-Mukautettu taso\-JE\-130\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="62fe6-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="62fe6-546">IFRS 16 -kirja\-Mukautettu taso\-JE\-140\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="62fe6-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="62fe6-547">IFRS 16 -kirja\-Mukautettu taso\-JE\-150\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="62fe6-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="62fe6-548">IFRS 16 -kirja\-Mukautettu taso\-JE\-160\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="62fe6-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="62fe6-549">IFRS 16 -kirja\-Mukautettu taso\-JE\-170\-Debet \(Kredit\)</span><span class="sxs-lookup"><span data-stu-id="62fe6-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="62fe6-550">Mukautettu taso \+ Nykyinen taso \- Kokonaissummat</span><span class="sxs-lookup"><span data-stu-id="62fe6-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="62fe6-551">1</span><span class="sxs-lookup"><span data-stu-id="62fe6-551">1</span></span>          | <span data-ttu-id="62fe6-552">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="62fe6-552">Lease expense</span></span>            | <span data-ttu-id="62fe6-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="62fe6-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-554">1,000\.00</span></span>               |   | <span data-ttu-id="62fe6-555">\-1 000</span><span class="sxs-lookup"><span data-stu-id="62fe6-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="62fe6-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-556">0\.00</span></span>                                   |
| <span data-ttu-id="62fe6-557">2</span><span class="sxs-lookup"><span data-stu-id="62fe6-557">2</span></span>          | <span data-ttu-id="62fe6-558">Pankkikulu</span><span class="sxs-lookup"><span data-stu-id="62fe6-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="62fe6-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="62fe6-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="62fe6-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-561">3\.00</span></span>                                   |
| <span data-ttu-id="62fe6-562">3</span><span class="sxs-lookup"><span data-stu-id="62fe6-562">3</span></span>          | <span data-ttu-id="62fe6-563">ALV-kulu</span><span class="sxs-lookup"><span data-stu-id="62fe6-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="62fe6-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="62fe6-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="62fe6-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-566">5\.00</span></span>                                   |
| <span data-ttu-id="62fe6-567">4</span><span class="sxs-lookup"><span data-stu-id="62fe6-567">4</span></span>          | <span data-ttu-id="62fe6-568">Selvitystili</span><span class="sxs-lookup"><span data-stu-id="62fe6-568">Clearing account</span></span>         | <span data-ttu-id="62fe6-569">\-1 000\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="62fe6-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="62fe6-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-571">0\.00</span></span>                   |   | <span data-ttu-id="62fe6-572">1 000</span><span class="sxs-lookup"><span data-stu-id="62fe6-572">1,000</span></span>                                           |                                                | <span data-ttu-id="62fe6-573">\-1 000</span><span class="sxs-lookup"><span data-stu-id="62fe6-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="62fe6-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-574">0\.00</span></span>                                   |
| <span data-ttu-id="62fe6-575">5</span><span class="sxs-lookup"><span data-stu-id="62fe6-575">5</span></span>          | <span data-ttu-id="62fe6-576">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="62fe6-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="62fe6-577">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="62fe6-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-578">1,008\.00</span></span>                                         | <span data-ttu-id="62fe6-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="62fe6-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-580">0\.00</span></span>                                   |
| <span data-ttu-id="62fe6-581">6</span><span class="sxs-lookup"><span data-stu-id="62fe6-581">6</span></span>          | <span data-ttu-id="62fe6-582">Käyttöoikeusomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="62fe6-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="62fe6-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="62fe6-584">22,794</span><span class="sxs-lookup"><span data-stu-id="62fe6-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="62fe6-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="62fe6-585">22,793\.90</span></span>                              |
| <span data-ttu-id="62fe6-586">7</span><span class="sxs-lookup"><span data-stu-id="62fe6-586">7</span></span>          | <span data-ttu-id="62fe6-587">Rahoitusleasingsopimuksen velvoite</span><span class="sxs-lookup"><span data-stu-id="62fe6-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="62fe6-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="62fe6-589">\-22 794</span><span class="sxs-lookup"><span data-stu-id="62fe6-589">\-22,794</span></span>                                       | <span data-ttu-id="62fe6-590">1 000</span><span class="sxs-lookup"><span data-stu-id="62fe6-590">1,000</span></span>                                          | <span data-ttu-id="62fe6-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="62fe6-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="62fe6-592">\-21,888\.87</span><span class="sxs-lookup"><span data-stu-id="62fe6-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="62fe6-593">8</span><span class="sxs-lookup"><span data-stu-id="62fe6-593">8</span></span>          | <span data-ttu-id="62fe6-594">Korkokustannus</span><span class="sxs-lookup"><span data-stu-id="62fe6-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="62fe6-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="62fe6-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="62fe6-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="62fe6-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="62fe6-597">94\.97</span></span>                                  |
| <span data-ttu-id="62fe6-598">9</span><span class="sxs-lookup"><span data-stu-id="62fe6-598">9</span></span>          | <span data-ttu-id="62fe6-599">Maksu</span><span class="sxs-lookup"><span data-stu-id="62fe6-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="62fe6-600">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="62fe6-601">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="62fe6-602">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="62fe6-603">10</span><span class="sxs-lookup"><span data-stu-id="62fe6-603">10</span></span>         | <span data-ttu-id="62fe6-604">Poistokulu</span><span class="sxs-lookup"><span data-stu-id="62fe6-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="62fe6-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="62fe6-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="62fe6-606">949\.75</span></span>                                        | <span data-ttu-id="62fe6-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="62fe6-607">949\.75</span></span>                                 |
| <span data-ttu-id="62fe6-608">11</span><span class="sxs-lookup"><span data-stu-id="62fe6-608">11</span></span>         | <span data-ttu-id="62fe6-609">Kertynyt poisto</span><span class="sxs-lookup"><span data-stu-id="62fe6-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="62fe6-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="62fe6-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="62fe6-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="62fe6-611">\-949\.75</span></span>                                      | <span data-ttu-id="62fe6-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="62fe6-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
