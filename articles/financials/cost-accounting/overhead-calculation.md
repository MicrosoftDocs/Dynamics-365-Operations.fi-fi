---
title: Yleiskustannuslaskenta
description: "Tässä aiheessa kuvataan tyypillinen yleiskustannusten laskenta- ja kohdistusprosessi."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 936e54c0ef1de449afda2392cd1fbb304eed631b
ms.contentlocale: fi-fi
ms.lasthandoff: 01/17/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="4e959-103">Yleiskustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="4e959-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4e959-104">Tässä aiheessa kuvataan tyypillinen yleiskustannusten laskenta- ja kohdistusprosessi.</span><span class="sxs-lookup"><span data-stu-id="4e959-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="4e959-105">Sanaston määritelmä</span><span class="sxs-lookup"><span data-stu-id="4e959-105">Term definition</span></span>
---------------

<span data-ttu-id="4e959-106">Yleiskustannukset ovat yrityksen toiminnasta syntyviä kustannuksia, joita ei voi suoraan liittää mihinkään tiettyyn liiketoiminnan tehtävään, tuotteeseen tai palveluun.</span><span class="sxs-lookup"><span data-stu-id="4e959-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="4e959-107">Yleiskustannukset ovat tärkeä tuki voittoa tuottavien tehtävien luonnissa.</span><span class="sxs-lookup"><span data-stu-id="4e959-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="4e959-108">Seuraavassa on joitakin esimerkkejä yleiskustannuksista:</span><span class="sxs-lookup"><span data-stu-id="4e959-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="4e959-109">Vuokra</span><span class="sxs-lookup"><span data-stu-id="4e959-109">Rent</span></span>
-   <span data-ttu-id="4e959-110">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-110">Electricity</span></span>
-   <span data-ttu-id="4e959-111">Hallinnon palkat</span><span class="sxs-lookup"><span data-stu-id="4e959-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="4e959-112">Yleiskustannuslaskennan yleiskuva</span><span class="sxs-lookup"><span data-stu-id="4e959-112">Overhead calculation overview</span></span>
<span data-ttu-id="4e959-113">Yleiskustannusten laskenta suorittaa kustannuslaskennan käytännöt oikeassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="4e959-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="4e959-114">Yleiskustannusten laskennan voi suorittaa useita kertoja samalle tilikaudelle, jos kustannuslaskennan käytännöt ovat muuttuneet tai erityisiä virheitä on havaittu.</span><span class="sxs-lookup"><span data-stu-id="4e959-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="4e959-115">Kukin laskenta-ajo tallennetaan ja kullekin annetaan yksilöllinen versiotunnus, jonka avulla eri laskenta-ajoja voi verrata toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="4e959-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="4e959-116">Yleiskustannusten laskenta luo kustannustapahtumia, joille annetaan kirjauspäivä.</span><span class="sxs-lookup"><span data-stu-id="4e959-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="4e959-117">Kirjauspäivä vastaa laskennassa käytettyä tilikauden päättymispäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="4e959-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="4e959-118">Yksilöivä versiotunnus sisältää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="4e959-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="4e959-119">Versiotyyppi</span><span class="sxs-lookup"><span data-stu-id="4e959-119">Version type</span></span>
-   <span data-ttu-id="4e959-120">Päivämäärä ja aika</span><span class="sxs-lookup"><span data-stu-id="4e959-120">Date and time</span></span>
-   <span data-ttu-id="4e959-121">Kustannuslaskennan kirjanpito</span><span class="sxs-lookup"><span data-stu-id="4e959-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="4e959-122">Tilikausi </span><span class="sxs-lookup"><span data-stu-id="4e959-122">Fiscal year</span></span>
-   <span data-ttu-id="4e959-123">Tilikausi  </span><span class="sxs-lookup"><span data-stu-id="4e959-123">Fiscal period</span></span>

<span data-ttu-id="4e959-124">Yleiskustannusten laskenta ajetaan versiosta riippumattomana.</span><span class="sxs-lookup"><span data-stu-id="4e959-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="4e959-125">Voit siis laskea budjetin version ennen todellista versiota.</span><span class="sxs-lookup"><span data-stu-id="4e959-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="4e959-126">Yleiskustannusten laskenta koostuu neljästä vaiheesta, jotka esitellään seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="4e959-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="4e959-127">Kussakin vaiheessa luodaan kirjauskansion otsikko, jolla on kirjauskansiovientejä.</span><span class="sxs-lookup"><span data-stu-id="4e959-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="4e959-128">Tämä kirjauskansion otsikko säilyttää kunkin laskentavaiheen syöttötiedot.</span><span class="sxs-lookup"><span data-stu-id="4e959-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="4e959-129">Käytännöt ja säännöt ajetaan kullekin kirjauskansion riville, ja tuloksena luodaan kustannustapahtumia.</span><span class="sxs-lookup"><span data-stu-id="4e959-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="4e959-130">Tämän ansiosta kaikki laskutoimitukset ovat täysin jäljitettävissä.</span><span class="sxs-lookup"><span data-stu-id="4e959-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="4e959-131">[![Yleiskustannuslaskenta](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="4e959-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="4e959-132">Laske ja kohdista sähkön yleiskustannukset</span><span class="sxs-lookup"><span data-stu-id="4e959-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="4e959-133">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="4e959-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="4e959-134">Tarkka johdon näkymä ei täten ole saatavilla kustannuslaskennassa.</span><span class="sxs-lookup"><span data-stu-id="4e959-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="4e959-135">Jotta kustannuslaskenta tarjoaisi oikean johdon näkymän kaikista organisaation yksiköistä ja tasoista, kustannusten on virrattava organisaation yksiköiden läpi.</span><span class="sxs-lookup"><span data-stu-id="4e959-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="4e959-136">Tämän virran on perustuttava joko tarkkaan tietoon kulutuksesta tai perusteltuun arvioon.</span><span class="sxs-lookup"><span data-stu-id="4e959-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="4e959-137">Sähkökustannukset voi kirjata kirjanpitoon seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="4e959-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e959-138">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="4e959-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4e959-139">Kustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="4e959-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="4e959-140">Päätili</span><span class="sxs-lookup"><span data-stu-id="4e959-140">Main account</span></span></th>
<th><span data-ttu-id="4e959-141">Summa kirjanpitovaluuttana</span><span class="sxs-lookup"><span data-stu-id="4e959-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-142">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="4e959-143">CC099</span><span class="sxs-lookup"><span data-stu-id="4e959-143">CC099</span></span></td>
<td><span data-ttu-id="4e959-144">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="4e959-144">Default cost center</span></span></td>
<td><span data-ttu-id="4e959-145">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-145">10001</span></span></td>
<td><span data-ttu-id="4e959-146">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-146">Electricity</span></span></td>
<td><span data-ttu-id="4e959-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="4e959-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="4e959-148">Vaihe 1: Käsittele kustannustoiminnan laskenta</span><span class="sxs-lookup"><span data-stu-id="4e959-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="4e959-149">Kun kustannustapahtumat tuodaan lähdetiedoista, niille asetetaan kustannuslaskennassa oletusarvoisesti **Luokittelematon** -kustannustoimintaluokka.</span><span class="sxs-lookup"><span data-stu-id="4e959-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="4e959-150">Voit luokitella kustannustapahtumia uudelleen **kiinteäksi kustannukseksi** tai **muuttuvaksi kustannukseksi** kustannustoiminnan käytäntösäännöillä.</span><span class="sxs-lookup"><span data-stu-id="4e959-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="4e959-151">Määritä kustannustoiminnan sääntö</span><span class="sxs-lookup"><span data-stu-id="4e959-151">Define the cost behavior rule</span></span>

<span data-ttu-id="4e959-152">Joissain tapauksissa osa kustannuksesta on kiinteä ja loppuosa perustuu kulutukseen.</span><span class="sxs-lookup"><span data-stu-id="4e959-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="4e959-153">Sähkölaskut sopivat usein tähän määritelmään.</span><span class="sxs-lookup"><span data-stu-id="4e959-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="4e959-154">Maksat ensin määrätyn, kiinteän maksun, jonka lisäksi maksat kulutuksesta kilowattitunteina (kWh).</span><span class="sxs-lookup"><span data-stu-id="4e959-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="4e959-155">Jos kiinteä maksu on esimerkiksi 1 000,00, kustannustoiminnan sääntö määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4e959-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="4e959-156">Kiinteä määrä 1 000,00</span><span class="sxs-lookup"><span data-stu-id="4e959-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="4e959-157">0 &lt;= 1 000,00 = Kiinteä</span><span class="sxs-lookup"><span data-stu-id="4e959-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="4e959-158">1000,01 &lt; N = Muuttuva</span><span class="sxs-lookup"><span data-stu-id="4e959-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="4e959-159">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="4e959-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e959-160">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="4e959-160">Journal</span></span></th>
<th><span data-ttu-id="4e959-161">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="4e959-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4e959-162">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="4e959-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4e959-163">Versio</span><span class="sxs-lookup"><span data-stu-id="4e959-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-164">00001</span><span class="sxs-lookup"><span data-stu-id="4e959-164">00001</span></span></td>
<td><span data-ttu-id="4e959-165">Kustannustoiminnan laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="4e959-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="4e959-166">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="4e959-166">Fiscal</span></span></td>
<td><span data-ttu-id="4e959-167">2017</span><span class="sxs-lookup"><span data-stu-id="4e959-167">2017</span></span></td>
<td><span data-ttu-id="4e959-168">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="4e959-168">Period 1</span></span></td>
<td><span data-ttu-id="4e959-169">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="4e959-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4e959-170">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="4e959-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e959-171">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="4e959-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4e959-172">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4e959-173">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="4e959-173">Cost element</span></span></th>
<th><span data-ttu-id="4e959-174">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="4e959-174">Cost behavior</span></span></th>
<th><span data-ttu-id="4e959-175">Summa</span><span class="sxs-lookup"><span data-stu-id="4e959-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-176">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="4e959-177">CC099</span><span class="sxs-lookup"><span data-stu-id="4e959-177">CC099</span></span></td>
<td><span data-ttu-id="4e959-178">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="4e959-178">Default cost center</span></span></td>
<td><span data-ttu-id="4e959-179">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-179">10001</span></span></td>
<td><span data-ttu-id="4e959-180">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-180">Electricity</span></span></td>
<td><span data-ttu-id="4e959-181">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="4e959-181">Unclassified</span></span></td>
<td><span data-ttu-id="4e959-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="4e959-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4e959-183">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="4e959-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e959-184">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4e959-185">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="4e959-185">Cost element</span></span></th>
<th><span data-ttu-id="4e959-186">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="4e959-186">Cost behavior</span></span></th>
<th><span data-ttu-id="4e959-187">Summa</span><span class="sxs-lookup"><span data-stu-id="4e959-187">Amount</span></span></th>
<th><span data-ttu-id="4e959-188">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="4e959-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-189">CC099</span><span class="sxs-lookup"><span data-stu-id="4e959-189">CC099</span></span></td>
<td><span data-ttu-id="4e959-190">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="4e959-190">Default cost center</span></span></td>
<td><span data-ttu-id="4e959-191">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-191">10001</span></span></td>
<td><span data-ttu-id="4e959-192">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-192">Electricity</span></span></td>
<td><span data-ttu-id="4e959-193">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="4e959-193">Unclassified</span></span></td>
<td><span data-ttu-id="4e959-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="4e959-194">10,000.00</span></span></td>
<td><span data-ttu-id="4e959-195">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-196">CC099</span><span class="sxs-lookup"><span data-stu-id="4e959-196">CC099</span></span></td>
<td><span data-ttu-id="4e959-197">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="4e959-197">Default cost center</span></span></td>
<td><span data-ttu-id="4e959-198">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-198">10001</span></span></td>
<td><span data-ttu-id="4e959-199">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-199">Electricity</span></span></td>
<td><span data-ttu-id="4e959-200">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="4e959-200">Unclassified</span></span></td>
<td><span data-ttu-id="4e959-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="4e959-201">-10,000.00</span></span></td>
<td><span data-ttu-id="4e959-202">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-203">CC099</span><span class="sxs-lookup"><span data-stu-id="4e959-203">CC099</span></span></td>
<td><span data-ttu-id="4e959-204">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="4e959-204">Default cost center</span></span></td>
<td><span data-ttu-id="4e959-205">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-205">10001</span></span></td>
<td><span data-ttu-id="4e959-206">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-206">Electricity</span></span></td>
<td><span data-ttu-id="4e959-207">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-207">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="4e959-208">1,000.00</span></span></td>
<td><span data-ttu-id="4e959-209">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-210">CC099</span><span class="sxs-lookup"><span data-stu-id="4e959-210">CC099</span></span></td>
<td><span data-ttu-id="4e959-211">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="4e959-211">Default cost center</span></span></td>
<td><span data-ttu-id="4e959-212">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-212">10001</span></span></td>
<td><span data-ttu-id="4e959-213">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-213">Electricity</span></span></td>
<td><span data-ttu-id="4e959-214">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-214">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="4e959-215">9,000.00</span></span></td>
<td><span data-ttu-id="4e959-216">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e959-217">Lisätietoja kustannustoiminnasta on kohdassa Kustannustoimintakäytännöt.</span><span class="sxs-lookup"><span data-stu-id="4e959-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="4e959-218">(Huomaa, että ohjeaihe ei ole vielä valmis; se on saatavilla pian.)</span><span class="sxs-lookup"><span data-stu-id="4e959-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="4e959-219">Vaihe 2: Käsittele kustannusten jaon laskenta</span><span class="sxs-lookup"><span data-stu-id="4e959-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="4e959-220">Kustannusten jakoa käytetään kustannusten jakamiseen yhdestä kustannusobjektista toiseen (tai useampaan kustannusobjektiin) määrittämällä asiaankuuluvan kohdistusperusteen.</span><span class="sxs-lookup"><span data-stu-id="4e959-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="4e959-221">Kustannusten jako ja kustannusten kohdistus eroavat toisistaan sillä, että kustannusten jako tapahtuu aina alkuperäisen kustannuksen ensisijaisen kustannuselementin tasolla.</span><span class="sxs-lookup"><span data-stu-id="4e959-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="4e959-222">Määritä kustannusten jaon sääntö</span><span class="sxs-lookup"><span data-stu-id="4e959-222">Define the cost distribution rule</span></span>

<span data-ttu-id="4e959-223">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="4e959-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="4e959-224">Kustannuslaskenta ei tarjoa tästä tarpeeksi tarkkoja tietoja.</span><span class="sxs-lookup"><span data-stu-id="4e959-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="4e959-225">Muuttuva kustannus tulisi jakaa yksittäisille kustannusobjekteille reiluin perustein.</span><span class="sxs-lookup"><span data-stu-id="4e959-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="4e959-226">Loogisin kohdistusperuste on sähkönkulutus (kWh).</span><span class="sxs-lookup"><span data-stu-id="4e959-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="4e959-227">Luodaan tilastollinen dimensionjäsen nimeltä Sähkö, johon kirjataan sähkönkulutus.</span><span class="sxs-lookup"><span data-stu-id="4e959-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="4e959-228">Oletusarvon mukaan kaikki tilastolliset dimensiojäsenet ovat käytettävissä kohdistusperusteina.</span><span class="sxs-lookup"><span data-stu-id="4e959-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e959-229">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-229">Cost object</span></span></th>
<th><span data-ttu-id="4e959-230">kWh</span><span class="sxs-lookup"><span data-stu-id="4e959-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-231">CC001</span><span class="sxs-lookup"><span data-stu-id="4e959-231">CC001</span></span></td>
<td><span data-ttu-id="4e959-232">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="4e959-232">HR</span></span></td>
<td><span data-ttu-id="4e959-233">1 000</span><span class="sxs-lookup"><span data-stu-id="4e959-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-234">CC002</span><span class="sxs-lookup"><span data-stu-id="4e959-234">CC002</span></span></td>
<td><span data-ttu-id="4e959-235">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="4e959-235">Finance</span></span></td>
<td><span data-ttu-id="4e959-236">6,000</span><span class="sxs-lookup"><span data-stu-id="4e959-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-237">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-237">CC003</span></span></td>
<td><span data-ttu-id="4e959-238">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="4e959-238">Assembly</span></span></td>
<td><span data-ttu-id="4e959-239">0</span><span class="sxs-lookup"><span data-stu-id="4e959-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e959-240">Seuraavassa taulukossa on esitetty tulos, kun sähkönkulutusta käytetään kohdistusperusteena muuttuville kuluille.</span><span class="sxs-lookup"><span data-stu-id="4e959-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e959-241">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-241">Cost object</span></span></th>
<th><span data-ttu-id="4e959-242">Suuruus</span><span class="sxs-lookup"><span data-stu-id="4e959-242">Magnitude</span></span></th>
<th><span data-ttu-id="4e959-243">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="4e959-243">Allocation factor</span></span></th>
<th><span data-ttu-id="4e959-244">Summa</span><span class="sxs-lookup"><span data-stu-id="4e959-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-245">CC001</span><span class="sxs-lookup"><span data-stu-id="4e959-245">CC001</span></span></td>
<td><span data-ttu-id="4e959-246">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="4e959-246">HR</span></span></td>
<td><span data-ttu-id="4e959-247">1 000</span><span class="sxs-lookup"><span data-stu-id="4e959-247">1,000</span></span></td>
<td><span data-ttu-id="4e959-248">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="4e959-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4e959-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4e959-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-250">CC002</span><span class="sxs-lookup"><span data-stu-id="4e959-250">CC002</span></span></td>
<td><span data-ttu-id="4e959-251">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="4e959-251">Finance</span></span></td>
<td><span data-ttu-id="4e959-252">6,000</span><span class="sxs-lookup"><span data-stu-id="4e959-252">6,000</span></span></td>
<td><span data-ttu-id="4e959-253">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="4e959-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4e959-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4e959-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-255">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-255">CC003</span></span></td>
<td><span data-ttu-id="4e959-256">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="4e959-256">Assembly</span></span></td>
<td><span data-ttu-id="4e959-257">0</span><span class="sxs-lookup"><span data-stu-id="4e959-257">0</span></span></td>
<td><span data-ttu-id="4e959-258">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="4e959-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4e959-259">0,00</span><span class="sxs-lookup"><span data-stu-id="4e959-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e959-260">Kiinteä kustannus tulisi jakaa tasaisesti yksittäisille kustannusobjekteille, jotka ovat kuluttaneet sähköä.</span><span class="sxs-lookup"><span data-stu-id="4e959-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="4e959-261">Voit käyttää sähkön tilastollista dimensiojäsentä kaavan kohdistusperusteena tämän tavoitteen saavuttamiseksi: (sähkö &gt;0,00) Seuraavassa taulukossa on esitetty tulos siitä, kun sähkönkulutus on määritetty muuttuvien kustannusten kohdistusperusteeksi.</span><span class="sxs-lookup"><span data-stu-id="4e959-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e959-262">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-262">Cost object</span></span></th>
<th><span data-ttu-id="4e959-263">Resepti</span><span class="sxs-lookup"><span data-stu-id="4e959-263">Formula</span></span></th>
<th><span data-ttu-id="4e959-264">Suuruus</span><span class="sxs-lookup"><span data-stu-id="4e959-264">Magnitude</span></span></th>
<th><span data-ttu-id="4e959-265">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="4e959-265">Allocation factor</span></span></th>
<th><span data-ttu-id="4e959-266">Summa</span><span class="sxs-lookup"><span data-stu-id="4e959-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-267">CC001</span><span class="sxs-lookup"><span data-stu-id="4e959-267">CC001</span></span></td>
<td><span data-ttu-id="4e959-268">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="4e959-268">HR</span></span></td>
<td><span data-ttu-id="4e959-269">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4e959-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4e959-270">1</span><span class="sxs-lookup"><span data-stu-id="4e959-270">1</span></span></td>
<td><span data-ttu-id="4e959-271">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="4e959-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4e959-272">500,00</span><span class="sxs-lookup"><span data-stu-id="4e959-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-273">CC002</span><span class="sxs-lookup"><span data-stu-id="4e959-273">CC002</span></span></td>
<td><span data-ttu-id="4e959-274">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="4e959-274">Finance</span></span></td>
<td><span data-ttu-id="4e959-275">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4e959-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4e959-276">1</span><span class="sxs-lookup"><span data-stu-id="4e959-276">1</span></span></td>
<td><span data-ttu-id="4e959-277">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="4e959-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4e959-278">500,00</span><span class="sxs-lookup"><span data-stu-id="4e959-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-279">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-279">CC003</span></span></td>
<td><span data-ttu-id="4e959-280">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="4e959-280">Assembly</span></span></td>
<td><span data-ttu-id="4e959-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4e959-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4e959-282">0</span><span class="sxs-lookup"><span data-stu-id="4e959-282">0</span></span></td>
<td><span data-ttu-id="4e959-283">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="4e959-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4e959-284">0,00</span><span class="sxs-lookup"><span data-stu-id="4e959-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4e959-285">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="4e959-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e959-286">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="4e959-286">Journal</span></span></th>
<th><span data-ttu-id="4e959-287">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="4e959-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4e959-288">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="4e959-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4e959-289">Versio</span><span class="sxs-lookup"><span data-stu-id="4e959-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-290">00002</span><span class="sxs-lookup"><span data-stu-id="4e959-290">00002</span></span></td>
<td><span data-ttu-id="4e959-291">Kustannusten jaon laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="4e959-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="4e959-292">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="4e959-292">Fiscal</span></span></td>
<td><span data-ttu-id="4e959-293">2017</span><span class="sxs-lookup"><span data-stu-id="4e959-293">2017</span></span></td>
<td><span data-ttu-id="4e959-294">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="4e959-294">Period 1</span></span></td>
<td><span data-ttu-id="4e959-295">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="4e959-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4e959-296">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="4e959-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e959-297">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="4e959-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4e959-298">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4e959-299">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="4e959-299">Cost element</span></span></th>
<th><span data-ttu-id="4e959-300">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="4e959-300">Cost behavior</span></span></th>
<th><span data-ttu-id="4e959-301">Summa</span><span class="sxs-lookup"><span data-stu-id="4e959-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-302">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e959-303">CC099</span><span class="sxs-lookup"><span data-stu-id="4e959-303">CC099</span></span></td>
<td><span data-ttu-id="4e959-304">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="4e959-304">Default cost center</span></span></td>
<td><span data-ttu-id="4e959-305">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-305">10001</span></span></td>
<td><span data-ttu-id="4e959-306">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-306">Electricity</span></span></td>
<td><span data-ttu-id="4e959-307">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-307">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-308">1 000,00</span><span class="sxs-lookup"><span data-stu-id="4e959-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-309">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e959-310">CC099</span><span class="sxs-lookup"><span data-stu-id="4e959-310">CC099</span></span></td>
<td><span data-ttu-id="4e959-311">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="4e959-311">Default cost center</span></span></td>
<td><span data-ttu-id="4e959-312">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-312">10001</span></span></td>
<td><span data-ttu-id="4e959-313">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-313">Electricity</span></span></td>
<td><span data-ttu-id="4e959-314">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-314">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="4e959-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4e959-316">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="4e959-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e959-317">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4e959-318">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="4e959-318">Cost element</span></span></th>
<th><span data-ttu-id="4e959-319">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="4e959-319">Cost behavior</span></span></th>
<th><span data-ttu-id="4e959-320">Summa</span><span class="sxs-lookup"><span data-stu-id="4e959-320">Amount</span></span></th>
<th><span data-ttu-id="4e959-321">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="4e959-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-322">CC099</span><span class="sxs-lookup"><span data-stu-id="4e959-322">CC099</span></span></td>
<td><span data-ttu-id="4e959-323">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="4e959-323">Default cost center</span></span></td>
<td><span data-ttu-id="4e959-324">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-324">10001</span></span></td>
<td><span data-ttu-id="4e959-325">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-325">Electricity</span></span></td>
<td><span data-ttu-id="4e959-326">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-326">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-327">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="4e959-327">-1,000.00</span></span></td>
<td><span data-ttu-id="4e959-328">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-329">CC001</span><span class="sxs-lookup"><span data-stu-id="4e959-329">CC001</span></span></td>
<td><span data-ttu-id="4e959-330">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="4e959-330">HR</span></span></td>
<td><span data-ttu-id="4e959-331">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-331">10001</span></span></td>
<td><span data-ttu-id="4e959-332">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-332">Electricity</span></span></td>
<td><span data-ttu-id="4e959-333">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-333">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-334">500,00</span><span class="sxs-lookup"><span data-stu-id="4e959-334">500.00</span></span></td>
<td><span data-ttu-id="4e959-335">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-336">CC002</span><span class="sxs-lookup"><span data-stu-id="4e959-336">CC002</span></span></td>
<td><span data-ttu-id="4e959-337">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="4e959-337">Finance</span></span></td>
<td><span data-ttu-id="4e959-338">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-338">10001</span></span></td>
<td><span data-ttu-id="4e959-339">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-339">Electricity</span></span></td>
<td><span data-ttu-id="4e959-340">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-340">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-341">500,00</span><span class="sxs-lookup"><span data-stu-id="4e959-341">500.00</span></span></td>
<td><span data-ttu-id="4e959-342">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-343">CC099</span><span class="sxs-lookup"><span data-stu-id="4e959-343">CC099</span></span></td>
<td><span data-ttu-id="4e959-344">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="4e959-344">Default cost center</span></span></td>
<td><span data-ttu-id="4e959-345">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-345">10001</span></span></td>
<td><span data-ttu-id="4e959-346">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-346">Electricity</span></span></td>
<td><span data-ttu-id="4e959-347">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-347">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-348">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="4e959-348">-9,000.00</span></span></td>
<td><span data-ttu-id="4e959-349">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-350">CC001</span><span class="sxs-lookup"><span data-stu-id="4e959-350">CC001</span></span></td>
<td><span data-ttu-id="4e959-351">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="4e959-351">HR</span></span></td>
<td><span data-ttu-id="4e959-352">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-352">10001</span></span></td>
<td><span data-ttu-id="4e959-353">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-353">Electricity</span></span></td>
<td><span data-ttu-id="4e959-354">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-354">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4e959-355">1,285.71</span></span></td>
<td><span data-ttu-id="4e959-356">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-357">CC002</span><span class="sxs-lookup"><span data-stu-id="4e959-357">CC002</span></span></td>
<td><span data-ttu-id="4e959-358">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="4e959-358">Finance</span></span></td>
<td><span data-ttu-id="4e959-359">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-359">10001</span></span></td>
<td><span data-ttu-id="4e959-360">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-360">Electricity</span></span></td>
<td><span data-ttu-id="4e959-361">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-361">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4e959-362">7,714.29</span></span></td>
<td><span data-ttu-id="4e959-363">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e959-364">Lisätietoja kustannusten jaosta ja kohdistusperusteita löydät kohdasta Kustannusten jakokäytännöt ja kohdistusperusteet.</span><span class="sxs-lookup"><span data-stu-id="4e959-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="4e959-365">(Huomaa, että ohjeaihe ei ole vielä valmis; se on saatavilla pian.)</span><span class="sxs-lookup"><span data-stu-id="4e959-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="4e959-366">Vaihe 3: Käsittele yleiskustannustason laskenta</span><span class="sxs-lookup"><span data-stu-id="4e959-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="4e959-367">Yleiskustannustasolla veloitetaan yksi tai useampi määrätty kustannusobjekti.</span><span class="sxs-lookup"><span data-stu-id="4e959-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="4e959-368">Veloitus perustuu ennalta määrättyyn kustannustasoon sekä määritetyn kohdistusperusteen suuruuteen.</span><span class="sxs-lookup"><span data-stu-id="4e959-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="4e959-369">Määritä yleiskustannustaso.</span><span class="sxs-lookup"><span data-stu-id="4e959-369">Define the overhead rate</span></span>

<span data-ttu-id="4e959-370">Kustannusobjekti CC001 HR vaikuttaa joukkoon sisäisiä projekteja.</span><span class="sxs-lookup"><span data-stu-id="4e959-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="4e959-371">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon projektit.</span><span class="sxs-lookup"><span data-stu-id="4e959-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e959-372">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-372">Cost object</span></span></th>
<th><span data-ttu-id="4e959-373">Tunnit</span><span class="sxs-lookup"><span data-stu-id="4e959-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-374">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4e959-374">Proj 1</span></span></td>
<td><span data-ttu-id="4e959-375">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="4e959-375">Project 1</span></span></td>
<td><span data-ttu-id="4e959-376">3</span><span class="sxs-lookup"><span data-stu-id="4e959-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-377">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4e959-377">Proj 2</span></span></td>
<td><span data-ttu-id="4e959-378">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="4e959-378">Project 2</span></span></td>
<td><span data-ttu-id="4e959-379">1</span><span class="sxs-lookup"><span data-stu-id="4e959-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e959-380">Kustannusprojektien osuudelle on määritetty ennalta kustannushinta.</span><span class="sxs-lookup"><span data-stu-id="4e959-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e959-381">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-381">Cost object</span></span></th>
<th><span data-ttu-id="4e959-382">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="4e959-382">Cost element</span></span></th>
<th><span data-ttu-id="4e959-383">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="4e959-383">Cost behavior</span></span></th>
<th><span data-ttu-id="4e959-384">Yksiköt</span><span class="sxs-lookup"><span data-stu-id="4e959-384">Units</span></span></th>
<th><span data-ttu-id="4e959-385">Osuus</span><span class="sxs-lookup"><span data-stu-id="4e959-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-386">CC001</span><span class="sxs-lookup"><span data-stu-id="4e959-386">CC001</span></span></td>
<td><span data-ttu-id="4e959-387">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="4e959-387">HR</span></span></td>
<td><span data-ttu-id="4e959-388">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-388">10001</span></span></td>
<td><span data-ttu-id="4e959-389">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-389">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-390">1</span><span class="sxs-lookup"><span data-stu-id="4e959-390">1</span></span></td>
<td><span data-ttu-id="4e959-391">10</span><span class="sxs-lookup"><span data-stu-id="4e959-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e959-392">Seuraavassa taulukossa on esitetty tulos, kun Henkilöstöhallinnon projekteja käytetään kohdistusperusteena.</span><span class="sxs-lookup"><span data-stu-id="4e959-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e959-393">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-393">Cost object</span></span></th>
<th><span data-ttu-id="4e959-394">Suuruus</span><span class="sxs-lookup"><span data-stu-id="4e959-394">Magnitude</span></span></th>
<th><span data-ttu-id="4e959-395">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="4e959-395">Cost element</span></span></th>
<th><span data-ttu-id="4e959-396">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="4e959-396">Allocation factor</span></span></th>
<th><span data-ttu-id="4e959-397">Summa</span><span class="sxs-lookup"><span data-stu-id="4e959-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-398">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4e959-398">Proj 1</span></span></td>
<td><span data-ttu-id="4e959-399">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="4e959-399">Project 1</span></span></td>
<td><span data-ttu-id="4e959-400">3</span><span class="sxs-lookup"><span data-stu-id="4e959-400">3</span></span></td>
<td><span data-ttu-id="4e959-401">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-401">10001</span></span></td>
<td><span data-ttu-id="4e959-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="4e959-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4e959-403">30,00</span><span class="sxs-lookup"><span data-stu-id="4e959-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-404">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4e959-404">Proj 2</span></span></td>
<td><span data-ttu-id="4e959-405">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="4e959-405">Project 2</span></span></td>
<td><span data-ttu-id="4e959-406">1</span><span class="sxs-lookup"><span data-stu-id="4e959-406">1</span></span></td>
<td><span data-ttu-id="4e959-407">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-407">10001</span></span></td>
<td><span data-ttu-id="4e959-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="4e959-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4e959-409">10,00</span><span class="sxs-lookup"><span data-stu-id="4e959-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4e959-410">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="4e959-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e959-411">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="4e959-411">Journal</span></span></th>
<th><span data-ttu-id="4e959-412">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="4e959-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4e959-413">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="4e959-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4e959-414">Versio</span><span class="sxs-lookup"><span data-stu-id="4e959-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-415">00003</span><span class="sxs-lookup"><span data-stu-id="4e959-415">00003</span></span></td>
<td><span data-ttu-id="4e959-416">Yleiskustannustason laskelman kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="4e959-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="4e959-417">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="4e959-417">Fiscal</span></span></td>
<td><span data-ttu-id="4e959-418">2017</span><span class="sxs-lookup"><span data-stu-id="4e959-418">2017</span></span></td>
<td><span data-ttu-id="4e959-419">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="4e959-419">Period 1</span></span></td>
<td><span data-ttu-id="4e959-420">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="4e959-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="4e959-421">Kirjauskansioviennit (Yleiskustannustason laskennan kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="4e959-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e959-422">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="4e959-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4e959-423">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-423">Cost object</span></span></th>
<th><span data-ttu-id="4e959-424">Suuruus</span><span class="sxs-lookup"><span data-stu-id="4e959-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-425">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e959-426">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4e959-426">Proj 1</span></span></td>
<td><span data-ttu-id="4e959-427">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="4e959-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4e959-428">3,00</span><span class="sxs-lookup"><span data-stu-id="4e959-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-429">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e959-430">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4e959-430">Proj 2</span></span></td>
<td><span data-ttu-id="4e959-431">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="4e959-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4e959-432">1,00</span><span class="sxs-lookup"><span data-stu-id="4e959-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4e959-433">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="4e959-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e959-434">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4e959-435">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="4e959-435">Cost element</span></span></th>
<th><span data-ttu-id="4e959-436">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="4e959-436">Cost behavior</span></span></th>
<th><span data-ttu-id="4e959-437">Summa</span><span class="sxs-lookup"><span data-stu-id="4e959-437">Amount</span></span></th>
<th><span data-ttu-id="4e959-438">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="4e959-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="4e959-439">CC0001</span></span></td>
<td><span data-ttu-id="4e959-440">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="4e959-440">HR</span></span></td>
<td><span data-ttu-id="4e959-441">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-441">10001</span></span></td>
<td><span data-ttu-id="4e959-442">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-442">Electricity</span></span></td>
<td><span data-ttu-id="4e959-443">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-443">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="4e959-444">-30.00</span></span></td>
<td><span data-ttu-id="4e959-445">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-446">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4e959-446">Proj 1</span></span></td>
<td><span data-ttu-id="4e959-447">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="4e959-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4e959-448">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-448">10001</span></span></td>
<td><span data-ttu-id="4e959-449">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-449">Electricity</span></span></td>
<td><span data-ttu-id="4e959-450">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-450">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-451">30,00</span><span class="sxs-lookup"><span data-stu-id="4e959-451">30.00</span></span></td>
<td><span data-ttu-id="4e959-452">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-453">CC001</span><span class="sxs-lookup"><span data-stu-id="4e959-453">CC001</span></span></td>
<td><span data-ttu-id="4e959-454">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="4e959-454">HR</span></span></td>
<td><span data-ttu-id="4e959-455">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-455">10001</span></span></td>
<td><span data-ttu-id="4e959-456">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-456">Electricity</span></span></td>
<td><span data-ttu-id="4e959-457">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-457">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="4e959-458">-10.00</span></span></td>
<td><span data-ttu-id="4e959-459">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-460">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4e959-460">Proj 2</span></span></td>
<td><span data-ttu-id="4e959-461">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="4e959-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4e959-462">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-462">10001</span></span></td>
<td><span data-ttu-id="4e959-463">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-463">Electricity</span></span></td>
<td><span data-ttu-id="4e959-464">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-464">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-465">10,00</span><span class="sxs-lookup"><span data-stu-id="4e959-465">10.00</span></span></td>
<td><span data-ttu-id="4e959-466">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e959-467">Lisätietoja yleiskustannustason käytännöistä löydät kohdista Yleiskustannusten käytännöt ja Kohdistusperusteet.</span><span class="sxs-lookup"><span data-stu-id="4e959-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="4e959-468">(Huomaa, että ohjeaihe ei ole vielä valmis; se on saatavilla pian.)</span><span class="sxs-lookup"><span data-stu-id="4e959-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="4e959-469">Vaihe 4: Käsittele kustannusten kohdistuksen laskenta</span><span class="sxs-lookup"><span data-stu-id="4e959-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="4e959-470">Kohdistuksella kustannusobjektin saldo liitetään toisiin kustannusobjekteihin käyttämällä kohdistusperustetta.</span><span class="sxs-lookup"><span data-stu-id="4e959-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="4e959-471">Finance and Operations tukee vastavuoroista kohdistusmenetelmää.</span><span class="sxs-lookup"><span data-stu-id="4e959-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="4e959-472">Vastavuoroisessa kohdistusmenetelmässä tunnistetaan oheiskustannusobjektien käyttämät, keskinäiset palvelut täysin.</span><span class="sxs-lookup"><span data-stu-id="4e959-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="4e959-473">Järjestelmä määrittää oikean kohdistusjärjestyksen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="4e959-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="4e959-474">Kustannusobjektin saldo kohdistetaan yhdellä kohdistusperusteella.</span><span class="sxs-lookup"><span data-stu-id="4e959-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="4e959-475">Kustannusobjektien dimensiot ja niiden vastaavat jäsenet ylittävät kohdistukset ovat tuettuja.</span><span class="sxs-lookup"><span data-stu-id="4e959-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="4e959-476">Kustannusseurantayksikkö hallitsee kohdistusjärjestystä.</span><span class="sxs-lookup"><span data-stu-id="4e959-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="4e959-477">[![Vastavuoroinen menetelmä](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="4e959-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="4e959-478">Määritä kustannuksen kohdistus</span><span class="sxs-lookup"><span data-stu-id="4e959-478">Define the cost allocation</span></span>

<span data-ttu-id="4e959-479">Tämä on yksinkertainen esimerkki, jossa kerrotaan, miten voit jäljittää kustannuksen virran.</span><span class="sxs-lookup"><span data-stu-id="4e959-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="4e959-480">Kustannusobjekti CC001 HR liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="4e959-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="4e959-481">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="4e959-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e959-482">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-482">Cost object</span></span></th>
<th><span data-ttu-id="4e959-483">HR-palvelut</span><span class="sxs-lookup"><span data-stu-id="4e959-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-484">CC002</span><span class="sxs-lookup"><span data-stu-id="4e959-484">CC002</span></span></td>
<td><span data-ttu-id="4e959-485">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="4e959-485">Finance</span></span></td>
<td><span data-ttu-id="4e959-486">35</span><span class="sxs-lookup"><span data-stu-id="4e959-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-487">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-487">CC003</span></span></td>
<td><span data-ttu-id="4e959-488">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="4e959-488">Assembly</span></span></td>
<td><span data-ttu-id="4e959-489">55</span><span class="sxs-lookup"><span data-stu-id="4e959-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-490">CC004</span><span class="sxs-lookup"><span data-stu-id="4e959-490">CC004</span></span></td>
<td><span data-ttu-id="4e959-491">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="4e959-491">Packaging</span></span></td>
<td><span data-ttu-id="4e959-492">10</span><span class="sxs-lookup"><span data-stu-id="4e959-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e959-493">Kustannusobjekti CC002 Taloushallinto liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="4e959-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="4e959-494">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Taloushallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="4e959-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e959-495">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-495">Cost object</span></span></th>
<th><span data-ttu-id="4e959-496">Taloushallinnon palvelut</span><span class="sxs-lookup"><span data-stu-id="4e959-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-497">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-497">CC003</span></span></td>
<td><span data-ttu-id="4e959-498">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="4e959-498">Assembly</span></span></td>
<td><span data-ttu-id="4e959-499">65</span><span class="sxs-lookup"><span data-stu-id="4e959-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-500">CC004</span><span class="sxs-lookup"><span data-stu-id="4e959-500">CC004</span></span></td>
<td><span data-ttu-id="4e959-501">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="4e959-501">Packaging</span></span></td>
<td><span data-ttu-id="4e959-502">35</span><span class="sxs-lookup"><span data-stu-id="4e959-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e959-503">Kustannusobjekti CC003 Kokoonpano liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="4e959-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="4e959-504">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Kokoonpanopalvelut.</span><span class="sxs-lookup"><span data-stu-id="4e959-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e959-505">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-505">Cost object</span></span></th>
<th><span data-ttu-id="4e959-506">Kokoonpanopalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="4e959-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-507">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-507">Prod 1</span></span></td>
<td><span data-ttu-id="4e959-508">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-508">Product 1</span></span></td>
<td><span data-ttu-id="4e959-509">60</span><span class="sxs-lookup"><span data-stu-id="4e959-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-510">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-510">Prod 2</span></span></td>
<td><span data-ttu-id="4e959-511">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-511">Product 2</span></span></td>
<td><span data-ttu-id="4e959-512">20</span><span class="sxs-lookup"><span data-stu-id="4e959-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e959-513">Kustannusobjekti CC004 Pakkaus liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="4e959-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="4e959-514">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Pakkauspalvelut.</span><span class="sxs-lookup"><span data-stu-id="4e959-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e959-515">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-515">Cost object</span></span></th>
<th><span data-ttu-id="4e959-516">Pakkauspalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="4e959-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-517">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-517">Prod 1</span></span></td>
<td><span data-ttu-id="4e959-518">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-518">Product 1</span></span></td>
<td><span data-ttu-id="4e959-519">80</span><span class="sxs-lookup"><span data-stu-id="4e959-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-520">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-520">Prod 2</span></span></td>
<td><span data-ttu-id="4e959-521">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-521">Product 2</span></span></td>
<td><span data-ttu-id="4e959-522">päivänä</span><span class="sxs-lookup"><span data-stu-id="4e959-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e959-523">**Huomautus:** Finance and Operationsissa tilastomittaukset, kuten tuotteen kuluttamat tuotantotunnit, voidaan johtaa lähdetiedoista.</span><span class="sxs-lookup"><span data-stu-id="4e959-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="4e959-524">Lisätietoja tilastomittausten lähteistä on kohdassa Tilastomittauksen lähdemallit.</span><span class="sxs-lookup"><span data-stu-id="4e959-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="4e959-525">(Huomaa, että ohjeaihe ei ole vielä valmis; se on saatavilla pian.) Seuraavassa taulukossa näytetään tulos, kun HR-palveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteä ja muuttuva kustannus).</span><span class="sxs-lookup"><span data-stu-id="4e959-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e959-526">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-526">Cost object</span></span></th>
<th><span data-ttu-id="4e959-527">Suuruus</span><span class="sxs-lookup"><span data-stu-id="4e959-527">Magnitude</span></span></th>
<th><span data-ttu-id="4e959-528">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="4e959-528">Allocation factor</span></span></th>
<th><span data-ttu-id="4e959-529">Summa</span><span class="sxs-lookup"><span data-stu-id="4e959-529">Amount</span></span></th>
<th><span data-ttu-id="4e959-530">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="4e959-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-531">CC002</span><span class="sxs-lookup"><span data-stu-id="4e959-531">CC002</span></span></td>
<td><span data-ttu-id="4e959-532">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="4e959-532">Finance</span></span></td>
<td><span data-ttu-id="4e959-533">35</span><span class="sxs-lookup"><span data-stu-id="4e959-533">35</span></span></td>
<td><span data-ttu-id="4e959-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4e959-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4e959-535">175.00</span><span class="sxs-lookup"><span data-stu-id="4e959-535">175.00</span></span></td>
<td><span data-ttu-id="4e959-536">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-537">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-537">CC003</span></span></td>
<td><span data-ttu-id="4e959-538">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="4e959-538">Assembly</span></span></td>
<td><span data-ttu-id="4e959-539">55</span><span class="sxs-lookup"><span data-stu-id="4e959-539">55</span></span></td>
<td><span data-ttu-id="4e959-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4e959-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4e959-541">275.00</span><span class="sxs-lookup"><span data-stu-id="4e959-541">275.00</span></span></td>
<td><span data-ttu-id="4e959-542">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-543">CC004</span><span class="sxs-lookup"><span data-stu-id="4e959-543">CC004</span></span></td>
<td><span data-ttu-id="4e959-544">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="4e959-544">Packaging</span></span></td>
<td><span data-ttu-id="4e959-545">10</span><span class="sxs-lookup"><span data-stu-id="4e959-545">10</span></span></td>
<td><span data-ttu-id="4e959-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4e959-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4e959-547">50,00</span><span class="sxs-lookup"><span data-stu-id="4e959-547">50.00</span></span></td>
<td><span data-ttu-id="4e959-548">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-549">CC002</span><span class="sxs-lookup"><span data-stu-id="4e959-549">CC002</span></span></td>
<td><span data-ttu-id="4e959-550">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="4e959-550">Finance</span></span></td>
<td><span data-ttu-id="4e959-551">35</span><span class="sxs-lookup"><span data-stu-id="4e959-551">35</span></span></td>
<td><span data-ttu-id="4e959-552">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="4e959-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4e959-553">436.00</span><span class="sxs-lookup"><span data-stu-id="4e959-553">436.00</span></span></td>
<td><span data-ttu-id="4e959-554">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-555">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-555">CC003</span></span></td>
<td><span data-ttu-id="4e959-556">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="4e959-556">Assembly</span></span></td>
<td><span data-ttu-id="4e959-557">55</span><span class="sxs-lookup"><span data-stu-id="4e959-557">55</span></span></td>
<td><span data-ttu-id="4e959-558">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="4e959-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4e959-559">685.14</span><span class="sxs-lookup"><span data-stu-id="4e959-559">685.14</span></span></td>
<td><span data-ttu-id="4e959-560">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-561">CC004</span><span class="sxs-lookup"><span data-stu-id="4e959-561">CC004</span></span></td>
<td><span data-ttu-id="4e959-562">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="4e959-562">Packaging</span></span></td>
<td><span data-ttu-id="4e959-563">10</span><span class="sxs-lookup"><span data-stu-id="4e959-563">10</span></span></td>
<td><span data-ttu-id="4e959-564">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="4e959-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4e959-565">124.57</span><span class="sxs-lookup"><span data-stu-id="4e959-565">124.57</span></span></td>
<td><span data-ttu-id="4e959-566">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e959-567">Seuraavassa taulukossa näytetään tulos, kun Taloushallinnon palveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="4e959-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e959-568">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-568">Cost object</span></span></th>
<th><span data-ttu-id="4e959-569">Suuruus</span><span class="sxs-lookup"><span data-stu-id="4e959-569">Magnitude</span></span></th>
<th><span data-ttu-id="4e959-570">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="4e959-570">Allocation factor</span></span></th>
<th><span data-ttu-id="4e959-571">Summa</span><span class="sxs-lookup"><span data-stu-id="4e959-571">Amount</span></span></th>
<th><span data-ttu-id="4e959-572">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="4e959-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-573">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-573">CC003</span></span></td>
<td><span data-ttu-id="4e959-574">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="4e959-574">Assembly</span></span></td>
<td><span data-ttu-id="4e959-575">65</span><span class="sxs-lookup"><span data-stu-id="4e959-575">65</span></span></td>
<td><span data-ttu-id="4e959-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="4e959-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4e959-577">438.75</span><span class="sxs-lookup"><span data-stu-id="4e959-577">438.75</span></span></td>
<td><span data-ttu-id="4e959-578">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-579">CC004</span><span class="sxs-lookup"><span data-stu-id="4e959-579">CC004</span></span></td>
<td><span data-ttu-id="4e959-580">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="4e959-580">Packaging</span></span></td>
<td><span data-ttu-id="4e959-581">35</span><span class="sxs-lookup"><span data-stu-id="4e959-581">35</span></span></td>
<td><span data-ttu-id="4e959-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="4e959-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4e959-583">236.25</span><span class="sxs-lookup"><span data-stu-id="4e959-583">236.25</span></span></td>
<td><span data-ttu-id="4e959-584">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-585">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-585">CC003</span></span></td>
<td><span data-ttu-id="4e959-586">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="4e959-586">Assembly</span></span></td>
<td><span data-ttu-id="4e959-587">65</span><span class="sxs-lookup"><span data-stu-id="4e959-587">65</span></span></td>
<td><span data-ttu-id="4e959-588">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="4e959-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4e959-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4e959-589">5,297.69</span></span></td>
<td><span data-ttu-id="4e959-590">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-591">CC004</span><span class="sxs-lookup"><span data-stu-id="4e959-591">CC004</span></span></td>
<td><span data-ttu-id="4e959-592">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="4e959-592">Packaging</span></span></td>
<td><span data-ttu-id="4e959-593">35</span><span class="sxs-lookup"><span data-stu-id="4e959-593">35</span></span></td>
<td><span data-ttu-id="4e959-594">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="4e959-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4e959-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4e959-595">2,852.60</span></span></td>
<td><span data-ttu-id="4e959-596">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e959-597">Seuraavassa taulukossa näytetään tulos, kun Kokoonpanopalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="4e959-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e959-598">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-598">Cost object</span></span></th>
<th><span data-ttu-id="4e959-599">Suuruus</span><span class="sxs-lookup"><span data-stu-id="4e959-599">Magnitude</span></span></th>
<th><span data-ttu-id="4e959-600">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="4e959-600">Allocation factor</span></span></th>
<th><span data-ttu-id="4e959-601">Summa</span><span class="sxs-lookup"><span data-stu-id="4e959-601">Amount</span></span></th>
<th><span data-ttu-id="4e959-602">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="4e959-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-603">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-603">Prod 1</span></span></td>
<td><span data-ttu-id="4e959-604">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-604">Product 1</span></span></td>
<td><span data-ttu-id="4e959-605">60</span><span class="sxs-lookup"><span data-stu-id="4e959-605">60</span></span></td>
<td><span data-ttu-id="4e959-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="4e959-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4e959-607">535.31</span><span class="sxs-lookup"><span data-stu-id="4e959-607">535.31</span></span></td>
<td><span data-ttu-id="4e959-608">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-609">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-609">Prod 2</span></span></td>
<td><span data-ttu-id="4e959-610">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-610">Product 2</span></span></td>
<td><span data-ttu-id="4e959-611">20</span><span class="sxs-lookup"><span data-stu-id="4e959-611">20</span></span></td>
<td><span data-ttu-id="4e959-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="4e959-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4e959-613">178.44</span><span class="sxs-lookup"><span data-stu-id="4e959-613">178.44</span></span></td>
<td><span data-ttu-id="4e959-614">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-615">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-615">Prod 1</span></span></td>
<td><span data-ttu-id="4e959-616">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-616">Product 1</span></span></td>
<td><span data-ttu-id="4e959-617">60</span><span class="sxs-lookup"><span data-stu-id="4e959-617">60</span></span></td>
<td><span data-ttu-id="4e959-618">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="4e959-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4e959-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4e959-619">4,487.12</span></span></td>
<td><span data-ttu-id="4e959-620">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-621">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-621">Prod 2</span></span></td>
<td><span data-ttu-id="4e959-622">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-622">Product 2</span></span></td>
<td><span data-ttu-id="4e959-623">20</span><span class="sxs-lookup"><span data-stu-id="4e959-623">20</span></span></td>
<td><span data-ttu-id="4e959-624">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="4e959-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4e959-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4e959-625">1,495.71</span></span></td>
<td><span data-ttu-id="4e959-626">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e959-627">Seuraavassa taulukossa näytetään tulos, kun Pakkauspalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="4e959-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e959-628">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-628">Cost object</span></span></th>
<th><span data-ttu-id="4e959-629">Suuruus</span><span class="sxs-lookup"><span data-stu-id="4e959-629">Magnitude</span></span></th>
<th><span data-ttu-id="4e959-630">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="4e959-630">Allocation factor</span></span></th>
<th><span data-ttu-id="4e959-631">Summa</span><span class="sxs-lookup"><span data-stu-id="4e959-631">Amount</span></span></th>
<th><span data-ttu-id="4e959-632">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="4e959-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-633">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-633">Prod 1</span></span></td>
<td><span data-ttu-id="4e959-634">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-634">Product 1</span></span></td>
<td><span data-ttu-id="4e959-635">80</span><span class="sxs-lookup"><span data-stu-id="4e959-635">80</span></span></td>
<td><span data-ttu-id="4e959-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="4e959-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4e959-637">241.05</span><span class="sxs-lookup"><span data-stu-id="4e959-637">241.05</span></span></td>
<td><span data-ttu-id="4e959-638">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-639">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-639">Prod 2</span></span></td>
<td><span data-ttu-id="4e959-640">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-640">Product 2</span></span></td>
<td><span data-ttu-id="4e959-641">15</span><span class="sxs-lookup"><span data-stu-id="4e959-641">15</span></span></td>
<td><span data-ttu-id="4e959-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="4e959-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4e959-643">45.20</span><span class="sxs-lookup"><span data-stu-id="4e959-643">45.20</span></span></td>
<td><span data-ttu-id="4e959-644">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-645">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-645">Prod 1</span></span></td>
<td><span data-ttu-id="4e959-646">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-646">Product 1</span></span></td>
<td><span data-ttu-id="4e959-647">80</span><span class="sxs-lookup"><span data-stu-id="4e959-647">80</span></span></td>
<td><span data-ttu-id="4e959-648">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="4e959-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4e959-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4e959-649">2,507.09</span></span></td>
<td><span data-ttu-id="4e959-650">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-651">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-651">Prod 2</span></span></td>
<td><span data-ttu-id="4e959-652">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-652">Product 2</span></span></td>
<td><span data-ttu-id="4e959-653">15</span><span class="sxs-lookup"><span data-stu-id="4e959-653">15</span></span></td>
<td><span data-ttu-id="4e959-654">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="4e959-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4e959-655">470.08</span><span class="sxs-lookup"><span data-stu-id="4e959-655">470.08</span></span></td>
<td><span data-ttu-id="4e959-656">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4e959-657">Kirjauskansioviennit (kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="4e959-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e959-658">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="4e959-658">Journal</span></span></th>
<th><span data-ttu-id="4e959-659">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="4e959-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4e959-660">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="4e959-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4e959-661">Versio</span><span class="sxs-lookup"><span data-stu-id="4e959-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-662">00004</span><span class="sxs-lookup"><span data-stu-id="4e959-662">00004</span></span></td>
<td><span data-ttu-id="4e959-663">Kustannusten kohdistuskirjauskansio</span><span class="sxs-lookup"><span data-stu-id="4e959-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="4e959-664">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="4e959-664">Fiscal</span></span></td>
<td><span data-ttu-id="4e959-665">2017</span><span class="sxs-lookup"><span data-stu-id="4e959-665">2017</span></span></td>
<td><span data-ttu-id="4e959-666">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="4e959-666">Period 1</span></span></td>
<td><span data-ttu-id="4e959-667">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="4e959-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="4e959-668">Kirjauskansion rivit</span><span class="sxs-lookup"><span data-stu-id="4e959-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e959-669">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="4e959-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4e959-670">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4e959-671">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="4e959-671">Cost element</span></span></th>
<th><span data-ttu-id="4e959-672">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="4e959-672">Cost behavior</span></span></th>
<th><span data-ttu-id="4e959-673">Summa</span><span class="sxs-lookup"><span data-stu-id="4e959-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-674">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e959-675">CC001</span><span class="sxs-lookup"><span data-stu-id="4e959-675">CC001</span></span></td>
<td><span data-ttu-id="4e959-676">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="4e959-676">HR</span></span></td>
<td><span data-ttu-id="4e959-677">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-677">10001</span></span></td>
<td><span data-ttu-id="4e959-678">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-678">Electricity</span></span></td>
<td><span data-ttu-id="4e959-679">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-679">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-680">500,00</span><span class="sxs-lookup"><span data-stu-id="4e959-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-681">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e959-682">CC001</span><span class="sxs-lookup"><span data-stu-id="4e959-682">CC001</span></span></td>
<td><span data-ttu-id="4e959-683">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="4e959-683">HR</span></span></td>
<td><span data-ttu-id="4e959-684">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-684">10001</span></span></td>
<td><span data-ttu-id="4e959-685">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-685">Electricity</span></span></td>
<td><span data-ttu-id="4e959-686">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-686">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="4e959-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-688">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e959-689">CC002</span><span class="sxs-lookup"><span data-stu-id="4e959-689">CC002</span></span></td>
<td><span data-ttu-id="4e959-690">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="4e959-690">Finance</span></span></td>
<td><span data-ttu-id="4e959-691">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-691">10001</span></span></td>
<td><span data-ttu-id="4e959-692">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-692">Electricity</span></span></td>
<td><span data-ttu-id="4e959-693">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-693">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-694">675.00</span><span class="sxs-lookup"><span data-stu-id="4e959-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-695">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e959-696">CC002</span><span class="sxs-lookup"><span data-stu-id="4e959-696">CC002</span></span></td>
<td><span data-ttu-id="4e959-697">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="4e959-697">Finance</span></span></td>
<td><span data-ttu-id="4e959-698">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-698">10001</span></span></td>
<td><span data-ttu-id="4e959-699">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-699">Electricity</span></span></td>
<td><span data-ttu-id="4e959-700">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-700">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="4e959-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-702">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e959-703">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-703">CC003</span></span></td>
<td><span data-ttu-id="4e959-704">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="4e959-704">Assembly</span></span></td>
<td><span data-ttu-id="4e959-705">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-705">10001</span></span></td>
<td><span data-ttu-id="4e959-706">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-706">Electricity</span></span></td>
<td><span data-ttu-id="4e959-707">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-707">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-708">713.75</span><span class="sxs-lookup"><span data-stu-id="4e959-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-709">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e959-710">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-710">CC003</span></span></td>
<td><span data-ttu-id="4e959-711">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="4e959-711">Assembly</span></span></td>
<td><span data-ttu-id="4e959-712">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-712">10001</span></span></td>
<td><span data-ttu-id="4e959-713">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-713">Electricity</span></span></td>
<td><span data-ttu-id="4e959-714">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-714">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="4e959-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-716">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e959-717">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-717">CC003</span></span></td>
<td><span data-ttu-id="4e959-718">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="4e959-718">Packaging</span></span></td>
<td><span data-ttu-id="4e959-719">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-719">10001</span></span></td>
<td><span data-ttu-id="4e959-720">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-720">Electricity</span></span></td>
<td><span data-ttu-id="4e959-721">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-721">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-722">286.25</span><span class="sxs-lookup"><span data-stu-id="4e959-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-723">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e959-724">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-724">CC003</span></span></td>
<td><span data-ttu-id="4e959-725">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="4e959-725">Packaging</span></span></td>
<td><span data-ttu-id="4e959-726">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-726">10001</span></span></td>
<td><span data-ttu-id="4e959-727">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-727">Electricity</span></span></td>
<td><span data-ttu-id="4e959-728">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-728">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="4e959-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-730">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e959-731">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-731">Prod 1</span></span></td>
<td><span data-ttu-id="4e959-732">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-732">Product 1</span></span></td>
<td><span data-ttu-id="4e959-733">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-733">10001</span></span></td>
<td><span data-ttu-id="4e959-734">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-734">Electricity</span></span></td>
<td><span data-ttu-id="4e959-735">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-735">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-736">776.36</span><span class="sxs-lookup"><span data-stu-id="4e959-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-737">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e959-738">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-738">Prod 1</span></span></td>
<td><span data-ttu-id="4e959-739">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-739">Product 1</span></span></td>
<td><span data-ttu-id="4e959-740">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-740">10001</span></span></td>
<td><span data-ttu-id="4e959-741">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-741">Electricity</span></span></td>
<td><span data-ttu-id="4e959-742">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-742">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4e959-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-744">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e959-745">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-745">Prod 2</span></span></td>
<td><span data-ttu-id="4e959-746">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-746">Product 1</span></span></td>
<td><span data-ttu-id="4e959-747">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-747">10001</span></span></td>
<td><span data-ttu-id="4e959-748">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-748">Electricity</span></span></td>
<td><span data-ttu-id="4e959-749">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-749">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-750">223.64</span><span class="sxs-lookup"><span data-stu-id="4e959-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-751">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e959-752">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-752">Prod 2</span></span></td>
<td><span data-ttu-id="4e959-753">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-753">Product 1</span></span></td>
<td><span data-ttu-id="4e959-754">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-754">10001</span></span></td>
<td><span data-ttu-id="4e959-755">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-755">Electricity</span></span></td>
<td><span data-ttu-id="4e959-756">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-756">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4e959-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4e959-758">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="4e959-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e959-759">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4e959-760">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="4e959-760">Cost element</span></span></th>
<th><span data-ttu-id="4e959-761">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="4e959-761">Cost behavior</span></span></th>
<th><span data-ttu-id="4e959-762">Summa</span><span class="sxs-lookup"><span data-stu-id="4e959-762">Amount</span></span></th>
<th><span data-ttu-id="4e959-763">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="4e959-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e959-764">CC001</span><span class="sxs-lookup"><span data-stu-id="4e959-764">CC001</span></span></td>
<td><span data-ttu-id="4e959-765">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="4e959-765">HR</span></span></td>
<td><span data-ttu-id="4e959-766">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-766">10001</span></span></td>
<td><span data-ttu-id="4e959-767">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-767">Electricity</span></span></td>
<td><span data-ttu-id="4e959-768">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-768">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="4e959-769">-500.00</span></span></td>
<td><span data-ttu-id="4e959-770">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-771">CC002</span><span class="sxs-lookup"><span data-stu-id="4e959-771">CC002</span></span></td>
<td><span data-ttu-id="4e959-772">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="4e959-772">Finance</span></span></td>
<td><span data-ttu-id="4e959-773">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-773">10001</span></span></td>
<td><span data-ttu-id="4e959-774">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-774">Electricity</span></span></td>
<td><span data-ttu-id="4e959-775">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-775">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-776">175.00</span><span class="sxs-lookup"><span data-stu-id="4e959-776">175.00</span></span></td>
<td><span data-ttu-id="4e959-777">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-778">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-778">CC003</span></span></td>
<td><span data-ttu-id="4e959-779">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="4e959-779">Assembly</span></span></td>
<td><span data-ttu-id="4e959-780">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-780">10001</span></span></td>
<td><span data-ttu-id="4e959-781">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-781">Electricity</span></span></td>
<td><span data-ttu-id="4e959-782">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-782">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-783">275.00</span><span class="sxs-lookup"><span data-stu-id="4e959-783">275.00</span></span></td>
<td><span data-ttu-id="4e959-784">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-785">CC004</span><span class="sxs-lookup"><span data-stu-id="4e959-785">CC004</span></span></td>
<td><span data-ttu-id="4e959-786">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="4e959-786">Packaging</span></span></td>
<td><span data-ttu-id="4e959-787">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-787">10001</span></span></td>
<td><span data-ttu-id="4e959-788">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-788">Electricity</span></span></td>
<td><span data-ttu-id="4e959-789">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-789">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-790">50,00</span><span class="sxs-lookup"><span data-stu-id="4e959-790">50,00</span></span></td>
<td><span data-ttu-id="4e959-791">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-792">CC001</span><span class="sxs-lookup"><span data-stu-id="4e959-792">CC001</span></span></td>
<td><span data-ttu-id="4e959-793">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="4e959-793">HR</span></span></td>
<td><span data-ttu-id="4e959-794">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-794">10001</span></span></td>
<td><span data-ttu-id="4e959-795">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-795">Electricity</span></span></td>
<td><span data-ttu-id="4e959-796">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-796">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-797">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="4e959-797">-1,245.71</span></span></td>
<td><span data-ttu-id="4e959-798">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-799">CC002</span><span class="sxs-lookup"><span data-stu-id="4e959-799">CC002</span></span></td>
<td><span data-ttu-id="4e959-800">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="4e959-800">Finance</span></span></td>
<td><span data-ttu-id="4e959-801">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-801">10001</span></span></td>
<td><span data-ttu-id="4e959-802">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-802">Electricity</span></span></td>
<td><span data-ttu-id="4e959-803">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-803">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-804">436.00</span><span class="sxs-lookup"><span data-stu-id="4e959-804">436.00</span></span></td>
<td><span data-ttu-id="4e959-805">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-806">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-806">CC003</span></span></td>
<td><span data-ttu-id="4e959-807">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="4e959-807">Assembly</span></span></td>
<td><span data-ttu-id="4e959-808">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-808">10001</span></span></td>
<td><span data-ttu-id="4e959-809">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-809">Electricity</span></span></td>
<td><span data-ttu-id="4e959-810">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-810">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-811">685.14</span><span class="sxs-lookup"><span data-stu-id="4e959-811">685.14</span></span></td>
<td><span data-ttu-id="4e959-812">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-813">CC004</span><span class="sxs-lookup"><span data-stu-id="4e959-813">CC004</span></span></td>
<td><span data-ttu-id="4e959-814">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="4e959-814">Packaging</span></span></td>
<td><span data-ttu-id="4e959-815">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-815">10001</span></span></td>
<td><span data-ttu-id="4e959-816">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-816">Electricity</span></span></td>
<td><span data-ttu-id="4e959-817">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-817">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-818">124.57</span><span class="sxs-lookup"><span data-stu-id="4e959-818">124.57</span></span></td>
<td><span data-ttu-id="4e959-819">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-820">CC002</span><span class="sxs-lookup"><span data-stu-id="4e959-820">CC002</span></span></td>
<td><span data-ttu-id="4e959-821">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="4e959-821">Finance</span></span></td>
<td><span data-ttu-id="4e959-822">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-822">10001</span></span></td>
<td><span data-ttu-id="4e959-823">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-823">Electricity</span></span></td>
<td><span data-ttu-id="4e959-824">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-824">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="4e959-825">-675.00</span></span></td>
<td><span data-ttu-id="4e959-826">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-827">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-827">CC003</span></span></td>
<td><span data-ttu-id="4e959-828">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="4e959-828">Assembly</span></span></td>
<td><span data-ttu-id="4e959-829">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-829">10001</span></span></td>
<td><span data-ttu-id="4e959-830">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-830">Electricity</span></span></td>
<td><span data-ttu-id="4e959-831">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-831">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-832">438.75</span><span class="sxs-lookup"><span data-stu-id="4e959-832">438.75</span></span></td>
<td><span data-ttu-id="4e959-833">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-834">CC004</span><span class="sxs-lookup"><span data-stu-id="4e959-834">CC004</span></span></td>
<td><span data-ttu-id="4e959-835">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="4e959-835">Packaging</span></span></td>
<td><span data-ttu-id="4e959-836">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-836">10001</span></span></td>
<td><span data-ttu-id="4e959-837">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-837">Electricity</span></span></td>
<td><span data-ttu-id="4e959-838">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-838">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-839">236.25</span><span class="sxs-lookup"><span data-stu-id="4e959-839">236.25</span></span></td>
<td><span data-ttu-id="4e959-840">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-841">CC002</span><span class="sxs-lookup"><span data-stu-id="4e959-841">CC002</span></span></td>
<td><span data-ttu-id="4e959-842">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="4e959-842">Finance</span></span></td>
<td><span data-ttu-id="4e959-843">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-843">10001</span></span></td>
<td><span data-ttu-id="4e959-844">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-844">Electricity</span></span></td>
<td><span data-ttu-id="4e959-845">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-845">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-846">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="4e959-846">-8,150.29</span></span></td>
<td><span data-ttu-id="4e959-847">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-848">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-848">CC003</span></span></td>
<td><span data-ttu-id="4e959-849">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="4e959-849">Assembly</span></span></td>
<td><span data-ttu-id="4e959-850">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-850">10001</span></span></td>
<td><span data-ttu-id="4e959-851">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-851">Electricity</span></span></td>
<td><span data-ttu-id="4e959-852">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-852">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4e959-853">5,297.69</span></span></td>
<td><span data-ttu-id="4e959-854">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-855">CC004</span><span class="sxs-lookup"><span data-stu-id="4e959-855">CC004</span></span></td>
<td><span data-ttu-id="4e959-856">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="4e959-856">Packaging</span></span></td>
<td><span data-ttu-id="4e959-857">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-857">10001</span></span></td>
<td><span data-ttu-id="4e959-858">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-858">Electricity</span></span></td>
<td><span data-ttu-id="4e959-859">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-859">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4e959-860">2,852.60</span></span></td>
<td><span data-ttu-id="4e959-861">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-862">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-862">CC003</span></span></td>
<td><span data-ttu-id="4e959-863">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="4e959-863">Assembly</span></span></td>
<td><span data-ttu-id="4e959-864">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-864">10001</span></span></td>
<td><span data-ttu-id="4e959-865">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-865">Electricity</span></span></td>
<td><span data-ttu-id="4e959-866">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-866">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-867">-713,75</span><span class="sxs-lookup"><span data-stu-id="4e959-867">-713.75</span></span></td>
<td><span data-ttu-id="4e959-868">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-869">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-869">Prod 1</span></span></td>
<td><span data-ttu-id="4e959-870">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-870">Product 1</span></span></td>
<td><span data-ttu-id="4e959-871">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-871">10001</span></span></td>
<td><span data-ttu-id="4e959-872">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-872">Electricity</span></span></td>
<td><span data-ttu-id="4e959-873">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-873">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-874">535.31</span><span class="sxs-lookup"><span data-stu-id="4e959-874">535.31</span></span></td>
<td><span data-ttu-id="4e959-875">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-876">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-876">Prod 2</span></span></td>
<td><span data-ttu-id="4e959-877">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-877">Product 2</span></span></td>
<td><span data-ttu-id="4e959-878">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-878">10001</span></span></td>
<td><span data-ttu-id="4e959-879">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-879">Electricity</span></span></td>
<td><span data-ttu-id="4e959-880">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-880">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-881">178.44</span><span class="sxs-lookup"><span data-stu-id="4e959-881">178.44</span></span></td>
<td><span data-ttu-id="4e959-882">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-883">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-883">CC003</span></span></td>
<td><span data-ttu-id="4e959-884">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="4e959-884">Assembly</span></span></td>
<td><span data-ttu-id="4e959-885">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-885">10001</span></span></td>
<td><span data-ttu-id="4e959-886">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-886">Electricity</span></span></td>
<td><span data-ttu-id="4e959-887">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-887">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-888">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="4e959-888">-5,982.83</span></span></td>
<td><span data-ttu-id="4e959-889">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-890">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-890">Prod 1</span></span></td>
<td><span data-ttu-id="4e959-891">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-891">Product 1</span></span></td>
<td><span data-ttu-id="4e959-892">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-892">10001</span></span></td>
<td><span data-ttu-id="4e959-893">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-893">Electricity</span></span></td>
<td><span data-ttu-id="4e959-894">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-894">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4e959-895">4,487.12</span></span></td>
<td><span data-ttu-id="4e959-896">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-897">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-897">Prod 2</span></span></td>
<td><span data-ttu-id="4e959-898">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-898">Product 2</span></span></td>
<td><span data-ttu-id="4e959-899">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-899">10001</span></span></td>
<td><span data-ttu-id="4e959-900">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-900">Electricity</span></span></td>
<td><span data-ttu-id="4e959-901">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-901">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4e959-902">1,495.71</span></span></td>
<td><span data-ttu-id="4e959-903">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-904">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-904">CC003</span></span></td>
<td><span data-ttu-id="4e959-905">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="4e959-905">Assembly</span></span></td>
<td><span data-ttu-id="4e959-906">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-906">10001</span></span></td>
<td><span data-ttu-id="4e959-907">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-907">Electricity</span></span></td>
<td><span data-ttu-id="4e959-908">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-908">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="4e959-909">-286.25</span></span></td>
<td><span data-ttu-id="4e959-910">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-911">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-911">Prod 1</span></span></td>
<td><span data-ttu-id="4e959-912">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-912">Product 1</span></span></td>
<td><span data-ttu-id="4e959-913">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-913">10001</span></span></td>
<td><span data-ttu-id="4e959-914">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-914">Electricity</span></span></td>
<td><span data-ttu-id="4e959-915">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-915">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-916">241.05</span><span class="sxs-lookup"><span data-stu-id="4e959-916">241.05</span></span></td>
<td><span data-ttu-id="4e959-917">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-918">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-918">Prod 2</span></span></td>
<td><span data-ttu-id="4e959-919">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-919">Product 2</span></span></td>
<td><span data-ttu-id="4e959-920">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-920">10001</span></span></td>
<td><span data-ttu-id="4e959-921">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-921">Electricity</span></span></td>
<td><span data-ttu-id="4e959-922">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-922">Fixed cost</span></span></td>
<td><span data-ttu-id="4e959-923">45.20</span><span class="sxs-lookup"><span data-stu-id="4e959-923">45.20</span></span></td>
<td><span data-ttu-id="4e959-924">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-925">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-925">CC003</span></span></td>
<td><span data-ttu-id="4e959-926">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="4e959-926">Assembly</span></span></td>
<td><span data-ttu-id="4e959-927">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-927">10001</span></span></td>
<td><span data-ttu-id="4e959-928">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-928">Electricity</span></span></td>
<td><span data-ttu-id="4e959-929">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-929">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-930">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="4e959-930">-2,977.17</span></span></td>
<td><span data-ttu-id="4e959-931">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-932">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-932">Prod 1</span></span></td>
<td><span data-ttu-id="4e959-933">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-933">Product 1</span></span></td>
<td><span data-ttu-id="4e959-934">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-934">10001</span></span></td>
<td><span data-ttu-id="4e959-935">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-935">Electricity</span></span></td>
<td><span data-ttu-id="4e959-936">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-936">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4e959-937">2,507.09</span></span></td>
<td><span data-ttu-id="4e959-938">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e959-939">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-939">Prod 2</span></span></td>
<td><span data-ttu-id="4e959-940">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-940">Product 2</span></span></td>
<td><span data-ttu-id="4e959-941">10 001</span><span class="sxs-lookup"><span data-stu-id="4e959-941">10001</span></span></td>
<td><span data-ttu-id="4e959-942">Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-942">Electricity</span></span></td>
<td><span data-ttu-id="4e959-943">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-943">Variable cost</span></span></td>
<td><span data-ttu-id="4e959-944">470.08</span><span class="sxs-lookup"><span data-stu-id="4e959-944">470.08</span></span></td>
<td><span data-ttu-id="4e959-945">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="4e959-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="4e959-946">Johtopäätökset</span><span class="sxs-lookup"><span data-stu-id="4e959-946">Conclusion</span></span>
<span data-ttu-id="4e959-947">Kirjanpidossa kirjataan tyhjään kustannuspaikkatunnukseen sähkökustannus arvolla 10 000,00.</span><span class="sxs-lookup"><span data-stu-id="4e959-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="4e959-948">Tämän ansiosta kustannuslaskijat tietävät, että kustannus on kohdistettava.</span><span class="sxs-lookup"><span data-stu-id="4e959-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="4e959-949">Kustannukset virtaavat kirjanpidossa organisaation yksiköiden ja tasojen läpi käytössä olevien käytäntöjen ja sääntöjen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="4e959-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="4e959-950">Kukin kustannus on liitetty kustannusperusteeseen, joka sisältää parhaan arvion kustannusten kohdistuksesta.</span><span class="sxs-lookup"><span data-stu-id="4e959-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="4e959-951">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="4e959-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="4e959-952">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="4e959-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="4e959-953">Yhteensä</span><span class="sxs-lookup"><span data-stu-id="4e959-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4e959-954">CC099</span><span class="sxs-lookup"><span data-stu-id="4e959-954">CC099</span></span></th>
<th><span data-ttu-id="4e959-955">CC001</span><span class="sxs-lookup"><span data-stu-id="4e959-955">CC001</span></span></th>
<th><span data-ttu-id="4e959-956">CC002</span><span class="sxs-lookup"><span data-stu-id="4e959-956">CC002</span></span></th>
<th><span data-ttu-id="4e959-957">CC003</span><span class="sxs-lookup"><span data-stu-id="4e959-957">CC003</span></span></th>
<th><span data-ttu-id="4e959-958">CC004</span><span class="sxs-lookup"><span data-stu-id="4e959-958">CC004</span></span></th>
<th><span data-ttu-id="4e959-959">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4e959-959">Proj 1</span></span></th>
<th><span data-ttu-id="4e959-960">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4e959-960">Proj 2</span></span></th>
<th><span data-ttu-id="4e959-961">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="4e959-961">Prod 1</span></span></th>
<th><span data-ttu-id="4e959-962">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="4e959-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="4e959-963">10001 Sähkö</span><span class="sxs-lookup"><span data-stu-id="4e959-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="4e959-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-965"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="4e959-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-966"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="4e959-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-967"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="4e959-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4e959-968"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="4e959-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-969"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="4e959-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-970"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="4e959-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-971"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="4e959-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-972"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="4e959-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="4e959-973">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="4e959-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-974">0,00</span><span class="sxs-lookup"><span data-stu-id="4e959-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="4e959-975">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="4e959-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-976">0,00</span><span class="sxs-lookup"><span data-stu-id="4e959-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-977">0,00</span><span class="sxs-lookup"><span data-stu-id="4e959-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-978">0,00</span><span class="sxs-lookup"><span data-stu-id="4e959-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-979">0,00</span><span class="sxs-lookup"><span data-stu-id="4e959-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-980">0,00</span><span class="sxs-lookup"><span data-stu-id="4e959-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4e959-981">776.36</span><span class="sxs-lookup"><span data-stu-id="4e959-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-982">223.64</span><span class="sxs-lookup"><span data-stu-id="4e959-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-983"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="4e959-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="4e959-984">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="4e959-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-985">000</span><span class="sxs-lookup"><span data-stu-id="4e959-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-986">0,00</span><span class="sxs-lookup"><span data-stu-id="4e959-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-987">0,00</span><span class="sxs-lookup"><span data-stu-id="4e959-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-988">0,00</span><span class="sxs-lookup"><span data-stu-id="4e959-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-989">0,00</span><span class="sxs-lookup"><span data-stu-id="4e959-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-990">30,00</span><span class="sxs-lookup"><span data-stu-id="4e959-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-991">10,00</span><span class="sxs-lookup"><span data-stu-id="4e959-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4e959-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4e959-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e959-994"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="4e959-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="4e959-995">Tässä ohjeaiheessa esitellään, miten ensisijainen kustannuselementti, 10001 Sähkö, virtaa kustannusobjektien läpi.</span><span class="sxs-lookup"><span data-stu-id="4e959-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="4e959-996">Tästä syystä tämä yleiskustannus kohdistetaan organisaation alimmalle tasolle.</span><span class="sxs-lookup"><span data-stu-id="4e959-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="4e959-997">Toisin sanoen alimman tason kustannusobjektit kantavat kustannuksen.</span><span class="sxs-lookup"><span data-stu-id="4e959-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="4e959-998">Jos tarvitset visuaalisen näkymän kustannuksen virrasta kustannusobjektien välillä, voit käyttää kustannuksen koontikäytäntösääntöjä kustannusvirran visualisointiin.</span><span class="sxs-lookup"><span data-stu-id="4e959-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="4e959-999">Lisätietoja on kohdassa Kustannusten koontikäytäntösäännöt.</span><span class="sxs-lookup"><span data-stu-id="4e959-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="4e959-1000">(Huomaa, että ohjeaihe ei ole vielä valmis; se on saatavilla pian.)</span><span class="sxs-lookup"><span data-stu-id="4e959-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




