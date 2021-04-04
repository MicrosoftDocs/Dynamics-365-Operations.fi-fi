---
title: Osto- ja kulutusanalyysin Power BI -sisältö
description: Tässä ohjeaiheessa kerrotaan, mitä osto- ja kulutusanalyysin Power BI -sisältö sisältää.
author: FrankDahl
manager: AnnBe
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
ms.openlocfilehash: a4149b13754b544558dbb5666fbec7df97e5c5d8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559546"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="f7d2a-103">Osto- ja kulutusanalyysin Power BI -sisältö</span><span class="sxs-lookup"><span data-stu-id="f7d2a-103">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7d2a-104">Tässä ohjeaiheessa kerrotaan, mitä **osto- ja kulutusanalyysin** Microsoft Power BI -sisältö sisältää.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-104">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="f7d2a-105">Siinä selitetään, miten sisältyvät Power BI -raportit avataan, sekä kerrotaan sisällön muodostamisessa käytettävistä tietomallista ja yksiköistä.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-105">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="f7d2a-106">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="f7d2a-106">Overview</span></span>

<span data-ttu-id="f7d2a-107">**Osto- ja kustannusanalyysin** Power BI -sisältö on suunniteltu ostopäälliköiden ja budjetista vastaavien esimiesten käyttöön, sillä auttaa seuraamaan ostoja ja kulutusta.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-107">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="f7d2a-108">Esimiehet voivat analysoida ostoja ja kulutusta seuraavin tavoin:</span><span class="sxs-lookup"><span data-stu-id="f7d2a-108">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="f7d2a-109">Ostot vuoden alusta (toimittajaryhmän ja yksittäisten toimittajien, hankintaluokan ja yksittäisten tuotteiden ja toimittajan sijainnin mukaan)</span><span class="sxs-lookup"><span data-stu-id="f7d2a-109">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="f7d2a-110">Ostojen vuosittainen muutos (toimittajaryhmän ja hankintaluokan mukaan)</span><span class="sxs-lookup"><span data-stu-id="f7d2a-110">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="f7d2a-111">Sisältö käyttää ostotapahtumiin liittyviä tietoja ja antaa koko yrityksen ostolukujen koostenäkymän sekä toimittaja- ja tuotekohtaisen erittelyn ostoista ja kulutuksesta.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-111">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="f7d2a-112">Raportit korostavat ostojen ja kulutuksen muutoksia ajanjakson aikana.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-112">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="f7d2a-113">Tämän vuoksi raportteja voidaan käyttää, kun esimiehille ilmoitetaan yksittäisten toimittajien ja tuotteiden positiivisista ja negatiivisista kulutussuuntauksista.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-113">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="f7d2a-114">Lisäksi kaaviot osoittavat eri hankintaluokkien ja toimittajaryhmien ostot ja kulutuksen.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-114">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="f7d2a-115">Näin ollen luokka- ja aluepäälliköitä voivat käyttää kaavioita apuna kulutuskäyttäytymisessä tapahtuvien muutoksien havaitsemisessa.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-115">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="f7d2a-116">Power BI -sisällön käyttäminen</span><span class="sxs-lookup"><span data-stu-id="f7d2a-116">Accessing the Power BI content</span></span>
<span data-ttu-id="f7d2a-117">**Osto- ja kulutusanalyysin** Power BI -sisältö näkyy **Osto- ja kulutusanalyysi** -sivulla (**Hankinta** \> **Kyselyt ja raportit** \> **Ostojen suorituskykyanalyysi** \> **Osto- ja kulutusanalyysi**).</span><span class="sxs-lookup"><span data-stu-id="f7d2a-117">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="f7d2a-118">Mittarit, jotka sisältyvät Power BI -sisältöön</span><span class="sxs-lookup"><span data-stu-id="f7d2a-118">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="f7d2a-119">**Ostojen ja kulutuksen analyysin** Power BI -sisältöön kuuluu raportti, joka koostuu mittarijoukosta.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-119">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="f7d2a-120">Nämä mittarit visualisoidaan kaavioina, ruutuina ja taulukoina.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-120">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="f7d2a-121">Seuraavassa osissa on visualisointien yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-121">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="f7d2a-122">Ostot toimittajan mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="f7d2a-122">Purchase by vendor report page</span></span>
<span data-ttu-id="f7d2a-123">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="f7d2a-123">**Charts**</span></span>
- <span data-ttu-id="f7d2a-124">10 parasta toimittajaa ostojen mukaan (pinottu palkkikaavio)</span><span class="sxs-lookup"><span data-stu-id="f7d2a-124">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="f7d2a-125">Ostot yhteensä toimittajaryhmän/maan/nimen mukaan (ympyräkaavio)</span><span class="sxs-lookup"><span data-stu-id="f7d2a-125">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="f7d2a-126">Ostot toimittajaryhmän/maan/nimen mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="f7d2a-126">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="f7d2a-127">Ostot keskimäärin toimittajaryhmän/maan/nimen mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="f7d2a-127">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="f7d2a-128">**Ruudut**</span><span class="sxs-lookup"><span data-stu-id="f7d2a-128">**Tiles**</span></span>
- <span data-ttu-id="f7d2a-129">Osto yhteensä</span><span class="sxs-lookup"><span data-stu-id="f7d2a-129">Total purchase</span></span>
- <span data-ttu-id="f7d2a-130">Ostojen vuosittainen kasvu</span><span class="sxs-lookup"><span data-stu-id="f7d2a-130">YOY purchase growth</span></span>
- <span data-ttu-id="f7d2a-131">Toimittajien kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="f7d2a-131">Total # vendors</span></span>
- <span data-ttu-id="f7d2a-132">Aktiivisten toimittajien kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="f7d2a-132">Total # of active vendors</span></span>

<span data-ttu-id="f7d2a-133">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="f7d2a-133">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="f7d2a-134">Ostot tuotteen mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="f7d2a-134">Purchase by product report page</span></span>

<span data-ttu-id="f7d2a-135">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="f7d2a-135">**Charts**</span></span>
- <span data-ttu-id="f7d2a-136">Ostot hankintaluokan / tuotteen nimen mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="f7d2a-136">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="f7d2a-137">Ostot yhteensä hankintaluokan / tuotteen nimen mukaan (ympyräkaavio)</span><span class="sxs-lookup"><span data-stu-id="f7d2a-137">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="f7d2a-138">10 parasta tuotetta ostojen mukaan (pinottu palkkikaavio)</span><span class="sxs-lookup"><span data-stu-id="f7d2a-138">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="f7d2a-139">**Ruudut**</span><span class="sxs-lookup"><span data-stu-id="f7d2a-139">**Tiles**</span></span>
- <span data-ttu-id="f7d2a-140">Tuotteiden kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="f7d2a-140">Total # of products</span></span></li>
- <span data-ttu-id="f7d2a-141">Kaikkien aktiivisten tuotteiden prosenttiosuus tuotteiden kokonaismäärästä</span><span class="sxs-lookup"><span data-stu-id="f7d2a-141">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="f7d2a-142">Tuotteiden määrä, joista koostuu 80 % ostoista</span><span class="sxs-lookup"><span data-stu-id="f7d2a-142">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="f7d2a-143">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="f7d2a-143">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="f7d2a-144">Ostot ajanjakson mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="f7d2a-144">Purchase by period report page</span></span>
<span data-ttu-id="f7d2a-145">Tällä sivulla nähdään ostot tänä ja edellisenä vuonna sekä kasvu hankintaluokan mukaan.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-145">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="f7d2a-146">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="f7d2a-146">**Charts**</span></span> 
- <span data-ttu-id="f7d2a-147">Ostot kuukauden/päivän mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="f7d2a-147">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="f7d2a-148">Kumulatiivisten ostojen vuosittainen varianssi (vesiputouskaavio)</span><span class="sxs-lookup"><span data-stu-id="f7d2a-148">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="f7d2a-149">Ostot yhteensä, vuosittainen kasvu (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="f7d2a-149">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="f7d2a-150">Hankintaraportti (matriisi)</span><span class="sxs-lookup"><span data-stu-id="f7d2a-150">Procurement statement (matrix)</span></span>

<span data-ttu-id="f7d2a-151">**Ruudut**</span><span class="sxs-lookup"><span data-stu-id="f7d2a-151">**Tiles**</span></span>
- <span data-ttu-id="f7d2a-152">Ostojen vuosittainen kasvu</span><span class="sxs-lookup"><span data-stu-id="f7d2a-152">YOY purchase growth</span></span>
- <span data-ttu-id="f7d2a-153">Ostojen vuosittainen kasvuprosentti</span><span class="sxs-lookup"><span data-stu-id="f7d2a-153">YOY purchase growth %</span></span>

<span data-ttu-id="f7d2a-154">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="f7d2a-154">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="f7d2a-155">Ostot toimittajan toimipaikan mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="f7d2a-155">Purchase by vendor location report page</span></span>

<span data-ttu-id="f7d2a-156">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="f7d2a-156">**Charts**</span></span>
- <span data-ttu-id="f7d2a-157">Ostot kaupungin mukaan</span><span class="sxs-lookup"><span data-stu-id="f7d2a-157">Purchase by city</span></span>
- <span data-ttu-id="f7d2a-158">Ostojen vuosittainen kasvuprosentti</span><span class="sxs-lookup"><span data-stu-id="f7d2a-158">Purchase YOY growth %</span></span>
- <span data-ttu-id="f7d2a-159">Ostot maan mukaan</span><span class="sxs-lookup"><span data-stu-id="f7d2a-159">Purchase by country</span></span>

<span data-ttu-id="f7d2a-160">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="f7d2a-160">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="f7d2a-161">Ostojen ja kulutuksen analyysi ajan mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="f7d2a-161">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="f7d2a-162">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="f7d2a-162">**Charts**</span></span> 
- <span data-ttu-id="f7d2a-163">Ostojen kuluva vuosi kuukauden/päivän mukaan (viivakaavio)</span><span class="sxs-lookup"><span data-stu-id="f7d2a-163">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="f7d2a-164">Ostojen kuluva ja edellinen vuosi (viiva- ja sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="f7d2a-164">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="f7d2a-165">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="f7d2a-165">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="f7d2a-166">Ostojen ja kulutuksen analyysi toimittajan mukaan -raporttisivu</span><span class="sxs-lookup"><span data-stu-id="f7d2a-166">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="f7d2a-167">**Kaaviot**</span><span class="sxs-lookup"><span data-stu-id="f7d2a-167">**Charts**</span></span> 
- <span data-ttu-id="f7d2a-168">10 parasta toimittajaa ostojen prosenttiosuuden mukaan (suppilokaavio)</span><span class="sxs-lookup"><span data-stu-id="f7d2a-168">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="f7d2a-169">10 toimittajaa, joiden vuosittainen kulutus on noussut eniten</span><span class="sxs-lookup"><span data-stu-id="f7d2a-169">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="f7d2a-170">10 toimittajaa, joiden vuosittainen kulutus on laskenut eniten</span><span class="sxs-lookup"><span data-stu-id="f7d2a-170">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="f7d2a-171">**Esimerkki** 
</span><span class="sxs-lookup"><span data-stu-id="f7d2a-171">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="f7d2a-172">Tietomalli ja yksiköt</span><span class="sxs-lookup"><span data-stu-id="f7d2a-172">Data model and entities</span></span>
<span data-ttu-id="f7d2a-173">Seuraavia tietoja käytetään **osto- ja kulutusanalyysin** Power BI -sisällön raporttisivujen täyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-173">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="f7d2a-174">Nämä tiedot esitetään koottuina mittauksina, joka vaiheistetaan yksikkösäilössä.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-174">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="f7d2a-175">Yksikkösäilö on analytiikkaa varten optimoitu Microsoft SQL Server -tietokanta.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-175">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="f7d2a-176">Lisätietoja on kohdassa [Power BI:n ja yksikkösäilön integraatio](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="f7d2a-176">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="f7d2a-177">Sisällön koostetut mittaukset ovat alijoukko Microsoft Dynamics AX 2012:n ja Microsoft Dynamics AX 2012 R3:n ostokuutiossa saatavilla olleista koostetuista mittauksista.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-177">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="f7d2a-178">Jotta kuution koostetut mittaukset voi tallentaa yksikkösäilöön, niistä on tehtävä käyttöönottokelpoisia.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-178">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="f7d2a-179">Lisätietoja koostettujen mittojen tallentamisesta yksikkösäilöön on kohdassa [Power BI:n ja yksikkösäilön integrointi](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="f7d2a-179">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="f7d2a-180">Seuraavat tärkeät koostemitat ovat käytettävissä suoraan laskun rivien yksiköstä. Niitä käytetään sisällön perustana.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-180">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="f7d2a-181">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="f7d2a-181">Entity</span></span>        | <span data-ttu-id="f7d2a-182">Tärkeät koostemitat</span><span class="sxs-lookup"><span data-stu-id="f7d2a-182">Key aggregate measurements</span></span> | <span data-ttu-id="f7d2a-183">Tietolähde</span><span class="sxs-lookup"><span data-stu-id="f7d2a-183">Data source</span></span>                                 | <span data-ttu-id="f7d2a-184">Kenttä</span><span class="sxs-lookup"><span data-stu-id="f7d2a-184">Field</span></span>              | <span data-ttu-id="f7d2a-185">kuvaus</span><span class="sxs-lookup"><span data-stu-id="f7d2a-185">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="f7d2a-186">Laskurivit</span><span class="sxs-lookup"><span data-stu-id="f7d2a-186">Invoice lines</span></span> | <span data-ttu-id="f7d2a-187">Osto</span><span class="sxs-lookup"><span data-stu-id="f7d2a-187">Purchase</span></span>                   | <span data-ttu-id="f7d2a-188">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="f7d2a-188">VendInvoiceTrans</span></span>                            | <span data-ttu-id="f7d2a-189">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="f7d2a-189">SUM(LineAmountMST)</span></span> | <span data-ttu-id="f7d2a-190">Summa kirjanpitovaluuttana.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-190">The amount in the accounting currency.</span></span> |

<span data-ttu-id="f7d2a-191">Seuraavassa taulukossa esitellään tärkeät mitat, jotka lasketaan sisällössä ja jotka saadaan laskun rivien yksiköstä.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-191">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="f7d2a-192">Mitta</span><span class="sxs-lookup"><span data-stu-id="f7d2a-192">Measure</span></span>               | <span data-ttu-id="f7d2a-193">Laskelma</span><span class="sxs-lookup"><span data-stu-id="f7d2a-193">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7d2a-194">Kuluvan vuoden ostot</span><span class="sxs-lookup"><span data-stu-id="f7d2a-194">Purchase current year</span></span> | <span data-ttu-id="f7d2a-195">Kuluvan vuoden ostot = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="f7d2a-195">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="f7d2a-196">Edellisen vuoden ostot</span><span class="sxs-lookup"><span data-stu-id="f7d2a-196">Purchase last year</span></span>    | <span data-ttu-id="f7d2a-197">Edellisen vuoden ostot = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="f7d2a-197">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="f7d2a-198">Ostojen vuosittainen kasvu</span><span class="sxs-lookup"><span data-stu-id="f7d2a-198">YOY purchase growth</span></span>   | <span data-ttu-id="f7d2a-199">Ostojen vuosittainen kasvu = \[Kuluvan vuoden ostot\] – \[Edellisen vuoden ostot\]</span><span class="sxs-lookup"><span data-stu-id="f7d2a-199">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="f7d2a-200">Seuraavia sisällön tärkeitä dimensioita käytetään koostemittojen ositussuodattimina. Tämä parantaa rakeisuutta ja sen avulla saadaan entistä tarkempaa analyysitietoa.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-200">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="f7d2a-201">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="f7d2a-201">Entity</span></span>                 | <span data-ttu-id="f7d2a-202">Esimerkkejä määritteistä</span><span class="sxs-lookup"><span data-stu-id="f7d2a-202">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="f7d2a-203">Toimittajat</span><span class="sxs-lookup"><span data-stu-id="f7d2a-203">Vendors</span></span>                | <span data-ttu-id="f7d2a-204">Toimittajaryhmät, toimittajan maa tai alueet, toimittajan nimi</span><span class="sxs-lookup"><span data-stu-id="f7d2a-204">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="f7d2a-205">Tuotteet</span><span class="sxs-lookup"><span data-stu-id="f7d2a-205">Products</span></span>               | <span data-ttu-id="f7d2a-206">Tuotenumero, tuotteen nimi, nimikeryhmien nimi</span><span class="sxs-lookup"><span data-stu-id="f7d2a-206">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="f7d2a-207">Hankintaluokat</span><span class="sxs-lookup"><span data-stu-id="f7d2a-207">Procurement categories</span></span> | <span data-ttu-id="f7d2a-208">Hankintaluokka, hankintaluokkien nimet</span><span class="sxs-lookup"><span data-stu-id="f7d2a-208">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="f7d2a-209">Oikeushenkilöt</span><span class="sxs-lookup"><span data-stu-id="f7d2a-209">Legal entities</span></span>         | <span data-ttu-id="f7d2a-210">Yrityksen nimi</span><span class="sxs-lookup"><span data-stu-id="f7d2a-210">Legal entity name</span></span>                                     |
| <span data-ttu-id="f7d2a-211">Päivämäärät</span><span class="sxs-lookup"><span data-stu-id="f7d2a-211">Dates</span></span>                  | <span data-ttu-id="f7d2a-212">Päivämäärät, vuosisiirtymä</span><span class="sxs-lookup"><span data-stu-id="f7d2a-212">Dates, Year offset</span></span>                                    |

<span data-ttu-id="f7d2a-213">Kuluvan kalenterivuoden tiedot näkyvät oletusarvoisesti sisällössä.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-213">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="f7d2a-214">Voit kuitenkin muuttaa päivämääräsuodatinta raportin suodatinosassa.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-214">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="f7d2a-215">Voit muuttaa myös yrityssuodatinta.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-215">You can also change the company filter.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]