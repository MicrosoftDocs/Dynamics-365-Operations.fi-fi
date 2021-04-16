---
title: Osto- ja kulutusanalyysin Power BI -sisältö
description: Tässä ohjeaiheessa kerrotaan, mitä osto- ja kulutusanalyysin Power BI -sisältö sisältää.
author: FrankDahl
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f9741b5f30f5e62b9e80000953113377fe016253
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749366"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="929bc-103">Osto- ja kulutusanalyysin Power BI -sisältö</span><span class="sxs-lookup"><span data-stu-id="929bc-103">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="929bc-104">Tässä ohjeaiheessa kerrotaan, mitä **osto- ja kulutusanalyysin** Microsoft Power BI -sisältö sisältää.</span><span class="sxs-lookup"><span data-stu-id="929bc-104">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="929bc-105">Siinä selitetään, miten sisältyvät Power BI -raportit avataan, sekä kerrotaan sisällön muodostamisessa käytettävistä tietomallista ja yksiköistä.</span><span class="sxs-lookup"><span data-stu-id="929bc-105">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="929bc-106">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="929bc-106">Overview</span></span>

<span data-ttu-id="929bc-107">**Osto- ja kustannusanalyysin** Power BI -sisältö on suunniteltu ostopäälliköiden ja budjetista vastaavien esimiesten käyttöön, sillä auttaa seuraamaan ostoja ja kulutusta.</span><span class="sxs-lookup"><span data-stu-id="929bc-107">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="929bc-108">Esimiehet voivat analysoida ostoja ja kulutusta seuraavin tavoin:</span><span class="sxs-lookup"><span data-stu-id="929bc-108">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="929bc-109">Ostot vuoden alusta (toimittajaryhmän ja yksittäisten toimittajien, hankintaluokan ja yksittäisten tuotteiden ja toimittajan sijainnin mukaan)</span><span class="sxs-lookup"><span data-stu-id="929bc-109">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="929bc-110">Ostojen vuosittainen muutos (toimittajaryhmän ja hankintaluokan mukaan)</span><span class="sxs-lookup"><span data-stu-id="929bc-110">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="929bc-111">Sisältö käyttää ostotapahtumiin liittyviä tietoja ja antaa koko yrityksen ostolukujen koostenäkymän sekä toimittaja- ja tuotekohtaisen erittelyn ostoista ja kulutuksesta.</span><span class="sxs-lookup"><span data-stu-id="929bc-111">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="929bc-112">Raportit korostavat ostojen ja kulutuksen muutoksia ajanjakson aikana.</span><span class="sxs-lookup"><span data-stu-id="929bc-112">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="929bc-113">Tämän vuoksi raportteja voidaan käyttää, kun esimiehille ilmoitetaan yksittäisten toimittajien ja tuotteiden positiivisista ja negatiivisista kulutussuuntauksista.</span><span class="sxs-lookup"><span data-stu-id="929bc-113">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="929bc-114">Lisäksi kaaviot osoittavat eri hankintaluokkien ja toimittajaryhmien ostot ja kulutuksen.</span><span class="sxs-lookup"><span data-stu-id="929bc-114">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="929bc-115">Näin ollen luokka- ja aluepäälliköitä voivat käyttää kaavioita apuna kulutuskäyttäytymisessä tapahtuvien muutoksien havaitsemisessa.</span><span class="sxs-lookup"><span data-stu-id="929bc-115">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="929bc-116">Power BI -sisällön käyttäminen</span><span class="sxs-lookup"><span data-stu-id="929bc-116">Accessing the Power BI content</span></span>
<span data-ttu-id="929bc-117">**Osto- ja kulutusanalyysin** Power BI -sisältö näkyy **Osto- ja kulutusanalyysi** -sivulla (**Hankinta** \> **Kyselyt ja raportit** \> **Ostojen suorituskykyanalyysi** \> **Osto- ja kulutusanalyysi**).</span><span class="sxs-lookup"><span data-stu-id="929bc-117">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="929bc-118">Mittarit, jotka sisältyvät Power BI -sisältöön</span><span class="sxs-lookup"><span data-stu-id="929bc-118">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="929bc-119">**Ostojen ja kulutuksen analyysin** Power BI -sisältöön kuuluu raportti, joka koostuu mittarijoukosta.</span><span class="sxs-lookup"><span data-stu-id="929bc-119">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="929bc-120">Nämä mittarit visualisoidaan kaavioina, ruutuina ja taulukoina.</span><span class="sxs-lookup"><span data-stu-id="929bc-120">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="929bc-121">Seuraavassa osissa on visualisointien yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="929bc-121">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="929bc-122">Ostot toimittajan mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="929bc-122">Purchase by vendor report page</span></span>
<span data-ttu-id="929bc-123">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="929bc-123">**Charts**</span></span>
- <span data-ttu-id="929bc-124">10 parasta toimittajaa ostojen mukaan (pinottu palkkikaavio)</span><span class="sxs-lookup"><span data-stu-id="929bc-124">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="929bc-125">Ostot yhteensä toimittajaryhmän/maan/nimen mukaan (ympyräkaavio)</span><span class="sxs-lookup"><span data-stu-id="929bc-125">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="929bc-126">Ostot toimittajaryhmän/maan/nimen mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="929bc-126">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="929bc-127">Ostot keskimäärin toimittajaryhmän/maan/nimen mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="929bc-127">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="929bc-128">**Ruudut**</span><span class="sxs-lookup"><span data-stu-id="929bc-128">**Tiles**</span></span>
- <span data-ttu-id="929bc-129">Osto yhteensä</span><span class="sxs-lookup"><span data-stu-id="929bc-129">Total purchase</span></span>
- <span data-ttu-id="929bc-130">Ostojen vuosittainen kasvu</span><span class="sxs-lookup"><span data-stu-id="929bc-130">YOY purchase growth</span></span>
- <span data-ttu-id="929bc-131">Toimittajien kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="929bc-131">Total # vendors</span></span>
- <span data-ttu-id="929bc-132">Aktiivisten toimittajien kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="929bc-132">Total # of active vendors</span></span>

<span data-ttu-id="929bc-133">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="929bc-133">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="929bc-134">Ostot tuotteen mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="929bc-134">Purchase by product report page</span></span>

<span data-ttu-id="929bc-135">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="929bc-135">**Charts**</span></span>
- <span data-ttu-id="929bc-136">Ostot hankintaluokan / tuotteen nimen mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="929bc-136">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="929bc-137">Ostot yhteensä hankintaluokan / tuotteen nimen mukaan (ympyräkaavio)</span><span class="sxs-lookup"><span data-stu-id="929bc-137">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="929bc-138">10 parasta tuotetta ostojen mukaan (pinottu palkkikaavio)</span><span class="sxs-lookup"><span data-stu-id="929bc-138">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="929bc-139">**Ruudut**</span><span class="sxs-lookup"><span data-stu-id="929bc-139">**Tiles**</span></span>
- <span data-ttu-id="929bc-140">Tuotteiden kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="929bc-140">Total # of products</span></span></li>
- <span data-ttu-id="929bc-141">Kaikkien aktiivisten tuotteiden prosenttiosuus tuotteiden kokonaismäärästä</span><span class="sxs-lookup"><span data-stu-id="929bc-141">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="929bc-142">Tuotteiden määrä, joista koostuu 80 % ostoista</span><span class="sxs-lookup"><span data-stu-id="929bc-142">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="929bc-143">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="929bc-143">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="929bc-144">Ostot ajanjakson mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="929bc-144">Purchase by period report page</span></span>
<span data-ttu-id="929bc-145">Tällä sivulla nähdään ostot tänä ja edellisenä vuonna sekä kasvu hankintaluokan mukaan.</span><span class="sxs-lookup"><span data-stu-id="929bc-145">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="929bc-146">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="929bc-146">**Charts**</span></span> 
- <span data-ttu-id="929bc-147">Ostot kuukauden/päivän mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="929bc-147">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="929bc-148">Kumulatiivisten ostojen vuosittainen varianssi (vesiputouskaavio)</span><span class="sxs-lookup"><span data-stu-id="929bc-148">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="929bc-149">Ostot yhteensä, vuosittainen kasvu (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="929bc-149">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="929bc-150">Hankintaraportti (matriisi)</span><span class="sxs-lookup"><span data-stu-id="929bc-150">Procurement statement (matrix)</span></span>

<span data-ttu-id="929bc-151">**Ruudut**</span><span class="sxs-lookup"><span data-stu-id="929bc-151">**Tiles**</span></span>
- <span data-ttu-id="929bc-152">Ostojen vuosittainen kasvu</span><span class="sxs-lookup"><span data-stu-id="929bc-152">YOY purchase growth</span></span>
- <span data-ttu-id="929bc-153">Ostojen vuosittainen kasvuprosentti</span><span class="sxs-lookup"><span data-stu-id="929bc-153">YOY purchase growth %</span></span>

<span data-ttu-id="929bc-154">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="929bc-154">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="929bc-155">Ostot toimittajan toimipaikan mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="929bc-155">Purchase by vendor location report page</span></span>

<span data-ttu-id="929bc-156">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="929bc-156">**Charts**</span></span>
- <span data-ttu-id="929bc-157">Ostot kaupungin mukaan</span><span class="sxs-lookup"><span data-stu-id="929bc-157">Purchase by city</span></span>
- <span data-ttu-id="929bc-158">Ostojen vuosittainen kasvuprosentti</span><span class="sxs-lookup"><span data-stu-id="929bc-158">Purchase YOY growth %</span></span>
- <span data-ttu-id="929bc-159">Ostot maan mukaan</span><span class="sxs-lookup"><span data-stu-id="929bc-159">Purchase by country</span></span>

<span data-ttu-id="929bc-160">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="929bc-160">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="929bc-161">Ostojen ja kulutuksen analyysi ajan mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="929bc-161">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="929bc-162">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="929bc-162">**Charts**</span></span> 
- <span data-ttu-id="929bc-163">Ostojen kuluva vuosi kuukauden/päivän mukaan (viivakaavio)</span><span class="sxs-lookup"><span data-stu-id="929bc-163">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="929bc-164">Ostojen kuluva ja edellinen vuosi (viiva- ja sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="929bc-164">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="929bc-165">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="929bc-165">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="929bc-166">Ostojen ja kulutuksen analyysi toimittajan mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="929bc-166">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="929bc-167">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="929bc-167">**Charts**</span></span> 
- <span data-ttu-id="929bc-168">10 parasta toimittajaa ostojen prosenttiosuuden mukaan (suppilokaavio)</span><span class="sxs-lookup"><span data-stu-id="929bc-168">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="929bc-169">10 toimittajaa, joiden vuosittainen kulutus on noussut eniten</span><span class="sxs-lookup"><span data-stu-id="929bc-169">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="929bc-170">10 toimittajaa, joiden vuosittainen kulutus on laskenut eniten</span><span class="sxs-lookup"><span data-stu-id="929bc-170">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="929bc-171">**Esimerkki** 
</span><span class="sxs-lookup"><span data-stu-id="929bc-171">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="929bc-172">Tietomalli ja yksiköt</span><span class="sxs-lookup"><span data-stu-id="929bc-172">Data model and entities</span></span>
<span data-ttu-id="929bc-173">Seuraavia tietoja käytetään **osto- ja kulutusanalyysin** Power BI -sisällön raporttisivujen täyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="929bc-173">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="929bc-174">Nämä tiedot esitetään koottuina mittauksina, joka vaiheistetaan yksikkösäilössä.</span><span class="sxs-lookup"><span data-stu-id="929bc-174">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="929bc-175">Yksikkösäilö on analytiikkaa varten optimoitu Microsoft SQL Server -tietokanta.</span><span class="sxs-lookup"><span data-stu-id="929bc-175">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="929bc-176">Lisätietoja on kohdassa [Power BI:n ja yksikkösäilön integraatio](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="929bc-176">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="929bc-177">Sisällön koostetut mittaukset ovat alijoukko Microsoft Dynamics AX 2012:n ja Microsoft Dynamics AX 2012 R3:n ostokuutiossa saatavilla olleista koostetuista mittauksista.</span><span class="sxs-lookup"><span data-stu-id="929bc-177">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="929bc-178">Jotta kuution koostetut mittaukset voi tallentaa yksikkösäilöön, niistä on tehtävä käyttöönottokelpoisia.</span><span class="sxs-lookup"><span data-stu-id="929bc-178">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="929bc-179">Lisätietoja koostettujen mittojen tallentamisesta yksikkösäilöön on kohdassa [Power BI:n ja yksikkösäilön integrointi](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="929bc-179">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="929bc-180">Seuraavat tärkeät koostemitat ovat käytettävissä suoraan laskun rivien yksiköstä. Niitä käytetään sisällön perustana.</span><span class="sxs-lookup"><span data-stu-id="929bc-180">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="929bc-181">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="929bc-181">Entity</span></span>        | <span data-ttu-id="929bc-182">Tärkeät koostemitat</span><span class="sxs-lookup"><span data-stu-id="929bc-182">Key aggregate measurements</span></span> | <span data-ttu-id="929bc-183">Tietolähde</span><span class="sxs-lookup"><span data-stu-id="929bc-183">Data source</span></span>                                 | <span data-ttu-id="929bc-184">Kenttä</span><span class="sxs-lookup"><span data-stu-id="929bc-184">Field</span></span>              | <span data-ttu-id="929bc-185">kuvaus</span><span class="sxs-lookup"><span data-stu-id="929bc-185">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="929bc-186">Laskurivit</span><span class="sxs-lookup"><span data-stu-id="929bc-186">Invoice lines</span></span> | <span data-ttu-id="929bc-187">Osto</span><span class="sxs-lookup"><span data-stu-id="929bc-187">Purchase</span></span>                   | <span data-ttu-id="929bc-188">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="929bc-188">VendInvoiceTrans</span></span>                            | <span data-ttu-id="929bc-189">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="929bc-189">SUM(LineAmountMST)</span></span> | <span data-ttu-id="929bc-190">Summa kirjanpitovaluuttana.</span><span class="sxs-lookup"><span data-stu-id="929bc-190">The amount in the accounting currency.</span></span> |

<span data-ttu-id="929bc-191">Seuraavassa taulukossa esitellään tärkeät mitat, jotka lasketaan sisällössä ja jotka saadaan laskun rivien yksiköstä.</span><span class="sxs-lookup"><span data-stu-id="929bc-191">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="929bc-192">Mitta</span><span class="sxs-lookup"><span data-stu-id="929bc-192">Measure</span></span>               | <span data-ttu-id="929bc-193">Laskelma</span><span class="sxs-lookup"><span data-stu-id="929bc-193">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="929bc-194">Kuluvan vuoden ostot</span><span class="sxs-lookup"><span data-stu-id="929bc-194">Purchase current year</span></span> | <span data-ttu-id="929bc-195">Kuluvan vuoden ostot = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="929bc-195">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="929bc-196">Edellisen vuoden ostot</span><span class="sxs-lookup"><span data-stu-id="929bc-196">Purchase last year</span></span>    | <span data-ttu-id="929bc-197">Edellisen vuoden ostot = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="929bc-197">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="929bc-198">Ostojen vuosittainen kasvu</span><span class="sxs-lookup"><span data-stu-id="929bc-198">YOY purchase growth</span></span>   | <span data-ttu-id="929bc-199">Ostojen vuosittainen kasvu = \[Kuluvan vuoden ostot\] – \[Edellisen vuoden ostot\]</span><span class="sxs-lookup"><span data-stu-id="929bc-199">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="929bc-200">Seuraavia sisällön tärkeitä dimensioita käytetään koostemittojen ositussuodattimina. Tämä parantaa rakeisuutta ja sen avulla saadaan entistä tarkempaa analyysitietoa.</span><span class="sxs-lookup"><span data-stu-id="929bc-200">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="929bc-201">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="929bc-201">Entity</span></span>                 | <span data-ttu-id="929bc-202">Esimerkkejä määritteistä</span><span class="sxs-lookup"><span data-stu-id="929bc-202">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="929bc-203">Toimittajat</span><span class="sxs-lookup"><span data-stu-id="929bc-203">Vendors</span></span>                | <span data-ttu-id="929bc-204">Toimittajaryhmät, toimittajan maa tai alueet, toimittajan nimi</span><span class="sxs-lookup"><span data-stu-id="929bc-204">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="929bc-205">Tuotteet</span><span class="sxs-lookup"><span data-stu-id="929bc-205">Products</span></span>               | <span data-ttu-id="929bc-206">Tuotenumero, tuotteen nimi, nimikeryhmien nimi</span><span class="sxs-lookup"><span data-stu-id="929bc-206">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="929bc-207">Hankintaluokat</span><span class="sxs-lookup"><span data-stu-id="929bc-207">Procurement categories</span></span> | <span data-ttu-id="929bc-208">Hankintaluokka, hankintaluokkien nimet</span><span class="sxs-lookup"><span data-stu-id="929bc-208">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="929bc-209">Oikeushenkilöt</span><span class="sxs-lookup"><span data-stu-id="929bc-209">Legal entities</span></span>         | <span data-ttu-id="929bc-210">Yrityksen nimi</span><span class="sxs-lookup"><span data-stu-id="929bc-210">Legal entity name</span></span>                                     |
| <span data-ttu-id="929bc-211">Päivämäärät</span><span class="sxs-lookup"><span data-stu-id="929bc-211">Dates</span></span>                  | <span data-ttu-id="929bc-212">Päivämäärät, vuosisiirtymä</span><span class="sxs-lookup"><span data-stu-id="929bc-212">Dates, Year offset</span></span>                                    |

<span data-ttu-id="929bc-213">Kuluvan kalenterivuoden tiedot näkyvät oletusarvoisesti sisällössä.</span><span class="sxs-lookup"><span data-stu-id="929bc-213">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="929bc-214">Voit kuitenkin muuttaa päivämääräsuodatinta raportin suodatinosassa.</span><span class="sxs-lookup"><span data-stu-id="929bc-214">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="929bc-215">Voit muuttaa myös yrityssuodatinta.</span><span class="sxs-lookup"><span data-stu-id="929bc-215">You can also change the company filter.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]