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
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "335114"
---
# <a name="overhead-calculation"></a><span data-ttu-id="e74e6-103">Yleiskustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="e74e6-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e74e6-104">Tässä aiheessa kuvataan tyypillinen yleiskustannusten laskenta- ja kohdistusprosessi.</span><span class="sxs-lookup"><span data-stu-id="e74e6-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="e74e6-105">Sanaston määritelmä</span><span class="sxs-lookup"><span data-stu-id="e74e6-105">Term definition</span></span>
---------------

<span data-ttu-id="e74e6-106">Yleiskustannukset ovat yrityksen toiminnasta syntyviä kustannuksia, joita ei voi suoraan liittää mihinkään tiettyyn liiketoiminnan tehtävään, tuotteeseen tai palveluun.</span><span class="sxs-lookup"><span data-stu-id="e74e6-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="e74e6-107">Yleiskustannukset ovat tärkeä tuki voittoa tuottavien tehtävien luonnissa.</span><span class="sxs-lookup"><span data-stu-id="e74e6-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="e74e6-108">Seuraavassa on joitakin esimerkkejä yleiskustannuksista:</span><span class="sxs-lookup"><span data-stu-id="e74e6-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="e74e6-109">Vuokra</span><span class="sxs-lookup"><span data-stu-id="e74e6-109">Rent</span></span>
-   <span data-ttu-id="e74e6-110">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-110">Electricity</span></span>
-   <span data-ttu-id="e74e6-111">Hallinnon palkat</span><span class="sxs-lookup"><span data-stu-id="e74e6-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="e74e6-112">Yleiskustannuslaskennan yleiskuva</span><span class="sxs-lookup"><span data-stu-id="e74e6-112">Overhead calculation overview</span></span>
<span data-ttu-id="e74e6-113">Yleiskustannusten laskenta suorittaa kustannuslaskennan käytännöt oikeassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="e74e6-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="e74e6-114">Yleiskustannusten laskennan voi suorittaa useita kertoja samalle tilikaudelle, jos kustannuslaskennan käytännöt ovat muuttuneet tai erityisiä virheitä on havaittu.</span><span class="sxs-lookup"><span data-stu-id="e74e6-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="e74e6-115">Kukin laskenta-ajo tallennetaan ja kullekin annetaan yksilöllinen versiotunnus, jonka avulla eri laskenta-ajoja voi verrata toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="e74e6-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="e74e6-116">Yleiskustannusten laskenta luo kustannustapahtumia, joille annetaan kirjauspäivä.</span><span class="sxs-lookup"><span data-stu-id="e74e6-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="e74e6-117">Kirjauspäivä vastaa laskennassa käytettyä tilikauden päättymispäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="e74e6-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="e74e6-118">Yksilöivä versiotunnus sisältää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="e74e6-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="e74e6-119">Versiotyyppi</span><span class="sxs-lookup"><span data-stu-id="e74e6-119">Version type</span></span>
-   <span data-ttu-id="e74e6-120">Päivämäärä ja aika</span><span class="sxs-lookup"><span data-stu-id="e74e6-120">Date and time</span></span>
-   <span data-ttu-id="e74e6-121">Kustannuslaskennan kirjanpito</span><span class="sxs-lookup"><span data-stu-id="e74e6-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="e74e6-122">Tilikausi </span><span class="sxs-lookup"><span data-stu-id="e74e6-122">Fiscal year</span></span>
-   <span data-ttu-id="e74e6-123">Tilikausi  </span><span class="sxs-lookup"><span data-stu-id="e74e6-123">Fiscal period</span></span>

<span data-ttu-id="e74e6-124">Yleiskustannusten laskenta ajetaan versiosta riippumattomana.</span><span class="sxs-lookup"><span data-stu-id="e74e6-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="e74e6-125">Voit siis laskea budjetin version ennen todellista versiota.</span><span class="sxs-lookup"><span data-stu-id="e74e6-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="e74e6-126">Yleiskustannusten laskenta koostuu neljästä vaiheesta, jotka esitellään seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="e74e6-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="e74e6-127">Kussakin vaiheessa luodaan kirjauskansion otsikko, jolla on kirjauskansiovientejä.</span><span class="sxs-lookup"><span data-stu-id="e74e6-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="e74e6-128">Tämä kirjauskansion otsikko säilyttää kunkin laskentavaiheen syöttötiedot.</span><span class="sxs-lookup"><span data-stu-id="e74e6-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="e74e6-129">Käytännöt ja säännöt ajetaan kullekin kirjauskansion riville, ja tuloksena luodaan kustannustapahtumia.</span><span class="sxs-lookup"><span data-stu-id="e74e6-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="e74e6-130">Tämän ansiosta kaikki laskutoimitukset ovat täysin jäljitettävissä.</span><span class="sxs-lookup"><span data-stu-id="e74e6-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="e74e6-131">[![Yleiskustannuslaskenta](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="e74e6-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="e74e6-132">Laske ja kohdista sähkön yleiskustannukset</span><span class="sxs-lookup"><span data-stu-id="e74e6-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="e74e6-133">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="e74e6-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="e74e6-134">Tarkka johdon näkymä ei täten ole saatavilla kustannuslaskennassa.</span><span class="sxs-lookup"><span data-stu-id="e74e6-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="e74e6-135">Jotta kustannuslaskenta tarjoaisi oikean johdon näkymän kaikista organisaation yksiköistä ja tasoista, kustannusten on virrattava organisaation yksiköiden läpi.</span><span class="sxs-lookup"><span data-stu-id="e74e6-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="e74e6-136">Tämän virran on perustuttava joko tarkkaan tietoon kulutuksesta tai perusteltuun arvioon.</span><span class="sxs-lookup"><span data-stu-id="e74e6-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="e74e6-137">Sähkökustannukset voi kirjata kirjanpitoon seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="e74e6-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e74e6-138">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="e74e6-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e74e6-139">Kustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="e74e6-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="e74e6-140">Päätili</span><span class="sxs-lookup"><span data-stu-id="e74e6-140">Main account</span></span></th>
<th><span data-ttu-id="e74e6-141">Summa kirjanpitovaluuttana</span><span class="sxs-lookup"><span data-stu-id="e74e6-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-142">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="e74e6-143">CC099</span><span class="sxs-lookup"><span data-stu-id="e74e6-143">CC099</span></span></td>
<td><span data-ttu-id="e74e6-144">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="e74e6-144">Default cost center</span></span></td>
<td><span data-ttu-id="e74e6-145">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-145">10001</span></span></td>
<td><span data-ttu-id="e74e6-146">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-146">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="e74e6-148">Vaihe 1: Käsittele kustannustoiminnan laskenta</span><span class="sxs-lookup"><span data-stu-id="e74e6-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="e74e6-149">Kun kustannustapahtumat tuodaan lähdetiedoista, niille asetetaan kustannuslaskennassa oletusarvoisesti **Luokittelematon** -kustannustoimintaluokka.</span><span class="sxs-lookup"><span data-stu-id="e74e6-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="e74e6-150">Voit luokitella kustannustapahtumia uudelleen **kiinteäksi kustannukseksi** tai **muuttuvaksi kustannukseksi** kustannustoiminnan käytäntösäännöillä.</span><span class="sxs-lookup"><span data-stu-id="e74e6-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="e74e6-151">Määritä kustannustoiminnan sääntö</span><span class="sxs-lookup"><span data-stu-id="e74e6-151">Define the cost behavior rule</span></span>

<span data-ttu-id="e74e6-152">Joissain tapauksissa osa kustannuksesta on kiinteä ja loppuosa perustuu kulutukseen.</span><span class="sxs-lookup"><span data-stu-id="e74e6-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="e74e6-153">Sähkölaskut sopivat usein tähän määritelmään.</span><span class="sxs-lookup"><span data-stu-id="e74e6-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="e74e6-154">Maksat ensin määrätyn, kiinteän maksun, jonka lisäksi maksat kulutuksesta kilowattitunteina (kWh).</span><span class="sxs-lookup"><span data-stu-id="e74e6-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="e74e6-155">Jos kiinteä maksu on esimerkiksi 1 000,00, kustannustoiminnan sääntö määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e74e6-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="e74e6-156">Kiinteä määrä 1 000,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="e74e6-157">0 &lt;= 1 000,00 = Kiinteä</span><span class="sxs-lookup"><span data-stu-id="e74e6-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="e74e6-158">1000,01 &lt; N = Muuttuva</span><span class="sxs-lookup"><span data-stu-id="e74e6-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="e74e6-159">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="e74e6-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e74e6-160">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="e74e6-160">Journal</span></span></th>
<th><span data-ttu-id="e74e6-161">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="e74e6-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e74e6-162">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="e74e6-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e74e6-163">Versio</span><span class="sxs-lookup"><span data-stu-id="e74e6-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-164">00001</span><span class="sxs-lookup"><span data-stu-id="e74e6-164">00001</span></span></td>
<td><span data-ttu-id="e74e6-165">Kustannustoiminnan laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="e74e6-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="e74e6-166">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="e74e6-166">Fiscal</span></span></td>
<td><span data-ttu-id="e74e6-167">2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-167">2017</span></span></td>
<td><span data-ttu-id="e74e6-168">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-168">Period 1</span></span></td>
<td><span data-ttu-id="e74e6-169">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e74e6-170">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="e74e6-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e74e6-171">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="e74e6-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e74e6-172">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e74e6-173">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="e74e6-173">Cost element</span></span></th>
<th><span data-ttu-id="e74e6-174">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="e74e6-174">Cost behavior</span></span></th>
<th><span data-ttu-id="e74e6-175">Summa</span><span class="sxs-lookup"><span data-stu-id="e74e6-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-176">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="e74e6-177">CC099</span><span class="sxs-lookup"><span data-stu-id="e74e6-177">CC099</span></span></td>
<td><span data-ttu-id="e74e6-178">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="e74e6-178">Default cost center</span></span></td>
<td><span data-ttu-id="e74e6-179">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-179">10001</span></span></td>
<td><span data-ttu-id="e74e6-180">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-180">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-181">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="e74e6-181">Unclassified</span></span></td>
<td><span data-ttu-id="e74e6-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e74e6-183">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="e74e6-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e74e6-184">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e74e6-185">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="e74e6-185">Cost element</span></span></th>
<th><span data-ttu-id="e74e6-186">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="e74e6-186">Cost behavior</span></span></th>
<th><span data-ttu-id="e74e6-187">Summa</span><span class="sxs-lookup"><span data-stu-id="e74e6-187">Amount</span></span></th>
<th><span data-ttu-id="e74e6-188">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="e74e6-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-189">CC099</span><span class="sxs-lookup"><span data-stu-id="e74e6-189">CC099</span></span></td>
<td><span data-ttu-id="e74e6-190">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="e74e6-190">Default cost center</span></span></td>
<td><span data-ttu-id="e74e6-191">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-191">10001</span></span></td>
<td><span data-ttu-id="e74e6-192">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-192">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-193">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="e74e6-193">Unclassified</span></span></td>
<td><span data-ttu-id="e74e6-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-194">10,000.00</span></span></td>
<td><span data-ttu-id="e74e6-195">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-196">CC099</span><span class="sxs-lookup"><span data-stu-id="e74e6-196">CC099</span></span></td>
<td><span data-ttu-id="e74e6-197">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="e74e6-197">Default cost center</span></span></td>
<td><span data-ttu-id="e74e6-198">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-198">10001</span></span></td>
<td><span data-ttu-id="e74e6-199">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-199">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-200">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="e74e6-200">Unclassified</span></span></td>
<td><span data-ttu-id="e74e6-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-201">-10,000.00</span></span></td>
<td><span data-ttu-id="e74e6-202">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-203">CC099</span><span class="sxs-lookup"><span data-stu-id="e74e6-203">CC099</span></span></td>
<td><span data-ttu-id="e74e6-204">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="e74e6-204">Default cost center</span></span></td>
<td><span data-ttu-id="e74e6-205">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-205">10001</span></span></td>
<td><span data-ttu-id="e74e6-206">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-206">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-207">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-207">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-208">1,000.00</span></span></td>
<td><span data-ttu-id="e74e6-209">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-210">CC099</span><span class="sxs-lookup"><span data-stu-id="e74e6-210">CC099</span></span></td>
<td><span data-ttu-id="e74e6-211">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="e74e6-211">Default cost center</span></span></td>
<td><span data-ttu-id="e74e6-212">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-212">10001</span></span></td>
<td><span data-ttu-id="e74e6-213">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-213">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-214">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-214">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="e74e6-215">9,000.00</span></span></td>
<td><span data-ttu-id="e74e6-216">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e74e6-217">Lisätietoja on kohdassa [Kustannustoimintakäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="e74e6-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="e74e6-218">Vaihe 2: Käsittele kustannusten jaon laskenta</span><span class="sxs-lookup"><span data-stu-id="e74e6-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="e74e6-219">Kustannusten jakoa käytetään kustannusten jakamiseen yhdestä kustannusobjektista toiseen (tai useampaan kustannusobjektiin) määrittämällä asiaankuuluvan kohdistusperusteen.</span><span class="sxs-lookup"><span data-stu-id="e74e6-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="e74e6-220">Kustannusten jako ja kustannusten kohdistus eroavat toisistaan sillä, että kustannusten jako tapahtuu aina alkuperäisen kustannuksen ensisijaisen kustannuselementin tasolla.</span><span class="sxs-lookup"><span data-stu-id="e74e6-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="e74e6-221">Määritä kustannusten jaon sääntö</span><span class="sxs-lookup"><span data-stu-id="e74e6-221">Define the cost distribution rule</span></span>

<span data-ttu-id="e74e6-222">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="e74e6-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="e74e6-223">Kustannuslaskenta ei tarjoa tästä tarpeeksi tarkkoja tietoja.</span><span class="sxs-lookup"><span data-stu-id="e74e6-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="e74e6-224">Muuttuva kustannus tulisi jakaa yksittäisille kustannusobjekteille reiluin perustein.</span><span class="sxs-lookup"><span data-stu-id="e74e6-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="e74e6-225">Loogisin kohdistusperuste on sähkönkulutus (kWh).</span><span class="sxs-lookup"><span data-stu-id="e74e6-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="e74e6-226">Luodaan tilastollinen dimensionjäsen nimeltä Sähkö, johon kirjataan sähkönkulutus.</span><span class="sxs-lookup"><span data-stu-id="e74e6-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="e74e6-227">Oletusarvon mukaan kaikki tilastolliset dimensiojäsenet ovat käytettävissä kohdistusperusteina.</span><span class="sxs-lookup"><span data-stu-id="e74e6-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e74e6-228">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-228">Cost object</span></span></th>
<th><span data-ttu-id="e74e6-229">kWh</span><span class="sxs-lookup"><span data-stu-id="e74e6-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-230">CC001</span><span class="sxs-lookup"><span data-stu-id="e74e6-230">CC001</span></span></td>
<td><span data-ttu-id="e74e6-231">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="e74e6-231">HR</span></span></td>
<td><span data-ttu-id="e74e6-232">1 000</span><span class="sxs-lookup"><span data-stu-id="e74e6-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-233">CC002</span><span class="sxs-lookup"><span data-stu-id="e74e6-233">CC002</span></span></td>
<td><span data-ttu-id="e74e6-234">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="e74e6-234">Finance</span></span></td>
<td><span data-ttu-id="e74e6-235">6,000</span><span class="sxs-lookup"><span data-stu-id="e74e6-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-236">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-236">CC003</span></span></td>
<td><span data-ttu-id="e74e6-237">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="e74e6-237">Assembly</span></span></td>
<td><span data-ttu-id="e74e6-238">0</span><span class="sxs-lookup"><span data-stu-id="e74e6-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e74e6-239">Seuraavassa taulukossa on esitetty tulos, kun sähkönkulutusta käytetään kohdistusperusteena muuttuville kuluille.</span><span class="sxs-lookup"><span data-stu-id="e74e6-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e74e6-240">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-240">Cost object</span></span></th>
<th><span data-ttu-id="e74e6-241">Suuruus</span><span class="sxs-lookup"><span data-stu-id="e74e6-241">Magnitude</span></span></th>
<th><span data-ttu-id="e74e6-242">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="e74e6-242">Allocation factor</span></span></th>
<th><span data-ttu-id="e74e6-243">Summa</span><span class="sxs-lookup"><span data-stu-id="e74e6-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-244">CC001</span><span class="sxs-lookup"><span data-stu-id="e74e6-244">CC001</span></span></td>
<td><span data-ttu-id="e74e6-245">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="e74e6-245">HR</span></span></td>
<td><span data-ttu-id="e74e6-246">1 000</span><span class="sxs-lookup"><span data-stu-id="e74e6-246">1,000</span></span></td>
<td><span data-ttu-id="e74e6-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e74e6-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="e74e6-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-249">CC002</span><span class="sxs-lookup"><span data-stu-id="e74e6-249">CC002</span></span></td>
<td><span data-ttu-id="e74e6-250">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="e74e6-250">Finance</span></span></td>
<td><span data-ttu-id="e74e6-251">6,000</span><span class="sxs-lookup"><span data-stu-id="e74e6-251">6,000</span></span></td>
<td><span data-ttu-id="e74e6-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e74e6-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="e74e6-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-254">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-254">CC003</span></span></td>
<td><span data-ttu-id="e74e6-255">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="e74e6-255">Assembly</span></span></td>
<td><span data-ttu-id="e74e6-256">0</span><span class="sxs-lookup"><span data-stu-id="e74e6-256">0</span></span></td>
<td><span data-ttu-id="e74e6-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e74e6-258">0,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e74e6-259">Kiinteä kustannus tulisi jakaa tasaisesti yksittäisille kustannusobjekteille, jotka ovat kuluttaneet sähköä.</span><span class="sxs-lookup"><span data-stu-id="e74e6-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="e74e6-260">Voit käyttää sähkön tilastollista dimensiojäsentä kaavan kohdistusperusteena tämän tavoitteen saavuttamiseksi: (sähkö &gt;0,00) Seuraavassa taulukossa on esitetty tulos siitä, kun sähkönkulutus on määritetty muuttuvien kustannusten kohdistusperusteeksi.</span><span class="sxs-lookup"><span data-stu-id="e74e6-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e74e6-261">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-261">Cost object</span></span></th>
<th><span data-ttu-id="e74e6-262">Resepti</span><span class="sxs-lookup"><span data-stu-id="e74e6-262">Formula</span></span></th>
<th><span data-ttu-id="e74e6-263">Suuruus</span><span class="sxs-lookup"><span data-stu-id="e74e6-263">Magnitude</span></span></th>
<th><span data-ttu-id="e74e6-264">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="e74e6-264">Allocation factor</span></span></th>
<th><span data-ttu-id="e74e6-265">Summa</span><span class="sxs-lookup"><span data-stu-id="e74e6-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-266">CC001</span><span class="sxs-lookup"><span data-stu-id="e74e6-266">CC001</span></span></td>
<td><span data-ttu-id="e74e6-267">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="e74e6-267">HR</span></span></td>
<td><span data-ttu-id="e74e6-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="e74e6-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e74e6-269">1</span><span class="sxs-lookup"><span data-stu-id="e74e6-269">1</span></span></td>
<td><span data-ttu-id="e74e6-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e74e6-271">500,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-272">CC002</span><span class="sxs-lookup"><span data-stu-id="e74e6-272">CC002</span></span></td>
<td><span data-ttu-id="e74e6-273">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="e74e6-273">Finance</span></span></td>
<td><span data-ttu-id="e74e6-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="e74e6-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e74e6-275">1</span><span class="sxs-lookup"><span data-stu-id="e74e6-275">1</span></span></td>
<td><span data-ttu-id="e74e6-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e74e6-277">500,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-278">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-278">CC003</span></span></td>
<td><span data-ttu-id="e74e6-279">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="e74e6-279">Assembly</span></span></td>
<td><span data-ttu-id="e74e6-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="e74e6-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e74e6-281">0</span><span class="sxs-lookup"><span data-stu-id="e74e6-281">0</span></span></td>
<td><span data-ttu-id="e74e6-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e74e6-283">0,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="e74e6-284">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="e74e6-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e74e6-285">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="e74e6-285">Journal</span></span></th>
<th><span data-ttu-id="e74e6-286">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="e74e6-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e74e6-287">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="e74e6-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e74e6-288">Versio</span><span class="sxs-lookup"><span data-stu-id="e74e6-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-289">00002</span><span class="sxs-lookup"><span data-stu-id="e74e6-289">00002</span></span></td>
<td><span data-ttu-id="e74e6-290">Kustannusten jaon laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="e74e6-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="e74e6-291">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="e74e6-291">Fiscal</span></span></td>
<td><span data-ttu-id="e74e6-292">2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-292">2017</span></span></td>
<td><span data-ttu-id="e74e6-293">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-293">Period 1</span></span></td>
<td><span data-ttu-id="e74e6-294">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e74e6-295">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="e74e6-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e74e6-296">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="e74e6-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e74e6-297">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e74e6-298">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="e74e6-298">Cost element</span></span></th>
<th><span data-ttu-id="e74e6-299">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="e74e6-299">Cost behavior</span></span></th>
<th><span data-ttu-id="e74e6-300">Summa</span><span class="sxs-lookup"><span data-stu-id="e74e6-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-301">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="e74e6-302">CC099</span><span class="sxs-lookup"><span data-stu-id="e74e6-302">CC099</span></span></td>
<td><span data-ttu-id="e74e6-303">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="e74e6-303">Default cost center</span></span></td>
<td><span data-ttu-id="e74e6-304">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-304">10001</span></span></td>
<td><span data-ttu-id="e74e6-305">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-305">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-306">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-306">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-308">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="e74e6-309">CC099</span><span class="sxs-lookup"><span data-stu-id="e74e6-309">CC099</span></span></td>
<td><span data-ttu-id="e74e6-310">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="e74e6-310">Default cost center</span></span></td>
<td><span data-ttu-id="e74e6-311">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-311">10001</span></span></td>
<td><span data-ttu-id="e74e6-312">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-312">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-313">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-313">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="e74e6-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e74e6-315">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="e74e6-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e74e6-316">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e74e6-317">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="e74e6-317">Cost element</span></span></th>
<th><span data-ttu-id="e74e6-318">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="e74e6-318">Cost behavior</span></span></th>
<th><span data-ttu-id="e74e6-319">Summa</span><span class="sxs-lookup"><span data-stu-id="e74e6-319">Amount</span></span></th>
<th><span data-ttu-id="e74e6-320">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="e74e6-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-321">CC099</span><span class="sxs-lookup"><span data-stu-id="e74e6-321">CC099</span></span></td>
<td><span data-ttu-id="e74e6-322">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="e74e6-322">Default cost center</span></span></td>
<td><span data-ttu-id="e74e6-323">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-323">10001</span></span></td>
<td><span data-ttu-id="e74e6-324">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-324">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-325">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-325">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-326">-1,000.00</span></span></td>
<td><span data-ttu-id="e74e6-327">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-328">CC001</span><span class="sxs-lookup"><span data-stu-id="e74e6-328">CC001</span></span></td>
<td><span data-ttu-id="e74e6-329">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="e74e6-329">HR</span></span></td>
<td><span data-ttu-id="e74e6-330">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-330">10001</span></span></td>
<td><span data-ttu-id="e74e6-331">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-331">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-332">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-332">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-333">500,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-333">500.00</span></span></td>
<td><span data-ttu-id="e74e6-334">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-335">CC002</span><span class="sxs-lookup"><span data-stu-id="e74e6-335">CC002</span></span></td>
<td><span data-ttu-id="e74e6-336">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="e74e6-336">Finance</span></span></td>
<td><span data-ttu-id="e74e6-337">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-337">10001</span></span></td>
<td><span data-ttu-id="e74e6-338">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-338">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-339">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-339">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-340">500,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-340">500.00</span></span></td>
<td><span data-ttu-id="e74e6-341">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-342">CC099</span><span class="sxs-lookup"><span data-stu-id="e74e6-342">CC099</span></span></td>
<td><span data-ttu-id="e74e6-343">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="e74e6-343">Default cost center</span></span></td>
<td><span data-ttu-id="e74e6-344">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-344">10001</span></span></td>
<td><span data-ttu-id="e74e6-345">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-345">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-346">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-346">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-347">-9,000.00</span></span></td>
<td><span data-ttu-id="e74e6-348">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-349">CC001</span><span class="sxs-lookup"><span data-stu-id="e74e6-349">CC001</span></span></td>
<td><span data-ttu-id="e74e6-350">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="e74e6-350">HR</span></span></td>
<td><span data-ttu-id="e74e6-351">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-351">10001</span></span></td>
<td><span data-ttu-id="e74e6-352">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-352">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-353">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-353">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="e74e6-354">1,285.71</span></span></td>
<td><span data-ttu-id="e74e6-355">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-356">CC002</span><span class="sxs-lookup"><span data-stu-id="e74e6-356">CC002</span></span></td>
<td><span data-ttu-id="e74e6-357">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="e74e6-357">Finance</span></span></td>
<td><span data-ttu-id="e74e6-358">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-358">10001</span></span></td>
<td><span data-ttu-id="e74e6-359">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-359">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-360">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-360">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="e74e6-361">7,714.29</span></span></td>
<td><span data-ttu-id="e74e6-362">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e74e6-363">Lisätietoja on kohdassa [Jakelukäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="e74e6-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="e74e6-364">Vaihe 3: Käsittele yleiskustannustason laskenta</span><span class="sxs-lookup"><span data-stu-id="e74e6-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="e74e6-365">Yleiskustannustasolla veloitetaan yksi tai useampi määrätty kustannusobjekti.</span><span class="sxs-lookup"><span data-stu-id="e74e6-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="e74e6-366">Veloitus perustuu ennalta määrättyyn kustannustasoon sekä määritetyn kohdistusperusteen suuruuteen.</span><span class="sxs-lookup"><span data-stu-id="e74e6-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="e74e6-367">Määritä yleiskustannustaso.</span><span class="sxs-lookup"><span data-stu-id="e74e6-367">Define the overhead rate</span></span>

<span data-ttu-id="e74e6-368">Kustannusobjekti CC001 HR vaikuttaa joukkoon sisäisiä projekteja.</span><span class="sxs-lookup"><span data-stu-id="e74e6-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="e74e6-369">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon projektit.</span><span class="sxs-lookup"><span data-stu-id="e74e6-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e74e6-370">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-370">Cost object</span></span></th>
<th><span data-ttu-id="e74e6-371">Tunnit</span><span class="sxs-lookup"><span data-stu-id="e74e6-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-372">Proj 1</span></span></td>
<td><span data-ttu-id="e74e6-373">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-373">Project 1</span></span></td>
<td><span data-ttu-id="e74e6-374">3</span><span class="sxs-lookup"><span data-stu-id="e74e6-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-375">Proj 2</span></span></td>
<td><span data-ttu-id="e74e6-376">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-376">Project 2</span></span></td>
<td><span data-ttu-id="e74e6-377">1</span><span class="sxs-lookup"><span data-stu-id="e74e6-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e74e6-378">Kustannusprojektien osuudelle on määritetty ennalta kustannushinta.</span><span class="sxs-lookup"><span data-stu-id="e74e6-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e74e6-379">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-379">Cost object</span></span></th>
<th><span data-ttu-id="e74e6-380">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="e74e6-380">Cost element</span></span></th>
<th><span data-ttu-id="e74e6-381">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="e74e6-381">Cost behavior</span></span></th>
<th><span data-ttu-id="e74e6-382">Yksiköt</span><span class="sxs-lookup"><span data-stu-id="e74e6-382">Units</span></span></th>
<th><span data-ttu-id="e74e6-383">Osuus</span><span class="sxs-lookup"><span data-stu-id="e74e6-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-384">CC001</span><span class="sxs-lookup"><span data-stu-id="e74e6-384">CC001</span></span></td>
<td><span data-ttu-id="e74e6-385">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="e74e6-385">HR</span></span></td>
<td><span data-ttu-id="e74e6-386">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-386">10001</span></span></td>
<td><span data-ttu-id="e74e6-387">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-387">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-388">1</span><span class="sxs-lookup"><span data-stu-id="e74e6-388">1</span></span></td>
<td><span data-ttu-id="e74e6-389">10</span><span class="sxs-lookup"><span data-stu-id="e74e6-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e74e6-390">Seuraavassa taulukossa on esitetty tulos, kun Henkilöstöhallinnon projekteja käytetään kohdistusperusteena.</span><span class="sxs-lookup"><span data-stu-id="e74e6-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e74e6-391">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-391">Cost object</span></span></th>
<th><span data-ttu-id="e74e6-392">Suuruus</span><span class="sxs-lookup"><span data-stu-id="e74e6-392">Magnitude</span></span></th>
<th><span data-ttu-id="e74e6-393">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="e74e6-393">Cost element</span></span></th>
<th><span data-ttu-id="e74e6-394">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="e74e6-394">Allocation factor</span></span></th>
<th><span data-ttu-id="e74e6-395">Summa</span><span class="sxs-lookup"><span data-stu-id="e74e6-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-396">Proj 1</span></span></td>
<td><span data-ttu-id="e74e6-397">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-397">Project 1</span></span></td>
<td><span data-ttu-id="e74e6-398">3</span><span class="sxs-lookup"><span data-stu-id="e74e6-398">3</span></span></td>
<td><span data-ttu-id="e74e6-399">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-399">10001</span></span></td>
<td><span data-ttu-id="e74e6-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="e74e6-401">30,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-402">Proj 2</span></span></td>
<td><span data-ttu-id="e74e6-403">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-403">Project 2</span></span></td>
<td><span data-ttu-id="e74e6-404">1</span><span class="sxs-lookup"><span data-stu-id="e74e6-404">1</span></span></td>
<td><span data-ttu-id="e74e6-405">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-405">10001</span></span></td>
<td><span data-ttu-id="e74e6-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="e74e6-407">10,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="e74e6-408">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="e74e6-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e74e6-409">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="e74e6-409">Journal</span></span></th>
<th><span data-ttu-id="e74e6-410">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="e74e6-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e74e6-411">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="e74e6-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e74e6-412">Versio</span><span class="sxs-lookup"><span data-stu-id="e74e6-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-413">00003</span><span class="sxs-lookup"><span data-stu-id="e74e6-413">00003</span></span></td>
<td><span data-ttu-id="e74e6-414">Yleiskustannustason laskelman kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="e74e6-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="e74e6-415">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="e74e6-415">Fiscal</span></span></td>
<td><span data-ttu-id="e74e6-416">2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-416">2017</span></span></td>
<td><span data-ttu-id="e74e6-417">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-417">Period 1</span></span></td>
<td><span data-ttu-id="e74e6-418">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="e74e6-419">Kirjauskansioviennit (Yleiskustannustason laskennan kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="e74e6-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e74e6-420">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="e74e6-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e74e6-421">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-421">Cost object</span></span></th>
<th><span data-ttu-id="e74e6-422">Suuruus</span><span class="sxs-lookup"><span data-stu-id="e74e6-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-423">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="e74e6-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-424">Proj 1</span></span></td>
<td><span data-ttu-id="e74e6-425">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="e74e6-426">3,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-427">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="e74e6-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-428">Proj 2</span></span></td>
<td><span data-ttu-id="e74e6-429">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="e74e6-430">1,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e74e6-431">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="e74e6-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e74e6-432">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e74e6-433">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="e74e6-433">Cost element</span></span></th>
<th><span data-ttu-id="e74e6-434">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="e74e6-434">Cost behavior</span></span></th>
<th><span data-ttu-id="e74e6-435">Summa</span><span class="sxs-lookup"><span data-stu-id="e74e6-435">Amount</span></span></th>
<th><span data-ttu-id="e74e6-436">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="e74e6-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="e74e6-437">CC0001</span></span></td>
<td><span data-ttu-id="e74e6-438">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="e74e6-438">HR</span></span></td>
<td><span data-ttu-id="e74e6-439">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-439">10001</span></span></td>
<td><span data-ttu-id="e74e6-440">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-440">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-441">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-441">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-442">-30.00</span></span></td>
<td><span data-ttu-id="e74e6-443">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-444">Proj 1</span></span></td>
<td><span data-ttu-id="e74e6-445">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="e74e6-446">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-446">10001</span></span></td>
<td><span data-ttu-id="e74e6-447">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-447">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-448">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-448">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-449">30,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-449">30.00</span></span></td>
<td><span data-ttu-id="e74e6-450">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-451">CC001</span><span class="sxs-lookup"><span data-stu-id="e74e6-451">CC001</span></span></td>
<td><span data-ttu-id="e74e6-452">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="e74e6-452">HR</span></span></td>
<td><span data-ttu-id="e74e6-453">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-453">10001</span></span></td>
<td><span data-ttu-id="e74e6-454">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-454">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-455">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-455">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-456">-10.00</span></span></td>
<td><span data-ttu-id="e74e6-457">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-458">Proj 2</span></span></td>
<td><span data-ttu-id="e74e6-459">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="e74e6-460">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-460">10001</span></span></td>
<td><span data-ttu-id="e74e6-461">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-461">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-462">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-462">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-463">10.00</span><span class="sxs-lookup"><span data-stu-id="e74e6-463">10.00</span></span></td>
<td><span data-ttu-id="e74e6-464">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e74e6-465">Lisätietoja on kohdassa [Yleisen laskennan suorittaminen](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="e74e6-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="e74e6-466">Vaihe 4: Käsittele kustannusten kohdistuksen laskenta</span><span class="sxs-lookup"><span data-stu-id="e74e6-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="e74e6-467">Kohdistuksella kustannusobjektin saldo liitetään toisiin kustannusobjekteihin käyttämällä kohdistusperustetta.</span><span class="sxs-lookup"><span data-stu-id="e74e6-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="e74e6-468">Finance and Operations tukee vastavuoroista kohdistusmenetelmää.</span><span class="sxs-lookup"><span data-stu-id="e74e6-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="e74e6-469">Vastavuoroisessa kohdistusmenetelmässä tunnistetaan oheiskustannusobjektien käyttämät, keskinäiset palvelut täysin.</span><span class="sxs-lookup"><span data-stu-id="e74e6-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="e74e6-470">Järjestelmä määrittää oikean kohdistusjärjestyksen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="e74e6-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="e74e6-471">Kustannusobjektin saldo kohdistetaan yhdellä kohdistusperusteella.</span><span class="sxs-lookup"><span data-stu-id="e74e6-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="e74e6-472">Kustannusobjektien dimensiot ja niiden vastaavat jäsenet ylittävät kohdistukset ovat tuettuja.</span><span class="sxs-lookup"><span data-stu-id="e74e6-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="e74e6-473">Kustannusseurantayksikkö hallitsee kohdistusjärjestystä.</span><span class="sxs-lookup"><span data-stu-id="e74e6-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="e74e6-474">[![Vastavuoroinen menetelmä](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="e74e6-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="e74e6-475">Määritä kustannuksen kohdistus</span><span class="sxs-lookup"><span data-stu-id="e74e6-475">Define the cost allocation</span></span>

<span data-ttu-id="e74e6-476">Tämä on yksinkertainen esimerkki, jossa kerrotaan, miten voit jäljittää kustannuksen virran.</span><span class="sxs-lookup"><span data-stu-id="e74e6-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="e74e6-477">Kustannusobjekti CC001 HR liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="e74e6-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="e74e6-478">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="e74e6-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e74e6-479">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-479">Cost object</span></span></th>
<th><span data-ttu-id="e74e6-480">HR-palvelut</span><span class="sxs-lookup"><span data-stu-id="e74e6-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-481">CC002</span><span class="sxs-lookup"><span data-stu-id="e74e6-481">CC002</span></span></td>
<td><span data-ttu-id="e74e6-482">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="e74e6-482">Finance</span></span></td>
<td><span data-ttu-id="e74e6-483">35</span><span class="sxs-lookup"><span data-stu-id="e74e6-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-484">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-484">CC003</span></span></td>
<td><span data-ttu-id="e74e6-485">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="e74e6-485">Assembly</span></span></td>
<td><span data-ttu-id="e74e6-486">55</span><span class="sxs-lookup"><span data-stu-id="e74e6-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-487">CC004</span><span class="sxs-lookup"><span data-stu-id="e74e6-487">CC004</span></span></td>
<td><span data-ttu-id="e74e6-488">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="e74e6-488">Packaging</span></span></td>
<td><span data-ttu-id="e74e6-489">10</span><span class="sxs-lookup"><span data-stu-id="e74e6-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e74e6-490">Kustannusobjekti CC002 Taloushallinto liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="e74e6-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="e74e6-491">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Taloushallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="e74e6-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e74e6-492">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-492">Cost object</span></span></th>
<th><span data-ttu-id="e74e6-493">Taloushallinnon palvelut</span><span class="sxs-lookup"><span data-stu-id="e74e6-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-494">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-494">CC003</span></span></td>
<td><span data-ttu-id="e74e6-495">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="e74e6-495">Assembly</span></span></td>
<td><span data-ttu-id="e74e6-496">65</span><span class="sxs-lookup"><span data-stu-id="e74e6-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-497">CC004</span><span class="sxs-lookup"><span data-stu-id="e74e6-497">CC004</span></span></td>
<td><span data-ttu-id="e74e6-498">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="e74e6-498">Packaging</span></span></td>
<td><span data-ttu-id="e74e6-499">35</span><span class="sxs-lookup"><span data-stu-id="e74e6-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e74e6-500">Kustannusobjekti CC003 Kokoonpano liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="e74e6-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="e74e6-501">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Kokoonpanopalvelut.</span><span class="sxs-lookup"><span data-stu-id="e74e6-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e74e6-502">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-502">Cost object</span></span></th>
<th><span data-ttu-id="e74e6-503">Kokoonpanopalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="e74e6-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-504">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-504">Prod 1</span></span></td>
<td><span data-ttu-id="e74e6-505">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-505">Product 1</span></span></td>
<td><span data-ttu-id="e74e6-506">60</span><span class="sxs-lookup"><span data-stu-id="e74e6-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-507">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-507">Prod 2</span></span></td>
<td><span data-ttu-id="e74e6-508">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-508">Product 2</span></span></td>
<td><span data-ttu-id="e74e6-509">20</span><span class="sxs-lookup"><span data-stu-id="e74e6-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e74e6-510">Kustannusobjekti CC004 Pakkaus liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="e74e6-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="e74e6-511">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Pakkauspalvelut.</span><span class="sxs-lookup"><span data-stu-id="e74e6-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e74e6-512">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-512">Cost object</span></span></th>
<th><span data-ttu-id="e74e6-513">Pakkauspalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="e74e6-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-514">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-514">Prod 1</span></span></td>
<td><span data-ttu-id="e74e6-515">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-515">Product 1</span></span></td>
<td><span data-ttu-id="e74e6-516">80</span><span class="sxs-lookup"><span data-stu-id="e74e6-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-517">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-517">Prod 2</span></span></td>
<td><span data-ttu-id="e74e6-518">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-518">Product 2</span></span></td>
<td><span data-ttu-id="e74e6-519">päivänä</span><span class="sxs-lookup"><span data-stu-id="e74e6-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e74e6-520">Finance and Operationsissa tilastomittaukset, kuten tämän tuotteen kuluttamat tuotantotunnit, voidaan johtaa lähdetiedoista.</span><span class="sxs-lookup"><span data-stu-id="e74e6-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="e74e6-521">Lisätietoja on kohdassa [Tilastomittauksen lähdemalli](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="e74e6-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="e74e6-522">Seuraavassa taulukossa näytetään tulos, kun henkilöstöhallinnon palveluja käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="e74e6-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e74e6-523">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-523">Cost object</span></span></th>
<th><span data-ttu-id="e74e6-524">Suuruus</span><span class="sxs-lookup"><span data-stu-id="e74e6-524">Magnitude</span></span></th>
<th><span data-ttu-id="e74e6-525">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="e74e6-525">Allocation factor</span></span></th>
<th><span data-ttu-id="e74e6-526">Summa</span><span class="sxs-lookup"><span data-stu-id="e74e6-526">Amount</span></span></th>
<th><span data-ttu-id="e74e6-527">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="e74e6-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-528">CC002</span><span class="sxs-lookup"><span data-stu-id="e74e6-528">CC002</span></span></td>
<td><span data-ttu-id="e74e6-529">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="e74e6-529">Finance</span></span></td>
<td><span data-ttu-id="e74e6-530">35</span><span class="sxs-lookup"><span data-stu-id="e74e6-530">35</span></span></td>
<td><span data-ttu-id="e74e6-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e74e6-532">175.00</span><span class="sxs-lookup"><span data-stu-id="e74e6-532">175.00</span></span></td>
<td><span data-ttu-id="e74e6-533">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-534">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-534">CC003</span></span></td>
<td><span data-ttu-id="e74e6-535">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="e74e6-535">Assembly</span></span></td>
<td><span data-ttu-id="e74e6-536">55</span><span class="sxs-lookup"><span data-stu-id="e74e6-536">55</span></span></td>
<td><span data-ttu-id="e74e6-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e74e6-538">275.00</span><span class="sxs-lookup"><span data-stu-id="e74e6-538">275.00</span></span></td>
<td><span data-ttu-id="e74e6-539">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-540">CC004</span><span class="sxs-lookup"><span data-stu-id="e74e6-540">CC004</span></span></td>
<td><span data-ttu-id="e74e6-541">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="e74e6-541">Packaging</span></span></td>
<td><span data-ttu-id="e74e6-542">10</span><span class="sxs-lookup"><span data-stu-id="e74e6-542">10</span></span></td>
<td><span data-ttu-id="e74e6-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e74e6-544">50,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-544">50.00</span></span></td>
<td><span data-ttu-id="e74e6-545">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-546">CC002</span><span class="sxs-lookup"><span data-stu-id="e74e6-546">CC002</span></span></td>
<td><span data-ttu-id="e74e6-547">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="e74e6-547">Finance</span></span></td>
<td><span data-ttu-id="e74e6-548">35</span><span class="sxs-lookup"><span data-stu-id="e74e6-548">35</span></span></td>
<td><span data-ttu-id="e74e6-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="e74e6-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e74e6-550">436.00</span><span class="sxs-lookup"><span data-stu-id="e74e6-550">436.00</span></span></td>
<td><span data-ttu-id="e74e6-551">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-552">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-552">CC003</span></span></td>
<td><span data-ttu-id="e74e6-553">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="e74e6-553">Assembly</span></span></td>
<td><span data-ttu-id="e74e6-554">55</span><span class="sxs-lookup"><span data-stu-id="e74e6-554">55</span></span></td>
<td><span data-ttu-id="e74e6-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="e74e6-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e74e6-556">685.14</span><span class="sxs-lookup"><span data-stu-id="e74e6-556">685.14</span></span></td>
<td><span data-ttu-id="e74e6-557">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-558">CC004</span><span class="sxs-lookup"><span data-stu-id="e74e6-558">CC004</span></span></td>
<td><span data-ttu-id="e74e6-559">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="e74e6-559">Packaging</span></span></td>
<td><span data-ttu-id="e74e6-560">10</span><span class="sxs-lookup"><span data-stu-id="e74e6-560">10</span></span></td>
<td><span data-ttu-id="e74e6-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="e74e6-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e74e6-562">124.57</span><span class="sxs-lookup"><span data-stu-id="e74e6-562">124.57</span></span></td>
<td><span data-ttu-id="e74e6-563">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e74e6-564">Seuraavassa taulukossa näytetään tulos, kun Taloushallinnon palveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="e74e6-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e74e6-565">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-565">Cost object</span></span></th>
<th><span data-ttu-id="e74e6-566">Suuruus</span><span class="sxs-lookup"><span data-stu-id="e74e6-566">Magnitude</span></span></th>
<th><span data-ttu-id="e74e6-567">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="e74e6-567">Allocation factor</span></span></th>
<th><span data-ttu-id="e74e6-568">Summa</span><span class="sxs-lookup"><span data-stu-id="e74e6-568">Amount</span></span></th>
<th><span data-ttu-id="e74e6-569">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="e74e6-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-570">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-570">CC003</span></span></td>
<td><span data-ttu-id="e74e6-571">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="e74e6-571">Assembly</span></span></td>
<td><span data-ttu-id="e74e6-572">65</span><span class="sxs-lookup"><span data-stu-id="e74e6-572">65</span></span></td>
<td><span data-ttu-id="e74e6-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="e74e6-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="e74e6-574">438.75</span><span class="sxs-lookup"><span data-stu-id="e74e6-574">438.75</span></span></td>
<td><span data-ttu-id="e74e6-575">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-576">CC004</span><span class="sxs-lookup"><span data-stu-id="e74e6-576">CC004</span></span></td>
<td><span data-ttu-id="e74e6-577">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="e74e6-577">Packaging</span></span></td>
<td><span data-ttu-id="e74e6-578">35</span><span class="sxs-lookup"><span data-stu-id="e74e6-578">35</span></span></td>
<td><span data-ttu-id="e74e6-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="e74e6-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="e74e6-580">236.25</span><span class="sxs-lookup"><span data-stu-id="e74e6-580">236.25</span></span></td>
<td><span data-ttu-id="e74e6-581">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-582">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-582">CC003</span></span></td>
<td><span data-ttu-id="e74e6-583">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="e74e6-583">Assembly</span></span></td>
<td><span data-ttu-id="e74e6-584">65</span><span class="sxs-lookup"><span data-stu-id="e74e6-584">65</span></span></td>
<td><span data-ttu-id="e74e6-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="e74e6-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="e74e6-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="e74e6-586">5,297.69</span></span></td>
<td><span data-ttu-id="e74e6-587">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-588">CC004</span><span class="sxs-lookup"><span data-stu-id="e74e6-588">CC004</span></span></td>
<td><span data-ttu-id="e74e6-589">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="e74e6-589">Packaging</span></span></td>
<td><span data-ttu-id="e74e6-590">35</span><span class="sxs-lookup"><span data-stu-id="e74e6-590">35</span></span></td>
<td><span data-ttu-id="e74e6-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="e74e6-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="e74e6-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="e74e6-592">2,852.60</span></span></td>
<td><span data-ttu-id="e74e6-593">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e74e6-594">Seuraavassa taulukossa näytetään tulos, kun Kokoonpanopalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="e74e6-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e74e6-595">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-595">Cost object</span></span></th>
<th><span data-ttu-id="e74e6-596">Suuruus</span><span class="sxs-lookup"><span data-stu-id="e74e6-596">Magnitude</span></span></th>
<th><span data-ttu-id="e74e6-597">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="e74e6-597">Allocation factor</span></span></th>
<th><span data-ttu-id="e74e6-598">Summa</span><span class="sxs-lookup"><span data-stu-id="e74e6-598">Amount</span></span></th>
<th><span data-ttu-id="e74e6-599">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="e74e6-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-600">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-600">Prod 1</span></span></td>
<td><span data-ttu-id="e74e6-601">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-601">Product 1</span></span></td>
<td><span data-ttu-id="e74e6-602">60</span><span class="sxs-lookup"><span data-stu-id="e74e6-602">60</span></span></td>
<td><span data-ttu-id="e74e6-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="e74e6-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="e74e6-604">535.31</span><span class="sxs-lookup"><span data-stu-id="e74e6-604">535.31</span></span></td>
<td><span data-ttu-id="e74e6-605">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-606">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-606">Prod 2</span></span></td>
<td><span data-ttu-id="e74e6-607">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-607">Product 2</span></span></td>
<td><span data-ttu-id="e74e6-608">20</span><span class="sxs-lookup"><span data-stu-id="e74e6-608">20</span></span></td>
<td><span data-ttu-id="e74e6-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="e74e6-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="e74e6-610">178.44</span><span class="sxs-lookup"><span data-stu-id="e74e6-610">178.44</span></span></td>
<td><span data-ttu-id="e74e6-611">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-612">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-612">Prod 1</span></span></td>
<td><span data-ttu-id="e74e6-613">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-613">Product 1</span></span></td>
<td><span data-ttu-id="e74e6-614">60</span><span class="sxs-lookup"><span data-stu-id="e74e6-614">60</span></span></td>
<td><span data-ttu-id="e74e6-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="e74e6-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="e74e6-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="e74e6-616">4,487.12</span></span></td>
<td><span data-ttu-id="e74e6-617">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-618">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-618">Prod 2</span></span></td>
<td><span data-ttu-id="e74e6-619">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-619">Product 2</span></span></td>
<td><span data-ttu-id="e74e6-620">20</span><span class="sxs-lookup"><span data-stu-id="e74e6-620">20</span></span></td>
<td><span data-ttu-id="e74e6-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="e74e6-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="e74e6-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="e74e6-622">1,495.71</span></span></td>
<td><span data-ttu-id="e74e6-623">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e74e6-624">Seuraavassa taulukossa näytetään tulos, kun Pakkauspalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="e74e6-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e74e6-625">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-625">Cost object</span></span></th>
<th><span data-ttu-id="e74e6-626">Suuruus</span><span class="sxs-lookup"><span data-stu-id="e74e6-626">Magnitude</span></span></th>
<th><span data-ttu-id="e74e6-627">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="e74e6-627">Allocation factor</span></span></th>
<th><span data-ttu-id="e74e6-628">Summa</span><span class="sxs-lookup"><span data-stu-id="e74e6-628">Amount</span></span></th>
<th><span data-ttu-id="e74e6-629">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="e74e6-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-630">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-630">Prod 1</span></span></td>
<td><span data-ttu-id="e74e6-631">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-631">Product 1</span></span></td>
<td><span data-ttu-id="e74e6-632">80</span><span class="sxs-lookup"><span data-stu-id="e74e6-632">80</span></span></td>
<td><span data-ttu-id="e74e6-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="e74e6-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="e74e6-634">241.05</span><span class="sxs-lookup"><span data-stu-id="e74e6-634">241.05</span></span></td>
<td><span data-ttu-id="e74e6-635">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-636">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-636">Prod 2</span></span></td>
<td><span data-ttu-id="e74e6-637">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-637">Product 2</span></span></td>
<td><span data-ttu-id="e74e6-638">15</span><span class="sxs-lookup"><span data-stu-id="e74e6-638">15</span></span></td>
<td><span data-ttu-id="e74e6-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="e74e6-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="e74e6-640">45.20</span><span class="sxs-lookup"><span data-stu-id="e74e6-640">45.20</span></span></td>
<td><span data-ttu-id="e74e6-641">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-642">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-642">Prod 1</span></span></td>
<td><span data-ttu-id="e74e6-643">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-643">Product 1</span></span></td>
<td><span data-ttu-id="e74e6-644">80</span><span class="sxs-lookup"><span data-stu-id="e74e6-644">80</span></span></td>
<td><span data-ttu-id="e74e6-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="e74e6-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="e74e6-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="e74e6-646">2,507.09</span></span></td>
<td><span data-ttu-id="e74e6-647">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-648">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-648">Prod 2</span></span></td>
<td><span data-ttu-id="e74e6-649">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-649">Product 2</span></span></td>
<td><span data-ttu-id="e74e6-650">15</span><span class="sxs-lookup"><span data-stu-id="e74e6-650">15</span></span></td>
<td><span data-ttu-id="e74e6-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="e74e6-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="e74e6-652">470.08</span><span class="sxs-lookup"><span data-stu-id="e74e6-652">470.08</span></span></td>
<td><span data-ttu-id="e74e6-653">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e74e6-654">Kirjauskansioviennit (kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="e74e6-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e74e6-655">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="e74e6-655">Journal</span></span></th>
<th><span data-ttu-id="e74e6-656">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="e74e6-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e74e6-657">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="e74e6-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e74e6-658">Versio</span><span class="sxs-lookup"><span data-stu-id="e74e6-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-659">00004</span><span class="sxs-lookup"><span data-stu-id="e74e6-659">00004</span></span></td>
<td><span data-ttu-id="e74e6-660">Kustannusten kohdistuskirjauskansio</span><span class="sxs-lookup"><span data-stu-id="e74e6-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="e74e6-661">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="e74e6-661">Fiscal</span></span></td>
<td><span data-ttu-id="e74e6-662">2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-662">2017</span></span></td>
<td><span data-ttu-id="e74e6-663">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-663">Period 1</span></span></td>
<td><span data-ttu-id="e74e6-664">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="e74e6-665">Kirjauskansion rivit</span><span class="sxs-lookup"><span data-stu-id="e74e6-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e74e6-666">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="e74e6-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e74e6-667">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e74e6-668">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="e74e6-668">Cost element</span></span></th>
<th><span data-ttu-id="e74e6-669">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="e74e6-669">Cost behavior</span></span></th>
<th><span data-ttu-id="e74e6-670">Summa</span><span class="sxs-lookup"><span data-stu-id="e74e6-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-671">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="e74e6-672">CC001</span><span class="sxs-lookup"><span data-stu-id="e74e6-672">CC001</span></span></td>
<td><span data-ttu-id="e74e6-673">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="e74e6-673">HR</span></span></td>
<td><span data-ttu-id="e74e6-674">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-674">10001</span></span></td>
<td><span data-ttu-id="e74e6-675">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-675">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-676">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-676">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-677">500,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-678">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="e74e6-679">CC001</span><span class="sxs-lookup"><span data-stu-id="e74e6-679">CC001</span></span></td>
<td><span data-ttu-id="e74e6-680">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="e74e6-680">HR</span></span></td>
<td><span data-ttu-id="e74e6-681">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-681">10001</span></span></td>
<td><span data-ttu-id="e74e6-682">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-682">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-683">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-683">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="e74e6-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-685">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="e74e6-686">CC002</span><span class="sxs-lookup"><span data-stu-id="e74e6-686">CC002</span></span></td>
<td><span data-ttu-id="e74e6-687">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="e74e6-687">Finance</span></span></td>
<td><span data-ttu-id="e74e6-688">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-688">10001</span></span></td>
<td><span data-ttu-id="e74e6-689">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-689">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-690">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-690">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-691">675.00</span><span class="sxs-lookup"><span data-stu-id="e74e6-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-692">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="e74e6-693">CC002</span><span class="sxs-lookup"><span data-stu-id="e74e6-693">CC002</span></span></td>
<td><span data-ttu-id="e74e6-694">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="e74e6-694">Finance</span></span></td>
<td><span data-ttu-id="e74e6-695">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-695">10001</span></span></td>
<td><span data-ttu-id="e74e6-696">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-696">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-697">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-697">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="e74e6-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-699">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="e74e6-700">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-700">CC003</span></span></td>
<td><span data-ttu-id="e74e6-701">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="e74e6-701">Assembly</span></span></td>
<td><span data-ttu-id="e74e6-702">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-702">10001</span></span></td>
<td><span data-ttu-id="e74e6-703">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-703">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-704">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-704">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-705">713.75</span><span class="sxs-lookup"><span data-stu-id="e74e6-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-706">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="e74e6-707">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-707">CC003</span></span></td>
<td><span data-ttu-id="e74e6-708">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="e74e6-708">Assembly</span></span></td>
<td><span data-ttu-id="e74e6-709">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-709">10001</span></span></td>
<td><span data-ttu-id="e74e6-710">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-710">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-711">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-711">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="e74e6-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-713">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="e74e6-714">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-714">CC003</span></span></td>
<td><span data-ttu-id="e74e6-715">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="e74e6-715">Packaging</span></span></td>
<td><span data-ttu-id="e74e6-716">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-716">10001</span></span></td>
<td><span data-ttu-id="e74e6-717">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-717">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-718">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-718">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-719">286.25</span><span class="sxs-lookup"><span data-stu-id="e74e6-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-720">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="e74e6-721">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-721">CC003</span></span></td>
<td><span data-ttu-id="e74e6-722">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="e74e6-722">Packaging</span></span></td>
<td><span data-ttu-id="e74e6-723">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-723">10001</span></span></td>
<td><span data-ttu-id="e74e6-724">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-724">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-725">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-725">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="e74e6-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-727">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="e74e6-728">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-728">Prod 1</span></span></td>
<td><span data-ttu-id="e74e6-729">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-729">Product 1</span></span></td>
<td><span data-ttu-id="e74e6-730">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-730">10001</span></span></td>
<td><span data-ttu-id="e74e6-731">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-731">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-732">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-732">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-733">776.36</span><span class="sxs-lookup"><span data-stu-id="e74e6-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-734">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="e74e6-735">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-735">Prod 1</span></span></td>
<td><span data-ttu-id="e74e6-736">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-736">Product 1</span></span></td>
<td><span data-ttu-id="e74e6-737">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-737">10001</span></span></td>
<td><span data-ttu-id="e74e6-738">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-738">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-739">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-739">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="e74e6-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-741">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="e74e6-742">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-742">Prod 2</span></span></td>
<td><span data-ttu-id="e74e6-743">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-743">Product 1</span></span></td>
<td><span data-ttu-id="e74e6-744">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-744">10001</span></span></td>
<td><span data-ttu-id="e74e6-745">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-745">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-746">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-746">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-747">223.64</span><span class="sxs-lookup"><span data-stu-id="e74e6-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-748">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="e74e6-749">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-749">Prod 2</span></span></td>
<td><span data-ttu-id="e74e6-750">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-750">Product 1</span></span></td>
<td><span data-ttu-id="e74e6-751">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-751">10001</span></span></td>
<td><span data-ttu-id="e74e6-752">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-752">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-753">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-753">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="e74e6-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e74e6-755">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="e74e6-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e74e6-756">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e74e6-757">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="e74e6-757">Cost element</span></span></th>
<th><span data-ttu-id="e74e6-758">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="e74e6-758">Cost behavior</span></span></th>
<th><span data-ttu-id="e74e6-759">Summa</span><span class="sxs-lookup"><span data-stu-id="e74e6-759">Amount</span></span></th>
<th><span data-ttu-id="e74e6-760">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="e74e6-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e74e6-761">CC001</span><span class="sxs-lookup"><span data-stu-id="e74e6-761">CC001</span></span></td>
<td><span data-ttu-id="e74e6-762">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="e74e6-762">HR</span></span></td>
<td><span data-ttu-id="e74e6-763">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-763">10001</span></span></td>
<td><span data-ttu-id="e74e6-764">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-764">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-765">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-765">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-766">-500.00</span></span></td>
<td><span data-ttu-id="e74e6-767">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-768">CC002</span><span class="sxs-lookup"><span data-stu-id="e74e6-768">CC002</span></span></td>
<td><span data-ttu-id="e74e6-769">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="e74e6-769">Finance</span></span></td>
<td><span data-ttu-id="e74e6-770">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-770">10001</span></span></td>
<td><span data-ttu-id="e74e6-771">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-771">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-772">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-772">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-773">175.00</span><span class="sxs-lookup"><span data-stu-id="e74e6-773">175.00</span></span></td>
<td><span data-ttu-id="e74e6-774">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-775">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-775">CC003</span></span></td>
<td><span data-ttu-id="e74e6-776">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="e74e6-776">Assembly</span></span></td>
<td><span data-ttu-id="e74e6-777">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-777">10001</span></span></td>
<td><span data-ttu-id="e74e6-778">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-778">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-779">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-779">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-780">275.00</span><span class="sxs-lookup"><span data-stu-id="e74e6-780">275.00</span></span></td>
<td><span data-ttu-id="e74e6-781">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-782">CC004</span><span class="sxs-lookup"><span data-stu-id="e74e6-782">CC004</span></span></td>
<td><span data-ttu-id="e74e6-783">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="e74e6-783">Packaging</span></span></td>
<td><span data-ttu-id="e74e6-784">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-784">10001</span></span></td>
<td><span data-ttu-id="e74e6-785">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-785">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-786">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-786">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-787">50,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-787">50,00</span></span></td>
<td><span data-ttu-id="e74e6-788">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-789">CC001</span><span class="sxs-lookup"><span data-stu-id="e74e6-789">CC001</span></span></td>
<td><span data-ttu-id="e74e6-790">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="e74e6-790">HR</span></span></td>
<td><span data-ttu-id="e74e6-791">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-791">10001</span></span></td>
<td><span data-ttu-id="e74e6-792">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-792">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-793">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-793">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="e74e6-794">-1,245.71</span></span></td>
<td><span data-ttu-id="e74e6-795">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-796">CC002</span><span class="sxs-lookup"><span data-stu-id="e74e6-796">CC002</span></span></td>
<td><span data-ttu-id="e74e6-797">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="e74e6-797">Finance</span></span></td>
<td><span data-ttu-id="e74e6-798">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-798">10001</span></span></td>
<td><span data-ttu-id="e74e6-799">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-799">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-800">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-800">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-801">436.00</span><span class="sxs-lookup"><span data-stu-id="e74e6-801">436.00</span></span></td>
<td><span data-ttu-id="e74e6-802">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-803">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-803">CC003</span></span></td>
<td><span data-ttu-id="e74e6-804">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="e74e6-804">Assembly</span></span></td>
<td><span data-ttu-id="e74e6-805">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-805">10001</span></span></td>
<td><span data-ttu-id="e74e6-806">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-806">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-807">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-807">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-808">685.14</span><span class="sxs-lookup"><span data-stu-id="e74e6-808">685.14</span></span></td>
<td><span data-ttu-id="e74e6-809">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-810">CC004</span><span class="sxs-lookup"><span data-stu-id="e74e6-810">CC004</span></span></td>
<td><span data-ttu-id="e74e6-811">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="e74e6-811">Packaging</span></span></td>
<td><span data-ttu-id="e74e6-812">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-812">10001</span></span></td>
<td><span data-ttu-id="e74e6-813">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-813">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-814">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-814">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-815">124.57</span><span class="sxs-lookup"><span data-stu-id="e74e6-815">124.57</span></span></td>
<td><span data-ttu-id="e74e6-816">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-817">CC002</span><span class="sxs-lookup"><span data-stu-id="e74e6-817">CC002</span></span></td>
<td><span data-ttu-id="e74e6-818">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="e74e6-818">Finance</span></span></td>
<td><span data-ttu-id="e74e6-819">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-819">10001</span></span></td>
<td><span data-ttu-id="e74e6-820">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-820">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-821">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-821">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-822">-675.00</span></span></td>
<td><span data-ttu-id="e74e6-823">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-824">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-824">CC003</span></span></td>
<td><span data-ttu-id="e74e6-825">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="e74e6-825">Assembly</span></span></td>
<td><span data-ttu-id="e74e6-826">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-826">10001</span></span></td>
<td><span data-ttu-id="e74e6-827">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-827">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-828">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-828">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-829">438.75</span><span class="sxs-lookup"><span data-stu-id="e74e6-829">438.75</span></span></td>
<td><span data-ttu-id="e74e6-830">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-831">CC004</span><span class="sxs-lookup"><span data-stu-id="e74e6-831">CC004</span></span></td>
<td><span data-ttu-id="e74e6-832">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="e74e6-832">Packaging</span></span></td>
<td><span data-ttu-id="e74e6-833">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-833">10001</span></span></td>
<td><span data-ttu-id="e74e6-834">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-834">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-835">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-835">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-836">236.25</span><span class="sxs-lookup"><span data-stu-id="e74e6-836">236.25</span></span></td>
<td><span data-ttu-id="e74e6-837">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-838">CC002</span><span class="sxs-lookup"><span data-stu-id="e74e6-838">CC002</span></span></td>
<td><span data-ttu-id="e74e6-839">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="e74e6-839">Finance</span></span></td>
<td><span data-ttu-id="e74e6-840">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-840">10001</span></span></td>
<td><span data-ttu-id="e74e6-841">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-841">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-842">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-842">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="e74e6-843">-8,150.29</span></span></td>
<td><span data-ttu-id="e74e6-844">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-845">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-845">CC003</span></span></td>
<td><span data-ttu-id="e74e6-846">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="e74e6-846">Assembly</span></span></td>
<td><span data-ttu-id="e74e6-847">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-847">10001</span></span></td>
<td><span data-ttu-id="e74e6-848">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-848">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-849">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-849">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="e74e6-850">5,297.69</span></span></td>
<td><span data-ttu-id="e74e6-851">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-852">CC004</span><span class="sxs-lookup"><span data-stu-id="e74e6-852">CC004</span></span></td>
<td><span data-ttu-id="e74e6-853">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="e74e6-853">Packaging</span></span></td>
<td><span data-ttu-id="e74e6-854">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-854">10001</span></span></td>
<td><span data-ttu-id="e74e6-855">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-855">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-856">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-856">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="e74e6-857">2,852.60</span></span></td>
<td><span data-ttu-id="e74e6-858">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-859">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-859">CC003</span></span></td>
<td><span data-ttu-id="e74e6-860">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="e74e6-860">Assembly</span></span></td>
<td><span data-ttu-id="e74e6-861">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-861">10001</span></span></td>
<td><span data-ttu-id="e74e6-862">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-862">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-863">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-863">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="e74e6-864">-713.75</span></span></td>
<td><span data-ttu-id="e74e6-865">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-866">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-866">Prod 1</span></span></td>
<td><span data-ttu-id="e74e6-867">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-867">Product 1</span></span></td>
<td><span data-ttu-id="e74e6-868">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-868">10001</span></span></td>
<td><span data-ttu-id="e74e6-869">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-869">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-870">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-870">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-871">535.31</span><span class="sxs-lookup"><span data-stu-id="e74e6-871">535.31</span></span></td>
<td><span data-ttu-id="e74e6-872">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-873">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-873">Prod 2</span></span></td>
<td><span data-ttu-id="e74e6-874">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-874">Product 2</span></span></td>
<td><span data-ttu-id="e74e6-875">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-875">10001</span></span></td>
<td><span data-ttu-id="e74e6-876">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-876">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-877">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-877">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-878">178.44</span><span class="sxs-lookup"><span data-stu-id="e74e6-878">178.44</span></span></td>
<td><span data-ttu-id="e74e6-879">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-880">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-880">CC003</span></span></td>
<td><span data-ttu-id="e74e6-881">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="e74e6-881">Assembly</span></span></td>
<td><span data-ttu-id="e74e6-882">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-882">10001</span></span></td>
<td><span data-ttu-id="e74e6-883">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-883">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-884">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-884">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="e74e6-885">-5,982.83</span></span></td>
<td><span data-ttu-id="e74e6-886">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-887">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-887">Prod 1</span></span></td>
<td><span data-ttu-id="e74e6-888">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-888">Product 1</span></span></td>
<td><span data-ttu-id="e74e6-889">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-889">10001</span></span></td>
<td><span data-ttu-id="e74e6-890">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-890">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-891">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-891">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="e74e6-892">4,487.12</span></span></td>
<td><span data-ttu-id="e74e6-893">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-894">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-894">Prod 2</span></span></td>
<td><span data-ttu-id="e74e6-895">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-895">Product 2</span></span></td>
<td><span data-ttu-id="e74e6-896">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-896">10001</span></span></td>
<td><span data-ttu-id="e74e6-897">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-897">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-898">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-898">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="e74e6-899">1,495.71</span></span></td>
<td><span data-ttu-id="e74e6-900">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-901">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-901">CC003</span></span></td>
<td><span data-ttu-id="e74e6-902">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="e74e6-902">Assembly</span></span></td>
<td><span data-ttu-id="e74e6-903">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-903">10001</span></span></td>
<td><span data-ttu-id="e74e6-904">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-904">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-905">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-905">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="e74e6-906">-286.25</span></span></td>
<td><span data-ttu-id="e74e6-907">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-908">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-908">Prod 1</span></span></td>
<td><span data-ttu-id="e74e6-909">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-909">Product 1</span></span></td>
<td><span data-ttu-id="e74e6-910">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-910">10001</span></span></td>
<td><span data-ttu-id="e74e6-911">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-911">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-912">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-912">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-913">241.05</span><span class="sxs-lookup"><span data-stu-id="e74e6-913">241.05</span></span></td>
<td><span data-ttu-id="e74e6-914">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-915">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-915">Prod 2</span></span></td>
<td><span data-ttu-id="e74e6-916">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-916">Product 2</span></span></td>
<td><span data-ttu-id="e74e6-917">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-917">10001</span></span></td>
<td><span data-ttu-id="e74e6-918">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-918">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-919">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-919">Fixed cost</span></span></td>
<td><span data-ttu-id="e74e6-920">45.20</span><span class="sxs-lookup"><span data-stu-id="e74e6-920">45.20</span></span></td>
<td><span data-ttu-id="e74e6-921">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-922">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-922">CC003</span></span></td>
<td><span data-ttu-id="e74e6-923">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="e74e6-923">Assembly</span></span></td>
<td><span data-ttu-id="e74e6-924">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-924">10001</span></span></td>
<td><span data-ttu-id="e74e6-925">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-925">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-926">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-926">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-927">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="e74e6-927">-2,977.17</span></span></td>
<td><span data-ttu-id="e74e6-928">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-929">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-929">Prod 1</span></span></td>
<td><span data-ttu-id="e74e6-930">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-930">Product 1</span></span></td>
<td><span data-ttu-id="e74e6-931">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-931">10001</span></span></td>
<td><span data-ttu-id="e74e6-932">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-932">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-933">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-933">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="e74e6-934">2,507.09</span></span></td>
<td><span data-ttu-id="e74e6-935">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e74e6-936">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-936">Prod 2</span></span></td>
<td><span data-ttu-id="e74e6-937">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-937">Product 2</span></span></td>
<td><span data-ttu-id="e74e6-938">10 001</span><span class="sxs-lookup"><span data-stu-id="e74e6-938">10001</span></span></td>
<td><span data-ttu-id="e74e6-939">Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-939">Electricity</span></span></td>
<td><span data-ttu-id="e74e6-940">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-940">Variable cost</span></span></td>
<td><span data-ttu-id="e74e6-941">470.08</span><span class="sxs-lookup"><span data-stu-id="e74e6-941">470.08</span></span></td>
<td><span data-ttu-id="e74e6-942">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="e74e6-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="e74e6-943">Johtopäätökset</span><span class="sxs-lookup"><span data-stu-id="e74e6-943">Conclusion</span></span>
<span data-ttu-id="e74e6-944">Kirjanpidossa kirjataan tyhjään kustannuspaikkatunnukseen sähkökustannus arvolla 10 000,00.</span><span class="sxs-lookup"><span data-stu-id="e74e6-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="e74e6-945">Tämän ansiosta kustannuslaskijat tietävät, että kustannus on kohdistettava.</span><span class="sxs-lookup"><span data-stu-id="e74e6-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="e74e6-946">Kustannukset virtaavat kirjanpidossa organisaation yksiköiden ja tasojen läpi käytössä olevien käytäntöjen ja sääntöjen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="e74e6-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="e74e6-947">Kukin kustannus on liitetty kustannusperusteeseen, joka sisältää parhaan arvion kustannusten kohdistuksesta.</span><span class="sxs-lookup"><span data-stu-id="e74e6-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="e74e6-948">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="e74e6-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="e74e6-949">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="e74e6-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="e74e6-950">Yhteensä</span><span class="sxs-lookup"><span data-stu-id="e74e6-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="e74e6-951">CC099</span><span class="sxs-lookup"><span data-stu-id="e74e6-951">CC099</span></span></th>
<th><span data-ttu-id="e74e6-952">CC001</span><span class="sxs-lookup"><span data-stu-id="e74e6-952">CC001</span></span></th>
<th><span data-ttu-id="e74e6-953">CC002</span><span class="sxs-lookup"><span data-stu-id="e74e6-953">CC002</span></span></th>
<th><span data-ttu-id="e74e6-954">CC003</span><span class="sxs-lookup"><span data-stu-id="e74e6-954">CC003</span></span></th>
<th><span data-ttu-id="e74e6-955">CC004</span><span class="sxs-lookup"><span data-stu-id="e74e6-955">CC004</span></span></th>
<th><span data-ttu-id="e74e6-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-956">Proj 1</span></span></th>
<th><span data-ttu-id="e74e6-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-957">Proj 2</span></span></th>
<th><span data-ttu-id="e74e6-958">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="e74e6-958">Prod 1</span></span></th>
<th><span data-ttu-id="e74e6-959">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="e74e6-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="e74e6-960">10001 Sähkö</span><span class="sxs-lookup"><span data-stu-id="e74e6-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="e74e6-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="e74e6-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="e74e6-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="e74e6-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="e74e6-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="e74e6-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="e74e6-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="e74e6-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="e74e6-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="e74e6-970">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="e74e6-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-971">0,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="e74e6-972">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="e74e6-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-973">0,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-974">0,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-975">0,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-976">0,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-977">0,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-978">776.36</span><span class="sxs-lookup"><span data-stu-id="e74e6-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-979">223.64</span><span class="sxs-lookup"><span data-stu-id="e74e6-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="e74e6-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="e74e6-981">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="e74e6-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-982">000</span><span class="sxs-lookup"><span data-stu-id="e74e6-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-983">0,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-984">0,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-985">0,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-986">0,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-987">30,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-988">10,00</span><span class="sxs-lookup"><span data-stu-id="e74e6-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="e74e6-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="e74e6-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e74e6-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="e74e6-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e74e6-992">Tässä ohjeaiheessa esitellään, miten ensisijainen kustannuselementti, 10001 Sähkö, virtaa kustannusobjektien läpi.</span><span class="sxs-lookup"><span data-stu-id="e74e6-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="e74e6-993">Tästä syystä tämä yleiskustannus kohdistetaan organisaation alimmalle tasolle.</span><span class="sxs-lookup"><span data-stu-id="e74e6-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="e74e6-994">Toisin sanoen alimman tason kustannusobjektit kantavat kustannuksen.</span><span class="sxs-lookup"><span data-stu-id="e74e6-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="e74e6-995">Jos tarvitset visuaalisen näkymän kustannuksen virrasta kustannusobjektien välillä, voit käyttää kustannuksen koontikäytäntösääntöjä kustannusvirran visualisointiin.</span><span class="sxs-lookup"><span data-stu-id="e74e6-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="e74e6-996">Lisätietoja on kohdassa [Kustannusten koonti](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="e74e6-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



