---
title: Sähköisen raportoinnin muodon suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi
description: Tässä ohjeaiheessa on tietoja suorituskykyongelmien vianmäärityksestä sähköisen raportoinnin (ER) suorituskyvyn jäljitystoiminnon avulla.
author: NickSelin
manager: AnnBe
ms.date: 06/12/2019
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
ms.openlocfilehash: 97511e23f0ea2842e625799c0a2c1e51b5832feb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182137"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="5ef19-103">Sähköisen raportoinnin muotojen suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi</span><span class="sxs-lookup"><span data-stu-id="5ef19-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5ef19-104">Osana sähköisten raportointikonfiguraatioiden suunnittelua sähköisten asiakirjojen luomista varten määritetään menetelmä, jonka avulla tiedot haetaan sovelluksesta ja syötetään luotavaan tuotokseen.</span><span class="sxs-lookup"><span data-stu-id="5ef19-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="5ef19-105">ER Performance Trace -toiminto auttaa vähentämään huomattavasti aikaa ja kustannuksia, jotka liittyvät ER-muodon suorituksen yksityiskohtien keräämiseen ja niiden käyttämiseen suorituskykyongelmien vianmäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="5ef19-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="5ef19-106">Tässä opetusohjelmassa on ohjeita siitä, miten suorituskykyä voidaan seurata suoritettavissa ER-muodoissa ja miten suorituskykyä voidaan parantaa näiden jälkien tietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="5ef19-106">This tutorial provides guidelines about how to take performance traces for executed ER formats, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5ef19-107">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="5ef19-107">Prerequisites</span></span>

<span data-ttu-id="5ef19-108">Tämän opetusohjelman esimerkkien suorittaminen edellyttää seuraavia käyttöoikeuksia:</span><span class="sxs-lookup"><span data-stu-id="5ef19-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="5ef19-109">Jonkin seuraavien roolien käyttöoikeus:</span><span class="sxs-lookup"><span data-stu-id="5ef19-109">Access to one of the following roles:</span></span>

    - <span data-ttu-id="5ef19-110">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="5ef19-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="5ef19-111">Sähköisen raportoinnin toiminnallinen konsultti</span><span class="sxs-lookup"><span data-stu-id="5ef19-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="5ef19-112">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="5ef19-112">System administrator</span></span>

- <span data-ttu-id="5ef19-113">Käyttöoikeus Regulatory Configuration Services (RCS) -esiintymään, joka on valmisteltu samalle vuokralaiselle kuin sovellus, jollekin seuraavista rooleista:</span><span class="sxs-lookup"><span data-stu-id="5ef19-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as the application, for one of the following roles:</span></span>

    - <span data-ttu-id="5ef19-114">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="5ef19-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="5ef19-115">Sähköisen raportoinnin toiminnallinen konsultti</span><span class="sxs-lookup"><span data-stu-id="5ef19-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="5ef19-116">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="5ef19-116">System administrator</span></span>

<span data-ttu-id="5ef19-117">Seuraavat tiedostot täytyy myös ladata ja tallentaa paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="5ef19-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="5ef19-118">Tiedosto</span><span class="sxs-lookup"><span data-stu-id="5ef19-118">File</span></span>                                  | <span data-ttu-id="5ef19-119">Sisältö</span><span class="sxs-lookup"><span data-stu-id="5ef19-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="5ef19-120">Suorituskyvyn jäljitysmalli.versio.1</span><span class="sxs-lookup"><span data-stu-id="5ef19-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="5ef19-121">Esimerkin ER-tietomallin konfigurointi</span><span class="sxs-lookup"><span data-stu-id="5ef19-121">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| <span data-ttu-id="5ef19-122">Suorituskyvyn jäljitysmetadata.versio.1</span><span class="sxs-lookup"><span data-stu-id="5ef19-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="5ef19-123">Esimerkin ER-metadatan konfigurointi</span><span class="sxs-lookup"><span data-stu-id="5ef19-123">Sample ER metadata configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| <span data-ttu-id="5ef19-124">Suorituskyvyn jäljitysmapping.versio.1</span><span class="sxs-lookup"><span data-stu-id="5ef19-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="5ef19-125">Esimerkin ER-mallikartoituksen konfigurointi</span><span class="sxs-lookup"><span data-stu-id="5ef19-125">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="5ef19-126">Suorituskyvyn jäljitysformat.versio.1</span><span class="sxs-lookup"><span data-stu-id="5ef19-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="5ef19-127">Esimerkin ER-format-konfigurointi</span><span class="sxs-lookup"><span data-stu-id="5ef19-127">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="5ef19-128">Konfiguroi ER-parametrit</span><span class="sxs-lookup"><span data-stu-id="5ef19-128">Configure ER parameters</span></span>

<span data-ttu-id="5ef19-129">Jokainen sovelluksessa luotu ER-suorituskykyjäljitys tallennetaan suorituslokitietueen liitteenä.</span><span class="sxs-lookup"><span data-stu-id="5ef19-129">Each ER performance trace that is generated in the application is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="5ef19-130">Näiden liitteiden hallinnassa käytetään tiedostojen hallinnan (DM) kehystä.</span><span class="sxs-lookup"><span data-stu-id="5ef19-130">The Document management (DM) framework is used to manage these attachments.</span></span> <span data-ttu-id="5ef19-131">Sinun on määritettävä ER-parametrit etukäteen ja määritettävä DM-tiedosto tyyppi, jota käytetään suorituskykyjälkien liittämiseen.</span><span class="sxs-lookup"><span data-stu-id="5ef19-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="5ef19-132">Valitse **Sähköinen raportointi** -työtilasta **Sähköisen raportoinnin parametrit**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-132">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="5ef19-133">Valitse sitten **Sähköisen raportoinnin parametrit** -sivun **Liitteet**-välilehden **Muut**-kentästä suorituskyvyn jäljille käytettävä DM-tiedostotyyppi.</span><span class="sxs-lookup"><span data-stu-id="5ef19-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Sähköisen raportoinnin parametrit -sivu](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="5ef19-135">Jos haluat olla käytettävissä **Muut** -hakukentässä, DM-tiedostotyyppi on konfiguroitava seuraavalla tavalla **Asiakirjatyypit**-sivulla (**Organisaation hallinta \> Asiakirjan hallinta \> Asiakirjatyypit**):</span><span class="sxs-lookup"><span data-stu-id="5ef19-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="5ef19-136">**Luokka:** Liitä tiedosto</span><span class="sxs-lookup"><span data-stu-id="5ef19-136">**Class:** Attach file</span></span>
- <span data-ttu-id="5ef19-137">**Ryhmä:** Tiedosto</span><span class="sxs-lookup"><span data-stu-id="5ef19-137">**Group:** File</span></span>

![Asiakirjatyypit-sivu](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="5ef19-139">Valitun tiedostotyypin on oltava käytettävissä kaikissa nykyisen esiintymän yrityksissä, koska DM-liitteet ovat yrityskohtaisia.</span><span class="sxs-lookup"><span data-stu-id="5ef19-139">The selected document type must be available in every company of the current instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="5ef19-140">Konfiguroi RCS-parametrit</span><span class="sxs-lookup"><span data-stu-id="5ef19-140">Configure RCS parameters</span></span>

<span data-ttu-id="5ef19-141">Luodut ER-suorituskykyjäljet tuodaan RCS:ään analysointia varten käyttämällä ER Format Designeria ja ER Mapping Designeria.</span><span class="sxs-lookup"><span data-stu-id="5ef19-141">ER performance traces that are generated will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="5ef19-142">Koska ER-suorituskykyjäljet tallennetaan ER-muotoon liittyvän suorituslokitietueen liitteinä, RCS-parametrit on määritettävä etukäteen, jotta voidaan määrittää DM-tiedostotyyppi, jota käytetään suorituskykyjälkien liittämiseen.</span><span class="sxs-lookup"><span data-stu-id="5ef19-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="5ef19-143">Valitse yrityksellesi määritetyn RCS-esiintymän **Sähköisen raportoinnin** -työtilassa **Sähköiset raportointiparametrit**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="5ef19-144">Valitse sitten **Sähköisen raportoinnin parametrit** -sivun **Liitteet**-välilehden **Muut**-kentästä suorituskyvyn jäljille käytettävä DM-tiedostotyyppi.</span><span class="sxs-lookup"><span data-stu-id="5ef19-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Sähköisen raportoinnin parametrit -sivu RCS:ssä](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="5ef19-146">Jos haluat olla käytettävissä **Muut** -hakukentässä, DM-tiedostotyyppi on konfiguroitava seuraavalla tavalla **Asiakirjatyypit**-sivulla (**Organisaation hallinta \> Asiakirjan hallinta \> Asiakirjatyypit**):</span><span class="sxs-lookup"><span data-stu-id="5ef19-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="5ef19-147">**Luokka:** Liitä tiedosto</span><span class="sxs-lookup"><span data-stu-id="5ef19-147">**Class:** Attach file</span></span>
- <span data-ttu-id="5ef19-148">**Ryhmä:** Tiedosto</span><span class="sxs-lookup"><span data-stu-id="5ef19-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="5ef19-149">Suunnittele ER-ratkaisu</span><span class="sxs-lookup"><span data-stu-id="5ef19-149">Design an ER solution</span></span>

<span data-ttu-id="5ef19-150">Oletetaan, että olet aloittanut uuden ER-ratkaisun suunnittelun, joka luo toimittajatapahtumia esittelevän uuden raportin.</span><span class="sxs-lookup"><span data-stu-id="5ef19-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="5ef19-151">Tällä hetkellä voit etsiä valitun toimittajan tapahtumat **Toimittajatapahtumat**-sivulta (Siirry **Ostoreskontra \> Toimittajat \> Kaikki toimittajat**, valitse toimittaja ja sitten toimintoruudun **Toimittaja**-välilehti kohdassa valitse **Tapahtumat**-ryhmästä **Tapahtumat**).</span><span class="sxs-lookup"><span data-stu-id="5ef19-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="5ef19-152">Haluat kuitenkin saada kaikki toimittajatapahtumat samaan aikaan yhdessä sähköisessä asiakirjassa XML-muodossa.</span><span class="sxs-lookup"><span data-stu-id="5ef19-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="5ef19-153">Tämä ratkaisu koostuu useista ER-konfiguraatioista, jotka sisältävät vaaditun tietomallin, metatiedot, mallien yhdistämismääritykset ja muotokomponentit.</span><span class="sxs-lookup"><span data-stu-id="5ef19-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="5ef19-154">Kirjaudu yrityksen RCS-esiintymään, joka on valmisteltu yrityksellesi.</span><span class="sxs-lookup"><span data-stu-id="5ef19-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="5ef19-155">Tässä opetusohjelmassa luodaan ja muokataan konfiguraatioita malliyritykselle **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="5ef19-156">Varmista siksi, että tämä konfigurointipalvelu on lisätty RCS-järjestelmään ja valittu aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="5ef19-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="5ef19-157">Lisätietoja on kohdassa [Luo konfigurointipalvelut ja merkitse ne aktiivisiksi](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) menettelyiksi.</span><span class="sxs-lookup"><span data-stu-id="5ef19-157">For instructions, see the [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) procedure.</span></span>
3. <span data-ttu-id="5ef19-158">Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="5ef19-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="5ef19-159">Tuo **Konfiguraatiot** -sivulla lataamasi ER-kokoonpanot RCS-edellytyksenä seuraavassa järjestyksessä: tietomalli, metatiedot, mallikartoitus, muoto.</span><span class="sxs-lookup"><span data-stu-id="5ef19-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="5ef19-160">Luo kukin mukautus seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="5ef19-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="5ef19-161">Valitse toimintoruudusta **Vaihda \> Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="5ef19-162">Valitse haluamasi ER-kokoonpanon tiedosto XML-muodossa valitsemalla **Selaa**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="5ef19-163">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-163">Select **OK**.</span></span>

    ![Konfiguroinnit-sivu RCS:ssä](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="5ef19-165">ER-ratkaisun suorittaminen jäljityksen suorittamista varten</span><span class="sxs-lookup"><span data-stu-id="5ef19-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="5ef19-166">Oletetaan, että olet suunnitellut ER-ratkaisun ensimmäisen version.</span><span class="sxs-lookup"><span data-stu-id="5ef19-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="5ef19-167">Nyt haluat testata sitä esiintymässäsi ja analysoida suorituskykyä.</span><span class="sxs-lookup"><span data-stu-id="5ef19-167">You now want to test it in your instance and analyze execution performance.</span></span>

### <a id='import-configuration'></a><span data-ttu-id="5ef19-168">ER-konfiguraation tuominen RCI:sta Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="5ef19-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="5ef19-169">Kirjaudu sisään sovelluksen esiintymään.</span><span class="sxs-lookup"><span data-stu-id="5ef19-169">Sign in to your application instance.</span></span>
2. <span data-ttu-id="5ef19-170">Tämän opetusohjelman avulla voit tuoda konfiguraatiot RCS-esiintymästäsi (jossa suunnittelet ER-komponentteja) esiintymääsi (jossa testaat ja lopulta käytät niitä).</span><span class="sxs-lookup"><span data-stu-id="5ef19-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your instance (where you test and finally use them).</span></span> <span data-ttu-id="5ef19-171">Siksi on varmistettava, että kaikki vaaditut tiedot on valmisteltu.</span><span class="sxs-lookup"><span data-stu-id="5ef19-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="5ef19-172">Ohjeita on kohdassa [Sähköisen raportoinnin konfiguraatioiden tuonti Regulatory Configuration Services (RCS) -palvelusta](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations).</span><span class="sxs-lookup"><span data-stu-id="5ef19-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations) procedure.</span></span>
3. <span data-ttu-id="5ef19-173">Seuraavien vaiheiden mukaisesti voit tuoda konfiguraatiot RCS:stä sovellukseen:</span><span class="sxs-lookup"><span data-stu-id="5ef19-173">Follow these steps to import the configurations from RCS into the application:</span></span>

    1. <span data-ttu-id="5ef19-174">Valitse **Sähköisen raportoinnin** työtilassa**Litware, Inc**-määrityspalveluruudussa **Arkistot**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="5ef19-175">Valitse **Konfiguraatiosäilö**-sivun ruudukossa oleva säilö, jonka tyyppi on **RCS** ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="5ef19-176">Valitse **Konfiguraatiot**-pikavälilehdessä **Suorituskyvyn jäljitysmuodon** konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="5ef19-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="5ef19-177">Valitse **Versiot**-pikavälilehdellä valitun konfiguraation versio **1.1** ja valitse sitten **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![Konfiguraatiosäilön sivu](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="5ef19-179">Tietomallin ja mallin yhdistämismääritysten vastaavat versiot tuodaan automaattisesti valmiiksi tuodun ER-muodon konfiguroinnin edellytyksinä.</span><span class="sxs-lookup"><span data-stu-id="5ef19-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="5ef19-180">ER-suorituskykyjäljityksen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="5ef19-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="5ef19-181">Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-181">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="5ef19-182">Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="5ef19-183">Toimi **Käyttäjäparametrit**-valintaikkunan **Suorituksen jäljitys** -osassa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="5ef19-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="5ef19-184">Valitse **Suorituksen jäljitys muoto** -kentässä **Korjaa jäljitystiedosto** -kentässä, joka alkaa keräämään tietoja ER-muodon suorittamisesta.</span><span class="sxs-lookup"><span data-stu-id="5ef19-184">In the **Execution trace format** field, select **Debug trace format** to start to collect the details of ER format execution.</span></span> <span data-ttu-id="5ef19-185">Kun tämä arvo valitaan, suorituskyvyn jäljitys kerää seuraaviin toimiin kuluvaa aikaa koskevia tietoja:</span><span class="sxs-lookup"><span data-stu-id="5ef19-185">When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</span></span>

        - <span data-ttu-id="5ef19-186">Kunkin tietolähteen suorittamista mallikartoituksista, joita kutsutaan tietojen hakemiseksi</span><span class="sxs-lookup"><span data-stu-id="5ef19-186">Running each data source in the model mapping that is called to get data</span></span>
        - <span data-ttu-id="5ef19-187">Kunkin muotoilunimikkeen käsitteleminen siten, että se syöttää tietoja luotavalle tulosteelle</span><span class="sxs-lookup"><span data-stu-id="5ef19-187">Processing each format item to enter data in the output that is generated</span></span>

        <span data-ttu-id="5ef19-188">**Suorituksen jäljitysmuoto** -kentän avulla voit määrittää sen luodun suorituskykyjäljityksen muodon, johon suoritustiedot tallennetaan ER-ja Mapping-elementeissä.</span><span class="sxs-lookup"><span data-stu-id="5ef19-188">You use the **Execution trace format** field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</span></span> <span data-ttu-id="5ef19-189">Kun valitset arvoksi **Virheen korjauksen jäljitysmuodon**, pystyt analysoimaan jäljityksen sisältöä ER Operation Designerissa ja näkemään ER-muodon tai määrityselementit, jotka mainitaan jäljityksessä.</span><span class="sxs-lookup"><span data-stu-id="5ef19-189">By selecting **Debug trace format** as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</span></span>

    2. <span data-ttu-id="5ef19-190">Määritä seuraavat asetukset: **Kyllä**, jos haluat kerätä tarkempia tietoja ER-mallin kartoituksesta ja ER-muotokomponenttien suorittamisesta.</span><span class="sxs-lookup"><span data-stu-id="5ef19-190">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="5ef19-191">**Kyselyn tilastotietojen kerääminen** – Kun tämä vaihtoehto on käytössä, suorituskyvyn jäljitys kerää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="5ef19-191">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="5ef19-192">Tietolähteiden tekemien kutsujen määrä</span><span class="sxs-lookup"><span data-stu-id="5ef19-192">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="5ef19-193">Tietokantaan lisättyjen toistettujen kutsujen määrä</span><span class="sxs-lookup"><span data-stu-id="5ef19-193">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="5ef19-194">Tietokantakutsujen tekemiseen käytettävien SQL-lauseiden tiedot</span><span class="sxs-lookup"><span data-stu-id="5ef19-194">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="5ef19-195">**Jäljitysvälimuistin käyttäminen** – Kun tämä asetus on käytössä, suorituskyvyn jäljitys kerää tietoja ER-mallikartoituksen välimuistin käytöstä.</span><span class="sxs-lookup"><span data-stu-id="5ef19-195">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="5ef19-196">**Jäljitystietojen käyttö** – Kun tämä asetus on käytössä, suorituskyvyn jäljitys kerää tietoja siitä, kuinka monta käyntiä tietokantaan on tehty tietueluettelotyypin suoritettavissa tietolähteissä.</span><span class="sxs-lookup"><span data-stu-id="5ef19-196">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="5ef19-197">**Jäljitystietojen luettelointi** – Kun tämä asetus on käytössä, suorituskyvyn jäljitys kerää tietoja siitä, kuinka monta käyntiä tietokantaan on tehty tietueluettelotyypin suoritettavissa tietolähteissä.</span><span class="sxs-lookup"><span data-stu-id="5ef19-197">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5ef19-198">**Käyttäjäparametrit** -valintaikkunan parametrit koskevat käyttäjää ja nykyistä yritystä.</span><span class="sxs-lookup"><span data-stu-id="5ef19-198">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![Käyttäjän parametrit -valintaikkuna](./media/GER-PerfTrace-GER-UserParameters.png)

### <a id='run-format'></a><span data-ttu-id="5ef19-200">Suorita ER-muoto</span><span class="sxs-lookup"><span data-stu-id="5ef19-200">Run the ER format</span></span>

1. <span data-ttu-id="5ef19-201">Valitse **DEMF**-yritys.</span><span class="sxs-lookup"><span data-stu-id="5ef19-201">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="5ef19-202">Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-202">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="5ef19-203">Valitse **Konfiguraatiot**-sivulla konfiguraatiopuussa **Suorituskyvyn jäljitysmuodon** nimike.</span><span class="sxs-lookup"><span data-stu-id="5ef19-203">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="5ef19-204">Valitse toimintoruudussa **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-204">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="5ef19-205">Huomaa, että luotu tiedosto sisältää tietoja kuuden toimittajan 265-tapahtumista.</span><span class="sxs-lookup"><span data-stu-id="5ef19-205">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="5ef19-206">Suorituksen jäljityksen tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="5ef19-206">Review the execution trace</span></span>

### <a id='export-trace'></a><span data-ttu-id="5ef19-207">Vie luotu jäljitys sovelluksesta</span><span class="sxs-lookup"><span data-stu-id="5ef19-207">Export the generated trace from the application</span></span>

<span data-ttu-id="5ef19-208">Suorituskykyjäljet irrotetaan lähde-ER-muodosta, ja ne voidaan sarjoittaa ulkoiseen zip-tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="5ef19-208">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="5ef19-209">Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Määritysten virheenkorjauslokit**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-209">Go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="5ef19-210">Valitse **Sähköisen raportoinnin ajon lokit** -sivun vasemmanpuoleisen ruudun **Konfiguration nimi** -kentässä **Suorituskyvyn jäljitysmuoto** jos haluat löytää lokitiedostot, jotka on luotu **Suoritus kyvyn jäljitysmuodon** konfiguraatiolle.</span><span class="sxs-lookup"><span data-stu-id="5ef19-210">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="5ef19-211">Valitse **Liitteet**-painikkeen sivun oikeassa yläkulmassa (paperiliitinsymboli) tai paina **Ctrl+Shift+A**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-211">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![Liitteet-painike Sähköisen raportoinnin ajolokit -sivulla](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="5ef19-213">**Valitse sähköisen raportoinnin ajon lokit** -sivun toimintoruudussa **Avaa**, jos haluat saada suorituskyvyn jäljityksen zip-tiedostona ja tallentaa sen paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="5ef19-213">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![Sähköisen raportoinnin ajolokien liitteet](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="5ef19-215">Luotu jäljitys viittaa lähde-ER-raporttiin yksilöivän raporttitunnuksen avulla vain **GUID**-muodossa.</span><span class="sxs-lookup"><span data-stu-id="5ef19-215">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="5ef19-216">Muodon versionumerointia ei oteta huomioon.</span><span class="sxs-lookup"><span data-stu-id="5ef19-216">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="5ef19-217">Huomaa, että suoritetun ER-muodon ja ER-mallikartoituksen muodostaman suorituskyvyn jäljittämisen välinen yhteys perustuu käytössä olevaan juurihakemistoon ja yhteiseen tietomalliin.</span><span class="sxs-lookup"><span data-stu-id="5ef19-217">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="5ef19-218">Muodon versionumerointia ja mallin yhdistämistä ei oteta huomioon.</span><span class="sxs-lookup"><span data-stu-id="5ef19-218">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="5ef19-219">Mallimerkinnän **oletusarvoa mallimerkintää varten** ei myöskään oteta huomioon.</span><span class="sxs-lookup"><span data-stu-id="5ef19-219">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a id='import-trace'></a><span data-ttu-id="5ef19-220">Tuo tuotettu jälki RCS:ään.</span><span class="sxs-lookup"><span data-stu-id="5ef19-220">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="5ef19-221">Valitse RCS:ssä **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="5ef19-221">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="5ef19-222">Laajenna **Konfiguraatiot**-sivun konfiguraatiopuussa **Suorituskyvyn jäljitysmalli** -nimike ja valitse **Suorituskyvyn seurannan muoto** -nimike.</span><span class="sxs-lookup"><span data-stu-id="5ef19-222">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="5ef19-223">Valitse toimintoruudussa **Suunnittelija**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-223">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="5ef19-224">Valitse **Muodon suunnittelija**-sivulla hallintapaneelista **Suorituskyvyn jäljitysmuoto**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-224">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="5ef19-225">Valitse **Suorituskyvyn jäljitystulosten asetukset** -valintaikkunasta **Tuo suorituskyvyn jäljitys**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-225">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="5ef19-226">Valitse **Selaa** valitaksesi aiemmin viemäsi zip-tiedoston.</span><span class="sxs-lookup"><span data-stu-id="5ef19-226">Select **Browse** to select the zip file that you exported earlier.</span></span>
7. <span data-ttu-id="5ef19-227">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-227">Select **OK**.</span></span>

    ![Suorituskyvyn jäljitystulosten asetukset -valintaikkuna RCS-kohteessa](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="5ef19-229">Suorituskyvyn seurannan käyttäminen RCS – Format -suoritusanalyysissä</span><span class="sxs-lookup"><span data-stu-id="5ef19-229">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="5ef19-230">Laajenna kaikkien muotoilukohteiden sisältö valitsemalla **Laajenna/tiivistä**-vaihtoehto **Muodon suunnittelija**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="5ef19-230">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="5ef19-231">Huomaa, että joistakin nykyisen muodon kohteista näytetään lisätietoja:</span><span class="sxs-lookup"><span data-stu-id="5ef19-231">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="5ef19-232">Todellinen aika, joka käytettiin tietojen syöttämiseen luotuun tulosteeseen kohteen muotoilun avulla</span><span class="sxs-lookup"><span data-stu-id="5ef19-232">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="5ef19-233">Sama aika ilmaistaan prosentteina kokonaisajasta, joka käytettiin koko tuotoksen tuottamiseen.</span><span class="sxs-lookup"><span data-stu-id="5ef19-233">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![Muodon suunnittelutoiminto -sivu RCS:ssä](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="5ef19-235">Sulje **Muodon suunnittelutoiminto** -sivu.</span><span class="sxs-lookup"><span data-stu-id="5ef19-235">Close **Format designer** page.</span></span>

### <a id='use-trace'></a><span data-ttu-id="5ef19-236">Suorituskyvyn seurannan käyttäminen RCS:ssä – Mallin määritys</span><span class="sxs-lookup"><span data-stu-id="5ef19-236">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="5ef19-237">Valitse RCS:ssä **Konfiguraatiot**-sivulla konfiguraatiopuussa **Suorituskyvyn jäljitysmääritys** -nimike.</span><span class="sxs-lookup"><span data-stu-id="5ef19-237">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="5ef19-238">Valitse toimintoruudussa **Suunnittelija**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-238">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="5ef19-239">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-239">Select **Designer**.</span></span>
4. <span data-ttu-id="5ef19-240">Valitse **Mallin määrityssuunnittelija** -sivulla hallintapaneelista **Suorituskyvyn jäljitysmuoto**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-240">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="5ef19-241">Valitse aiemmin tuotu jäljitys.</span><span class="sxs-lookup"><span data-stu-id="5ef19-241">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="5ef19-242">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-242">Select **OK**.</span></span>

<span data-ttu-id="5ef19-243">Huomaa, että joidenkin nykyisen mallimääritysten tietolähdenimikkeiden käytettävissä on uusia tietoja:</span><span class="sxs-lookup"><span data-stu-id="5ef19-243">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="5ef19-244">Tietolähteen avulla tietoja haettaessa käytetty todellinen aika</span><span class="sxs-lookup"><span data-stu-id="5ef19-244">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="5ef19-245">Sama aika ilmaistaan prosentteina kokonaisajasta, joka käytettiin koko mallin määrityksen suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="5ef19-245">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="5ef19-246">Huomaa, että ER ilmoittaa, että nykyisen mallin yhdistämismääritys kopioi tietokantapyynnöt, kun VendTable/\<Relations/VendTrans\_. VendTable AccountNum-tietolähde suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="5ef19-246">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="5ef19-247">Tämä päällekkäisyys johtuu siitä, että toimittajatapahtumien luetteloa kutsutaan kaksi kertaa kutakin iteroitua toimittajatietuetta varten:</span><span class="sxs-lookup"><span data-stu-id="5ef19-247">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="5ef19-248">Yksi kutsu tehdään tietomallin kunkin tapahtuman tietojen syöttämiseen määritettyjen sidosten perusteella.</span><span class="sxs-lookup"><span data-stu-id="5ef19-248">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="5ef19-249">Yksi kutsu tehdään, kun toimittaja määrittää lasketun määrän tapahtumia toimittajakohtaisesti tietomallissa.</span><span class="sxs-lookup"><span data-stu-id="5ef19-249">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![Virheilmoitus tietokantapyyntöjen kopioista RCS-mallin malli kartoituksen suunnittelusivulla](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="5ef19-251">Arvo **\[Q:530\]** ilmaisee, että VendTrans-taulua kutsuttiin 530 kertaa palauttamaan kyseisessä taulussa oleva tietue VendTable/\<Relations/VendTrans. VendTable\_AccountNum-tieto lähteeseen.</span><span class="sxs-lookup"><span data-stu-id="5ef19-251">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="5ef19-252">Arvo **\[530\]** ilmaisee, että VendTable/\<Relations/VendTrans. VendTable\_AccountNum-tietolähdettä kutsuttiin 530 kertaa palaamaan, jolloin tietue palautetaan kyseiseen tietolähteeseen ja sen tiedot syötetään tietomalliin.</span><span class="sxs-lookup"><span data-stu-id="5ef19-252">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="5ef19-253">Suosittelemme, että käytät VendTable/\<Relations/VendTrans. VendTable\_AccountNum-tietolähteen välimuistia, jotta voit vähentää 265-tapahtumien tietojen saamiseksi tehtyjen kutsujen määrää ja parantaa mallimäärityksen suorituskykyä.</span><span class="sxs-lookup"><span data-stu-id="5ef19-253">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="5ef19-254">Voi myös olla hyödyllistä vähentää LedgerTransTypeList-tietolähteeseen tehtyjen kutsujen määrää.</span><span class="sxs-lookup"><span data-stu-id="5ef19-254">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="5ef19-255">Tätä tietolähdettä käytetään liittämään kaikki **lLedgerTransType**-luetteloinnin arvot sen otsikkoon.</span><span class="sxs-lookup"><span data-stu-id="5ef19-255">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="5ef19-256">Käyttämällä tätä tietolähdettä voit löytää asianmukaisen tunnisteen ja syöttää sen kunkin toimittajatapahtuman tietomalliin.</span><span class="sxs-lookup"><span data-stu-id="5ef19-256">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="5ef19-257">Tähän tietolähteeseen soitettujen kutsujen määrä (9 027) on melko suuri 265-tapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="5ef19-257">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![Mallin määrityksen suunnittelijasivu RCS:ssä näyttää 9 027 puhelua tietolähteeseen](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="5ef19-259">Paranna mallin määritystä suorituksen jälkeisten tietojen perusteella</span><span class="sxs-lookup"><span data-stu-id="5ef19-259">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="5ef19-260">Mallin määrityksen logiikan muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="5ef19-260">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="5ef19-261">Seuraavia ohjeita noudattamalla voit käyttää välimuistia, joka estää kaksoissoittoja tietokantaan:</span><span class="sxs-lookup"><span data-stu-id="5ef19-261">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="5ef19-262">Valitse RCS:ssä **Mallin määrityksen suunnittelu** -sivun **Tietolähteet**-ruudusta **VendTable**-nimike.</span><span class="sxs-lookup"><span data-stu-id="5ef19-262">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="5ef19-263">Valitse **Välimuisti**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-263">Select **Cache**.</span></span>
    3. <span data-ttu-id="5ef19-264">Laajenna **VendTable**-nimike, laajenna VendTable-tietolähde ( **\<Suhde**-nimike), yksi-moneen-suhteiden luettelo ja valitse **VendTrans.VendTable\_AccountNum**-nimike</span><span class="sxs-lookup"><span data-stu-id="5ef19-264">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="5ef19-265">Valitse **Välimuisti**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-265">Select **Cache**.</span></span>

    ![Asetusten tallentaminen välimuistiin, jotta kaksinkertaiset kutsut voidaan estää](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="5ef19-267">Siirrä LedgerTransTypeList-tietolähde VendTable-tietolähteen käyttöalueeseen seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="5ef19-267">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="5ef19-268">Laajenna **Tietolähdetyypit**-ruudussa **Funktiot**-nimike ja valitse **Laskettu kenttä** -nimike.</span><span class="sxs-lookup"><span data-stu-id="5ef19-268">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="5ef19-269">Valitse **Tietolähteet**-ruudusta **VendTable**-nimike.</span><span class="sxs-lookup"><span data-stu-id="5ef19-269">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="5ef19-270">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-270">Select **Add**.</span></span>
    4. <span data-ttu-id="5ef19-271">Kirjoita **Nimi**-kenttään **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-271">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="5ef19-272">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-272">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="5ef19-273">Kirjoita **Kaava**-kenttään **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-273">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="5ef19-274">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-274">Select **Save**.</span></span>
    8. <span data-ttu-id="5ef19-275">Sulje **Kaavaeditori**-sivu.</span><span class="sxs-lookup"><span data-stu-id="5ef19-275">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="5ef19-276">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-276">Click **OK**.</span></span>

3. <span data-ttu-id="5ef19-277">Suorita **\$TransType**-kentän tallentaminen välimuistiin seuraavien vaiheiden mukaisesti:</span><span class="sxs-lookup"><span data-stu-id="5ef19-277">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="5ef19-278">Valitse **LedgerTransTypeList**-nimike.</span><span class="sxs-lookup"><span data-stu-id="5ef19-278">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="5ef19-279">Valitse **Välimuisti**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-279">Select **Cache**.</span></span>
    3. <span data-ttu-id="5ef19-280">Valitse **VendTable.\$TransType**-nimike.</span><span class="sxs-lookup"><span data-stu-id="5ef19-280">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="5ef19-281">Valitse **Välimuisti**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-281">Select **Cache**.</span></span>

    ![$TransType-kentän asetusten tallentaminen välimuistiin](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="5ef19-283">Näiden vaiheiden avulla voit muuttaa **\$TransTypeRecord**-kenttää siten, että se alkaa käyttää välimuistissa olevaa **\$TransType**-kenttää:</span><span class="sxs-lookup"><span data-stu-id="5ef19-283">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="5ef19-284">Laajenna **Tietolähteet**-ruudussa **VendTable**-nimike, laajenna **\<Suhteet**-nimike, laajenna **VendTrans.VendTable\_AccountNum**-nimike ja valitse **VendTable. VendTrans. VendTable\_AccountNum.\$Transtyperecord** -nimike.</span><span class="sxs-lookup"><span data-stu-id="5ef19-284">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="5ef19-285">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-285">Select **Edit**.</span></span>
    3. <span data-ttu-id="5ef19-286">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-286">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="5ef19-287">Etsi **Kaava**-kentästä seuraava lauseke:</span><span class="sxs-lookup"><span data-stu-id="5ef19-287">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="5ef19-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="5ef19-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="5ef19-289">Syötä **Kaava**-kenttään seuraava lauseke:</span><span class="sxs-lookup"><span data-stu-id="5ef19-289">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="5ef19-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="5ef19-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="5ef19-291">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-291">Select **Save**.</span></span>
    7. <span data-ttu-id="5ef19-292">Sulje **Kaavaeditori**-sivu.</span><span class="sxs-lookup"><span data-stu-id="5ef19-292">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="5ef19-293">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-293">Select **OK**.</span></span>

5. <span data-ttu-id="5ef19-294">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-294">Select **Save**.</span></span>
6. <span data-ttu-id="5ef19-295">Sulje **Mallimäärityksen sunnittelun** sivu.</span><span class="sxs-lookup"><span data-stu-id="5ef19-295">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="5ef19-296">Sulje **Mallimääritykset**-sivu.</span><span class="sxs-lookup"><span data-stu-id="5ef19-296">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="5ef19-297">ER-mallin yhdistämismäärityksen muokatun version täydentäminen</span><span class="sxs-lookup"><span data-stu-id="5ef19-297">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="5ef19-298">Valitse RCS-järjestelmän **Konfiguraatiot**-sivun **Versiot**-pikavälilehdessä **Suorituskyvyn jäljityksen** määrityksen versio **1.2**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-298">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="5ef19-299">Valitse **Muutoksen tila**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-299">Select **Change status**.</span></span>
3. <span data-ttu-id="5ef19-300">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-300">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a><span data-ttu-id="5ef19-301">Tuo muokattu ER-mallin yhdistämismääritys RCS:stä sovellukseen</span><span class="sxs-lookup"><span data-stu-id="5ef19-301">Import the modified ER model mapping configuration from RCS into the application</span></span>

<span data-ttu-id="5ef19-302">Toista tämän aiheen [Tuo ER-konfiguraatio RCS:stä Finance and Operationsiin](#import-configuration) -osiossa kuvatut vaiheet tuodaksesi **Suorituskyvyn jäljityskartoitus** -konfiguraation version 1.2.</span><span class="sxs-lookup"><span data-stu-id="5ef19-302">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="5ef19-303">Muokatun ER-ratkaisun suorittaminen jäljityksen suorittamista varten</span><span class="sxs-lookup"><span data-stu-id="5ef19-303">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="5ef19-304">Suorita ER-muoto</span><span class="sxs-lookup"><span data-stu-id="5ef19-304">Run the ER format</span></span>

<span data-ttu-id="5ef19-305">Luo uusi suoritusjälki [Suorita ER-muoto](#run-format) toistamalla tämän aiheen aikaisemmissa jaksoissa esitetyt vaiheet.</span><span class="sxs-lookup"><span data-stu-id="5ef19-305">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="5ef19-306">Suorituksen jäljityksen tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="5ef19-306">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><span data-ttu-id="5ef19-307">Vie luotu jäljitys sovelluksesta</span><span class="sxs-lookup"><span data-stu-id="5ef19-307">Export the generated trace from the application</span></span>

<span data-ttu-id="5ef19-308">Toista tämän aiheen [Vie luotu jäljitys sovelluksesta](#export-trace) -osiossa kuvatut vaiheet tallentaaksesi uuden suorituskyvyn jäljityksen paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="5ef19-308">Repeat the steps in the [Export the generated trace from the application](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="5ef19-309">Tuo tuotettu jälki RCS:ään.</span><span class="sxs-lookup"><span data-stu-id="5ef19-309">Import the generated trace into RCS</span></span>

<span data-ttu-id="5ef19-310">Toista tässä osassa aiemmin kerrotut vaiheet [Tuo luodut jäljet RCS](#import-trace) tuodaksesi uudet suorituskykyjäljet RCS:ään.</span><span class="sxs-lookup"><span data-stu-id="5ef19-310">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="5ef19-311">Suorituskyvyn seurannan käyttäminen RCS:ssä – Mallin määritys</span><span class="sxs-lookup"><span data-stu-id="5ef19-311">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="5ef19-312">Suorita aiemmin tämän ohjeaiheen [Suorituskyvyn seurannan käyttäminen RCS:ssä – Mallin määritys](#use-trace) -osassa kuvatut suorituskyvyn jäljitys -kohdan vaiheet, kun haluat analysoida viimeisimmän suorituskyvyn jäljityksen.</span><span class="sxs-lookup"><span data-stu-id="5ef19-312">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="5ef19-313">Huomaa, että mallimääritykseen tehdyt oikaisut ovat poistaneet tietokannasta päällekkäisiä kyselyitä.</span><span class="sxs-lookup"><span data-stu-id="5ef19-313">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="5ef19-314">Tämän mallimäärityksen tietokantataulukoihin ja tietolähteisiin tehtyjen kutsujen määrä on myös vähennetty.</span><span class="sxs-lookup"><span data-stu-id="5ef19-314">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="5ef19-315">Näin ollen koko ER-ratkaisun suorituskyky on parantunut.</span><span class="sxs-lookup"><span data-stu-id="5ef19-315">Therefore, the performance of the whole ER solution has improved.</span></span>

![Jäljitä tietoja VendTable-tietolähteestä RCS-mallin mallinmäärityssuunnittelija-sivulta](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="5ef19-317">Jäljitystiedoissa VendTable-tietolähteen arvo **\[12\]** ilmaisee, että tätä tietolähdettä kutsuttiin 12 kertaa.</span><span class="sxs-lookup"><span data-stu-id="5ef19-317">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="5ef19-318">Arvo **\[Q:6\]** ilmaisee, että tietokantakutsuille on käännetty kuusi kutsua VendTable-tauluun.</span><span class="sxs-lookup"><span data-stu-id="5ef19-318">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="5ef19-319">Arvo **\[C:6\]** ilmaisee, että tietokannasta noudetut tiedot tallennettiin välimuistiin ja kuusi muuta kutsua käsiteltiin välimuistin avulla.</span><span class="sxs-lookup"><span data-stu-id="5ef19-319">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="5ef19-320">Huomaa, että LedgerTransTypeList-tietolähteeseen soitettujen kutsujen määrä on vähentynyt 9 027:sta 240:een.</span><span class="sxs-lookup"><span data-stu-id="5ef19-320">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![Jäljitä tietoja LedgerTransTypeList-tietolähteestä RCS-mallin mallinmäärityssuunnittelija-sivulta](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a><span data-ttu-id="5ef19-322">Tarkasta suorituksen jäljitys sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="5ef19-322">Review the execution trace in the application</span></span>

<span data-ttu-id="5ef19-323">RCS:n lisäksi jotkin versiot voivat tarjota ER-kehyssuunnittelijakokemuksen ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="5ef19-323">In addition to RCS, some versions might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="5ef19-324">Näissä versioissa on **Ota käyttöön suunnittelutila** -vaihtoehto, joka voidaan ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="5ef19-324">These versions have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="5ef19-325">Tämä vaihtoehto löytyy **Sähköisen raportoinnin parametrit** -sivun **Yleiset**-välilehdestä, jonka voit avata **Sähköisen raportoinnin** työtilassa.</span><span class="sxs-lookup"><span data-stu-id="5ef19-325">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![Ota käyttöön suunnittelutila -vaihtoehto Sähköisen raportoinnin parametrit- sivulla](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="5ef19-327">Jos käytät jotakin näistä versioista, voit analysoida luotuja suorituskyvyn jäljityksiä suoraan sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="5ef19-327">If you use one of these versions, you can analyze the details of generated performance traces directly in the application.</span></span> <span data-ttu-id="5ef19-328">Sinun ei tarvitse viedä niitä sovelluksesta ja tuoda niitä RCS:ään.</span><span class="sxs-lookup"><span data-stu-id="5ef19-328">You don't have to export them from the application and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="5ef19-329">Suorituksen jäljityksen tarkasteleminen ulkoisten työkalujen avulla</span><span class="sxs-lookup"><span data-stu-id="5ef19-329">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="5ef19-330">Konfiguroi käyttäjäparametrit</span><span class="sxs-lookup"><span data-stu-id="5ef19-330">Configure user parameters</span></span>

1. <span data-ttu-id="5ef19-331">Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-331">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="5ef19-332">Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-332">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="5ef19-333">Valitse **Käyttäjäparametrit** -valintaikkunan **Suorituksen jäljitys** -osan **Suorituksen jäljitys muoto-osan** -kentässä **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-333">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="5ef19-334">Suorita ER-muoto</span><span class="sxs-lookup"><span data-stu-id="5ef19-334">Run the ER format</span></span>

<span data-ttu-id="5ef19-335">Luo uusi suoritusjälki [Suorita ER-muoto](#run-format) toistamalla tämän aiheen aikaisemmissa jaksoissa esitetyt vaiheet.</span><span class="sxs-lookup"><span data-stu-id="5ef19-335">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="5ef19-336">Huomaa, että Internet-selain tarjoaa zip-tiedoston ladattavaksi.</span><span class="sxs-lookup"><span data-stu-id="5ef19-336">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="5ef19-337">Tämä tiedosto sisältää suorituskyvyn jäljityksen PerfView-muodossa.</span><span class="sxs-lookup"><span data-stu-id="5ef19-337">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="5ef19-338">Tämän jälkeen voit analysoida ER Format Execution -toiminnon tietoja Perxview-suorituskyvyn analysointityökalun avulla.</span><span class="sxs-lookup"><span data-stu-id="5ef19-338">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>

![Suoritetun ER-muodon jäljitystiedot PerfView-muodossa](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a><span data-ttu-id="5ef19-340">Tietokantakyselyjä sisältävän suorituksen jäljityksen tarkastelemisen arviointi ulkoisilla työkaluilla</span><span class="sxs-lookup"><span data-stu-id="5ef19-340">Use external tools to review an execution trace that includes database queries</span></span>

<span data-ttu-id="5ef19-341">ER-kehykseen tehtyjen parannusten ansiosta PerfView-muodossa luotu suorituskyvyn jäljitys sisältää nyt enemmän tietoja ER-muodon suorittamisesta.</span><span class="sxs-lookup"><span data-stu-id="5ef19-341">Because of improvements that have been made to the ER framework, the performance trace that is generated in PerfView format now offers more details about ER format execution.</span></span> <span data-ttu-id="5ef19-342">Microsoft Dynamics 365 for Finance and Operations -versiossa 10.0.4 (heinäkuu 2019) tämä jäljitys voi sisältää myös tietoja suoritetuista sovellustietokannan SQL-kyselyistä.</span><span class="sxs-lookup"><span data-stu-id="5ef19-342">In Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019), this trace can also include details of executed SQL queries to the application database.</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="5ef19-343">Konfiguroi käyttäjäparametrit</span><span class="sxs-lookup"><span data-stu-id="5ef19-343">Configure user parameters</span></span>

1. <span data-ttu-id="5ef19-344">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-344">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="5ef19-345">Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-345">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="5ef19-346">Määritä seuraavat parametrit **Käyttäjäparametrit**-valintaikkunan **Suorituksen jäljitys** -osassa:</span><span class="sxs-lookup"><span data-stu-id="5ef19-346">In the **User parameters** dialog box, in the **Execution tracing** section, set the following parameters:</span></span>

    - <span data-ttu-id="5ef19-347">Valitse **Suorituksen jäljitysmuoto** -kentässä **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-347">In the **Execution trace format** field, select **PerfView XML**.</span></span>
    - <span data-ttu-id="5ef19-348">Määritä **Kerää kyselytilastot** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-348">Set the **Collect query statistics** option to **Yes**.</span></span>
    - <span data-ttu-id="5ef19-349">Määritä **Jäljitä kysely** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="5ef19-349">Set the **Trace query** option to **Yes**.</span></span>

    ![Käyttäjän parametrit -valintaikkuna](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a><span data-ttu-id="5ef19-351">Suorita ER-muoto</span><span class="sxs-lookup"><span data-stu-id="5ef19-351">Run the ER format</span></span>

<span data-ttu-id="5ef19-352">Luo uusi suoritusjälki [Suorita ER-muoto](#run-format) toistamalla tämän aiheen aikaisemmissa jaksoissa esitetyt vaiheet.</span><span class="sxs-lookup"><span data-stu-id="5ef19-352">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="5ef19-353">Huomaa, että Internet-selain tarjoaa zip-tiedoston ladattavaksi.</span><span class="sxs-lookup"><span data-stu-id="5ef19-353">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="5ef19-354">Tämä tiedosto sisältää suorituskyvyn jäljityksen PerfView-muodossa.</span><span class="sxs-lookup"><span data-stu-id="5ef19-354">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="5ef19-355">Tämän jälkeen voit analysoida ER Format Execution -toiminnon tietoja Perxview-suorituskyvyn analysointityökalun avulla.</span><span class="sxs-lookup"><span data-stu-id="5ef19-355">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span> <span data-ttu-id="5ef19-356">Tämä jäljitys sisältää nyt tiedot SQL-tietokannan käytöstä ER-muodon suorittamisen aikana.</span><span class="sxs-lookup"><span data-stu-id="5ef19-356">This trace now includes the details of SQL database access during the execution of the ER format.</span></span>

![Suoritetun ER-muodon jäljitystiedot PerfView-muodossa](./media/GER-PerfTrace2-PerfViewTrace2.PNG)
