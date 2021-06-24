---
title: ER-konfiguraatioiden suorituskykyongelmien vianmääritys
description: Tässä ohjeaiheessa on tietoja sähköisen raportoinnin konfiguraatioiden suorituskykyyn liittyvistä ongelmista ja korjaamisesta.
author: NickSelin
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: d77c2aad904ba911ac19009d6a981ea4153aaa48
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216862"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a><span data-ttu-id="69321-103">ER-konfiguraatioiden suorituskykyongelmien vianmääritys</span><span class="sxs-lookup"><span data-stu-id="69321-103">Troubleshooting performance issues in ER configurations</span></span>

<span data-ttu-id="69321-104">Tässä ohjeaiheessa on tietoja [sähköisen raportoinnin](general-electronic-reporting.md) (ER) [konfiguraatioiden](general-electronic-reporting.md#Configuration) suorituskykyyn liittyvistä ongelmista ja niiden ratkaisemisesta.</span><span class="sxs-lookup"><span data-stu-id="69321-104">This topic explains how to find and solve performance issues in [Electronic reporting](general-electronic-reporting.md) (ER) [configurations](general-electronic-reporting.md#Configuration).</span></span>

<span data-ttu-id="69321-105">Suorituskyvyn tutkimus käsittää yleensä useita vaiheita.</span><span class="sxs-lookup"><span data-stu-id="69321-105">Typically, performance investigation consists of several steps.</span></span>

1. <span data-ttu-id="69321-106">[Kerää](#collecting-data) tiedot.</span><span class="sxs-lookup"><span data-stu-id="69321-106">[Collect](#collecting-data) data.</span></span>
2. <span data-ttu-id="69321-107">Analysoi kerätyt tiedot.</span><span class="sxs-lookup"><span data-stu-id="69321-107">Analyze the collected data.</span></span>
3. <span data-ttu-id="69321-108">Analyysin tulosten perusteella voit [tehdä muutoksia](#making-changes) ER-konfiguraatioiden avulla tai päättää kerätä lisää tietoja.</span><span class="sxs-lookup"><span data-stu-id="69321-108">Based on the results of the analysis, use ER configurations to [make changes](#making-changes), or decide to collect more data.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="69321-109">Vianmääritys</span><span class="sxs-lookup"><span data-stu-id="69321-109">Troubleshooting</span></span>

### <a name="analyze-execution-time"></a><span data-ttu-id="69321-110">Suoritusajan analysoiminen</span><span class="sxs-lookup"><span data-stu-id="69321-110">Analyze execution time</span></span>

<span data-ttu-id="69321-111">Suoritusaika voi riippua odottamattomista seikoista, kuten muista samassa ympäristössä suoritetuista tehtävistä ja välimuistista, joka käyttää tietoja ensimmäisen kutsumisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="69321-111">Execution time can depend on unpredictable factors, such as other tasks that are running in the same environment and caching that uses data when it's called for the first time.</span></span> <span data-ttu-id="69321-112">Siksi sinun on toistettava suoritus ja mittaus useita kertoja.</span><span class="sxs-lookup"><span data-stu-id="69321-112">Therefore, you should repeat the execution and measurement several times.</span></span>

<span data-ttu-id="69321-113">Joskus suorituskykyongelmat eivät johdu raportoinnissa käytettävästä ER-muodon konfiguraatiosta.</span><span class="sxs-lookup"><span data-stu-id="69321-113">Sometimes, performance issues aren't caused by an ER format configuration that is used for reporting.</span></span> <span data-ttu-id="69321-114">Sen sijaan ne johtuvat X++-koodista, jota käytetään tämän ER-muodon konfiguraation avaamiseen.</span><span class="sxs-lookup"><span data-stu-id="69321-114">Instead, they are caused by the X++ code that is used to open that ER format configuration.</span></span>

1. <span data-ttu-id="69321-115">Voit tarkastella raportin suoritusaikaa joko [toimintokeskuksessa](#infolog-time) tai [tapahtumalokissa](#event-log-time).</span><span class="sxs-lookup"><span data-stu-id="69321-115">In either the [Action center](#infolog-time) or the [event log](#event-log-time), look at the execution time of the report.</span></span>
2. <span data-ttu-id="69321-116">Vertaa raportin suoritusaikaa skenaarion kokonaissuoritukseen.</span><span class="sxs-lookup"><span data-stu-id="69321-116">Compare the execution time of the report with the total execution time in the scenario.</span></span>
3. <span data-ttu-id="69321-117">Jos raportin suoritusaika on paljon pienempi kuin kokonaissuorituksen aika, ota huomioon raportin käsittelemien tietojen määrä:</span><span class="sxs-lookup"><span data-stu-id="69321-117">If the execution time of the report is much less than the total execution time, consider the amount of data that the report processes:</span></span>

    - <span data-ttu-id="69321-118">Jos raportissa on pieni määrä tietoja, ongelma saattaa liittyä konfiguraation latausaikaan.</span><span class="sxs-lookup"><span data-stu-id="69321-118">If the report processes a small amount of data, the issue might involve the loading time of the configuration.</span></span>
    - <span data-ttu-id="69321-119">Jos raportti käsittelee paljon tietoja, ongelma saattaa liittyä X++-koodin esikäsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="69321-119">If the report processes a large amount of data, the issue might involve preprocessing X++.</span></span> <span data-ttu-id="69321-120">Analysoi tämä tapaus [jäljitysjäsentimen](#analyze-trace-parser-trace) avulla.</span><span class="sxs-lookup"><span data-stu-id="69321-120">Use [Trace parser](#analyze-trace-parser-trace) to analyze this case.</span></span>

    <span data-ttu-id="69321-121">Lisätietoja on seuraavissa osissa.</span><span class="sxs-lookup"><span data-stu-id="69321-121">For other cases, see the next sections.</span></span>

4. <span data-ttu-id="69321-122">Suorita useita testejä, joihin liittyy erilaisia tietomääriä. Näin voit määrittää, miten suoritusaika määräytyy datamäärän mukaan.</span><span class="sxs-lookup"><span data-stu-id="69321-122">Run multiple tests that involve different amounts of data to determine how the execution time depends on the amount of data.</span></span>

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a><span data-ttu-id="69321-123">Analysoi jäljityksen jäsentimen jäljitykset</span><span class="sxs-lookup"><span data-stu-id="69321-123">Analyze Trace parser traces</span></span>

<span data-ttu-id="69321-124">Valmistele pieni esimerkki tai kerää useita jäljityksiä raportin luonnin satunnaisten osien aikana.</span><span class="sxs-lookup"><span data-stu-id="69321-124">Prepare a small example, or collect several traces during random parts of the report generation.</span></span>

<span data-ttu-id="69321-125">Tee sitten [jäljityksen jäsentimessä](#trace-parser) normaali alhaalta ylöspäin -analyysi ja vastaa seuraaviin kysymyksiin:</span><span class="sxs-lookup"><span data-stu-id="69321-125">Then, in [Trace parser](#trace-parser), do a standard bottom-to-up analysis, and answer the following questions:</span></span>

- <span data-ttu-id="69321-126">Mitkä ovat ajan kulutuksen kannalta käytetyimmät metodit?</span><span class="sxs-lookup"><span data-stu-id="69321-126">What are the top methods in terms of time consumption?</span></span>
- <span data-ttu-id="69321-127">Kuinka suuren osan kokonaisajasta nämä metodit käyttävät?</span><span class="sxs-lookup"><span data-stu-id="69321-127">What part of the overall time do those methods use?</span></span>

<span data-ttu-id="69321-128">Vastaa samoihin kysymyksiin kyselyiden osalta.</span><span class="sxs-lookup"><span data-stu-id="69321-128">Answer the same questions for queries.</span></span>

<span data-ttu-id="69321-129">Jos näet, että menetelmien etuliitteenä on "ER", siirry seuraavaan osaan.</span><span class="sxs-lookup"><span data-stu-id="69321-129">If you see that methods are prefixed with "ER," move on to the next section.</span></span>

<span data-ttu-id="69321-130">Jos näet, että metodit tai kyselyt ovat peräisin sovelluspaketista, kannattaa käyttää yleisiä optimointeja (esimerkiksi indeksien luontia).</span><span class="sxs-lookup"><span data-stu-id="69321-130">If you see that methods or queries originated in the application suite, consider generic optimizations (for example, create indexes).</span></span>

<span data-ttu-id="69321-131">Analysoi kutsujen määrä.</span><span class="sxs-lookup"><span data-stu-id="69321-131">Analyze the number of calls.</span></span> <span data-ttu-id="69321-132">Jos määrä on odotettua suurempi, harkitse konfiguraation vastaavien solmujen välimuistiin tallentamista.</span><span class="sxs-lookup"><span data-stu-id="69321-132">If the number is significantly higher than expected, consider caching the corresponding nodes of the configuration.</span></span>

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a><span data-ttu-id="69321-133">Tietokantakutsujen analysoiminen</span><span class="sxs-lookup"><span data-stu-id="69321-133">Analyze database calls</span></span>

<span data-ttu-id="69321-134">Valmistele esimerkki, jossa on hieman tietoja, jotta voit kerätä [ER-jäljityksen](#electronic-reporting-traces).</span><span class="sxs-lookup"><span data-stu-id="69321-134">Prepare an example that has a small amount of data, so that you can collect an [ER trace](#electronic-reporting-traces).</span></span>

<span data-ttu-id="69321-135">Avaa sitten jäljitys ER-mallin määritysten suunnitteluohjelmassa ja katso sivun alaosaa.</span><span class="sxs-lookup"><span data-stu-id="69321-135">Then open the trace in the ER model mapping designer, and look at the bottom of the page.</span></span> <span data-ttu-id="69321-136">Vastaa seuraaviin kysymyksiin:</span><span class="sxs-lookup"><span data-stu-id="69321-136">Answer the following questions:</span></span>

- <span data-ttu-id="69321-137">Onko kyselyiden kaksoiskappaleita?</span><span class="sxs-lookup"><span data-stu-id="69321-137">Is there any query duplication?</span></span> <span data-ttu-id="69321-138">Jos on, harkitse jotakin seuraavista korjauksista:</span><span class="sxs-lookup"><span data-stu-id="69321-138">If there is, consider one of the following fixes:</span></span>

    - <span data-ttu-id="69321-139">[Käytä välimuistiintallentamista](#use-caching), jos yhdessä päätietueessa on useita kutsuja.</span><span class="sxs-lookup"><span data-stu-id="69321-139">[Use caching](#use-caching) if you think that there are several calls inside one parent record.</span></span>
    - <span data-ttu-id="69321-140">[Käytä välimuistiin tallennettua ja parametrien perusteella laskettua kenttää](#cached-parameterized), jos samaan tietueeseen kohdistuu kutsuja eri tietueissa.</span><span class="sxs-lookup"><span data-stu-id="69321-140">[Use a cached, parameterized calculated field](#cached-parameterized) if you think that there are calls to the same record inside different records.</span></span>
    - <span data-ttu-id="69321-141">[Käytä **JOIN**-tietolähdettä](#use-join-datasource), jos sinun on luettava eri tietokannasta merkittävä määrä eri tietueita.</span><span class="sxs-lookup"><span data-stu-id="69321-141">[Use a **JOIN** data source](#use-join-datasource) if you have to read to a substantial number of different records from a database.</span></span>

- <span data-ttu-id="69321-142">Vastaako kyselyiden ja noudettujen tietueiden määrä yleistä tietomäärää?</span><span class="sxs-lookup"><span data-stu-id="69321-142">Does the number of queries and fetched records correspond to the overall amount of data?</span></span> <span data-ttu-id="69321-143">Jos asiakirjassa on esimerkiksi 10 riviä, osoittavatko tilastotiedot, että raportti sisältää 10 riviä tai 1 000 riviä?</span><span class="sxs-lookup"><span data-stu-id="69321-143">For example, if a document has 10 lines, do the statistics show that the report extracts 10 lines or 1,000 lines?</span></span> <span data-ttu-id="69321-144">Jos sinulla on noudettuna suuri tietueiden määrä, ota huomioon jokin seuraavista korjauksista:</span><span class="sxs-lookup"><span data-stu-id="69321-144">If you have a substantial number of fetched records, consider one of the following fixes:</span></span>

    - <span data-ttu-id="69321-145">[Käytä **FILTER**-toimintoa **WHERE**-toiminnon asemesta](#filter), kun käsittelet tietoja SQL Serverin puolella.</span><span class="sxs-lookup"><span data-stu-id="69321-145">[Use the **FILTER** function instead of the **WHERE** function](#filter) to process data on the SQL Server side.</span></span>
    - <span data-ttu-id="69321-146">Välimuistiin tallentaminen estää samojen tietojen hakemisen.</span><span class="sxs-lookup"><span data-stu-id="69321-146">Use caching to avoid fetching the same data.</span></span>
    - <span data-ttu-id="69321-147">[Koostavia tietofunktioita käyttämällä](#collected-data) voidaan välttää samojen tietojen hakeminen yhteenvetoa varten.</span><span class="sxs-lookup"><span data-stu-id="69321-147">[Use collected data functions](#collected-data) to avoid fetching the same data for summarization.</span></span>

### <a name="analyze-perfview-traces"></a><span data-ttu-id="69321-148">PerfView-jäljityksen analysoiminen</span><span class="sxs-lookup"><span data-stu-id="69321-148">Analyze PerfView traces</span></span>

<span data-ttu-id="69321-149">[PerfView](#perfview) on työkalu kokeneille kehittäjille.</span><span class="sxs-lookup"><span data-stu-id="69321-149">[PerfView](#perfview) is a tool for experienced developers.</span></span> <span data-ttu-id="69321-150">Lisätietoja seuraavista vaiheista on ohjeaiheessa [Seinäkellon ajan tutkimuksen perustiedot](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span><span class="sxs-lookup"><span data-stu-id="69321-150">For more detailed information about the following steps, see [Wall Clock Time Investigation Basics](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span></span>

1. <span data-ttu-id="69321-151">Kerää jäljitys säieajan avulla.</span><span class="sxs-lookup"><span data-stu-id="69321-151">Collect a trace by using thread time.</span></span>
2. <span data-ttu-id="69321-152">Sisällytä vain pinot, jotka käyttävät **runUnattended**-määritystä, kun haluat suodattaa vain konfiguraation suorittamisen sisältävät säikeet.</span><span class="sxs-lookup"><span data-stu-id="69321-152">Include only stacks that use **runUnattended**, to filter only the thread that has configuration execution.</span></span> <span data-ttu-id="69321-153">(Lisää **runUnattended** **IncPats**-syöttöruutuun.)</span><span class="sxs-lookup"><span data-stu-id="69321-153">(Add **runUnattended** to the **IncPats** input box.)</span></span>
3. <span data-ttu-id="69321-154">Kerää kaikki, suorittimen, verkon ja estojen ajat.</span><span class="sxs-lookup"><span data-stu-id="69321-154">Fold all CPU, network, and blocked time.</span></span>
4. <span data-ttu-id="69321-155">Lataa [PerfViewin ER-esimääritykset](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span><span class="sxs-lookup"><span data-stu-id="69321-155">Load [ER presets for PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span></span>
5. <span data-ttu-id="69321-156">Valitse **ER** \> **Muu esimääritys**.</span><span class="sxs-lookup"><span data-stu-id="69321-156">Select **ER** \> **Other preset**.</span></span>
6. <span data-ttu-id="69321-157">Tarkastele nimiä:</span><span class="sxs-lookup"><span data-stu-id="69321-157">Look at the names:</span></span>

    - <span data-ttu-id="69321-158">Todennäköisesti näet alustan koodin, joka kuluttaa eniten aikaa.</span><span class="sxs-lookup"><span data-stu-id="69321-158">You will probably see the platform code that consumes the most time.</span></span>
    - <span data-ttu-id="69321-159">Voit kaksoisnapauttaa (tai kaksoisnapsauttaa) ja käydä läpi **kutsuttavia kohteita**.</span><span class="sxs-lookup"><span data-stu-id="69321-159">You can double-tap (or double-click) and go up through **callees**.</span></span>

        <span data-ttu-id="69321-160">Jos käytössä on luokkia, joissa on etuliite "ERExpression" ja jos ne ovat kaavoihin liittyviä toimintoja, voit päätellä toiminnon nimen luokan nimen perusteella ja voit tarkastella määritteitä ER-säilössä.</span><span class="sxs-lookup"><span data-stu-id="69321-160">If you find classes that have the prefix "ERExpression," and if they are functions that are related to formulas, you can guess the function name based on the class name, and you can look at the ER repo to view the attributes.</span></span>

### <a name="fixes"></a><span data-ttu-id="69321-161">Korjaukset</span><span class="sxs-lookup"><span data-stu-id="69321-161">Fixes</span></span>

- <span data-ttu-id="69321-162">Jos kyselyt kuluttavat suurimman osan suorittimen ajasta, yritä vähentää kyselyiden määrää:</span><span class="sxs-lookup"><span data-stu-id="69321-162">If you see that most of the CPU time is consumed by queries, try to reduce the number of queries:</span></span>

    - <span data-ttu-id="69321-163">[Tarkista ER-jäljitys](#analyze-database-calls) kaksoiskappalekyselyiden varalta.</span><span class="sxs-lookup"><span data-stu-id="69321-163">[Review the ER trace](#analyze-database-calls) for duplicated queries.</span></span>
    - <span data-ttu-id="69321-164">Katso, montako tietuetta haetaan, ja arvioi, paljonko tietoja pitäisi teoreettisesti hakea.</span><span class="sxs-lookup"><span data-stu-id="69321-164">See how many records are fetched, and evaluate how much data should theoretically be fetched.</span></span>

- <span data-ttu-id="69321-165">Jos näet, että käytettävät toiminnot kuluttavat suurimman osan suorittimen ajasta, etsi konfiguraation paikka, joka kuluttaa eniten resursseja.</span><span class="sxs-lookup"><span data-stu-id="69321-165">If you see that most of the CPU time is consumed by the functions that are used, try to find the place in the configuration that consumes the most resources.</span></span>
- <span data-ttu-id="69321-166">Jos näet, että tietojen keruutoiminnot kuluttavat suurimman osan suoritinajasta, kannattaa mallin määrityspuolella korvata ne *SQL:n GROUP BY -määrityksellä*.</span><span class="sxs-lookup"><span data-stu-id="69321-166">If you see that most of the CPU time is consumed by data collection functions, consider replacing them with *SQL group by* on the model mapping side.</span></span>

### <a name="collecting-data"></a><a name="collecting-data"></a><span data-ttu-id="69321-167">Tietojenkeruu</span><span class="sxs-lookup"><span data-stu-id="69321-167">Collecting data</span></span>

<span data-ttu-id="69321-168">Ympäristösi mukaan saatavilla olevia tietoja voidaan kerätä useilla eri tavoilla:</span><span class="sxs-lookup"><span data-stu-id="69321-168">Depending on your environment, there are several ways to collect available data:</span></span>

- <span data-ttu-id="69321-169">Hae kokonaissuoritusaika:</span><span class="sxs-lookup"><span data-stu-id="69321-169">Get the total running time:</span></span>

    - <span data-ttu-id="69321-170">Toimintokeskuksesta</span><span class="sxs-lookup"><span data-stu-id="69321-170">From the Action center</span></span>
    - <span data-ttu-id="69321-171">Tapahtumalokista</span><span class="sxs-lookup"><span data-stu-id="69321-171">From the event log</span></span>

- <span data-ttu-id="69321-172">Profiloi suoritus:</span><span class="sxs-lookup"><span data-stu-id="69321-172">Profile the execution:</span></span>

    - <span data-ttu-id="69321-173">ER-työkalujen avulla</span><span class="sxs-lookup"><span data-stu-id="69321-173">By using ER tools</span></span>
    - <span data-ttu-id="69321-174">Jäljityksen jäsennyksen avulla</span><span class="sxs-lookup"><span data-stu-id="69321-174">By using Trace parser</span></span>
    - <span data-ttu-id="69321-175">PerfViewin avulla</span><span class="sxs-lookup"><span data-stu-id="69321-175">By using PerfView</span></span>

#### <a name="collecting-data-in-a-production-environment"></a><span data-ttu-id="69321-176">Tietojen kerääminen tuotantoympäristössä</span><span class="sxs-lookup"><span data-stu-id="69321-176">Collecting data in a production environment</span></span>

<span data-ttu-id="69321-177">Joskus ongelmat voidaan toistaa vain tuotantoympäristössä.</span><span class="sxs-lookup"><span data-stu-id="69321-177">Sometimes, issues can be reproduced only in a production environment.</span></span> <span data-ttu-id="69321-178">Tietoja voidaan kerätä seuraavilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="69321-178">Data can be collected in the following ways:</span></span>

- <span data-ttu-id="69321-179">[Jäljityksen jäsentimen](../perf-test/trace-trace-tutorial.md) jäljityksien avulla</span><span class="sxs-lookup"><span data-stu-id="69321-179">By using [Trace parser](../perf-test/trace-trace-tutorial.md) traces</span></span>
- <span data-ttu-id="69321-180">Käyttämällä [ER-suorituksen](trace-execution-er-troubleshoot-perf.md) jäljitystä</span><span class="sxs-lookup"><span data-stu-id="69321-180">By using [ER execution](trace-execution-er-troubleshoot-perf.md) traces</span></span>
- <span data-ttu-id="69321-181">Käyttämällä kokonaissuorituksen aikaa</span><span class="sxs-lookup"><span data-stu-id="69321-181">By using the total execution time</span></span>

#### <a name="collecting-data-in-a-development-environment"></a><span data-ttu-id="69321-182">Tietojen kerääminen kehitysympäristössä</span><span class="sxs-lookup"><span data-stu-id="69321-182">Collecting data in a development environment</span></span>

<span data-ttu-id="69321-183">Tuotantoympäristössä käytettävissä olevien mainittujen työkalujen lisäksi kehitysympäristössä voi käyttää useita työkaluja:</span><span class="sxs-lookup"><span data-stu-id="69321-183">In addition to the tools that can be used in a production environment, there are several tools that you can use in a development environment:</span></span>

- <span data-ttu-id="69321-184">Tapahtumaloki (Microsoft-Dynamics-ElectronicReporting).</span><span class="sxs-lookup"><span data-stu-id="69321-184">Event log (Microsoft-Dynamics-ElectronicReporting).</span></span> <span data-ttu-id="69321-185">Tämä loki voi antaa sinulle kokonaissuorituksen ajan.</span><span class="sxs-lookup"><span data-stu-id="69321-185">This log can give you the total execution time.</span></span>
- <span data-ttu-id="69321-186">Yleiset .NET-työkalut, esimerkiksi PerfView.</span><span class="sxs-lookup"><span data-stu-id="69321-186">Common .NET tools, such as PerfView.</span></span>

<span data-ttu-id="69321-187">Kehitysympäristön avulla voit myös joustavammin kokeilla.</span><span class="sxs-lookup"><span data-stu-id="69321-187">Additionally, a development environment gives you more flexibility to experiment.</span></span> <span data-ttu-id="69321-188">Voit esimerkiksi poistaa raporttien osia käytöstä, kun haluat nähdä, miten suoritusaika vaikuttaa.</span><span class="sxs-lookup"><span data-stu-id="69321-188">For example, you can turn off parts of reports to see how the execution time is affected.</span></span>

### <a name="tools"></a><a name="tools"></a><span data-ttu-id="69321-189">Työkalut</span><span class="sxs-lookup"><span data-stu-id="69321-189">Tools</span></span>

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a><span data-ttu-id="69321-190">Suoritusaika toimintokeskuksessa</span><span class="sxs-lookup"><span data-stu-id="69321-190">Execution time in the Action center</span></span>

<span data-ttu-id="69321-191">ER voi näyttää konfiguraation suoritusajan toimintokeskuksessa.</span><span class="sxs-lookup"><span data-stu-id="69321-191">ER can show the execution time of the configuration in the Action center.</span></span> <span data-ttu-id="69321-192">Tämä vaihtoehto toimii vain tietylle käyttäjälle ja tietylle yritykselle, ja vain vuorovaikutteisissa istunnoissa.</span><span class="sxs-lookup"><span data-stu-id="69321-192">This option works only for a specific user and a specific company, and only for interactive sessions.</span></span> <span data-ttu-id="69321-193">Voit ottaa tämän ominaisuuden käyttöön noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="69321-193">To make this feature available, follow these steps.</span></span>

1. <span data-ttu-id="69321-194">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="69321-194">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="69321-195">Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.</span><span class="sxs-lookup"><span data-stu-id="69321-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="69321-196">Määritä **Käyttäjän parametrit** -valintaikkunassa **Näytä tiedoston luontiaika** -valinnaksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="69321-196">In the **User parameters** dialog box, set the **Show file generation time** option to **Yes**.</span></span>

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a><span data-ttu-id="69321-197">Suoritusaika tapahtumalokissa</span><span class="sxs-lookup"><span data-stu-id="69321-197">Execution time in the event log</span></span>

1. <span data-ttu-id="69321-198">Avaa Windowsin tapahtumien katseluohjelma.</span><span class="sxs-lookup"><span data-stu-id="69321-198">Open Windows Event Viewer.</span></span>
2. <span data-ttu-id="69321-199">Avaa **Sovellukset ja palvelut** -kohdassa **Microsoft-Dynamics-ElectronicReporting/Operational**.</span><span class="sxs-lookup"><span data-stu-id="69321-199">Under **Applications and Services logs**, open **Microsoft-Dynamics-ElectronicReporting/Operational**.</span></span>
3. <span data-ttu-id="69321-200">Etsi **FormatMapingRun**-tapahtumia, joissa **EventID=2**, koska nämä tapahtumat sisältävät kulunutta aikaa koskevat tiedot.</span><span class="sxs-lookup"><span data-stu-id="69321-200">Look for **FormatMapingRun** events where **EventID=2**, because these events contain the information about elapsed time.</span></span>

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a><span data-ttu-id="69321-201">Jäljityksen jäsentimen jäljitykset</span><span class="sxs-lookup"><span data-stu-id="69321-201">Trace parser traces</span></span> 

<span data-ttu-id="69321-202">Koska ER on toteutettu X++-koodilla, voit käyttää yleisiä X++-työkaluja suorituskyvyn analysoimiseen.</span><span class="sxs-lookup"><span data-stu-id="69321-202">Because ER is implemented in X++, you can use common X++ tools to analyze performance.</span></span> <span data-ttu-id="69321-203">Lisätietoja on kohdassa [Jäljityksen ottaminen jäljityksen jäsennyksen avulla](../perf-test/trace-trace-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="69321-203">For more information, see [Take traces by using Trace parser](../perf-test/trace-trace-tutorial.md).</span></span>

<span data-ttu-id="69321-204">Tähän lähestymistapaan liittyy muutamia rajoituksia.</span><span class="sxs-lookup"><span data-stu-id="69321-204">There are a few limitations to this approach.</span></span> <span data-ttu-id="69321-205">Koska osa ER:stä on toteutettu C#-koodilla, kaikki tiedot eivät ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="69321-205">Because part of ER is implemented in C#, not all the details will be available.</span></span> <span data-ttu-id="69321-206">Voit kuitenkin tarkastella tietojen käyttötietoja.</span><span class="sxs-lookup"><span data-stu-id="69321-206">However, you can view the data usage details.</span></span> <span data-ttu-id="69321-207">Lisäksi pitkät raporttien ajot voivat ylittää jäljityksen tallennusrajoitukset.</span><span class="sxs-lookup"><span data-stu-id="69321-207">Additionally, long report runs can exceed trace storage limitations.</span></span>

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a><span data-ttu-id="69321-208">ER-jäljitys</span><span class="sxs-lookup"><span data-stu-id="69321-208">ER traces</span></span>

<span data-ttu-id="69321-209">ER voi kerätä omat jäljityksensä, ja sillä on visuaalisia ja analyysityökaluja kyseisiä jäljityksiä varten.</span><span class="sxs-lookup"><span data-stu-id="69321-209">ER can collect its own traces, and it has visualization and analysis tools for those traces.</span></span> <span data-ttu-id="69321-210">Lisätietoja: [Sähköisen raportoinnin muotojen suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="69321-210">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

#### <a name="perfview"></a><a name="perfview"></a><span data-ttu-id="69321-211">PerfView</span><span class="sxs-lookup"><span data-stu-id="69321-211">PerfView</span></span>

<span data-ttu-id="69321-212">Koska sekä X++ että ER on toteutettu .NET-alustalla, voit käyttää yleisiä .NET-työkaluja.</span><span class="sxs-lookup"><span data-stu-id="69321-212">Because both X++ and ER are implemented on top of the .NET platform, you can use common .NET tools.</span></span> <span data-ttu-id="69321-213">Voit käyttää esimerkiksi maksutonta [PerfView](https://github.com/Microsoft/perfview)-työkalua.</span><span class="sxs-lookup"><span data-stu-id="69321-213">For example, you can use the free [PerfView](https://github.com/Microsoft/perfview) tool.</span></span>

<span data-ttu-id="69321-214">Voit myös kerätä tietoja komentoriviltä.</span><span class="sxs-lookup"><span data-stu-id="69321-214">You can also collect data from the command line.</span></span> <span data-ttu-id="69321-215">Esimerkiksi seuraava Windows PowerShell -komentosarja kerää suoritusajan, kunnes kaikki kaavan suoritukset pysäytetään koneessa.</span><span class="sxs-lookup"><span data-stu-id="69321-215">For example, the following Windows PowerShell script collects the execution time until any format execution is stopped on the machine.</span></span>

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

<span data-ttu-id="69321-216">Tähän lähestymistapaan liittyy muutamia rajoituksia.</span><span class="sxs-lookup"><span data-stu-id="69321-216">There are a few limitations to this approach.</span></span> <span data-ttu-id="69321-217">Sinulla on oltava järjestelmänvalvojan käyttöoikeus koneeseen.</span><span class="sxs-lookup"><span data-stu-id="69321-217">You must have administrative access to the machine.</span></span> <span data-ttu-id="69321-218">Lisäksi sinun on oltava kokenut kehittäjä, koska oppimiseen kuluu pitkä aika.</span><span class="sxs-lookup"><span data-stu-id="69321-218">Additionally, you must be an experienced developer, because there is a steep learning curve.</span></span>

### <a name="making-changes"></a><a name="making-changes"></a><span data-ttu-id="69321-219">Muutosten tekeminen</span><span class="sxs-lookup"><span data-stu-id="69321-219">Making changes</span></span>

#### <a name="use-caching"></a><a name="use-caching"></a><span data-ttu-id="69321-220">Käytä välimuistiin tallentamista</span><span class="sxs-lookup"><span data-stu-id="69321-220">Use caching</span></span>

<span data-ttu-id="69321-221">Vaikka välimuistiin tallentaminen vähentää tietojen hakemiseen tarvittavaa aikaa, se kuluttaa muistia.</span><span class="sxs-lookup"><span data-stu-id="69321-221">Although caching reduces the amount of time that is required to fetch data again, it costs memory.</span></span> <span data-ttu-id="69321-222">Käytä välimuistiin tallentamista, kun haettavat tiedot eivät ole hyvin suuria.</span><span class="sxs-lookup"><span data-stu-id="69321-222">Use caching in cases where the amount of fetched data isn't very large.</span></span> <span data-ttu-id="69321-223">Lisätietoja ja esimerkki siitä, miten välimuistiin tallentamista käytetään, on kohdassa [Mallin määrityksen parantaminen suoritusjäljityksen tietojen perusteella](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span><span class="sxs-lookup"><span data-stu-id="69321-223">For more information and an example that shows how to use caching, see [Improve the model mapping based on information from the execution trace](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span></span>

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a><span data-ttu-id="69321-224">Käytä välimuistiin tallennettua parametrisoitua laskettua kenttää</span><span class="sxs-lookup"><span data-stu-id="69321-224">Use a cached, parameterized calculated field</span></span>

<span data-ttu-id="69321-225">Joskus arvot on etsittävä toistuvasti.</span><span class="sxs-lookup"><span data-stu-id="69321-225">Sometimes, values must be looked up repeatedly.</span></span> <span data-ttu-id="69321-226">Esimerkkejä tällaisista ovat tilien nimet ja tilinumerot.</span><span class="sxs-lookup"><span data-stu-id="69321-226">Examples include account names and account numbers.</span></span> <span data-ttu-id="69321-227">Voit säästää aikaa luomalla lasketun kentän, jonka parametrit ovat ylimmällä tasolla, ja lisätä sitten kentän välimuistiin.</span><span class="sxs-lookup"><span data-stu-id="69321-227">To help save time, you can create a calculated field that has parameters on the top level, and then add the field to the cache.</span></span>

<span data-ttu-id="69321-228">Tätä menetelmää kannattaa käyttää vain, jos välimuistiin tallennettujen tietojen koko on pieni.</span><span class="sxs-lookup"><span data-stu-id="69321-228">We recommend that you use this approach only when the size of the cached data is small.</span></span> <span data-ttu-id="69321-229">Lisätietoja on kohdassa [ER-ratkaisujen suorituskyvyn parantamiseen lisäämällä parametrisoituja laskettujen kenttien tietolähteitä](er-calculated-field-ds-performance.md).</span><span class="sxs-lookup"><span data-stu-id="69321-229">For more information, see [Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources](er-calculated-field-ds-performance.md).</span></span>

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a><span data-ttu-id="69321-230">Käytä JOIN-tietolähdettä</span><span class="sxs-lookup"><span data-stu-id="69321-230">Use a JOIN data source</span></span>

<span data-ttu-id="69321-231">**JOIN**-tietolähde mahdollistaa usean yhdistetyn tietueen hakemisen yhdellä kyselyllä.</span><span class="sxs-lookup"><span data-stu-id="69321-231">A **JOIN** data source enables several connected records to be fetched by one query.</span></span> <span data-ttu-id="69321-232">Kutakin liitettyä tietuetta ei tarvitse hakea erillisellä kyselyllä.</span><span class="sxs-lookup"><span data-stu-id="69321-232">A separate query doesn't have to be used to fetch each connected record.</span></span> <span data-ttu-id="69321-233">Jos sinulla on esimerkiksi 1 000 riviä ja haet kunkin rivin nimiketiedot suhteen mukaan, kyselyjä on 1 001 (= 1 000 + 1).</span><span class="sxs-lookup"><span data-stu-id="69321-233">For example, if you have 1,000 lines, and you fetch item data for each line by relation, you will have 1,001 queries (= 1,000 + 1).</span></span> <span data-ttu-id="69321-234">Jos käytät **JOIN**-tietolähdettä, samat tiedot voi hakea vain yhden kyselyn avulla.</span><span class="sxs-lookup"><span data-stu-id="69321-234">If you use a **JOIN** data source, you will use only one query to fetch the same data.</span></span> <span data-ttu-id="69321-235">Lisätietoja: [Käytä sähköisen raportoinnin (ER) mallimäärityksissä JOIN-tietolähteitä saadaksesi tietoja useista sovellustaulukoista](er-join-data-sources.md).</span><span class="sxs-lookup"><span data-stu-id="69321-235">For more information, see [Use JOIN data sources in ER model mappings to get data from multiple application tables](er-join-data-sources.md).</span></span>

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a><span data-ttu-id="69321-236">Käytä FILTER-toimintoa WHERE-toiminnon asemesta</span><span class="sxs-lookup"><span data-stu-id="69321-236">Use the FILTER function instead of the WHERE function</span></span>

<span data-ttu-id="69321-237">**[FILTER](er-functions-list-filter.md)**-toiminto suorittaa ehdot SQL Serverissä, kun taas **WHERE**-toiminto noutaa kaikki tiedot luettelosta yksi tietue kerrallaan ja soveltaa ehtoa kuhunkin tietueeseen.</span><span class="sxs-lookup"><span data-stu-id="69321-237">The **[FILTER](er-functions-list-filter.md)** function runs conditions on SQL Server, whereas the **WHERE** function fetches all data from the list, one record at a time, and applies the condition for each record.</span></span> <span data-ttu-id="69321-238">Haluat esimerkiksi valita yhden tietueen 1 000 tietueesta.</span><span class="sxs-lookup"><span data-stu-id="69321-238">For example, you want to select one record out of 1,000 records.</span></span> <span data-ttu-id="69321-239">Jos käytät **WHERE**-toimintoa, kaikki 1 000 tietuetta haetaan.</span><span class="sxs-lookup"><span data-stu-id="69321-239">If you use **WHERE**, all 1,000 records will be fetched.</span></span> <span data-ttu-id="69321-240">Jos kuitenkin käytät **FILTER**-toimintoa, noudetaan täsmälleen yksi tietue.</span><span class="sxs-lookup"><span data-stu-id="69321-240">However, if you use **FILTER**, exactly one record will be fetched.</span></span> <span data-ttu-id="69321-241">**FILTER** voi käyttää myös tietokantapuolen indeksejä.</span><span class="sxs-lookup"><span data-stu-id="69321-241">**FILTER** can also use indexes on the database side.</span></span>

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a><span data-ttu-id="69321-242">Kerättyjen tietotoimintojen tai kumulatiivisen datatietolähteen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="69321-242">Using collected data functions or an accumulated data data source</span></span>

<span data-ttu-id="69321-243">Jos konfiguraatiossa on *GROUP BY* -komponentti, joka sisältää aiemmin haettujen tietojen yhteenvedon raportissa, komponentti noutaa kaikki tiedot uudelleen.</span><span class="sxs-lookup"><span data-stu-id="69321-243">If your configuration has a *group by* component that summarizes previously fetched data by report, the component will fetch all the data again.</span></span> <span data-ttu-id="69321-244">Käyttämällä kerättyjä datafunktioita ER:n avulla voit koota tietoja ensimmäisen noutamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="69321-244">By using collected data functions, you enable ER to accumulate data during the first fetch.</span></span> <span data-ttu-id="69321-245">Lisä tietoja on kohdassa [ER – Määritä muoto suorittamaan laskenta ja summaus](tasks/er-format-counting-summing-2.md).</span><span class="sxs-lookup"><span data-stu-id="69321-245">For more information, see [ER Configure format to do counting and summing](tasks/er-format-counting-summing-2.md).</span></span>

#### <a name="rewrite-parts-of-the-configuration-in-x"></a><span data-ttu-id="69321-246">Korvaa osia konfiguraatiosta X++-koodissa</span><span class="sxs-lookup"><span data-stu-id="69321-246">Rewrite parts of the configuration in X++</span></span>

<span data-ttu-id="69321-247">ER tukee taulujen ja luokkien sekä laajennusten kutsumenetelmiä.</span><span class="sxs-lookup"><span data-stu-id="69321-247">ER supports calling methods of tables and classes, including extensions.</span></span> <span data-ttu-id="69321-248">Harkitse mallimäärityksen osien uudelleen kirjoittamista X++-koodissa suorituskyvyn parantamiseksi.</span><span class="sxs-lookup"><span data-stu-id="69321-248">Consider rewriting parts of the model mapping in X++ to help improve performance.</span></span>

<span data-ttu-id="69321-249">ER voi kuluttaa seuraavien lähteiden tietoja:</span><span class="sxs-lookup"><span data-stu-id="69321-249">ER can consume data from the following sources:</span></span>

- <span data-ttu-id="69321-250">Luokat (**objekti**- ja **luokka**-tietolähteet)</span><span class="sxs-lookup"><span data-stu-id="69321-250">Classes (**object** and **class** data sources)</span></span>
- <span data-ttu-id="69321-251">Taulut (**taulu**- ja **taulutietue**-tietolähteet)</span><span class="sxs-lookup"><span data-stu-id="69321-251">Tables (**table** and **table records** data sources)</span></span>

<span data-ttu-id="69321-252">[ER-sovellusliittymän](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) avulla voi myös lähettää esilasketut tiedot kutsuvasta koodista.</span><span class="sxs-lookup"><span data-stu-id="69321-252">The [ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) also provides a way to send precalculated data from the calling code.</span></span> <span data-ttu-id="69321-253">Sovellusohjelma sisältää useita esimerkkejä tästä lähestymistavasta.</span><span class="sxs-lookup"><span data-stu-id="69321-253">The application suite contains numerous examples of this approach.</span></span>
