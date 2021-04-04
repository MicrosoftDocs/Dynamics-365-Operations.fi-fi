---
title: Työn luonnin aikatauluttaminen aallon aikana
description: Tässä aiheessa käsitellään työn luonnin aikatauluttamisen aaltokäsittelymenetelmän määrittämistä ja käyttämistä.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 36a450f78695f617056875f8d236fe46bc66aaaf
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501219"
---
# <a name="schedule-work-creation-during-wave"></a><span data-ttu-id="3539b-103">Työn luonnin aikatauluttaminen aallon aikana</span><span class="sxs-lookup"><span data-stu-id="3539b-103">Schedule work creation during wave</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="3539b-104">*Työn luonnin aikataulutustoimintoa* käytetään aaltoprosessin osana parantamaan aaltokäsittelyn siirtomäärää siten, että järjestelmä luo työn käyttämällä rinnakkaiskäsittelyä.</span><span class="sxs-lookup"><span data-stu-id="3539b-104">Use the *Schedule work creation* feature as part of your waving process to help increase wave processing throughput by having the system create work using parallel processing.</span></span>

<span data-ttu-id="3539b-105">Kun toiminto on otettu käyttöön, suunniteltu työ luodaan automaattisesti, ja järjestelmä käsittelee sen jossain vaiheessa, jolloin varsinainen työ luodaan.</span><span class="sxs-lookup"><span data-stu-id="3539b-105">When the functionality is enabled, planned work will automatically get created, which the system will eventually process to create actual work.</span></span> <span data-ttu-id="3539b-106">Jos aallon kuormarivien määrä saavuttaa esimääritetyn rajan, järjestelmä luo varsinaisen työn nopeammin hyödyntämällä rinnakkaista, asynkronista käsittelyä.</span><span class="sxs-lookup"><span data-stu-id="3539b-106">If the number of wave load lines reaches a predetermined threshold, the system will create actual work more quickly by applying parallel, asynchronous processing.</span></span>

## <a name="enable-the-schedule-work-creation-feature"></a><span data-ttu-id="3539b-107">Työn luonnin aikataulutustoiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="3539b-107">Enable the Schedule work creation feature</span></span>

### <a name="enable-the-feature-in-feature-management"></a><span data-ttu-id="3539b-108">Toiminnon ottaminen käyttöön ominaisuuksien hallinnassa</span><span class="sxs-lookup"><span data-stu-id="3539b-108">Enable the feature in feature management</span></span>

<span data-ttu-id="3539b-109">Ennen kuin *työn luonnin aikataulutustoimintoa* voidaan käyttää, se on otettava käyttöön järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="3539b-109">Before you can use the *Schedule work creation* feature, it must be turned on in your system.</span></span> <span data-ttu-id="3539b-110">Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="3539b-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="3539b-111">Tässä tapauksessa toiminto näkyy seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="3539b-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="3539b-112">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="3539b-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="3539b-113">**Toiminnon nimi:** *Työn luonnin aikataulutus*</span><span class="sxs-lookup"><span data-stu-id="3539b-113">**Feature name:** *Schedule work creation*</span></span>

> [!NOTE]
> <span data-ttu-id="3539b-114">*Organisaation laajuinen työn esto* -toiminto on oltava otettuna käyttöön, ennen kuin *Aikatauluta työn luonti* voidaan ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="3539b-114">The *Organization-wide work blocking* feature must be enabled before you can enable *Schedule work creation*.</span></span>

### <a name="manually-enable-batch-processing-of-waves"></a><span data-ttu-id="3539b-115">Aaltojen eräkäsittelyn ottaminen käyttöön manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="3539b-115">Manually enable batch processing of waves</span></span>

<span data-ttu-id="3539b-116">Varastotyön luominen hyödyntämällä rinnakkaista, asynkronista menetelmää edellyttää, että aaltokäsittely suoritetaan erinä.</span><span class="sxs-lookup"><span data-stu-id="3539b-116">To take advantage of a parallel asynchronous method to create warehouse work, your wave process must be running in batch.</span></span> <span data-ttu-id="3539b-117">Se määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="3539b-117">To set this up:</span></span>

1. <span data-ttu-id="3539b-118">Valitse  **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.</span><span class="sxs-lookup"><span data-stu-id="3539b-118">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>

1. <span data-ttu-id="3539b-119">Määritä **Yleiset**-välilehden **Käsittele aaltoja erässä** -asetukseksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="3539b-119">On the **General** tab, set **Process waves in batch** to *Yes*.</span></span> <span data-ttu-id="3539b-120">Valinnaisena on mahdollista valita myös erillinen **Aallon käsittelyn eräryhmä**, joka estää eräjonon käsittelemisen suorittaminen samanaikaisesti muiden prosessien kanssa.</span><span class="sxs-lookup"><span data-stu-id="3539b-120">Optionally, you can also select a dedicated **Wave processing batch group** to prevent your batch queue processing from running at the same time as other processes.</span></span>

1. <span data-ttu-id="3539b-121">Määritä **Odota lukitusta (ms)**, jota käytetään, kun järjestelmä käsittelee useita aaltoja samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="3539b-121">Set the **Wait for lock (ms) time**, which applies when the system is processing several waves at the same time.</span></span> <span data-ttu-id="3539b-122">Useimmille suurille aaltokäsittelyille arvoksi kannattaa valita *60 000*.</span><span class="sxs-lookup"><span data-stu-id="3539b-122">For most larger waving processes, we recommend a value of *60000*.</span></span>

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a><span data-ttu-id="3539b-123">Uuden aallon vaihemenetelmän ottaminen käyttöön manuaalisesti aiemmin luoduissa aaltomalleissa</span><span class="sxs-lookup"><span data-stu-id="3539b-123">Manually enable the new wave step method for existing wave templates</span></span>

<span data-ttu-id="3539b-124">Aloita luomalla uusi aallon vaihemenetelmä ja ottamalla se käyttöön rinnakkaisessa, asynkronisessa tehtävän käsittelyssä.</span><span class="sxs-lookup"><span data-stu-id="3539b-124">Start by creating the new wave step method and enabling it for parallel asynchronous task processing.</span></span>

1. <span data-ttu-id="3539b-125">Valitse  **Varastonhallinta \> Asetukset \> Aallot \> Aallon käsittelymenetelmät**.</span><span class="sxs-lookup"><span data-stu-id="3539b-125">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>

1. <span data-ttu-id="3539b-126">Valitse  **Luo menetelmät uudelleen** ja kiinnitä huomiota siihen, että *WHSScheduleWorkCreationWaveStepMethod* on lisätty luetteloon lähetyksen aaltomalleissa käytettävissä olevista aallon käsittelymenetelmistä.</span><span class="sxs-lookup"><span data-stu-id="3539b-126">Select  **Regenerate method** and note that *WHSScheduleWorkCreationWaveStepMethod* has been added to the list of wave process methods you can use in your shipping wave templates.</span></span>

1. <span data-ttu-id="3539b-127">Valitse tietue, jonka **Menetelmän nimi** on *WHSScheduleWorkCreationWaveStepMethod*, ja valitse **Tehtävän määritys**.</span><span class="sxs-lookup"><span data-stu-id="3539b-127">Select the record with the **Method name** *WHSScheduleWorkCreationWaveStepMethod* and select **Task configuration**.</span></span>

1. <span data-ttu-id="3539b-128">Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi** ja käyttämällä seuraavia asetuksia:</span><span class="sxs-lookup"><span data-stu-id="3539b-128">To add a new row to the grid, select **New** on the Action Pane and use the following settings:</span></span>

    - <span data-ttu-id="3539b-129">**Varasto** – valitse varasto, jota käytetään työn luonnin käsittelyn aikatauluttamiseen.</span><span class="sxs-lookup"><span data-stu-id="3539b-129">**Warehouse** - Select the warehouse you will use to schedule work creation processing.</span></span>

    - <span data-ttu-id="3539b-130">**Erätehtävien enimmäismäärä** – Määritä erätehtävien enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="3539b-130">**Maximum number of batch tasks** - Specify a maximum number of batch tasks.</span></span> <span data-ttu-id="3539b-131">Useimmissa tapauksissa tämän arvon on syytä olla 8–16, mutta optimaalista asetusta eri skenaarioihin kannattaa etsiä kokeilemalla.</span><span class="sxs-lookup"><span data-stu-id="3539b-131">In most cases, this value should be in the range from 8-16, however we recommend that you experiment with the optimal setting based on your scenarios.</span></span>

    - <span data-ttu-id="3539b-132">**Aallon käsittelyn eräryhmä** – valitse erillinen aallon käsittelyn eräryhmä optimoimaan eräjonon käsittely.</span><span class="sxs-lookup"><span data-stu-id="3539b-132">**Wave processing batch group** - Select a dedicated wave processing batch group to optimize your batch queue processing.</span></span>

<span data-ttu-id="3539b-133">Aiemmin luotu aaltomalli voidaan nyt päivittää (tai uusi aaltomalli luoda) käyttämään aallon *Aikatauluta työn luonti* -käsittelymenetelmää.</span><span class="sxs-lookup"><span data-stu-id="3539b-133">Now you are ready to update an existing wave template (or create a new one) to use the *Schedule work creation* wave processing method.</span></span>

1. <span data-ttu-id="3539b-134">Valitse  **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.</span><span class="sxs-lookup"><span data-stu-id="3539b-134">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>

1. <span data-ttu-id="3539b-135">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="3539b-135">Select **Edit** on the Action Pane.</span></span>

1. <span data-ttu-id="3539b-136">Valitse luetteloruudussa päivitettävä aaltomalli. (Jos testaukseen käytetään esittelytietoja, voit käyttää mallia *24 Lähetyksen oletus*).</span><span class="sxs-lookup"><span data-stu-id="3539b-136">In the list pane, select the wave template you would like to update (if you are testing using demo data, then you could use *24 Shipping default*).</span></span>

1. <span data-ttu-id="3539b-137">Laajenna **Menetelmät**-pikavälilehti ja valitse **Jäljellä olevat menetelmät** -ruudukossa rivi, jonka **Nimi** on *Aikatauluta työn luonti*.</span><span class="sxs-lookup"><span data-stu-id="3539b-137">Expand the **Methods** FastTab and select the row with the **Name** *Schedule work creation* in the **Remaining methods** grid.</span></span>

1. <span data-ttu-id="3539b-138">Valitse **Valitut menetelmät** -sarakkeeseen osoittava nuoli ja siirrä valittu rivi kyseiseen sarakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="3539b-138">Select the arrow pointing to the **Selected methods** column to move the selected row to that column.</span></span> <span data-ttu-id="3539b-139">(Valittuna voi olla kerralla vain yksi menetelmä, jossa on käytössä joko *WHSScheduleWorkCreationWaveStepMethod* tai *createWork*, joten aiemmin luotu rivi, jonka **Menetelmän nimi** on *createWork*, siirretään automaattisesti **Jäljellä olevat menetelmät** -ruudukkoon.)</span><span class="sxs-lookup"><span data-stu-id="3539b-139">(You can only have one selected method at a time that uses either *WHSScheduleWorkCreationWaveStepMethod* or *createWork*, so the existing row with **Method name** *createWork* is automatically moved to the **Remaining methods** grid.)</span></span>

## <a name="set-wave-task-processing-threshold-data"></a><span data-ttu-id="3539b-140">Aallon tehtävän käsittelyn raja-arvotietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3539b-140">Set wave task processing threshold data</span></span>

<span data-ttu-id="3539b-141">Järjestelmä luo oletusarvoiset aallon tehtävän käsittelyn raja-arvotiedot, kun aaltokäsittely suoritetaan ensimmäisen kerran käyttämällä tehtävään perustuvaa käsittelyä.</span><span class="sxs-lookup"><span data-stu-id="3539b-141">The system will create default wave task processing threshold data the first time a wave process runs using any task-based processing.</span></span> <span data-ttu-id="3539b-142">Tietojen avulla määritetään, milloin aaltokäsittely suoritetaan asynkronisesti ja tehtävään perustuen, jolloin työn rinnakkainen käsittely ja luonti on mahdollista.</span><span class="sxs-lookup"><span data-stu-id="3539b-142">The data is used to control when wave processing will run asynchronously and be task-based, which enables it to process and create work in parallel.</span></span>

<span data-ttu-id="3539b-143">Oletustiedot käyttävät aluksi kuormarivien minimimäärän (MINIMUMWAVELOADLINES) raja-arvona 15:tä.</span><span class="sxs-lookup"><span data-stu-id="3539b-143">The default data will initially use a threshold value of 15 for the minimum number of load lines (MINIMUMWAVELOADLINES).</span></span> <span data-ttu-id="3539b-144">Tämä tarkoittaa sitä, että kun järjestelmä käsittelee yli 15 kuormariviä sisältävää aaltoa, se käyttää asynkronista tehtävien käsittelyä.</span><span class="sxs-lookup"><span data-stu-id="3539b-144">This means that when the system processes a wave with more than 15 loads lines, it will use asynchronous task processing.</span></span> <span data-ttu-id="3539b-145">Nämä tiedot voidaan lisätä tai päivittää manuaalisesti testiympäristöjen **WHSWaveTaskProcessingThresholdParameters**-taulussa. Jos tätä asetusta on muutettava tuotantoympäristössä, päivitystä on pyydettävä Microsoftin tuesta.</span><span class="sxs-lookup"><span data-stu-id="3539b-145">You can manually insert/update this data in the **WHSWaveTaskProcessingThresholdParameters** table in your test environments, but if you need to change this setting in a production environment, you must contact Microsoft Support to request the update.</span></span>

## <a name="work-with-the-feature"></a><span data-ttu-id="3539b-146">Toiminnon käyttäminen</span><span class="sxs-lookup"><span data-stu-id="3539b-146">Work with the feature</span></span>

<span data-ttu-id="3539b-147">Kun *Aikatauluta työn luonti* -toiminto on otettu käyttöön, aaltokäsittely luo suunnitellun työn, jota uuden työn luontiprosessi käyttää jossain vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="3539b-147">When the *Schedule work creation* functionality is enabled, wave processing will create planned work, which will eventually be used by the new work creation process.</span></span> <span data-ttu-id="3539b-148">Työ estetään työn luonnin aikana *Organisaation laajuinen työn esto* -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="3539b-148">During work creation, the work will be blocked using the *Organization-wide work blocking* feature.</span></span>

<span data-ttu-id="3539b-149">Seuraava vuokaavio osoittaa, miten suunniteltu työ luodaan aaltokäsittelyn aikana.</span><span class="sxs-lookup"><span data-stu-id="3539b-149">The following flowchart shows how planned work is created during wave processing.</span></span>

![Ajoita työn luonti](media/schedule-work-creation-process.png)

### <a name="planned-work"></a><span data-ttu-id="3539b-151">Suunniteltu työ</span><span class="sxs-lookup"><span data-stu-id="3539b-151">Planned work</span></span>

<span data-ttu-id="3539b-152">**Suunnitellun työn tiedot** -sivulla (**Varastonhallinta \> Työ \> Suunnitellun työn tiedot**) on tietoja suunnitellusta työstä, joka luotiin ensin aaltokäsittelyn aikana.</span><span class="sxs-lookup"><span data-stu-id="3539b-152">The **Planned work details** page (**Warehouse management \> Work \> Planned work details**) shows information about the planned work, which is initially created during wave processing.</span></span> <span data-ttu-id="3539b-153">Seuraavat **Prosessin tila** -arvot ovat käytettävissä:</span><span class="sxs-lookup"><span data-stu-id="3539b-153">The following **Process status** values are available:</span></span>

- <span data-ttu-id="3539b-154">**Asetettu jonoon** – suunniteltu työ odottaa, että sitä käytetään työn luontiin.</span><span class="sxs-lookup"><span data-stu-id="3539b-154">**Queued** - The planned work is waiting to be used to create work.</span></span>
- <span data-ttu-id="3539b-155">**Valmis** – suunniteltua työtä on käytetty työn luontiin.</span><span class="sxs-lookup"><span data-stu-id="3539b-155">**Completed** - The planned work has been used to create work.</span></span>
- <span data-ttu-id="3539b-156">**Epäonnistui** – Aaltokäsittely on epäonnistunut.</span><span class="sxs-lookup"><span data-stu-id="3539b-156">**Failed** – The wave processing has failed.</span></span> <span data-ttu-id="3539b-157">Huomaa, että suunnitellun työn tila voi olla **Epäonnistui** riippumatta siitä, onko sillä liittyvää varsinaista työtä.</span><span class="sxs-lookup"><span data-stu-id="3539b-157">Note that the planned work can be in a **Failed** state with or without related actual work.</span></span> <span data-ttu-id="3539b-158">Kun varsinaisen työn luontiprosessi epäonnistuu, varsinaisen työn tilaksi jää *Peruutettu*.</span><span class="sxs-lookup"><span data-stu-id="3539b-158">When the actual work creation process fails, the actual work remains in status *Cancelled*.</span></span>

### <a name="batch-job-for-the-work-creation-process"></a><span data-ttu-id="3539b-159">Työn luontiprosessin erätyö</span><span class="sxs-lookup"><span data-stu-id="3539b-159">Batch job for the work creation process</span></span>

<span data-ttu-id="3539b-160">Käsittelyaaltojen erätöitä voi tarkastella valitsemalla **Kaikki aallot** -sivun toimintoruudussa **Erätyöt**.</span><span class="sxs-lookup"><span data-stu-id="3539b-160">To view the batch jobs for processing waves, select **Batch jobs** on the Action Pane on the **All waves** page.</span></span>

<span data-ttu-id="3539b-161">Tällä tavoin voi tarkastella kunkin erätyötunnuksen kaikki erätehtävän tietoja.</span><span class="sxs-lookup"><span data-stu-id="3539b-161">From here, you can view all the batch task details for each of the batch job IDs.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]