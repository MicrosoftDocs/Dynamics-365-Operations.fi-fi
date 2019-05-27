---
title: Yleiskustannuslaskenta
description: Tässä aiheessa kuvataan tyypillinen yleiskustannusten laskenta- ja kohdistusprosessi.
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544052"
---
# <a name="overhead-calculation"></a><span data-ttu-id="75620-103">Yleiskustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="75620-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75620-104">Tässä aiheessa kuvataan tyypillinen yleiskustannusten laskenta- ja kohdistusprosessi.</span><span class="sxs-lookup"><span data-stu-id="75620-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="75620-105">Sanaston määritelmä</span><span class="sxs-lookup"><span data-stu-id="75620-105">Term definition</span></span>
---------------

<span data-ttu-id="75620-106">Yleiskustannukset ovat yrityksen toiminnasta syntyviä kustannuksia, joita ei voi suoraan liittää mihinkään tiettyyn liiketoiminnan tehtävään, tuotteeseen tai palveluun.</span><span class="sxs-lookup"><span data-stu-id="75620-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="75620-107">Yleiskustannukset ovat tärkeä tuki voittoa tuottavien tehtävien luonnissa.</span><span class="sxs-lookup"><span data-stu-id="75620-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="75620-108">Seuraavassa on joitakin esimerkkejä yleiskustannuksista:</span><span class="sxs-lookup"><span data-stu-id="75620-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="75620-109">Vuokra</span><span class="sxs-lookup"><span data-stu-id="75620-109">Rent</span></span>
-   <span data-ttu-id="75620-110">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-110">Electricity</span></span>
-   <span data-ttu-id="75620-111">Hallinnon palkat</span><span class="sxs-lookup"><span data-stu-id="75620-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="75620-112">Yleiskustannuslaskennan yleiskuva</span><span class="sxs-lookup"><span data-stu-id="75620-112">Overhead calculation overview</span></span>
<span data-ttu-id="75620-113">Yleiskustannusten laskenta suorittaa kustannuslaskennan käytännöt oikeassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="75620-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="75620-114">Yleiskustannusten laskennan voi suorittaa useita kertoja samalle tilikaudelle, jos kustannuslaskennan käytännöt ovat muuttuneet tai erityisiä virheitä on havaittu.</span><span class="sxs-lookup"><span data-stu-id="75620-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="75620-115">Kukin laskenta-ajo tallennetaan ja kullekin annetaan yksilöllinen versiotunnus, jonka avulla eri laskenta-ajoja voi verrata toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="75620-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="75620-116">Yleiskustannusten laskenta luo kustannustapahtumia, joille annetaan kirjauspäivä.</span><span class="sxs-lookup"><span data-stu-id="75620-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="75620-117">Kirjauspäivä vastaa laskennassa käytettyä tilikauden päättymispäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="75620-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="75620-118">Yksilöivä versiotunnus sisältää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="75620-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="75620-119">Versiotyyppi</span><span class="sxs-lookup"><span data-stu-id="75620-119">Version type</span></span>
-   <span data-ttu-id="75620-120">Päivämäärä ja aika</span><span class="sxs-lookup"><span data-stu-id="75620-120">Date and time</span></span>
-   <span data-ttu-id="75620-121">Kustannuslaskennan kirjanpito</span><span class="sxs-lookup"><span data-stu-id="75620-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="75620-122">Tilikausi </span><span class="sxs-lookup"><span data-stu-id="75620-122">Fiscal year</span></span>
-   <span data-ttu-id="75620-123">Tilikausi  </span><span class="sxs-lookup"><span data-stu-id="75620-123">Fiscal period</span></span>

<span data-ttu-id="75620-124">Yleiskustannusten laskenta ajetaan versiosta riippumattomana.</span><span class="sxs-lookup"><span data-stu-id="75620-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="75620-125">Voit siis laskea budjetin version ennen todellista versiota.</span><span class="sxs-lookup"><span data-stu-id="75620-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="75620-126">Yleiskustannusten laskenta koostuu neljästä vaiheesta, jotka esitellään seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="75620-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="75620-127">Kussakin vaiheessa luodaan kirjauskansion otsikko, jolla on kirjauskansiovientejä.</span><span class="sxs-lookup"><span data-stu-id="75620-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="75620-128">Tämä kirjauskansion otsikko säilyttää kunkin laskentavaiheen syöttötiedot.</span><span class="sxs-lookup"><span data-stu-id="75620-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="75620-129">Käytännöt ja säännöt ajetaan kullekin kirjauskansion riville, ja tuloksena luodaan kustannustapahtumia.</span><span class="sxs-lookup"><span data-stu-id="75620-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="75620-130">Tämän ansiosta kaikki laskutoimitukset ovat täysin jäljitettävissä.</span><span class="sxs-lookup"><span data-stu-id="75620-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="75620-131">[![Yleiskustannuslaskenta](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="75620-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="75620-132">Laske ja kohdista sähkön yleiskustannukset</span><span class="sxs-lookup"><span data-stu-id="75620-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="75620-133">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="75620-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="75620-134">Tarkka johdon näkymä ei täten ole saatavilla kustannuslaskennassa.</span><span class="sxs-lookup"><span data-stu-id="75620-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="75620-135">Jotta kustannuslaskenta tarjoaisi oikean johdon näkymän kaikista organisaation yksiköistä ja tasoista, kustannusten on virrattava organisaation yksiköiden läpi.</span><span class="sxs-lookup"><span data-stu-id="75620-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="75620-136">Tämän virran on perustuttava joko tarkkaan tietoon kulutuksesta tai perusteltuun arvioon.</span><span class="sxs-lookup"><span data-stu-id="75620-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="75620-137">Sähkökustannukset voi kirjata kirjanpitoon seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="75620-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="75620-138">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="75620-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="75620-139">Kustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="75620-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="75620-140">Päätili</span><span class="sxs-lookup"><span data-stu-id="75620-140">Main account</span></span></th>
<th><span data-ttu-id="75620-141">Summa kirjanpitovaluuttana</span><span class="sxs-lookup"><span data-stu-id="75620-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-142">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="75620-143">CC099</span><span class="sxs-lookup"><span data-stu-id="75620-143">CC099</span></span></td>
<td><span data-ttu-id="75620-144">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="75620-144">Default cost center</span></span></td>
<td><span data-ttu-id="75620-145">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-145">10001</span></span></td>
<td><span data-ttu-id="75620-146">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-146">Electricity</span></span></td>
<td><span data-ttu-id="75620-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="75620-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="75620-148">Vaihe 1: Käsittele kustannustoiminnan laskenta</span><span class="sxs-lookup"><span data-stu-id="75620-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="75620-149">Kun kustannustapahtumat tuodaan lähdetiedoista, niille asetetaan kustannuslaskennassa oletusarvoisesti **Luokittelematon** -kustannustoimintaluokka.</span><span class="sxs-lookup"><span data-stu-id="75620-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="75620-150">Voit luokitella kustannustapahtumia uudelleen **kiinteäksi kustannukseksi** tai **muuttuvaksi kustannukseksi** kustannustoiminnan käytäntösäännöillä.</span><span class="sxs-lookup"><span data-stu-id="75620-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="75620-151">Määritä kustannustoiminnan sääntö</span><span class="sxs-lookup"><span data-stu-id="75620-151">Define the cost behavior rule</span></span>

<span data-ttu-id="75620-152">Joissain tapauksissa osa kustannuksesta on kiinteä ja loppuosa perustuu kulutukseen.</span><span class="sxs-lookup"><span data-stu-id="75620-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="75620-153">Sähkölaskut sopivat usein tähän määritelmään.</span><span class="sxs-lookup"><span data-stu-id="75620-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="75620-154">Maksat ensin määrätyn, kiinteän maksun, jonka lisäksi maksat kulutuksesta kilowattitunteina (kWh).</span><span class="sxs-lookup"><span data-stu-id="75620-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="75620-155">Jos kiinteä maksu on esimerkiksi 1 000,00, kustannustoiminnan sääntö määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="75620-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="75620-156">Kiinteä määrä 1 000,00</span><span class="sxs-lookup"><span data-stu-id="75620-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="75620-157">0 &lt;= 1 000,00 = Kiinteä</span><span class="sxs-lookup"><span data-stu-id="75620-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="75620-158">1000,01 &lt; N = Muuttuva</span><span class="sxs-lookup"><span data-stu-id="75620-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="75620-159">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="75620-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="75620-160">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="75620-160">Journal</span></span></th>
<th><span data-ttu-id="75620-161">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="75620-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="75620-162">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="75620-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="75620-163">Versio</span><span class="sxs-lookup"><span data-stu-id="75620-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-164">00001</span><span class="sxs-lookup"><span data-stu-id="75620-164">00001</span></span></td>
<td><span data-ttu-id="75620-165">Kustannustoiminnan laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="75620-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="75620-166">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="75620-166">Fiscal</span></span></td>
<td><span data-ttu-id="75620-167">2017</span><span class="sxs-lookup"><span data-stu-id="75620-167">2017</span></span></td>
<td><span data-ttu-id="75620-168">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="75620-168">Period 1</span></span></td>
<td><span data-ttu-id="75620-169">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="75620-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="75620-170">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="75620-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="75620-171">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="75620-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="75620-172">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="75620-173">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="75620-173">Cost element</span></span></th>
<th><span data-ttu-id="75620-174">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="75620-174">Cost behavior</span></span></th>
<th><span data-ttu-id="75620-175">Summa</span><span class="sxs-lookup"><span data-stu-id="75620-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-176">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="75620-177">CC099</span><span class="sxs-lookup"><span data-stu-id="75620-177">CC099</span></span></td>
<td><span data-ttu-id="75620-178">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="75620-178">Default cost center</span></span></td>
<td><span data-ttu-id="75620-179">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-179">10001</span></span></td>
<td><span data-ttu-id="75620-180">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-180">Electricity</span></span></td>
<td><span data-ttu-id="75620-181">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="75620-181">Unclassified</span></span></td>
<td><span data-ttu-id="75620-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="75620-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="75620-183">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="75620-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75620-184">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="75620-185">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="75620-185">Cost element</span></span></th>
<th><span data-ttu-id="75620-186">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="75620-186">Cost behavior</span></span></th>
<th><span data-ttu-id="75620-187">Summa</span><span class="sxs-lookup"><span data-stu-id="75620-187">Amount</span></span></th>
<th><span data-ttu-id="75620-188">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="75620-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-189">CC099</span><span class="sxs-lookup"><span data-stu-id="75620-189">CC099</span></span></td>
<td><span data-ttu-id="75620-190">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="75620-190">Default cost center</span></span></td>
<td><span data-ttu-id="75620-191">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-191">10001</span></span></td>
<td><span data-ttu-id="75620-192">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-192">Electricity</span></span></td>
<td><span data-ttu-id="75620-193">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="75620-193">Unclassified</span></span></td>
<td><span data-ttu-id="75620-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="75620-194">10,000.00</span></span></td>
<td><span data-ttu-id="75620-195">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-196">CC099</span><span class="sxs-lookup"><span data-stu-id="75620-196">CC099</span></span></td>
<td><span data-ttu-id="75620-197">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="75620-197">Default cost center</span></span></td>
<td><span data-ttu-id="75620-198">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-198">10001</span></span></td>
<td><span data-ttu-id="75620-199">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-199">Electricity</span></span></td>
<td><span data-ttu-id="75620-200">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="75620-200">Unclassified</span></span></td>
<td><span data-ttu-id="75620-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="75620-201">-10,000.00</span></span></td>
<td><span data-ttu-id="75620-202">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-203">CC099</span><span class="sxs-lookup"><span data-stu-id="75620-203">CC099</span></span></td>
<td><span data-ttu-id="75620-204">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="75620-204">Default cost center</span></span></td>
<td><span data-ttu-id="75620-205">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-205">10001</span></span></td>
<td><span data-ttu-id="75620-206">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-206">Electricity</span></span></td>
<td><span data-ttu-id="75620-207">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-207">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="75620-208">1,000.00</span></span></td>
<td><span data-ttu-id="75620-209">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-210">CC099</span><span class="sxs-lookup"><span data-stu-id="75620-210">CC099</span></span></td>
<td><span data-ttu-id="75620-211">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="75620-211">Default cost center</span></span></td>
<td><span data-ttu-id="75620-212">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-212">10001</span></span></td>
<td><span data-ttu-id="75620-213">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-213">Electricity</span></span></td>
<td><span data-ttu-id="75620-214">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-214">Variable cost</span></span></td>
<td><span data-ttu-id="75620-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="75620-215">9,000.00</span></span></td>
<td><span data-ttu-id="75620-216">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75620-217">Lisätietoja on kohdassa [Kustannustoimintakäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="75620-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="75620-218">Vaihe 2: Käsittele kustannusten jaon laskenta</span><span class="sxs-lookup"><span data-stu-id="75620-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="75620-219">Kustannusten jakoa käytetään kustannusten jakamiseen yhdestä kustannusobjektista toiseen (tai useampaan kustannusobjektiin) määrittämällä asiaankuuluvan kohdistusperusteen.</span><span class="sxs-lookup"><span data-stu-id="75620-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="75620-220">Kustannusten jako ja kustannusten kohdistus eroavat toisistaan sillä, että kustannusten jako tapahtuu aina alkuperäisen kustannuksen ensisijaisen kustannuselementin tasolla.</span><span class="sxs-lookup"><span data-stu-id="75620-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="75620-221">Määritä kustannusten jaon sääntö</span><span class="sxs-lookup"><span data-stu-id="75620-221">Define the cost distribution rule</span></span>

<span data-ttu-id="75620-222">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="75620-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="75620-223">Kustannuslaskenta ei tarjoa tästä tarpeeksi tarkkoja tietoja.</span><span class="sxs-lookup"><span data-stu-id="75620-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="75620-224">Muuttuva kustannus tulisi jakaa yksittäisille kustannusobjekteille reiluin perustein.</span><span class="sxs-lookup"><span data-stu-id="75620-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="75620-225">Loogisin kohdistusperuste on sähkönkulutus (kWh).</span><span class="sxs-lookup"><span data-stu-id="75620-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="75620-226">Luodaan tilastollinen dimensionjäsen nimeltä Sähkö, johon kirjataan sähkönkulutus.</span><span class="sxs-lookup"><span data-stu-id="75620-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="75620-227">Oletusarvon mukaan kaikki tilastolliset dimensiojäsenet ovat käytettävissä kohdistusperusteina.</span><span class="sxs-lookup"><span data-stu-id="75620-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75620-228">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-228">Cost object</span></span></th>
<th><span data-ttu-id="75620-229">kWh</span><span class="sxs-lookup"><span data-stu-id="75620-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-230">CC001</span><span class="sxs-lookup"><span data-stu-id="75620-230">CC001</span></span></td>
<td><span data-ttu-id="75620-231">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="75620-231">HR</span></span></td>
<td><span data-ttu-id="75620-232">1 000</span><span class="sxs-lookup"><span data-stu-id="75620-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-233">CC002</span><span class="sxs-lookup"><span data-stu-id="75620-233">CC002</span></span></td>
<td><span data-ttu-id="75620-234">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="75620-234">Finance</span></span></td>
<td><span data-ttu-id="75620-235">6,000</span><span class="sxs-lookup"><span data-stu-id="75620-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-236">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-236">CC003</span></span></td>
<td><span data-ttu-id="75620-237">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="75620-237">Assembly</span></span></td>
<td><span data-ttu-id="75620-238">0</span><span class="sxs-lookup"><span data-stu-id="75620-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75620-239">Seuraavassa taulukossa on esitetty tulos, kun sähkönkulutusta käytetään kohdistusperusteena muuttuville kuluille.</span><span class="sxs-lookup"><span data-stu-id="75620-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75620-240">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-240">Cost object</span></span></th>
<th><span data-ttu-id="75620-241">Suuruus</span><span class="sxs-lookup"><span data-stu-id="75620-241">Magnitude</span></span></th>
<th><span data-ttu-id="75620-242">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="75620-242">Allocation factor</span></span></th>
<th><span data-ttu-id="75620-243">Summa</span><span class="sxs-lookup"><span data-stu-id="75620-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-244">CC001</span><span class="sxs-lookup"><span data-stu-id="75620-244">CC001</span></span></td>
<td><span data-ttu-id="75620-245">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="75620-245">HR</span></span></td>
<td><span data-ttu-id="75620-246">1 000</span><span class="sxs-lookup"><span data-stu-id="75620-246">1,000</span></span></td>
<td><span data-ttu-id="75620-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="75620-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="75620-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="75620-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-249">CC002</span><span class="sxs-lookup"><span data-stu-id="75620-249">CC002</span></span></td>
<td><span data-ttu-id="75620-250">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="75620-250">Finance</span></span></td>
<td><span data-ttu-id="75620-251">6,000</span><span class="sxs-lookup"><span data-stu-id="75620-251">6,000</span></span></td>
<td><span data-ttu-id="75620-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="75620-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="75620-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="75620-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-254">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-254">CC003</span></span></td>
<td><span data-ttu-id="75620-255">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="75620-255">Assembly</span></span></td>
<td><span data-ttu-id="75620-256">0</span><span class="sxs-lookup"><span data-stu-id="75620-256">0</span></span></td>
<td><span data-ttu-id="75620-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="75620-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="75620-258">0,00</span><span class="sxs-lookup"><span data-stu-id="75620-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75620-259">Kiinteä kustannus tulisi jakaa tasaisesti yksittäisille kustannusobjekteille, jotka ovat kuluttaneet sähköä.</span><span class="sxs-lookup"><span data-stu-id="75620-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="75620-260">Voit käyttää sähkön tilastollista dimensiojäsentä kaavan kohdistusperusteena tämän tavoitteen saavuttamiseksi: (sähkö &gt;0,00) Seuraavassa taulukossa on esitetty tulos siitä, kun sähkönkulutus on määritetty muuttuvien kustannusten kohdistusperusteeksi.</span><span class="sxs-lookup"><span data-stu-id="75620-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75620-261">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-261">Cost object</span></span></th>
<th><span data-ttu-id="75620-262">Resepti</span><span class="sxs-lookup"><span data-stu-id="75620-262">Formula</span></span></th>
<th><span data-ttu-id="75620-263">Suuruus</span><span class="sxs-lookup"><span data-stu-id="75620-263">Magnitude</span></span></th>
<th><span data-ttu-id="75620-264">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="75620-264">Allocation factor</span></span></th>
<th><span data-ttu-id="75620-265">Summa</span><span class="sxs-lookup"><span data-stu-id="75620-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-266">CC001</span><span class="sxs-lookup"><span data-stu-id="75620-266">CC001</span></span></td>
<td><span data-ttu-id="75620-267">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="75620-267">HR</span></span></td>
<td><span data-ttu-id="75620-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="75620-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="75620-269">1</span><span class="sxs-lookup"><span data-stu-id="75620-269">1</span></span></td>
<td><span data-ttu-id="75620-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="75620-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="75620-271">500,00</span><span class="sxs-lookup"><span data-stu-id="75620-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-272">CC002</span><span class="sxs-lookup"><span data-stu-id="75620-272">CC002</span></span></td>
<td><span data-ttu-id="75620-273">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="75620-273">Finance</span></span></td>
<td><span data-ttu-id="75620-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="75620-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="75620-275">1</span><span class="sxs-lookup"><span data-stu-id="75620-275">1</span></span></td>
<td><span data-ttu-id="75620-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="75620-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="75620-277">500,00</span><span class="sxs-lookup"><span data-stu-id="75620-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-278">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-278">CC003</span></span></td>
<td><span data-ttu-id="75620-279">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="75620-279">Assembly</span></span></td>
<td><span data-ttu-id="75620-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="75620-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="75620-281">0</span><span class="sxs-lookup"><span data-stu-id="75620-281">0</span></span></td>
<td><span data-ttu-id="75620-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="75620-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="75620-283">0,00</span><span class="sxs-lookup"><span data-stu-id="75620-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="75620-284">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="75620-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="75620-285">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="75620-285">Journal</span></span></th>
<th><span data-ttu-id="75620-286">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="75620-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="75620-287">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="75620-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="75620-288">Versio</span><span class="sxs-lookup"><span data-stu-id="75620-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-289">00002</span><span class="sxs-lookup"><span data-stu-id="75620-289">00002</span></span></td>
<td><span data-ttu-id="75620-290">Kustannusten jaon laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="75620-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="75620-291">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="75620-291">Fiscal</span></span></td>
<td><span data-ttu-id="75620-292">2017</span><span class="sxs-lookup"><span data-stu-id="75620-292">2017</span></span></td>
<td><span data-ttu-id="75620-293">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="75620-293">Period 1</span></span></td>
<td><span data-ttu-id="75620-294">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="75620-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="75620-295">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="75620-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="75620-296">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="75620-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="75620-297">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="75620-298">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="75620-298">Cost element</span></span></th>
<th><span data-ttu-id="75620-299">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="75620-299">Cost behavior</span></span></th>
<th><span data-ttu-id="75620-300">Summa</span><span class="sxs-lookup"><span data-stu-id="75620-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-301">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="75620-302">CC099</span><span class="sxs-lookup"><span data-stu-id="75620-302">CC099</span></span></td>
<td><span data-ttu-id="75620-303">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="75620-303">Default cost center</span></span></td>
<td><span data-ttu-id="75620-304">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-304">10001</span></span></td>
<td><span data-ttu-id="75620-305">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-305">Electricity</span></span></td>
<td><span data-ttu-id="75620-306">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-306">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="75620-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-308">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="75620-309">CC099</span><span class="sxs-lookup"><span data-stu-id="75620-309">CC099</span></span></td>
<td><span data-ttu-id="75620-310">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="75620-310">Default cost center</span></span></td>
<td><span data-ttu-id="75620-311">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-311">10001</span></span></td>
<td><span data-ttu-id="75620-312">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-312">Electricity</span></span></td>
<td><span data-ttu-id="75620-313">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-313">Variable cost</span></span></td>
<td><span data-ttu-id="75620-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="75620-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="75620-315">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="75620-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75620-316">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="75620-317">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="75620-317">Cost element</span></span></th>
<th><span data-ttu-id="75620-318">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="75620-318">Cost behavior</span></span></th>
<th><span data-ttu-id="75620-319">Summa</span><span class="sxs-lookup"><span data-stu-id="75620-319">Amount</span></span></th>
<th><span data-ttu-id="75620-320">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="75620-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-321">CC099</span><span class="sxs-lookup"><span data-stu-id="75620-321">CC099</span></span></td>
<td><span data-ttu-id="75620-322">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="75620-322">Default cost center</span></span></td>
<td><span data-ttu-id="75620-323">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-323">10001</span></span></td>
<td><span data-ttu-id="75620-324">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-324">Electricity</span></span></td>
<td><span data-ttu-id="75620-325">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-325">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="75620-326">-1,000.00</span></span></td>
<td><span data-ttu-id="75620-327">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-328">CC001</span><span class="sxs-lookup"><span data-stu-id="75620-328">CC001</span></span></td>
<td><span data-ttu-id="75620-329">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="75620-329">HR</span></span></td>
<td><span data-ttu-id="75620-330">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-330">10001</span></span></td>
<td><span data-ttu-id="75620-331">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-331">Electricity</span></span></td>
<td><span data-ttu-id="75620-332">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-332">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-333">500,00</span><span class="sxs-lookup"><span data-stu-id="75620-333">500.00</span></span></td>
<td><span data-ttu-id="75620-334">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-335">CC002</span><span class="sxs-lookup"><span data-stu-id="75620-335">CC002</span></span></td>
<td><span data-ttu-id="75620-336">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="75620-336">Finance</span></span></td>
<td><span data-ttu-id="75620-337">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-337">10001</span></span></td>
<td><span data-ttu-id="75620-338">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-338">Electricity</span></span></td>
<td><span data-ttu-id="75620-339">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-339">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-340">500,00</span><span class="sxs-lookup"><span data-stu-id="75620-340">500.00</span></span></td>
<td><span data-ttu-id="75620-341">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-342">CC099</span><span class="sxs-lookup"><span data-stu-id="75620-342">CC099</span></span></td>
<td><span data-ttu-id="75620-343">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="75620-343">Default cost center</span></span></td>
<td><span data-ttu-id="75620-344">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-344">10001</span></span></td>
<td><span data-ttu-id="75620-345">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-345">Electricity</span></span></td>
<td><span data-ttu-id="75620-346">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-346">Variable cost</span></span></td>
<td><span data-ttu-id="75620-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="75620-347">-9,000.00</span></span></td>
<td><span data-ttu-id="75620-348">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-349">CC001</span><span class="sxs-lookup"><span data-stu-id="75620-349">CC001</span></span></td>
<td><span data-ttu-id="75620-350">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="75620-350">HR</span></span></td>
<td><span data-ttu-id="75620-351">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-351">10001</span></span></td>
<td><span data-ttu-id="75620-352">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-352">Electricity</span></span></td>
<td><span data-ttu-id="75620-353">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-353">Variable cost</span></span></td>
<td><span data-ttu-id="75620-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="75620-354">1,285.71</span></span></td>
<td><span data-ttu-id="75620-355">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-356">CC002</span><span class="sxs-lookup"><span data-stu-id="75620-356">CC002</span></span></td>
<td><span data-ttu-id="75620-357">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="75620-357">Finance</span></span></td>
<td><span data-ttu-id="75620-358">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-358">10001</span></span></td>
<td><span data-ttu-id="75620-359">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-359">Electricity</span></span></td>
<td><span data-ttu-id="75620-360">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-360">Variable cost</span></span></td>
<td><span data-ttu-id="75620-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="75620-361">7,714.29</span></span></td>
<td><span data-ttu-id="75620-362">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75620-363">Lisätietoja on kohdassa [Jakelukäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="75620-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="75620-364">Vaihe 3: Käsittele yleiskustannustason laskenta</span><span class="sxs-lookup"><span data-stu-id="75620-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="75620-365">Yleiskustannustasolla veloitetaan yksi tai useampi määrätty kustannusobjekti.</span><span class="sxs-lookup"><span data-stu-id="75620-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="75620-366">Veloitus perustuu ennalta määrättyyn kustannustasoon sekä määritetyn kohdistusperusteen suuruuteen.</span><span class="sxs-lookup"><span data-stu-id="75620-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="75620-367">Määritä yleiskustannustaso.</span><span class="sxs-lookup"><span data-stu-id="75620-367">Define the overhead rate</span></span>

<span data-ttu-id="75620-368">Kustannusobjekti CC001 HR vaikuttaa joukkoon sisäisiä projekteja.</span><span class="sxs-lookup"><span data-stu-id="75620-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="75620-369">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon projektit.</span><span class="sxs-lookup"><span data-stu-id="75620-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75620-370">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-370">Cost object</span></span></th>
<th><span data-ttu-id="75620-371">Tunnit</span><span class="sxs-lookup"><span data-stu-id="75620-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="75620-372">Proj 1</span></span></td>
<td><span data-ttu-id="75620-373">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="75620-373">Project 1</span></span></td>
<td><span data-ttu-id="75620-374">3</span><span class="sxs-lookup"><span data-stu-id="75620-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="75620-375">Proj 2</span></span></td>
<td><span data-ttu-id="75620-376">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="75620-376">Project 2</span></span></td>
<td><span data-ttu-id="75620-377">1</span><span class="sxs-lookup"><span data-stu-id="75620-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75620-378">Kustannusprojektien osuudelle on määritetty ennalta kustannushinta.</span><span class="sxs-lookup"><span data-stu-id="75620-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75620-379">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-379">Cost object</span></span></th>
<th><span data-ttu-id="75620-380">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="75620-380">Cost element</span></span></th>
<th><span data-ttu-id="75620-381">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="75620-381">Cost behavior</span></span></th>
<th><span data-ttu-id="75620-382">Yksiköt</span><span class="sxs-lookup"><span data-stu-id="75620-382">Units</span></span></th>
<th><span data-ttu-id="75620-383">Osuus</span><span class="sxs-lookup"><span data-stu-id="75620-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-384">CC001</span><span class="sxs-lookup"><span data-stu-id="75620-384">CC001</span></span></td>
<td><span data-ttu-id="75620-385">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="75620-385">HR</span></span></td>
<td><span data-ttu-id="75620-386">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-386">10001</span></span></td>
<td><span data-ttu-id="75620-387">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-387">Variable cost</span></span></td>
<td><span data-ttu-id="75620-388">1</span><span class="sxs-lookup"><span data-stu-id="75620-388">1</span></span></td>
<td><span data-ttu-id="75620-389">10</span><span class="sxs-lookup"><span data-stu-id="75620-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75620-390">Seuraavassa taulukossa on esitetty tulos, kun Henkilöstöhallinnon projekteja käytetään kohdistusperusteena.</span><span class="sxs-lookup"><span data-stu-id="75620-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75620-391">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-391">Cost object</span></span></th>
<th><span data-ttu-id="75620-392">Suuruus</span><span class="sxs-lookup"><span data-stu-id="75620-392">Magnitude</span></span></th>
<th><span data-ttu-id="75620-393">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="75620-393">Cost element</span></span></th>
<th><span data-ttu-id="75620-394">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="75620-394">Allocation factor</span></span></th>
<th><span data-ttu-id="75620-395">Summa</span><span class="sxs-lookup"><span data-stu-id="75620-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="75620-396">Proj 1</span></span></td>
<td><span data-ttu-id="75620-397">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="75620-397">Project 1</span></span></td>
<td><span data-ttu-id="75620-398">3</span><span class="sxs-lookup"><span data-stu-id="75620-398">3</span></span></td>
<td><span data-ttu-id="75620-399">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-399">10001</span></span></td>
<td><span data-ttu-id="75620-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="75620-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="75620-401">30,00</span><span class="sxs-lookup"><span data-stu-id="75620-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="75620-402">Proj 2</span></span></td>
<td><span data-ttu-id="75620-403">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="75620-403">Project 2</span></span></td>
<td><span data-ttu-id="75620-404">1</span><span class="sxs-lookup"><span data-stu-id="75620-404">1</span></span></td>
<td><span data-ttu-id="75620-405">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-405">10001</span></span></td>
<td><span data-ttu-id="75620-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="75620-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="75620-407">10,00</span><span class="sxs-lookup"><span data-stu-id="75620-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="75620-408">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="75620-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="75620-409">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="75620-409">Journal</span></span></th>
<th><span data-ttu-id="75620-410">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="75620-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="75620-411">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="75620-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="75620-412">Versio</span><span class="sxs-lookup"><span data-stu-id="75620-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-413">00003</span><span class="sxs-lookup"><span data-stu-id="75620-413">00003</span></span></td>
<td><span data-ttu-id="75620-414">Yleiskustannustason laskelman kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="75620-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="75620-415">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="75620-415">Fiscal</span></span></td>
<td><span data-ttu-id="75620-416">2017</span><span class="sxs-lookup"><span data-stu-id="75620-416">2017</span></span></td>
<td><span data-ttu-id="75620-417">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="75620-417">Period 1</span></span></td>
<td><span data-ttu-id="75620-418">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="75620-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="75620-419">Kirjauskansioviennit (Yleiskustannustason laskennan kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="75620-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="75620-420">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="75620-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="75620-421">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-421">Cost object</span></span></th>
<th><span data-ttu-id="75620-422">Suuruus</span><span class="sxs-lookup"><span data-stu-id="75620-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-423">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="75620-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="75620-424">Proj 1</span></span></td>
<td><span data-ttu-id="75620-425">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="75620-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="75620-426">3,00</span><span class="sxs-lookup"><span data-stu-id="75620-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-427">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="75620-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="75620-428">Proj 2</span></span></td>
<td><span data-ttu-id="75620-429">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="75620-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="75620-430">1,00</span><span class="sxs-lookup"><span data-stu-id="75620-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="75620-431">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="75620-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75620-432">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="75620-433">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="75620-433">Cost element</span></span></th>
<th><span data-ttu-id="75620-434">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="75620-434">Cost behavior</span></span></th>
<th><span data-ttu-id="75620-435">Summa</span><span class="sxs-lookup"><span data-stu-id="75620-435">Amount</span></span></th>
<th><span data-ttu-id="75620-436">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="75620-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="75620-437">CC0001</span></span></td>
<td><span data-ttu-id="75620-438">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="75620-438">HR</span></span></td>
<td><span data-ttu-id="75620-439">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-439">10001</span></span></td>
<td><span data-ttu-id="75620-440">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-440">Electricity</span></span></td>
<td><span data-ttu-id="75620-441">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-441">Variable cost</span></span></td>
<td><span data-ttu-id="75620-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="75620-442">-30.00</span></span></td>
<td><span data-ttu-id="75620-443">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="75620-444">Proj 1</span></span></td>
<td><span data-ttu-id="75620-445">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="75620-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="75620-446">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-446">10001</span></span></td>
<td><span data-ttu-id="75620-447">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-447">Electricity</span></span></td>
<td><span data-ttu-id="75620-448">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-448">Variable cost</span></span></td>
<td><span data-ttu-id="75620-449">30,00</span><span class="sxs-lookup"><span data-stu-id="75620-449">30.00</span></span></td>
<td><span data-ttu-id="75620-450">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-451">CC001</span><span class="sxs-lookup"><span data-stu-id="75620-451">CC001</span></span></td>
<td><span data-ttu-id="75620-452">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="75620-452">HR</span></span></td>
<td><span data-ttu-id="75620-453">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-453">10001</span></span></td>
<td><span data-ttu-id="75620-454">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-454">Electricity</span></span></td>
<td><span data-ttu-id="75620-455">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-455">Variable cost</span></span></td>
<td><span data-ttu-id="75620-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="75620-456">-10.00</span></span></td>
<td><span data-ttu-id="75620-457">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="75620-458">Proj 2</span></span></td>
<td><span data-ttu-id="75620-459">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="75620-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="75620-460">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-460">10001</span></span></td>
<td><span data-ttu-id="75620-461">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-461">Electricity</span></span></td>
<td><span data-ttu-id="75620-462">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-462">Variable cost</span></span></td>
<td><span data-ttu-id="75620-463">10.00</span><span class="sxs-lookup"><span data-stu-id="75620-463">10.00</span></span></td>
<td><span data-ttu-id="75620-464">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75620-465">Lisätietoja on kohdassa [Yleisen laskennan suorittaminen](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="75620-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="75620-466">Vaihe 4: Käsittele kustannusten kohdistuksen laskenta</span><span class="sxs-lookup"><span data-stu-id="75620-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="75620-467">Kohdistuksella kustannusobjektin saldo liitetään toisiin kustannusobjekteihin käyttämällä kohdistusperustetta.</span><span class="sxs-lookup"><span data-stu-id="75620-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="75620-468">Finance and Operations tukee vastavuoroista kohdistusmenetelmää.</span><span class="sxs-lookup"><span data-stu-id="75620-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="75620-469">Vastavuoroisessa kohdistusmenetelmässä tunnistetaan oheiskustannusobjektien käyttämät, keskinäiset palvelut täysin.</span><span class="sxs-lookup"><span data-stu-id="75620-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="75620-470">Järjestelmä määrittää oikean kohdistusjärjestyksen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="75620-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="75620-471">Kustannusobjektin saldo kohdistetaan yhdellä kohdistusperusteella.</span><span class="sxs-lookup"><span data-stu-id="75620-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="75620-472">Kustannusobjektien dimensiot ja niiden vastaavat jäsenet ylittävät kohdistukset ovat tuettuja.</span><span class="sxs-lookup"><span data-stu-id="75620-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="75620-473">Kustannusseurantayksikkö hallitsee kohdistusjärjestystä.</span><span class="sxs-lookup"><span data-stu-id="75620-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="75620-474">[![Vastavuoroinen menetelmä](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="75620-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="75620-475">Määritä kustannuksen kohdistus</span><span class="sxs-lookup"><span data-stu-id="75620-475">Define the cost allocation</span></span>

<span data-ttu-id="75620-476">Tämä on yksinkertainen esimerkki, jossa kerrotaan, miten voit jäljittää kustannuksen virran.</span><span class="sxs-lookup"><span data-stu-id="75620-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="75620-477">Kustannusobjekti CC001 HR liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="75620-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="75620-478">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="75620-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75620-479">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-479">Cost object</span></span></th>
<th><span data-ttu-id="75620-480">HR-palvelut</span><span class="sxs-lookup"><span data-stu-id="75620-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-481">CC002</span><span class="sxs-lookup"><span data-stu-id="75620-481">CC002</span></span></td>
<td><span data-ttu-id="75620-482">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="75620-482">Finance</span></span></td>
<td><span data-ttu-id="75620-483">35</span><span class="sxs-lookup"><span data-stu-id="75620-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-484">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-484">CC003</span></span></td>
<td><span data-ttu-id="75620-485">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="75620-485">Assembly</span></span></td>
<td><span data-ttu-id="75620-486">55</span><span class="sxs-lookup"><span data-stu-id="75620-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-487">CC004</span><span class="sxs-lookup"><span data-stu-id="75620-487">CC004</span></span></td>
<td><span data-ttu-id="75620-488">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="75620-488">Packaging</span></span></td>
<td><span data-ttu-id="75620-489">10</span><span class="sxs-lookup"><span data-stu-id="75620-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75620-490">Kustannusobjekti CC002 Taloushallinto liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="75620-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="75620-491">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Taloushallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="75620-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75620-492">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-492">Cost object</span></span></th>
<th><span data-ttu-id="75620-493">Taloushallinnon palvelut</span><span class="sxs-lookup"><span data-stu-id="75620-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-494">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-494">CC003</span></span></td>
<td><span data-ttu-id="75620-495">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="75620-495">Assembly</span></span></td>
<td><span data-ttu-id="75620-496">65</span><span class="sxs-lookup"><span data-stu-id="75620-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-497">CC004</span><span class="sxs-lookup"><span data-stu-id="75620-497">CC004</span></span></td>
<td><span data-ttu-id="75620-498">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="75620-498">Packaging</span></span></td>
<td><span data-ttu-id="75620-499">35</span><span class="sxs-lookup"><span data-stu-id="75620-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75620-500">Kustannusobjekti CC003 Kokoonpano liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="75620-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="75620-501">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Kokoonpanopalvelut.</span><span class="sxs-lookup"><span data-stu-id="75620-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75620-502">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-502">Cost object</span></span></th>
<th><span data-ttu-id="75620-503">Kokoonpanopalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="75620-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-504">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-504">Prod 1</span></span></td>
<td><span data-ttu-id="75620-505">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-505">Product 1</span></span></td>
<td><span data-ttu-id="75620-506">60</span><span class="sxs-lookup"><span data-stu-id="75620-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-507">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-507">Prod 2</span></span></td>
<td><span data-ttu-id="75620-508">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-508">Product 2</span></span></td>
<td><span data-ttu-id="75620-509">20</span><span class="sxs-lookup"><span data-stu-id="75620-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75620-510">Kustannusobjekti CC004 Pakkaus liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="75620-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="75620-511">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Pakkauspalvelut.</span><span class="sxs-lookup"><span data-stu-id="75620-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75620-512">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-512">Cost object</span></span></th>
<th><span data-ttu-id="75620-513">Pakkauspalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="75620-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-514">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-514">Prod 1</span></span></td>
<td><span data-ttu-id="75620-515">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-515">Product 1</span></span></td>
<td><span data-ttu-id="75620-516">80</span><span class="sxs-lookup"><span data-stu-id="75620-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-517">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-517">Prod 2</span></span></td>
<td><span data-ttu-id="75620-518">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-518">Product 2</span></span></td>
<td><span data-ttu-id="75620-519">päivänä</span><span class="sxs-lookup"><span data-stu-id="75620-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="75620-520">Finance and Operationsissa tilastomittaukset, kuten tämän tuotteen kuluttamat tuotantotunnit, voidaan johtaa lähdetiedoista.</span><span class="sxs-lookup"><span data-stu-id="75620-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="75620-521">Lisätietoja on kohdassa [Tilastomittauksen lähdemalli](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="75620-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="75620-522">Seuraavassa taulukossa näytetään tulos, kun henkilöstöhallinnon palveluja käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="75620-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75620-523">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-523">Cost object</span></span></th>
<th><span data-ttu-id="75620-524">Suuruus</span><span class="sxs-lookup"><span data-stu-id="75620-524">Magnitude</span></span></th>
<th><span data-ttu-id="75620-525">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="75620-525">Allocation factor</span></span></th>
<th><span data-ttu-id="75620-526">Summa</span><span class="sxs-lookup"><span data-stu-id="75620-526">Amount</span></span></th>
<th><span data-ttu-id="75620-527">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="75620-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-528">CC002</span><span class="sxs-lookup"><span data-stu-id="75620-528">CC002</span></span></td>
<td><span data-ttu-id="75620-529">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="75620-529">Finance</span></span></td>
<td><span data-ttu-id="75620-530">35</span><span class="sxs-lookup"><span data-stu-id="75620-530">35</span></span></td>
<td><span data-ttu-id="75620-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="75620-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="75620-532">175.00</span><span class="sxs-lookup"><span data-stu-id="75620-532">175.00</span></span></td>
<td><span data-ttu-id="75620-533">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-534">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-534">CC003</span></span></td>
<td><span data-ttu-id="75620-535">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="75620-535">Assembly</span></span></td>
<td><span data-ttu-id="75620-536">55</span><span class="sxs-lookup"><span data-stu-id="75620-536">55</span></span></td>
<td><span data-ttu-id="75620-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="75620-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="75620-538">275.00</span><span class="sxs-lookup"><span data-stu-id="75620-538">275.00</span></span></td>
<td><span data-ttu-id="75620-539">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-540">CC004</span><span class="sxs-lookup"><span data-stu-id="75620-540">CC004</span></span></td>
<td><span data-ttu-id="75620-541">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="75620-541">Packaging</span></span></td>
<td><span data-ttu-id="75620-542">10</span><span class="sxs-lookup"><span data-stu-id="75620-542">10</span></span></td>
<td><span data-ttu-id="75620-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="75620-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="75620-544">50,00</span><span class="sxs-lookup"><span data-stu-id="75620-544">50.00</span></span></td>
<td><span data-ttu-id="75620-545">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-546">CC002</span><span class="sxs-lookup"><span data-stu-id="75620-546">CC002</span></span></td>
<td><span data-ttu-id="75620-547">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="75620-547">Finance</span></span></td>
<td><span data-ttu-id="75620-548">35</span><span class="sxs-lookup"><span data-stu-id="75620-548">35</span></span></td>
<td><span data-ttu-id="75620-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="75620-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="75620-550">436.00</span><span class="sxs-lookup"><span data-stu-id="75620-550">436.00</span></span></td>
<td><span data-ttu-id="75620-551">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-552">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-552">CC003</span></span></td>
<td><span data-ttu-id="75620-553">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="75620-553">Assembly</span></span></td>
<td><span data-ttu-id="75620-554">55</span><span class="sxs-lookup"><span data-stu-id="75620-554">55</span></span></td>
<td><span data-ttu-id="75620-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="75620-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="75620-556">685.14</span><span class="sxs-lookup"><span data-stu-id="75620-556">685.14</span></span></td>
<td><span data-ttu-id="75620-557">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-558">CC004</span><span class="sxs-lookup"><span data-stu-id="75620-558">CC004</span></span></td>
<td><span data-ttu-id="75620-559">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="75620-559">Packaging</span></span></td>
<td><span data-ttu-id="75620-560">10</span><span class="sxs-lookup"><span data-stu-id="75620-560">10</span></span></td>
<td><span data-ttu-id="75620-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="75620-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="75620-562">124.57</span><span class="sxs-lookup"><span data-stu-id="75620-562">124.57</span></span></td>
<td><span data-ttu-id="75620-563">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75620-564">Seuraavassa taulukossa näytetään tulos, kun Taloushallinnon palveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="75620-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75620-565">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-565">Cost object</span></span></th>
<th><span data-ttu-id="75620-566">Suuruus</span><span class="sxs-lookup"><span data-stu-id="75620-566">Magnitude</span></span></th>
<th><span data-ttu-id="75620-567">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="75620-567">Allocation factor</span></span></th>
<th><span data-ttu-id="75620-568">Summa</span><span class="sxs-lookup"><span data-stu-id="75620-568">Amount</span></span></th>
<th><span data-ttu-id="75620-569">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="75620-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-570">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-570">CC003</span></span></td>
<td><span data-ttu-id="75620-571">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="75620-571">Assembly</span></span></td>
<td><span data-ttu-id="75620-572">65</span><span class="sxs-lookup"><span data-stu-id="75620-572">65</span></span></td>
<td><span data-ttu-id="75620-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="75620-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="75620-574">438.75</span><span class="sxs-lookup"><span data-stu-id="75620-574">438.75</span></span></td>
<td><span data-ttu-id="75620-575">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-576">CC004</span><span class="sxs-lookup"><span data-stu-id="75620-576">CC004</span></span></td>
<td><span data-ttu-id="75620-577">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="75620-577">Packaging</span></span></td>
<td><span data-ttu-id="75620-578">35</span><span class="sxs-lookup"><span data-stu-id="75620-578">35</span></span></td>
<td><span data-ttu-id="75620-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="75620-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="75620-580">236.25</span><span class="sxs-lookup"><span data-stu-id="75620-580">236.25</span></span></td>
<td><span data-ttu-id="75620-581">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-582">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-582">CC003</span></span></td>
<td><span data-ttu-id="75620-583">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="75620-583">Assembly</span></span></td>
<td><span data-ttu-id="75620-584">65</span><span class="sxs-lookup"><span data-stu-id="75620-584">65</span></span></td>
<td><span data-ttu-id="75620-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="75620-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="75620-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="75620-586">5,297.69</span></span></td>
<td><span data-ttu-id="75620-587">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-588">CC004</span><span class="sxs-lookup"><span data-stu-id="75620-588">CC004</span></span></td>
<td><span data-ttu-id="75620-589">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="75620-589">Packaging</span></span></td>
<td><span data-ttu-id="75620-590">35</span><span class="sxs-lookup"><span data-stu-id="75620-590">35</span></span></td>
<td><span data-ttu-id="75620-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="75620-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="75620-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="75620-592">2,852.60</span></span></td>
<td><span data-ttu-id="75620-593">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75620-594">Seuraavassa taulukossa näytetään tulos, kun Kokoonpanopalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="75620-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75620-595">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-595">Cost object</span></span></th>
<th><span data-ttu-id="75620-596">Suuruus</span><span class="sxs-lookup"><span data-stu-id="75620-596">Magnitude</span></span></th>
<th><span data-ttu-id="75620-597">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="75620-597">Allocation factor</span></span></th>
<th><span data-ttu-id="75620-598">Summa</span><span class="sxs-lookup"><span data-stu-id="75620-598">Amount</span></span></th>
<th><span data-ttu-id="75620-599">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="75620-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-600">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-600">Prod 1</span></span></td>
<td><span data-ttu-id="75620-601">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-601">Product 1</span></span></td>
<td><span data-ttu-id="75620-602">60</span><span class="sxs-lookup"><span data-stu-id="75620-602">60</span></span></td>
<td><span data-ttu-id="75620-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="75620-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="75620-604">535.31</span><span class="sxs-lookup"><span data-stu-id="75620-604">535.31</span></span></td>
<td><span data-ttu-id="75620-605">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-606">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-606">Prod 2</span></span></td>
<td><span data-ttu-id="75620-607">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-607">Product 2</span></span></td>
<td><span data-ttu-id="75620-608">20</span><span class="sxs-lookup"><span data-stu-id="75620-608">20</span></span></td>
<td><span data-ttu-id="75620-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="75620-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="75620-610">178.44</span><span class="sxs-lookup"><span data-stu-id="75620-610">178.44</span></span></td>
<td><span data-ttu-id="75620-611">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-612">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-612">Prod 1</span></span></td>
<td><span data-ttu-id="75620-613">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-613">Product 1</span></span></td>
<td><span data-ttu-id="75620-614">60</span><span class="sxs-lookup"><span data-stu-id="75620-614">60</span></span></td>
<td><span data-ttu-id="75620-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="75620-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="75620-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="75620-616">4,487.12</span></span></td>
<td><span data-ttu-id="75620-617">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-618">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-618">Prod 2</span></span></td>
<td><span data-ttu-id="75620-619">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-619">Product 2</span></span></td>
<td><span data-ttu-id="75620-620">20</span><span class="sxs-lookup"><span data-stu-id="75620-620">20</span></span></td>
<td><span data-ttu-id="75620-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="75620-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="75620-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="75620-622">1,495.71</span></span></td>
<td><span data-ttu-id="75620-623">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75620-624">Seuraavassa taulukossa näytetään tulos, kun Pakkauspalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="75620-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75620-625">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-625">Cost object</span></span></th>
<th><span data-ttu-id="75620-626">Suuruus</span><span class="sxs-lookup"><span data-stu-id="75620-626">Magnitude</span></span></th>
<th><span data-ttu-id="75620-627">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="75620-627">Allocation factor</span></span></th>
<th><span data-ttu-id="75620-628">Summa</span><span class="sxs-lookup"><span data-stu-id="75620-628">Amount</span></span></th>
<th><span data-ttu-id="75620-629">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="75620-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-630">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-630">Prod 1</span></span></td>
<td><span data-ttu-id="75620-631">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-631">Product 1</span></span></td>
<td><span data-ttu-id="75620-632">80</span><span class="sxs-lookup"><span data-stu-id="75620-632">80</span></span></td>
<td><span data-ttu-id="75620-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="75620-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="75620-634">241.05</span><span class="sxs-lookup"><span data-stu-id="75620-634">241.05</span></span></td>
<td><span data-ttu-id="75620-635">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-636">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-636">Prod 2</span></span></td>
<td><span data-ttu-id="75620-637">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-637">Product 2</span></span></td>
<td><span data-ttu-id="75620-638">15</span><span class="sxs-lookup"><span data-stu-id="75620-638">15</span></span></td>
<td><span data-ttu-id="75620-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="75620-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="75620-640">45.20</span><span class="sxs-lookup"><span data-stu-id="75620-640">45.20</span></span></td>
<td><span data-ttu-id="75620-641">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-642">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-642">Prod 1</span></span></td>
<td><span data-ttu-id="75620-643">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-643">Product 1</span></span></td>
<td><span data-ttu-id="75620-644">80</span><span class="sxs-lookup"><span data-stu-id="75620-644">80</span></span></td>
<td><span data-ttu-id="75620-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="75620-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="75620-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="75620-646">2,507.09</span></span></td>
<td><span data-ttu-id="75620-647">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-648">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-648">Prod 2</span></span></td>
<td><span data-ttu-id="75620-649">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-649">Product 2</span></span></td>
<td><span data-ttu-id="75620-650">15</span><span class="sxs-lookup"><span data-stu-id="75620-650">15</span></span></td>
<td><span data-ttu-id="75620-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="75620-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="75620-652">470.08</span><span class="sxs-lookup"><span data-stu-id="75620-652">470.08</span></span></td>
<td><span data-ttu-id="75620-653">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="75620-654">Kirjauskansioviennit (kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="75620-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="75620-655">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="75620-655">Journal</span></span></th>
<th><span data-ttu-id="75620-656">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="75620-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="75620-657">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="75620-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="75620-658">Versio</span><span class="sxs-lookup"><span data-stu-id="75620-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-659">00004</span><span class="sxs-lookup"><span data-stu-id="75620-659">00004</span></span></td>
<td><span data-ttu-id="75620-660">Kustannusten kohdistuskirjauskansio</span><span class="sxs-lookup"><span data-stu-id="75620-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="75620-661">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="75620-661">Fiscal</span></span></td>
<td><span data-ttu-id="75620-662">2017</span><span class="sxs-lookup"><span data-stu-id="75620-662">2017</span></span></td>
<td><span data-ttu-id="75620-663">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="75620-663">Period 1</span></span></td>
<td><span data-ttu-id="75620-664">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="75620-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="75620-665">Kirjauskansion rivit</span><span class="sxs-lookup"><span data-stu-id="75620-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="75620-666">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="75620-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="75620-667">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="75620-668">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="75620-668">Cost element</span></span></th>
<th><span data-ttu-id="75620-669">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="75620-669">Cost behavior</span></span></th>
<th><span data-ttu-id="75620-670">Summa</span><span class="sxs-lookup"><span data-stu-id="75620-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-671">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="75620-672">CC001</span><span class="sxs-lookup"><span data-stu-id="75620-672">CC001</span></span></td>
<td><span data-ttu-id="75620-673">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="75620-673">HR</span></span></td>
<td><span data-ttu-id="75620-674">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-674">10001</span></span></td>
<td><span data-ttu-id="75620-675">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-675">Electricity</span></span></td>
<td><span data-ttu-id="75620-676">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-676">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-677">500,00</span><span class="sxs-lookup"><span data-stu-id="75620-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-678">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="75620-679">CC001</span><span class="sxs-lookup"><span data-stu-id="75620-679">CC001</span></span></td>
<td><span data-ttu-id="75620-680">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="75620-680">HR</span></span></td>
<td><span data-ttu-id="75620-681">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-681">10001</span></span></td>
<td><span data-ttu-id="75620-682">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-682">Electricity</span></span></td>
<td><span data-ttu-id="75620-683">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-683">Variable cost</span></span></td>
<td><span data-ttu-id="75620-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="75620-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-685">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="75620-686">CC002</span><span class="sxs-lookup"><span data-stu-id="75620-686">CC002</span></span></td>
<td><span data-ttu-id="75620-687">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="75620-687">Finance</span></span></td>
<td><span data-ttu-id="75620-688">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-688">10001</span></span></td>
<td><span data-ttu-id="75620-689">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-689">Electricity</span></span></td>
<td><span data-ttu-id="75620-690">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-690">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-691">675.00</span><span class="sxs-lookup"><span data-stu-id="75620-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-692">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="75620-693">CC002</span><span class="sxs-lookup"><span data-stu-id="75620-693">CC002</span></span></td>
<td><span data-ttu-id="75620-694">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="75620-694">Finance</span></span></td>
<td><span data-ttu-id="75620-695">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-695">10001</span></span></td>
<td><span data-ttu-id="75620-696">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-696">Electricity</span></span></td>
<td><span data-ttu-id="75620-697">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-697">Variable cost</span></span></td>
<td><span data-ttu-id="75620-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="75620-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-699">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="75620-700">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-700">CC003</span></span></td>
<td><span data-ttu-id="75620-701">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="75620-701">Assembly</span></span></td>
<td><span data-ttu-id="75620-702">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-702">10001</span></span></td>
<td><span data-ttu-id="75620-703">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-703">Electricity</span></span></td>
<td><span data-ttu-id="75620-704">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-704">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-705">713.75</span><span class="sxs-lookup"><span data-stu-id="75620-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-706">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="75620-707">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-707">CC003</span></span></td>
<td><span data-ttu-id="75620-708">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="75620-708">Assembly</span></span></td>
<td><span data-ttu-id="75620-709">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-709">10001</span></span></td>
<td><span data-ttu-id="75620-710">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-710">Electricity</span></span></td>
<td><span data-ttu-id="75620-711">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-711">Variable cost</span></span></td>
<td><span data-ttu-id="75620-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="75620-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-713">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="75620-714">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-714">CC003</span></span></td>
<td><span data-ttu-id="75620-715">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="75620-715">Packaging</span></span></td>
<td><span data-ttu-id="75620-716">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-716">10001</span></span></td>
<td><span data-ttu-id="75620-717">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-717">Electricity</span></span></td>
<td><span data-ttu-id="75620-718">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-718">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-719">286.25</span><span class="sxs-lookup"><span data-stu-id="75620-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-720">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="75620-721">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-721">CC003</span></span></td>
<td><span data-ttu-id="75620-722">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="75620-722">Packaging</span></span></td>
<td><span data-ttu-id="75620-723">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-723">10001</span></span></td>
<td><span data-ttu-id="75620-724">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-724">Electricity</span></span></td>
<td><span data-ttu-id="75620-725">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-725">Variable cost</span></span></td>
<td><span data-ttu-id="75620-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="75620-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-727">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="75620-728">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-728">Prod 1</span></span></td>
<td><span data-ttu-id="75620-729">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-729">Product 1</span></span></td>
<td><span data-ttu-id="75620-730">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-730">10001</span></span></td>
<td><span data-ttu-id="75620-731">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-731">Electricity</span></span></td>
<td><span data-ttu-id="75620-732">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-732">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-733">776.36</span><span class="sxs-lookup"><span data-stu-id="75620-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-734">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="75620-735">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-735">Prod 1</span></span></td>
<td><span data-ttu-id="75620-736">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-736">Product 1</span></span></td>
<td><span data-ttu-id="75620-737">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-737">10001</span></span></td>
<td><span data-ttu-id="75620-738">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-738">Electricity</span></span></td>
<td><span data-ttu-id="75620-739">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-739">Variable cost</span></span></td>
<td><span data-ttu-id="75620-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="75620-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-741">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="75620-742">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-742">Prod 2</span></span></td>
<td><span data-ttu-id="75620-743">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-743">Product 1</span></span></td>
<td><span data-ttu-id="75620-744">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-744">10001</span></span></td>
<td><span data-ttu-id="75620-745">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-745">Electricity</span></span></td>
<td><span data-ttu-id="75620-746">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-746">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-747">223.64</span><span class="sxs-lookup"><span data-stu-id="75620-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-748">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="75620-749">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-749">Prod 2</span></span></td>
<td><span data-ttu-id="75620-750">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-750">Product 1</span></span></td>
<td><span data-ttu-id="75620-751">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-751">10001</span></span></td>
<td><span data-ttu-id="75620-752">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-752">Electricity</span></span></td>
<td><span data-ttu-id="75620-753">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-753">Variable cost</span></span></td>
<td><span data-ttu-id="75620-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="75620-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="75620-755">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="75620-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75620-756">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="75620-757">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="75620-757">Cost element</span></span></th>
<th><span data-ttu-id="75620-758">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="75620-758">Cost behavior</span></span></th>
<th><span data-ttu-id="75620-759">Summa</span><span class="sxs-lookup"><span data-stu-id="75620-759">Amount</span></span></th>
<th><span data-ttu-id="75620-760">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="75620-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75620-761">CC001</span><span class="sxs-lookup"><span data-stu-id="75620-761">CC001</span></span></td>
<td><span data-ttu-id="75620-762">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="75620-762">HR</span></span></td>
<td><span data-ttu-id="75620-763">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-763">10001</span></span></td>
<td><span data-ttu-id="75620-764">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-764">Electricity</span></span></td>
<td><span data-ttu-id="75620-765">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-765">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="75620-766">-500.00</span></span></td>
<td><span data-ttu-id="75620-767">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-768">CC002</span><span class="sxs-lookup"><span data-stu-id="75620-768">CC002</span></span></td>
<td><span data-ttu-id="75620-769">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="75620-769">Finance</span></span></td>
<td><span data-ttu-id="75620-770">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-770">10001</span></span></td>
<td><span data-ttu-id="75620-771">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-771">Electricity</span></span></td>
<td><span data-ttu-id="75620-772">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-772">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-773">175.00</span><span class="sxs-lookup"><span data-stu-id="75620-773">175.00</span></span></td>
<td><span data-ttu-id="75620-774">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-775">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-775">CC003</span></span></td>
<td><span data-ttu-id="75620-776">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="75620-776">Assembly</span></span></td>
<td><span data-ttu-id="75620-777">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-777">10001</span></span></td>
<td><span data-ttu-id="75620-778">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-778">Electricity</span></span></td>
<td><span data-ttu-id="75620-779">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-779">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-780">275.00</span><span class="sxs-lookup"><span data-stu-id="75620-780">275.00</span></span></td>
<td><span data-ttu-id="75620-781">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-782">CC004</span><span class="sxs-lookup"><span data-stu-id="75620-782">CC004</span></span></td>
<td><span data-ttu-id="75620-783">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="75620-783">Packaging</span></span></td>
<td><span data-ttu-id="75620-784">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-784">10001</span></span></td>
<td><span data-ttu-id="75620-785">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-785">Electricity</span></span></td>
<td><span data-ttu-id="75620-786">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-786">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-787">50,00</span><span class="sxs-lookup"><span data-stu-id="75620-787">50,00</span></span></td>
<td><span data-ttu-id="75620-788">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-789">CC001</span><span class="sxs-lookup"><span data-stu-id="75620-789">CC001</span></span></td>
<td><span data-ttu-id="75620-790">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="75620-790">HR</span></span></td>
<td><span data-ttu-id="75620-791">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-791">10001</span></span></td>
<td><span data-ttu-id="75620-792">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-792">Electricity</span></span></td>
<td><span data-ttu-id="75620-793">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-793">Variable cost</span></span></td>
<td><span data-ttu-id="75620-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="75620-794">-1,245.71</span></span></td>
<td><span data-ttu-id="75620-795">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-796">CC002</span><span class="sxs-lookup"><span data-stu-id="75620-796">CC002</span></span></td>
<td><span data-ttu-id="75620-797">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="75620-797">Finance</span></span></td>
<td><span data-ttu-id="75620-798">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-798">10001</span></span></td>
<td><span data-ttu-id="75620-799">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-799">Electricity</span></span></td>
<td><span data-ttu-id="75620-800">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-800">Variable cost</span></span></td>
<td><span data-ttu-id="75620-801">436.00</span><span class="sxs-lookup"><span data-stu-id="75620-801">436.00</span></span></td>
<td><span data-ttu-id="75620-802">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-803">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-803">CC003</span></span></td>
<td><span data-ttu-id="75620-804">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="75620-804">Assembly</span></span></td>
<td><span data-ttu-id="75620-805">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-805">10001</span></span></td>
<td><span data-ttu-id="75620-806">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-806">Electricity</span></span></td>
<td><span data-ttu-id="75620-807">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-807">Variable cost</span></span></td>
<td><span data-ttu-id="75620-808">685.14</span><span class="sxs-lookup"><span data-stu-id="75620-808">685.14</span></span></td>
<td><span data-ttu-id="75620-809">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-810">CC004</span><span class="sxs-lookup"><span data-stu-id="75620-810">CC004</span></span></td>
<td><span data-ttu-id="75620-811">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="75620-811">Packaging</span></span></td>
<td><span data-ttu-id="75620-812">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-812">10001</span></span></td>
<td><span data-ttu-id="75620-813">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-813">Electricity</span></span></td>
<td><span data-ttu-id="75620-814">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-814">Variable cost</span></span></td>
<td><span data-ttu-id="75620-815">124.57</span><span class="sxs-lookup"><span data-stu-id="75620-815">124.57</span></span></td>
<td><span data-ttu-id="75620-816">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-817">CC002</span><span class="sxs-lookup"><span data-stu-id="75620-817">CC002</span></span></td>
<td><span data-ttu-id="75620-818">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="75620-818">Finance</span></span></td>
<td><span data-ttu-id="75620-819">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-819">10001</span></span></td>
<td><span data-ttu-id="75620-820">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-820">Electricity</span></span></td>
<td><span data-ttu-id="75620-821">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-821">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="75620-822">-675.00</span></span></td>
<td><span data-ttu-id="75620-823">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-824">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-824">CC003</span></span></td>
<td><span data-ttu-id="75620-825">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="75620-825">Assembly</span></span></td>
<td><span data-ttu-id="75620-826">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-826">10001</span></span></td>
<td><span data-ttu-id="75620-827">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-827">Electricity</span></span></td>
<td><span data-ttu-id="75620-828">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-828">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-829">438.75</span><span class="sxs-lookup"><span data-stu-id="75620-829">438.75</span></span></td>
<td><span data-ttu-id="75620-830">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-831">CC004</span><span class="sxs-lookup"><span data-stu-id="75620-831">CC004</span></span></td>
<td><span data-ttu-id="75620-832">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="75620-832">Packaging</span></span></td>
<td><span data-ttu-id="75620-833">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-833">10001</span></span></td>
<td><span data-ttu-id="75620-834">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-834">Electricity</span></span></td>
<td><span data-ttu-id="75620-835">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-835">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-836">236.25</span><span class="sxs-lookup"><span data-stu-id="75620-836">236.25</span></span></td>
<td><span data-ttu-id="75620-837">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-838">CC002</span><span class="sxs-lookup"><span data-stu-id="75620-838">CC002</span></span></td>
<td><span data-ttu-id="75620-839">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="75620-839">Finance</span></span></td>
<td><span data-ttu-id="75620-840">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-840">10001</span></span></td>
<td><span data-ttu-id="75620-841">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-841">Electricity</span></span></td>
<td><span data-ttu-id="75620-842">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-842">Variable cost</span></span></td>
<td><span data-ttu-id="75620-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="75620-843">-8,150.29</span></span></td>
<td><span data-ttu-id="75620-844">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-845">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-845">CC003</span></span></td>
<td><span data-ttu-id="75620-846">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="75620-846">Assembly</span></span></td>
<td><span data-ttu-id="75620-847">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-847">10001</span></span></td>
<td><span data-ttu-id="75620-848">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-848">Electricity</span></span></td>
<td><span data-ttu-id="75620-849">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-849">Variable cost</span></span></td>
<td><span data-ttu-id="75620-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="75620-850">5,297.69</span></span></td>
<td><span data-ttu-id="75620-851">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-852">CC004</span><span class="sxs-lookup"><span data-stu-id="75620-852">CC004</span></span></td>
<td><span data-ttu-id="75620-853">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="75620-853">Packaging</span></span></td>
<td><span data-ttu-id="75620-854">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-854">10001</span></span></td>
<td><span data-ttu-id="75620-855">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-855">Electricity</span></span></td>
<td><span data-ttu-id="75620-856">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-856">Variable cost</span></span></td>
<td><span data-ttu-id="75620-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="75620-857">2,852.60</span></span></td>
<td><span data-ttu-id="75620-858">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-859">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-859">CC003</span></span></td>
<td><span data-ttu-id="75620-860">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="75620-860">Assembly</span></span></td>
<td><span data-ttu-id="75620-861">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-861">10001</span></span></td>
<td><span data-ttu-id="75620-862">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-862">Electricity</span></span></td>
<td><span data-ttu-id="75620-863">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-863">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="75620-864">-713.75</span></span></td>
<td><span data-ttu-id="75620-865">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-866">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-866">Prod 1</span></span></td>
<td><span data-ttu-id="75620-867">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-867">Product 1</span></span></td>
<td><span data-ttu-id="75620-868">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-868">10001</span></span></td>
<td><span data-ttu-id="75620-869">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-869">Electricity</span></span></td>
<td><span data-ttu-id="75620-870">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-870">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-871">535.31</span><span class="sxs-lookup"><span data-stu-id="75620-871">535.31</span></span></td>
<td><span data-ttu-id="75620-872">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-873">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-873">Prod 2</span></span></td>
<td><span data-ttu-id="75620-874">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-874">Product 2</span></span></td>
<td><span data-ttu-id="75620-875">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-875">10001</span></span></td>
<td><span data-ttu-id="75620-876">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-876">Electricity</span></span></td>
<td><span data-ttu-id="75620-877">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-877">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-878">178.44</span><span class="sxs-lookup"><span data-stu-id="75620-878">178.44</span></span></td>
<td><span data-ttu-id="75620-879">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-880">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-880">CC003</span></span></td>
<td><span data-ttu-id="75620-881">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="75620-881">Assembly</span></span></td>
<td><span data-ttu-id="75620-882">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-882">10001</span></span></td>
<td><span data-ttu-id="75620-883">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-883">Electricity</span></span></td>
<td><span data-ttu-id="75620-884">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-884">Variable cost</span></span></td>
<td><span data-ttu-id="75620-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="75620-885">-5,982.83</span></span></td>
<td><span data-ttu-id="75620-886">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-887">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-887">Prod 1</span></span></td>
<td><span data-ttu-id="75620-888">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-888">Product 1</span></span></td>
<td><span data-ttu-id="75620-889">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-889">10001</span></span></td>
<td><span data-ttu-id="75620-890">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-890">Electricity</span></span></td>
<td><span data-ttu-id="75620-891">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-891">Variable cost</span></span></td>
<td><span data-ttu-id="75620-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="75620-892">4,487.12</span></span></td>
<td><span data-ttu-id="75620-893">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-894">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-894">Prod 2</span></span></td>
<td><span data-ttu-id="75620-895">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-895">Product 2</span></span></td>
<td><span data-ttu-id="75620-896">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-896">10001</span></span></td>
<td><span data-ttu-id="75620-897">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-897">Electricity</span></span></td>
<td><span data-ttu-id="75620-898">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-898">Variable cost</span></span></td>
<td><span data-ttu-id="75620-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="75620-899">1,495.71</span></span></td>
<td><span data-ttu-id="75620-900">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-901">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-901">CC003</span></span></td>
<td><span data-ttu-id="75620-902">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="75620-902">Assembly</span></span></td>
<td><span data-ttu-id="75620-903">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-903">10001</span></span></td>
<td><span data-ttu-id="75620-904">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-904">Electricity</span></span></td>
<td><span data-ttu-id="75620-905">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-905">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="75620-906">-286.25</span></span></td>
<td><span data-ttu-id="75620-907">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-908">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-908">Prod 1</span></span></td>
<td><span data-ttu-id="75620-909">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-909">Product 1</span></span></td>
<td><span data-ttu-id="75620-910">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-910">10001</span></span></td>
<td><span data-ttu-id="75620-911">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-911">Electricity</span></span></td>
<td><span data-ttu-id="75620-912">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-912">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-913">241.05</span><span class="sxs-lookup"><span data-stu-id="75620-913">241.05</span></span></td>
<td><span data-ttu-id="75620-914">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-915">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-915">Prod 2</span></span></td>
<td><span data-ttu-id="75620-916">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-916">Product 2</span></span></td>
<td><span data-ttu-id="75620-917">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-917">10001</span></span></td>
<td><span data-ttu-id="75620-918">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-918">Electricity</span></span></td>
<td><span data-ttu-id="75620-919">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-919">Fixed cost</span></span></td>
<td><span data-ttu-id="75620-920">45.20</span><span class="sxs-lookup"><span data-stu-id="75620-920">45.20</span></span></td>
<td><span data-ttu-id="75620-921">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-922">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-922">CC003</span></span></td>
<td><span data-ttu-id="75620-923">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="75620-923">Assembly</span></span></td>
<td><span data-ttu-id="75620-924">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-924">10001</span></span></td>
<td><span data-ttu-id="75620-925">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-925">Electricity</span></span></td>
<td><span data-ttu-id="75620-926">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-926">Variable cost</span></span></td>
<td><span data-ttu-id="75620-927">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="75620-927">-2,977.17</span></span></td>
<td><span data-ttu-id="75620-928">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-929">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-929">Prod 1</span></span></td>
<td><span data-ttu-id="75620-930">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-930">Product 1</span></span></td>
<td><span data-ttu-id="75620-931">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-931">10001</span></span></td>
<td><span data-ttu-id="75620-932">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-932">Electricity</span></span></td>
<td><span data-ttu-id="75620-933">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-933">Variable cost</span></span></td>
<td><span data-ttu-id="75620-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="75620-934">2,507.09</span></span></td>
<td><span data-ttu-id="75620-935">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75620-936">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-936">Prod 2</span></span></td>
<td><span data-ttu-id="75620-937">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-937">Product 2</span></span></td>
<td><span data-ttu-id="75620-938">10 001</span><span class="sxs-lookup"><span data-stu-id="75620-938">10001</span></span></td>
<td><span data-ttu-id="75620-939">Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-939">Electricity</span></span></td>
<td><span data-ttu-id="75620-940">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-940">Variable cost</span></span></td>
<td><span data-ttu-id="75620-941">470.08</span><span class="sxs-lookup"><span data-stu-id="75620-941">470.08</span></span></td>
<td><span data-ttu-id="75620-942">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="75620-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="75620-943">Johtopäätökset</span><span class="sxs-lookup"><span data-stu-id="75620-943">Conclusion</span></span>
<span data-ttu-id="75620-944">Kirjanpidossa kirjataan tyhjään kustannuspaikkatunnukseen sähkökustannus arvolla 10 000,00.</span><span class="sxs-lookup"><span data-stu-id="75620-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="75620-945">Tämän ansiosta kustannuslaskijat tietävät, että kustannus on kohdistettava.</span><span class="sxs-lookup"><span data-stu-id="75620-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="75620-946">Kustannukset virtaavat kirjanpidossa organisaation yksiköiden ja tasojen läpi käytössä olevien käytäntöjen ja sääntöjen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="75620-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="75620-947">Kukin kustannus on liitetty kustannusperusteeseen, joka sisältää parhaan arvion kustannusten kohdistuksesta.</span><span class="sxs-lookup"><span data-stu-id="75620-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="75620-948">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="75620-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="75620-949">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="75620-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="75620-950">Yhteensä</span><span class="sxs-lookup"><span data-stu-id="75620-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="75620-951">CC099</span><span class="sxs-lookup"><span data-stu-id="75620-951">CC099</span></span></th>
<th><span data-ttu-id="75620-952">CC001</span><span class="sxs-lookup"><span data-stu-id="75620-952">CC001</span></span></th>
<th><span data-ttu-id="75620-953">CC002</span><span class="sxs-lookup"><span data-stu-id="75620-953">CC002</span></span></th>
<th><span data-ttu-id="75620-954">CC003</span><span class="sxs-lookup"><span data-stu-id="75620-954">CC003</span></span></th>
<th><span data-ttu-id="75620-955">CC004</span><span class="sxs-lookup"><span data-stu-id="75620-955">CC004</span></span></th>
<th><span data-ttu-id="75620-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="75620-956">Proj 1</span></span></th>
<th><span data-ttu-id="75620-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="75620-957">Proj 2</span></span></th>
<th><span data-ttu-id="75620-958">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="75620-958">Prod 1</span></span></th>
<th><span data-ttu-id="75620-959">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="75620-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="75620-960">10001 Sähkö</span><span class="sxs-lookup"><span data-stu-id="75620-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="75620-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="75620-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="75620-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="75620-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="75620-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="75620-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="75620-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="75620-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="75620-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="75620-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="75620-970">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="75620-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-971">0,00</span><span class="sxs-lookup"><span data-stu-id="75620-971">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="75620-972">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="75620-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-973">0,00</span><span class="sxs-lookup"><span data-stu-id="75620-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-974">0,00</span><span class="sxs-lookup"><span data-stu-id="75620-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-975">0,00</span><span class="sxs-lookup"><span data-stu-id="75620-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-976">0,00</span><span class="sxs-lookup"><span data-stu-id="75620-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-977">0,00</span><span class="sxs-lookup"><span data-stu-id="75620-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="75620-978">776.36</span><span class="sxs-lookup"><span data-stu-id="75620-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-979">223.64</span><span class="sxs-lookup"><span data-stu-id="75620-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="75620-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="75620-981">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="75620-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-982">000</span><span class="sxs-lookup"><span data-stu-id="75620-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-983">0,00</span><span class="sxs-lookup"><span data-stu-id="75620-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-984">0,00</span><span class="sxs-lookup"><span data-stu-id="75620-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-985">0,00</span><span class="sxs-lookup"><span data-stu-id="75620-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-986">0,00</span><span class="sxs-lookup"><span data-stu-id="75620-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-987">30,00</span><span class="sxs-lookup"><span data-stu-id="75620-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-988">10,00</span><span class="sxs-lookup"><span data-stu-id="75620-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="75620-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="75620-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75620-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="75620-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="75620-992">Tässä ohjeaiheessa esitellään, miten ensisijainen kustannuselementti, 10001 Sähkö, virtaa kustannusobjektien läpi.</span><span class="sxs-lookup"><span data-stu-id="75620-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="75620-993">Tästä syystä tämä yleiskustannus kohdistetaan organisaation alimmalle tasolle.</span><span class="sxs-lookup"><span data-stu-id="75620-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="75620-994">Toisin sanoen alimman tason kustannusobjektit kantavat kustannuksen.</span><span class="sxs-lookup"><span data-stu-id="75620-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="75620-995">Jos tarvitset visuaalisen näkymän kustannuksen virrasta kustannusobjektien välillä, voit käyttää kustannuksen koontikäytäntösääntöjä kustannusvirran visualisointiin.</span><span class="sxs-lookup"><span data-stu-id="75620-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="75620-996">Lisätietoja on kohdassa [Kustannusten koonti](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="75620-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



