---
title: Pääsuunnitteluajon valvonta
description: Tässä ohjeaiheessa selvitetään, miten tuotannon suunnittelija näkee, käsitelläänkö pääsuunnitteluajoa.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 159043f37b067df26fdd1de5610eafd663bf6a57
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209556"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="ba0a3-103">Pääsuunnitteluajon valvonta</span><span class="sxs-lookup"><span data-stu-id="ba0a3-103">Monitor a master planning run</span></span>

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a><span data-ttu-id="ba0a3-104">Pääsuunnittelun edistymisen visualisointi Gantt-kaavion avulla</span><span class="sxs-lookup"><span data-stu-id="ba0a3-104">Use a Gantt chart to visualize master planning progress</span></span>

<span data-ttu-id="ba0a3-105">**Näytä pääsuunnittelun edistyminen** -sivulla pääsuunnitteluajoen historiatietoja Gantt-kaaviona.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-105">From the **View master planning progress** page, you can view details of historical master planning runs as a Gantt chart.</span></span> <span data-ttu-id="ba0a3-106">Tämän toiminnon avulla voi selvittää, kuinka kauan aikaa pääsuunnittelun eri vaiheisiin kului.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-106">This functionality can help you understand the time that is spent on the various phases of master planning.</span></span> <span data-ttu-id="ba0a3-107">Nykyisessä aktiivisessa suunnittelutyössä **Näytä pääsuunnittelun edistyminen** -sivun avulla voi seurata edistymistä ja näyttää arvioidun jäljellä olevan ajan.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-107">For a current active planning job, the **View master planning progress** page can be used to track progress and view the estimated remaining time.</span></span>

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a><span data-ttu-id="ba0a3-108">Pääsuunnittelun etenemisen visualisointitoiminnon ottaminen käyttöön ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="ba0a3-108">Turn on and use the Master plan progress visualization feature</span></span>

<span data-ttu-id="ba0a3-109">Voit käyttää tätä toimintoa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="ba0a3-109">To use this functionality, follow these steps.</span></span>

1. <span data-ttu-id="ba0a3-110">Valitse **Toimintojen hallinta** -työtilan **Uusi**-lehden luettelossa **Pääsuunnittelun etenemisen visualisointi**.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-110">In the **Feature management** workspace, on the **New** tab, select **Master planning progress visualization** in the list.</span></span> <span data-ttu-id="ba0a3-111">Jos toiminto ei ole **Uusi**-välilehdessä, tarkista myös **Ei käytössä**- ja **Kaikki**-välilehdet.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="ba0a3-112">Valitse **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-112">Select **Enable now**.</span></span> <span data-ttu-id="ba0a3-113">Vaihtoehtoisesti voi valita **Aikataulu** ja valita sitten ajan, jolloin haluat ottaa toiminnon käyttöön.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

<span data-ttu-id="ba0a3-114">**Näytä pääsuunnittelun edistyminen** -sivulla voi olla näkyvissä sekä historiallisia että aktiivisia suunnittelutöitä.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-114">The **View master planning progress** page can display both historical planning jobs and active planning jobs.</span></span> 

<span data-ttu-id="ba0a3-115">Historiallisten suunnittelutöiden näyttämiseen on kaksi vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-115">To view historical planning jobs, there are two options.</span></span> 

1. <span data-ttu-id="ba0a3-116">Valitse ensin **Pääsuunnittelu \> Asetukset \> Suunnitelmat \> Pääsuunnitelmat** ja valitse sitten toimintoruudussa **Historia**.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-116">Go to **Master planning \> Setup \> Plans \> Master plans**, and then, on the Action Pane, select **History**.</span></span> <span data-ttu-id="ba0a3-117">Kun sopiva työ on valittu, valitse ensin **Kyselyt** ja sitten **Näytä edistyminen**</span><span class="sxs-lookup"><span data-stu-id="ba0a3-117">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>
1. <span data-ttu-id="ba0a3-118">Valitse ensin **Pääsuunnittelu \> Työtilat \> Pääsuunnittelu** ja valitse sitten Pääsuunnittelu-ruudussa **Historia**.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-118">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **History**.</span></span> <span data-ttu-id="ba0a3-119">Kun sopiva työ on valittu, valitse ensin **Kyselyt** ja sitten **Näytä edistyminen**</span><span class="sxs-lookup"><span data-stu-id="ba0a3-119">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="ba0a3-120">Aktiivisten suunnittelutöiden näyttämiseen on kaksi vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-120">To view active planning jobs, there are two options.</span></span> 
1. <span data-ttu-id="ba0a3-121">Valitse ensin **Pääsuunnittelu \> Työtilat \> Pääsuunnittelu** ja valitse sitten toimintoruudussa **Keskeneräiset suunnitteluprosessit**.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-121">Go to **Master planning \> Workspaces \> Master planning**, on the Action Pane, select **Unfinished planning process**.</span></span> <span data-ttu-id="ba0a3-122">Kun sopiva työ on valittu, valitse ensin **Kyselyt** ja sitten **Näytä edistyminen**.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-122">With the desired job selected, select **Inquiries**,  and then select **View progress**.</span></span>
1. <span data-ttu-id="ba0a3-123">Valitse ensin **Pääsuunnittelu \> Työtilat \> Pääsuunnittelu** ja valitse sitten Pääsuunnittelu-ruudussa **Näytä edistyminen**.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-123">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **View progress**.</span></span> <span data-ttu-id="ba0a3-124">Kun sopiva työ on valittu, valitse ensin **Kyselyt** ja sitten **Näytä edistyminen**</span><span class="sxs-lookup"><span data-stu-id="ba0a3-124">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="ba0a3-125">Huomaa, että voit tarkastella aktiivisia töitä vain silloin, kun suunnittelutyötä käsitellään.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-125">Note you can view active jobs only when a planning job is processing.</span></span>

### <a name="analyze-a-master-planning-job"></a><span data-ttu-id="ba0a3-126">Pääsuunnittelun työn analysoiminen</span><span class="sxs-lookup"><span data-stu-id="ba0a3-126">Analyze a master planning job</span></span>

<span data-ttu-id="ba0a3-127">Voit laajentaa Gantt-kaavion kunkin seuraavista suunnitteluprosesseista ja tarkastella ajankäyttöön liittyviä lisätietoja:</span><span class="sxs-lookup"><span data-stu-id="ba0a3-127">In the Gantt chart, you can expand each of the following planning processes to view additional details about the time that is spent:</span></span>

- <span data-ttu-id="ba0a3-128">Alustetaan</span><span class="sxs-lookup"><span data-stu-id="ba0a3-128">Initializing</span></span>
- <span data-ttu-id="ba0a3-129">Poistetaan ja lisätään tietoja</span><span class="sxs-lookup"><span data-stu-id="ba0a3-129">Deleting and inserting data</span></span>
- <span data-ttu-id="ba0a3-130">Kattavuussuunnittelu</span><span class="sxs-lookup"><span data-stu-id="ba0a3-130">Coverage planning</span></span>
- <span data-ttu-id="ba0a3-131">Viiveet</span><span class="sxs-lookup"><span data-stu-id="ba0a3-131">Delays</span></span>
- <span data-ttu-id="ba0a3-132">Toimintosanomat</span><span class="sxs-lookup"><span data-stu-id="ba0a3-132">Action messages</span></span>
- <span data-ttu-id="ba0a3-133">Viimeistely</span><span class="sxs-lookup"><span data-stu-id="ba0a3-133">Finalization</span></span>
- <span data-ttu-id="ba0a3-134">Automaattinen vahvistus</span><span class="sxs-lookup"><span data-stu-id="ba0a3-134">Auto-firming</span></span>

<span data-ttu-id="ba0a3-135">Gantt-kaavio on kätevä työkalu, jos haluat tarkastella toimenpidesanomien vaikutusta.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-135">The Gantt chart is a useful tool if you want to view the impact of using action messages.</span></span>

#### <a name="navigation-in-the-gantt-chart"></a><span data-ttu-id="ba0a3-136">Siirtyminen Gantt-kaaviossa</span><span class="sxs-lookup"><span data-stu-id="ba0a3-136">Navigation in the Gantt chart</span></span>

- <span data-ttu-id="ba0a3-137">Voit laajentaa valittua ryhmää ja näyttää tiedot valitsemalla plus-merkin (**+**) puunäkymässä.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-137">To expand the selected group and show the details, select the plus sign (**+**) in the tree view.</span></span>
- <span data-ttu-id="ba0a3-138">Voit pienentää valitun ryhmän valitsemalla puunäkymässä miinus-merkin (**–**).</span><span class="sxs-lookup"><span data-stu-id="ba0a3-138">To collapse the selected group, select the minus sign (**–**) in the tree view.</span></span>
- <span data-ttu-id="ba0a3-139">Voit käyttää näppäimistöä siirtymiseen.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-139">You can use your keyboard for navigation.</span></span> <span data-ttu-id="ba0a3-140">Voit siirtyä riviltä toiselle **ylänuoli**- ja **alanuoli**-näppäimillä.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-140">Use the **Up arrow** and **Down arrow** keys to move between rows.</span></span> <span data-ttu-id="ba0a3-141">Voit laajentaa ja tiivistää ryhmiä **oikealla** ja **vasemmalla nuolinäppäimellä**.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-141">Use the **Right arrow** and **Left arrow** keys to expand and collapse groups.</span></span>
- <span data-ttu-id="ba0a3-142">Voit avata tai sulkea kaikki Gantt-kaavion tasot valitsemalla **Laajenna kaikki** tai **Tiivistä kaikki**.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-142">To open or close all levels in the Gantt chart, select **Expand all** or **Collapse all**.</span></span>
- <span data-ttu-id="ba0a3-143">Voit tarkastella liittyvää käsittelyaikaa pitämällä hiiren osoitinta tehtävän päällä.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-143">To view the related processing time, hover over a task.</span></span> <span data-ttu-id="ba0a3-144">(Tehtävät ovat Gantt-kaavion alin taso.)</span><span class="sxs-lookup"><span data-stu-id="ba0a3-144">(Tasks are the lowest level in the Gantt chart.)</span></span>

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a><span data-ttu-id="ba0a3-145">Töiden vertailu näyttämällä muu pääsuunnitteluajo</span><span class="sxs-lookup"><span data-stu-id="ba0a3-145">View an additional master planning run to compare jobs</span></span>

<span data-ttu-id="ba0a3-146">Valitsemalla pääsuunnittelutyön **Näytä muu pääsuunnitteluajo** -kentässä, voit tarkastella toista pääsuunnittelutyötä Gantt-kaaviossa ja vertailla töitä.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-146">By selecting a master planning job on field **Show additional master planning run**, you can view an additional master planning run in the Gantt chart and compare the two jobs.</span></span>

#### <a name="bom-level-display"></a><span data-ttu-id="ba0a3-147">Tuoterakennetason näyttö</span><span class="sxs-lookup"><span data-stu-id="ba0a3-147">BOM-level display</span></span>

<span data-ttu-id="ba0a3-148">Tuoterakennetasot näytetään eri tavalla, kun kyse on kattavuuden suunnittelusta, viiveistä, toimenpiteistä ja vahvistuksesta.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-148">Bill of materials (BOM) levels are shown differently for coverage planning, delays, actions, and firming.</span></span>

- <span data-ttu-id="ba0a3-149">**Kattavuuden suunnittelu** – Tuoterakennetasot näytetään odotetusti.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-149">**Coverage planning** – BOM levels are shown as expected.</span></span> <span data-ttu-id="ba0a3-150">Ne lasketaan ylhäältä alaspäin.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-150">They are calculated from the top down.</span></span>

    <span data-ttu-id="ba0a3-151">**Esimerkki:** tuoterakennetaso 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="ba0a3-151">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="ba0a3-152">**Viiveet** – Tuoterakennetasot näytetään kattavuuden suunnittelun tuoterakennetasoina –1:llä kerrottuna.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-152">**Delays** – BOM levels are shown as the coverage planning BOM levels multiplied by –1.</span></span> <span data-ttu-id="ba0a3-153">(Toisin sanoen niissä on negatiivinen merkki.)</span><span class="sxs-lookup"><span data-stu-id="ba0a3-153">(In other words, they have a negative sign.)</span></span>

    <span data-ttu-id="ba0a3-154">**Esimerkki:** tuoterakennetaso –2, –1, 0</span><span class="sxs-lookup"><span data-stu-id="ba0a3-154">**Example:** BOM level –2, –1, 0</span></span>

- <span data-ttu-id="ba0a3-155">**Toimenpidesanoma** – Tuoterakennetasot näytetään odotetusti.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-155">**Action message** – BOM levels are shown as expected.</span></span> <span data-ttu-id="ba0a3-156">Ne lasketaan ylhäältä alaspäin.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-156">They are calculated from the top down.</span></span>

    <span data-ttu-id="ba0a3-157">**Esimerkki:** tuoterakennetaso 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="ba0a3-157">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="ba0a3-158">**Automaattinen vahvistus** – tuoterakennetasot näytetään 999, josta on vähennetty kattavuuden suunnittelu tuoterakennetaso.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-158">**Auto-firming** – BOM levels are shown as 999 minus the coverage planning BOM level.</span></span>

    <span data-ttu-id="ba0a3-159">**Esimerkki:** tuoterakennetaso 999, 998, 997</span><span class="sxs-lookup"><span data-stu-id="ba0a3-159">**Example:** BOM level 999, 998, 997</span></span>

<span data-ttu-id="ba0a3-160">Seuraavassa taulukossa on edellisten yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-160">The following table summarizes the behavior.</span></span>

| <span data-ttu-id="ba0a3-161">Näytettävä tuoterakennetaso</span><span class="sxs-lookup"><span data-stu-id="ba0a3-161">BOM level that is shown</span></span> | <span data-ttu-id="ba0a3-162">Loppunimike</span><span class="sxs-lookup"><span data-stu-id="ba0a3-162">End item</span></span> | <span data-ttu-id="ba0a3-163">Alikomponentti</span><span class="sxs-lookup"><span data-stu-id="ba0a3-163">Subcomponent</span></span> | <span data-ttu-id="ba0a3-164">Raaka-aine</span><span class="sxs-lookup"><span data-stu-id="ba0a3-164">Raw material</span></span> |
|---|---|---|---|
| <span data-ttu-id="ba0a3-165">Kattavuussuunnittelu</span><span class="sxs-lookup"><span data-stu-id="ba0a3-165">Coverage planning</span></span> | <span data-ttu-id="ba0a3-166">0</span><span class="sxs-lookup"><span data-stu-id="ba0a3-166">0</span></span> | <span data-ttu-id="ba0a3-167">1</span><span class="sxs-lookup"><span data-stu-id="ba0a3-167">1</span></span> | <span data-ttu-id="ba0a3-168">2</span><span class="sxs-lookup"><span data-stu-id="ba0a3-168">2</span></span> |
| <span data-ttu-id="ba0a3-169">Viiveet</span><span class="sxs-lookup"><span data-stu-id="ba0a3-169">Delays</span></span> | <span data-ttu-id="ba0a3-170">0</span><span class="sxs-lookup"><span data-stu-id="ba0a3-170">0</span></span> | <span data-ttu-id="ba0a3-171">–1</span><span class="sxs-lookup"><span data-stu-id="ba0a3-171">–1</span></span> | <span data-ttu-id="ba0a3-172">–2</span><span class="sxs-lookup"><span data-stu-id="ba0a3-172">–2</span></span> |
| <span data-ttu-id="ba0a3-173">Toimenpidesanoma</span><span class="sxs-lookup"><span data-stu-id="ba0a3-173">Action message</span></span> | <span data-ttu-id="ba0a3-174">0</span><span class="sxs-lookup"><span data-stu-id="ba0a3-174">0</span></span> | <span data-ttu-id="ba0a3-175">1</span><span class="sxs-lookup"><span data-stu-id="ba0a3-175">1</span></span> | <span data-ttu-id="ba0a3-176">2</span><span class="sxs-lookup"><span data-stu-id="ba0a3-176">2</span></span> |
| <span data-ttu-id="ba0a3-177">Automaattinen vahvistus</span><span class="sxs-lookup"><span data-stu-id="ba0a3-177">Auto-firming</span></span> | <span data-ttu-id="ba0a3-178">999</span><span class="sxs-lookup"><span data-stu-id="ba0a3-178">999</span></span> | <span data-ttu-id="ba0a3-179">998</span><span class="sxs-lookup"><span data-stu-id="ba0a3-179">998</span></span> | <span data-ttu-id="ba0a3-180">997</span><span class="sxs-lookup"><span data-stu-id="ba0a3-180">997</span></span> |

#### <a name="visualize-progress"></a><span data-ttu-id="ba0a3-181">Edistymisen visualisointi</span><span class="sxs-lookup"><span data-stu-id="ba0a3-181">Visualize progress</span></span>

<span data-ttu-id="ba0a3-182">Jos tarkastelet käsittelyssä olevaa pääsuunnittelutyötä, edistyminen näytetään Gantt-kaaviossa värien avulla.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-182">If you view a master planning job that is currently running, progress is shown through colors in the Gantt chart.</span></span> <span data-ttu-id="ba0a3-183">Seuraava värien teema on sininen.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-183">The following colors apply to the blue theme.</span></span> <span data-ttu-id="ba0a3-184">Muiden väriteemojen värit ovat erilaiset.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-184">For other color themes, the colors will differ.</span></span>

- <span data-ttu-id="ba0a3-185">**Tummansininen** – valmistuneet suunnittelutehtävät.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-185">**Dark blue** – Completed planning tasks.</span></span>
- <span data-ttu-id="ba0a3-186">**Oranssi** – käsiteltävänä oleva tehtävä.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-186">**Orange** – The task that is currently in progress.</span></span>
- <span data-ttu-id="ba0a3-187">**Vaaleansininen** – arvio jäljellä olevista tehtävistä.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-187">**Light blue** – The estimate for remaining tasks.</span></span>

<span data-ttu-id="ba0a3-188">Väri näkyy vain Gantt-kaavion alimmalla tasolla.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-188">The color is shown only on the lowest level in the Gantt chart.</span></span> <span data-ttu-id="ba0a3-189">Valitsemalla **Laajenna kaikki** voit tarkastella kaikkia pääsuunnittelutyön tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-189">Select **Expand all** to view all tasks in the master planning job.</span></span> <span data-ttu-id="ba0a3-190">Arvio jäljellä olevista tehtävistä perustuu historiallisiin pääsuunnittelutöihin.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-190">The estimate of remaining tasks is based on historical master planning jobs.</span></span>

## <a name="run-master-planning-and-track-processing-time"></a><span data-ttu-id="ba0a3-191">Pääsuunnittelun suorittaminen ja käsittelyajan seuraaminen</span><span class="sxs-lookup"><span data-stu-id="ba0a3-191">Run master planning and track processing time</span></span>

1. <span data-ttu-id="ba0a3-192">Valitse oletuskoontinäytössä **Pääsuunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-192">On the default dashboard, select **Master planning**.</span></span>
1. <span data-ttu-id="ba0a3-193">Anna tai valitse **Suunnitelma**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-193">In the **Plan** field, enter or select a value.</span></span>
1. <span data-ttu-id="ba0a3-194">Valitse **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-194">Select **Run**.</span></span>
1. <span data-ttu-id="ba0a3-195">Määritä **Seuraa käsittelyaikaa**-asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-195">Set the **Track processing time** option to **Yes**.</span></span>
1. <span data-ttu-id="ba0a3-196">Syötä **Säikeiden määrä** -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-196">In the **Number of threads** field, enter a number.</span></span>
1. <span data-ttu-id="ba0a3-197">Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodatus**.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-197">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="ba0a3-198">Valitse ruudukossa rivi, jonka **Kenttä**-kentän arvona on **Nimiketunnus**.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-198">In the grid, select the row where the **Field** field is set to **Item number**.</span></span>
1. <span data-ttu-id="ba0a3-199">Anna **Ehdot**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-199">In the **Criteria** field, enter a value.</span></span>
1. <span data-ttu-id="ba0a3-200">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ba0a3-200">Select **OK**.</span></span>
