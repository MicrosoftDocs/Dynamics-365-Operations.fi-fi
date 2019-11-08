---
title: Osto- ja kulutusanalyysin Power BI -sisältö
description: Tässä ohjeaiheessa kerrotaan, mitä osto- ja kulutusanalyysin Power BI -sisältö sisältää. Siinä selitetään, miten sisältöön sisältyvät raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d25bacc2ec1f8e13376b96e188b099a184f7f8c6
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569129"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="0e84b-104">Osto- ja kulutusanalyysin Power BI -sisältö</span><span class="sxs-lookup"><span data-stu-id="0e84b-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e84b-105">Tässä ohjeaiheessa kerrotaan, mitä **osto- ja kulutusanalyysin** Microsoft Power BI -sisältö sisältää.</span><span class="sxs-lookup"><span data-stu-id="0e84b-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="0e84b-106">Siinä selitetään, miten sisältyvät Power BI -raportit avataan, sekä kerrotaan sisällön muodostamisessa käytettävistä tietomallista ja yksiköistä.</span><span class="sxs-lookup"><span data-stu-id="0e84b-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="0e84b-107">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="0e84b-107">Overview</span></span>

<span data-ttu-id="0e84b-108">**Osto- ja kustannusanalyysin** Power BI -sisältö on suunniteltu ostopäälliköiden ja budjetista vastaavien esimiesten käyttöön, sillä auttaa seuraamaan ostoja ja kulutusta.</span><span class="sxs-lookup"><span data-stu-id="0e84b-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="0e84b-109">Esimiehet voivat analysoida ostoja ja kulutusta seuraavin tavoin:</span><span class="sxs-lookup"><span data-stu-id="0e84b-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="0e84b-110">Ostot vuoden alusta (toimittajaryhmän ja yksittäisten toimittajien, hankintaluokan ja yksittäisten tuotteiden ja toimittajan sijainnin mukaan)</span><span class="sxs-lookup"><span data-stu-id="0e84b-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="0e84b-111">Ostojen vuosittainen muutos (toimittajaryhmän ja hankintaluokan mukaan)</span><span class="sxs-lookup"><span data-stu-id="0e84b-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="0e84b-112">Sisältö käyttää ostotapahtumiin liittyviä tietoja ja antaa koko yrityksen ostolukujen koostenäkymän sekä toimittaja- ja tuotekohtaisen erittelyn ostoista ja kulutuksesta.</span><span class="sxs-lookup"><span data-stu-id="0e84b-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="0e84b-113">Raportit korostavat ostojen ja kulutuksen muutoksia ajanjakson aikana.</span><span class="sxs-lookup"><span data-stu-id="0e84b-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="0e84b-114">Tämän vuoksi raportteja voidaan käyttää, kun esimiehille ilmoitetaan yksittäisten toimittajien ja tuotteiden positiivisista ja negatiivisista kulutussuuntauksista.</span><span class="sxs-lookup"><span data-stu-id="0e84b-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="0e84b-115">Lisäksi kaaviot osoittavat eri hankintaluokkien ja toimittajaryhmien ostot ja kulutuksen.</span><span class="sxs-lookup"><span data-stu-id="0e84b-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="0e84b-116">Näin ollen luokka- ja aluepäälliköitä voivat käyttää kaavioita apuna kulutuskäyttäytymisessä tapahtuvien muutoksien havaitsemisessa.</span><span class="sxs-lookup"><span data-stu-id="0e84b-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="0e84b-117">Power BI -sisällön käyttäminen</span><span class="sxs-lookup"><span data-stu-id="0e84b-117">Accessing the Power BI content</span></span>
<span data-ttu-id="0e84b-118">**Osto- ja kulutusanalyysin** Power BI -sisältö näkyy **Osto- ja kulutusanalyysi** -sivulla (**Hankinta** \> **Kyselyt ja raportit** \> **Ostojen suorituskykyanalyysi** \> **Osto- ja kulutusanalyysi**).</span><span class="sxs-lookup"><span data-stu-id="0e84b-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="0e84b-119">Mittarit, jotka sisältyvät Power BI -sisältöön</span><span class="sxs-lookup"><span data-stu-id="0e84b-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="0e84b-120">**Ostojen ja kulutuksen analyysin** Power BI -sisältöön kuuluu raportti, joka koostuu mittarijoukosta.</span><span class="sxs-lookup"><span data-stu-id="0e84b-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="0e84b-121">Nämä mittarit visualisoidaan kaavioina, ruutuina ja taulukoina.</span><span class="sxs-lookup"><span data-stu-id="0e84b-121">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="0e84b-122">Seuraavassa osissa on visualisointien yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="0e84b-122">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="0e84b-123">Ostot toimittajan mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="0e84b-123">Purchase by vendor report page</span></span>
<span data-ttu-id="0e84b-124">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="0e84b-124">**Charts**</span></span>
- <span data-ttu-id="0e84b-125">10 parasta toimittajaa ostojen mukaan (pinottu palkkikaavio)</span><span class="sxs-lookup"><span data-stu-id="0e84b-125">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="0e84b-126">Ostot yhteensä toimittajaryhmän/maan/nimen mukaan (ympyräkaavio)</span><span class="sxs-lookup"><span data-stu-id="0e84b-126">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="0e84b-127">Ostot toimittajaryhmän/maan/nimen mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="0e84b-127">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="0e84b-128">Ostot keskimäärin toimittajaryhmän/maan/nimen mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="0e84b-128">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="0e84b-129">**Ruudut**</span><span class="sxs-lookup"><span data-stu-id="0e84b-129">**Tiles**</span></span>
- <span data-ttu-id="0e84b-130">Osto yhteensä</span><span class="sxs-lookup"><span data-stu-id="0e84b-130">Total purchase</span></span>
- <span data-ttu-id="0e84b-131">Ostojen vuosittainen kasvu</span><span class="sxs-lookup"><span data-stu-id="0e84b-131">YOY purchase growth</span></span>
- <span data-ttu-id="0e84b-132">Toimittajien kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="0e84b-132">Total # vendors</span></span>
- <span data-ttu-id="0e84b-133">Aktiivisten toimittajien kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="0e84b-133">Total # of active vendors</span></span>

<span data-ttu-id="0e84b-134">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="0e84b-134">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="0e84b-135">Ostot tuotteen mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="0e84b-135">Purchase by product report page</span></span>

<span data-ttu-id="0e84b-136">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="0e84b-136">**Charts**</span></span>
- <span data-ttu-id="0e84b-137">Ostot hankintaluokan / tuotteen nimen mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="0e84b-137">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="0e84b-138">Ostot yhteensä hankintaluokan / tuotteen nimen mukaan (ympyräkaavio)</span><span class="sxs-lookup"><span data-stu-id="0e84b-138">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="0e84b-139">10 parasta tuotetta ostojen mukaan (pinottu palkkikaavio)</span><span class="sxs-lookup"><span data-stu-id="0e84b-139">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="0e84b-140">**Ruudut**</span><span class="sxs-lookup"><span data-stu-id="0e84b-140">**Tiles**</span></span>
- <span data-ttu-id="0e84b-141">Tuotteiden kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="0e84b-141">Total # of products</span></span></li>
- <span data-ttu-id="0e84b-142">Kaikkien aktiivisten tuotteiden prosenttiosuus tuotteiden kokonaismäärästä</span><span class="sxs-lookup"><span data-stu-id="0e84b-142">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="0e84b-143">Tuotteiden määrä, joista koostuu 80 % ostoista</span><span class="sxs-lookup"><span data-stu-id="0e84b-143">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="0e84b-144">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="0e84b-144">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="0e84b-145">Ostot ajanjakson mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="0e84b-145">Purchase by period report page</span></span>
<span data-ttu-id="0e84b-146">Tällä sivulla nähdään ostot tänä ja edellisenä vuonna sekä kasvu hankintaluokan mukaan.</span><span class="sxs-lookup"><span data-stu-id="0e84b-146">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="0e84b-147">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="0e84b-147">**Charts**</span></span> 
- <span data-ttu-id="0e84b-148">Ostot kuukauden/päivän mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="0e84b-148">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="0e84b-149">Kumulatiivisten ostojen vuosittainen varianssi (vesiputouskaavio)</span><span class="sxs-lookup"><span data-stu-id="0e84b-149">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="0e84b-150">Ostot yhteensä, vuosittainen kasvu (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="0e84b-150">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="0e84b-151">Hankintaraportti (matriisi)</span><span class="sxs-lookup"><span data-stu-id="0e84b-151">Procurement statement (matrix)</span></span>

<span data-ttu-id="0e84b-152">**Ruudut**</span><span class="sxs-lookup"><span data-stu-id="0e84b-152">**Tiles**</span></span>
- <span data-ttu-id="0e84b-153">Ostojen vuosittainen kasvu</span><span class="sxs-lookup"><span data-stu-id="0e84b-153">YOY purchase growth</span></span>
- <span data-ttu-id="0e84b-154">Ostojen vuosittainen kasvuprosentti</span><span class="sxs-lookup"><span data-stu-id="0e84b-154">YOY purchase growth %</span></span>

<span data-ttu-id="0e84b-155">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="0e84b-155">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="0e84b-156">Ostot toimittajan toimipaikan mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="0e84b-156">Purchase by vendor location report page</span></span>

<span data-ttu-id="0e84b-157">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="0e84b-157">**Charts**</span></span>
- <span data-ttu-id="0e84b-158">Ostot kaupungin mukaan</span><span class="sxs-lookup"><span data-stu-id="0e84b-158">Purchase by city</span></span>
- <span data-ttu-id="0e84b-159">Ostojen vuosittainen kasvuprosentti</span><span class="sxs-lookup"><span data-stu-id="0e84b-159">Purchase YOY growth %</span></span>
- <span data-ttu-id="0e84b-160">Ostot maan mukaan</span><span class="sxs-lookup"><span data-stu-id="0e84b-160">Purchase by country</span></span>

<span data-ttu-id="0e84b-161">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="0e84b-161">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="0e84b-162">Ostojen ja kulutuksen analyysi ajan mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="0e84b-162">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="0e84b-163">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="0e84b-163">**Charts**</span></span> 
- <span data-ttu-id="0e84b-164">Ostojen kuluva vuosi kuukauden/päivän mukaan (viivakaavio)</span><span class="sxs-lookup"><span data-stu-id="0e84b-164">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="0e84b-165">Ostojen kuluva ja edellinen vuosi (viiva- ja sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="0e84b-165">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="0e84b-166">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="0e84b-166">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="0e84b-167">Ostojen ja kulutuksen analyysi toimittajan mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="0e84b-167">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="0e84b-168">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="0e84b-168">**Charts**</span></span> 
- <span data-ttu-id="0e84b-169">10 parasta toimittajaa ostojen prosenttiosuuden mukaan (suppilokaavio)</span><span class="sxs-lookup"><span data-stu-id="0e84b-169">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="0e84b-170">10 toimittajaa, joiden vuosittainen kulutus on noussut eniten</span><span class="sxs-lookup"><span data-stu-id="0e84b-170">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="0e84b-171">10 toimittajaa, joiden vuosittainen kulutus on laskenut eniten</span><span class="sxs-lookup"><span data-stu-id="0e84b-171">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="0e84b-172">**Esimerkki** 
</span><span class="sxs-lookup"><span data-stu-id="0e84b-172">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="0e84b-173">Tietomalli ja yksiköt</span><span class="sxs-lookup"><span data-stu-id="0e84b-173">Data model and entities</span></span>
<span data-ttu-id="0e84b-174">Seuraavia tietoja käytetään **osto- ja kulutusanalyysin** Power BI -sisällön raporttisivujen täyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="0e84b-174">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="0e84b-175">Nämä tiedot esitetään koottuina mittauksina, joka vaiheistetaan yksikkösäilössä.</span><span class="sxs-lookup"><span data-stu-id="0e84b-175">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="0e84b-176">Yksikkösäilö on analytiikkaa varten optimoitu Microsoft SQL Server -tietokanta.</span><span class="sxs-lookup"><span data-stu-id="0e84b-176">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="0e84b-177">Lisätietoja on kohdassa [Power BI:n ja yksikkösäilön integroinnin yleiskatsaus](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="0e84b-177">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="0e84b-178">Sisällön koostetut mittaukset ovat alijoukko Microsoft Dynamics AX 2012:n ja Microsoft Dynamics AX 2012 R3:n ostokuutiossa saatavilla olleista koostetuista mittauksista.</span><span class="sxs-lookup"><span data-stu-id="0e84b-178">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="0e84b-179">Jotta kuution koostetut mittaukset voi tallentaa yksikkösäilöön, niistä on tehtävä käyttöönottokelpoisia.</span><span class="sxs-lookup"><span data-stu-id="0e84b-179">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="0e84b-180">Lisätietoja koostettujen mittojen tallentamisesta yksikkösäilöön on kohdassa [Power BI:n ja yksikkösäilön integroinnin yleiskatsaus](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="0e84b-180">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="0e84b-181">Seuraavat tärkeät koostemitat ovat käytettävissä suoraan laskun rivien yksiköstä. Niitä käytetään sisällön perustana.</span><span class="sxs-lookup"><span data-stu-id="0e84b-181">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="0e84b-182">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="0e84b-182">Entity</span></span>        | <span data-ttu-id="0e84b-183">Tärkeät koostemitat</span><span class="sxs-lookup"><span data-stu-id="0e84b-183">Key aggregate measurements</span></span> | <span data-ttu-id="0e84b-184">Tietolähde</span><span class="sxs-lookup"><span data-stu-id="0e84b-184">Data source</span></span>                                 | <span data-ttu-id="0e84b-185">Kenttä</span><span class="sxs-lookup"><span data-stu-id="0e84b-185">Field</span></span>              | <span data-ttu-id="0e84b-186">kuvaus</span><span class="sxs-lookup"><span data-stu-id="0e84b-186">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="0e84b-187">Laskurivit</span><span class="sxs-lookup"><span data-stu-id="0e84b-187">Invoice lines</span></span> | <span data-ttu-id="0e84b-188">Osto</span><span class="sxs-lookup"><span data-stu-id="0e84b-188">Purchase</span></span>                   | <span data-ttu-id="0e84b-189">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="0e84b-189">VendInvoiceTrans</span></span>                            | <span data-ttu-id="0e84b-190">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="0e84b-190">SUM(LineAmountMST)</span></span> | <span data-ttu-id="0e84b-191">Summa kirjanpitovaluuttana.</span><span class="sxs-lookup"><span data-stu-id="0e84b-191">The amount in the accounting currency.</span></span> |

<span data-ttu-id="0e84b-192">Seuraavassa taulukossa esitellään tärkeät mitat, jotka lasketaan sisällössä ja jotka saadaan laskun rivien yksiköstä.</span><span class="sxs-lookup"><span data-stu-id="0e84b-192">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="0e84b-193">Mitta</span><span class="sxs-lookup"><span data-stu-id="0e84b-193">Measure</span></span>               | <span data-ttu-id="0e84b-194">Laskelma</span><span class="sxs-lookup"><span data-stu-id="0e84b-194">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e84b-195">Kuluvan vuoden ostot</span><span class="sxs-lookup"><span data-stu-id="0e84b-195">Purchase current year</span></span> | <span data-ttu-id="0e84b-196">Kuluvan vuoden ostot = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="0e84b-196">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="0e84b-197">Edellisen vuoden ostot</span><span class="sxs-lookup"><span data-stu-id="0e84b-197">Purchase last year</span></span>    | <span data-ttu-id="0e84b-198">Edellisen vuoden ostot = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="0e84b-198">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="0e84b-199">Ostojen vuosittainen kasvu</span><span class="sxs-lookup"><span data-stu-id="0e84b-199">YOY purchase growth</span></span>   | <span data-ttu-id="0e84b-200">Ostojen vuosittainen kasvu = \[Kuluvan vuoden ostot\] – \[Edellisen vuoden ostot\]</span><span class="sxs-lookup"><span data-stu-id="0e84b-200">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="0e84b-201">Seuraavia sisällön tärkeitä dimensioita käytetään koostemittojen ositussuodattimina. Tämä parantaa rakeisuutta ja sen avulla saadaan entistä tarkempaa analyysitietoa.</span><span class="sxs-lookup"><span data-stu-id="0e84b-201">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="0e84b-202">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="0e84b-202">Entity</span></span>                 | <span data-ttu-id="0e84b-203">Esimerkkejä määritteistä</span><span class="sxs-lookup"><span data-stu-id="0e84b-203">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="0e84b-204">Toimittajat</span><span class="sxs-lookup"><span data-stu-id="0e84b-204">Vendors</span></span>                | <span data-ttu-id="0e84b-205">Toimittajaryhmät, toimittajan maa tai alueet, toimittajan nimi</span><span class="sxs-lookup"><span data-stu-id="0e84b-205">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="0e84b-206">Tuotteet</span><span class="sxs-lookup"><span data-stu-id="0e84b-206">Products</span></span>               | <span data-ttu-id="0e84b-207">Tuotenumero, tuotteen nimi, nimikeryhmien nimi</span><span class="sxs-lookup"><span data-stu-id="0e84b-207">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="0e84b-208">Hankintaluokat</span><span class="sxs-lookup"><span data-stu-id="0e84b-208">Procurement categories</span></span> | <span data-ttu-id="0e84b-209">Hankintaluokka, hankintaluokkien nimet</span><span class="sxs-lookup"><span data-stu-id="0e84b-209">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="0e84b-210">Oikeushenkilöt</span><span class="sxs-lookup"><span data-stu-id="0e84b-210">Legal entities</span></span>         | <span data-ttu-id="0e84b-211">Yrityksen nimi</span><span class="sxs-lookup"><span data-stu-id="0e84b-211">Legal entity name</span></span>                                     |
| <span data-ttu-id="0e84b-212">Päivämäärät</span><span class="sxs-lookup"><span data-stu-id="0e84b-212">Dates</span></span>                  | <span data-ttu-id="0e84b-213">Päivämäärät, vuosisiirtymä</span><span class="sxs-lookup"><span data-stu-id="0e84b-213">Dates, Year offset</span></span>                                    |

<span data-ttu-id="0e84b-214">Kuluvan kalenterivuoden tiedot näkyvät oletusarvoisesti sisällössä.</span><span class="sxs-lookup"><span data-stu-id="0e84b-214">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="0e84b-215">Voit kuitenkin muuttaa päivämääräsuodatinta raportin suodatinosassa.</span><span class="sxs-lookup"><span data-stu-id="0e84b-215">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="0e84b-216">Voit muuttaa myös yrityssuodatinta.</span><span class="sxs-lookup"><span data-stu-id="0e84b-216">You can also change the company filter.</span></span>
