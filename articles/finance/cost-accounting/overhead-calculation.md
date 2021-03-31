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
ms.openlocfilehash: 882804141a6b520e2420343958c7a6b02a7e09ae
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208844"
---
# <a name="overhead-calculation"></a><span data-ttu-id="aba35-103">Yleiskustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="aba35-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aba35-104">Tässä aiheessa kuvataan tyypillinen yleiskustannusten laskenta- ja kohdistusprosessi.</span><span class="sxs-lookup"><span data-stu-id="aba35-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="aba35-105">Sanaston määritelmä</span><span class="sxs-lookup"><span data-stu-id="aba35-105">Term definition</span></span>
---------------

<span data-ttu-id="aba35-106">Yleiskustannukset ovat yrityksen toiminnasta syntyviä kustannuksia, joita ei voi suoraan liittää mihinkään tiettyyn liiketoiminnan tehtävään, tuotteeseen tai palveluun.</span><span class="sxs-lookup"><span data-stu-id="aba35-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="aba35-107">Yleiskustannukset ovat tärkeä tuki voittoa tuottavien tehtävien luonnissa.</span><span class="sxs-lookup"><span data-stu-id="aba35-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="aba35-108">Seuraavassa on joitakin esimerkkejä yleiskustannuksista:</span><span class="sxs-lookup"><span data-stu-id="aba35-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="aba35-109">Vuokra</span><span class="sxs-lookup"><span data-stu-id="aba35-109">Rent</span></span>
-   <span data-ttu-id="aba35-110">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-110">Electricity</span></span>
-   <span data-ttu-id="aba35-111">Hallinnon palkat</span><span class="sxs-lookup"><span data-stu-id="aba35-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="aba35-112">Yleiskustannuslaskennan yleiskuva</span><span class="sxs-lookup"><span data-stu-id="aba35-112">Overhead calculation overview</span></span>
<span data-ttu-id="aba35-113">Yleiskustannusten laskenta suorittaa kustannuslaskennan käytännöt oikeassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="aba35-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="aba35-114">Yleiskustannusten laskennan voi suorittaa useita kertoja samalle tilikaudelle, jos kustannuslaskennan käytännöt ovat muuttuneet tai erityisiä virheitä on havaittu.</span><span class="sxs-lookup"><span data-stu-id="aba35-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="aba35-115">Kukin laskenta-ajo tallennetaan ja kullekin annetaan yksilöllinen versiotunnus, jonka avulla eri laskenta-ajoja voi verrata toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="aba35-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="aba35-116">Yleiskustannusten laskenta luo kustannustapahtumia, joille annetaan kirjauspäivä.</span><span class="sxs-lookup"><span data-stu-id="aba35-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="aba35-117">Kirjauspäivä vastaa laskennassa käytettyä tilikauden päättymispäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="aba35-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="aba35-118">Yksilöivä versiotunnus sisältää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="aba35-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="aba35-119">Versiotyyppi</span><span class="sxs-lookup"><span data-stu-id="aba35-119">Version type</span></span>
-   <span data-ttu-id="aba35-120">Päivämäärä ja aika</span><span class="sxs-lookup"><span data-stu-id="aba35-120">Date and time</span></span>
-   <span data-ttu-id="aba35-121">Kustannuslaskennan kirjanpito</span><span class="sxs-lookup"><span data-stu-id="aba35-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="aba35-122">Tilikausi </span><span class="sxs-lookup"><span data-stu-id="aba35-122">Fiscal year</span></span>
-   <span data-ttu-id="aba35-123">Tilikausi  </span><span class="sxs-lookup"><span data-stu-id="aba35-123">Fiscal period</span></span>

<span data-ttu-id="aba35-124">Yleiskustannusten laskenta ajetaan versiosta riippumattomana.</span><span class="sxs-lookup"><span data-stu-id="aba35-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="aba35-125">Voit siis laskea budjetin version ennen todellista versiota.</span><span class="sxs-lookup"><span data-stu-id="aba35-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="aba35-126">Yleiskustannusten laskenta koostuu neljästä vaiheesta, jotka esitellään seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="aba35-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="aba35-127">Kussakin vaiheessa luodaan kirjauskansion otsikko, jolla on kirjauskansiovientejä.</span><span class="sxs-lookup"><span data-stu-id="aba35-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="aba35-128">Tämä kirjauskansion otsikko säilyttää kunkin laskentavaiheen syöttötiedot.</span><span class="sxs-lookup"><span data-stu-id="aba35-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="aba35-129">Käytännöt ja säännöt ajetaan kullekin kirjauskansion riville, ja tuloksena luodaan kustannustapahtumia.</span><span class="sxs-lookup"><span data-stu-id="aba35-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="aba35-130">Tämän ansiosta kaikki laskutoimitukset ovat täysin jäljitettävissä.</span><span class="sxs-lookup"><span data-stu-id="aba35-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="aba35-131">[![Yleiskustannuslaskenta](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="aba35-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="aba35-132">Laske ja kohdista sähkön yleiskustannukset</span><span class="sxs-lookup"><span data-stu-id="aba35-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="aba35-133">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="aba35-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="aba35-134">Tarkka johdon näkymä ei täten ole saatavilla kustannuslaskennassa.</span><span class="sxs-lookup"><span data-stu-id="aba35-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="aba35-135">Jotta kustannuslaskenta tarjoaisi oikean johdon näkymän kaikista organisaation yksiköistä ja tasoista, kustannusten on virrattava organisaation yksiköiden läpi.</span><span class="sxs-lookup"><span data-stu-id="aba35-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="aba35-136">Tämän virran on perustuttava joko tarkkaan tietoon kulutuksesta tai perusteltuun arvioon.</span><span class="sxs-lookup"><span data-stu-id="aba35-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="aba35-137">Sähkökustannukset voi kirjata kirjanpitoon seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="aba35-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="aba35-138">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="aba35-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="aba35-139">Kustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="aba35-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="aba35-140">Päätili</span><span class="sxs-lookup"><span data-stu-id="aba35-140">Main account</span></span></th>
<th><span data-ttu-id="aba35-141">Summa kirjanpitovaluuttana</span><span class="sxs-lookup"><span data-stu-id="aba35-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-142">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="aba35-143">CC099</span><span class="sxs-lookup"><span data-stu-id="aba35-143">CC099</span></span></td>
<td><span data-ttu-id="aba35-144">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="aba35-144">Default cost center</span></span></td>
<td><span data-ttu-id="aba35-145">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-145">10001</span></span></td>
<td><span data-ttu-id="aba35-146">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-146">Electricity</span></span></td>
<td><span data-ttu-id="aba35-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="aba35-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="aba35-148">Vaihe 1: Käsittele kustannustoiminnan laskenta</span><span class="sxs-lookup"><span data-stu-id="aba35-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="aba35-149">Kun kustannustapahtumat tuodaan lähdetiedoista, niille asetetaan kustannuslaskennassa oletusarvoisesti **Luokittelematon** -kustannustoimintaluokka.</span><span class="sxs-lookup"><span data-stu-id="aba35-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="aba35-150">Voit luokitella kustannustapahtumia uudelleen **kiinteäksi kustannukseksi** tai **muuttuvaksi kustannukseksi** kustannustoiminnan käytäntösäännöillä.</span><span class="sxs-lookup"><span data-stu-id="aba35-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="aba35-151">Määritä kustannustoiminnan sääntö</span><span class="sxs-lookup"><span data-stu-id="aba35-151">Define the cost behavior rule</span></span>

<span data-ttu-id="aba35-152">Joissain tapauksissa osa kustannuksesta on kiinteä ja loppuosa perustuu kulutukseen.</span><span class="sxs-lookup"><span data-stu-id="aba35-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="aba35-153">Sähkölaskut sopivat usein tähän määritelmään.</span><span class="sxs-lookup"><span data-stu-id="aba35-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="aba35-154">Maksat ensin määrätyn, kiinteän maksun, jonka lisäksi maksat kulutuksesta kilowattitunteina (kWh).</span><span class="sxs-lookup"><span data-stu-id="aba35-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="aba35-155">Jos kiinteä maksu on esimerkiksi 1 000,00, kustannustoiminnan sääntö määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="aba35-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="aba35-156">Kiinteä määrä 1 000,00</span><span class="sxs-lookup"><span data-stu-id="aba35-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="aba35-157">0 &lt;= 1 000,00 = Kiinteä</span><span class="sxs-lookup"><span data-stu-id="aba35-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="aba35-158">1000,01 &lt; N = Muuttuva</span><span class="sxs-lookup"><span data-stu-id="aba35-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="aba35-159">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="aba35-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="aba35-160">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="aba35-160">Journal</span></span></th>
<th><span data-ttu-id="aba35-161">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="aba35-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="aba35-162">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="aba35-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="aba35-163">Versio</span><span class="sxs-lookup"><span data-stu-id="aba35-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-164">00001</span><span class="sxs-lookup"><span data-stu-id="aba35-164">00001</span></span></td>
<td><span data-ttu-id="aba35-165">Kustannustoiminnan laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="aba35-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="aba35-166">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="aba35-166">Fiscal</span></span></td>
<td><span data-ttu-id="aba35-167">2017</span><span class="sxs-lookup"><span data-stu-id="aba35-167">2017</span></span></td>
<td><span data-ttu-id="aba35-168">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="aba35-168">Period 1</span></span></td>
<td><span data-ttu-id="aba35-169">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="aba35-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="aba35-170">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="aba35-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="aba35-171">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="aba35-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="aba35-172">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="aba35-173">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="aba35-173">Cost element</span></span></th>
<th><span data-ttu-id="aba35-174">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="aba35-174">Cost behavior</span></span></th>
<th><span data-ttu-id="aba35-175">Summa</span><span class="sxs-lookup"><span data-stu-id="aba35-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-176">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="aba35-177">CC099</span><span class="sxs-lookup"><span data-stu-id="aba35-177">CC099</span></span></td>
<td><span data-ttu-id="aba35-178">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="aba35-178">Default cost center</span></span></td>
<td><span data-ttu-id="aba35-179">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-179">10001</span></span></td>
<td><span data-ttu-id="aba35-180">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-180">Electricity</span></span></td>
<td><span data-ttu-id="aba35-181">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="aba35-181">Unclassified</span></span></td>
<td><span data-ttu-id="aba35-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="aba35-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="aba35-183">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="aba35-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="aba35-184">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="aba35-185">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="aba35-185">Cost element</span></span></th>
<th><span data-ttu-id="aba35-186">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="aba35-186">Cost behavior</span></span></th>
<th><span data-ttu-id="aba35-187">Summa</span><span class="sxs-lookup"><span data-stu-id="aba35-187">Amount</span></span></th>
<th><span data-ttu-id="aba35-188">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="aba35-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-189">CC099</span><span class="sxs-lookup"><span data-stu-id="aba35-189">CC099</span></span></td>
<td><span data-ttu-id="aba35-190">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="aba35-190">Default cost center</span></span></td>
<td><span data-ttu-id="aba35-191">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-191">10001</span></span></td>
<td><span data-ttu-id="aba35-192">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-192">Electricity</span></span></td>
<td><span data-ttu-id="aba35-193">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="aba35-193">Unclassified</span></span></td>
<td><span data-ttu-id="aba35-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="aba35-194">10,000.00</span></span></td>
<td><span data-ttu-id="aba35-195">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-196">CC099</span><span class="sxs-lookup"><span data-stu-id="aba35-196">CC099</span></span></td>
<td><span data-ttu-id="aba35-197">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="aba35-197">Default cost center</span></span></td>
<td><span data-ttu-id="aba35-198">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-198">10001</span></span></td>
<td><span data-ttu-id="aba35-199">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-199">Electricity</span></span></td>
<td><span data-ttu-id="aba35-200">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="aba35-200">Unclassified</span></span></td>
<td><span data-ttu-id="aba35-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="aba35-201">-10,000.00</span></span></td>
<td><span data-ttu-id="aba35-202">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-203">CC099</span><span class="sxs-lookup"><span data-stu-id="aba35-203">CC099</span></span></td>
<td><span data-ttu-id="aba35-204">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="aba35-204">Default cost center</span></span></td>
<td><span data-ttu-id="aba35-205">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-205">10001</span></span></td>
<td><span data-ttu-id="aba35-206">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-206">Electricity</span></span></td>
<td><span data-ttu-id="aba35-207">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-207">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="aba35-208">1,000.00</span></span></td>
<td><span data-ttu-id="aba35-209">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-210">CC099</span><span class="sxs-lookup"><span data-stu-id="aba35-210">CC099</span></span></td>
<td><span data-ttu-id="aba35-211">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="aba35-211">Default cost center</span></span></td>
<td><span data-ttu-id="aba35-212">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-212">10001</span></span></td>
<td><span data-ttu-id="aba35-213">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-213">Electricity</span></span></td>
<td><span data-ttu-id="aba35-214">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-214">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="aba35-215">9,000.00</span></span></td>
<td><span data-ttu-id="aba35-216">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="aba35-217">Lisätietoja on kohdassa [Kustannustoimintakäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="aba35-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="aba35-218">Vaihe 2: Käsittele kustannusten jaon laskenta</span><span class="sxs-lookup"><span data-stu-id="aba35-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="aba35-219">Kustannusten jakoa käytetään kustannusten jakamiseen yhdestä kustannusobjektista toiseen (tai useampaan kustannusobjektiin) määrittämällä asiaankuuluvan kohdistusperusteen.</span><span class="sxs-lookup"><span data-stu-id="aba35-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="aba35-220">Kustannusten jako ja kustannusten kohdistus eroavat toisistaan sillä, että kustannusten jako tapahtuu aina alkuperäisen kustannuksen ensisijaisen kustannuselementin tasolla.</span><span class="sxs-lookup"><span data-stu-id="aba35-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="aba35-221">Määritä kustannusten jaon sääntö</span><span class="sxs-lookup"><span data-stu-id="aba35-221">Define the cost distribution rule</span></span>

<span data-ttu-id="aba35-222">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="aba35-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="aba35-223">Kustannuslaskenta ei tarjoa tästä tarpeeksi tarkkoja tietoja.</span><span class="sxs-lookup"><span data-stu-id="aba35-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="aba35-224">Muuttuva kustannus tulisi jakaa yksittäisille kustannusobjekteille reiluin perustein.</span><span class="sxs-lookup"><span data-stu-id="aba35-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="aba35-225">Loogisin kohdistusperuste on sähkönkulutus (kWh).</span><span class="sxs-lookup"><span data-stu-id="aba35-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="aba35-226">Luodaan tilastollinen dimensionjäsen nimeltä Sähkö, johon kirjataan sähkönkulutus.</span><span class="sxs-lookup"><span data-stu-id="aba35-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="aba35-227">Oletusarvon mukaan kaikki tilastolliset dimensiojäsenet ovat käytettävissä kohdistusperusteina.</span><span class="sxs-lookup"><span data-stu-id="aba35-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="aba35-228">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-228">Cost object</span></span></th>
<th><span data-ttu-id="aba35-229">kWh</span><span class="sxs-lookup"><span data-stu-id="aba35-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-230">CC001</span><span class="sxs-lookup"><span data-stu-id="aba35-230">CC001</span></span></td>
<td><span data-ttu-id="aba35-231">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="aba35-231">HR</span></span></td>
<td><span data-ttu-id="aba35-232">1 000</span><span class="sxs-lookup"><span data-stu-id="aba35-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-233">CC002</span><span class="sxs-lookup"><span data-stu-id="aba35-233">CC002</span></span></td>
<td><span data-ttu-id="aba35-234">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="aba35-234">Finance</span></span></td>
<td><span data-ttu-id="aba35-235">6,000</span><span class="sxs-lookup"><span data-stu-id="aba35-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-236">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-236">CC003</span></span></td>
<td><span data-ttu-id="aba35-237">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="aba35-237">Assembly</span></span></td>
<td><span data-ttu-id="aba35-238">0</span><span class="sxs-lookup"><span data-stu-id="aba35-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="aba35-239">Seuraavassa taulukossa on esitetty tulos, kun sähkönkulutusta käytetään kohdistusperusteena muuttuville kuluille.</span><span class="sxs-lookup"><span data-stu-id="aba35-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="aba35-240">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-240">Cost object</span></span></th>
<th><span data-ttu-id="aba35-241">Suuruus</span><span class="sxs-lookup"><span data-stu-id="aba35-241">Magnitude</span></span></th>
<th><span data-ttu-id="aba35-242">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="aba35-242">Allocation factor</span></span></th>
<th><span data-ttu-id="aba35-243">Summa</span><span class="sxs-lookup"><span data-stu-id="aba35-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-244">CC001</span><span class="sxs-lookup"><span data-stu-id="aba35-244">CC001</span></span></td>
<td><span data-ttu-id="aba35-245">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="aba35-245">HR</span></span></td>
<td><span data-ttu-id="aba35-246">1 000</span><span class="sxs-lookup"><span data-stu-id="aba35-246">1,000</span></span></td>
<td><span data-ttu-id="aba35-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="aba35-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="aba35-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="aba35-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-249">CC002</span><span class="sxs-lookup"><span data-stu-id="aba35-249">CC002</span></span></td>
<td><span data-ttu-id="aba35-250">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="aba35-250">Finance</span></span></td>
<td><span data-ttu-id="aba35-251">6,000</span><span class="sxs-lookup"><span data-stu-id="aba35-251">6,000</span></span></td>
<td><span data-ttu-id="aba35-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="aba35-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="aba35-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="aba35-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-254">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-254">CC003</span></span></td>
<td><span data-ttu-id="aba35-255">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="aba35-255">Assembly</span></span></td>
<td><span data-ttu-id="aba35-256">0</span><span class="sxs-lookup"><span data-stu-id="aba35-256">0</span></span></td>
<td><span data-ttu-id="aba35-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="aba35-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="aba35-258">0,00</span><span class="sxs-lookup"><span data-stu-id="aba35-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="aba35-259">Kiinteä kustannus tulisi jakaa tasaisesti yksittäisille kustannusobjekteille, jotka ovat kuluttaneet sähköä.</span><span class="sxs-lookup"><span data-stu-id="aba35-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="aba35-260">Voit käyttää sähkön tilastollista dimensiojäsentä kaavan kohdistusperusteena tämän tavoitteen saavuttamiseksi: (sähkö &gt;0,00) Seuraavassa taulukossa on esitetty tulos siitä, kun sähkönkulutus on määritetty muuttuvien kustannusten kohdistusperusteeksi.</span><span class="sxs-lookup"><span data-stu-id="aba35-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="aba35-261">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-261">Cost object</span></span></th>
<th><span data-ttu-id="aba35-262">Resepti</span><span class="sxs-lookup"><span data-stu-id="aba35-262">Formula</span></span></th>
<th><span data-ttu-id="aba35-263">Suuruus</span><span class="sxs-lookup"><span data-stu-id="aba35-263">Magnitude</span></span></th>
<th><span data-ttu-id="aba35-264">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="aba35-264">Allocation factor</span></span></th>
<th><span data-ttu-id="aba35-265">Summa</span><span class="sxs-lookup"><span data-stu-id="aba35-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-266">CC001</span><span class="sxs-lookup"><span data-stu-id="aba35-266">CC001</span></span></td>
<td><span data-ttu-id="aba35-267">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="aba35-267">HR</span></span></td>
<td><span data-ttu-id="aba35-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="aba35-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="aba35-269">1</span><span class="sxs-lookup"><span data-stu-id="aba35-269">1</span></span></td>
<td><span data-ttu-id="aba35-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="aba35-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="aba35-271">500,00</span><span class="sxs-lookup"><span data-stu-id="aba35-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-272">CC002</span><span class="sxs-lookup"><span data-stu-id="aba35-272">CC002</span></span></td>
<td><span data-ttu-id="aba35-273">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="aba35-273">Finance</span></span></td>
<td><span data-ttu-id="aba35-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="aba35-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="aba35-275">1</span><span class="sxs-lookup"><span data-stu-id="aba35-275">1</span></span></td>
<td><span data-ttu-id="aba35-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="aba35-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="aba35-277">500,00</span><span class="sxs-lookup"><span data-stu-id="aba35-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-278">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-278">CC003</span></span></td>
<td><span data-ttu-id="aba35-279">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="aba35-279">Assembly</span></span></td>
<td><span data-ttu-id="aba35-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="aba35-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="aba35-281">0</span><span class="sxs-lookup"><span data-stu-id="aba35-281">0</span></span></td>
<td><span data-ttu-id="aba35-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="aba35-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="aba35-283">0,00</span><span class="sxs-lookup"><span data-stu-id="aba35-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="aba35-284">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="aba35-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="aba35-285">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="aba35-285">Journal</span></span></th>
<th><span data-ttu-id="aba35-286">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="aba35-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="aba35-287">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="aba35-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="aba35-288">Versio</span><span class="sxs-lookup"><span data-stu-id="aba35-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-289">00002</span><span class="sxs-lookup"><span data-stu-id="aba35-289">00002</span></span></td>
<td><span data-ttu-id="aba35-290">Kustannusten jaon laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="aba35-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="aba35-291">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="aba35-291">Fiscal</span></span></td>
<td><span data-ttu-id="aba35-292">2017</span><span class="sxs-lookup"><span data-stu-id="aba35-292">2017</span></span></td>
<td><span data-ttu-id="aba35-293">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="aba35-293">Period 1</span></span></td>
<td><span data-ttu-id="aba35-294">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="aba35-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="aba35-295">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="aba35-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="aba35-296">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="aba35-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="aba35-297">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="aba35-298">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="aba35-298">Cost element</span></span></th>
<th><span data-ttu-id="aba35-299">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="aba35-299">Cost behavior</span></span></th>
<th><span data-ttu-id="aba35-300">Summa</span><span class="sxs-lookup"><span data-stu-id="aba35-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-301">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="aba35-302">CC099</span><span class="sxs-lookup"><span data-stu-id="aba35-302">CC099</span></span></td>
<td><span data-ttu-id="aba35-303">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="aba35-303">Default cost center</span></span></td>
<td><span data-ttu-id="aba35-304">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-304">10001</span></span></td>
<td><span data-ttu-id="aba35-305">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-305">Electricity</span></span></td>
<td><span data-ttu-id="aba35-306">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-306">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="aba35-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-308">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="aba35-309">CC099</span><span class="sxs-lookup"><span data-stu-id="aba35-309">CC099</span></span></td>
<td><span data-ttu-id="aba35-310">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="aba35-310">Default cost center</span></span></td>
<td><span data-ttu-id="aba35-311">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-311">10001</span></span></td>
<td><span data-ttu-id="aba35-312">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-312">Electricity</span></span></td>
<td><span data-ttu-id="aba35-313">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-313">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="aba35-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="aba35-315">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="aba35-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="aba35-316">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="aba35-317">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="aba35-317">Cost element</span></span></th>
<th><span data-ttu-id="aba35-318">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="aba35-318">Cost behavior</span></span></th>
<th><span data-ttu-id="aba35-319">Summa</span><span class="sxs-lookup"><span data-stu-id="aba35-319">Amount</span></span></th>
<th><span data-ttu-id="aba35-320">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="aba35-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-321">CC099</span><span class="sxs-lookup"><span data-stu-id="aba35-321">CC099</span></span></td>
<td><span data-ttu-id="aba35-322">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="aba35-322">Default cost center</span></span></td>
<td><span data-ttu-id="aba35-323">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-323">10001</span></span></td>
<td><span data-ttu-id="aba35-324">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-324">Electricity</span></span></td>
<td><span data-ttu-id="aba35-325">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-325">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="aba35-326">-1,000.00</span></span></td>
<td><span data-ttu-id="aba35-327">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-328">CC001</span><span class="sxs-lookup"><span data-stu-id="aba35-328">CC001</span></span></td>
<td><span data-ttu-id="aba35-329">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="aba35-329">HR</span></span></td>
<td><span data-ttu-id="aba35-330">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-330">10001</span></span></td>
<td><span data-ttu-id="aba35-331">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-331">Electricity</span></span></td>
<td><span data-ttu-id="aba35-332">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-332">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-333">500,00</span><span class="sxs-lookup"><span data-stu-id="aba35-333">500.00</span></span></td>
<td><span data-ttu-id="aba35-334">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-335">CC002</span><span class="sxs-lookup"><span data-stu-id="aba35-335">CC002</span></span></td>
<td><span data-ttu-id="aba35-336">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="aba35-336">Finance</span></span></td>
<td><span data-ttu-id="aba35-337">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-337">10001</span></span></td>
<td><span data-ttu-id="aba35-338">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-338">Electricity</span></span></td>
<td><span data-ttu-id="aba35-339">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-339">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-340">500,00</span><span class="sxs-lookup"><span data-stu-id="aba35-340">500.00</span></span></td>
<td><span data-ttu-id="aba35-341">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-342">CC099</span><span class="sxs-lookup"><span data-stu-id="aba35-342">CC099</span></span></td>
<td><span data-ttu-id="aba35-343">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="aba35-343">Default cost center</span></span></td>
<td><span data-ttu-id="aba35-344">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-344">10001</span></span></td>
<td><span data-ttu-id="aba35-345">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-345">Electricity</span></span></td>
<td><span data-ttu-id="aba35-346">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-346">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="aba35-347">-9,000.00</span></span></td>
<td><span data-ttu-id="aba35-348">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-349">CC001</span><span class="sxs-lookup"><span data-stu-id="aba35-349">CC001</span></span></td>
<td><span data-ttu-id="aba35-350">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="aba35-350">HR</span></span></td>
<td><span data-ttu-id="aba35-351">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-351">10001</span></span></td>
<td><span data-ttu-id="aba35-352">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-352">Electricity</span></span></td>
<td><span data-ttu-id="aba35-353">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-353">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="aba35-354">1,285.71</span></span></td>
<td><span data-ttu-id="aba35-355">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-356">CC002</span><span class="sxs-lookup"><span data-stu-id="aba35-356">CC002</span></span></td>
<td><span data-ttu-id="aba35-357">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="aba35-357">Finance</span></span></td>
<td><span data-ttu-id="aba35-358">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-358">10001</span></span></td>
<td><span data-ttu-id="aba35-359">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-359">Electricity</span></span></td>
<td><span data-ttu-id="aba35-360">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-360">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="aba35-361">7,714.29</span></span></td>
<td><span data-ttu-id="aba35-362">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="aba35-363">Lisätietoja on kohdassa [Jakelukäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="aba35-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="aba35-364">Vaihe 3: Käsittele yleiskustannustason laskenta</span><span class="sxs-lookup"><span data-stu-id="aba35-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="aba35-365">Yleiskustannustasolla veloitetaan yksi tai useampi määrätty kustannusobjekti.</span><span class="sxs-lookup"><span data-stu-id="aba35-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="aba35-366">Veloitus perustuu ennalta määrättyyn kustannustasoon sekä määritetyn kohdistusperusteen suuruuteen.</span><span class="sxs-lookup"><span data-stu-id="aba35-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="aba35-367">Määritä yleiskustannustaso.</span><span class="sxs-lookup"><span data-stu-id="aba35-367">Define the overhead rate</span></span>

<span data-ttu-id="aba35-368">Kustannusobjekti CC001 HR vaikuttaa joukkoon sisäisiä projekteja.</span><span class="sxs-lookup"><span data-stu-id="aba35-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="aba35-369">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon projektit.</span><span class="sxs-lookup"><span data-stu-id="aba35-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="aba35-370">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-370">Cost object</span></span></th>
<th><span data-ttu-id="aba35-371">Tunnit</span><span class="sxs-lookup"><span data-stu-id="aba35-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="aba35-372">Proj 1</span></span></td>
<td><span data-ttu-id="aba35-373">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="aba35-373">Project 1</span></span></td>
<td><span data-ttu-id="aba35-374">3</span><span class="sxs-lookup"><span data-stu-id="aba35-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="aba35-375">Proj 2</span></span></td>
<td><span data-ttu-id="aba35-376">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="aba35-376">Project 2</span></span></td>
<td><span data-ttu-id="aba35-377">1</span><span class="sxs-lookup"><span data-stu-id="aba35-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="aba35-378">Kustannusprojektien osuudelle on määritetty ennalta kustannushinta.</span><span class="sxs-lookup"><span data-stu-id="aba35-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="aba35-379">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-379">Cost object</span></span></th>
<th><span data-ttu-id="aba35-380">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="aba35-380">Cost element</span></span></th>
<th><span data-ttu-id="aba35-381">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="aba35-381">Cost behavior</span></span></th>
<th><span data-ttu-id="aba35-382">Yksiköt</span><span class="sxs-lookup"><span data-stu-id="aba35-382">Units</span></span></th>
<th><span data-ttu-id="aba35-383">Osuus</span><span class="sxs-lookup"><span data-stu-id="aba35-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-384">CC001</span><span class="sxs-lookup"><span data-stu-id="aba35-384">CC001</span></span></td>
<td><span data-ttu-id="aba35-385">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="aba35-385">HR</span></span></td>
<td><span data-ttu-id="aba35-386">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-386">10001</span></span></td>
<td><span data-ttu-id="aba35-387">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-387">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-388">1</span><span class="sxs-lookup"><span data-stu-id="aba35-388">1</span></span></td>
<td><span data-ttu-id="aba35-389">10</span><span class="sxs-lookup"><span data-stu-id="aba35-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="aba35-390">Seuraavassa taulukossa on esitetty tulos, kun Henkilöstöhallinnon projekteja käytetään kohdistusperusteena.</span><span class="sxs-lookup"><span data-stu-id="aba35-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="aba35-391">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-391">Cost object</span></span></th>
<th><span data-ttu-id="aba35-392">Suuruus</span><span class="sxs-lookup"><span data-stu-id="aba35-392">Magnitude</span></span></th>
<th><span data-ttu-id="aba35-393">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="aba35-393">Cost element</span></span></th>
<th><span data-ttu-id="aba35-394">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="aba35-394">Allocation factor</span></span></th>
<th><span data-ttu-id="aba35-395">Summa</span><span class="sxs-lookup"><span data-stu-id="aba35-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="aba35-396">Proj 1</span></span></td>
<td><span data-ttu-id="aba35-397">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="aba35-397">Project 1</span></span></td>
<td><span data-ttu-id="aba35-398">3</span><span class="sxs-lookup"><span data-stu-id="aba35-398">3</span></span></td>
<td><span data-ttu-id="aba35-399">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-399">10001</span></span></td>
<td><span data-ttu-id="aba35-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="aba35-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="aba35-401">30,00</span><span class="sxs-lookup"><span data-stu-id="aba35-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="aba35-402">Proj 2</span></span></td>
<td><span data-ttu-id="aba35-403">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="aba35-403">Project 2</span></span></td>
<td><span data-ttu-id="aba35-404">1</span><span class="sxs-lookup"><span data-stu-id="aba35-404">1</span></span></td>
<td><span data-ttu-id="aba35-405">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-405">10001</span></span></td>
<td><span data-ttu-id="aba35-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="aba35-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="aba35-407">10,00</span><span class="sxs-lookup"><span data-stu-id="aba35-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="aba35-408">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="aba35-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="aba35-409">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="aba35-409">Journal</span></span></th>
<th><span data-ttu-id="aba35-410">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="aba35-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="aba35-411">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="aba35-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="aba35-412">Versio</span><span class="sxs-lookup"><span data-stu-id="aba35-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-413">00003</span><span class="sxs-lookup"><span data-stu-id="aba35-413">00003</span></span></td>
<td><span data-ttu-id="aba35-414">Yleiskustannustason laskelman kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="aba35-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="aba35-415">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="aba35-415">Fiscal</span></span></td>
<td><span data-ttu-id="aba35-416">2017</span><span class="sxs-lookup"><span data-stu-id="aba35-416">2017</span></span></td>
<td><span data-ttu-id="aba35-417">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="aba35-417">Period 1</span></span></td>
<td><span data-ttu-id="aba35-418">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="aba35-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="aba35-419">Kirjauskansioviennit (Yleiskustannustason laskennan kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="aba35-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="aba35-420">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="aba35-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="aba35-421">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-421">Cost object</span></span></th>
<th><span data-ttu-id="aba35-422">Suuruus</span><span class="sxs-lookup"><span data-stu-id="aba35-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-423">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="aba35-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="aba35-424">Proj 1</span></span></td>
<td><span data-ttu-id="aba35-425">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="aba35-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="aba35-426">3,00</span><span class="sxs-lookup"><span data-stu-id="aba35-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-427">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="aba35-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="aba35-428">Proj 2</span></span></td>
<td><span data-ttu-id="aba35-429">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="aba35-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="aba35-430">1,00</span><span class="sxs-lookup"><span data-stu-id="aba35-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="aba35-431">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="aba35-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="aba35-432">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="aba35-433">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="aba35-433">Cost element</span></span></th>
<th><span data-ttu-id="aba35-434">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="aba35-434">Cost behavior</span></span></th>
<th><span data-ttu-id="aba35-435">Summa</span><span class="sxs-lookup"><span data-stu-id="aba35-435">Amount</span></span></th>
<th><span data-ttu-id="aba35-436">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="aba35-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="aba35-437">CC0001</span></span></td>
<td><span data-ttu-id="aba35-438">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="aba35-438">HR</span></span></td>
<td><span data-ttu-id="aba35-439">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-439">10001</span></span></td>
<td><span data-ttu-id="aba35-440">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-440">Electricity</span></span></td>
<td><span data-ttu-id="aba35-441">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-441">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="aba35-442">-30.00</span></span></td>
<td><span data-ttu-id="aba35-443">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="aba35-444">Proj 1</span></span></td>
<td><span data-ttu-id="aba35-445">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="aba35-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="aba35-446">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-446">10001</span></span></td>
<td><span data-ttu-id="aba35-447">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-447">Electricity</span></span></td>
<td><span data-ttu-id="aba35-448">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-448">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-449">30,00</span><span class="sxs-lookup"><span data-stu-id="aba35-449">30.00</span></span></td>
<td><span data-ttu-id="aba35-450">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-451">CC001</span><span class="sxs-lookup"><span data-stu-id="aba35-451">CC001</span></span></td>
<td><span data-ttu-id="aba35-452">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="aba35-452">HR</span></span></td>
<td><span data-ttu-id="aba35-453">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-453">10001</span></span></td>
<td><span data-ttu-id="aba35-454">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-454">Electricity</span></span></td>
<td><span data-ttu-id="aba35-455">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-455">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="aba35-456">-10.00</span></span></td>
<td><span data-ttu-id="aba35-457">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="aba35-458">Proj 2</span></span></td>
<td><span data-ttu-id="aba35-459">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="aba35-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="aba35-460">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-460">10001</span></span></td>
<td><span data-ttu-id="aba35-461">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-461">Electricity</span></span></td>
<td><span data-ttu-id="aba35-462">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-462">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-463">10.00</span><span class="sxs-lookup"><span data-stu-id="aba35-463">10.00</span></span></td>
<td><span data-ttu-id="aba35-464">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="aba35-465">Lisätietoja on kohdassa [Yleisen laskennan suorittaminen](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="aba35-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="aba35-466">Vaihe 4: Käsittele kustannusten kohdistuksen laskenta</span><span class="sxs-lookup"><span data-stu-id="aba35-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="aba35-467">Kohdistuksella kustannusobjektin saldo liitetään toisiin kustannusobjekteihin käyttämällä kohdistusperustetta.</span><span class="sxs-lookup"><span data-stu-id="aba35-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="aba35-468">Finance tukee vastavuoroista kohdistusmenetelmää.</span><span class="sxs-lookup"><span data-stu-id="aba35-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="aba35-469">Vastavuoroisessa kohdistusmenetelmässä tunnistetaan oheiskustannusobjektien käyttämät, keskinäiset palvelut täysin.</span><span class="sxs-lookup"><span data-stu-id="aba35-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="aba35-470">Järjestelmä määrittää oikean kohdistusjärjestyksen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="aba35-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="aba35-471">Kustannusobjektin saldo kohdistetaan yhdellä kohdistusperusteella.</span><span class="sxs-lookup"><span data-stu-id="aba35-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="aba35-472">Kustannusobjektien dimensiot ja niiden vastaavat jäsenet ylittävät kohdistukset ovat tuettuja.</span><span class="sxs-lookup"><span data-stu-id="aba35-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="aba35-473">Kustannusseurantayksikkö hallitsee kohdistusjärjestystä.</span><span class="sxs-lookup"><span data-stu-id="aba35-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="aba35-474">[![Vastavuoroinen menetelmä](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="aba35-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="aba35-475">Määritä kustannuksen kohdistus</span><span class="sxs-lookup"><span data-stu-id="aba35-475">Define the cost allocation</span></span>

<span data-ttu-id="aba35-476">Tämä on yksinkertainen esimerkki, jossa kerrotaan, miten voit jäljittää kustannuksen virran.</span><span class="sxs-lookup"><span data-stu-id="aba35-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="aba35-477">Kustannusobjekti CC001 HR liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="aba35-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="aba35-478">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="aba35-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="aba35-479">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-479">Cost object</span></span></th>
<th><span data-ttu-id="aba35-480">HR-palvelut</span><span class="sxs-lookup"><span data-stu-id="aba35-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-481">CC002</span><span class="sxs-lookup"><span data-stu-id="aba35-481">CC002</span></span></td>
<td><span data-ttu-id="aba35-482">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="aba35-482">Finance</span></span></td>
<td><span data-ttu-id="aba35-483">35</span><span class="sxs-lookup"><span data-stu-id="aba35-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-484">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-484">CC003</span></span></td>
<td><span data-ttu-id="aba35-485">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="aba35-485">Assembly</span></span></td>
<td><span data-ttu-id="aba35-486">55</span><span class="sxs-lookup"><span data-stu-id="aba35-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-487">CC004</span><span class="sxs-lookup"><span data-stu-id="aba35-487">CC004</span></span></td>
<td><span data-ttu-id="aba35-488">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="aba35-488">Packaging</span></span></td>
<td><span data-ttu-id="aba35-489">10</span><span class="sxs-lookup"><span data-stu-id="aba35-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="aba35-490">Kustannusobjekti CC002 Taloushallinto liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="aba35-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="aba35-491">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Taloushallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="aba35-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="aba35-492">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-492">Cost object</span></span></th>
<th><span data-ttu-id="aba35-493">Taloushallinnon palvelut</span><span class="sxs-lookup"><span data-stu-id="aba35-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-494">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-494">CC003</span></span></td>
<td><span data-ttu-id="aba35-495">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="aba35-495">Assembly</span></span></td>
<td><span data-ttu-id="aba35-496">65</span><span class="sxs-lookup"><span data-stu-id="aba35-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-497">CC004</span><span class="sxs-lookup"><span data-stu-id="aba35-497">CC004</span></span></td>
<td><span data-ttu-id="aba35-498">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="aba35-498">Packaging</span></span></td>
<td><span data-ttu-id="aba35-499">35</span><span class="sxs-lookup"><span data-stu-id="aba35-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="aba35-500">Kustannusobjekti CC003 Kokoonpano liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="aba35-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="aba35-501">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Kokoonpanopalvelut.</span><span class="sxs-lookup"><span data-stu-id="aba35-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="aba35-502">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-502">Cost object</span></span></th>
<th><span data-ttu-id="aba35-503">Kokoonpanopalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="aba35-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-504">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-504">Prod 1</span></span></td>
<td><span data-ttu-id="aba35-505">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-505">Product 1</span></span></td>
<td><span data-ttu-id="aba35-506">60</span><span class="sxs-lookup"><span data-stu-id="aba35-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-507">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-507">Prod 2</span></span></td>
<td><span data-ttu-id="aba35-508">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-508">Product 2</span></span></td>
<td><span data-ttu-id="aba35-509">20</span><span class="sxs-lookup"><span data-stu-id="aba35-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="aba35-510">Kustannusobjekti CC004 Pakkaus liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="aba35-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="aba35-511">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Pakkauspalvelut.</span><span class="sxs-lookup"><span data-stu-id="aba35-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="aba35-512">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-512">Cost object</span></span></th>
<th><span data-ttu-id="aba35-513">Pakkauspalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="aba35-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-514">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-514">Prod 1</span></span></td>
<td><span data-ttu-id="aba35-515">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-515">Product 1</span></span></td>
<td><span data-ttu-id="aba35-516">80</span><span class="sxs-lookup"><span data-stu-id="aba35-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-517">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-517">Prod 2</span></span></td>
<td><span data-ttu-id="aba35-518">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-518">Product 2</span></span></td>
<td><span data-ttu-id="aba35-519">15</span><span class="sxs-lookup"><span data-stu-id="aba35-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="aba35-520">Tilastomittaukset, kuten tämän tuotteen kuluttamat tuotantotunnit, voidaan johtaa lähdetiedoista.</span><span class="sxs-lookup"><span data-stu-id="aba35-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="aba35-521">Lisätietoja on kohdassa [Tilastomittauksen lähdemalli](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="aba35-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="aba35-522">Seuraavassa taulukossa näytetään tulos, kun henkilöstöhallinnon palveluja käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="aba35-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="aba35-523">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-523">Cost object</span></span></th>
<th><span data-ttu-id="aba35-524">Suuruus</span><span class="sxs-lookup"><span data-stu-id="aba35-524">Magnitude</span></span></th>
<th><span data-ttu-id="aba35-525">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="aba35-525">Allocation factor</span></span></th>
<th><span data-ttu-id="aba35-526">Summa</span><span class="sxs-lookup"><span data-stu-id="aba35-526">Amount</span></span></th>
<th><span data-ttu-id="aba35-527">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="aba35-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-528">CC002</span><span class="sxs-lookup"><span data-stu-id="aba35-528">CC002</span></span></td>
<td><span data-ttu-id="aba35-529">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="aba35-529">Finance</span></span></td>
<td><span data-ttu-id="aba35-530">35</span><span class="sxs-lookup"><span data-stu-id="aba35-530">35</span></span></td>
<td><span data-ttu-id="aba35-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="aba35-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="aba35-532">175.00</span><span class="sxs-lookup"><span data-stu-id="aba35-532">175.00</span></span></td>
<td><span data-ttu-id="aba35-533">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-534">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-534">CC003</span></span></td>
<td><span data-ttu-id="aba35-535">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="aba35-535">Assembly</span></span></td>
<td><span data-ttu-id="aba35-536">55</span><span class="sxs-lookup"><span data-stu-id="aba35-536">55</span></span></td>
<td><span data-ttu-id="aba35-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="aba35-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="aba35-538">275.00</span><span class="sxs-lookup"><span data-stu-id="aba35-538">275.00</span></span></td>
<td><span data-ttu-id="aba35-539">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-540">CC004</span><span class="sxs-lookup"><span data-stu-id="aba35-540">CC004</span></span></td>
<td><span data-ttu-id="aba35-541">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="aba35-541">Packaging</span></span></td>
<td><span data-ttu-id="aba35-542">10</span><span class="sxs-lookup"><span data-stu-id="aba35-542">10</span></span></td>
<td><span data-ttu-id="aba35-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="aba35-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="aba35-544">50,00</span><span class="sxs-lookup"><span data-stu-id="aba35-544">50.00</span></span></td>
<td><span data-ttu-id="aba35-545">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-546">CC002</span><span class="sxs-lookup"><span data-stu-id="aba35-546">CC002</span></span></td>
<td><span data-ttu-id="aba35-547">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="aba35-547">Finance</span></span></td>
<td><span data-ttu-id="aba35-548">35</span><span class="sxs-lookup"><span data-stu-id="aba35-548">35</span></span></td>
<td><span data-ttu-id="aba35-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="aba35-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="aba35-550">436.00</span><span class="sxs-lookup"><span data-stu-id="aba35-550">436.00</span></span></td>
<td><span data-ttu-id="aba35-551">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-552">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-552">CC003</span></span></td>
<td><span data-ttu-id="aba35-553">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="aba35-553">Assembly</span></span></td>
<td><span data-ttu-id="aba35-554">55</span><span class="sxs-lookup"><span data-stu-id="aba35-554">55</span></span></td>
<td><span data-ttu-id="aba35-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="aba35-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="aba35-556">685.14</span><span class="sxs-lookup"><span data-stu-id="aba35-556">685.14</span></span></td>
<td><span data-ttu-id="aba35-557">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-558">CC004</span><span class="sxs-lookup"><span data-stu-id="aba35-558">CC004</span></span></td>
<td><span data-ttu-id="aba35-559">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="aba35-559">Packaging</span></span></td>
<td><span data-ttu-id="aba35-560">10</span><span class="sxs-lookup"><span data-stu-id="aba35-560">10</span></span></td>
<td><span data-ttu-id="aba35-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="aba35-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="aba35-562">124.57</span><span class="sxs-lookup"><span data-stu-id="aba35-562">124.57</span></span></td>
<td><span data-ttu-id="aba35-563">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="aba35-564">Seuraavassa taulukossa näytetään tulos, kun Taloushallinnon palveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="aba35-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="aba35-565">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-565">Cost object</span></span></th>
<th><span data-ttu-id="aba35-566">Suuruus</span><span class="sxs-lookup"><span data-stu-id="aba35-566">Magnitude</span></span></th>
<th><span data-ttu-id="aba35-567">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="aba35-567">Allocation factor</span></span></th>
<th><span data-ttu-id="aba35-568">Summa</span><span class="sxs-lookup"><span data-stu-id="aba35-568">Amount</span></span></th>
<th><span data-ttu-id="aba35-569">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="aba35-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-570">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-570">CC003</span></span></td>
<td><span data-ttu-id="aba35-571">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="aba35-571">Assembly</span></span></td>
<td><span data-ttu-id="aba35-572">65</span><span class="sxs-lookup"><span data-stu-id="aba35-572">65</span></span></td>
<td><span data-ttu-id="aba35-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="aba35-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="aba35-574">438.75</span><span class="sxs-lookup"><span data-stu-id="aba35-574">438.75</span></span></td>
<td><span data-ttu-id="aba35-575">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-576">CC004</span><span class="sxs-lookup"><span data-stu-id="aba35-576">CC004</span></span></td>
<td><span data-ttu-id="aba35-577">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="aba35-577">Packaging</span></span></td>
<td><span data-ttu-id="aba35-578">35</span><span class="sxs-lookup"><span data-stu-id="aba35-578">35</span></span></td>
<td><span data-ttu-id="aba35-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="aba35-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="aba35-580">236.25</span><span class="sxs-lookup"><span data-stu-id="aba35-580">236.25</span></span></td>
<td><span data-ttu-id="aba35-581">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-582">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-582">CC003</span></span></td>
<td><span data-ttu-id="aba35-583">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="aba35-583">Assembly</span></span></td>
<td><span data-ttu-id="aba35-584">65</span><span class="sxs-lookup"><span data-stu-id="aba35-584">65</span></span></td>
<td><span data-ttu-id="aba35-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="aba35-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="aba35-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="aba35-586">5,297.69</span></span></td>
<td><span data-ttu-id="aba35-587">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-588">CC004</span><span class="sxs-lookup"><span data-stu-id="aba35-588">CC004</span></span></td>
<td><span data-ttu-id="aba35-589">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="aba35-589">Packaging</span></span></td>
<td><span data-ttu-id="aba35-590">35</span><span class="sxs-lookup"><span data-stu-id="aba35-590">35</span></span></td>
<td><span data-ttu-id="aba35-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="aba35-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="aba35-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="aba35-592">2,852.60</span></span></td>
<td><span data-ttu-id="aba35-593">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="aba35-594">Seuraavassa taulukossa näytetään tulos, kun Kokoonpanopalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="aba35-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="aba35-595">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-595">Cost object</span></span></th>
<th><span data-ttu-id="aba35-596">Suuruus</span><span class="sxs-lookup"><span data-stu-id="aba35-596">Magnitude</span></span></th>
<th><span data-ttu-id="aba35-597">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="aba35-597">Allocation factor</span></span></th>
<th><span data-ttu-id="aba35-598">Summa</span><span class="sxs-lookup"><span data-stu-id="aba35-598">Amount</span></span></th>
<th><span data-ttu-id="aba35-599">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="aba35-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-600">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-600">Prod 1</span></span></td>
<td><span data-ttu-id="aba35-601">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-601">Product 1</span></span></td>
<td><span data-ttu-id="aba35-602">60</span><span class="sxs-lookup"><span data-stu-id="aba35-602">60</span></span></td>
<td><span data-ttu-id="aba35-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="aba35-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="aba35-604">535.31</span><span class="sxs-lookup"><span data-stu-id="aba35-604">535.31</span></span></td>
<td><span data-ttu-id="aba35-605">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-606">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-606">Prod 2</span></span></td>
<td><span data-ttu-id="aba35-607">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-607">Product 2</span></span></td>
<td><span data-ttu-id="aba35-608">20</span><span class="sxs-lookup"><span data-stu-id="aba35-608">20</span></span></td>
<td><span data-ttu-id="aba35-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="aba35-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="aba35-610">178.44</span><span class="sxs-lookup"><span data-stu-id="aba35-610">178.44</span></span></td>
<td><span data-ttu-id="aba35-611">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-612">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-612">Prod 1</span></span></td>
<td><span data-ttu-id="aba35-613">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-613">Product 1</span></span></td>
<td><span data-ttu-id="aba35-614">60</span><span class="sxs-lookup"><span data-stu-id="aba35-614">60</span></span></td>
<td><span data-ttu-id="aba35-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="aba35-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="aba35-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="aba35-616">4,487.12</span></span></td>
<td><span data-ttu-id="aba35-617">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-618">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-618">Prod 2</span></span></td>
<td><span data-ttu-id="aba35-619">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-619">Product 2</span></span></td>
<td><span data-ttu-id="aba35-620">20</span><span class="sxs-lookup"><span data-stu-id="aba35-620">20</span></span></td>
<td><span data-ttu-id="aba35-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="aba35-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="aba35-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="aba35-622">1,495.71</span></span></td>
<td><span data-ttu-id="aba35-623">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="aba35-624">Seuraavassa taulukossa näytetään tulos, kun Pakkauspalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="aba35-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="aba35-625">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-625">Cost object</span></span></th>
<th><span data-ttu-id="aba35-626">Suuruus</span><span class="sxs-lookup"><span data-stu-id="aba35-626">Magnitude</span></span></th>
<th><span data-ttu-id="aba35-627">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="aba35-627">Allocation factor</span></span></th>
<th><span data-ttu-id="aba35-628">Summa</span><span class="sxs-lookup"><span data-stu-id="aba35-628">Amount</span></span></th>
<th><span data-ttu-id="aba35-629">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="aba35-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-630">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-630">Prod 1</span></span></td>
<td><span data-ttu-id="aba35-631">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-631">Product 1</span></span></td>
<td><span data-ttu-id="aba35-632">80</span><span class="sxs-lookup"><span data-stu-id="aba35-632">80</span></span></td>
<td><span data-ttu-id="aba35-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="aba35-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="aba35-634">241.05</span><span class="sxs-lookup"><span data-stu-id="aba35-634">241.05</span></span></td>
<td><span data-ttu-id="aba35-635">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-636">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-636">Prod 2</span></span></td>
<td><span data-ttu-id="aba35-637">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-637">Product 2</span></span></td>
<td><span data-ttu-id="aba35-638">15</span><span class="sxs-lookup"><span data-stu-id="aba35-638">15</span></span></td>
<td><span data-ttu-id="aba35-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="aba35-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="aba35-640">45.20</span><span class="sxs-lookup"><span data-stu-id="aba35-640">45.20</span></span></td>
<td><span data-ttu-id="aba35-641">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-642">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-642">Prod 1</span></span></td>
<td><span data-ttu-id="aba35-643">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-643">Product 1</span></span></td>
<td><span data-ttu-id="aba35-644">80</span><span class="sxs-lookup"><span data-stu-id="aba35-644">80</span></span></td>
<td><span data-ttu-id="aba35-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="aba35-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="aba35-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="aba35-646">2,507.09</span></span></td>
<td><span data-ttu-id="aba35-647">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-648">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-648">Prod 2</span></span></td>
<td><span data-ttu-id="aba35-649">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-649">Product 2</span></span></td>
<td><span data-ttu-id="aba35-650">15</span><span class="sxs-lookup"><span data-stu-id="aba35-650">15</span></span></td>
<td><span data-ttu-id="aba35-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="aba35-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="aba35-652">470.08</span><span class="sxs-lookup"><span data-stu-id="aba35-652">470.08</span></span></td>
<td><span data-ttu-id="aba35-653">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="aba35-654">Kirjauskansioviennit (kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="aba35-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="aba35-655">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="aba35-655">Journal</span></span></th>
<th><span data-ttu-id="aba35-656">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="aba35-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="aba35-657">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="aba35-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="aba35-658">Versio</span><span class="sxs-lookup"><span data-stu-id="aba35-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-659">00004</span><span class="sxs-lookup"><span data-stu-id="aba35-659">00004</span></span></td>
<td><span data-ttu-id="aba35-660">Kustannusten kohdistuskirjauskansio</span><span class="sxs-lookup"><span data-stu-id="aba35-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="aba35-661">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="aba35-661">Fiscal</span></span></td>
<td><span data-ttu-id="aba35-662">2017</span><span class="sxs-lookup"><span data-stu-id="aba35-662">2017</span></span></td>
<td><span data-ttu-id="aba35-663">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="aba35-663">Period 1</span></span></td>
<td><span data-ttu-id="aba35-664">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="aba35-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="aba35-665">Kirjauskansion rivit</span><span class="sxs-lookup"><span data-stu-id="aba35-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="aba35-666">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="aba35-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="aba35-667">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="aba35-668">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="aba35-668">Cost element</span></span></th>
<th><span data-ttu-id="aba35-669">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="aba35-669">Cost behavior</span></span></th>
<th><span data-ttu-id="aba35-670">Summa</span><span class="sxs-lookup"><span data-stu-id="aba35-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-671">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="aba35-672">CC001</span><span class="sxs-lookup"><span data-stu-id="aba35-672">CC001</span></span></td>
<td><span data-ttu-id="aba35-673">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="aba35-673">HR</span></span></td>
<td><span data-ttu-id="aba35-674">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-674">10001</span></span></td>
<td><span data-ttu-id="aba35-675">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-675">Electricity</span></span></td>
<td><span data-ttu-id="aba35-676">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-676">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-677">500,00</span><span class="sxs-lookup"><span data-stu-id="aba35-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-678">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="aba35-679">CC001</span><span class="sxs-lookup"><span data-stu-id="aba35-679">CC001</span></span></td>
<td><span data-ttu-id="aba35-680">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="aba35-680">HR</span></span></td>
<td><span data-ttu-id="aba35-681">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-681">10001</span></span></td>
<td><span data-ttu-id="aba35-682">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-682">Electricity</span></span></td>
<td><span data-ttu-id="aba35-683">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-683">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="aba35-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-685">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="aba35-686">CC002</span><span class="sxs-lookup"><span data-stu-id="aba35-686">CC002</span></span></td>
<td><span data-ttu-id="aba35-687">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="aba35-687">Finance</span></span></td>
<td><span data-ttu-id="aba35-688">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-688">10001</span></span></td>
<td><span data-ttu-id="aba35-689">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-689">Electricity</span></span></td>
<td><span data-ttu-id="aba35-690">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-690">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-691">675.00</span><span class="sxs-lookup"><span data-stu-id="aba35-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-692">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="aba35-693">CC002</span><span class="sxs-lookup"><span data-stu-id="aba35-693">CC002</span></span></td>
<td><span data-ttu-id="aba35-694">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="aba35-694">Finance</span></span></td>
<td><span data-ttu-id="aba35-695">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-695">10001</span></span></td>
<td><span data-ttu-id="aba35-696">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-696">Electricity</span></span></td>
<td><span data-ttu-id="aba35-697">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-697">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="aba35-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-699">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="aba35-700">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-700">CC003</span></span></td>
<td><span data-ttu-id="aba35-701">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="aba35-701">Assembly</span></span></td>
<td><span data-ttu-id="aba35-702">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-702">10001</span></span></td>
<td><span data-ttu-id="aba35-703">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-703">Electricity</span></span></td>
<td><span data-ttu-id="aba35-704">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-704">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-705">713.75</span><span class="sxs-lookup"><span data-stu-id="aba35-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-706">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="aba35-707">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-707">CC003</span></span></td>
<td><span data-ttu-id="aba35-708">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="aba35-708">Assembly</span></span></td>
<td><span data-ttu-id="aba35-709">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-709">10001</span></span></td>
<td><span data-ttu-id="aba35-710">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-710">Electricity</span></span></td>
<td><span data-ttu-id="aba35-711">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-711">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="aba35-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-713">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="aba35-714">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-714">CC003</span></span></td>
<td><span data-ttu-id="aba35-715">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="aba35-715">Packaging</span></span></td>
<td><span data-ttu-id="aba35-716">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-716">10001</span></span></td>
<td><span data-ttu-id="aba35-717">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-717">Electricity</span></span></td>
<td><span data-ttu-id="aba35-718">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-718">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-719">286.25</span><span class="sxs-lookup"><span data-stu-id="aba35-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-720">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="aba35-721">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-721">CC003</span></span></td>
<td><span data-ttu-id="aba35-722">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="aba35-722">Packaging</span></span></td>
<td><span data-ttu-id="aba35-723">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-723">10001</span></span></td>
<td><span data-ttu-id="aba35-724">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-724">Electricity</span></span></td>
<td><span data-ttu-id="aba35-725">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-725">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="aba35-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-727">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="aba35-728">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-728">Prod 1</span></span></td>
<td><span data-ttu-id="aba35-729">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-729">Product 1</span></span></td>
<td><span data-ttu-id="aba35-730">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-730">10001</span></span></td>
<td><span data-ttu-id="aba35-731">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-731">Electricity</span></span></td>
<td><span data-ttu-id="aba35-732">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-732">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-733">776.36</span><span class="sxs-lookup"><span data-stu-id="aba35-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-734">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="aba35-735">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-735">Prod 1</span></span></td>
<td><span data-ttu-id="aba35-736">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-736">Product 1</span></span></td>
<td><span data-ttu-id="aba35-737">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-737">10001</span></span></td>
<td><span data-ttu-id="aba35-738">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-738">Electricity</span></span></td>
<td><span data-ttu-id="aba35-739">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-739">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="aba35-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-741">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="aba35-742">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-742">Prod 2</span></span></td>
<td><span data-ttu-id="aba35-743">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-743">Product 1</span></span></td>
<td><span data-ttu-id="aba35-744">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-744">10001</span></span></td>
<td><span data-ttu-id="aba35-745">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-745">Electricity</span></span></td>
<td><span data-ttu-id="aba35-746">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-746">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-747">223.64</span><span class="sxs-lookup"><span data-stu-id="aba35-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-748">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="aba35-749">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-749">Prod 2</span></span></td>
<td><span data-ttu-id="aba35-750">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-750">Product 1</span></span></td>
<td><span data-ttu-id="aba35-751">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-751">10001</span></span></td>
<td><span data-ttu-id="aba35-752">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-752">Electricity</span></span></td>
<td><span data-ttu-id="aba35-753">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-753">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="aba35-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="aba35-755">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="aba35-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="aba35-756">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="aba35-757">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="aba35-757">Cost element</span></span></th>
<th><span data-ttu-id="aba35-758">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="aba35-758">Cost behavior</span></span></th>
<th><span data-ttu-id="aba35-759">Summa</span><span class="sxs-lookup"><span data-stu-id="aba35-759">Amount</span></span></th>
<th><span data-ttu-id="aba35-760">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="aba35-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aba35-761">CC001</span><span class="sxs-lookup"><span data-stu-id="aba35-761">CC001</span></span></td>
<td><span data-ttu-id="aba35-762">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="aba35-762">HR</span></span></td>
<td><span data-ttu-id="aba35-763">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-763">10001</span></span></td>
<td><span data-ttu-id="aba35-764">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-764">Electricity</span></span></td>
<td><span data-ttu-id="aba35-765">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-765">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="aba35-766">-500.00</span></span></td>
<td><span data-ttu-id="aba35-767">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-768">CC002</span><span class="sxs-lookup"><span data-stu-id="aba35-768">CC002</span></span></td>
<td><span data-ttu-id="aba35-769">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="aba35-769">Finance</span></span></td>
<td><span data-ttu-id="aba35-770">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-770">10001</span></span></td>
<td><span data-ttu-id="aba35-771">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-771">Electricity</span></span></td>
<td><span data-ttu-id="aba35-772">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-772">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-773">175.00</span><span class="sxs-lookup"><span data-stu-id="aba35-773">175.00</span></span></td>
<td><span data-ttu-id="aba35-774">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-775">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-775">CC003</span></span></td>
<td><span data-ttu-id="aba35-776">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="aba35-776">Assembly</span></span></td>
<td><span data-ttu-id="aba35-777">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-777">10001</span></span></td>
<td><span data-ttu-id="aba35-778">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-778">Electricity</span></span></td>
<td><span data-ttu-id="aba35-779">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-779">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-780">275.00</span><span class="sxs-lookup"><span data-stu-id="aba35-780">275.00</span></span></td>
<td><span data-ttu-id="aba35-781">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-782">CC004</span><span class="sxs-lookup"><span data-stu-id="aba35-782">CC004</span></span></td>
<td><span data-ttu-id="aba35-783">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="aba35-783">Packaging</span></span></td>
<td><span data-ttu-id="aba35-784">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-784">10001</span></span></td>
<td><span data-ttu-id="aba35-785">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-785">Electricity</span></span></td>
<td><span data-ttu-id="aba35-786">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-786">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-787">50,00</span><span class="sxs-lookup"><span data-stu-id="aba35-787">50,00</span></span></td>
<td><span data-ttu-id="aba35-788">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-789">CC001</span><span class="sxs-lookup"><span data-stu-id="aba35-789">CC001</span></span></td>
<td><span data-ttu-id="aba35-790">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="aba35-790">HR</span></span></td>
<td><span data-ttu-id="aba35-791">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-791">10001</span></span></td>
<td><span data-ttu-id="aba35-792">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-792">Electricity</span></span></td>
<td><span data-ttu-id="aba35-793">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-793">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="aba35-794">-1,245.71</span></span></td>
<td><span data-ttu-id="aba35-795">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-796">CC002</span><span class="sxs-lookup"><span data-stu-id="aba35-796">CC002</span></span></td>
<td><span data-ttu-id="aba35-797">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="aba35-797">Finance</span></span></td>
<td><span data-ttu-id="aba35-798">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-798">10001</span></span></td>
<td><span data-ttu-id="aba35-799">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-799">Electricity</span></span></td>
<td><span data-ttu-id="aba35-800">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-800">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-801">436.00</span><span class="sxs-lookup"><span data-stu-id="aba35-801">436.00</span></span></td>
<td><span data-ttu-id="aba35-802">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-803">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-803">CC003</span></span></td>
<td><span data-ttu-id="aba35-804">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="aba35-804">Assembly</span></span></td>
<td><span data-ttu-id="aba35-805">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-805">10001</span></span></td>
<td><span data-ttu-id="aba35-806">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-806">Electricity</span></span></td>
<td><span data-ttu-id="aba35-807">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-807">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-808">685.14</span><span class="sxs-lookup"><span data-stu-id="aba35-808">685.14</span></span></td>
<td><span data-ttu-id="aba35-809">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-810">CC004</span><span class="sxs-lookup"><span data-stu-id="aba35-810">CC004</span></span></td>
<td><span data-ttu-id="aba35-811">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="aba35-811">Packaging</span></span></td>
<td><span data-ttu-id="aba35-812">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-812">10001</span></span></td>
<td><span data-ttu-id="aba35-813">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-813">Electricity</span></span></td>
<td><span data-ttu-id="aba35-814">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-814">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-815">124.57</span><span class="sxs-lookup"><span data-stu-id="aba35-815">124.57</span></span></td>
<td><span data-ttu-id="aba35-816">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-817">CC002</span><span class="sxs-lookup"><span data-stu-id="aba35-817">CC002</span></span></td>
<td><span data-ttu-id="aba35-818">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="aba35-818">Finance</span></span></td>
<td><span data-ttu-id="aba35-819">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-819">10001</span></span></td>
<td><span data-ttu-id="aba35-820">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-820">Electricity</span></span></td>
<td><span data-ttu-id="aba35-821">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-821">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="aba35-822">-675.00</span></span></td>
<td><span data-ttu-id="aba35-823">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-824">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-824">CC003</span></span></td>
<td><span data-ttu-id="aba35-825">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="aba35-825">Assembly</span></span></td>
<td><span data-ttu-id="aba35-826">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-826">10001</span></span></td>
<td><span data-ttu-id="aba35-827">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-827">Electricity</span></span></td>
<td><span data-ttu-id="aba35-828">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-828">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-829">438.75</span><span class="sxs-lookup"><span data-stu-id="aba35-829">438.75</span></span></td>
<td><span data-ttu-id="aba35-830">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-831">CC004</span><span class="sxs-lookup"><span data-stu-id="aba35-831">CC004</span></span></td>
<td><span data-ttu-id="aba35-832">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="aba35-832">Packaging</span></span></td>
<td><span data-ttu-id="aba35-833">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-833">10001</span></span></td>
<td><span data-ttu-id="aba35-834">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-834">Electricity</span></span></td>
<td><span data-ttu-id="aba35-835">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-835">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-836">236.25</span><span class="sxs-lookup"><span data-stu-id="aba35-836">236.25</span></span></td>
<td><span data-ttu-id="aba35-837">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-838">CC002</span><span class="sxs-lookup"><span data-stu-id="aba35-838">CC002</span></span></td>
<td><span data-ttu-id="aba35-839">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="aba35-839">Finance</span></span></td>
<td><span data-ttu-id="aba35-840">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-840">10001</span></span></td>
<td><span data-ttu-id="aba35-841">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-841">Electricity</span></span></td>
<td><span data-ttu-id="aba35-842">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-842">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="aba35-843">-8,150.29</span></span></td>
<td><span data-ttu-id="aba35-844">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-845">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-845">CC003</span></span></td>
<td><span data-ttu-id="aba35-846">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="aba35-846">Assembly</span></span></td>
<td><span data-ttu-id="aba35-847">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-847">10001</span></span></td>
<td><span data-ttu-id="aba35-848">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-848">Electricity</span></span></td>
<td><span data-ttu-id="aba35-849">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-849">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="aba35-850">5,297.69</span></span></td>
<td><span data-ttu-id="aba35-851">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-852">CC004</span><span class="sxs-lookup"><span data-stu-id="aba35-852">CC004</span></span></td>
<td><span data-ttu-id="aba35-853">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="aba35-853">Packaging</span></span></td>
<td><span data-ttu-id="aba35-854">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-854">10001</span></span></td>
<td><span data-ttu-id="aba35-855">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-855">Electricity</span></span></td>
<td><span data-ttu-id="aba35-856">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-856">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="aba35-857">2,852.60</span></span></td>
<td><span data-ttu-id="aba35-858">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-859">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-859">CC003</span></span></td>
<td><span data-ttu-id="aba35-860">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="aba35-860">Assembly</span></span></td>
<td><span data-ttu-id="aba35-861">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-861">10001</span></span></td>
<td><span data-ttu-id="aba35-862">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-862">Electricity</span></span></td>
<td><span data-ttu-id="aba35-863">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-863">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="aba35-864">-713.75</span></span></td>
<td><span data-ttu-id="aba35-865">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-866">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-866">Prod 1</span></span></td>
<td><span data-ttu-id="aba35-867">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-867">Product 1</span></span></td>
<td><span data-ttu-id="aba35-868">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-868">10001</span></span></td>
<td><span data-ttu-id="aba35-869">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-869">Electricity</span></span></td>
<td><span data-ttu-id="aba35-870">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-870">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-871">535.31</span><span class="sxs-lookup"><span data-stu-id="aba35-871">535.31</span></span></td>
<td><span data-ttu-id="aba35-872">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-873">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-873">Prod 2</span></span></td>
<td><span data-ttu-id="aba35-874">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-874">Product 2</span></span></td>
<td><span data-ttu-id="aba35-875">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-875">10001</span></span></td>
<td><span data-ttu-id="aba35-876">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-876">Electricity</span></span></td>
<td><span data-ttu-id="aba35-877">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-877">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-878">178.44</span><span class="sxs-lookup"><span data-stu-id="aba35-878">178.44</span></span></td>
<td><span data-ttu-id="aba35-879">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-880">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-880">CC003</span></span></td>
<td><span data-ttu-id="aba35-881">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="aba35-881">Assembly</span></span></td>
<td><span data-ttu-id="aba35-882">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-882">10001</span></span></td>
<td><span data-ttu-id="aba35-883">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-883">Electricity</span></span></td>
<td><span data-ttu-id="aba35-884">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-884">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="aba35-885">-5,982.83</span></span></td>
<td><span data-ttu-id="aba35-886">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-887">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-887">Prod 1</span></span></td>
<td><span data-ttu-id="aba35-888">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-888">Product 1</span></span></td>
<td><span data-ttu-id="aba35-889">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-889">10001</span></span></td>
<td><span data-ttu-id="aba35-890">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-890">Electricity</span></span></td>
<td><span data-ttu-id="aba35-891">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-891">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="aba35-892">4,487.12</span></span></td>
<td><span data-ttu-id="aba35-893">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-894">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-894">Prod 2</span></span></td>
<td><span data-ttu-id="aba35-895">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-895">Product 2</span></span></td>
<td><span data-ttu-id="aba35-896">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-896">10001</span></span></td>
<td><span data-ttu-id="aba35-897">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-897">Electricity</span></span></td>
<td><span data-ttu-id="aba35-898">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-898">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="aba35-899">1,495.71</span></span></td>
<td><span data-ttu-id="aba35-900">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-901">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-901">CC003</span></span></td>
<td><span data-ttu-id="aba35-902">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="aba35-902">Assembly</span></span></td>
<td><span data-ttu-id="aba35-903">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-903">10001</span></span></td>
<td><span data-ttu-id="aba35-904">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-904">Electricity</span></span></td>
<td><span data-ttu-id="aba35-905">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-905">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="aba35-906">-286.25</span></span></td>
<td><span data-ttu-id="aba35-907">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-908">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-908">Prod 1</span></span></td>
<td><span data-ttu-id="aba35-909">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-909">Product 1</span></span></td>
<td><span data-ttu-id="aba35-910">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-910">10001</span></span></td>
<td><span data-ttu-id="aba35-911">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-911">Electricity</span></span></td>
<td><span data-ttu-id="aba35-912">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-912">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-913">241.05</span><span class="sxs-lookup"><span data-stu-id="aba35-913">241.05</span></span></td>
<td><span data-ttu-id="aba35-914">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-915">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-915">Prod 2</span></span></td>
<td><span data-ttu-id="aba35-916">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-916">Product 2</span></span></td>
<td><span data-ttu-id="aba35-917">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-917">10001</span></span></td>
<td><span data-ttu-id="aba35-918">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-918">Electricity</span></span></td>
<td><span data-ttu-id="aba35-919">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-919">Fixed cost</span></span></td>
<td><span data-ttu-id="aba35-920">45.20</span><span class="sxs-lookup"><span data-stu-id="aba35-920">45.20</span></span></td>
<td><span data-ttu-id="aba35-921">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-922">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-922">CC003</span></span></td>
<td><span data-ttu-id="aba35-923">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="aba35-923">Assembly</span></span></td>
<td><span data-ttu-id="aba35-924">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-924">10001</span></span></td>
<td><span data-ttu-id="aba35-925">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-925">Electricity</span></span></td>
<td><span data-ttu-id="aba35-926">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-926">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-927">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="aba35-927">-2,977.17</span></span></td>
<td><span data-ttu-id="aba35-928">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-929">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-929">Prod 1</span></span></td>
<td><span data-ttu-id="aba35-930">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-930">Product 1</span></span></td>
<td><span data-ttu-id="aba35-931">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-931">10001</span></span></td>
<td><span data-ttu-id="aba35-932">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-932">Electricity</span></span></td>
<td><span data-ttu-id="aba35-933">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-933">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="aba35-934">2,507.09</span></span></td>
<td><span data-ttu-id="aba35-935">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aba35-936">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-936">Prod 2</span></span></td>
<td><span data-ttu-id="aba35-937">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-937">Product 2</span></span></td>
<td><span data-ttu-id="aba35-938">10 001</span><span class="sxs-lookup"><span data-stu-id="aba35-938">10001</span></span></td>
<td><span data-ttu-id="aba35-939">Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-939">Electricity</span></span></td>
<td><span data-ttu-id="aba35-940">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-940">Variable cost</span></span></td>
<td><span data-ttu-id="aba35-941">470.08</span><span class="sxs-lookup"><span data-stu-id="aba35-941">470.08</span></span></td>
<td><span data-ttu-id="aba35-942">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="aba35-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="aba35-943">Johtopäätökset</span><span class="sxs-lookup"><span data-stu-id="aba35-943">Conclusion</span></span>
<span data-ttu-id="aba35-944">Kirjanpidossa kirjataan tyhjään kustannuspaikkatunnukseen sähkökustannus arvolla 10 000,00.</span><span class="sxs-lookup"><span data-stu-id="aba35-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="aba35-945">Tämän ansiosta kustannuslaskijat tietävät, että kustannus on kohdistettava.</span><span class="sxs-lookup"><span data-stu-id="aba35-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="aba35-946">Kustannukset virtaavat kirjanpidossa organisaation yksiköiden ja tasojen läpi käytössä olevien käytäntöjen ja sääntöjen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="aba35-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="aba35-947">Kukin kustannus on liitetty kustannusperusteeseen, joka sisältää parhaan arvion kustannusten kohdistuksesta.</span><span class="sxs-lookup"><span data-stu-id="aba35-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="aba35-948">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="aba35-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="aba35-949">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="aba35-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="aba35-950">Yhteensä</span><span class="sxs-lookup"><span data-stu-id="aba35-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="aba35-951">CC099</span><span class="sxs-lookup"><span data-stu-id="aba35-951">CC099</span></span></th>
<th><span data-ttu-id="aba35-952">CC001</span><span class="sxs-lookup"><span data-stu-id="aba35-952">CC001</span></span></th>
<th><span data-ttu-id="aba35-953">CC002</span><span class="sxs-lookup"><span data-stu-id="aba35-953">CC002</span></span></th>
<th><span data-ttu-id="aba35-954">CC003</span><span class="sxs-lookup"><span data-stu-id="aba35-954">CC003</span></span></th>
<th><span data-ttu-id="aba35-955">CC004</span><span class="sxs-lookup"><span data-stu-id="aba35-955">CC004</span></span></th>
<th><span data-ttu-id="aba35-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="aba35-956">Proj 1</span></span></th>
<th><span data-ttu-id="aba35-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="aba35-957">Proj 2</span></span></th>
<th><span data-ttu-id="aba35-958">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="aba35-958">Prod 1</span></span></th>
<th><span data-ttu-id="aba35-959">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="aba35-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="aba35-960">10001 Sähkö</span><span class="sxs-lookup"><span data-stu-id="aba35-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="aba35-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="aba35-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="aba35-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="aba35-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="aba35-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="aba35-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="aba35-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="aba35-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="aba35-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="aba35-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="aba35-970">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="aba35-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-971">0,00</span><span class="sxs-lookup"><span data-stu-id="aba35-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="aba35-972">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="aba35-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-973">0,00</span><span class="sxs-lookup"><span data-stu-id="aba35-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-974">0,00</span><span class="sxs-lookup"><span data-stu-id="aba35-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-975">0,00</span><span class="sxs-lookup"><span data-stu-id="aba35-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-976">0,00</span><span class="sxs-lookup"><span data-stu-id="aba35-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-977">0,00</span><span class="sxs-lookup"><span data-stu-id="aba35-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="aba35-978">776.36</span><span class="sxs-lookup"><span data-stu-id="aba35-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-979">223.64</span><span class="sxs-lookup"><span data-stu-id="aba35-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="aba35-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="aba35-981">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="aba35-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-982">000</span><span class="sxs-lookup"><span data-stu-id="aba35-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-983">0,00</span><span class="sxs-lookup"><span data-stu-id="aba35-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-984">0,00</span><span class="sxs-lookup"><span data-stu-id="aba35-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-985">0,00</span><span class="sxs-lookup"><span data-stu-id="aba35-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-986">0,00</span><span class="sxs-lookup"><span data-stu-id="aba35-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-987">30,00</span><span class="sxs-lookup"><span data-stu-id="aba35-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-988">10,00</span><span class="sxs-lookup"><span data-stu-id="aba35-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="aba35-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="aba35-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="aba35-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="aba35-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="aba35-992">Tässä ohjeaiheessa esitellään, miten ensisijainen kustannuselementti, 10001 Sähkö, virtaa kustannusobjektien läpi.</span><span class="sxs-lookup"><span data-stu-id="aba35-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="aba35-993">Tästä syystä tämä yleiskustannus kohdistetaan organisaation alimmalle tasolle.</span><span class="sxs-lookup"><span data-stu-id="aba35-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="aba35-994">Toisin sanoen alimman tason kustannusobjektit kantavat kustannuksen.</span><span class="sxs-lookup"><span data-stu-id="aba35-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="aba35-995">Jos tarvitset visuaalisen näkymän kustannuksen virrasta kustannusobjektien välillä, voit käyttää kustannuksen koontikäytäntösääntöjä kustannusvirran visualisointiin.</span><span class="sxs-lookup"><span data-stu-id="aba35-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="aba35-996">Lisätietoja on kohdassa [Kustannusten koontikäytäntö ja yleiskustannuslaskenta](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="aba35-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]