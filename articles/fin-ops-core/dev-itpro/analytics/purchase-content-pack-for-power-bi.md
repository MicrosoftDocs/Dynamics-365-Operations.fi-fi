---
title: Osto- ja kulutusanalyysin Power BI -sisältö
description: Tässä ohjeaiheessa kerrotaan, mitä osto- ja kulutusanalyysin Power BI -sisältö sisältää.
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
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5914abaafab509e278d7a85441928feddb0b5164
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093439"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="8e2ed-103">Osto- ja kulutusanalyysin Power BI -sisältö</span><span class="sxs-lookup"><span data-stu-id="8e2ed-103">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e2ed-104">Tässä ohjeaiheessa kerrotaan, mitä **osto- ja kulutusanalyysin** Microsoft Power BI -sisältö sisältää.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-104">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="8e2ed-105">Siinä selitetään, miten sisältyvät Power BI -raportit avataan, sekä kerrotaan sisällön muodostamisessa käytettävistä tietomallista ja yksiköistä.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-105">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="8e2ed-106">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="8e2ed-106">Overview</span></span>

<span data-ttu-id="8e2ed-107">**Osto- ja kustannusanalyysin** Power BI -sisältö on suunniteltu ostopäälliköiden ja budjetista vastaavien esimiesten käyttöön, sillä auttaa seuraamaan ostoja ja kulutusta.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-107">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="8e2ed-108">Esimiehet voivat analysoida ostoja ja kulutusta seuraavin tavoin:</span><span class="sxs-lookup"><span data-stu-id="8e2ed-108">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="8e2ed-109">Ostot vuoden alusta (toimittajaryhmän ja yksittäisten toimittajien, hankintaluokan ja yksittäisten tuotteiden ja toimittajan sijainnin mukaan)</span><span class="sxs-lookup"><span data-stu-id="8e2ed-109">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="8e2ed-110">Ostojen vuosittainen muutos (toimittajaryhmän ja hankintaluokan mukaan)</span><span class="sxs-lookup"><span data-stu-id="8e2ed-110">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="8e2ed-111">Sisältö käyttää ostotapahtumiin liittyviä tietoja ja antaa koko yrityksen ostolukujen koostenäkymän sekä toimittaja- ja tuotekohtaisen erittelyn ostoista ja kulutuksesta.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-111">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="8e2ed-112">Raportit korostavat ostojen ja kulutuksen muutoksia ajanjakson aikana.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-112">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="8e2ed-113">Tämän vuoksi raportteja voidaan käyttää, kun esimiehille ilmoitetaan yksittäisten toimittajien ja tuotteiden positiivisista ja negatiivisista kulutussuuntauksista.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-113">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="8e2ed-114">Lisäksi kaaviot osoittavat eri hankintaluokkien ja toimittajaryhmien ostot ja kulutuksen.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-114">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="8e2ed-115">Näin ollen luokka- ja aluepäälliköitä voivat käyttää kaavioita apuna kulutuskäyttäytymisessä tapahtuvien muutoksien havaitsemisessa.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-115">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="8e2ed-116">Power BI -sisällön käyttäminen</span><span class="sxs-lookup"><span data-stu-id="8e2ed-116">Accessing the Power BI content</span></span>
<span data-ttu-id="8e2ed-117">**Osto- ja kulutusanalyysin** Power BI -sisältö näkyy **Osto- ja kulutusanalyysi** -sivulla (**Hankinta** \> **Kyselyt ja raportit** \> **Ostojen suorituskykyanalyysi** \> **Osto- ja kulutusanalyysi**).</span><span class="sxs-lookup"><span data-stu-id="8e2ed-117">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="8e2ed-118">Mittarit, jotka sisältyvät Power BI -sisältöön</span><span class="sxs-lookup"><span data-stu-id="8e2ed-118">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="8e2ed-119">**Ostojen ja kulutuksen analyysin** Power BI -sisältöön kuuluu raportti, joka koostuu mittarijoukosta.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-119">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="8e2ed-120">Nämä mittarit visualisoidaan kaavioina, ruutuina ja taulukoina.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-120">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="8e2ed-121">Seuraavassa osissa on visualisointien yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-121">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="8e2ed-122">Ostot toimittajan mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="8e2ed-122">Purchase by vendor report page</span></span>
<span data-ttu-id="8e2ed-123">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="8e2ed-123">**Charts**</span></span>
- <span data-ttu-id="8e2ed-124">10 parasta toimittajaa ostojen mukaan (pinottu palkkikaavio)</span><span class="sxs-lookup"><span data-stu-id="8e2ed-124">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="8e2ed-125">Ostot yhteensä toimittajaryhmän/maan/nimen mukaan (ympyräkaavio)</span><span class="sxs-lookup"><span data-stu-id="8e2ed-125">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="8e2ed-126">Ostot toimittajaryhmän/maan/nimen mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="8e2ed-126">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="8e2ed-127">Ostot keskimäärin toimittajaryhmän/maan/nimen mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="8e2ed-127">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="8e2ed-128">**Ruudut**</span><span class="sxs-lookup"><span data-stu-id="8e2ed-128">**Tiles**</span></span>
- <span data-ttu-id="8e2ed-129">Osto yhteensä</span><span class="sxs-lookup"><span data-stu-id="8e2ed-129">Total purchase</span></span>
- <span data-ttu-id="8e2ed-130">Ostojen vuosittainen kasvu</span><span class="sxs-lookup"><span data-stu-id="8e2ed-130">YOY purchase growth</span></span>
- <span data-ttu-id="8e2ed-131">Toimittajien kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="8e2ed-131">Total # vendors</span></span>
- <span data-ttu-id="8e2ed-132">Aktiivisten toimittajien kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="8e2ed-132">Total # of active vendors</span></span>

<span data-ttu-id="8e2ed-133">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="8e2ed-133">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="8e2ed-134">Ostot tuotteen mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="8e2ed-134">Purchase by product report page</span></span>

<span data-ttu-id="8e2ed-135">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="8e2ed-135">**Charts**</span></span>
- <span data-ttu-id="8e2ed-136">Ostot hankintaluokan / tuotteen nimen mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="8e2ed-136">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="8e2ed-137">Ostot yhteensä hankintaluokan / tuotteen nimen mukaan (ympyräkaavio)</span><span class="sxs-lookup"><span data-stu-id="8e2ed-137">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="8e2ed-138">10 parasta tuotetta ostojen mukaan (pinottu palkkikaavio)</span><span class="sxs-lookup"><span data-stu-id="8e2ed-138">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="8e2ed-139">**Ruudut**</span><span class="sxs-lookup"><span data-stu-id="8e2ed-139">**Tiles**</span></span>
- <span data-ttu-id="8e2ed-140">Tuotteiden kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="8e2ed-140">Total # of products</span></span></li>
- <span data-ttu-id="8e2ed-141">Kaikkien aktiivisten tuotteiden prosenttiosuus tuotteiden kokonaismäärästä</span><span class="sxs-lookup"><span data-stu-id="8e2ed-141">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="8e2ed-142">Tuotteiden määrä, joista koostuu 80 % ostoista</span><span class="sxs-lookup"><span data-stu-id="8e2ed-142">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="8e2ed-143">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="8e2ed-143">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="8e2ed-144">Ostot ajanjakson mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="8e2ed-144">Purchase by period report page</span></span>
<span data-ttu-id="8e2ed-145">Tällä sivulla nähdään ostot tänä ja edellisenä vuonna sekä kasvu hankintaluokan mukaan.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-145">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="8e2ed-146">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="8e2ed-146">**Charts**</span></span> 
- <span data-ttu-id="8e2ed-147">Ostot kuukauden/päivän mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="8e2ed-147">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="8e2ed-148">Kumulatiivisten ostojen vuosittainen varianssi (vesiputouskaavio)</span><span class="sxs-lookup"><span data-stu-id="8e2ed-148">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="8e2ed-149">Ostot yhteensä, vuosittainen kasvu (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="8e2ed-149">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="8e2ed-150">Hankintaraportti (matriisi)</span><span class="sxs-lookup"><span data-stu-id="8e2ed-150">Procurement statement (matrix)</span></span>

<span data-ttu-id="8e2ed-151">**Ruudut**</span><span class="sxs-lookup"><span data-stu-id="8e2ed-151">**Tiles**</span></span>
- <span data-ttu-id="8e2ed-152">Ostojen vuosittainen kasvu</span><span class="sxs-lookup"><span data-stu-id="8e2ed-152">YOY purchase growth</span></span>
- <span data-ttu-id="8e2ed-153">Ostojen vuosittainen kasvuprosentti</span><span class="sxs-lookup"><span data-stu-id="8e2ed-153">YOY purchase growth %</span></span>

<span data-ttu-id="8e2ed-154">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="8e2ed-154">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="8e2ed-155">Ostot toimittajan toimipaikan mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="8e2ed-155">Purchase by vendor location report page</span></span>

<span data-ttu-id="8e2ed-156">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="8e2ed-156">**Charts**</span></span>
- <span data-ttu-id="8e2ed-157">Ostot kaupungin mukaan</span><span class="sxs-lookup"><span data-stu-id="8e2ed-157">Purchase by city</span></span>
- <span data-ttu-id="8e2ed-158">Ostojen vuosittainen kasvuprosentti</span><span class="sxs-lookup"><span data-stu-id="8e2ed-158">Purchase YOY growth %</span></span>
- <span data-ttu-id="8e2ed-159">Ostot maan mukaan</span><span class="sxs-lookup"><span data-stu-id="8e2ed-159">Purchase by country</span></span>

<span data-ttu-id="8e2ed-160">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="8e2ed-160">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="8e2ed-161">Ostojen ja kulutuksen analyysi ajan mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="8e2ed-161">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="8e2ed-162">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="8e2ed-162">**Charts**</span></span> 
- <span data-ttu-id="8e2ed-163">Ostojen kuluva vuosi kuukauden/päivän mukaan (viivakaavio)</span><span class="sxs-lookup"><span data-stu-id="8e2ed-163">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="8e2ed-164">Ostojen kuluva ja edellinen vuosi (viiva- ja sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="8e2ed-164">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="8e2ed-165">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="8e2ed-165">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="8e2ed-166">Ostojen ja kulutuksen analyysi toimittajan mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="8e2ed-166">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="8e2ed-167">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="8e2ed-167">**Charts**</span></span> 
- <span data-ttu-id="8e2ed-168">10 parasta toimittajaa ostojen prosenttiosuuden mukaan (suppilokaavio)</span><span class="sxs-lookup"><span data-stu-id="8e2ed-168">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="8e2ed-169">10 toimittajaa, joiden vuosittainen kulutus on noussut eniten</span><span class="sxs-lookup"><span data-stu-id="8e2ed-169">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="8e2ed-170">10 toimittajaa, joiden vuosittainen kulutus on laskenut eniten</span><span class="sxs-lookup"><span data-stu-id="8e2ed-170">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="8e2ed-171">**Esimerkki** 
</span><span class="sxs-lookup"><span data-stu-id="8e2ed-171">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="8e2ed-172">Tietomalli ja yksiköt</span><span class="sxs-lookup"><span data-stu-id="8e2ed-172">Data model and entities</span></span>
<span data-ttu-id="8e2ed-173">Seuraavia tietoja käytetään **osto- ja kulutusanalyysin** Power BI -sisällön raporttisivujen täyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-173">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="8e2ed-174">Nämä tiedot esitetään koottuina mittauksina, joka vaiheistetaan yksikkösäilössä.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-174">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="8e2ed-175">Yksikkösäilö on analytiikkaa varten optimoitu Microsoft SQL Server -tietokanta.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-175">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="8e2ed-176">Lisätietoja on kohdassa [Power BI:n ja yksikkösäilön integraatio](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="8e2ed-176">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="8e2ed-177">Sisällön koostetut mittaukset ovat alijoukko Microsoft Dynamics AX 2012:n ja Microsoft Dynamics AX 2012 R3:n ostokuutiossa saatavilla olleista koostetuista mittauksista.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-177">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="8e2ed-178">Jotta kuution koostetut mittaukset voi tallentaa yksikkösäilöön, niistä on tehtävä käyttöönottokelpoisia.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-178">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="8e2ed-179">Lisätietoja koostettujen mittojen tallentamisesta yksikkösäilöön on kohdassa [Power BI:n ja yksikkösäilön integrointi](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="8e2ed-179">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="8e2ed-180">Seuraavat tärkeät koostemitat ovat käytettävissä suoraan laskun rivien yksiköstä. Niitä käytetään sisällön perustana.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-180">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="8e2ed-181">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="8e2ed-181">Entity</span></span>        | <span data-ttu-id="8e2ed-182">Tärkeät koostemitat</span><span class="sxs-lookup"><span data-stu-id="8e2ed-182">Key aggregate measurements</span></span> | <span data-ttu-id="8e2ed-183">Tietolähde</span><span class="sxs-lookup"><span data-stu-id="8e2ed-183">Data source</span></span>                                 | <span data-ttu-id="8e2ed-184">Kenttä</span><span class="sxs-lookup"><span data-stu-id="8e2ed-184">Field</span></span>              | <span data-ttu-id="8e2ed-185">kuvaus</span><span class="sxs-lookup"><span data-stu-id="8e2ed-185">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="8e2ed-186">Laskurivit</span><span class="sxs-lookup"><span data-stu-id="8e2ed-186">Invoice lines</span></span> | <span data-ttu-id="8e2ed-187">Osto</span><span class="sxs-lookup"><span data-stu-id="8e2ed-187">Purchase</span></span>                   | <span data-ttu-id="8e2ed-188">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="8e2ed-188">VendInvoiceTrans</span></span>                            | <span data-ttu-id="8e2ed-189">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="8e2ed-189">SUM(LineAmountMST)</span></span> | <span data-ttu-id="8e2ed-190">Summa kirjanpitovaluuttana.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-190">The amount in the accounting currency.</span></span> |

<span data-ttu-id="8e2ed-191">Seuraavassa taulukossa esitellään tärkeät mitat, jotka lasketaan sisällössä ja jotka saadaan laskun rivien yksiköstä.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-191">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="8e2ed-192">Mitta</span><span class="sxs-lookup"><span data-stu-id="8e2ed-192">Measure</span></span>               | <span data-ttu-id="8e2ed-193">Laskelma</span><span class="sxs-lookup"><span data-stu-id="8e2ed-193">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e2ed-194">Kuluvan vuoden ostot</span><span class="sxs-lookup"><span data-stu-id="8e2ed-194">Purchase current year</span></span> | <span data-ttu-id="8e2ed-195">Kuluvan vuoden ostot = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="8e2ed-195">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="8e2ed-196">Edellisen vuoden ostot</span><span class="sxs-lookup"><span data-stu-id="8e2ed-196">Purchase last year</span></span>    | <span data-ttu-id="8e2ed-197">Edellisen vuoden ostot = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="8e2ed-197">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="8e2ed-198">Ostojen vuosittainen kasvu</span><span class="sxs-lookup"><span data-stu-id="8e2ed-198">YOY purchase growth</span></span>   | <span data-ttu-id="8e2ed-199">Ostojen vuosittainen kasvu = \[Kuluvan vuoden ostot\] – \[Edellisen vuoden ostot\]</span><span class="sxs-lookup"><span data-stu-id="8e2ed-199">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="8e2ed-200">Seuraavia sisällön tärkeitä dimensioita käytetään koostemittojen ositussuodattimina. Tämä parantaa rakeisuutta ja sen avulla saadaan entistä tarkempaa analyysitietoa.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-200">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="8e2ed-201">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="8e2ed-201">Entity</span></span>                 | <span data-ttu-id="8e2ed-202">Esimerkkejä määritteistä</span><span class="sxs-lookup"><span data-stu-id="8e2ed-202">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="8e2ed-203">Toimittajat</span><span class="sxs-lookup"><span data-stu-id="8e2ed-203">Vendors</span></span>                | <span data-ttu-id="8e2ed-204">Toimittajaryhmät, toimittajan maa tai alueet, toimittajan nimi</span><span class="sxs-lookup"><span data-stu-id="8e2ed-204">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="8e2ed-205">Tuotteet</span><span class="sxs-lookup"><span data-stu-id="8e2ed-205">Products</span></span>               | <span data-ttu-id="8e2ed-206">Tuotenumero, tuotteen nimi, nimikeryhmien nimi</span><span class="sxs-lookup"><span data-stu-id="8e2ed-206">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="8e2ed-207">Hankintaluokat</span><span class="sxs-lookup"><span data-stu-id="8e2ed-207">Procurement categories</span></span> | <span data-ttu-id="8e2ed-208">Hankintaluokka, hankintaluokkien nimet</span><span class="sxs-lookup"><span data-stu-id="8e2ed-208">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="8e2ed-209">Oikeushenkilöt</span><span class="sxs-lookup"><span data-stu-id="8e2ed-209">Legal entities</span></span>         | <span data-ttu-id="8e2ed-210">Yrityksen nimi</span><span class="sxs-lookup"><span data-stu-id="8e2ed-210">Legal entity name</span></span>                                     |
| <span data-ttu-id="8e2ed-211">Päivämäärät</span><span class="sxs-lookup"><span data-stu-id="8e2ed-211">Dates</span></span>                  | <span data-ttu-id="8e2ed-212">Päivämäärät, vuosisiirtymä</span><span class="sxs-lookup"><span data-stu-id="8e2ed-212">Dates, Year offset</span></span>                                    |

<span data-ttu-id="8e2ed-213">Kuluvan kalenterivuoden tiedot näkyvät oletusarvoisesti sisällössä.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-213">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="8e2ed-214">Voit kuitenkin muuttaa päivämääräsuodatinta raportin suodatinosassa.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-214">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="8e2ed-215">Voit muuttaa myös yrityssuodatinta.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-215">You can also change the company filter.</span></span>
