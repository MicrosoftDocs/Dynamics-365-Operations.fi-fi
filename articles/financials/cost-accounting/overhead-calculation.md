---
title: Yleiskustannuslaskenta
description: "Tässä aiheessa kuvataan tyypillinen yleiskustannusten laskenta- ja kohdistusprosessi."
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 12ae99c15bafcd9cc08b30903fe3f251f446b17d
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.contentlocale: fi-fi
ms.lasthandoff: 10/05/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="5dd94-103">Yleiskustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="5dd94-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5dd94-104">Tässä aiheessa kuvataan tyypillinen yleiskustannusten laskenta- ja kohdistusprosessi.</span><span class="sxs-lookup"><span data-stu-id="5dd94-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="5dd94-105">Sanaston määritelmä</span><span class="sxs-lookup"><span data-stu-id="5dd94-105">Term definition</span></span>
---------------

<span data-ttu-id="5dd94-106">Yleiskustannukset ovat yrityksen toiminnasta syntyviä kustannuksia, joita ei voi suoraan liittää mihinkään tiettyyn liiketoiminnan tehtävään, tuotteeseen tai palveluun.</span><span class="sxs-lookup"><span data-stu-id="5dd94-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="5dd94-107">Yleiskustannukset ovat tärkeä tuki voittoa tuottavien tehtävien luonnissa.</span><span class="sxs-lookup"><span data-stu-id="5dd94-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="5dd94-108">Seuraavassa on joitakin esimerkkejä yleiskustannuksista:</span><span class="sxs-lookup"><span data-stu-id="5dd94-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="5dd94-109">Vuokra</span><span class="sxs-lookup"><span data-stu-id="5dd94-109">Rent</span></span>
-   <span data-ttu-id="5dd94-110">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-110">Electricity</span></span>
-   <span data-ttu-id="5dd94-111">Hallinnon palkat</span><span class="sxs-lookup"><span data-stu-id="5dd94-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="5dd94-112">Yleiskustannuslaskennan yleiskuva</span><span class="sxs-lookup"><span data-stu-id="5dd94-112">Overhead calculation overview</span></span>
<span data-ttu-id="5dd94-113">Yleiskustannusten laskenta suorittaa kustannuslaskennan käytännöt oikeassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="5dd94-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="5dd94-114">Yleiskustannusten laskennan voi suorittaa useita kertoja samalle tilikaudelle, jos kustannuslaskennan käytännöt ovat muuttuneet tai erityisiä virheitä on havaittu.</span><span class="sxs-lookup"><span data-stu-id="5dd94-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="5dd94-115">Kukin laskenta-ajo tallennetaan ja kullekin annetaan yksilöllinen versiotunnus, jonka avulla eri laskenta-ajoja voi verrata toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="5dd94-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="5dd94-116">Yleiskustannusten laskenta luo kustannustapahtumia, joille annetaan kirjauspäivä.</span><span class="sxs-lookup"><span data-stu-id="5dd94-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="5dd94-117">Kirjauspäivä vastaa laskennassa käytettyä tilikauden päättymispäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="5dd94-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="5dd94-118">Yksilöivä versiotunnus sisältää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="5dd94-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="5dd94-119">Versiotyyppi</span><span class="sxs-lookup"><span data-stu-id="5dd94-119">Version type</span></span>
-   <span data-ttu-id="5dd94-120">Päivämäärä ja aika</span><span class="sxs-lookup"><span data-stu-id="5dd94-120">Date and time</span></span>
-   <span data-ttu-id="5dd94-121">Kustannuslaskennan kirjanpito</span><span class="sxs-lookup"><span data-stu-id="5dd94-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="5dd94-122">Tilikausi </span><span class="sxs-lookup"><span data-stu-id="5dd94-122">Fiscal year</span></span>
-   <span data-ttu-id="5dd94-123">Tilikausi  </span><span class="sxs-lookup"><span data-stu-id="5dd94-123">Fiscal period</span></span>

<span data-ttu-id="5dd94-124">Yleiskustannusten laskenta ajetaan versiosta riippumattomana.</span><span class="sxs-lookup"><span data-stu-id="5dd94-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="5dd94-125">Voit siis laskea budjetin version ennen todellista versiota.</span><span class="sxs-lookup"><span data-stu-id="5dd94-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="5dd94-126">Yleiskustannusten laskenta koostuu neljästä vaiheesta, jotka esitellään seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="5dd94-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="5dd94-127">Kussakin vaiheessa luodaan kirjauskansion otsikko, jolla on kirjauskansiovientejä.</span><span class="sxs-lookup"><span data-stu-id="5dd94-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="5dd94-128">Tämä kirjauskansion otsikko säilyttää kunkin laskentavaiheen syöttötiedot.</span><span class="sxs-lookup"><span data-stu-id="5dd94-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="5dd94-129">Käytännöt ja säännöt ajetaan kullekin kirjauskansion riville, ja tuloksena luodaan kustannustapahtumia.</span><span class="sxs-lookup"><span data-stu-id="5dd94-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="5dd94-130">Tämän ansiosta kaikki laskutoimitukset ovat täysin jäljitettävissä.</span><span class="sxs-lookup"><span data-stu-id="5dd94-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="5dd94-131">[![Yleiskustannuslaskenta](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="5dd94-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="5dd94-132">Laske ja kohdista sähkön yleiskustannukset</span><span class="sxs-lookup"><span data-stu-id="5dd94-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="5dd94-133">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="5dd94-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="5dd94-134">Tarkka johdon näkymä ei täten ole saatavilla kustannuslaskennassa.</span><span class="sxs-lookup"><span data-stu-id="5dd94-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="5dd94-135">Jotta kustannuslaskenta tarjoaisi oikean johdon näkymän kaikista organisaation yksiköistä ja tasoista, kustannusten on virrattava organisaation yksiköiden läpi.</span><span class="sxs-lookup"><span data-stu-id="5dd94-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="5dd94-136">Tämän virran on perustuttava joko tarkkaan tietoon kulutuksesta tai perusteltuun arvioon.</span><span class="sxs-lookup"><span data-stu-id="5dd94-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="5dd94-137">Sähkökustannukset voi kirjata kirjanpitoon seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="5dd94-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5dd94-138">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="5dd94-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5dd94-139">Kustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5dd94-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="5dd94-140">Päätili</span><span class="sxs-lookup"><span data-stu-id="5dd94-140">Main account</span></span></th>
<th><span data-ttu-id="5dd94-141">Summa kirjanpitovaluuttana</span><span class="sxs-lookup"><span data-stu-id="5dd94-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-142">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="5dd94-143">CC099</span><span class="sxs-lookup"><span data-stu-id="5dd94-143">CC099</span></span></td>
<td><span data-ttu-id="5dd94-144">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5dd94-144">Default cost center</span></span></td>
<td><span data-ttu-id="5dd94-145">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-145">10001</span></span></td>
<td><span data-ttu-id="5dd94-146">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-146">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="5dd94-148">Vaihe 1: Käsittele kustannustoiminnan laskenta</span><span class="sxs-lookup"><span data-stu-id="5dd94-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="5dd94-149">Kun kustannustapahtumat tuodaan lähdetiedoista, niille asetetaan kustannuslaskennassa oletusarvoisesti **Luokittelematon** -kustannustoimintaluokka.</span><span class="sxs-lookup"><span data-stu-id="5dd94-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="5dd94-150">Voit luokitella kustannustapahtumia uudelleen **kiinteäksi kustannukseksi** tai **muuttuvaksi kustannukseksi** kustannustoiminnan käytäntösäännöillä.</span><span class="sxs-lookup"><span data-stu-id="5dd94-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="5dd94-151">Määritä kustannustoiminnan sääntö</span><span class="sxs-lookup"><span data-stu-id="5dd94-151">Define the cost behavior rule</span></span>

<span data-ttu-id="5dd94-152">Joissain tapauksissa osa kustannuksesta on kiinteä ja loppuosa perustuu kulutukseen.</span><span class="sxs-lookup"><span data-stu-id="5dd94-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="5dd94-153">Sähkölaskut sopivat usein tähän määritelmään.</span><span class="sxs-lookup"><span data-stu-id="5dd94-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="5dd94-154">Maksat ensin määrätyn, kiinteän maksun, jonka lisäksi maksat kulutuksesta kilowattitunteina (kWh).</span><span class="sxs-lookup"><span data-stu-id="5dd94-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="5dd94-155">Jos kiinteä maksu on esimerkiksi 1 000,00, kustannustoiminnan sääntö määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="5dd94-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="5dd94-156">Kiinteä määrä 1 000,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="5dd94-157">0 &lt;= 1 000,00 = Kiinteä</span><span class="sxs-lookup"><span data-stu-id="5dd94-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="5dd94-158">1000,01 &lt; N = Muuttuva</span><span class="sxs-lookup"><span data-stu-id="5dd94-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="5dd94-159">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5dd94-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5dd94-160">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5dd94-160">Journal</span></span></th>
<th><span data-ttu-id="5dd94-161">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="5dd94-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5dd94-162">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="5dd94-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5dd94-163">Versio</span><span class="sxs-lookup"><span data-stu-id="5dd94-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-164">00001</span><span class="sxs-lookup"><span data-stu-id="5dd94-164">00001</span></span></td>
<td><span data-ttu-id="5dd94-165">Kustannustoiminnan laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5dd94-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="5dd94-166">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="5dd94-166">Fiscal</span></span></td>
<td><span data-ttu-id="5dd94-167">2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-167">2017</span></span></td>
<td><span data-ttu-id="5dd94-168">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-168">Period 1</span></span></td>
<td><span data-ttu-id="5dd94-169">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5dd94-170">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="5dd94-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5dd94-171">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="5dd94-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5dd94-172">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5dd94-173">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="5dd94-173">Cost element</span></span></th>
<th><span data-ttu-id="5dd94-174">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5dd94-174">Cost behavior</span></span></th>
<th><span data-ttu-id="5dd94-175">Summa</span><span class="sxs-lookup"><span data-stu-id="5dd94-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-176">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="5dd94-177">CC099</span><span class="sxs-lookup"><span data-stu-id="5dd94-177">CC099</span></span></td>
<td><span data-ttu-id="5dd94-178">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5dd94-178">Default cost center</span></span></td>
<td><span data-ttu-id="5dd94-179">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-179">10001</span></span></td>
<td><span data-ttu-id="5dd94-180">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-180">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-181">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="5dd94-181">Unclassified</span></span></td>
<td><span data-ttu-id="5dd94-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5dd94-183">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="5dd94-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5dd94-184">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5dd94-185">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="5dd94-185">Cost element</span></span></th>
<th><span data-ttu-id="5dd94-186">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5dd94-186">Cost behavior</span></span></th>
<th><span data-ttu-id="5dd94-187">Summa</span><span class="sxs-lookup"><span data-stu-id="5dd94-187">Amount</span></span></th>
<th><span data-ttu-id="5dd94-188">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="5dd94-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-189">CC099</span><span class="sxs-lookup"><span data-stu-id="5dd94-189">CC099</span></span></td>
<td><span data-ttu-id="5dd94-190">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5dd94-190">Default cost center</span></span></td>
<td><span data-ttu-id="5dd94-191">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-191">10001</span></span></td>
<td><span data-ttu-id="5dd94-192">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-192">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-193">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="5dd94-193">Unclassified</span></span></td>
<td><span data-ttu-id="5dd94-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-194">10,000.00</span></span></td>
<td><span data-ttu-id="5dd94-195">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-196">CC099</span><span class="sxs-lookup"><span data-stu-id="5dd94-196">CC099</span></span></td>
<td><span data-ttu-id="5dd94-197">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5dd94-197">Default cost center</span></span></td>
<td><span data-ttu-id="5dd94-198">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-198">10001</span></span></td>
<td><span data-ttu-id="5dd94-199">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-199">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-200">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="5dd94-200">Unclassified</span></span></td>
<td><span data-ttu-id="5dd94-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-201">-10,000.00</span></span></td>
<td><span data-ttu-id="5dd94-202">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-203">CC099</span><span class="sxs-lookup"><span data-stu-id="5dd94-203">CC099</span></span></td>
<td><span data-ttu-id="5dd94-204">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5dd94-204">Default cost center</span></span></td>
<td><span data-ttu-id="5dd94-205">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-205">10001</span></span></td>
<td><span data-ttu-id="5dd94-206">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-206">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-207">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-207">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-208">1,000.00</span></span></td>
<td><span data-ttu-id="5dd94-209">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-210">CC099</span><span class="sxs-lookup"><span data-stu-id="5dd94-210">CC099</span></span></td>
<td><span data-ttu-id="5dd94-211">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5dd94-211">Default cost center</span></span></td>
<td><span data-ttu-id="5dd94-212">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-212">10001</span></span></td>
<td><span data-ttu-id="5dd94-213">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-213">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-214">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-214">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="5dd94-215">9,000.00</span></span></td>
<td><span data-ttu-id="5dd94-216">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5dd94-217">Lisätietoja on kohdassa [Kustannustoimintakäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="5dd94-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="5dd94-218">Vaihe 2: Käsittele kustannusten jaon laskenta</span><span class="sxs-lookup"><span data-stu-id="5dd94-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="5dd94-219">Kustannusten jakoa käytetään kustannusten jakamiseen yhdestä kustannusobjektista toiseen (tai useampaan kustannusobjektiin) määrittämällä asiaankuuluvan kohdistusperusteen.</span><span class="sxs-lookup"><span data-stu-id="5dd94-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="5dd94-220">Kustannusten jako ja kustannusten kohdistus eroavat toisistaan sillä, että kustannusten jako tapahtuu aina alkuperäisen kustannuksen ensisijaisen kustannuselementin tasolla.</span><span class="sxs-lookup"><span data-stu-id="5dd94-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="5dd94-221">Määritä kustannusten jaon sääntö</span><span class="sxs-lookup"><span data-stu-id="5dd94-221">Define the cost distribution rule</span></span>

<span data-ttu-id="5dd94-222">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="5dd94-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="5dd94-223">Kustannuslaskenta ei tarjoa tästä tarpeeksi tarkkoja tietoja.</span><span class="sxs-lookup"><span data-stu-id="5dd94-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="5dd94-224">Muuttuva kustannus tulisi jakaa yksittäisille kustannusobjekteille reiluin perustein.</span><span class="sxs-lookup"><span data-stu-id="5dd94-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="5dd94-225">Loogisin kohdistusperuste on sähkönkulutus (kWh).</span><span class="sxs-lookup"><span data-stu-id="5dd94-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="5dd94-226">Luodaan tilastollinen dimensionjäsen nimeltä Sähkö, johon kirjataan sähkönkulutus.</span><span class="sxs-lookup"><span data-stu-id="5dd94-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="5dd94-227">Oletusarvon mukaan kaikki tilastolliset dimensiojäsenet ovat käytettävissä kohdistusperusteina.</span><span class="sxs-lookup"><span data-stu-id="5dd94-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5dd94-228">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-228">Cost object</span></span></th>
<th><span data-ttu-id="5dd94-229">kWh</span><span class="sxs-lookup"><span data-stu-id="5dd94-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-230">CC001</span><span class="sxs-lookup"><span data-stu-id="5dd94-230">CC001</span></span></td>
<td><span data-ttu-id="5dd94-231">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5dd94-231">HR</span></span></td>
<td><span data-ttu-id="5dd94-232">1 000</span><span class="sxs-lookup"><span data-stu-id="5dd94-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-233">CC002</span><span class="sxs-lookup"><span data-stu-id="5dd94-233">CC002</span></span></td>
<td><span data-ttu-id="5dd94-234">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5dd94-234">Finance</span></span></td>
<td><span data-ttu-id="5dd94-235">6,000</span><span class="sxs-lookup"><span data-stu-id="5dd94-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-236">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-236">CC003</span></span></td>
<td><span data-ttu-id="5dd94-237">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5dd94-237">Assembly</span></span></td>
<td><span data-ttu-id="5dd94-238">0</span><span class="sxs-lookup"><span data-stu-id="5dd94-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5dd94-239">Seuraavassa taulukossa on esitetty tulos, kun sähkönkulutusta käytetään kohdistusperusteena muuttuville kuluille.</span><span class="sxs-lookup"><span data-stu-id="5dd94-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5dd94-240">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-240">Cost object</span></span></th>
<th><span data-ttu-id="5dd94-241">Suuruus</span><span class="sxs-lookup"><span data-stu-id="5dd94-241">Magnitude</span></span></th>
<th><span data-ttu-id="5dd94-242">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="5dd94-242">Allocation factor</span></span></th>
<th><span data-ttu-id="5dd94-243">Summa</span><span class="sxs-lookup"><span data-stu-id="5dd94-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-244">CC001</span><span class="sxs-lookup"><span data-stu-id="5dd94-244">CC001</span></span></td>
<td><span data-ttu-id="5dd94-245">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5dd94-245">HR</span></span></td>
<td><span data-ttu-id="5dd94-246">1 000</span><span class="sxs-lookup"><span data-stu-id="5dd94-246">1,000</span></span></td>
<td><span data-ttu-id="5dd94-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5dd94-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="5dd94-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-249">CC002</span><span class="sxs-lookup"><span data-stu-id="5dd94-249">CC002</span></span></td>
<td><span data-ttu-id="5dd94-250">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5dd94-250">Finance</span></span></td>
<td><span data-ttu-id="5dd94-251">6,000</span><span class="sxs-lookup"><span data-stu-id="5dd94-251">6,000</span></span></td>
<td><span data-ttu-id="5dd94-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5dd94-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="5dd94-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-254">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-254">CC003</span></span></td>
<td><span data-ttu-id="5dd94-255">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5dd94-255">Assembly</span></span></td>
<td><span data-ttu-id="5dd94-256">0</span><span class="sxs-lookup"><span data-stu-id="5dd94-256">0</span></span></td>
<td><span data-ttu-id="5dd94-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5dd94-258">0,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5dd94-259">Kiinteä kustannus tulisi jakaa tasaisesti yksittäisille kustannusobjekteille, jotka ovat kuluttaneet sähköä.</span><span class="sxs-lookup"><span data-stu-id="5dd94-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="5dd94-260">Voit käyttää sähkön tilastollista dimensiojäsentä kaavan kohdistusperusteena tämän tavoitteen saavuttamiseksi: (sähkö &gt;0,00) Seuraavassa taulukossa on esitetty tulos siitä, kun sähkönkulutus on määritetty muuttuvien kustannusten kohdistusperusteeksi.</span><span class="sxs-lookup"><span data-stu-id="5dd94-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5dd94-261">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-261">Cost object</span></span></th>
<th><span data-ttu-id="5dd94-262">Resepti</span><span class="sxs-lookup"><span data-stu-id="5dd94-262">Formula</span></span></th>
<th><span data-ttu-id="5dd94-263">Suuruus</span><span class="sxs-lookup"><span data-stu-id="5dd94-263">Magnitude</span></span></th>
<th><span data-ttu-id="5dd94-264">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="5dd94-264">Allocation factor</span></span></th>
<th><span data-ttu-id="5dd94-265">Summa</span><span class="sxs-lookup"><span data-stu-id="5dd94-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-266">CC001</span><span class="sxs-lookup"><span data-stu-id="5dd94-266">CC001</span></span></td>
<td><span data-ttu-id="5dd94-267">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5dd94-267">HR</span></span></td>
<td><span data-ttu-id="5dd94-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="5dd94-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5dd94-269">1</span><span class="sxs-lookup"><span data-stu-id="5dd94-269">1</span></span></td>
<td><span data-ttu-id="5dd94-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5dd94-271">500,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-272">CC002</span><span class="sxs-lookup"><span data-stu-id="5dd94-272">CC002</span></span></td>
<td><span data-ttu-id="5dd94-273">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5dd94-273">Finance</span></span></td>
<td><span data-ttu-id="5dd94-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="5dd94-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5dd94-275">1</span><span class="sxs-lookup"><span data-stu-id="5dd94-275">1</span></span></td>
<td><span data-ttu-id="5dd94-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5dd94-277">500,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-278">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-278">CC003</span></span></td>
<td><span data-ttu-id="5dd94-279">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5dd94-279">Assembly</span></span></td>
<td><span data-ttu-id="5dd94-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="5dd94-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5dd94-281">0</span><span class="sxs-lookup"><span data-stu-id="5dd94-281">0</span></span></td>
<td><span data-ttu-id="5dd94-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5dd94-283">0,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="5dd94-284">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5dd94-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5dd94-285">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5dd94-285">Journal</span></span></th>
<th><span data-ttu-id="5dd94-286">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="5dd94-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5dd94-287">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="5dd94-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5dd94-288">Versio</span><span class="sxs-lookup"><span data-stu-id="5dd94-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-289">00002</span><span class="sxs-lookup"><span data-stu-id="5dd94-289">00002</span></span></td>
<td><span data-ttu-id="5dd94-290">Kustannusten jaon laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5dd94-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="5dd94-291">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="5dd94-291">Fiscal</span></span></td>
<td><span data-ttu-id="5dd94-292">2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-292">2017</span></span></td>
<td><span data-ttu-id="5dd94-293">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-293">Period 1</span></span></td>
<td><span data-ttu-id="5dd94-294">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5dd94-295">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="5dd94-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5dd94-296">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="5dd94-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5dd94-297">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5dd94-298">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="5dd94-298">Cost element</span></span></th>
<th><span data-ttu-id="5dd94-299">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5dd94-299">Cost behavior</span></span></th>
<th><span data-ttu-id="5dd94-300">Summa</span><span class="sxs-lookup"><span data-stu-id="5dd94-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-301">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="5dd94-302">CC099</span><span class="sxs-lookup"><span data-stu-id="5dd94-302">CC099</span></span></td>
<td><span data-ttu-id="5dd94-303">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5dd94-303">Default cost center</span></span></td>
<td><span data-ttu-id="5dd94-304">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-304">10001</span></span></td>
<td><span data-ttu-id="5dd94-305">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-305">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-306">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-306">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-308">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="5dd94-309">CC099</span><span class="sxs-lookup"><span data-stu-id="5dd94-309">CC099</span></span></td>
<td><span data-ttu-id="5dd94-310">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5dd94-310">Default cost center</span></span></td>
<td><span data-ttu-id="5dd94-311">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-311">10001</span></span></td>
<td><span data-ttu-id="5dd94-312">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-312">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-313">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-313">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="5dd94-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5dd94-315">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="5dd94-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5dd94-316">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5dd94-317">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="5dd94-317">Cost element</span></span></th>
<th><span data-ttu-id="5dd94-318">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5dd94-318">Cost behavior</span></span></th>
<th><span data-ttu-id="5dd94-319">Summa</span><span class="sxs-lookup"><span data-stu-id="5dd94-319">Amount</span></span></th>
<th><span data-ttu-id="5dd94-320">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="5dd94-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-321">CC099</span><span class="sxs-lookup"><span data-stu-id="5dd94-321">CC099</span></span></td>
<td><span data-ttu-id="5dd94-322">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5dd94-322">Default cost center</span></span></td>
<td><span data-ttu-id="5dd94-323">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-323">10001</span></span></td>
<td><span data-ttu-id="5dd94-324">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-324">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-325">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-325">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-326">-1,000.00</span></span></td>
<td><span data-ttu-id="5dd94-327">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-328">CC001</span><span class="sxs-lookup"><span data-stu-id="5dd94-328">CC001</span></span></td>
<td><span data-ttu-id="5dd94-329">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5dd94-329">HR</span></span></td>
<td><span data-ttu-id="5dd94-330">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-330">10001</span></span></td>
<td><span data-ttu-id="5dd94-331">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-331">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-332">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-332">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-333">500,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-333">500.00</span></span></td>
<td><span data-ttu-id="5dd94-334">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-335">CC002</span><span class="sxs-lookup"><span data-stu-id="5dd94-335">CC002</span></span></td>
<td><span data-ttu-id="5dd94-336">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5dd94-336">Finance</span></span></td>
<td><span data-ttu-id="5dd94-337">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-337">10001</span></span></td>
<td><span data-ttu-id="5dd94-338">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-338">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-339">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-339">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-340">500,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-340">500.00</span></span></td>
<td><span data-ttu-id="5dd94-341">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-342">CC099</span><span class="sxs-lookup"><span data-stu-id="5dd94-342">CC099</span></span></td>
<td><span data-ttu-id="5dd94-343">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="5dd94-343">Default cost center</span></span></td>
<td><span data-ttu-id="5dd94-344">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-344">10001</span></span></td>
<td><span data-ttu-id="5dd94-345">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-345">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-346">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-346">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-347">-9,000.00</span></span></td>
<td><span data-ttu-id="5dd94-348">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-349">CC001</span><span class="sxs-lookup"><span data-stu-id="5dd94-349">CC001</span></span></td>
<td><span data-ttu-id="5dd94-350">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5dd94-350">HR</span></span></td>
<td><span data-ttu-id="5dd94-351">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-351">10001</span></span></td>
<td><span data-ttu-id="5dd94-352">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-352">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-353">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-353">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="5dd94-354">1,285.71</span></span></td>
<td><span data-ttu-id="5dd94-355">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-356">CC002</span><span class="sxs-lookup"><span data-stu-id="5dd94-356">CC002</span></span></td>
<td><span data-ttu-id="5dd94-357">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5dd94-357">Finance</span></span></td>
<td><span data-ttu-id="5dd94-358">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-358">10001</span></span></td>
<td><span data-ttu-id="5dd94-359">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-359">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-360">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-360">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="5dd94-361">7,714.29</span></span></td>
<td><span data-ttu-id="5dd94-362">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5dd94-363">Lisätietoja on kohdassa [Jakelukäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="5dd94-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="5dd94-364">Vaihe 3: Käsittele yleiskustannustason laskenta</span><span class="sxs-lookup"><span data-stu-id="5dd94-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="5dd94-365">Yleiskustannustasolla veloitetaan yksi tai useampi määrätty kustannusobjekti.</span><span class="sxs-lookup"><span data-stu-id="5dd94-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="5dd94-366">Veloitus perustuu ennalta määrättyyn kustannustasoon sekä määritetyn kohdistusperusteen suuruuteen.</span><span class="sxs-lookup"><span data-stu-id="5dd94-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="5dd94-367">Määritä yleiskustannustaso.</span><span class="sxs-lookup"><span data-stu-id="5dd94-367">Define the overhead rate</span></span>

<span data-ttu-id="5dd94-368">Kustannusobjekti CC001 HR vaikuttaa joukkoon sisäisiä projekteja.</span><span class="sxs-lookup"><span data-stu-id="5dd94-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="5dd94-369">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon projektit.</span><span class="sxs-lookup"><span data-stu-id="5dd94-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5dd94-370">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-370">Cost object</span></span></th>
<th><span data-ttu-id="5dd94-371">Tunnit</span><span class="sxs-lookup"><span data-stu-id="5dd94-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-372">Proj 1</span></span></td>
<td><span data-ttu-id="5dd94-373">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-373">Project 1</span></span></td>
<td><span data-ttu-id="5dd94-374">3</span><span class="sxs-lookup"><span data-stu-id="5dd94-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-375">Proj 2</span></span></td>
<td><span data-ttu-id="5dd94-376">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-376">Project 2</span></span></td>
<td><span data-ttu-id="5dd94-377">1</span><span class="sxs-lookup"><span data-stu-id="5dd94-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5dd94-378">Kustannusprojektien osuudelle on määritetty ennalta kustannushinta.</span><span class="sxs-lookup"><span data-stu-id="5dd94-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5dd94-379">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-379">Cost object</span></span></th>
<th><span data-ttu-id="5dd94-380">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="5dd94-380">Cost element</span></span></th>
<th><span data-ttu-id="5dd94-381">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5dd94-381">Cost behavior</span></span></th>
<th><span data-ttu-id="5dd94-382">Yksiköt</span><span class="sxs-lookup"><span data-stu-id="5dd94-382">Units</span></span></th>
<th><span data-ttu-id="5dd94-383">Osuus</span><span class="sxs-lookup"><span data-stu-id="5dd94-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-384">CC001</span><span class="sxs-lookup"><span data-stu-id="5dd94-384">CC001</span></span></td>
<td><span data-ttu-id="5dd94-385">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5dd94-385">HR</span></span></td>
<td><span data-ttu-id="5dd94-386">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-386">10001</span></span></td>
<td><span data-ttu-id="5dd94-387">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-387">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-388">1</span><span class="sxs-lookup"><span data-stu-id="5dd94-388">1</span></span></td>
<td><span data-ttu-id="5dd94-389">10</span><span class="sxs-lookup"><span data-stu-id="5dd94-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5dd94-390">Seuraavassa taulukossa on esitetty tulos, kun Henkilöstöhallinnon projekteja käytetään kohdistusperusteena.</span><span class="sxs-lookup"><span data-stu-id="5dd94-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5dd94-391">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-391">Cost object</span></span></th>
<th><span data-ttu-id="5dd94-392">Suuruus</span><span class="sxs-lookup"><span data-stu-id="5dd94-392">Magnitude</span></span></th>
<th><span data-ttu-id="5dd94-393">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="5dd94-393">Cost element</span></span></th>
<th><span data-ttu-id="5dd94-394">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="5dd94-394">Allocation factor</span></span></th>
<th><span data-ttu-id="5dd94-395">Summa</span><span class="sxs-lookup"><span data-stu-id="5dd94-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-396">Proj 1</span></span></td>
<td><span data-ttu-id="5dd94-397">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-397">Project 1</span></span></td>
<td><span data-ttu-id="5dd94-398">3</span><span class="sxs-lookup"><span data-stu-id="5dd94-398">3</span></span></td>
<td><span data-ttu-id="5dd94-399">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-399">10001</span></span></td>
<td><span data-ttu-id="5dd94-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="5dd94-401">30,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-402">Proj 2</span></span></td>
<td><span data-ttu-id="5dd94-403">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-403">Project 2</span></span></td>
<td><span data-ttu-id="5dd94-404">1</span><span class="sxs-lookup"><span data-stu-id="5dd94-404">1</span></span></td>
<td><span data-ttu-id="5dd94-405">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-405">10001</span></span></td>
<td><span data-ttu-id="5dd94-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="5dd94-407">10,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="5dd94-408">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5dd94-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5dd94-409">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5dd94-409">Journal</span></span></th>
<th><span data-ttu-id="5dd94-410">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="5dd94-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5dd94-411">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="5dd94-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5dd94-412">Versio</span><span class="sxs-lookup"><span data-stu-id="5dd94-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-413">00003</span><span class="sxs-lookup"><span data-stu-id="5dd94-413">00003</span></span></td>
<td><span data-ttu-id="5dd94-414">Yleiskustannustason laskelman kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5dd94-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="5dd94-415">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="5dd94-415">Fiscal</span></span></td>
<td><span data-ttu-id="5dd94-416">2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-416">2017</span></span></td>
<td><span data-ttu-id="5dd94-417">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-417">Period 1</span></span></td>
<td><span data-ttu-id="5dd94-418">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="5dd94-419">Kirjauskansioviennit (Yleiskustannustason laskennan kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="5dd94-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5dd94-420">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="5dd94-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5dd94-421">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-421">Cost object</span></span></th>
<th><span data-ttu-id="5dd94-422">Suuruus</span><span class="sxs-lookup"><span data-stu-id="5dd94-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-423">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="5dd94-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-424">Proj 1</span></span></td>
<td><span data-ttu-id="5dd94-425">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="5dd94-426">3,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-427">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="5dd94-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-428">Proj 2</span></span></td>
<td><span data-ttu-id="5dd94-429">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="5dd94-430">1,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5dd94-431">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="5dd94-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5dd94-432">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5dd94-433">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="5dd94-433">Cost element</span></span></th>
<th><span data-ttu-id="5dd94-434">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5dd94-434">Cost behavior</span></span></th>
<th><span data-ttu-id="5dd94-435">Summa</span><span class="sxs-lookup"><span data-stu-id="5dd94-435">Amount</span></span></th>
<th><span data-ttu-id="5dd94-436">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="5dd94-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="5dd94-437">CC0001</span></span></td>
<td><span data-ttu-id="5dd94-438">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5dd94-438">HR</span></span></td>
<td><span data-ttu-id="5dd94-439">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-439">10001</span></span></td>
<td><span data-ttu-id="5dd94-440">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-440">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-441">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-441">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-442">-30.00</span></span></td>
<td><span data-ttu-id="5dd94-443">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-444">Proj 1</span></span></td>
<td><span data-ttu-id="5dd94-445">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="5dd94-446">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-446">10001</span></span></td>
<td><span data-ttu-id="5dd94-447">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-447">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-448">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-448">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-449">30,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-449">30.00</span></span></td>
<td><span data-ttu-id="5dd94-450">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-451">CC001</span><span class="sxs-lookup"><span data-stu-id="5dd94-451">CC001</span></span></td>
<td><span data-ttu-id="5dd94-452">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5dd94-452">HR</span></span></td>
<td><span data-ttu-id="5dd94-453">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-453">10001</span></span></td>
<td><span data-ttu-id="5dd94-454">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-454">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-455">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-455">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-456">-10.00</span></span></td>
<td><span data-ttu-id="5dd94-457">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-458">Proj 2</span></span></td>
<td><span data-ttu-id="5dd94-459">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="5dd94-460">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-460">10001</span></span></td>
<td><span data-ttu-id="5dd94-461">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-461">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-462">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-462">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-463">10.00</span><span class="sxs-lookup"><span data-stu-id="5dd94-463">10.00</span></span></td>
<td><span data-ttu-id="5dd94-464">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5dd94-465">Lisätietoja on kohdassa [Yleisen laskennan suorittaminen](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="5dd94-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="5dd94-466">Vaihe 4: Käsittele kustannusten kohdistuksen laskenta</span><span class="sxs-lookup"><span data-stu-id="5dd94-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="5dd94-467">Kohdistuksella kustannusobjektin saldo liitetään toisiin kustannusobjekteihin käyttämällä kohdistusperustetta.</span><span class="sxs-lookup"><span data-stu-id="5dd94-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="5dd94-468">Finance and Operations tukee vastavuoroista kohdistusmenetelmää.</span><span class="sxs-lookup"><span data-stu-id="5dd94-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="5dd94-469">Vastavuoroisessa kohdistusmenetelmässä tunnistetaan oheiskustannusobjektien käyttämät, keskinäiset palvelut täysin.</span><span class="sxs-lookup"><span data-stu-id="5dd94-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="5dd94-470">Järjestelmä määrittää oikean kohdistusjärjestyksen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="5dd94-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="5dd94-471">Kustannusobjektin saldo kohdistetaan yhdellä kohdistusperusteella.</span><span class="sxs-lookup"><span data-stu-id="5dd94-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="5dd94-472">Kustannusobjektien dimensiot ja niiden vastaavat jäsenet ylittävät kohdistukset ovat tuettuja.</span><span class="sxs-lookup"><span data-stu-id="5dd94-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="5dd94-473">Kustannusseurantayksikkö hallitsee kohdistusjärjestystä.</span><span class="sxs-lookup"><span data-stu-id="5dd94-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="5dd94-474">[![Vastavuoroinen menetelmä](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="5dd94-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="5dd94-475">Määritä kustannuksen kohdistus</span><span class="sxs-lookup"><span data-stu-id="5dd94-475">Define the cost allocation</span></span>

<span data-ttu-id="5dd94-476">Tämä on yksinkertainen esimerkki, jossa kerrotaan, miten voit jäljittää kustannuksen virran.</span><span class="sxs-lookup"><span data-stu-id="5dd94-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="5dd94-477">Kustannusobjekti CC001 HR liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="5dd94-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="5dd94-478">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="5dd94-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5dd94-479">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-479">Cost object</span></span></th>
<th><span data-ttu-id="5dd94-480">HR-palvelut</span><span class="sxs-lookup"><span data-stu-id="5dd94-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-481">CC002</span><span class="sxs-lookup"><span data-stu-id="5dd94-481">CC002</span></span></td>
<td><span data-ttu-id="5dd94-482">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5dd94-482">Finance</span></span></td>
<td><span data-ttu-id="5dd94-483">35</span><span class="sxs-lookup"><span data-stu-id="5dd94-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-484">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-484">CC003</span></span></td>
<td><span data-ttu-id="5dd94-485">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5dd94-485">Assembly</span></span></td>
<td><span data-ttu-id="5dd94-486">55</span><span class="sxs-lookup"><span data-stu-id="5dd94-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-487">CC004</span><span class="sxs-lookup"><span data-stu-id="5dd94-487">CC004</span></span></td>
<td><span data-ttu-id="5dd94-488">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5dd94-488">Packaging</span></span></td>
<td><span data-ttu-id="5dd94-489">10</span><span class="sxs-lookup"><span data-stu-id="5dd94-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5dd94-490">Kustannusobjekti CC002 Taloushallinto liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="5dd94-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="5dd94-491">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Taloushallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="5dd94-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5dd94-492">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-492">Cost object</span></span></th>
<th><span data-ttu-id="5dd94-493">Taloushallinnon palvelut</span><span class="sxs-lookup"><span data-stu-id="5dd94-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-494">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-494">CC003</span></span></td>
<td><span data-ttu-id="5dd94-495">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5dd94-495">Assembly</span></span></td>
<td><span data-ttu-id="5dd94-496">65</span><span class="sxs-lookup"><span data-stu-id="5dd94-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-497">CC004</span><span class="sxs-lookup"><span data-stu-id="5dd94-497">CC004</span></span></td>
<td><span data-ttu-id="5dd94-498">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5dd94-498">Packaging</span></span></td>
<td><span data-ttu-id="5dd94-499">35</span><span class="sxs-lookup"><span data-stu-id="5dd94-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5dd94-500">Kustannusobjekti CC003 Kokoonpano liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="5dd94-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="5dd94-501">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Kokoonpanopalvelut.</span><span class="sxs-lookup"><span data-stu-id="5dd94-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5dd94-502">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-502">Cost object</span></span></th>
<th><span data-ttu-id="5dd94-503">Kokoonpanopalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="5dd94-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-504">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-504">Prod 1</span></span></td>
<td><span data-ttu-id="5dd94-505">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-505">Product 1</span></span></td>
<td><span data-ttu-id="5dd94-506">60</span><span class="sxs-lookup"><span data-stu-id="5dd94-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-507">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-507">Prod 2</span></span></td>
<td><span data-ttu-id="5dd94-508">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-508">Product 2</span></span></td>
<td><span data-ttu-id="5dd94-509">20</span><span class="sxs-lookup"><span data-stu-id="5dd94-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5dd94-510">Kustannusobjekti CC004 Pakkaus liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="5dd94-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="5dd94-511">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Pakkauspalvelut.</span><span class="sxs-lookup"><span data-stu-id="5dd94-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5dd94-512">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-512">Cost object</span></span></th>
<th><span data-ttu-id="5dd94-513">Pakkauspalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="5dd94-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-514">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-514">Prod 1</span></span></td>
<td><span data-ttu-id="5dd94-515">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-515">Product 1</span></span></td>
<td><span data-ttu-id="5dd94-516">80</span><span class="sxs-lookup"><span data-stu-id="5dd94-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-517">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-517">Prod 2</span></span></td>
<td><span data-ttu-id="5dd94-518">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-518">Product 2</span></span></td>
<td><span data-ttu-id="5dd94-519">päivänä</span><span class="sxs-lookup"><span data-stu-id="5dd94-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5dd94-520">Finance and Operationsissa tilastomittaukset, kuten tämän tuotteen kuluttamat tuotantotunnit, voidaan johtaa lähdetiedoista.</span><span class="sxs-lookup"><span data-stu-id="5dd94-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="5dd94-521">Lisätietoja on kohdassa [Tilastomittauksen lähdemalli](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="5dd94-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="5dd94-522">Seuraavassa taulukossa näytetään tulos, kun henkilöstöhallinnon palveluja käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="5dd94-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5dd94-523">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-523">Cost object</span></span></th>
<th><span data-ttu-id="5dd94-524">Suuruus</span><span class="sxs-lookup"><span data-stu-id="5dd94-524">Magnitude</span></span></th>
<th><span data-ttu-id="5dd94-525">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="5dd94-525">Allocation factor</span></span></th>
<th><span data-ttu-id="5dd94-526">Summa</span><span class="sxs-lookup"><span data-stu-id="5dd94-526">Amount</span></span></th>
<th><span data-ttu-id="5dd94-527">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5dd94-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-528">CC002</span><span class="sxs-lookup"><span data-stu-id="5dd94-528">CC002</span></span></td>
<td><span data-ttu-id="5dd94-529">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5dd94-529">Finance</span></span></td>
<td><span data-ttu-id="5dd94-530">35</span><span class="sxs-lookup"><span data-stu-id="5dd94-530">35</span></span></td>
<td><span data-ttu-id="5dd94-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5dd94-532">175.00</span><span class="sxs-lookup"><span data-stu-id="5dd94-532">175.00</span></span></td>
<td><span data-ttu-id="5dd94-533">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-534">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-534">CC003</span></span></td>
<td><span data-ttu-id="5dd94-535">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5dd94-535">Assembly</span></span></td>
<td><span data-ttu-id="5dd94-536">55</span><span class="sxs-lookup"><span data-stu-id="5dd94-536">55</span></span></td>
<td><span data-ttu-id="5dd94-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5dd94-538">275.00</span><span class="sxs-lookup"><span data-stu-id="5dd94-538">275.00</span></span></td>
<td><span data-ttu-id="5dd94-539">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-540">CC004</span><span class="sxs-lookup"><span data-stu-id="5dd94-540">CC004</span></span></td>
<td><span data-ttu-id="5dd94-541">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5dd94-541">Packaging</span></span></td>
<td><span data-ttu-id="5dd94-542">10</span><span class="sxs-lookup"><span data-stu-id="5dd94-542">10</span></span></td>
<td><span data-ttu-id="5dd94-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5dd94-544">50,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-544">50.00</span></span></td>
<td><span data-ttu-id="5dd94-545">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-546">CC002</span><span class="sxs-lookup"><span data-stu-id="5dd94-546">CC002</span></span></td>
<td><span data-ttu-id="5dd94-547">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5dd94-547">Finance</span></span></td>
<td><span data-ttu-id="5dd94-548">35</span><span class="sxs-lookup"><span data-stu-id="5dd94-548">35</span></span></td>
<td><span data-ttu-id="5dd94-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="5dd94-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5dd94-550">436.00</span><span class="sxs-lookup"><span data-stu-id="5dd94-550">436.00</span></span></td>
<td><span data-ttu-id="5dd94-551">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-552">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-552">CC003</span></span></td>
<td><span data-ttu-id="5dd94-553">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5dd94-553">Assembly</span></span></td>
<td><span data-ttu-id="5dd94-554">55</span><span class="sxs-lookup"><span data-stu-id="5dd94-554">55</span></span></td>
<td><span data-ttu-id="5dd94-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="5dd94-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5dd94-556">685.14</span><span class="sxs-lookup"><span data-stu-id="5dd94-556">685.14</span></span></td>
<td><span data-ttu-id="5dd94-557">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-558">CC004</span><span class="sxs-lookup"><span data-stu-id="5dd94-558">CC004</span></span></td>
<td><span data-ttu-id="5dd94-559">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5dd94-559">Packaging</span></span></td>
<td><span data-ttu-id="5dd94-560">10</span><span class="sxs-lookup"><span data-stu-id="5dd94-560">10</span></span></td>
<td><span data-ttu-id="5dd94-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="5dd94-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5dd94-562">124.57</span><span class="sxs-lookup"><span data-stu-id="5dd94-562">124.57</span></span></td>
<td><span data-ttu-id="5dd94-563">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5dd94-564">Seuraavassa taulukossa näytetään tulos, kun Taloushallinnon palveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="5dd94-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5dd94-565">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-565">Cost object</span></span></th>
<th><span data-ttu-id="5dd94-566">Suuruus</span><span class="sxs-lookup"><span data-stu-id="5dd94-566">Magnitude</span></span></th>
<th><span data-ttu-id="5dd94-567">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="5dd94-567">Allocation factor</span></span></th>
<th><span data-ttu-id="5dd94-568">Summa</span><span class="sxs-lookup"><span data-stu-id="5dd94-568">Amount</span></span></th>
<th><span data-ttu-id="5dd94-569">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5dd94-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-570">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-570">CC003</span></span></td>
<td><span data-ttu-id="5dd94-571">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5dd94-571">Assembly</span></span></td>
<td><span data-ttu-id="5dd94-572">65</span><span class="sxs-lookup"><span data-stu-id="5dd94-572">65</span></span></td>
<td><span data-ttu-id="5dd94-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="5dd94-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="5dd94-574">438.75</span><span class="sxs-lookup"><span data-stu-id="5dd94-574">438.75</span></span></td>
<td><span data-ttu-id="5dd94-575">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-576">CC004</span><span class="sxs-lookup"><span data-stu-id="5dd94-576">CC004</span></span></td>
<td><span data-ttu-id="5dd94-577">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5dd94-577">Packaging</span></span></td>
<td><span data-ttu-id="5dd94-578">35</span><span class="sxs-lookup"><span data-stu-id="5dd94-578">35</span></span></td>
<td><span data-ttu-id="5dd94-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="5dd94-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="5dd94-580">236.25</span><span class="sxs-lookup"><span data-stu-id="5dd94-580">236.25</span></span></td>
<td><span data-ttu-id="5dd94-581">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-582">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-582">CC003</span></span></td>
<td><span data-ttu-id="5dd94-583">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5dd94-583">Assembly</span></span></td>
<td><span data-ttu-id="5dd94-584">65</span><span class="sxs-lookup"><span data-stu-id="5dd94-584">65</span></span></td>
<td><span data-ttu-id="5dd94-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="5dd94-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="5dd94-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="5dd94-586">5,297.69</span></span></td>
<td><span data-ttu-id="5dd94-587">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-588">CC004</span><span class="sxs-lookup"><span data-stu-id="5dd94-588">CC004</span></span></td>
<td><span data-ttu-id="5dd94-589">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5dd94-589">Packaging</span></span></td>
<td><span data-ttu-id="5dd94-590">35</span><span class="sxs-lookup"><span data-stu-id="5dd94-590">35</span></span></td>
<td><span data-ttu-id="5dd94-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="5dd94-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="5dd94-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="5dd94-592">2,852.60</span></span></td>
<td><span data-ttu-id="5dd94-593">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5dd94-594">Seuraavassa taulukossa näytetään tulos, kun Kokoonpanopalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="5dd94-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5dd94-595">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-595">Cost object</span></span></th>
<th><span data-ttu-id="5dd94-596">Suuruus</span><span class="sxs-lookup"><span data-stu-id="5dd94-596">Magnitude</span></span></th>
<th><span data-ttu-id="5dd94-597">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="5dd94-597">Allocation factor</span></span></th>
<th><span data-ttu-id="5dd94-598">Summa</span><span class="sxs-lookup"><span data-stu-id="5dd94-598">Amount</span></span></th>
<th><span data-ttu-id="5dd94-599">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5dd94-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-600">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-600">Prod 1</span></span></td>
<td><span data-ttu-id="5dd94-601">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-601">Product 1</span></span></td>
<td><span data-ttu-id="5dd94-602">60</span><span class="sxs-lookup"><span data-stu-id="5dd94-602">60</span></span></td>
<td><span data-ttu-id="5dd94-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="5dd94-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="5dd94-604">535.31</span><span class="sxs-lookup"><span data-stu-id="5dd94-604">535.31</span></span></td>
<td><span data-ttu-id="5dd94-605">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-606">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-606">Prod 2</span></span></td>
<td><span data-ttu-id="5dd94-607">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-607">Product 2</span></span></td>
<td><span data-ttu-id="5dd94-608">20</span><span class="sxs-lookup"><span data-stu-id="5dd94-608">20</span></span></td>
<td><span data-ttu-id="5dd94-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="5dd94-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="5dd94-610">178.44</span><span class="sxs-lookup"><span data-stu-id="5dd94-610">178.44</span></span></td>
<td><span data-ttu-id="5dd94-611">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-612">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-612">Prod 1</span></span></td>
<td><span data-ttu-id="5dd94-613">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-613">Product 1</span></span></td>
<td><span data-ttu-id="5dd94-614">60</span><span class="sxs-lookup"><span data-stu-id="5dd94-614">60</span></span></td>
<td><span data-ttu-id="5dd94-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="5dd94-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="5dd94-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="5dd94-616">4,487.12</span></span></td>
<td><span data-ttu-id="5dd94-617">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-618">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-618">Prod 2</span></span></td>
<td><span data-ttu-id="5dd94-619">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-619">Product 2</span></span></td>
<td><span data-ttu-id="5dd94-620">20</span><span class="sxs-lookup"><span data-stu-id="5dd94-620">20</span></span></td>
<td><span data-ttu-id="5dd94-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="5dd94-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="5dd94-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="5dd94-622">1,495.71</span></span></td>
<td><span data-ttu-id="5dd94-623">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5dd94-624">Seuraavassa taulukossa näytetään tulos, kun Pakkauspalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="5dd94-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5dd94-625">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-625">Cost object</span></span></th>
<th><span data-ttu-id="5dd94-626">Suuruus</span><span class="sxs-lookup"><span data-stu-id="5dd94-626">Magnitude</span></span></th>
<th><span data-ttu-id="5dd94-627">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="5dd94-627">Allocation factor</span></span></th>
<th><span data-ttu-id="5dd94-628">Summa</span><span class="sxs-lookup"><span data-stu-id="5dd94-628">Amount</span></span></th>
<th><span data-ttu-id="5dd94-629">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5dd94-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-630">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-630">Prod 1</span></span></td>
<td><span data-ttu-id="5dd94-631">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-631">Product 1</span></span></td>
<td><span data-ttu-id="5dd94-632">80</span><span class="sxs-lookup"><span data-stu-id="5dd94-632">80</span></span></td>
<td><span data-ttu-id="5dd94-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="5dd94-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="5dd94-634">241.05</span><span class="sxs-lookup"><span data-stu-id="5dd94-634">241.05</span></span></td>
<td><span data-ttu-id="5dd94-635">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-636">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-636">Prod 2</span></span></td>
<td><span data-ttu-id="5dd94-637">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-637">Product 2</span></span></td>
<td><span data-ttu-id="5dd94-638">15</span><span class="sxs-lookup"><span data-stu-id="5dd94-638">15</span></span></td>
<td><span data-ttu-id="5dd94-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="5dd94-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="5dd94-640">45.20</span><span class="sxs-lookup"><span data-stu-id="5dd94-640">45.20</span></span></td>
<td><span data-ttu-id="5dd94-641">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-642">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-642">Prod 1</span></span></td>
<td><span data-ttu-id="5dd94-643">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-643">Product 1</span></span></td>
<td><span data-ttu-id="5dd94-644">80</span><span class="sxs-lookup"><span data-stu-id="5dd94-644">80</span></span></td>
<td><span data-ttu-id="5dd94-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="5dd94-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="5dd94-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="5dd94-646">2,507.09</span></span></td>
<td><span data-ttu-id="5dd94-647">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-648">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-648">Prod 2</span></span></td>
<td><span data-ttu-id="5dd94-649">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-649">Product 2</span></span></td>
<td><span data-ttu-id="5dd94-650">15</span><span class="sxs-lookup"><span data-stu-id="5dd94-650">15</span></span></td>
<td><span data-ttu-id="5dd94-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="5dd94-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="5dd94-652">470.08</span><span class="sxs-lookup"><span data-stu-id="5dd94-652">470.08</span></span></td>
<td><span data-ttu-id="5dd94-653">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5dd94-654">Kirjauskansioviennit (kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="5dd94-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5dd94-655">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5dd94-655">Journal</span></span></th>
<th><span data-ttu-id="5dd94-656">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="5dd94-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5dd94-657">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="5dd94-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5dd94-658">Versio</span><span class="sxs-lookup"><span data-stu-id="5dd94-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-659">00004</span><span class="sxs-lookup"><span data-stu-id="5dd94-659">00004</span></span></td>
<td><span data-ttu-id="5dd94-660">Kustannusten kohdistuskirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5dd94-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="5dd94-661">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="5dd94-661">Fiscal</span></span></td>
<td><span data-ttu-id="5dd94-662">2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-662">2017</span></span></td>
<td><span data-ttu-id="5dd94-663">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-663">Period 1</span></span></td>
<td><span data-ttu-id="5dd94-664">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="5dd94-665">Kirjauskansion rivit</span><span class="sxs-lookup"><span data-stu-id="5dd94-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5dd94-666">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="5dd94-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5dd94-667">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5dd94-668">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="5dd94-668">Cost element</span></span></th>
<th><span data-ttu-id="5dd94-669">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5dd94-669">Cost behavior</span></span></th>
<th><span data-ttu-id="5dd94-670">Summa</span><span class="sxs-lookup"><span data-stu-id="5dd94-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-671">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="5dd94-672">CC001</span><span class="sxs-lookup"><span data-stu-id="5dd94-672">CC001</span></span></td>
<td><span data-ttu-id="5dd94-673">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5dd94-673">HR</span></span></td>
<td><span data-ttu-id="5dd94-674">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-674">10001</span></span></td>
<td><span data-ttu-id="5dd94-675">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-675">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-676">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-676">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-677">500,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-678">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="5dd94-679">CC001</span><span class="sxs-lookup"><span data-stu-id="5dd94-679">CC001</span></span></td>
<td><span data-ttu-id="5dd94-680">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5dd94-680">HR</span></span></td>
<td><span data-ttu-id="5dd94-681">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-681">10001</span></span></td>
<td><span data-ttu-id="5dd94-682">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-682">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-683">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-683">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="5dd94-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-685">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="5dd94-686">CC002</span><span class="sxs-lookup"><span data-stu-id="5dd94-686">CC002</span></span></td>
<td><span data-ttu-id="5dd94-687">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5dd94-687">Finance</span></span></td>
<td><span data-ttu-id="5dd94-688">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-688">10001</span></span></td>
<td><span data-ttu-id="5dd94-689">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-689">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-690">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-690">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-691">675.00</span><span class="sxs-lookup"><span data-stu-id="5dd94-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-692">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="5dd94-693">CC002</span><span class="sxs-lookup"><span data-stu-id="5dd94-693">CC002</span></span></td>
<td><span data-ttu-id="5dd94-694">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5dd94-694">Finance</span></span></td>
<td><span data-ttu-id="5dd94-695">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-695">10001</span></span></td>
<td><span data-ttu-id="5dd94-696">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-696">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-697">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-697">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="5dd94-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-699">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="5dd94-700">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-700">CC003</span></span></td>
<td><span data-ttu-id="5dd94-701">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5dd94-701">Assembly</span></span></td>
<td><span data-ttu-id="5dd94-702">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-702">10001</span></span></td>
<td><span data-ttu-id="5dd94-703">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-703">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-704">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-704">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-705">713.75</span><span class="sxs-lookup"><span data-stu-id="5dd94-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-706">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="5dd94-707">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-707">CC003</span></span></td>
<td><span data-ttu-id="5dd94-708">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5dd94-708">Assembly</span></span></td>
<td><span data-ttu-id="5dd94-709">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-709">10001</span></span></td>
<td><span data-ttu-id="5dd94-710">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-710">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-711">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-711">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="5dd94-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-713">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="5dd94-714">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-714">CC003</span></span></td>
<td><span data-ttu-id="5dd94-715">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5dd94-715">Packaging</span></span></td>
<td><span data-ttu-id="5dd94-716">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-716">10001</span></span></td>
<td><span data-ttu-id="5dd94-717">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-717">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-718">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-718">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-719">286.25</span><span class="sxs-lookup"><span data-stu-id="5dd94-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-720">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="5dd94-721">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-721">CC003</span></span></td>
<td><span data-ttu-id="5dd94-722">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5dd94-722">Packaging</span></span></td>
<td><span data-ttu-id="5dd94-723">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-723">10001</span></span></td>
<td><span data-ttu-id="5dd94-724">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-724">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-725">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-725">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="5dd94-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-727">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="5dd94-728">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-728">Prod 1</span></span></td>
<td><span data-ttu-id="5dd94-729">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-729">Product 1</span></span></td>
<td><span data-ttu-id="5dd94-730">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-730">10001</span></span></td>
<td><span data-ttu-id="5dd94-731">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-731">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-732">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-732">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-733">776.36</span><span class="sxs-lookup"><span data-stu-id="5dd94-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-734">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="5dd94-735">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-735">Prod 1</span></span></td>
<td><span data-ttu-id="5dd94-736">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-736">Product 1</span></span></td>
<td><span data-ttu-id="5dd94-737">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-737">10001</span></span></td>
<td><span data-ttu-id="5dd94-738">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-738">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-739">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-739">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="5dd94-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-741">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="5dd94-742">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-742">Prod 2</span></span></td>
<td><span data-ttu-id="5dd94-743">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-743">Product 1</span></span></td>
<td><span data-ttu-id="5dd94-744">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-744">10001</span></span></td>
<td><span data-ttu-id="5dd94-745">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-745">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-746">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-746">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-747">223.64</span><span class="sxs-lookup"><span data-stu-id="5dd94-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-748">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="5dd94-749">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-749">Prod 2</span></span></td>
<td><span data-ttu-id="5dd94-750">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-750">Product 1</span></span></td>
<td><span data-ttu-id="5dd94-751">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-751">10001</span></span></td>
<td><span data-ttu-id="5dd94-752">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-752">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-753">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-753">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="5dd94-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5dd94-755">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="5dd94-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5dd94-756">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5dd94-757">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="5dd94-757">Cost element</span></span></th>
<th><span data-ttu-id="5dd94-758">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="5dd94-758">Cost behavior</span></span></th>
<th><span data-ttu-id="5dd94-759">Summa</span><span class="sxs-lookup"><span data-stu-id="5dd94-759">Amount</span></span></th>
<th><span data-ttu-id="5dd94-760">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="5dd94-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5dd94-761">CC001</span><span class="sxs-lookup"><span data-stu-id="5dd94-761">CC001</span></span></td>
<td><span data-ttu-id="5dd94-762">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5dd94-762">HR</span></span></td>
<td><span data-ttu-id="5dd94-763">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-763">10001</span></span></td>
<td><span data-ttu-id="5dd94-764">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-764">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-765">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-765">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-766">-500.00</span></span></td>
<td><span data-ttu-id="5dd94-767">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-768">CC002</span><span class="sxs-lookup"><span data-stu-id="5dd94-768">CC002</span></span></td>
<td><span data-ttu-id="5dd94-769">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5dd94-769">Finance</span></span></td>
<td><span data-ttu-id="5dd94-770">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-770">10001</span></span></td>
<td><span data-ttu-id="5dd94-771">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-771">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-772">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-772">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-773">175.00</span><span class="sxs-lookup"><span data-stu-id="5dd94-773">175.00</span></span></td>
<td><span data-ttu-id="5dd94-774">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-775">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-775">CC003</span></span></td>
<td><span data-ttu-id="5dd94-776">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5dd94-776">Assembly</span></span></td>
<td><span data-ttu-id="5dd94-777">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-777">10001</span></span></td>
<td><span data-ttu-id="5dd94-778">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-778">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-779">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-779">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-780">275.00</span><span class="sxs-lookup"><span data-stu-id="5dd94-780">275.00</span></span></td>
<td><span data-ttu-id="5dd94-781">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-782">CC004</span><span class="sxs-lookup"><span data-stu-id="5dd94-782">CC004</span></span></td>
<td><span data-ttu-id="5dd94-783">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5dd94-783">Packaging</span></span></td>
<td><span data-ttu-id="5dd94-784">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-784">10001</span></span></td>
<td><span data-ttu-id="5dd94-785">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-785">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-786">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-786">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-787">50,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-787">50,00</span></span></td>
<td><span data-ttu-id="5dd94-788">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-789">CC001</span><span class="sxs-lookup"><span data-stu-id="5dd94-789">CC001</span></span></td>
<td><span data-ttu-id="5dd94-790">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="5dd94-790">HR</span></span></td>
<td><span data-ttu-id="5dd94-791">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-791">10001</span></span></td>
<td><span data-ttu-id="5dd94-792">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-792">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-793">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-793">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="5dd94-794">-1,245.71</span></span></td>
<td><span data-ttu-id="5dd94-795">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-796">CC002</span><span class="sxs-lookup"><span data-stu-id="5dd94-796">CC002</span></span></td>
<td><span data-ttu-id="5dd94-797">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5dd94-797">Finance</span></span></td>
<td><span data-ttu-id="5dd94-798">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-798">10001</span></span></td>
<td><span data-ttu-id="5dd94-799">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-799">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-800">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-800">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-801">436.00</span><span class="sxs-lookup"><span data-stu-id="5dd94-801">436.00</span></span></td>
<td><span data-ttu-id="5dd94-802">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-803">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-803">CC003</span></span></td>
<td><span data-ttu-id="5dd94-804">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5dd94-804">Assembly</span></span></td>
<td><span data-ttu-id="5dd94-805">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-805">10001</span></span></td>
<td><span data-ttu-id="5dd94-806">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-806">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-807">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-807">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-808">685.14</span><span class="sxs-lookup"><span data-stu-id="5dd94-808">685.14</span></span></td>
<td><span data-ttu-id="5dd94-809">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-810">CC004</span><span class="sxs-lookup"><span data-stu-id="5dd94-810">CC004</span></span></td>
<td><span data-ttu-id="5dd94-811">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5dd94-811">Packaging</span></span></td>
<td><span data-ttu-id="5dd94-812">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-812">10001</span></span></td>
<td><span data-ttu-id="5dd94-813">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-813">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-814">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-814">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-815">124.57</span><span class="sxs-lookup"><span data-stu-id="5dd94-815">124.57</span></span></td>
<td><span data-ttu-id="5dd94-816">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-817">CC002</span><span class="sxs-lookup"><span data-stu-id="5dd94-817">CC002</span></span></td>
<td><span data-ttu-id="5dd94-818">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5dd94-818">Finance</span></span></td>
<td><span data-ttu-id="5dd94-819">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-819">10001</span></span></td>
<td><span data-ttu-id="5dd94-820">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-820">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-821">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-821">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-822">-675.00</span></span></td>
<td><span data-ttu-id="5dd94-823">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-824">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-824">CC003</span></span></td>
<td><span data-ttu-id="5dd94-825">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5dd94-825">Assembly</span></span></td>
<td><span data-ttu-id="5dd94-826">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-826">10001</span></span></td>
<td><span data-ttu-id="5dd94-827">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-827">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-828">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-828">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-829">438.75</span><span class="sxs-lookup"><span data-stu-id="5dd94-829">438.75</span></span></td>
<td><span data-ttu-id="5dd94-830">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-831">CC004</span><span class="sxs-lookup"><span data-stu-id="5dd94-831">CC004</span></span></td>
<td><span data-ttu-id="5dd94-832">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5dd94-832">Packaging</span></span></td>
<td><span data-ttu-id="5dd94-833">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-833">10001</span></span></td>
<td><span data-ttu-id="5dd94-834">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-834">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-835">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-835">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-836">236.25</span><span class="sxs-lookup"><span data-stu-id="5dd94-836">236.25</span></span></td>
<td><span data-ttu-id="5dd94-837">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-838">CC002</span><span class="sxs-lookup"><span data-stu-id="5dd94-838">CC002</span></span></td>
<td><span data-ttu-id="5dd94-839">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="5dd94-839">Finance</span></span></td>
<td><span data-ttu-id="5dd94-840">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-840">10001</span></span></td>
<td><span data-ttu-id="5dd94-841">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-841">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-842">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-842">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="5dd94-843">-8,150.29</span></span></td>
<td><span data-ttu-id="5dd94-844">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-845">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-845">CC003</span></span></td>
<td><span data-ttu-id="5dd94-846">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5dd94-846">Assembly</span></span></td>
<td><span data-ttu-id="5dd94-847">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-847">10001</span></span></td>
<td><span data-ttu-id="5dd94-848">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-848">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-849">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-849">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="5dd94-850">5,297.69</span></span></td>
<td><span data-ttu-id="5dd94-851">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-852">CC004</span><span class="sxs-lookup"><span data-stu-id="5dd94-852">CC004</span></span></td>
<td><span data-ttu-id="5dd94-853">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="5dd94-853">Packaging</span></span></td>
<td><span data-ttu-id="5dd94-854">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-854">10001</span></span></td>
<td><span data-ttu-id="5dd94-855">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-855">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-856">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-856">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="5dd94-857">2,852.60</span></span></td>
<td><span data-ttu-id="5dd94-858">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-859">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-859">CC003</span></span></td>
<td><span data-ttu-id="5dd94-860">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5dd94-860">Assembly</span></span></td>
<td><span data-ttu-id="5dd94-861">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-861">10001</span></span></td>
<td><span data-ttu-id="5dd94-862">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-862">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-863">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-863">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="5dd94-864">-713.75</span></span></td>
<td><span data-ttu-id="5dd94-865">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-866">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-866">Prod 1</span></span></td>
<td><span data-ttu-id="5dd94-867">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-867">Product 1</span></span></td>
<td><span data-ttu-id="5dd94-868">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-868">10001</span></span></td>
<td><span data-ttu-id="5dd94-869">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-869">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-870">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-870">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-871">535.31</span><span class="sxs-lookup"><span data-stu-id="5dd94-871">535.31</span></span></td>
<td><span data-ttu-id="5dd94-872">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-873">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-873">Prod 2</span></span></td>
<td><span data-ttu-id="5dd94-874">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-874">Product 2</span></span></td>
<td><span data-ttu-id="5dd94-875">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-875">10001</span></span></td>
<td><span data-ttu-id="5dd94-876">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-876">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-877">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-877">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-878">178.44</span><span class="sxs-lookup"><span data-stu-id="5dd94-878">178.44</span></span></td>
<td><span data-ttu-id="5dd94-879">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-880">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-880">CC003</span></span></td>
<td><span data-ttu-id="5dd94-881">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5dd94-881">Assembly</span></span></td>
<td><span data-ttu-id="5dd94-882">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-882">10001</span></span></td>
<td><span data-ttu-id="5dd94-883">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-883">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-884">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-884">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="5dd94-885">-5,982.83</span></span></td>
<td><span data-ttu-id="5dd94-886">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-887">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-887">Prod 1</span></span></td>
<td><span data-ttu-id="5dd94-888">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-888">Product 1</span></span></td>
<td><span data-ttu-id="5dd94-889">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-889">10001</span></span></td>
<td><span data-ttu-id="5dd94-890">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-890">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-891">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-891">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="5dd94-892">4,487.12</span></span></td>
<td><span data-ttu-id="5dd94-893">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-894">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-894">Prod 2</span></span></td>
<td><span data-ttu-id="5dd94-895">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-895">Product 2</span></span></td>
<td><span data-ttu-id="5dd94-896">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-896">10001</span></span></td>
<td><span data-ttu-id="5dd94-897">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-897">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-898">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-898">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="5dd94-899">1,495.71</span></span></td>
<td><span data-ttu-id="5dd94-900">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-901">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-901">CC003</span></span></td>
<td><span data-ttu-id="5dd94-902">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5dd94-902">Assembly</span></span></td>
<td><span data-ttu-id="5dd94-903">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-903">10001</span></span></td>
<td><span data-ttu-id="5dd94-904">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-904">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-905">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-905">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="5dd94-906">-286.25</span></span></td>
<td><span data-ttu-id="5dd94-907">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-908">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-908">Prod 1</span></span></td>
<td><span data-ttu-id="5dd94-909">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-909">Product 1</span></span></td>
<td><span data-ttu-id="5dd94-910">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-910">10001</span></span></td>
<td><span data-ttu-id="5dd94-911">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-911">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-912">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-912">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-913">241.05</span><span class="sxs-lookup"><span data-stu-id="5dd94-913">241.05</span></span></td>
<td><span data-ttu-id="5dd94-914">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-915">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-915">Prod 2</span></span></td>
<td><span data-ttu-id="5dd94-916">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-916">Product 2</span></span></td>
<td><span data-ttu-id="5dd94-917">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-917">10001</span></span></td>
<td><span data-ttu-id="5dd94-918">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-918">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-919">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-919">Fixed cost</span></span></td>
<td><span data-ttu-id="5dd94-920">45.20</span><span class="sxs-lookup"><span data-stu-id="5dd94-920">45.20</span></span></td>
<td><span data-ttu-id="5dd94-921">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-922">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-922">CC003</span></span></td>
<td><span data-ttu-id="5dd94-923">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="5dd94-923">Assembly</span></span></td>
<td><span data-ttu-id="5dd94-924">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-924">10001</span></span></td>
<td><span data-ttu-id="5dd94-925">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-925">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-926">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-926">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-927">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="5dd94-927">-2,977.17</span></span></td>
<td><span data-ttu-id="5dd94-928">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-929">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-929">Prod 1</span></span></td>
<td><span data-ttu-id="5dd94-930">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-930">Product 1</span></span></td>
<td><span data-ttu-id="5dd94-931">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-931">10001</span></span></td>
<td><span data-ttu-id="5dd94-932">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-932">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-933">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-933">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="5dd94-934">2,507.09</span></span></td>
<td><span data-ttu-id="5dd94-935">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5dd94-936">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-936">Prod 2</span></span></td>
<td><span data-ttu-id="5dd94-937">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-937">Product 2</span></span></td>
<td><span data-ttu-id="5dd94-938">10 001</span><span class="sxs-lookup"><span data-stu-id="5dd94-938">10001</span></span></td>
<td><span data-ttu-id="5dd94-939">Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-939">Electricity</span></span></td>
<td><span data-ttu-id="5dd94-940">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-940">Variable cost</span></span></td>
<td><span data-ttu-id="5dd94-941">470.08</span><span class="sxs-lookup"><span data-stu-id="5dd94-941">470.08</span></span></td>
<td><span data-ttu-id="5dd94-942">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="5dd94-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="5dd94-943">Johtopäätökset</span><span class="sxs-lookup"><span data-stu-id="5dd94-943">Conclusion</span></span>
<span data-ttu-id="5dd94-944">Kirjanpidossa kirjataan tyhjään kustannuspaikkatunnukseen sähkökustannus arvolla 10 000,00.</span><span class="sxs-lookup"><span data-stu-id="5dd94-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="5dd94-945">Tämän ansiosta kustannuslaskijat tietävät, että kustannus on kohdistettava.</span><span class="sxs-lookup"><span data-stu-id="5dd94-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="5dd94-946">Kustannukset virtaavat kirjanpidossa organisaation yksiköiden ja tasojen läpi käytössä olevien käytäntöjen ja sääntöjen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="5dd94-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="5dd94-947">Kukin kustannus on liitetty kustannusperusteeseen, joka sisältää parhaan arvion kustannusten kohdistuksesta.</span><span class="sxs-lookup"><span data-stu-id="5dd94-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="5dd94-948">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="5dd94-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="5dd94-949">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="5dd94-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="5dd94-950">Yhteensä</span><span class="sxs-lookup"><span data-stu-id="5dd94-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5dd94-951">CC099</span><span class="sxs-lookup"><span data-stu-id="5dd94-951">CC099</span></span></th>
<th><span data-ttu-id="5dd94-952">CC001</span><span class="sxs-lookup"><span data-stu-id="5dd94-952">CC001</span></span></th>
<th><span data-ttu-id="5dd94-953">CC002</span><span class="sxs-lookup"><span data-stu-id="5dd94-953">CC002</span></span></th>
<th><span data-ttu-id="5dd94-954">CC003</span><span class="sxs-lookup"><span data-stu-id="5dd94-954">CC003</span></span></th>
<th><span data-ttu-id="5dd94-955">CC004</span><span class="sxs-lookup"><span data-stu-id="5dd94-955">CC004</span></span></th>
<th><span data-ttu-id="5dd94-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-956">Proj 1</span></span></th>
<th><span data-ttu-id="5dd94-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-957">Proj 2</span></span></th>
<th><span data-ttu-id="5dd94-958">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="5dd94-958">Prod 1</span></span></th>
<th><span data-ttu-id="5dd94-959">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="5dd94-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="5dd94-960">10001 Sähkö</span><span class="sxs-lookup"><span data-stu-id="5dd94-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="5dd94-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="5dd94-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="5dd94-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="5dd94-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="5dd94-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="5dd94-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="5dd94-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="5dd94-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="5dd94-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="5dd94-970">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="5dd94-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-971">0,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="5dd94-972">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="5dd94-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-973">0,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-974">0,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-975">0,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-976">0,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-977">0,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-978">776.36</span><span class="sxs-lookup"><span data-stu-id="5dd94-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-979">223.64</span><span class="sxs-lookup"><span data-stu-id="5dd94-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="5dd94-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="5dd94-981">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="5dd94-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-982">000</span><span class="sxs-lookup"><span data-stu-id="5dd94-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-983">0,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-984">0,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-985">0,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-986">0,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-987">30,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-988">10,00</span><span class="sxs-lookup"><span data-stu-id="5dd94-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="5dd94-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="5dd94-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5dd94-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="5dd94-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5dd94-992">Tässä ohjeaiheessa esitellään, miten ensisijainen kustannuselementti, 10001 Sähkö, virtaa kustannusobjektien läpi.</span><span class="sxs-lookup"><span data-stu-id="5dd94-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="5dd94-993">Tästä syystä tämä yleiskustannus kohdistetaan organisaation alimmalle tasolle.</span><span class="sxs-lookup"><span data-stu-id="5dd94-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="5dd94-994">Toisin sanoen alimman tason kustannusobjektit kantavat kustannuksen.</span><span class="sxs-lookup"><span data-stu-id="5dd94-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="5dd94-995">Jos tarvitset visuaalisen näkymän kustannuksen virrasta kustannusobjektien välillä, voit käyttää kustannuksen koontikäytäntösääntöjä kustannusvirran visualisointiin.</span><span class="sxs-lookup"><span data-stu-id="5dd94-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="5dd94-996">Lisätietoja on kohdassa [Kustannusten koonti](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="5dd94-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>




