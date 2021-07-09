---
title: Pilvi- ja reunapalvelujen Scale Unitien tuotannonohjauksen kuormitukset
description: Tässä aiheessa käsitellään tuotannonohjauksen kuormitusten käyttöä pilvi- ja reunapalvelujen scale unitien kanssa.
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: b1e2006c0d9b9effe331a644aaaa9fa33ff2fb7c
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270532"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a><span data-ttu-id="1aa3d-103">Valmistuksen suorituksen kuormitukset pilven ja reunan asteikon yksiköitä varten</span><span class="sxs-lookup"><span data-stu-id="1aa3d-103">Manufacturing execution workloads for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]

> [!WARNING]
> <span data-ttu-id="1aa3d-104">Tuotannon suorituksen kuormitus on esikatseltavissa tällä hetkellä.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-104">The manufacturing execution workload is available in preview at this point in time.</span></span>
> <span data-ttu-id="1aa3d-105">Joitakin liiketoimintatoimintoja ei tueta kokonaisuudessaan julkisessa esiversiossa, kun kuormituksen scale uniteja käytetään.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-105">Some business functionality isn't fully supported in the public preview when workload scale units are used.</span></span>

<span data-ttu-id="1aa3d-106">Tuotannon suorittamisessa asteikkoyksiköt toimittavat seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="1aa3d-106">In manufacturing execution, scale units deliver the following capabilities:</span></span>

- <span data-ttu-id="1aa3d-107">Koneenkäyttäjät ja työnjohtajat voivat käyttää operatiivista tuotantosuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-107">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="1aa3d-108">Koneenkäyttäjät voivat pitää suunnitelman ajan tasalla suorittamalla erillisen valmistuksen ja prosessivalmistuksen töitä.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-108">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="1aa3d-109">Tuotannoin työnjohtaja voi muokata operatiivista suunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-109">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="1aa3d-110">Työntekijät voivat käyttää reunapalvelujen työajanseurantaa kellokorttina ja varmistaa näin oikean palkanlaskennan.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-110">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="1aa3d-111">Tässä aiheessa käsitellään tuotannonohjauksen kuormitusten käyttöä pilvi- ja reunapalvelujen scale unitien kanssa.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-111">This topic describes how manufacturing execution workloads work with cloud and edge scale units.</span></span>

## <a name="the-manufacturing-lifecycle"></a><span data-ttu-id="1aa3d-112">Valmistuksen elinkaari</span><span class="sxs-lookup"><span data-stu-id="1aa3d-112">The manufacturing lifecycle</span></span>

<span data-ttu-id="1aa3d-113">Valmistuksen elinkaari jaetaan seuraavan kuvan osoittamalla tavalla kolmeen osaan: *suunnittelu*, *toteutus* ja *viimeistely*.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-113">As the following illustration shows, the manufacturing lifecycle is divided into three phases: *Plan*, *Execute*, and *Finalize*.</span></span>

<span data-ttu-id="1aa3d-114">[![Valmistuksen toteutusvaiheet, kun käytössä on yksi ympäristö](media/mes-phases.png "Valmistuksen toteutusvaiheet, kun käytössä on yksi ympäristö")](media/mes-phases-large.png)</span><span class="sxs-lookup"><span data-stu-id="1aa3d-114">[![Manufacturing execution phases when a single environment is used](media/mes-phases.png "Manufacturing execution phases when a single environment is used")](media/mes-phases-large.png)</span></span>

<span data-ttu-id="1aa3d-115">_Suunnittelu_-vaihe sisältää tuotannon määrittelyn, suunnittelun, tilauksen luonnin ja aikatauluttamisen sekä vapautuksen.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-115">The _Plan_ phase includes product definition, planning, order creation and scheduling, and release.</span></span> <span data-ttu-id="1aa3d-116">Vapautusvaihe ilmaisee siirtymisen _Suunnittelu_-vaiheesta _Toteutus_-vaiheeseen.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-116">The release step indicates the transition from the _Plan_ phase to the _Execute_ phase.</span></span> <span data-ttu-id="1aa3d-117">Kun tuotantotilaus vapautetaan, tuotantotilauksen työt tulevat näkyviin tuotannossa ja ovat valmiita toteuttamiseen.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-117">When a production order is released, the production order jobs will be visible on the production floor and ready for execution.</span></span>

<span data-ttu-id="1aa3d-118">Kun tuotantotyö merkitään valmiiksi, se siirtyy _Suorita_-vaiheesta _Viimeistely_-vaiheeseen.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-118">When a production job is marked as completed, it moves from the _Execute_ phase to the _Finalize_ phase.</span></span> <span data-ttu-id="1aa3d-119">_Viimeistely_-vaiheessa *Toteutus*-vaiheet rekisteröinnit siirtyvät hyväksymistyönkulkuun, jossa ne lasketaan, hyväksytään ja siirretään.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-119">In the _Finalize_ phase, the registrations from the *Execute* phase go through an approval workflow, where they are calculated, approved, and transferred.</span></span> <span data-ttu-id="1aa3d-120">Tuotantotilaus on silloin valmis.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-120">At that point, the production order is completed.</span></span> <span data-ttu-id="1aa3d-121">Niinpä työntekijöiden palkkaperuste luodaan.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-121">Therefore, the basis for the workers' pay is generated.</span></span>

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a><span data-ttu-id="1aa3d-122">Toteutusvaiheen jakaminen erillisiksi kuormituksiksi</span><span class="sxs-lookup"><span data-stu-id="1aa3d-122">Splitting the Execute phase into a separate workload</span></span>

<span data-ttu-id="1aa3d-123">Kuten seuraavassa kuvassa osoitetaan, scale uniteja käytettäessä _Toteutus_-vaihe jaetaan erilliseksi kuormitukseksi.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-123">As the following illustration shows, when scale units are used, the _Execute_ phase is split out as a separate workload.</span></span>

<span data-ttu-id="1aa3d-124">[![Valmistuksen toteutusvaiheet scale uniteja käytettäessä](media/mes-phases-workloads.png "Valmistuksen toteutusvaiheet scale uniteja käytettäessä")](media/mes-phases-workloads-large.png)</span><span class="sxs-lookup"><span data-stu-id="1aa3d-124">[![Manufacturing execution phases when scale units are used](media/mes-phases-workloads.png "Manufacturing execution phases when scale units are used")](media/mes-phases-workloads-large.png)</span></span>

<span data-ttu-id="1aa3d-125">Malli siirtyy nyt yhden esiintymän asennuksesta keskukseen ja scale uniteihin perustuvaan mallin.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-125">The model now goes from a single-instance installation to a model that is based on the hub and scale units.</span></span> <span data-ttu-id="1aa3d-126">_Suunnittelu_- ja _Viimeistely_-vaiheet suoritetaan taustatoimintoina keskuksessa ja tuotannonohjauksen kuormitus suoritetaan scale uniteina.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-126">The _Plan_ and _Finalize_ phases run as back-office operations on the hub, and the manufacturing execution workload runs on the scale units.</span></span> <span data-ttu-id="1aa3d-127">Tietoja siirretään asynkronisesti keskuksen ja scale unitien välillä.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-127">Data is transferred asynchronously between the hub and scale units.</span></span>

<span data-ttu-id="1aa3d-128">Kun tuotantotilaus vapautetaan keskukseen, kaikki tuotantotöiden käsittelyyn tarvittavat tiedot siirretään scale unitiin.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-128">When a production order is released on the hub, all data that is required to process production jobs is transferred to the scale unit.</span></span> <span data-ttu-id="1aa3d-129">Näitä tietoja ovat esimerkiksi tuotantotilaukset, tuotannon reititykset, tuoterakenteet ja tuotteet.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-129">This data includes production orders, production routes, bills of materials, and products.</span></span> <span data-ttu-id="1aa3d-130">Myös tiedot, jotka eivät liity tuotantotilaukseen (kuten epäsuorat tehtävät, poissaolokoodit ja tuotannon parametrit), siirretään keskuksesta scale unitiin.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-130">Data that isn't related to a production order (such as indirect activities, absence codes, and production parameters) is also transferred from the hub to the scale unit.</span></span> <span data-ttu-id="1aa3d-131">Pääsääntöisesti tiedot, jotka ovat peräisin keskuksesta ja jotka siirretään scale unitiin, voidaan luoda ja päivittää vain keskuksessa.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-131">As a rule, data that originates from the hub and that is transferred to the scale unit can be created or updated only on the hub.</span></span> <span data-ttu-id="1aa3d-132">Niinpä scale unitissa ei voi luoda uutta poissaolokoodia tai epäsuoraa tehtävää, vaan niitä voidaan käyttää vain rekisteröintiin.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-132">For example, a new absence code or indirect activity can't be created on the scale unit&mdash;they can be used only for registration.</span></span> <span data-ttu-id="1aa3d-133">Toteutuksen aikana scale unitissa tehdyt rekisteröinnit siirretään sitten keskukseen, jossa työajanseurannan hyväksynnän, varaston ja taloushallinnon päivitykset käsitellään.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-133">The registrations that are made on the scale unit during execution are then transferred to the hub, where time and attendance approval, inventory, and financial updates are processed.</span></span>

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a><span data-ttu-id="1aa3d-134">Kuormituksissa suoritettavat tuotannonohjauksen tehtävät</span><span class="sxs-lookup"><span data-stu-id="1aa3d-134">Manufacturing execution tasks that can be run on workloads</span></span>

<span data-ttu-id="1aa3d-135">Seuraavat tuotannonohjauksen tehtävät voidaan tällä hetkellä suorittaa kuormituksissa scale uniteja käytettäessä:</span><span class="sxs-lookup"><span data-stu-id="1aa3d-135">The following manufacturing execution tasks can currently be run on workloads when scale units are used:</span></span>

- <span data-ttu-id="1aa3d-136">Saapuminen, kirjautuminen, poistuminen ja poissaolo</span><span class="sxs-lookup"><span data-stu-id="1aa3d-136">Clock-in, log-in, clock-out, and absence</span></span>
- <span data-ttu-id="1aa3d-137">Aloita työ</span><span class="sxs-lookup"><span data-stu-id="1aa3d-137">Start job</span></span>
- <span data-ttu-id="1aa3d-138">Töiden niputtaminen</span><span class="sxs-lookup"><span data-stu-id="1aa3d-138">Bundle jobs</span></span>
- <span data-ttu-id="1aa3d-139">Raportointi on meneillään</span><span class="sxs-lookup"><span data-stu-id="1aa3d-139">Report progress</span></span>
- <span data-ttu-id="1aa3d-140">Ilmoita hävikki</span><span class="sxs-lookup"><span data-stu-id="1aa3d-140">Report scrap</span></span>
- <span data-ttu-id="1aa3d-141">Epäsuora tehtävä</span><span class="sxs-lookup"><span data-stu-id="1aa3d-141">Indirect activity</span></span>
- <span data-ttu-id="1aa3d-142">Tauko</span><span class="sxs-lookup"><span data-stu-id="1aa3d-142">Break</span></span>
- <span data-ttu-id="1aa3d-143">Ilmoita valmiiksi ja hyllytettäväksi (vaatii, että suoritat myös Scale Unitin varaston suorituksen kuormituksen, katso myös kohta [Ilmoita valmiiksi ja hyllytettäväksi Scale Unitille](#RAF))</span><span class="sxs-lookup"><span data-stu-id="1aa3d-143">Report as finished and putaway (requires that you also run the warehouse execution workload on your scale unit, see also [Report as finished and putaway on a scale unit](#RAF))</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a><span data-ttu-id="1aa3d-144">Tuotannonohjauksen kuormitusten käyttäminen keskuksessa</span><span class="sxs-lookup"><span data-stu-id="1aa3d-144">Working with manufacturing execution workloads on the hub</span></span>

<span data-ttu-id="1aa3d-145">Yleensä prosessit, joita tarvitaan tuotannonohjauksen kuormitusten suorittamiseen, suoritetaan automaattisesti, jotta keskus ja kaikki scale unitit pysyvät tarvittaessa synkronoituina.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-145">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="1aa3d-146">Ongelmatilanteessa voidaan kuitenkin käynnistää manuaalisesti kuormituksista vastaanotettavien lähtötietojen rekisteröintien käsitteleminen ja/tai rekisteröinnin käsittelylokin tarkistaminen.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-146">However, if you're having trouble, you can manually trigger the processing of raw registrations that are received from workloads and/or check the registration processing log.</span></span>

### <a name="manually-process-raw-registrations"></a><span data-ttu-id="1aa3d-147">Lähtötietojen rekisteröintien manuaalinen käsittely</span><span class="sxs-lookup"><span data-stu-id="1aa3d-147">Manually process raw registrations</span></span>

<span data-ttu-id="1aa3d-148">Supply Chain Managementin erätyö suoritetaan automaattisesti, ja se käsittelee kaikki kuormituksista vastaanotetut rekisteröinnit.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-148">A batch job in Supply Chain Management runs automatically to process all the registrations that have been received from the workloads.</span></span> <span data-ttu-id="1aa3d-149">Tämä työ luo tarvittavat tuotantokirjauskansiot ja lokikirjaviennit, kun kuormituksen valmistuneen työn rekisteröinti käsitellään.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-149">This job creates the required production journals and logbook entries when a registration is processed for a completed job on the workload.</span></span>

<span data-ttu-id="1aa3d-150">Vaikka työ suoritetaan yleensä automaattisesti, se voidaan suorittaa manuaalisesti koska tahansa kirjautumalla keskukseen ja valitsemalla **Tuotannonhallinta \> Kausittaiset tehtävät \> Taustatoimintojen kuormituksen hallinta \> Lähdetietojen rekisteröintien käsittely**.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-150">Although the job usually runs automatically, you can run it manually at any time by signing in to the hub and going to **Production control \> Periodic tasks \> Backoffice workload management \> Process raw registrations**.</span></span>

### <a name="check-the-raw-registration-processing-log"></a><span data-ttu-id="1aa3d-151">Lähdetietojen rekisteröinnin käsittelylokin tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="1aa3d-151">Check the raw registration processing log</span></span>

<span data-ttu-id="1aa3d-152">Rekisteröinnin käsittelylokia voi tarkastella kirjautumalla keskukseen ja valitsemalla **Tuotannonhallinta \> Kausittaiset tehtävät \> Taustatoimintojen kuormituksen hallinta \> Lähdetietojen rekisteröinnin käsittelyloki**.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-152">To review the registration processing log, sign in to the hub, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Raw registration processing log**.</span></span> <span data-ttu-id="1aa3d-153">**Lähdetietojen rekisteröinnin käsittelyloki** -sivulla on luettelo käsitellyistä lähdetietojen rekisteröinneistä ja kunkin rekisteröinnin tila.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-153">The **Raw registration processing log** page shows a list of processed raw registrations and the status of each registration.</span></span>

<span data-ttu-id="1aa3d-154">![Lähdetietojen rekisteröinnin käsittelyloki -sivu](media/mes-processing-log.png "Lähdetietojen rekisteröinnin käsittelyloki -sivu")</span><span class="sxs-lookup"><span data-stu-id="1aa3d-154">![Raw registration processing log page](media/mes-processing-log.png "Raw registration processing log page")</span></span>

<span data-ttu-id="1aa3d-155">Luettelossa olevaa rekisteröintiä voi käsitellä valitsemalla ensin se ja sitten jompikumpi seuraavista painikkeista toimintoruudussa:</span><span class="sxs-lookup"><span data-stu-id="1aa3d-155">You can work on any registration in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="1aa3d-156">**Käsittele** – Valittu rekisteröinti käsitellään manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-156">**Process** – Manually process the selected registration.</span></span> <span data-ttu-id="1aa3d-157">Tämä toiminto voi olla kätevä, jos _Lähdetietojen rekisteröintien käsittely_ -työtä ei ole suoritettu tai se epäonnistui.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-157">This action can be useful if the _Process raw registrations_ job hasn't run, or if it failed.</span></span>
- <span data-ttu-id="1aa3d-158">**Peruuta** – valitun rekisteröinnin peruuttaminen.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-158">**Cancel** – Cancel the selected registration.</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a><span data-ttu-id="1aa3d-159">Tuotannonohjauksen kuormitusten käyttäminen scale unitissa</span><span class="sxs-lookup"><span data-stu-id="1aa3d-159">Working with manufacturing execution workloads on a scale unit</span></span>

<span data-ttu-id="1aa3d-160">Yleensä prosessit, joita tarvitaan tuotannonohjauksen kuormitusten suorittamiseen, suoritetaan automaattisesti, jotta keskus ja kaikki scale unitit pysyvät tarvittaessa synkronoituina.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-160">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="1aa3d-161">Ongelmatilanteessa scale unitissa käsiteltyjen tilausten historia voidaan kuitenkin tarkistaa tai _Tuotannon keskuksesta scale unitiin viestikäsittely_ -työ voidaan suorittaa manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-161">However, if you're having trouble, you can check the history of orders that have been processed on a scale unit or manually run the _Manufacturing hub to scale unit message processor_ job.</span></span>

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a><span data-ttu-id="1aa3d-162">Scale unitissa käsiteltyjen valmistustöiden historian näyttäminen</span><span class="sxs-lookup"><span data-stu-id="1aa3d-162">View the history of manufacturing jobs that have been processed on a scale unit</span></span>

<span data-ttu-id="1aa3d-163">Scale unitissa käsiteltyjen valmistustöiden historiaa voi tarkastella kirjautumalla scale unit -koneeseen ja valitsemalla **Tuotannon hallinta \> Kausittaiset tehtävät \> Taustatoimintojen kuormituksen hallinta \> Valmistustöiden käsittelyhistoria**.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-163">To review the history of manufacturing jobs that have been processed on a scale unit, sign in to the scale unit machine, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing jobs processing history**.</span></span> <span data-ttu-id="1aa3d-164">**Valmistustöiden käsittelyhistoria** -sivulla on tuotantotilausten käsittelyhistoria scale unitissa.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-164">The **Manufacturing jobs processing history** page shows the processing history of the production orders on the scale unit.</span></span> <span data-ttu-id="1aa3d-165">Luettelossa olevaa tuotantotilausta voi käsitellä valitsemalla ensin se ja sitten jompikumpi seuraavista painikkeista toimintoruudussa:</span><span class="sxs-lookup"><span data-stu-id="1aa3d-165">You can work on any production order in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="1aa3d-166">**Käsittele** – valittu tuotantotilaus käsitellään manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-166">**Process** – Manually process the selected production order.</span></span>
- <span data-ttu-id="1aa3d-167">**Peruuta** – valittu tuotantotilaus peruutetaan.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-167">**Cancel** – Cancel the selected production order.</span></span>

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a><span data-ttu-id="1aa3d-168">Tuotannon keskuksesta scale unitiin viestikäsittely -työ</span><span class="sxs-lookup"><span data-stu-id="1aa3d-168">Manufacturing hub to scale unit message processor job</span></span>

<span data-ttu-id="1aa3d-169">_Tuotannon keskuksesta scale unitiin viestikäsittely_ -työ käsittelee tiedot keskuksesta scale unitiin.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-169">The _Manufacturing hub to scale unit message processor_ job processes data from the hub to the scale unit.</span></span> <span data-ttu-id="1aa3d-170">Tämä työ käynnistyy automaattisesti, kun tuotannonohjauksen kuormitus otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-170">This job is automatically started when the manufacturing execution workload is deployed.</span></span> <span data-ttu-id="1aa3d-171">Se voidaan kuitenkin suorittaa myös manuaalisesti koska tahansa valitsemalla **Tuotannonhallinta \> Kausittaiset tehtävät \> Taustatoimintojen kuormituksen hallinta \> Tuotannon keskuksesta scale unitiin viestikäsittely**.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-171">However, you can run it manually at any time by going to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing hub to scale unit message processor**.</span></span>

<a name="RAF"></a>

## <a name="report-as-finished-and-putaway-on-a-scale-unit"></a><span data-ttu-id="1aa3d-172">Ilmoita valmiiksi ja hyllytettäväksi Scale Unitille</span><span class="sxs-lookup"><span data-stu-id="1aa3d-172">Report as finished and putaway on a scale unit</span></span>

<!-- KFM: 
This section describes how to enable the abilities to report as finished and then putaway finished items when you are using to a scale unit.

### Enable and use report as finished and putaway on a scale unit -->

<span data-ttu-id="1aa3d-173">Nykyisessä versiossa [varaston suorittamisen kuormitus](cloud-edge-workload-warehousing.md) tukee ilmoittamista valmiiksi ja hyllytettäviksi (valmiit tuotteet, rinnakkaistuotteet ja sivutuotteet) (ei valmistuksen suorituksen kuormitus).</span><span class="sxs-lookup"><span data-stu-id="1aa3d-173">In the current release, report as finished and putaway operations (for finished products, co-products, and by-products) are supported by the [warehouse execution workload](cloud-edge-workload-warehousing.md) (not the manufacturing execution workload).</span></span> <span data-ttu-id="1aa3d-174">Jos siis haluat käyttää tätä toimintoa Scale Unitin yhteydessä, toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="1aa3d-174">Therefore, to use this functionality when connected to a scale unit, you must do the following:</span></span>

- <span data-ttu-id="1aa3d-175">Asenna Scale Unitiin sekä varaston suorituksen kuormitus että valmistuksen suorittamisen kuormitus.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-175">Install both the warehouse execution workload and the manufacturing execution workload on your scale unit.</span></span>
- <span data-ttu-id="1aa3d-176">Warehouse Management -mobiilisovelluksen avulla voit ilmoittaa töitä valmiiksi ja hyllytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-176">Use the Warehouse Management mobile app to report as finished and process the putaway work.</span></span> <span data-ttu-id="1aa3d-177">Tuotannon käyttöliittymä ei tällä hetkellä tue näitä prosesseja.</span><span class="sxs-lookup"><span data-stu-id="1aa3d-177">The production floor execution interface does not currently support these processes.</span></span>

<!-- KFM: API details needed

### Customize report as finished and putaway functionality

 -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
