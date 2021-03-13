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
ms.openlocfilehash: d60248f2bd6774b2e9afdb3632b6eb31d67349ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009515"
---
# <a name="overhead-calculation"></a><span data-ttu-id="7792c-103">Yleiskustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="7792c-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7792c-104">Tässä aiheessa kuvataan tyypillinen yleiskustannusten laskenta- ja kohdistusprosessi.</span><span class="sxs-lookup"><span data-stu-id="7792c-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="7792c-105">Sanaston määritelmä</span><span class="sxs-lookup"><span data-stu-id="7792c-105">Term definition</span></span>
---------------

<span data-ttu-id="7792c-106">Yleiskustannukset ovat yrityksen toiminnasta syntyviä kustannuksia, joita ei voi suoraan liittää mihinkään tiettyyn liiketoiminnan tehtävään, tuotteeseen tai palveluun.</span><span class="sxs-lookup"><span data-stu-id="7792c-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="7792c-107">Yleiskustannukset ovat tärkeä tuki voittoa tuottavien tehtävien luonnissa.</span><span class="sxs-lookup"><span data-stu-id="7792c-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="7792c-108">Seuraavassa on joitakin esimerkkejä yleiskustannuksista:</span><span class="sxs-lookup"><span data-stu-id="7792c-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="7792c-109">Vuokra</span><span class="sxs-lookup"><span data-stu-id="7792c-109">Rent</span></span>
-   <span data-ttu-id="7792c-110">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-110">Electricity</span></span>
-   <span data-ttu-id="7792c-111">Hallinnon palkat</span><span class="sxs-lookup"><span data-stu-id="7792c-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="7792c-112">Yleiskustannuslaskennan yleiskuva</span><span class="sxs-lookup"><span data-stu-id="7792c-112">Overhead calculation overview</span></span>
<span data-ttu-id="7792c-113">Yleiskustannusten laskenta suorittaa kustannuslaskennan käytännöt oikeassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="7792c-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="7792c-114">Yleiskustannusten laskennan voi suorittaa useita kertoja samalle tilikaudelle, jos kustannuslaskennan käytännöt ovat muuttuneet tai erityisiä virheitä on havaittu.</span><span class="sxs-lookup"><span data-stu-id="7792c-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="7792c-115">Kukin laskenta-ajo tallennetaan ja kullekin annetaan yksilöllinen versiotunnus, jonka avulla eri laskenta-ajoja voi verrata toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="7792c-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="7792c-116">Yleiskustannusten laskenta luo kustannustapahtumia, joille annetaan kirjauspäivä.</span><span class="sxs-lookup"><span data-stu-id="7792c-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="7792c-117">Kirjauspäivä vastaa laskennassa käytettyä tilikauden päättymispäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="7792c-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="7792c-118">Yksilöivä versiotunnus sisältää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="7792c-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="7792c-119">Versiotyyppi</span><span class="sxs-lookup"><span data-stu-id="7792c-119">Version type</span></span>
-   <span data-ttu-id="7792c-120">Päivämäärä ja aika</span><span class="sxs-lookup"><span data-stu-id="7792c-120">Date and time</span></span>
-   <span data-ttu-id="7792c-121">Kustannuslaskennan kirjanpito</span><span class="sxs-lookup"><span data-stu-id="7792c-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="7792c-122">Tilikausi </span><span class="sxs-lookup"><span data-stu-id="7792c-122">Fiscal year</span></span>
-   <span data-ttu-id="7792c-123">Tilikausi  </span><span class="sxs-lookup"><span data-stu-id="7792c-123">Fiscal period</span></span>

<span data-ttu-id="7792c-124">Yleiskustannusten laskenta ajetaan versiosta riippumattomana.</span><span class="sxs-lookup"><span data-stu-id="7792c-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="7792c-125">Voit siis laskea budjetin version ennen todellista versiota.</span><span class="sxs-lookup"><span data-stu-id="7792c-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="7792c-126">Yleiskustannusten laskenta koostuu neljästä vaiheesta, jotka esitellään seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="7792c-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="7792c-127">Kussakin vaiheessa luodaan kirjauskansion otsikko, jolla on kirjauskansiovientejä.</span><span class="sxs-lookup"><span data-stu-id="7792c-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="7792c-128">Tämä kirjauskansion otsikko säilyttää kunkin laskentavaiheen syöttötiedot.</span><span class="sxs-lookup"><span data-stu-id="7792c-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="7792c-129">Käytännöt ja säännöt ajetaan kullekin kirjauskansion riville, ja tuloksena luodaan kustannustapahtumia.</span><span class="sxs-lookup"><span data-stu-id="7792c-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="7792c-130">Tämän ansiosta kaikki laskutoimitukset ovat täysin jäljitettävissä.</span><span class="sxs-lookup"><span data-stu-id="7792c-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="7792c-131">[![Yleiskustannuslaskenta](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="7792c-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="7792c-132">Laske ja kohdista sähkön yleiskustannukset</span><span class="sxs-lookup"><span data-stu-id="7792c-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="7792c-133">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="7792c-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="7792c-134">Tarkka johdon näkymä ei täten ole saatavilla kustannuslaskennassa.</span><span class="sxs-lookup"><span data-stu-id="7792c-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="7792c-135">Jotta kustannuslaskenta tarjoaisi oikean johdon näkymän kaikista organisaation yksiköistä ja tasoista, kustannusten on virrattava organisaation yksiköiden läpi.</span><span class="sxs-lookup"><span data-stu-id="7792c-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="7792c-136">Tämän virran on perustuttava joko tarkkaan tietoon kulutuksesta tai perusteltuun arvioon.</span><span class="sxs-lookup"><span data-stu-id="7792c-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="7792c-137">Sähkökustannukset voi kirjata kirjanpitoon seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="7792c-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7792c-138">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="7792c-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7792c-139">Kustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="7792c-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="7792c-140">Päätili</span><span class="sxs-lookup"><span data-stu-id="7792c-140">Main account</span></span></th>
<th><span data-ttu-id="7792c-141">Summa kirjanpitovaluuttana</span><span class="sxs-lookup"><span data-stu-id="7792c-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-142">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="7792c-143">CC099</span><span class="sxs-lookup"><span data-stu-id="7792c-143">CC099</span></span></td>
<td><span data-ttu-id="7792c-144">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="7792c-144">Default cost center</span></span></td>
<td><span data-ttu-id="7792c-145">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-145">10001</span></span></td>
<td><span data-ttu-id="7792c-146">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-146">Electricity</span></span></td>
<td><span data-ttu-id="7792c-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="7792c-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="7792c-148">Vaihe 1: Käsittele kustannustoiminnan laskenta</span><span class="sxs-lookup"><span data-stu-id="7792c-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="7792c-149">Kun kustannustapahtumat tuodaan lähdetiedoista, niille asetetaan kustannuslaskennassa oletusarvoisesti **Luokittelematon** -kustannustoimintaluokka.</span><span class="sxs-lookup"><span data-stu-id="7792c-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="7792c-150">Voit luokitella kustannustapahtumia uudelleen **kiinteäksi kustannukseksi** tai **muuttuvaksi kustannukseksi** kustannustoiminnan käytäntösäännöillä.</span><span class="sxs-lookup"><span data-stu-id="7792c-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="7792c-151">Määritä kustannustoiminnan sääntö</span><span class="sxs-lookup"><span data-stu-id="7792c-151">Define the cost behavior rule</span></span>

<span data-ttu-id="7792c-152">Joissain tapauksissa osa kustannuksesta on kiinteä ja loppuosa perustuu kulutukseen.</span><span class="sxs-lookup"><span data-stu-id="7792c-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="7792c-153">Sähkölaskut sopivat usein tähän määritelmään.</span><span class="sxs-lookup"><span data-stu-id="7792c-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="7792c-154">Maksat ensin määrätyn, kiinteän maksun, jonka lisäksi maksat kulutuksesta kilowattitunteina (kWh).</span><span class="sxs-lookup"><span data-stu-id="7792c-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="7792c-155">Jos kiinteä maksu on esimerkiksi 1 000,00, kustannustoiminnan sääntö määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="7792c-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="7792c-156">Kiinteä määrä 1 000,00</span><span class="sxs-lookup"><span data-stu-id="7792c-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="7792c-157">0 &lt;= 1 000,00 = Kiinteä</span><span class="sxs-lookup"><span data-stu-id="7792c-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="7792c-158">1000,01 &lt; N = Muuttuva</span><span class="sxs-lookup"><span data-stu-id="7792c-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="7792c-159">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="7792c-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7792c-160">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="7792c-160">Journal</span></span></th>
<th><span data-ttu-id="7792c-161">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="7792c-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7792c-162">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="7792c-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7792c-163">Versio</span><span class="sxs-lookup"><span data-stu-id="7792c-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-164">00001</span><span class="sxs-lookup"><span data-stu-id="7792c-164">00001</span></span></td>
<td><span data-ttu-id="7792c-165">Kustannustoiminnan laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="7792c-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="7792c-166">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="7792c-166">Fiscal</span></span></td>
<td><span data-ttu-id="7792c-167">2017</span><span class="sxs-lookup"><span data-stu-id="7792c-167">2017</span></span></td>
<td><span data-ttu-id="7792c-168">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="7792c-168">Period 1</span></span></td>
<td><span data-ttu-id="7792c-169">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="7792c-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7792c-170">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="7792c-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7792c-171">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="7792c-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7792c-172">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7792c-173">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="7792c-173">Cost element</span></span></th>
<th><span data-ttu-id="7792c-174">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="7792c-174">Cost behavior</span></span></th>
<th><span data-ttu-id="7792c-175">Summa</span><span class="sxs-lookup"><span data-stu-id="7792c-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-176">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="7792c-177">CC099</span><span class="sxs-lookup"><span data-stu-id="7792c-177">CC099</span></span></td>
<td><span data-ttu-id="7792c-178">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="7792c-178">Default cost center</span></span></td>
<td><span data-ttu-id="7792c-179">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-179">10001</span></span></td>
<td><span data-ttu-id="7792c-180">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-180">Electricity</span></span></td>
<td><span data-ttu-id="7792c-181">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="7792c-181">Unclassified</span></span></td>
<td><span data-ttu-id="7792c-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="7792c-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7792c-183">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="7792c-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7792c-184">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7792c-185">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="7792c-185">Cost element</span></span></th>
<th><span data-ttu-id="7792c-186">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="7792c-186">Cost behavior</span></span></th>
<th><span data-ttu-id="7792c-187">Summa</span><span class="sxs-lookup"><span data-stu-id="7792c-187">Amount</span></span></th>
<th><span data-ttu-id="7792c-188">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="7792c-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-189">CC099</span><span class="sxs-lookup"><span data-stu-id="7792c-189">CC099</span></span></td>
<td><span data-ttu-id="7792c-190">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="7792c-190">Default cost center</span></span></td>
<td><span data-ttu-id="7792c-191">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-191">10001</span></span></td>
<td><span data-ttu-id="7792c-192">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-192">Electricity</span></span></td>
<td><span data-ttu-id="7792c-193">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="7792c-193">Unclassified</span></span></td>
<td><span data-ttu-id="7792c-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="7792c-194">10,000.00</span></span></td>
<td><span data-ttu-id="7792c-195">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-196">CC099</span><span class="sxs-lookup"><span data-stu-id="7792c-196">CC099</span></span></td>
<td><span data-ttu-id="7792c-197">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="7792c-197">Default cost center</span></span></td>
<td><span data-ttu-id="7792c-198">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-198">10001</span></span></td>
<td><span data-ttu-id="7792c-199">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-199">Electricity</span></span></td>
<td><span data-ttu-id="7792c-200">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="7792c-200">Unclassified</span></span></td>
<td><span data-ttu-id="7792c-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="7792c-201">-10,000.00</span></span></td>
<td><span data-ttu-id="7792c-202">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-203">CC099</span><span class="sxs-lookup"><span data-stu-id="7792c-203">CC099</span></span></td>
<td><span data-ttu-id="7792c-204">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="7792c-204">Default cost center</span></span></td>
<td><span data-ttu-id="7792c-205">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-205">10001</span></span></td>
<td><span data-ttu-id="7792c-206">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-206">Electricity</span></span></td>
<td><span data-ttu-id="7792c-207">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-207">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="7792c-208">1,000.00</span></span></td>
<td><span data-ttu-id="7792c-209">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-210">CC099</span><span class="sxs-lookup"><span data-stu-id="7792c-210">CC099</span></span></td>
<td><span data-ttu-id="7792c-211">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="7792c-211">Default cost center</span></span></td>
<td><span data-ttu-id="7792c-212">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-212">10001</span></span></td>
<td><span data-ttu-id="7792c-213">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-213">Electricity</span></span></td>
<td><span data-ttu-id="7792c-214">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-214">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="7792c-215">9,000.00</span></span></td>
<td><span data-ttu-id="7792c-216">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7792c-217">Lisätietoja on kohdassa [Kustannustoimintakäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="7792c-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="7792c-218">Vaihe 2: Käsittele kustannusten jaon laskenta</span><span class="sxs-lookup"><span data-stu-id="7792c-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="7792c-219">Kustannusten jakoa käytetään kustannusten jakamiseen yhdestä kustannusobjektista toiseen (tai useampaan kustannusobjektiin) määrittämällä asiaankuuluvan kohdistusperusteen.</span><span class="sxs-lookup"><span data-stu-id="7792c-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="7792c-220">Kustannusten jako ja kustannusten kohdistus eroavat toisistaan sillä, että kustannusten jako tapahtuu aina alkuperäisen kustannuksen ensisijaisen kustannuselementin tasolla.</span><span class="sxs-lookup"><span data-stu-id="7792c-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="7792c-221">Määritä kustannusten jaon sääntö</span><span class="sxs-lookup"><span data-stu-id="7792c-221">Define the cost distribution rule</span></span>

<span data-ttu-id="7792c-222">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="7792c-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="7792c-223">Kustannuslaskenta ei tarjoa tästä tarpeeksi tarkkoja tietoja.</span><span class="sxs-lookup"><span data-stu-id="7792c-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="7792c-224">Muuttuva kustannus tulisi jakaa yksittäisille kustannusobjekteille reiluin perustein.</span><span class="sxs-lookup"><span data-stu-id="7792c-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="7792c-225">Loogisin kohdistusperuste on sähkönkulutus (kWh).</span><span class="sxs-lookup"><span data-stu-id="7792c-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="7792c-226">Luodaan tilastollinen dimensionjäsen nimeltä Sähkö, johon kirjataan sähkönkulutus.</span><span class="sxs-lookup"><span data-stu-id="7792c-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="7792c-227">Oletusarvon mukaan kaikki tilastolliset dimensiojäsenet ovat käytettävissä kohdistusperusteina.</span><span class="sxs-lookup"><span data-stu-id="7792c-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7792c-228">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-228">Cost object</span></span></th>
<th><span data-ttu-id="7792c-229">kWh</span><span class="sxs-lookup"><span data-stu-id="7792c-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-230">CC001</span><span class="sxs-lookup"><span data-stu-id="7792c-230">CC001</span></span></td>
<td><span data-ttu-id="7792c-231">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="7792c-231">HR</span></span></td>
<td><span data-ttu-id="7792c-232">1 000</span><span class="sxs-lookup"><span data-stu-id="7792c-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-233">CC002</span><span class="sxs-lookup"><span data-stu-id="7792c-233">CC002</span></span></td>
<td><span data-ttu-id="7792c-234">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="7792c-234">Finance</span></span></td>
<td><span data-ttu-id="7792c-235">6,000</span><span class="sxs-lookup"><span data-stu-id="7792c-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-236">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-236">CC003</span></span></td>
<td><span data-ttu-id="7792c-237">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="7792c-237">Assembly</span></span></td>
<td><span data-ttu-id="7792c-238">0</span><span class="sxs-lookup"><span data-stu-id="7792c-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7792c-239">Seuraavassa taulukossa on esitetty tulos, kun sähkönkulutusta käytetään kohdistusperusteena muuttuville kuluille.</span><span class="sxs-lookup"><span data-stu-id="7792c-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7792c-240">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-240">Cost object</span></span></th>
<th><span data-ttu-id="7792c-241">Suuruus</span><span class="sxs-lookup"><span data-stu-id="7792c-241">Magnitude</span></span></th>
<th><span data-ttu-id="7792c-242">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="7792c-242">Allocation factor</span></span></th>
<th><span data-ttu-id="7792c-243">Summa</span><span class="sxs-lookup"><span data-stu-id="7792c-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-244">CC001</span><span class="sxs-lookup"><span data-stu-id="7792c-244">CC001</span></span></td>
<td><span data-ttu-id="7792c-245">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="7792c-245">HR</span></span></td>
<td><span data-ttu-id="7792c-246">1 000</span><span class="sxs-lookup"><span data-stu-id="7792c-246">1,000</span></span></td>
<td><span data-ttu-id="7792c-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="7792c-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7792c-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="7792c-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-249">CC002</span><span class="sxs-lookup"><span data-stu-id="7792c-249">CC002</span></span></td>
<td><span data-ttu-id="7792c-250">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="7792c-250">Finance</span></span></td>
<td><span data-ttu-id="7792c-251">6,000</span><span class="sxs-lookup"><span data-stu-id="7792c-251">6,000</span></span></td>
<td><span data-ttu-id="7792c-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="7792c-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7792c-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="7792c-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-254">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-254">CC003</span></span></td>
<td><span data-ttu-id="7792c-255">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="7792c-255">Assembly</span></span></td>
<td><span data-ttu-id="7792c-256">0</span><span class="sxs-lookup"><span data-stu-id="7792c-256">0</span></span></td>
<td><span data-ttu-id="7792c-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="7792c-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7792c-258">0,00</span><span class="sxs-lookup"><span data-stu-id="7792c-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7792c-259">Kiinteä kustannus tulisi jakaa tasaisesti yksittäisille kustannusobjekteille, jotka ovat kuluttaneet sähköä.</span><span class="sxs-lookup"><span data-stu-id="7792c-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="7792c-260">Voit käyttää sähkön tilastollista dimensiojäsentä kaavan kohdistusperusteena tämän tavoitteen saavuttamiseksi: (sähkö &gt;0,00) Seuraavassa taulukossa on esitetty tulos siitä, kun sähkönkulutus on määritetty muuttuvien kustannusten kohdistusperusteeksi.</span><span class="sxs-lookup"><span data-stu-id="7792c-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7792c-261">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-261">Cost object</span></span></th>
<th><span data-ttu-id="7792c-262">Resepti</span><span class="sxs-lookup"><span data-stu-id="7792c-262">Formula</span></span></th>
<th><span data-ttu-id="7792c-263">Suuruus</span><span class="sxs-lookup"><span data-stu-id="7792c-263">Magnitude</span></span></th>
<th><span data-ttu-id="7792c-264">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="7792c-264">Allocation factor</span></span></th>
<th><span data-ttu-id="7792c-265">Summa</span><span class="sxs-lookup"><span data-stu-id="7792c-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-266">CC001</span><span class="sxs-lookup"><span data-stu-id="7792c-266">CC001</span></span></td>
<td><span data-ttu-id="7792c-267">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="7792c-267">HR</span></span></td>
<td><span data-ttu-id="7792c-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="7792c-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7792c-269">1</span><span class="sxs-lookup"><span data-stu-id="7792c-269">1</span></span></td>
<td><span data-ttu-id="7792c-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="7792c-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7792c-271">500,00</span><span class="sxs-lookup"><span data-stu-id="7792c-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-272">CC002</span><span class="sxs-lookup"><span data-stu-id="7792c-272">CC002</span></span></td>
<td><span data-ttu-id="7792c-273">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="7792c-273">Finance</span></span></td>
<td><span data-ttu-id="7792c-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="7792c-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7792c-275">1</span><span class="sxs-lookup"><span data-stu-id="7792c-275">1</span></span></td>
<td><span data-ttu-id="7792c-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="7792c-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7792c-277">500,00</span><span class="sxs-lookup"><span data-stu-id="7792c-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-278">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-278">CC003</span></span></td>
<td><span data-ttu-id="7792c-279">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="7792c-279">Assembly</span></span></td>
<td><span data-ttu-id="7792c-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="7792c-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7792c-281">0</span><span class="sxs-lookup"><span data-stu-id="7792c-281">0</span></span></td>
<td><span data-ttu-id="7792c-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="7792c-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7792c-283">0,00</span><span class="sxs-lookup"><span data-stu-id="7792c-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="7792c-284">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="7792c-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7792c-285">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="7792c-285">Journal</span></span></th>
<th><span data-ttu-id="7792c-286">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="7792c-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7792c-287">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="7792c-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7792c-288">Versio</span><span class="sxs-lookup"><span data-stu-id="7792c-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-289">00002</span><span class="sxs-lookup"><span data-stu-id="7792c-289">00002</span></span></td>
<td><span data-ttu-id="7792c-290">Kustannusten jaon laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="7792c-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="7792c-291">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="7792c-291">Fiscal</span></span></td>
<td><span data-ttu-id="7792c-292">2017</span><span class="sxs-lookup"><span data-stu-id="7792c-292">2017</span></span></td>
<td><span data-ttu-id="7792c-293">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="7792c-293">Period 1</span></span></td>
<td><span data-ttu-id="7792c-294">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="7792c-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7792c-295">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="7792c-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7792c-296">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="7792c-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7792c-297">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7792c-298">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="7792c-298">Cost element</span></span></th>
<th><span data-ttu-id="7792c-299">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="7792c-299">Cost behavior</span></span></th>
<th><span data-ttu-id="7792c-300">Summa</span><span class="sxs-lookup"><span data-stu-id="7792c-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-301">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="7792c-302">CC099</span><span class="sxs-lookup"><span data-stu-id="7792c-302">CC099</span></span></td>
<td><span data-ttu-id="7792c-303">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="7792c-303">Default cost center</span></span></td>
<td><span data-ttu-id="7792c-304">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-304">10001</span></span></td>
<td><span data-ttu-id="7792c-305">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-305">Electricity</span></span></td>
<td><span data-ttu-id="7792c-306">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-306">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="7792c-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-308">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="7792c-309">CC099</span><span class="sxs-lookup"><span data-stu-id="7792c-309">CC099</span></span></td>
<td><span data-ttu-id="7792c-310">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="7792c-310">Default cost center</span></span></td>
<td><span data-ttu-id="7792c-311">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-311">10001</span></span></td>
<td><span data-ttu-id="7792c-312">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-312">Electricity</span></span></td>
<td><span data-ttu-id="7792c-313">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-313">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="7792c-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7792c-315">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="7792c-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7792c-316">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7792c-317">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="7792c-317">Cost element</span></span></th>
<th><span data-ttu-id="7792c-318">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="7792c-318">Cost behavior</span></span></th>
<th><span data-ttu-id="7792c-319">Summa</span><span class="sxs-lookup"><span data-stu-id="7792c-319">Amount</span></span></th>
<th><span data-ttu-id="7792c-320">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="7792c-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-321">CC099</span><span class="sxs-lookup"><span data-stu-id="7792c-321">CC099</span></span></td>
<td><span data-ttu-id="7792c-322">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="7792c-322">Default cost center</span></span></td>
<td><span data-ttu-id="7792c-323">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-323">10001</span></span></td>
<td><span data-ttu-id="7792c-324">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-324">Electricity</span></span></td>
<td><span data-ttu-id="7792c-325">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-325">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="7792c-326">-1,000.00</span></span></td>
<td><span data-ttu-id="7792c-327">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-328">CC001</span><span class="sxs-lookup"><span data-stu-id="7792c-328">CC001</span></span></td>
<td><span data-ttu-id="7792c-329">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="7792c-329">HR</span></span></td>
<td><span data-ttu-id="7792c-330">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-330">10001</span></span></td>
<td><span data-ttu-id="7792c-331">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-331">Electricity</span></span></td>
<td><span data-ttu-id="7792c-332">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-332">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-333">500,00</span><span class="sxs-lookup"><span data-stu-id="7792c-333">500.00</span></span></td>
<td><span data-ttu-id="7792c-334">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-335">CC002</span><span class="sxs-lookup"><span data-stu-id="7792c-335">CC002</span></span></td>
<td><span data-ttu-id="7792c-336">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="7792c-336">Finance</span></span></td>
<td><span data-ttu-id="7792c-337">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-337">10001</span></span></td>
<td><span data-ttu-id="7792c-338">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-338">Electricity</span></span></td>
<td><span data-ttu-id="7792c-339">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-339">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-340">500,00</span><span class="sxs-lookup"><span data-stu-id="7792c-340">500.00</span></span></td>
<td><span data-ttu-id="7792c-341">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-342">CC099</span><span class="sxs-lookup"><span data-stu-id="7792c-342">CC099</span></span></td>
<td><span data-ttu-id="7792c-343">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="7792c-343">Default cost center</span></span></td>
<td><span data-ttu-id="7792c-344">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-344">10001</span></span></td>
<td><span data-ttu-id="7792c-345">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-345">Electricity</span></span></td>
<td><span data-ttu-id="7792c-346">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-346">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="7792c-347">-9,000.00</span></span></td>
<td><span data-ttu-id="7792c-348">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-349">CC001</span><span class="sxs-lookup"><span data-stu-id="7792c-349">CC001</span></span></td>
<td><span data-ttu-id="7792c-350">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="7792c-350">HR</span></span></td>
<td><span data-ttu-id="7792c-351">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-351">10001</span></span></td>
<td><span data-ttu-id="7792c-352">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-352">Electricity</span></span></td>
<td><span data-ttu-id="7792c-353">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-353">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="7792c-354">1,285.71</span></span></td>
<td><span data-ttu-id="7792c-355">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-356">CC002</span><span class="sxs-lookup"><span data-stu-id="7792c-356">CC002</span></span></td>
<td><span data-ttu-id="7792c-357">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="7792c-357">Finance</span></span></td>
<td><span data-ttu-id="7792c-358">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-358">10001</span></span></td>
<td><span data-ttu-id="7792c-359">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-359">Electricity</span></span></td>
<td><span data-ttu-id="7792c-360">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-360">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="7792c-361">7,714.29</span></span></td>
<td><span data-ttu-id="7792c-362">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7792c-363">Lisätietoja on kohdassa [Jakelukäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="7792c-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="7792c-364">Vaihe 3: Käsittele yleiskustannustason laskenta</span><span class="sxs-lookup"><span data-stu-id="7792c-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="7792c-365">Yleiskustannustasolla veloitetaan yksi tai useampi määrätty kustannusobjekti.</span><span class="sxs-lookup"><span data-stu-id="7792c-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="7792c-366">Veloitus perustuu ennalta määrättyyn kustannustasoon sekä määritetyn kohdistusperusteen suuruuteen.</span><span class="sxs-lookup"><span data-stu-id="7792c-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="7792c-367">Määritä yleiskustannustaso.</span><span class="sxs-lookup"><span data-stu-id="7792c-367">Define the overhead rate</span></span>

<span data-ttu-id="7792c-368">Kustannusobjekti CC001 HR vaikuttaa joukkoon sisäisiä projekteja.</span><span class="sxs-lookup"><span data-stu-id="7792c-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="7792c-369">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon projektit.</span><span class="sxs-lookup"><span data-stu-id="7792c-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7792c-370">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-370">Cost object</span></span></th>
<th><span data-ttu-id="7792c-371">Tunnit</span><span class="sxs-lookup"><span data-stu-id="7792c-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7792c-372">Proj 1</span></span></td>
<td><span data-ttu-id="7792c-373">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="7792c-373">Project 1</span></span></td>
<td><span data-ttu-id="7792c-374">3</span><span class="sxs-lookup"><span data-stu-id="7792c-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7792c-375">Proj 2</span></span></td>
<td><span data-ttu-id="7792c-376">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="7792c-376">Project 2</span></span></td>
<td><span data-ttu-id="7792c-377">1</span><span class="sxs-lookup"><span data-stu-id="7792c-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7792c-378">Kustannusprojektien osuudelle on määritetty ennalta kustannushinta.</span><span class="sxs-lookup"><span data-stu-id="7792c-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7792c-379">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-379">Cost object</span></span></th>
<th><span data-ttu-id="7792c-380">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="7792c-380">Cost element</span></span></th>
<th><span data-ttu-id="7792c-381">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="7792c-381">Cost behavior</span></span></th>
<th><span data-ttu-id="7792c-382">Yksiköt</span><span class="sxs-lookup"><span data-stu-id="7792c-382">Units</span></span></th>
<th><span data-ttu-id="7792c-383">Osuus</span><span class="sxs-lookup"><span data-stu-id="7792c-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-384">CC001</span><span class="sxs-lookup"><span data-stu-id="7792c-384">CC001</span></span></td>
<td><span data-ttu-id="7792c-385">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="7792c-385">HR</span></span></td>
<td><span data-ttu-id="7792c-386">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-386">10001</span></span></td>
<td><span data-ttu-id="7792c-387">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-387">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-388">1</span><span class="sxs-lookup"><span data-stu-id="7792c-388">1</span></span></td>
<td><span data-ttu-id="7792c-389">10</span><span class="sxs-lookup"><span data-stu-id="7792c-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7792c-390">Seuraavassa taulukossa on esitetty tulos, kun Henkilöstöhallinnon projekteja käytetään kohdistusperusteena.</span><span class="sxs-lookup"><span data-stu-id="7792c-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7792c-391">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-391">Cost object</span></span></th>
<th><span data-ttu-id="7792c-392">Suuruus</span><span class="sxs-lookup"><span data-stu-id="7792c-392">Magnitude</span></span></th>
<th><span data-ttu-id="7792c-393">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="7792c-393">Cost element</span></span></th>
<th><span data-ttu-id="7792c-394">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="7792c-394">Allocation factor</span></span></th>
<th><span data-ttu-id="7792c-395">Summa</span><span class="sxs-lookup"><span data-stu-id="7792c-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7792c-396">Proj 1</span></span></td>
<td><span data-ttu-id="7792c-397">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="7792c-397">Project 1</span></span></td>
<td><span data-ttu-id="7792c-398">3</span><span class="sxs-lookup"><span data-stu-id="7792c-398">3</span></span></td>
<td><span data-ttu-id="7792c-399">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-399">10001</span></span></td>
<td><span data-ttu-id="7792c-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="7792c-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="7792c-401">30,00</span><span class="sxs-lookup"><span data-stu-id="7792c-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7792c-402">Proj 2</span></span></td>
<td><span data-ttu-id="7792c-403">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="7792c-403">Project 2</span></span></td>
<td><span data-ttu-id="7792c-404">1</span><span class="sxs-lookup"><span data-stu-id="7792c-404">1</span></span></td>
<td><span data-ttu-id="7792c-405">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-405">10001</span></span></td>
<td><span data-ttu-id="7792c-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="7792c-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="7792c-407">10,00</span><span class="sxs-lookup"><span data-stu-id="7792c-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="7792c-408">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="7792c-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7792c-409">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="7792c-409">Journal</span></span></th>
<th><span data-ttu-id="7792c-410">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="7792c-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7792c-411">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="7792c-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7792c-412">Versio</span><span class="sxs-lookup"><span data-stu-id="7792c-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-413">00003</span><span class="sxs-lookup"><span data-stu-id="7792c-413">00003</span></span></td>
<td><span data-ttu-id="7792c-414">Yleiskustannustason laskelman kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="7792c-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="7792c-415">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="7792c-415">Fiscal</span></span></td>
<td><span data-ttu-id="7792c-416">2017</span><span class="sxs-lookup"><span data-stu-id="7792c-416">2017</span></span></td>
<td><span data-ttu-id="7792c-417">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="7792c-417">Period 1</span></span></td>
<td><span data-ttu-id="7792c-418">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="7792c-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="7792c-419">Kirjauskansioviennit (Yleiskustannustason laskennan kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="7792c-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7792c-420">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="7792c-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7792c-421">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-421">Cost object</span></span></th>
<th><span data-ttu-id="7792c-422">Suuruus</span><span class="sxs-lookup"><span data-stu-id="7792c-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-423">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="7792c-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7792c-424">Proj 1</span></span></td>
<td><span data-ttu-id="7792c-425">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="7792c-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="7792c-426">3,00</span><span class="sxs-lookup"><span data-stu-id="7792c-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-427">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="7792c-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7792c-428">Proj 2</span></span></td>
<td><span data-ttu-id="7792c-429">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="7792c-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="7792c-430">1,00</span><span class="sxs-lookup"><span data-stu-id="7792c-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7792c-431">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="7792c-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7792c-432">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7792c-433">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="7792c-433">Cost element</span></span></th>
<th><span data-ttu-id="7792c-434">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="7792c-434">Cost behavior</span></span></th>
<th><span data-ttu-id="7792c-435">Summa</span><span class="sxs-lookup"><span data-stu-id="7792c-435">Amount</span></span></th>
<th><span data-ttu-id="7792c-436">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="7792c-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="7792c-437">CC0001</span></span></td>
<td><span data-ttu-id="7792c-438">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="7792c-438">HR</span></span></td>
<td><span data-ttu-id="7792c-439">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-439">10001</span></span></td>
<td><span data-ttu-id="7792c-440">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-440">Electricity</span></span></td>
<td><span data-ttu-id="7792c-441">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-441">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="7792c-442">-30.00</span></span></td>
<td><span data-ttu-id="7792c-443">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7792c-444">Proj 1</span></span></td>
<td><span data-ttu-id="7792c-445">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="7792c-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="7792c-446">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-446">10001</span></span></td>
<td><span data-ttu-id="7792c-447">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-447">Electricity</span></span></td>
<td><span data-ttu-id="7792c-448">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-448">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-449">30,00</span><span class="sxs-lookup"><span data-stu-id="7792c-449">30.00</span></span></td>
<td><span data-ttu-id="7792c-450">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-451">CC001</span><span class="sxs-lookup"><span data-stu-id="7792c-451">CC001</span></span></td>
<td><span data-ttu-id="7792c-452">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="7792c-452">HR</span></span></td>
<td><span data-ttu-id="7792c-453">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-453">10001</span></span></td>
<td><span data-ttu-id="7792c-454">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-454">Electricity</span></span></td>
<td><span data-ttu-id="7792c-455">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-455">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="7792c-456">-10.00</span></span></td>
<td><span data-ttu-id="7792c-457">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7792c-458">Proj 2</span></span></td>
<td><span data-ttu-id="7792c-459">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="7792c-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="7792c-460">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-460">10001</span></span></td>
<td><span data-ttu-id="7792c-461">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-461">Electricity</span></span></td>
<td><span data-ttu-id="7792c-462">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-462">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-463">10.00</span><span class="sxs-lookup"><span data-stu-id="7792c-463">10.00</span></span></td>
<td><span data-ttu-id="7792c-464">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7792c-465">Lisätietoja on kohdassa [Yleisen laskennan suorittaminen](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="7792c-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="7792c-466">Vaihe 4: Käsittele kustannusten kohdistuksen laskenta</span><span class="sxs-lookup"><span data-stu-id="7792c-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="7792c-467">Kohdistuksella kustannusobjektin saldo liitetään toisiin kustannusobjekteihin käyttämällä kohdistusperustetta.</span><span class="sxs-lookup"><span data-stu-id="7792c-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="7792c-468">Finance tukee vastavuoroista kohdistusmenetelmää.</span><span class="sxs-lookup"><span data-stu-id="7792c-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="7792c-469">Vastavuoroisessa kohdistusmenetelmässä tunnistetaan oheiskustannusobjektien käyttämät, keskinäiset palvelut täysin.</span><span class="sxs-lookup"><span data-stu-id="7792c-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="7792c-470">Järjestelmä määrittää oikean kohdistusjärjestyksen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="7792c-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="7792c-471">Kustannusobjektin saldo kohdistetaan yhdellä kohdistusperusteella.</span><span class="sxs-lookup"><span data-stu-id="7792c-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="7792c-472">Kustannusobjektien dimensiot ja niiden vastaavat jäsenet ylittävät kohdistukset ovat tuettuja.</span><span class="sxs-lookup"><span data-stu-id="7792c-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="7792c-473">Kustannusseurantayksikkö hallitsee kohdistusjärjestystä.</span><span class="sxs-lookup"><span data-stu-id="7792c-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="7792c-474">[![Vastavuoroinen menetelmä](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="7792c-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="7792c-475">Määritä kustannuksen kohdistus</span><span class="sxs-lookup"><span data-stu-id="7792c-475">Define the cost allocation</span></span>

<span data-ttu-id="7792c-476">Tämä on yksinkertainen esimerkki, jossa kerrotaan, miten voit jäljittää kustannuksen virran.</span><span class="sxs-lookup"><span data-stu-id="7792c-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="7792c-477">Kustannusobjekti CC001 HR liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="7792c-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="7792c-478">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="7792c-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7792c-479">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-479">Cost object</span></span></th>
<th><span data-ttu-id="7792c-480">HR-palvelut</span><span class="sxs-lookup"><span data-stu-id="7792c-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-481">CC002</span><span class="sxs-lookup"><span data-stu-id="7792c-481">CC002</span></span></td>
<td><span data-ttu-id="7792c-482">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="7792c-482">Finance</span></span></td>
<td><span data-ttu-id="7792c-483">35</span><span class="sxs-lookup"><span data-stu-id="7792c-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-484">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-484">CC003</span></span></td>
<td><span data-ttu-id="7792c-485">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="7792c-485">Assembly</span></span></td>
<td><span data-ttu-id="7792c-486">55</span><span class="sxs-lookup"><span data-stu-id="7792c-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-487">CC004</span><span class="sxs-lookup"><span data-stu-id="7792c-487">CC004</span></span></td>
<td><span data-ttu-id="7792c-488">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="7792c-488">Packaging</span></span></td>
<td><span data-ttu-id="7792c-489">10</span><span class="sxs-lookup"><span data-stu-id="7792c-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7792c-490">Kustannusobjekti CC002 Taloushallinto liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="7792c-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="7792c-491">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Taloushallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="7792c-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7792c-492">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-492">Cost object</span></span></th>
<th><span data-ttu-id="7792c-493">Taloushallinnon palvelut</span><span class="sxs-lookup"><span data-stu-id="7792c-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-494">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-494">CC003</span></span></td>
<td><span data-ttu-id="7792c-495">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="7792c-495">Assembly</span></span></td>
<td><span data-ttu-id="7792c-496">65</span><span class="sxs-lookup"><span data-stu-id="7792c-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-497">CC004</span><span class="sxs-lookup"><span data-stu-id="7792c-497">CC004</span></span></td>
<td><span data-ttu-id="7792c-498">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="7792c-498">Packaging</span></span></td>
<td><span data-ttu-id="7792c-499">35</span><span class="sxs-lookup"><span data-stu-id="7792c-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7792c-500">Kustannusobjekti CC003 Kokoonpano liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="7792c-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="7792c-501">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Kokoonpanopalvelut.</span><span class="sxs-lookup"><span data-stu-id="7792c-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7792c-502">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-502">Cost object</span></span></th>
<th><span data-ttu-id="7792c-503">Kokoonpanopalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="7792c-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-504">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-504">Prod 1</span></span></td>
<td><span data-ttu-id="7792c-505">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-505">Product 1</span></span></td>
<td><span data-ttu-id="7792c-506">60</span><span class="sxs-lookup"><span data-stu-id="7792c-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-507">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-507">Prod 2</span></span></td>
<td><span data-ttu-id="7792c-508">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-508">Product 2</span></span></td>
<td><span data-ttu-id="7792c-509">20</span><span class="sxs-lookup"><span data-stu-id="7792c-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7792c-510">Kustannusobjekti CC004 Pakkaus liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="7792c-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="7792c-511">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Pakkauspalvelut.</span><span class="sxs-lookup"><span data-stu-id="7792c-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7792c-512">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-512">Cost object</span></span></th>
<th><span data-ttu-id="7792c-513">Pakkauspalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="7792c-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-514">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-514">Prod 1</span></span></td>
<td><span data-ttu-id="7792c-515">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-515">Product 1</span></span></td>
<td><span data-ttu-id="7792c-516">80</span><span class="sxs-lookup"><span data-stu-id="7792c-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-517">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-517">Prod 2</span></span></td>
<td><span data-ttu-id="7792c-518">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-518">Product 2</span></span></td>
<td><span data-ttu-id="7792c-519">15</span><span class="sxs-lookup"><span data-stu-id="7792c-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="7792c-520">Tilastomittaukset, kuten tämän tuotteen kuluttamat tuotantotunnit, voidaan johtaa lähdetiedoista.</span><span class="sxs-lookup"><span data-stu-id="7792c-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="7792c-521">Lisätietoja on kohdassa [Tilastomittauksen lähdemalli](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="7792c-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="7792c-522">Seuraavassa taulukossa näytetään tulos, kun henkilöstöhallinnon palveluja käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="7792c-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7792c-523">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-523">Cost object</span></span></th>
<th><span data-ttu-id="7792c-524">Suuruus</span><span class="sxs-lookup"><span data-stu-id="7792c-524">Magnitude</span></span></th>
<th><span data-ttu-id="7792c-525">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="7792c-525">Allocation factor</span></span></th>
<th><span data-ttu-id="7792c-526">Summa</span><span class="sxs-lookup"><span data-stu-id="7792c-526">Amount</span></span></th>
<th><span data-ttu-id="7792c-527">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="7792c-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-528">CC002</span><span class="sxs-lookup"><span data-stu-id="7792c-528">CC002</span></span></td>
<td><span data-ttu-id="7792c-529">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="7792c-529">Finance</span></span></td>
<td><span data-ttu-id="7792c-530">35</span><span class="sxs-lookup"><span data-stu-id="7792c-530">35</span></span></td>
<td><span data-ttu-id="7792c-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="7792c-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7792c-532">175.00</span><span class="sxs-lookup"><span data-stu-id="7792c-532">175.00</span></span></td>
<td><span data-ttu-id="7792c-533">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-534">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-534">CC003</span></span></td>
<td><span data-ttu-id="7792c-535">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="7792c-535">Assembly</span></span></td>
<td><span data-ttu-id="7792c-536">55</span><span class="sxs-lookup"><span data-stu-id="7792c-536">55</span></span></td>
<td><span data-ttu-id="7792c-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="7792c-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7792c-538">275.00</span><span class="sxs-lookup"><span data-stu-id="7792c-538">275.00</span></span></td>
<td><span data-ttu-id="7792c-539">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-540">CC004</span><span class="sxs-lookup"><span data-stu-id="7792c-540">CC004</span></span></td>
<td><span data-ttu-id="7792c-541">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="7792c-541">Packaging</span></span></td>
<td><span data-ttu-id="7792c-542">10</span><span class="sxs-lookup"><span data-stu-id="7792c-542">10</span></span></td>
<td><span data-ttu-id="7792c-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="7792c-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7792c-544">50,00</span><span class="sxs-lookup"><span data-stu-id="7792c-544">50.00</span></span></td>
<td><span data-ttu-id="7792c-545">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-546">CC002</span><span class="sxs-lookup"><span data-stu-id="7792c-546">CC002</span></span></td>
<td><span data-ttu-id="7792c-547">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="7792c-547">Finance</span></span></td>
<td><span data-ttu-id="7792c-548">35</span><span class="sxs-lookup"><span data-stu-id="7792c-548">35</span></span></td>
<td><span data-ttu-id="7792c-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="7792c-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7792c-550">436.00</span><span class="sxs-lookup"><span data-stu-id="7792c-550">436.00</span></span></td>
<td><span data-ttu-id="7792c-551">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-552">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-552">CC003</span></span></td>
<td><span data-ttu-id="7792c-553">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="7792c-553">Assembly</span></span></td>
<td><span data-ttu-id="7792c-554">55</span><span class="sxs-lookup"><span data-stu-id="7792c-554">55</span></span></td>
<td><span data-ttu-id="7792c-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="7792c-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7792c-556">685.14</span><span class="sxs-lookup"><span data-stu-id="7792c-556">685.14</span></span></td>
<td><span data-ttu-id="7792c-557">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-558">CC004</span><span class="sxs-lookup"><span data-stu-id="7792c-558">CC004</span></span></td>
<td><span data-ttu-id="7792c-559">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="7792c-559">Packaging</span></span></td>
<td><span data-ttu-id="7792c-560">10</span><span class="sxs-lookup"><span data-stu-id="7792c-560">10</span></span></td>
<td><span data-ttu-id="7792c-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="7792c-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7792c-562">124.57</span><span class="sxs-lookup"><span data-stu-id="7792c-562">124.57</span></span></td>
<td><span data-ttu-id="7792c-563">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7792c-564">Seuraavassa taulukossa näytetään tulos, kun Taloushallinnon palveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="7792c-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7792c-565">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-565">Cost object</span></span></th>
<th><span data-ttu-id="7792c-566">Suuruus</span><span class="sxs-lookup"><span data-stu-id="7792c-566">Magnitude</span></span></th>
<th><span data-ttu-id="7792c-567">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="7792c-567">Allocation factor</span></span></th>
<th><span data-ttu-id="7792c-568">Summa</span><span class="sxs-lookup"><span data-stu-id="7792c-568">Amount</span></span></th>
<th><span data-ttu-id="7792c-569">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="7792c-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-570">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-570">CC003</span></span></td>
<td><span data-ttu-id="7792c-571">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="7792c-571">Assembly</span></span></td>
<td><span data-ttu-id="7792c-572">65</span><span class="sxs-lookup"><span data-stu-id="7792c-572">65</span></span></td>
<td><span data-ttu-id="7792c-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="7792c-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="7792c-574">438.75</span><span class="sxs-lookup"><span data-stu-id="7792c-574">438.75</span></span></td>
<td><span data-ttu-id="7792c-575">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-576">CC004</span><span class="sxs-lookup"><span data-stu-id="7792c-576">CC004</span></span></td>
<td><span data-ttu-id="7792c-577">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="7792c-577">Packaging</span></span></td>
<td><span data-ttu-id="7792c-578">35</span><span class="sxs-lookup"><span data-stu-id="7792c-578">35</span></span></td>
<td><span data-ttu-id="7792c-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="7792c-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="7792c-580">236.25</span><span class="sxs-lookup"><span data-stu-id="7792c-580">236.25</span></span></td>
<td><span data-ttu-id="7792c-581">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-582">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-582">CC003</span></span></td>
<td><span data-ttu-id="7792c-583">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="7792c-583">Assembly</span></span></td>
<td><span data-ttu-id="7792c-584">65</span><span class="sxs-lookup"><span data-stu-id="7792c-584">65</span></span></td>
<td><span data-ttu-id="7792c-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="7792c-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="7792c-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="7792c-586">5,297.69</span></span></td>
<td><span data-ttu-id="7792c-587">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-588">CC004</span><span class="sxs-lookup"><span data-stu-id="7792c-588">CC004</span></span></td>
<td><span data-ttu-id="7792c-589">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="7792c-589">Packaging</span></span></td>
<td><span data-ttu-id="7792c-590">35</span><span class="sxs-lookup"><span data-stu-id="7792c-590">35</span></span></td>
<td><span data-ttu-id="7792c-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="7792c-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="7792c-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="7792c-592">2,852.60</span></span></td>
<td><span data-ttu-id="7792c-593">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7792c-594">Seuraavassa taulukossa näytetään tulos, kun Kokoonpanopalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="7792c-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7792c-595">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-595">Cost object</span></span></th>
<th><span data-ttu-id="7792c-596">Suuruus</span><span class="sxs-lookup"><span data-stu-id="7792c-596">Magnitude</span></span></th>
<th><span data-ttu-id="7792c-597">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="7792c-597">Allocation factor</span></span></th>
<th><span data-ttu-id="7792c-598">Summa</span><span class="sxs-lookup"><span data-stu-id="7792c-598">Amount</span></span></th>
<th><span data-ttu-id="7792c-599">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="7792c-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-600">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-600">Prod 1</span></span></td>
<td><span data-ttu-id="7792c-601">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-601">Product 1</span></span></td>
<td><span data-ttu-id="7792c-602">60</span><span class="sxs-lookup"><span data-stu-id="7792c-602">60</span></span></td>
<td><span data-ttu-id="7792c-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="7792c-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="7792c-604">535.31</span><span class="sxs-lookup"><span data-stu-id="7792c-604">535.31</span></span></td>
<td><span data-ttu-id="7792c-605">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-606">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-606">Prod 2</span></span></td>
<td><span data-ttu-id="7792c-607">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-607">Product 2</span></span></td>
<td><span data-ttu-id="7792c-608">20</span><span class="sxs-lookup"><span data-stu-id="7792c-608">20</span></span></td>
<td><span data-ttu-id="7792c-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="7792c-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="7792c-610">178.44</span><span class="sxs-lookup"><span data-stu-id="7792c-610">178.44</span></span></td>
<td><span data-ttu-id="7792c-611">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-612">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-612">Prod 1</span></span></td>
<td><span data-ttu-id="7792c-613">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-613">Product 1</span></span></td>
<td><span data-ttu-id="7792c-614">60</span><span class="sxs-lookup"><span data-stu-id="7792c-614">60</span></span></td>
<td><span data-ttu-id="7792c-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="7792c-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="7792c-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="7792c-616">4,487.12</span></span></td>
<td><span data-ttu-id="7792c-617">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-618">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-618">Prod 2</span></span></td>
<td><span data-ttu-id="7792c-619">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-619">Product 2</span></span></td>
<td><span data-ttu-id="7792c-620">20</span><span class="sxs-lookup"><span data-stu-id="7792c-620">20</span></span></td>
<td><span data-ttu-id="7792c-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="7792c-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="7792c-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="7792c-622">1,495.71</span></span></td>
<td><span data-ttu-id="7792c-623">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7792c-624">Seuraavassa taulukossa näytetään tulos, kun Pakkauspalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="7792c-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7792c-625">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-625">Cost object</span></span></th>
<th><span data-ttu-id="7792c-626">Suuruus</span><span class="sxs-lookup"><span data-stu-id="7792c-626">Magnitude</span></span></th>
<th><span data-ttu-id="7792c-627">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="7792c-627">Allocation factor</span></span></th>
<th><span data-ttu-id="7792c-628">Summa</span><span class="sxs-lookup"><span data-stu-id="7792c-628">Amount</span></span></th>
<th><span data-ttu-id="7792c-629">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="7792c-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-630">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-630">Prod 1</span></span></td>
<td><span data-ttu-id="7792c-631">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-631">Product 1</span></span></td>
<td><span data-ttu-id="7792c-632">80</span><span class="sxs-lookup"><span data-stu-id="7792c-632">80</span></span></td>
<td><span data-ttu-id="7792c-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="7792c-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="7792c-634">241.05</span><span class="sxs-lookup"><span data-stu-id="7792c-634">241.05</span></span></td>
<td><span data-ttu-id="7792c-635">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-636">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-636">Prod 2</span></span></td>
<td><span data-ttu-id="7792c-637">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-637">Product 2</span></span></td>
<td><span data-ttu-id="7792c-638">15</span><span class="sxs-lookup"><span data-stu-id="7792c-638">15</span></span></td>
<td><span data-ttu-id="7792c-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="7792c-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="7792c-640">45.20</span><span class="sxs-lookup"><span data-stu-id="7792c-640">45.20</span></span></td>
<td><span data-ttu-id="7792c-641">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-642">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-642">Prod 1</span></span></td>
<td><span data-ttu-id="7792c-643">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-643">Product 1</span></span></td>
<td><span data-ttu-id="7792c-644">80</span><span class="sxs-lookup"><span data-stu-id="7792c-644">80</span></span></td>
<td><span data-ttu-id="7792c-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="7792c-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="7792c-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="7792c-646">2,507.09</span></span></td>
<td><span data-ttu-id="7792c-647">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-648">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-648">Prod 2</span></span></td>
<td><span data-ttu-id="7792c-649">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-649">Product 2</span></span></td>
<td><span data-ttu-id="7792c-650">15</span><span class="sxs-lookup"><span data-stu-id="7792c-650">15</span></span></td>
<td><span data-ttu-id="7792c-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="7792c-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="7792c-652">470.08</span><span class="sxs-lookup"><span data-stu-id="7792c-652">470.08</span></span></td>
<td><span data-ttu-id="7792c-653">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7792c-654">Kirjauskansioviennit (kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="7792c-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7792c-655">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="7792c-655">Journal</span></span></th>
<th><span data-ttu-id="7792c-656">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="7792c-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7792c-657">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="7792c-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7792c-658">Versio</span><span class="sxs-lookup"><span data-stu-id="7792c-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-659">00004</span><span class="sxs-lookup"><span data-stu-id="7792c-659">00004</span></span></td>
<td><span data-ttu-id="7792c-660">Kustannusten kohdistuskirjauskansio</span><span class="sxs-lookup"><span data-stu-id="7792c-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="7792c-661">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="7792c-661">Fiscal</span></span></td>
<td><span data-ttu-id="7792c-662">2017</span><span class="sxs-lookup"><span data-stu-id="7792c-662">2017</span></span></td>
<td><span data-ttu-id="7792c-663">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="7792c-663">Period 1</span></span></td>
<td><span data-ttu-id="7792c-664">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="7792c-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="7792c-665">Kirjauskansion rivit</span><span class="sxs-lookup"><span data-stu-id="7792c-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7792c-666">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="7792c-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7792c-667">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7792c-668">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="7792c-668">Cost element</span></span></th>
<th><span data-ttu-id="7792c-669">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="7792c-669">Cost behavior</span></span></th>
<th><span data-ttu-id="7792c-670">Summa</span><span class="sxs-lookup"><span data-stu-id="7792c-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-671">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="7792c-672">CC001</span><span class="sxs-lookup"><span data-stu-id="7792c-672">CC001</span></span></td>
<td><span data-ttu-id="7792c-673">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="7792c-673">HR</span></span></td>
<td><span data-ttu-id="7792c-674">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-674">10001</span></span></td>
<td><span data-ttu-id="7792c-675">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-675">Electricity</span></span></td>
<td><span data-ttu-id="7792c-676">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-676">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-677">500,00</span><span class="sxs-lookup"><span data-stu-id="7792c-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-678">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="7792c-679">CC001</span><span class="sxs-lookup"><span data-stu-id="7792c-679">CC001</span></span></td>
<td><span data-ttu-id="7792c-680">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="7792c-680">HR</span></span></td>
<td><span data-ttu-id="7792c-681">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-681">10001</span></span></td>
<td><span data-ttu-id="7792c-682">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-682">Electricity</span></span></td>
<td><span data-ttu-id="7792c-683">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-683">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="7792c-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-685">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="7792c-686">CC002</span><span class="sxs-lookup"><span data-stu-id="7792c-686">CC002</span></span></td>
<td><span data-ttu-id="7792c-687">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="7792c-687">Finance</span></span></td>
<td><span data-ttu-id="7792c-688">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-688">10001</span></span></td>
<td><span data-ttu-id="7792c-689">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-689">Electricity</span></span></td>
<td><span data-ttu-id="7792c-690">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-690">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-691">675.00</span><span class="sxs-lookup"><span data-stu-id="7792c-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-692">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="7792c-693">CC002</span><span class="sxs-lookup"><span data-stu-id="7792c-693">CC002</span></span></td>
<td><span data-ttu-id="7792c-694">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="7792c-694">Finance</span></span></td>
<td><span data-ttu-id="7792c-695">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-695">10001</span></span></td>
<td><span data-ttu-id="7792c-696">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-696">Electricity</span></span></td>
<td><span data-ttu-id="7792c-697">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-697">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="7792c-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-699">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="7792c-700">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-700">CC003</span></span></td>
<td><span data-ttu-id="7792c-701">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="7792c-701">Assembly</span></span></td>
<td><span data-ttu-id="7792c-702">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-702">10001</span></span></td>
<td><span data-ttu-id="7792c-703">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-703">Electricity</span></span></td>
<td><span data-ttu-id="7792c-704">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-704">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-705">713.75</span><span class="sxs-lookup"><span data-stu-id="7792c-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-706">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="7792c-707">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-707">CC003</span></span></td>
<td><span data-ttu-id="7792c-708">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="7792c-708">Assembly</span></span></td>
<td><span data-ttu-id="7792c-709">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-709">10001</span></span></td>
<td><span data-ttu-id="7792c-710">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-710">Electricity</span></span></td>
<td><span data-ttu-id="7792c-711">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-711">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="7792c-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-713">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="7792c-714">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-714">CC003</span></span></td>
<td><span data-ttu-id="7792c-715">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="7792c-715">Packaging</span></span></td>
<td><span data-ttu-id="7792c-716">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-716">10001</span></span></td>
<td><span data-ttu-id="7792c-717">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-717">Electricity</span></span></td>
<td><span data-ttu-id="7792c-718">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-718">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-719">286.25</span><span class="sxs-lookup"><span data-stu-id="7792c-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-720">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="7792c-721">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-721">CC003</span></span></td>
<td><span data-ttu-id="7792c-722">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="7792c-722">Packaging</span></span></td>
<td><span data-ttu-id="7792c-723">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-723">10001</span></span></td>
<td><span data-ttu-id="7792c-724">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-724">Electricity</span></span></td>
<td><span data-ttu-id="7792c-725">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-725">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="7792c-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-727">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="7792c-728">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-728">Prod 1</span></span></td>
<td><span data-ttu-id="7792c-729">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-729">Product 1</span></span></td>
<td><span data-ttu-id="7792c-730">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-730">10001</span></span></td>
<td><span data-ttu-id="7792c-731">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-731">Electricity</span></span></td>
<td><span data-ttu-id="7792c-732">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-732">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-733">776.36</span><span class="sxs-lookup"><span data-stu-id="7792c-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-734">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="7792c-735">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-735">Prod 1</span></span></td>
<td><span data-ttu-id="7792c-736">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-736">Product 1</span></span></td>
<td><span data-ttu-id="7792c-737">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-737">10001</span></span></td>
<td><span data-ttu-id="7792c-738">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-738">Electricity</span></span></td>
<td><span data-ttu-id="7792c-739">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-739">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="7792c-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-741">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="7792c-742">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-742">Prod 2</span></span></td>
<td><span data-ttu-id="7792c-743">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-743">Product 1</span></span></td>
<td><span data-ttu-id="7792c-744">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-744">10001</span></span></td>
<td><span data-ttu-id="7792c-745">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-745">Electricity</span></span></td>
<td><span data-ttu-id="7792c-746">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-746">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-747">223.64</span><span class="sxs-lookup"><span data-stu-id="7792c-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-748">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="7792c-749">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-749">Prod 2</span></span></td>
<td><span data-ttu-id="7792c-750">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-750">Product 1</span></span></td>
<td><span data-ttu-id="7792c-751">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-751">10001</span></span></td>
<td><span data-ttu-id="7792c-752">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-752">Electricity</span></span></td>
<td><span data-ttu-id="7792c-753">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-753">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="7792c-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7792c-755">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="7792c-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7792c-756">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7792c-757">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="7792c-757">Cost element</span></span></th>
<th><span data-ttu-id="7792c-758">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="7792c-758">Cost behavior</span></span></th>
<th><span data-ttu-id="7792c-759">Summa</span><span class="sxs-lookup"><span data-stu-id="7792c-759">Amount</span></span></th>
<th><span data-ttu-id="7792c-760">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="7792c-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7792c-761">CC001</span><span class="sxs-lookup"><span data-stu-id="7792c-761">CC001</span></span></td>
<td><span data-ttu-id="7792c-762">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="7792c-762">HR</span></span></td>
<td><span data-ttu-id="7792c-763">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-763">10001</span></span></td>
<td><span data-ttu-id="7792c-764">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-764">Electricity</span></span></td>
<td><span data-ttu-id="7792c-765">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-765">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="7792c-766">-500.00</span></span></td>
<td><span data-ttu-id="7792c-767">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-768">CC002</span><span class="sxs-lookup"><span data-stu-id="7792c-768">CC002</span></span></td>
<td><span data-ttu-id="7792c-769">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="7792c-769">Finance</span></span></td>
<td><span data-ttu-id="7792c-770">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-770">10001</span></span></td>
<td><span data-ttu-id="7792c-771">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-771">Electricity</span></span></td>
<td><span data-ttu-id="7792c-772">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-772">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-773">175.00</span><span class="sxs-lookup"><span data-stu-id="7792c-773">175.00</span></span></td>
<td><span data-ttu-id="7792c-774">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-775">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-775">CC003</span></span></td>
<td><span data-ttu-id="7792c-776">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="7792c-776">Assembly</span></span></td>
<td><span data-ttu-id="7792c-777">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-777">10001</span></span></td>
<td><span data-ttu-id="7792c-778">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-778">Electricity</span></span></td>
<td><span data-ttu-id="7792c-779">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-779">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-780">275.00</span><span class="sxs-lookup"><span data-stu-id="7792c-780">275.00</span></span></td>
<td><span data-ttu-id="7792c-781">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-782">CC004</span><span class="sxs-lookup"><span data-stu-id="7792c-782">CC004</span></span></td>
<td><span data-ttu-id="7792c-783">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="7792c-783">Packaging</span></span></td>
<td><span data-ttu-id="7792c-784">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-784">10001</span></span></td>
<td><span data-ttu-id="7792c-785">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-785">Electricity</span></span></td>
<td><span data-ttu-id="7792c-786">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-786">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-787">50,00</span><span class="sxs-lookup"><span data-stu-id="7792c-787">50,00</span></span></td>
<td><span data-ttu-id="7792c-788">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-789">CC001</span><span class="sxs-lookup"><span data-stu-id="7792c-789">CC001</span></span></td>
<td><span data-ttu-id="7792c-790">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="7792c-790">HR</span></span></td>
<td><span data-ttu-id="7792c-791">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-791">10001</span></span></td>
<td><span data-ttu-id="7792c-792">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-792">Electricity</span></span></td>
<td><span data-ttu-id="7792c-793">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-793">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="7792c-794">-1,245.71</span></span></td>
<td><span data-ttu-id="7792c-795">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-796">CC002</span><span class="sxs-lookup"><span data-stu-id="7792c-796">CC002</span></span></td>
<td><span data-ttu-id="7792c-797">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="7792c-797">Finance</span></span></td>
<td><span data-ttu-id="7792c-798">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-798">10001</span></span></td>
<td><span data-ttu-id="7792c-799">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-799">Electricity</span></span></td>
<td><span data-ttu-id="7792c-800">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-800">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-801">436.00</span><span class="sxs-lookup"><span data-stu-id="7792c-801">436.00</span></span></td>
<td><span data-ttu-id="7792c-802">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-803">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-803">CC003</span></span></td>
<td><span data-ttu-id="7792c-804">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="7792c-804">Assembly</span></span></td>
<td><span data-ttu-id="7792c-805">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-805">10001</span></span></td>
<td><span data-ttu-id="7792c-806">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-806">Electricity</span></span></td>
<td><span data-ttu-id="7792c-807">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-807">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-808">685.14</span><span class="sxs-lookup"><span data-stu-id="7792c-808">685.14</span></span></td>
<td><span data-ttu-id="7792c-809">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-810">CC004</span><span class="sxs-lookup"><span data-stu-id="7792c-810">CC004</span></span></td>
<td><span data-ttu-id="7792c-811">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="7792c-811">Packaging</span></span></td>
<td><span data-ttu-id="7792c-812">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-812">10001</span></span></td>
<td><span data-ttu-id="7792c-813">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-813">Electricity</span></span></td>
<td><span data-ttu-id="7792c-814">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-814">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-815">124.57</span><span class="sxs-lookup"><span data-stu-id="7792c-815">124.57</span></span></td>
<td><span data-ttu-id="7792c-816">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-817">CC002</span><span class="sxs-lookup"><span data-stu-id="7792c-817">CC002</span></span></td>
<td><span data-ttu-id="7792c-818">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="7792c-818">Finance</span></span></td>
<td><span data-ttu-id="7792c-819">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-819">10001</span></span></td>
<td><span data-ttu-id="7792c-820">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-820">Electricity</span></span></td>
<td><span data-ttu-id="7792c-821">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-821">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="7792c-822">-675.00</span></span></td>
<td><span data-ttu-id="7792c-823">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-824">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-824">CC003</span></span></td>
<td><span data-ttu-id="7792c-825">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="7792c-825">Assembly</span></span></td>
<td><span data-ttu-id="7792c-826">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-826">10001</span></span></td>
<td><span data-ttu-id="7792c-827">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-827">Electricity</span></span></td>
<td><span data-ttu-id="7792c-828">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-828">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-829">438.75</span><span class="sxs-lookup"><span data-stu-id="7792c-829">438.75</span></span></td>
<td><span data-ttu-id="7792c-830">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-831">CC004</span><span class="sxs-lookup"><span data-stu-id="7792c-831">CC004</span></span></td>
<td><span data-ttu-id="7792c-832">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="7792c-832">Packaging</span></span></td>
<td><span data-ttu-id="7792c-833">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-833">10001</span></span></td>
<td><span data-ttu-id="7792c-834">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-834">Electricity</span></span></td>
<td><span data-ttu-id="7792c-835">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-835">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-836">236.25</span><span class="sxs-lookup"><span data-stu-id="7792c-836">236.25</span></span></td>
<td><span data-ttu-id="7792c-837">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-838">CC002</span><span class="sxs-lookup"><span data-stu-id="7792c-838">CC002</span></span></td>
<td><span data-ttu-id="7792c-839">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="7792c-839">Finance</span></span></td>
<td><span data-ttu-id="7792c-840">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-840">10001</span></span></td>
<td><span data-ttu-id="7792c-841">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-841">Electricity</span></span></td>
<td><span data-ttu-id="7792c-842">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-842">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="7792c-843">-8,150.29</span></span></td>
<td><span data-ttu-id="7792c-844">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-845">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-845">CC003</span></span></td>
<td><span data-ttu-id="7792c-846">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="7792c-846">Assembly</span></span></td>
<td><span data-ttu-id="7792c-847">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-847">10001</span></span></td>
<td><span data-ttu-id="7792c-848">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-848">Electricity</span></span></td>
<td><span data-ttu-id="7792c-849">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-849">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="7792c-850">5,297.69</span></span></td>
<td><span data-ttu-id="7792c-851">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-852">CC004</span><span class="sxs-lookup"><span data-stu-id="7792c-852">CC004</span></span></td>
<td><span data-ttu-id="7792c-853">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="7792c-853">Packaging</span></span></td>
<td><span data-ttu-id="7792c-854">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-854">10001</span></span></td>
<td><span data-ttu-id="7792c-855">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-855">Electricity</span></span></td>
<td><span data-ttu-id="7792c-856">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-856">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="7792c-857">2,852.60</span></span></td>
<td><span data-ttu-id="7792c-858">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-859">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-859">CC003</span></span></td>
<td><span data-ttu-id="7792c-860">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="7792c-860">Assembly</span></span></td>
<td><span data-ttu-id="7792c-861">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-861">10001</span></span></td>
<td><span data-ttu-id="7792c-862">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-862">Electricity</span></span></td>
<td><span data-ttu-id="7792c-863">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-863">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="7792c-864">-713.75</span></span></td>
<td><span data-ttu-id="7792c-865">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-866">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-866">Prod 1</span></span></td>
<td><span data-ttu-id="7792c-867">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-867">Product 1</span></span></td>
<td><span data-ttu-id="7792c-868">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-868">10001</span></span></td>
<td><span data-ttu-id="7792c-869">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-869">Electricity</span></span></td>
<td><span data-ttu-id="7792c-870">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-870">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-871">535.31</span><span class="sxs-lookup"><span data-stu-id="7792c-871">535.31</span></span></td>
<td><span data-ttu-id="7792c-872">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-873">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-873">Prod 2</span></span></td>
<td><span data-ttu-id="7792c-874">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-874">Product 2</span></span></td>
<td><span data-ttu-id="7792c-875">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-875">10001</span></span></td>
<td><span data-ttu-id="7792c-876">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-876">Electricity</span></span></td>
<td><span data-ttu-id="7792c-877">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-877">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-878">178.44</span><span class="sxs-lookup"><span data-stu-id="7792c-878">178.44</span></span></td>
<td><span data-ttu-id="7792c-879">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-880">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-880">CC003</span></span></td>
<td><span data-ttu-id="7792c-881">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="7792c-881">Assembly</span></span></td>
<td><span data-ttu-id="7792c-882">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-882">10001</span></span></td>
<td><span data-ttu-id="7792c-883">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-883">Electricity</span></span></td>
<td><span data-ttu-id="7792c-884">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-884">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="7792c-885">-5,982.83</span></span></td>
<td><span data-ttu-id="7792c-886">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-887">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-887">Prod 1</span></span></td>
<td><span data-ttu-id="7792c-888">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-888">Product 1</span></span></td>
<td><span data-ttu-id="7792c-889">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-889">10001</span></span></td>
<td><span data-ttu-id="7792c-890">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-890">Electricity</span></span></td>
<td><span data-ttu-id="7792c-891">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-891">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="7792c-892">4,487.12</span></span></td>
<td><span data-ttu-id="7792c-893">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-894">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-894">Prod 2</span></span></td>
<td><span data-ttu-id="7792c-895">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-895">Product 2</span></span></td>
<td><span data-ttu-id="7792c-896">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-896">10001</span></span></td>
<td><span data-ttu-id="7792c-897">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-897">Electricity</span></span></td>
<td><span data-ttu-id="7792c-898">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-898">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="7792c-899">1,495.71</span></span></td>
<td><span data-ttu-id="7792c-900">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-901">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-901">CC003</span></span></td>
<td><span data-ttu-id="7792c-902">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="7792c-902">Assembly</span></span></td>
<td><span data-ttu-id="7792c-903">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-903">10001</span></span></td>
<td><span data-ttu-id="7792c-904">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-904">Electricity</span></span></td>
<td><span data-ttu-id="7792c-905">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-905">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="7792c-906">-286.25</span></span></td>
<td><span data-ttu-id="7792c-907">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-908">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-908">Prod 1</span></span></td>
<td><span data-ttu-id="7792c-909">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-909">Product 1</span></span></td>
<td><span data-ttu-id="7792c-910">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-910">10001</span></span></td>
<td><span data-ttu-id="7792c-911">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-911">Electricity</span></span></td>
<td><span data-ttu-id="7792c-912">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-912">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-913">241.05</span><span class="sxs-lookup"><span data-stu-id="7792c-913">241.05</span></span></td>
<td><span data-ttu-id="7792c-914">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-915">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-915">Prod 2</span></span></td>
<td><span data-ttu-id="7792c-916">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-916">Product 2</span></span></td>
<td><span data-ttu-id="7792c-917">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-917">10001</span></span></td>
<td><span data-ttu-id="7792c-918">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-918">Electricity</span></span></td>
<td><span data-ttu-id="7792c-919">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-919">Fixed cost</span></span></td>
<td><span data-ttu-id="7792c-920">45.20</span><span class="sxs-lookup"><span data-stu-id="7792c-920">45.20</span></span></td>
<td><span data-ttu-id="7792c-921">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-922">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-922">CC003</span></span></td>
<td><span data-ttu-id="7792c-923">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="7792c-923">Assembly</span></span></td>
<td><span data-ttu-id="7792c-924">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-924">10001</span></span></td>
<td><span data-ttu-id="7792c-925">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-925">Electricity</span></span></td>
<td><span data-ttu-id="7792c-926">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-926">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-927">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="7792c-927">-2,977.17</span></span></td>
<td><span data-ttu-id="7792c-928">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-929">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-929">Prod 1</span></span></td>
<td><span data-ttu-id="7792c-930">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-930">Product 1</span></span></td>
<td><span data-ttu-id="7792c-931">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-931">10001</span></span></td>
<td><span data-ttu-id="7792c-932">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-932">Electricity</span></span></td>
<td><span data-ttu-id="7792c-933">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-933">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="7792c-934">2,507.09</span></span></td>
<td><span data-ttu-id="7792c-935">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7792c-936">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-936">Prod 2</span></span></td>
<td><span data-ttu-id="7792c-937">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-937">Product 2</span></span></td>
<td><span data-ttu-id="7792c-938">10 001</span><span class="sxs-lookup"><span data-stu-id="7792c-938">10001</span></span></td>
<td><span data-ttu-id="7792c-939">Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-939">Electricity</span></span></td>
<td><span data-ttu-id="7792c-940">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-940">Variable cost</span></span></td>
<td><span data-ttu-id="7792c-941">470.08</span><span class="sxs-lookup"><span data-stu-id="7792c-941">470.08</span></span></td>
<td><span data-ttu-id="7792c-942">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="7792c-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="7792c-943">Johtopäätökset</span><span class="sxs-lookup"><span data-stu-id="7792c-943">Conclusion</span></span>
<span data-ttu-id="7792c-944">Kirjanpidossa kirjataan tyhjään kustannuspaikkatunnukseen sähkökustannus arvolla 10 000,00.</span><span class="sxs-lookup"><span data-stu-id="7792c-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="7792c-945">Tämän ansiosta kustannuslaskijat tietävät, että kustannus on kohdistettava.</span><span class="sxs-lookup"><span data-stu-id="7792c-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="7792c-946">Kustannukset virtaavat kirjanpidossa organisaation yksiköiden ja tasojen läpi käytössä olevien käytäntöjen ja sääntöjen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="7792c-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="7792c-947">Kukin kustannus on liitetty kustannusperusteeseen, joka sisältää parhaan arvion kustannusten kohdistuksesta.</span><span class="sxs-lookup"><span data-stu-id="7792c-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="7792c-948">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="7792c-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="7792c-949">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="7792c-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="7792c-950">Yhteensä</span><span class="sxs-lookup"><span data-stu-id="7792c-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="7792c-951">CC099</span><span class="sxs-lookup"><span data-stu-id="7792c-951">CC099</span></span></th>
<th><span data-ttu-id="7792c-952">CC001</span><span class="sxs-lookup"><span data-stu-id="7792c-952">CC001</span></span></th>
<th><span data-ttu-id="7792c-953">CC002</span><span class="sxs-lookup"><span data-stu-id="7792c-953">CC002</span></span></th>
<th><span data-ttu-id="7792c-954">CC003</span><span class="sxs-lookup"><span data-stu-id="7792c-954">CC003</span></span></th>
<th><span data-ttu-id="7792c-955">CC004</span><span class="sxs-lookup"><span data-stu-id="7792c-955">CC004</span></span></th>
<th><span data-ttu-id="7792c-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7792c-956">Proj 1</span></span></th>
<th><span data-ttu-id="7792c-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7792c-957">Proj 2</span></span></th>
<th><span data-ttu-id="7792c-958">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="7792c-958">Prod 1</span></span></th>
<th><span data-ttu-id="7792c-959">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="7792c-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="7792c-960">10001 Sähkö</span><span class="sxs-lookup"><span data-stu-id="7792c-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="7792c-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="7792c-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="7792c-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="7792c-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="7792c-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="7792c-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="7792c-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="7792c-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="7792c-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="7792c-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="7792c-970">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="7792c-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-971">0,00</span><span class="sxs-lookup"><span data-stu-id="7792c-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="7792c-972">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="7792c-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-973">0,00</span><span class="sxs-lookup"><span data-stu-id="7792c-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-974">0,00</span><span class="sxs-lookup"><span data-stu-id="7792c-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-975">0,00</span><span class="sxs-lookup"><span data-stu-id="7792c-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-976">0,00</span><span class="sxs-lookup"><span data-stu-id="7792c-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-977">0,00</span><span class="sxs-lookup"><span data-stu-id="7792c-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="7792c-978">776.36</span><span class="sxs-lookup"><span data-stu-id="7792c-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-979">223.64</span><span class="sxs-lookup"><span data-stu-id="7792c-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="7792c-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="7792c-981">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="7792c-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-982">000</span><span class="sxs-lookup"><span data-stu-id="7792c-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-983">0,00</span><span class="sxs-lookup"><span data-stu-id="7792c-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-984">0,00</span><span class="sxs-lookup"><span data-stu-id="7792c-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-985">0,00</span><span class="sxs-lookup"><span data-stu-id="7792c-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-986">0,00</span><span class="sxs-lookup"><span data-stu-id="7792c-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-987">30,00</span><span class="sxs-lookup"><span data-stu-id="7792c-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-988">10,00</span><span class="sxs-lookup"><span data-stu-id="7792c-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="7792c-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="7792c-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7792c-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="7792c-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="7792c-992">Tässä ohjeaiheessa esitellään, miten ensisijainen kustannuselementti, 10001 Sähkö, virtaa kustannusobjektien läpi.</span><span class="sxs-lookup"><span data-stu-id="7792c-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="7792c-993">Tästä syystä tämä yleiskustannus kohdistetaan organisaation alimmalle tasolle.</span><span class="sxs-lookup"><span data-stu-id="7792c-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="7792c-994">Toisin sanoen alimman tason kustannusobjektit kantavat kustannuksen.</span><span class="sxs-lookup"><span data-stu-id="7792c-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="7792c-995">Jos tarvitset visuaalisen näkymän kustannuksen virrasta kustannusobjektien välillä, voit käyttää kustannuksen koontikäytäntösääntöjä kustannusvirran visualisointiin.</span><span class="sxs-lookup"><span data-stu-id="7792c-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="7792c-996">Lisätietoja on kohdassa [Kustannusten koontikäytäntö ja yleiskustannuslaskenta](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="7792c-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



