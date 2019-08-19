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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: cef4a80aa12927fdbffea4bb6bcb108ad81494a6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841486"
---
# <a name="overhead-calculation"></a><span data-ttu-id="be9dc-103">Yleiskustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="be9dc-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be9dc-104">Tässä aiheessa kuvataan tyypillinen yleiskustannusten laskenta- ja kohdistusprosessi.</span><span class="sxs-lookup"><span data-stu-id="be9dc-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="be9dc-105">Sanaston määritelmä</span><span class="sxs-lookup"><span data-stu-id="be9dc-105">Term definition</span></span>
---------------

<span data-ttu-id="be9dc-106">Yleiskustannukset ovat yrityksen toiminnasta syntyviä kustannuksia, joita ei voi suoraan liittää mihinkään tiettyyn liiketoiminnan tehtävään, tuotteeseen tai palveluun.</span><span class="sxs-lookup"><span data-stu-id="be9dc-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="be9dc-107">Yleiskustannukset ovat tärkeä tuki voittoa tuottavien tehtävien luonnissa.</span><span class="sxs-lookup"><span data-stu-id="be9dc-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="be9dc-108">Seuraavassa on joitakin esimerkkejä yleiskustannuksista:</span><span class="sxs-lookup"><span data-stu-id="be9dc-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="be9dc-109">Vuokra</span><span class="sxs-lookup"><span data-stu-id="be9dc-109">Rent</span></span>
-   <span data-ttu-id="be9dc-110">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-110">Electricity</span></span>
-   <span data-ttu-id="be9dc-111">Hallinnon palkat</span><span class="sxs-lookup"><span data-stu-id="be9dc-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="be9dc-112">Yleiskustannuslaskennan yleiskuva</span><span class="sxs-lookup"><span data-stu-id="be9dc-112">Overhead calculation overview</span></span>
<span data-ttu-id="be9dc-113">Yleiskustannusten laskenta suorittaa kustannuslaskennan käytännöt oikeassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="be9dc-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="be9dc-114">Yleiskustannusten laskennan voi suorittaa useita kertoja samalle tilikaudelle, jos kustannuslaskennan käytännöt ovat muuttuneet tai erityisiä virheitä on havaittu.</span><span class="sxs-lookup"><span data-stu-id="be9dc-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="be9dc-115">Kukin laskenta-ajo tallennetaan ja kullekin annetaan yksilöllinen versiotunnus, jonka avulla eri laskenta-ajoja voi verrata toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="be9dc-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="be9dc-116">Yleiskustannusten laskenta luo kustannustapahtumia, joille annetaan kirjauspäivä.</span><span class="sxs-lookup"><span data-stu-id="be9dc-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="be9dc-117">Kirjauspäivä vastaa laskennassa käytettyä tilikauden päättymispäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="be9dc-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="be9dc-118">Yksilöivä versiotunnus sisältää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="be9dc-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="be9dc-119">Versiotyyppi</span><span class="sxs-lookup"><span data-stu-id="be9dc-119">Version type</span></span>
-   <span data-ttu-id="be9dc-120">Päivämäärä ja aika</span><span class="sxs-lookup"><span data-stu-id="be9dc-120">Date and time</span></span>
-   <span data-ttu-id="be9dc-121">Kustannuslaskennan kirjanpito</span><span class="sxs-lookup"><span data-stu-id="be9dc-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="be9dc-122">Tilikausi </span><span class="sxs-lookup"><span data-stu-id="be9dc-122">Fiscal year</span></span>
-   <span data-ttu-id="be9dc-123">Tilikausi  </span><span class="sxs-lookup"><span data-stu-id="be9dc-123">Fiscal period</span></span>

<span data-ttu-id="be9dc-124">Yleiskustannusten laskenta ajetaan versiosta riippumattomana.</span><span class="sxs-lookup"><span data-stu-id="be9dc-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="be9dc-125">Voit siis laskea budjetin version ennen todellista versiota.</span><span class="sxs-lookup"><span data-stu-id="be9dc-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="be9dc-126">Yleiskustannusten laskenta koostuu neljästä vaiheesta, jotka esitellään seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="be9dc-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="be9dc-127">Kussakin vaiheessa luodaan kirjauskansion otsikko, jolla on kirjauskansiovientejä.</span><span class="sxs-lookup"><span data-stu-id="be9dc-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="be9dc-128">Tämä kirjauskansion otsikko säilyttää kunkin laskentavaiheen syöttötiedot.</span><span class="sxs-lookup"><span data-stu-id="be9dc-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="be9dc-129">Käytännöt ja säännöt ajetaan kullekin kirjauskansion riville, ja tuloksena luodaan kustannustapahtumia.</span><span class="sxs-lookup"><span data-stu-id="be9dc-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="be9dc-130">Tämän ansiosta kaikki laskutoimitukset ovat täysin jäljitettävissä.</span><span class="sxs-lookup"><span data-stu-id="be9dc-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="be9dc-131">[![Yleiskustannuslaskenta](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="be9dc-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="be9dc-132">Laske ja kohdista sähkön yleiskustannukset</span><span class="sxs-lookup"><span data-stu-id="be9dc-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="be9dc-133">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="be9dc-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="be9dc-134">Tarkka johdon näkymä ei täten ole saatavilla kustannuslaskennassa.</span><span class="sxs-lookup"><span data-stu-id="be9dc-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="be9dc-135">Jotta kustannuslaskenta tarjoaisi oikean johdon näkymän kaikista organisaation yksiköistä ja tasoista, kustannusten on virrattava organisaation yksiköiden läpi.</span><span class="sxs-lookup"><span data-stu-id="be9dc-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="be9dc-136">Tämän virran on perustuttava joko tarkkaan tietoon kulutuksesta tai perusteltuun arvioon.</span><span class="sxs-lookup"><span data-stu-id="be9dc-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="be9dc-137">Sähkökustannukset voi kirjata kirjanpitoon seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="be9dc-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="be9dc-138">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="be9dc-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="be9dc-139">Kustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="be9dc-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="be9dc-140">Päätili</span><span class="sxs-lookup"><span data-stu-id="be9dc-140">Main account</span></span></th>
<th><span data-ttu-id="be9dc-141">Summa kirjanpitovaluuttana</span><span class="sxs-lookup"><span data-stu-id="be9dc-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-142">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="be9dc-143">CC099</span><span class="sxs-lookup"><span data-stu-id="be9dc-143">CC099</span></span></td>
<td><span data-ttu-id="be9dc-144">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="be9dc-144">Default cost center</span></span></td>
<td><span data-ttu-id="be9dc-145">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-145">10001</span></span></td>
<td><span data-ttu-id="be9dc-146">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-146">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="be9dc-148">Vaihe 1: Käsittele kustannustoiminnan laskenta</span><span class="sxs-lookup"><span data-stu-id="be9dc-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="be9dc-149">Kun kustannustapahtumat tuodaan lähdetiedoista, niille asetetaan kustannuslaskennassa oletusarvoisesti **Luokittelematon** -kustannustoimintaluokka.</span><span class="sxs-lookup"><span data-stu-id="be9dc-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="be9dc-150">Voit luokitella kustannustapahtumia uudelleen **kiinteäksi kustannukseksi** tai **muuttuvaksi kustannukseksi** kustannustoiminnan käytäntösäännöillä.</span><span class="sxs-lookup"><span data-stu-id="be9dc-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="be9dc-151">Määritä kustannustoiminnan sääntö</span><span class="sxs-lookup"><span data-stu-id="be9dc-151">Define the cost behavior rule</span></span>

<span data-ttu-id="be9dc-152">Joissain tapauksissa osa kustannuksesta on kiinteä ja loppuosa perustuu kulutukseen.</span><span class="sxs-lookup"><span data-stu-id="be9dc-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="be9dc-153">Sähkölaskut sopivat usein tähän määritelmään.</span><span class="sxs-lookup"><span data-stu-id="be9dc-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="be9dc-154">Maksat ensin määrätyn, kiinteän maksun, jonka lisäksi maksat kulutuksesta kilowattitunteina (kWh).</span><span class="sxs-lookup"><span data-stu-id="be9dc-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="be9dc-155">Jos kiinteä maksu on esimerkiksi 1 000,00, kustannustoiminnan sääntö määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="be9dc-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="be9dc-156">Kiinteä määrä 1 000,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="be9dc-157">0 &lt;= 1 000,00 = Kiinteä</span><span class="sxs-lookup"><span data-stu-id="be9dc-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="be9dc-158">1000,01 &lt; N = Muuttuva</span><span class="sxs-lookup"><span data-stu-id="be9dc-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="be9dc-159">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="be9dc-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="be9dc-160">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="be9dc-160">Journal</span></span></th>
<th><span data-ttu-id="be9dc-161">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="be9dc-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="be9dc-162">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="be9dc-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="be9dc-163">Versio</span><span class="sxs-lookup"><span data-stu-id="be9dc-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-164">00001</span><span class="sxs-lookup"><span data-stu-id="be9dc-164">00001</span></span></td>
<td><span data-ttu-id="be9dc-165">Kustannustoiminnan laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="be9dc-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="be9dc-166">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="be9dc-166">Fiscal</span></span></td>
<td><span data-ttu-id="be9dc-167">2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-167">2017</span></span></td>
<td><span data-ttu-id="be9dc-168">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-168">Period 1</span></span></td>
<td><span data-ttu-id="be9dc-169">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="be9dc-170">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="be9dc-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="be9dc-171">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="be9dc-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="be9dc-172">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="be9dc-173">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="be9dc-173">Cost element</span></span></th>
<th><span data-ttu-id="be9dc-174">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="be9dc-174">Cost behavior</span></span></th>
<th><span data-ttu-id="be9dc-175">Summa</span><span class="sxs-lookup"><span data-stu-id="be9dc-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-176">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="be9dc-177">CC099</span><span class="sxs-lookup"><span data-stu-id="be9dc-177">CC099</span></span></td>
<td><span data-ttu-id="be9dc-178">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="be9dc-178">Default cost center</span></span></td>
<td><span data-ttu-id="be9dc-179">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-179">10001</span></span></td>
<td><span data-ttu-id="be9dc-180">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-180">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-181">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="be9dc-181">Unclassified</span></span></td>
<td><span data-ttu-id="be9dc-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="be9dc-183">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="be9dc-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="be9dc-184">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="be9dc-185">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="be9dc-185">Cost element</span></span></th>
<th><span data-ttu-id="be9dc-186">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="be9dc-186">Cost behavior</span></span></th>
<th><span data-ttu-id="be9dc-187">Summa</span><span class="sxs-lookup"><span data-stu-id="be9dc-187">Amount</span></span></th>
<th><span data-ttu-id="be9dc-188">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="be9dc-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-189">CC099</span><span class="sxs-lookup"><span data-stu-id="be9dc-189">CC099</span></span></td>
<td><span data-ttu-id="be9dc-190">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="be9dc-190">Default cost center</span></span></td>
<td><span data-ttu-id="be9dc-191">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-191">10001</span></span></td>
<td><span data-ttu-id="be9dc-192">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-192">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-193">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="be9dc-193">Unclassified</span></span></td>
<td><span data-ttu-id="be9dc-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-194">10,000.00</span></span></td>
<td><span data-ttu-id="be9dc-195">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-196">CC099</span><span class="sxs-lookup"><span data-stu-id="be9dc-196">CC099</span></span></td>
<td><span data-ttu-id="be9dc-197">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="be9dc-197">Default cost center</span></span></td>
<td><span data-ttu-id="be9dc-198">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-198">10001</span></span></td>
<td><span data-ttu-id="be9dc-199">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-199">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-200">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="be9dc-200">Unclassified</span></span></td>
<td><span data-ttu-id="be9dc-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-201">-10,000.00</span></span></td>
<td><span data-ttu-id="be9dc-202">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-203">CC099</span><span class="sxs-lookup"><span data-stu-id="be9dc-203">CC099</span></span></td>
<td><span data-ttu-id="be9dc-204">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="be9dc-204">Default cost center</span></span></td>
<td><span data-ttu-id="be9dc-205">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-205">10001</span></span></td>
<td><span data-ttu-id="be9dc-206">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-206">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-207">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-207">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-208">1,000.00</span></span></td>
<td><span data-ttu-id="be9dc-209">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-210">CC099</span><span class="sxs-lookup"><span data-stu-id="be9dc-210">CC099</span></span></td>
<td><span data-ttu-id="be9dc-211">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="be9dc-211">Default cost center</span></span></td>
<td><span data-ttu-id="be9dc-212">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-212">10001</span></span></td>
<td><span data-ttu-id="be9dc-213">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-213">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-214">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-214">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="be9dc-215">9,000.00</span></span></td>
<td><span data-ttu-id="be9dc-216">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="be9dc-217">Lisätietoja on kohdassa [Kustannustoimintakäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="be9dc-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="be9dc-218">Vaihe 2: Käsittele kustannusten jaon laskenta</span><span class="sxs-lookup"><span data-stu-id="be9dc-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="be9dc-219">Kustannusten jakoa käytetään kustannusten jakamiseen yhdestä kustannusobjektista toiseen (tai useampaan kustannusobjektiin) määrittämällä asiaankuuluvan kohdistusperusteen.</span><span class="sxs-lookup"><span data-stu-id="be9dc-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="be9dc-220">Kustannusten jako ja kustannusten kohdistus eroavat toisistaan sillä, että kustannusten jako tapahtuu aina alkuperäisen kustannuksen ensisijaisen kustannuselementin tasolla.</span><span class="sxs-lookup"><span data-stu-id="be9dc-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="be9dc-221">Määritä kustannusten jaon sääntö</span><span class="sxs-lookup"><span data-stu-id="be9dc-221">Define the cost distribution rule</span></span>

<span data-ttu-id="be9dc-222">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="be9dc-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="be9dc-223">Kustannuslaskenta ei tarjoa tästä tarpeeksi tarkkoja tietoja.</span><span class="sxs-lookup"><span data-stu-id="be9dc-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="be9dc-224">Muuttuva kustannus tulisi jakaa yksittäisille kustannusobjekteille reiluin perustein.</span><span class="sxs-lookup"><span data-stu-id="be9dc-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="be9dc-225">Loogisin kohdistusperuste on sähkönkulutus (kWh).</span><span class="sxs-lookup"><span data-stu-id="be9dc-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="be9dc-226">Luodaan tilastollinen dimensionjäsen nimeltä Sähkö, johon kirjataan sähkönkulutus.</span><span class="sxs-lookup"><span data-stu-id="be9dc-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="be9dc-227">Oletusarvon mukaan kaikki tilastolliset dimensiojäsenet ovat käytettävissä kohdistusperusteina.</span><span class="sxs-lookup"><span data-stu-id="be9dc-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="be9dc-228">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-228">Cost object</span></span></th>
<th><span data-ttu-id="be9dc-229">kWh</span><span class="sxs-lookup"><span data-stu-id="be9dc-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-230">CC001</span><span class="sxs-lookup"><span data-stu-id="be9dc-230">CC001</span></span></td>
<td><span data-ttu-id="be9dc-231">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="be9dc-231">HR</span></span></td>
<td><span data-ttu-id="be9dc-232">1 000</span><span class="sxs-lookup"><span data-stu-id="be9dc-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-233">CC002</span><span class="sxs-lookup"><span data-stu-id="be9dc-233">CC002</span></span></td>
<td><span data-ttu-id="be9dc-234">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="be9dc-234">Finance</span></span></td>
<td><span data-ttu-id="be9dc-235">6,000</span><span class="sxs-lookup"><span data-stu-id="be9dc-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-236">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-236">CC003</span></span></td>
<td><span data-ttu-id="be9dc-237">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="be9dc-237">Assembly</span></span></td>
<td><span data-ttu-id="be9dc-238">0</span><span class="sxs-lookup"><span data-stu-id="be9dc-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="be9dc-239">Seuraavassa taulukossa on esitetty tulos, kun sähkönkulutusta käytetään kohdistusperusteena muuttuville kuluille.</span><span class="sxs-lookup"><span data-stu-id="be9dc-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="be9dc-240">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-240">Cost object</span></span></th>
<th><span data-ttu-id="be9dc-241">Suuruus</span><span class="sxs-lookup"><span data-stu-id="be9dc-241">Magnitude</span></span></th>
<th><span data-ttu-id="be9dc-242">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="be9dc-242">Allocation factor</span></span></th>
<th><span data-ttu-id="be9dc-243">Summa</span><span class="sxs-lookup"><span data-stu-id="be9dc-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-244">CC001</span><span class="sxs-lookup"><span data-stu-id="be9dc-244">CC001</span></span></td>
<td><span data-ttu-id="be9dc-245">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="be9dc-245">HR</span></span></td>
<td><span data-ttu-id="be9dc-246">1 000</span><span class="sxs-lookup"><span data-stu-id="be9dc-246">1,000</span></span></td>
<td><span data-ttu-id="be9dc-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="be9dc-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="be9dc-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-249">CC002</span><span class="sxs-lookup"><span data-stu-id="be9dc-249">CC002</span></span></td>
<td><span data-ttu-id="be9dc-250">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="be9dc-250">Finance</span></span></td>
<td><span data-ttu-id="be9dc-251">6,000</span><span class="sxs-lookup"><span data-stu-id="be9dc-251">6,000</span></span></td>
<td><span data-ttu-id="be9dc-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="be9dc-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="be9dc-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-254">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-254">CC003</span></span></td>
<td><span data-ttu-id="be9dc-255">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="be9dc-255">Assembly</span></span></td>
<td><span data-ttu-id="be9dc-256">0</span><span class="sxs-lookup"><span data-stu-id="be9dc-256">0</span></span></td>
<td><span data-ttu-id="be9dc-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="be9dc-258">0,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="be9dc-259">Kiinteä kustannus tulisi jakaa tasaisesti yksittäisille kustannusobjekteille, jotka ovat kuluttaneet sähköä.</span><span class="sxs-lookup"><span data-stu-id="be9dc-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="be9dc-260">Voit käyttää sähkön tilastollista dimensiojäsentä kaavan kohdistusperusteena tämän tavoitteen saavuttamiseksi: (sähkö &gt;0,00) Seuraavassa taulukossa on esitetty tulos siitä, kun sähkönkulutus on määritetty muuttuvien kustannusten kohdistusperusteeksi.</span><span class="sxs-lookup"><span data-stu-id="be9dc-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="be9dc-261">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-261">Cost object</span></span></th>
<th><span data-ttu-id="be9dc-262">Resepti</span><span class="sxs-lookup"><span data-stu-id="be9dc-262">Formula</span></span></th>
<th><span data-ttu-id="be9dc-263">Suuruus</span><span class="sxs-lookup"><span data-stu-id="be9dc-263">Magnitude</span></span></th>
<th><span data-ttu-id="be9dc-264">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="be9dc-264">Allocation factor</span></span></th>
<th><span data-ttu-id="be9dc-265">Summa</span><span class="sxs-lookup"><span data-stu-id="be9dc-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-266">CC001</span><span class="sxs-lookup"><span data-stu-id="be9dc-266">CC001</span></span></td>
<td><span data-ttu-id="be9dc-267">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="be9dc-267">HR</span></span></td>
<td><span data-ttu-id="be9dc-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="be9dc-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="be9dc-269">1</span><span class="sxs-lookup"><span data-stu-id="be9dc-269">1</span></span></td>
<td><span data-ttu-id="be9dc-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="be9dc-271">500,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-272">CC002</span><span class="sxs-lookup"><span data-stu-id="be9dc-272">CC002</span></span></td>
<td><span data-ttu-id="be9dc-273">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="be9dc-273">Finance</span></span></td>
<td><span data-ttu-id="be9dc-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="be9dc-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="be9dc-275">1</span><span class="sxs-lookup"><span data-stu-id="be9dc-275">1</span></span></td>
<td><span data-ttu-id="be9dc-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="be9dc-277">500,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-278">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-278">CC003</span></span></td>
<td><span data-ttu-id="be9dc-279">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="be9dc-279">Assembly</span></span></td>
<td><span data-ttu-id="be9dc-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="be9dc-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="be9dc-281">0</span><span class="sxs-lookup"><span data-stu-id="be9dc-281">0</span></span></td>
<td><span data-ttu-id="be9dc-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="be9dc-283">0,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="be9dc-284">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="be9dc-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="be9dc-285">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="be9dc-285">Journal</span></span></th>
<th><span data-ttu-id="be9dc-286">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="be9dc-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="be9dc-287">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="be9dc-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="be9dc-288">Versio</span><span class="sxs-lookup"><span data-stu-id="be9dc-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-289">00002</span><span class="sxs-lookup"><span data-stu-id="be9dc-289">00002</span></span></td>
<td><span data-ttu-id="be9dc-290">Kustannusten jaon laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="be9dc-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="be9dc-291">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="be9dc-291">Fiscal</span></span></td>
<td><span data-ttu-id="be9dc-292">2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-292">2017</span></span></td>
<td><span data-ttu-id="be9dc-293">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-293">Period 1</span></span></td>
<td><span data-ttu-id="be9dc-294">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="be9dc-295">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="be9dc-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="be9dc-296">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="be9dc-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="be9dc-297">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="be9dc-298">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="be9dc-298">Cost element</span></span></th>
<th><span data-ttu-id="be9dc-299">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="be9dc-299">Cost behavior</span></span></th>
<th><span data-ttu-id="be9dc-300">Summa</span><span class="sxs-lookup"><span data-stu-id="be9dc-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-301">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="be9dc-302">CC099</span><span class="sxs-lookup"><span data-stu-id="be9dc-302">CC099</span></span></td>
<td><span data-ttu-id="be9dc-303">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="be9dc-303">Default cost center</span></span></td>
<td><span data-ttu-id="be9dc-304">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-304">10001</span></span></td>
<td><span data-ttu-id="be9dc-305">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-305">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-306">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-306">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-308">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="be9dc-309">CC099</span><span class="sxs-lookup"><span data-stu-id="be9dc-309">CC099</span></span></td>
<td><span data-ttu-id="be9dc-310">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="be9dc-310">Default cost center</span></span></td>
<td><span data-ttu-id="be9dc-311">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-311">10001</span></span></td>
<td><span data-ttu-id="be9dc-312">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-312">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-313">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-313">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="be9dc-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="be9dc-315">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="be9dc-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="be9dc-316">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="be9dc-317">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="be9dc-317">Cost element</span></span></th>
<th><span data-ttu-id="be9dc-318">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="be9dc-318">Cost behavior</span></span></th>
<th><span data-ttu-id="be9dc-319">Summa</span><span class="sxs-lookup"><span data-stu-id="be9dc-319">Amount</span></span></th>
<th><span data-ttu-id="be9dc-320">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="be9dc-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-321">CC099</span><span class="sxs-lookup"><span data-stu-id="be9dc-321">CC099</span></span></td>
<td><span data-ttu-id="be9dc-322">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="be9dc-322">Default cost center</span></span></td>
<td><span data-ttu-id="be9dc-323">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-323">10001</span></span></td>
<td><span data-ttu-id="be9dc-324">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-324">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-325">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-325">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-326">-1,000.00</span></span></td>
<td><span data-ttu-id="be9dc-327">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-328">CC001</span><span class="sxs-lookup"><span data-stu-id="be9dc-328">CC001</span></span></td>
<td><span data-ttu-id="be9dc-329">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="be9dc-329">HR</span></span></td>
<td><span data-ttu-id="be9dc-330">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-330">10001</span></span></td>
<td><span data-ttu-id="be9dc-331">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-331">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-332">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-332">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-333">500,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-333">500.00</span></span></td>
<td><span data-ttu-id="be9dc-334">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-335">CC002</span><span class="sxs-lookup"><span data-stu-id="be9dc-335">CC002</span></span></td>
<td><span data-ttu-id="be9dc-336">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="be9dc-336">Finance</span></span></td>
<td><span data-ttu-id="be9dc-337">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-337">10001</span></span></td>
<td><span data-ttu-id="be9dc-338">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-338">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-339">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-339">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-340">500,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-340">500.00</span></span></td>
<td><span data-ttu-id="be9dc-341">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-342">CC099</span><span class="sxs-lookup"><span data-stu-id="be9dc-342">CC099</span></span></td>
<td><span data-ttu-id="be9dc-343">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="be9dc-343">Default cost center</span></span></td>
<td><span data-ttu-id="be9dc-344">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-344">10001</span></span></td>
<td><span data-ttu-id="be9dc-345">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-345">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-346">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-346">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-347">-9,000.00</span></span></td>
<td><span data-ttu-id="be9dc-348">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-349">CC001</span><span class="sxs-lookup"><span data-stu-id="be9dc-349">CC001</span></span></td>
<td><span data-ttu-id="be9dc-350">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="be9dc-350">HR</span></span></td>
<td><span data-ttu-id="be9dc-351">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-351">10001</span></span></td>
<td><span data-ttu-id="be9dc-352">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-352">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-353">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-353">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="be9dc-354">1,285.71</span></span></td>
<td><span data-ttu-id="be9dc-355">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-356">CC002</span><span class="sxs-lookup"><span data-stu-id="be9dc-356">CC002</span></span></td>
<td><span data-ttu-id="be9dc-357">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="be9dc-357">Finance</span></span></td>
<td><span data-ttu-id="be9dc-358">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-358">10001</span></span></td>
<td><span data-ttu-id="be9dc-359">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-359">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-360">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-360">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="be9dc-361">7,714.29</span></span></td>
<td><span data-ttu-id="be9dc-362">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="be9dc-363">Lisätietoja on kohdassa [Jakelukäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="be9dc-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="be9dc-364">Vaihe 3: Käsittele yleiskustannustason laskenta</span><span class="sxs-lookup"><span data-stu-id="be9dc-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="be9dc-365">Yleiskustannustasolla veloitetaan yksi tai useampi määrätty kustannusobjekti.</span><span class="sxs-lookup"><span data-stu-id="be9dc-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="be9dc-366">Veloitus perustuu ennalta määrättyyn kustannustasoon sekä määritetyn kohdistusperusteen suuruuteen.</span><span class="sxs-lookup"><span data-stu-id="be9dc-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="be9dc-367">Määritä yleiskustannustaso.</span><span class="sxs-lookup"><span data-stu-id="be9dc-367">Define the overhead rate</span></span>

<span data-ttu-id="be9dc-368">Kustannusobjekti CC001 HR vaikuttaa joukkoon sisäisiä projekteja.</span><span class="sxs-lookup"><span data-stu-id="be9dc-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="be9dc-369">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon projektit.</span><span class="sxs-lookup"><span data-stu-id="be9dc-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="be9dc-370">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-370">Cost object</span></span></th>
<th><span data-ttu-id="be9dc-371">Tunnit</span><span class="sxs-lookup"><span data-stu-id="be9dc-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-372">Proj 1</span></span></td>
<td><span data-ttu-id="be9dc-373">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-373">Project 1</span></span></td>
<td><span data-ttu-id="be9dc-374">3</span><span class="sxs-lookup"><span data-stu-id="be9dc-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-375">Proj 2</span></span></td>
<td><span data-ttu-id="be9dc-376">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-376">Project 2</span></span></td>
<td><span data-ttu-id="be9dc-377">1</span><span class="sxs-lookup"><span data-stu-id="be9dc-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="be9dc-378">Kustannusprojektien osuudelle on määritetty ennalta kustannushinta.</span><span class="sxs-lookup"><span data-stu-id="be9dc-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="be9dc-379">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-379">Cost object</span></span></th>
<th><span data-ttu-id="be9dc-380">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="be9dc-380">Cost element</span></span></th>
<th><span data-ttu-id="be9dc-381">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="be9dc-381">Cost behavior</span></span></th>
<th><span data-ttu-id="be9dc-382">Yksiköt</span><span class="sxs-lookup"><span data-stu-id="be9dc-382">Units</span></span></th>
<th><span data-ttu-id="be9dc-383">Osuus</span><span class="sxs-lookup"><span data-stu-id="be9dc-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-384">CC001</span><span class="sxs-lookup"><span data-stu-id="be9dc-384">CC001</span></span></td>
<td><span data-ttu-id="be9dc-385">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="be9dc-385">HR</span></span></td>
<td><span data-ttu-id="be9dc-386">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-386">10001</span></span></td>
<td><span data-ttu-id="be9dc-387">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-387">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-388">1</span><span class="sxs-lookup"><span data-stu-id="be9dc-388">1</span></span></td>
<td><span data-ttu-id="be9dc-389">10</span><span class="sxs-lookup"><span data-stu-id="be9dc-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="be9dc-390">Seuraavassa taulukossa on esitetty tulos, kun Henkilöstöhallinnon projekteja käytetään kohdistusperusteena.</span><span class="sxs-lookup"><span data-stu-id="be9dc-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="be9dc-391">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-391">Cost object</span></span></th>
<th><span data-ttu-id="be9dc-392">Suuruus</span><span class="sxs-lookup"><span data-stu-id="be9dc-392">Magnitude</span></span></th>
<th><span data-ttu-id="be9dc-393">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="be9dc-393">Cost element</span></span></th>
<th><span data-ttu-id="be9dc-394">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="be9dc-394">Allocation factor</span></span></th>
<th><span data-ttu-id="be9dc-395">Summa</span><span class="sxs-lookup"><span data-stu-id="be9dc-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-396">Proj 1</span></span></td>
<td><span data-ttu-id="be9dc-397">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-397">Project 1</span></span></td>
<td><span data-ttu-id="be9dc-398">3</span><span class="sxs-lookup"><span data-stu-id="be9dc-398">3</span></span></td>
<td><span data-ttu-id="be9dc-399">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-399">10001</span></span></td>
<td><span data-ttu-id="be9dc-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="be9dc-401">30,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-402">Proj 2</span></span></td>
<td><span data-ttu-id="be9dc-403">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-403">Project 2</span></span></td>
<td><span data-ttu-id="be9dc-404">1</span><span class="sxs-lookup"><span data-stu-id="be9dc-404">1</span></span></td>
<td><span data-ttu-id="be9dc-405">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-405">10001</span></span></td>
<td><span data-ttu-id="be9dc-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="be9dc-407">10,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="be9dc-408">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="be9dc-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="be9dc-409">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="be9dc-409">Journal</span></span></th>
<th><span data-ttu-id="be9dc-410">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="be9dc-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="be9dc-411">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="be9dc-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="be9dc-412">Versio</span><span class="sxs-lookup"><span data-stu-id="be9dc-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-413">00003</span><span class="sxs-lookup"><span data-stu-id="be9dc-413">00003</span></span></td>
<td><span data-ttu-id="be9dc-414">Yleiskustannustason laskelman kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="be9dc-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="be9dc-415">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="be9dc-415">Fiscal</span></span></td>
<td><span data-ttu-id="be9dc-416">2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-416">2017</span></span></td>
<td><span data-ttu-id="be9dc-417">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-417">Period 1</span></span></td>
<td><span data-ttu-id="be9dc-418">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="be9dc-419">Kirjauskansioviennit (Yleiskustannustason laskennan kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="be9dc-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="be9dc-420">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="be9dc-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="be9dc-421">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-421">Cost object</span></span></th>
<th><span data-ttu-id="be9dc-422">Suuruus</span><span class="sxs-lookup"><span data-stu-id="be9dc-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-423">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="be9dc-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-424">Proj 1</span></span></td>
<td><span data-ttu-id="be9dc-425">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="be9dc-426">3,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-427">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="be9dc-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-428">Proj 2</span></span></td>
<td><span data-ttu-id="be9dc-429">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="be9dc-430">1,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="be9dc-431">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="be9dc-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="be9dc-432">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="be9dc-433">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="be9dc-433">Cost element</span></span></th>
<th><span data-ttu-id="be9dc-434">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="be9dc-434">Cost behavior</span></span></th>
<th><span data-ttu-id="be9dc-435">Summa</span><span class="sxs-lookup"><span data-stu-id="be9dc-435">Amount</span></span></th>
<th><span data-ttu-id="be9dc-436">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="be9dc-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="be9dc-437">CC0001</span></span></td>
<td><span data-ttu-id="be9dc-438">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="be9dc-438">HR</span></span></td>
<td><span data-ttu-id="be9dc-439">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-439">10001</span></span></td>
<td><span data-ttu-id="be9dc-440">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-440">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-441">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-441">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-442">-30.00</span></span></td>
<td><span data-ttu-id="be9dc-443">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-444">Proj 1</span></span></td>
<td><span data-ttu-id="be9dc-445">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="be9dc-446">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-446">10001</span></span></td>
<td><span data-ttu-id="be9dc-447">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-447">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-448">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-448">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-449">30,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-449">30.00</span></span></td>
<td><span data-ttu-id="be9dc-450">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-451">CC001</span><span class="sxs-lookup"><span data-stu-id="be9dc-451">CC001</span></span></td>
<td><span data-ttu-id="be9dc-452">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="be9dc-452">HR</span></span></td>
<td><span data-ttu-id="be9dc-453">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-453">10001</span></span></td>
<td><span data-ttu-id="be9dc-454">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-454">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-455">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-455">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-456">-10.00</span></span></td>
<td><span data-ttu-id="be9dc-457">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-458">Proj 2</span></span></td>
<td><span data-ttu-id="be9dc-459">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="be9dc-460">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-460">10001</span></span></td>
<td><span data-ttu-id="be9dc-461">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-461">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-462">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-462">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-463">10.00</span><span class="sxs-lookup"><span data-stu-id="be9dc-463">10.00</span></span></td>
<td><span data-ttu-id="be9dc-464">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="be9dc-465">Lisätietoja on kohdassa [Yleisen laskennan suorittaminen](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="be9dc-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="be9dc-466">Vaihe 4: Käsittele kustannusten kohdistuksen laskenta</span><span class="sxs-lookup"><span data-stu-id="be9dc-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="be9dc-467">Kohdistuksella kustannusobjektin saldo liitetään toisiin kustannusobjekteihin käyttämällä kohdistusperustetta.</span><span class="sxs-lookup"><span data-stu-id="be9dc-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="be9dc-468">Finance and Operations tukee vastavuoroista kohdistusmenetelmää.</span><span class="sxs-lookup"><span data-stu-id="be9dc-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="be9dc-469">Vastavuoroisessa kohdistusmenetelmässä tunnistetaan oheiskustannusobjektien käyttämät, keskinäiset palvelut täysin.</span><span class="sxs-lookup"><span data-stu-id="be9dc-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="be9dc-470">Järjestelmä määrittää oikean kohdistusjärjestyksen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="be9dc-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="be9dc-471">Kustannusobjektin saldo kohdistetaan yhdellä kohdistusperusteella.</span><span class="sxs-lookup"><span data-stu-id="be9dc-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="be9dc-472">Kustannusobjektien dimensiot ja niiden vastaavat jäsenet ylittävät kohdistukset ovat tuettuja.</span><span class="sxs-lookup"><span data-stu-id="be9dc-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="be9dc-473">Kustannusseurantayksikkö hallitsee kohdistusjärjestystä.</span><span class="sxs-lookup"><span data-stu-id="be9dc-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="be9dc-474">[![Vastavuoroinen menetelmä](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="be9dc-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="be9dc-475">Määritä kustannuksen kohdistus</span><span class="sxs-lookup"><span data-stu-id="be9dc-475">Define the cost allocation</span></span>

<span data-ttu-id="be9dc-476">Tämä on yksinkertainen esimerkki, jossa kerrotaan, miten voit jäljittää kustannuksen virran.</span><span class="sxs-lookup"><span data-stu-id="be9dc-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="be9dc-477">Kustannusobjekti CC001 HR liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="be9dc-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="be9dc-478">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="be9dc-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="be9dc-479">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-479">Cost object</span></span></th>
<th><span data-ttu-id="be9dc-480">HR-palvelut</span><span class="sxs-lookup"><span data-stu-id="be9dc-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-481">CC002</span><span class="sxs-lookup"><span data-stu-id="be9dc-481">CC002</span></span></td>
<td><span data-ttu-id="be9dc-482">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="be9dc-482">Finance</span></span></td>
<td><span data-ttu-id="be9dc-483">35</span><span class="sxs-lookup"><span data-stu-id="be9dc-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-484">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-484">CC003</span></span></td>
<td><span data-ttu-id="be9dc-485">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="be9dc-485">Assembly</span></span></td>
<td><span data-ttu-id="be9dc-486">55</span><span class="sxs-lookup"><span data-stu-id="be9dc-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-487">CC004</span><span class="sxs-lookup"><span data-stu-id="be9dc-487">CC004</span></span></td>
<td><span data-ttu-id="be9dc-488">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="be9dc-488">Packaging</span></span></td>
<td><span data-ttu-id="be9dc-489">10</span><span class="sxs-lookup"><span data-stu-id="be9dc-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="be9dc-490">Kustannusobjekti CC002 Taloushallinto liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="be9dc-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="be9dc-491">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Taloushallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="be9dc-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="be9dc-492">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-492">Cost object</span></span></th>
<th><span data-ttu-id="be9dc-493">Taloushallinnon palvelut</span><span class="sxs-lookup"><span data-stu-id="be9dc-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-494">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-494">CC003</span></span></td>
<td><span data-ttu-id="be9dc-495">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="be9dc-495">Assembly</span></span></td>
<td><span data-ttu-id="be9dc-496">65</span><span class="sxs-lookup"><span data-stu-id="be9dc-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-497">CC004</span><span class="sxs-lookup"><span data-stu-id="be9dc-497">CC004</span></span></td>
<td><span data-ttu-id="be9dc-498">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="be9dc-498">Packaging</span></span></td>
<td><span data-ttu-id="be9dc-499">35</span><span class="sxs-lookup"><span data-stu-id="be9dc-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="be9dc-500">Kustannusobjekti CC003 Kokoonpano liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="be9dc-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="be9dc-501">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Kokoonpanopalvelut.</span><span class="sxs-lookup"><span data-stu-id="be9dc-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="be9dc-502">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-502">Cost object</span></span></th>
<th><span data-ttu-id="be9dc-503">Kokoonpanopalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="be9dc-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-504">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-504">Prod 1</span></span></td>
<td><span data-ttu-id="be9dc-505">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-505">Product 1</span></span></td>
<td><span data-ttu-id="be9dc-506">60</span><span class="sxs-lookup"><span data-stu-id="be9dc-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-507">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-507">Prod 2</span></span></td>
<td><span data-ttu-id="be9dc-508">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-508">Product 2</span></span></td>
<td><span data-ttu-id="be9dc-509">20</span><span class="sxs-lookup"><span data-stu-id="be9dc-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="be9dc-510">Kustannusobjekti CC004 Pakkaus liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="be9dc-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="be9dc-511">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Pakkauspalvelut.</span><span class="sxs-lookup"><span data-stu-id="be9dc-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="be9dc-512">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-512">Cost object</span></span></th>
<th><span data-ttu-id="be9dc-513">Pakkauspalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="be9dc-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-514">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-514">Prod 1</span></span></td>
<td><span data-ttu-id="be9dc-515">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-515">Product 1</span></span></td>
<td><span data-ttu-id="be9dc-516">80</span><span class="sxs-lookup"><span data-stu-id="be9dc-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-517">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-517">Prod 2</span></span></td>
<td><span data-ttu-id="be9dc-518">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-518">Product 2</span></span></td>
<td><span data-ttu-id="be9dc-519">päivänä</span><span class="sxs-lookup"><span data-stu-id="be9dc-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="be9dc-520">Finance and Operationsissa tilastomittaukset, kuten tämän tuotteen kuluttamat tuotantotunnit, voidaan johtaa lähdetiedoista.</span><span class="sxs-lookup"><span data-stu-id="be9dc-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="be9dc-521">Lisätietoja on kohdassa [Tilastomittauksen lähdemalli](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="be9dc-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="be9dc-522">Seuraavassa taulukossa näytetään tulos, kun henkilöstöhallinnon palveluja käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="be9dc-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="be9dc-523">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-523">Cost object</span></span></th>
<th><span data-ttu-id="be9dc-524">Suuruus</span><span class="sxs-lookup"><span data-stu-id="be9dc-524">Magnitude</span></span></th>
<th><span data-ttu-id="be9dc-525">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="be9dc-525">Allocation factor</span></span></th>
<th><span data-ttu-id="be9dc-526">Summa</span><span class="sxs-lookup"><span data-stu-id="be9dc-526">Amount</span></span></th>
<th><span data-ttu-id="be9dc-527">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="be9dc-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-528">CC002</span><span class="sxs-lookup"><span data-stu-id="be9dc-528">CC002</span></span></td>
<td><span data-ttu-id="be9dc-529">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="be9dc-529">Finance</span></span></td>
<td><span data-ttu-id="be9dc-530">35</span><span class="sxs-lookup"><span data-stu-id="be9dc-530">35</span></span></td>
<td><span data-ttu-id="be9dc-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="be9dc-532">175.00</span><span class="sxs-lookup"><span data-stu-id="be9dc-532">175.00</span></span></td>
<td><span data-ttu-id="be9dc-533">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-534">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-534">CC003</span></span></td>
<td><span data-ttu-id="be9dc-535">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="be9dc-535">Assembly</span></span></td>
<td><span data-ttu-id="be9dc-536">55</span><span class="sxs-lookup"><span data-stu-id="be9dc-536">55</span></span></td>
<td><span data-ttu-id="be9dc-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="be9dc-538">275.00</span><span class="sxs-lookup"><span data-stu-id="be9dc-538">275.00</span></span></td>
<td><span data-ttu-id="be9dc-539">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-540">CC004</span><span class="sxs-lookup"><span data-stu-id="be9dc-540">CC004</span></span></td>
<td><span data-ttu-id="be9dc-541">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="be9dc-541">Packaging</span></span></td>
<td><span data-ttu-id="be9dc-542">10</span><span class="sxs-lookup"><span data-stu-id="be9dc-542">10</span></span></td>
<td><span data-ttu-id="be9dc-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="be9dc-544">50,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-544">50.00</span></span></td>
<td><span data-ttu-id="be9dc-545">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-546">CC002</span><span class="sxs-lookup"><span data-stu-id="be9dc-546">CC002</span></span></td>
<td><span data-ttu-id="be9dc-547">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="be9dc-547">Finance</span></span></td>
<td><span data-ttu-id="be9dc-548">35</span><span class="sxs-lookup"><span data-stu-id="be9dc-548">35</span></span></td>
<td><span data-ttu-id="be9dc-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="be9dc-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="be9dc-550">436.00</span><span class="sxs-lookup"><span data-stu-id="be9dc-550">436.00</span></span></td>
<td><span data-ttu-id="be9dc-551">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-552">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-552">CC003</span></span></td>
<td><span data-ttu-id="be9dc-553">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="be9dc-553">Assembly</span></span></td>
<td><span data-ttu-id="be9dc-554">55</span><span class="sxs-lookup"><span data-stu-id="be9dc-554">55</span></span></td>
<td><span data-ttu-id="be9dc-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="be9dc-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="be9dc-556">685.14</span><span class="sxs-lookup"><span data-stu-id="be9dc-556">685.14</span></span></td>
<td><span data-ttu-id="be9dc-557">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-558">CC004</span><span class="sxs-lookup"><span data-stu-id="be9dc-558">CC004</span></span></td>
<td><span data-ttu-id="be9dc-559">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="be9dc-559">Packaging</span></span></td>
<td><span data-ttu-id="be9dc-560">10</span><span class="sxs-lookup"><span data-stu-id="be9dc-560">10</span></span></td>
<td><span data-ttu-id="be9dc-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="be9dc-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="be9dc-562">124.57</span><span class="sxs-lookup"><span data-stu-id="be9dc-562">124.57</span></span></td>
<td><span data-ttu-id="be9dc-563">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="be9dc-564">Seuraavassa taulukossa näytetään tulos, kun Taloushallinnon palveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="be9dc-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="be9dc-565">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-565">Cost object</span></span></th>
<th><span data-ttu-id="be9dc-566">Suuruus</span><span class="sxs-lookup"><span data-stu-id="be9dc-566">Magnitude</span></span></th>
<th><span data-ttu-id="be9dc-567">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="be9dc-567">Allocation factor</span></span></th>
<th><span data-ttu-id="be9dc-568">Summa</span><span class="sxs-lookup"><span data-stu-id="be9dc-568">Amount</span></span></th>
<th><span data-ttu-id="be9dc-569">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="be9dc-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-570">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-570">CC003</span></span></td>
<td><span data-ttu-id="be9dc-571">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="be9dc-571">Assembly</span></span></td>
<td><span data-ttu-id="be9dc-572">65</span><span class="sxs-lookup"><span data-stu-id="be9dc-572">65</span></span></td>
<td><span data-ttu-id="be9dc-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="be9dc-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="be9dc-574">438.75</span><span class="sxs-lookup"><span data-stu-id="be9dc-574">438.75</span></span></td>
<td><span data-ttu-id="be9dc-575">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-576">CC004</span><span class="sxs-lookup"><span data-stu-id="be9dc-576">CC004</span></span></td>
<td><span data-ttu-id="be9dc-577">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="be9dc-577">Packaging</span></span></td>
<td><span data-ttu-id="be9dc-578">35</span><span class="sxs-lookup"><span data-stu-id="be9dc-578">35</span></span></td>
<td><span data-ttu-id="be9dc-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="be9dc-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="be9dc-580">236.25</span><span class="sxs-lookup"><span data-stu-id="be9dc-580">236.25</span></span></td>
<td><span data-ttu-id="be9dc-581">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-582">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-582">CC003</span></span></td>
<td><span data-ttu-id="be9dc-583">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="be9dc-583">Assembly</span></span></td>
<td><span data-ttu-id="be9dc-584">65</span><span class="sxs-lookup"><span data-stu-id="be9dc-584">65</span></span></td>
<td><span data-ttu-id="be9dc-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="be9dc-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="be9dc-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="be9dc-586">5,297.69</span></span></td>
<td><span data-ttu-id="be9dc-587">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-588">CC004</span><span class="sxs-lookup"><span data-stu-id="be9dc-588">CC004</span></span></td>
<td><span data-ttu-id="be9dc-589">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="be9dc-589">Packaging</span></span></td>
<td><span data-ttu-id="be9dc-590">35</span><span class="sxs-lookup"><span data-stu-id="be9dc-590">35</span></span></td>
<td><span data-ttu-id="be9dc-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="be9dc-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="be9dc-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="be9dc-592">2,852.60</span></span></td>
<td><span data-ttu-id="be9dc-593">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="be9dc-594">Seuraavassa taulukossa näytetään tulos, kun Kokoonpanopalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="be9dc-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="be9dc-595">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-595">Cost object</span></span></th>
<th><span data-ttu-id="be9dc-596">Suuruus</span><span class="sxs-lookup"><span data-stu-id="be9dc-596">Magnitude</span></span></th>
<th><span data-ttu-id="be9dc-597">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="be9dc-597">Allocation factor</span></span></th>
<th><span data-ttu-id="be9dc-598">Summa</span><span class="sxs-lookup"><span data-stu-id="be9dc-598">Amount</span></span></th>
<th><span data-ttu-id="be9dc-599">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="be9dc-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-600">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-600">Prod 1</span></span></td>
<td><span data-ttu-id="be9dc-601">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-601">Product 1</span></span></td>
<td><span data-ttu-id="be9dc-602">60</span><span class="sxs-lookup"><span data-stu-id="be9dc-602">60</span></span></td>
<td><span data-ttu-id="be9dc-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="be9dc-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="be9dc-604">535.31</span><span class="sxs-lookup"><span data-stu-id="be9dc-604">535.31</span></span></td>
<td><span data-ttu-id="be9dc-605">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-606">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-606">Prod 2</span></span></td>
<td><span data-ttu-id="be9dc-607">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-607">Product 2</span></span></td>
<td><span data-ttu-id="be9dc-608">20</span><span class="sxs-lookup"><span data-stu-id="be9dc-608">20</span></span></td>
<td><span data-ttu-id="be9dc-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="be9dc-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="be9dc-610">178.44</span><span class="sxs-lookup"><span data-stu-id="be9dc-610">178.44</span></span></td>
<td><span data-ttu-id="be9dc-611">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-612">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-612">Prod 1</span></span></td>
<td><span data-ttu-id="be9dc-613">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-613">Product 1</span></span></td>
<td><span data-ttu-id="be9dc-614">60</span><span class="sxs-lookup"><span data-stu-id="be9dc-614">60</span></span></td>
<td><span data-ttu-id="be9dc-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="be9dc-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="be9dc-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="be9dc-616">4,487.12</span></span></td>
<td><span data-ttu-id="be9dc-617">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-618">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-618">Prod 2</span></span></td>
<td><span data-ttu-id="be9dc-619">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-619">Product 2</span></span></td>
<td><span data-ttu-id="be9dc-620">20</span><span class="sxs-lookup"><span data-stu-id="be9dc-620">20</span></span></td>
<td><span data-ttu-id="be9dc-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="be9dc-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="be9dc-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="be9dc-622">1,495.71</span></span></td>
<td><span data-ttu-id="be9dc-623">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="be9dc-624">Seuraavassa taulukossa näytetään tulos, kun Pakkauspalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="be9dc-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="be9dc-625">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-625">Cost object</span></span></th>
<th><span data-ttu-id="be9dc-626">Suuruus</span><span class="sxs-lookup"><span data-stu-id="be9dc-626">Magnitude</span></span></th>
<th><span data-ttu-id="be9dc-627">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="be9dc-627">Allocation factor</span></span></th>
<th><span data-ttu-id="be9dc-628">Summa</span><span class="sxs-lookup"><span data-stu-id="be9dc-628">Amount</span></span></th>
<th><span data-ttu-id="be9dc-629">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="be9dc-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-630">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-630">Prod 1</span></span></td>
<td><span data-ttu-id="be9dc-631">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-631">Product 1</span></span></td>
<td><span data-ttu-id="be9dc-632">80</span><span class="sxs-lookup"><span data-stu-id="be9dc-632">80</span></span></td>
<td><span data-ttu-id="be9dc-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="be9dc-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="be9dc-634">241.05</span><span class="sxs-lookup"><span data-stu-id="be9dc-634">241.05</span></span></td>
<td><span data-ttu-id="be9dc-635">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-636">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-636">Prod 2</span></span></td>
<td><span data-ttu-id="be9dc-637">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-637">Product 2</span></span></td>
<td><span data-ttu-id="be9dc-638">15</span><span class="sxs-lookup"><span data-stu-id="be9dc-638">15</span></span></td>
<td><span data-ttu-id="be9dc-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="be9dc-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="be9dc-640">45.20</span><span class="sxs-lookup"><span data-stu-id="be9dc-640">45.20</span></span></td>
<td><span data-ttu-id="be9dc-641">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-642">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-642">Prod 1</span></span></td>
<td><span data-ttu-id="be9dc-643">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-643">Product 1</span></span></td>
<td><span data-ttu-id="be9dc-644">80</span><span class="sxs-lookup"><span data-stu-id="be9dc-644">80</span></span></td>
<td><span data-ttu-id="be9dc-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="be9dc-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="be9dc-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="be9dc-646">2,507.09</span></span></td>
<td><span data-ttu-id="be9dc-647">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-648">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-648">Prod 2</span></span></td>
<td><span data-ttu-id="be9dc-649">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-649">Product 2</span></span></td>
<td><span data-ttu-id="be9dc-650">15</span><span class="sxs-lookup"><span data-stu-id="be9dc-650">15</span></span></td>
<td><span data-ttu-id="be9dc-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="be9dc-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="be9dc-652">470.08</span><span class="sxs-lookup"><span data-stu-id="be9dc-652">470.08</span></span></td>
<td><span data-ttu-id="be9dc-653">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="be9dc-654">Kirjauskansioviennit (kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="be9dc-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="be9dc-655">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="be9dc-655">Journal</span></span></th>
<th><span data-ttu-id="be9dc-656">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="be9dc-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="be9dc-657">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="be9dc-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="be9dc-658">Versio</span><span class="sxs-lookup"><span data-stu-id="be9dc-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-659">00004</span><span class="sxs-lookup"><span data-stu-id="be9dc-659">00004</span></span></td>
<td><span data-ttu-id="be9dc-660">Kustannusten kohdistuskirjauskansio</span><span class="sxs-lookup"><span data-stu-id="be9dc-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="be9dc-661">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="be9dc-661">Fiscal</span></span></td>
<td><span data-ttu-id="be9dc-662">2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-662">2017</span></span></td>
<td><span data-ttu-id="be9dc-663">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-663">Period 1</span></span></td>
<td><span data-ttu-id="be9dc-664">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="be9dc-665">Kirjauskansion rivit</span><span class="sxs-lookup"><span data-stu-id="be9dc-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="be9dc-666">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="be9dc-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="be9dc-667">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="be9dc-668">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="be9dc-668">Cost element</span></span></th>
<th><span data-ttu-id="be9dc-669">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="be9dc-669">Cost behavior</span></span></th>
<th><span data-ttu-id="be9dc-670">Summa</span><span class="sxs-lookup"><span data-stu-id="be9dc-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-671">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="be9dc-672">CC001</span><span class="sxs-lookup"><span data-stu-id="be9dc-672">CC001</span></span></td>
<td><span data-ttu-id="be9dc-673">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="be9dc-673">HR</span></span></td>
<td><span data-ttu-id="be9dc-674">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-674">10001</span></span></td>
<td><span data-ttu-id="be9dc-675">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-675">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-676">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-676">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-677">500,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-678">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="be9dc-679">CC001</span><span class="sxs-lookup"><span data-stu-id="be9dc-679">CC001</span></span></td>
<td><span data-ttu-id="be9dc-680">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="be9dc-680">HR</span></span></td>
<td><span data-ttu-id="be9dc-681">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-681">10001</span></span></td>
<td><span data-ttu-id="be9dc-682">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-682">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-683">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-683">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="be9dc-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-685">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="be9dc-686">CC002</span><span class="sxs-lookup"><span data-stu-id="be9dc-686">CC002</span></span></td>
<td><span data-ttu-id="be9dc-687">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="be9dc-687">Finance</span></span></td>
<td><span data-ttu-id="be9dc-688">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-688">10001</span></span></td>
<td><span data-ttu-id="be9dc-689">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-689">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-690">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-690">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-691">675.00</span><span class="sxs-lookup"><span data-stu-id="be9dc-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-692">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="be9dc-693">CC002</span><span class="sxs-lookup"><span data-stu-id="be9dc-693">CC002</span></span></td>
<td><span data-ttu-id="be9dc-694">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="be9dc-694">Finance</span></span></td>
<td><span data-ttu-id="be9dc-695">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-695">10001</span></span></td>
<td><span data-ttu-id="be9dc-696">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-696">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-697">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-697">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="be9dc-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-699">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="be9dc-700">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-700">CC003</span></span></td>
<td><span data-ttu-id="be9dc-701">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="be9dc-701">Assembly</span></span></td>
<td><span data-ttu-id="be9dc-702">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-702">10001</span></span></td>
<td><span data-ttu-id="be9dc-703">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-703">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-704">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-704">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-705">713.75</span><span class="sxs-lookup"><span data-stu-id="be9dc-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-706">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="be9dc-707">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-707">CC003</span></span></td>
<td><span data-ttu-id="be9dc-708">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="be9dc-708">Assembly</span></span></td>
<td><span data-ttu-id="be9dc-709">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-709">10001</span></span></td>
<td><span data-ttu-id="be9dc-710">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-710">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-711">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-711">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="be9dc-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-713">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="be9dc-714">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-714">CC003</span></span></td>
<td><span data-ttu-id="be9dc-715">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="be9dc-715">Packaging</span></span></td>
<td><span data-ttu-id="be9dc-716">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-716">10001</span></span></td>
<td><span data-ttu-id="be9dc-717">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-717">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-718">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-718">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-719">286.25</span><span class="sxs-lookup"><span data-stu-id="be9dc-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-720">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="be9dc-721">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-721">CC003</span></span></td>
<td><span data-ttu-id="be9dc-722">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="be9dc-722">Packaging</span></span></td>
<td><span data-ttu-id="be9dc-723">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-723">10001</span></span></td>
<td><span data-ttu-id="be9dc-724">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-724">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-725">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-725">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="be9dc-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-727">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="be9dc-728">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-728">Prod 1</span></span></td>
<td><span data-ttu-id="be9dc-729">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-729">Product 1</span></span></td>
<td><span data-ttu-id="be9dc-730">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-730">10001</span></span></td>
<td><span data-ttu-id="be9dc-731">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-731">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-732">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-732">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-733">776.36</span><span class="sxs-lookup"><span data-stu-id="be9dc-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-734">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="be9dc-735">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-735">Prod 1</span></span></td>
<td><span data-ttu-id="be9dc-736">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-736">Product 1</span></span></td>
<td><span data-ttu-id="be9dc-737">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-737">10001</span></span></td>
<td><span data-ttu-id="be9dc-738">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-738">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-739">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-739">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="be9dc-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-741">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="be9dc-742">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-742">Prod 2</span></span></td>
<td><span data-ttu-id="be9dc-743">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-743">Product 1</span></span></td>
<td><span data-ttu-id="be9dc-744">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-744">10001</span></span></td>
<td><span data-ttu-id="be9dc-745">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-745">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-746">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-746">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-747">223.64</span><span class="sxs-lookup"><span data-stu-id="be9dc-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-748">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="be9dc-749">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-749">Prod 2</span></span></td>
<td><span data-ttu-id="be9dc-750">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-750">Product 1</span></span></td>
<td><span data-ttu-id="be9dc-751">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-751">10001</span></span></td>
<td><span data-ttu-id="be9dc-752">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-752">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-753">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-753">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="be9dc-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="be9dc-755">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="be9dc-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="be9dc-756">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="be9dc-757">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="be9dc-757">Cost element</span></span></th>
<th><span data-ttu-id="be9dc-758">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="be9dc-758">Cost behavior</span></span></th>
<th><span data-ttu-id="be9dc-759">Summa</span><span class="sxs-lookup"><span data-stu-id="be9dc-759">Amount</span></span></th>
<th><span data-ttu-id="be9dc-760">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="be9dc-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be9dc-761">CC001</span><span class="sxs-lookup"><span data-stu-id="be9dc-761">CC001</span></span></td>
<td><span data-ttu-id="be9dc-762">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="be9dc-762">HR</span></span></td>
<td><span data-ttu-id="be9dc-763">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-763">10001</span></span></td>
<td><span data-ttu-id="be9dc-764">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-764">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-765">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-765">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-766">-500.00</span></span></td>
<td><span data-ttu-id="be9dc-767">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-768">CC002</span><span class="sxs-lookup"><span data-stu-id="be9dc-768">CC002</span></span></td>
<td><span data-ttu-id="be9dc-769">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="be9dc-769">Finance</span></span></td>
<td><span data-ttu-id="be9dc-770">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-770">10001</span></span></td>
<td><span data-ttu-id="be9dc-771">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-771">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-772">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-772">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-773">175.00</span><span class="sxs-lookup"><span data-stu-id="be9dc-773">175.00</span></span></td>
<td><span data-ttu-id="be9dc-774">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-775">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-775">CC003</span></span></td>
<td><span data-ttu-id="be9dc-776">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="be9dc-776">Assembly</span></span></td>
<td><span data-ttu-id="be9dc-777">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-777">10001</span></span></td>
<td><span data-ttu-id="be9dc-778">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-778">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-779">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-779">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-780">275.00</span><span class="sxs-lookup"><span data-stu-id="be9dc-780">275.00</span></span></td>
<td><span data-ttu-id="be9dc-781">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-782">CC004</span><span class="sxs-lookup"><span data-stu-id="be9dc-782">CC004</span></span></td>
<td><span data-ttu-id="be9dc-783">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="be9dc-783">Packaging</span></span></td>
<td><span data-ttu-id="be9dc-784">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-784">10001</span></span></td>
<td><span data-ttu-id="be9dc-785">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-785">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-786">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-786">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-787">50,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-787">50,00</span></span></td>
<td><span data-ttu-id="be9dc-788">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-789">CC001</span><span class="sxs-lookup"><span data-stu-id="be9dc-789">CC001</span></span></td>
<td><span data-ttu-id="be9dc-790">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="be9dc-790">HR</span></span></td>
<td><span data-ttu-id="be9dc-791">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-791">10001</span></span></td>
<td><span data-ttu-id="be9dc-792">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-792">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-793">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-793">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="be9dc-794">-1,245.71</span></span></td>
<td><span data-ttu-id="be9dc-795">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-796">CC002</span><span class="sxs-lookup"><span data-stu-id="be9dc-796">CC002</span></span></td>
<td><span data-ttu-id="be9dc-797">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="be9dc-797">Finance</span></span></td>
<td><span data-ttu-id="be9dc-798">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-798">10001</span></span></td>
<td><span data-ttu-id="be9dc-799">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-799">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-800">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-800">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-801">436.00</span><span class="sxs-lookup"><span data-stu-id="be9dc-801">436.00</span></span></td>
<td><span data-ttu-id="be9dc-802">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-803">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-803">CC003</span></span></td>
<td><span data-ttu-id="be9dc-804">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="be9dc-804">Assembly</span></span></td>
<td><span data-ttu-id="be9dc-805">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-805">10001</span></span></td>
<td><span data-ttu-id="be9dc-806">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-806">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-807">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-807">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-808">685.14</span><span class="sxs-lookup"><span data-stu-id="be9dc-808">685.14</span></span></td>
<td><span data-ttu-id="be9dc-809">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-810">CC004</span><span class="sxs-lookup"><span data-stu-id="be9dc-810">CC004</span></span></td>
<td><span data-ttu-id="be9dc-811">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="be9dc-811">Packaging</span></span></td>
<td><span data-ttu-id="be9dc-812">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-812">10001</span></span></td>
<td><span data-ttu-id="be9dc-813">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-813">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-814">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-814">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-815">124.57</span><span class="sxs-lookup"><span data-stu-id="be9dc-815">124.57</span></span></td>
<td><span data-ttu-id="be9dc-816">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-817">CC002</span><span class="sxs-lookup"><span data-stu-id="be9dc-817">CC002</span></span></td>
<td><span data-ttu-id="be9dc-818">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="be9dc-818">Finance</span></span></td>
<td><span data-ttu-id="be9dc-819">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-819">10001</span></span></td>
<td><span data-ttu-id="be9dc-820">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-820">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-821">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-821">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-822">-675.00</span></span></td>
<td><span data-ttu-id="be9dc-823">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-824">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-824">CC003</span></span></td>
<td><span data-ttu-id="be9dc-825">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="be9dc-825">Assembly</span></span></td>
<td><span data-ttu-id="be9dc-826">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-826">10001</span></span></td>
<td><span data-ttu-id="be9dc-827">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-827">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-828">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-828">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-829">438.75</span><span class="sxs-lookup"><span data-stu-id="be9dc-829">438.75</span></span></td>
<td><span data-ttu-id="be9dc-830">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-831">CC004</span><span class="sxs-lookup"><span data-stu-id="be9dc-831">CC004</span></span></td>
<td><span data-ttu-id="be9dc-832">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="be9dc-832">Packaging</span></span></td>
<td><span data-ttu-id="be9dc-833">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-833">10001</span></span></td>
<td><span data-ttu-id="be9dc-834">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-834">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-835">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-835">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-836">236.25</span><span class="sxs-lookup"><span data-stu-id="be9dc-836">236.25</span></span></td>
<td><span data-ttu-id="be9dc-837">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-838">CC002</span><span class="sxs-lookup"><span data-stu-id="be9dc-838">CC002</span></span></td>
<td><span data-ttu-id="be9dc-839">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="be9dc-839">Finance</span></span></td>
<td><span data-ttu-id="be9dc-840">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-840">10001</span></span></td>
<td><span data-ttu-id="be9dc-841">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-841">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-842">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-842">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="be9dc-843">-8,150.29</span></span></td>
<td><span data-ttu-id="be9dc-844">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-845">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-845">CC003</span></span></td>
<td><span data-ttu-id="be9dc-846">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="be9dc-846">Assembly</span></span></td>
<td><span data-ttu-id="be9dc-847">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-847">10001</span></span></td>
<td><span data-ttu-id="be9dc-848">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-848">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-849">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-849">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="be9dc-850">5,297.69</span></span></td>
<td><span data-ttu-id="be9dc-851">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-852">CC004</span><span class="sxs-lookup"><span data-stu-id="be9dc-852">CC004</span></span></td>
<td><span data-ttu-id="be9dc-853">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="be9dc-853">Packaging</span></span></td>
<td><span data-ttu-id="be9dc-854">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-854">10001</span></span></td>
<td><span data-ttu-id="be9dc-855">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-855">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-856">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-856">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="be9dc-857">2,852.60</span></span></td>
<td><span data-ttu-id="be9dc-858">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-859">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-859">CC003</span></span></td>
<td><span data-ttu-id="be9dc-860">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="be9dc-860">Assembly</span></span></td>
<td><span data-ttu-id="be9dc-861">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-861">10001</span></span></td>
<td><span data-ttu-id="be9dc-862">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-862">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-863">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-863">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="be9dc-864">-713.75</span></span></td>
<td><span data-ttu-id="be9dc-865">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-866">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-866">Prod 1</span></span></td>
<td><span data-ttu-id="be9dc-867">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-867">Product 1</span></span></td>
<td><span data-ttu-id="be9dc-868">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-868">10001</span></span></td>
<td><span data-ttu-id="be9dc-869">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-869">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-870">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-870">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-871">535.31</span><span class="sxs-lookup"><span data-stu-id="be9dc-871">535.31</span></span></td>
<td><span data-ttu-id="be9dc-872">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-873">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-873">Prod 2</span></span></td>
<td><span data-ttu-id="be9dc-874">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-874">Product 2</span></span></td>
<td><span data-ttu-id="be9dc-875">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-875">10001</span></span></td>
<td><span data-ttu-id="be9dc-876">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-876">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-877">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-877">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-878">178.44</span><span class="sxs-lookup"><span data-stu-id="be9dc-878">178.44</span></span></td>
<td><span data-ttu-id="be9dc-879">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-880">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-880">CC003</span></span></td>
<td><span data-ttu-id="be9dc-881">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="be9dc-881">Assembly</span></span></td>
<td><span data-ttu-id="be9dc-882">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-882">10001</span></span></td>
<td><span data-ttu-id="be9dc-883">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-883">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-884">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-884">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="be9dc-885">-5,982.83</span></span></td>
<td><span data-ttu-id="be9dc-886">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-887">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-887">Prod 1</span></span></td>
<td><span data-ttu-id="be9dc-888">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-888">Product 1</span></span></td>
<td><span data-ttu-id="be9dc-889">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-889">10001</span></span></td>
<td><span data-ttu-id="be9dc-890">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-890">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-891">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-891">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="be9dc-892">4,487.12</span></span></td>
<td><span data-ttu-id="be9dc-893">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-894">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-894">Prod 2</span></span></td>
<td><span data-ttu-id="be9dc-895">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-895">Product 2</span></span></td>
<td><span data-ttu-id="be9dc-896">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-896">10001</span></span></td>
<td><span data-ttu-id="be9dc-897">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-897">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-898">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-898">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="be9dc-899">1,495.71</span></span></td>
<td><span data-ttu-id="be9dc-900">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-901">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-901">CC003</span></span></td>
<td><span data-ttu-id="be9dc-902">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="be9dc-902">Assembly</span></span></td>
<td><span data-ttu-id="be9dc-903">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-903">10001</span></span></td>
<td><span data-ttu-id="be9dc-904">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-904">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-905">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-905">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="be9dc-906">-286.25</span></span></td>
<td><span data-ttu-id="be9dc-907">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-908">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-908">Prod 1</span></span></td>
<td><span data-ttu-id="be9dc-909">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-909">Product 1</span></span></td>
<td><span data-ttu-id="be9dc-910">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-910">10001</span></span></td>
<td><span data-ttu-id="be9dc-911">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-911">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-912">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-912">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-913">241.05</span><span class="sxs-lookup"><span data-stu-id="be9dc-913">241.05</span></span></td>
<td><span data-ttu-id="be9dc-914">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-915">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-915">Prod 2</span></span></td>
<td><span data-ttu-id="be9dc-916">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-916">Product 2</span></span></td>
<td><span data-ttu-id="be9dc-917">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-917">10001</span></span></td>
<td><span data-ttu-id="be9dc-918">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-918">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-919">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-919">Fixed cost</span></span></td>
<td><span data-ttu-id="be9dc-920">45.20</span><span class="sxs-lookup"><span data-stu-id="be9dc-920">45.20</span></span></td>
<td><span data-ttu-id="be9dc-921">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-922">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-922">CC003</span></span></td>
<td><span data-ttu-id="be9dc-923">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="be9dc-923">Assembly</span></span></td>
<td><span data-ttu-id="be9dc-924">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-924">10001</span></span></td>
<td><span data-ttu-id="be9dc-925">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-925">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-926">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-926">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-927">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="be9dc-927">-2,977.17</span></span></td>
<td><span data-ttu-id="be9dc-928">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-929">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-929">Prod 1</span></span></td>
<td><span data-ttu-id="be9dc-930">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-930">Product 1</span></span></td>
<td><span data-ttu-id="be9dc-931">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-931">10001</span></span></td>
<td><span data-ttu-id="be9dc-932">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-932">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-933">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-933">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="be9dc-934">2,507.09</span></span></td>
<td><span data-ttu-id="be9dc-935">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be9dc-936">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-936">Prod 2</span></span></td>
<td><span data-ttu-id="be9dc-937">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-937">Product 2</span></span></td>
<td><span data-ttu-id="be9dc-938">10 001</span><span class="sxs-lookup"><span data-stu-id="be9dc-938">10001</span></span></td>
<td><span data-ttu-id="be9dc-939">Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-939">Electricity</span></span></td>
<td><span data-ttu-id="be9dc-940">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-940">Variable cost</span></span></td>
<td><span data-ttu-id="be9dc-941">470.08</span><span class="sxs-lookup"><span data-stu-id="be9dc-941">470.08</span></span></td>
<td><span data-ttu-id="be9dc-942">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="be9dc-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="be9dc-943">Johtopäätökset</span><span class="sxs-lookup"><span data-stu-id="be9dc-943">Conclusion</span></span>
<span data-ttu-id="be9dc-944">Kirjanpidossa kirjataan tyhjään kustannuspaikkatunnukseen sähkökustannus arvolla 10 000,00.</span><span class="sxs-lookup"><span data-stu-id="be9dc-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="be9dc-945">Tämän ansiosta kustannuslaskijat tietävät, että kustannus on kohdistettava.</span><span class="sxs-lookup"><span data-stu-id="be9dc-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="be9dc-946">Kustannukset virtaavat kirjanpidossa organisaation yksiköiden ja tasojen läpi käytössä olevien käytäntöjen ja sääntöjen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="be9dc-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="be9dc-947">Kukin kustannus on liitetty kustannusperusteeseen, joka sisältää parhaan arvion kustannusten kohdistuksesta.</span><span class="sxs-lookup"><span data-stu-id="be9dc-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="be9dc-948">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="be9dc-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="be9dc-949">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="be9dc-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="be9dc-950">Yhteensä</span><span class="sxs-lookup"><span data-stu-id="be9dc-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="be9dc-951">CC099</span><span class="sxs-lookup"><span data-stu-id="be9dc-951">CC099</span></span></th>
<th><span data-ttu-id="be9dc-952">CC001</span><span class="sxs-lookup"><span data-stu-id="be9dc-952">CC001</span></span></th>
<th><span data-ttu-id="be9dc-953">CC002</span><span class="sxs-lookup"><span data-stu-id="be9dc-953">CC002</span></span></th>
<th><span data-ttu-id="be9dc-954">CC003</span><span class="sxs-lookup"><span data-stu-id="be9dc-954">CC003</span></span></th>
<th><span data-ttu-id="be9dc-955">CC004</span><span class="sxs-lookup"><span data-stu-id="be9dc-955">CC004</span></span></th>
<th><span data-ttu-id="be9dc-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-956">Proj 1</span></span></th>
<th><span data-ttu-id="be9dc-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-957">Proj 2</span></span></th>
<th><span data-ttu-id="be9dc-958">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="be9dc-958">Prod 1</span></span></th>
<th><span data-ttu-id="be9dc-959">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="be9dc-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="be9dc-960">10001 Sähkö</span><span class="sxs-lookup"><span data-stu-id="be9dc-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="be9dc-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="be9dc-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="be9dc-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="be9dc-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="be9dc-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="be9dc-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="be9dc-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="be9dc-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="be9dc-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="be9dc-970">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="be9dc-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-971">0,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="be9dc-972">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="be9dc-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-973">0,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-974">0,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-975">0,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-976">0,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-977">0,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-978">776.36</span><span class="sxs-lookup"><span data-stu-id="be9dc-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-979">223.64</span><span class="sxs-lookup"><span data-stu-id="be9dc-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="be9dc-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="be9dc-981">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="be9dc-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-982">000</span><span class="sxs-lookup"><span data-stu-id="be9dc-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-983">0,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-984">0,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-985">0,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-986">0,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-987">30,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-988">10,00</span><span class="sxs-lookup"><span data-stu-id="be9dc-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="be9dc-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="be9dc-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="be9dc-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="be9dc-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="be9dc-992">Tässä ohjeaiheessa esitellään, miten ensisijainen kustannuselementti, 10001 Sähkö, virtaa kustannusobjektien läpi.</span><span class="sxs-lookup"><span data-stu-id="be9dc-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="be9dc-993">Tästä syystä tämä yleiskustannus kohdistetaan organisaation alimmalle tasolle.</span><span class="sxs-lookup"><span data-stu-id="be9dc-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="be9dc-994">Toisin sanoen alimman tason kustannusobjektit kantavat kustannuksen.</span><span class="sxs-lookup"><span data-stu-id="be9dc-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="be9dc-995">Jos tarvitset visuaalisen näkymän kustannuksen virrasta kustannusobjektien välillä, voit käyttää kustannuksen koontikäytäntösääntöjä kustannusvirran visualisointiin.</span><span class="sxs-lookup"><span data-stu-id="be9dc-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="be9dc-996">Lisätietoja on kohdassa [Kustannusten koonti](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="be9dc-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



