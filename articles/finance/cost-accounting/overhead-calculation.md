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
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 923e6e38a664e17ec3349d839c4b77ec903c5dc2
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976472"
---
# <a name="overhead-calculation"></a><span data-ttu-id="0f2e3-103">Yleiskustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="0f2e3-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f2e3-104">Tässä aiheessa kuvataan tyypillinen yleiskustannusten laskenta- ja kohdistusprosessi.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="0f2e3-105">Sanaston määritelmä</span><span class="sxs-lookup"><span data-stu-id="0f2e3-105">Term definition</span></span>
---------------

<span data-ttu-id="0f2e3-106">Yleiskustannukset ovat yrityksen toiminnasta syntyviä kustannuksia, joita ei voi suoraan liittää mihinkään tiettyyn liiketoiminnan tehtävään, tuotteeseen tai palveluun.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="0f2e3-107">Yleiskustannukset ovat tärkeä tuki voittoa tuottavien tehtävien luonnissa.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="0f2e3-108">Seuraavassa on joitakin esimerkkejä yleiskustannuksista:</span><span class="sxs-lookup"><span data-stu-id="0f2e3-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="0f2e3-109">Vuokra</span><span class="sxs-lookup"><span data-stu-id="0f2e3-109">Rent</span></span>
-   <span data-ttu-id="0f2e3-110">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-110">Electricity</span></span>
-   <span data-ttu-id="0f2e3-111">Hallinnon palkat</span><span class="sxs-lookup"><span data-stu-id="0f2e3-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="0f2e3-112">Yleiskustannuslaskennan yleiskuva</span><span class="sxs-lookup"><span data-stu-id="0f2e3-112">Overhead calculation overview</span></span>
<span data-ttu-id="0f2e3-113">Yleiskustannusten laskenta suorittaa kustannuslaskennan käytännöt oikeassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="0f2e3-114">Yleiskustannusten laskennan voi suorittaa useita kertoja samalle tilikaudelle, jos kustannuslaskennan käytännöt ovat muuttuneet tai erityisiä virheitä on havaittu.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="0f2e3-115">Kukin laskenta-ajo tallennetaan ja kullekin annetaan yksilöllinen versiotunnus, jonka avulla eri laskenta-ajoja voi verrata toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="0f2e3-116">Yleiskustannusten laskenta luo kustannustapahtumia, joille annetaan kirjauspäivä.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="0f2e3-117">Kirjauspäivä vastaa laskennassa käytettyä tilikauden päättymispäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="0f2e3-118">Yksilöivä versiotunnus sisältää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="0f2e3-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="0f2e3-119">Versiotyyppi</span><span class="sxs-lookup"><span data-stu-id="0f2e3-119">Version type</span></span>
-   <span data-ttu-id="0f2e3-120">Päivämäärä ja aika</span><span class="sxs-lookup"><span data-stu-id="0f2e3-120">Date and time</span></span>
-   <span data-ttu-id="0f2e3-121">Kustannuslaskennan kirjanpito</span><span class="sxs-lookup"><span data-stu-id="0f2e3-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="0f2e3-122">Tilikausi </span><span class="sxs-lookup"><span data-stu-id="0f2e3-122">Fiscal year</span></span>
-   <span data-ttu-id="0f2e3-123">Tilikausi  </span><span class="sxs-lookup"><span data-stu-id="0f2e3-123">Fiscal period</span></span>

<span data-ttu-id="0f2e3-124">Yleiskustannusten laskenta ajetaan versiosta riippumattomana.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="0f2e3-125">Voit siis laskea budjetin version ennen todellista versiota.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="0f2e3-126">Yleiskustannusten laskenta koostuu neljästä vaiheesta, jotka esitellään seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="0f2e3-127">Kussakin vaiheessa luodaan kirjauskansion otsikko, jolla on kirjauskansiovientejä.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="0f2e3-128">Tämä kirjauskansion otsikko säilyttää kunkin laskentavaiheen syöttötiedot.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="0f2e3-129">Käytännöt ja säännöt ajetaan kullekin kirjauskansion riville, ja tuloksena luodaan kustannustapahtumia.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="0f2e3-130">Tämän ansiosta kaikki laskutoimitukset ovat täysin jäljitettävissä.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="0f2e3-131">[![Yleiskustannuslaskenta](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="0f2e3-132">Laske ja kohdista sähkön yleiskustannukset</span><span class="sxs-lookup"><span data-stu-id="0f2e3-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="0f2e3-133">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="0f2e3-134">Tarkka johdon näkymä ei täten ole saatavilla kustannuslaskennassa.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="0f2e3-135">Jotta kustannuslaskenta tarjoaisi oikean johdon näkymän kaikista organisaation yksiköistä ja tasoista, kustannusten on virrattava organisaation yksiköiden läpi.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="0f2e3-136">Tämän virran on perustuttava joko tarkkaan tietoon kulutuksesta tai perusteltuun arvioon.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="0f2e3-137">Sähkökustannukset voi kirjata kirjanpitoon seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0f2e3-138">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="0f2e3-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="0f2e3-139">Kustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="0f2e3-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="0f2e3-140">Päätili</span><span class="sxs-lookup"><span data-stu-id="0f2e3-140">Main account</span></span></th>
<th><span data-ttu-id="0f2e3-141">Summa kirjanpitovaluuttana</span><span class="sxs-lookup"><span data-stu-id="0f2e3-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-142">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="0f2e3-143">CC099</span><span class="sxs-lookup"><span data-stu-id="0f2e3-143">CC099</span></span></td>
<td><span data-ttu-id="0f2e3-144">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="0f2e3-144">Default cost center</span></span></td>
<td><span data-ttu-id="0f2e3-145">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-145">10001</span></span></td>
<td><span data-ttu-id="0f2e3-146">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-146">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="0f2e3-148">Vaihe 1: Käsittele kustannustoiminnan laskenta</span><span class="sxs-lookup"><span data-stu-id="0f2e3-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="0f2e3-149">Kun kustannustapahtumat tuodaan lähdetiedoista, niille asetetaan kustannuslaskennassa oletusarvoisesti **Luokittelematon** -kustannustoimintaluokka.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="0f2e3-150">Voit luokitella kustannustapahtumia uudelleen **kiinteäksi kustannukseksi** tai **muuttuvaksi kustannukseksi** kustannustoiminnan käytäntösäännöillä.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="0f2e3-151">Määritä kustannustoiminnan sääntö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-151">Define the cost behavior rule</span></span>

<span data-ttu-id="0f2e3-152">Joissain tapauksissa osa kustannuksesta on kiinteä ja loppuosa perustuu kulutukseen.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="0f2e3-153">Sähkölaskut sopivat usein tähän määritelmään.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="0f2e3-154">Maksat ensin määrätyn, kiinteän maksun, jonka lisäksi maksat kulutuksesta kilowattitunteina (kWh).</span><span class="sxs-lookup"><span data-stu-id="0f2e3-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="0f2e3-155">Jos kiinteä maksu on esimerkiksi 1 000,00, kustannustoiminnan sääntö määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="0f2e3-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="0f2e3-156">Kiinteä määrä 1 000,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="0f2e3-157">0 &lt;= 1 000,00 = Kiinteä</span><span class="sxs-lookup"><span data-stu-id="0f2e3-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="0f2e3-158">1000,01 &lt; N = Muuttuva</span><span class="sxs-lookup"><span data-stu-id="0f2e3-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="0f2e3-159">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="0f2e3-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0f2e3-160">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="0f2e3-160">Journal</span></span></th>
<th><span data-ttu-id="0f2e3-161">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="0f2e3-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="0f2e3-162">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="0f2e3-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="0f2e3-163">Versio</span><span class="sxs-lookup"><span data-stu-id="0f2e3-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-164">00001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-164">00001</span></span></td>
<td><span data-ttu-id="0f2e3-165">Kustannustoiminnan laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="0f2e3-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="0f2e3-166">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="0f2e3-166">Fiscal</span></span></td>
<td><span data-ttu-id="0f2e3-167">2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-167">2017</span></span></td>
<td><span data-ttu-id="0f2e3-168">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-168">Period 1</span></span></td>
<td><span data-ttu-id="0f2e3-169">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="0f2e3-170">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0f2e3-171">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="0f2e3-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="0f2e3-172">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="0f2e3-173">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="0f2e3-173">Cost element</span></span></th>
<th><span data-ttu-id="0f2e3-174">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="0f2e3-174">Cost behavior</span></span></th>
<th><span data-ttu-id="0f2e3-175">Summa</span><span class="sxs-lookup"><span data-stu-id="0f2e3-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-176">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="0f2e3-177">CC099</span><span class="sxs-lookup"><span data-stu-id="0f2e3-177">CC099</span></span></td>
<td><span data-ttu-id="0f2e3-178">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="0f2e3-178">Default cost center</span></span></td>
<td><span data-ttu-id="0f2e3-179">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-179">10001</span></span></td>
<td><span data-ttu-id="0f2e3-180">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-180">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-181">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="0f2e3-181">Unclassified</span></span></td>
<td><span data-ttu-id="0f2e3-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="0f2e3-183">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="0f2e3-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0f2e3-184">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="0f2e3-185">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="0f2e3-185">Cost element</span></span></th>
<th><span data-ttu-id="0f2e3-186">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="0f2e3-186">Cost behavior</span></span></th>
<th><span data-ttu-id="0f2e3-187">Summa</span><span class="sxs-lookup"><span data-stu-id="0f2e3-187">Amount</span></span></th>
<th><span data-ttu-id="0f2e3-188">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="0f2e3-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-189">CC099</span><span class="sxs-lookup"><span data-stu-id="0f2e3-189">CC099</span></span></td>
<td><span data-ttu-id="0f2e3-190">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="0f2e3-190">Default cost center</span></span></td>
<td><span data-ttu-id="0f2e3-191">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-191">10001</span></span></td>
<td><span data-ttu-id="0f2e3-192">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-192">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-193">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="0f2e3-193">Unclassified</span></span></td>
<td><span data-ttu-id="0f2e3-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-194">10,000.00</span></span></td>
<td><span data-ttu-id="0f2e3-195">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-196">CC099</span><span class="sxs-lookup"><span data-stu-id="0f2e3-196">CC099</span></span></td>
<td><span data-ttu-id="0f2e3-197">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="0f2e3-197">Default cost center</span></span></td>
<td><span data-ttu-id="0f2e3-198">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-198">10001</span></span></td>
<td><span data-ttu-id="0f2e3-199">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-199">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-200">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="0f2e3-200">Unclassified</span></span></td>
<td><span data-ttu-id="0f2e3-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-201">-10,000.00</span></span></td>
<td><span data-ttu-id="0f2e3-202">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-203">CC099</span><span class="sxs-lookup"><span data-stu-id="0f2e3-203">CC099</span></span></td>
<td><span data-ttu-id="0f2e3-204">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="0f2e3-204">Default cost center</span></span></td>
<td><span data-ttu-id="0f2e3-205">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-205">10001</span></span></td>
<td><span data-ttu-id="0f2e3-206">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-206">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-207">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-207">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-208">1,000.00</span></span></td>
<td><span data-ttu-id="0f2e3-209">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-210">CC099</span><span class="sxs-lookup"><span data-stu-id="0f2e3-210">CC099</span></span></td>
<td><span data-ttu-id="0f2e3-211">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="0f2e3-211">Default cost center</span></span></td>
<td><span data-ttu-id="0f2e3-212">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-212">10001</span></span></td>
<td><span data-ttu-id="0f2e3-213">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-213">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-214">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-214">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-215">9,000.00</span></span></td>
<td><span data-ttu-id="0f2e3-216">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0f2e3-217">Lisätietoja on kohdassa [Kustannustoimintakäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="0f2e3-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="0f2e3-218">Vaihe 2: Käsittele kustannusten jaon laskenta</span><span class="sxs-lookup"><span data-stu-id="0f2e3-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="0f2e3-219">Kustannusten jakoa käytetään kustannusten jakamiseen yhdestä kustannusobjektista toiseen (tai useampaan kustannusobjektiin) määrittämällä asiaankuuluvan kohdistusperusteen.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="0f2e3-220">Kustannusten jako ja kustannusten kohdistus eroavat toisistaan sillä, että kustannusten jako tapahtuu aina alkuperäisen kustannuksen ensisijaisen kustannuselementin tasolla.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="0f2e3-221">Määritä kustannusten jaon sääntö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-221">Define the cost distribution rule</span></span>

<span data-ttu-id="0f2e3-222">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="0f2e3-223">Kustannuslaskenta ei tarjoa tästä tarpeeksi tarkkoja tietoja.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="0f2e3-224">Muuttuva kustannus tulisi jakaa yksittäisille kustannusobjekteille reiluin perustein.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="0f2e3-225">Loogisin kohdistusperuste on sähkönkulutus (kWh).</span><span class="sxs-lookup"><span data-stu-id="0f2e3-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="0f2e3-226">Luodaan tilastollinen dimensionjäsen nimeltä Sähkö, johon kirjataan sähkönkulutus.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="0f2e3-227">Oletusarvon mukaan kaikki tilastolliset dimensiojäsenet ovat käytettävissä kohdistusperusteina.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0f2e3-228">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-228">Cost object</span></span></th>
<th><span data-ttu-id="0f2e3-229">kWh</span><span class="sxs-lookup"><span data-stu-id="0f2e3-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-230">CC001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-230">CC001</span></span></td>
<td><span data-ttu-id="0f2e3-231">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="0f2e3-231">HR</span></span></td>
<td><span data-ttu-id="0f2e3-232">1 000</span><span class="sxs-lookup"><span data-stu-id="0f2e3-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-233">CC002</span><span class="sxs-lookup"><span data-stu-id="0f2e3-233">CC002</span></span></td>
<td><span data-ttu-id="0f2e3-234">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="0f2e3-234">Finance</span></span></td>
<td><span data-ttu-id="0f2e3-235">6,000</span><span class="sxs-lookup"><span data-stu-id="0f2e3-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-236">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-236">CC003</span></span></td>
<td><span data-ttu-id="0f2e3-237">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="0f2e3-237">Assembly</span></span></td>
<td><span data-ttu-id="0f2e3-238">0</span><span class="sxs-lookup"><span data-stu-id="0f2e3-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0f2e3-239">Seuraavassa taulukossa on esitetty tulos, kun sähkönkulutusta käytetään kohdistusperusteena muuttuville kuluille.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0f2e3-240">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-240">Cost object</span></span></th>
<th><span data-ttu-id="0f2e3-241">Suuruus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-241">Magnitude</span></span></th>
<th><span data-ttu-id="0f2e3-242">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="0f2e3-242">Allocation factor</span></span></th>
<th><span data-ttu-id="0f2e3-243">Summa</span><span class="sxs-lookup"><span data-stu-id="0f2e3-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-244">CC001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-244">CC001</span></span></td>
<td><span data-ttu-id="0f2e3-245">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="0f2e3-245">HR</span></span></td>
<td><span data-ttu-id="0f2e3-246">1 000</span><span class="sxs-lookup"><span data-stu-id="0f2e3-246">1,000</span></span></td>
<td><span data-ttu-id="0f2e3-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="0f2e3-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="0f2e3-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-249">CC002</span><span class="sxs-lookup"><span data-stu-id="0f2e3-249">CC002</span></span></td>
<td><span data-ttu-id="0f2e3-250">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="0f2e3-250">Finance</span></span></td>
<td><span data-ttu-id="0f2e3-251">6,000</span><span class="sxs-lookup"><span data-stu-id="0f2e3-251">6,000</span></span></td>
<td><span data-ttu-id="0f2e3-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="0f2e3-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="0f2e3-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-254">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-254">CC003</span></span></td>
<td><span data-ttu-id="0f2e3-255">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="0f2e3-255">Assembly</span></span></td>
<td><span data-ttu-id="0f2e3-256">0</span><span class="sxs-lookup"><span data-stu-id="0f2e3-256">0</span></span></td>
<td><span data-ttu-id="0f2e3-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="0f2e3-258">0,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0f2e3-259">Kiinteä kustannus tulisi jakaa tasaisesti yksittäisille kustannusobjekteille, jotka ovat kuluttaneet sähköä.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="0f2e3-260">Voit käyttää sähkön tilastollista dimensiojäsentä kaavan kohdistusperusteena tämän tavoitteen saavuttamiseksi: (sähkö &gt;0,00) Seuraavassa taulukossa on esitetty tulos siitä, kun sähkönkulutus on määritetty muuttuvien kustannusten kohdistusperusteeksi.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0f2e3-261">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-261">Cost object</span></span></th>
<th><span data-ttu-id="0f2e3-262">Resepti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-262">Formula</span></span></th>
<th><span data-ttu-id="0f2e3-263">Suuruus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-263">Magnitude</span></span></th>
<th><span data-ttu-id="0f2e3-264">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="0f2e3-264">Allocation factor</span></span></th>
<th><span data-ttu-id="0f2e3-265">Summa</span><span class="sxs-lookup"><span data-stu-id="0f2e3-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-266">CC001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-266">CC001</span></span></td>
<td><span data-ttu-id="0f2e3-267">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="0f2e3-267">HR</span></span></td>
<td><span data-ttu-id="0f2e3-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="0f2e3-269">1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-269">1</span></span></td>
<td><span data-ttu-id="0f2e3-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="0f2e3-271">500,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-272">CC002</span><span class="sxs-lookup"><span data-stu-id="0f2e3-272">CC002</span></span></td>
<td><span data-ttu-id="0f2e3-273">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="0f2e3-273">Finance</span></span></td>
<td><span data-ttu-id="0f2e3-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="0f2e3-275">1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-275">1</span></span></td>
<td><span data-ttu-id="0f2e3-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="0f2e3-277">500,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-278">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-278">CC003</span></span></td>
<td><span data-ttu-id="0f2e3-279">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="0f2e3-279">Assembly</span></span></td>
<td><span data-ttu-id="0f2e3-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="0f2e3-281">0</span><span class="sxs-lookup"><span data-stu-id="0f2e3-281">0</span></span></td>
<td><span data-ttu-id="0f2e3-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="0f2e3-283">0,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="0f2e3-284">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="0f2e3-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0f2e3-285">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="0f2e3-285">Journal</span></span></th>
<th><span data-ttu-id="0f2e3-286">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="0f2e3-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="0f2e3-287">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="0f2e3-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="0f2e3-288">Versio</span><span class="sxs-lookup"><span data-stu-id="0f2e3-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-289">00002</span><span class="sxs-lookup"><span data-stu-id="0f2e3-289">00002</span></span></td>
<td><span data-ttu-id="0f2e3-290">Kustannusten jaon laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="0f2e3-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="0f2e3-291">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="0f2e3-291">Fiscal</span></span></td>
<td><span data-ttu-id="0f2e3-292">2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-292">2017</span></span></td>
<td><span data-ttu-id="0f2e3-293">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-293">Period 1</span></span></td>
<td><span data-ttu-id="0f2e3-294">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="0f2e3-295">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0f2e3-296">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="0f2e3-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="0f2e3-297">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="0f2e3-298">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="0f2e3-298">Cost element</span></span></th>
<th><span data-ttu-id="0f2e3-299">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="0f2e3-299">Cost behavior</span></span></th>
<th><span data-ttu-id="0f2e3-300">Summa</span><span class="sxs-lookup"><span data-stu-id="0f2e3-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-301">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="0f2e3-302">CC099</span><span class="sxs-lookup"><span data-stu-id="0f2e3-302">CC099</span></span></td>
<td><span data-ttu-id="0f2e3-303">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="0f2e3-303">Default cost center</span></span></td>
<td><span data-ttu-id="0f2e3-304">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-304">10001</span></span></td>
<td><span data-ttu-id="0f2e3-305">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-305">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-306">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-306">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-308">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="0f2e3-309">CC099</span><span class="sxs-lookup"><span data-stu-id="0f2e3-309">CC099</span></span></td>
<td><span data-ttu-id="0f2e3-310">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="0f2e3-310">Default cost center</span></span></td>
<td><span data-ttu-id="0f2e3-311">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-311">10001</span></span></td>
<td><span data-ttu-id="0f2e3-312">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-312">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-313">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-313">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="0f2e3-315">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="0f2e3-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0f2e3-316">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="0f2e3-317">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="0f2e3-317">Cost element</span></span></th>
<th><span data-ttu-id="0f2e3-318">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="0f2e3-318">Cost behavior</span></span></th>
<th><span data-ttu-id="0f2e3-319">Summa</span><span class="sxs-lookup"><span data-stu-id="0f2e3-319">Amount</span></span></th>
<th><span data-ttu-id="0f2e3-320">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="0f2e3-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-321">CC099</span><span class="sxs-lookup"><span data-stu-id="0f2e3-321">CC099</span></span></td>
<td><span data-ttu-id="0f2e3-322">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="0f2e3-322">Default cost center</span></span></td>
<td><span data-ttu-id="0f2e3-323">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-323">10001</span></span></td>
<td><span data-ttu-id="0f2e3-324">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-324">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-325">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-325">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-326">-1,000.00</span></span></td>
<td><span data-ttu-id="0f2e3-327">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-328">CC001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-328">CC001</span></span></td>
<td><span data-ttu-id="0f2e3-329">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="0f2e3-329">HR</span></span></td>
<td><span data-ttu-id="0f2e3-330">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-330">10001</span></span></td>
<td><span data-ttu-id="0f2e3-331">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-331">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-332">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-332">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-333">500,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-333">500.00</span></span></td>
<td><span data-ttu-id="0f2e3-334">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-335">CC002</span><span class="sxs-lookup"><span data-stu-id="0f2e3-335">CC002</span></span></td>
<td><span data-ttu-id="0f2e3-336">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="0f2e3-336">Finance</span></span></td>
<td><span data-ttu-id="0f2e3-337">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-337">10001</span></span></td>
<td><span data-ttu-id="0f2e3-338">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-338">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-339">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-339">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-340">500,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-340">500.00</span></span></td>
<td><span data-ttu-id="0f2e3-341">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-342">CC099</span><span class="sxs-lookup"><span data-stu-id="0f2e3-342">CC099</span></span></td>
<td><span data-ttu-id="0f2e3-343">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="0f2e3-343">Default cost center</span></span></td>
<td><span data-ttu-id="0f2e3-344">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-344">10001</span></span></td>
<td><span data-ttu-id="0f2e3-345">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-345">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-346">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-346">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-347">-9,000.00</span></span></td>
<td><span data-ttu-id="0f2e3-348">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-349">CC001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-349">CC001</span></span></td>
<td><span data-ttu-id="0f2e3-350">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="0f2e3-350">HR</span></span></td>
<td><span data-ttu-id="0f2e3-351">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-351">10001</span></span></td>
<td><span data-ttu-id="0f2e3-352">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-352">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-353">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-353">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="0f2e3-354">1,285.71</span></span></td>
<td><span data-ttu-id="0f2e3-355">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-356">CC002</span><span class="sxs-lookup"><span data-stu-id="0f2e3-356">CC002</span></span></td>
<td><span data-ttu-id="0f2e3-357">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="0f2e3-357">Finance</span></span></td>
<td><span data-ttu-id="0f2e3-358">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-358">10001</span></span></td>
<td><span data-ttu-id="0f2e3-359">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-359">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-360">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-360">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="0f2e3-361">7,714.29</span></span></td>
<td><span data-ttu-id="0f2e3-362">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0f2e3-363">Lisätietoja on kohdassa [Jakelukäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="0f2e3-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="0f2e3-364">Vaihe 3: Käsittele yleiskustannustason laskenta</span><span class="sxs-lookup"><span data-stu-id="0f2e3-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="0f2e3-365">Yleiskustannustasolla veloitetaan yksi tai useampi määrätty kustannusobjekti.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="0f2e3-366">Veloitus perustuu ennalta määrättyyn kustannustasoon sekä määritetyn kohdistusperusteen suuruuteen.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="0f2e3-367">Määritä yleiskustannustaso.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-367">Define the overhead rate</span></span>

<span data-ttu-id="0f2e3-368">Kustannusobjekti CC001 HR vaikuttaa joukkoon sisäisiä projekteja.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="0f2e3-369">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon projektit.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0f2e3-370">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-370">Cost object</span></span></th>
<th><span data-ttu-id="0f2e3-371">Tunnit</span><span class="sxs-lookup"><span data-stu-id="0f2e3-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-372">Proj 1</span></span></td>
<td><span data-ttu-id="0f2e3-373">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-373">Project 1</span></span></td>
<td><span data-ttu-id="0f2e3-374">3</span><span class="sxs-lookup"><span data-stu-id="0f2e3-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-375">Proj 2</span></span></td>
<td><span data-ttu-id="0f2e3-376">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-376">Project 2</span></span></td>
<td><span data-ttu-id="0f2e3-377">1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0f2e3-378">Kustannusprojektien osuudelle on määritetty ennalta kustannushinta.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0f2e3-379">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-379">Cost object</span></span></th>
<th><span data-ttu-id="0f2e3-380">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="0f2e3-380">Cost element</span></span></th>
<th><span data-ttu-id="0f2e3-381">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="0f2e3-381">Cost behavior</span></span></th>
<th><span data-ttu-id="0f2e3-382">Yksiköt</span><span class="sxs-lookup"><span data-stu-id="0f2e3-382">Units</span></span></th>
<th><span data-ttu-id="0f2e3-383">Osuus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-384">CC001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-384">CC001</span></span></td>
<td><span data-ttu-id="0f2e3-385">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="0f2e3-385">HR</span></span></td>
<td><span data-ttu-id="0f2e3-386">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-386">10001</span></span></td>
<td><span data-ttu-id="0f2e3-387">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-387">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-388">1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-388">1</span></span></td>
<td><span data-ttu-id="0f2e3-389">10</span><span class="sxs-lookup"><span data-stu-id="0f2e3-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0f2e3-390">Seuraavassa taulukossa on esitetty tulos, kun Henkilöstöhallinnon projekteja käytetään kohdistusperusteena.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0f2e3-391">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-391">Cost object</span></span></th>
<th><span data-ttu-id="0f2e3-392">Suuruus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-392">Magnitude</span></span></th>
<th><span data-ttu-id="0f2e3-393">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="0f2e3-393">Cost element</span></span></th>
<th><span data-ttu-id="0f2e3-394">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="0f2e3-394">Allocation factor</span></span></th>
<th><span data-ttu-id="0f2e3-395">Summa</span><span class="sxs-lookup"><span data-stu-id="0f2e3-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-396">Proj 1</span></span></td>
<td><span data-ttu-id="0f2e3-397">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-397">Project 1</span></span></td>
<td><span data-ttu-id="0f2e3-398">3</span><span class="sxs-lookup"><span data-stu-id="0f2e3-398">3</span></span></td>
<td><span data-ttu-id="0f2e3-399">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-399">10001</span></span></td>
<td><span data-ttu-id="0f2e3-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="0f2e3-401">30,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-402">Proj 2</span></span></td>
<td><span data-ttu-id="0f2e3-403">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-403">Project 2</span></span></td>
<td><span data-ttu-id="0f2e3-404">1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-404">1</span></span></td>
<td><span data-ttu-id="0f2e3-405">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-405">10001</span></span></td>
<td><span data-ttu-id="0f2e3-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="0f2e3-407">10,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="0f2e3-408">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="0f2e3-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0f2e3-409">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="0f2e3-409">Journal</span></span></th>
<th><span data-ttu-id="0f2e3-410">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="0f2e3-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="0f2e3-411">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="0f2e3-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="0f2e3-412">Versio</span><span class="sxs-lookup"><span data-stu-id="0f2e3-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-413">00003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-413">00003</span></span></td>
<td><span data-ttu-id="0f2e3-414">Yleiskustannustason laskelman kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="0f2e3-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="0f2e3-415">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="0f2e3-415">Fiscal</span></span></td>
<td><span data-ttu-id="0f2e3-416">2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-416">2017</span></span></td>
<td><span data-ttu-id="0f2e3-417">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-417">Period 1</span></span></td>
<td><span data-ttu-id="0f2e3-418">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="0f2e3-419">Kirjauskansioviennit (Yleiskustannustason laskennan kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0f2e3-420">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="0f2e3-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="0f2e3-421">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-421">Cost object</span></span></th>
<th><span data-ttu-id="0f2e3-422">Suuruus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-423">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="0f2e3-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-424">Proj 1</span></span></td>
<td><span data-ttu-id="0f2e3-425">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="0f2e3-426">3,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-427">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="0f2e3-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-428">Proj 2</span></span></td>
<td><span data-ttu-id="0f2e3-429">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="0f2e3-430">1,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="0f2e3-431">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="0f2e3-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0f2e3-432">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="0f2e3-433">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="0f2e3-433">Cost element</span></span></th>
<th><span data-ttu-id="0f2e3-434">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="0f2e3-434">Cost behavior</span></span></th>
<th><span data-ttu-id="0f2e3-435">Summa</span><span class="sxs-lookup"><span data-stu-id="0f2e3-435">Amount</span></span></th>
<th><span data-ttu-id="0f2e3-436">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="0f2e3-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-437">CC0001</span></span></td>
<td><span data-ttu-id="0f2e3-438">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="0f2e3-438">HR</span></span></td>
<td><span data-ttu-id="0f2e3-439">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-439">10001</span></span></td>
<td><span data-ttu-id="0f2e3-440">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-440">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-441">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-441">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-442">-30.00</span></span></td>
<td><span data-ttu-id="0f2e3-443">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-444">Proj 1</span></span></td>
<td><span data-ttu-id="0f2e3-445">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="0f2e3-446">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-446">10001</span></span></td>
<td><span data-ttu-id="0f2e3-447">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-447">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-448">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-448">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-449">30,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-449">30.00</span></span></td>
<td><span data-ttu-id="0f2e3-450">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-451">CC001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-451">CC001</span></span></td>
<td><span data-ttu-id="0f2e3-452">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="0f2e3-452">HR</span></span></td>
<td><span data-ttu-id="0f2e3-453">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-453">10001</span></span></td>
<td><span data-ttu-id="0f2e3-454">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-454">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-455">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-455">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-456">-10.00</span></span></td>
<td><span data-ttu-id="0f2e3-457">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-458">Proj 2</span></span></td>
<td><span data-ttu-id="0f2e3-459">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="0f2e3-460">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-460">10001</span></span></td>
<td><span data-ttu-id="0f2e3-461">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-461">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-462">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-462">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-463">10.00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-463">10.00</span></span></td>
<td><span data-ttu-id="0f2e3-464">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0f2e3-465">Lisätietoja on kohdassa [Yleisen laskennan suorittaminen](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="0f2e3-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="0f2e3-466">Vaihe 4: Käsittele kustannusten kohdistuksen laskenta</span><span class="sxs-lookup"><span data-stu-id="0f2e3-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="0f2e3-467">Kohdistuksella kustannusobjektin saldo liitetään toisiin kustannusobjekteihin käyttämällä kohdistusperustetta.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="0f2e3-468">Finance tukee vastavuoroista kohdistusmenetelmää.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="0f2e3-469">Vastavuoroisessa kohdistusmenetelmässä tunnistetaan oheiskustannusobjektien käyttämät, keskinäiset palvelut täysin.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="0f2e3-470">Järjestelmä määrittää oikean kohdistusjärjestyksen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="0f2e3-471">Kustannusobjektin saldo kohdistetaan yhdellä kohdistusperusteella.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="0f2e3-472">Kustannusobjektien dimensiot ja niiden vastaavat jäsenet ylittävät kohdistukset ovat tuettuja.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="0f2e3-473">Kustannusseurantayksikkö hallitsee kohdistusjärjestystä.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="0f2e3-474">[![Vastavuoroinen menetelmä](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="0f2e3-475">Määritä kustannuksen kohdistus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-475">Define the cost allocation</span></span>

<span data-ttu-id="0f2e3-476">Tämä on yksinkertainen esimerkki, jossa kerrotaan, miten voit jäljittää kustannuksen virran.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="0f2e3-477">Kustannusobjekti CC001 HR liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="0f2e3-478">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0f2e3-479">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-479">Cost object</span></span></th>
<th><span data-ttu-id="0f2e3-480">HR-palvelut</span><span class="sxs-lookup"><span data-stu-id="0f2e3-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-481">CC002</span><span class="sxs-lookup"><span data-stu-id="0f2e3-481">CC002</span></span></td>
<td><span data-ttu-id="0f2e3-482">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="0f2e3-482">Finance</span></span></td>
<td><span data-ttu-id="0f2e3-483">35</span><span class="sxs-lookup"><span data-stu-id="0f2e3-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-484">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-484">CC003</span></span></td>
<td><span data-ttu-id="0f2e3-485">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="0f2e3-485">Assembly</span></span></td>
<td><span data-ttu-id="0f2e3-486">55</span><span class="sxs-lookup"><span data-stu-id="0f2e3-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-487">CC004</span><span class="sxs-lookup"><span data-stu-id="0f2e3-487">CC004</span></span></td>
<td><span data-ttu-id="0f2e3-488">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-488">Packaging</span></span></td>
<td><span data-ttu-id="0f2e3-489">10</span><span class="sxs-lookup"><span data-stu-id="0f2e3-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0f2e3-490">Kustannusobjekti CC002 Taloushallinto liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="0f2e3-491">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Taloushallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0f2e3-492">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-492">Cost object</span></span></th>
<th><span data-ttu-id="0f2e3-493">Taloushallinnon palvelut</span><span class="sxs-lookup"><span data-stu-id="0f2e3-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-494">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-494">CC003</span></span></td>
<td><span data-ttu-id="0f2e3-495">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="0f2e3-495">Assembly</span></span></td>
<td><span data-ttu-id="0f2e3-496">65</span><span class="sxs-lookup"><span data-stu-id="0f2e3-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-497">CC004</span><span class="sxs-lookup"><span data-stu-id="0f2e3-497">CC004</span></span></td>
<td><span data-ttu-id="0f2e3-498">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-498">Packaging</span></span></td>
<td><span data-ttu-id="0f2e3-499">35</span><span class="sxs-lookup"><span data-stu-id="0f2e3-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0f2e3-500">Kustannusobjekti CC003 Kokoonpano liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="0f2e3-501">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Kokoonpanopalvelut.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0f2e3-502">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-502">Cost object</span></span></th>
<th><span data-ttu-id="0f2e3-503">Kokoonpanopalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-504">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-504">Prod 1</span></span></td>
<td><span data-ttu-id="0f2e3-505">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-505">Product 1</span></span></td>
<td><span data-ttu-id="0f2e3-506">60</span><span class="sxs-lookup"><span data-stu-id="0f2e3-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-507">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-507">Prod 2</span></span></td>
<td><span data-ttu-id="0f2e3-508">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-508">Product 2</span></span></td>
<td><span data-ttu-id="0f2e3-509">20</span><span class="sxs-lookup"><span data-stu-id="0f2e3-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0f2e3-510">Kustannusobjekti CC004 Pakkaus liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="0f2e3-511">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Pakkauspalvelut.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0f2e3-512">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-512">Cost object</span></span></th>
<th><span data-ttu-id="0f2e3-513">Pakkauspalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-514">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-514">Prod 1</span></span></td>
<td><span data-ttu-id="0f2e3-515">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-515">Product 1</span></span></td>
<td><span data-ttu-id="0f2e3-516">80</span><span class="sxs-lookup"><span data-stu-id="0f2e3-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-517">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-517">Prod 2</span></span></td>
<td><span data-ttu-id="0f2e3-518">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-518">Product 2</span></span></td>
<td><span data-ttu-id="0f2e3-519">15</span><span class="sxs-lookup"><span data-stu-id="0f2e3-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="0f2e3-520">Tilastomittaukset, kuten tämän tuotteen kuluttamat tuotantotunnit, voidaan johtaa lähdetiedoista.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="0f2e3-521">Lisätietoja on kohdassa [Tilastomittauksen lähdemalli](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="0f2e3-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="0f2e3-522">Seuraavassa taulukossa näytetään tulos, kun henkilöstöhallinnon palveluja käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="0f2e3-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0f2e3-523">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-523">Cost object</span></span></th>
<th><span data-ttu-id="0f2e3-524">Suuruus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-524">Magnitude</span></span></th>
<th><span data-ttu-id="0f2e3-525">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="0f2e3-525">Allocation factor</span></span></th>
<th><span data-ttu-id="0f2e3-526">Summa</span><span class="sxs-lookup"><span data-stu-id="0f2e3-526">Amount</span></span></th>
<th><span data-ttu-id="0f2e3-527">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="0f2e3-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-528">CC002</span><span class="sxs-lookup"><span data-stu-id="0f2e3-528">CC002</span></span></td>
<td><span data-ttu-id="0f2e3-529">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="0f2e3-529">Finance</span></span></td>
<td><span data-ttu-id="0f2e3-530">35</span><span class="sxs-lookup"><span data-stu-id="0f2e3-530">35</span></span></td>
<td><span data-ttu-id="0f2e3-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="0f2e3-532">175.00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-532">175.00</span></span></td>
<td><span data-ttu-id="0f2e3-533">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-534">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-534">CC003</span></span></td>
<td><span data-ttu-id="0f2e3-535">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="0f2e3-535">Assembly</span></span></td>
<td><span data-ttu-id="0f2e3-536">55</span><span class="sxs-lookup"><span data-stu-id="0f2e3-536">55</span></span></td>
<td><span data-ttu-id="0f2e3-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="0f2e3-538">275.00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-538">275.00</span></span></td>
<td><span data-ttu-id="0f2e3-539">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-540">CC004</span><span class="sxs-lookup"><span data-stu-id="0f2e3-540">CC004</span></span></td>
<td><span data-ttu-id="0f2e3-541">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-541">Packaging</span></span></td>
<td><span data-ttu-id="0f2e3-542">10</span><span class="sxs-lookup"><span data-stu-id="0f2e3-542">10</span></span></td>
<td><span data-ttu-id="0f2e3-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="0f2e3-544">50,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-544">50.00</span></span></td>
<td><span data-ttu-id="0f2e3-545">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-546">CC002</span><span class="sxs-lookup"><span data-stu-id="0f2e3-546">CC002</span></span></td>
<td><span data-ttu-id="0f2e3-547">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="0f2e3-547">Finance</span></span></td>
<td><span data-ttu-id="0f2e3-548">35</span><span class="sxs-lookup"><span data-stu-id="0f2e3-548">35</span></span></td>
<td><span data-ttu-id="0f2e3-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="0f2e3-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="0f2e3-550">436.00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-550">436.00</span></span></td>
<td><span data-ttu-id="0f2e3-551">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-552">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-552">CC003</span></span></td>
<td><span data-ttu-id="0f2e3-553">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="0f2e3-553">Assembly</span></span></td>
<td><span data-ttu-id="0f2e3-554">55</span><span class="sxs-lookup"><span data-stu-id="0f2e3-554">55</span></span></td>
<td><span data-ttu-id="0f2e3-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="0f2e3-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="0f2e3-556">685.14</span><span class="sxs-lookup"><span data-stu-id="0f2e3-556">685.14</span></span></td>
<td><span data-ttu-id="0f2e3-557">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-558">CC004</span><span class="sxs-lookup"><span data-stu-id="0f2e3-558">CC004</span></span></td>
<td><span data-ttu-id="0f2e3-559">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-559">Packaging</span></span></td>
<td><span data-ttu-id="0f2e3-560">10</span><span class="sxs-lookup"><span data-stu-id="0f2e3-560">10</span></span></td>
<td><span data-ttu-id="0f2e3-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="0f2e3-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="0f2e3-562">124.57</span><span class="sxs-lookup"><span data-stu-id="0f2e3-562">124.57</span></span></td>
<td><span data-ttu-id="0f2e3-563">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0f2e3-564">Seuraavassa taulukossa näytetään tulos, kun Taloushallinnon palveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="0f2e3-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0f2e3-565">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-565">Cost object</span></span></th>
<th><span data-ttu-id="0f2e3-566">Suuruus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-566">Magnitude</span></span></th>
<th><span data-ttu-id="0f2e3-567">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="0f2e3-567">Allocation factor</span></span></th>
<th><span data-ttu-id="0f2e3-568">Summa</span><span class="sxs-lookup"><span data-stu-id="0f2e3-568">Amount</span></span></th>
<th><span data-ttu-id="0f2e3-569">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="0f2e3-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-570">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-570">CC003</span></span></td>
<td><span data-ttu-id="0f2e3-571">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="0f2e3-571">Assembly</span></span></td>
<td><span data-ttu-id="0f2e3-572">65</span><span class="sxs-lookup"><span data-stu-id="0f2e3-572">65</span></span></td>
<td><span data-ttu-id="0f2e3-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="0f2e3-574">438.75</span><span class="sxs-lookup"><span data-stu-id="0f2e3-574">438.75</span></span></td>
<td><span data-ttu-id="0f2e3-575">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-576">CC004</span><span class="sxs-lookup"><span data-stu-id="0f2e3-576">CC004</span></span></td>
<td><span data-ttu-id="0f2e3-577">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-577">Packaging</span></span></td>
<td><span data-ttu-id="0f2e3-578">35</span><span class="sxs-lookup"><span data-stu-id="0f2e3-578">35</span></span></td>
<td><span data-ttu-id="0f2e3-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="0f2e3-580">236.25</span><span class="sxs-lookup"><span data-stu-id="0f2e3-580">236.25</span></span></td>
<td><span data-ttu-id="0f2e3-581">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-582">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-582">CC003</span></span></td>
<td><span data-ttu-id="0f2e3-583">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="0f2e3-583">Assembly</span></span></td>
<td><span data-ttu-id="0f2e3-584">65</span><span class="sxs-lookup"><span data-stu-id="0f2e3-584">65</span></span></td>
<td><span data-ttu-id="0f2e3-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="0f2e3-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="0f2e3-586">5,297.69</span></span></td>
<td><span data-ttu-id="0f2e3-587">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-588">CC004</span><span class="sxs-lookup"><span data-stu-id="0f2e3-588">CC004</span></span></td>
<td><span data-ttu-id="0f2e3-589">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-589">Packaging</span></span></td>
<td><span data-ttu-id="0f2e3-590">35</span><span class="sxs-lookup"><span data-stu-id="0f2e3-590">35</span></span></td>
<td><span data-ttu-id="0f2e3-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="0f2e3-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="0f2e3-592">2,852.60</span></span></td>
<td><span data-ttu-id="0f2e3-593">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0f2e3-594">Seuraavassa taulukossa näytetään tulos, kun Kokoonpanopalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="0f2e3-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0f2e3-595">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-595">Cost object</span></span></th>
<th><span data-ttu-id="0f2e3-596">Suuruus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-596">Magnitude</span></span></th>
<th><span data-ttu-id="0f2e3-597">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="0f2e3-597">Allocation factor</span></span></th>
<th><span data-ttu-id="0f2e3-598">Summa</span><span class="sxs-lookup"><span data-stu-id="0f2e3-598">Amount</span></span></th>
<th><span data-ttu-id="0f2e3-599">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="0f2e3-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-600">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-600">Prod 1</span></span></td>
<td><span data-ttu-id="0f2e3-601">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-601">Product 1</span></span></td>
<td><span data-ttu-id="0f2e3-602">60</span><span class="sxs-lookup"><span data-stu-id="0f2e3-602">60</span></span></td>
<td><span data-ttu-id="0f2e3-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="0f2e3-604">535.31</span><span class="sxs-lookup"><span data-stu-id="0f2e3-604">535.31</span></span></td>
<td><span data-ttu-id="0f2e3-605">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-606">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-606">Prod 2</span></span></td>
<td><span data-ttu-id="0f2e3-607">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-607">Product 2</span></span></td>
<td><span data-ttu-id="0f2e3-608">20</span><span class="sxs-lookup"><span data-stu-id="0f2e3-608">20</span></span></td>
<td><span data-ttu-id="0f2e3-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="0f2e3-610">178.44</span><span class="sxs-lookup"><span data-stu-id="0f2e3-610">178.44</span></span></td>
<td><span data-ttu-id="0f2e3-611">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-612">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-612">Prod 1</span></span></td>
<td><span data-ttu-id="0f2e3-613">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-613">Product 1</span></span></td>
<td><span data-ttu-id="0f2e3-614">60</span><span class="sxs-lookup"><span data-stu-id="0f2e3-614">60</span></span></td>
<td><span data-ttu-id="0f2e3-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="0f2e3-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="0f2e3-616">4,487.12</span></span></td>
<td><span data-ttu-id="0f2e3-617">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-618">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-618">Prod 2</span></span></td>
<td><span data-ttu-id="0f2e3-619">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-619">Product 2</span></span></td>
<td><span data-ttu-id="0f2e3-620">20</span><span class="sxs-lookup"><span data-stu-id="0f2e3-620">20</span></span></td>
<td><span data-ttu-id="0f2e3-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="0f2e3-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="0f2e3-622">1,495.71</span></span></td>
<td><span data-ttu-id="0f2e3-623">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0f2e3-624">Seuraavassa taulukossa näytetään tulos, kun Pakkauspalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="0f2e3-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0f2e3-625">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-625">Cost object</span></span></th>
<th><span data-ttu-id="0f2e3-626">Suuruus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-626">Magnitude</span></span></th>
<th><span data-ttu-id="0f2e3-627">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="0f2e3-627">Allocation factor</span></span></th>
<th><span data-ttu-id="0f2e3-628">Summa</span><span class="sxs-lookup"><span data-stu-id="0f2e3-628">Amount</span></span></th>
<th><span data-ttu-id="0f2e3-629">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="0f2e3-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-630">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-630">Prod 1</span></span></td>
<td><span data-ttu-id="0f2e3-631">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-631">Product 1</span></span></td>
<td><span data-ttu-id="0f2e3-632">80</span><span class="sxs-lookup"><span data-stu-id="0f2e3-632">80</span></span></td>
<td><span data-ttu-id="0f2e3-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="0f2e3-634">241.05</span><span class="sxs-lookup"><span data-stu-id="0f2e3-634">241.05</span></span></td>
<td><span data-ttu-id="0f2e3-635">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-636">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-636">Prod 2</span></span></td>
<td><span data-ttu-id="0f2e3-637">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-637">Product 2</span></span></td>
<td><span data-ttu-id="0f2e3-638">15</span><span class="sxs-lookup"><span data-stu-id="0f2e3-638">15</span></span></td>
<td><span data-ttu-id="0f2e3-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="0f2e3-640">45.20</span><span class="sxs-lookup"><span data-stu-id="0f2e3-640">45.20</span></span></td>
<td><span data-ttu-id="0f2e3-641">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-642">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-642">Prod 1</span></span></td>
<td><span data-ttu-id="0f2e3-643">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-643">Product 1</span></span></td>
<td><span data-ttu-id="0f2e3-644">80</span><span class="sxs-lookup"><span data-stu-id="0f2e3-644">80</span></span></td>
<td><span data-ttu-id="0f2e3-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="0f2e3-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="0f2e3-646">2,507.09</span></span></td>
<td><span data-ttu-id="0f2e3-647">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-648">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-648">Prod 2</span></span></td>
<td><span data-ttu-id="0f2e3-649">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-649">Product 2</span></span></td>
<td><span data-ttu-id="0f2e3-650">15</span><span class="sxs-lookup"><span data-stu-id="0f2e3-650">15</span></span></td>
<td><span data-ttu-id="0f2e3-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="0f2e3-652">470.08</span><span class="sxs-lookup"><span data-stu-id="0f2e3-652">470.08</span></span></td>
<td><span data-ttu-id="0f2e3-653">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="0f2e3-654">Kirjauskansioviennit (kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0f2e3-655">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="0f2e3-655">Journal</span></span></th>
<th><span data-ttu-id="0f2e3-656">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="0f2e3-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="0f2e3-657">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="0f2e3-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="0f2e3-658">Versio</span><span class="sxs-lookup"><span data-stu-id="0f2e3-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-659">00004</span><span class="sxs-lookup"><span data-stu-id="0f2e3-659">00004</span></span></td>
<td><span data-ttu-id="0f2e3-660">Kustannusten kohdistuskirjauskansio</span><span class="sxs-lookup"><span data-stu-id="0f2e3-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="0f2e3-661">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="0f2e3-661">Fiscal</span></span></td>
<td><span data-ttu-id="0f2e3-662">2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-662">2017</span></span></td>
<td><span data-ttu-id="0f2e3-663">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-663">Period 1</span></span></td>
<td><span data-ttu-id="0f2e3-664">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="0f2e3-665">Kirjauskansion rivit</span><span class="sxs-lookup"><span data-stu-id="0f2e3-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0f2e3-666">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="0f2e3-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="0f2e3-667">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="0f2e3-668">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="0f2e3-668">Cost element</span></span></th>
<th><span data-ttu-id="0f2e3-669">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="0f2e3-669">Cost behavior</span></span></th>
<th><span data-ttu-id="0f2e3-670">Summa</span><span class="sxs-lookup"><span data-stu-id="0f2e3-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-671">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="0f2e3-672">CC001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-672">CC001</span></span></td>
<td><span data-ttu-id="0f2e3-673">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="0f2e3-673">HR</span></span></td>
<td><span data-ttu-id="0f2e3-674">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-674">10001</span></span></td>
<td><span data-ttu-id="0f2e3-675">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-675">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-676">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-676">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-677">500,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-678">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="0f2e3-679">CC001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-679">CC001</span></span></td>
<td><span data-ttu-id="0f2e3-680">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="0f2e3-680">HR</span></span></td>
<td><span data-ttu-id="0f2e3-681">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-681">10001</span></span></td>
<td><span data-ttu-id="0f2e3-682">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-682">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-683">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-683">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="0f2e3-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-685">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="0f2e3-686">CC002</span><span class="sxs-lookup"><span data-stu-id="0f2e3-686">CC002</span></span></td>
<td><span data-ttu-id="0f2e3-687">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="0f2e3-687">Finance</span></span></td>
<td><span data-ttu-id="0f2e3-688">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-688">10001</span></span></td>
<td><span data-ttu-id="0f2e3-689">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-689">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-690">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-690">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-691">675.00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-692">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="0f2e3-693">CC002</span><span class="sxs-lookup"><span data-stu-id="0f2e3-693">CC002</span></span></td>
<td><span data-ttu-id="0f2e3-694">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="0f2e3-694">Finance</span></span></td>
<td><span data-ttu-id="0f2e3-695">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-695">10001</span></span></td>
<td><span data-ttu-id="0f2e3-696">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-696">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-697">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-697">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="0f2e3-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-699">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="0f2e3-700">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-700">CC003</span></span></td>
<td><span data-ttu-id="0f2e3-701">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="0f2e3-701">Assembly</span></span></td>
<td><span data-ttu-id="0f2e3-702">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-702">10001</span></span></td>
<td><span data-ttu-id="0f2e3-703">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-703">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-704">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-704">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-705">713.75</span><span class="sxs-lookup"><span data-stu-id="0f2e3-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-706">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="0f2e3-707">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-707">CC003</span></span></td>
<td><span data-ttu-id="0f2e3-708">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="0f2e3-708">Assembly</span></span></td>
<td><span data-ttu-id="0f2e3-709">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-709">10001</span></span></td>
<td><span data-ttu-id="0f2e3-710">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-710">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-711">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-711">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="0f2e3-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-713">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="0f2e3-714">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-714">CC003</span></span></td>
<td><span data-ttu-id="0f2e3-715">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-715">Packaging</span></span></td>
<td><span data-ttu-id="0f2e3-716">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-716">10001</span></span></td>
<td><span data-ttu-id="0f2e3-717">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-717">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-718">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-718">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-719">286.25</span><span class="sxs-lookup"><span data-stu-id="0f2e3-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-720">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="0f2e3-721">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-721">CC003</span></span></td>
<td><span data-ttu-id="0f2e3-722">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-722">Packaging</span></span></td>
<td><span data-ttu-id="0f2e3-723">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-723">10001</span></span></td>
<td><span data-ttu-id="0f2e3-724">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-724">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-725">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-725">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="0f2e3-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-727">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="0f2e3-728">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-728">Prod 1</span></span></td>
<td><span data-ttu-id="0f2e3-729">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-729">Product 1</span></span></td>
<td><span data-ttu-id="0f2e3-730">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-730">10001</span></span></td>
<td><span data-ttu-id="0f2e3-731">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-731">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-732">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-732">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-733">776.36</span><span class="sxs-lookup"><span data-stu-id="0f2e3-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-734">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="0f2e3-735">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-735">Prod 1</span></span></td>
<td><span data-ttu-id="0f2e3-736">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-736">Product 1</span></span></td>
<td><span data-ttu-id="0f2e3-737">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-737">10001</span></span></td>
<td><span data-ttu-id="0f2e3-738">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-738">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-739">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-739">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="0f2e3-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-741">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="0f2e3-742">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-742">Prod 2</span></span></td>
<td><span data-ttu-id="0f2e3-743">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-743">Product 1</span></span></td>
<td><span data-ttu-id="0f2e3-744">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-744">10001</span></span></td>
<td><span data-ttu-id="0f2e3-745">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-745">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-746">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-746">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-747">223.64</span><span class="sxs-lookup"><span data-stu-id="0f2e3-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-748">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="0f2e3-749">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-749">Prod 2</span></span></td>
<td><span data-ttu-id="0f2e3-750">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-750">Product 1</span></span></td>
<td><span data-ttu-id="0f2e3-751">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-751">10001</span></span></td>
<td><span data-ttu-id="0f2e3-752">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-752">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-753">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-753">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="0f2e3-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="0f2e3-755">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="0f2e3-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0f2e3-756">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="0f2e3-757">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="0f2e3-757">Cost element</span></span></th>
<th><span data-ttu-id="0f2e3-758">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="0f2e3-758">Cost behavior</span></span></th>
<th><span data-ttu-id="0f2e3-759">Summa</span><span class="sxs-lookup"><span data-stu-id="0f2e3-759">Amount</span></span></th>
<th><span data-ttu-id="0f2e3-760">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="0f2e3-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f2e3-761">CC001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-761">CC001</span></span></td>
<td><span data-ttu-id="0f2e3-762">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="0f2e3-762">HR</span></span></td>
<td><span data-ttu-id="0f2e3-763">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-763">10001</span></span></td>
<td><span data-ttu-id="0f2e3-764">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-764">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-765">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-765">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-766">-500.00</span></span></td>
<td><span data-ttu-id="0f2e3-767">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-768">CC002</span><span class="sxs-lookup"><span data-stu-id="0f2e3-768">CC002</span></span></td>
<td><span data-ttu-id="0f2e3-769">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="0f2e3-769">Finance</span></span></td>
<td><span data-ttu-id="0f2e3-770">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-770">10001</span></span></td>
<td><span data-ttu-id="0f2e3-771">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-771">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-772">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-772">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-773">175.00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-773">175.00</span></span></td>
<td><span data-ttu-id="0f2e3-774">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-775">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-775">CC003</span></span></td>
<td><span data-ttu-id="0f2e3-776">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="0f2e3-776">Assembly</span></span></td>
<td><span data-ttu-id="0f2e3-777">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-777">10001</span></span></td>
<td><span data-ttu-id="0f2e3-778">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-778">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-779">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-779">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-780">275.00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-780">275.00</span></span></td>
<td><span data-ttu-id="0f2e3-781">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-782">CC004</span><span class="sxs-lookup"><span data-stu-id="0f2e3-782">CC004</span></span></td>
<td><span data-ttu-id="0f2e3-783">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-783">Packaging</span></span></td>
<td><span data-ttu-id="0f2e3-784">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-784">10001</span></span></td>
<td><span data-ttu-id="0f2e3-785">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-785">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-786">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-786">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-787">50,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-787">50,00</span></span></td>
<td><span data-ttu-id="0f2e3-788">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-789">CC001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-789">CC001</span></span></td>
<td><span data-ttu-id="0f2e3-790">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="0f2e3-790">HR</span></span></td>
<td><span data-ttu-id="0f2e3-791">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-791">10001</span></span></td>
<td><span data-ttu-id="0f2e3-792">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-792">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-793">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-793">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="0f2e3-794">-1,245.71</span></span></td>
<td><span data-ttu-id="0f2e3-795">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-796">CC002</span><span class="sxs-lookup"><span data-stu-id="0f2e3-796">CC002</span></span></td>
<td><span data-ttu-id="0f2e3-797">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="0f2e3-797">Finance</span></span></td>
<td><span data-ttu-id="0f2e3-798">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-798">10001</span></span></td>
<td><span data-ttu-id="0f2e3-799">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-799">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-800">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-800">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-801">436.00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-801">436.00</span></span></td>
<td><span data-ttu-id="0f2e3-802">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-803">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-803">CC003</span></span></td>
<td><span data-ttu-id="0f2e3-804">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="0f2e3-804">Assembly</span></span></td>
<td><span data-ttu-id="0f2e3-805">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-805">10001</span></span></td>
<td><span data-ttu-id="0f2e3-806">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-806">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-807">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-807">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-808">685.14</span><span class="sxs-lookup"><span data-stu-id="0f2e3-808">685.14</span></span></td>
<td><span data-ttu-id="0f2e3-809">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-810">CC004</span><span class="sxs-lookup"><span data-stu-id="0f2e3-810">CC004</span></span></td>
<td><span data-ttu-id="0f2e3-811">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-811">Packaging</span></span></td>
<td><span data-ttu-id="0f2e3-812">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-812">10001</span></span></td>
<td><span data-ttu-id="0f2e3-813">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-813">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-814">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-814">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-815">124.57</span><span class="sxs-lookup"><span data-stu-id="0f2e3-815">124.57</span></span></td>
<td><span data-ttu-id="0f2e3-816">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-817">CC002</span><span class="sxs-lookup"><span data-stu-id="0f2e3-817">CC002</span></span></td>
<td><span data-ttu-id="0f2e3-818">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="0f2e3-818">Finance</span></span></td>
<td><span data-ttu-id="0f2e3-819">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-819">10001</span></span></td>
<td><span data-ttu-id="0f2e3-820">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-820">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-821">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-821">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-822">-675.00</span></span></td>
<td><span data-ttu-id="0f2e3-823">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-824">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-824">CC003</span></span></td>
<td><span data-ttu-id="0f2e3-825">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="0f2e3-825">Assembly</span></span></td>
<td><span data-ttu-id="0f2e3-826">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-826">10001</span></span></td>
<td><span data-ttu-id="0f2e3-827">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-827">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-828">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-828">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-829">438.75</span><span class="sxs-lookup"><span data-stu-id="0f2e3-829">438.75</span></span></td>
<td><span data-ttu-id="0f2e3-830">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-831">CC004</span><span class="sxs-lookup"><span data-stu-id="0f2e3-831">CC004</span></span></td>
<td><span data-ttu-id="0f2e3-832">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-832">Packaging</span></span></td>
<td><span data-ttu-id="0f2e3-833">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-833">10001</span></span></td>
<td><span data-ttu-id="0f2e3-834">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-834">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-835">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-835">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-836">236.25</span><span class="sxs-lookup"><span data-stu-id="0f2e3-836">236.25</span></span></td>
<td><span data-ttu-id="0f2e3-837">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-838">CC002</span><span class="sxs-lookup"><span data-stu-id="0f2e3-838">CC002</span></span></td>
<td><span data-ttu-id="0f2e3-839">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="0f2e3-839">Finance</span></span></td>
<td><span data-ttu-id="0f2e3-840">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-840">10001</span></span></td>
<td><span data-ttu-id="0f2e3-841">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-841">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-842">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-842">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="0f2e3-843">-8,150.29</span></span></td>
<td><span data-ttu-id="0f2e3-844">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-845">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-845">CC003</span></span></td>
<td><span data-ttu-id="0f2e3-846">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="0f2e3-846">Assembly</span></span></td>
<td><span data-ttu-id="0f2e3-847">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-847">10001</span></span></td>
<td><span data-ttu-id="0f2e3-848">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-848">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-849">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-849">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="0f2e3-850">5,297.69</span></span></td>
<td><span data-ttu-id="0f2e3-851">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-852">CC004</span><span class="sxs-lookup"><span data-stu-id="0f2e3-852">CC004</span></span></td>
<td><span data-ttu-id="0f2e3-853">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-853">Packaging</span></span></td>
<td><span data-ttu-id="0f2e3-854">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-854">10001</span></span></td>
<td><span data-ttu-id="0f2e3-855">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-855">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-856">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-856">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="0f2e3-857">2,852.60</span></span></td>
<td><span data-ttu-id="0f2e3-858">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-859">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-859">CC003</span></span></td>
<td><span data-ttu-id="0f2e3-860">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="0f2e3-860">Assembly</span></span></td>
<td><span data-ttu-id="0f2e3-861">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-861">10001</span></span></td>
<td><span data-ttu-id="0f2e3-862">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-862">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-863">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-863">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="0f2e3-864">-713.75</span></span></td>
<td><span data-ttu-id="0f2e3-865">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-866">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-866">Prod 1</span></span></td>
<td><span data-ttu-id="0f2e3-867">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-867">Product 1</span></span></td>
<td><span data-ttu-id="0f2e3-868">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-868">10001</span></span></td>
<td><span data-ttu-id="0f2e3-869">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-869">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-870">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-870">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-871">535.31</span><span class="sxs-lookup"><span data-stu-id="0f2e3-871">535.31</span></span></td>
<td><span data-ttu-id="0f2e3-872">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-873">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-873">Prod 2</span></span></td>
<td><span data-ttu-id="0f2e3-874">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-874">Product 2</span></span></td>
<td><span data-ttu-id="0f2e3-875">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-875">10001</span></span></td>
<td><span data-ttu-id="0f2e3-876">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-876">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-877">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-877">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-878">178.44</span><span class="sxs-lookup"><span data-stu-id="0f2e3-878">178.44</span></span></td>
<td><span data-ttu-id="0f2e3-879">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-880">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-880">CC003</span></span></td>
<td><span data-ttu-id="0f2e3-881">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="0f2e3-881">Assembly</span></span></td>
<td><span data-ttu-id="0f2e3-882">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-882">10001</span></span></td>
<td><span data-ttu-id="0f2e3-883">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-883">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-884">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-884">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="0f2e3-885">-5,982.83</span></span></td>
<td><span data-ttu-id="0f2e3-886">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-887">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-887">Prod 1</span></span></td>
<td><span data-ttu-id="0f2e3-888">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-888">Product 1</span></span></td>
<td><span data-ttu-id="0f2e3-889">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-889">10001</span></span></td>
<td><span data-ttu-id="0f2e3-890">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-890">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-891">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-891">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="0f2e3-892">4,487.12</span></span></td>
<td><span data-ttu-id="0f2e3-893">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-894">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-894">Prod 2</span></span></td>
<td><span data-ttu-id="0f2e3-895">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-895">Product 2</span></span></td>
<td><span data-ttu-id="0f2e3-896">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-896">10001</span></span></td>
<td><span data-ttu-id="0f2e3-897">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-897">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-898">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-898">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="0f2e3-899">1,495.71</span></span></td>
<td><span data-ttu-id="0f2e3-900">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-901">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-901">CC003</span></span></td>
<td><span data-ttu-id="0f2e3-902">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="0f2e3-902">Assembly</span></span></td>
<td><span data-ttu-id="0f2e3-903">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-903">10001</span></span></td>
<td><span data-ttu-id="0f2e3-904">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-904">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-905">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-905">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="0f2e3-906">-286.25</span></span></td>
<td><span data-ttu-id="0f2e3-907">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-908">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-908">Prod 1</span></span></td>
<td><span data-ttu-id="0f2e3-909">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-909">Product 1</span></span></td>
<td><span data-ttu-id="0f2e3-910">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-910">10001</span></span></td>
<td><span data-ttu-id="0f2e3-911">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-911">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-912">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-912">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-913">241.05</span><span class="sxs-lookup"><span data-stu-id="0f2e3-913">241.05</span></span></td>
<td><span data-ttu-id="0f2e3-914">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-915">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-915">Prod 2</span></span></td>
<td><span data-ttu-id="0f2e3-916">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-916">Product 2</span></span></td>
<td><span data-ttu-id="0f2e3-917">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-917">10001</span></span></td>
<td><span data-ttu-id="0f2e3-918">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-918">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-919">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-919">Fixed cost</span></span></td>
<td><span data-ttu-id="0f2e3-920">45.20</span><span class="sxs-lookup"><span data-stu-id="0f2e3-920">45.20</span></span></td>
<td><span data-ttu-id="0f2e3-921">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-922">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-922">CC003</span></span></td>
<td><span data-ttu-id="0f2e3-923">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="0f2e3-923">Assembly</span></span></td>
<td><span data-ttu-id="0f2e3-924">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-924">10001</span></span></td>
<td><span data-ttu-id="0f2e3-925">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-925">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-926">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-926">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-927">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="0f2e3-927">-2,977.17</span></span></td>
<td><span data-ttu-id="0f2e3-928">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-929">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-929">Prod 1</span></span></td>
<td><span data-ttu-id="0f2e3-930">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-930">Product 1</span></span></td>
<td><span data-ttu-id="0f2e3-931">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-931">10001</span></span></td>
<td><span data-ttu-id="0f2e3-932">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-932">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-933">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-933">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="0f2e3-934">2,507.09</span></span></td>
<td><span data-ttu-id="0f2e3-935">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f2e3-936">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-936">Prod 2</span></span></td>
<td><span data-ttu-id="0f2e3-937">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-937">Product 2</span></span></td>
<td><span data-ttu-id="0f2e3-938">10 001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-938">10001</span></span></td>
<td><span data-ttu-id="0f2e3-939">Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-939">Electricity</span></span></td>
<td><span data-ttu-id="0f2e3-940">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-940">Variable cost</span></span></td>
<td><span data-ttu-id="0f2e3-941">470.08</span><span class="sxs-lookup"><span data-stu-id="0f2e3-941">470.08</span></span></td>
<td><span data-ttu-id="0f2e3-942">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="0f2e3-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="0f2e3-943">Johtopäätökset</span><span class="sxs-lookup"><span data-stu-id="0f2e3-943">Conclusion</span></span>
<span data-ttu-id="0f2e3-944">Kirjanpidossa kirjataan tyhjään kustannuspaikkatunnukseen sähkökustannus arvolla 10 000,00.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="0f2e3-945">Tämän ansiosta kustannuslaskijat tietävät, että kustannus on kohdistettava.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="0f2e3-946">Kustannukset virtaavat kirjanpidossa organisaation yksiköiden ja tasojen läpi käytössä olevien käytäntöjen ja sääntöjen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="0f2e3-947">Kukin kustannus on liitetty kustannusperusteeseen, joka sisältää parhaan arvion kustannusten kohdistuksesta.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="0f2e3-948">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="0f2e3-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="0f2e3-949">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="0f2e3-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="0f2e3-950">Yhteensä</span><span class="sxs-lookup"><span data-stu-id="0f2e3-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0f2e3-951">CC099</span><span class="sxs-lookup"><span data-stu-id="0f2e3-951">CC099</span></span></th>
<th><span data-ttu-id="0f2e3-952">CC001</span><span class="sxs-lookup"><span data-stu-id="0f2e3-952">CC001</span></span></th>
<th><span data-ttu-id="0f2e3-953">CC002</span><span class="sxs-lookup"><span data-stu-id="0f2e3-953">CC002</span></span></th>
<th><span data-ttu-id="0f2e3-954">CC003</span><span class="sxs-lookup"><span data-stu-id="0f2e3-954">CC003</span></span></th>
<th><span data-ttu-id="0f2e3-955">CC004</span><span class="sxs-lookup"><span data-stu-id="0f2e3-955">CC004</span></span></th>
<th><span data-ttu-id="0f2e3-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-956">Proj 1</span></span></th>
<th><span data-ttu-id="0f2e3-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-957">Proj 2</span></span></th>
<th><span data-ttu-id="0f2e3-958">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="0f2e3-958">Prod 1</span></span></th>
<th><span data-ttu-id="0f2e3-959">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="0f2e3-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="0f2e3-960">10001 Sähkö</span><span class="sxs-lookup"><span data-stu-id="0f2e3-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="0f2e3-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="0f2e3-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="0f2e3-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="0f2e3-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="0f2e3-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="0f2e3-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="0f2e3-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="0f2e3-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="0f2e3-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="0f2e3-970">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="0f2e3-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-971">0,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="0f2e3-972">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="0f2e3-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-973">0,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-974">0,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-975">0,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-976">0,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-977">0,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-978">776.36</span><span class="sxs-lookup"><span data-stu-id="0f2e3-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-979">223.64</span><span class="sxs-lookup"><span data-stu-id="0f2e3-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="0f2e3-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="0f2e3-981">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="0f2e3-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-982">000</span><span class="sxs-lookup"><span data-stu-id="0f2e3-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-983">0,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-984">0,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-985">0,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-986">0,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-987">30,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-988">10,00</span><span class="sxs-lookup"><span data-stu-id="0f2e3-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="0f2e3-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="0f2e3-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0f2e3-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="0f2e3-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="0f2e3-992">Tässä ohjeaiheessa esitellään, miten ensisijainen kustannuselementti, 10001 Sähkö, virtaa kustannusobjektien läpi.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="0f2e3-993">Tästä syystä tämä yleiskustannus kohdistetaan organisaation alimmalle tasolle.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="0f2e3-994">Toisin sanoen alimman tason kustannusobjektit kantavat kustannuksen.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="0f2e3-995">Jos tarvitset visuaalisen näkymän kustannuksen virrasta kustannusobjektien välillä, voit käyttää kustannuksen koontikäytäntösääntöjä kustannusvirran visualisointiin.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="0f2e3-996">Lisätietoja on kohdassa [Kustannusten koontikäytäntö ja yleiskustannuslaskenta](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="0f2e3-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



