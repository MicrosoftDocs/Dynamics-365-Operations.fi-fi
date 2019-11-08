---
title: Analyysiraporttien käyttäminen Microsoft Dynamics 365 Talent – Attractissa
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent – Attractin työhönottoprosessin merkityksellisten tietojen analyysiraportteja
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: 5a4d160e8c90725d5ea129a76fd48da1c5af7900
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551515"
---
# <a name="use-analytic-reports-in-microsoft-dynamics-365-talent---attract"></a><span data-ttu-id="6a4eb-103">Analyysiraporttien käyttäminen Microsoft Dynamics 365 Talent – Attractissa</span><span class="sxs-lookup"><span data-stu-id="6a4eb-103">Use analytic reports in Microsoft Dynamics 365 Talent - Attract</span></span>

<span data-ttu-id="6a4eb-104">Microsoft Dynamics 365 Talent: Attractin analyyttiset raportit tarjoavat OOTB-ratkaisun työhönottoprosessin merkityksellisille tiedoille.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-104">Analytic reports in Microsoft Dynamics 365 Talent: Attract provide an out-of-the-box (OOTB) solution for hiring process insights.</span></span> <span data-ttu-id="6a4eb-105">Käytettävissä olevia ominaisuuksia ovat:</span><span class="sxs-lookup"><span data-stu-id="6a4eb-105">Availabe features include:</span></span>

- <span data-ttu-id="6a4eb-106">**Työn analytiikka** Napsauta työpaikan hakijoiden mittarit **Analytiikka**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-106">**Job analytics:** Click the **Analytics** tab within a job for metrics on the job's applicants.</span></span>
- <span data-ttu-id="6a4eb-107">**Analyysikeskus:** Valitse **Analyysit** vasemmanpuoleisesta siirtymispalkista, kun haluat yhdistää eri töiden metriikat.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-107">**Analytics hub:** Click **Analytics** on the left navigation for aggregated metrics across jobs.</span></span>
- <span data-ttu-id="6a4eb-108">**Käyttäjäkohtaiset käyttöoikeudet:** Attractin [roolin](security-attract.md) hallitsemien raporttien käyttäminen ja työn osallistujarooli.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-108">**User-specific security:** Access to reports is controlled by Attract [role](security-attract.md) and job participant role.</span></span>
- <span data-ttu-id="6a4eb-109">**Ristiinsuodatus:** Valitse raportissa visualisointi, jos haluat tarkastella muita valittujen tietojen mukaan suodatettuja mittareita.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-109">**Cross-filtering:** Click visuals within a report to view other metrics filtered by selected data.</span></span>

>[!NOTE] 
>- <span data-ttu-id="6a4eb-110">Tämä ominaisuus on tällä hetkellä vain [esiversiossa](access-preview-feature.md).</span><span class="sxs-lookup"><span data-stu-id="6a4eb-110">This feature is currently in [preview](access-preview-feature.md).</span></span> <span data-ttu-id="6a4eb-111">Jos haluat kokeilla sitä, sinulla on oltava [**kattava työhönottolisäosa**](attract-comprehensive-hiring.md).</span><span class="sxs-lookup"><span data-stu-id="6a4eb-111">To try it, you must have the [**Comprehensive Hiring Add-On**](attract-comprehensive-hiring.md).</span></span>
>- <span data-ttu-id="6a4eb-112">Kaikki julkiset esikatseluraportit näkyvät englanniksi.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-112">All public preview reports are displayed in English.</span></span>
>- <span data-ttu-id="6a4eb-113">Raportit päivitetään joka kolmas tunti.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-113">Reports refresh every 3 hours.</span></span> <span data-ttu-id="6a4eb-114">Viimeisin päivitysaika (paikallisessa aikavyöhykkeessä) sijaitsee raportin yläosassa.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-114">The last refresh time (in the local timezone) is located at the top of the report.</span></span> <span data-ttu-id="6a4eb-115">Päivitysajat ovat likiarvo ja vaihtelevat alueen tietojen määrän ja resurssien kuormituksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-115">Refresh times are an approximation and vary based on data volume and resource load in your region.</span></span>

## <a name="job-analytics"></a><span data-ttu-id="6a4eb-116">Työn analytiikka</span><span class="sxs-lookup"><span data-stu-id="6a4eb-116">Job Analytics</span></span>

<span data-ttu-id="6a4eb-117">Työn analytiikka -raportit ovat tilannekuva työn työhönottoprosessista.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-117">Job Analytics reports are a snapshot of the hiring process for a job.</span></span>  <span data-ttu-id="6a4eb-118">Tärkeimpiä mittareita ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="6a4eb-118">Key metrics include:</span></span>

- <span data-ttu-id="6a4eb-119">Aktiiviset hakijat vaiheen mukaan</span><span class="sxs-lookup"><span data-stu-id="6a4eb-119">Active applicants by stage</span></span>
- <span data-ttu-id="6a4eb-120">Hakijalähde</span><span class="sxs-lookup"><span data-stu-id="6a4eb-120">Applicant source</span></span>
- <span data-ttu-id="6a4eb-121">Hakijan tyyppi (sisäinen tai ulkoinen)</span><span class="sxs-lookup"><span data-stu-id="6a4eb-121">Applicant type (internal or external)</span></span>

## <a name="analytics-hub"></a><span data-ttu-id="6a4eb-122">Analytiikkakeskus</span><span class="sxs-lookup"><span data-stu-id="6a4eb-122">Analytics Hub</span></span>

<span data-ttu-id="6a4eb-123">Analytiikkakeskus raportoi eri töistä kerätyt tiedot, mikä auttaa löytämään työhönottoprosessin trendejä.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-123">Analytics Hub reports aggregate data across jobs to surface trends in the hiring process.</span></span> <span data-ttu-id="6a4eb-124">Attract sisältää kaksi OOTB-raporttia: putken yhteenveto ja kanava-analyysi.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-124">Attract includes two OOTB reports: Pipeline Summary and Funnel Analysis.</span></span>

### <a name="pipeline-summary"></a><span data-ttu-id="6a4eb-125">Putken yhteenveto</span><span class="sxs-lookup"><span data-stu-id="6a4eb-125">Pipeline Summary</span></span>

<span data-ttu-id="6a4eb-126">Putken yhteenvetoraportti kokoaa avoimien töiden tiedot.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-126">The Pipeline Summary report aggregates data for open jobs.</span></span> <span data-ttu-id="6a4eb-127">Tärkeimpiä mittareita ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="6a4eb-127">Key metrics include:</span></span>

- <span data-ttu-id="6a4eb-128">Kaikkien työpaikkojen hakijat vaiheen mukaan</span><span class="sxs-lookup"><span data-stu-id="6a4eb-128">Applicants across all jobs by stage</span></span>
- <span data-ttu-id="6a4eb-129">Hakijalähde</span><span class="sxs-lookup"><span data-stu-id="6a4eb-129">Applicant source</span></span>
- <span data-ttu-id="6a4eb-130">Avoimet työpaikat virkaikätason mukaan</span><span class="sxs-lookup"><span data-stu-id="6a4eb-130">Open jobs by seniority level</span></span>

### <a name="funnel-analysis"></a><span data-ttu-id="6a4eb-131">Kanava-analyysi</span><span class="sxs-lookup"><span data-stu-id="6a4eb-131">Funnel Analysis</span></span>

<span data-ttu-id="6a4eb-132">Kanava-analyysiraportti kokoaa tiedot täytettyjen töiden osalta.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-132">The Funnel Analysis report aggregates data for jobs that have been closed as filled.</span></span> <span data-ttu-id="6a4eb-133">Tärkeimpiä mittareita ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="6a4eb-133">Key metrics include:</span></span>

- <span data-ttu-id="6a4eb-134">Palkkausaika</span><span class="sxs-lookup"><span data-stu-id="6a4eb-134">Time to hire</span></span>
- <span data-ttu-id="6a4eb-135">Muuntomittarit (valittaessa osoittamalla)</span><span class="sxs-lookup"><span data-stu-id="6a4eb-135">Conversion metrics (on hover)</span></span>
- <span data-ttu-id="6a4eb-136">Tarjouksen hyväksymisprosentti</span><span class="sxs-lookup"><span data-stu-id="6a4eb-136">Offer acceptance rate</span></span>

<span data-ttu-id="6a4eb-137">Huomautus: kun haluat käyttää raportoinnissa mahdollisimman tarkkaa aikaa, suosittelemme, että käytät [tarjouksen hallinta](offer-setup.md) -toimintoa, joka on käytettävissä osana kattavaa työhönottolisäosaa.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-137">Note: For the most accurate time to hire reporting, it is recommended that you use [Offer management](offer-setup.md), a feature available as part of the Comprehensive Hiring Add-On.</span></span>

>[!TIP] 
><span data-ttu-id="6a4eb-138">Saat lisätietoja viemällä osoittimen grafiikkakohdan päälle.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-138">Try hovering over visuals for additional information.</span></span> <span data-ttu-id="6a4eb-139">Jos esimerkiksi viet osoittimen **aktiivisten hakijoiden** päälle, näytössä näkyy keskimääräiset päivät vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-139">For example, hovering over **Active applicants** visuals will display the average days in stage.</span></span> <span data-ttu-id="6a4eb-140">Näiden tietojen analysointi voi antaa tärkeitä tietoja, joiden avulla työhönottoaikaa voidaan vähentää ja jotta rekrytoijat voivat keskittyä eri vaiheissa käytetyn ajan lyhentämiseen.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-140">Analyzing this information can provide insights critical to reducing time to hire and enable recruiters to focus on ways to reduce the time spent in each stage.</span></span>

## <a name="user-specific-security"></a><span data-ttu-id="6a4eb-141">Käyttäjäkohtainen turvallisuus</span><span class="sxs-lookup"><span data-stu-id="6a4eb-141">User-specific security</span></span>

<span data-ttu-id="6a4eb-142">Attract-raportit ovat käytettävissä järjestelmänvalvoja-, lue kaikki-, rekrytoija-, ja vuokrauspäällikkö[rooleille](security-attract.md).</span><span class="sxs-lookup"><span data-stu-id="6a4eb-142">Attract reports are accessible for Admin, Read All, Recruiter, and Hiring Manager [roles](security-attract.md).</span></span> <span data-ttu-id="6a4eb-143">Jos käyttäjälle ei ole määritetty roolia, hän ei voi käyttää kumpaakaan analyysiraporttisivua (Työn analytiikka tai Analytiikkakeskus).</span><span class="sxs-lookup"><span data-stu-id="6a4eb-143">Unassigned users do not have access to either of the analytic report pages (Job Analytics or Analytics Hub).</span></span>

<span data-ttu-id="6a4eb-144">Työn analytiikka -raportti esittää tietoja valitusta työstä.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-144">Job Analytics reports display data for the selected job.</span></span> <span data-ttu-id="6a4eb-145">Analyysikeskus raportoi koostettuja tietoja kaikista töistä, joita käyttäjä voi tarkastella.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-145">Analytics Hub reports aggregate data across all jobs a user can view.</span></span> <span data-ttu-id="6a4eb-146">Käyttäjät, jotka voivat tarkastella työsivun sekä omat työt- että kaikki työt -sivua, käyttävät samoja näkymiä analyysikeskuksessa.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-146">Users that can view both My jobs and All jobs on the Jobs page have the same views available in the Analytics Hub.</span></span>

## <a name="cross-filter"></a><span data-ttu-id="6a4eb-147">Ristiinsuodatin</span><span class="sxs-lookup"><span data-stu-id="6a4eb-147">Cross-filter</span></span>

<span data-ttu-id="6a4eb-148">Yksi Power BI -järjestelmän suurista ominaisuuksista on se, miten kaikki raporttisivun visualisoinnit ovat yhteydessä toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-148">One of the great features of Power BI is the way all visuals on a report page are interconnected.</span></span> <span data-ttu-id="6a4eb-149">Jos valitset tietopisteen jostakin visuaalista, kaikki muut sivun visualisoinnit, jotka sisältävät kyseisen tiedon muutoksen, perustuvat kyseiseen valintaan.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-149">If you select a data point on one of the visuals, all the other visuals on the page that contain that data change, based on that selection.</span></span> <span data-ttu-id="6a4eb-150">Lue lisää ja katso esimerkki siitä [miten visualisoinnit ristiinsuodattavat toisensa Power BI -raportissa.](https://docs.microsoft.com/power-bi/consumer/end-user-interactions)</span><span class="sxs-lookup"><span data-stu-id="6a4eb-150">Find out more and see an example in [How visuals cross-filter each other in a Power BI report](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span></span>

## <a name="export-to-excel"></a><span data-ttu-id="6a4eb-151">Vie Exceliin</span><span class="sxs-lookup"><span data-stu-id="6a4eb-151">Export to Excel</span></span>

<span data-ttu-id="6a4eb-152">Jos haluat tarkastella raportin tietoja Excelissä, voit napsauttaa asetukset-valikkoa (kolme pistettä) visuaalisessa näkymässä ja valita **vie pohjana olevat tiedot**.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-152">To view report data in Excel, you can click the options menu (three dots) on a visual and select **Export underlying data**.</span></span> <span data-ttu-id="6a4eb-153">Viedyt tiedot viedään suodatettuina ja niiden käyttöoikeudet otetaan huomioon Attractissa.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-153">Exported data will export as filtered, respecting user permissions in Attract.</span></span> <span data-ttu-id="6a4eb-154">Lisätietoja on kohdassa [tietojen vieminen visualisoinnin](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data)avulla.</span><span class="sxs-lookup"><span data-stu-id="6a4eb-154">For more information, see [Export data from visualizations](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span></span>
