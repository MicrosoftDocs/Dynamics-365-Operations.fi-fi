---
title: Aallon kohdistus
description: Tässä aiheessa kuvataan, miten voit määrittää aallon kohdistusvaiheen. Tässä aiheessa kuvataan myös, miten sen rinnakkaiskäsittely otetaan käyttöön.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: feee33a7d4ea3f0d9c4d671210293a28aac14f61
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823164"
---
# <a name="wave-allocation"></a><span data-ttu-id="c34bf-103">Aallon kohdistus</span><span class="sxs-lookup"><span data-stu-id="c34bf-103">Wave allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c34bf-104">Aallon käsittelyssä voi kulua kauan, ja suurin osa käsittelyajasta kuluu kohdistusvaiheessa ja työn luontivaiheessa.</span><span class="sxs-lookup"><span data-stu-id="c34bf-104">Wave processing can be time consuming, and most of the processing time is spent in the allocation step and in the work creation step.</span></span>

<span data-ttu-id="c34bf-105">Kaikki nämä vaiheet on nyt mahdollista suorittaa rinnakkain, mikä voi parantaa aallon käsittelyn suorituskykyä ja mahdollistaa suuremman määrän aaltojen samassa varastossa.</span><span class="sxs-lookup"><span data-stu-id="c34bf-105">It is now possible to run each of these steps in parallel, which can improve the performance of the wave processing, and allow for a larger throughput of waves in the same warehouse.</span></span> <span data-ttu-id="c34bf-106">Tässä aiheessa kerrotaan, miten voit määrittää aallon kohdistusmenetelmän, joka suoritetaan rinnakkain.</span><span class="sxs-lookup"><span data-stu-id="c34bf-106">This topic explains how to set up the wave allocation method to run in parallel.</span></span> <span data-ttu-id="c34bf-107">Lisätietoja siitä, miten työn luonti määritetään samanaikaista ajoa varten, on kohdassa [Aikatauluta työn luonti aallon aikana](configure-wave-schedule-work-creation.md).</span><span class="sxs-lookup"><span data-stu-id="c34bf-107">For more information about how to set up work creation to run in parallel, see [Schedule work creation during wave](configure-wave-schedule-work-creation.md).</span></span>

<span data-ttu-id="c34bf-108">Aiemmin varastossa voi kohdistaa vain yhden aallon kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="c34bf-108">Previously it was only possible to allocate one wave at a warehouse at a time.</span></span> <span data-ttu-id="c34bf-109">Tämä rajoitus on poistettu ja korvattu uudella rajoituksella, joka lukitsee vain ne nimikkeet ja dimensiot, jotka ovat varaushierarkiassa yläpuolella.</span><span class="sxs-lookup"><span data-stu-id="c34bf-109">This constraint has been removed and replaced by a new constraint that only locks the item and dimensions that are above location in the reservation hierarchy.</span></span> <span data-ttu-id="c34bf-110">Sijainnin yläpuolella olevat dimensiot sisältävät aina tuotedimensioita.</span><span class="sxs-lookup"><span data-stu-id="c34bf-110">Dimensions above the location always include product dimensions.</span></span> <span data-ttu-id="c34bf-111">Jos nimike on määritetty esimerkiksi *Väri*-määrityksen avulla, *punaisen*, *sinisen* ja *keltaisen* variantin voi kunkin käsitellä rinnakkain.</span><span class="sxs-lookup"><span data-stu-id="c34bf-111">For example, if an item is configured using *Color*, then variants for *Red*, *Blue*, and *Yellow* could each be processed in parallel.</span></span>

<span data-ttu-id="c34bf-112">Tämä tarkoittaa, että jos sama nimike, jolla on samat dimensiot sijainnin yläpuolella, kohdistetaan yhteen aaltoon, muiden aaltojen on odotettava lukitusta samalle nimikkeelle ja dimensioille.</span><span class="sxs-lookup"><span data-stu-id="c34bf-112">This means that if the same item with the same dimensions above the location is being allocated by one wave, other waves will have to wait to acquire a lock on the same item and dimensions.</span></span> <span data-ttu-id="c34bf-113">Jos lukitusta ei voi hankkia ajoissa, tulee virhe ja aallon käsittely epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="c34bf-113">If the lock can't be acquired in a timely manner, an error will occur and the wave processing will fail.</span></span>

<span data-ttu-id="c34bf-114">Rinnakkaiskäsittelyn hyödyntäminen edellyttää, että aalto on suoritettava erätyönä.</span><span class="sxs-lookup"><span data-stu-id="c34bf-114">In order to utilize parallel processing, the wave must run in batch.</span></span>

## <a name="performance-improvements"></a><span data-ttu-id="c34bf-115">Suorituskykyä koskevat parannukset</span><span class="sxs-lookup"><span data-stu-id="c34bf-115">Performance improvements</span></span>

<span data-ttu-id="c34bf-116">Rinnakkaiskäsittelyn suorituskykyedut kuuluvat kahteen luokkaan:</span><span class="sxs-lookup"><span data-stu-id="c34bf-116">Performance benefits of parallel processing fall in two categories:</span></span>

- <span data-ttu-id="c34bf-117">**Parannettu siirtomäärä** – Aaltojen siirtomäärä parantuu yleensä, vaikka rinnakkaiskäsittelyä ei ole määritetty, erityisesti tilanteissa, joissa nimikkeillä ei ole päällekkäisyyksiä aaltojen sisällä.</span><span class="sxs-lookup"><span data-stu-id="c34bf-117">**Improved throughput** - The throughput of waves will typically improve even if parallel processing isn't configured, especially for scenarios where there is no overlap of items within the waves.</span></span>
- <span data-ttu-id="c34bf-118">**Yksittäisen aallon kohdistuksen parannus** – Testaaminen asiakastiedoilla on osoittanut, että suorituskyky parani lähes 50 prosenttia sen jälkeen, kun siirryttiin rinnakkaisiin kohdistuksiin.</span><span class="sxs-lookup"><span data-stu-id="c34bf-118">**Improvement of the allocation for a single wave** - Testing on customer data has shown a near 50% performance improvement after switching to parallel allocation.</span></span> <span data-ttu-id="c34bf-119">Rinnakkaiskäsittely tehdään sijainnin yläpuolella olevien nimikkeiden ja dimensioiden mukaan, joten parannukset määräytyvät sen mukaan, montako eri nimikettä aalto sisältää, mikä on käytettävissä oleva infrastruktuuri sekä mikä on kohdistuksen kesto verrattuna työn luonnin kestoon.</span><span class="sxs-lookup"><span data-stu-id="c34bf-119">The parallel processing is done per items and dimensions above the location, so the improvements depend on how many different items a wave contains, the infrastructure available, and the duration of the allocation versus the duration of the work creation.</span></span>

## <a name="configure-parallel-allocation"></a><span data-ttu-id="c34bf-120">Rinnakkaisen kohdistuksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c34bf-120">Configure parallel allocation</span></span>

### <a name="warehouse-management-parameters"></a><span data-ttu-id="c34bf-121">Varastonhallinnan parametrit</span><span class="sxs-lookup"><span data-stu-id="c34bf-121">Warehouse management parameters</span></span>

<span data-ttu-id="c34bf-122">Jos haluat käyttää rinnakkaista kohdistuskäsittelyä, siirry kohtaan **Varastonhallinta > Asetukset > Varastonhallinnan parametrit**, avaa **AAllon käsittely** -välilehti ja tee seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="c34bf-122">To use parallel allocation processing, go to **Warehouse management > Setup > Warehouse management parameters**, open the **Wave processing** tab, and make the following settings:</span></span>

- <span data-ttu-id="c34bf-123">**Aallon käsittelyn eräryhmä** – Valitse eräryhmä, jota aaltojen alkukäsittelyn tulisi käyttää.</span><span class="sxs-lookup"><span data-stu-id="c34bf-123">**Wave processing batch group** - Select the batch group that the initial processing of the waves should use.</span></span> <span data-ttu-id="c34bf-124">Kohdistuksen käsittely tämän jälkeen voidaan tehdä käyttämällä eri eräryhmiä.</span><span class="sxs-lookup"><span data-stu-id="c34bf-124">The subsequent processing of allocation can be done using different batch groups.</span></span>
- <span data-ttu-id="c34bf-125">**Käsittele aallot erinä** – Määritä arvoksi *Kyllä*, jos haluat käyttää rinnakkaiskäsittelyä.</span><span class="sxs-lookup"><span data-stu-id="c34bf-125">**Process waves in batch** - Set this to *Yes* to use parallel processing.</span></span>
- <span data-ttu-id="c34bf-126">**Odota lukitusta (ms)** – Kirjoita millisekunteina aika, jonka kohdistusvaihe odottaa järjestelmäresurssia, joka on toisen kohdistusvaiheen lukitsema.</span><span class="sxs-lookup"><span data-stu-id="c34bf-126">**Wait for lock (ms)** - Enter the time, in milliseconds, that an allocation step will wait for a system resource that is locked by another allocation step.</span></span> <span data-ttu-id="c34bf-127">Kun tämä aika ylitetään, aaltoa ei käsitellä ja virhesanoma tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="c34bf-127">When this time is exceeded, the wave is not processed and an error message is displayed.</span></span> <span data-ttu-id="c34bf-128">Yhden loogisen yksikön kohdistukselle on suositeltavaa sallia vähintään muutaman sekunnin aika.</span><span class="sxs-lookup"><span data-stu-id="c34bf-128">We recommend that you allow at least a few seconds to allow for allocation of one logical unit to finish.</span></span>

<span data-ttu-id="c34bf-129">Lisätietoja näistä ja muista aallon käsittelyvaihtoehdoista **Varastonhallinnan parametrit** -sivulla on kohdassa [Varastonhallinnan parametrit aaltojen käsittelylle](wave-warehouse-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c34bf-129">For information about these and other wave processing options on the **Warehouse management parameters** page, see [Warehouse parameters for wave processing](wave-warehouse-parameters.md).</span></span>

## <a name="wave-process-methods"></a><span data-ttu-id="c34bf-130">Aallon käsittelymenetelmät</span><span class="sxs-lookup"><span data-stu-id="c34bf-130">Wave process methods</span></span>

<span data-ttu-id="c34bf-131">Rinnakkaiskäsittelyn voi määrittää seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="c34bf-131">To set up parallel processing:</span></span>

1. <span data-ttu-id="c34bf-132">Valitse **Varastonhallinta > Asetukset > Aallot A Aallon käsittelymenetelmät**.</span><span class="sxs-lookup"><span data-stu-id="c34bf-132">Go to **Warehouse Management > Setup > Waves > Wave process methods**.</span></span>
1. <span data-ttu-id="c34bf-133">Valitse ruudukossa `allocateWave`-menetelmä.</span><span class="sxs-lookup"><span data-stu-id="c34bf-133">Select the `allocateWave` method in the grid.</span></span>
1. <span data-ttu-id="c34bf-134">Valitse toimintoruudussa **Tehtävän määritys**.</span><span class="sxs-lookup"><span data-stu-id="c34bf-134">On the Action Pane, select **Task configuration**.</span></span>
1. <span data-ttu-id="c34bf-135">**Aallon jälkeisen menetelmän tehtävän määritys** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="c34bf-135">The **Wave post method task configuration** page opens.</span></span> <span data-ttu-id="c34bf-136">Tässä ruudukossa luetellaan kaikki varastot, joissa olet konfiguroinut `allocateWave`-menetelmän.</span><span class="sxs-lookup"><span data-stu-id="c34bf-136">This grid lists each warehouse where you have configured the `allocateWave` method.</span></span> <span data-ttu-id="c34bf-137">Rinnakkaiskäsittelyä käytetään vain luettelon varastoissa.</span><span class="sxs-lookup"><span data-stu-id="c34bf-137">Parallel processing will only be used for warehouses that are listed.</span></span> <span data-ttu-id="c34bf-138">Toimintoruudun painikkeiden avulla voit tarvittaessa lisätä varastoja ruudukkoon tai poistaa niitä ruudukosta.</span><span class="sxs-lookup"><span data-stu-id="c34bf-138">Use the Action Pane buttons to add or remove warehouses from the grid as needed.</span></span> 
1. <span data-ttu-id="c34bf-139">Tee kullekin varastolle seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="c34bf-139">For each warehouse, make the following settings:</span></span>
    - <span data-ttu-id="c34bf-140">**Erätehtävien enimmäismäärä** – Määritä erätehtävien määrä, jota valitun varaston kohdistukssa on käytettävä.</span><span class="sxs-lookup"><span data-stu-id="c34bf-140">**Maximum number of batch tasks** - Specify the number of batch tasks that should be used for the allocation for the selected warehouse.</span></span> <span data-ttu-id="c34bf-141">Erätehtävien optimaalinen määrä riippuu käytettävissä olevasta infrastruktuurista ja palvelimessa käsiteltävästä erätyöstä.</span><span class="sxs-lookup"><span data-stu-id="c34bf-141">The optimal number of batch tasks depends on the infrastructure available and what other batch jobs are being processed on the server.</span></span> <span data-ttu-id="c34bf-142">Kokonaan aaltojen käsittelyyn määritetyllä neljän ytimen ympäristöllä tehdyt testit osoittivat, että kahdeksan tehtävän käyttö tuotti hyviä tuloksia.</span><span class="sxs-lookup"><span data-stu-id="c34bf-142">Tests done on a four core environment that was dedicated to wave processing showed that using eight tasks produced good results.</span></span>
    - <span data-ttu-id="c34bf-143">**Aallon käsittelyn eräryhmä** – Tiettyjä eräryhmiä voidaan käyttää eri varastoille, jotta kohdistuskäsittely voidaan skaalata varastokohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="c34bf-143">**Wave processing batch group** - Specific batch groups can be used for different warehouses to allow the allocation processing to scale out per warehouse.</span></span>

## <a name="enable-or-disable-parallelization-across-all-legal-entities"></a><span data-ttu-id="c34bf-144">Rinnakkaisuuden ottaminen käyttöön ja poistaminen käytöstä kaikissa yrityksissä</span><span class="sxs-lookup"><span data-stu-id="c34bf-144">Enable or disable parallelization across all legal entities</span></span>

<span data-ttu-id="c34bf-145">Suosittelemme, että määrität `allocateWave`-menetelmän, joka suoritetaan rinnakkain kaikissa yritysyksiköissä, koska tämä parantaa aaltokäsittelyn suorituskykyä.</span><span class="sxs-lookup"><span data-stu-id="c34bf-145">We recommend that you set the `allocateWave` method to run in parallel across all legal entities because this helps to improve the performance of the wave processing.</span></span> <span data-ttu-id="c34bf-146">Alkaen Supply Chain Management -versiosta 10.0.17 *Aaltojen rinnakkaisuus Allocate Wave -menetelmälle* -ominaisuus on oletusarvon mukaan käytössä kaikissa uusissa ja päivitetyissä asennuksissa, eikä sitä voi enää poistaa käytöstä.</span><span class="sxs-lookup"><span data-stu-id="c34bf-146">Starting in Supply Chain Management version 10.0.17, the *Wave parallelization for Allocate Wave method* feature is enabled by default for all new and updated installations, and can't be turned off again.</span></span> <span data-ttu-id="c34bf-147">Kun tämä ominaisuus on otettu käyttöön, tapahtuu seuraavaa:</span><span class="sxs-lookup"><span data-stu-id="c34bf-147">After enabling this feature, the following occurs:</span></span>

- <span data-ttu-id="c34bf-148">`allocateWave`-menetelmä päivitetään niin, että se sisältää tehtävän konfiguraation asetuksen, jonka avulla voit **Aallon käsittelymenetelmät** -sivulla määrittää samalla kertaa suoritettavien tehtävien määrän, joka vastaa rinnakkaisten prosessien määrää.</span><span class="sxs-lookup"><span data-stu-id="c34bf-148">The `allocateWave` method is updated to include a task configuration setting that lets you use the **Wave process methods** page to define the number of tasks that will run simultaneously, equivalent to the number of parallel processes.</span></span> <span data-ttu-id="c34bf-149">Tästä seuraa, että aallon kohdistusvaiheissa käytetty aika (joka on tavallisesti 30 – 60 % käsittelyn kokonaisajasta) vähenee tehtävien määrää vastaavalla kertoimella.</span><span class="sxs-lookup"><span data-stu-id="c34bf-149">As a result, the time used on the allocate-wave step (which is typically 30% to 60% of the total processing time) is reduced by a factor roughly equivalent to the number of tasks.</span></span> <span data-ttu-id="c34bf-150">Voit myös valita erän, joka määritetään näiden tehtävien suorittamista varten.</span><span class="sxs-lookup"><span data-stu-id="c34bf-150">It's also possible to select which batch will be assigned to process these tasks.</span></span> <span data-ttu-id="c34bf-151">On tärkeää muistaa, että kaikki yritykset on konfiguroitu käsittelemään aaltoja erissä.</span><span class="sxs-lookup"><span data-stu-id="c34bf-151">It's important to note that all of your legal entities will be configured to process waves in batch.</span></span> <span data-ttu-id="c34bf-152">Käytössä olevat konfiguraatiot säilytetään niiden varastojen varastoissa, jotka on jo konfiguroitu käsittelemään aaltoja erätyönä, ja varastoissa, jotka on jo määritetty käyttämään `allocateWave`-menetelmää rinnakkain.</span><span class="sxs-lookup"><span data-stu-id="c34bf-152">For the warehouses that are already configured to process waves in batch, and for the warehouses that are already configured to use the `allocateWave` method in parallel, the existing configuration will be kept.</span></span>
- <span data-ttu-id="c34bf-153">Oletusarvon mukaan kaikki uudet yritykset on määritetty käsittelemään aaltoja erissä.</span><span class="sxs-lookup"><span data-stu-id="c34bf-153">By default, all the new legal entities are configured to process waves in batch.</span></span> <span data-ttu-id="c34bf-154">Kaikissa uusissa varastoissa, joiden **Varastonhallintaprosessit**-asetus on käytössä, `allocateWave`-menetelmä on määritetty suoritettavaksi oletusarvon mukaan rinnakkain.</span><span class="sxs-lookup"><span data-stu-id="c34bf-154">All new warehouses with the **Warehouse management processes** option enabled will have the `allocateWave` method configured to run in parallel by default.</span></span>
- <span data-ttu-id="c34bf-155">**Varastonhallinnan parametrit** -sivulla **Käsittele aallot erinä** -arvona on *Kyllä* ja **Odota lukitusta  (ms)** -arvoksi asetetaan 15 sekunnin oletusarvo.</span><span class="sxs-lookup"><span data-stu-id="c34bf-155">On the **Warehouse management parameters** page, **Process saves in batch** is set to *Yes* and  **Wait for lock (ms)** set to a default 15 seconds.</span></span> <span data-ttu-id="c34bf-156">Tämä tarkoittaa, että kaikki aallot suoritetaan erinä.</span><span class="sxs-lookup"><span data-stu-id="c34bf-156">This means that all waves will be executed in batch.</span></span> <span data-ttu-id="c34bf-157">Kun aaltoa suoritetaan, se hankkii nimikkeeseen ja sen ylätason sijainnin dimensioiden lukituksen kohdistusvaiheen aikana.</span><span class="sxs-lookup"><span data-stu-id="c34bf-157">When a wave is running, it acquires a lock on the item and dimensions above location during the allocation step.</span></span> <span data-ttu-id="c34bf-158">Kun toinen aallon käsittelytehtävä yrittää hankkia saman lukituksen samalle tietueelle, se estetään, kunnes nykyinen käsittely on valmis.</span><span class="sxs-lookup"><span data-stu-id="c34bf-158">When another wave processing task tries to acquire the same lock for the identical record, it is blocked until the current process is finished.</span></span> <span data-ttu-id="c34bf-159">**Odota lukitusta (ms)** -asetus määrittää enimmäisajan, jonka järjestelmä odottaa ennen lukituksen vapauttamista.</span><span class="sxs-lookup"><span data-stu-id="c34bf-159">The **Wait for lock (ms)** settings establishes the maximum time the system will wait before the lock is released.</span></span>

<span data-ttu-id="c34bf-160">Rinnakkainen kohdistuksen käsittely edellyttää, että aallon käsittely suoritetaan erätyönä.</span><span class="sxs-lookup"><span data-stu-id="c34bf-160">Parallel allocation processing requires wave processing to run in batch.</span></span> <span data-ttu-id="c34bf-161">Sen vuoksi aaltojen käsittelyteho pienenenee, jos poistat **Käsittele aallot erinä** -määrityksen käytöstä, erityisesti jos aallon käsittely käyttää rinnakkaista prosessia, joka on määritetty asiaankuuluvien aaltomenetelmien tehtäväkonfiguraatiossa.</span><span class="sxs-lookup"><span data-stu-id="c34bf-161">Therefore, you will reduce your wave processing performance if you turn off the **Process saves in batch** setting, especially if wave processing is using a parallel process as defined by the task configuration for the relevant wave methods.</span></span>

<span data-ttu-id="c34bf-162">Voit tarvittaessa kumota kaikki asetukset, jotka on tehty oletusarvoisesti, kun *Aaltojen rinnakkaisuus Allocate Wave -menetelmälle* -ominaisuus on automaattisesti otettu käyttöön esiintymässä.</span><span class="sxs-lookup"><span data-stu-id="c34bf-162">If necessary, you can undo each of the settings made by default when the *Wave parallelization for Allocate Wave method* feature is automatically enabled for your instance.</span></span> <span data-ttu-id="c34bf-163">Toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="c34bf-163">To do this:</span></span>

- <span data-ttu-id="c34bf-164">Valitse **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.</span><span class="sxs-lookup"><span data-stu-id="c34bf-164">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span> <span data-ttu-id="c34bf-165">Käytä **Aallon käsittely** -välilehdessä haluamiasi arvoja **Käsittele aallot erinä**- ja **Odota lukitusta (ms)** -asetuksille.</span><span class="sxs-lookup"><span data-stu-id="c34bf-165">On the **Wave processing** tab, apply your preferred values for **Process waves in batch** and **Wait for lock (ms)**.</span></span>
- <span data-ttu-id="c34bf-166">Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aallon käsittelymenetelmät**.</span><span class="sxs-lookup"><span data-stu-id="c34bf-166">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span> <span data-ttu-id="c34bf-167">Valitse `allocateWave`-menetelmä.</span><span class="sxs-lookup"><span data-stu-id="c34bf-167">Select the `allocateWave` method.</span></span> <span data-ttu-id="c34bf-168">Valitse toimintoruudusta **Tehtävän määritys** avataksesi sivun, jolla luetellaan kaikki varastot, joissa menetelmä on määritetty suoritettavaksi rinnakkain.</span><span class="sxs-lookup"><span data-stu-id="c34bf-168">On the Action Pane, select **Task configuration** to open a page that lists each warehouse where the method is set to run in parallel.</span></span> <span data-ttu-id="c34bf-169">Muokkaa tai poista erätehtävien määrää ja määritettyä aaltoryhmää kullekin luettelossa olevalle varastolle tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="c34bf-169">Modify or delete the number of batch tasks and the assigned wave group for each listed warehouse as needed.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="c34bf-170">Vianmääritys</span><span class="sxs-lookup"><span data-stu-id="c34bf-170">Troubleshooting</span></span>

### <a name="troubleshoot-using-the-infolog"></a><span data-ttu-id="c34bf-171">Vianmääritys infolokin avulla</span><span class="sxs-lookup"><span data-stu-id="c34bf-171">Troubleshoot using the Infolog</span></span>

<span data-ttu-id="c34bf-172">Koska käytetään eräkehystä, aaltojen käsittelyssä esiintyvät virheet siepataan erätöiden infolokien osana.</span><span class="sxs-lookup"><span data-stu-id="c34bf-172">Because the batch framework is used, errors that occur during wave processing will be captured as part of the batch jobs Infologs.</span></span> <span data-ttu-id="c34bf-173">Voit lukea aaltoon liittyvät erätyöt seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="c34bf-173">To read the batch jobs related to a wave:</span></span>

1. <span data-ttu-id="c34bf-174">Valitse **Varastonhallinta \> Lähtevät aallot \> Lähetysaallot \> Kaikki aallot**.</span><span class="sxs-lookup"><span data-stu-id="c34bf-174">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="c34bf-175">Valitse tarkastettava aalto.</span><span class="sxs-lookup"><span data-stu-id="c34bf-175">Select the wave you want to inspect.</span></span>
1. <span data-ttu-id="c34bf-176">Avaa toimintoruudussa **Aalto**-välilehti ja valitse **Aalto** -ryhmässä **Erätyöt**.</span><span class="sxs-lookup"><span data-stu-id="c34bf-176">On the Action Pane, open the **Wave** tab and, from the **Wave** group, select **Batch jobs**.</span></span>

<span data-ttu-id="c34bf-177">Aaltojen käsittely itsensä korjaavaa, joten kaikki käsittelyn aikana havainnut virheet on raportoitava infolokin avulla.</span><span class="sxs-lookup"><span data-stu-id="c34bf-177">Wave processing is self-correcting, so any error detected during processing should be reported using the Infolog.</span></span>

<span data-ttu-id="c34bf-178">Rinnakkaiskäsittelyyn liittyvä tyypillinen virhe voi olla se, että kaksi aaltoa yrittää kohdistaa saman nimikkeen samanaikaisesti, eikä yksi niistä ole valmis, jotta toinen ei voi hankkia lukitusta määritettynä aikana.</span><span class="sxs-lookup"><span data-stu-id="c34bf-178">A typical error related to parallel processing could be that two waves try to allocate the same item at the same time and one does not complete so that the other wave is unable to acquire a lock within the specified time.</span></span> <span data-ttu-id="c34bf-179">Jos näin tapahtuu, erätöiden loki sisältää tiedot, joiden mukaan nimikkeen lukitusta ei voitu hankkia. Tällöin epäonnistunut aalto on käsiteltävä uudelleen.</span><span class="sxs-lookup"><span data-stu-id="c34bf-179">If this situation occurs, the batch jobs log will contain information stating that the lock for the item could not be acquired, in which case the wave that failed must be processed again.</span></span>

<span data-ttu-id="c34bf-180">Koska käsittely on rinnakkaista, tiedot on ylläpidettävä eri taulukoissa käsittelyn tilan seuraamista varten.</span><span class="sxs-lookup"><span data-stu-id="c34bf-180">Because the processing is happening in parallel, data must be maintained in different tables to track the state of the processing.</span></span> <span data-ttu-id="c34bf-181">Tämä tarkoittaa, että erätöiden lokit voivat sisältää virheitä, kuten avainten kaksoiskappaleiden virheitä.</span><span class="sxs-lookup"><span data-stu-id="c34bf-181">This means that the logs for the batch jobs might contain errors such as duplicate key errors.</span></span>

<span data-ttu-id="c34bf-182">Erätehtävien virheet kuuluvat myös erätöiden lokiin.</span><span class="sxs-lookup"><span data-stu-id="c34bf-182">The errors from the batch tasks are also part of the batch jobs log.</span></span> <span data-ttu-id="c34bf-183">Tärkeimmät tiedot ovat yleensä alaosassa.</span><span class="sxs-lookup"><span data-stu-id="c34bf-183">The most important information is typically at the bottom.</span></span>

<span data-ttu-id="c34bf-184">Muutamista harvinaisissa tapauksissa, jos esimerkiksi SQL-yhteys päätettiin, voidaan aallon käsittely lopettaa epäyhtenäisessä tilassa, jossa erätyö näyttää olevan käynnissä, mutta käsittely on pysäytetty.</span><span class="sxs-lookup"><span data-stu-id="c34bf-184">In rare cases, for example if the SQL connection ended, it is possible for the wave processing to end in an inconsistent state where the batch job appears to be running but the processing is stopped.</span></span> <span data-ttu-id="c34bf-185">Aalto ei voi käsitellä tällaisia virheitä, joten epäonnistuneita aaltoja yritetään puhdistaa, kun seuraava aalto suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="c34bf-185">The wave can't handle errors like this, so an attempt to clean up failed waves is done when the next wave runs.</span></span> <span data-ttu-id="c34bf-186">Voit myös tehdä seuraavat toimet, jos nykyinen aalto on epäyhtenäisessä tilassa:</span><span class="sxs-lookup"><span data-stu-id="c34bf-186">Alternatively, if the current wave is in an inconsistent state, perform the following steps:</span></span>

1. <span data-ttu-id="c34bf-187">Valitse **Varastonhallinta \> Lähtevät aallot \> Lähetysaallot \> Kaikki aallot**.</span><span class="sxs-lookup"><span data-stu-id="c34bf-187">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="c34bf-188">Valitse aalto, jonka haluat siivota.</span><span class="sxs-lookup"><span data-stu-id="c34bf-188">Select the wave you need to clean up.</span></span>
1. <span data-ttu-id="c34bf-189">Avaa toimintoruudussa **Aalto**-välilehti ja valitse **Aalto** -ryhmässä **Tyhjennä aallon tiedot**.</span><span class="sxs-lookup"><span data-stu-id="c34bf-189">On the Action Pane, open the **Wave** tab and, in the **Wave** group, select **Cleanup wave data**.</span></span>

### <a name="troubleshoot-using-the-wave-progress-log"></a><span data-ttu-id="c34bf-190">Vianmääritys aallon etenemislokin avulla</span><span class="sxs-lookup"><span data-stu-id="c34bf-190">Troubleshoot using the wave progress log</span></span>

<span data-ttu-id="c34bf-191">Jos **Varastonhallinnan parametrit** -sivulla on otettu käyttöön **Luo aallon etenemisloki** -asetus, lokitietue luodaan aina, kun nimikkeen ja sen dimensioiden aikakohdistukset alkavat ja päättyvät.</span><span class="sxs-lookup"><span data-stu-id="c34bf-191">If the **Create wave progress log** option is enabled on the **Warehouse management parameters** page, then a log record is created every time allocation for an item and its dimensions begins and ends.</span></span> <span data-ttu-id="c34bf-192">Ota tämä loki käyttöön vain silloin, kun tarvitset sitä, esimerkiksi alkutestauksen tai vianmäärityksen aikana.</span><span class="sxs-lookup"><span data-stu-id="c34bf-192">You should only enable this log when you need it, for example, during initial testing or for troubleshooting.</span></span> <span data-ttu-id="c34bf-193">Kun tämä asetus on käytössä, voit tarkastella lokia seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="c34bf-193">When this option is enabled, you can view the log by taking the following steps:</span></span>

1. <span data-ttu-id="c34bf-194">Valitse **Varastonhallinta \> Lähtevät aallot \> Lähetysaallot \> Kaikki aallot**.</span><span class="sxs-lookup"><span data-stu-id="c34bf-194">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="c34bf-195">Valitse tarkastettava aalto.</span><span class="sxs-lookup"><span data-stu-id="c34bf-195">Select the wave you want to inspect.</span></span>
1. <span data-ttu-id="c34bf-196">Valitse toimintoruudun **Aalto**-välilehden **Aalto**-ryhmässä **Edistyminen**.</span><span class="sxs-lookup"><span data-stu-id="c34bf-196">On the Action Pane, open the **Wave** tab and, in the **Wave** group, select **Progress**.</span></span>