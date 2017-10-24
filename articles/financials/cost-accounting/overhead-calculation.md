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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0ea6f7428cd5c7618d2d69f1fb66fd9539ad1073
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="99418-103">Yleiskustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="99418-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="99418-104">Tässä aiheessa kuvataan tyypillinen yleiskustannusten laskenta- ja kohdistusprosessi.</span><span class="sxs-lookup"><span data-stu-id="99418-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="99418-105">Sanaston määritelmä</span><span class="sxs-lookup"><span data-stu-id="99418-105">Term definition</span></span>
---------------

<span data-ttu-id="99418-106">Yleiskustannukset ovat yrityksen toiminnasta syntyviä kustannuksia, joita ei voi suoraan liittää mihinkään tiettyyn liiketoiminnan tehtävään, tuotteeseen tai palveluun.</span><span class="sxs-lookup"><span data-stu-id="99418-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="99418-107">Yleiskustannukset ovat tärkeä tuki voittoa tuottavien tehtävien luonnissa.</span><span class="sxs-lookup"><span data-stu-id="99418-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="99418-108">Seuraavassa on joitakin esimerkkejä yleiskustannuksista:</span><span class="sxs-lookup"><span data-stu-id="99418-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="99418-109">Vuokra</span><span class="sxs-lookup"><span data-stu-id="99418-109">Rent</span></span>
-   <span data-ttu-id="99418-110">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-110">Electricity</span></span>
-   <span data-ttu-id="99418-111">Hallinnon palkat</span><span class="sxs-lookup"><span data-stu-id="99418-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="99418-112">Yleiskustannuslaskennan yleiskuva</span><span class="sxs-lookup"><span data-stu-id="99418-112">Overhead calculation overview</span></span>
<span data-ttu-id="99418-113">Yleiskustannusten laskenta suorittaa kustannuslaskennan käytännöt oikeassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="99418-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="99418-114">Yleiskustannusten laskennan voi suorittaa useita kertoja samalle tilikaudelle, jos kustannuslaskennan käytännöt ovat muuttuneet tai erityisiä virheitä on havaittu.</span><span class="sxs-lookup"><span data-stu-id="99418-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="99418-115">Kukin laskenta-ajo tallennetaan ja kullekin annetaan yksilöllinen versiotunnus, jonka avulla eri laskenta-ajoja voi verrata toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="99418-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="99418-116">Yleiskustannusten laskenta luo kustannustapahtumia, joille annetaan kirjauspäivä.</span><span class="sxs-lookup"><span data-stu-id="99418-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="99418-117">Kirjauspäivä vastaa laskennassa käytettyä tilikauden päättymispäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="99418-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="99418-118">Yksilöivä versiotunnus sisältää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="99418-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="99418-119">Versiotyyppi</span><span class="sxs-lookup"><span data-stu-id="99418-119">Version type</span></span>
-   <span data-ttu-id="99418-120">Päivämäärä ja aika</span><span class="sxs-lookup"><span data-stu-id="99418-120">Date and time</span></span>
-   <span data-ttu-id="99418-121">Kustannuslaskennan kirjanpito</span><span class="sxs-lookup"><span data-stu-id="99418-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="99418-122">Tilikausi </span><span class="sxs-lookup"><span data-stu-id="99418-122">Fiscal year</span></span>
-   <span data-ttu-id="99418-123">Tilikausi  </span><span class="sxs-lookup"><span data-stu-id="99418-123">Fiscal period</span></span>

<span data-ttu-id="99418-124">Yleiskustannusten laskenta ajetaan versiosta riippumattomana.</span><span class="sxs-lookup"><span data-stu-id="99418-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="99418-125">Voit siis laskea budjetin version ennen todellista versiota.</span><span class="sxs-lookup"><span data-stu-id="99418-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="99418-126">Yleiskustannusten laskenta koostuu neljästä vaiheesta, jotka esitellään seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="99418-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="99418-127">Kussakin vaiheessa luodaan kirjauskansion otsikko, jolla on kirjauskansiovientejä.</span><span class="sxs-lookup"><span data-stu-id="99418-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="99418-128">Tämä kirjauskansion otsikko säilyttää kunkin laskentavaiheen syöttötiedot.</span><span class="sxs-lookup"><span data-stu-id="99418-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="99418-129">Käytännöt ja säännöt ajetaan kullekin kirjauskansion riville, ja tuloksena luodaan kustannustapahtumia.</span><span class="sxs-lookup"><span data-stu-id="99418-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="99418-130">Tämän ansiosta kaikki laskutoimitukset ovat täysin jäljitettävissä.</span><span class="sxs-lookup"><span data-stu-id="99418-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="99418-131">[![Yleiskustannuslaskenta](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="99418-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="99418-132">Laske ja kohdista sähkön yleiskustannukset</span><span class="sxs-lookup"><span data-stu-id="99418-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="99418-133">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="99418-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="99418-134">Tarkka johdon näkymä ei täten ole saatavilla kustannuslaskennassa.</span><span class="sxs-lookup"><span data-stu-id="99418-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="99418-135">Jotta kustannuslaskenta tarjoaisi oikean johdon näkymän kaikista organisaation yksiköistä ja tasoista, kustannusten on virrattava organisaation yksiköiden läpi.</span><span class="sxs-lookup"><span data-stu-id="99418-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="99418-136">Tämän virran on perustuttava joko tarkkaan tietoon kulutuksesta tai perusteltuun arvioon.</span><span class="sxs-lookup"><span data-stu-id="99418-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="99418-137">Sähkökustannukset voi kirjata kirjanpitoon seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="99418-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="99418-138">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="99418-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="99418-139">Kustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="99418-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="99418-140">Päätili</span><span class="sxs-lookup"><span data-stu-id="99418-140">Main account</span></span></th>
<th><span data-ttu-id="99418-141">Summa kirjanpitovaluuttana</span><span class="sxs-lookup"><span data-stu-id="99418-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-142">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="99418-143">CC099</span><span class="sxs-lookup"><span data-stu-id="99418-143">CC099</span></span></td>
<td><span data-ttu-id="99418-144">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="99418-144">Default cost center</span></span></td>
<td><span data-ttu-id="99418-145">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-145">10001</span></span></td>
<td><span data-ttu-id="99418-146">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-146">Electricity</span></span></td>
<td><span data-ttu-id="99418-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="99418-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="99418-148">Vaihe 1: Käsittele kustannustoiminnan laskenta</span><span class="sxs-lookup"><span data-stu-id="99418-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="99418-149">Kun kustannustapahtumat tuodaan lähdetiedoista, niille asetetaan kustannuslaskennassa oletusarvoisesti **Luokittelematon** -kustannustoimintaluokka.</span><span class="sxs-lookup"><span data-stu-id="99418-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="99418-150">Voit luokitella kustannustapahtumia uudelleen **kiinteäksi kustannukseksi** tai **muuttuvaksi kustannukseksi** kustannustoiminnan käytäntösäännöillä.</span><span class="sxs-lookup"><span data-stu-id="99418-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="99418-151">Määritä kustannustoiminnan sääntö</span><span class="sxs-lookup"><span data-stu-id="99418-151">Define the cost behavior rule</span></span>

<span data-ttu-id="99418-152">Joissain tapauksissa osa kustannuksesta on kiinteä ja loppuosa perustuu kulutukseen.</span><span class="sxs-lookup"><span data-stu-id="99418-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="99418-153">Sähkölaskut sopivat usein tähän määritelmään.</span><span class="sxs-lookup"><span data-stu-id="99418-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="99418-154">Maksat ensin määrätyn, kiinteän maksun, jonka lisäksi maksat kulutuksesta kilowattitunteina (kWh).</span><span class="sxs-lookup"><span data-stu-id="99418-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="99418-155">Jos kiinteä maksu on esimerkiksi 1 000,00, kustannustoiminnan sääntö määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="99418-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="99418-156">Kiinteä määrä 1 000,00</span><span class="sxs-lookup"><span data-stu-id="99418-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="99418-157">0 &lt;= 1 000,00 = Kiinteä</span><span class="sxs-lookup"><span data-stu-id="99418-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="99418-158">1000,01 &lt; N = Muuttuva</span><span class="sxs-lookup"><span data-stu-id="99418-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="99418-159">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="99418-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="99418-160">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="99418-160">Journal</span></span></th>
<th><span data-ttu-id="99418-161">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="99418-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="99418-162">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="99418-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="99418-163">Versio</span><span class="sxs-lookup"><span data-stu-id="99418-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-164">00001</span><span class="sxs-lookup"><span data-stu-id="99418-164">00001</span></span></td>
<td><span data-ttu-id="99418-165">Kustannustoiminnan laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="99418-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="99418-166">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="99418-166">Fiscal</span></span></td>
<td><span data-ttu-id="99418-167">2017</span><span class="sxs-lookup"><span data-stu-id="99418-167">2017</span></span></td>
<td><span data-ttu-id="99418-168">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="99418-168">Period 1</span></span></td>
<td><span data-ttu-id="99418-169">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="99418-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="99418-170">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="99418-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="99418-171">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="99418-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="99418-172">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="99418-173">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="99418-173">Cost element</span></span></th>
<th><span data-ttu-id="99418-174">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="99418-174">Cost behavior</span></span></th>
<th><span data-ttu-id="99418-175">Summa</span><span class="sxs-lookup"><span data-stu-id="99418-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-176">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="99418-177">CC099</span><span class="sxs-lookup"><span data-stu-id="99418-177">CC099</span></span></td>
<td><span data-ttu-id="99418-178">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="99418-178">Default cost center</span></span></td>
<td><span data-ttu-id="99418-179">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-179">10001</span></span></td>
<td><span data-ttu-id="99418-180">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-180">Electricity</span></span></td>
<td><span data-ttu-id="99418-181">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="99418-181">Unclassified</span></span></td>
<td><span data-ttu-id="99418-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="99418-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="99418-183">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="99418-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="99418-184">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="99418-185">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="99418-185">Cost element</span></span></th>
<th><span data-ttu-id="99418-186">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="99418-186">Cost behavior</span></span></th>
<th><span data-ttu-id="99418-187">Summa</span><span class="sxs-lookup"><span data-stu-id="99418-187">Amount</span></span></th>
<th><span data-ttu-id="99418-188">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="99418-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-189">CC099</span><span class="sxs-lookup"><span data-stu-id="99418-189">CC099</span></span></td>
<td><span data-ttu-id="99418-190">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="99418-190">Default cost center</span></span></td>
<td><span data-ttu-id="99418-191">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-191">10001</span></span></td>
<td><span data-ttu-id="99418-192">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-192">Electricity</span></span></td>
<td><span data-ttu-id="99418-193">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="99418-193">Unclassified</span></span></td>
<td><span data-ttu-id="99418-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="99418-194">10,000.00</span></span></td>
<td><span data-ttu-id="99418-195">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-196">CC099</span><span class="sxs-lookup"><span data-stu-id="99418-196">CC099</span></span></td>
<td><span data-ttu-id="99418-197">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="99418-197">Default cost center</span></span></td>
<td><span data-ttu-id="99418-198">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-198">10001</span></span></td>
<td><span data-ttu-id="99418-199">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-199">Electricity</span></span></td>
<td><span data-ttu-id="99418-200">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="99418-200">Unclassified</span></span></td>
<td><span data-ttu-id="99418-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="99418-201">-10,000.00</span></span></td>
<td><span data-ttu-id="99418-202">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-203">CC099</span><span class="sxs-lookup"><span data-stu-id="99418-203">CC099</span></span></td>
<td><span data-ttu-id="99418-204">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="99418-204">Default cost center</span></span></td>
<td><span data-ttu-id="99418-205">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-205">10001</span></span></td>
<td><span data-ttu-id="99418-206">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-206">Electricity</span></span></td>
<td><span data-ttu-id="99418-207">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-207">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="99418-208">1,000.00</span></span></td>
<td><span data-ttu-id="99418-209">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-210">CC099</span><span class="sxs-lookup"><span data-stu-id="99418-210">CC099</span></span></td>
<td><span data-ttu-id="99418-211">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="99418-211">Default cost center</span></span></td>
<td><span data-ttu-id="99418-212">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-212">10001</span></span></td>
<td><span data-ttu-id="99418-213">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-213">Electricity</span></span></td>
<td><span data-ttu-id="99418-214">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-214">Variable cost</span></span></td>
<td><span data-ttu-id="99418-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="99418-215">9,000.00</span></span></td>
<td><span data-ttu-id="99418-216">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="99418-217">Lisätietoja kustannustoiminnasta on kohdassa Kustannustoimintakäytännöt.</span><span class="sxs-lookup"><span data-stu-id="99418-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="99418-218">(Huomaa, että ohjeaihe ei ole vielä valmis; se on saatavilla pian.)</span><span class="sxs-lookup"><span data-stu-id="99418-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="99418-219">Vaihe 2: Käsittele kustannusten jaon laskenta</span><span class="sxs-lookup"><span data-stu-id="99418-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="99418-220">Kustannusten jakoa käytetään kustannusten jakamiseen yhdestä kustannusobjektista toiseen (tai useampaan kustannusobjektiin) määrittämällä asiaankuuluvan kohdistusperusteen.</span><span class="sxs-lookup"><span data-stu-id="99418-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="99418-221">Kustannusten jako ja kustannusten kohdistus eroavat toisistaan sillä, että kustannusten jako tapahtuu aina alkuperäisen kustannuksen ensisijaisen kustannuselementin tasolla.</span><span class="sxs-lookup"><span data-stu-id="99418-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="99418-222">Määritä kustannusten jaon sääntö</span><span class="sxs-lookup"><span data-stu-id="99418-222">Define the cost distribution rule</span></span>

<span data-ttu-id="99418-223">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="99418-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="99418-224">Kustannuslaskenta ei tarjoa tästä tarpeeksi tarkkoja tietoja.</span><span class="sxs-lookup"><span data-stu-id="99418-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="99418-225">Muuttuva kustannus tulisi jakaa yksittäisille kustannusobjekteille reiluin perustein.</span><span class="sxs-lookup"><span data-stu-id="99418-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="99418-226">Loogisin kohdistusperuste on sähkönkulutus (kWh).</span><span class="sxs-lookup"><span data-stu-id="99418-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="99418-227">Luodaan tilastollinen dimensionjäsen nimeltä Sähkö, johon kirjataan sähkönkulutus.</span><span class="sxs-lookup"><span data-stu-id="99418-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="99418-228">Oletusarvon mukaan kaikki tilastolliset dimensiojäsenet ovat käytettävissä kohdistusperusteina.</span><span class="sxs-lookup"><span data-stu-id="99418-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="99418-229">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-229">Cost object</span></span></th>
<th><span data-ttu-id="99418-230">kWh</span><span class="sxs-lookup"><span data-stu-id="99418-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-231">CC001</span><span class="sxs-lookup"><span data-stu-id="99418-231">CC001</span></span></td>
<td><span data-ttu-id="99418-232">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="99418-232">HR</span></span></td>
<td><span data-ttu-id="99418-233">1 000</span><span class="sxs-lookup"><span data-stu-id="99418-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-234">CC002</span><span class="sxs-lookup"><span data-stu-id="99418-234">CC002</span></span></td>
<td><span data-ttu-id="99418-235">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="99418-235">Finance</span></span></td>
<td><span data-ttu-id="99418-236">6,000</span><span class="sxs-lookup"><span data-stu-id="99418-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-237">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-237">CC003</span></span></td>
<td><span data-ttu-id="99418-238">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="99418-238">Assembly</span></span></td>
<td><span data-ttu-id="99418-239">0</span><span class="sxs-lookup"><span data-stu-id="99418-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="99418-240">Seuraavassa taulukossa on esitetty tulos, kun sähkönkulutusta käytetään kohdistusperusteena muuttuville kuluille.</span><span class="sxs-lookup"><span data-stu-id="99418-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="99418-241">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-241">Cost object</span></span></th>
<th><span data-ttu-id="99418-242">Suuruus</span><span class="sxs-lookup"><span data-stu-id="99418-242">Magnitude</span></span></th>
<th><span data-ttu-id="99418-243">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="99418-243">Allocation factor</span></span></th>
<th><span data-ttu-id="99418-244">Summa</span><span class="sxs-lookup"><span data-stu-id="99418-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-245">CC001</span><span class="sxs-lookup"><span data-stu-id="99418-245">CC001</span></span></td>
<td><span data-ttu-id="99418-246">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="99418-246">HR</span></span></td>
<td><span data-ttu-id="99418-247">1 000</span><span class="sxs-lookup"><span data-stu-id="99418-247">1,000</span></span></td>
<td><span data-ttu-id="99418-248">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="99418-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="99418-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="99418-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-250">CC002</span><span class="sxs-lookup"><span data-stu-id="99418-250">CC002</span></span></td>
<td><span data-ttu-id="99418-251">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="99418-251">Finance</span></span></td>
<td><span data-ttu-id="99418-252">6,000</span><span class="sxs-lookup"><span data-stu-id="99418-252">6,000</span></span></td>
<td><span data-ttu-id="99418-253">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="99418-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="99418-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="99418-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-255">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-255">CC003</span></span></td>
<td><span data-ttu-id="99418-256">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="99418-256">Assembly</span></span></td>
<td><span data-ttu-id="99418-257">0</span><span class="sxs-lookup"><span data-stu-id="99418-257">0</span></span></td>
<td><span data-ttu-id="99418-258">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="99418-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="99418-259">0,00</span><span class="sxs-lookup"><span data-stu-id="99418-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="99418-260">Kiinteä kustannus tulisi jakaa tasaisesti yksittäisille kustannusobjekteille, jotka ovat kuluttaneet sähköä.</span><span class="sxs-lookup"><span data-stu-id="99418-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="99418-261">Voit käyttää sähkön tilastollista dimensiojäsentä kaavan kohdistusperusteena tämän tavoitteen saavuttamiseksi: (sähkö &gt;0,00) Seuraavassa taulukossa on esitetty tulos siitä, kun sähkönkulutus on määritetty muuttuvien kustannusten kohdistusperusteeksi.</span><span class="sxs-lookup"><span data-stu-id="99418-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="99418-262">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-262">Cost object</span></span></th>
<th><span data-ttu-id="99418-263">Resepti</span><span class="sxs-lookup"><span data-stu-id="99418-263">Formula</span></span></th>
<th><span data-ttu-id="99418-264">Suuruus</span><span class="sxs-lookup"><span data-stu-id="99418-264">Magnitude</span></span></th>
<th><span data-ttu-id="99418-265">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="99418-265">Allocation factor</span></span></th>
<th><span data-ttu-id="99418-266">Summa</span><span class="sxs-lookup"><span data-stu-id="99418-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-267">CC001</span><span class="sxs-lookup"><span data-stu-id="99418-267">CC001</span></span></td>
<td><span data-ttu-id="99418-268">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="99418-268">HR</span></span></td>
<td><span data-ttu-id="99418-269">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="99418-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="99418-270">1</span><span class="sxs-lookup"><span data-stu-id="99418-270">1</span></span></td>
<td><span data-ttu-id="99418-271">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="99418-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="99418-272">500,00</span><span class="sxs-lookup"><span data-stu-id="99418-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-273">CC002</span><span class="sxs-lookup"><span data-stu-id="99418-273">CC002</span></span></td>
<td><span data-ttu-id="99418-274">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="99418-274">Finance</span></span></td>
<td><span data-ttu-id="99418-275">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="99418-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="99418-276">1</span><span class="sxs-lookup"><span data-stu-id="99418-276">1</span></span></td>
<td><span data-ttu-id="99418-277">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="99418-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="99418-278">500,00</span><span class="sxs-lookup"><span data-stu-id="99418-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-279">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-279">CC003</span></span></td>
<td><span data-ttu-id="99418-280">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="99418-280">Assembly</span></span></td>
<td><span data-ttu-id="99418-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="99418-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="99418-282">0</span><span class="sxs-lookup"><span data-stu-id="99418-282">0</span></span></td>
<td><span data-ttu-id="99418-283">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="99418-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="99418-284">0,00</span><span class="sxs-lookup"><span data-stu-id="99418-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="99418-285">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="99418-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="99418-286">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="99418-286">Journal</span></span></th>
<th><span data-ttu-id="99418-287">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="99418-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="99418-288">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="99418-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="99418-289">Versio</span><span class="sxs-lookup"><span data-stu-id="99418-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-290">00002</span><span class="sxs-lookup"><span data-stu-id="99418-290">00002</span></span></td>
<td><span data-ttu-id="99418-291">Kustannusten jaon laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="99418-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="99418-292">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="99418-292">Fiscal</span></span></td>
<td><span data-ttu-id="99418-293">2017</span><span class="sxs-lookup"><span data-stu-id="99418-293">2017</span></span></td>
<td><span data-ttu-id="99418-294">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="99418-294">Period 1</span></span></td>
<td><span data-ttu-id="99418-295">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="99418-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="99418-296">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="99418-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="99418-297">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="99418-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="99418-298">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="99418-299">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="99418-299">Cost element</span></span></th>
<th><span data-ttu-id="99418-300">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="99418-300">Cost behavior</span></span></th>
<th><span data-ttu-id="99418-301">Summa</span><span class="sxs-lookup"><span data-stu-id="99418-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-302">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="99418-303">CC099</span><span class="sxs-lookup"><span data-stu-id="99418-303">CC099</span></span></td>
<td><span data-ttu-id="99418-304">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="99418-304">Default cost center</span></span></td>
<td><span data-ttu-id="99418-305">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-305">10001</span></span></td>
<td><span data-ttu-id="99418-306">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-306">Electricity</span></span></td>
<td><span data-ttu-id="99418-307">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-307">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-308">1 000,00</span><span class="sxs-lookup"><span data-stu-id="99418-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-309">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="99418-310">CC099</span><span class="sxs-lookup"><span data-stu-id="99418-310">CC099</span></span></td>
<td><span data-ttu-id="99418-311">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="99418-311">Default cost center</span></span></td>
<td><span data-ttu-id="99418-312">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-312">10001</span></span></td>
<td><span data-ttu-id="99418-313">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-313">Electricity</span></span></td>
<td><span data-ttu-id="99418-314">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-314">Variable cost</span></span></td>
<td><span data-ttu-id="99418-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="99418-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="99418-316">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="99418-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="99418-317">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="99418-318">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="99418-318">Cost element</span></span></th>
<th><span data-ttu-id="99418-319">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="99418-319">Cost behavior</span></span></th>
<th><span data-ttu-id="99418-320">Summa</span><span class="sxs-lookup"><span data-stu-id="99418-320">Amount</span></span></th>
<th><span data-ttu-id="99418-321">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="99418-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-322">CC099</span><span class="sxs-lookup"><span data-stu-id="99418-322">CC099</span></span></td>
<td><span data-ttu-id="99418-323">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="99418-323">Default cost center</span></span></td>
<td><span data-ttu-id="99418-324">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-324">10001</span></span></td>
<td><span data-ttu-id="99418-325">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-325">Electricity</span></span></td>
<td><span data-ttu-id="99418-326">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-326">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-327">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="99418-327">-1,000.00</span></span></td>
<td><span data-ttu-id="99418-328">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-329">CC001</span><span class="sxs-lookup"><span data-stu-id="99418-329">CC001</span></span></td>
<td><span data-ttu-id="99418-330">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="99418-330">HR</span></span></td>
<td><span data-ttu-id="99418-331">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-331">10001</span></span></td>
<td><span data-ttu-id="99418-332">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-332">Electricity</span></span></td>
<td><span data-ttu-id="99418-333">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-333">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-334">500,00</span><span class="sxs-lookup"><span data-stu-id="99418-334">500.00</span></span></td>
<td><span data-ttu-id="99418-335">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-336">CC002</span><span class="sxs-lookup"><span data-stu-id="99418-336">CC002</span></span></td>
<td><span data-ttu-id="99418-337">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="99418-337">Finance</span></span></td>
<td><span data-ttu-id="99418-338">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-338">10001</span></span></td>
<td><span data-ttu-id="99418-339">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-339">Electricity</span></span></td>
<td><span data-ttu-id="99418-340">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-340">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-341">500,00</span><span class="sxs-lookup"><span data-stu-id="99418-341">500.00</span></span></td>
<td><span data-ttu-id="99418-342">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-343">CC099</span><span class="sxs-lookup"><span data-stu-id="99418-343">CC099</span></span></td>
<td><span data-ttu-id="99418-344">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="99418-344">Default cost center</span></span></td>
<td><span data-ttu-id="99418-345">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-345">10001</span></span></td>
<td><span data-ttu-id="99418-346">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-346">Electricity</span></span></td>
<td><span data-ttu-id="99418-347">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-347">Variable cost</span></span></td>
<td><span data-ttu-id="99418-348">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="99418-348">-9,000.00</span></span></td>
<td><span data-ttu-id="99418-349">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-350">CC001</span><span class="sxs-lookup"><span data-stu-id="99418-350">CC001</span></span></td>
<td><span data-ttu-id="99418-351">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="99418-351">HR</span></span></td>
<td><span data-ttu-id="99418-352">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-352">10001</span></span></td>
<td><span data-ttu-id="99418-353">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-353">Electricity</span></span></td>
<td><span data-ttu-id="99418-354">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-354">Variable cost</span></span></td>
<td><span data-ttu-id="99418-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="99418-355">1,285.71</span></span></td>
<td><span data-ttu-id="99418-356">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-357">CC002</span><span class="sxs-lookup"><span data-stu-id="99418-357">CC002</span></span></td>
<td><span data-ttu-id="99418-358">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="99418-358">Finance</span></span></td>
<td><span data-ttu-id="99418-359">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-359">10001</span></span></td>
<td><span data-ttu-id="99418-360">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-360">Electricity</span></span></td>
<td><span data-ttu-id="99418-361">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-361">Variable cost</span></span></td>
<td><span data-ttu-id="99418-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="99418-362">7,714.29</span></span></td>
<td><span data-ttu-id="99418-363">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="99418-364">Lisätietoja kustannusten jaosta ja kohdistusperusteita löydät kohdasta Kustannusten jakokäytännöt ja kohdistusperusteet.</span><span class="sxs-lookup"><span data-stu-id="99418-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="99418-365">(Huomaa, että ohjeaihe ei ole vielä valmis; se on saatavilla pian.)</span><span class="sxs-lookup"><span data-stu-id="99418-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="99418-366">Vaihe 3: Käsittele yleiskustannustason laskenta</span><span class="sxs-lookup"><span data-stu-id="99418-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="99418-367">Yleiskustannustasolla veloitetaan yksi tai useampi määrätty kustannusobjekti.</span><span class="sxs-lookup"><span data-stu-id="99418-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="99418-368">Veloitus perustuu ennalta määrättyyn kustannustasoon sekä määritetyn kohdistusperusteen suuruuteen.</span><span class="sxs-lookup"><span data-stu-id="99418-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="99418-369">Määritä yleiskustannustaso.</span><span class="sxs-lookup"><span data-stu-id="99418-369">Define the overhead rate</span></span>

<span data-ttu-id="99418-370">Kustannusobjekti CC001 HR vaikuttaa joukkoon sisäisiä projekteja.</span><span class="sxs-lookup"><span data-stu-id="99418-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="99418-371">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon projektit.</span><span class="sxs-lookup"><span data-stu-id="99418-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="99418-372">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-372">Cost object</span></span></th>
<th><span data-ttu-id="99418-373">Tunnit</span><span class="sxs-lookup"><span data-stu-id="99418-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-374">Proj 1</span><span class="sxs-lookup"><span data-stu-id="99418-374">Proj 1</span></span></td>
<td><span data-ttu-id="99418-375">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="99418-375">Project 1</span></span></td>
<td><span data-ttu-id="99418-376">3</span><span class="sxs-lookup"><span data-stu-id="99418-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-377">Proj 2</span><span class="sxs-lookup"><span data-stu-id="99418-377">Proj 2</span></span></td>
<td><span data-ttu-id="99418-378">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="99418-378">Project 2</span></span></td>
<td><span data-ttu-id="99418-379">1</span><span class="sxs-lookup"><span data-stu-id="99418-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="99418-380">Kustannusprojektien osuudelle on määritetty ennalta kustannushinta.</span><span class="sxs-lookup"><span data-stu-id="99418-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="99418-381">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-381">Cost object</span></span></th>
<th><span data-ttu-id="99418-382">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="99418-382">Cost element</span></span></th>
<th><span data-ttu-id="99418-383">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="99418-383">Cost behavior</span></span></th>
<th><span data-ttu-id="99418-384">Yksiköt</span><span class="sxs-lookup"><span data-stu-id="99418-384">Units</span></span></th>
<th><span data-ttu-id="99418-385">Osuus</span><span class="sxs-lookup"><span data-stu-id="99418-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-386">CC001</span><span class="sxs-lookup"><span data-stu-id="99418-386">CC001</span></span></td>
<td><span data-ttu-id="99418-387">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="99418-387">HR</span></span></td>
<td><span data-ttu-id="99418-388">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-388">10001</span></span></td>
<td><span data-ttu-id="99418-389">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-389">Variable cost</span></span></td>
<td><span data-ttu-id="99418-390">1</span><span class="sxs-lookup"><span data-stu-id="99418-390">1</span></span></td>
<td><span data-ttu-id="99418-391">10</span><span class="sxs-lookup"><span data-stu-id="99418-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="99418-392">Seuraavassa taulukossa on esitetty tulos, kun Henkilöstöhallinnon projekteja käytetään kohdistusperusteena.</span><span class="sxs-lookup"><span data-stu-id="99418-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="99418-393">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-393">Cost object</span></span></th>
<th><span data-ttu-id="99418-394">Suuruus</span><span class="sxs-lookup"><span data-stu-id="99418-394">Magnitude</span></span></th>
<th><span data-ttu-id="99418-395">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="99418-395">Cost element</span></span></th>
<th><span data-ttu-id="99418-396">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="99418-396">Allocation factor</span></span></th>
<th><span data-ttu-id="99418-397">Summa</span><span class="sxs-lookup"><span data-stu-id="99418-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-398">Proj 1</span><span class="sxs-lookup"><span data-stu-id="99418-398">Proj 1</span></span></td>
<td><span data-ttu-id="99418-399">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="99418-399">Project 1</span></span></td>
<td><span data-ttu-id="99418-400">3</span><span class="sxs-lookup"><span data-stu-id="99418-400">3</span></span></td>
<td><span data-ttu-id="99418-401">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-401">10001</span></span></td>
<td><span data-ttu-id="99418-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="99418-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="99418-403">30,00</span><span class="sxs-lookup"><span data-stu-id="99418-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-404">Proj 2</span><span class="sxs-lookup"><span data-stu-id="99418-404">Proj 2</span></span></td>
<td><span data-ttu-id="99418-405">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="99418-405">Project 2</span></span></td>
<td><span data-ttu-id="99418-406">1</span><span class="sxs-lookup"><span data-stu-id="99418-406">1</span></span></td>
<td><span data-ttu-id="99418-407">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-407">10001</span></span></td>
<td><span data-ttu-id="99418-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="99418-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="99418-409">10,00</span><span class="sxs-lookup"><span data-stu-id="99418-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="99418-410">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="99418-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="99418-411">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="99418-411">Journal</span></span></th>
<th><span data-ttu-id="99418-412">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="99418-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="99418-413">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="99418-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="99418-414">Versio</span><span class="sxs-lookup"><span data-stu-id="99418-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-415">00003</span><span class="sxs-lookup"><span data-stu-id="99418-415">00003</span></span></td>
<td><span data-ttu-id="99418-416">Yleiskustannustason laskelman kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="99418-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="99418-417">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="99418-417">Fiscal</span></span></td>
<td><span data-ttu-id="99418-418">2017</span><span class="sxs-lookup"><span data-stu-id="99418-418">2017</span></span></td>
<td><span data-ttu-id="99418-419">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="99418-419">Period 1</span></span></td>
<td><span data-ttu-id="99418-420">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="99418-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="99418-421">Kirjauskansioviennit (Yleiskustannustason laskennan kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="99418-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="99418-422">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="99418-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="99418-423">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-423">Cost object</span></span></th>
<th><span data-ttu-id="99418-424">Suuruus</span><span class="sxs-lookup"><span data-stu-id="99418-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-425">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="99418-426">Proj 1</span><span class="sxs-lookup"><span data-stu-id="99418-426">Proj 1</span></span></td>
<td><span data-ttu-id="99418-427">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="99418-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="99418-428">3,00</span><span class="sxs-lookup"><span data-stu-id="99418-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-429">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="99418-430">Proj 2</span><span class="sxs-lookup"><span data-stu-id="99418-430">Proj 2</span></span></td>
<td><span data-ttu-id="99418-431">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="99418-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="99418-432">1,00</span><span class="sxs-lookup"><span data-stu-id="99418-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="99418-433">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="99418-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="99418-434">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="99418-435">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="99418-435">Cost element</span></span></th>
<th><span data-ttu-id="99418-436">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="99418-436">Cost behavior</span></span></th>
<th><span data-ttu-id="99418-437">Summa</span><span class="sxs-lookup"><span data-stu-id="99418-437">Amount</span></span></th>
<th><span data-ttu-id="99418-438">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="99418-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="99418-439">CC0001</span></span></td>
<td><span data-ttu-id="99418-440">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="99418-440">HR</span></span></td>
<td><span data-ttu-id="99418-441">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-441">10001</span></span></td>
<td><span data-ttu-id="99418-442">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-442">Electricity</span></span></td>
<td><span data-ttu-id="99418-443">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-443">Variable cost</span></span></td>
<td><span data-ttu-id="99418-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="99418-444">-30.00</span></span></td>
<td><span data-ttu-id="99418-445">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-446">Proj 1</span><span class="sxs-lookup"><span data-stu-id="99418-446">Proj 1</span></span></td>
<td><span data-ttu-id="99418-447">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="99418-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="99418-448">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-448">10001</span></span></td>
<td><span data-ttu-id="99418-449">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-449">Electricity</span></span></td>
<td><span data-ttu-id="99418-450">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-450">Variable cost</span></span></td>
<td><span data-ttu-id="99418-451">30,00</span><span class="sxs-lookup"><span data-stu-id="99418-451">30.00</span></span></td>
<td><span data-ttu-id="99418-452">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-453">CC001</span><span class="sxs-lookup"><span data-stu-id="99418-453">CC001</span></span></td>
<td><span data-ttu-id="99418-454">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="99418-454">HR</span></span></td>
<td><span data-ttu-id="99418-455">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-455">10001</span></span></td>
<td><span data-ttu-id="99418-456">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-456">Electricity</span></span></td>
<td><span data-ttu-id="99418-457">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-457">Variable cost</span></span></td>
<td><span data-ttu-id="99418-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="99418-458">-10.00</span></span></td>
<td><span data-ttu-id="99418-459">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-460">Proj 2</span><span class="sxs-lookup"><span data-stu-id="99418-460">Proj 2</span></span></td>
<td><span data-ttu-id="99418-461">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="99418-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="99418-462">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-462">10001</span></span></td>
<td><span data-ttu-id="99418-463">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-463">Electricity</span></span></td>
<td><span data-ttu-id="99418-464">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-464">Variable cost</span></span></td>
<td><span data-ttu-id="99418-465">10,00</span><span class="sxs-lookup"><span data-stu-id="99418-465">10.00</span></span></td>
<td><span data-ttu-id="99418-466">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="99418-467">Lisätietoja yleiskustannustason käytännöistä löydät kohdista Yleiskustannusten käytännöt ja Kohdistusperusteet.</span><span class="sxs-lookup"><span data-stu-id="99418-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="99418-468">(Huomaa, että ohjeaihe ei ole vielä valmis; se on saatavilla pian.)</span><span class="sxs-lookup"><span data-stu-id="99418-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="99418-469">Vaihe 4: Käsittele kustannusten kohdistuksen laskenta</span><span class="sxs-lookup"><span data-stu-id="99418-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="99418-470">Kohdistuksella kustannusobjektin saldo liitetään toisiin kustannusobjekteihin käyttämällä kohdistusperustetta.</span><span class="sxs-lookup"><span data-stu-id="99418-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="99418-471">Finance and Operations tukee vastavuoroista kohdistusmenetelmää.</span><span class="sxs-lookup"><span data-stu-id="99418-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="99418-472">Vastavuoroisessa kohdistusmenetelmässä tunnistetaan oheiskustannusobjektien käyttämät, keskinäiset palvelut täysin.</span><span class="sxs-lookup"><span data-stu-id="99418-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="99418-473">Järjestelmä määrittää oikean kohdistusjärjestyksen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="99418-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="99418-474">Kustannusobjektin saldo kohdistetaan yhdellä kohdistusperusteella.</span><span class="sxs-lookup"><span data-stu-id="99418-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="99418-475">Kustannusobjektien dimensiot ja niiden vastaavat jäsenet ylittävät kohdistukset ovat tuettuja.</span><span class="sxs-lookup"><span data-stu-id="99418-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="99418-476">Kustannusseurantayksikkö hallitsee kohdistusjärjestystä.</span><span class="sxs-lookup"><span data-stu-id="99418-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="99418-477">[![Vastavuoroinen menetelmä](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="99418-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="99418-478">Määritä kustannuksen kohdistus</span><span class="sxs-lookup"><span data-stu-id="99418-478">Define the cost allocation</span></span>

<span data-ttu-id="99418-479">Tämä on yksinkertainen esimerkki, jossa kerrotaan, miten voit jäljittää kustannuksen virran.</span><span class="sxs-lookup"><span data-stu-id="99418-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="99418-480">Kustannusobjekti CC001 HR liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="99418-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="99418-481">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="99418-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="99418-482">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-482">Cost object</span></span></th>
<th><span data-ttu-id="99418-483">HR-palvelut</span><span class="sxs-lookup"><span data-stu-id="99418-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-484">CC002</span><span class="sxs-lookup"><span data-stu-id="99418-484">CC002</span></span></td>
<td><span data-ttu-id="99418-485">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="99418-485">Finance</span></span></td>
<td><span data-ttu-id="99418-486">35</span><span class="sxs-lookup"><span data-stu-id="99418-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-487">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-487">CC003</span></span></td>
<td><span data-ttu-id="99418-488">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="99418-488">Assembly</span></span></td>
<td><span data-ttu-id="99418-489">55</span><span class="sxs-lookup"><span data-stu-id="99418-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-490">CC004</span><span class="sxs-lookup"><span data-stu-id="99418-490">CC004</span></span></td>
<td><span data-ttu-id="99418-491">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="99418-491">Packaging</span></span></td>
<td><span data-ttu-id="99418-492">10</span><span class="sxs-lookup"><span data-stu-id="99418-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="99418-493">Kustannusobjekti CC002 Taloushallinto liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="99418-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="99418-494">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Taloushallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="99418-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="99418-495">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-495">Cost object</span></span></th>
<th><span data-ttu-id="99418-496">Taloushallinnon palvelut</span><span class="sxs-lookup"><span data-stu-id="99418-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-497">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-497">CC003</span></span></td>
<td><span data-ttu-id="99418-498">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="99418-498">Assembly</span></span></td>
<td><span data-ttu-id="99418-499">65</span><span class="sxs-lookup"><span data-stu-id="99418-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-500">CC004</span><span class="sxs-lookup"><span data-stu-id="99418-500">CC004</span></span></td>
<td><span data-ttu-id="99418-501">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="99418-501">Packaging</span></span></td>
<td><span data-ttu-id="99418-502">35</span><span class="sxs-lookup"><span data-stu-id="99418-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="99418-503">Kustannusobjekti CC003 Kokoonpano liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="99418-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="99418-504">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Kokoonpanopalvelut.</span><span class="sxs-lookup"><span data-stu-id="99418-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="99418-505">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-505">Cost object</span></span></th>
<th><span data-ttu-id="99418-506">Kokoonpanopalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="99418-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-507">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-507">Prod 1</span></span></td>
<td><span data-ttu-id="99418-508">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-508">Product 1</span></span></td>
<td><span data-ttu-id="99418-509">60</span><span class="sxs-lookup"><span data-stu-id="99418-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-510">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-510">Prod 2</span></span></td>
<td><span data-ttu-id="99418-511">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-511">Product 2</span></span></td>
<td><span data-ttu-id="99418-512">20</span><span class="sxs-lookup"><span data-stu-id="99418-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="99418-513">Kustannusobjekti CC004 Pakkaus liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="99418-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="99418-514">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Pakkauspalvelut.</span><span class="sxs-lookup"><span data-stu-id="99418-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="99418-515">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-515">Cost object</span></span></th>
<th><span data-ttu-id="99418-516">Pakkauspalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="99418-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-517">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-517">Prod 1</span></span></td>
<td><span data-ttu-id="99418-518">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-518">Product 1</span></span></td>
<td><span data-ttu-id="99418-519">80</span><span class="sxs-lookup"><span data-stu-id="99418-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-520">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-520">Prod 2</span></span></td>
<td><span data-ttu-id="99418-521">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-521">Product 2</span></span></td>
<td><span data-ttu-id="99418-522">päivänä</span><span class="sxs-lookup"><span data-stu-id="99418-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="99418-523">**Huomautus:** Finance and Operationsissa tilastomittaukset, kuten tuotteen kuluttamat tuotantotunnit, voidaan johtaa lähdetiedoista.</span><span class="sxs-lookup"><span data-stu-id="99418-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="99418-524">Lisätietoja tilastomittausten lähteistä on kohdassa Tilastomittauksen lähdemallit.</span><span class="sxs-lookup"><span data-stu-id="99418-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="99418-525">(Huomaa, että ohjeaihe ei ole vielä valmis; se on saatavilla pian.) Seuraavassa taulukossa näytetään tulos, kun HR-palveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteä ja muuttuva kustannus).</span><span class="sxs-lookup"><span data-stu-id="99418-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="99418-526">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-526">Cost object</span></span></th>
<th><span data-ttu-id="99418-527">Suuruus</span><span class="sxs-lookup"><span data-stu-id="99418-527">Magnitude</span></span></th>
<th><span data-ttu-id="99418-528">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="99418-528">Allocation factor</span></span></th>
<th><span data-ttu-id="99418-529">Summa</span><span class="sxs-lookup"><span data-stu-id="99418-529">Amount</span></span></th>
<th><span data-ttu-id="99418-530">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="99418-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-531">CC002</span><span class="sxs-lookup"><span data-stu-id="99418-531">CC002</span></span></td>
<td><span data-ttu-id="99418-532">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="99418-532">Finance</span></span></td>
<td><span data-ttu-id="99418-533">35</span><span class="sxs-lookup"><span data-stu-id="99418-533">35</span></span></td>
<td><span data-ttu-id="99418-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="99418-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="99418-535">175.00</span><span class="sxs-lookup"><span data-stu-id="99418-535">175.00</span></span></td>
<td><span data-ttu-id="99418-536">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-537">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-537">CC003</span></span></td>
<td><span data-ttu-id="99418-538">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="99418-538">Assembly</span></span></td>
<td><span data-ttu-id="99418-539">55</span><span class="sxs-lookup"><span data-stu-id="99418-539">55</span></span></td>
<td><span data-ttu-id="99418-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="99418-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="99418-541">275.00</span><span class="sxs-lookup"><span data-stu-id="99418-541">275.00</span></span></td>
<td><span data-ttu-id="99418-542">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-543">CC004</span><span class="sxs-lookup"><span data-stu-id="99418-543">CC004</span></span></td>
<td><span data-ttu-id="99418-544">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="99418-544">Packaging</span></span></td>
<td><span data-ttu-id="99418-545">10</span><span class="sxs-lookup"><span data-stu-id="99418-545">10</span></span></td>
<td><span data-ttu-id="99418-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="99418-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="99418-547">50,00</span><span class="sxs-lookup"><span data-stu-id="99418-547">50.00</span></span></td>
<td><span data-ttu-id="99418-548">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-549">CC002</span><span class="sxs-lookup"><span data-stu-id="99418-549">CC002</span></span></td>
<td><span data-ttu-id="99418-550">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="99418-550">Finance</span></span></td>
<td><span data-ttu-id="99418-551">35</span><span class="sxs-lookup"><span data-stu-id="99418-551">35</span></span></td>
<td><span data-ttu-id="99418-552">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="99418-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="99418-553">436.00</span><span class="sxs-lookup"><span data-stu-id="99418-553">436.00</span></span></td>
<td><span data-ttu-id="99418-554">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-555">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-555">CC003</span></span></td>
<td><span data-ttu-id="99418-556">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="99418-556">Assembly</span></span></td>
<td><span data-ttu-id="99418-557">55</span><span class="sxs-lookup"><span data-stu-id="99418-557">55</span></span></td>
<td><span data-ttu-id="99418-558">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="99418-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="99418-559">685.14</span><span class="sxs-lookup"><span data-stu-id="99418-559">685.14</span></span></td>
<td><span data-ttu-id="99418-560">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-561">CC004</span><span class="sxs-lookup"><span data-stu-id="99418-561">CC004</span></span></td>
<td><span data-ttu-id="99418-562">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="99418-562">Packaging</span></span></td>
<td><span data-ttu-id="99418-563">10</span><span class="sxs-lookup"><span data-stu-id="99418-563">10</span></span></td>
<td><span data-ttu-id="99418-564">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="99418-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="99418-565">124.57</span><span class="sxs-lookup"><span data-stu-id="99418-565">124.57</span></span></td>
<td><span data-ttu-id="99418-566">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="99418-567">Seuraavassa taulukossa näytetään tulos, kun Taloushallinnon palveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="99418-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="99418-568">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-568">Cost object</span></span></th>
<th><span data-ttu-id="99418-569">Suuruus</span><span class="sxs-lookup"><span data-stu-id="99418-569">Magnitude</span></span></th>
<th><span data-ttu-id="99418-570">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="99418-570">Allocation factor</span></span></th>
<th><span data-ttu-id="99418-571">Summa</span><span class="sxs-lookup"><span data-stu-id="99418-571">Amount</span></span></th>
<th><span data-ttu-id="99418-572">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="99418-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-573">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-573">CC003</span></span></td>
<td><span data-ttu-id="99418-574">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="99418-574">Assembly</span></span></td>
<td><span data-ttu-id="99418-575">65</span><span class="sxs-lookup"><span data-stu-id="99418-575">65</span></span></td>
<td><span data-ttu-id="99418-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="99418-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="99418-577">438.75</span><span class="sxs-lookup"><span data-stu-id="99418-577">438.75</span></span></td>
<td><span data-ttu-id="99418-578">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-579">CC004</span><span class="sxs-lookup"><span data-stu-id="99418-579">CC004</span></span></td>
<td><span data-ttu-id="99418-580">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="99418-580">Packaging</span></span></td>
<td><span data-ttu-id="99418-581">35</span><span class="sxs-lookup"><span data-stu-id="99418-581">35</span></span></td>
<td><span data-ttu-id="99418-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="99418-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="99418-583">236.25</span><span class="sxs-lookup"><span data-stu-id="99418-583">236.25</span></span></td>
<td><span data-ttu-id="99418-584">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-585">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-585">CC003</span></span></td>
<td><span data-ttu-id="99418-586">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="99418-586">Assembly</span></span></td>
<td><span data-ttu-id="99418-587">65</span><span class="sxs-lookup"><span data-stu-id="99418-587">65</span></span></td>
<td><span data-ttu-id="99418-588">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="99418-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="99418-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="99418-589">5,297.69</span></span></td>
<td><span data-ttu-id="99418-590">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-591">CC004</span><span class="sxs-lookup"><span data-stu-id="99418-591">CC004</span></span></td>
<td><span data-ttu-id="99418-592">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="99418-592">Packaging</span></span></td>
<td><span data-ttu-id="99418-593">35</span><span class="sxs-lookup"><span data-stu-id="99418-593">35</span></span></td>
<td><span data-ttu-id="99418-594">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="99418-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="99418-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="99418-595">2,852.60</span></span></td>
<td><span data-ttu-id="99418-596">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="99418-597">Seuraavassa taulukossa näytetään tulos, kun Kokoonpanopalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="99418-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="99418-598">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-598">Cost object</span></span></th>
<th><span data-ttu-id="99418-599">Suuruus</span><span class="sxs-lookup"><span data-stu-id="99418-599">Magnitude</span></span></th>
<th><span data-ttu-id="99418-600">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="99418-600">Allocation factor</span></span></th>
<th><span data-ttu-id="99418-601">Summa</span><span class="sxs-lookup"><span data-stu-id="99418-601">Amount</span></span></th>
<th><span data-ttu-id="99418-602">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="99418-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-603">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-603">Prod 1</span></span></td>
<td><span data-ttu-id="99418-604">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-604">Product 1</span></span></td>
<td><span data-ttu-id="99418-605">60</span><span class="sxs-lookup"><span data-stu-id="99418-605">60</span></span></td>
<td><span data-ttu-id="99418-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="99418-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="99418-607">535.31</span><span class="sxs-lookup"><span data-stu-id="99418-607">535.31</span></span></td>
<td><span data-ttu-id="99418-608">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-609">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-609">Prod 2</span></span></td>
<td><span data-ttu-id="99418-610">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-610">Product 2</span></span></td>
<td><span data-ttu-id="99418-611">20</span><span class="sxs-lookup"><span data-stu-id="99418-611">20</span></span></td>
<td><span data-ttu-id="99418-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="99418-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="99418-613">178.44</span><span class="sxs-lookup"><span data-stu-id="99418-613">178.44</span></span></td>
<td><span data-ttu-id="99418-614">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-615">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-615">Prod 1</span></span></td>
<td><span data-ttu-id="99418-616">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-616">Product 1</span></span></td>
<td><span data-ttu-id="99418-617">60</span><span class="sxs-lookup"><span data-stu-id="99418-617">60</span></span></td>
<td><span data-ttu-id="99418-618">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="99418-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="99418-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="99418-619">4,487.12</span></span></td>
<td><span data-ttu-id="99418-620">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-621">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-621">Prod 2</span></span></td>
<td><span data-ttu-id="99418-622">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-622">Product 2</span></span></td>
<td><span data-ttu-id="99418-623">20</span><span class="sxs-lookup"><span data-stu-id="99418-623">20</span></span></td>
<td><span data-ttu-id="99418-624">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="99418-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="99418-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="99418-625">1,495.71</span></span></td>
<td><span data-ttu-id="99418-626">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="99418-627">Seuraavassa taulukossa näytetään tulos, kun Pakkauspalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="99418-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="99418-628">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-628">Cost object</span></span></th>
<th><span data-ttu-id="99418-629">Suuruus</span><span class="sxs-lookup"><span data-stu-id="99418-629">Magnitude</span></span></th>
<th><span data-ttu-id="99418-630">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="99418-630">Allocation factor</span></span></th>
<th><span data-ttu-id="99418-631">Summa</span><span class="sxs-lookup"><span data-stu-id="99418-631">Amount</span></span></th>
<th><span data-ttu-id="99418-632">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="99418-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-633">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-633">Prod 1</span></span></td>
<td><span data-ttu-id="99418-634">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-634">Product 1</span></span></td>
<td><span data-ttu-id="99418-635">80</span><span class="sxs-lookup"><span data-stu-id="99418-635">80</span></span></td>
<td><span data-ttu-id="99418-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="99418-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="99418-637">241.05</span><span class="sxs-lookup"><span data-stu-id="99418-637">241.05</span></span></td>
<td><span data-ttu-id="99418-638">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-639">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-639">Prod 2</span></span></td>
<td><span data-ttu-id="99418-640">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-640">Product 2</span></span></td>
<td><span data-ttu-id="99418-641">15</span><span class="sxs-lookup"><span data-stu-id="99418-641">15</span></span></td>
<td><span data-ttu-id="99418-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="99418-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="99418-643">45.20</span><span class="sxs-lookup"><span data-stu-id="99418-643">45.20</span></span></td>
<td><span data-ttu-id="99418-644">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-645">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-645">Prod 1</span></span></td>
<td><span data-ttu-id="99418-646">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-646">Product 1</span></span></td>
<td><span data-ttu-id="99418-647">80</span><span class="sxs-lookup"><span data-stu-id="99418-647">80</span></span></td>
<td><span data-ttu-id="99418-648">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="99418-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="99418-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="99418-649">2,507.09</span></span></td>
<td><span data-ttu-id="99418-650">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-651">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-651">Prod 2</span></span></td>
<td><span data-ttu-id="99418-652">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-652">Product 2</span></span></td>
<td><span data-ttu-id="99418-653">15</span><span class="sxs-lookup"><span data-stu-id="99418-653">15</span></span></td>
<td><span data-ttu-id="99418-654">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="99418-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="99418-655">470.08</span><span class="sxs-lookup"><span data-stu-id="99418-655">470.08</span></span></td>
<td><span data-ttu-id="99418-656">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="99418-657">Kirjauskansioviennit (kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="99418-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="99418-658">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="99418-658">Journal</span></span></th>
<th><span data-ttu-id="99418-659">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="99418-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="99418-660">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="99418-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="99418-661">Versio</span><span class="sxs-lookup"><span data-stu-id="99418-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-662">00004</span><span class="sxs-lookup"><span data-stu-id="99418-662">00004</span></span></td>
<td><span data-ttu-id="99418-663">Kustannusten kohdistuskirjauskansio</span><span class="sxs-lookup"><span data-stu-id="99418-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="99418-664">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="99418-664">Fiscal</span></span></td>
<td><span data-ttu-id="99418-665">2017</span><span class="sxs-lookup"><span data-stu-id="99418-665">2017</span></span></td>
<td><span data-ttu-id="99418-666">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="99418-666">Period 1</span></span></td>
<td><span data-ttu-id="99418-667">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="99418-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="99418-668">Kirjauskansion rivit</span><span class="sxs-lookup"><span data-stu-id="99418-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="99418-669">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="99418-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="99418-670">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="99418-671">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="99418-671">Cost element</span></span></th>
<th><span data-ttu-id="99418-672">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="99418-672">Cost behavior</span></span></th>
<th><span data-ttu-id="99418-673">Summa</span><span class="sxs-lookup"><span data-stu-id="99418-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-674">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="99418-675">CC001</span><span class="sxs-lookup"><span data-stu-id="99418-675">CC001</span></span></td>
<td><span data-ttu-id="99418-676">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="99418-676">HR</span></span></td>
<td><span data-ttu-id="99418-677">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-677">10001</span></span></td>
<td><span data-ttu-id="99418-678">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-678">Electricity</span></span></td>
<td><span data-ttu-id="99418-679">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-679">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-680">500,00</span><span class="sxs-lookup"><span data-stu-id="99418-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-681">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="99418-682">CC001</span><span class="sxs-lookup"><span data-stu-id="99418-682">CC001</span></span></td>
<td><span data-ttu-id="99418-683">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="99418-683">HR</span></span></td>
<td><span data-ttu-id="99418-684">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-684">10001</span></span></td>
<td><span data-ttu-id="99418-685">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-685">Electricity</span></span></td>
<td><span data-ttu-id="99418-686">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-686">Variable cost</span></span></td>
<td><span data-ttu-id="99418-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="99418-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-688">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="99418-689">CC002</span><span class="sxs-lookup"><span data-stu-id="99418-689">CC002</span></span></td>
<td><span data-ttu-id="99418-690">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="99418-690">Finance</span></span></td>
<td><span data-ttu-id="99418-691">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-691">10001</span></span></td>
<td><span data-ttu-id="99418-692">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-692">Electricity</span></span></td>
<td><span data-ttu-id="99418-693">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-693">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-694">675.00</span><span class="sxs-lookup"><span data-stu-id="99418-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-695">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="99418-696">CC002</span><span class="sxs-lookup"><span data-stu-id="99418-696">CC002</span></span></td>
<td><span data-ttu-id="99418-697">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="99418-697">Finance</span></span></td>
<td><span data-ttu-id="99418-698">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-698">10001</span></span></td>
<td><span data-ttu-id="99418-699">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-699">Electricity</span></span></td>
<td><span data-ttu-id="99418-700">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-700">Variable cost</span></span></td>
<td><span data-ttu-id="99418-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="99418-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-702">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="99418-703">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-703">CC003</span></span></td>
<td><span data-ttu-id="99418-704">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="99418-704">Assembly</span></span></td>
<td><span data-ttu-id="99418-705">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-705">10001</span></span></td>
<td><span data-ttu-id="99418-706">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-706">Electricity</span></span></td>
<td><span data-ttu-id="99418-707">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-707">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-708">713.75</span><span class="sxs-lookup"><span data-stu-id="99418-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-709">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="99418-710">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-710">CC003</span></span></td>
<td><span data-ttu-id="99418-711">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="99418-711">Assembly</span></span></td>
<td><span data-ttu-id="99418-712">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-712">10001</span></span></td>
<td><span data-ttu-id="99418-713">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-713">Electricity</span></span></td>
<td><span data-ttu-id="99418-714">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-714">Variable cost</span></span></td>
<td><span data-ttu-id="99418-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="99418-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-716">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="99418-717">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-717">CC003</span></span></td>
<td><span data-ttu-id="99418-718">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="99418-718">Packaging</span></span></td>
<td><span data-ttu-id="99418-719">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-719">10001</span></span></td>
<td><span data-ttu-id="99418-720">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-720">Electricity</span></span></td>
<td><span data-ttu-id="99418-721">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-721">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-722">286.25</span><span class="sxs-lookup"><span data-stu-id="99418-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-723">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="99418-724">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-724">CC003</span></span></td>
<td><span data-ttu-id="99418-725">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="99418-725">Packaging</span></span></td>
<td><span data-ttu-id="99418-726">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-726">10001</span></span></td>
<td><span data-ttu-id="99418-727">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-727">Electricity</span></span></td>
<td><span data-ttu-id="99418-728">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-728">Variable cost</span></span></td>
<td><span data-ttu-id="99418-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="99418-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-730">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="99418-731">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-731">Prod 1</span></span></td>
<td><span data-ttu-id="99418-732">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-732">Product 1</span></span></td>
<td><span data-ttu-id="99418-733">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-733">10001</span></span></td>
<td><span data-ttu-id="99418-734">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-734">Electricity</span></span></td>
<td><span data-ttu-id="99418-735">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-735">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-736">776.36</span><span class="sxs-lookup"><span data-stu-id="99418-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-737">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="99418-738">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-738">Prod 1</span></span></td>
<td><span data-ttu-id="99418-739">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-739">Product 1</span></span></td>
<td><span data-ttu-id="99418-740">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-740">10001</span></span></td>
<td><span data-ttu-id="99418-741">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-741">Electricity</span></span></td>
<td><span data-ttu-id="99418-742">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-742">Variable cost</span></span></td>
<td><span data-ttu-id="99418-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="99418-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-744">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="99418-745">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-745">Prod 2</span></span></td>
<td><span data-ttu-id="99418-746">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-746">Product 1</span></span></td>
<td><span data-ttu-id="99418-747">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-747">10001</span></span></td>
<td><span data-ttu-id="99418-748">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-748">Electricity</span></span></td>
<td><span data-ttu-id="99418-749">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-749">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-750">223.64</span><span class="sxs-lookup"><span data-stu-id="99418-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-751">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="99418-752">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-752">Prod 2</span></span></td>
<td><span data-ttu-id="99418-753">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-753">Product 1</span></span></td>
<td><span data-ttu-id="99418-754">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-754">10001</span></span></td>
<td><span data-ttu-id="99418-755">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-755">Electricity</span></span></td>
<td><span data-ttu-id="99418-756">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-756">Variable cost</span></span></td>
<td><span data-ttu-id="99418-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="99418-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="99418-758">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="99418-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="99418-759">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="99418-760">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="99418-760">Cost element</span></span></th>
<th><span data-ttu-id="99418-761">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="99418-761">Cost behavior</span></span></th>
<th><span data-ttu-id="99418-762">Summa</span><span class="sxs-lookup"><span data-stu-id="99418-762">Amount</span></span></th>
<th><span data-ttu-id="99418-763">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="99418-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="99418-764">CC001</span><span class="sxs-lookup"><span data-stu-id="99418-764">CC001</span></span></td>
<td><span data-ttu-id="99418-765">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="99418-765">HR</span></span></td>
<td><span data-ttu-id="99418-766">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-766">10001</span></span></td>
<td><span data-ttu-id="99418-767">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-767">Electricity</span></span></td>
<td><span data-ttu-id="99418-768">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-768">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="99418-769">-500.00</span></span></td>
<td><span data-ttu-id="99418-770">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-771">CC002</span><span class="sxs-lookup"><span data-stu-id="99418-771">CC002</span></span></td>
<td><span data-ttu-id="99418-772">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="99418-772">Finance</span></span></td>
<td><span data-ttu-id="99418-773">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-773">10001</span></span></td>
<td><span data-ttu-id="99418-774">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-774">Electricity</span></span></td>
<td><span data-ttu-id="99418-775">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-775">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-776">175.00</span><span class="sxs-lookup"><span data-stu-id="99418-776">175.00</span></span></td>
<td><span data-ttu-id="99418-777">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-778">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-778">CC003</span></span></td>
<td><span data-ttu-id="99418-779">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="99418-779">Assembly</span></span></td>
<td><span data-ttu-id="99418-780">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-780">10001</span></span></td>
<td><span data-ttu-id="99418-781">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-781">Electricity</span></span></td>
<td><span data-ttu-id="99418-782">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-782">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-783">275.00</span><span class="sxs-lookup"><span data-stu-id="99418-783">275.00</span></span></td>
<td><span data-ttu-id="99418-784">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-785">CC004</span><span class="sxs-lookup"><span data-stu-id="99418-785">CC004</span></span></td>
<td><span data-ttu-id="99418-786">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="99418-786">Packaging</span></span></td>
<td><span data-ttu-id="99418-787">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-787">10001</span></span></td>
<td><span data-ttu-id="99418-788">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-788">Electricity</span></span></td>
<td><span data-ttu-id="99418-789">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-789">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-790">50,00</span><span class="sxs-lookup"><span data-stu-id="99418-790">50,00</span></span></td>
<td><span data-ttu-id="99418-791">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-792">CC001</span><span class="sxs-lookup"><span data-stu-id="99418-792">CC001</span></span></td>
<td><span data-ttu-id="99418-793">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="99418-793">HR</span></span></td>
<td><span data-ttu-id="99418-794">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-794">10001</span></span></td>
<td><span data-ttu-id="99418-795">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-795">Electricity</span></span></td>
<td><span data-ttu-id="99418-796">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-796">Variable cost</span></span></td>
<td><span data-ttu-id="99418-797">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="99418-797">-1,245.71</span></span></td>
<td><span data-ttu-id="99418-798">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-799">CC002</span><span class="sxs-lookup"><span data-stu-id="99418-799">CC002</span></span></td>
<td><span data-ttu-id="99418-800">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="99418-800">Finance</span></span></td>
<td><span data-ttu-id="99418-801">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-801">10001</span></span></td>
<td><span data-ttu-id="99418-802">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-802">Electricity</span></span></td>
<td><span data-ttu-id="99418-803">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-803">Variable cost</span></span></td>
<td><span data-ttu-id="99418-804">436.00</span><span class="sxs-lookup"><span data-stu-id="99418-804">436.00</span></span></td>
<td><span data-ttu-id="99418-805">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-806">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-806">CC003</span></span></td>
<td><span data-ttu-id="99418-807">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="99418-807">Assembly</span></span></td>
<td><span data-ttu-id="99418-808">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-808">10001</span></span></td>
<td><span data-ttu-id="99418-809">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-809">Electricity</span></span></td>
<td><span data-ttu-id="99418-810">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-810">Variable cost</span></span></td>
<td><span data-ttu-id="99418-811">685.14</span><span class="sxs-lookup"><span data-stu-id="99418-811">685.14</span></span></td>
<td><span data-ttu-id="99418-812">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-813">CC004</span><span class="sxs-lookup"><span data-stu-id="99418-813">CC004</span></span></td>
<td><span data-ttu-id="99418-814">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="99418-814">Packaging</span></span></td>
<td><span data-ttu-id="99418-815">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-815">10001</span></span></td>
<td><span data-ttu-id="99418-816">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-816">Electricity</span></span></td>
<td><span data-ttu-id="99418-817">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-817">Variable cost</span></span></td>
<td><span data-ttu-id="99418-818">124.57</span><span class="sxs-lookup"><span data-stu-id="99418-818">124.57</span></span></td>
<td><span data-ttu-id="99418-819">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-820">CC002</span><span class="sxs-lookup"><span data-stu-id="99418-820">CC002</span></span></td>
<td><span data-ttu-id="99418-821">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="99418-821">Finance</span></span></td>
<td><span data-ttu-id="99418-822">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-822">10001</span></span></td>
<td><span data-ttu-id="99418-823">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-823">Electricity</span></span></td>
<td><span data-ttu-id="99418-824">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-824">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="99418-825">-675.00</span></span></td>
<td><span data-ttu-id="99418-826">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-827">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-827">CC003</span></span></td>
<td><span data-ttu-id="99418-828">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="99418-828">Assembly</span></span></td>
<td><span data-ttu-id="99418-829">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-829">10001</span></span></td>
<td><span data-ttu-id="99418-830">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-830">Electricity</span></span></td>
<td><span data-ttu-id="99418-831">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-831">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-832">438.75</span><span class="sxs-lookup"><span data-stu-id="99418-832">438.75</span></span></td>
<td><span data-ttu-id="99418-833">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-834">CC004</span><span class="sxs-lookup"><span data-stu-id="99418-834">CC004</span></span></td>
<td><span data-ttu-id="99418-835">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="99418-835">Packaging</span></span></td>
<td><span data-ttu-id="99418-836">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-836">10001</span></span></td>
<td><span data-ttu-id="99418-837">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-837">Electricity</span></span></td>
<td><span data-ttu-id="99418-838">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-838">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-839">236.25</span><span class="sxs-lookup"><span data-stu-id="99418-839">236.25</span></span></td>
<td><span data-ttu-id="99418-840">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-841">CC002</span><span class="sxs-lookup"><span data-stu-id="99418-841">CC002</span></span></td>
<td><span data-ttu-id="99418-842">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="99418-842">Finance</span></span></td>
<td><span data-ttu-id="99418-843">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-843">10001</span></span></td>
<td><span data-ttu-id="99418-844">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-844">Electricity</span></span></td>
<td><span data-ttu-id="99418-845">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-845">Variable cost</span></span></td>
<td><span data-ttu-id="99418-846">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="99418-846">-8,150.29</span></span></td>
<td><span data-ttu-id="99418-847">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-848">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-848">CC003</span></span></td>
<td><span data-ttu-id="99418-849">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="99418-849">Assembly</span></span></td>
<td><span data-ttu-id="99418-850">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-850">10001</span></span></td>
<td><span data-ttu-id="99418-851">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-851">Electricity</span></span></td>
<td><span data-ttu-id="99418-852">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-852">Variable cost</span></span></td>
<td><span data-ttu-id="99418-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="99418-853">5,297.69</span></span></td>
<td><span data-ttu-id="99418-854">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-855">CC004</span><span class="sxs-lookup"><span data-stu-id="99418-855">CC004</span></span></td>
<td><span data-ttu-id="99418-856">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="99418-856">Packaging</span></span></td>
<td><span data-ttu-id="99418-857">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-857">10001</span></span></td>
<td><span data-ttu-id="99418-858">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-858">Electricity</span></span></td>
<td><span data-ttu-id="99418-859">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-859">Variable cost</span></span></td>
<td><span data-ttu-id="99418-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="99418-860">2,852.60</span></span></td>
<td><span data-ttu-id="99418-861">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-862">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-862">CC003</span></span></td>
<td><span data-ttu-id="99418-863">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="99418-863">Assembly</span></span></td>
<td><span data-ttu-id="99418-864">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-864">10001</span></span></td>
<td><span data-ttu-id="99418-865">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-865">Electricity</span></span></td>
<td><span data-ttu-id="99418-866">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-866">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-867">-713,75</span><span class="sxs-lookup"><span data-stu-id="99418-867">-713.75</span></span></td>
<td><span data-ttu-id="99418-868">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-869">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-869">Prod 1</span></span></td>
<td><span data-ttu-id="99418-870">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-870">Product 1</span></span></td>
<td><span data-ttu-id="99418-871">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-871">10001</span></span></td>
<td><span data-ttu-id="99418-872">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-872">Electricity</span></span></td>
<td><span data-ttu-id="99418-873">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-873">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-874">535.31</span><span class="sxs-lookup"><span data-stu-id="99418-874">535.31</span></span></td>
<td><span data-ttu-id="99418-875">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-876">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-876">Prod 2</span></span></td>
<td><span data-ttu-id="99418-877">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-877">Product 2</span></span></td>
<td><span data-ttu-id="99418-878">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-878">10001</span></span></td>
<td><span data-ttu-id="99418-879">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-879">Electricity</span></span></td>
<td><span data-ttu-id="99418-880">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-880">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-881">178.44</span><span class="sxs-lookup"><span data-stu-id="99418-881">178.44</span></span></td>
<td><span data-ttu-id="99418-882">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-883">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-883">CC003</span></span></td>
<td><span data-ttu-id="99418-884">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="99418-884">Assembly</span></span></td>
<td><span data-ttu-id="99418-885">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-885">10001</span></span></td>
<td><span data-ttu-id="99418-886">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-886">Electricity</span></span></td>
<td><span data-ttu-id="99418-887">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-887">Variable cost</span></span></td>
<td><span data-ttu-id="99418-888">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="99418-888">-5,982.83</span></span></td>
<td><span data-ttu-id="99418-889">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-890">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-890">Prod 1</span></span></td>
<td><span data-ttu-id="99418-891">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-891">Product 1</span></span></td>
<td><span data-ttu-id="99418-892">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-892">10001</span></span></td>
<td><span data-ttu-id="99418-893">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-893">Electricity</span></span></td>
<td><span data-ttu-id="99418-894">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-894">Variable cost</span></span></td>
<td><span data-ttu-id="99418-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="99418-895">4,487.12</span></span></td>
<td><span data-ttu-id="99418-896">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-897">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-897">Prod 2</span></span></td>
<td><span data-ttu-id="99418-898">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-898">Product 2</span></span></td>
<td><span data-ttu-id="99418-899">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-899">10001</span></span></td>
<td><span data-ttu-id="99418-900">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-900">Electricity</span></span></td>
<td><span data-ttu-id="99418-901">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-901">Variable cost</span></span></td>
<td><span data-ttu-id="99418-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="99418-902">1,495.71</span></span></td>
<td><span data-ttu-id="99418-903">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-904">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-904">CC003</span></span></td>
<td><span data-ttu-id="99418-905">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="99418-905">Assembly</span></span></td>
<td><span data-ttu-id="99418-906">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-906">10001</span></span></td>
<td><span data-ttu-id="99418-907">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-907">Electricity</span></span></td>
<td><span data-ttu-id="99418-908">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-908">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="99418-909">-286.25</span></span></td>
<td><span data-ttu-id="99418-910">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-911">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-911">Prod 1</span></span></td>
<td><span data-ttu-id="99418-912">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-912">Product 1</span></span></td>
<td><span data-ttu-id="99418-913">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-913">10001</span></span></td>
<td><span data-ttu-id="99418-914">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-914">Electricity</span></span></td>
<td><span data-ttu-id="99418-915">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-915">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-916">241.05</span><span class="sxs-lookup"><span data-stu-id="99418-916">241.05</span></span></td>
<td><span data-ttu-id="99418-917">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-918">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-918">Prod 2</span></span></td>
<td><span data-ttu-id="99418-919">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-919">Product 2</span></span></td>
<td><span data-ttu-id="99418-920">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-920">10001</span></span></td>
<td><span data-ttu-id="99418-921">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-921">Electricity</span></span></td>
<td><span data-ttu-id="99418-922">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-922">Fixed cost</span></span></td>
<td><span data-ttu-id="99418-923">45.20</span><span class="sxs-lookup"><span data-stu-id="99418-923">45.20</span></span></td>
<td><span data-ttu-id="99418-924">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-925">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-925">CC003</span></span></td>
<td><span data-ttu-id="99418-926">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="99418-926">Assembly</span></span></td>
<td><span data-ttu-id="99418-927">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-927">10001</span></span></td>
<td><span data-ttu-id="99418-928">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-928">Electricity</span></span></td>
<td><span data-ttu-id="99418-929">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-929">Variable cost</span></span></td>
<td><span data-ttu-id="99418-930">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="99418-930">-2,977.17</span></span></td>
<td><span data-ttu-id="99418-931">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-932">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-932">Prod 1</span></span></td>
<td><span data-ttu-id="99418-933">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-933">Product 1</span></span></td>
<td><span data-ttu-id="99418-934">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-934">10001</span></span></td>
<td><span data-ttu-id="99418-935">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-935">Electricity</span></span></td>
<td><span data-ttu-id="99418-936">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-936">Variable cost</span></span></td>
<td><span data-ttu-id="99418-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="99418-937">2,507.09</span></span></td>
<td><span data-ttu-id="99418-938">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="99418-939">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-939">Prod 2</span></span></td>
<td><span data-ttu-id="99418-940">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-940">Product 2</span></span></td>
<td><span data-ttu-id="99418-941">10 001</span><span class="sxs-lookup"><span data-stu-id="99418-941">10001</span></span></td>
<td><span data-ttu-id="99418-942">Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-942">Electricity</span></span></td>
<td><span data-ttu-id="99418-943">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-943">Variable cost</span></span></td>
<td><span data-ttu-id="99418-944">470.08</span><span class="sxs-lookup"><span data-stu-id="99418-944">470.08</span></span></td>
<td><span data-ttu-id="99418-945">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="99418-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="99418-946">Johtopäätökset</span><span class="sxs-lookup"><span data-stu-id="99418-946">Conclusion</span></span>
<span data-ttu-id="99418-947">Kirjanpidossa kirjataan tyhjään kustannuspaikkatunnukseen sähkökustannus arvolla 10 000,00.</span><span class="sxs-lookup"><span data-stu-id="99418-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="99418-948">Tämän ansiosta kustannuslaskijat tietävät, että kustannus on kohdistettava.</span><span class="sxs-lookup"><span data-stu-id="99418-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="99418-949">Kustannukset virtaavat kirjanpidossa organisaation yksiköiden ja tasojen läpi käytössä olevien käytäntöjen ja sääntöjen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="99418-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="99418-950">Kukin kustannus on liitetty kustannusperusteeseen, joka sisältää parhaan arvion kustannusten kohdistuksesta.</span><span class="sxs-lookup"><span data-stu-id="99418-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="99418-951">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="99418-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="99418-952">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="99418-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="99418-953">Yhteensä</span><span class="sxs-lookup"><span data-stu-id="99418-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="99418-954">CC099</span><span class="sxs-lookup"><span data-stu-id="99418-954">CC099</span></span></th>
<th><span data-ttu-id="99418-955">CC001</span><span class="sxs-lookup"><span data-stu-id="99418-955">CC001</span></span></th>
<th><span data-ttu-id="99418-956">CC002</span><span class="sxs-lookup"><span data-stu-id="99418-956">CC002</span></span></th>
<th><span data-ttu-id="99418-957">CC003</span><span class="sxs-lookup"><span data-stu-id="99418-957">CC003</span></span></th>
<th><span data-ttu-id="99418-958">CC004</span><span class="sxs-lookup"><span data-stu-id="99418-958">CC004</span></span></th>
<th><span data-ttu-id="99418-959">Proj 1</span><span class="sxs-lookup"><span data-stu-id="99418-959">Proj 1</span></span></th>
<th><span data-ttu-id="99418-960">Proj 2</span><span class="sxs-lookup"><span data-stu-id="99418-960">Proj 2</span></span></th>
<th><span data-ttu-id="99418-961">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="99418-961">Prod 1</span></span></th>
<th><span data-ttu-id="99418-962">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="99418-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="99418-963">10001 Sähkö</span><span class="sxs-lookup"><span data-stu-id="99418-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="99418-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-965"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="99418-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-966"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="99418-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-967"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="99418-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="99418-968"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="99418-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-969"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="99418-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-970"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="99418-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-971"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="99418-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-972"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="99418-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="99418-973">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="99418-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-974">0,00</span><span class="sxs-lookup"><span data-stu-id="99418-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="99418-975">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="99418-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-976">0,00</span><span class="sxs-lookup"><span data-stu-id="99418-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-977">0,00</span><span class="sxs-lookup"><span data-stu-id="99418-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-978">0,00</span><span class="sxs-lookup"><span data-stu-id="99418-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-979">0,00</span><span class="sxs-lookup"><span data-stu-id="99418-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-980">0,00</span><span class="sxs-lookup"><span data-stu-id="99418-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="99418-981">776.36</span><span class="sxs-lookup"><span data-stu-id="99418-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-982">223.64</span><span class="sxs-lookup"><span data-stu-id="99418-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-983"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="99418-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="99418-984">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="99418-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-985">000</span><span class="sxs-lookup"><span data-stu-id="99418-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-986">0,00</span><span class="sxs-lookup"><span data-stu-id="99418-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-987">0,00</span><span class="sxs-lookup"><span data-stu-id="99418-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-988">0,00</span><span class="sxs-lookup"><span data-stu-id="99418-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-989">0,00</span><span class="sxs-lookup"><span data-stu-id="99418-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-990">30,00</span><span class="sxs-lookup"><span data-stu-id="99418-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-991">10,00</span><span class="sxs-lookup"><span data-stu-id="99418-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="99418-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="99418-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="99418-994"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="99418-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="99418-995">Tässä ohjeaiheessa esitellään, miten ensisijainen kustannuselementti, 10001 Sähkö, virtaa kustannusobjektien läpi.</span><span class="sxs-lookup"><span data-stu-id="99418-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="99418-996">Tästä syystä tämä yleiskustannus kohdistetaan organisaation alimmalle tasolle.</span><span class="sxs-lookup"><span data-stu-id="99418-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="99418-997">Toisin sanoen alimman tason kustannusobjektit kantavat kustannuksen.</span><span class="sxs-lookup"><span data-stu-id="99418-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="99418-998">Jos tarvitset visuaalisen näkymän kustannuksen virrasta kustannusobjektien välillä, voit käyttää kustannuksen koontikäytäntösääntöjä kustannusvirran visualisointiin.</span><span class="sxs-lookup"><span data-stu-id="99418-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="99418-999">Lisätietoja on kohdassa Kustannusten koontikäytäntösäännöt.</span><span class="sxs-lookup"><span data-stu-id="99418-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="99418-1000">(Huomaa, että ohjeaihe ei ole vielä valmis; se on saatavilla pian.)</span><span class="sxs-lookup"><span data-stu-id="99418-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




