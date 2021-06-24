---
title: Yleiskustannuslaskenta
description: Tässä aiheessa kuvataan tyypillinen yleiskustannusten laskenta- ja kohdistusprosessi.
author: AndersGirke
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 8dc312e66dc666ac6c23bac6b705ffc7893fd06b
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187994"
---
# <a name="overhead-calculation"></a><span data-ttu-id="5898b-103">Yleiskustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="5898b-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5898b-104">Tässä aiheessa kuvataan tyypillinen yleiskustannusten laskenta- ja kohdistusprosessi.</span><span class="sxs-lookup"><span data-stu-id="5898b-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

## <a name="term-definition"></a><span data-ttu-id="5898b-105">Sanaston määritelmä</span><span class="sxs-lookup"><span data-stu-id="5898b-105">Term definition</span></span>

<span data-ttu-id="5898b-106">Yleiskustannukset ovat yrityksen toiminnasta syntyviä kustannuksia, joita ei voi suoraan liittää mihinkään tiettyyn liiketoiminnan tehtävään, tuotteeseen tai palveluun.</span><span class="sxs-lookup"><span data-stu-id="5898b-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="5898b-107">Yleiskustannukset ovat tärkeä tuki voittoa tuottavien tehtävien luonnissa.</span><span class="sxs-lookup"><span data-stu-id="5898b-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="5898b-108">Seuraavassa on joitakin esimerkkejä yleiskustannuksista:</span><span class="sxs-lookup"><span data-stu-id="5898b-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="5898b-109">Vuokra</span><span class="sxs-lookup"><span data-stu-id="5898b-109">Rent</span></span>
-   <span data-ttu-id="5898b-110">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-110">Electricity</span></span>
-   <span data-ttu-id="5898b-111">Hallinnon palkat</span><span class="sxs-lookup"><span data-stu-id="5898b-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="5898b-112">Yleiskustannuslaskennan yleiskuva</span><span class="sxs-lookup"><span data-stu-id="5898b-112">Overhead calculation overview</span></span>
<span data-ttu-id="5898b-113">Yleiskustannusten laskenta suorittaa kustannuslaskennan käytännöt oikeassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="5898b-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="5898b-114">Yleiskustannusten laskennan voi suorittaa useita kertoja samalle tilikaudelle, jos kustannuslaskennan käytännöt ovat muuttuneet tai erityisiä virheitä on havaittu.</span><span class="sxs-lookup"><span data-stu-id="5898b-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="5898b-115">Kukin laskenta-ajo tallennetaan ja kullekin annetaan yksilöllinen versiotunnus, jonka avulla eri laskenta-ajoja voi verrata toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="5898b-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="5898b-116">Yleiskustannusten laskenta luo kustannustapahtumia, joille annetaan kirjauspäivä.</span><span class="sxs-lookup"><span data-stu-id="5898b-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="5898b-117">Kirjauspäivä vastaa laskennassa käytettyä tilikauden päättymispäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="5898b-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="5898b-118">Yksilöivä versiotunnus sisältää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="5898b-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="5898b-119">Versiotyyppi</span><span class="sxs-lookup"><span data-stu-id="5898b-119">Version type</span></span>
-   <span data-ttu-id="5898b-120">Päivämäärä ja aika</span><span class="sxs-lookup"><span data-stu-id="5898b-120">Date and time</span></span>
-   <span data-ttu-id="5898b-121">Kustannuslaskennan kirjanpito</span><span class="sxs-lookup"><span data-stu-id="5898b-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="5898b-122">Tilikausi </span><span class="sxs-lookup"><span data-stu-id="5898b-122">Fiscal year</span></span>
-   <span data-ttu-id="5898b-123">Tilikausi  </span><span class="sxs-lookup"><span data-stu-id="5898b-123">Fiscal period</span></span>

<span data-ttu-id="5898b-124">Yleiskustannusten laskenta ajetaan versiosta riippumattomana.</span><span class="sxs-lookup"><span data-stu-id="5898b-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="5898b-125">Voit siis laskea budjetin version ennen todellista versiota.</span><span class="sxs-lookup"><span data-stu-id="5898b-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="5898b-126">Yleiskustannusten laskenta koostuu neljästä vaiheesta, jotka esitellään seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="5898b-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="5898b-127">Kussakin vaiheessa luodaan kirjauskansion otsikko, jolla on kirjauskansiovientejä.</span><span class="sxs-lookup"><span data-stu-id="5898b-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="5898b-128">Tämä kirjauskansion otsikko säilyttää kunkin laskentavaiheen syöttötiedot.</span><span class="sxs-lookup"><span data-stu-id="5898b-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="5898b-129">Käytännöt ja säännöt ajetaan kullekin kirjauskansion riville, ja tuloksena luodaan kustannustapahtumia.</span><span class="sxs-lookup"><span data-stu-id="5898b-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="5898b-130">Tämän ansiosta kaikki laskutoimitukset ovat täysin jäljitettävissä.</span><span class="sxs-lookup"><span data-stu-id="5898b-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="5898b-131">[![Yleiskustannuslaskenta](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="5898b-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="5898b-132">Laske ja kohdista sähkön yleiskustannukset</span><span class="sxs-lookup"><span data-stu-id="5898b-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="5898b-133">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="5898b-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="5898b-134">Tarkka johdon näkymä ei täten ole saatavilla kustannuslaskennassa.</span><span class="sxs-lookup"><span data-stu-id="5898b-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="5898b-135">Jotta kustannuslaskenta tarjoaisi oikean johdon näkymän kaikista organisaation yksiköistä ja tasoista, kustannusten on virrattava organisaation yksiköiden läpi.</span><span class="sxs-lookup"><span data-stu-id="5898b-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="5898b-136">Tämän virran on perustuttava joko tarkkaan tietoon kulutuksesta tai perusteltuun arvioon.</span><span class="sxs-lookup"><span data-stu-id="5898b-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="5898b-137">Sähkökustannukset voi kirjata kirjanpitoon seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="5898b-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5898b-138">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="5898b-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5898b-139">Kustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5898b-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="5898b-140">Päätili</span><span class="sxs-lookup"><span data-stu-id="5898b-140">Main account</span></span></th>
<th><span data-ttu-id="5898b-141">Summa kirjanpitovaluuttana</span><span class="sxs-lookup"><span data-stu-id="5898b-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-142">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="5898b-143">CC099</span><span class="sxs-lookup"><span data-stu-id="5898b-143">CC099</span></span></td>
<td><span data-ttu-id="5898b-144">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5898b-144">Default cost center</span></span></td>
<td><span data-ttu-id="5898b-145">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-145">10001</span></span></td>
<td><span data-ttu-id="5898b-146">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-146">Electricity</span></span></td>
<td><span data-ttu-id="5898b-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="5898b-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="5898b-148">Vaihe 1: Käsittele kustannustoiminnan laskenta</span><span class="sxs-lookup"><span data-stu-id="5898b-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="5898b-149">Kun kustannustapahtumat tuodaan lähdetiedoista, niille asetetaan kustannuslaskennassa oletusarvoisesti **Luokittelematon** -kustannustoimintaluokka.</span><span class="sxs-lookup"><span data-stu-id="5898b-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="5898b-150">Voit luokitella kustannustapahtumia uudelleen **kiinteäksi kustannukseksi** tai **muuttuvaksi kustannukseksi** kustannustoiminnan käytäntösäännöillä.</span><span class="sxs-lookup"><span data-stu-id="5898b-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="5898b-151">Määritä kustannustoiminnan sääntö</span><span class="sxs-lookup"><span data-stu-id="5898b-151">Define the cost behavior rule</span></span>

<span data-ttu-id="5898b-152">Joissain tapauksissa osa kustannuksesta on kiinteä ja loppuosa perustuu kulutukseen.</span><span class="sxs-lookup"><span data-stu-id="5898b-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="5898b-153">Sähkölaskut sopivat usein tähän määritelmään.</span><span class="sxs-lookup"><span data-stu-id="5898b-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="5898b-154">Maksat ensin määrätyn, kiinteän maksun, jonka lisäksi maksat kulutuksesta kilowattitunteina (kWh).</span><span class="sxs-lookup"><span data-stu-id="5898b-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="5898b-155">Jos kiinteä maksu on esimerkiksi 1 000,00, kustannustoiminnan sääntö määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="5898b-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="5898b-156">Kiinteä määrä 1 000,00</span><span class="sxs-lookup"><span data-stu-id="5898b-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="5898b-157">0 &lt;= 1 000,00 = Kiinteä</span><span class="sxs-lookup"><span data-stu-id="5898b-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="5898b-158">1000,01 &lt; N = Muuttuva</span><span class="sxs-lookup"><span data-stu-id="5898b-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="5898b-159">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5898b-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5898b-160">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5898b-160">Journal</span></span></th>
<th><span data-ttu-id="5898b-161">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="5898b-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5898b-162">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="5898b-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5898b-163">Versio</span><span class="sxs-lookup"><span data-stu-id="5898b-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-164">00001</span><span class="sxs-lookup"><span data-stu-id="5898b-164">00001</span></span></td>
<td><span data-ttu-id="5898b-165">Kustannustoiminnan laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5898b-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="5898b-166">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="5898b-166">Fiscal</span></span></td>
<td><span data-ttu-id="5898b-167">2017</span><span class="sxs-lookup"><span data-stu-id="5898b-167">2017</span></span></td>
<td><span data-ttu-id="5898b-168">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="5898b-168">Period 1</span></span></td>
<td><span data-ttu-id="5898b-169">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="5898b-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5898b-170">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="5898b-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5898b-171">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="5898b-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5898b-172">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5898b-173">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="5898b-173">Cost element</span></span></th>
<th><span data-ttu-id="5898b-174">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5898b-174">Cost behavior</span></span></th>
<th><span data-ttu-id="5898b-175">Summa</span><span class="sxs-lookup"><span data-stu-id="5898b-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-176">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="5898b-177">CC099</span><span class="sxs-lookup"><span data-stu-id="5898b-177">CC099</span></span></td>
<td><span data-ttu-id="5898b-178">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5898b-178">Default cost center</span></span></td>
<td><span data-ttu-id="5898b-179">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-179">10001</span></span></td>
<td><span data-ttu-id="5898b-180">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-180">Electricity</span></span></td>
<td><span data-ttu-id="5898b-181">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="5898b-181">Unclassified</span></span></td>
<td><span data-ttu-id="5898b-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="5898b-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5898b-183">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="5898b-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5898b-184">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5898b-185">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="5898b-185">Cost element</span></span></th>
<th><span data-ttu-id="5898b-186">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5898b-186">Cost behavior</span></span></th>
<th><span data-ttu-id="5898b-187">Summa</span><span class="sxs-lookup"><span data-stu-id="5898b-187">Amount</span></span></th>
<th><span data-ttu-id="5898b-188">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="5898b-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-189">CC099</span><span class="sxs-lookup"><span data-stu-id="5898b-189">CC099</span></span></td>
<td><span data-ttu-id="5898b-190">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5898b-190">Default cost center</span></span></td>
<td><span data-ttu-id="5898b-191">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-191">10001</span></span></td>
<td><span data-ttu-id="5898b-192">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-192">Electricity</span></span></td>
<td><span data-ttu-id="5898b-193">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="5898b-193">Unclassified</span></span></td>
<td><span data-ttu-id="5898b-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="5898b-194">10,000.00</span></span></td>
<td><span data-ttu-id="5898b-195">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-196">CC099</span><span class="sxs-lookup"><span data-stu-id="5898b-196">CC099</span></span></td>
<td><span data-ttu-id="5898b-197">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5898b-197">Default cost center</span></span></td>
<td><span data-ttu-id="5898b-198">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-198">10001</span></span></td>
<td><span data-ttu-id="5898b-199">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-199">Electricity</span></span></td>
<td><span data-ttu-id="5898b-200">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="5898b-200">Unclassified</span></span></td>
<td><span data-ttu-id="5898b-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="5898b-201">-10,000.00</span></span></td>
<td><span data-ttu-id="5898b-202">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-203">CC099</span><span class="sxs-lookup"><span data-stu-id="5898b-203">CC099</span></span></td>
<td><span data-ttu-id="5898b-204">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5898b-204">Default cost center</span></span></td>
<td><span data-ttu-id="5898b-205">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-205">10001</span></span></td>
<td><span data-ttu-id="5898b-206">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-206">Electricity</span></span></td>
<td><span data-ttu-id="5898b-207">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-207">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="5898b-208">1,000.00</span></span></td>
<td><span data-ttu-id="5898b-209">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-210">CC099</span><span class="sxs-lookup"><span data-stu-id="5898b-210">CC099</span></span></td>
<td><span data-ttu-id="5898b-211">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5898b-211">Default cost center</span></span></td>
<td><span data-ttu-id="5898b-212">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-212">10001</span></span></td>
<td><span data-ttu-id="5898b-213">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-213">Electricity</span></span></td>
<td><span data-ttu-id="5898b-214">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-214">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="5898b-215">9,000.00</span></span></td>
<td><span data-ttu-id="5898b-216">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5898b-217">Lisätietoja on kohdassa [Kustannustoimintakäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="5898b-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="5898b-218">Vaihe 2: Käsittele kustannusten jaon laskenta</span><span class="sxs-lookup"><span data-stu-id="5898b-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="5898b-219">Kustannusten jakoa käytetään kustannusten jakamiseen yhdestä kustannusobjektista toiseen (tai useampaan kustannusobjektiin) määrittämällä asiaankuuluvan kohdistusperusteen.</span><span class="sxs-lookup"><span data-stu-id="5898b-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="5898b-220">Kustannusten jako ja kustannusten kohdistus eroavat toisistaan sillä, että kustannusten jako tapahtuu aina alkuperäisen kustannuksen ensisijaisen kustannuselementin tasolla.</span><span class="sxs-lookup"><span data-stu-id="5898b-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="5898b-221">Määritä kustannusten jaon sääntö</span><span class="sxs-lookup"><span data-stu-id="5898b-221">Define the cost distribution rule</span></span>

<span data-ttu-id="5898b-222">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="5898b-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="5898b-223">Kustannuslaskenta ei tarjoa tästä tarpeeksi tarkkoja tietoja.</span><span class="sxs-lookup"><span data-stu-id="5898b-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="5898b-224">Muuttuva kustannus tulisi jakaa yksittäisille kustannusobjekteille reiluin perustein.</span><span class="sxs-lookup"><span data-stu-id="5898b-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="5898b-225">Loogisin kohdistusperuste on sähkönkulutus (kWh).</span><span class="sxs-lookup"><span data-stu-id="5898b-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="5898b-226">Luodaan tilastollinen dimensionjäsen nimeltä Sähkö, johon kirjataan sähkönkulutus.</span><span class="sxs-lookup"><span data-stu-id="5898b-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="5898b-227">Oletusarvon mukaan kaikki tilastolliset dimensiojäsenet ovat käytettävissä kohdistusperusteina.</span><span class="sxs-lookup"><span data-stu-id="5898b-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5898b-228">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-228">Cost object</span></span></th>
<th><span data-ttu-id="5898b-229">kWh</span><span class="sxs-lookup"><span data-stu-id="5898b-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-230">CC001</span><span class="sxs-lookup"><span data-stu-id="5898b-230">CC001</span></span></td>
<td><span data-ttu-id="5898b-231">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5898b-231">HR</span></span></td>
<td><span data-ttu-id="5898b-232">1 000</span><span class="sxs-lookup"><span data-stu-id="5898b-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-233">CC002</span><span class="sxs-lookup"><span data-stu-id="5898b-233">CC002</span></span></td>
<td><span data-ttu-id="5898b-234">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5898b-234">Finance</span></span></td>
<td><span data-ttu-id="5898b-235">6,000</span><span class="sxs-lookup"><span data-stu-id="5898b-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-236">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-236">CC003</span></span></td>
<td><span data-ttu-id="5898b-237">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5898b-237">Assembly</span></span></td>
<td><span data-ttu-id="5898b-238">0</span><span class="sxs-lookup"><span data-stu-id="5898b-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5898b-239">Seuraavassa taulukossa on esitetty tulos, kun sähkönkulutusta käytetään kohdistusperusteena muuttuville kuluille.</span><span class="sxs-lookup"><span data-stu-id="5898b-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5898b-240">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-240">Cost object</span></span></th>
<th><span data-ttu-id="5898b-241">Suuruus</span><span class="sxs-lookup"><span data-stu-id="5898b-241">Magnitude</span></span></th>
<th><span data-ttu-id="5898b-242">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="5898b-242">Allocation factor</span></span></th>
<th><span data-ttu-id="5898b-243">Summa</span><span class="sxs-lookup"><span data-stu-id="5898b-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-244">CC001</span><span class="sxs-lookup"><span data-stu-id="5898b-244">CC001</span></span></td>
<td><span data-ttu-id="5898b-245">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5898b-245">HR</span></span></td>
<td><span data-ttu-id="5898b-246">1 000</span><span class="sxs-lookup"><span data-stu-id="5898b-246">1,000</span></span></td>
<td><span data-ttu-id="5898b-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="5898b-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5898b-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="5898b-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-249">CC002</span><span class="sxs-lookup"><span data-stu-id="5898b-249">CC002</span></span></td>
<td><span data-ttu-id="5898b-250">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5898b-250">Finance</span></span></td>
<td><span data-ttu-id="5898b-251">6,000</span><span class="sxs-lookup"><span data-stu-id="5898b-251">6,000</span></span></td>
<td><span data-ttu-id="5898b-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="5898b-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5898b-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="5898b-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-254">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-254">CC003</span></span></td>
<td><span data-ttu-id="5898b-255">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5898b-255">Assembly</span></span></td>
<td><span data-ttu-id="5898b-256">0</span><span class="sxs-lookup"><span data-stu-id="5898b-256">0</span></span></td>
<td><span data-ttu-id="5898b-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="5898b-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5898b-258">0,00</span><span class="sxs-lookup"><span data-stu-id="5898b-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5898b-259">Kiinteä kustannus tulisi jakaa tasaisesti yksittäisille kustannusobjekteille, jotka ovat kuluttaneet sähköä.</span><span class="sxs-lookup"><span data-stu-id="5898b-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="5898b-260">Voit käyttää sähkön tilastollista dimensiojäsentä kaavan kohdistusperusteena tämän tavoitteen saavuttamiseksi: (sähkö &gt;0,00) Seuraavassa taulukossa on esitetty tulos siitä, kun sähkönkulutus on määritetty muuttuvien kustannusten kohdistusperusteeksi.</span><span class="sxs-lookup"><span data-stu-id="5898b-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5898b-261">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-261">Cost object</span></span></th>
<th><span data-ttu-id="5898b-262">Resepti</span><span class="sxs-lookup"><span data-stu-id="5898b-262">Formula</span></span></th>
<th><span data-ttu-id="5898b-263">Suuruus</span><span class="sxs-lookup"><span data-stu-id="5898b-263">Magnitude</span></span></th>
<th><span data-ttu-id="5898b-264">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="5898b-264">Allocation factor</span></span></th>
<th><span data-ttu-id="5898b-265">Summa</span><span class="sxs-lookup"><span data-stu-id="5898b-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-266">CC001</span><span class="sxs-lookup"><span data-stu-id="5898b-266">CC001</span></span></td>
<td><span data-ttu-id="5898b-267">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5898b-267">HR</span></span></td>
<td><span data-ttu-id="5898b-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="5898b-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5898b-269">1</span><span class="sxs-lookup"><span data-stu-id="5898b-269">1</span></span></td>
<td><span data-ttu-id="5898b-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="5898b-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5898b-271">500,00</span><span class="sxs-lookup"><span data-stu-id="5898b-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-272">CC002</span><span class="sxs-lookup"><span data-stu-id="5898b-272">CC002</span></span></td>
<td><span data-ttu-id="5898b-273">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5898b-273">Finance</span></span></td>
<td><span data-ttu-id="5898b-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="5898b-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5898b-275">1</span><span class="sxs-lookup"><span data-stu-id="5898b-275">1</span></span></td>
<td><span data-ttu-id="5898b-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="5898b-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5898b-277">500,00</span><span class="sxs-lookup"><span data-stu-id="5898b-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-278">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-278">CC003</span></span></td>
<td><span data-ttu-id="5898b-279">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5898b-279">Assembly</span></span></td>
<td><span data-ttu-id="5898b-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="5898b-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5898b-281">0</span><span class="sxs-lookup"><span data-stu-id="5898b-281">0</span></span></td>
<td><span data-ttu-id="5898b-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="5898b-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5898b-283">0,00</span><span class="sxs-lookup"><span data-stu-id="5898b-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="5898b-284">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5898b-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5898b-285">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5898b-285">Journal</span></span></th>
<th><span data-ttu-id="5898b-286">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="5898b-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5898b-287">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="5898b-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5898b-288">Versio</span><span class="sxs-lookup"><span data-stu-id="5898b-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-289">00002</span><span class="sxs-lookup"><span data-stu-id="5898b-289">00002</span></span></td>
<td><span data-ttu-id="5898b-290">Kustannusten jaon laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5898b-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="5898b-291">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="5898b-291">Fiscal</span></span></td>
<td><span data-ttu-id="5898b-292">2017</span><span class="sxs-lookup"><span data-stu-id="5898b-292">2017</span></span></td>
<td><span data-ttu-id="5898b-293">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="5898b-293">Period 1</span></span></td>
<td><span data-ttu-id="5898b-294">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="5898b-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5898b-295">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="5898b-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5898b-296">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="5898b-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5898b-297">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5898b-298">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="5898b-298">Cost element</span></span></th>
<th><span data-ttu-id="5898b-299">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5898b-299">Cost behavior</span></span></th>
<th><span data-ttu-id="5898b-300">Summa</span><span class="sxs-lookup"><span data-stu-id="5898b-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-301">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="5898b-302">CC099</span><span class="sxs-lookup"><span data-stu-id="5898b-302">CC099</span></span></td>
<td><span data-ttu-id="5898b-303">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5898b-303">Default cost center</span></span></td>
<td><span data-ttu-id="5898b-304">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-304">10001</span></span></td>
<td><span data-ttu-id="5898b-305">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-305">Electricity</span></span></td>
<td><span data-ttu-id="5898b-306">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-306">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="5898b-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-308">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="5898b-309">CC099</span><span class="sxs-lookup"><span data-stu-id="5898b-309">CC099</span></span></td>
<td><span data-ttu-id="5898b-310">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5898b-310">Default cost center</span></span></td>
<td><span data-ttu-id="5898b-311">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-311">10001</span></span></td>
<td><span data-ttu-id="5898b-312">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-312">Electricity</span></span></td>
<td><span data-ttu-id="5898b-313">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-313">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="5898b-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5898b-315">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="5898b-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5898b-316">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5898b-317">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="5898b-317">Cost element</span></span></th>
<th><span data-ttu-id="5898b-318">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5898b-318">Cost behavior</span></span></th>
<th><span data-ttu-id="5898b-319">Summa</span><span class="sxs-lookup"><span data-stu-id="5898b-319">Amount</span></span></th>
<th><span data-ttu-id="5898b-320">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="5898b-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-321">CC099</span><span class="sxs-lookup"><span data-stu-id="5898b-321">CC099</span></span></td>
<td><span data-ttu-id="5898b-322">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5898b-322">Default cost center</span></span></td>
<td><span data-ttu-id="5898b-323">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-323">10001</span></span></td>
<td><span data-ttu-id="5898b-324">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-324">Electricity</span></span></td>
<td><span data-ttu-id="5898b-325">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-325">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="5898b-326">-1,000.00</span></span></td>
<td><span data-ttu-id="5898b-327">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-328">CC001</span><span class="sxs-lookup"><span data-stu-id="5898b-328">CC001</span></span></td>
<td><span data-ttu-id="5898b-329">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5898b-329">HR</span></span></td>
<td><span data-ttu-id="5898b-330">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-330">10001</span></span></td>
<td><span data-ttu-id="5898b-331">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-331">Electricity</span></span></td>
<td><span data-ttu-id="5898b-332">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-332">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-333">500,00</span><span class="sxs-lookup"><span data-stu-id="5898b-333">500.00</span></span></td>
<td><span data-ttu-id="5898b-334">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-335">CC002</span><span class="sxs-lookup"><span data-stu-id="5898b-335">CC002</span></span></td>
<td><span data-ttu-id="5898b-336">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5898b-336">Finance</span></span></td>
<td><span data-ttu-id="5898b-337">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-337">10001</span></span></td>
<td><span data-ttu-id="5898b-338">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-338">Electricity</span></span></td>
<td><span data-ttu-id="5898b-339">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-339">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-340">500,00</span><span class="sxs-lookup"><span data-stu-id="5898b-340">500.00</span></span></td>
<td><span data-ttu-id="5898b-341">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-342">CC099</span><span class="sxs-lookup"><span data-stu-id="5898b-342">CC099</span></span></td>
<td><span data-ttu-id="5898b-343">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5898b-343">Default cost center</span></span></td>
<td><span data-ttu-id="5898b-344">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-344">10001</span></span></td>
<td><span data-ttu-id="5898b-345">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-345">Electricity</span></span></td>
<td><span data-ttu-id="5898b-346">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-346">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="5898b-347">-9,000.00</span></span></td>
<td><span data-ttu-id="5898b-348">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-349">CC001</span><span class="sxs-lookup"><span data-stu-id="5898b-349">CC001</span></span></td>
<td><span data-ttu-id="5898b-350">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5898b-350">HR</span></span></td>
<td><span data-ttu-id="5898b-351">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-351">10001</span></span></td>
<td><span data-ttu-id="5898b-352">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-352">Electricity</span></span></td>
<td><span data-ttu-id="5898b-353">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-353">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="5898b-354">1,285.71</span></span></td>
<td><span data-ttu-id="5898b-355">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-356">CC002</span><span class="sxs-lookup"><span data-stu-id="5898b-356">CC002</span></span></td>
<td><span data-ttu-id="5898b-357">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5898b-357">Finance</span></span></td>
<td><span data-ttu-id="5898b-358">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-358">10001</span></span></td>
<td><span data-ttu-id="5898b-359">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-359">Electricity</span></span></td>
<td><span data-ttu-id="5898b-360">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-360">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="5898b-361">7,714.29</span></span></td>
<td><span data-ttu-id="5898b-362">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5898b-363">Lisätietoja on kohdassa [Jakelukäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="5898b-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="5898b-364">Vaihe 3: Käsittele yleiskustannustason laskenta</span><span class="sxs-lookup"><span data-stu-id="5898b-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="5898b-365">Yleiskustannustasolla veloitetaan yksi tai useampi määrätty kustannusobjekti.</span><span class="sxs-lookup"><span data-stu-id="5898b-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="5898b-366">Veloitus perustuu ennalta määrättyyn kustannustasoon sekä määritetyn kohdistusperusteen suuruuteen.</span><span class="sxs-lookup"><span data-stu-id="5898b-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="5898b-367">Määritä yleiskustannustaso.</span><span class="sxs-lookup"><span data-stu-id="5898b-367">Define the overhead rate</span></span>

<span data-ttu-id="5898b-368">Kustannusobjekti CC001 HR vaikuttaa joukkoon sisäisiä projekteja.</span><span class="sxs-lookup"><span data-stu-id="5898b-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="5898b-369">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon projektit.</span><span class="sxs-lookup"><span data-stu-id="5898b-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5898b-370">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-370">Cost object</span></span></th>
<th><span data-ttu-id="5898b-371">Tunnit</span><span class="sxs-lookup"><span data-stu-id="5898b-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5898b-372">Proj 1</span></span></td>
<td><span data-ttu-id="5898b-373">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="5898b-373">Project 1</span></span></td>
<td><span data-ttu-id="5898b-374">3</span><span class="sxs-lookup"><span data-stu-id="5898b-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5898b-375">Proj 2</span></span></td>
<td><span data-ttu-id="5898b-376">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="5898b-376">Project 2</span></span></td>
<td><span data-ttu-id="5898b-377">1</span><span class="sxs-lookup"><span data-stu-id="5898b-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5898b-378">Kustannusprojektien osuudelle on määritetty ennalta kustannushinta.</span><span class="sxs-lookup"><span data-stu-id="5898b-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5898b-379">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-379">Cost object</span></span></th>
<th><span data-ttu-id="5898b-380">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="5898b-380">Cost element</span></span></th>
<th><span data-ttu-id="5898b-381">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5898b-381">Cost behavior</span></span></th>
<th><span data-ttu-id="5898b-382">Yksiköt</span><span class="sxs-lookup"><span data-stu-id="5898b-382">Units</span></span></th>
<th><span data-ttu-id="5898b-383">Osuus</span><span class="sxs-lookup"><span data-stu-id="5898b-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-384">CC001</span><span class="sxs-lookup"><span data-stu-id="5898b-384">CC001</span></span></td>
<td><span data-ttu-id="5898b-385">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5898b-385">HR</span></span></td>
<td><span data-ttu-id="5898b-386">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-386">10001</span></span></td>
<td><span data-ttu-id="5898b-387">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-387">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-388">1</span><span class="sxs-lookup"><span data-stu-id="5898b-388">1</span></span></td>
<td><span data-ttu-id="5898b-389">10</span><span class="sxs-lookup"><span data-stu-id="5898b-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5898b-390">Seuraavassa taulukossa on esitetty tulos, kun Henkilöstöhallinnon projekteja käytetään kohdistusperusteena.</span><span class="sxs-lookup"><span data-stu-id="5898b-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5898b-391">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-391">Cost object</span></span></th>
<th><span data-ttu-id="5898b-392">Suuruus</span><span class="sxs-lookup"><span data-stu-id="5898b-392">Magnitude</span></span></th>
<th><span data-ttu-id="5898b-393">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="5898b-393">Cost element</span></span></th>
<th><span data-ttu-id="5898b-394">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="5898b-394">Allocation factor</span></span></th>
<th><span data-ttu-id="5898b-395">Summa</span><span class="sxs-lookup"><span data-stu-id="5898b-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5898b-396">Proj 1</span></span></td>
<td><span data-ttu-id="5898b-397">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="5898b-397">Project 1</span></span></td>
<td><span data-ttu-id="5898b-398">3</span><span class="sxs-lookup"><span data-stu-id="5898b-398">3</span></span></td>
<td><span data-ttu-id="5898b-399">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-399">10001</span></span></td>
<td><span data-ttu-id="5898b-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="5898b-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="5898b-401">30,00</span><span class="sxs-lookup"><span data-stu-id="5898b-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5898b-402">Proj 2</span></span></td>
<td><span data-ttu-id="5898b-403">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="5898b-403">Project 2</span></span></td>
<td><span data-ttu-id="5898b-404">1</span><span class="sxs-lookup"><span data-stu-id="5898b-404">1</span></span></td>
<td><span data-ttu-id="5898b-405">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-405">10001</span></span></td>
<td><span data-ttu-id="5898b-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="5898b-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="5898b-407">10,00</span><span class="sxs-lookup"><span data-stu-id="5898b-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="5898b-408">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5898b-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5898b-409">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5898b-409">Journal</span></span></th>
<th><span data-ttu-id="5898b-410">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="5898b-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5898b-411">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="5898b-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5898b-412">Versio</span><span class="sxs-lookup"><span data-stu-id="5898b-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-413">00003</span><span class="sxs-lookup"><span data-stu-id="5898b-413">00003</span></span></td>
<td><span data-ttu-id="5898b-414">Yleiskustannustason laskelman kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5898b-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="5898b-415">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="5898b-415">Fiscal</span></span></td>
<td><span data-ttu-id="5898b-416">2017</span><span class="sxs-lookup"><span data-stu-id="5898b-416">2017</span></span></td>
<td><span data-ttu-id="5898b-417">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="5898b-417">Period 1</span></span></td>
<td><span data-ttu-id="5898b-418">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="5898b-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="5898b-419">Kirjauskansioviennit (Yleiskustannustason laskennan kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="5898b-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5898b-420">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="5898b-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5898b-421">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-421">Cost object</span></span></th>
<th><span data-ttu-id="5898b-422">Suuruus</span><span class="sxs-lookup"><span data-stu-id="5898b-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-423">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="5898b-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5898b-424">Proj 1</span></span></td>
<td><span data-ttu-id="5898b-425">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="5898b-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="5898b-426">3,00</span><span class="sxs-lookup"><span data-stu-id="5898b-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-427">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="5898b-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5898b-428">Proj 2</span></span></td>
<td><span data-ttu-id="5898b-429">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="5898b-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="5898b-430">1,00</span><span class="sxs-lookup"><span data-stu-id="5898b-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5898b-431">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="5898b-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5898b-432">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5898b-433">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="5898b-433">Cost element</span></span></th>
<th><span data-ttu-id="5898b-434">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5898b-434">Cost behavior</span></span></th>
<th><span data-ttu-id="5898b-435">Summa</span><span class="sxs-lookup"><span data-stu-id="5898b-435">Amount</span></span></th>
<th><span data-ttu-id="5898b-436">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="5898b-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="5898b-437">CC0001</span></span></td>
<td><span data-ttu-id="5898b-438">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5898b-438">HR</span></span></td>
<td><span data-ttu-id="5898b-439">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-439">10001</span></span></td>
<td><span data-ttu-id="5898b-440">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-440">Electricity</span></span></td>
<td><span data-ttu-id="5898b-441">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-441">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="5898b-442">-30.00</span></span></td>
<td><span data-ttu-id="5898b-443">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5898b-444">Proj 1</span></span></td>
<td><span data-ttu-id="5898b-445">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="5898b-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="5898b-446">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-446">10001</span></span></td>
<td><span data-ttu-id="5898b-447">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-447">Electricity</span></span></td>
<td><span data-ttu-id="5898b-448">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-448">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-449">30,00</span><span class="sxs-lookup"><span data-stu-id="5898b-449">30.00</span></span></td>
<td><span data-ttu-id="5898b-450">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-451">CC001</span><span class="sxs-lookup"><span data-stu-id="5898b-451">CC001</span></span></td>
<td><span data-ttu-id="5898b-452">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5898b-452">HR</span></span></td>
<td><span data-ttu-id="5898b-453">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-453">10001</span></span></td>
<td><span data-ttu-id="5898b-454">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-454">Electricity</span></span></td>
<td><span data-ttu-id="5898b-455">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-455">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="5898b-456">-10.00</span></span></td>
<td><span data-ttu-id="5898b-457">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5898b-458">Proj 2</span></span></td>
<td><span data-ttu-id="5898b-459">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="5898b-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="5898b-460">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-460">10001</span></span></td>
<td><span data-ttu-id="5898b-461">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-461">Electricity</span></span></td>
<td><span data-ttu-id="5898b-462">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-462">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-463">10.00</span><span class="sxs-lookup"><span data-stu-id="5898b-463">10.00</span></span></td>
<td><span data-ttu-id="5898b-464">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5898b-465">Lisätietoja on kohdassa [Yleisen laskennan suorittaminen](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="5898b-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="5898b-466">Vaihe 4: Käsittele kustannusten kohdistuksen laskenta</span><span class="sxs-lookup"><span data-stu-id="5898b-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="5898b-467">Kohdistuksella kustannusobjektin saldo liitetään toisiin kustannusobjekteihin käyttämällä kohdistusperustetta.</span><span class="sxs-lookup"><span data-stu-id="5898b-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="5898b-468">Finance tukee vastavuoroista kohdistusmenetelmää.</span><span class="sxs-lookup"><span data-stu-id="5898b-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="5898b-469">Vastavuoroisessa kohdistusmenetelmässä tunnistetaan oheiskustannusobjektien käyttämät, keskinäiset palvelut täysin.</span><span class="sxs-lookup"><span data-stu-id="5898b-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="5898b-470">Järjestelmä määrittää oikean kohdistusjärjestyksen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="5898b-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="5898b-471">Kustannusobjektin saldo kohdistetaan yhdellä kohdistusperusteella.</span><span class="sxs-lookup"><span data-stu-id="5898b-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="5898b-472">Kustannusobjektien dimensiot ja niiden vastaavat jäsenet ylittävät kohdistukset ovat tuettuja.</span><span class="sxs-lookup"><span data-stu-id="5898b-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="5898b-473">Kustannusseurantayksikkö hallitsee kohdistusjärjestystä.</span><span class="sxs-lookup"><span data-stu-id="5898b-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="5898b-474">[![Vastavuoroinen menetelmä](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="5898b-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="5898b-475">Määritä kustannuksen kohdistus</span><span class="sxs-lookup"><span data-stu-id="5898b-475">Define the cost allocation</span></span>

<span data-ttu-id="5898b-476">Tämä on yksinkertainen esimerkki, jossa kerrotaan, miten voit jäljittää kustannuksen virran.</span><span class="sxs-lookup"><span data-stu-id="5898b-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="5898b-477">Kustannusobjekti CC001 HR liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="5898b-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="5898b-478">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="5898b-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5898b-479">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-479">Cost object</span></span></th>
<th><span data-ttu-id="5898b-480">HR-palvelut</span><span class="sxs-lookup"><span data-stu-id="5898b-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-481">CC002</span><span class="sxs-lookup"><span data-stu-id="5898b-481">CC002</span></span></td>
<td><span data-ttu-id="5898b-482">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5898b-482">Finance</span></span></td>
<td><span data-ttu-id="5898b-483">35</span><span class="sxs-lookup"><span data-stu-id="5898b-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-484">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-484">CC003</span></span></td>
<td><span data-ttu-id="5898b-485">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5898b-485">Assembly</span></span></td>
<td><span data-ttu-id="5898b-486">55</span><span class="sxs-lookup"><span data-stu-id="5898b-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-487">CC004</span><span class="sxs-lookup"><span data-stu-id="5898b-487">CC004</span></span></td>
<td><span data-ttu-id="5898b-488">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5898b-488">Packaging</span></span></td>
<td><span data-ttu-id="5898b-489">10</span><span class="sxs-lookup"><span data-stu-id="5898b-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5898b-490">Kustannusobjekti CC002 Taloushallinto liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="5898b-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="5898b-491">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Taloushallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="5898b-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5898b-492">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-492">Cost object</span></span></th>
<th><span data-ttu-id="5898b-493">Taloushallinnon palvelut</span><span class="sxs-lookup"><span data-stu-id="5898b-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-494">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-494">CC003</span></span></td>
<td><span data-ttu-id="5898b-495">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5898b-495">Assembly</span></span></td>
<td><span data-ttu-id="5898b-496">65</span><span class="sxs-lookup"><span data-stu-id="5898b-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-497">CC004</span><span class="sxs-lookup"><span data-stu-id="5898b-497">CC004</span></span></td>
<td><span data-ttu-id="5898b-498">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5898b-498">Packaging</span></span></td>
<td><span data-ttu-id="5898b-499">35</span><span class="sxs-lookup"><span data-stu-id="5898b-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5898b-500">Kustannusobjekti CC003 Kokoonpano liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="5898b-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="5898b-501">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Kokoonpanopalvelut.</span><span class="sxs-lookup"><span data-stu-id="5898b-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5898b-502">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-502">Cost object</span></span></th>
<th><span data-ttu-id="5898b-503">Kokoonpanopalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="5898b-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-504">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-504">Prod 1</span></span></td>
<td><span data-ttu-id="5898b-505">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-505">Product 1</span></span></td>
<td><span data-ttu-id="5898b-506">60</span><span class="sxs-lookup"><span data-stu-id="5898b-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-507">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-507">Prod 2</span></span></td>
<td><span data-ttu-id="5898b-508">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-508">Product 2</span></span></td>
<td><span data-ttu-id="5898b-509">20</span><span class="sxs-lookup"><span data-stu-id="5898b-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5898b-510">Kustannusobjekti CC004 Pakkaus liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="5898b-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="5898b-511">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Pakkauspalvelut.</span><span class="sxs-lookup"><span data-stu-id="5898b-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5898b-512">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-512">Cost object</span></span></th>
<th><span data-ttu-id="5898b-513">Pakkauspalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="5898b-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-514">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-514">Prod 1</span></span></td>
<td><span data-ttu-id="5898b-515">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-515">Product 1</span></span></td>
<td><span data-ttu-id="5898b-516">80</span><span class="sxs-lookup"><span data-stu-id="5898b-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-517">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-517">Prod 2</span></span></td>
<td><span data-ttu-id="5898b-518">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-518">Product 2</span></span></td>
<td><span data-ttu-id="5898b-519">15</span><span class="sxs-lookup"><span data-stu-id="5898b-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5898b-520">Tilastomittaukset, kuten tämän tuotteen kuluttamat tuotantotunnit, voidaan johtaa lähdetiedoista.</span><span class="sxs-lookup"><span data-stu-id="5898b-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="5898b-521">Lisätietoja on kohdassa [Tilastomittauksen lähdemalli](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="5898b-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="5898b-522">Seuraavassa taulukossa näytetään tulos, kun henkilöstöhallinnon palveluja käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="5898b-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5898b-523">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-523">Cost object</span></span></th>
<th><span data-ttu-id="5898b-524">Suuruus</span><span class="sxs-lookup"><span data-stu-id="5898b-524">Magnitude</span></span></th>
<th><span data-ttu-id="5898b-525">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="5898b-525">Allocation factor</span></span></th>
<th><span data-ttu-id="5898b-526">Summa</span><span class="sxs-lookup"><span data-stu-id="5898b-526">Amount</span></span></th>
<th><span data-ttu-id="5898b-527">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5898b-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-528">CC002</span><span class="sxs-lookup"><span data-stu-id="5898b-528">CC002</span></span></td>
<td><span data-ttu-id="5898b-529">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5898b-529">Finance</span></span></td>
<td><span data-ttu-id="5898b-530">35</span><span class="sxs-lookup"><span data-stu-id="5898b-530">35</span></span></td>
<td><span data-ttu-id="5898b-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="5898b-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5898b-532">175.00</span><span class="sxs-lookup"><span data-stu-id="5898b-532">175.00</span></span></td>
<td><span data-ttu-id="5898b-533">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-534">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-534">CC003</span></span></td>
<td><span data-ttu-id="5898b-535">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5898b-535">Assembly</span></span></td>
<td><span data-ttu-id="5898b-536">55</span><span class="sxs-lookup"><span data-stu-id="5898b-536">55</span></span></td>
<td><span data-ttu-id="5898b-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="5898b-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5898b-538">275.00</span><span class="sxs-lookup"><span data-stu-id="5898b-538">275.00</span></span></td>
<td><span data-ttu-id="5898b-539">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-540">CC004</span><span class="sxs-lookup"><span data-stu-id="5898b-540">CC004</span></span></td>
<td><span data-ttu-id="5898b-541">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5898b-541">Packaging</span></span></td>
<td><span data-ttu-id="5898b-542">10</span><span class="sxs-lookup"><span data-stu-id="5898b-542">10</span></span></td>
<td><span data-ttu-id="5898b-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="5898b-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5898b-544">50,00</span><span class="sxs-lookup"><span data-stu-id="5898b-544">50.00</span></span></td>
<td><span data-ttu-id="5898b-545">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-546">CC002</span><span class="sxs-lookup"><span data-stu-id="5898b-546">CC002</span></span></td>
<td><span data-ttu-id="5898b-547">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5898b-547">Finance</span></span></td>
<td><span data-ttu-id="5898b-548">35</span><span class="sxs-lookup"><span data-stu-id="5898b-548">35</span></span></td>
<td><span data-ttu-id="5898b-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="5898b-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5898b-550">436.00</span><span class="sxs-lookup"><span data-stu-id="5898b-550">436.00</span></span></td>
<td><span data-ttu-id="5898b-551">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-552">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-552">CC003</span></span></td>
<td><span data-ttu-id="5898b-553">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5898b-553">Assembly</span></span></td>
<td><span data-ttu-id="5898b-554">55</span><span class="sxs-lookup"><span data-stu-id="5898b-554">55</span></span></td>
<td><span data-ttu-id="5898b-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="5898b-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5898b-556">685.14</span><span class="sxs-lookup"><span data-stu-id="5898b-556">685.14</span></span></td>
<td><span data-ttu-id="5898b-557">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-558">CC004</span><span class="sxs-lookup"><span data-stu-id="5898b-558">CC004</span></span></td>
<td><span data-ttu-id="5898b-559">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5898b-559">Packaging</span></span></td>
<td><span data-ttu-id="5898b-560">10</span><span class="sxs-lookup"><span data-stu-id="5898b-560">10</span></span></td>
<td><span data-ttu-id="5898b-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="5898b-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5898b-562">124.57</span><span class="sxs-lookup"><span data-stu-id="5898b-562">124.57</span></span></td>
<td><span data-ttu-id="5898b-563">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5898b-564">Seuraavassa taulukossa näytetään tulos, kun Taloushallinnon palveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="5898b-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5898b-565">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-565">Cost object</span></span></th>
<th><span data-ttu-id="5898b-566">Suuruus</span><span class="sxs-lookup"><span data-stu-id="5898b-566">Magnitude</span></span></th>
<th><span data-ttu-id="5898b-567">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="5898b-567">Allocation factor</span></span></th>
<th><span data-ttu-id="5898b-568">Summa</span><span class="sxs-lookup"><span data-stu-id="5898b-568">Amount</span></span></th>
<th><span data-ttu-id="5898b-569">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5898b-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-570">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-570">CC003</span></span></td>
<td><span data-ttu-id="5898b-571">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5898b-571">Assembly</span></span></td>
<td><span data-ttu-id="5898b-572">65</span><span class="sxs-lookup"><span data-stu-id="5898b-572">65</span></span></td>
<td><span data-ttu-id="5898b-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="5898b-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="5898b-574">438.75</span><span class="sxs-lookup"><span data-stu-id="5898b-574">438.75</span></span></td>
<td><span data-ttu-id="5898b-575">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-576">CC004</span><span class="sxs-lookup"><span data-stu-id="5898b-576">CC004</span></span></td>
<td><span data-ttu-id="5898b-577">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5898b-577">Packaging</span></span></td>
<td><span data-ttu-id="5898b-578">35</span><span class="sxs-lookup"><span data-stu-id="5898b-578">35</span></span></td>
<td><span data-ttu-id="5898b-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="5898b-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="5898b-580">236.25</span><span class="sxs-lookup"><span data-stu-id="5898b-580">236.25</span></span></td>
<td><span data-ttu-id="5898b-581">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-582">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-582">CC003</span></span></td>
<td><span data-ttu-id="5898b-583">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5898b-583">Assembly</span></span></td>
<td><span data-ttu-id="5898b-584">65</span><span class="sxs-lookup"><span data-stu-id="5898b-584">65</span></span></td>
<td><span data-ttu-id="5898b-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="5898b-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="5898b-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="5898b-586">5,297.69</span></span></td>
<td><span data-ttu-id="5898b-587">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-588">CC004</span><span class="sxs-lookup"><span data-stu-id="5898b-588">CC004</span></span></td>
<td><span data-ttu-id="5898b-589">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5898b-589">Packaging</span></span></td>
<td><span data-ttu-id="5898b-590">35</span><span class="sxs-lookup"><span data-stu-id="5898b-590">35</span></span></td>
<td><span data-ttu-id="5898b-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="5898b-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="5898b-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="5898b-592">2,852.60</span></span></td>
<td><span data-ttu-id="5898b-593">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5898b-594">Seuraavassa taulukossa näytetään tulos, kun Kokoonpanopalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="5898b-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5898b-595">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-595">Cost object</span></span></th>
<th><span data-ttu-id="5898b-596">Suuruus</span><span class="sxs-lookup"><span data-stu-id="5898b-596">Magnitude</span></span></th>
<th><span data-ttu-id="5898b-597">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="5898b-597">Allocation factor</span></span></th>
<th><span data-ttu-id="5898b-598">Summa</span><span class="sxs-lookup"><span data-stu-id="5898b-598">Amount</span></span></th>
<th><span data-ttu-id="5898b-599">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5898b-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-600">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-600">Prod 1</span></span></td>
<td><span data-ttu-id="5898b-601">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-601">Product 1</span></span></td>
<td><span data-ttu-id="5898b-602">60</span><span class="sxs-lookup"><span data-stu-id="5898b-602">60</span></span></td>
<td><span data-ttu-id="5898b-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="5898b-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="5898b-604">535.31</span><span class="sxs-lookup"><span data-stu-id="5898b-604">535.31</span></span></td>
<td><span data-ttu-id="5898b-605">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-606">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-606">Prod 2</span></span></td>
<td><span data-ttu-id="5898b-607">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-607">Product 2</span></span></td>
<td><span data-ttu-id="5898b-608">20</span><span class="sxs-lookup"><span data-stu-id="5898b-608">20</span></span></td>
<td><span data-ttu-id="5898b-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="5898b-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="5898b-610">178.44</span><span class="sxs-lookup"><span data-stu-id="5898b-610">178.44</span></span></td>
<td><span data-ttu-id="5898b-611">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-612">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-612">Prod 1</span></span></td>
<td><span data-ttu-id="5898b-613">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-613">Product 1</span></span></td>
<td><span data-ttu-id="5898b-614">60</span><span class="sxs-lookup"><span data-stu-id="5898b-614">60</span></span></td>
<td><span data-ttu-id="5898b-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="5898b-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="5898b-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="5898b-616">4,487.12</span></span></td>
<td><span data-ttu-id="5898b-617">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-618">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-618">Prod 2</span></span></td>
<td><span data-ttu-id="5898b-619">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-619">Product 2</span></span></td>
<td><span data-ttu-id="5898b-620">20</span><span class="sxs-lookup"><span data-stu-id="5898b-620">20</span></span></td>
<td><span data-ttu-id="5898b-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="5898b-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="5898b-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="5898b-622">1,495.71</span></span></td>
<td><span data-ttu-id="5898b-623">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5898b-624">Seuraavassa taulukossa näytetään tulos, kun Pakkauspalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="5898b-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5898b-625">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-625">Cost object</span></span></th>
<th><span data-ttu-id="5898b-626">Suuruus</span><span class="sxs-lookup"><span data-stu-id="5898b-626">Magnitude</span></span></th>
<th><span data-ttu-id="5898b-627">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="5898b-627">Allocation factor</span></span></th>
<th><span data-ttu-id="5898b-628">Summa</span><span class="sxs-lookup"><span data-stu-id="5898b-628">Amount</span></span></th>
<th><span data-ttu-id="5898b-629">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5898b-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-630">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-630">Prod 1</span></span></td>
<td><span data-ttu-id="5898b-631">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-631">Product 1</span></span></td>
<td><span data-ttu-id="5898b-632">80</span><span class="sxs-lookup"><span data-stu-id="5898b-632">80</span></span></td>
<td><span data-ttu-id="5898b-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="5898b-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="5898b-634">241.05</span><span class="sxs-lookup"><span data-stu-id="5898b-634">241.05</span></span></td>
<td><span data-ttu-id="5898b-635">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-636">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-636">Prod 2</span></span></td>
<td><span data-ttu-id="5898b-637">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-637">Product 2</span></span></td>
<td><span data-ttu-id="5898b-638">15</span><span class="sxs-lookup"><span data-stu-id="5898b-638">15</span></span></td>
<td><span data-ttu-id="5898b-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="5898b-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="5898b-640">45.20</span><span class="sxs-lookup"><span data-stu-id="5898b-640">45.20</span></span></td>
<td><span data-ttu-id="5898b-641">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-642">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-642">Prod 1</span></span></td>
<td><span data-ttu-id="5898b-643">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-643">Product 1</span></span></td>
<td><span data-ttu-id="5898b-644">80</span><span class="sxs-lookup"><span data-stu-id="5898b-644">80</span></span></td>
<td><span data-ttu-id="5898b-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="5898b-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="5898b-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="5898b-646">2,507.09</span></span></td>
<td><span data-ttu-id="5898b-647">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-648">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-648">Prod 2</span></span></td>
<td><span data-ttu-id="5898b-649">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-649">Product 2</span></span></td>
<td><span data-ttu-id="5898b-650">15</span><span class="sxs-lookup"><span data-stu-id="5898b-650">15</span></span></td>
<td><span data-ttu-id="5898b-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="5898b-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="5898b-652">470.08</span><span class="sxs-lookup"><span data-stu-id="5898b-652">470.08</span></span></td>
<td><span data-ttu-id="5898b-653">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5898b-654">Kirjauskansioviennit (kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="5898b-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5898b-655">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5898b-655">Journal</span></span></th>
<th><span data-ttu-id="5898b-656">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="5898b-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5898b-657">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="5898b-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5898b-658">Versio</span><span class="sxs-lookup"><span data-stu-id="5898b-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-659">00004</span><span class="sxs-lookup"><span data-stu-id="5898b-659">00004</span></span></td>
<td><span data-ttu-id="5898b-660">Kustannusten kohdistuskirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5898b-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="5898b-661">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="5898b-661">Fiscal</span></span></td>
<td><span data-ttu-id="5898b-662">2017</span><span class="sxs-lookup"><span data-stu-id="5898b-662">2017</span></span></td>
<td><span data-ttu-id="5898b-663">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="5898b-663">Period 1</span></span></td>
<td><span data-ttu-id="5898b-664">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="5898b-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="5898b-665">Kirjauskansion rivit</span><span class="sxs-lookup"><span data-stu-id="5898b-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5898b-666">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="5898b-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5898b-667">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5898b-668">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="5898b-668">Cost element</span></span></th>
<th><span data-ttu-id="5898b-669">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5898b-669">Cost behavior</span></span></th>
<th><span data-ttu-id="5898b-670">Summa</span><span class="sxs-lookup"><span data-stu-id="5898b-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-671">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="5898b-672">CC001</span><span class="sxs-lookup"><span data-stu-id="5898b-672">CC001</span></span></td>
<td><span data-ttu-id="5898b-673">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5898b-673">HR</span></span></td>
<td><span data-ttu-id="5898b-674">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-674">10001</span></span></td>
<td><span data-ttu-id="5898b-675">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-675">Electricity</span></span></td>
<td><span data-ttu-id="5898b-676">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-676">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-677">500,00</span><span class="sxs-lookup"><span data-stu-id="5898b-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-678">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="5898b-679">CC001</span><span class="sxs-lookup"><span data-stu-id="5898b-679">CC001</span></span></td>
<td><span data-ttu-id="5898b-680">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5898b-680">HR</span></span></td>
<td><span data-ttu-id="5898b-681">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-681">10001</span></span></td>
<td><span data-ttu-id="5898b-682">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-682">Electricity</span></span></td>
<td><span data-ttu-id="5898b-683">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-683">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="5898b-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-685">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="5898b-686">CC002</span><span class="sxs-lookup"><span data-stu-id="5898b-686">CC002</span></span></td>
<td><span data-ttu-id="5898b-687">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5898b-687">Finance</span></span></td>
<td><span data-ttu-id="5898b-688">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-688">10001</span></span></td>
<td><span data-ttu-id="5898b-689">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-689">Electricity</span></span></td>
<td><span data-ttu-id="5898b-690">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-690">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-691">675.00</span><span class="sxs-lookup"><span data-stu-id="5898b-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-692">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="5898b-693">CC002</span><span class="sxs-lookup"><span data-stu-id="5898b-693">CC002</span></span></td>
<td><span data-ttu-id="5898b-694">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5898b-694">Finance</span></span></td>
<td><span data-ttu-id="5898b-695">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-695">10001</span></span></td>
<td><span data-ttu-id="5898b-696">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-696">Electricity</span></span></td>
<td><span data-ttu-id="5898b-697">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-697">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="5898b-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-699">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="5898b-700">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-700">CC003</span></span></td>
<td><span data-ttu-id="5898b-701">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5898b-701">Assembly</span></span></td>
<td><span data-ttu-id="5898b-702">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-702">10001</span></span></td>
<td><span data-ttu-id="5898b-703">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-703">Electricity</span></span></td>
<td><span data-ttu-id="5898b-704">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-704">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-705">713.75</span><span class="sxs-lookup"><span data-stu-id="5898b-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-706">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="5898b-707">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-707">CC003</span></span></td>
<td><span data-ttu-id="5898b-708">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5898b-708">Assembly</span></span></td>
<td><span data-ttu-id="5898b-709">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-709">10001</span></span></td>
<td><span data-ttu-id="5898b-710">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-710">Electricity</span></span></td>
<td><span data-ttu-id="5898b-711">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-711">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="5898b-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-713">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="5898b-714">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-714">CC003</span></span></td>
<td><span data-ttu-id="5898b-715">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5898b-715">Packaging</span></span></td>
<td><span data-ttu-id="5898b-716">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-716">10001</span></span></td>
<td><span data-ttu-id="5898b-717">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-717">Electricity</span></span></td>
<td><span data-ttu-id="5898b-718">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-718">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-719">286.25</span><span class="sxs-lookup"><span data-stu-id="5898b-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-720">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="5898b-721">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-721">CC003</span></span></td>
<td><span data-ttu-id="5898b-722">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5898b-722">Packaging</span></span></td>
<td><span data-ttu-id="5898b-723">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-723">10001</span></span></td>
<td><span data-ttu-id="5898b-724">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-724">Electricity</span></span></td>
<td><span data-ttu-id="5898b-725">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-725">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="5898b-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-727">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="5898b-728">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-728">Prod 1</span></span></td>
<td><span data-ttu-id="5898b-729">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-729">Product 1</span></span></td>
<td><span data-ttu-id="5898b-730">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-730">10001</span></span></td>
<td><span data-ttu-id="5898b-731">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-731">Electricity</span></span></td>
<td><span data-ttu-id="5898b-732">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-732">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-733">776.36</span><span class="sxs-lookup"><span data-stu-id="5898b-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-734">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="5898b-735">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-735">Prod 1</span></span></td>
<td><span data-ttu-id="5898b-736">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-736">Product 1</span></span></td>
<td><span data-ttu-id="5898b-737">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-737">10001</span></span></td>
<td><span data-ttu-id="5898b-738">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-738">Electricity</span></span></td>
<td><span data-ttu-id="5898b-739">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-739">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="5898b-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-741">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="5898b-742">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-742">Prod 2</span></span></td>
<td><span data-ttu-id="5898b-743">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-743">Product 1</span></span></td>
<td><span data-ttu-id="5898b-744">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-744">10001</span></span></td>
<td><span data-ttu-id="5898b-745">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-745">Electricity</span></span></td>
<td><span data-ttu-id="5898b-746">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-746">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-747">223.64</span><span class="sxs-lookup"><span data-stu-id="5898b-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-748">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="5898b-749">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-749">Prod 2</span></span></td>
<td><span data-ttu-id="5898b-750">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-750">Product 1</span></span></td>
<td><span data-ttu-id="5898b-751">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-751">10001</span></span></td>
<td><span data-ttu-id="5898b-752">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-752">Electricity</span></span></td>
<td><span data-ttu-id="5898b-753">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-753">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="5898b-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5898b-755">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="5898b-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5898b-756">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5898b-757">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="5898b-757">Cost element</span></span></th>
<th><span data-ttu-id="5898b-758">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5898b-758">Cost behavior</span></span></th>
<th><span data-ttu-id="5898b-759">Summa</span><span class="sxs-lookup"><span data-stu-id="5898b-759">Amount</span></span></th>
<th><span data-ttu-id="5898b-760">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="5898b-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5898b-761">CC001</span><span class="sxs-lookup"><span data-stu-id="5898b-761">CC001</span></span></td>
<td><span data-ttu-id="5898b-762">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5898b-762">HR</span></span></td>
<td><span data-ttu-id="5898b-763">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-763">10001</span></span></td>
<td><span data-ttu-id="5898b-764">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-764">Electricity</span></span></td>
<td><span data-ttu-id="5898b-765">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-765">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="5898b-766">-500.00</span></span></td>
<td><span data-ttu-id="5898b-767">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-768">CC002</span><span class="sxs-lookup"><span data-stu-id="5898b-768">CC002</span></span></td>
<td><span data-ttu-id="5898b-769">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5898b-769">Finance</span></span></td>
<td><span data-ttu-id="5898b-770">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-770">10001</span></span></td>
<td><span data-ttu-id="5898b-771">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-771">Electricity</span></span></td>
<td><span data-ttu-id="5898b-772">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-772">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-773">175.00</span><span class="sxs-lookup"><span data-stu-id="5898b-773">175.00</span></span></td>
<td><span data-ttu-id="5898b-774">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-775">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-775">CC003</span></span></td>
<td><span data-ttu-id="5898b-776">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5898b-776">Assembly</span></span></td>
<td><span data-ttu-id="5898b-777">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-777">10001</span></span></td>
<td><span data-ttu-id="5898b-778">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-778">Electricity</span></span></td>
<td><span data-ttu-id="5898b-779">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-779">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-780">275.00</span><span class="sxs-lookup"><span data-stu-id="5898b-780">275.00</span></span></td>
<td><span data-ttu-id="5898b-781">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-782">CC004</span><span class="sxs-lookup"><span data-stu-id="5898b-782">CC004</span></span></td>
<td><span data-ttu-id="5898b-783">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5898b-783">Packaging</span></span></td>
<td><span data-ttu-id="5898b-784">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-784">10001</span></span></td>
<td><span data-ttu-id="5898b-785">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-785">Electricity</span></span></td>
<td><span data-ttu-id="5898b-786">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-786">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-787">50,00</span><span class="sxs-lookup"><span data-stu-id="5898b-787">50,00</span></span></td>
<td><span data-ttu-id="5898b-788">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-789">CC001</span><span class="sxs-lookup"><span data-stu-id="5898b-789">CC001</span></span></td>
<td><span data-ttu-id="5898b-790">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5898b-790">HR</span></span></td>
<td><span data-ttu-id="5898b-791">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-791">10001</span></span></td>
<td><span data-ttu-id="5898b-792">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-792">Electricity</span></span></td>
<td><span data-ttu-id="5898b-793">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-793">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="5898b-794">-1,245.71</span></span></td>
<td><span data-ttu-id="5898b-795">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-796">CC002</span><span class="sxs-lookup"><span data-stu-id="5898b-796">CC002</span></span></td>
<td><span data-ttu-id="5898b-797">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5898b-797">Finance</span></span></td>
<td><span data-ttu-id="5898b-798">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-798">10001</span></span></td>
<td><span data-ttu-id="5898b-799">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-799">Electricity</span></span></td>
<td><span data-ttu-id="5898b-800">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-800">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-801">436.00</span><span class="sxs-lookup"><span data-stu-id="5898b-801">436.00</span></span></td>
<td><span data-ttu-id="5898b-802">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-803">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-803">CC003</span></span></td>
<td><span data-ttu-id="5898b-804">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5898b-804">Assembly</span></span></td>
<td><span data-ttu-id="5898b-805">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-805">10001</span></span></td>
<td><span data-ttu-id="5898b-806">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-806">Electricity</span></span></td>
<td><span data-ttu-id="5898b-807">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-807">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-808">685.14</span><span class="sxs-lookup"><span data-stu-id="5898b-808">685.14</span></span></td>
<td><span data-ttu-id="5898b-809">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-810">CC004</span><span class="sxs-lookup"><span data-stu-id="5898b-810">CC004</span></span></td>
<td><span data-ttu-id="5898b-811">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5898b-811">Packaging</span></span></td>
<td><span data-ttu-id="5898b-812">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-812">10001</span></span></td>
<td><span data-ttu-id="5898b-813">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-813">Electricity</span></span></td>
<td><span data-ttu-id="5898b-814">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-814">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-815">124.57</span><span class="sxs-lookup"><span data-stu-id="5898b-815">124.57</span></span></td>
<td><span data-ttu-id="5898b-816">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-817">CC002</span><span class="sxs-lookup"><span data-stu-id="5898b-817">CC002</span></span></td>
<td><span data-ttu-id="5898b-818">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5898b-818">Finance</span></span></td>
<td><span data-ttu-id="5898b-819">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-819">10001</span></span></td>
<td><span data-ttu-id="5898b-820">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-820">Electricity</span></span></td>
<td><span data-ttu-id="5898b-821">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-821">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="5898b-822">-675.00</span></span></td>
<td><span data-ttu-id="5898b-823">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-824">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-824">CC003</span></span></td>
<td><span data-ttu-id="5898b-825">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5898b-825">Assembly</span></span></td>
<td><span data-ttu-id="5898b-826">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-826">10001</span></span></td>
<td><span data-ttu-id="5898b-827">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-827">Electricity</span></span></td>
<td><span data-ttu-id="5898b-828">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-828">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-829">438.75</span><span class="sxs-lookup"><span data-stu-id="5898b-829">438.75</span></span></td>
<td><span data-ttu-id="5898b-830">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-831">CC004</span><span class="sxs-lookup"><span data-stu-id="5898b-831">CC004</span></span></td>
<td><span data-ttu-id="5898b-832">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5898b-832">Packaging</span></span></td>
<td><span data-ttu-id="5898b-833">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-833">10001</span></span></td>
<td><span data-ttu-id="5898b-834">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-834">Electricity</span></span></td>
<td><span data-ttu-id="5898b-835">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-835">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-836">236.25</span><span class="sxs-lookup"><span data-stu-id="5898b-836">236.25</span></span></td>
<td><span data-ttu-id="5898b-837">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-838">CC002</span><span class="sxs-lookup"><span data-stu-id="5898b-838">CC002</span></span></td>
<td><span data-ttu-id="5898b-839">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5898b-839">Finance</span></span></td>
<td><span data-ttu-id="5898b-840">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-840">10001</span></span></td>
<td><span data-ttu-id="5898b-841">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-841">Electricity</span></span></td>
<td><span data-ttu-id="5898b-842">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-842">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="5898b-843">-8,150.29</span></span></td>
<td><span data-ttu-id="5898b-844">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-845">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-845">CC003</span></span></td>
<td><span data-ttu-id="5898b-846">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5898b-846">Assembly</span></span></td>
<td><span data-ttu-id="5898b-847">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-847">10001</span></span></td>
<td><span data-ttu-id="5898b-848">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-848">Electricity</span></span></td>
<td><span data-ttu-id="5898b-849">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-849">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="5898b-850">5,297.69</span></span></td>
<td><span data-ttu-id="5898b-851">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-852">CC004</span><span class="sxs-lookup"><span data-stu-id="5898b-852">CC004</span></span></td>
<td><span data-ttu-id="5898b-853">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5898b-853">Packaging</span></span></td>
<td><span data-ttu-id="5898b-854">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-854">10001</span></span></td>
<td><span data-ttu-id="5898b-855">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-855">Electricity</span></span></td>
<td><span data-ttu-id="5898b-856">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-856">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="5898b-857">2,852.60</span></span></td>
<td><span data-ttu-id="5898b-858">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-859">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-859">CC003</span></span></td>
<td><span data-ttu-id="5898b-860">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5898b-860">Assembly</span></span></td>
<td><span data-ttu-id="5898b-861">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-861">10001</span></span></td>
<td><span data-ttu-id="5898b-862">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-862">Electricity</span></span></td>
<td><span data-ttu-id="5898b-863">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-863">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="5898b-864">-713.75</span></span></td>
<td><span data-ttu-id="5898b-865">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-866">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-866">Prod 1</span></span></td>
<td><span data-ttu-id="5898b-867">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-867">Product 1</span></span></td>
<td><span data-ttu-id="5898b-868">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-868">10001</span></span></td>
<td><span data-ttu-id="5898b-869">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-869">Electricity</span></span></td>
<td><span data-ttu-id="5898b-870">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-870">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-871">535.31</span><span class="sxs-lookup"><span data-stu-id="5898b-871">535.31</span></span></td>
<td><span data-ttu-id="5898b-872">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-873">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-873">Prod 2</span></span></td>
<td><span data-ttu-id="5898b-874">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-874">Product 2</span></span></td>
<td><span data-ttu-id="5898b-875">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-875">10001</span></span></td>
<td><span data-ttu-id="5898b-876">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-876">Electricity</span></span></td>
<td><span data-ttu-id="5898b-877">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-877">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-878">178.44</span><span class="sxs-lookup"><span data-stu-id="5898b-878">178.44</span></span></td>
<td><span data-ttu-id="5898b-879">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-880">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-880">CC003</span></span></td>
<td><span data-ttu-id="5898b-881">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5898b-881">Assembly</span></span></td>
<td><span data-ttu-id="5898b-882">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-882">10001</span></span></td>
<td><span data-ttu-id="5898b-883">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-883">Electricity</span></span></td>
<td><span data-ttu-id="5898b-884">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-884">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="5898b-885">-5,982.83</span></span></td>
<td><span data-ttu-id="5898b-886">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-887">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-887">Prod 1</span></span></td>
<td><span data-ttu-id="5898b-888">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-888">Product 1</span></span></td>
<td><span data-ttu-id="5898b-889">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-889">10001</span></span></td>
<td><span data-ttu-id="5898b-890">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-890">Electricity</span></span></td>
<td><span data-ttu-id="5898b-891">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-891">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="5898b-892">4,487.12</span></span></td>
<td><span data-ttu-id="5898b-893">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-894">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-894">Prod 2</span></span></td>
<td><span data-ttu-id="5898b-895">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-895">Product 2</span></span></td>
<td><span data-ttu-id="5898b-896">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-896">10001</span></span></td>
<td><span data-ttu-id="5898b-897">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-897">Electricity</span></span></td>
<td><span data-ttu-id="5898b-898">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-898">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="5898b-899">1,495.71</span></span></td>
<td><span data-ttu-id="5898b-900">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-901">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-901">CC003</span></span></td>
<td><span data-ttu-id="5898b-902">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5898b-902">Assembly</span></span></td>
<td><span data-ttu-id="5898b-903">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-903">10001</span></span></td>
<td><span data-ttu-id="5898b-904">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-904">Electricity</span></span></td>
<td><span data-ttu-id="5898b-905">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-905">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="5898b-906">-286.25</span></span></td>
<td><span data-ttu-id="5898b-907">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-908">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-908">Prod 1</span></span></td>
<td><span data-ttu-id="5898b-909">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-909">Product 1</span></span></td>
<td><span data-ttu-id="5898b-910">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-910">10001</span></span></td>
<td><span data-ttu-id="5898b-911">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-911">Electricity</span></span></td>
<td><span data-ttu-id="5898b-912">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-912">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-913">241.05</span><span class="sxs-lookup"><span data-stu-id="5898b-913">241.05</span></span></td>
<td><span data-ttu-id="5898b-914">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-915">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-915">Prod 2</span></span></td>
<td><span data-ttu-id="5898b-916">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-916">Product 2</span></span></td>
<td><span data-ttu-id="5898b-917">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-917">10001</span></span></td>
<td><span data-ttu-id="5898b-918">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-918">Electricity</span></span></td>
<td><span data-ttu-id="5898b-919">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-919">Fixed cost</span></span></td>
<td><span data-ttu-id="5898b-920">45.20</span><span class="sxs-lookup"><span data-stu-id="5898b-920">45.20</span></span></td>
<td><span data-ttu-id="5898b-921">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-922">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-922">CC003</span></span></td>
<td><span data-ttu-id="5898b-923">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5898b-923">Assembly</span></span></td>
<td><span data-ttu-id="5898b-924">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-924">10001</span></span></td>
<td><span data-ttu-id="5898b-925">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-925">Electricity</span></span></td>
<td><span data-ttu-id="5898b-926">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-926">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-927">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="5898b-927">-2,977.17</span></span></td>
<td><span data-ttu-id="5898b-928">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-929">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-929">Prod 1</span></span></td>
<td><span data-ttu-id="5898b-930">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-930">Product 1</span></span></td>
<td><span data-ttu-id="5898b-931">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-931">10001</span></span></td>
<td><span data-ttu-id="5898b-932">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-932">Electricity</span></span></td>
<td><span data-ttu-id="5898b-933">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-933">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="5898b-934">2,507.09</span></span></td>
<td><span data-ttu-id="5898b-935">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5898b-936">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-936">Prod 2</span></span></td>
<td><span data-ttu-id="5898b-937">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-937">Product 2</span></span></td>
<td><span data-ttu-id="5898b-938">10 001</span><span class="sxs-lookup"><span data-stu-id="5898b-938">10001</span></span></td>
<td><span data-ttu-id="5898b-939">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-939">Electricity</span></span></td>
<td><span data-ttu-id="5898b-940">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-940">Variable cost</span></span></td>
<td><span data-ttu-id="5898b-941">470.08</span><span class="sxs-lookup"><span data-stu-id="5898b-941">470.08</span></span></td>
<td><span data-ttu-id="5898b-942">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5898b-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="5898b-943">Johtopäätökset</span><span class="sxs-lookup"><span data-stu-id="5898b-943">Conclusion</span></span>
<span data-ttu-id="5898b-944">Kirjanpidossa kirjataan tyhjään kustannuspaikkatunnukseen sähkökustannus arvolla 10 000,00.</span><span class="sxs-lookup"><span data-stu-id="5898b-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="5898b-945">Tämän ansiosta kustannuslaskijat tietävät, että kustannus on kohdistettava.</span><span class="sxs-lookup"><span data-stu-id="5898b-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="5898b-946">Kustannukset virtaavat kirjanpidossa organisaation yksiköiden ja tasojen läpi käytössä olevien käytäntöjen ja sääntöjen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="5898b-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="5898b-947">Kukin kustannus on liitetty kustannusperusteeseen, joka sisältää parhaan arvion kustannusten kohdistuksesta.</span><span class="sxs-lookup"><span data-stu-id="5898b-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="5898b-948">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="5898b-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="5898b-949">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5898b-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="5898b-950">Yhteensä</span><span class="sxs-lookup"><span data-stu-id="5898b-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5898b-951">CC099</span><span class="sxs-lookup"><span data-stu-id="5898b-951">CC099</span></span></th>
<th><span data-ttu-id="5898b-952">CC001</span><span class="sxs-lookup"><span data-stu-id="5898b-952">CC001</span></span></th>
<th><span data-ttu-id="5898b-953">CC002</span><span class="sxs-lookup"><span data-stu-id="5898b-953">CC002</span></span></th>
<th><span data-ttu-id="5898b-954">CC003</span><span class="sxs-lookup"><span data-stu-id="5898b-954">CC003</span></span></th>
<th><span data-ttu-id="5898b-955">CC004</span><span class="sxs-lookup"><span data-stu-id="5898b-955">CC004</span></span></th>
<th><span data-ttu-id="5898b-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5898b-956">Proj 1</span></span></th>
<th><span data-ttu-id="5898b-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5898b-957">Proj 2</span></span></th>
<th><span data-ttu-id="5898b-958">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5898b-958">Prod 1</span></span></th>
<th><span data-ttu-id="5898b-959">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5898b-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="5898b-960">10001 Sähkö</span><span class="sxs-lookup"><span data-stu-id="5898b-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="5898b-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="5898b-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="5898b-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="5898b-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="5898b-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="5898b-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="5898b-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="5898b-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="5898b-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="5898b-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="5898b-970">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="5898b-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-971">0,00</span><span class="sxs-lookup"><span data-stu-id="5898b-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="5898b-972">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5898b-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-973">0,00</span><span class="sxs-lookup"><span data-stu-id="5898b-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-974">0,00</span><span class="sxs-lookup"><span data-stu-id="5898b-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-975">0,00</span><span class="sxs-lookup"><span data-stu-id="5898b-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-976">0,00</span><span class="sxs-lookup"><span data-stu-id="5898b-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-977">0,00</span><span class="sxs-lookup"><span data-stu-id="5898b-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="5898b-978">776.36</span><span class="sxs-lookup"><span data-stu-id="5898b-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-979">223.64</span><span class="sxs-lookup"><span data-stu-id="5898b-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="5898b-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="5898b-981">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5898b-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-982">000</span><span class="sxs-lookup"><span data-stu-id="5898b-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-983">0,00</span><span class="sxs-lookup"><span data-stu-id="5898b-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-984">0,00</span><span class="sxs-lookup"><span data-stu-id="5898b-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-985">0,00</span><span class="sxs-lookup"><span data-stu-id="5898b-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-986">0,00</span><span class="sxs-lookup"><span data-stu-id="5898b-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-987">30,00</span><span class="sxs-lookup"><span data-stu-id="5898b-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-988">10,00</span><span class="sxs-lookup"><span data-stu-id="5898b-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="5898b-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="5898b-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5898b-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="5898b-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5898b-992">Tässä ohjeaiheessa esitellään, miten ensisijainen kustannuselementti, 10001 Sähkö, virtaa kustannusobjektien läpi.</span><span class="sxs-lookup"><span data-stu-id="5898b-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="5898b-993">Tästä syystä tämä yleiskustannus kohdistetaan organisaation alimmalle tasolle.</span><span class="sxs-lookup"><span data-stu-id="5898b-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="5898b-994">Toisin sanoen alimman tason kustannusobjektit kantavat kustannuksen.</span><span class="sxs-lookup"><span data-stu-id="5898b-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="5898b-995">Jos tarvitset visuaalisen näkymän kustannuksen virrasta kustannusobjektien välillä, voit käyttää kustannuksen koontikäytäntösääntöjä kustannusvirran visualisointiin.</span><span class="sxs-lookup"><span data-stu-id="5898b-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="5898b-996">Lisätietoja on kohdassa [Kustannusten koontikäytäntö ja yleiskustannuslaskenta](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="5898b-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]