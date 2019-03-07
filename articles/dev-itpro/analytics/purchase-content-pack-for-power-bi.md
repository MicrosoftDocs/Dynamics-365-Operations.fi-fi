---
title: Osto- ja kulutusanalyysin Power BI -sisältö
description: Tässä ohjeaiheessa kerrotaan, mitä osto- ja kulutusanalyysin Power BI -sisältö sisältää. Siinä selitetään, miten sisältöön sisältyvät raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä.
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 069c4dc21959ab603ba6ca3da0ac68ef20325265
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "313839"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="9b900-104">Osto- ja kulutusanalyysin Power BI -sisältö</span><span class="sxs-lookup"><span data-stu-id="9b900-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b900-105">Tässä ohjeaiheessa kerrotaan, mitä **osto- ja kulutusanalyysin** Microsoft Power BI -sisältö sisältää.</span><span class="sxs-lookup"><span data-stu-id="9b900-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="9b900-106">Siinä selitetään, miten sisältyvät Power BI -raportit avataan, sekä kerrotaan sisällön muodostamisessa käytettävistä tietomallista ja yksiköistä.</span><span class="sxs-lookup"><span data-stu-id="9b900-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="9b900-107">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="9b900-107">Overview</span></span>

<span data-ttu-id="9b900-108">**Osto- ja kustannusanalyysin** Power BI -sisältö on suunniteltu ostopäälliköiden ja budjetista vastaavien esimiesten käyttöön, sillä auttaa seuraamaan ostoja ja kulutusta.</span><span class="sxs-lookup"><span data-stu-id="9b900-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="9b900-109">Esimiehet voivat analysoida ostoja ja kulutusta seuraavin tavoin:</span><span class="sxs-lookup"><span data-stu-id="9b900-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="9b900-110">Ostot vuoden alusta (toimittajaryhmän ja yksittäisten toimittajien, hankintaluokan ja yksittäisten tuotteiden ja toimittajan sijainnin mukaan)</span><span class="sxs-lookup"><span data-stu-id="9b900-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="9b900-111">Ostojen vuosittainen muutos (toimittajaryhmän ja hankintaluokan mukaan)</span><span class="sxs-lookup"><span data-stu-id="9b900-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="9b900-112">Sisältö käyttää ostotapahtumiin liittyviä tietoja ja antaa koko yrityksen ostolukujen koostenäkymän sekä toimittaja- ja tuotekohtaisen erittelyn ostoista ja kulutuksesta.</span><span class="sxs-lookup"><span data-stu-id="9b900-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="9b900-113">Raportit korostavat ostojen ja kulutuksen muutoksia ajanjakson aikana.</span><span class="sxs-lookup"><span data-stu-id="9b900-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="9b900-114">Tämän vuoksi raportteja voidaan käyttää, kun esimiehille ilmoitetaan yksittäisten toimittajien ja tuotteiden positiivisista ja negatiivisista kulutussuuntauksista.</span><span class="sxs-lookup"><span data-stu-id="9b900-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="9b900-115">Lisäksi kaaviot osoittavat eri hankintaluokkien ja toimittajaryhmien ostot ja kulutuksen.</span><span class="sxs-lookup"><span data-stu-id="9b900-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="9b900-116">Näin ollen luokka- ja aluepäälliköitä voivat käyttää kaavioita apuna kulutuskäyttäytymisessä tapahtuvien muutoksien havaitsemisessa.</span><span class="sxs-lookup"><span data-stu-id="9b900-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="9b900-117">Power BI -sisällön käyttäminen</span><span class="sxs-lookup"><span data-stu-id="9b900-117">Accessing the Power BI content</span></span>
<span data-ttu-id="9b900-118">**Osto- ja kulutusanalyysin** Power BI -sisältö näkyy **Osto- ja kulutusanalyysi** -sivulla (**Hankinta** \> **Kyselyt ja raportit** \> **Ostojen suorituskykyanalyysi** \> **Osto- ja kulutusanalyysi**).</span><span class="sxs-lookup"><span data-stu-id="9b900-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="9b900-119">Mittarit, jotka sisältyvät Power BI -sisältöön</span><span class="sxs-lookup"><span data-stu-id="9b900-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="9b900-120">**Ostojen ja kulutuksen analyysin** Power BI -sisältöön kuuluu raportti, joka koostuu mittarijoukosta.</span><span class="sxs-lookup"><span data-stu-id="9b900-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="9b900-121">Nämä mittarit visualisoidaan kaavioina, ruutuina ja taulukoina.</span><span class="sxs-lookup"><span data-stu-id="9b900-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="9b900-122">Seuraavassa taulukossa on visualisointien yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="9b900-122">The following table provides an overview of the visualizations.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9b900-123">Raporttisivu</span><span class="sxs-lookup"><span data-stu-id="9b900-123">Report page</span></span></th>
<th><span data-ttu-id="9b900-124">Kaaviot</span><span class="sxs-lookup"><span data-stu-id="9b900-124">Charts</span></span></th>
<th><span data-ttu-id="9b900-125">Ruudut</span><span class="sxs-lookup"><span data-stu-id="9b900-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9b900-126">Ostot toimittajan mukaan</span><span class="sxs-lookup"><span data-stu-id="9b900-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="9b900-127">10 parasta toimittajaa ostojen mukaan (pinottu palkkikaavio)</span><span class="sxs-lookup"><span data-stu-id="9b900-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="9b900-128">Ostot yhteensä toimittajaryhmän/maan/nimen mukaan (ympyräkaavio)</span><span class="sxs-lookup"><span data-stu-id="9b900-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="9b900-129">Ostot toimittajaryhmän/maan/nimen mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="9b900-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="9b900-130">Ostot keskimäärin toimittajaryhmän/maan/nimen mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="9b900-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9b900-131">Osto yhteensä</span><span class="sxs-lookup"><span data-stu-id="9b900-131">Total purchase</span></span></li>
<li><span data-ttu-id="9b900-132">Ostojen vuosittainen kasvu</span><span class="sxs-lookup"><span data-stu-id="9b900-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="9b900-133">Toimittajien kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="9b900-133">Total # vendors</span></span></li>
<li><span data-ttu-id="9b900-134">Aktiivisten toimittajien kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="9b900-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="9b900-135">Ostot tuotteen mukaan</span><span class="sxs-lookup"><span data-stu-id="9b900-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="9b900-136">Ostot hankintaluokan / tuotteen nimen mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="9b900-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="9b900-137">Ostot yhteensä hankintaluokan / tuotteen nimen mukaan (ympyräkaavio)</span><span class="sxs-lookup"><span data-stu-id="9b900-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="9b900-138">10 parasta tuotetta ostojen mukaan (pinottu palkkikaavio)</span><span class="sxs-lookup"><span data-stu-id="9b900-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9b900-139">Tuotteiden kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="9b900-139">Total # of products</span></span></li>
<li><span data-ttu-id="9b900-140">Kaikkien aktiivisten tuotteiden prosenttiosuus tuotteiden kokonaismäärästä</span><span class="sxs-lookup"><span data-stu-id="9b900-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="9b900-141">Tuotteiden määrä, joista koostuu 80 % ostoista</span><span class="sxs-lookup"><span data-stu-id="9b900-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="9b900-142">Ostot kauden mukaan\*</span><span class="sxs-lookup"><span data-stu-id="9b900-142">Purchase by period\*</span></span></td>
<td><ul>
<li><span data-ttu-id="9b900-143">Ostot kuukauden/päivän mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="9b900-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="9b900-144">Kumulatiivisten ostojen vuosittainen varianssi (vesiputouskaavio)</span><span class="sxs-lookup"><span data-stu-id="9b900-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="9b900-145">Ostot yhteensä, vuosittainen kasvu (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="9b900-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="9b900-146">Hankintaraportti (matriisi)</span><span class="sxs-lookup"><span data-stu-id="9b900-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9b900-147">Ostojen vuosittainen kasvu</span><span class="sxs-lookup"><span data-stu-id="9b900-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="9b900-148">Ostojen vuosittainen kasvuprosentti</span><span class="sxs-lookup"><span data-stu-id="9b900-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="9b900-149">Ostot toimittajan sijainnin mukaan</span><span class="sxs-lookup"><span data-stu-id="9b900-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="9b900-150">Ostot kaupungin mukaan</span><span class="sxs-lookup"><span data-stu-id="9b900-150">Purchase by city</span></span></li>
<li><span data-ttu-id="9b900-151">Ostojen vuosittainen kasvuprosentti</span><span class="sxs-lookup"><span data-stu-id="9b900-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="9b900-152">Ostot maan mukaan</span><span class="sxs-lookup"><span data-stu-id="9b900-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="9b900-153">Ostojen ja kulutuksen analyysi ajan mukaan</span><span class="sxs-lookup"><span data-stu-id="9b900-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="9b900-154">Ostojen kuluva vuosi kuukauden/päivän mukaan (viivakaavio)</span><span class="sxs-lookup"><span data-stu-id="9b900-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="9b900-155">Ostojen kuluva ja edellinen vuosi (viiva- ja sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="9b900-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="9b900-156">Ostojen ja kulutuksen analyysi toimittajan mukaan</span><span class="sxs-lookup"><span data-stu-id="9b900-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="9b900-157">10 parasta toimittajaa ostojen prosenttiosuuden mukaan (suppilokaavio)</span><span class="sxs-lookup"><span data-stu-id="9b900-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="9b900-158">10 toimittajaa, joiden vuosittainen kulutus on noussut eniten</span><span class="sxs-lookup"><span data-stu-id="9b900-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="9b900-159">10 toimittajaa, joiden vuosittainen kulutus on laskenut eniten</span><span class="sxs-lookup"><span data-stu-id="9b900-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9b900-160">\* Ostot tänä ja edellisenä vuonna sekä kasvu hankintaluokan mukaan</span><span class="sxs-lookup"><span data-stu-id="9b900-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="9b900-161">Tietomalli ja yksiköt</span><span class="sxs-lookup"><span data-stu-id="9b900-161">Data model and entities</span></span>
<span data-ttu-id="9b900-162">Seuraavia tietoja käytetään **osto- ja kulutusanalyysin** Power BI -sisällön raporttisivujen täyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="9b900-162">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="9b900-163">Nämä tiedot esitetään koottuina mittauksina, joka vaiheistetaan yksikkösäilössä.</span><span class="sxs-lookup"><span data-stu-id="9b900-163">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="9b900-164">Yksikkösäilö on analytiikkaa varten optimoitu Microsoft SQL Server -tietokanta.</span><span class="sxs-lookup"><span data-stu-id="9b900-164">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="9b900-165">Lisätietoja on kohdassa [Power BI:n ja yksikkösäilön integroinnin yleiskatsaus](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="9b900-165">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="9b900-166">Sisällön koostetut mittaukset ovat alijoukko Microsoft Dynamics AX 2012:n ja Microsoft Dynamics AX 2012 R3:n ostokuutiossa saatavilla olleista koostetuista mittauksista.</span><span class="sxs-lookup"><span data-stu-id="9b900-166">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="9b900-167">Jotta kuution koostetut mittaukset voi tallentaa yksikkösäilöön, niistä on tehtävä käyttöönottokelpoisia.</span><span class="sxs-lookup"><span data-stu-id="9b900-167">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="9b900-168">Lisätietoja koostettujen mittojen tallentamisesta yksikkösäilöön on kohdassa [Power BI:n ja yksikkösäilön integroinnin yleiskatsaus](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="9b900-168">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="9b900-169">Seuraavat tärkeät koostemitat ovat käytettävissä suoraan laskun rivien yksiköstä. Niitä käytetään sisällön perustana.</span><span class="sxs-lookup"><span data-stu-id="9b900-169">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="9b900-170">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="9b900-170">Entity</span></span>        | <span data-ttu-id="9b900-171">Tärkeät koostemitat</span><span class="sxs-lookup"><span data-stu-id="9b900-171">Key aggregate measurements</span></span> | <span data-ttu-id="9b900-172">Tietolähde</span><span class="sxs-lookup"><span data-stu-id="9b900-172">Data source</span></span>                                 | <span data-ttu-id="9b900-173">Kenttä</span><span class="sxs-lookup"><span data-stu-id="9b900-173">Field</span></span>              | <span data-ttu-id="9b900-174">kuvaus</span><span class="sxs-lookup"><span data-stu-id="9b900-174">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="9b900-175">Laskurivit</span><span class="sxs-lookup"><span data-stu-id="9b900-175">Invoice lines</span></span> | <span data-ttu-id="9b900-176">Osto</span><span class="sxs-lookup"><span data-stu-id="9b900-176">Purchase</span></span>                   | <span data-ttu-id="9b900-177">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="9b900-177">VendInvoiceTrans</span></span>                            | <span data-ttu-id="9b900-178">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="9b900-178">SUM(LineAmountMST)</span></span> | <span data-ttu-id="9b900-179">Summa kirjanpitovaluuttana.</span><span class="sxs-lookup"><span data-stu-id="9b900-179">The amount in the accounting currency.</span></span> |

<span data-ttu-id="9b900-180">Seuraavassa taulukossa esitellään tärkeät mitat, jotka lasketaan sisällössä ja jotka saadaan laskun rivien yksiköstä.</span><span class="sxs-lookup"><span data-stu-id="9b900-180">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="9b900-181">Mitta</span><span class="sxs-lookup"><span data-stu-id="9b900-181">Measure</span></span>               | <span data-ttu-id="9b900-182">Laskelma</span><span class="sxs-lookup"><span data-stu-id="9b900-182">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b900-183">Kuluvan vuoden ostot</span><span class="sxs-lookup"><span data-stu-id="9b900-183">Purchase current year</span></span> | <span data-ttu-id="9b900-184">Kuluvan vuoden ostot = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="9b900-184">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="9b900-185">Edellisen vuoden ostot</span><span class="sxs-lookup"><span data-stu-id="9b900-185">Purchase last year</span></span>    | <span data-ttu-id="9b900-186">Edellisen vuoden ostot = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="9b900-186">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="9b900-187">Ostojen vuosittainen kasvu</span><span class="sxs-lookup"><span data-stu-id="9b900-187">YOY purchase growth</span></span>   | <span data-ttu-id="9b900-188">Ostojen vuosittainen kasvu = \[Kuluvan vuoden ostot\] – \[Edellisen vuoden ostot\]</span><span class="sxs-lookup"><span data-stu-id="9b900-188">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="9b900-189">Seuraavia sisällön tärkeitä dimensioita käytetään koostemittojen ositussuodattimina. Tämä parantaa rakeisuutta ja sen avulla saadaan entistä tarkempaa analyysitietoa.</span><span class="sxs-lookup"><span data-stu-id="9b900-189">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="9b900-190">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="9b900-190">Entity</span></span>                 | <span data-ttu-id="9b900-191">Esimerkkejä määritteistä</span><span class="sxs-lookup"><span data-stu-id="9b900-191">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="9b900-192">Toimittajat</span><span class="sxs-lookup"><span data-stu-id="9b900-192">Vendors</span></span>                | <span data-ttu-id="9b900-193">Toimittajaryhmät, toimittajan maa tai alueet, toimittajan nimi</span><span class="sxs-lookup"><span data-stu-id="9b900-193">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="9b900-194">Tuotteet</span><span class="sxs-lookup"><span data-stu-id="9b900-194">Products</span></span>               | <span data-ttu-id="9b900-195">Tuotenumero, tuotteen nimi, nimikeryhmien nimi</span><span class="sxs-lookup"><span data-stu-id="9b900-195">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="9b900-196">Hankintaluokat</span><span class="sxs-lookup"><span data-stu-id="9b900-196">Procurement categories</span></span> | <span data-ttu-id="9b900-197">Hankintaluokka, hankintaluokkien nimet</span><span class="sxs-lookup"><span data-stu-id="9b900-197">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="9b900-198">Oikeushenkilöt</span><span class="sxs-lookup"><span data-stu-id="9b900-198">Legal entities</span></span>         | <span data-ttu-id="9b900-199">Yrityksen nimi</span><span class="sxs-lookup"><span data-stu-id="9b900-199">Legal entity name</span></span>                                     |
| <span data-ttu-id="9b900-200">Päivämäärät</span><span class="sxs-lookup"><span data-stu-id="9b900-200">Dates</span></span>                  | <span data-ttu-id="9b900-201">Päivämäärät, vuosisiirtymä</span><span class="sxs-lookup"><span data-stu-id="9b900-201">Dates, Year offset</span></span>                                    |

<span data-ttu-id="9b900-202">Kuluvan kalenterivuoden tiedot näkyvät oletusarvoisesti sisällössä.</span><span class="sxs-lookup"><span data-stu-id="9b900-202">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="9b900-203">Voit kuitenkin muuttaa päivämääräsuodatinta raportin suodatinosassa.</span><span class="sxs-lookup"><span data-stu-id="9b900-203">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="9b900-204">Voit muuttaa myös yrityssuodatinta.</span><span class="sxs-lookup"><span data-stu-id="9b900-204">You can also change the company filter.</span></span>
