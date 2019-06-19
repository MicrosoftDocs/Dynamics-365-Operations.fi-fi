---
title: Sähköisen raportoinnin muodon suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi
description: Tässä ohjeaiheessa on tietoja suorituskykyongelmien vianmäärityksestä sähköisen raportoinnin (ER) suorituskyvyn jäljitystoiminnon avulla.
author: NickSelin
manager: AnnBe
ms.date: 05/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: aa71db2752889bc905c22bab1cf2fa46d7ee07c7
ms.sourcegitcommit: 67d00b95952faf0db580d341249d4e50be59119c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1576543"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="ca57c-103">Sähköisen raportoinnin muotojen suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi</span><span class="sxs-lookup"><span data-stu-id="ca57c-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ca57c-104">Osana sähköisten raportointikonfiguraatioiden suunnittelua sähköisten asiakirjojen luomista varten määritetään menetelmä, jonka avulla tiedot haetaan Microsoft Dynamics 365 for Finance and Operationsista ja syötetään tuotavaan tuotokseen.</span><span class="sxs-lookup"><span data-stu-id="ca57c-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of Microsoft Dynamics 365 for Finance and Operations and enter it in the output that is generated.</span></span> <span data-ttu-id="ca57c-105">ER Performance Trace -toiminto auttaa vähentämään huomattavasti aikaa ja kustannuksia, jotka liittyvät ER-muodon suorituksen yksityiskohtien keräämiseen ja niiden käyttämiseen suorituskykyongelmien vianmäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="ca57c-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="ca57c-106">Tässä opetusohjelmassa on ohjeita siitä, miten suorituskykyä voidaan seurata suoritettavissa ER-muodoissa Finance and Operationsin yhteydessä ja miten suorituskykyä voidaan parantaa näiden jälkien tietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="ca57c-106">This tutorial provides guidelines about how to take performance traces for executed ER formats in Finance and Operations, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ca57c-107">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="ca57c-107">Prerequisites</span></span>

<span data-ttu-id="ca57c-108">Tämän opetusohjelman esimerkkien suorittaminen edellyttää seuraavia käyttöoikeuksia:</span><span class="sxs-lookup"><span data-stu-id="ca57c-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="ca57c-109">Finance and Operations -käyttöoikeudet seuraaville rooleille:</span><span class="sxs-lookup"><span data-stu-id="ca57c-109">Access to Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="ca57c-110">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="ca57c-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="ca57c-111">Sähköisen raportoinnin toiminnallinen konsultti</span><span class="sxs-lookup"><span data-stu-id="ca57c-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="ca57c-112">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="ca57c-112">System administrator</span></span>

- <span data-ttu-id="ca57c-113">Voit käyttää järjestelmän (RCS) esiintymää, joka on valmisteltu samalle vuokralaiselle kuin Finance and Operations jostakin seuraavista rooleista:</span><span class="sxs-lookup"><span data-stu-id="ca57c-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance and Operations, for one of the following roles:</span></span>

    - <span data-ttu-id="ca57c-114">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="ca57c-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="ca57c-115">Sähköisen raportoinnin toiminnallinen konsultti</span><span class="sxs-lookup"><span data-stu-id="ca57c-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="ca57c-116">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="ca57c-116">System administrator</span></span>

<span data-ttu-id="ca57c-117">Seuraavat tiedostot täytyy myös ladata ja tallentaa paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="ca57c-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="ca57c-118">Tiedosto</span><span class="sxs-lookup"><span data-stu-id="ca57c-118">File</span></span>                                  | <span data-ttu-id="ca57c-119">Sisältö</span><span class="sxs-lookup"><span data-stu-id="ca57c-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="ca57c-120">Suorituskyvyn jäljitysmalli.versio.1</span><span class="sxs-lookup"><span data-stu-id="ca57c-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="ca57c-121">Esimerkin ER-tietomallin konfigurointi</span><span class="sxs-lookup"><span data-stu-id="ca57c-121">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| <span data-ttu-id="ca57c-122">Suorituskyvyn jäljitysmetadata.versio.1</span><span class="sxs-lookup"><span data-stu-id="ca57c-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="ca57c-123">Esimerkin ER-metadatan konfigurointi</span><span class="sxs-lookup"><span data-stu-id="ca57c-123">Sample ER metadata configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| <span data-ttu-id="ca57c-124">Suorituskyvyn jäljitysmapping.versio.1</span><span class="sxs-lookup"><span data-stu-id="ca57c-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="ca57c-125">Esimerkin ER-mallikartoituksen konfigurointi</span><span class="sxs-lookup"><span data-stu-id="ca57c-125">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="ca57c-126">Suorituskyvyn jäljitysformat.versio.1</span><span class="sxs-lookup"><span data-stu-id="ca57c-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="ca57c-127">Esimerkin ER-format-konfigurointi</span><span class="sxs-lookup"><span data-stu-id="ca57c-127">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="ca57c-128">Konfiguroi ER-parametrit</span><span class="sxs-lookup"><span data-stu-id="ca57c-128">Configure ER parameters</span></span>

<span data-ttu-id="ca57c-129">Kukin Finance and Operationsin suorituskyvyn jäljitys tallennetaan suorituslokitietueen liitteenä.</span><span class="sxs-lookup"><span data-stu-id="ca57c-129">Each ER performance trace that is generated in Finance and Operations is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="ca57c-130">Näiden liitteiden hallinnassa käytetään Finance and Operationsin tiedostohallinnan (DM) kehystä.</span><span class="sxs-lookup"><span data-stu-id="ca57c-130">The Document management (DM) framework of Finance and Operations is used to manage these attachments.</span></span> <span data-ttu-id="ca57c-131">Sinun on määritettävä ER-parametrit etukäteen ja määritettävä DM-tiedosto tyyppi, jota käytetään suorituskykyjälkien liittämiseen.</span><span class="sxs-lookup"><span data-stu-id="ca57c-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="ca57c-132">Valitse Finance and Operationissa **Sähköisen raportoinnin** työtilassa **Sähköisen raportoinnin parametrit**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-132">In Finance and Operation, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="ca57c-133">Valitse sitten **Sähköisen raportoinnin parametrit** -sivun **Liitteet**-välilehden **Muut**-kentästä suorituskyvyn jäljille käytettävä DM-tiedostotyyppi.</span><span class="sxs-lookup"><span data-stu-id="ca57c-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Sähköisen raportoinnin parametrisivu Finance and Operationsissa](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="ca57c-135">Jos haluat olla käytettävissä **Muut** -hakukentässä, DM-tiedostotyyppi on konfiguroitava seuraavalla tavalla **Asiakirjatyypit**-sivulla (**Organisaation hallinta \> Asiakirjan hallinta \> Asiakirjatyypit**):</span><span class="sxs-lookup"><span data-stu-id="ca57c-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="ca57c-136">**Luokka:** Liitä tiedosto</span><span class="sxs-lookup"><span data-stu-id="ca57c-136">**Class:** Attach file</span></span>
- <span data-ttu-id="ca57c-137">**Ryhmä:** Tiedosto</span><span class="sxs-lookup"><span data-stu-id="ca57c-137">**Group:** File</span></span>

![Finance and Operations -tiedostotyypit-sivu](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="ca57c-139">Valitun tiedostotyypin on oltava käytettävissä kaikissa nykyisen Finance and Operations -esiintymän yrityksissä, koska DM-liitteet ovat yrityskohtaisia.</span><span class="sxs-lookup"><span data-stu-id="ca57c-139">The selected document type must be available in every company of the current Finance and Operations instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="ca57c-140">Konfiguroi RCS-parametrit</span><span class="sxs-lookup"><span data-stu-id="ca57c-140">Configure RCS parameters</span></span>

<span data-ttu-id="ca57c-141">Finance and Operationsissa luodut ER-suorituskykyjäljet tuodaan RCS-määritykseen analysointia varten käyttämällä ER Format Designeria ja ER Mapping Designeria.</span><span class="sxs-lookup"><span data-stu-id="ca57c-141">ER performance traces that are generated in Finance and Operations will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="ca57c-142">Koska ER-suorituskykyjäljet tallennetaan ER-muotoon liittyvän suorituslokitietueen liitteinä, RCS-parametrit on määritettävä etukäteen, jotta voidaan määrittää DM-tiedostotyyppi, jota käytetään suorituskykyjälkien liittämiseen.</span><span class="sxs-lookup"><span data-stu-id="ca57c-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="ca57c-143">Valitse yrityksellesi määritetyn RCS-esiintymän **Sähköisen raportoinnin** -työtilassa **Sähköiset raportointiparametrit**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="ca57c-144">Valitse sitten **Sähköisen raportoinnin parametrit** -sivun **Liitteet**-välilehden **Muut**-kentästä suorituskyvyn jäljille käytettävä DM-tiedostotyyppi.</span><span class="sxs-lookup"><span data-stu-id="ca57c-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Sähköisen raportoinnin parametrit -sivu RCS:ssä](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="ca57c-146">Jos haluat olla käytettävissä **Muut** -hakukentässä, DM-tiedostotyyppi on konfiguroitava seuraavalla tavalla **Asiakirjatyypit**-sivulla (**Organisaation hallinta \> Asiakirjan hallinta \> Asiakirjatyypit**):</span><span class="sxs-lookup"><span data-stu-id="ca57c-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="ca57c-147">**Luokka:** Liitä tiedosto</span><span class="sxs-lookup"><span data-stu-id="ca57c-147">**Class:** Attach file</span></span>
- <span data-ttu-id="ca57c-148">**Ryhmä:** Tiedosto</span><span class="sxs-lookup"><span data-stu-id="ca57c-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="ca57c-149">Suunnittele ER-ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ca57c-149">Design an ER solution</span></span>

<span data-ttu-id="ca57c-150">Oletetaan, että olet aloittanut uuden ER-ratkaisun suunnittelun, joka luo toimittajatapahtumia esittelevän uuden raportin.</span><span class="sxs-lookup"><span data-stu-id="ca57c-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="ca57c-151">Tällä hetkellä voit etsiä valitun toimittajan tapahtumat **Toimittajatapahtumat**-sivulta (Siirry **Ostoreskontra \> Toimittajat \> Kaikki toimittajat**, valitse toimittaja ja sitten toimintoruudun **Toimittaja**-välilehti kohdassa valitse **Tapahtumat**-ryhmästä **Tapahtumat**).</span><span class="sxs-lookup"><span data-stu-id="ca57c-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="ca57c-152">Haluat kuitenkin saada kaikki toimittajatapahtumat samaan aikaan yhdessä sähköisessä asiakirjassa XML-muodossa.</span><span class="sxs-lookup"><span data-stu-id="ca57c-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="ca57c-153">Tämä ratkaisu koostuu useista ER-konfiguraatioista, jotka sisältävät vaaditun tietomallin, metatiedot, mallien yhdistämismääritykset ja muotokomponentit.</span><span class="sxs-lookup"><span data-stu-id="ca57c-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="ca57c-154">Kirjaudu yrityksen RCS-esiintymään, joka on valmisteltu yrityksellesi.</span><span class="sxs-lookup"><span data-stu-id="ca57c-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="ca57c-155">Tässä opetusohjelmassa luodaan ja muokataan konfiguraatioita malliyritykselle **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="ca57c-156">Varmista siksi, että tämä konfigurointipalvelu on lisätty RCS-järjestelmään ja valittu aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="ca57c-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="ca57c-157">Lisätietoja on kohdassa [Luo konfigurointipalvelut ja merkitse ne aktiivisiksi](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) menettelyiksi.</span><span class="sxs-lookup"><span data-stu-id="ca57c-157">For instructions, see the [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) procedure.</span></span>
3. <span data-ttu-id="ca57c-158">Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="ca57c-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="ca57c-159">Tuo **Konfiguraatiot** -sivulla lataamasi ER-kokoonpanot RCS-edellytyksenä seuraavassa järjestyksessä: tietomalli, metatiedot, mallikartoitus, muoto.</span><span class="sxs-lookup"><span data-stu-id="ca57c-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="ca57c-160">Luo kukin mukautus seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="ca57c-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="ca57c-161">Valitse toimintoruudusta **Vaihda \> Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="ca57c-162">Valitse haluamasi ER-kokoonpanon tiedosto XML-muodossa valitsemalla **Selaa**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="ca57c-163">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-163">Select **OK**.</span></span>

    ![Konfiguroinnit-sivu RCS:ssä](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="ca57c-165">ER-ratkaisun suorittaminen jäljityksen suorittamista varten</span><span class="sxs-lookup"><span data-stu-id="ca57c-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="ca57c-166">Oletetaan, että olet suunnitellut ER-ratkaisun ensimmäisen version.</span><span class="sxs-lookup"><span data-stu-id="ca57c-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="ca57c-167">Haluat nyt testata sen Finance and Operations -esiintymässä ja analysoida suorituskykyä.</span><span class="sxs-lookup"><span data-stu-id="ca57c-167">You now want to test it in your Finance and Operations instance and analyze execution performance.</span></span>

### <a id='import-configuration'></a><span data-ttu-id="ca57c-168">ER-konfiguraation tuominen RCI:sta Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="ca57c-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="ca57c-169">Kirjaudu omaan Finance and Operations -esiintymään.</span><span class="sxs-lookup"><span data-stu-id="ca57c-169">Sign in to your Finance and Operations instance.</span></span>
2. <span data-ttu-id="ca57c-170">Tämän opetusohjelman avulla voit tuoda konfiguraatiot RCS-esiintymästä (jossa suunnittelet ER-komponentteja) Finance and Operations -esiintymään (jossa testaat ja lopulta käytät niitä).</span><span class="sxs-lookup"><span data-stu-id="ca57c-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your Finance and Operations instance (where you test and finally use them).</span></span> <span data-ttu-id="ca57c-171">Siksi on varmistettava, että kaikki vaaditut tiedot on valmisteltu.</span><span class="sxs-lookup"><span data-stu-id="ca57c-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="ca57c-172">Ohjeita on kohdassa [Sähköisen raportoinnin konfiguraatioiden tuonti Regulatory Configuration Services (RCS) -palvelusta](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations).</span><span class="sxs-lookup"><span data-stu-id="ca57c-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations) procedure.</span></span>
3. <span data-ttu-id="ca57c-173">Seuraavien vaiheiden mukaisesti voit tuoda konfiguraatiot RCS-asetuksista Finance and Operationsiin:</span><span class="sxs-lookup"><span data-stu-id="ca57c-173">Follow these steps to import the configurations from RCS into Finance and Operations:</span></span>

    1. <span data-ttu-id="ca57c-174">Valitse **Sähköisen raportoinnin** työtilassa**Litware, Inc**-määrityspalveluruudussa **Arkistot**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="ca57c-175">Valitse **Konfiguraatiosäilö**-sivun ruudukossa oleva säilö, jonka tyyppi on **RCS** ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="ca57c-176">Valitse **Konfiguraatiot**-pikavälilehdessä **Suorituskyvyn jäljitysmuodon** konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="ca57c-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="ca57c-177">Valitse **Versiot**-pikavälilehdellä valitun konfiguraation versio **1.1** ja valitse sitten **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![Konfigurointivaraston sivu Finance and Operationsissa](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="ca57c-179">Tietomallin ja mallin yhdistämismääritysten vastaavat versiot tuodaan automaattisesti valmiiksi tuodun ER-muodon konfiguroinnin edellytyksinä.</span><span class="sxs-lookup"><span data-stu-id="ca57c-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="ca57c-180">ER-suorituskykyjäljityksen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="ca57c-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="ca57c-181">Valitse Finance and Operationsissa **Organisaation hallinto \> Sähköinen raportointi \> Määritykset**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-181">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="ca57c-182">Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="ca57c-183">Toimi **Käyttäjäparametrit**-valintaikkunan **Suorituksen jäljitys** -osassa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="ca57c-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="ca57c-184">Valitse **Suorituksen jäljitys muoto** -kentässä **Korjaa jäljitystiedosto** -kentässä, joka alkaa keräämään tietoja ER-muodon suorittamisesta.</span><span class="sxs-lookup"><span data-stu-id="ca57c-184">In the **Execution trace format** field, select **Debug trace format** to start to collect the details of ER format execution.</span></span> <span data-ttu-id="ca57c-185">Kun tämä arvo valitaan, suorituskyvyn jäljitys kerää seuraaviin toimiin kuluvaa aikaa koskevia tietoja:</span><span class="sxs-lookup"><span data-stu-id="ca57c-185">When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</span></span>

        - <span data-ttu-id="ca57c-186">Kunkin tietolähteen suorittamista mallikartoituksista, joita kutsutaan tietojen hakemiseksi</span><span class="sxs-lookup"><span data-stu-id="ca57c-186">Running each data source in the model mapping that is called to get data</span></span>
        - <span data-ttu-id="ca57c-187">Kunkin muotoilunimikkeen käsitteleminen siten, että se syöttää tietoja luotavalle tulosteelle</span><span class="sxs-lookup"><span data-stu-id="ca57c-187">Processing each format item to enter data in the output that is generated</span></span>

        <span data-ttu-id="ca57c-188">**Suorituksen jäljitysmuoto** -kentän avulla voit määrittää sen luodun suorituskykyjäljityksen muodon, johon suoritustiedot tallennetaan ER-ja Mapping-elementeissä.</span><span class="sxs-lookup"><span data-stu-id="ca57c-188">You use the **Execution trace format** field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</span></span> <span data-ttu-id="ca57c-189">Kun valitset arvoksi **Virheen korjauksen jäljitysmuodon**, pystyt analysoimaan jäljityksen sisältöä ER Operation Designerissa ja näkemään ER-muodon tai määrityselementit, jotka mainitaan jäljityksessä.</span><span class="sxs-lookup"><span data-stu-id="ca57c-189">By selecting **Debug trace format** as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</span></span>

    2. <span data-ttu-id="ca57c-190">Määritä seuraavat asetukset: **Kyllä**, jos haluat kerätä tarkempia tietoja ER-mallin kartoituksesta ja ER-muotokomponenttien suorittamisesta.</span><span class="sxs-lookup"><span data-stu-id="ca57c-190">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="ca57c-191">**Kyselyn tilastotietojen kerääminen** – Kun tämä vaihtoehto on käytössä, suorituskyvyn jäljitys kerää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="ca57c-191">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="ca57c-192">Tietolähteiden tekemien kutsujen määrä</span><span class="sxs-lookup"><span data-stu-id="ca57c-192">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="ca57c-193">Tietokantaan lisättyjen toistettujen kutsujen määrä</span><span class="sxs-lookup"><span data-stu-id="ca57c-193">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="ca57c-194">Tietokantakutsujen tekemiseen käytettävien SQL-lauseiden tiedot</span><span class="sxs-lookup"><span data-stu-id="ca57c-194">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="ca57c-195">**Jäljitysvälimuistin käyttäminen** – Kun tämä asetus on käytössä, suorituskyvyn jäljitys kerää tietoja ER-mallikartoituksen välimuistin käytöstä.</span><span class="sxs-lookup"><span data-stu-id="ca57c-195">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="ca57c-196">**Jäljitystietojen käyttö** – Kun tämä asetus on käytössä, suorituskyvyn jäljitys kerää tietoja siitä, kuinka monta käyntiä tietokantaan on tehty tietueluettelotyypin suoritettavissa tietolähteissä.</span><span class="sxs-lookup"><span data-stu-id="ca57c-196">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="ca57c-197">**Jäljitystietojen luettelointi** – Kun tämä asetus on käytössä, suorituskyvyn jäljitys kerää tietoja siitä, kuinka monta käyntiä tietokantaan on tehty tietueluettelotyypin suoritettavissa tietolähteissä.</span><span class="sxs-lookup"><span data-stu-id="ca57c-197">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ca57c-198">**Käyttäjäparametrit** -valintaikkunan parametrit koskevat käyttäjää ja nykyistä yritystä.</span><span class="sxs-lookup"><span data-stu-id="ca57c-198">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![Käyttäjäparametrit-valintaikkuna Finance and Operationsissa](./media/GER-PerfTrace-GER-UserParameters.png)

### <a id='run-format'></a><span data-ttu-id="ca57c-200">Suorita ER-muoto</span><span class="sxs-lookup"><span data-stu-id="ca57c-200">Run the ER format</span></span>

1. <span data-ttu-id="ca57c-201">Valitse **DEMF**-yritys Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="ca57c-201">In Finance and Operations, select the **DEMF** company.</span></span>
2. <span data-ttu-id="ca57c-202">Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-202">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="ca57c-203">Valitse **Konfiguraatiot**-sivulla konfiguraatiopuussa **Suorituskyvyn jäljitysmuodon** nimike.</span><span class="sxs-lookup"><span data-stu-id="ca57c-203">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="ca57c-204">Valitse toimintoruudussa **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-204">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="ca57c-205">Huomaa, että luotu tiedosto sisältää tietoja kuuden toimittajan 265-tapahtumista.</span><span class="sxs-lookup"><span data-stu-id="ca57c-205">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="ca57c-206">Suorituksen jäljityksen tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="ca57c-206">Review the execution trace</span></span>

### <a id='export-trace'></a><span data-ttu-id="ca57c-207">Vie luotu jäljitys Finance and Operationsista</span><span class="sxs-lookup"><span data-stu-id="ca57c-207">Export the generated trace from Finance and Operations</span></span>

<span data-ttu-id="ca57c-208">Suorituskykyjäljet irrotetaan lähde-ER-muodosta, ja ne voidaan sarjoittaa ulkoiseen zip-tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="ca57c-208">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="ca57c-209">Valitse Finance and Operationsissa **Organisaation hallinto \> Sähköinen raportointi \> Määritysten virheenkorjauslokit**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-209">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="ca57c-210">Valitse **Sähköisen raportoinnin ajon lokit** -sivun vasemmanpuoleisen ruudun **Konfiguration nimi** -kentässä **Suorituskyvyn jäljitysmuoto** jos haluat löytää lokitiedostot, jotka on luotu **Suoritus kyvyn jäljitysmuodon** konfiguraatiolle.</span><span class="sxs-lookup"><span data-stu-id="ca57c-210">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="ca57c-211">Valitse **Liitteet**-painikkeen sivun oikeassa yläkulmassa (paperiliitinsymboli) tai paina **Ctrl+Shift+A**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-211">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![Liitteet-painike sähköisen raportoinnin ajon lokit -sivulla Finance and Operationsissa](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="ca57c-213">**Valitse sähköisen raportoinnin ajon lokit** -sivun toimintoruudussa **Avaa**, jos haluat saada suorituskyvyn jäljityksen zip-tiedostona ja tallentaa sen paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="ca57c-213">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![Liitteet sähköisen raportoinnin ajon lokit -sivulla Finance and Operationsissa](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="ca57c-215">Luotu jäljitys viittaa lähde-ER-raporttiin yksilöivän raporttitunnuksen avulla vain **GUID**-muodossa.</span><span class="sxs-lookup"><span data-stu-id="ca57c-215">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="ca57c-216">Muodon versionumerointia ei oteta huomioon.</span><span class="sxs-lookup"><span data-stu-id="ca57c-216">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="ca57c-217">Huomaa, että suoritetun ER-muodon ja ER-mallikartoituksen muodostaman suorituskyvyn jäljittämisen välinen yhteys perustuu käytössä olevaan juurihakemistoon ja yhteiseen tietomalliin.</span><span class="sxs-lookup"><span data-stu-id="ca57c-217">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="ca57c-218">Muodon versionumerointia ja mallin yhdistämistä ei oteta huomioon.</span><span class="sxs-lookup"><span data-stu-id="ca57c-218">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="ca57c-219">Mallimerkinnän **oletusarvoa mallimerkintää varten** ei myöskään oteta huomioon.</span><span class="sxs-lookup"><span data-stu-id="ca57c-219">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a id='import-trace'></a><span data-ttu-id="ca57c-220">Tuo tuotettu jälki RCS:ään.</span><span class="sxs-lookup"><span data-stu-id="ca57c-220">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="ca57c-221">Valitse RCS:ssä **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="ca57c-221">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="ca57c-222">Laajenna **Konfiguraatiot**-sivun konfiguraatiopuussa **Suorituskyvyn jäljitysmalli** -nimike ja valitse **Suorituskyvyn seurannan muoto** -nimike.</span><span class="sxs-lookup"><span data-stu-id="ca57c-222">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="ca57c-223">Valitse toimintoruudussa **Suunnittelija**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-223">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="ca57c-224">Valitse **Muodon suunnittelija**-sivulla hallintapaneelista **Suorituskyvyn jäljitysmuoto**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-224">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="ca57c-225">Valitse **Suorituskyvyn jäljitystulosten asetukset** -valintaikkunasta **Tuo suorituskyvyn jäljitys**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-225">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="ca57c-226">Valitse **Selaa** ja valitse zip-tiedosto, jonka olet vienyt Finance and Operationsista aiemmin.</span><span class="sxs-lookup"><span data-stu-id="ca57c-226">Select **Browse** to select the zip file that you exported from Finance and Operations earlier.</span></span>
7. <span data-ttu-id="ca57c-227">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-227">Select **OK**.</span></span>

    ![Suorituskyvyn jäljitystulosten asetukset -valintaikkuna RCS-kohteessa](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="ca57c-229">Suorituskyvyn seurannan käyttäminen RCS – Format -suoritusanalyysissä</span><span class="sxs-lookup"><span data-stu-id="ca57c-229">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="ca57c-230">Laajenna kaikkien muotoilukohteiden sisältö valitsemalla **Laajenna/tiivistä**-vaihtoehto **Muodon suunnittelija**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="ca57c-230">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="ca57c-231">Huomaa, että joistakin nykyisen muodon kohteista näytetään lisätietoja:</span><span class="sxs-lookup"><span data-stu-id="ca57c-231">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="ca57c-232">Todellinen aika, joka käytettiin tietojen syöttämiseen luotuun tulosteeseen kohteen muotoilun avulla</span><span class="sxs-lookup"><span data-stu-id="ca57c-232">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="ca57c-233">Sama aika ilmaistaan prosentteina kokonaisajasta, joka käytettiin koko tuotoksen tuottamiseen.</span><span class="sxs-lookup"><span data-stu-id="ca57c-233">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![Muodon suunnittelutoiminto -sivu RCS:ssä](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="ca57c-235">Sulje **Muodon suunnittelutoiminto** -sivu.</span><span class="sxs-lookup"><span data-stu-id="ca57c-235">Close **Format designer** page.</span></span>

### <a id='use-trace'></a><span data-ttu-id="ca57c-236">Suorituskyvyn seurannan käyttäminen RCS:ssä – Mallin määritys</span><span class="sxs-lookup"><span data-stu-id="ca57c-236">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="ca57c-237">Valitse RCS:ssä **Konfiguraatiot**-sivulla konfiguraatiopuussa **Suorituskyvyn jäljitysmääritys** -nimike.</span><span class="sxs-lookup"><span data-stu-id="ca57c-237">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="ca57c-238">Valitse toimintoruudussa **Suunnittelija**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-238">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="ca57c-239">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-239">Select **Designer**.</span></span>
4. <span data-ttu-id="ca57c-240">Valitse **Mallin määrityssuunnittelija** -sivulla hallintapaneelista **Suorituskyvyn jäljitysmuoto**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-240">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="ca57c-241">Valitse aiemmin tuotu jäljitys.</span><span class="sxs-lookup"><span data-stu-id="ca57c-241">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="ca57c-242">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-242">Select **OK**.</span></span>

<span data-ttu-id="ca57c-243">Huomaa, että joidenkin nykyisen mallimääritysten tietolähdenimikkeiden käytettävissä on uusia tietoja:</span><span class="sxs-lookup"><span data-stu-id="ca57c-243">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="ca57c-244">Tietolähteen avulla tietoja haettaessa käytetty todellinen aika</span><span class="sxs-lookup"><span data-stu-id="ca57c-244">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="ca57c-245">Sama aika ilmaistaan prosentteina kokonaisajasta, joka käytettiin koko mallin määrityksen suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="ca57c-245">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="ca57c-246">Huomaa, että ER ilmoittaa, että nykyisen mallin yhdistämismääritys kopioi tietokantapyynnöt, kun VendTable/\<Relations/VendTrans\_. VendTable AccountNum-tietolähde suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="ca57c-246">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="ca57c-247">Tämä päällekkäisyys johtuu siitä, että toimittajatapahtumien luetteloa kutsutaan kaksi kertaa kutakin iteroitua toimittajatietuetta varten:</span><span class="sxs-lookup"><span data-stu-id="ca57c-247">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="ca57c-248">Yksi kutsu tehdään tietomallin kunkin tapahtuman tietojen syöttämiseen määritettyjen sidosten perusteella.</span><span class="sxs-lookup"><span data-stu-id="ca57c-248">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="ca57c-249">Yksi kutsu tehdään, kun toimittaja määrittää lasketun määrän tapahtumia toimittajakohtaisesti tietomallissa.</span><span class="sxs-lookup"><span data-stu-id="ca57c-249">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![Virheilmoitus tietokantapyyntöjen kopioista RCS-mallin malli kartoituksen suunnittelusivulla](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="ca57c-251">Arvo **\[Q:530\]** ilmaisee, että VendTrans-taulua kutsuttiin 530 kertaa palauttamaan kyseisessä taulussa oleva tietue VendTable/\<Relations/VendTrans. VendTable\_AccountNum-tieto lähteeseen.</span><span class="sxs-lookup"><span data-stu-id="ca57c-251">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="ca57c-252">Arvo **\[530\]** ilmaisee, että VendTable/\<Relations/VendTrans. VendTable\_AccountNum-tietolähdettä kutsuttiin 530 kertaa palaamaan, jolloin tietue palautetaan kyseiseen tietolähteeseen ja sen tiedot syötetään tietomalliin.</span><span class="sxs-lookup"><span data-stu-id="ca57c-252">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="ca57c-253">Suosittelemme, että käytät VendTable/\<Relations/VendTrans. VendTable\_AccountNum-tietolähteen välimuistia, jotta voit vähentää 265-tapahtumien tietojen saamiseksi tehtyjen kutsujen määrää ja parantaa mallimäärityksen suorituskykyä.</span><span class="sxs-lookup"><span data-stu-id="ca57c-253">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="ca57c-254">Voi myös olla hyödyllistä vähentää LedgerTransTypeList-tietolähteeseen tehtyjen kutsujen määrää.</span><span class="sxs-lookup"><span data-stu-id="ca57c-254">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="ca57c-255">Tätä tietolähdettä käytetään liittämään kaikki **lLedgerTransType**-luetteloinnin arvot sen otsikkoon.</span><span class="sxs-lookup"><span data-stu-id="ca57c-255">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="ca57c-256">Käyttämällä tätä tietolähdettä voit löytää asianmukaisen tunnisteen ja syöttää sen kunkin toimittajatapahtuman tietomalliin.</span><span class="sxs-lookup"><span data-stu-id="ca57c-256">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="ca57c-257">Tähän tietolähteeseen soitettujen kutsujen määrä (9 027) on melko suuri 265-tapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="ca57c-257">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![Mallin määrityksen suunnittelijasivu RCS:ssä näyttää 9 027 puhelua tietolähteeseen](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="ca57c-259">Paranna mallin määritystä suorituksen jälkeisten tietojen perusteella</span><span class="sxs-lookup"><span data-stu-id="ca57c-259">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="ca57c-260">Mallin määrityksen logiikan muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="ca57c-260">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="ca57c-261">Seuraavia ohjeita noudattamalla voit käyttää välimuistia, joka estää kaksoissoittoja tietokantaan:</span><span class="sxs-lookup"><span data-stu-id="ca57c-261">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="ca57c-262">Valitse RCS:ssä **Mallin määrityksen suunnittelu** -sivun **Tietolähteet**-ruudusta **VendTable**-nimike.</span><span class="sxs-lookup"><span data-stu-id="ca57c-262">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="ca57c-263">Valitse **Välimuisti**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-263">Select **Cache**.</span></span>
    3. <span data-ttu-id="ca57c-264">Laajenna **VendTable**-nimike, laajenna VendTable-tietolähde ( **\<Suhde**-nimike), yksi-moneen-suhteiden luettelo ja valitse **VendTrans.VendTable\_AccountNum**-nimike</span><span class="sxs-lookup"><span data-stu-id="ca57c-264">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="ca57c-265">Valitse **Välimuisti**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-265">Select **Cache**.</span></span>

    ![Asetusten tallentaminen välimuistiin, jotta kaksinkertaiset kutsut voidaan estää](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="ca57c-267">Siirrä LedgerTransTypeList-tietolähde VendTable-tietolähteen käyttöalueeseen seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="ca57c-267">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="ca57c-268">Laajenna **Tietolähdetyypit**-ruudussa **Funktiot**-nimike ja valitse **Laskettu kenttä** -nimike.</span><span class="sxs-lookup"><span data-stu-id="ca57c-268">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="ca57c-269">Valitse **Tietolähteet**-ruudusta **VendTable**-nimike.</span><span class="sxs-lookup"><span data-stu-id="ca57c-269">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="ca57c-270">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-270">Select **Add**.</span></span>
    4. <span data-ttu-id="ca57c-271">Kirjoita **Nimi**-kenttään **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-271">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="ca57c-272">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-272">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="ca57c-273">Kirjoita **Kaava**-kenttään **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-273">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="ca57c-274">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-274">Select **Save**.</span></span>
    8. <span data-ttu-id="ca57c-275">Sulje **Kaavaeditori**-sivu.</span><span class="sxs-lookup"><span data-stu-id="ca57c-275">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="ca57c-276">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-276">Click **OK**.</span></span>

3. <span data-ttu-id="ca57c-277">Suorita **\$TransType**-kentän tallentaminen välimuistiin seuraavien vaiheiden mukaisesti:</span><span class="sxs-lookup"><span data-stu-id="ca57c-277">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="ca57c-278">Valitse **LedgerTransTypeList**-nimike.</span><span class="sxs-lookup"><span data-stu-id="ca57c-278">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="ca57c-279">Valitse **Välimuisti**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-279">Select **Cache**.</span></span>
    3. <span data-ttu-id="ca57c-280">Valitse **VendTable.\$TransType**-nimike.</span><span class="sxs-lookup"><span data-stu-id="ca57c-280">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="ca57c-281">Valitse **Välimuisti**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-281">Select **Cache**.</span></span>

    ![$TransType-kentän asetusten tallentaminen välimuistiin](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="ca57c-283">Näiden vaiheiden avulla voit muuttaa **\$TransTypeRecord**-kenttää siten, että se alkaa käyttää välimuistissa olevaa **\$TransType**-kenttää:</span><span class="sxs-lookup"><span data-stu-id="ca57c-283">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="ca57c-284">Laajenna **Tietolähteet**-ruudussa **VendTable**-nimike, laajenna **\<Suhteet**-nimike, laajenna **VendTrans.VendTable\_AccountNum**-nimike ja valitse **VendTable. VendTrans. VendTable\_AccountNum.\$Transtyperecord** -nimike.</span><span class="sxs-lookup"><span data-stu-id="ca57c-284">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="ca57c-285">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-285">Select **Edit**.</span></span>
    3. <span data-ttu-id="ca57c-286">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-286">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="ca57c-287">Etsi **Kaava**-kentästä seuraava lauseke:</span><span class="sxs-lookup"><span data-stu-id="ca57c-287">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="ca57c-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="ca57c-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="ca57c-289">Syötä **Kaava**-kenttään seuraava lauseke:</span><span class="sxs-lookup"><span data-stu-id="ca57c-289">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="ca57c-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="ca57c-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="ca57c-291">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-291">Select **Save**.</span></span>
    7. <span data-ttu-id="ca57c-292">Sulje **Kaavaeditori**-sivu.</span><span class="sxs-lookup"><span data-stu-id="ca57c-292">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="ca57c-293">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-293">Select **OK**.</span></span>

5. <span data-ttu-id="ca57c-294">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-294">Select **Save**.</span></span>
6. <span data-ttu-id="ca57c-295">Sulje **Mallimäärityksen sunnittelun** sivu.</span><span class="sxs-lookup"><span data-stu-id="ca57c-295">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="ca57c-296">Sulje **Mallimääritykset**-sivu.</span><span class="sxs-lookup"><span data-stu-id="ca57c-296">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="ca57c-297">ER-mallin yhdistämismäärityksen muokatun version täydentäminen</span><span class="sxs-lookup"><span data-stu-id="ca57c-297">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="ca57c-298">Valitse RCS-järjestelmän **Konfiguraatiot**-sivun **Versiot**-pikavälilehdessä **Suorituskyvyn jäljityksen** määrityksen versio **1.2**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-298">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="ca57c-299">Valitse **Muutoksen tila**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-299">Select **Change status**.</span></span>
3. <span data-ttu-id="ca57c-300">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-300">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-finance-and-operations"></a><span data-ttu-id="ca57c-301">Tuo muutettu ER-mallin kartoitusmääritys RCI:sta Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="ca57c-301">Import the modified ER model mapping configuration from RCS into Finance and Operations</span></span>

<span data-ttu-id="ca57c-302">Tuo tämän jakson aikaisemmissa osissa esitetyt vaiheet [Tuo ER-konfiguraatio RCS:stä Finance and Operationsiin](#import-configuration) tuodaksesi **Suorituskyvyn jäljityskartoitus** -konfiguraation versiot 1.2 Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="ca57c-302">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration into Finance and Operations.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="ca57c-303">Muokatun ER-ratkaisun suorittaminen jäljityksen suorittamista varten</span><span class="sxs-lookup"><span data-stu-id="ca57c-303">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="ca57c-304">Suorita ER-muoto</span><span class="sxs-lookup"><span data-stu-id="ca57c-304">Run the ER format</span></span>

<span data-ttu-id="ca57c-305">Luo uusi suoritusjälki [Suorita ER-muoto](#run-format) toistamalla tämän aiheen aikaisemmissa jaksoissa esitetyt vaiheet.</span><span class="sxs-lookup"><span data-stu-id="ca57c-305">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="ca57c-306">Suorituksen jäljityksen tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="ca57c-306">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-finance-and-operations"></a><span data-ttu-id="ca57c-307">Vie luotu jäljitys Finance and Operationsista</span><span class="sxs-lookup"><span data-stu-id="ca57c-307">Export the generated trace from Finance and Operations</span></span>

<span data-ttu-id="ca57c-308">Toista aiemmin tässä aiheessa kerrotut jakson vaiheet [Valitse luotu jälki Finance and Operationsista](#export-trace) jos haluat tallentaa uuden suoritusjäljen paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="ca57c-308">Repeat the steps in the [Export the generated trace from Finance and Operations](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="ca57c-309">Tuo tuotettu jälki RCS:ään.</span><span class="sxs-lookup"><span data-stu-id="ca57c-309">Import the generated trace into RCS</span></span>

<span data-ttu-id="ca57c-310">Toista tässä osassa aiemmin kerrotut vaiheet [Tuo luodut jäljet RCS](#import-trace) tuodaksesi uudet suorituskykyjäljet RCS:ään.</span><span class="sxs-lookup"><span data-stu-id="ca57c-310">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="ca57c-311">Suorituskyvyn seurannan käyttäminen RCS:ssä – Mallin määritys</span><span class="sxs-lookup"><span data-stu-id="ca57c-311">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="ca57c-312">Suorita aiemmin tämän ohjeaiheen [Suorituskyvyn seurannan käyttäminen RCS:ssä – Mallin määritys](#use-trace) -osassa kuvatut suorituskyvyn jäljitys -kohdan vaiheet, kun haluat analysoida viimeisimmän suorituskyvyn jäljityksen.</span><span class="sxs-lookup"><span data-stu-id="ca57c-312">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="ca57c-313">Huomaa, että mallimääritykseen tehdyt oikaisut ovat poistaneet tietokannasta päällekkäisiä kyselyitä.</span><span class="sxs-lookup"><span data-stu-id="ca57c-313">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="ca57c-314">Tämän mallimäärityksen tietokantataulukoihin ja tietolähteisiin tehtyjen kutsujen määrä on myös vähennetty.</span><span class="sxs-lookup"><span data-stu-id="ca57c-314">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="ca57c-315">Näin ollen koko ER-ratkaisun suorituskyky on parantunut.</span><span class="sxs-lookup"><span data-stu-id="ca57c-315">Therefore, the performance of the whole ER solution has improved.</span></span>

![Jäljitä tietoja VendTable-tietolähteestä RCS-mallin mallinmäärityssuunnittelija-sivulta](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="ca57c-317">Jäljitystiedoissa VendTable-tietolähteen arvo **\[12\]** ilmaisee, että tätä tietolähdettä kutsuttiin 12 kertaa.</span><span class="sxs-lookup"><span data-stu-id="ca57c-317">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="ca57c-318">Arvo **\[Q:6\]** ilmaisee, että tietokantakutsuille on käännetty kuusi kutsua VendTable-tauluun.</span><span class="sxs-lookup"><span data-stu-id="ca57c-318">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="ca57c-319">Arvo **\[C:6\]** ilmaisee, että tietokannasta noudetut tiedot tallennettiin välimuistiin ja kuusi muuta kutsua käsiteltiin välimuistin avulla.</span><span class="sxs-lookup"><span data-stu-id="ca57c-319">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="ca57c-320">Huomaa, että LedgerTransTypeList-tietolähteeseen soitettujen kutsujen määrä on vähentynyt 9 027:sta 240:een.</span><span class="sxs-lookup"><span data-stu-id="ca57c-320">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![Jäljitä tietoja LedgerTransTypeList-tietolähteestä RCS-mallin mallinmäärityssuunnittelija-sivulta](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-finance-and-operations"></a><span data-ttu-id="ca57c-322">Suorituksen jäljityksen tarkasteleminen Finance and Operationsissa</span><span class="sxs-lookup"><span data-stu-id="ca57c-322">Review the execution trace in Finance and Operations</span></span>

<span data-ttu-id="ca57c-323">RCS-ohjelman lisäksi jotkin Finance and Operations -versiot voivat tarjota ER-kehyssuunnittelijakokemuksen ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="ca57c-323">In addition to RCS, some versions of Finance and Operations might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="ca57c-324">Näissä Finance and Operations -versioissa on **Ota käyttöön suunnittelutila** -vaihtoehto, joka voidaan ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="ca57c-324">These versions of Finance and Operations have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="ca57c-325">Tämä vaihtoehto löytyy **Sähköisen raportoinnin parametrit** -sivun **Yleiset**-välilehdestä, jonka voit avata **Sähköisen raportoinnin** työtilassa.</span><span class="sxs-lookup"><span data-stu-id="ca57c-325">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![Ota suunnittelutilan vaihtoehto käyttöön Finance and Operationsin sähköisen raportoinnin parametrit -sivulla](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="ca57c-327">Jos käytät jotakin näistä Finance and Operations -versioista, voit analysoida luotuja suorituskykytietoja suoraan Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="ca57c-327">If you use one of these versions of Finance and Operations, you can analyze the details of generated performance traces directly in Finance and Operations.</span></span> <span data-ttu-id="ca57c-328">Sinun ei tarvitse viedä niitä Finance and Operationsista ja tuoda niitä RCS-järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="ca57c-328">You don't have to export them from Finance and Operation and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="ca57c-329">Suorituksen jäljityksen tarkasteleminen ulkoisten työkalujen avulla</span><span class="sxs-lookup"><span data-stu-id="ca57c-329">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="ca57c-330">Konfiguroi käyttäjäparametrit</span><span class="sxs-lookup"><span data-stu-id="ca57c-330">Configure user parameters</span></span>

1. <span data-ttu-id="ca57c-331">Valitse Finance and Operationsissa **Organisaation hallinto \> Sähköinen raportointi \> Määritykset**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-331">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="ca57c-332">Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-332">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="ca57c-333">Valitse **Käyttäjäparametrit** -valintaikkunan **Suorituksen jäljitys** -osan **Suorituksen jäljitys muoto-osan** -kentässä **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="ca57c-333">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="ca57c-334">Suorita ER-muoto</span><span class="sxs-lookup"><span data-stu-id="ca57c-334">Run the ER format</span></span>

<span data-ttu-id="ca57c-335">Luo uusi suoritusjälki [Suorita ER-muoto](#run-format) toistamalla tämän aiheen aikaisemmissa jaksoissa esitetyt vaiheet.</span><span class="sxs-lookup"><span data-stu-id="ca57c-335">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="ca57c-336">Huomaa, että Internet-selain tarjoaa zip-tiedoston ladattavaksi.</span><span class="sxs-lookup"><span data-stu-id="ca57c-336">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="ca57c-337">Tämä tiedosto sisältää suorituskyvyn jäljityksen PerfView-muodossa.</span><span class="sxs-lookup"><span data-stu-id="ca57c-337">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="ca57c-338">Tämän jälkeen voit analysoida ER Format Execution -toiminnon tietoja Perxview-suorituskyvyn analysointityökalun avulla.</span><span class="sxs-lookup"><span data-stu-id="ca57c-338">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>
