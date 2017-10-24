---
title: "Ostojen ja kulutuksen analyysi - Power BI -sisältö"
description: "Tässä ohjeaiheessa kerrotaan, mitä osto- ja kulutusanalyysin Power BI -sisältö sisältää. Siinä selitetään, miten sisältöön sisältyvät raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä."
author: FrankDahl
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3e42746329b1194c0ce0e2fb5c476742259a5b43
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="11e10-104">Ostojen ja kulutuksen analyysi - Power BI -sisältö</span><span class="sxs-lookup"><span data-stu-id="11e10-104">Purchase spend analysis Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="11e10-105">Tässä ohjeaiheessa kerrotaan, mitä **osto- ja kulutusanalyysin** Microsoft Power BI -sisältö sisältää.</span><span class="sxs-lookup"><span data-stu-id="11e10-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="11e10-106">Siinä kuvataan, miten avaat Power BI -raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä.</span><span class="sxs-lookup"><span data-stu-id="11e10-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="11e10-107">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="11e10-107">Overview</span></span>

<span data-ttu-id="11e10-108">**Osto- ja kustannusanalyysin** Power BI -sisältö on suunniteltu ostopäälliköiden ja budjetista vastaavien esimiesten käyttöön, sillä auttaa seuraamaan ostoja ja kulutusta.</span><span class="sxs-lookup"><span data-stu-id="11e10-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="11e10-109">Esimiehet voivat analysoida ostoja ja kulutusta seuraavin tavoin:</span><span class="sxs-lookup"><span data-stu-id="11e10-109">Managers can analyze purchase spending in the following ways:</span></span>

-   <span data-ttu-id="11e10-110">Ostot vuoden alusta (toimittajaryhmän ja yksittäisten toimittajien, hankintaluokan ja yksittäisten tuotteiden ja toimittajan sijainnin mukaan)</span><span class="sxs-lookup"><span data-stu-id="11e10-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
-   <span data-ttu-id="11e10-111">Ostojen vuosittainen muutos (toimittajaryhmän ja hankintaluokan mukaan)</span><span class="sxs-lookup"><span data-stu-id="11e10-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="11e10-112">Sisältö käyttää ostotapahtumiin liittyviä tietoja ja antaa koko yrityksen ostolukujen koostenäkymän sekä toimittaja- ja tuotekohtaisen erittelyn ostoista ja kulutuksesta.</span><span class="sxs-lookup"><span data-stu-id="11e10-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="11e10-113">Raportit korostavat ostojen ja kulutuksen muutoksia ajanjakson aikana.</span><span class="sxs-lookup"><span data-stu-id="11e10-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="11e10-114">Tämän vuoksi raportteja voidaan käyttää, kun esimiehille ilmoitetaan yksittäisten toimittajien ja tuotteiden positiivisista ja negatiivisista kulutussuuntauksista.</span><span class="sxs-lookup"><span data-stu-id="11e10-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="11e10-115">Lisäksi kaaviot osoittavat eri hankintaluokkien ja toimittajaryhmien ostot ja kulutuksen.</span><span class="sxs-lookup"><span data-stu-id="11e10-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="11e10-116">Näin ollen luokka- ja aluepäälliköitä voivat käyttää kaavioita apuna kulutuskäyttäytymisessä tapahtuvien muutoksien havaitsemisessa.</span><span class="sxs-lookup"><span data-stu-id="11e10-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="11e10-117">Power BI -sisällön käyttö</span><span class="sxs-lookup"><span data-stu-id="11e10-117">Accessing the Power BI content</span></span>
<span data-ttu-id="11e10-118">Jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys, **osto- ja kulutusanalyysin** Power BI -sisältö näkyy **Osto- ja kulutusanalyysi** -sivulla (**Hankinta** > **Kyselyt ja raportit** > **Ostojen suorituskykyanalyysi** > **Osto- ja kulutusanalyysi**).</span><span class="sxs-lookup"><span data-stu-id="11e10-118">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), the **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** > **Inquiries and reports** > **Purchase performance analysis** > **Purchase and spend analysis**).</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="11e10-119">Mittareita, jotka sisältyvät Power BI -sisältöön</span><span class="sxs-lookup"><span data-stu-id="11e10-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="11e10-120">**Ostojen ja kulutuksen analyysin** Power BI -sisältöön lukeutuu raportti, joka koostuu mittarijoukosta.</span><span class="sxs-lookup"><span data-stu-id="11e10-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="11e10-121">Nämä mittarit visualisoidaan kaavioina, ruutuina ja taulukoina.</span><span class="sxs-lookup"><span data-stu-id="11e10-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="11e10-122">Seuraavassa taulukossa on visualisointien yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="11e10-122">The following table provides an overview of the visualizations.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11e10-123">Raporttisivu</span><span class="sxs-lookup"><span data-stu-id="11e10-123">Report page</span></span></th>
<th><span data-ttu-id="11e10-124">Kaaviot</span><span class="sxs-lookup"><span data-stu-id="11e10-124">Charts</span></span></th>
<th><span data-ttu-id="11e10-125">Ruudut</span><span class="sxs-lookup"><span data-stu-id="11e10-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="11e10-126">Ostot toimittajan mukaan</span><span class="sxs-lookup"><span data-stu-id="11e10-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="11e10-127">10 parasta toimittajaa ostojen mukaan (pinottu palkkikaavio)</span><span class="sxs-lookup"><span data-stu-id="11e10-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="11e10-128">Ostot yhteensä toimittajaryhmän/maan/nimen mukaan (ympyräkaavio)</span><span class="sxs-lookup"><span data-stu-id="11e10-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="11e10-129">Ostot toimittajaryhmän/maan/nimen mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="11e10-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="11e10-130">Ostot keskimäärin toimittajaryhmän/maan/nimen mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="11e10-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="11e10-131">Osto yhteensä</span><span class="sxs-lookup"><span data-stu-id="11e10-131">Total purchase</span></span></li>
<li><span data-ttu-id="11e10-132">Ostojen vuosittainen kasvu</span><span class="sxs-lookup"><span data-stu-id="11e10-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="11e10-133">Toimittajien kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="11e10-133">Total # vendors</span></span></li>
<li><span data-ttu-id="11e10-134">Aktiivisten toimittajien kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="11e10-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11e10-135">Ostot tuotteen mukaan</span><span class="sxs-lookup"><span data-stu-id="11e10-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="11e10-136">Ostot hankintaluokan / tuotteen nimen mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="11e10-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="11e10-137">Ostot yhteensä hankintaluokan / tuotteen nimen mukaan (ympyräkaavio)</span><span class="sxs-lookup"><span data-stu-id="11e10-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="11e10-138">10 parasta tuotetta ostojen mukaan (pinottu palkkikaavio)</span><span class="sxs-lookup"><span data-stu-id="11e10-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="11e10-139">Tuotteiden kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="11e10-139">Total # of products</span></span></li>
<li><span data-ttu-id="11e10-140">Kaikkien aktiivisten tuotteiden prosenttiosuus tuotteiden kokonaismäärästä</span><span class="sxs-lookup"><span data-stu-id="11e10-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="11e10-141">Tuotteiden määrä, joista koostuu 80 % ostoista</span><span class="sxs-lookup"><span data-stu-id="11e10-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11e10-142">Ostot kauden mukaan*</span><span class="sxs-lookup"><span data-stu-id="11e10-142">Purchase by period*</span></span></td>
<td><ul>
<li><span data-ttu-id="11e10-143">Ostot kuukauden/päivän mukaan (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="11e10-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="11e10-144">Kumulatiivisten ostojen vuosittainen varianssi (vesiputouskaavio)</span><span class="sxs-lookup"><span data-stu-id="11e10-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="11e10-145">Ostot yhteensä, vuosittainen kasvu (sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="11e10-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="11e10-146">Hankintaraportti (matriisi)</span><span class="sxs-lookup"><span data-stu-id="11e10-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="11e10-147">Ostojen vuosittainen kasvu</span><span class="sxs-lookup"><span data-stu-id="11e10-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="11e10-148">Ostojen vuosittainen kasvuprosentti</span><span class="sxs-lookup"><span data-stu-id="11e10-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11e10-149">Ostot toimittajan sijainnin mukaan</span><span class="sxs-lookup"><span data-stu-id="11e10-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="11e10-150">Ostot kaupungin mukaan</span><span class="sxs-lookup"><span data-stu-id="11e10-150">Purchase by city</span></span></li>
<li><span data-ttu-id="11e10-151">Ostojen vuosittainen kasvuprosentti</span><span class="sxs-lookup"><span data-stu-id="11e10-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="11e10-152">Ostot maan mukaan</span><span class="sxs-lookup"><span data-stu-id="11e10-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11e10-153">Ostojen ja kulutuksen analyysi ajan mukaan</span><span class="sxs-lookup"><span data-stu-id="11e10-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="11e10-154">Ostojen kuluva vuosi kuukauden/päivän mukaan (viivakaavio)</span><span class="sxs-lookup"><span data-stu-id="11e10-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="11e10-155">Ostojen kuluva ja edellinen vuosi (viiva- ja sarakekaavio)</span><span class="sxs-lookup"><span data-stu-id="11e10-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11e10-156">Ostojen ja kulutuksen analyysi toimittajan mukaan</span><span class="sxs-lookup"><span data-stu-id="11e10-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="11e10-157">10 parasta toimittajaa ostojen prosenttiosuuden mukaan (suppilokaavio)</span><span class="sxs-lookup"><span data-stu-id="11e10-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="11e10-158">10 toimittajaa, joiden vuosittainen kulutus on noussut eniten</span><span class="sxs-lookup"><span data-stu-id="11e10-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="11e10-159">10 toimittajaa, joiden vuosittainen kulutus on laskenut eniten</span><span class="sxs-lookup"><span data-stu-id="11e10-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="11e10-160">\* Ostot tänä ja edellisenä vuonna sekä kasvu hankintaluokan mukaan</span><span class="sxs-lookup"><span data-stu-id="11e10-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="11e10-161">Power BI -sisällön laajentaminen</span><span class="sxs-lookup"><span data-stu-id="11e10-161">Extending the Power BI content</span></span>
<span data-ttu-id="11e10-162">Jos käytät Microsoft Dynamics Lifecycle Servicesin (LCS) sisältöpaketteja, voit tehdä erinomaisia analyyseja henkilöille, jotka eivät käytä Microsoft Dynamics 365:tä.</span><span class="sxs-lookup"><span data-stu-id="11e10-162">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="11e10-163">Voit muokata näitä sisältöpaketit sisältämään muita raportteja ja visuaalisia tietoja ja julkaista sitten sisältöpaketit analysoitavaksi Power BI.com -vuokraajassa.</span><span class="sxs-lookup"><span data-stu-id="11e10-163">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="11e10-164">**Osto- ja kulutusanalyysin** Power BI -sisältö sijaitsee LCS:n Jaettu omaisuus -kirjastossa.</span><span class="sxs-lookup"><span data-stu-id="11e10-164">You can find the **Purchase spend analysis** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="11e10-165">Lisätietoja sisällön lataamisesta ja sen käyttöönottamisesta organisaatiossa on ohjeaiheessa [Microsoftin ja kumppaneiden Power BI -sisältö LCS-sovelluksessa](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="11e10-165">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="11e10-166">Katso Power BI -sisällön käyttöönotosta kertova esittely Office Mixin kohdassa [Microsoftin ja kumppaneiden Power BI -sisältö Dynamics Lifecycle Services -sovelluksessa](https://mix.office.com/watch/9puyb1b2xs1w).</span><span class="sxs-lookup"><span data-stu-id="11e10-166">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

<span data-ttu-id="11e10-167">Muista ladata käyttämääsi Dynamics 365 -versiota vastaava **osto- ja kulutusanalyysin** sisältö.</span><span class="sxs-lookup"><span data-stu-id="11e10-167">Be sure to download the **Purchase spend analysis** content that applies to the version of Dynamics 365 that you're using.</span></span>

> [!NOTE]
> <span data-ttu-id="11e10-168">Jos käytössä on Microsoft Dynamics 365 for Operations versio 1611, Power BI -sisällön edellytyksenä on KB 4011327.</span><span class="sxs-lookup"><span data-stu-id="11e10-168">If you're using Microsoft Dynamics 365 for Operations version 1611, KB 4011327 is a prerequisite for this Power BI content.</span></span> <span data-ttu-id="11e10-169">Kun olet kirjautunut LCS:ään, voit siirtyä tietämyskantaan osoitteessa https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span><span class="sxs-lookup"><span data-stu-id="11e10-169">After you sign in to LCS, you can access the KB at https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="11e10-170">Tietomalli ja yksiköt</span><span class="sxs-lookup"><span data-stu-id="11e10-170">Data model and entities</span></span>
<span data-ttu-id="11e10-171">Seuraavia tietoja käytetään **osto- ja kulutusanalyysin** Power BI -sisällön raporttisivujen täyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="11e10-171">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="11e10-172">Nämä tiedot esitetään koottuina mittauksina, joka vaiheistetaan yksikkösäilössä.</span><span class="sxs-lookup"><span data-stu-id="11e10-172">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="11e10-173">Yksikkösäilö on analytiikkaa varten optimoitu Microsoft SQL Server -tietokanta.</span><span class="sxs-lookup"><span data-stu-id="11e10-173">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="11e10-174">Lisätietoja on ohjeaiheessa [yleiskatsaus Power BI:n integraatiosta yksikkökaupan kanssa](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="11e10-174">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="11e10-175">Sisällön koostetut mittaukset ovat alijoukko Microsoft Dynamics AX 2012:n ja AX 2012 R3:n ostokuutiossa saatavilla olleista koostemitoista.</span><span class="sxs-lookup"><span data-stu-id="11e10-175">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="11e10-176">Jotta kuution koostetut mittaukset voi tallentaa yksikkösäilöön, niistä on tehtävä käyttöönottokelpoisia.</span><span class="sxs-lookup"><span data-stu-id="11e10-176">To stage the cube’s aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="11e10-177">Lisätietoja koostettujen mittojen tallentamisesta yksikkösäilöön on ohjeaiheessa [Power BI:n ja yksikkösäilön integroinnin yleiskatsaus](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="11e10-177">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="11e10-178">Seuraavat tärkeät koostemitat ovat käytettävissä suoraan laskun rivien yksiköstä. Niitä käytetään sisällön perustana.</span><span class="sxs-lookup"><span data-stu-id="11e10-178">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="11e10-179">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="11e10-179">Entity</span></span>        | <span data-ttu-id="11e10-180">Tärkeät koostemitat</span><span class="sxs-lookup"><span data-stu-id="11e10-180">Key aggregate measurements</span></span> | <span data-ttu-id="11e10-181">Tietolähde</span><span class="sxs-lookup"><span data-stu-id="11e10-181">Data source</span></span>                                 | <span data-ttu-id="11e10-182">Kenttä</span><span class="sxs-lookup"><span data-stu-id="11e10-182">Field</span></span>              | <span data-ttu-id="11e10-183">kuvaus</span><span class="sxs-lookup"><span data-stu-id="11e10-183">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="11e10-184">Laskurivit</span><span class="sxs-lookup"><span data-stu-id="11e10-184">Invoice lines</span></span> | <span data-ttu-id="11e10-185">Osto</span><span class="sxs-lookup"><span data-stu-id="11e10-185">Purchase</span></span>                   | <span data-ttu-id="11e10-186">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="11e10-186">VendInvoiceTrans</span></span>                            | <span data-ttu-id="11e10-187">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="11e10-187">SUM(LineAmountMST)</span></span> | <span data-ttu-id="11e10-188">Summa kirjanpitovaluuttana.</span><span class="sxs-lookup"><span data-stu-id="11e10-188">The amount in the accounting currency.</span></span> |

<span data-ttu-id="11e10-189">Seuraavassa taulukossa esitellään tärkeät mitat, jotka lasketaan sisällössä ja jotka saadaan laskun rivien yksiköstä.</span><span class="sxs-lookup"><span data-stu-id="11e10-189">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="11e10-190">Mitta</span><span class="sxs-lookup"><span data-stu-id="11e10-190">Measure</span></span>               | <span data-ttu-id="11e10-191">Laskelma</span><span class="sxs-lookup"><span data-stu-id="11e10-191">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11e10-192">Kuluvan vuoden ostot</span><span class="sxs-lookup"><span data-stu-id="11e10-192">Purchase current year</span></span> | <span data-ttu-id="11e10-193">Kuluvan vuoden ostot = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="11e10-193">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="11e10-194">Edellisen vuoden ostot</span><span class="sxs-lookup"><span data-stu-id="11e10-194">Purchase last year</span></span>    | <span data-ttu-id="11e10-195">Edellisen vuoden ostot = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="11e10-195">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="11e10-196">Ostojen vuosittainen kasvu</span><span class="sxs-lookup"><span data-stu-id="11e10-196">YOY purchase growth</span></span>   | <span data-ttu-id="11e10-197">Ostojen vuosittainen kasvu = \[Kuluvan vuoden ostot\] – \[Edellisen vuoden ostot\]</span><span class="sxs-lookup"><span data-stu-id="11e10-197">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="11e10-198">Seuraavia sisällön tärkeitä dimensioita käytetään koostemittojen ositussuodattimina. Tämä parantaa rakeisuutta ja sen avulla saadaan entistä tarkempaa analyysitietoa.</span><span class="sxs-lookup"><span data-stu-id="11e10-198">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="11e10-199">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="11e10-199">Entity</span></span>                 | <span data-ttu-id="11e10-200">Esimerkkejä määritteistä</span><span class="sxs-lookup"><span data-stu-id="11e10-200">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="11e10-201">Toimittajat</span><span class="sxs-lookup"><span data-stu-id="11e10-201">Vendors</span></span>                | <span data-ttu-id="11e10-202">Toimittajaryhmät, toimittajan maa tai alueet, toimittajan nimi</span><span class="sxs-lookup"><span data-stu-id="11e10-202">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="11e10-203">Tuotteet</span><span class="sxs-lookup"><span data-stu-id="11e10-203">Products</span></span>               | <span data-ttu-id="11e10-204">Tuotenumero, tuotteen nimi, nimikeryhmien nimi</span><span class="sxs-lookup"><span data-stu-id="11e10-204">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="11e10-205">Hankintaluokat</span><span class="sxs-lookup"><span data-stu-id="11e10-205">Procurement categories</span></span> | <span data-ttu-id="11e10-206">Hankintaluokka, hankintaluokkien nimet</span><span class="sxs-lookup"><span data-stu-id="11e10-206">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="11e10-207">Oikeushenkilöt</span><span class="sxs-lookup"><span data-stu-id="11e10-207">Legal entities</span></span>         | <span data-ttu-id="11e10-208">Yrityksen nimi</span><span class="sxs-lookup"><span data-stu-id="11e10-208">Legal entity name</span></span>                                     |
| <span data-ttu-id="11e10-209">Päivämäärät</span><span class="sxs-lookup"><span data-stu-id="11e10-209">Dates</span></span>                  | <span data-ttu-id="11e10-210">Päivämäärät, vuosisiirtymä</span><span class="sxs-lookup"><span data-stu-id="11e10-210">Dates, Year offset</span></span>                                    |

<span data-ttu-id="11e10-211">Kuluvan kalenterivuoden tiedot näkyvät oletusarvoisesti sisällössä.</span><span class="sxs-lookup"><span data-stu-id="11e10-211">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="11e10-212">Voit kuitenkin muuttaa päivämääräsuodatinta raportin suodatinosassa.</span><span class="sxs-lookup"><span data-stu-id="11e10-212">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="11e10-213">Voit muuttaa myös yrityssuodatinta.</span><span class="sxs-lookup"><span data-stu-id="11e10-213">You can also change the company filter.</span></span>

