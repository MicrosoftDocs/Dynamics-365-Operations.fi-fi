---
title: Sähköisen raportoinnin muotojen suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi
description: Tässä ohjeaiheessa on tietoja suorituskykyongelmien vianmäärityksestä sähköisen raportoinnin (ER) suorituskyvyn jäljitystoiminnon avulla.
author: NickSelin
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7fbec962fea374afdbabaad48a42dad380708678
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295570"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="6661f-103">Sähköisen raportoinnin muotojen suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi</span><span class="sxs-lookup"><span data-stu-id="6661f-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6661f-104">Osana sähköisten raportointikonfiguraatioiden suunnittelua sähköisten asiakirjojen luomista varten määritetään menetelmä, jonka avulla tiedot haetaan sovelluksesta ja syötetään luotavaan tuotokseen.</span><span class="sxs-lookup"><span data-stu-id="6661f-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="6661f-105">ER Performance Trace -toiminto auttaa vähentämään huomattavasti aikaa ja kustannuksia, jotka liittyvät ER-muodon suorituksen yksityiskohtien keräämiseen ja niiden käyttämiseen suorituskykyongelmien vianmäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="6661f-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="6661f-106">Tässä opetusohjelmassa on ohjeita siitä, miten suorituskykyä voidaan seurata suoritettavissa ER-muodoissa ja miten suorituskykyä voidaan parantaa näiden jälkien tietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="6661f-106">This tutorial provides guidelines about how to take performance traces for executed ER formats, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6661f-107">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="6661f-107">Prerequisites</span></span>

<span data-ttu-id="6661f-108">Tämän opetusohjelman esimerkkien suorittaminen edellyttää seuraavia käyttöoikeuksia:</span><span class="sxs-lookup"><span data-stu-id="6661f-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="6661f-109">Jonkin seuraavien roolien käyttöoikeus:</span><span class="sxs-lookup"><span data-stu-id="6661f-109">Access to one of the following roles:</span></span>

    - <span data-ttu-id="6661f-110">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="6661f-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="6661f-111">Sähköisen raportoinnin toiminnallinen konsultti</span><span class="sxs-lookup"><span data-stu-id="6661f-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="6661f-112">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="6661f-112">System administrator</span></span>

- <span data-ttu-id="6661f-113">Käyttöoikeus Regulatory Configuration Services (RCS) -esiintymään, joka on valmisteltu samalle vuokralaiselle kuin sovellus, jollekin seuraavista rooleista:</span><span class="sxs-lookup"><span data-stu-id="6661f-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as the application, for one of the following roles:</span></span>

    - <span data-ttu-id="6661f-114">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="6661f-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="6661f-115">Sähköisen raportoinnin toiminnallinen konsultti</span><span class="sxs-lookup"><span data-stu-id="6661f-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="6661f-116">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="6661f-116">System administrator</span></span>

<span data-ttu-id="6661f-117">Seuraavat tiedostot täytyy myös ladata ja tallentaa paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="6661f-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="6661f-118">Tiedosto</span><span class="sxs-lookup"><span data-stu-id="6661f-118">File</span></span>                                  | <span data-ttu-id="6661f-119">Sisältö</span><span class="sxs-lookup"><span data-stu-id="6661f-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="6661f-120">Suorituskyvyn jäljitysmalli.versio.1</span><span class="sxs-lookup"><span data-stu-id="6661f-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="6661f-121">Esimerkin ER-tietomallin konfigurointi</span><span class="sxs-lookup"><span data-stu-id="6661f-121">Sample ER data model configuration</span></span>](https://download.microsoft.com/download/0/a/a/0aa84e48-8040-4c46-b542-e3bf15c9b2ad/Performancetracemodelversion.1.xml)    |
| <span data-ttu-id="6661f-122">Suorituskyvyn jäljitysmetadata.versio.1</span><span class="sxs-lookup"><span data-stu-id="6661f-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="6661f-123">Esimerkin ER-metadatan konfigurointi</span><span class="sxs-lookup"><span data-stu-id="6661f-123">Sample ER metadata configuration</span></span>](https://download.microsoft.com/download/a/9/3/a937e8c4-1f8a-43e4-83ee-7d599cf7d983/Performancetracemetadataversion.1.xml)      |
| <span data-ttu-id="6661f-124">Suorituskyvyn jäljitysmapping.versio.1</span><span class="sxs-lookup"><span data-stu-id="6661f-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="6661f-125">Esimerkin ER-mallikartoituksen konfigurointi</span><span class="sxs-lookup"><span data-stu-id="6661f-125">Sample ER model mapping configuration</span></span>](https://download.microsoft.com/download/7/7/3/77379bdc-7b22-4cfc-9b64-a9147599f931/Performancetracemappingversion1.1.xml) |
| <span data-ttu-id="6661f-126">Suorituskyvyn jäljitysformat.versio.1</span><span class="sxs-lookup"><span data-stu-id="6661f-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="6661f-127">Esimerkin ER-format-konfigurointi</span><span class="sxs-lookup"><span data-stu-id="6661f-127">Sample ER format configuration</span></span>](https://download.microsoft.com/download/8/6/8/868ba581-5a06-459e-b173-fb00f038b37f/Performancetraceformatversion1.1.xml)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="6661f-128">Konfiguroi ER-parametrit</span><span class="sxs-lookup"><span data-stu-id="6661f-128">Configure ER parameters</span></span>

<span data-ttu-id="6661f-129">Jokainen sovelluksessa luotu ER-suorituskykyjäljitys tallennetaan suorituslokitietueen liitteenä.</span><span class="sxs-lookup"><span data-stu-id="6661f-129">Each ER performance trace that is generated in the application is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="6661f-130">Näiden liitteiden hallinnassa käytetään tiedostojen hallinnan (DM) kehystä.</span><span class="sxs-lookup"><span data-stu-id="6661f-130">The Document management (DM) framework is used to manage these attachments.</span></span> <span data-ttu-id="6661f-131">Sinun on määritettävä ER-parametrit etukäteen ja määritettävä DM-tiedosto tyyppi, jota käytetään suorituskykyjälkien liittämiseen.</span><span class="sxs-lookup"><span data-stu-id="6661f-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="6661f-132">Valitse **Sähköinen raportointi** -työtilasta **Sähköisen raportoinnin parametrit**.</span><span class="sxs-lookup"><span data-stu-id="6661f-132">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="6661f-133">Valitse sitten **Sähköisen raportoinnin parametrit** -sivun **Liitteet**-välilehden **Muut**-kentästä suorituskyvyn jäljille käytettävä DM-tiedostotyyppi.</span><span class="sxs-lookup"><span data-stu-id="6661f-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Sähköisen raportoinnin parametrit -sivu](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="6661f-135">Jos haluat olla käytettävissä **Muut** -hakukentässä, DM-tiedostotyyppi on konfiguroitava seuraavalla tavalla **Asiakirjatyypit**-sivulla (**Organisaation hallinta \> Asiakirjan hallinta \> Asiakirjatyypit**):</span><span class="sxs-lookup"><span data-stu-id="6661f-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="6661f-136">**Luokka:** Liitä tiedosto</span><span class="sxs-lookup"><span data-stu-id="6661f-136">**Class:** Attach file</span></span>
- <span data-ttu-id="6661f-137">**Ryhmä:** Tiedosto</span><span class="sxs-lookup"><span data-stu-id="6661f-137">**Group:** File</span></span>

![Asiakirjatyypit-sivu](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="6661f-139">Valitun tiedostotyypin on oltava käytettävissä kaikissa nykyisen esiintymän yrityksissä, koska DM-liitteet ovat yrityskohtaisia.</span><span class="sxs-lookup"><span data-stu-id="6661f-139">The selected document type must be available in every company of the current instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="6661f-140">Konfiguroi RCS-parametrit</span><span class="sxs-lookup"><span data-stu-id="6661f-140">Configure RCS parameters</span></span>

<span data-ttu-id="6661f-141">Luodut ER-suorituskykyjäljet tuodaan RCS:ään analysointia varten käyttämällä ER Format Designeria ja ER Mapping Designeria.</span><span class="sxs-lookup"><span data-stu-id="6661f-141">ER performance traces that are generated will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="6661f-142">Koska ER-suorituskykyjäljet tallennetaan ER-muotoon liittyvän suorituslokitietueen liitteinä, RCS-parametrit on määritettävä etukäteen, jotta voidaan määrittää DM-tiedostotyyppi, jota käytetään suorituskykyjälkien liittämiseen.</span><span class="sxs-lookup"><span data-stu-id="6661f-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="6661f-143">Valitse yrityksellesi määritetyn RCS-esiintymän **Sähköisen raportoinnin** -työtilassa **Sähköiset raportointiparametrit**.</span><span class="sxs-lookup"><span data-stu-id="6661f-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="6661f-144">Valitse sitten **Sähköisen raportoinnin parametrit** -sivun **Liitteet**-välilehden **Muut**-kentästä suorituskyvyn jäljille käytettävä DM-tiedostotyyppi.</span><span class="sxs-lookup"><span data-stu-id="6661f-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Sähköisen raportoinnin parametrit -sivu RCS:ssä](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="6661f-146">Jos haluat olla käytettävissä **Muut** -hakukentässä, DM-tiedostotyyppi on konfiguroitava seuraavalla tavalla **Asiakirjatyypit**-sivulla (**Organisaation hallinta \> Asiakirjan hallinta \> Asiakirjatyypit**):</span><span class="sxs-lookup"><span data-stu-id="6661f-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="6661f-147">**Luokka:** Liitä tiedosto</span><span class="sxs-lookup"><span data-stu-id="6661f-147">**Class:** Attach file</span></span>
- <span data-ttu-id="6661f-148">**Ryhmä:** Tiedosto</span><span class="sxs-lookup"><span data-stu-id="6661f-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="6661f-149">Suunnittele ER-ratkaisu</span><span class="sxs-lookup"><span data-stu-id="6661f-149">Design an ER solution</span></span>

<span data-ttu-id="6661f-150">Oletetaan, että olet aloittanut uuden ER-ratkaisun suunnittelun, joka luo toimittajatapahtumia esittelevän uuden raportin.</span><span class="sxs-lookup"><span data-stu-id="6661f-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="6661f-151">Tällä hetkellä voit etsiä valitun toimittajan tapahtumat **Toimittajatapahtumat**-sivulta (Siirry **Ostoreskontra \> Toimittajat \> Kaikki toimittajat**, valitse toimittaja ja sitten toimintoruudun **Toimittaja**-välilehti kohdassa valitse **Tapahtumat**-ryhmästä **Tapahtumat**).</span><span class="sxs-lookup"><span data-stu-id="6661f-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="6661f-152">Haluat kuitenkin saada kaikki toimittajatapahtumat samaan aikaan yhdessä sähköisessä asiakirjassa XML-muodossa.</span><span class="sxs-lookup"><span data-stu-id="6661f-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="6661f-153">Tämä ratkaisu koostuu useista ER-konfiguraatioista, jotka sisältävät vaaditun tietomallin, metatiedot, mallien yhdistämismääritykset ja muotokomponentit.</span><span class="sxs-lookup"><span data-stu-id="6661f-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="6661f-154">Kirjaudu yrityksen RCS-esiintymään, joka on valmisteltu yrityksellesi.</span><span class="sxs-lookup"><span data-stu-id="6661f-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="6661f-155">Tässä opetusohjelmassa luodaan ja muokataan konfiguraatioita malliyritykselle **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="6661f-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="6661f-156">Varmista siksi, että tämä konfigurointipalvelu on lisätty RCS-järjestelmään ja valittu aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="6661f-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="6661f-157">Lisätietoja on kohdassa [Luo konfigurointipalvelut ja merkitse ne aktiivisiksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) menettelyiksi.</span><span class="sxs-lookup"><span data-stu-id="6661f-157">For instructions, see the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>
3. <span data-ttu-id="6661f-158">Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="6661f-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="6661f-159">Tuo **Konfiguraatiot** -sivulla lataamasi ER-kokoonpanot RCS-edellytyksenä seuraavassa järjestyksessä: tietomalli, metatiedot, mallikartoitus, muoto.</span><span class="sxs-lookup"><span data-stu-id="6661f-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="6661f-160">Luo kukin mukautus seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6661f-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="6661f-161">Valitse toimintoruudusta **Vaihda \> Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="6661f-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="6661f-162">Valitse haluamasi ER-kokoonpanon tiedosto XML-muodossa valitsemalla **Selaa**.</span><span class="sxs-lookup"><span data-stu-id="6661f-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="6661f-163">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6661f-163">Select **OK**.</span></span>

    ![Konfiguroinnit-sivu RCS:ssä](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="6661f-165">ER-ratkaisun suorittaminen jäljityksen suorittamista varten</span><span class="sxs-lookup"><span data-stu-id="6661f-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="6661f-166">Oletetaan, että olet suunnitellut ER-ratkaisun ensimmäisen version.</span><span class="sxs-lookup"><span data-stu-id="6661f-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="6661f-167">Nyt haluat testata sitä esiintymässäsi ja analysoida suorituskykyä.</span><span class="sxs-lookup"><span data-stu-id="6661f-167">You now want to test it in your instance and analyze execution performance.</span></span>

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a><span data-ttu-id="6661f-168">Sähköisen raportoinnin konfiguraation tuominen RCS:stä Finance and Operations -sovellukseen</span><span class="sxs-lookup"><span data-stu-id="6661f-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="6661f-169">Kirjaudu sisään sovelluksen esiintymään.</span><span class="sxs-lookup"><span data-stu-id="6661f-169">Sign in to your application instance.</span></span>
2. <span data-ttu-id="6661f-170">Tämän opetusohjelman avulla voit tuoda konfiguraatiot RCS-esiintymästäsi (jossa suunnittelet ER-komponentteja) esiintymääsi (jossa testaat ja lopulta käytät niitä).</span><span class="sxs-lookup"><span data-stu-id="6661f-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your instance (where you test and finally use them).</span></span> <span data-ttu-id="6661f-171">Siksi on varmistettava, että kaikki vaaditut tiedot on valmisteltu.</span><span class="sxs-lookup"><span data-stu-id="6661f-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="6661f-172">Ohjeita on kohdassa [Sähköisen raportoinnin konfiguraatioiden tuonti Regulatory Configuration Services (RCS) -palvelusta](rcs-download-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="6661f-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md) procedure.</span></span>
3. <span data-ttu-id="6661f-173">Seuraavien vaiheiden mukaisesti voit tuoda konfiguraatiot RCS:stä sovellukseen:</span><span class="sxs-lookup"><span data-stu-id="6661f-173">Follow these steps to import the configurations from RCS into the application:</span></span>

    1. <span data-ttu-id="6661f-174">Valitse **Sähköisen raportoinnin** työtilassa **Litware, Inc**-määrityspalveluruudussa **Arkistot**.</span><span class="sxs-lookup"><span data-stu-id="6661f-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="6661f-175">Valitse **Konfiguraatiosäilö**-sivun ruudukossa oleva säilö, jonka tyyppi on **RCS** ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="6661f-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="6661f-176">Valitse **Konfiguraatiot**-pikavälilehdessä **Suorituskyvyn jäljitysmuodon** konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="6661f-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="6661f-177">Valitse **Versiot**-pikavälilehdellä valitun konfiguraation versio **1.1** ja valitse sitten **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="6661f-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![Konfiguraatiosäilön sivu](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="6661f-179">Tietomallin ja mallin yhdistämismääritysten vastaavat versiot tuodaan automaattisesti valmiiksi tuodun ER-muodon konfiguroinnin edellytyksinä.</span><span class="sxs-lookup"><span data-stu-id="6661f-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="6661f-180">ER-suorituskykyjäljityksen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="6661f-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="6661f-181">Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="6661f-181">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="6661f-182">Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.</span><span class="sxs-lookup"><span data-stu-id="6661f-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="6661f-183">Toimi **Käyttäjäparametrit**-valintaikkunan **Suorituksen jäljitys** -osassa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6661f-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="6661f-184">**Suorituksen jäljitysmuoto** -kentän avulla voit määrittää sen luodun suorituskykyjäljityksen muodon, johon suoritustiedot tulee tallentaa ER-ja Mapping-elementeissä:</span><span class="sxs-lookup"><span data-stu-id="6661f-184">In the **Execution trace format** field, specify the format of the generated performance trace that the execution details should be stored in for ER format and mapping elements:</span></span>

        - <span data-ttu-id="6661f-185">**Virheenkorjauksen jäljitysmuoto** – Valitse tämä arvo, jos aiot suorittaa vuorovaikutteisesti ER-muodon, jolla on lyhyt suoritusaika.</span><span class="sxs-lookup"><span data-stu-id="6661f-185">**Debug trace format** – Select this value if you plan to interactively run an ER format that has a short execution time.</span></span> <span data-ttu-id="6661f-186">Tämän jälkeen aloitetaan ER-muodon suorittamista koskevat tiedot.</span><span class="sxs-lookup"><span data-stu-id="6661f-186">The collection of details about ER format execution is then started.</span></span> <span data-ttu-id="6661f-187">Kun tämä arvo valitaan, suorituskyvyn jäljitys kerää seuraaviin toimiin kuluvaa aikaa koskevia tietoja:</span><span class="sxs-lookup"><span data-stu-id="6661f-187">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="6661f-188">Kunkin tietolähteen suorittamista mallikartoituksista, joita kutsutaan tietojen hakemiseksi</span><span class="sxs-lookup"><span data-stu-id="6661f-188">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="6661f-189">Kunkin muotoilunimikkeen käsitteleminen siten, että se syöttää tietoja luotavalle tulosteelle</span><span class="sxs-lookup"><span data-stu-id="6661f-189">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="6661f-190">Jos valitset **virheenkorjauksen jäljitysmuodon** arvon, voit analysoida jäljityksen sisältöä ER:n toiminnan suunnitteluohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="6661f-190">If you select the **Debug trace format** value, you can analyze the content of the trace in the ER Operation designer.</span></span> <span data-ttu-id="6661f-191">Siinä voit tarkastella ER-muotoisia tai määrityselementtejä, jotka on mainittu jäljityksessä.</span><span class="sxs-lookup"><span data-stu-id="6661f-191">There, you can view the ER format or mapping elements that are mentioned in the trace.</span></span>

        - <span data-ttu-id="6661f-192">**Koostettu jäljitysmuoto** – Valitse tämä arvo, jos aiot suorittaa vuorovaikutteisesti ER-muodon, jolla on pitkä suoritusaika erätilassa.</span><span class="sxs-lookup"><span data-stu-id="6661f-192">**Aggregated trace format** – Select this value if you plan to run an ER format that has a long execution time in batch mode.</span></span> <span data-ttu-id="6661f-193">Tämän jälkeen aloitetaan ER-muodon suorittamista koskevat koostetut tiedot.</span><span class="sxs-lookup"><span data-stu-id="6661f-193">The collection of the aggregated details about ER format execution is then started.</span></span> <span data-ttu-id="6661f-194">Kun tämä arvo valitaan, suorituskyvyn jäljitys kerää seuraaviin toimiin kuluvaa aikaa koskevia tietoja:</span><span class="sxs-lookup"><span data-stu-id="6661f-194">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="6661f-195">Kunkin tietolähteen suorittamista mallikartoituksista, joita kutsutaan tietojen hakemiseksi</span><span class="sxs-lookup"><span data-stu-id="6661f-195">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="6661f-196">Kunkin tietolähteen suorittamista muotokartoituksista, joita kutsutaan tietojen hakemiseksi</span><span class="sxs-lookup"><span data-stu-id="6661f-196">Running each data source in the format mapping that is called to get data</span></span>
            - <span data-ttu-id="6661f-197">Kunkin muotoilunimikkeen käsitteleminen siten, että se syöttää tietoja luotavalle tulosteelle</span><span class="sxs-lookup"><span data-stu-id="6661f-197">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="6661f-198">**Koostettu jäljitysmuoto** -arvo on käytettävissä Microsoft Dynamics 365 Financen versiossa 10.0.20 ja sitä myöhemmässä versiossa.</span><span class="sxs-lookup"><span data-stu-id="6661f-198">The **Aggregated trace format** value is available in Microsoft Dynamics 365 Finance version 10.0.20 and later.</span></span>

            <span data-ttu-id="6661f-199">Voit tarkastella yhden komponentin kokonaissuorituksen aikaa ER-muodon suunnittelussa ja ER-mallin määrityksen suunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="6661f-199">In the ER format designer and ER model mapping designer, you can view the total execution time for a single component.</span></span> <span data-ttu-id="6661f-200">Lisäksi jäljitys sisältää suoritusta koskevia tietoja, kuten suoritusten määrän sekä yksittäisen suorituksen vähimmäis- ja enimmäisajan.</span><span class="sxs-lookup"><span data-stu-id="6661f-200">Additionally, the trace contains details about the execution, such as the number of executions, and the minimum and maximum time of a single execution.</span></span>

            > [!NOTE]
            > <span data-ttu-id="6661f-201">Jäljitys kerätään jäljitettyjen komponenttien polun perusteella.</span><span class="sxs-lookup"><span data-stu-id="6661f-201">This trace is collected based on the traced components path.</span></span> <span data-ttu-id="6661f-202">Tilastot saattavat olla virheelliset, jos yksi pääkomponentti sisältää useita nimeämättömiä alikomponentteja tai jos useilla alikomponenteilla on sama nimi.</span><span class="sxs-lookup"><span data-stu-id="6661f-202">Therefore, the statistics might be incorrect when a single parent component contains several unnamed child components, or when several child components have the same name.</span></span>

    2. <span data-ttu-id="6661f-203">Määritä seuraavat asetukset: **Kyllä**, jos haluat kerätä tarkempia tietoja ER-mallin kartoituksesta ja ER-muotokomponenttien suorittamisesta.</span><span class="sxs-lookup"><span data-stu-id="6661f-203">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="6661f-204">**Kyselyn tilastotietojen kerääminen** – Kun tämä vaihtoehto on käytössä, suorituskyvyn jäljitys kerää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="6661f-204">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="6661f-205">Tietolähteiden tekemien kutsujen määrä</span><span class="sxs-lookup"><span data-stu-id="6661f-205">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="6661f-206">Tietokantaan lisättyjen toistettujen kutsujen määrä</span><span class="sxs-lookup"><span data-stu-id="6661f-206">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="6661f-207">Tietokantakutsujen tekemiseen käytettävien SQL-lauseiden tiedot</span><span class="sxs-lookup"><span data-stu-id="6661f-207">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="6661f-208">**Jäljitysvälimuistin käyttäminen** – Kun tämä asetus on käytössä, suorituskyvyn jäljitys kerää tietoja ER-mallikartoituksen välimuistin käytöstä.</span><span class="sxs-lookup"><span data-stu-id="6661f-208">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="6661f-209">**Jäljitystietojen käyttö** – Kun tämä asetus on käytössä, suorituskyvyn jäljitys kerää tietoja siitä, kuinka monta käyntiä tietokantaan on tehty tietueluettelotyypin suoritettavissa tietolähteissä.</span><span class="sxs-lookup"><span data-stu-id="6661f-209">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="6661f-210">**Jäljitystietojen luettelointi** – Kun tämä asetus on käytössä, suorituskyvyn jäljitys kerää tietoja siitä, kuinka monta käyntiä tietokantaan on tehty tietueluettelotyypin suoritettavissa tietolähteissä.</span><span class="sxs-lookup"><span data-stu-id="6661f-210">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6661f-211">**Käyttäjäparametrit** -valintaikkunan parametrit koskevat käyttäjää ja nykyistä yritystä.</span><span class="sxs-lookup"><span data-stu-id="6661f-211">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![Käyttäjän parametrit -valintaikkuna](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a><span data-ttu-id="6661f-213">Suorita ER-muoto</span><span class="sxs-lookup"><span data-stu-id="6661f-213">Run the ER format</span></span>

1. <span data-ttu-id="6661f-214">Valitse **DEMF**-yritys.</span><span class="sxs-lookup"><span data-stu-id="6661f-214">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="6661f-215">Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="6661f-215">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="6661f-216">Valitse **Konfiguraatiot**-sivulla konfiguraatiopuussa **Suorituskyvyn jäljitysmuodon** nimike.</span><span class="sxs-lookup"><span data-stu-id="6661f-216">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="6661f-217">Valitse toimintoruudussa **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="6661f-217">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="6661f-218">Huomaa, että luotu tiedosto sisältää tietoja kuuden toimittajan 265-tapahtumista.</span><span class="sxs-lookup"><span data-stu-id="6661f-218">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="6661f-219">Suorituksen jäljityksen tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="6661f-219">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a><span data-ttu-id="6661f-220">Vie luotu jäljitys sovelluksesta</span><span class="sxs-lookup"><span data-stu-id="6661f-220">Export the generated trace from the application</span></span>

<span data-ttu-id="6661f-221">Suorituskykyjäljet irrotetaan lähde-ER-muodosta, ja ne voidaan sarjoittaa ulkoiseen zip-tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="6661f-221">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="6661f-222">Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Määritysten virheenkorjauslokit**.</span><span class="sxs-lookup"><span data-stu-id="6661f-222">Go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="6661f-223">Valitse **Sähköisen raportoinnin ajon lokit** -sivun vasemmanpuoleisen ruudun **Konfiguration nimi** -kentässä **Suorituskyvyn jäljitysmuoto** jos haluat löytää lokitiedostot, jotka on luotu **Suoritus kyvyn jäljitysmuodon** konfiguraatiolle.</span><span class="sxs-lookup"><span data-stu-id="6661f-223">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="6661f-224">Valitse **Liitteet**-painikkeen sivun oikeassa yläkulmassa (paperiliitinsymboli) tai paina **Ctrl+Shift+A**.</span><span class="sxs-lookup"><span data-stu-id="6661f-224">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![Liitteet-painike Sähköisen raportoinnin ajolokit -sivulla](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="6661f-226">**Valitse sähköisen raportoinnin ajon lokit** -sivun toimintoruudussa **Avaa**, jos haluat saada suorituskyvyn jäljityksen zip-tiedostona ja tallentaa sen paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="6661f-226">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![Sähköisen raportoinnin ajolokien liitteet](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="6661f-228">Luotu jäljitys viittaa lähde-ER-raporttiin yksilöivän raporttitunnuksen avulla vain **GUID**-muodossa.</span><span class="sxs-lookup"><span data-stu-id="6661f-228">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="6661f-229">Muodon versionumerointia ei oteta huomioon.</span><span class="sxs-lookup"><span data-stu-id="6661f-229">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="6661f-230">Huomaa, että suoritetun ER-muodon ja ER-mallikartoituksen muodostaman suorituskyvyn jäljittämisen välinen yhteys perustuu käytössä olevaan juurihakemistoon ja yhteiseen tietomalliin.</span><span class="sxs-lookup"><span data-stu-id="6661f-230">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="6661f-231">Muodon versionumerointia ja mallin yhdistämistä ei oteta huomioon.</span><span class="sxs-lookup"><span data-stu-id="6661f-231">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="6661f-232">Mallimerkinnän **oletusarvoa mallimerkintää varten** ei myöskään oteta huomioon.</span><span class="sxs-lookup"><span data-stu-id="6661f-232">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a><span data-ttu-id="6661f-233">Tuo tuotettu jälki RCS:ään.</span><span class="sxs-lookup"><span data-stu-id="6661f-233">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="6661f-234">Valitse RCS:ssä **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="6661f-234">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="6661f-235">Laajenna **Konfiguraatiot**-sivun konfiguraatiopuussa **Suorituskyvyn jäljitysmalli** -nimike ja valitse **Suorituskyvyn seurannan muoto** -nimike.</span><span class="sxs-lookup"><span data-stu-id="6661f-235">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="6661f-236">Valitse toimintoruudussa **Suunnittelija**.</span><span class="sxs-lookup"><span data-stu-id="6661f-236">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="6661f-237">Valitse **Muodon suunnittelija**-sivulla hallintapaneelista **Suorituskyvyn jäljitysmuoto**.</span><span class="sxs-lookup"><span data-stu-id="6661f-237">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="6661f-238">Valitse **Suorituskyvyn jäljitystulosten asetukset** -valintaikkunasta **Tuo suorituskyvyn jäljitys**.</span><span class="sxs-lookup"><span data-stu-id="6661f-238">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="6661f-239">Valitse **Selaa** valitaksesi aiemmin viemäsi zip-tiedoston.</span><span class="sxs-lookup"><span data-stu-id="6661f-239">Select **Browse** to select the zip file that you exported earlier.</span></span>
7. <span data-ttu-id="6661f-240">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6661f-240">Select **OK**.</span></span>

    ![Suorituskyvyn jäljitystulosten asetukset -valintaikkuna RCS-kohteessa](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="6661f-242">Suorituskyvyn seurannan käyttäminen RCS – Format -suoritusanalyysissä</span><span class="sxs-lookup"><span data-stu-id="6661f-242">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="6661f-243">Laajenna kaikkien muotoilukohteiden sisältö valitsemalla **Laajenna/tiivistä**-vaihtoehto **Muodon suunnittelija**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="6661f-243">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="6661f-244">Huomaa, että joistakin nykyisen muodon kohteista näytetään lisätietoja:</span><span class="sxs-lookup"><span data-stu-id="6661f-244">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="6661f-245">Todellinen aika, joka käytettiin tietojen syöttämiseen luotuun tulosteeseen kohteen muotoilun avulla</span><span class="sxs-lookup"><span data-stu-id="6661f-245">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="6661f-246">Sama aika ilmaistaan prosentteina kokonaisajasta, joka käytettiin koko tuotoksen tuottamiseen.</span><span class="sxs-lookup"><span data-stu-id="6661f-246">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![Muodon suunnittelutoiminto -sivu RCS:ssä](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="6661f-248">Sulje **Muodon suunnittelutoiminto** -sivu.</span><span class="sxs-lookup"><span data-stu-id="6661f-248">Close **Format designer** page.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a><span data-ttu-id="6661f-249">Suorituskyvyn seurannan käyttäminen RCS:ssä – Mallin määritys</span><span class="sxs-lookup"><span data-stu-id="6661f-249">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="6661f-250">Valitse RCS:ssä **Konfiguraatiot**-sivulla konfiguraatiopuussa **Suorituskyvyn jäljitysmääritys** -nimike.</span><span class="sxs-lookup"><span data-stu-id="6661f-250">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="6661f-251">Valitse toimintoruudussa **Suunnittelija**.</span><span class="sxs-lookup"><span data-stu-id="6661f-251">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="6661f-252">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="6661f-252">Select **Designer**.</span></span>
4. <span data-ttu-id="6661f-253">Valitse **Mallin määrityssuunnittelija** -sivulla hallintapaneelista **Suorituskyvyn jäljitysmuoto**.</span><span class="sxs-lookup"><span data-stu-id="6661f-253">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="6661f-254">Valitse aiemmin tuotu jäljitys.</span><span class="sxs-lookup"><span data-stu-id="6661f-254">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="6661f-255">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6661f-255">Select **OK**.</span></span>

<span data-ttu-id="6661f-256">Huomaa, että joidenkin nykyisen mallimääritysten tietolähdenimikkeiden käytettävissä on uusia tietoja:</span><span class="sxs-lookup"><span data-stu-id="6661f-256">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="6661f-257">Tietolähteen avulla tietoja haettaessa käytetty todellinen aika</span><span class="sxs-lookup"><span data-stu-id="6661f-257">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="6661f-258">Sama aika ilmaistaan prosentteina kokonaisajasta, joka käytettiin koko mallin määrityksen suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="6661f-258">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="6661f-259">Huomaa, että ER ilmoittaa, että nykyisen mallin yhdistämismääritys kopioi tietokantapyynnöt, kun VendTable/\<Relations/VendTrans\_. VendTable AccountNum-tietolähde suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="6661f-259">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="6661f-260">Tämä päällekkäisyys johtuu siitä, että toimittajatapahtumien luetteloa kutsutaan kaksi kertaa kutakin iteroitua toimittajatietuetta varten:</span><span class="sxs-lookup"><span data-stu-id="6661f-260">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="6661f-261">Yksi kutsu tehdään tietomallin kunkin tapahtuman tietojen syöttämiseen määritettyjen sidosten perusteella.</span><span class="sxs-lookup"><span data-stu-id="6661f-261">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="6661f-262">Yksi kutsu tehdään, kun toimittaja määrittää lasketun määrän tapahtumia toimittajakohtaisesti tietomallissa.</span><span class="sxs-lookup"><span data-stu-id="6661f-262">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![Virheilmoitus tietokantapyyntöjen kopioista RCS-mallin malli kartoituksen suunnittelusivulla](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="6661f-264">Arvo **\[Q:530\]** ilmaisee, että VendTrans-taulua kutsuttiin 530 kertaa palauttamaan kyseisessä taulussa oleva tietue VendTable/\<Relations/VendTrans. VendTable\_AccountNum-tieto lähteeseen.</span><span class="sxs-lookup"><span data-stu-id="6661f-264">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="6661f-265">Arvo **\[530\]** ilmaisee, että VendTable/\<Relations/VendTrans. VendTable\_AccountNum-tietolähdettä kutsuttiin 530 kertaa palaamaan, jolloin tietue palautetaan kyseiseen tietolähteeseen ja sen tiedot syötetään tietomalliin.</span><span class="sxs-lookup"><span data-stu-id="6661f-265">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="6661f-266">Suosittelemme, että käytät VendTable/\<Relations/VendTrans. VendTable\_AccountNum-tietolähteen välimuistia, jotta voit vähentää 265-tapahtumien tietojen saamiseksi tehtyjen kutsujen määrää ja parantaa mallimäärityksen suorituskykyä.</span><span class="sxs-lookup"><span data-stu-id="6661f-266">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="6661f-267">Voi myös olla hyödyllistä vähentää LedgerTransTypeList-tietolähteeseen tehtyjen kutsujen määrää.</span><span class="sxs-lookup"><span data-stu-id="6661f-267">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="6661f-268">Tätä tietolähdettä käytetään liittämään kaikki **lLedgerTransType**-luetteloinnin arvot sen otsikkoon.</span><span class="sxs-lookup"><span data-stu-id="6661f-268">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="6661f-269">Käyttämällä tätä tietolähdettä voit löytää asianmukaisen tunnisteen ja syöttää sen kunkin toimittajatapahtuman tietomalliin.</span><span class="sxs-lookup"><span data-stu-id="6661f-269">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="6661f-270">Tähän tietolähteeseen soitettujen kutsujen määrä (9 027) on melko suuri 265-tapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="6661f-270">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![Mallin määrityksen suunnittelijasivu RCS:ssä näyttää 9 027 puhelua tietolähteeseen](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="6661f-272">Paranna mallin määritystä suorituksen jälkeisten tietojen perusteella</span><span class="sxs-lookup"><span data-stu-id="6661f-272">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="6661f-273">Mallin määrityksen logiikan muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="6661f-273">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="6661f-274">Seuraavia ohjeita noudattamalla voit käyttää välimuistia, joka estää kaksoissoittoja tietokantaan:</span><span class="sxs-lookup"><span data-stu-id="6661f-274">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="6661f-275">Valitse RCS:ssä **Mallin määrityksen suunnittelu** -sivun **Tietolähteet**-ruudusta **VendTable**-nimike.</span><span class="sxs-lookup"><span data-stu-id="6661f-275">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="6661f-276">Valitse **Välimuisti**.</span><span class="sxs-lookup"><span data-stu-id="6661f-276">Select **Cache**.</span></span>
    3. <span data-ttu-id="6661f-277">Laajenna **VendTable**-nimike, laajenna VendTable-tietolähde ( **\<Suhde**-nimike), yksi-moneen-suhteiden luettelo ja valitse **VendTrans.VendTable\_AccountNum**-nimike</span><span class="sxs-lookup"><span data-stu-id="6661f-277">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="6661f-278">Valitse **Välimuisti**.</span><span class="sxs-lookup"><span data-stu-id="6661f-278">Select **Cache**.</span></span>

    ![Asetusten tallentaminen välimuistiin, jotta kaksinkertaiset kutsut voidaan estää](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="6661f-280">Siirrä LedgerTransTypeList-tietolähde VendTable-tietolähteen käyttöalueeseen seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6661f-280">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="6661f-281">Laajenna **Tietolähdetyypit**-ruudussa **Funktiot**-nimike ja valitse **Laskettu kenttä** -nimike.</span><span class="sxs-lookup"><span data-stu-id="6661f-281">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="6661f-282">Valitse **Tietolähteet**-ruudusta **VendTable**-nimike.</span><span class="sxs-lookup"><span data-stu-id="6661f-282">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="6661f-283">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="6661f-283">Select **Add**.</span></span>
    4. <span data-ttu-id="6661f-284">Kirjoita **Nimi**-kenttään **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="6661f-284">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="6661f-285">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="6661f-285">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="6661f-286">Kirjoita **Kaava**-kenttään **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="6661f-286">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="6661f-287">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6661f-287">Select **Save**.</span></span>
    8. <span data-ttu-id="6661f-288">Sulje **Kaavaeditori**-sivu.</span><span class="sxs-lookup"><span data-stu-id="6661f-288">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="6661f-289">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6661f-289">Click **OK**.</span></span>

3. <span data-ttu-id="6661f-290">Suorita **\$TransType**-kentän tallentaminen välimuistiin seuraavien vaiheiden mukaisesti:</span><span class="sxs-lookup"><span data-stu-id="6661f-290">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="6661f-291">Valitse **LedgerTransTypeList**-nimike.</span><span class="sxs-lookup"><span data-stu-id="6661f-291">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="6661f-292">Valitse **Välimuisti**.</span><span class="sxs-lookup"><span data-stu-id="6661f-292">Select **Cache**.</span></span>
    3. <span data-ttu-id="6661f-293">Valitse **VendTable.\$TransType**-nimike.</span><span class="sxs-lookup"><span data-stu-id="6661f-293">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="6661f-294">Valitse **Välimuisti**.</span><span class="sxs-lookup"><span data-stu-id="6661f-294">Select **Cache**.</span></span>

    ![$TransType-kentän asetusten tallentaminen välimuistiin](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="6661f-296">Näiden vaiheiden avulla voit muuttaa **\$TransTypeRecord**-kenttää siten, että se alkaa käyttää välimuistissa olevaa **\$TransType**-kenttää:</span><span class="sxs-lookup"><span data-stu-id="6661f-296">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="6661f-297">Laajenna **Tietolähteet**-ruudussa **VendTable**-nimike, laajenna **\<Suhteet**-nimike, laajenna **VendTrans.VendTable\_AccountNum**-nimike ja valitse **VendTable. VendTrans. VendTable\_AccountNum.\$Transtyperecord** -nimike.</span><span class="sxs-lookup"><span data-stu-id="6661f-297">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="6661f-298">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="6661f-298">Select **Edit**.</span></span>
    3. <span data-ttu-id="6661f-299">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="6661f-299">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="6661f-300">Etsi **Kaava**-kentästä seuraava lauseke:</span><span class="sxs-lookup"><span data-stu-id="6661f-300">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="6661f-301">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="6661f-301">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="6661f-302">Syötä **Kaava**-kenttään seuraava lauseke:</span><span class="sxs-lookup"><span data-stu-id="6661f-302">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="6661f-303">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="6661f-303">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="6661f-304">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6661f-304">Select **Save**.</span></span>
    7. <span data-ttu-id="6661f-305">Sulje **Kaavaeditori**-sivu.</span><span class="sxs-lookup"><span data-stu-id="6661f-305">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="6661f-306">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6661f-306">Select **OK**.</span></span>

5. <span data-ttu-id="6661f-307">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6661f-307">Select **Save**.</span></span>
6. <span data-ttu-id="6661f-308">Sulje **Mallimäärityksen sunnittelun** sivu.</span><span class="sxs-lookup"><span data-stu-id="6661f-308">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="6661f-309">Sulje **Mallimääritykset**-sivu.</span><span class="sxs-lookup"><span data-stu-id="6661f-309">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="6661f-310">ER-mallin yhdistämismäärityksen muokatun version täydentäminen</span><span class="sxs-lookup"><span data-stu-id="6661f-310">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="6661f-311">Valitse RCS-järjestelmän **Konfiguraatiot**-sivun **Versiot**-pikavälilehdessä **Suorituskyvyn jäljityksen** määrityksen versio **1.2**.</span><span class="sxs-lookup"><span data-stu-id="6661f-311">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="6661f-312">Valitse **Muutoksen tila**.</span><span class="sxs-lookup"><span data-stu-id="6661f-312">Select **Change status**.</span></span>
3. <span data-ttu-id="6661f-313">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="6661f-313">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a><span data-ttu-id="6661f-314">Tuo muokattu ER-mallin yhdistämismääritys RCS:stä sovellukseen</span><span class="sxs-lookup"><span data-stu-id="6661f-314">Import the modified ER model mapping configuration from RCS into the application</span></span>

<span data-ttu-id="6661f-315">Toista tämän aiheen [Sähköisen raportoinnin konfiguraation tuominen RCS:stä Finance and Operations -sovellukseen](#import-configuration) -osiossa kuvatut vaiheet tuodaksesi **Suorituskyvyn jäljityskartoitus** -konfiguraation version 1.2.</span><span class="sxs-lookup"><span data-stu-id="6661f-315">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="6661f-316">Muokatun ER-ratkaisun suorittaminen jäljityksen suorittamista varten</span><span class="sxs-lookup"><span data-stu-id="6661f-316">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="6661f-317">Suorita ER-muoto</span><span class="sxs-lookup"><span data-stu-id="6661f-317">Run the ER format</span></span>

<span data-ttu-id="6661f-318">Luo uusi suoritusjälki [Suorita ER-muoto](#run-format) toistamalla tämän aiheen aikaisemmissa jaksoissa esitetyt vaiheet.</span><span class="sxs-lookup"><span data-stu-id="6661f-318">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="work-with-the-execution-trace"></a><span data-ttu-id="6661f-319">Suorituksen jäljityksen käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="6661f-319">Work with the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><span data-ttu-id="6661f-320">Vie luotu jäljitys sovelluksesta</span><span class="sxs-lookup"><span data-stu-id="6661f-320">Export the generated trace from the application</span></span>

<span data-ttu-id="6661f-321">Toista tämän aiheen [Vie luotu jäljitys sovelluksesta](#export-trace) -osiossa kuvatut vaiheet tallentaaksesi uuden suorituskyvyn jäljityksen paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="6661f-321">Repeat the steps in the [Export the generated trace from the application](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="6661f-322">Tuo tuotettu jälki RCS:ään.</span><span class="sxs-lookup"><span data-stu-id="6661f-322">Import the generated trace into RCS</span></span>

<span data-ttu-id="6661f-323">Toista tässä osassa aiemmin kerrotut vaiheet [Tuo luodut jäljet RCS](#import-trace) tuodaksesi uudet suorituskykyjäljet RCS:ään.</span><span class="sxs-lookup"><span data-stu-id="6661f-323">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="6661f-324">Suorituskyvyn seurannan käyttäminen RCS:ssä – Mallin määritys</span><span class="sxs-lookup"><span data-stu-id="6661f-324">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="6661f-325">Suorita aiemmin tämän ohjeaiheen [Suorituskyvyn seurannan käyttäminen RCS:ssä – Mallin määritys](#use-trace) -osassa kuvatut suorituskyvyn jäljitys -kohdan vaiheet, kun haluat analysoida viimeisimmän suorituskyvyn jäljityksen.</span><span class="sxs-lookup"><span data-stu-id="6661f-325">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="6661f-326">Huomaa, että mallimääritykseen tehdyt oikaisut ovat poistaneet tietokannasta päällekkäisiä kyselyitä.</span><span class="sxs-lookup"><span data-stu-id="6661f-326">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="6661f-327">Tämän mallimäärityksen tietokantataulukoihin ja tietolähteisiin tehtyjen kutsujen määrä on myös vähennetty.</span><span class="sxs-lookup"><span data-stu-id="6661f-327">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="6661f-328">Näin ollen koko ER-ratkaisun suorituskyky on parantunut.</span><span class="sxs-lookup"><span data-stu-id="6661f-328">Therefore, the performance of the whole ER solution has improved.</span></span>

![Jäljitä tietoja VendTable-tietolähteestä RCS-mallin mallinmäärityssuunnittelija-sivulta](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="6661f-330">Jäljitystiedoissa VendTable-tietolähteen arvo **\[12\]** ilmaisee, että tätä tietolähdettä kutsuttiin 12 kertaa.</span><span class="sxs-lookup"><span data-stu-id="6661f-330">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="6661f-331">Arvo **\[Q:6\]** ilmaisee, että tietokantakutsuille on käännetty kuusi kutsua VendTable-tauluun.</span><span class="sxs-lookup"><span data-stu-id="6661f-331">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="6661f-332">Arvo **\[C:6\]** ilmaisee, että tietokannasta noudetut tiedot tallennettiin välimuistiin ja kuusi muuta kutsua käsiteltiin välimuistin avulla.</span><span class="sxs-lookup"><span data-stu-id="6661f-332">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="6661f-333">Huomaa, että LedgerTransTypeList-tietolähteeseen soitettujen kutsujen määrä on vähentynyt 9 027:sta 240:een.</span><span class="sxs-lookup"><span data-stu-id="6661f-333">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![Jäljitä tietoja LedgerTransTypeList-tietolähteestä RCS-mallin mallinmäärityssuunnittelija-sivulta](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a><span data-ttu-id="6661f-335">Tarkasta suorituksen jäljitys sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="6661f-335">Review the execution trace in the application</span></span>

<span data-ttu-id="6661f-336">RCS:n lisäksi jotkin versiot voivat tarjota ER-kehyssuunnittelijakokemuksen ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="6661f-336">In addition to RCS, some versions might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="6661f-337">Näissä versioissa on **Ota käyttöön suunnittelutila** -vaihtoehto, joka voidaan ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="6661f-337">These versions have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="6661f-338">Tämä vaihtoehto löytyy **Sähköisen raportoinnin parametrit** -sivun **Yleiset**-välilehdestä, jonka voit avata **Sähköisen raportoinnin** työtilassa.</span><span class="sxs-lookup"><span data-stu-id="6661f-338">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![Ota käyttöön suunnittelutila -vaihtoehto Sähköisen raportoinnin parametrit- sivulla](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="6661f-340">Jos käytät jotakin näistä versioista, voit analysoida luotuja suorituskyvyn jäljityksiä suoraan sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="6661f-340">If you use one of these versions, you can analyze the details of generated performance traces directly in the application.</span></span> <span data-ttu-id="6661f-341">Sinun ei tarvitse viedä niitä sovelluksesta ja tuoda niitä RCS:ään.</span><span class="sxs-lookup"><span data-stu-id="6661f-341">You don't have to export them from the application and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="6661f-342">Suorituksen jäljityksen tarkasteleminen ulkoisten työkalujen avulla</span><span class="sxs-lookup"><span data-stu-id="6661f-342">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="6661f-343">Konfiguroi käyttäjäparametrit</span><span class="sxs-lookup"><span data-stu-id="6661f-343">Configure user parameters</span></span>

1. <span data-ttu-id="6661f-344">Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="6661f-344">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="6661f-345">Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.</span><span class="sxs-lookup"><span data-stu-id="6661f-345">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="6661f-346">Valitse **Käyttäjäparametrit** -valintaikkunan **Suorituksen jäljitys** -osan **Suorituksen jäljitys muoto-osan** -kentässä **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="6661f-346">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="6661f-347">Suorita ER-muoto</span><span class="sxs-lookup"><span data-stu-id="6661f-347">Run the ER format</span></span>

<span data-ttu-id="6661f-348">Luo uusi suoritusjälki [Suorita ER-muoto](#run-format) toistamalla tämän aiheen aikaisemmissa jaksoissa esitetyt vaiheet.</span><span class="sxs-lookup"><span data-stu-id="6661f-348">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="6661f-349">Huomaa, että Internet-selain tarjoaa zip-tiedoston ladattavaksi.</span><span class="sxs-lookup"><span data-stu-id="6661f-349">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="6661f-350">Tämä tiedosto sisältää suorituskyvyn jäljityksen PerfView-muodossa.</span><span class="sxs-lookup"><span data-stu-id="6661f-350">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="6661f-351">Tämän jälkeen voit analysoida ER Format Execution -toiminnon tietoja Perxview-suorituskyvyn analysointityökalun avulla.</span><span class="sxs-lookup"><span data-stu-id="6661f-351">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>

![Suorituskyvyn jäljitystiedot PerfView-muodossa](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a><span data-ttu-id="6661f-353">Tietokantakyselyjä sisältävän suorituksen jäljityksen tarkastelemisen arviointi ulkoisilla työkaluilla</span><span class="sxs-lookup"><span data-stu-id="6661f-353">Use external tools to review an execution trace that includes database queries</span></span>

<span data-ttu-id="6661f-354">ER-kehykseen tehtyjen parannusten ansiosta PerfView-muodossa luotu suorituskyvyn jäljitys sisältää nyt enemmän tietoja ER-muodon suorittamisesta.</span><span class="sxs-lookup"><span data-stu-id="6661f-354">Because of improvements that have been made to the ER framework, the performance trace that is generated in PerfView format now offers more details about ER format execution.</span></span> <span data-ttu-id="6661f-355">Microsoft Dynamics 365 for Finance and Operations -versiossa 10.0.4 (heinäkuu 2019) tämä jäljitys voi sisältää myös tietoja suoritetuista sovellustietokannan SQL-kyselyistä.</span><span class="sxs-lookup"><span data-stu-id="6661f-355">In Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019), this trace can also include details of executed SQL queries to the application database.</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="6661f-356">Konfiguroi käyttäjäparametrit</span><span class="sxs-lookup"><span data-stu-id="6661f-356">Configure user parameters</span></span>

1. <span data-ttu-id="6661f-357">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="6661f-357">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="6661f-358">Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.</span><span class="sxs-lookup"><span data-stu-id="6661f-358">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="6661f-359">Määritä seuraavat parametrit **Käyttäjäparametrit**-valintaikkunan **Suorituksen jäljitys** -osassa:</span><span class="sxs-lookup"><span data-stu-id="6661f-359">In the **User parameters** dialog box, in the **Execution tracing** section, set the following parameters:</span></span>

    - <span data-ttu-id="6661f-360">Valitse **Suorituksen jäljitysmuoto** -kentässä **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="6661f-360">In the **Execution trace format** field, select **PerfView XML**.</span></span>
    - <span data-ttu-id="6661f-361">Määritä **Kerää kyselytilastot** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="6661f-361">Set the **Collect query statistics** option to **Yes**.</span></span>
    - <span data-ttu-id="6661f-362">Määritä **Jäljitä kysely** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="6661f-362">Set the **Trace query** option to **Yes**.</span></span>

    ![Suorituksen jäljitys -osa, Käyttäjän parametrit -valintaruutu](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a><span data-ttu-id="6661f-364">Suorita ER-muoto</span><span class="sxs-lookup"><span data-stu-id="6661f-364">Run the ER format</span></span>

<span data-ttu-id="6661f-365">Luo uusi suoritusjälki [Suorita ER-muoto](#run-format) toistamalla tämän aiheen aikaisemmissa jaksoissa esitetyt vaiheet.</span><span class="sxs-lookup"><span data-stu-id="6661f-365">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="6661f-366">Huomaa, että Internet-selain tarjoaa zip-tiedoston ladattavaksi.</span><span class="sxs-lookup"><span data-stu-id="6661f-366">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="6661f-367">Tämä tiedosto sisältää suorituskyvyn jäljityksen PerfView-muodossa.</span><span class="sxs-lookup"><span data-stu-id="6661f-367">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="6661f-368">Tämän jälkeen voit analysoida ER Format Execution -toiminnon tietoja Perxview-suorituskyvyn analysointityökalun avulla.</span><span class="sxs-lookup"><span data-stu-id="6661f-368">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span> <span data-ttu-id="6661f-369">Tämä jäljitys sisältää nyt tiedot SQL-tietokannan käytöstä ER-muodon suorittamisen aikana.</span><span class="sxs-lookup"><span data-stu-id="6661f-369">This trace now includes the details of SQL database access during the execution of the ER format.</span></span>

![Suoritetun ER-muodon jäljitystiedot PerfView-muodossa](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a><span data-ttu-id="6661f-371">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6661f-371">Additional resources</span></span>

- [<span data-ttu-id="6661f-372">Sähköisen raportoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="6661f-372">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="6661f-373">Paranna sähköisen raportoinnin ratkaisujen suorituskykyä lisäämällä parametrisoidut LASKETTU KENTTÄ -tietolähteet.</span><span class="sxs-lookup"><span data-stu-id="6661f-373">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
