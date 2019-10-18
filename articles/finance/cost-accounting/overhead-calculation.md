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
ms.openlocfilehash: 6c045f82f3288dba193721dd80c90e68750af9a7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177549"
---
# <a name="overhead-calculation"></a><span data-ttu-id="160d5-103">Yleiskustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="160d5-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="160d5-104">Tässä aiheessa kuvataan tyypillinen yleiskustannusten laskenta- ja kohdistusprosessi.</span><span class="sxs-lookup"><span data-stu-id="160d5-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="160d5-105">Sanaston määritelmä</span><span class="sxs-lookup"><span data-stu-id="160d5-105">Term definition</span></span>
---------------

<span data-ttu-id="160d5-106">Yleiskustannukset ovat yrityksen toiminnasta syntyviä kustannuksia, joita ei voi suoraan liittää mihinkään tiettyyn liiketoiminnan tehtävään, tuotteeseen tai palveluun.</span><span class="sxs-lookup"><span data-stu-id="160d5-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="160d5-107">Yleiskustannukset ovat tärkeä tuki voittoa tuottavien tehtävien luonnissa.</span><span class="sxs-lookup"><span data-stu-id="160d5-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="160d5-108">Seuraavassa on joitakin esimerkkejä yleiskustannuksista:</span><span class="sxs-lookup"><span data-stu-id="160d5-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="160d5-109">Vuokra</span><span class="sxs-lookup"><span data-stu-id="160d5-109">Rent</span></span>
-   <span data-ttu-id="160d5-110">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-110">Electricity</span></span>
-   <span data-ttu-id="160d5-111">Hallinnon palkat</span><span class="sxs-lookup"><span data-stu-id="160d5-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="160d5-112">Yleiskustannuslaskennan yleiskuva</span><span class="sxs-lookup"><span data-stu-id="160d5-112">Overhead calculation overview</span></span>
<span data-ttu-id="160d5-113">Yleiskustannusten laskenta suorittaa kustannuslaskennan käytännöt oikeassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="160d5-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="160d5-114">Yleiskustannusten laskennan voi suorittaa useita kertoja samalle tilikaudelle, jos kustannuslaskennan käytännöt ovat muuttuneet tai erityisiä virheitä on havaittu.</span><span class="sxs-lookup"><span data-stu-id="160d5-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="160d5-115">Kukin laskenta-ajo tallennetaan ja kullekin annetaan yksilöllinen versiotunnus, jonka avulla eri laskenta-ajoja voi verrata toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="160d5-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="160d5-116">Yleiskustannusten laskenta luo kustannustapahtumia, joille annetaan kirjauspäivä.</span><span class="sxs-lookup"><span data-stu-id="160d5-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="160d5-117">Kirjauspäivä vastaa laskennassa käytettyä tilikauden päättymispäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="160d5-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="160d5-118">Yksilöivä versiotunnus sisältää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="160d5-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="160d5-119">Versiotyyppi</span><span class="sxs-lookup"><span data-stu-id="160d5-119">Version type</span></span>
-   <span data-ttu-id="160d5-120">Päivämäärä ja aika</span><span class="sxs-lookup"><span data-stu-id="160d5-120">Date and time</span></span>
-   <span data-ttu-id="160d5-121">Kustannuslaskennan kirjanpito</span><span class="sxs-lookup"><span data-stu-id="160d5-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="160d5-122">Tilikausi </span><span class="sxs-lookup"><span data-stu-id="160d5-122">Fiscal year</span></span>
-   <span data-ttu-id="160d5-123">Tilikausi  </span><span class="sxs-lookup"><span data-stu-id="160d5-123">Fiscal period</span></span>

<span data-ttu-id="160d5-124">Yleiskustannusten laskenta ajetaan versiosta riippumattomana.</span><span class="sxs-lookup"><span data-stu-id="160d5-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="160d5-125">Voit siis laskea budjetin version ennen todellista versiota.</span><span class="sxs-lookup"><span data-stu-id="160d5-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="160d5-126">Yleiskustannusten laskenta koostuu neljästä vaiheesta, jotka esitellään seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="160d5-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="160d5-127">Kussakin vaiheessa luodaan kirjauskansion otsikko, jolla on kirjauskansiovientejä.</span><span class="sxs-lookup"><span data-stu-id="160d5-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="160d5-128">Tämä kirjauskansion otsikko säilyttää kunkin laskentavaiheen syöttötiedot.</span><span class="sxs-lookup"><span data-stu-id="160d5-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="160d5-129">Käytännöt ja säännöt ajetaan kullekin kirjauskansion riville, ja tuloksena luodaan kustannustapahtumia.</span><span class="sxs-lookup"><span data-stu-id="160d5-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="160d5-130">Tämän ansiosta kaikki laskutoimitukset ovat täysin jäljitettävissä.</span><span class="sxs-lookup"><span data-stu-id="160d5-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="160d5-131">[![Yleiskustannuslaskenta](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="160d5-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="160d5-132">Laske ja kohdista sähkön yleiskustannukset</span><span class="sxs-lookup"><span data-stu-id="160d5-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="160d5-133">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="160d5-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="160d5-134">Tarkka johdon näkymä ei täten ole saatavilla kustannuslaskennassa.</span><span class="sxs-lookup"><span data-stu-id="160d5-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="160d5-135">Jotta kustannuslaskenta tarjoaisi oikean johdon näkymän kaikista organisaation yksiköistä ja tasoista, kustannusten on virrattava organisaation yksiköiden läpi.</span><span class="sxs-lookup"><span data-stu-id="160d5-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="160d5-136">Tämän virran on perustuttava joko tarkkaan tietoon kulutuksesta tai perusteltuun arvioon.</span><span class="sxs-lookup"><span data-stu-id="160d5-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="160d5-137">Sähkökustannukset voi kirjata kirjanpitoon seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="160d5-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="160d5-138">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="160d5-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="160d5-139">Kustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="160d5-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="160d5-140">Päätili</span><span class="sxs-lookup"><span data-stu-id="160d5-140">Main account</span></span></th>
<th><span data-ttu-id="160d5-141">Summa kirjanpitovaluuttana</span><span class="sxs-lookup"><span data-stu-id="160d5-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-142">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="160d5-143">CC099</span><span class="sxs-lookup"><span data-stu-id="160d5-143">CC099</span></span></td>
<td><span data-ttu-id="160d5-144">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="160d5-144">Default cost center</span></span></td>
<td><span data-ttu-id="160d5-145">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-145">10001</span></span></td>
<td><span data-ttu-id="160d5-146">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-146">Electricity</span></span></td>
<td><span data-ttu-id="160d5-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="160d5-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="160d5-148">Vaihe 1: Käsittele kustannustoiminnan laskenta</span><span class="sxs-lookup"><span data-stu-id="160d5-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="160d5-149">Kun kustannustapahtumat tuodaan lähdetiedoista, niille asetetaan kustannuslaskennassa oletusarvoisesti **Luokittelematon** -kustannustoimintaluokka.</span><span class="sxs-lookup"><span data-stu-id="160d5-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="160d5-150">Voit luokitella kustannustapahtumia uudelleen **kiinteäksi kustannukseksi** tai **muuttuvaksi kustannukseksi** kustannustoiminnan käytäntösäännöillä.</span><span class="sxs-lookup"><span data-stu-id="160d5-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="160d5-151">Määritä kustannustoiminnan sääntö</span><span class="sxs-lookup"><span data-stu-id="160d5-151">Define the cost behavior rule</span></span>

<span data-ttu-id="160d5-152">Joissain tapauksissa osa kustannuksesta on kiinteä ja loppuosa perustuu kulutukseen.</span><span class="sxs-lookup"><span data-stu-id="160d5-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="160d5-153">Sähkölaskut sopivat usein tähän määritelmään.</span><span class="sxs-lookup"><span data-stu-id="160d5-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="160d5-154">Maksat ensin määrätyn, kiinteän maksun, jonka lisäksi maksat kulutuksesta kilowattitunteina (kWh).</span><span class="sxs-lookup"><span data-stu-id="160d5-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="160d5-155">Jos kiinteä maksu on esimerkiksi 1 000,00, kustannustoiminnan sääntö määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="160d5-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="160d5-156">Kiinteä määrä 1 000,00</span><span class="sxs-lookup"><span data-stu-id="160d5-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="160d5-157">0 &lt;= 1 000,00 = Kiinteä</span><span class="sxs-lookup"><span data-stu-id="160d5-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="160d5-158">1000,01 &lt; N = Muuttuva</span><span class="sxs-lookup"><span data-stu-id="160d5-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="160d5-159">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="160d5-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="160d5-160">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="160d5-160">Journal</span></span></th>
<th><span data-ttu-id="160d5-161">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="160d5-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="160d5-162">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="160d5-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="160d5-163">Versio</span><span class="sxs-lookup"><span data-stu-id="160d5-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-164">00001</span><span class="sxs-lookup"><span data-stu-id="160d5-164">00001</span></span></td>
<td><span data-ttu-id="160d5-165">Kustannustoiminnan laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="160d5-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="160d5-166">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="160d5-166">Fiscal</span></span></td>
<td><span data-ttu-id="160d5-167">2017</span><span class="sxs-lookup"><span data-stu-id="160d5-167">2017</span></span></td>
<td><span data-ttu-id="160d5-168">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="160d5-168">Period 1</span></span></td>
<td><span data-ttu-id="160d5-169">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="160d5-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="160d5-170">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="160d5-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="160d5-171">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="160d5-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="160d5-172">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="160d5-173">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="160d5-173">Cost element</span></span></th>
<th><span data-ttu-id="160d5-174">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="160d5-174">Cost behavior</span></span></th>
<th><span data-ttu-id="160d5-175">Summa</span><span class="sxs-lookup"><span data-stu-id="160d5-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-176">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="160d5-177">CC099</span><span class="sxs-lookup"><span data-stu-id="160d5-177">CC099</span></span></td>
<td><span data-ttu-id="160d5-178">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="160d5-178">Default cost center</span></span></td>
<td><span data-ttu-id="160d5-179">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-179">10001</span></span></td>
<td><span data-ttu-id="160d5-180">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-180">Electricity</span></span></td>
<td><span data-ttu-id="160d5-181">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="160d5-181">Unclassified</span></span></td>
<td><span data-ttu-id="160d5-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="160d5-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="160d5-183">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="160d5-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="160d5-184">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="160d5-185">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="160d5-185">Cost element</span></span></th>
<th><span data-ttu-id="160d5-186">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="160d5-186">Cost behavior</span></span></th>
<th><span data-ttu-id="160d5-187">Summa</span><span class="sxs-lookup"><span data-stu-id="160d5-187">Amount</span></span></th>
<th><span data-ttu-id="160d5-188">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="160d5-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-189">CC099</span><span class="sxs-lookup"><span data-stu-id="160d5-189">CC099</span></span></td>
<td><span data-ttu-id="160d5-190">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="160d5-190">Default cost center</span></span></td>
<td><span data-ttu-id="160d5-191">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-191">10001</span></span></td>
<td><span data-ttu-id="160d5-192">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-192">Electricity</span></span></td>
<td><span data-ttu-id="160d5-193">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="160d5-193">Unclassified</span></span></td>
<td><span data-ttu-id="160d5-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="160d5-194">10,000.00</span></span></td>
<td><span data-ttu-id="160d5-195">3.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-196">CC099</span><span class="sxs-lookup"><span data-stu-id="160d5-196">CC099</span></span></td>
<td><span data-ttu-id="160d5-197">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="160d5-197">Default cost center</span></span></td>
<td><span data-ttu-id="160d5-198">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-198">10001</span></span></td>
<td><span data-ttu-id="160d5-199">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-199">Electricity</span></span></td>
<td><span data-ttu-id="160d5-200">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="160d5-200">Unclassified</span></span></td>
<td><span data-ttu-id="160d5-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="160d5-201">-10,000.00</span></span></td>
<td><span data-ttu-id="160d5-202">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-203">CC099</span><span class="sxs-lookup"><span data-stu-id="160d5-203">CC099</span></span></td>
<td><span data-ttu-id="160d5-204">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="160d5-204">Default cost center</span></span></td>
<td><span data-ttu-id="160d5-205">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-205">10001</span></span></td>
<td><span data-ttu-id="160d5-206">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-206">Electricity</span></span></td>
<td><span data-ttu-id="160d5-207">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-207">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="160d5-208">1,000.00</span></span></td>
<td><span data-ttu-id="160d5-209">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-210">CC099</span><span class="sxs-lookup"><span data-stu-id="160d5-210">CC099</span></span></td>
<td><span data-ttu-id="160d5-211">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="160d5-211">Default cost center</span></span></td>
<td><span data-ttu-id="160d5-212">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-212">10001</span></span></td>
<td><span data-ttu-id="160d5-213">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-213">Electricity</span></span></td>
<td><span data-ttu-id="160d5-214">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-214">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="160d5-215">9,000.00</span></span></td>
<td><span data-ttu-id="160d5-216">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="160d5-217">Lisätietoja on kohdassa [Kustannustoimintakäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="160d5-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="160d5-218">Vaihe 2: Käsittele kustannusten jaon laskenta</span><span class="sxs-lookup"><span data-stu-id="160d5-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="160d5-219">Kustannusten jakoa käytetään kustannusten jakamiseen yhdestä kustannusobjektista toiseen (tai useampaan kustannusobjektiin) määrittämällä asiaankuuluvan kohdistusperusteen.</span><span class="sxs-lookup"><span data-stu-id="160d5-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="160d5-220">Kustannusten jako ja kustannusten kohdistus eroavat toisistaan sillä, että kustannusten jako tapahtuu aina alkuperäisen kustannuksen ensisijaisen kustannuselementin tasolla.</span><span class="sxs-lookup"><span data-stu-id="160d5-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="160d5-221">Määritä kustannusten jaon sääntö</span><span class="sxs-lookup"><span data-stu-id="160d5-221">Define the cost distribution rule</span></span>

<span data-ttu-id="160d5-222">Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi.</span><span class="sxs-lookup"><span data-stu-id="160d5-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="160d5-223">Kustannuslaskenta ei tarjoa tästä tarpeeksi tarkkoja tietoja.</span><span class="sxs-lookup"><span data-stu-id="160d5-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="160d5-224">Muuttuva kustannus tulisi jakaa yksittäisille kustannusobjekteille reiluin perustein.</span><span class="sxs-lookup"><span data-stu-id="160d5-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="160d5-225">Loogisin kohdistusperuste on sähkönkulutus (kWh).</span><span class="sxs-lookup"><span data-stu-id="160d5-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="160d5-226">Luodaan tilastollinen dimensionjäsen nimeltä Sähkö, johon kirjataan sähkönkulutus.</span><span class="sxs-lookup"><span data-stu-id="160d5-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="160d5-227">Oletusarvon mukaan kaikki tilastolliset dimensiojäsenet ovat käytettävissä kohdistusperusteina.</span><span class="sxs-lookup"><span data-stu-id="160d5-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="160d5-228">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-228">Cost object</span></span></th>
<th><span data-ttu-id="160d5-229">kWh</span><span class="sxs-lookup"><span data-stu-id="160d5-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-230">CC001</span><span class="sxs-lookup"><span data-stu-id="160d5-230">CC001</span></span></td>
<td><span data-ttu-id="160d5-231">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="160d5-231">HR</span></span></td>
<td><span data-ttu-id="160d5-232">1 000</span><span class="sxs-lookup"><span data-stu-id="160d5-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-233">CC002</span><span class="sxs-lookup"><span data-stu-id="160d5-233">CC002</span></span></td>
<td><span data-ttu-id="160d5-234">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="160d5-234">Finance</span></span></td>
<td><span data-ttu-id="160d5-235">6,000</span><span class="sxs-lookup"><span data-stu-id="160d5-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-236">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-236">CC003</span></span></td>
<td><span data-ttu-id="160d5-237">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="160d5-237">Assembly</span></span></td>
<td><span data-ttu-id="160d5-238">0</span><span class="sxs-lookup"><span data-stu-id="160d5-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="160d5-239">Seuraavassa taulukossa on esitetty tulos, kun sähkönkulutusta käytetään kohdistusperusteena muuttuville kuluille.</span><span class="sxs-lookup"><span data-stu-id="160d5-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="160d5-240">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-240">Cost object</span></span></th>
<th><span data-ttu-id="160d5-241">Suuruus</span><span class="sxs-lookup"><span data-stu-id="160d5-241">Magnitude</span></span></th>
<th><span data-ttu-id="160d5-242">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="160d5-242">Allocation factor</span></span></th>
<th><span data-ttu-id="160d5-243">Summa</span><span class="sxs-lookup"><span data-stu-id="160d5-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-244">CC001</span><span class="sxs-lookup"><span data-stu-id="160d5-244">CC001</span></span></td>
<td><span data-ttu-id="160d5-245">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="160d5-245">HR</span></span></td>
<td><span data-ttu-id="160d5-246">1 000</span><span class="sxs-lookup"><span data-stu-id="160d5-246">1,000</span></span></td>
<td><span data-ttu-id="160d5-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="160d5-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="160d5-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="160d5-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-249">CC002</span><span class="sxs-lookup"><span data-stu-id="160d5-249">CC002</span></span></td>
<td><span data-ttu-id="160d5-250">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="160d5-250">Finance</span></span></td>
<td><span data-ttu-id="160d5-251">6,000</span><span class="sxs-lookup"><span data-stu-id="160d5-251">6,000</span></span></td>
<td><span data-ttu-id="160d5-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="160d5-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="160d5-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="160d5-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-254">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-254">CC003</span></span></td>
<td><span data-ttu-id="160d5-255">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="160d5-255">Assembly</span></span></td>
<td><span data-ttu-id="160d5-256">0</span><span class="sxs-lookup"><span data-stu-id="160d5-256">0</span></span></td>
<td><span data-ttu-id="160d5-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="160d5-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="160d5-258">0,00</span><span class="sxs-lookup"><span data-stu-id="160d5-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="160d5-259">Kiinteä kustannus tulisi jakaa tasaisesti yksittäisille kustannusobjekteille, jotka ovat kuluttaneet sähköä.</span><span class="sxs-lookup"><span data-stu-id="160d5-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="160d5-260">Voit käyttää sähkön tilastollista dimensiojäsentä kaavan kohdistusperusteena tämän tavoitteen saavuttamiseksi: (sähkö &gt;0,00) Seuraavassa taulukossa on esitetty tulos siitä, kun sähkönkulutus on määritetty muuttuvien kustannusten kohdistusperusteeksi.</span><span class="sxs-lookup"><span data-stu-id="160d5-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="160d5-261">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-261">Cost object</span></span></th>
<th><span data-ttu-id="160d5-262">Resepti</span><span class="sxs-lookup"><span data-stu-id="160d5-262">Formula</span></span></th>
<th><span data-ttu-id="160d5-263">Suuruus</span><span class="sxs-lookup"><span data-stu-id="160d5-263">Magnitude</span></span></th>
<th><span data-ttu-id="160d5-264">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="160d5-264">Allocation factor</span></span></th>
<th><span data-ttu-id="160d5-265">Summa</span><span class="sxs-lookup"><span data-stu-id="160d5-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-266">CC001</span><span class="sxs-lookup"><span data-stu-id="160d5-266">CC001</span></span></td>
<td><span data-ttu-id="160d5-267">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="160d5-267">HR</span></span></td>
<td><span data-ttu-id="160d5-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="160d5-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="160d5-269">1</span><span class="sxs-lookup"><span data-stu-id="160d5-269">1</span></span></td>
<td><span data-ttu-id="160d5-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="160d5-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="160d5-271">500,00</span><span class="sxs-lookup"><span data-stu-id="160d5-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-272">CC002</span><span class="sxs-lookup"><span data-stu-id="160d5-272">CC002</span></span></td>
<td><span data-ttu-id="160d5-273">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="160d5-273">Finance</span></span></td>
<td><span data-ttu-id="160d5-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="160d5-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="160d5-275">1</span><span class="sxs-lookup"><span data-stu-id="160d5-275">1</span></span></td>
<td><span data-ttu-id="160d5-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="160d5-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="160d5-277">500,00</span><span class="sxs-lookup"><span data-stu-id="160d5-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-278">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-278">CC003</span></span></td>
<td><span data-ttu-id="160d5-279">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="160d5-279">Assembly</span></span></td>
<td><span data-ttu-id="160d5-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="160d5-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="160d5-281">0</span><span class="sxs-lookup"><span data-stu-id="160d5-281">0</span></span></td>
<td><span data-ttu-id="160d5-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="160d5-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="160d5-283">0,00</span><span class="sxs-lookup"><span data-stu-id="160d5-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="160d5-284">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="160d5-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="160d5-285">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="160d5-285">Journal</span></span></th>
<th><span data-ttu-id="160d5-286">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="160d5-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="160d5-287">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="160d5-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="160d5-288">Versio</span><span class="sxs-lookup"><span data-stu-id="160d5-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-289">00002</span><span class="sxs-lookup"><span data-stu-id="160d5-289">00002</span></span></td>
<td><span data-ttu-id="160d5-290">Kustannusten jaon laskentakirjauskansio</span><span class="sxs-lookup"><span data-stu-id="160d5-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="160d5-291">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="160d5-291">Fiscal</span></span></td>
<td><span data-ttu-id="160d5-292">2017</span><span class="sxs-lookup"><span data-stu-id="160d5-292">2017</span></span></td>
<td><span data-ttu-id="160d5-293">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="160d5-293">Period 1</span></span></td>
<td><span data-ttu-id="160d5-294">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="160d5-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="160d5-295">Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="160d5-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="160d5-296">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="160d5-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="160d5-297">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="160d5-298">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="160d5-298">Cost element</span></span></th>
<th><span data-ttu-id="160d5-299">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="160d5-299">Cost behavior</span></span></th>
<th><span data-ttu-id="160d5-300">Summa</span><span class="sxs-lookup"><span data-stu-id="160d5-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-301">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="160d5-302">CC099</span><span class="sxs-lookup"><span data-stu-id="160d5-302">CC099</span></span></td>
<td><span data-ttu-id="160d5-303">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="160d5-303">Default cost center</span></span></td>
<td><span data-ttu-id="160d5-304">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-304">10001</span></span></td>
<td><span data-ttu-id="160d5-305">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-305">Electricity</span></span></td>
<td><span data-ttu-id="160d5-306">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-306">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="160d5-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-308">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="160d5-309">CC099</span><span class="sxs-lookup"><span data-stu-id="160d5-309">CC099</span></span></td>
<td><span data-ttu-id="160d5-310">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="160d5-310">Default cost center</span></span></td>
<td><span data-ttu-id="160d5-311">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-311">10001</span></span></td>
<td><span data-ttu-id="160d5-312">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-312">Electricity</span></span></td>
<td><span data-ttu-id="160d5-313">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-313">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="160d5-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="160d5-315">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="160d5-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="160d5-316">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="160d5-317">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="160d5-317">Cost element</span></span></th>
<th><span data-ttu-id="160d5-318">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="160d5-318">Cost behavior</span></span></th>
<th><span data-ttu-id="160d5-319">Summa</span><span class="sxs-lookup"><span data-stu-id="160d5-319">Amount</span></span></th>
<th><span data-ttu-id="160d5-320">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="160d5-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-321">CC099</span><span class="sxs-lookup"><span data-stu-id="160d5-321">CC099</span></span></td>
<td><span data-ttu-id="160d5-322">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="160d5-322">Default cost center</span></span></td>
<td><span data-ttu-id="160d5-323">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-323">10001</span></span></td>
<td><span data-ttu-id="160d5-324">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-324">Electricity</span></span></td>
<td><span data-ttu-id="160d5-325">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-325">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="160d5-326">-1,000.00</span></span></td>
<td><span data-ttu-id="160d5-327">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-328">CC001</span><span class="sxs-lookup"><span data-stu-id="160d5-328">CC001</span></span></td>
<td><span data-ttu-id="160d5-329">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="160d5-329">HR</span></span></td>
<td><span data-ttu-id="160d5-330">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-330">10001</span></span></td>
<td><span data-ttu-id="160d5-331">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-331">Electricity</span></span></td>
<td><span data-ttu-id="160d5-332">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-332">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-333">500,00</span><span class="sxs-lookup"><span data-stu-id="160d5-333">500.00</span></span></td>
<td><span data-ttu-id="160d5-334">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-335">CC002</span><span class="sxs-lookup"><span data-stu-id="160d5-335">CC002</span></span></td>
<td><span data-ttu-id="160d5-336">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="160d5-336">Finance</span></span></td>
<td><span data-ttu-id="160d5-337">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-337">10001</span></span></td>
<td><span data-ttu-id="160d5-338">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-338">Electricity</span></span></td>
<td><span data-ttu-id="160d5-339">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-339">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-340">500,00</span><span class="sxs-lookup"><span data-stu-id="160d5-340">500.00</span></span></td>
<td><span data-ttu-id="160d5-341">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-342">CC099</span><span class="sxs-lookup"><span data-stu-id="160d5-342">CC099</span></span></td>
<td><span data-ttu-id="160d5-343">Oletuskustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="160d5-343">Default cost center</span></span></td>
<td><span data-ttu-id="160d5-344">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-344">10001</span></span></td>
<td><span data-ttu-id="160d5-345">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-345">Electricity</span></span></td>
<td><span data-ttu-id="160d5-346">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-346">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="160d5-347">-9,000.00</span></span></td>
<td><span data-ttu-id="160d5-348">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-349">CC001</span><span class="sxs-lookup"><span data-stu-id="160d5-349">CC001</span></span></td>
<td><span data-ttu-id="160d5-350">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="160d5-350">HR</span></span></td>
<td><span data-ttu-id="160d5-351">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-351">10001</span></span></td>
<td><span data-ttu-id="160d5-352">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-352">Electricity</span></span></td>
<td><span data-ttu-id="160d5-353">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-353">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="160d5-354">1,285.71</span></span></td>
<td><span data-ttu-id="160d5-355">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-356">CC002</span><span class="sxs-lookup"><span data-stu-id="160d5-356">CC002</span></span></td>
<td><span data-ttu-id="160d5-357">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="160d5-357">Finance</span></span></td>
<td><span data-ttu-id="160d5-358">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-358">10001</span></span></td>
<td><span data-ttu-id="160d5-359">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-359">Electricity</span></span></td>
<td><span data-ttu-id="160d5-360">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-360">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="160d5-361">7,714.29</span></span></td>
<td><span data-ttu-id="160d5-362">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="160d5-363">Lisätietoja on kohdassa [Jakelukäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="160d5-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="160d5-364">Vaihe 3: Käsittele yleiskustannustason laskenta</span><span class="sxs-lookup"><span data-stu-id="160d5-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="160d5-365">Yleiskustannustasolla veloitetaan yksi tai useampi määrätty kustannusobjekti.</span><span class="sxs-lookup"><span data-stu-id="160d5-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="160d5-366">Veloitus perustuu ennalta määrättyyn kustannustasoon sekä määritetyn kohdistusperusteen suuruuteen.</span><span class="sxs-lookup"><span data-stu-id="160d5-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="160d5-367">Määritä yleiskustannustaso.</span><span class="sxs-lookup"><span data-stu-id="160d5-367">Define the overhead rate</span></span>

<span data-ttu-id="160d5-368">Kustannusobjekti CC001 HR vaikuttaa joukkoon sisäisiä projekteja.</span><span class="sxs-lookup"><span data-stu-id="160d5-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="160d5-369">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon projektit.</span><span class="sxs-lookup"><span data-stu-id="160d5-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="160d5-370">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-370">Cost object</span></span></th>
<th><span data-ttu-id="160d5-371">Tunnit</span><span class="sxs-lookup"><span data-stu-id="160d5-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="160d5-372">Proj 1</span></span></td>
<td><span data-ttu-id="160d5-373">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="160d5-373">Project 1</span></span></td>
<td><span data-ttu-id="160d5-374">3</span><span class="sxs-lookup"><span data-stu-id="160d5-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="160d5-375">Proj 2</span></span></td>
<td><span data-ttu-id="160d5-376">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="160d5-376">Project 2</span></span></td>
<td><span data-ttu-id="160d5-377">1</span><span class="sxs-lookup"><span data-stu-id="160d5-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="160d5-378">Kustannusprojektien osuudelle on määritetty ennalta kustannushinta.</span><span class="sxs-lookup"><span data-stu-id="160d5-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="160d5-379">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-379">Cost object</span></span></th>
<th><span data-ttu-id="160d5-380">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="160d5-380">Cost element</span></span></th>
<th><span data-ttu-id="160d5-381">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="160d5-381">Cost behavior</span></span></th>
<th><span data-ttu-id="160d5-382">Yksiköt</span><span class="sxs-lookup"><span data-stu-id="160d5-382">Units</span></span></th>
<th><span data-ttu-id="160d5-383">Osuus</span><span class="sxs-lookup"><span data-stu-id="160d5-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-384">CC001</span><span class="sxs-lookup"><span data-stu-id="160d5-384">CC001</span></span></td>
<td><span data-ttu-id="160d5-385">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="160d5-385">HR</span></span></td>
<td><span data-ttu-id="160d5-386">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-386">10001</span></span></td>
<td><span data-ttu-id="160d5-387">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-387">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-388">1</span><span class="sxs-lookup"><span data-stu-id="160d5-388">1</span></span></td>
<td><span data-ttu-id="160d5-389">10</span><span class="sxs-lookup"><span data-stu-id="160d5-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="160d5-390">Seuraavassa taulukossa on esitetty tulos, kun Henkilöstöhallinnon projekteja käytetään kohdistusperusteena.</span><span class="sxs-lookup"><span data-stu-id="160d5-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="160d5-391">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-391">Cost object</span></span></th>
<th><span data-ttu-id="160d5-392">Suuruus</span><span class="sxs-lookup"><span data-stu-id="160d5-392">Magnitude</span></span></th>
<th><span data-ttu-id="160d5-393">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="160d5-393">Cost element</span></span></th>
<th><span data-ttu-id="160d5-394">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="160d5-394">Allocation factor</span></span></th>
<th><span data-ttu-id="160d5-395">Summa</span><span class="sxs-lookup"><span data-stu-id="160d5-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="160d5-396">Proj 1</span></span></td>
<td><span data-ttu-id="160d5-397">Projekti 1</span><span class="sxs-lookup"><span data-stu-id="160d5-397">Project 1</span></span></td>
<td><span data-ttu-id="160d5-398">3</span><span class="sxs-lookup"><span data-stu-id="160d5-398">3</span></span></td>
<td><span data-ttu-id="160d5-399">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-399">10001</span></span></td>
<td><span data-ttu-id="160d5-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="160d5-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="160d5-401">30,00</span><span class="sxs-lookup"><span data-stu-id="160d5-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="160d5-402">Proj 2</span></span></td>
<td><span data-ttu-id="160d5-403">Projekti 2</span><span class="sxs-lookup"><span data-stu-id="160d5-403">Project 2</span></span></td>
<td><span data-ttu-id="160d5-404">1</span><span class="sxs-lookup"><span data-stu-id="160d5-404">1</span></span></td>
<td><span data-ttu-id="160d5-405">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-405">10001</span></span></td>
<td><span data-ttu-id="160d5-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="160d5-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="160d5-407">10,00</span><span class="sxs-lookup"><span data-stu-id="160d5-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="160d5-408">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="160d5-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="160d5-409">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="160d5-409">Journal</span></span></th>
<th><span data-ttu-id="160d5-410">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="160d5-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="160d5-411">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="160d5-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="160d5-412">Versio</span><span class="sxs-lookup"><span data-stu-id="160d5-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-413">00003</span><span class="sxs-lookup"><span data-stu-id="160d5-413">00003</span></span></td>
<td><span data-ttu-id="160d5-414">Yleiskustannustason laskelman kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="160d5-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="160d5-415">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="160d5-415">Fiscal</span></span></td>
<td><span data-ttu-id="160d5-416">2017</span><span class="sxs-lookup"><span data-stu-id="160d5-416">2017</span></span></td>
<td><span data-ttu-id="160d5-417">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="160d5-417">Period 1</span></span></td>
<td><span data-ttu-id="160d5-418">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="160d5-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="160d5-419">Kirjauskansioviennit (Yleiskustannustason laskennan kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="160d5-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="160d5-420">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="160d5-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="160d5-421">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-421">Cost object</span></span></th>
<th><span data-ttu-id="160d5-422">Suuruus</span><span class="sxs-lookup"><span data-stu-id="160d5-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-423">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="160d5-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="160d5-424">Proj 1</span></span></td>
<td><span data-ttu-id="160d5-425">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="160d5-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="160d5-426">3,00</span><span class="sxs-lookup"><span data-stu-id="160d5-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-427">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="160d5-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="160d5-428">Proj 2</span></span></td>
<td><span data-ttu-id="160d5-429">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="160d5-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="160d5-430">1,00</span><span class="sxs-lookup"><span data-stu-id="160d5-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="160d5-431">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="160d5-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="160d5-432">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="160d5-433">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="160d5-433">Cost element</span></span></th>
<th><span data-ttu-id="160d5-434">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="160d5-434">Cost behavior</span></span></th>
<th><span data-ttu-id="160d5-435">Summa</span><span class="sxs-lookup"><span data-stu-id="160d5-435">Amount</span></span></th>
<th><span data-ttu-id="160d5-436">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="160d5-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="160d5-437">CC0001</span></span></td>
<td><span data-ttu-id="160d5-438">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="160d5-438">HR</span></span></td>
<td><span data-ttu-id="160d5-439">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-439">10001</span></span></td>
<td><span data-ttu-id="160d5-440">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-440">Electricity</span></span></td>
<td><span data-ttu-id="160d5-441">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-441">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="160d5-442">-30.00</span></span></td>
<td><span data-ttu-id="160d5-443">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="160d5-444">Proj 1</span></span></td>
<td><span data-ttu-id="160d5-445">Sisäinen proj 1</span><span class="sxs-lookup"><span data-stu-id="160d5-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="160d5-446">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-446">10001</span></span></td>
<td><span data-ttu-id="160d5-447">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-447">Electricity</span></span></td>
<td><span data-ttu-id="160d5-448">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-448">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-449">30,00</span><span class="sxs-lookup"><span data-stu-id="160d5-449">30.00</span></span></td>
<td><span data-ttu-id="160d5-450">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-451">CC001</span><span class="sxs-lookup"><span data-stu-id="160d5-451">CC001</span></span></td>
<td><span data-ttu-id="160d5-452">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="160d5-452">HR</span></span></td>
<td><span data-ttu-id="160d5-453">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-453">10001</span></span></td>
<td><span data-ttu-id="160d5-454">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-454">Electricity</span></span></td>
<td><span data-ttu-id="160d5-455">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-455">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="160d5-456">-10.00</span></span></td>
<td><span data-ttu-id="160d5-457">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="160d5-458">Proj 2</span></span></td>
<td><span data-ttu-id="160d5-459">Sisäinen proj 2</span><span class="sxs-lookup"><span data-stu-id="160d5-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="160d5-460">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-460">10001</span></span></td>
<td><span data-ttu-id="160d5-461">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-461">Electricity</span></span></td>
<td><span data-ttu-id="160d5-462">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-462">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-463">10.00</span><span class="sxs-lookup"><span data-stu-id="160d5-463">10.00</span></span></td>
<td><span data-ttu-id="160d5-464">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="160d5-465">Lisätietoja on kohdassa [Yleisen laskennan suorittaminen](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="160d5-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="160d5-466">Vaihe 4: Käsittele kustannusten kohdistuksen laskenta</span><span class="sxs-lookup"><span data-stu-id="160d5-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="160d5-467">Kohdistuksella kustannusobjektin saldo liitetään toisiin kustannusobjekteihin käyttämällä kohdistusperustetta.</span><span class="sxs-lookup"><span data-stu-id="160d5-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="160d5-468">Finance tukee vastavuoroista kohdistusmenetelmää.</span><span class="sxs-lookup"><span data-stu-id="160d5-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="160d5-469">Vastavuoroisessa kohdistusmenetelmässä tunnistetaan oheiskustannusobjektien käyttämät, keskinäiset palvelut täysin.</span><span class="sxs-lookup"><span data-stu-id="160d5-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="160d5-470">Järjestelmä määrittää oikean kohdistusjärjestyksen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="160d5-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="160d5-471">Kustannusobjektin saldo kohdistetaan yhdellä kohdistusperusteella.</span><span class="sxs-lookup"><span data-stu-id="160d5-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="160d5-472">Kustannusobjektien dimensiot ja niiden vastaavat jäsenet ylittävät kohdistukset ovat tuettuja.</span><span class="sxs-lookup"><span data-stu-id="160d5-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="160d5-473">Kustannusseurantayksikkö hallitsee kohdistusjärjestystä.</span><span class="sxs-lookup"><span data-stu-id="160d5-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="160d5-474">[![Vastavuoroinen menetelmä](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="160d5-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="160d5-475">Määritä kustannuksen kohdistus</span><span class="sxs-lookup"><span data-stu-id="160d5-475">Define the cost allocation</span></span>

<span data-ttu-id="160d5-476">Tämä on yksinkertainen esimerkki, jossa kerrotaan, miten voit jäljittää kustannuksen virran.</span><span class="sxs-lookup"><span data-stu-id="160d5-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="160d5-477">Kustannusobjekti CC001 HR liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="160d5-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="160d5-478">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="160d5-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="160d5-479">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-479">Cost object</span></span></th>
<th><span data-ttu-id="160d5-480">HR-palvelut</span><span class="sxs-lookup"><span data-stu-id="160d5-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-481">CC002</span><span class="sxs-lookup"><span data-stu-id="160d5-481">CC002</span></span></td>
<td><span data-ttu-id="160d5-482">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="160d5-482">Finance</span></span></td>
<td><span data-ttu-id="160d5-483">35</span><span class="sxs-lookup"><span data-stu-id="160d5-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-484">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-484">CC003</span></span></td>
<td><span data-ttu-id="160d5-485">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="160d5-485">Assembly</span></span></td>
<td><span data-ttu-id="160d5-486">55</span><span class="sxs-lookup"><span data-stu-id="160d5-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-487">CC004</span><span class="sxs-lookup"><span data-stu-id="160d5-487">CC004</span></span></td>
<td><span data-ttu-id="160d5-488">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="160d5-488">Packaging</span></span></td>
<td><span data-ttu-id="160d5-489">10</span><span class="sxs-lookup"><span data-stu-id="160d5-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="160d5-490">Kustannusobjekti CC002 Taloushallinto liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="160d5-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="160d5-491">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Taloushallinnon palvelut.</span><span class="sxs-lookup"><span data-stu-id="160d5-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="160d5-492">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-492">Cost object</span></span></th>
<th><span data-ttu-id="160d5-493">Taloushallinnon palvelut</span><span class="sxs-lookup"><span data-stu-id="160d5-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-494">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-494">CC003</span></span></td>
<td><span data-ttu-id="160d5-495">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="160d5-495">Assembly</span></span></td>
<td><span data-ttu-id="160d5-496">65</span><span class="sxs-lookup"><span data-stu-id="160d5-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-497">CC004</span><span class="sxs-lookup"><span data-stu-id="160d5-497">CC004</span></span></td>
<td><span data-ttu-id="160d5-498">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="160d5-498">Packaging</span></span></td>
<td><span data-ttu-id="160d5-499">35</span><span class="sxs-lookup"><span data-stu-id="160d5-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="160d5-500">Kustannusobjekti CC003 Kokoonpano liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="160d5-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="160d5-501">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Kokoonpanopalvelut.</span><span class="sxs-lookup"><span data-stu-id="160d5-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="160d5-502">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-502">Cost object</span></span></th>
<th><span data-ttu-id="160d5-503">Kokoonpanopalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="160d5-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-504">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-504">Prod 1</span></span></td>
<td><span data-ttu-id="160d5-505">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-505">Product 1</span></span></td>
<td><span data-ttu-id="160d5-506">60</span><span class="sxs-lookup"><span data-stu-id="160d5-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-507">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-507">Prod 2</span></span></td>
<td><span data-ttu-id="160d5-508">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-508">Product 2</span></span></td>
<td><span data-ttu-id="160d5-509">20</span><span class="sxs-lookup"><span data-stu-id="160d5-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="160d5-510">Kustannusobjekti CC004 Pakkaus liittyy useaan kustannusobjektiin.</span><span class="sxs-lookup"><span data-stu-id="160d5-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="160d5-511">Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Pakkauspalvelut.</span><span class="sxs-lookup"><span data-stu-id="160d5-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="160d5-512">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-512">Cost object</span></span></th>
<th><span data-ttu-id="160d5-513">Pakkauspalvelut (tuntia)</span><span class="sxs-lookup"><span data-stu-id="160d5-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-514">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-514">Prod 1</span></span></td>
<td><span data-ttu-id="160d5-515">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-515">Product 1</span></span></td>
<td><span data-ttu-id="160d5-516">80</span><span class="sxs-lookup"><span data-stu-id="160d5-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-517">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-517">Prod 2</span></span></td>
<td><span data-ttu-id="160d5-518">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-518">Product 2</span></span></td>
<td><span data-ttu-id="160d5-519">15</span><span class="sxs-lookup"><span data-stu-id="160d5-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="160d5-520">Tilastomittaukset, kuten tämän tuotteen kuluttamat tuotantotunnit, voidaan johtaa lähdetiedoista.</span><span class="sxs-lookup"><span data-stu-id="160d5-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="160d5-521">Lisätietoja on kohdassa [Tilastomittauksen lähdemalli](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="160d5-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="160d5-522">Seuraavassa taulukossa näytetään tulos, kun henkilöstöhallinnon palveluja käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="160d5-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="160d5-523">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-523">Cost object</span></span></th>
<th><span data-ttu-id="160d5-524">Suuruus</span><span class="sxs-lookup"><span data-stu-id="160d5-524">Magnitude</span></span></th>
<th><span data-ttu-id="160d5-525">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="160d5-525">Allocation factor</span></span></th>
<th><span data-ttu-id="160d5-526">Summa</span><span class="sxs-lookup"><span data-stu-id="160d5-526">Amount</span></span></th>
<th><span data-ttu-id="160d5-527">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="160d5-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-528">CC002</span><span class="sxs-lookup"><span data-stu-id="160d5-528">CC002</span></span></td>
<td><span data-ttu-id="160d5-529">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="160d5-529">Finance</span></span></td>
<td><span data-ttu-id="160d5-530">35</span><span class="sxs-lookup"><span data-stu-id="160d5-530">35</span></span></td>
<td><span data-ttu-id="160d5-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="160d5-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="160d5-532">175.00</span><span class="sxs-lookup"><span data-stu-id="160d5-532">175.00</span></span></td>
<td><span data-ttu-id="160d5-533">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-534">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-534">CC003</span></span></td>
<td><span data-ttu-id="160d5-535">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="160d5-535">Assembly</span></span></td>
<td><span data-ttu-id="160d5-536">55</span><span class="sxs-lookup"><span data-stu-id="160d5-536">55</span></span></td>
<td><span data-ttu-id="160d5-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="160d5-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="160d5-538">275.00</span><span class="sxs-lookup"><span data-stu-id="160d5-538">275.00</span></span></td>
<td><span data-ttu-id="160d5-539">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-540">CC004</span><span class="sxs-lookup"><span data-stu-id="160d5-540">CC004</span></span></td>
<td><span data-ttu-id="160d5-541">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="160d5-541">Packaging</span></span></td>
<td><span data-ttu-id="160d5-542">10</span><span class="sxs-lookup"><span data-stu-id="160d5-542">10</span></span></td>
<td><span data-ttu-id="160d5-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="160d5-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="160d5-544">50,00</span><span class="sxs-lookup"><span data-stu-id="160d5-544">50.00</span></span></td>
<td><span data-ttu-id="160d5-545">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-546">CC002</span><span class="sxs-lookup"><span data-stu-id="160d5-546">CC002</span></span></td>
<td><span data-ttu-id="160d5-547">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="160d5-547">Finance</span></span></td>
<td><span data-ttu-id="160d5-548">35</span><span class="sxs-lookup"><span data-stu-id="160d5-548">35</span></span></td>
<td><span data-ttu-id="160d5-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="160d5-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="160d5-550">436.00</span><span class="sxs-lookup"><span data-stu-id="160d5-550">436.00</span></span></td>
<td><span data-ttu-id="160d5-551">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-552">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-552">CC003</span></span></td>
<td><span data-ttu-id="160d5-553">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="160d5-553">Assembly</span></span></td>
<td><span data-ttu-id="160d5-554">55</span><span class="sxs-lookup"><span data-stu-id="160d5-554">55</span></span></td>
<td><span data-ttu-id="160d5-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="160d5-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="160d5-556">685.14</span><span class="sxs-lookup"><span data-stu-id="160d5-556">685.14</span></span></td>
<td><span data-ttu-id="160d5-557">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-558">CC004</span><span class="sxs-lookup"><span data-stu-id="160d5-558">CC004</span></span></td>
<td><span data-ttu-id="160d5-559">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="160d5-559">Packaging</span></span></td>
<td><span data-ttu-id="160d5-560">10</span><span class="sxs-lookup"><span data-stu-id="160d5-560">10</span></span></td>
<td><span data-ttu-id="160d5-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="160d5-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="160d5-562">124.57</span><span class="sxs-lookup"><span data-stu-id="160d5-562">124.57</span></span></td>
<td><span data-ttu-id="160d5-563">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="160d5-564">Seuraavassa taulukossa näytetään tulos, kun Taloushallinnon palveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="160d5-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="160d5-565">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-565">Cost object</span></span></th>
<th><span data-ttu-id="160d5-566">Suuruus</span><span class="sxs-lookup"><span data-stu-id="160d5-566">Magnitude</span></span></th>
<th><span data-ttu-id="160d5-567">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="160d5-567">Allocation factor</span></span></th>
<th><span data-ttu-id="160d5-568">Summa</span><span class="sxs-lookup"><span data-stu-id="160d5-568">Amount</span></span></th>
<th><span data-ttu-id="160d5-569">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="160d5-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-570">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-570">CC003</span></span></td>
<td><span data-ttu-id="160d5-571">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="160d5-571">Assembly</span></span></td>
<td><span data-ttu-id="160d5-572">65</span><span class="sxs-lookup"><span data-stu-id="160d5-572">65</span></span></td>
<td><span data-ttu-id="160d5-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="160d5-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="160d5-574">438.75</span><span class="sxs-lookup"><span data-stu-id="160d5-574">438.75</span></span></td>
<td><span data-ttu-id="160d5-575">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-576">CC004</span><span class="sxs-lookup"><span data-stu-id="160d5-576">CC004</span></span></td>
<td><span data-ttu-id="160d5-577">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="160d5-577">Packaging</span></span></td>
<td><span data-ttu-id="160d5-578">35</span><span class="sxs-lookup"><span data-stu-id="160d5-578">35</span></span></td>
<td><span data-ttu-id="160d5-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="160d5-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="160d5-580">236.25</span><span class="sxs-lookup"><span data-stu-id="160d5-580">236.25</span></span></td>
<td><span data-ttu-id="160d5-581">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-582">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-582">CC003</span></span></td>
<td><span data-ttu-id="160d5-583">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="160d5-583">Assembly</span></span></td>
<td><span data-ttu-id="160d5-584">65</span><span class="sxs-lookup"><span data-stu-id="160d5-584">65</span></span></td>
<td><span data-ttu-id="160d5-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="160d5-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="160d5-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="160d5-586">5,297.69</span></span></td>
<td><span data-ttu-id="160d5-587">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-588">CC004</span><span class="sxs-lookup"><span data-stu-id="160d5-588">CC004</span></span></td>
<td><span data-ttu-id="160d5-589">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="160d5-589">Packaging</span></span></td>
<td><span data-ttu-id="160d5-590">35</span><span class="sxs-lookup"><span data-stu-id="160d5-590">35</span></span></td>
<td><span data-ttu-id="160d5-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="160d5-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="160d5-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="160d5-592">2,852.60</span></span></td>
<td><span data-ttu-id="160d5-593">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="160d5-594">Seuraavassa taulukossa näytetään tulos, kun Kokoonpanopalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="160d5-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="160d5-595">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-595">Cost object</span></span></th>
<th><span data-ttu-id="160d5-596">Suuruus</span><span class="sxs-lookup"><span data-stu-id="160d5-596">Magnitude</span></span></th>
<th><span data-ttu-id="160d5-597">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="160d5-597">Allocation factor</span></span></th>
<th><span data-ttu-id="160d5-598">Summa</span><span class="sxs-lookup"><span data-stu-id="160d5-598">Amount</span></span></th>
<th><span data-ttu-id="160d5-599">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="160d5-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-600">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-600">Prod 1</span></span></td>
<td><span data-ttu-id="160d5-601">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-601">Product 1</span></span></td>
<td><span data-ttu-id="160d5-602">60</span><span class="sxs-lookup"><span data-stu-id="160d5-602">60</span></span></td>
<td><span data-ttu-id="160d5-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="160d5-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="160d5-604">535.31</span><span class="sxs-lookup"><span data-stu-id="160d5-604">535.31</span></span></td>
<td><span data-ttu-id="160d5-605">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-606">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-606">Prod 2</span></span></td>
<td><span data-ttu-id="160d5-607">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-607">Product 2</span></span></td>
<td><span data-ttu-id="160d5-608">20</span><span class="sxs-lookup"><span data-stu-id="160d5-608">20</span></span></td>
<td><span data-ttu-id="160d5-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="160d5-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="160d5-610">178.44</span><span class="sxs-lookup"><span data-stu-id="160d5-610">178.44</span></span></td>
<td><span data-ttu-id="160d5-611">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-612">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-612">Prod 1</span></span></td>
<td><span data-ttu-id="160d5-613">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-613">Product 1</span></span></td>
<td><span data-ttu-id="160d5-614">60</span><span class="sxs-lookup"><span data-stu-id="160d5-614">60</span></span></td>
<td><span data-ttu-id="160d5-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="160d5-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="160d5-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="160d5-616">4,487.12</span></span></td>
<td><span data-ttu-id="160d5-617">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-618">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-618">Prod 2</span></span></td>
<td><span data-ttu-id="160d5-619">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-619">Product 2</span></span></td>
<td><span data-ttu-id="160d5-620">20</span><span class="sxs-lookup"><span data-stu-id="160d5-620">20</span></span></td>
<td><span data-ttu-id="160d5-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="160d5-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="160d5-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="160d5-622">1,495.71</span></span></td>
<td><span data-ttu-id="160d5-623">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="160d5-624">Seuraavassa taulukossa näytetään tulos, kun Pakkauspalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).</span><span class="sxs-lookup"><span data-stu-id="160d5-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="160d5-625">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-625">Cost object</span></span></th>
<th><span data-ttu-id="160d5-626">Suuruus</span><span class="sxs-lookup"><span data-stu-id="160d5-626">Magnitude</span></span></th>
<th><span data-ttu-id="160d5-627">Kohdistuskerroin</span><span class="sxs-lookup"><span data-stu-id="160d5-627">Allocation factor</span></span></th>
<th><span data-ttu-id="160d5-628">Summa</span><span class="sxs-lookup"><span data-stu-id="160d5-628">Amount</span></span></th>
<th><span data-ttu-id="160d5-629">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="160d5-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-630">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-630">Prod 1</span></span></td>
<td><span data-ttu-id="160d5-631">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-631">Product 1</span></span></td>
<td><span data-ttu-id="160d5-632">80</span><span class="sxs-lookup"><span data-stu-id="160d5-632">80</span></span></td>
<td><span data-ttu-id="160d5-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="160d5-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="160d5-634">241.05</span><span class="sxs-lookup"><span data-stu-id="160d5-634">241.05</span></span></td>
<td><span data-ttu-id="160d5-635">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-636">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-636">Prod 2</span></span></td>
<td><span data-ttu-id="160d5-637">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-637">Product 2</span></span></td>
<td><span data-ttu-id="160d5-638">15</span><span class="sxs-lookup"><span data-stu-id="160d5-638">15</span></span></td>
<td><span data-ttu-id="160d5-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="160d5-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="160d5-640">45.20</span><span class="sxs-lookup"><span data-stu-id="160d5-640">45.20</span></span></td>
<td><span data-ttu-id="160d5-641">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-642">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-642">Prod 1</span></span></td>
<td><span data-ttu-id="160d5-643">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-643">Product 1</span></span></td>
<td><span data-ttu-id="160d5-644">80</span><span class="sxs-lookup"><span data-stu-id="160d5-644">80</span></span></td>
<td><span data-ttu-id="160d5-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="160d5-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="160d5-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="160d5-646">2,507.09</span></span></td>
<td><span data-ttu-id="160d5-647">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-648">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-648">Prod 2</span></span></td>
<td><span data-ttu-id="160d5-649">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-649">Product 2</span></span></td>
<td><span data-ttu-id="160d5-650">15</span><span class="sxs-lookup"><span data-stu-id="160d5-650">15</span></span></td>
<td><span data-ttu-id="160d5-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="160d5-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="160d5-652">470.08</span><span class="sxs-lookup"><span data-stu-id="160d5-652">470.08</span></span></td>
<td><span data-ttu-id="160d5-653">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="160d5-654">Kirjauskansioviennit (kustannusobjektin saldon kirjauskansioviennit)</span><span class="sxs-lookup"><span data-stu-id="160d5-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="160d5-655">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="160d5-655">Journal</span></span></th>
<th><span data-ttu-id="160d5-656">Kirjauskansion tyyppi</span><span class="sxs-lookup"><span data-stu-id="160d5-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="160d5-657">Kirjanpidon vuosikalenterin kausi</span><span class="sxs-lookup"><span data-stu-id="160d5-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="160d5-658">Versio</span><span class="sxs-lookup"><span data-stu-id="160d5-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-659">00004</span><span class="sxs-lookup"><span data-stu-id="160d5-659">00004</span></span></td>
<td><span data-ttu-id="160d5-660">Kustannusten kohdistuskirjauskansio</span><span class="sxs-lookup"><span data-stu-id="160d5-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="160d5-661">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="160d5-661">Fiscal</span></span></td>
<td><span data-ttu-id="160d5-662">2017</span><span class="sxs-lookup"><span data-stu-id="160d5-662">2017</span></span></td>
<td><span data-ttu-id="160d5-663">Kausi 1</span><span class="sxs-lookup"><span data-stu-id="160d5-663">Period 1</span></span></td>
<td><span data-ttu-id="160d5-664">Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</span><span class="sxs-lookup"><span data-stu-id="160d5-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="160d5-665">Kirjauskansion rivit</span><span class="sxs-lookup"><span data-stu-id="160d5-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="160d5-666">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="160d5-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="160d5-667">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="160d5-668">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="160d5-668">Cost element</span></span></th>
<th><span data-ttu-id="160d5-669">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="160d5-669">Cost behavior</span></span></th>
<th><span data-ttu-id="160d5-670">Summa</span><span class="sxs-lookup"><span data-stu-id="160d5-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-671">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="160d5-672">CC001</span><span class="sxs-lookup"><span data-stu-id="160d5-672">CC001</span></span></td>
<td><span data-ttu-id="160d5-673">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="160d5-673">HR</span></span></td>
<td><span data-ttu-id="160d5-674">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-674">10001</span></span></td>
<td><span data-ttu-id="160d5-675">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-675">Electricity</span></span></td>
<td><span data-ttu-id="160d5-676">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-676">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-677">500,00</span><span class="sxs-lookup"><span data-stu-id="160d5-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-678">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="160d5-679">CC001</span><span class="sxs-lookup"><span data-stu-id="160d5-679">CC001</span></span></td>
<td><span data-ttu-id="160d5-680">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="160d5-680">HR</span></span></td>
<td><span data-ttu-id="160d5-681">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-681">10001</span></span></td>
<td><span data-ttu-id="160d5-682">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-682">Electricity</span></span></td>
<td><span data-ttu-id="160d5-683">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-683">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="160d5-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-685">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="160d5-686">CC002</span><span class="sxs-lookup"><span data-stu-id="160d5-686">CC002</span></span></td>
<td><span data-ttu-id="160d5-687">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="160d5-687">Finance</span></span></td>
<td><span data-ttu-id="160d5-688">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-688">10001</span></span></td>
<td><span data-ttu-id="160d5-689">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-689">Electricity</span></span></td>
<td><span data-ttu-id="160d5-690">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-690">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-691">675.00</span><span class="sxs-lookup"><span data-stu-id="160d5-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-692">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="160d5-693">CC002</span><span class="sxs-lookup"><span data-stu-id="160d5-693">CC002</span></span></td>
<td><span data-ttu-id="160d5-694">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="160d5-694">Finance</span></span></td>
<td><span data-ttu-id="160d5-695">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-695">10001</span></span></td>
<td><span data-ttu-id="160d5-696">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-696">Electricity</span></span></td>
<td><span data-ttu-id="160d5-697">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-697">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="160d5-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-699">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="160d5-700">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-700">CC003</span></span></td>
<td><span data-ttu-id="160d5-701">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="160d5-701">Assembly</span></span></td>
<td><span data-ttu-id="160d5-702">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-702">10001</span></span></td>
<td><span data-ttu-id="160d5-703">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-703">Electricity</span></span></td>
<td><span data-ttu-id="160d5-704">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-704">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-705">713.75</span><span class="sxs-lookup"><span data-stu-id="160d5-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-706">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="160d5-707">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-707">CC003</span></span></td>
<td><span data-ttu-id="160d5-708">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="160d5-708">Assembly</span></span></td>
<td><span data-ttu-id="160d5-709">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-709">10001</span></span></td>
<td><span data-ttu-id="160d5-710">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-710">Electricity</span></span></td>
<td><span data-ttu-id="160d5-711">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-711">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="160d5-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-713">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="160d5-714">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-714">CC003</span></span></td>
<td><span data-ttu-id="160d5-715">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="160d5-715">Packaging</span></span></td>
<td><span data-ttu-id="160d5-716">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-716">10001</span></span></td>
<td><span data-ttu-id="160d5-717">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-717">Electricity</span></span></td>
<td><span data-ttu-id="160d5-718">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-718">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-719">286.25</span><span class="sxs-lookup"><span data-stu-id="160d5-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-720">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="160d5-721">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-721">CC003</span></span></td>
<td><span data-ttu-id="160d5-722">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="160d5-722">Packaging</span></span></td>
<td><span data-ttu-id="160d5-723">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-723">10001</span></span></td>
<td><span data-ttu-id="160d5-724">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-724">Electricity</span></span></td>
<td><span data-ttu-id="160d5-725">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-725">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="160d5-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-727">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="160d5-728">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-728">Prod 1</span></span></td>
<td><span data-ttu-id="160d5-729">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-729">Product 1</span></span></td>
<td><span data-ttu-id="160d5-730">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-730">10001</span></span></td>
<td><span data-ttu-id="160d5-731">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-731">Electricity</span></span></td>
<td><span data-ttu-id="160d5-732">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-732">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-733">776.36</span><span class="sxs-lookup"><span data-stu-id="160d5-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-734">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="160d5-735">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-735">Prod 1</span></span></td>
<td><span data-ttu-id="160d5-736">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-736">Product 1</span></span></td>
<td><span data-ttu-id="160d5-737">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-737">10001</span></span></td>
<td><span data-ttu-id="160d5-738">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-738">Electricity</span></span></td>
<td><span data-ttu-id="160d5-739">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-739">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="160d5-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-741">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="160d5-742">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-742">Prod 2</span></span></td>
<td><span data-ttu-id="160d5-743">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-743">Product 1</span></span></td>
<td><span data-ttu-id="160d5-744">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-744">10001</span></span></td>
<td><span data-ttu-id="160d5-745">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-745">Electricity</span></span></td>
<td><span data-ttu-id="160d5-746">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-746">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-747">223.64</span><span class="sxs-lookup"><span data-stu-id="160d5-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-748">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="160d5-749">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-749">Prod 2</span></span></td>
<td><span data-ttu-id="160d5-750">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-750">Product 1</span></span></td>
<td><span data-ttu-id="160d5-751">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-751">10001</span></span></td>
<td><span data-ttu-id="160d5-752">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-752">Electricity</span></span></td>
<td><span data-ttu-id="160d5-753">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-753">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="160d5-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="160d5-755">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="160d5-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="160d5-756">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="160d5-757">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="160d5-757">Cost element</span></span></th>
<th><span data-ttu-id="160d5-758">Kustannustoiminta</span><span class="sxs-lookup"><span data-stu-id="160d5-758">Cost behavior</span></span></th>
<th><span data-ttu-id="160d5-759">Summa</span><span class="sxs-lookup"><span data-stu-id="160d5-759">Amount</span></span></th>
<th><span data-ttu-id="160d5-760">Kirjauspäivä</span><span class="sxs-lookup"><span data-stu-id="160d5-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="160d5-761">CC001</span><span class="sxs-lookup"><span data-stu-id="160d5-761">CC001</span></span></td>
<td><span data-ttu-id="160d5-762">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="160d5-762">HR</span></span></td>
<td><span data-ttu-id="160d5-763">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-763">10001</span></span></td>
<td><span data-ttu-id="160d5-764">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-764">Electricity</span></span></td>
<td><span data-ttu-id="160d5-765">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-765">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="160d5-766">-500.00</span></span></td>
<td><span data-ttu-id="160d5-767">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-768">CC002</span><span class="sxs-lookup"><span data-stu-id="160d5-768">CC002</span></span></td>
<td><span data-ttu-id="160d5-769">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="160d5-769">Finance</span></span></td>
<td><span data-ttu-id="160d5-770">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-770">10001</span></span></td>
<td><span data-ttu-id="160d5-771">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-771">Electricity</span></span></td>
<td><span data-ttu-id="160d5-772">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-772">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-773">175.00</span><span class="sxs-lookup"><span data-stu-id="160d5-773">175.00</span></span></td>
<td><span data-ttu-id="160d5-774">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-775">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-775">CC003</span></span></td>
<td><span data-ttu-id="160d5-776">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="160d5-776">Assembly</span></span></td>
<td><span data-ttu-id="160d5-777">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-777">10001</span></span></td>
<td><span data-ttu-id="160d5-778">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-778">Electricity</span></span></td>
<td><span data-ttu-id="160d5-779">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-779">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-780">275.00</span><span class="sxs-lookup"><span data-stu-id="160d5-780">275.00</span></span></td>
<td><span data-ttu-id="160d5-781">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-782">CC004</span><span class="sxs-lookup"><span data-stu-id="160d5-782">CC004</span></span></td>
<td><span data-ttu-id="160d5-783">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="160d5-783">Packaging</span></span></td>
<td><span data-ttu-id="160d5-784">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-784">10001</span></span></td>
<td><span data-ttu-id="160d5-785">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-785">Electricity</span></span></td>
<td><span data-ttu-id="160d5-786">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-786">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-787">50,00</span><span class="sxs-lookup"><span data-stu-id="160d5-787">50,00</span></span></td>
<td><span data-ttu-id="160d5-788">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-789">CC001</span><span class="sxs-lookup"><span data-stu-id="160d5-789">CC001</span></span></td>
<td><span data-ttu-id="160d5-790">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="160d5-790">HR</span></span></td>
<td><span data-ttu-id="160d5-791">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-791">10001</span></span></td>
<td><span data-ttu-id="160d5-792">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-792">Electricity</span></span></td>
<td><span data-ttu-id="160d5-793">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-793">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="160d5-794">-1,245.71</span></span></td>
<td><span data-ttu-id="160d5-795">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-796">CC002</span><span class="sxs-lookup"><span data-stu-id="160d5-796">CC002</span></span></td>
<td><span data-ttu-id="160d5-797">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="160d5-797">Finance</span></span></td>
<td><span data-ttu-id="160d5-798">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-798">10001</span></span></td>
<td><span data-ttu-id="160d5-799">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-799">Electricity</span></span></td>
<td><span data-ttu-id="160d5-800">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-800">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-801">436.00</span><span class="sxs-lookup"><span data-stu-id="160d5-801">436.00</span></span></td>
<td><span data-ttu-id="160d5-802">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-803">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-803">CC003</span></span></td>
<td><span data-ttu-id="160d5-804">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="160d5-804">Assembly</span></span></td>
<td><span data-ttu-id="160d5-805">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-805">10001</span></span></td>
<td><span data-ttu-id="160d5-806">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-806">Electricity</span></span></td>
<td><span data-ttu-id="160d5-807">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-807">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-808">685.14</span><span class="sxs-lookup"><span data-stu-id="160d5-808">685.14</span></span></td>
<td><span data-ttu-id="160d5-809">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-810">CC004</span><span class="sxs-lookup"><span data-stu-id="160d5-810">CC004</span></span></td>
<td><span data-ttu-id="160d5-811">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="160d5-811">Packaging</span></span></td>
<td><span data-ttu-id="160d5-812">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-812">10001</span></span></td>
<td><span data-ttu-id="160d5-813">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-813">Electricity</span></span></td>
<td><span data-ttu-id="160d5-814">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-814">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-815">124.57</span><span class="sxs-lookup"><span data-stu-id="160d5-815">124.57</span></span></td>
<td><span data-ttu-id="160d5-816">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-817">CC002</span><span class="sxs-lookup"><span data-stu-id="160d5-817">CC002</span></span></td>
<td><span data-ttu-id="160d5-818">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="160d5-818">Finance</span></span></td>
<td><span data-ttu-id="160d5-819">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-819">10001</span></span></td>
<td><span data-ttu-id="160d5-820">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-820">Electricity</span></span></td>
<td><span data-ttu-id="160d5-821">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-821">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="160d5-822">-675.00</span></span></td>
<td><span data-ttu-id="160d5-823">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-824">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-824">CC003</span></span></td>
<td><span data-ttu-id="160d5-825">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="160d5-825">Assembly</span></span></td>
<td><span data-ttu-id="160d5-826">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-826">10001</span></span></td>
<td><span data-ttu-id="160d5-827">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-827">Electricity</span></span></td>
<td><span data-ttu-id="160d5-828">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-828">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-829">438.75</span><span class="sxs-lookup"><span data-stu-id="160d5-829">438.75</span></span></td>
<td><span data-ttu-id="160d5-830">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-831">CC004</span><span class="sxs-lookup"><span data-stu-id="160d5-831">CC004</span></span></td>
<td><span data-ttu-id="160d5-832">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="160d5-832">Packaging</span></span></td>
<td><span data-ttu-id="160d5-833">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-833">10001</span></span></td>
<td><span data-ttu-id="160d5-834">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-834">Electricity</span></span></td>
<td><span data-ttu-id="160d5-835">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-835">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-836">236.25</span><span class="sxs-lookup"><span data-stu-id="160d5-836">236.25</span></span></td>
<td><span data-ttu-id="160d5-837">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-838">CC002</span><span class="sxs-lookup"><span data-stu-id="160d5-838">CC002</span></span></td>
<td><span data-ttu-id="160d5-839">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="160d5-839">Finance</span></span></td>
<td><span data-ttu-id="160d5-840">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-840">10001</span></span></td>
<td><span data-ttu-id="160d5-841">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-841">Electricity</span></span></td>
<td><span data-ttu-id="160d5-842">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-842">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="160d5-843">-8,150.29</span></span></td>
<td><span data-ttu-id="160d5-844">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-845">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-845">CC003</span></span></td>
<td><span data-ttu-id="160d5-846">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="160d5-846">Assembly</span></span></td>
<td><span data-ttu-id="160d5-847">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-847">10001</span></span></td>
<td><span data-ttu-id="160d5-848">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-848">Electricity</span></span></td>
<td><span data-ttu-id="160d5-849">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-849">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="160d5-850">5,297.69</span></span></td>
<td><span data-ttu-id="160d5-851">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-852">CC004</span><span class="sxs-lookup"><span data-stu-id="160d5-852">CC004</span></span></td>
<td><span data-ttu-id="160d5-853">Pakkaus</span><span class="sxs-lookup"><span data-stu-id="160d5-853">Packaging</span></span></td>
<td><span data-ttu-id="160d5-854">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-854">10001</span></span></td>
<td><span data-ttu-id="160d5-855">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-855">Electricity</span></span></td>
<td><span data-ttu-id="160d5-856">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-856">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="160d5-857">2,852.60</span></span></td>
<td><span data-ttu-id="160d5-858">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-859">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-859">CC003</span></span></td>
<td><span data-ttu-id="160d5-860">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="160d5-860">Assembly</span></span></td>
<td><span data-ttu-id="160d5-861">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-861">10001</span></span></td>
<td><span data-ttu-id="160d5-862">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-862">Electricity</span></span></td>
<td><span data-ttu-id="160d5-863">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-863">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="160d5-864">-713.75</span></span></td>
<td><span data-ttu-id="160d5-865">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-866">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-866">Prod 1</span></span></td>
<td><span data-ttu-id="160d5-867">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-867">Product 1</span></span></td>
<td><span data-ttu-id="160d5-868">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-868">10001</span></span></td>
<td><span data-ttu-id="160d5-869">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-869">Electricity</span></span></td>
<td><span data-ttu-id="160d5-870">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-870">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-871">535.31</span><span class="sxs-lookup"><span data-stu-id="160d5-871">535.31</span></span></td>
<td><span data-ttu-id="160d5-872">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-873">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-873">Prod 2</span></span></td>
<td><span data-ttu-id="160d5-874">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-874">Product 2</span></span></td>
<td><span data-ttu-id="160d5-875">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-875">10001</span></span></td>
<td><span data-ttu-id="160d5-876">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-876">Electricity</span></span></td>
<td><span data-ttu-id="160d5-877">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-877">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-878">178.44</span><span class="sxs-lookup"><span data-stu-id="160d5-878">178.44</span></span></td>
<td><span data-ttu-id="160d5-879">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-880">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-880">CC003</span></span></td>
<td><span data-ttu-id="160d5-881">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="160d5-881">Assembly</span></span></td>
<td><span data-ttu-id="160d5-882">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-882">10001</span></span></td>
<td><span data-ttu-id="160d5-883">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-883">Electricity</span></span></td>
<td><span data-ttu-id="160d5-884">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-884">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="160d5-885">-5,982.83</span></span></td>
<td><span data-ttu-id="160d5-886">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-887">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-887">Prod 1</span></span></td>
<td><span data-ttu-id="160d5-888">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-888">Product 1</span></span></td>
<td><span data-ttu-id="160d5-889">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-889">10001</span></span></td>
<td><span data-ttu-id="160d5-890">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-890">Electricity</span></span></td>
<td><span data-ttu-id="160d5-891">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-891">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="160d5-892">4,487.12</span></span></td>
<td><span data-ttu-id="160d5-893">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-894">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-894">Prod 2</span></span></td>
<td><span data-ttu-id="160d5-895">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-895">Product 2</span></span></td>
<td><span data-ttu-id="160d5-896">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-896">10001</span></span></td>
<td><span data-ttu-id="160d5-897">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-897">Electricity</span></span></td>
<td><span data-ttu-id="160d5-898">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-898">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="160d5-899">1,495.71</span></span></td>
<td><span data-ttu-id="160d5-900">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-901">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-901">CC003</span></span></td>
<td><span data-ttu-id="160d5-902">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="160d5-902">Assembly</span></span></td>
<td><span data-ttu-id="160d5-903">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-903">10001</span></span></td>
<td><span data-ttu-id="160d5-904">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-904">Electricity</span></span></td>
<td><span data-ttu-id="160d5-905">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-905">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="160d5-906">-286.25</span></span></td>
<td><span data-ttu-id="160d5-907">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-908">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-908">Prod 1</span></span></td>
<td><span data-ttu-id="160d5-909">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-909">Product 1</span></span></td>
<td><span data-ttu-id="160d5-910">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-910">10001</span></span></td>
<td><span data-ttu-id="160d5-911">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-911">Electricity</span></span></td>
<td><span data-ttu-id="160d5-912">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-912">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-913">241.05</span><span class="sxs-lookup"><span data-stu-id="160d5-913">241.05</span></span></td>
<td><span data-ttu-id="160d5-914">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-915">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-915">Prod 2</span></span></td>
<td><span data-ttu-id="160d5-916">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-916">Product 2</span></span></td>
<td><span data-ttu-id="160d5-917">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-917">10001</span></span></td>
<td><span data-ttu-id="160d5-918">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-918">Electricity</span></span></td>
<td><span data-ttu-id="160d5-919">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-919">Fixed cost</span></span></td>
<td><span data-ttu-id="160d5-920">45.20</span><span class="sxs-lookup"><span data-stu-id="160d5-920">45.20</span></span></td>
<td><span data-ttu-id="160d5-921">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-922">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-922">CC003</span></span></td>
<td><span data-ttu-id="160d5-923">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="160d5-923">Assembly</span></span></td>
<td><span data-ttu-id="160d5-924">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-924">10001</span></span></td>
<td><span data-ttu-id="160d5-925">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-925">Electricity</span></span></td>
<td><span data-ttu-id="160d5-926">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-926">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-927">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="160d5-927">-2,977.17</span></span></td>
<td><span data-ttu-id="160d5-928">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-929">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-929">Prod 1</span></span></td>
<td><span data-ttu-id="160d5-930">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-930">Product 1</span></span></td>
<td><span data-ttu-id="160d5-931">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-931">10001</span></span></td>
<td><span data-ttu-id="160d5-932">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-932">Electricity</span></span></td>
<td><span data-ttu-id="160d5-933">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-933">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="160d5-934">2,507.09</span></span></td>
<td><span data-ttu-id="160d5-935">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="160d5-936">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-936">Prod 2</span></span></td>
<td><span data-ttu-id="160d5-937">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-937">Product 2</span></span></td>
<td><span data-ttu-id="160d5-938">10 001</span><span class="sxs-lookup"><span data-stu-id="160d5-938">10001</span></span></td>
<td><span data-ttu-id="160d5-939">Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-939">Electricity</span></span></td>
<td><span data-ttu-id="160d5-940">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-940">Variable cost</span></span></td>
<td><span data-ttu-id="160d5-941">470.08</span><span class="sxs-lookup"><span data-stu-id="160d5-941">470.08</span></span></td>
<td><span data-ttu-id="160d5-942">31.1.2017</span><span class="sxs-lookup"><span data-stu-id="160d5-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="160d5-943">Johtopäätökset</span><span class="sxs-lookup"><span data-stu-id="160d5-943">Conclusion</span></span>
<span data-ttu-id="160d5-944">Kirjanpidossa kirjataan tyhjään kustannuspaikkatunnukseen sähkökustannus arvolla 10 000,00.</span><span class="sxs-lookup"><span data-stu-id="160d5-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="160d5-945">Tämän ansiosta kustannuslaskijat tietävät, että kustannus on kohdistettava.</span><span class="sxs-lookup"><span data-stu-id="160d5-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="160d5-946">Kustannukset virtaavat kirjanpidossa organisaation yksiköiden ja tasojen läpi käytössä olevien käytäntöjen ja sääntöjen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="160d5-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="160d5-947">Kukin kustannus on liitetty kustannusperusteeseen, joka sisältää parhaan arvion kustannusten kohdistuksesta.</span><span class="sxs-lookup"><span data-stu-id="160d5-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="160d5-948">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="160d5-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="160d5-949">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="160d5-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="160d5-950">Yhteensä</span><span class="sxs-lookup"><span data-stu-id="160d5-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="160d5-951">CC099</span><span class="sxs-lookup"><span data-stu-id="160d5-951">CC099</span></span></th>
<th><span data-ttu-id="160d5-952">CC001</span><span class="sxs-lookup"><span data-stu-id="160d5-952">CC001</span></span></th>
<th><span data-ttu-id="160d5-953">CC002</span><span class="sxs-lookup"><span data-stu-id="160d5-953">CC002</span></span></th>
<th><span data-ttu-id="160d5-954">CC003</span><span class="sxs-lookup"><span data-stu-id="160d5-954">CC003</span></span></th>
<th><span data-ttu-id="160d5-955">CC004</span><span class="sxs-lookup"><span data-stu-id="160d5-955">CC004</span></span></th>
<th><span data-ttu-id="160d5-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="160d5-956">Proj 1</span></span></th>
<th><span data-ttu-id="160d5-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="160d5-957">Proj 2</span></span></th>
<th><span data-ttu-id="160d5-958">Tuote 1</span><span class="sxs-lookup"><span data-stu-id="160d5-958">Prod 1</span></span></th>
<th><span data-ttu-id="160d5-959">Tuote 2</span><span class="sxs-lookup"><span data-stu-id="160d5-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="160d5-960">10001 Sähkö</span><span class="sxs-lookup"><span data-stu-id="160d5-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="160d5-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="160d5-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="160d5-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="160d5-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="160d5-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="160d5-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="160d5-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="160d5-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="160d5-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="160d5-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="160d5-970">Luokittelematon</span><span class="sxs-lookup"><span data-stu-id="160d5-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-971">0,00</span><span class="sxs-lookup"><span data-stu-id="160d5-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="160d5-972">Kiinteä kustannus</span><span class="sxs-lookup"><span data-stu-id="160d5-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-973">0,00</span><span class="sxs-lookup"><span data-stu-id="160d5-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-974">0,00</span><span class="sxs-lookup"><span data-stu-id="160d5-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-975">0,00</span><span class="sxs-lookup"><span data-stu-id="160d5-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-976">0,00</span><span class="sxs-lookup"><span data-stu-id="160d5-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-977">0,00</span><span class="sxs-lookup"><span data-stu-id="160d5-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="160d5-978">776.36</span><span class="sxs-lookup"><span data-stu-id="160d5-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-979">223.64</span><span class="sxs-lookup"><span data-stu-id="160d5-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="160d5-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="160d5-981">Muuttuva kulu</span><span class="sxs-lookup"><span data-stu-id="160d5-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-982">000</span><span class="sxs-lookup"><span data-stu-id="160d5-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-983">0,00</span><span class="sxs-lookup"><span data-stu-id="160d5-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-984">0,00</span><span class="sxs-lookup"><span data-stu-id="160d5-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-985">0,00</span><span class="sxs-lookup"><span data-stu-id="160d5-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-986">0,00</span><span class="sxs-lookup"><span data-stu-id="160d5-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-987">30,00</span><span class="sxs-lookup"><span data-stu-id="160d5-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-988">10,00</span><span class="sxs-lookup"><span data-stu-id="160d5-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="160d5-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="160d5-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="160d5-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="160d5-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="160d5-992">Tässä ohjeaiheessa esitellään, miten ensisijainen kustannuselementti, 10001 Sähkö, virtaa kustannusobjektien läpi.</span><span class="sxs-lookup"><span data-stu-id="160d5-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="160d5-993">Tästä syystä tämä yleiskustannus kohdistetaan organisaation alimmalle tasolle.</span><span class="sxs-lookup"><span data-stu-id="160d5-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="160d5-994">Toisin sanoen alimman tason kustannusobjektit kantavat kustannuksen.</span><span class="sxs-lookup"><span data-stu-id="160d5-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="160d5-995">Jos tarvitset visuaalisen näkymän kustannuksen virrasta kustannusobjektien välillä, voit käyttää kustannuksen koontikäytäntösääntöjä kustannusvirran visualisointiin.</span><span class="sxs-lookup"><span data-stu-id="160d5-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="160d5-996">Lisätietoja on kohdassa [Kustannusten koonti](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="160d5-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



