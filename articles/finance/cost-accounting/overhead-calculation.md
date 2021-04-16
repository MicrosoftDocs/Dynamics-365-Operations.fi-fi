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
ms.openlocfilehash: 2dddc22128621dc148a253cd568430587f294544
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822900"
---
# <a name="overhead-calculation"></a><span data-ttu-id="8e8bf-103">Yleiskustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="8e8bf-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e8bf-104">Tässä aiheessa kuvataan tyypillinen yleiskustannusten laskenta- ja kohdistusprosessi.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="8e8bf-105">Sanaston määritelmä</span><span class="sxs-lookup"><span data-stu-id="8e8bf-105">Term definition</span></span>
---------------

<span data-ttu-id="8e8bf-106">Yleiskustannukset ovat yrityksen toiminnasta syntyviä kustannuksia, joita ei voi suoraan liittää mihinkään tiettyyn liiketoiminnan tehtävään, tuotteeseen tai palveluun.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="8e8bf-107">Yleiskustannukset ovat tärkeä tuki voittoa tuottavien tehtävien luonnissa.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="8e8bf-108">Seuraavassa on joitakin esimerkkejä yleiskustannuksista:</span><span class="sxs-lookup"><span data-stu-id="8e8bf-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="8e8bf-109">Vuokra</span><span class="sxs-lookup"><span data-stu-id="8e8bf-109">Rent</span></span>
-   <span data-ttu-id="8e8bf-110">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-110">Electricity</span></span>
-   <span data-ttu-id="8e8bf-111">Hallinnon palkat</span><span class="sxs-lookup"><span data-stu-id="8e8bf-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="8e8bf-112">Yleiskustannuslaskennan yleiskuva</span><span class="sxs-lookup"><span data-stu-id="8e8bf-112">Overhead calculation overview</span></span>
<span data-ttu-id="8e8bf-113">Yleiskustannusten laskenta suorittaa kustannuslaskennan käytännöt oikeassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="8e8bf-114">Yleiskustannusten laskennan voi suorittaa useita kertoja samalle tilikaudelle, jos kustannuslaskennan käytännöt ovat muuttuneet tai erityisiä virheitä on havaittu.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="8e8bf-115">Kukin laskenta-ajo tallennetaan ja kullekin annetaan yksilöllinen versiotunnus, jonka avulla eri laskenta-ajoja voi verrata toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="8e8bf-116">Yleiskustannusten laskenta luo kustannustapahtumia, joille annetaan kirjauspäivä.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="8e8bf-117">Kirjauspäivä vastaa laskennassa käytettyä tilikauden päättymispäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="8e8bf-118">Yksilöivä versiotunnus sisältää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="8e8bf-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="8e8bf-119">Versiotyyppi</span><span class="sxs-lookup"><span data-stu-id="8e8bf-119">Version type</span></span>
-   <span data-ttu-id="8e8bf-120">Päivämäärä ja aika</span><span class="sxs-lookup"><span data-stu-id="8e8bf-120">Date and time</span></span>
-   <span data-ttu-id="8e8bf-121">Kustannuslaskennan kirjanpito</span><span class="sxs-lookup"><span data-stu-id="8e8bf-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="8e8bf-122">Tilikausi </span><span class="sxs-lookup"><span data-stu-id="8e8bf-122">Fiscal year</span></span>
-   <span data-ttu-id="8e8bf-123">Tilikausi  </span><span class="sxs-lookup"><span data-stu-id="8e8bf-123">Fiscal period</span></span>

<span data-ttu-id="8e8bf-124">Yleiskustannusten laskenta ajetaan versiosta riippumattomana.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="8e8bf-125">Voit siis laskea budjetin version ennen todellista versiota.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="8e8bf-126">Yleiskustannusten laskenta koostuu neljästä vaiheesta, jotka esitellään seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="8e8bf-127">Kussakin vaiheessa luodaan kirjauskansion otsikko, jolla on kirjauskansiovientejä.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="8e8bf-128">Tämä kirjauskansion otsikko säilyttää kunkin laskentavaiheen syöttötiedot.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="8e8bf-129">Käytännöt ja säännöt ajetaan kullekin kirjauskansion riville, ja tuloksena luodaan kustannustapahtumia.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="8e8bf-130">Tämän ansiosta kaikki laskutoimitukset ovat täysin jäljitettävissä.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="8e8bf-131">[![Yleiskustannuslaskenta](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="8e8bf-132">Laske ja kohdista sähkön yleiskustannukset</span><span class="sxs-lookup"><span data-stu-id="8e8bf-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="8e8bf-133">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="8e8bf-134">Tarkka johdon näkymä ei täten ole saatavilla kustannuslaskennassa.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="8e8bf-135">Jotta kustannuslaskenta tarjoaisi oikean johdon näkymän kaikista organisaation yksiköistä ja tasoista, kustannusten on virrattava organisaation yksiköiden läpi.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="8e8bf-136">Tämän virran on perustuttava joko tarkkaan tietoon kulutuksesta tai perusteltuun arvioon.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="8e8bf-137">Sähkökustannukset voi kirjata kirjanpitoon seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8e8bf-138">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="8e8bf-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8e8bf-139">Kustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="8e8bf-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="8e8bf-140">Päätili</span><span class="sxs-lookup"><span data-stu-id="8e8bf-140">Main account</span></span></th>
<th><span data-ttu-id="8e8bf-141">Summa kirjanpitovaluuttana</span><span class="sxs-lookup"><span data-stu-id="8e8bf-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-142">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="8e8bf-143">CC099</span><span class="sxs-lookup"><span data-stu-id="8e8bf-143">CC099</span></span></td>
<td><span data-ttu-id="8e8bf-144">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="8e8bf-144">Default cost center</span></span></td>
<td><span data-ttu-id="8e8bf-145">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-145">10001</span></span></td>
<td><span data-ttu-id="8e8bf-146">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-146">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="8e8bf-148">Vaihe 1: Käsittele kustannustoiminnan laskenta</span><span class="sxs-lookup"><span data-stu-id="8e8bf-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="8e8bf-149">Kun kustannustapahtumat tuodaan lähdetiedoista, niille asetetaan kustannuslaskennassa oletusarvoisesti **Luokittelematon** -kustannustoimintaluokka.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="8e8bf-150">Voit luokitella kustannustapahtumia uudelleen **kiinteäksi kustannukseksi** tai **muuttuvaksi kustannukseksi** kustannustoiminnan käytäntösäännöillä.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="8e8bf-151">Määritä kustannustoiminnan sääntö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-151">Define the cost behavior rule</span></span>

<span data-ttu-id="8e8bf-152">Joissain tapauksissa osa kustannuksesta on kiinteä ja loppuosa perustuu kulutukseen.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="8e8bf-153">Sähkölaskut sopivat usein tähän määritelmään.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="8e8bf-154">Maksat ensin määrätyn, kiinteän maksun, jonka lisäksi maksat kulutuksesta kilowattitunteina (kWh).</span><span class="sxs-lookup"><span data-stu-id="8e8bf-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="8e8bf-155">Jos kiinteä maksu on esimerkiksi 1 000,00, kustannustoiminnan sääntö määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="8e8bf-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="8e8bf-156">Kiinteä määrä 1 000,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="8e8bf-157">0 &lt;= 1 000,00 = Kiinteä</span><span class="sxs-lookup"><span data-stu-id="8e8bf-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="8e8bf-158">1000,01 &lt; N = Muuttuva</span><span class="sxs-lookup"><span data-stu-id="8e8bf-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="8e8bf-159">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="8e8bf-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8e8bf-160">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="8e8bf-160">Journal</span></span></th>
<th><span data-ttu-id="8e8bf-161">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="8e8bf-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8e8bf-162">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="8e8bf-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8e8bf-163">Versio</span><span class="sxs-lookup"><span data-stu-id="8e8bf-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-164">00001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-164">00001</span></span></td>
<td><span data-ttu-id="8e8bf-165">Kustannustoiminnan laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="8e8bf-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="8e8bf-166">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="8e8bf-166">Fiscal</span></span></td>
<td><span data-ttu-id="8e8bf-167">2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-167">2017</span></span></td>
<td><span data-ttu-id="8e8bf-168">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-168">Period 1</span></span></td>
<td><span data-ttu-id="8e8bf-169">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8e8bf-170">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8e8bf-171">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="8e8bf-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8e8bf-172">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8e8bf-173">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="8e8bf-173">Cost element</span></span></th>
<th><span data-ttu-id="8e8bf-174">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="8e8bf-174">Cost behavior</span></span></th>
<th><span data-ttu-id="8e8bf-175">Summa</span><span class="sxs-lookup"><span data-stu-id="8e8bf-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-176">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="8e8bf-177">CC099</span><span class="sxs-lookup"><span data-stu-id="8e8bf-177">CC099</span></span></td>
<td><span data-ttu-id="8e8bf-178">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="8e8bf-178">Default cost center</span></span></td>
<td><span data-ttu-id="8e8bf-179">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-179">10001</span></span></td>
<td><span data-ttu-id="8e8bf-180">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-180">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-181">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="8e8bf-181">Unclassified</span></span></td>
<td><span data-ttu-id="8e8bf-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8e8bf-183">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="8e8bf-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8e8bf-184">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8e8bf-185">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="8e8bf-185">Cost element</span></span></th>
<th><span data-ttu-id="8e8bf-186">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="8e8bf-186">Cost behavior</span></span></th>
<th><span data-ttu-id="8e8bf-187">Summa</span><span class="sxs-lookup"><span data-stu-id="8e8bf-187">Amount</span></span></th>
<th><span data-ttu-id="8e8bf-188">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="8e8bf-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-189">CC099</span><span class="sxs-lookup"><span data-stu-id="8e8bf-189">CC099</span></span></td>
<td><span data-ttu-id="8e8bf-190">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="8e8bf-190">Default cost center</span></span></td>
<td><span data-ttu-id="8e8bf-191">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-191">10001</span></span></td>
<td><span data-ttu-id="8e8bf-192">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-192">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-193">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="8e8bf-193">Unclassified</span></span></td>
<td><span data-ttu-id="8e8bf-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-194">10,000.00</span></span></td>
<td><span data-ttu-id="8e8bf-195">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-196">CC099</span><span class="sxs-lookup"><span data-stu-id="8e8bf-196">CC099</span></span></td>
<td><span data-ttu-id="8e8bf-197">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="8e8bf-197">Default cost center</span></span></td>
<td><span data-ttu-id="8e8bf-198">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-198">10001</span></span></td>
<td><span data-ttu-id="8e8bf-199">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-199">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-200">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="8e8bf-200">Unclassified</span></span></td>
<td><span data-ttu-id="8e8bf-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-201">-10,000.00</span></span></td>
<td><span data-ttu-id="8e8bf-202">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-203">CC099</span><span class="sxs-lookup"><span data-stu-id="8e8bf-203">CC099</span></span></td>
<td><span data-ttu-id="8e8bf-204">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="8e8bf-204">Default cost center</span></span></td>
<td><span data-ttu-id="8e8bf-205">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-205">10001</span></span></td>
<td><span data-ttu-id="8e8bf-206">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-206">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-207">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-207">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-208">1,000.00</span></span></td>
<td><span data-ttu-id="8e8bf-209">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-210">CC099</span><span class="sxs-lookup"><span data-stu-id="8e8bf-210">CC099</span></span></td>
<td><span data-ttu-id="8e8bf-211">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="8e8bf-211">Default cost center</span></span></td>
<td><span data-ttu-id="8e8bf-212">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-212">10001</span></span></td>
<td><span data-ttu-id="8e8bf-213">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-213">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-214">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-214">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-215">9,000.00</span></span></td>
<td><span data-ttu-id="8e8bf-216">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8e8bf-217">Lisätietoja on kohdassa [Kustannustoimintakäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="8e8bf-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="8e8bf-218">Vaihe 2: Käsittele kustannusten jaon laskenta</span><span class="sxs-lookup"><span data-stu-id="8e8bf-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="8e8bf-219">Kustannusten jakoa käytetään kustannusten jakamiseen yhdestä kustannusobjektista toiseen (tai useampaan kustannusobjektiin) määrittämällä asiaankuuluvan kohdistusperusteen.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="8e8bf-220">Kustannusten jako ja kustannusten kohdistus eroavat toisistaan sillä, että kustannusten jako tapahtuu aina alkuperäisen kustannuksen ensisijaisen kustannuselementin tasolla.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="8e8bf-221">Määritä kustannusten jaon sääntö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-221">Define the cost distribution rule</span></span>

<span data-ttu-id="8e8bf-222">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="8e8bf-223">Kustannuslaskenta ei tarjoa tästä tarpeeksi tarkkoja tietoja.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="8e8bf-224">Muuttuva kustannus tulisi jakaa yksittäisille kustannusobjekteille reiluin perustein.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="8e8bf-225">Loogisin kohdistusperuste on sähkönkulutus (kWh).</span><span class="sxs-lookup"><span data-stu-id="8e8bf-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="8e8bf-226">Luodaan tilastollinen dimensionjäsen nimeltä Sähkö, johon kirjataan sähkönkulutus.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="8e8bf-227">Oletusarvon mukaan kaikki tilastolliset dimensiojäsenet ovat käytettävissä kohdistusperusteina.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8e8bf-228">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-228">Cost object</span></span></th>
<th><span data-ttu-id="8e8bf-229">kWh</span><span class="sxs-lookup"><span data-stu-id="8e8bf-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-230">CC001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-230">CC001</span></span></td>
<td><span data-ttu-id="8e8bf-231">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="8e8bf-231">HR</span></span></td>
<td><span data-ttu-id="8e8bf-232">1 000</span><span class="sxs-lookup"><span data-stu-id="8e8bf-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-233">CC002</span><span class="sxs-lookup"><span data-stu-id="8e8bf-233">CC002</span></span></td>
<td><span data-ttu-id="8e8bf-234">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="8e8bf-234">Finance</span></span></td>
<td><span data-ttu-id="8e8bf-235">6,000</span><span class="sxs-lookup"><span data-stu-id="8e8bf-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-236">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-236">CC003</span></span></td>
<td><span data-ttu-id="8e8bf-237">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="8e8bf-237">Assembly</span></span></td>
<td><span data-ttu-id="8e8bf-238">0</span><span class="sxs-lookup"><span data-stu-id="8e8bf-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8e8bf-239">Seuraavassa taulukossa on esitetty tulos, kun sähkönkulutusta käytetään kohdistusperusteena muuttuville kuluille.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8e8bf-240">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-240">Cost object</span></span></th>
<th><span data-ttu-id="8e8bf-241">Suuruus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-241">Magnitude</span></span></th>
<th><span data-ttu-id="8e8bf-242">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="8e8bf-242">Allocation factor</span></span></th>
<th><span data-ttu-id="8e8bf-243">Summa</span><span class="sxs-lookup"><span data-stu-id="8e8bf-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-244">CC001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-244">CC001</span></span></td>
<td><span data-ttu-id="8e8bf-245">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="8e8bf-245">HR</span></span></td>
<td><span data-ttu-id="8e8bf-246">1 000</span><span class="sxs-lookup"><span data-stu-id="8e8bf-246">1,000</span></span></td>
<td><span data-ttu-id="8e8bf-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8e8bf-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="8e8bf-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-249">CC002</span><span class="sxs-lookup"><span data-stu-id="8e8bf-249">CC002</span></span></td>
<td><span data-ttu-id="8e8bf-250">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="8e8bf-250">Finance</span></span></td>
<td><span data-ttu-id="8e8bf-251">6,000</span><span class="sxs-lookup"><span data-stu-id="8e8bf-251">6,000</span></span></td>
<td><span data-ttu-id="8e8bf-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8e8bf-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="8e8bf-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-254">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-254">CC003</span></span></td>
<td><span data-ttu-id="8e8bf-255">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="8e8bf-255">Assembly</span></span></td>
<td><span data-ttu-id="8e8bf-256">0</span><span class="sxs-lookup"><span data-stu-id="8e8bf-256">0</span></span></td>
<td><span data-ttu-id="8e8bf-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8e8bf-258">0,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8e8bf-259">Kiinteä kustannus tulisi jakaa tasaisesti yksittäisille kustannusobjekteille, jotka ovat kuluttaneet sähköä.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="8e8bf-260">Voit käyttää sähkön tilastollista dimensiojäsentä kaavan kohdistusperusteena tämän tavoitteen saavuttamiseksi: (sähkö &gt;0,00) Seuraavassa taulukossa on esitetty tulos siitä, kun sähkönkulutus on määritetty muuttuvien kustannusten kohdistusperusteeksi.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8e8bf-261">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-261">Cost object</span></span></th>
<th><span data-ttu-id="8e8bf-262">Resepti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-262">Formula</span></span></th>
<th><span data-ttu-id="8e8bf-263">Suuruus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-263">Magnitude</span></span></th>
<th><span data-ttu-id="8e8bf-264">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="8e8bf-264">Allocation factor</span></span></th>
<th><span data-ttu-id="8e8bf-265">Summa</span><span class="sxs-lookup"><span data-stu-id="8e8bf-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-266">CC001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-266">CC001</span></span></td>
<td><span data-ttu-id="8e8bf-267">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="8e8bf-267">HR</span></span></td>
<td><span data-ttu-id="8e8bf-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8e8bf-269">1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-269">1</span></span></td>
<td><span data-ttu-id="8e8bf-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8e8bf-271">500,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-272">CC002</span><span class="sxs-lookup"><span data-stu-id="8e8bf-272">CC002</span></span></td>
<td><span data-ttu-id="8e8bf-273">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="8e8bf-273">Finance</span></span></td>
<td><span data-ttu-id="8e8bf-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8e8bf-275">1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-275">1</span></span></td>
<td><span data-ttu-id="8e8bf-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8e8bf-277">500,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-278">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-278">CC003</span></span></td>
<td><span data-ttu-id="8e8bf-279">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="8e8bf-279">Assembly</span></span></td>
<td><span data-ttu-id="8e8bf-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8e8bf-281">0</span><span class="sxs-lookup"><span data-stu-id="8e8bf-281">0</span></span></td>
<td><span data-ttu-id="8e8bf-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8e8bf-283">0,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="8e8bf-284">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="8e8bf-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8e8bf-285">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="8e8bf-285">Journal</span></span></th>
<th><span data-ttu-id="8e8bf-286">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="8e8bf-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8e8bf-287">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="8e8bf-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8e8bf-288">Versio</span><span class="sxs-lookup"><span data-stu-id="8e8bf-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-289">00002</span><span class="sxs-lookup"><span data-stu-id="8e8bf-289">00002</span></span></td>
<td><span data-ttu-id="8e8bf-290">Kustannusten jaon laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="8e8bf-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="8e8bf-291">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="8e8bf-291">Fiscal</span></span></td>
<td><span data-ttu-id="8e8bf-292">2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-292">2017</span></span></td>
<td><span data-ttu-id="8e8bf-293">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-293">Period 1</span></span></td>
<td><span data-ttu-id="8e8bf-294">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8e8bf-295">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8e8bf-296">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="8e8bf-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8e8bf-297">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8e8bf-298">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="8e8bf-298">Cost element</span></span></th>
<th><span data-ttu-id="8e8bf-299">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="8e8bf-299">Cost behavior</span></span></th>
<th><span data-ttu-id="8e8bf-300">Summa</span><span class="sxs-lookup"><span data-stu-id="8e8bf-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-301">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="8e8bf-302">CC099</span><span class="sxs-lookup"><span data-stu-id="8e8bf-302">CC099</span></span></td>
<td><span data-ttu-id="8e8bf-303">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="8e8bf-303">Default cost center</span></span></td>
<td><span data-ttu-id="8e8bf-304">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-304">10001</span></span></td>
<td><span data-ttu-id="8e8bf-305">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-305">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-306">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-306">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-308">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="8e8bf-309">CC099</span><span class="sxs-lookup"><span data-stu-id="8e8bf-309">CC099</span></span></td>
<td><span data-ttu-id="8e8bf-310">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="8e8bf-310">Default cost center</span></span></td>
<td><span data-ttu-id="8e8bf-311">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-311">10001</span></span></td>
<td><span data-ttu-id="8e8bf-312">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-312">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-313">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-313">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8e8bf-315">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="8e8bf-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8e8bf-316">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8e8bf-317">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="8e8bf-317">Cost element</span></span></th>
<th><span data-ttu-id="8e8bf-318">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="8e8bf-318">Cost behavior</span></span></th>
<th><span data-ttu-id="8e8bf-319">Summa</span><span class="sxs-lookup"><span data-stu-id="8e8bf-319">Amount</span></span></th>
<th><span data-ttu-id="8e8bf-320">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="8e8bf-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-321">CC099</span><span class="sxs-lookup"><span data-stu-id="8e8bf-321">CC099</span></span></td>
<td><span data-ttu-id="8e8bf-322">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="8e8bf-322">Default cost center</span></span></td>
<td><span data-ttu-id="8e8bf-323">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-323">10001</span></span></td>
<td><span data-ttu-id="8e8bf-324">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-324">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-325">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-325">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-326">-1,000.00</span></span></td>
<td><span data-ttu-id="8e8bf-327">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-328">CC001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-328">CC001</span></span></td>
<td><span data-ttu-id="8e8bf-329">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="8e8bf-329">HR</span></span></td>
<td><span data-ttu-id="8e8bf-330">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-330">10001</span></span></td>
<td><span data-ttu-id="8e8bf-331">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-331">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-332">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-332">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-333">500,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-333">500.00</span></span></td>
<td><span data-ttu-id="8e8bf-334">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-335">CC002</span><span class="sxs-lookup"><span data-stu-id="8e8bf-335">CC002</span></span></td>
<td><span data-ttu-id="8e8bf-336">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="8e8bf-336">Finance</span></span></td>
<td><span data-ttu-id="8e8bf-337">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-337">10001</span></span></td>
<td><span data-ttu-id="8e8bf-338">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-338">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-339">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-339">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-340">500,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-340">500.00</span></span></td>
<td><span data-ttu-id="8e8bf-341">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-342">CC099</span><span class="sxs-lookup"><span data-stu-id="8e8bf-342">CC099</span></span></td>
<td><span data-ttu-id="8e8bf-343">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="8e8bf-343">Default cost center</span></span></td>
<td><span data-ttu-id="8e8bf-344">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-344">10001</span></span></td>
<td><span data-ttu-id="8e8bf-345">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-345">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-346">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-346">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-347">-9,000.00</span></span></td>
<td><span data-ttu-id="8e8bf-348">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-349">CC001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-349">CC001</span></span></td>
<td><span data-ttu-id="8e8bf-350">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="8e8bf-350">HR</span></span></td>
<td><span data-ttu-id="8e8bf-351">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-351">10001</span></span></td>
<td><span data-ttu-id="8e8bf-352">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-352">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-353">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-353">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="8e8bf-354">1,285.71</span></span></td>
<td><span data-ttu-id="8e8bf-355">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-356">CC002</span><span class="sxs-lookup"><span data-stu-id="8e8bf-356">CC002</span></span></td>
<td><span data-ttu-id="8e8bf-357">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="8e8bf-357">Finance</span></span></td>
<td><span data-ttu-id="8e8bf-358">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-358">10001</span></span></td>
<td><span data-ttu-id="8e8bf-359">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-359">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-360">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-360">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="8e8bf-361">7,714.29</span></span></td>
<td><span data-ttu-id="8e8bf-362">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8e8bf-363">Lisätietoja on kohdassa [Jakelukäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="8e8bf-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="8e8bf-364">Vaihe 3: Käsittele yleiskustannustason laskenta</span><span class="sxs-lookup"><span data-stu-id="8e8bf-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="8e8bf-365">Yleiskustannustasolla veloitetaan yksi tai useampi määrätty kustannusobjekti.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="8e8bf-366">Veloitus perustuu ennalta määrättyyn kustannustasoon sekä määritetyn kohdistusperusteen suuruuteen.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="8e8bf-367">Määritä yleiskustannustaso.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-367">Define the overhead rate</span></span>

<span data-ttu-id="8e8bf-368">Kustannusobjekti CC001 HR vaikuttaa joukkoon sisäisiä projekteja.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="8e8bf-369">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon projektit.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8e8bf-370">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-370">Cost object</span></span></th>
<th><span data-ttu-id="8e8bf-371">Tunnit</span><span class="sxs-lookup"><span data-stu-id="8e8bf-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-372">Proj 1</span></span></td>
<td><span data-ttu-id="8e8bf-373">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-373">Project 1</span></span></td>
<td><span data-ttu-id="8e8bf-374">3</span><span class="sxs-lookup"><span data-stu-id="8e8bf-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-375">Proj 2</span></span></td>
<td><span data-ttu-id="8e8bf-376">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-376">Project 2</span></span></td>
<td><span data-ttu-id="8e8bf-377">1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8e8bf-378">Kustannusprojektien osuudelle on määritetty ennalta kustannushinta.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8e8bf-379">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-379">Cost object</span></span></th>
<th><span data-ttu-id="8e8bf-380">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="8e8bf-380">Cost element</span></span></th>
<th><span data-ttu-id="8e8bf-381">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="8e8bf-381">Cost behavior</span></span></th>
<th><span data-ttu-id="8e8bf-382">Yksiköt</span><span class="sxs-lookup"><span data-stu-id="8e8bf-382">Units</span></span></th>
<th><span data-ttu-id="8e8bf-383">Osuus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-384">CC001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-384">CC001</span></span></td>
<td><span data-ttu-id="8e8bf-385">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="8e8bf-385">HR</span></span></td>
<td><span data-ttu-id="8e8bf-386">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-386">10001</span></span></td>
<td><span data-ttu-id="8e8bf-387">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-387">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-388">1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-388">1</span></span></td>
<td><span data-ttu-id="8e8bf-389">10</span><span class="sxs-lookup"><span data-stu-id="8e8bf-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8e8bf-390">Seuraavassa taulukossa on esitetty tulos, kun Henkilöstöhallinnon projekteja käytetään kohdistusperusteena.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8e8bf-391">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-391">Cost object</span></span></th>
<th><span data-ttu-id="8e8bf-392">Suuruus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-392">Magnitude</span></span></th>
<th><span data-ttu-id="8e8bf-393">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="8e8bf-393">Cost element</span></span></th>
<th><span data-ttu-id="8e8bf-394">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="8e8bf-394">Allocation factor</span></span></th>
<th><span data-ttu-id="8e8bf-395">Summa</span><span class="sxs-lookup"><span data-stu-id="8e8bf-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-396">Proj 1</span></span></td>
<td><span data-ttu-id="8e8bf-397">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-397">Project 1</span></span></td>
<td><span data-ttu-id="8e8bf-398">3</span><span class="sxs-lookup"><span data-stu-id="8e8bf-398">3</span></span></td>
<td><span data-ttu-id="8e8bf-399">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-399">10001</span></span></td>
<td><span data-ttu-id="8e8bf-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="8e8bf-401">30,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-402">Proj 2</span></span></td>
<td><span data-ttu-id="8e8bf-403">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-403">Project 2</span></span></td>
<td><span data-ttu-id="8e8bf-404">1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-404">1</span></span></td>
<td><span data-ttu-id="8e8bf-405">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-405">10001</span></span></td>
<td><span data-ttu-id="8e8bf-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="8e8bf-407">10,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="8e8bf-408">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="8e8bf-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8e8bf-409">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="8e8bf-409">Journal</span></span></th>
<th><span data-ttu-id="8e8bf-410">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="8e8bf-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8e8bf-411">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="8e8bf-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8e8bf-412">Versio</span><span class="sxs-lookup"><span data-stu-id="8e8bf-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-413">00003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-413">00003</span></span></td>
<td><span data-ttu-id="8e8bf-414">Yleiskustannustason laskelman kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="8e8bf-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="8e8bf-415">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="8e8bf-415">Fiscal</span></span></td>
<td><span data-ttu-id="8e8bf-416">2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-416">2017</span></span></td>
<td><span data-ttu-id="8e8bf-417">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-417">Period 1</span></span></td>
<td><span data-ttu-id="8e8bf-418">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="8e8bf-419">Kirjauskansioviennit (Yleiskustannustason laskennan kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8e8bf-420">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="8e8bf-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8e8bf-421">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-421">Cost object</span></span></th>
<th><span data-ttu-id="8e8bf-422">Suuruus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-423">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="8e8bf-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-424">Proj 1</span></span></td>
<td><span data-ttu-id="8e8bf-425">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="8e8bf-426">3,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-427">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="8e8bf-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-428">Proj 2</span></span></td>
<td><span data-ttu-id="8e8bf-429">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="8e8bf-430">1,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8e8bf-431">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="8e8bf-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8e8bf-432">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8e8bf-433">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="8e8bf-433">Cost element</span></span></th>
<th><span data-ttu-id="8e8bf-434">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="8e8bf-434">Cost behavior</span></span></th>
<th><span data-ttu-id="8e8bf-435">Summa</span><span class="sxs-lookup"><span data-stu-id="8e8bf-435">Amount</span></span></th>
<th><span data-ttu-id="8e8bf-436">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="8e8bf-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-437">CC0001</span></span></td>
<td><span data-ttu-id="8e8bf-438">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="8e8bf-438">HR</span></span></td>
<td><span data-ttu-id="8e8bf-439">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-439">10001</span></span></td>
<td><span data-ttu-id="8e8bf-440">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-440">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-441">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-441">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-442">-30.00</span></span></td>
<td><span data-ttu-id="8e8bf-443">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-444">Proj 1</span></span></td>
<td><span data-ttu-id="8e8bf-445">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="8e8bf-446">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-446">10001</span></span></td>
<td><span data-ttu-id="8e8bf-447">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-447">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-448">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-448">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-449">30,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-449">30.00</span></span></td>
<td><span data-ttu-id="8e8bf-450">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-451">CC001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-451">CC001</span></span></td>
<td><span data-ttu-id="8e8bf-452">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="8e8bf-452">HR</span></span></td>
<td><span data-ttu-id="8e8bf-453">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-453">10001</span></span></td>
<td><span data-ttu-id="8e8bf-454">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-454">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-455">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-455">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-456">-10.00</span></span></td>
<td><span data-ttu-id="8e8bf-457">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-458">Proj 2</span></span></td>
<td><span data-ttu-id="8e8bf-459">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="8e8bf-460">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-460">10001</span></span></td>
<td><span data-ttu-id="8e8bf-461">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-461">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-462">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-462">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-463">10.00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-463">10.00</span></span></td>
<td><span data-ttu-id="8e8bf-464">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8e8bf-465">Lisätietoja on kohdassa [Yleisen laskennan suorittaminen](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="8e8bf-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="8e8bf-466">Vaihe 4: Käsittele kustannusten kohdistuksen laskenta</span><span class="sxs-lookup"><span data-stu-id="8e8bf-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="8e8bf-467">Kohdistuksella kustannusobjektin saldo liitetään toisiin kustannusobjekteihin käyttämällä kohdistusperustetta.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="8e8bf-468">Finance tukee vastavuoroista kohdistusmenetelmää.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="8e8bf-469">Vastavuoroisessa kohdistusmenetelmässä tunnistetaan oheiskustannusobjektien käyttämät, keskinäiset palvelut täysin.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="8e8bf-470">Järjestelmä määrittää oikean kohdistusjärjestyksen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="8e8bf-471">Kustannusobjektin saldo kohdistetaan yhdellä kohdistusperusteella.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="8e8bf-472">Kustannusobjektien dimensiot ja niiden vastaavat jäsenet ylittävät kohdistukset ovat tuettuja.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="8e8bf-473">Kustannusseurantayksikkö hallitsee kohdistusjärjestystä.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="8e8bf-474">[![Vastavuoroinen menetelmä](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="8e8bf-475">Määritä kustannuksen kohdistus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-475">Define the cost allocation</span></span>

<span data-ttu-id="8e8bf-476">Tämä on yksinkertainen esimerkki, jossa kerrotaan, miten voit jäljittää kustannuksen virran.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="8e8bf-477">Kustannusobjekti CC001 HR liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="8e8bf-478">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8e8bf-479">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-479">Cost object</span></span></th>
<th><span data-ttu-id="8e8bf-480">HR-palvelut</span><span class="sxs-lookup"><span data-stu-id="8e8bf-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-481">CC002</span><span class="sxs-lookup"><span data-stu-id="8e8bf-481">CC002</span></span></td>
<td><span data-ttu-id="8e8bf-482">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="8e8bf-482">Finance</span></span></td>
<td><span data-ttu-id="8e8bf-483">35</span><span class="sxs-lookup"><span data-stu-id="8e8bf-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-484">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-484">CC003</span></span></td>
<td><span data-ttu-id="8e8bf-485">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="8e8bf-485">Assembly</span></span></td>
<td><span data-ttu-id="8e8bf-486">55</span><span class="sxs-lookup"><span data-stu-id="8e8bf-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-487">CC004</span><span class="sxs-lookup"><span data-stu-id="8e8bf-487">CC004</span></span></td>
<td><span data-ttu-id="8e8bf-488">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-488">Packaging</span></span></td>
<td><span data-ttu-id="8e8bf-489">10</span><span class="sxs-lookup"><span data-stu-id="8e8bf-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8e8bf-490">Kustannusobjekti CC002 Taloushallinto liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="8e8bf-491">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Taloushallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8e8bf-492">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-492">Cost object</span></span></th>
<th><span data-ttu-id="8e8bf-493">Taloushallinnon palvelut</span><span class="sxs-lookup"><span data-stu-id="8e8bf-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-494">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-494">CC003</span></span></td>
<td><span data-ttu-id="8e8bf-495">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="8e8bf-495">Assembly</span></span></td>
<td><span data-ttu-id="8e8bf-496">65</span><span class="sxs-lookup"><span data-stu-id="8e8bf-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-497">CC004</span><span class="sxs-lookup"><span data-stu-id="8e8bf-497">CC004</span></span></td>
<td><span data-ttu-id="8e8bf-498">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-498">Packaging</span></span></td>
<td><span data-ttu-id="8e8bf-499">35</span><span class="sxs-lookup"><span data-stu-id="8e8bf-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8e8bf-500">Kustannusobjekti CC003 Kokoonpano liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="8e8bf-501">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Kokoonpanopalvelut.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8e8bf-502">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-502">Cost object</span></span></th>
<th><span data-ttu-id="8e8bf-503">Kokoonpanopalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-504">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-504">Prod 1</span></span></td>
<td><span data-ttu-id="8e8bf-505">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-505">Product 1</span></span></td>
<td><span data-ttu-id="8e8bf-506">60</span><span class="sxs-lookup"><span data-stu-id="8e8bf-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-507">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-507">Prod 2</span></span></td>
<td><span data-ttu-id="8e8bf-508">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-508">Product 2</span></span></td>
<td><span data-ttu-id="8e8bf-509">20</span><span class="sxs-lookup"><span data-stu-id="8e8bf-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8e8bf-510">Kustannusobjekti CC004 Pakkaus liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="8e8bf-511">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Pakkauspalvelut.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8e8bf-512">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-512">Cost object</span></span></th>
<th><span data-ttu-id="8e8bf-513">Pakkauspalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-514">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-514">Prod 1</span></span></td>
<td><span data-ttu-id="8e8bf-515">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-515">Product 1</span></span></td>
<td><span data-ttu-id="8e8bf-516">80</span><span class="sxs-lookup"><span data-stu-id="8e8bf-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-517">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-517">Prod 2</span></span></td>
<td><span data-ttu-id="8e8bf-518">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-518">Product 2</span></span></td>
<td><span data-ttu-id="8e8bf-519">15</span><span class="sxs-lookup"><span data-stu-id="8e8bf-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="8e8bf-520">Tilastomittaukset, kuten tämän tuotteen kuluttamat tuotantotunnit, voidaan johtaa lähdetiedoista.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="8e8bf-521">Lisätietoja on kohdassa [Tilastomittauksen lähdemalli](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="8e8bf-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="8e8bf-522">Seuraavassa taulukossa näytetään tulos, kun henkilöstöhallinnon palveluja käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="8e8bf-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8e8bf-523">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-523">Cost object</span></span></th>
<th><span data-ttu-id="8e8bf-524">Suuruus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-524">Magnitude</span></span></th>
<th><span data-ttu-id="8e8bf-525">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="8e8bf-525">Allocation factor</span></span></th>
<th><span data-ttu-id="8e8bf-526">Summa</span><span class="sxs-lookup"><span data-stu-id="8e8bf-526">Amount</span></span></th>
<th><span data-ttu-id="8e8bf-527">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="8e8bf-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-528">CC002</span><span class="sxs-lookup"><span data-stu-id="8e8bf-528">CC002</span></span></td>
<td><span data-ttu-id="8e8bf-529">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="8e8bf-529">Finance</span></span></td>
<td><span data-ttu-id="8e8bf-530">35</span><span class="sxs-lookup"><span data-stu-id="8e8bf-530">35</span></span></td>
<td><span data-ttu-id="8e8bf-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8e8bf-532">175.00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-532">175.00</span></span></td>
<td><span data-ttu-id="8e8bf-533">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-534">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-534">CC003</span></span></td>
<td><span data-ttu-id="8e8bf-535">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="8e8bf-535">Assembly</span></span></td>
<td><span data-ttu-id="8e8bf-536">55</span><span class="sxs-lookup"><span data-stu-id="8e8bf-536">55</span></span></td>
<td><span data-ttu-id="8e8bf-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8e8bf-538">275.00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-538">275.00</span></span></td>
<td><span data-ttu-id="8e8bf-539">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-540">CC004</span><span class="sxs-lookup"><span data-stu-id="8e8bf-540">CC004</span></span></td>
<td><span data-ttu-id="8e8bf-541">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-541">Packaging</span></span></td>
<td><span data-ttu-id="8e8bf-542">10</span><span class="sxs-lookup"><span data-stu-id="8e8bf-542">10</span></span></td>
<td><span data-ttu-id="8e8bf-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8e8bf-544">50,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-544">50.00</span></span></td>
<td><span data-ttu-id="8e8bf-545">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-546">CC002</span><span class="sxs-lookup"><span data-stu-id="8e8bf-546">CC002</span></span></td>
<td><span data-ttu-id="8e8bf-547">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="8e8bf-547">Finance</span></span></td>
<td><span data-ttu-id="8e8bf-548">35</span><span class="sxs-lookup"><span data-stu-id="8e8bf-548">35</span></span></td>
<td><span data-ttu-id="8e8bf-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="8e8bf-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8e8bf-550">436.00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-550">436.00</span></span></td>
<td><span data-ttu-id="8e8bf-551">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-552">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-552">CC003</span></span></td>
<td><span data-ttu-id="8e8bf-553">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="8e8bf-553">Assembly</span></span></td>
<td><span data-ttu-id="8e8bf-554">55</span><span class="sxs-lookup"><span data-stu-id="8e8bf-554">55</span></span></td>
<td><span data-ttu-id="8e8bf-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="8e8bf-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8e8bf-556">685.14</span><span class="sxs-lookup"><span data-stu-id="8e8bf-556">685.14</span></span></td>
<td><span data-ttu-id="8e8bf-557">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-558">CC004</span><span class="sxs-lookup"><span data-stu-id="8e8bf-558">CC004</span></span></td>
<td><span data-ttu-id="8e8bf-559">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-559">Packaging</span></span></td>
<td><span data-ttu-id="8e8bf-560">10</span><span class="sxs-lookup"><span data-stu-id="8e8bf-560">10</span></span></td>
<td><span data-ttu-id="8e8bf-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="8e8bf-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8e8bf-562">124.57</span><span class="sxs-lookup"><span data-stu-id="8e8bf-562">124.57</span></span></td>
<td><span data-ttu-id="8e8bf-563">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8e8bf-564">Seuraavassa taulukossa näytetään tulos, kun Taloushallinnon palveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="8e8bf-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8e8bf-565">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-565">Cost object</span></span></th>
<th><span data-ttu-id="8e8bf-566">Suuruus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-566">Magnitude</span></span></th>
<th><span data-ttu-id="8e8bf-567">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="8e8bf-567">Allocation factor</span></span></th>
<th><span data-ttu-id="8e8bf-568">Summa</span><span class="sxs-lookup"><span data-stu-id="8e8bf-568">Amount</span></span></th>
<th><span data-ttu-id="8e8bf-569">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="8e8bf-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-570">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-570">CC003</span></span></td>
<td><span data-ttu-id="8e8bf-571">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="8e8bf-571">Assembly</span></span></td>
<td><span data-ttu-id="8e8bf-572">65</span><span class="sxs-lookup"><span data-stu-id="8e8bf-572">65</span></span></td>
<td><span data-ttu-id="8e8bf-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="8e8bf-574">438.75</span><span class="sxs-lookup"><span data-stu-id="8e8bf-574">438.75</span></span></td>
<td><span data-ttu-id="8e8bf-575">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-576">CC004</span><span class="sxs-lookup"><span data-stu-id="8e8bf-576">CC004</span></span></td>
<td><span data-ttu-id="8e8bf-577">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-577">Packaging</span></span></td>
<td><span data-ttu-id="8e8bf-578">35</span><span class="sxs-lookup"><span data-stu-id="8e8bf-578">35</span></span></td>
<td><span data-ttu-id="8e8bf-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="8e8bf-580">236.25</span><span class="sxs-lookup"><span data-stu-id="8e8bf-580">236.25</span></span></td>
<td><span data-ttu-id="8e8bf-581">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-582">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-582">CC003</span></span></td>
<td><span data-ttu-id="8e8bf-583">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="8e8bf-583">Assembly</span></span></td>
<td><span data-ttu-id="8e8bf-584">65</span><span class="sxs-lookup"><span data-stu-id="8e8bf-584">65</span></span></td>
<td><span data-ttu-id="8e8bf-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="8e8bf-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="8e8bf-586">5,297.69</span></span></td>
<td><span data-ttu-id="8e8bf-587">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-588">CC004</span><span class="sxs-lookup"><span data-stu-id="8e8bf-588">CC004</span></span></td>
<td><span data-ttu-id="8e8bf-589">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-589">Packaging</span></span></td>
<td><span data-ttu-id="8e8bf-590">35</span><span class="sxs-lookup"><span data-stu-id="8e8bf-590">35</span></span></td>
<td><span data-ttu-id="8e8bf-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="8e8bf-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="8e8bf-592">2,852.60</span></span></td>
<td><span data-ttu-id="8e8bf-593">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8e8bf-594">Seuraavassa taulukossa näytetään tulos, kun Kokoonpanopalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="8e8bf-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8e8bf-595">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-595">Cost object</span></span></th>
<th><span data-ttu-id="8e8bf-596">Suuruus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-596">Magnitude</span></span></th>
<th><span data-ttu-id="8e8bf-597">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="8e8bf-597">Allocation factor</span></span></th>
<th><span data-ttu-id="8e8bf-598">Summa</span><span class="sxs-lookup"><span data-stu-id="8e8bf-598">Amount</span></span></th>
<th><span data-ttu-id="8e8bf-599">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="8e8bf-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-600">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-600">Prod 1</span></span></td>
<td><span data-ttu-id="8e8bf-601">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-601">Product 1</span></span></td>
<td><span data-ttu-id="8e8bf-602">60</span><span class="sxs-lookup"><span data-stu-id="8e8bf-602">60</span></span></td>
<td><span data-ttu-id="8e8bf-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="8e8bf-604">535.31</span><span class="sxs-lookup"><span data-stu-id="8e8bf-604">535.31</span></span></td>
<td><span data-ttu-id="8e8bf-605">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-606">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-606">Prod 2</span></span></td>
<td><span data-ttu-id="8e8bf-607">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-607">Product 2</span></span></td>
<td><span data-ttu-id="8e8bf-608">20</span><span class="sxs-lookup"><span data-stu-id="8e8bf-608">20</span></span></td>
<td><span data-ttu-id="8e8bf-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="8e8bf-610">178.44</span><span class="sxs-lookup"><span data-stu-id="8e8bf-610">178.44</span></span></td>
<td><span data-ttu-id="8e8bf-611">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-612">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-612">Prod 1</span></span></td>
<td><span data-ttu-id="8e8bf-613">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-613">Product 1</span></span></td>
<td><span data-ttu-id="8e8bf-614">60</span><span class="sxs-lookup"><span data-stu-id="8e8bf-614">60</span></span></td>
<td><span data-ttu-id="8e8bf-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="8e8bf-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="8e8bf-616">4,487.12</span></span></td>
<td><span data-ttu-id="8e8bf-617">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-618">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-618">Prod 2</span></span></td>
<td><span data-ttu-id="8e8bf-619">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-619">Product 2</span></span></td>
<td><span data-ttu-id="8e8bf-620">20</span><span class="sxs-lookup"><span data-stu-id="8e8bf-620">20</span></span></td>
<td><span data-ttu-id="8e8bf-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="8e8bf-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="8e8bf-622">1,495.71</span></span></td>
<td><span data-ttu-id="8e8bf-623">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8e8bf-624">Seuraavassa taulukossa näytetään tulos, kun Pakkauspalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="8e8bf-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8e8bf-625">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-625">Cost object</span></span></th>
<th><span data-ttu-id="8e8bf-626">Suuruus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-626">Magnitude</span></span></th>
<th><span data-ttu-id="8e8bf-627">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="8e8bf-627">Allocation factor</span></span></th>
<th><span data-ttu-id="8e8bf-628">Summa</span><span class="sxs-lookup"><span data-stu-id="8e8bf-628">Amount</span></span></th>
<th><span data-ttu-id="8e8bf-629">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="8e8bf-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-630">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-630">Prod 1</span></span></td>
<td><span data-ttu-id="8e8bf-631">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-631">Product 1</span></span></td>
<td><span data-ttu-id="8e8bf-632">80</span><span class="sxs-lookup"><span data-stu-id="8e8bf-632">80</span></span></td>
<td><span data-ttu-id="8e8bf-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="8e8bf-634">241.05</span><span class="sxs-lookup"><span data-stu-id="8e8bf-634">241.05</span></span></td>
<td><span data-ttu-id="8e8bf-635">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-636">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-636">Prod 2</span></span></td>
<td><span data-ttu-id="8e8bf-637">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-637">Product 2</span></span></td>
<td><span data-ttu-id="8e8bf-638">15</span><span class="sxs-lookup"><span data-stu-id="8e8bf-638">15</span></span></td>
<td><span data-ttu-id="8e8bf-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="8e8bf-640">45.20</span><span class="sxs-lookup"><span data-stu-id="8e8bf-640">45.20</span></span></td>
<td><span data-ttu-id="8e8bf-641">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-642">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-642">Prod 1</span></span></td>
<td><span data-ttu-id="8e8bf-643">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-643">Product 1</span></span></td>
<td><span data-ttu-id="8e8bf-644">80</span><span class="sxs-lookup"><span data-stu-id="8e8bf-644">80</span></span></td>
<td><span data-ttu-id="8e8bf-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="8e8bf-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="8e8bf-646">2,507.09</span></span></td>
<td><span data-ttu-id="8e8bf-647">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-648">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-648">Prod 2</span></span></td>
<td><span data-ttu-id="8e8bf-649">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-649">Product 2</span></span></td>
<td><span data-ttu-id="8e8bf-650">15</span><span class="sxs-lookup"><span data-stu-id="8e8bf-650">15</span></span></td>
<td><span data-ttu-id="8e8bf-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="8e8bf-652">470.08</span><span class="sxs-lookup"><span data-stu-id="8e8bf-652">470.08</span></span></td>
<td><span data-ttu-id="8e8bf-653">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8e8bf-654">Kirjauskansioviennit (kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="8e8bf-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8e8bf-655">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="8e8bf-655">Journal</span></span></th>
<th><span data-ttu-id="8e8bf-656">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="8e8bf-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8e8bf-657">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="8e8bf-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8e8bf-658">Versio</span><span class="sxs-lookup"><span data-stu-id="8e8bf-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-659">00004</span><span class="sxs-lookup"><span data-stu-id="8e8bf-659">00004</span></span></td>
<td><span data-ttu-id="8e8bf-660">Kustannusten kohdistuskirjauskansio</span><span class="sxs-lookup"><span data-stu-id="8e8bf-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="8e8bf-661">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="8e8bf-661">Fiscal</span></span></td>
<td><span data-ttu-id="8e8bf-662">2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-662">2017</span></span></td>
<td><span data-ttu-id="8e8bf-663">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-663">Period 1</span></span></td>
<td><span data-ttu-id="8e8bf-664">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="8e8bf-665">Kirjauskansion rivit</span><span class="sxs-lookup"><span data-stu-id="8e8bf-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8e8bf-666">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="8e8bf-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8e8bf-667">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8e8bf-668">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="8e8bf-668">Cost element</span></span></th>
<th><span data-ttu-id="8e8bf-669">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="8e8bf-669">Cost behavior</span></span></th>
<th><span data-ttu-id="8e8bf-670">Summa</span><span class="sxs-lookup"><span data-stu-id="8e8bf-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-671">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="8e8bf-672">CC001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-672">CC001</span></span></td>
<td><span data-ttu-id="8e8bf-673">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="8e8bf-673">HR</span></span></td>
<td><span data-ttu-id="8e8bf-674">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-674">10001</span></span></td>
<td><span data-ttu-id="8e8bf-675">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-675">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-676">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-676">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-677">500,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-678">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="8e8bf-679">CC001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-679">CC001</span></span></td>
<td><span data-ttu-id="8e8bf-680">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="8e8bf-680">HR</span></span></td>
<td><span data-ttu-id="8e8bf-681">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-681">10001</span></span></td>
<td><span data-ttu-id="8e8bf-682">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-682">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-683">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-683">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="8e8bf-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-685">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="8e8bf-686">CC002</span><span class="sxs-lookup"><span data-stu-id="8e8bf-686">CC002</span></span></td>
<td><span data-ttu-id="8e8bf-687">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="8e8bf-687">Finance</span></span></td>
<td><span data-ttu-id="8e8bf-688">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-688">10001</span></span></td>
<td><span data-ttu-id="8e8bf-689">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-689">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-690">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-690">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-691">675.00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-692">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="8e8bf-693">CC002</span><span class="sxs-lookup"><span data-stu-id="8e8bf-693">CC002</span></span></td>
<td><span data-ttu-id="8e8bf-694">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="8e8bf-694">Finance</span></span></td>
<td><span data-ttu-id="8e8bf-695">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-695">10001</span></span></td>
<td><span data-ttu-id="8e8bf-696">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-696">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-697">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-697">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="8e8bf-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-699">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="8e8bf-700">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-700">CC003</span></span></td>
<td><span data-ttu-id="8e8bf-701">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="8e8bf-701">Assembly</span></span></td>
<td><span data-ttu-id="8e8bf-702">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-702">10001</span></span></td>
<td><span data-ttu-id="8e8bf-703">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-703">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-704">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-704">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-705">713.75</span><span class="sxs-lookup"><span data-stu-id="8e8bf-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-706">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="8e8bf-707">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-707">CC003</span></span></td>
<td><span data-ttu-id="8e8bf-708">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="8e8bf-708">Assembly</span></span></td>
<td><span data-ttu-id="8e8bf-709">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-709">10001</span></span></td>
<td><span data-ttu-id="8e8bf-710">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-710">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-711">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-711">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="8e8bf-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-713">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="8e8bf-714">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-714">CC003</span></span></td>
<td><span data-ttu-id="8e8bf-715">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-715">Packaging</span></span></td>
<td><span data-ttu-id="8e8bf-716">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-716">10001</span></span></td>
<td><span data-ttu-id="8e8bf-717">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-717">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-718">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-718">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-719">286.25</span><span class="sxs-lookup"><span data-stu-id="8e8bf-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-720">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="8e8bf-721">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-721">CC003</span></span></td>
<td><span data-ttu-id="8e8bf-722">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-722">Packaging</span></span></td>
<td><span data-ttu-id="8e8bf-723">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-723">10001</span></span></td>
<td><span data-ttu-id="8e8bf-724">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-724">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-725">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-725">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="8e8bf-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-727">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="8e8bf-728">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-728">Prod 1</span></span></td>
<td><span data-ttu-id="8e8bf-729">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-729">Product 1</span></span></td>
<td><span data-ttu-id="8e8bf-730">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-730">10001</span></span></td>
<td><span data-ttu-id="8e8bf-731">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-731">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-732">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-732">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-733">776.36</span><span class="sxs-lookup"><span data-stu-id="8e8bf-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-734">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="8e8bf-735">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-735">Prod 1</span></span></td>
<td><span data-ttu-id="8e8bf-736">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-736">Product 1</span></span></td>
<td><span data-ttu-id="8e8bf-737">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-737">10001</span></span></td>
<td><span data-ttu-id="8e8bf-738">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-738">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-739">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-739">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="8e8bf-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-741">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="8e8bf-742">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-742">Prod 2</span></span></td>
<td><span data-ttu-id="8e8bf-743">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-743">Product 1</span></span></td>
<td><span data-ttu-id="8e8bf-744">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-744">10001</span></span></td>
<td><span data-ttu-id="8e8bf-745">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-745">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-746">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-746">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-747">223.64</span><span class="sxs-lookup"><span data-stu-id="8e8bf-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-748">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="8e8bf-749">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-749">Prod 2</span></span></td>
<td><span data-ttu-id="8e8bf-750">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-750">Product 1</span></span></td>
<td><span data-ttu-id="8e8bf-751">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-751">10001</span></span></td>
<td><span data-ttu-id="8e8bf-752">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-752">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-753">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-753">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="8e8bf-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8e8bf-755">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="8e8bf-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8e8bf-756">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8e8bf-757">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="8e8bf-757">Cost element</span></span></th>
<th><span data-ttu-id="8e8bf-758">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="8e8bf-758">Cost behavior</span></span></th>
<th><span data-ttu-id="8e8bf-759">Summa</span><span class="sxs-lookup"><span data-stu-id="8e8bf-759">Amount</span></span></th>
<th><span data-ttu-id="8e8bf-760">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="8e8bf-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e8bf-761">CC001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-761">CC001</span></span></td>
<td><span data-ttu-id="8e8bf-762">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="8e8bf-762">HR</span></span></td>
<td><span data-ttu-id="8e8bf-763">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-763">10001</span></span></td>
<td><span data-ttu-id="8e8bf-764">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-764">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-765">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-765">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-766">-500.00</span></span></td>
<td><span data-ttu-id="8e8bf-767">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-768">CC002</span><span class="sxs-lookup"><span data-stu-id="8e8bf-768">CC002</span></span></td>
<td><span data-ttu-id="8e8bf-769">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="8e8bf-769">Finance</span></span></td>
<td><span data-ttu-id="8e8bf-770">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-770">10001</span></span></td>
<td><span data-ttu-id="8e8bf-771">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-771">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-772">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-772">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-773">175.00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-773">175.00</span></span></td>
<td><span data-ttu-id="8e8bf-774">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-775">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-775">CC003</span></span></td>
<td><span data-ttu-id="8e8bf-776">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="8e8bf-776">Assembly</span></span></td>
<td><span data-ttu-id="8e8bf-777">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-777">10001</span></span></td>
<td><span data-ttu-id="8e8bf-778">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-778">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-779">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-779">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-780">275.00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-780">275.00</span></span></td>
<td><span data-ttu-id="8e8bf-781">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-782">CC004</span><span class="sxs-lookup"><span data-stu-id="8e8bf-782">CC004</span></span></td>
<td><span data-ttu-id="8e8bf-783">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-783">Packaging</span></span></td>
<td><span data-ttu-id="8e8bf-784">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-784">10001</span></span></td>
<td><span data-ttu-id="8e8bf-785">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-785">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-786">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-786">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-787">50,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-787">50,00</span></span></td>
<td><span data-ttu-id="8e8bf-788">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-789">CC001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-789">CC001</span></span></td>
<td><span data-ttu-id="8e8bf-790">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="8e8bf-790">HR</span></span></td>
<td><span data-ttu-id="8e8bf-791">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-791">10001</span></span></td>
<td><span data-ttu-id="8e8bf-792">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-792">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-793">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-793">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="8e8bf-794">-1,245.71</span></span></td>
<td><span data-ttu-id="8e8bf-795">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-796">CC002</span><span class="sxs-lookup"><span data-stu-id="8e8bf-796">CC002</span></span></td>
<td><span data-ttu-id="8e8bf-797">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="8e8bf-797">Finance</span></span></td>
<td><span data-ttu-id="8e8bf-798">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-798">10001</span></span></td>
<td><span data-ttu-id="8e8bf-799">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-799">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-800">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-800">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-801">436.00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-801">436.00</span></span></td>
<td><span data-ttu-id="8e8bf-802">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-803">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-803">CC003</span></span></td>
<td><span data-ttu-id="8e8bf-804">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="8e8bf-804">Assembly</span></span></td>
<td><span data-ttu-id="8e8bf-805">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-805">10001</span></span></td>
<td><span data-ttu-id="8e8bf-806">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-806">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-807">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-807">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-808">685.14</span><span class="sxs-lookup"><span data-stu-id="8e8bf-808">685.14</span></span></td>
<td><span data-ttu-id="8e8bf-809">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-810">CC004</span><span class="sxs-lookup"><span data-stu-id="8e8bf-810">CC004</span></span></td>
<td><span data-ttu-id="8e8bf-811">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-811">Packaging</span></span></td>
<td><span data-ttu-id="8e8bf-812">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-812">10001</span></span></td>
<td><span data-ttu-id="8e8bf-813">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-813">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-814">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-814">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-815">124.57</span><span class="sxs-lookup"><span data-stu-id="8e8bf-815">124.57</span></span></td>
<td><span data-ttu-id="8e8bf-816">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-817">CC002</span><span class="sxs-lookup"><span data-stu-id="8e8bf-817">CC002</span></span></td>
<td><span data-ttu-id="8e8bf-818">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="8e8bf-818">Finance</span></span></td>
<td><span data-ttu-id="8e8bf-819">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-819">10001</span></span></td>
<td><span data-ttu-id="8e8bf-820">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-820">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-821">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-821">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-822">-675.00</span></span></td>
<td><span data-ttu-id="8e8bf-823">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-824">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-824">CC003</span></span></td>
<td><span data-ttu-id="8e8bf-825">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="8e8bf-825">Assembly</span></span></td>
<td><span data-ttu-id="8e8bf-826">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-826">10001</span></span></td>
<td><span data-ttu-id="8e8bf-827">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-827">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-828">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-828">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-829">438.75</span><span class="sxs-lookup"><span data-stu-id="8e8bf-829">438.75</span></span></td>
<td><span data-ttu-id="8e8bf-830">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-831">CC004</span><span class="sxs-lookup"><span data-stu-id="8e8bf-831">CC004</span></span></td>
<td><span data-ttu-id="8e8bf-832">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-832">Packaging</span></span></td>
<td><span data-ttu-id="8e8bf-833">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-833">10001</span></span></td>
<td><span data-ttu-id="8e8bf-834">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-834">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-835">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-835">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-836">236.25</span><span class="sxs-lookup"><span data-stu-id="8e8bf-836">236.25</span></span></td>
<td><span data-ttu-id="8e8bf-837">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-838">CC002</span><span class="sxs-lookup"><span data-stu-id="8e8bf-838">CC002</span></span></td>
<td><span data-ttu-id="8e8bf-839">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="8e8bf-839">Finance</span></span></td>
<td><span data-ttu-id="8e8bf-840">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-840">10001</span></span></td>
<td><span data-ttu-id="8e8bf-841">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-841">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-842">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-842">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="8e8bf-843">-8,150.29</span></span></td>
<td><span data-ttu-id="8e8bf-844">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-845">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-845">CC003</span></span></td>
<td><span data-ttu-id="8e8bf-846">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="8e8bf-846">Assembly</span></span></td>
<td><span data-ttu-id="8e8bf-847">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-847">10001</span></span></td>
<td><span data-ttu-id="8e8bf-848">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-848">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-849">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-849">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="8e8bf-850">5,297.69</span></span></td>
<td><span data-ttu-id="8e8bf-851">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-852">CC004</span><span class="sxs-lookup"><span data-stu-id="8e8bf-852">CC004</span></span></td>
<td><span data-ttu-id="8e8bf-853">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-853">Packaging</span></span></td>
<td><span data-ttu-id="8e8bf-854">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-854">10001</span></span></td>
<td><span data-ttu-id="8e8bf-855">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-855">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-856">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-856">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="8e8bf-857">2,852.60</span></span></td>
<td><span data-ttu-id="8e8bf-858">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-859">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-859">CC003</span></span></td>
<td><span data-ttu-id="8e8bf-860">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="8e8bf-860">Assembly</span></span></td>
<td><span data-ttu-id="8e8bf-861">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-861">10001</span></span></td>
<td><span data-ttu-id="8e8bf-862">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-862">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-863">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-863">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="8e8bf-864">-713.75</span></span></td>
<td><span data-ttu-id="8e8bf-865">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-866">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-866">Prod 1</span></span></td>
<td><span data-ttu-id="8e8bf-867">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-867">Product 1</span></span></td>
<td><span data-ttu-id="8e8bf-868">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-868">10001</span></span></td>
<td><span data-ttu-id="8e8bf-869">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-869">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-870">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-870">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-871">535.31</span><span class="sxs-lookup"><span data-stu-id="8e8bf-871">535.31</span></span></td>
<td><span data-ttu-id="8e8bf-872">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-873">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-873">Prod 2</span></span></td>
<td><span data-ttu-id="8e8bf-874">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-874">Product 2</span></span></td>
<td><span data-ttu-id="8e8bf-875">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-875">10001</span></span></td>
<td><span data-ttu-id="8e8bf-876">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-876">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-877">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-877">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-878">178.44</span><span class="sxs-lookup"><span data-stu-id="8e8bf-878">178.44</span></span></td>
<td><span data-ttu-id="8e8bf-879">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-880">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-880">CC003</span></span></td>
<td><span data-ttu-id="8e8bf-881">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="8e8bf-881">Assembly</span></span></td>
<td><span data-ttu-id="8e8bf-882">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-882">10001</span></span></td>
<td><span data-ttu-id="8e8bf-883">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-883">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-884">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-884">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="8e8bf-885">-5,982.83</span></span></td>
<td><span data-ttu-id="8e8bf-886">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-887">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-887">Prod 1</span></span></td>
<td><span data-ttu-id="8e8bf-888">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-888">Product 1</span></span></td>
<td><span data-ttu-id="8e8bf-889">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-889">10001</span></span></td>
<td><span data-ttu-id="8e8bf-890">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-890">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-891">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-891">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="8e8bf-892">4,487.12</span></span></td>
<td><span data-ttu-id="8e8bf-893">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-894">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-894">Prod 2</span></span></td>
<td><span data-ttu-id="8e8bf-895">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-895">Product 2</span></span></td>
<td><span data-ttu-id="8e8bf-896">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-896">10001</span></span></td>
<td><span data-ttu-id="8e8bf-897">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-897">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-898">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-898">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="8e8bf-899">1,495.71</span></span></td>
<td><span data-ttu-id="8e8bf-900">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-901">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-901">CC003</span></span></td>
<td><span data-ttu-id="8e8bf-902">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="8e8bf-902">Assembly</span></span></td>
<td><span data-ttu-id="8e8bf-903">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-903">10001</span></span></td>
<td><span data-ttu-id="8e8bf-904">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-904">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-905">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-905">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="8e8bf-906">-286.25</span></span></td>
<td><span data-ttu-id="8e8bf-907">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-908">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-908">Prod 1</span></span></td>
<td><span data-ttu-id="8e8bf-909">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-909">Product 1</span></span></td>
<td><span data-ttu-id="8e8bf-910">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-910">10001</span></span></td>
<td><span data-ttu-id="8e8bf-911">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-911">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-912">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-912">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-913">241.05</span><span class="sxs-lookup"><span data-stu-id="8e8bf-913">241.05</span></span></td>
<td><span data-ttu-id="8e8bf-914">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-915">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-915">Prod 2</span></span></td>
<td><span data-ttu-id="8e8bf-916">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-916">Product 2</span></span></td>
<td><span data-ttu-id="8e8bf-917">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-917">10001</span></span></td>
<td><span data-ttu-id="8e8bf-918">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-918">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-919">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-919">Fixed cost</span></span></td>
<td><span data-ttu-id="8e8bf-920">45.20</span><span class="sxs-lookup"><span data-stu-id="8e8bf-920">45.20</span></span></td>
<td><span data-ttu-id="8e8bf-921">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-922">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-922">CC003</span></span></td>
<td><span data-ttu-id="8e8bf-923">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="8e8bf-923">Assembly</span></span></td>
<td><span data-ttu-id="8e8bf-924">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-924">10001</span></span></td>
<td><span data-ttu-id="8e8bf-925">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-925">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-926">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-926">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-927">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="8e8bf-927">-2,977.17</span></span></td>
<td><span data-ttu-id="8e8bf-928">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-929">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-929">Prod 1</span></span></td>
<td><span data-ttu-id="8e8bf-930">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-930">Product 1</span></span></td>
<td><span data-ttu-id="8e8bf-931">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-931">10001</span></span></td>
<td><span data-ttu-id="8e8bf-932">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-932">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-933">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-933">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="8e8bf-934">2,507.09</span></span></td>
<td><span data-ttu-id="8e8bf-935">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e8bf-936">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-936">Prod 2</span></span></td>
<td><span data-ttu-id="8e8bf-937">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-937">Product 2</span></span></td>
<td><span data-ttu-id="8e8bf-938">10 001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-938">10001</span></span></td>
<td><span data-ttu-id="8e8bf-939">Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-939">Electricity</span></span></td>
<td><span data-ttu-id="8e8bf-940">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-940">Variable cost</span></span></td>
<td><span data-ttu-id="8e8bf-941">470.08</span><span class="sxs-lookup"><span data-stu-id="8e8bf-941">470.08</span></span></td>
<td><span data-ttu-id="8e8bf-942">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="8e8bf-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="8e8bf-943">Johtopäätökset</span><span class="sxs-lookup"><span data-stu-id="8e8bf-943">Conclusion</span></span>
<span data-ttu-id="8e8bf-944">Kirjanpidossa kirjataan tyhjään kustannuspaikkatunnukseen sähkökustannus arvolla 10 000,00.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="8e8bf-945">Tämän ansiosta kustannuslaskijat tietävät, että kustannus on kohdistettava.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="8e8bf-946">Kustannukset virtaavat kirjanpidossa organisaation yksiköiden ja tasojen läpi käytössä olevien käytäntöjen ja sääntöjen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="8e8bf-947">Kukin kustannus on liitetty kustannusperusteeseen, joka sisältää parhaan arvion kustannusten kohdistuksesta.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="8e8bf-948">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="8e8bf-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="8e8bf-949">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="8e8bf-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="8e8bf-950">Yhteensä</span><span class="sxs-lookup"><span data-stu-id="8e8bf-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8e8bf-951">CC099</span><span class="sxs-lookup"><span data-stu-id="8e8bf-951">CC099</span></span></th>
<th><span data-ttu-id="8e8bf-952">CC001</span><span class="sxs-lookup"><span data-stu-id="8e8bf-952">CC001</span></span></th>
<th><span data-ttu-id="8e8bf-953">CC002</span><span class="sxs-lookup"><span data-stu-id="8e8bf-953">CC002</span></span></th>
<th><span data-ttu-id="8e8bf-954">CC003</span><span class="sxs-lookup"><span data-stu-id="8e8bf-954">CC003</span></span></th>
<th><span data-ttu-id="8e8bf-955">CC004</span><span class="sxs-lookup"><span data-stu-id="8e8bf-955">CC004</span></span></th>
<th><span data-ttu-id="8e8bf-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-956">Proj 1</span></span></th>
<th><span data-ttu-id="8e8bf-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-957">Proj 2</span></span></th>
<th><span data-ttu-id="8e8bf-958">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="8e8bf-958">Prod 1</span></span></th>
<th><span data-ttu-id="8e8bf-959">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="8e8bf-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="8e8bf-960">10001 Sähkö</span><span class="sxs-lookup"><span data-stu-id="8e8bf-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="8e8bf-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="8e8bf-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="8e8bf-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="8e8bf-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="8e8bf-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="8e8bf-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="8e8bf-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="8e8bf-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="8e8bf-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="8e8bf-970">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="8e8bf-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-971">0,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="8e8bf-972">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="8e8bf-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-973">0,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-974">0,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-975">0,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-976">0,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-977">0,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-978">776.36</span><span class="sxs-lookup"><span data-stu-id="8e8bf-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-979">223.64</span><span class="sxs-lookup"><span data-stu-id="8e8bf-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="8e8bf-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="8e8bf-981">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="8e8bf-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-982">000</span><span class="sxs-lookup"><span data-stu-id="8e8bf-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-983">0,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-984">0,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-985">0,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-986">0,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-987">30,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-988">10,00</span><span class="sxs-lookup"><span data-stu-id="8e8bf-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="8e8bf-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="8e8bf-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8e8bf-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="8e8bf-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="8e8bf-992">Tässä ohjeaiheessa esitellään, miten ensisijainen kustannuselementti, 10001 Sähkö, virtaa kustannusobjektien läpi.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="8e8bf-993">Tästä syystä tämä yleiskustannus kohdistetaan organisaation alimmalle tasolle.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="8e8bf-994">Toisin sanoen alimman tason kustannusobjektit kantavat kustannuksen.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="8e8bf-995">Jos tarvitset visuaalisen näkymän kustannuksen virrasta kustannusobjektien välillä, voit käyttää kustannuksen koontikäytäntösääntöjä kustannusvirran visualisointiin.</span><span class="sxs-lookup"><span data-stu-id="8e8bf-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="8e8bf-996">Lisätietoja on kohdassa [Kustannusten koontikäytäntö ja yleiskustannuslaskenta](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="8e8bf-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]