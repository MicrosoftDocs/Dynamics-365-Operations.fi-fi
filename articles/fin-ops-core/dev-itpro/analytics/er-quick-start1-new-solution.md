---
title: Suunnittele uusi ER-ratkaisu mukautetun raportin tulostamiseen
description: Tässä ohjeaiheessa kerrotaan miten ER-ratkaisu mukautetun raportin tulostamiseen suunnitellaan.
author: NickSelin
manager: AnnBe
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cd0d8e7aa9595e705416798772f52956ef609da
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680239"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a><span data-ttu-id="e97c0-103">Suunnittele uusi ER-ratkaisu mukautetun raportin tulostamiseen</span><span class="sxs-lookup"><span data-stu-id="e97c0-103">Design a new ER solution to print a custom report</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e97c0-104">Seuraavissa vaiheissa selitetään, miten järjestelmänvalvoja-, sähköisen raportoinnin kehittäjä- tai sähköisen raportoinnin toiminnallinen konsultti -roolin käyttäjä voi määrittää ER-kehyksen parametrit, suunnitella uuden ER-ratkaisun vaaditut ER-kokoonpanot tietyn yritystoimialueen tietojen käyttöä varten ja luoda mukautetun raportin Microsoft Office -muodossa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-104">The following steps explain how a user in the System Administrator, Electronic Reporting Developer, or Electronic Reporting Functional Consultant role can configure parameters of the ER framework, design the required ER configurations of a new ER solution to access the data of a particular business domain, and generate a custom report in Microsoft Office format.</span></span> <span data-ttu-id="e97c0-105">Nämä vaiheet voidaan suorittaa **USMF**-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-105">These steps can be completed in the **USMF** company.</span></span>

- [<span data-ttu-id="e97c0-106">Määritä ER-kehys</span><span class="sxs-lookup"><span data-stu-id="e97c0-106">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="e97c0-107">Konfiguroi ER-parametrit</span><span class="sxs-lookup"><span data-stu-id="e97c0-107">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="e97c0-108">Aktivoi ER-konfiguraation lähde</span><span class="sxs-lookup"><span data-stu-id="e97c0-108">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="e97c0-109">Tarkista ER-konfiguraation lähteiden luettelo</span><span class="sxs-lookup"><span data-stu-id="e97c0-109">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="e97c0-110">Lisää uusi ER-konfiguraation lähde</span><span class="sxs-lookup"><span data-stu-id="e97c0-110">Add a new ER configuration provider</span></span>](#AddProvider)
        - [<span data-ttu-id="e97c0-111">Aktivoi ER-konfiguraation lähde</span><span class="sxs-lookup"><span data-stu-id="e97c0-111">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="e97c0-112">Toimialuekohtaisen tietomallin suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-112">Design a domain-specific data model</span></span>](#DesignModel)

    - [<span data-ttu-id="e97c0-113">Uuden tietomallimäärityksen tuominen</span><span class="sxs-lookup"><span data-stu-id="e97c0-113">Import a new data model configuration</span></span>](#ImportDataModel)
    - [<span data-ttu-id="e97c0-114">Uuden tietomallin konfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="e97c0-114">Create a new data model configuration</span></span>](#DesignDataModel)

        - [<span data-ttu-id="e97c0-115">Tietomallin nimeäminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-115">Name the data model</span></span>](#NameDataModel)
        - [<span data-ttu-id="e97c0-116">Tietomallikenttien lisääminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-116">Add data model fields</span></span>](#FieldsEntry)
        - [<span data-ttu-id="e97c0-117">Tietomallin rakenteen täydentäminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-117">Complete the design of the data model</span></span>](#CompleteDataModel)

- [<span data-ttu-id="e97c0-118">Mallin määrityksen suunnitteleminen konfiguroidulle tietomallille</span><span class="sxs-lookup"><span data-stu-id="e97c0-118">Design a model mapping for the configured data model</span></span>](#DesignMapping)

    - [<span data-ttu-id="e97c0-119">Uuden mallimäärityksen tuominen</span><span class="sxs-lookup"><span data-stu-id="e97c0-119">Import a new model mapping configuration</span></span>](#ImportModelMapping)
    - [<span data-ttu-id="e97c0-120">Uuden mallin yhdistämismäärityksen luominen</span><span class="sxs-lookup"><span data-stu-id="e97c0-120">Create a new model mapping configuration</span></span>](#CreateModelMapping)

        - [<span data-ttu-id="e97c0-121">Uuden mallimäärityskomponentin suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-121">Design a new model mapping component</span></span>](#DesignMappingComponent)
        - [<span data-ttu-id="e97c0-122">Tietolähteiden lisääminen sovellustaulujen käyttämiseen</span><span class="sxs-lookup"><span data-stu-id="e97c0-122">Add data sources to access application tables</span></span>](#AddMmDataSource1)
        - [<span data-ttu-id="e97c0-123">Tietolähteiden lisääminen sovellusluettelointien käyttämiseen</span><span class="sxs-lookup"><span data-stu-id="e97c0-123">Add data sources to access application enumerations</span></span>](#AddMmDataSource2)
        - [<span data-ttu-id="e97c0-124">Voit luoda raportin määritetyllä kielellä lisäämällä ER-otsikoita</span><span class="sxs-lookup"><span data-stu-id="e97c0-124">Add ER labels to generate a report in a specified language</span></span>](#AddMmLabels)
        - [<span data-ttu-id="e97c0-125">Lisää tietolähde muuntamaan lueteltujen arvojen vertailutulokset tekstiarvoihin</span><span class="sxs-lookup"><span data-stu-id="e97c0-125">Add a data source to transform the results of comparing enumeration values to a text value</span></span>](#AddMmDataSource3)
        - [<span data-ttu-id="e97c0-126">Tietolähteen sitominen tietomallikenttiin</span><span class="sxs-lookup"><span data-stu-id="e97c0-126">Bind data sources to data model fields</span></span>](#AddMmBindings1)
        - [<span data-ttu-id="e97c0-127">Mallin määrityksen rakenteen täydentäminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-127">Complete the design of the model mapping</span></span>](#CompleteModelMapping)

- [<span data-ttu-id="e97c0-128">Mukautetun raportin mallin suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-128">Design a template for a custom report</span></span>](#DesignReportTemplate)
- [<span data-ttu-id="e97c0-129">Muodon suunnittelu</span><span class="sxs-lookup"><span data-stu-id="e97c0-129">Design a format</span></span>](#DesignFormat)

    - [<span data-ttu-id="e97c0-130">Tuo suunniteltu muotokonfiguraatio</span><span class="sxs-lookup"><span data-stu-id="e97c0-130">Import a designed format configuration</span></span>](#FormatImport)
    - [<span data-ttu-id="e97c0-131">Uuden muotokonfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="e97c0-131">Create a new format configuration</span></span>](#FormatCreate)

        - [<span data-ttu-id="e97c0-132">Tuo raporttimalli</span><span class="sxs-lookup"><span data-stu-id="e97c0-132">Import a report template</span></span>](#ImportReportTemplate)
        - [<span data-ttu-id="e97c0-133">Muodon konfigurointi</span><span class="sxs-lookup"><span data-stu-id="e97c0-133">Configure a format</span></span>](#ConfigureFormat)
        - [<span data-ttu-id="e97c0-134">Raportin otsikon tietojen sidonnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-134">Define the data binding for a report title</span></span>](#DefineFormatBindings)
        - [<span data-ttu-id="e97c0-135">Mallin tietolähteen tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-135">Review the model data source</span></span>](#ReviewModelDataSource)
        - [<span data-ttu-id="e97c0-136">Muotoelementtien sidonta tietolähdekenttiin</span><span class="sxs-lookup"><span data-stu-id="e97c0-136">Bind format elements to data source fields</span></span>](#BindFormatElements)

    - [<span data-ttu-id="e97c0-137">Suunnitellun muodon suorittaminen ER-muodosta</span><span class="sxs-lookup"><span data-stu-id="e97c0-137">Run a designed format from ER</span></span>](#RunFormatFromER)

- [<span data-ttu-id="e97c0-138">Suunnitellun muodon säätäminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-138">Tune a designed format</span></span>](#TuneFormat)

    - [<span data-ttu-id="e97c0-139">Tiedostomuodon muokkaaminen luodun tiedoston nimen muuttamista varten</span><span class="sxs-lookup"><span data-stu-id="e97c0-139">Modify a format to change the name of a generated document</span></span>](#ModifyToChangeName)
    - [<span data-ttu-id="e97c0-140">Muodon muokkaaminen muuttamalla kysymysten järjestystä</span><span class="sxs-lookup"><span data-stu-id="e97c0-140">Modify a format to change the order of questions</span></span>](#ModifyToOrder)
    - [<span data-ttu-id="e97c0-141">Muokatun muodon suorittaminen ER-muodosta</span><span class="sxs-lookup"><span data-stu-id="e97c0-141">Run a modified format from ER</span></span>](#RunFormatFromER2)
    - [<span data-ttu-id="e97c0-142">Suunnittele muoto loppuun</span><span class="sxs-lookup"><span data-stu-id="e97c0-142">Complete the format design</span></span>](#CompleteFormat)

- [<span data-ttu-id="e97c0-143">Sovelluksen artefaktien laatiminen suunniteltua raporttia varten</span><span class="sxs-lookup"><span data-stu-id="e97c0-143">Develop application artefacts to call the designed report</span></span>](#DevelopCustomCode)

    - [<span data-ttu-id="e97c0-144">Lähdekoodin muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-144">Modify source code</span></span>](#ModifySourceCode)

        - [<span data-ttu-id="e97c0-145">Tietosopimusluokan lisääminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-145">Add a data contract class</span></span>](#DataContractClass)
        - [<span data-ttu-id="e97c0-146">UI Builder -luokan lisääminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-146">Add a UI builder class</span></span>](#UIBuilderClass)
        - [<span data-ttu-id="e97c0-147">Tietopalveluluokan lisääminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-147">Add a data provider class</span></span>](#DataProviderClass)
        - [<span data-ttu-id="e97c0-148">Käyttöliittymätekstitiedoston lisääminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-148">Add a labels file</span></span>](#LabelsFile)
        - [<span data-ttu-id="e97c0-149">Raporttipalveluluokan lisääminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-149">Add a report service class</span></span>](#ServiceClass)
        - [<span data-ttu-id="e97c0-150">Raportin ohjainluokan lisääminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-150">Add a report controller class</span></span>](#ControllerClass)
        - [<span data-ttu-id="e97c0-151">Valikkovaihtoehdon lisääminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-151">Add a menu item</span></span>](#MenuItem)
        - [<span data-ttu-id="e97c0-152">Valikkovaihtoehdon lisääminen valikkoon</span><span class="sxs-lookup"><span data-stu-id="e97c0-152">Add a menu item to a menu</span></span>](#Menu)
        - [<span data-ttu-id="e97c0-153">Visual Studio -projektin luominen</span><span class="sxs-lookup"><span data-stu-id="e97c0-153">Build a Visual Studio project</span></span>](#BuildVSProject)

    - [<span data-ttu-id="e97c0-154">Muodon suorittaminen sovelluksesta</span><span class="sxs-lookup"><span data-stu-id="e97c0-154">Run a format from the application</span></span>](#RunFormatFromApp)

- [<span data-ttu-id="e97c0-155">Suunnitellun ER-ratkaisun säätäminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-155">Tune a designed ER solution</span></span>](#TuneSolution)

    - [<span data-ttu-id="e97c0-156">Mallin yhdistämismäärityksen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-156">Modify a model mapping</span></span>](#ModifyModelMapping)

        - [<span data-ttu-id="e97c0-157">Tietolähteiden lisääminen tietosopimusobjektien käyttämiseen</span><span class="sxs-lookup"><span data-stu-id="e97c0-157">Add data sources to access a data contract object</span></span>](#AddDataSource1)
        - [<span data-ttu-id="e97c0-158">Tietolähteen lisääminen ER-muotomääritystietueen käyttämiseen</span><span class="sxs-lookup"><span data-stu-id="e97c0-158">Add a data source to access ER format mapping records</span></span>](#AddDataSource2)
        - [<span data-ttu-id="e97c0-159">Tietolähteen lisääminen käynnissä olevan ER-muodon muotomääritystietueen käyttämiseen</span><span class="sxs-lookup"><span data-stu-id="e97c0-159">Add a data source to access a format mapping record of a running ER format</span></span>](#AddDataSource3)
        - [<span data-ttu-id="e97c0-160">Kirjoita suoritettavan ER-muodon nimi tietomalliin</span><span class="sxs-lookup"><span data-stu-id="e97c0-160">Enter the name of the running ER format in the data model</span></span>](#AddBinding)
        - [<span data-ttu-id="e97c0-161">Mallin määrityksen rakenteen täydentäminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-161">Complete the design of the model mapping</span></span>](#CompleteModelMapping2)

    - [<span data-ttu-id="e97c0-162">Muodon muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-162">Modify a format</span></span>](#ModifyFormat)

        - [<span data-ttu-id="e97c0-163">Lisää uusi muotoelementti</span><span class="sxs-lookup"><span data-stu-id="e97c0-163">Add a new format element</span></span>](#AddFormatElement)
        - [<span data-ttu-id="e97c0-164">Sido lisätty muotoelementti</span><span class="sxs-lookup"><span data-stu-id="e97c0-164">Bind the added format element</span></span>](#BindAddedFormatElement)
        - [<span data-ttu-id="e97c0-165">Suunnittele muoto loppuun</span><span class="sxs-lookup"><span data-stu-id="e97c0-165">Complete the format design</span></span>](#CompleteFormat2)

    - [<span data-ttu-id="e97c0-166">Muodon suorittaminen sovelluksesta</span><span class="sxs-lookup"><span data-stu-id="e97c0-166">Run a format from the application</span></span>](#RunFormatFromApp2)
    - [<span data-ttu-id="e97c0-167">Muodon suorittaminen ER-muodosta</span><span class="sxs-lookup"><span data-stu-id="e97c0-167">Run a format from ER</span></span>](#RunFormatFromER3)
    - [<span data-ttu-id="e97c0-168">Muotokohteen määrittäminen näytön esikatselua varten</span><span class="sxs-lookup"><span data-stu-id="e97c0-168">Configure a format destination for on-screen preview</span></span>](#ConfigureDestination)
    - [<span data-ttu-id="e97c0-169">Voit esikatsella sitä PDF-tiedostona suorittamalla sovelluksen muodon</span><span class="sxs-lookup"><span data-stu-id="e97c0-169">Run a format from the application to preview it as a PDF document</span></span>](#RunFormatFromApp3)

- [<span data-ttu-id="e97c0-170">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e97c0-170">Additional resources</span></span>](#References)

<span data-ttu-id="e97c0-171">Tässä esimerkissä luodaan uusi ER-ratkaisu [kyselylomake](https://docs.microsoft.com/dynamics365/human-resources/hr-learning-questionnaires)-moduulia varten.</span><span class="sxs-lookup"><span data-stu-id="e97c0-171">In this example, you will create a new ER solution for the [Questionnaire](https://docs.microsoft.com/dynamics365/human-resources/hr-learning-questionnaires) module.</span></span> <span data-ttu-id="e97c0-172">Uuden ER-ratkaisun avulla voit suunnitella raportin käyttämällä Microsoft Excel -laskentataulukkoa mallina.</span><span class="sxs-lookup"><span data-stu-id="e97c0-172">This new ER solution lets you design a report by using a Microsoft Excel worksheet as a template.</span></span> <span data-ttu-id="e97c0-173">Tämän jälkeen voit luoda **kyselylomake**-raportin Excel- tai PDF-muodossa sen lisäksi, että luot aiemmin luodun SQL Server Reporting Services (SSRS) -raportin.</span><span class="sxs-lookup"><span data-stu-id="e97c0-173">You can then generate the **Questionnaire** report in Excel or PDF format, in addition to generating the existing SQL Server Reporting Services (SSRS) report.</span></span> <span data-ttu-id="e97c0-174">Voit myös muokata uutta raporttia myöhemmin pyydettäessä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-174">You can also modify the new report later, upon request.</span></span> <span data-ttu-id="e97c0-175">Koodausta ei tarvita.</span><span class="sxs-lookup"><span data-stu-id="e97c0-175">No coding is required.</span></span>

1. <span data-ttu-id="e97c0-176">Voit suorittaa aiemmin luodun raportin siirtymällä kohtaan **kyselylomake** \> **suunnittelu** \> **kyselylomakkeiden raportti**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-176">To run the existing report, go to **Questionnaire** \> **Design** \> **Questionnaires report**.</span></span>

    ![Valitaan Kyselylomake-valikkokohta Kysely-moduulista nykyisen SSRS-raportin suorittamiseksi](./media/er-quick-start1-application-menu-origin.png)

2. <span data-ttu-id="e97c0-178">Määritä valintaehdot **kyselylomakkeiden raportti** -valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-178">In the **Questionnaires report** dialog box, specify selection criteria.</span></span> <span data-ttu-id="e97c0-179">Käytä suodatinta niin, että raportti sisältää vain **SBCCrsExam**-kyselyn.</span><span class="sxs-lookup"><span data-stu-id="e97c0-179">Apply a filter so that the report includes only the **SBCCrsExam** questionnaire.</span></span>

    ![Kyselylomakkeiden raportti -valintaikkunan valintaehtojen määrittäminen](./media/er-quick-start1-ssrs-report-dialog.png)

<span data-ttu-id="e97c0-181">Seuraavassa kuvassa näkyy SSRS-raportin luotu versio **SBCCrsExam**-kyselystä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-181">The following illustration shows the generated version of the SSRS report for the **SBCCrsExam** questionnaire.</span></span>

![Luotu SSRS-raportti](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a><span data-ttu-id="e97c0-183">Määritä ER-kehys</span><span class="sxs-lookup"><span data-stu-id="e97c0-183">Configure the ER framework</span></span>

<span data-ttu-id="e97c0-184">Sähköisen raportoinnin toiminnallisen kehittäjän roolissa olevan käyttäjän on määritettävä sähköisen raportoinnin parametrien vähimmäisjoukko, ennen kuin voit alkaa käyttää ER-kehystä uuden ER-ratkaisusi suunnitteluun.</span><span class="sxs-lookup"><span data-stu-id="e97c0-184">As a user in the Electronic Reporting Developer role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design your new ER solution.</span></span>

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a><span data-ttu-id="e97c0-185">Konfiguroi ER-parametrit</span><span class="sxs-lookup"><span data-stu-id="e97c0-185">Configure ER parameters</span></span>

1. <span data-ttu-id="e97c0-186">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-186">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e97c0-187">Valitse **Sähköinen raportointi** -työtilasta **Sähköisen raportoinnin parametrit**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-187">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="e97c0-188">Määritä **Sähköisen raportoinnin parametrit** -sivun **Yleinen**-välilehdessä **Ota käyttöön suunnittelutila** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-188">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="e97c0-189">Määritä **Liitteet**-välilehdessä seuraavat parametrit:</span><span class="sxs-lookup"><span data-stu-id="e97c0-189">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="e97c0-190">Määritä **Konfiguraatiot**-kenttä **Tiedostoon** **USMF**-yritykselle.</span><span class="sxs-lookup"><span data-stu-id="e97c0-190">Set the **Configurations** field to **File** for the **USMF** company.</span></span>
    - <span data-ttu-id="e97c0-191">Määritä **Työarkisto**-, **Väliaikainen**-, **Perusrivi**- ja **Muut**-kentissä **Tiedostoon**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-191">Set **Job archive**, **Temporary**, **Baseline**, and **Others** fields to **File**.</span></span>

<span data-ttu-id="e97c0-192">Lisätietoja ER-parametreista on kohdassa [Määritä ER-kehys](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e97c0-192">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a><span data-ttu-id="e97c0-193">Aktivoi ER-konfiguraation lähde</span><span class="sxs-lookup"><span data-stu-id="e97c0-193">Activate an ER configuration provider</span></span>

<span data-ttu-id="e97c0-194">Jokainen ER-konfiguraatio merkitään ER-konfiguraation lähteen omistamaksi.</span><span class="sxs-lookup"><span data-stu-id="e97c0-194">Every ER configuration is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="e97c0-195">Siksi sinun on aktivoitava ER-konfiguraation lähde **Sähköinen raportointi** -työtilassa, ennen kuin voit alkaa lisätä tai muokata mitä tahansa ER-konfiguraatioita.</span><span class="sxs-lookup"><span data-stu-id="e97c0-195">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit any ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="e97c0-196">Vain ER-konfiguraation omistaja voi muokata sitä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-196">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="e97c0-197">Siksi ennen kuin ER-konfiguraatiota voi muokata, asianmukainen ER-konfiguraation lähde on aktivoitava **Sähköinen raportointi** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-197">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a><span data-ttu-id="e97c0-198">Tarkista ER-konfiguraation lähteiden luettelo</span><span class="sxs-lookup"><span data-stu-id="e97c0-198">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="e97c0-199">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-199">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e97c0-200">Valitse **Sähköisen raportointi** -työtilan **Liittyvät linkit** -osassa **Konfiguraation lähteet**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-200">In the **Electronic reporting** workspace, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="e97c0-201">**Konfiguraation lähteet** -sivulla jokaisen konfiguraation lähteen tietueella on yksilöllinen nimi ja URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="e97c0-201">On the **Configuration providers** page, each configuration provider record has a unique name and URL.</span></span> <span data-ttu-id="e97c0-202">Tarkista tämän sivun sisältö.</span><span class="sxs-lookup"><span data-stu-id="e97c0-202">Review the contents of this page.</span></span> <span data-ttu-id="e97c0-203">Jos **Litware, Inc.** (`https://www.litware.com`) -tietue on jo olemassa, ohita seuraava menettely, [Lisää uusi ER-konfiguraation lähde](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="e97c0-203">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a><span data-ttu-id="e97c0-204">Lisää uusi ER-konfiguraation lähde</span><span class="sxs-lookup"><span data-stu-id="e97c0-204">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="e97c0-205">Valitse **Konfiguraation lähteet**-sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-205">On the **Configuration providers** page, select **New**.</span></span>
2. <span data-ttu-id="e97c0-206">Kirjoita **Nimi**-kenttään **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="e97c0-206">In the **Name** field, enter **Litware, Inc.**</span></span>
3. <span data-ttu-id="e97c0-207">Kirjoita **Internetosoite**-kenttään `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="e97c0-207">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
4. <span data-ttu-id="e97c0-208">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-208">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a><span data-ttu-id="e97c0-209">Aktivoi ER-konfiguraation lähde</span><span class="sxs-lookup"><span data-stu-id="e97c0-209">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="e97c0-210">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-210">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e97c0-211">Valitse **Sähköinen raportointi** -työtilassa **Litware, Inc**-määrityspalvelu.</span><span class="sxs-lookup"><span data-stu-id="e97c0-211">In the **Electronic reporting** workspace, select the **Litware, Inc.** configuration provider.</span></span>
3. <span data-ttu-id="e97c0-212">Valitse **Määritä aktiivinen**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-212">Select **Set active**.</span></span>

<span data-ttu-id="e97c0-213">Lisätietoja ER-konfiguraation lähteistä on kohdassa [Konfiguraation lähteiden luonti ja merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="e97c0-213">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a><span data-ttu-id="e97c0-214">Toimialuekohtaisen tietomallin suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-214">Design a domain-specific data model</span></span>

<span data-ttu-id="e97c0-215">Sinun on luotava uusi ER-konfiguraatio, joka sisältää [tietomalli](general-electronic-reporting.md#data-model-and-model-mapping-components)-komponentin **Kyselyn** liiketoimialueelle.</span><span class="sxs-lookup"><span data-stu-id="e97c0-215">You must create a new ER configuration that contains a [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** business domain.</span></span> <span data-ttu-id="e97c0-216">Tätä tietomallia käytetään myöhemmin tietolähteenä suunniteltaessa ER-muotoa **kyselylomake**-raportin luomiseksi.</span><span class="sxs-lookup"><span data-stu-id="e97c0-216">This data model will later be used as a data source when you design an ER format to generate the **Questionnaire** report.</span></span>

<span data-ttu-id="e97c0-217">Kun [tuot uuden tietomallin määritys](#ImportDataModel) -osan vaiheet, voit tuoda vaaditun tietomallin mukana olevasta XML-tiedostosta.</span><span class="sxs-lookup"><span data-stu-id="e97c0-217">By completing the steps in the [Import a new data model configuration](#ImportDataModel) section, you can import the required data model from the provided XML file.</span></span> <span data-ttu-id="e97c0-218">Voit myös suorittaa [uuden tietomallin määrityksen luomisen](#DesignDataModel) vaiheet ja suunnitella tämän tietomallin alusta alkaen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-218">Alternatively, you can complete the steps in the [Create a new data model configuration](#DesignDataModel) section to design this data model from scratch.</span></span>

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a><span data-ttu-id="e97c0-219">Uuden tietomallimäärityksen tuominen</span><span class="sxs-lookup"><span data-stu-id="e97c0-219">Import a new data model configuration</span></span>

1. <span data-ttu-id="e97c0-220">Lataa [kyselylomakkeet model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) -tiedosto ja tallenna se paikalliseen tietokoneeseen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-220">Download the [Questionnaires model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="e97c0-221">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-221">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="e97c0-222">Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-222">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="e97c0-223">Valitse toimintoruudussa **Vaihda** \> **Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-223">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="e97c0-224">Valitse **Selaa** ja etsi ja valitse **kyselylomakkeiden model.version.1.xml** -tiedosto.</span><span class="sxs-lookup"><span data-stu-id="e97c0-224">Select **Browse**, and then find and select the **Questionnaires model.version.1.xml** file.</span></span>
6. <span data-ttu-id="e97c0-225">Tuo konfigurointi valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-225">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="e97c0-226">Jos haluat jatkaa, ohita seuraavat vaiheet, [Luo uusi tietomallin konfiguraatio](#DesignDataModel).</span><span class="sxs-lookup"><span data-stu-id="e97c0-226">To continue, skip the next procedure, [Create a new data model configuration](#DesignDataModel).</span></span>

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a><span data-ttu-id="e97c0-227">Uuden tietomallin konfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="e97c0-227">Create a new data model configuration</span></span>

1. <span data-ttu-id="e97c0-228">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-228">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e97c0-229">Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-229">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="e97c0-230">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-230">Select **Create configuration**.</span></span>
4. <span data-ttu-id="e97c0-231">Kirjoita avattavan luettelon **Nimi**-kenttään **Kyselylomakemalli**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-231">In the drop-down dialog box, in the **Name** field, enter **Questionnaire model**.</span></span>
5. <span data-ttu-id="e97c0-232">Valitse **Luo konfigurointi** luodaksesi konfiguroinnin.</span><span class="sxs-lookup"><span data-stu-id="e97c0-232">Select **Create configuration** to create the configuration.</span></span>

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a><span data-ttu-id="e97c0-233">Tietomallin nimeäminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-233">Name the data model</span></span>

1. <span data-ttu-id="e97c0-234">Valitse **Konfiguraatiot**-sivun konfiguraatiopuun kohdasta **Kyselylomakemalli**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-234">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
2. <span data-ttu-id="e97c0-235">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-235">Select **Designer**.</span></span>
3. <span data-ttu-id="e97c0-236">Kirjoita **tietomallin suunnittelu** -sivun **Yleinen**-pikavälilehden **Nimi**-kenttään <a name="DataModeName"></a>**kyselylomakkeet**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-236">On the **Data model designer** page, on the **General** FastTab, in the **Name** field, enter <a name="DataModeName"></a>**Questionnaires**.</span></span>

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a><span data-ttu-id="e97c0-237">Uusien tietomallikenttien lisääminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-237">Add new data model fields</span></span>

1. <span data-ttu-id="e97c0-238">Valitse **Tietomallisuunnittelu**-sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-238">On the **Data model designer** page, select **New**.</span></span>
2. <span data-ttu-id="e97c0-239">Tee seuraavat toimet avattavassa valintaikkunassa tietomallisolmun lisäämistä varten:</span><span class="sxs-lookup"><span data-stu-id="e97c0-239">In the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="e97c0-240">Valitse uuden solmun tyypiksi **mallijuuri**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-240">Select **Model root** as the type of the new node.</span></span>
    2. <span data-ttu-id="e97c0-241">Kirjoita **Nimi**-kenttään <a name="RootDefinitionName"></a>**Juuri**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-241">In the **Name** field, enter <a name="RootDefinitionName"></a>**Root**.</span></span>
    3. <span data-ttu-id="e97c0-242">Valitse **Lisää** lisätäksesi uuden solmun.</span><span class="sxs-lookup"><span data-stu-id="e97c0-242">Select **Add** to add the new node.</span></span>

    <span data-ttu-id="e97c0-243">Tätä pääkuvausta käytetään **kyselylomake**-raportin tietojen toimittamisessa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-243">This root descriptor will be used to provide data for the **Questionnaire** report.</span></span> <span data-ttu-id="e97c0-244">Yksittäisellä tietomallilla voi olla useita kuvaajia.</span><span class="sxs-lookup"><span data-stu-id="e97c0-244">A single data model can have multiple descriptors.</span></span> <span data-ttu-id="e97c0-245">Kukin kuvaus voidaan määrittää yksittäiselle ER-muodolle, jotta raportin luomisessa tarvittavat tiedot tunnistetaan.</span><span class="sxs-lookup"><span data-stu-id="e97c0-245">Each descriptor can be specified for a single ER format, to identify data that is required to generate the report.</span></span>

3. <span data-ttu-id="e97c0-246">Valitse **Uusi** uudelleen ja tee sitten seuraavat toimet avattavassa valintaikkunassa tietomallisolmun lisäämistä varten:</span><span class="sxs-lookup"><span data-stu-id="e97c0-246">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="e97c0-247">Valitse **Aktiivisen solmun alikohde** uuden solmun tyypiksi.</span><span class="sxs-lookup"><span data-stu-id="e97c0-247">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="e97c0-248">Kirjoita **Nimi**-kenttään **CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-248">In the **Name** field, enter **CompanyName**.</span></span>
    3. <span data-ttu-id="e97c0-249">Valitse **Nimiketyyppi**-kentässä **Merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-249">In the **Item type** field, select **String**.</span></span>
    4. <span data-ttu-id="e97c0-250">Valitse **Lisää** lisätäksesi uuden kentän.</span><span class="sxs-lookup"><span data-stu-id="e97c0-250">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="e97c0-251">Tämä kenttä on pakollinen, jotta nykyisen yrityksen nimi voidaan välittää ER-raportiksi, joka kuluttaa tämän tietomallin tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-251">This field is required to pass the name of the current company to an ER report that consumes this data model as a data source.</span></span>

4. <span data-ttu-id="e97c0-252">Valitse **Uusi** uudelleen ja tee sitten seuraavat toimet avattavassa valintaikkunassa tietomallisolmun lisäämistä varten:</span><span class="sxs-lookup"><span data-stu-id="e97c0-252">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="e97c0-253">Valitse **Aktiivisen solmun alikohde** uuden solmun tyypiksi.</span><span class="sxs-lookup"><span data-stu-id="e97c0-253">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="e97c0-254">Kirjoita **Nimi**-kenttään **Kyselylomake**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-254">In the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="e97c0-255">Valitse **Nimiketyyppi**-kentässä **Tietueluettelo**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-255">In the **Item type** field, select **Record list**.</span></span>
    4. <span data-ttu-id="e97c0-256">Valitse **Lisää** lisätäksesi uuden kentän.</span><span class="sxs-lookup"><span data-stu-id="e97c0-256">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="e97c0-257">Tätä kenttää käytetään siirtämään kyselylomake ER-raporttiin, joka kuluttaa tämän tietomallin tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-257">This field will be used to pass the list of questionnaires to an ER report that consumes this data model as a data source.</span></span>

5. <span data-ttu-id="e97c0-258">Valitse **kyselylomake**-solmu.</span><span class="sxs-lookup"><span data-stu-id="e97c0-258">Select the **Questionnaire** node.</span></span>
6. <span data-ttu-id="e97c0-259">Jatka muokattavien tietomallien pakollisten kenttien lisäämistä samalla tavalla, kunnes seuraava tietomallirakenne on valmis.</span><span class="sxs-lookup"><span data-stu-id="e97c0-259">Continue to add the required fields of the editable data model in the same manner until you complete the following data model structure.</span></span>

    | <span data-ttu-id="e97c0-260">Kentän polku</span><span class="sxs-lookup"><span data-stu-id="e97c0-260">Field path</span></span>                                                    | <span data-ttu-id="e97c0-261">Tietotyyppi</span><span class="sxs-lookup"><span data-stu-id="e97c0-261">Data type</span></span>   | <span data-ttu-id="e97c0-262">Kentän nimi/palautettu arvo</span><span class="sxs-lookup"><span data-stu-id="e97c0-262">Field designation/returned value</span></span> |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | <span data-ttu-id="e97c0-263">Juuri</span><span class="sxs-lookup"><span data-stu-id="e97c0-263">Root</span></span>                                                          |             | <span data-ttu-id="e97c0-264">Viitepistekyselylomakkeen tietojen pyytämisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-264">The reference point to request questionnaire data.</span></span> |
    | <span data-ttu-id="e97c0-265">Juuri\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="e97c0-265">Root\\CompanyName</span></span>                                             | <span data-ttu-id="e97c0-266">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-266">String</span></span>      | <span data-ttu-id="e97c0-267">Nykyisen yrityksen nimi.</span><span class="sxs-lookup"><span data-stu-id="e97c0-267">The name of the current company.</span></span> |
    | <span data-ttu-id="e97c0-268">Juuri\\ExecutionContext</span><span class="sxs-lookup"><span data-stu-id="e97c0-268">Root\\ExecutionContext</span></span>                                        | <span data-ttu-id="e97c0-269">Tallenna</span><span class="sxs-lookup"><span data-stu-id="e97c0-269">Record</span></span>      | <span data-ttu-id="e97c0-270">Muotoile suorituksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="e97c0-270">Format execution details.</span></span> |
    | <span data-ttu-id="e97c0-271">Juuri\\ExecutionContext\\FormatName</span><span class="sxs-lookup"><span data-stu-id="e97c0-271">Root\\ExecutionContext\\FormatName</span></span>                            | <span data-ttu-id="e97c0-272">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-272">String</span></span>      | <span data-ttu-id="e97c0-273">Suoritettavan ER-muodon nimi.</span><span class="sxs-lookup"><span data-stu-id="e97c0-273">The name of the ER format that is being run.</span></span> |
    | <span data-ttu-id="e97c0-274">Juuri\\Kyselylomake</span><span class="sxs-lookup"><span data-stu-id="e97c0-274">Root\\Questionnaire</span></span>                                           | <span data-ttu-id="e97c0-275">Tietueluettelo</span><span class="sxs-lookup"><span data-stu-id="e97c0-275">Record list</span></span> | <span data-ttu-id="e97c0-276">Kyselylomakkeiden luettelo</span><span class="sxs-lookup"><span data-stu-id="e97c0-276">The list of questionnaires</span></span> |
    | <span data-ttu-id="e97c0-277">Juuri\\kyselylomake\\aktiivinen</span><span class="sxs-lookup"><span data-stu-id="e97c0-277">Root\\Questionnaire\\Active</span></span>                                   | <span data-ttu-id="e97c0-278">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-278">String</span></span>      | <span data-ttu-id="e97c0-279">Nykyisen kyselylomakkeen tila.</span><span class="sxs-lookup"><span data-stu-id="e97c0-279">The status of the current questionnaire.</span></span> |
    | <span data-ttu-id="e97c0-280">Juuri\\Kyselylomake\\Koodi</span><span class="sxs-lookup"><span data-stu-id="e97c0-280">Root\\Questionnaire\\Code</span></span>                                     | <span data-ttu-id="e97c0-281">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-281">String</span></span>      | <span data-ttu-id="e97c0-282">Nykyisen kyselylomakkeen koodi.</span><span class="sxs-lookup"><span data-stu-id="e97c0-282">The code of the current questionnaire.</span></span> |
    | <span data-ttu-id="e97c0-283">Juuri\\Kyselylomake\\Kuvaus</span><span class="sxs-lookup"><span data-stu-id="e97c0-283">Root\\Questionnaire\\Description</span></span>                              | <span data-ttu-id="e97c0-284">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-284">String</span></span>      | <span data-ttu-id="e97c0-285">Nykyisen kyselylomakkeen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="e97c0-285">The description of the current questionnaire.</span></span> |
    | <span data-ttu-id="e97c0-286">Juuri\\Kyselylomake\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="e97c0-286">Root\\Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="e97c0-287">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-287">String</span></span>      | <span data-ttu-id="e97c0-288">Nykyisen kyselylomakkeen tyyppi.</span><span class="sxs-lookup"><span data-stu-id="e97c0-288">The type of the current questionnaire.</span></span> |
    | <span data-ttu-id="e97c0-289">Juuri\\Kyselylomake\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="e97c0-289">Root\\Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="e97c0-290">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-290">String</span></span>      | <span data-ttu-id="e97c0-291">Nykyisen kyselylomakkeen numerojärjestys.</span><span class="sxs-lookup"><span data-stu-id="e97c0-291">The numerical order of the current questionnaire.</span></span> |
    | <span data-ttu-id="e97c0-292">Juuri\\Kyselylomake\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="e97c0-292">Root\\Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="e97c0-293">Tallenna</span><span class="sxs-lookup"><span data-stu-id="e97c0-293">Record</span></span>      | <span data-ttu-id="e97c0-294">Nykyisen kyselylomakkeen tulosparametrit.</span><span class="sxs-lookup"><span data-stu-id="e97c0-294">The result parameters of the current questionnaire.</span></span> |
    | <span data-ttu-id="e97c0-295">Juuri\\Kyselylomake\\ResultsGroup\\Koodi</span><span class="sxs-lookup"><span data-stu-id="e97c0-295">Root\\Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="e97c0-296">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-296">String</span></span>      | <span data-ttu-id="e97c0-297">Nykyisen tulosryhmän tunnuskoodi.</span><span class="sxs-lookup"><span data-stu-id="e97c0-297">The identification code of the current result group.</span></span> |
    | <span data-ttu-id="e97c0-298">Juuri\\Kyselylomake\\ResultsGroup\\Kuvaus</span><span class="sxs-lookup"><span data-stu-id="e97c0-298">Root\\Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="e97c0-299">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-299">String</span></span>      | <span data-ttu-id="e97c0-300">Nykyisen tulosryhmän kuvaus.</span><span class="sxs-lookup"><span data-stu-id="e97c0-300">The description of the current result group.</span></span> |
    | <span data-ttu-id="e97c0-301">Juuri\\Kyselylomake\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="e97c0-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="e97c0-302">Reaaliluku</span><span class="sxs-lookup"><span data-stu-id="e97c0-302">Real</span></span>        | <span data-ttu-id="e97c0-303">Ansaittujen pisteiden enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-303">The maximum number of points that could be earned.</span></span> |
    | <span data-ttu-id="e97c0-304">Juuri\\Kyselylomake\\Kysymys</span><span class="sxs-lookup"><span data-stu-id="e97c0-304">Root\\Questionnaire\\Question</span></span>                                 | <span data-ttu-id="e97c0-305">Tietueluettelo</span><span class="sxs-lookup"><span data-stu-id="e97c0-305">Record list</span></span> | <span data-ttu-id="e97c0-306">Nykyisen kyselylomakkeen kysymysluettelo.</span><span class="sxs-lookup"><span data-stu-id="e97c0-306">The list of questions for the current questionnaire.</span></span> |
    | <span data-ttu-id="e97c0-307">Juuri\\Kyselylomake\\Kysymys\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="e97c0-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="e97c0-308">Kokonaisluku</span><span class="sxs-lookup"><span data-stu-id="e97c0-308">Integer</span></span>     | <span data-ttu-id="e97c0-309">Nykyisen vastauskokoelman järjestysnumero.</span><span class="sxs-lookup"><span data-stu-id="e97c0-309">The sequence number of the current answer collection.</span></span> |
    | <span data-ttu-id="e97c0-310">Juuri\\Kyselylomake\\Kysymys\\Tunnus</span><span class="sxs-lookup"><span data-stu-id="e97c0-310">Root\\Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="e97c0-311">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-311">String</span></span>      | <span data-ttu-id="e97c0-312">Nykyisen kysymyksen tunnuskoodi.</span><span class="sxs-lookup"><span data-stu-id="e97c0-312">The identification code of the current question.</span></span> |
    | <span data-ttu-id="e97c0-313">Juuri\\Kyselylomake\\Kysymys\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="e97c0-313">Root\\Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="e97c0-314">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-314">String</span></span>      | <span data-ttu-id="e97c0-315">Lippu, joka ilmaisee, onko nykyiseen kysymykseen vastattava.</span><span class="sxs-lookup"><span data-stu-id="e97c0-315">A flag that indicates whether the current question must be answered.</span></span> |
    | <span data-ttu-id="e97c0-316">Juuri\\Kyselylomake\\Kysymys\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="e97c0-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="e97c0-317">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-317">String</span></span>      | <span data-ttu-id="e97c0-318">Lippu, joka ilmaisee, onko nykyinen kysymys ensisijainen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-318">A flag that indicates whether the current question is primary.</span></span> |
    | <span data-ttu-id="e97c0-319">Juuri\\Kyselylomake\\Kysymys\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="e97c0-319">Root\\Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="e97c0-320">Kokonaisluku</span><span class="sxs-lookup"><span data-stu-id="e97c0-320">Integer</span></span>     | <span data-ttu-id="e97c0-321">Nykyisen kysymyksen järjestysnumero.</span><span class="sxs-lookup"><span data-stu-id="e97c0-321">The sequence number of the current question.</span></span> |
    | <span data-ttu-id="e97c0-322">Juuri\\Kyselylomake\\Kysymys\\Teksti</span><span class="sxs-lookup"><span data-stu-id="e97c0-322">Root\\Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="e97c0-323">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-323">String</span></span>      | <span data-ttu-id="e97c0-324">Nykyisen kysymyksen teksti.</span><span class="sxs-lookup"><span data-stu-id="e97c0-324">The text of the current question.</span></span> |
    | <span data-ttu-id="e97c0-325">Juuri\\Kyselylomake\\Kysymys\\Vastaus</span><span class="sxs-lookup"><span data-stu-id="e97c0-325">Root\\Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="e97c0-326">Tietueluettelo</span><span class="sxs-lookup"><span data-stu-id="e97c0-326">Record list</span></span> | <span data-ttu-id="e97c0-327">Nykyisen kysymyksen vastausluettelo.</span><span class="sxs-lookup"><span data-stu-id="e97c0-327">The list of answers for the current question.</span></span> |
    | <span data-ttu-id="e97c0-328">Juuri\\Kyselylomake\\Kysymys\\Vastaus\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="e97c0-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="e97c0-329">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-329">String</span></span>      | <span data-ttu-id="e97c0-330">Lippu, joka ilmaisee, onko nykyinen vastaus oikein.</span><span class="sxs-lookup"><span data-stu-id="e97c0-330">A flag that indicates whether the current answer is correct.</span></span> |
    | <span data-ttu-id="e97c0-331">Juuri\\Kyselylomake\\Kysymys\\Vastaus\\Pisteet</span><span class="sxs-lookup"><span data-stu-id="e97c0-331">Root\\Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="e97c0-332">Reaaliluku</span><span class="sxs-lookup"><span data-stu-id="e97c0-332">Real</span></span>        | <span data-ttu-id="e97c0-333">Pisteet, jotka ansaitaan nykyisen vastauksen valinnan yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-333">The points that are earned when the current answer is selected.</span></span> |
    | <span data-ttu-id="e97c0-334">Juuri\\Kyselylomake\\Kysymys\\Vastaus\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="e97c0-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="e97c0-335">Kokonaisluku</span><span class="sxs-lookup"><span data-stu-id="e97c0-335">Integer</span></span>     | <span data-ttu-id="e97c0-336">Nykyisen vastauksen järjestysnumero.</span><span class="sxs-lookup"><span data-stu-id="e97c0-336">The sequence number of the current answer.</span></span> |
    | <span data-ttu-id="e97c0-337">Juuri\\Kyselylomake\\Kysymys\\Vastaus\\Teksti</span><span class="sxs-lookup"><span data-stu-id="e97c0-337">Root\\Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="e97c0-338">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-338">String</span></span>      | <span data-ttu-id="e97c0-339">Nykyisen vastauksen teksti.</span><span class="sxs-lookup"><span data-stu-id="e97c0-339">The text of the current answer.</span></span> |

    <span data-ttu-id="e97c0-340">Seuraavassa kuvassa näkyy **tietomallin suunnittelu** -sivulla valmiiksi muokattava tietomalli.</span><span class="sxs-lookup"><span data-stu-id="e97c0-340">The following illustration shows the completed editable data model on the **Data model designer** page.</span></span>

    ![Konfiguroitu tietomalli ER-tietomallin suunnittelussa](./media/er-quick-start1-model2.png)

7. <span data-ttu-id="e97c0-342">Tallenna muutokset.</span><span class="sxs-lookup"><span data-stu-id="e97c0-342">Save your changes.</span></span>
8. <span data-ttu-id="e97c0-343">Sulje **Tietomallin suunnittelu** -sivu.</span><span class="sxs-lookup"><span data-stu-id="e97c0-343">Close the **Data model designer** page.</span></span>

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a><span data-ttu-id="e97c0-344">Tietomallin rakenteen täydentäminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-344">Complete the design of the data model</span></span>

1. <span data-ttu-id="e97c0-345">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-345">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e97c0-346">Valitse **Konfiguraatiot**-sivun konfiguraatiopuun kohdasta **Kyselylomakemalli**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-346">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="e97c0-347">Valitse **Versiot**-pikavälilehdessä konfiguraatioversio, jonka tila on **Luonnos**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-347">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="e97c0-348">Valitse **Muutoksen tila** \> **Viimeistele**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-348">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="e97c0-349">Tämän konfiguraation version 1 tila muutetaan **luonnoksesta** **valmiiksi**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-349">The status of version 1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="e97c0-350">Versiota 1 ei voi enää muuttaa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-350">Version 1 can no longer be changed.</span></span> <span data-ttu-id="e97c0-351">Tämä versio sisältää konfiguroidun tietomallin, ja sitä voidaan käyttää muiden ER-konfiguraatioiden pohjana.</span><span class="sxs-lookup"><span data-stu-id="e97c0-351">This version contains the configured data model and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="e97c0-352">Tämän konfiguraation versio 2 luodaan, ja sen tila on **luonnos**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-352">Version 2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="e97c0-353">Voit muokata tätä versiota, jos haluat muuttaa **kyselylomakkeen** tietomallia.</span><span class="sxs-lookup"><span data-stu-id="e97c0-353">You can edit this version to adjust the **Questionnaire** data model.</span></span>

![Konfiguraatiosivun muokattavan ER-konfiguraation versiot](./media/er-quick-start1-model-configuration.png)

<span data-ttu-id="e97c0-355">Lisätietoja ER-kokoonpanojen versiotiedoista on kohdassa [sähköisen raportoinnin (ER) yleiskuvaus](general-electronic-reporting.md#component-versioning).</span><span class="sxs-lookup"><span data-stu-id="e97c0-355">For more information about versioning for ER configurations, see [Electronic reporting (ER) overview](general-electronic-reporting.md#component-versioning).</span></span>

> [!NOTE]
> <span data-ttu-id="e97c0-356">Määritetty tietomalli on **kyselylomakkeen** liiketoimialueen abstrakti esitystapa, eikä se sisällä suhteita Microsoft Dynamics 365 Financen artefakteihin.</span><span class="sxs-lookup"><span data-stu-id="e97c0-356">The configured data model is your abstract representation of the **Questionnaire** business domain and contains no relations to artefacts that are specific to Microsoft Dynamics 365 Finance.</span></span>

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a><span data-ttu-id="e97c0-357">Mallin määrityksen suunnitteleminen konfiguroidulle tietomallille</span><span class="sxs-lookup"><span data-stu-id="e97c0-357">Design a model mapping for the configured data model</span></span>

<span data-ttu-id="e97c0-358">Sähköisen raportoinnin kehittäjän roolin käyttäjänä sinun on luotava uusi ER-konfiguraatio, joka sisältää **kyselylomakkeen** tietomallin [mallinyhdistämis](general-electronic-reporting.md#data-model-and-model-mapping-components)-komponentin .</span><span class="sxs-lookup"><span data-stu-id="e97c0-358">As a user in the Electronic Reporting Developer role, you must create a new ER configuration that contains a [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** data model.</span></span> <span data-ttu-id="e97c0-359">Koska tämä komponentti toteuttaa Financen konfiguroidun tietomallin, se on Finance-kohtainen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-359">Because this component implements the configured data model for Finance, it's Finance-specific.</span></span> <span data-ttu-id="e97c0-360">Mallikartoituskomponentti on konfiguroitava niin, että se määrittää sovellusobjektit, joita käytetään määritetyn tietomallin täyttämiseen sovellustiedoilla suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="e97c0-360">You must configure the model mapping component to specify the application objects that must be used to fill in the configured data model with application data at runtime.</span></span> <span data-ttu-id="e97c0-361">Tämän tehtävän suorittaminen edellyttää, että olet tietoinen Financen **kyselylomakkeen** liiketoimialueen tietorakenteen toteutustiedoista.</span><span class="sxs-lookup"><span data-stu-id="e97c0-361">To complete this task, you must be aware of the implementation details of the data structure of the **Questionnaire** business domain in Finance.</span></span>

<span data-ttu-id="e97c0-362">Kun teet loppuun [tuot uuden mallin yhdistämismääritys](#ImportModelMapping) -osan vaiheet, voit tuoda vaaditun uuden mallin yhdistämismäärityksen mukana olevasta XML-tiedostosta.</span><span class="sxs-lookup"><span data-stu-id="e97c0-362">By completing the steps in the [Import a new model mapping configuration](#ImportModelMapping) section that follows, you can import the required model mapping configuration from the provided XML file.</span></span> <span data-ttu-id="e97c0-363">Voit myös suorittaa [uuden mallin yhdistämismäärityksen](#CreateModelMapping) vaiheet ja suunnitella tämän mallin yhdistämismäärityksen alusta alkaen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-363">Alternatively, you can complete the steps in the [Create a new model mapping configuration](#CreateModelMapping) section to design this model mapping from scratch.</span></span>

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a><span data-ttu-id="e97c0-364">Uuden mallin yhdistämismäärityksen tuominen</span><span class="sxs-lookup"><span data-stu-id="e97c0-364">Import a new model mapping configuration</span></span>

1. <span data-ttu-id="e97c0-365">Lataa [kyselylomakkeet mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) -tiedosto ja tallenna se paikalliseen tietokoneeseen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-365">Download the [Questionnaires mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="e97c0-366">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-366">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="e97c0-367">Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-367">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="e97c0-368">Valitse toimintoruudussa **Vaihda** \> **Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-368">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="e97c0-369">Valitse **Selaa** ja etsi ja valitse **kyselylomakkeiden mapping.version.1.1.xml** -tiedosto.</span><span class="sxs-lookup"><span data-stu-id="e97c0-369">Select **Browse**, and then find and select the **Questionnaires mapping.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="e97c0-370">Tuo konfigurointi valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-370">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="e97c0-371">Jos haluat jatkaa, ohita seuraavat vaiheet, [Luo uusi mallin yhdistämiskonfiguraatio](#CreateModelMapping).</span><span class="sxs-lookup"><span data-stu-id="e97c0-371">To continue, skip the next procedure, [Create a new model mapping configuration](#CreateModelMapping).</span></span>

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a><span data-ttu-id="e97c0-372">Uuden mallin yhdistämismäärityksen luominen</span><span class="sxs-lookup"><span data-stu-id="e97c0-372">Create a new model mapping configuration</span></span>

1. <span data-ttu-id="e97c0-373">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-373">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e97c0-374">Valitse **Konfiguraatiot**-sivun konfiguraatiopuun kohdasta **Kyselylomakemalli**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-374">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="e97c0-375">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-375">Select **Create configuration**.</span></span>
4. <span data-ttu-id="e97c0-376">Toimi avattavassa valintaikkunassa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e97c0-376">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="e97c0-377">Syötä **Uusi**-kenttään **Tietomallikyselylomakkeisiin perustuvat mallin määritykset**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-377">In the **New** field, select **Model Mapping based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="e97c0-378">Kirjoita **Nimi**-kenttään **Kyselylomakkeen yhdistäminen**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-378">In the **Name** field, enter **Questionnaire mapping**.</span></span>
    3. <span data-ttu-id="e97c0-379">**Valitse tietomallin määritys** -kentässä **Juuri**-määritys.</span><span class="sxs-lookup"><span data-stu-id="e97c0-379">In the **Data model definition** field, select the **Root** definition.</span></span>
    4. <span data-ttu-id="e97c0-380">Valitse **Luo konfigurointi** luodaksesi konfiguroinnin.</span><span class="sxs-lookup"><span data-stu-id="e97c0-380">Select **Create configuration** to create the configuration.</span></span>

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a><span data-ttu-id="e97c0-381">Uuden mallimäärityskomponentin suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-381">Design a new model mapping component</span></span>

1. <span data-ttu-id="e97c0-382">Valitse **Konfiguraatiot**-sivun konfiguraatiopuun kohdasta **Kyselylomakkeen yhdistäminen**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-382">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
2. <span data-ttu-id="e97c0-383">Avaa määritysluettelo valitsemalla **Suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-383">Select **Designer** to open the list of mappings.</span></span>
3. <span data-ttu-id="e97c0-384">Valitse **kyselylomakkeiden yhdistämismääritys**, joka lisättiin automaattisesti **Juuri**-määritystä varten</span><span class="sxs-lookup"><span data-stu-id="e97c0-384">Select the **Questionnaires mapping** mapping that was automatically added for the **Root** definition</span></span>
4. <span data-ttu-id="e97c0-385">Aloita valitun yhdistämismäärityksen määrittäminen valitsemalla **Suunnittelu**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="e97c0-385">Select **Designer** to start to configure the selected mapping.</span></span>

<span data-ttu-id="e97c0-386">**Juuri**-määritykselle lisätään automaattisesti uusi yhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="e97c0-386">A new mapping is automatically added for the **Root** definition.</span></span> <span data-ttu-id="e97c0-387">Tässä yhdistämisessä on **malliin**-suunta.</span><span class="sxs-lookup"><span data-stu-id="e97c0-387">This mapping has the **To model** direction.</span></span> <span data-ttu-id="e97c0-388">Tämän vuoksi tätä määritystä voidaan käyttää tarvittavien tietojen tietomallin täyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-388">Therefore, this mapping can be used to fill in a data model with required data.</span></span>

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a><span data-ttu-id="e97c0-389">Tietolähteiden lisääminen sovellustaulujen käyttämiseen</span><span class="sxs-lookup"><span data-stu-id="e97c0-389">Add data sources to access application tables</span></span>

<span data-ttu-id="e97c0-390">Sinun on konfiguroitava tietolähteet, jotta voit käyttää kyselylomakkeen tietoja sisältäviä sovellustauluja.</span><span class="sxs-lookup"><span data-stu-id="e97c0-390">You must configure data sources to access the application tables that contain questionnaire details.</span></span>

1. <span data-ttu-id="e97c0-391">Valitse **Mallin määrityksen suunnittelu** -sivun **Tietolähdetyypit**-ruudusta **Dynamics 365 for Operations\\Taulukkotiedot**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-391">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="e97c0-392">Lisää uusi tietolähde, jonka avulla pääsee käyttämään KMCollection-taulua, jossa jokainen tietue vastaa yhtä kyselylomaketta:</span><span class="sxs-lookup"><span data-stu-id="e97c0-392">Add a new data source that will be used to access the KMCollection table, where every record represents a single questionnaire:</span></span>

    1. <span data-ttu-id="e97c0-393">Valitse **Tietolähteet**-ruudussa **Lisää juuri**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-393">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="e97c0-394">Kirjoita valintaikkunan **Nimi**-kentässä **Kyselylomake**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-394">In dialog box, in the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="e97c0-395">Kirjoita **Taulu**-kenttään **KMCollection**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-395">In the **Table** field, enter **KMCollection**.</span></span>
    4. <span data-ttu-id="e97c0-396">Määritä **Kysy kyselyä** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-396">Set the **Ask for query** option to **Yes**.</span></span> <span data-ttu-id="e97c0-397">Tämän jälkeen voit määrittää tämän taulun [suodatus](../../fin-ops/get-started/advanced-filtering-query-options.md)-asetukset järjestelmän kyselyvalintaikkunassa suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="e97c0-397">You will then be able to specify [filtering](../../fin-ops/get-started/advanced-filtering-query-options.md) options for this table in the system query dialog box at runtime.</span></span>
    5. <span data-ttu-id="e97c0-398">Lisää uusi tietolähde valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-398">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="e97c0-399">Valitse **Tietolähdetyypit**-ruudusta **Dynamics 365 for Operations\\Taulukkotiedot**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-399">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
4. <span data-ttu-id="e97c0-400">Lisää uusi tietolähde, jonka avulla pääsee käyttämään KMQuestion-taulua, jossa jokainen tietue vastaa yhtä kysymystä lomakkeessa:</span><span class="sxs-lookup"><span data-stu-id="e97c0-400">Add a new data source that will be used to access the KMQuestion table, where every record represents a single question in a questionnaire:</span></span>

    1. <span data-ttu-id="e97c0-401">Valitse **Tietolähteet**-ruudussa **Lisää juuri**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-401">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="e97c0-402">Kirjoita valintaikkunan **Nimi**-kenttään **Kysymys**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-402">In the dialog box, in the **Name** field, enter **Question**.</span></span>
    3. <span data-ttu-id="e97c0-403">Kirjoita **Taulu**-kenttään **KMQuestion**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-403">In the **Table** field, enter **KMQuestion**.</span></span>
    4. <span data-ttu-id="e97c0-404">Lisää uusi tietolähde valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-404">Select **OK** to add the new data source.</span></span>

5. <span data-ttu-id="e97c0-405">Valitse **Tietolähdetyypit**-ruudusta **Dynamics 365 for Operations\\Taulukkotiedot**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-405">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
6. <span data-ttu-id="e97c0-406">Lisää uusi tietolähdeyritys, jonka avulla pääsee käyttämään KMAnswer-taulua, jossa jokainen tietue vastaa yhtä vastausta lomakkeessa:</span><span class="sxs-lookup"><span data-stu-id="e97c0-406">Add a new data source try that will be used to access the KMAnswer table, where every record represents a single answer to a question in a questionnaire:</span></span>

    1. <span data-ttu-id="e97c0-407">Valitse **Tietolähteet**-ruudussa **Lisää juuri**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-407">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="e97c0-408">Kirjoita **Nimi**-kenttään **Vastaus**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-408">In the **Name** field, enter **Answer**.</span></span>
    3. <span data-ttu-id="e97c0-409">Kirjoita **Taulu**-kenttään **KMAnswer**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-409">In the **Table** field, enter **KMAnswer**.</span></span>
    4. <span data-ttu-id="e97c0-410">Lisää uusi tietolähde valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-410">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="e97c0-411">Valitse **Tietolähdetyypit**-ruudusta **Toiminnot\\Laskettu kenttä**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-411">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="e97c0-412">Lisää uusi laskettu kenttä, jonka avulla voidaan käyttää KMQuestionResultGroup-taulun tietuetta pää-KMCollection-taulun jokaisesta tietueesta:</span><span class="sxs-lookup"><span data-stu-id="e97c0-412">Add a new calculated field that will be used to access a record of the KMQuestionResultGroup table from every record of the parent KMCollection table:</span></span>

    1. <span data-ttu-id="e97c0-413">Valitse **Tietolähteet**-ruudussa **Kyselylomake**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-413">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="e97c0-414">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-414">Select **Add**.</span></span>
    3. <span data-ttu-id="e97c0-415">Kirjoita valintaikkunan **Nimi**-kenttään **\$ResultGroup**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-415">In the dialog box, in the **Name** field, enter **\$ResultGroup**.</span></span>
    4. <span data-ttu-id="e97c0-416">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-416">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="e97c0-417">Syötä [ER-kaavaeditorin](general-electronic-reporting-formula-designer.md) **Kaava**-kenttään **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)**, jos haluat käyttää KMCollection- ja KMQuestionResultGroup-taulujen välistä yksi-moneen-[yhteyttä](er-formula-language.md#paths).</span><span class="sxs-lookup"><span data-stu-id="e97c0-417">In the [ER formula editor](general-electronic-reporting-formula-designer.md), in the **Formula** field, enter **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** to use the [path](er-formula-language.md#paths) of the one-to-many relation between the KMCollection and KMQuestionResultGroup tables.</span></span>
    6. <span data-ttu-id="e97c0-418">Valitse **Tallenna** ja sulje kaavaeditori.</span><span class="sxs-lookup"><span data-stu-id="e97c0-418">Select **Save**, and close the formula editor.</span></span>
    7. <span data-ttu-id="e97c0-419">Lisää uusi laskettu kenttä valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-419">Select **OK** to add the new calculated field.</span></span>

9. <span data-ttu-id="e97c0-420">Valitse **Tietolähdetyypit**-ruudusta **Toiminnot\\Laskettu kenttä**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-420">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
10. <span data-ttu-id="e97c0-421">Lisää uusi laskettu kenttä, jonka avulla voidaan käyttää KMQuestion-taulun kysymystietueita pää-KMCollectionQuestion-taulun jokaisesta tietueesta:</span><span class="sxs-lookup"><span data-stu-id="e97c0-421">Add a new calculated field that will be used to access question records of the KMQuestion table from every record of the parent KMCollectionQuestion table:</span></span>

    1. <span data-ttu-id="e97c0-422">Valitse **Tietolähteet**-ruudussa **Kyselylomake**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-422">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="e97c0-423">Laajenna **\<Suhteet**-solmu, joka sisältää yksi-moneen-suhteet KMCollection-tauluun.</span><span class="sxs-lookup"><span data-stu-id="e97c0-423">Expand the **\<Relations** node that contains one-to-many relations of the KMCollection table.</span></span>
    3. <span data-ttu-id="e97c0-424">Valitse liittyvä **KMCollectionQuestion**-taulu ja valitse sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-424">Select the related **KMCollectionQuestion** table, and then select **Add**.</span></span>
    4. <span data-ttu-id="e97c0-425">Kirjoita valintaikkunan **Nimi**-kenttään **\$Kysymys**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-425">In the dialog box, in the **Name** field, enter **\$Question**.</span></span>
    5. <span data-ttu-id="e97c0-426">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-426">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="e97c0-427">Kirjoita kaavaeditorissa **Kaava**-kenttään **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** ja palauta asianmukaiset kysymystiedot KMQuestion-taulusta.</span><span class="sxs-lookup"><span data-stu-id="e97c0-427">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** to return the appropriate question records from the KMQuestion table.</span></span>
    7. <span data-ttu-id="e97c0-428">Valitse **Tallenna** ja sulje kaavaeditori.</span><span class="sxs-lookup"><span data-stu-id="e97c0-428">Select **Save**, and close the formula editor.</span></span>
    8. <span data-ttu-id="e97c0-429">Lisää uusi laskettu kenttä valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-429">Select **OK** to add the new calculated field.</span></span>

11. <span data-ttu-id="e97c0-430">Valitse **Tietolähdetyypit**-ruudusta **Toiminnot\\Laskettu kenttä**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-430">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
12. <span data-ttu-id="e97c0-431">Lisää uusi laskettu kenttä, jonka avulla voidaan käyttää KMAnswer-taulun vastaustietueita pää-KMQuestion-taulun jokaisesta tietueesta:</span><span class="sxs-lookup"><span data-stu-id="e97c0-431">Add a new calculated field that will be used to access answer records of the KMAnswer table from every record of the parent KMQuestion table:</span></span>

    1. <span data-ttu-id="e97c0-432">Valitse **Tietolähteet**-ruudussa **Kyselylomake.\<Relations.KMCollectionQuestion.\$Kysymys** ja valitse sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-432">In the **Data sources** pane, select **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**, and then select **Add**.</span></span>
    2. <span data-ttu-id="e97c0-433">Kirjoita valintaikkunan **Nimi**-kenttään **\$Vastaus**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-433">In the dialog box, in the **Name** field, enter **\$Answer**.</span></span>
    3. <span data-ttu-id="e97c0-434">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-434">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="e97c0-435">Kirjoita kaavaeditorissa **Kaava**-kenttään **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** ja palauta asianmukaiset vastaustiedot KMAnswer-taulusta.</span><span class="sxs-lookup"><span data-stu-id="e97c0-435">In the formula editor, in the **Formula** field, enter **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** to return the appropriate answer records from the KMAnswer table.</span></span>
    5. <span data-ttu-id="e97c0-436">Valitse **Tallenna** ja sulje kaavaeditori.</span><span class="sxs-lookup"><span data-stu-id="e97c0-436">Select **Save**, and close the formula editor.</span></span>
    6. <span data-ttu-id="e97c0-437">Lisää uusi laskettu kenttä valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-437">Select **OK** to add the new calculated field.</span></span>

13. <span data-ttu-id="e97c0-438">Valitse **Tietolähdetyypit**-ruudusta **Dynamics 365 for Operations\\Taulukko**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-438">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table**.</span></span>
14. <span data-ttu-id="e97c0-439">Lisää uusi tietolähde, jota käytetään CompanyInfo-taulun menetelmien käyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-439">Add a new data source that will be used to access methods of the CompanyInfo table.</span></span> <span data-ttu-id="e97c0-440">Huomaa, että tämän taulun **find()**-menetelmä palauttaa tietueen, joka edustaa nykyisen Finance-instanssin yritystä, jota tämä yhdistäminen kutsuu kontekstissa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-440">Note that the **find()** method of this table returns a record that represents a company of the current Finance instance that this mapping is called in the context of.</span></span>

    1. <span data-ttu-id="e97c0-441">Valitse **Tietolähteet**-ruudussa **Lisää juuri**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-441">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="e97c0-442">Kirjoita valintaikkunan **Nimi**-kenttään **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-442">In the dialog box, in the **Name** field, enter **CompanyInfo**.</span></span>
    3. <span data-ttu-id="e97c0-443">Kirjoita **Taulu**-kenttään **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-443">In the **Table** field, enter **CompanyInfo**.</span></span>
    4. <span data-ttu-id="e97c0-444">Lisää uusi tietolähde valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-444">Select **OK** to add the new data source.</span></span>

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a><span data-ttu-id="e97c0-445">Tietolähteiden lisääminen sovellusluettelointien käyttämiseen</span><span class="sxs-lookup"><span data-stu-id="e97c0-445">Add data sources to access application enumerations</span></span>

<span data-ttu-id="e97c0-446">Sinun on konfiguroitava tietolähteet, jotta voit käyttää sovellusten luettelointeja ja verrattava niiden arvoja **luettelointi**-tyypin kenttien arvoihin sovellustaulukoissa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-446">You must configure data sources to access application enumerations and compare their values with values of fields of the **Enumeration** type in the application tables.</span></span> <span data-ttu-id="e97c0-447">Sinun on käytettävä vertailun tuloksia tietomallin asianmukaisten kenttien täyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-447">You must use the result of the comparison to fill in appropriate fields of the data model.</span></span>

1. <span data-ttu-id="e97c0-448">Valitse **Mallin määrityksen suunnittelu** -sivun **Tietolähdetyypit**-ruudusta **Dynamics 365 for Operations\\Luettelointi**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-448">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
2. <span data-ttu-id="e97c0-449">Lisää uusi tietolähde, jota käytetään **EnumAppNoYes**-luettelon arvojen käyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-449">Add a new data source that will be used to access values of the **EnumAppNoYes** enumeration:</span></span>

    1. <span data-ttu-id="e97c0-450">Valitse **Tietolähteet**-ruudussa **Lisää juuri**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-450">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="e97c0-451">Kirjoita valintaikkunan **Nimi**-kenttään **EnumAppNoYes**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-451">In the dialog box, in the **Name** field, enter **EnumAppNoYes**.</span></span>
    3. <span data-ttu-id="e97c0-452">Kirjoita **luettelointi**-kenttään **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-452">In the **Enumeration** field, enter **NoYes**.</span></span>
    4. <span data-ttu-id="e97c0-453">Lisää uusi tietolähde valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-453">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="e97c0-454">Valitse **Tietolähdetyypit**-ruudusta **Dynamics 365 for Operations\\Luettelointi**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-454">In the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
4. <span data-ttu-id="e97c0-455">Lisää uusi tietolähde, jota käytetään **KMCollectionQuestionMode**-luettelon arvojen käyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-455">Add a new data source that will be used to access the values of the **KMCollectionQuestionMode** enumeration:</span></span>

    1. <span data-ttu-id="e97c0-456">Valitse **Tietolähteet**-ruudussa **Lisää juuri**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-456">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="e97c0-457">Kirjoita valintaikkunan **Nimi**-kentässä **EnumAppQuestionOrder**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-457">In the dialog box, in the **Name** field, enter **EnumAppQuestionOrder**.</span></span>
    3. <span data-ttu-id="e97c0-458">Kirjoita **luettelointi**-kenttään **KMCollectionQuestionMode**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-458">In the **Enumeration** field, enter **KMCollectionQuestionMode**.</span></span>
    4. <span data-ttu-id="e97c0-459">Lisää uusi tietolähde valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-459">Select **OK** to add the new data source.</span></span>

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a><span data-ttu-id="e97c0-460">Voit luoda raportin määritetyllä kielellä lisäämällä ER-otsikoita</span><span class="sxs-lookup"><span data-stu-id="e97c0-460">Add ER labels to generate a report in a specified language</span></span>

<span data-ttu-id="e97c0-461">Voit lisätä ER-otsikoita ja määrittää jotkin tietolähteet palauttamaan arvoja, jotka määräytyvät mallin yhdistämiskutsun kontekstissa määritetyn kielen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e97c0-461">You can add ER labels to configure some of your data sources to return values that depend on the language that is defined in the context of the model mapping's call.</span></span>

1. <span data-ttu-id="e97c0-462">Valitse **Mallin määrityksen suunnittelu** -sivun **Tietolähteet**-ruudusta **Vastaus** ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-462">On the **Model mapping designer** page, in the **Data sources** pane, select **Answer**, and then select **Edit**.</span></span>
2. <span data-ttu-id="e97c0-463">Aktivoi **Otsikko**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-463">Activate the **Label** field.</span></span>
3. <span data-ttu-id="e97c0-464">Valitse **Käännä**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-464">Select **Translate**.</span></span>
4. <span data-ttu-id="e97c0-465">Toimi **Tekstin kääntäminen** -valintaikkunassa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e97c0-465">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="e97c0-466">Kirjoita **Etiketin tunnus** -kenttään **PositiveAnswer**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-466">In the **Label Id** field, enter **PositiveAnswer**.</span></span>
    2. <span data-ttu-id="e97c0-467">Kirjoita **Teksti oletuskielellä** -kenttään **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-467">In the **Text in default language** field, enter **Yes**.</span></span>
    3. <span data-ttu-id="e97c0-468">Valitse **Käännä**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-468">Select **Translate**.</span></span>
    4. <span data-ttu-id="e97c0-469">Kirjoita **Etiketin tunnus**-kenttään **NegativeAnswer**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-469">In the **Label Id** field, enter **NegativeAnswer**.</span></span>
    5. <span data-ttu-id="e97c0-470">Kirjoita **Teksti oletuskielellä** -kenttään **Ei**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-470">In the **Text in default language** field, enter **No**.</span></span>
    6. <span data-ttu-id="e97c0-471">Valitse **Käännä**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-471">Select **Translate**.</span></span>

5. <span data-ttu-id="e97c0-472">Sulkee **tekstin kääntäjä** -valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="e97c0-472">Close the **Text translation** dialog box.</span></span>
6. <span data-ttu-id="e97c0-473">Valitse **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-473">Select **Cancel**.</span></span>

![Muokattavien mallimääritysten ER-otsikoiden lisääminen](./media/er-quick-start1-adding-labels.png)

<span data-ttu-id="e97c0-475">Olet kirjoittanut vain oletuskielelle määritetyt ER-etiketit.</span><span class="sxs-lookup"><span data-stu-id="e97c0-475">You've entered ER labels only for the default language.</span></span> <span data-ttu-id="e97c0-476">Lisätietoja siitä, miten ER-etiketit voidaan kääntää muille kielille, on ohjeaiheessa [Monikielisten raporttien suunnitteleminen](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="e97c0-476">For information about how ER labels can be translated into other languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a><span data-ttu-id="e97c0-477">Lisää tietolähde muuntamaan lueteltujen arvojen vertailutulokset tekstiarvoihin</span><span class="sxs-lookup"><span data-stu-id="e97c0-477">Add a data source to transform the results of comparing enumeration values to a text value</span></span>

<span data-ttu-id="e97c0-478">Koska luettelointiarvojen ja tekstiarvojen vertailun tulokset on muunnettava useita kertoja lähteiden erojen osalta, tämä logiikka kannattaa määrittää yhdeksi tietolähteeksi.</span><span class="sxs-lookup"><span data-stu-id="e97c0-478">Because you must transform the results of the comparison between enumeration values and text values several times for difference sources, it's a good idea to configure this logic as a single data source.</span></span> <span data-ttu-id="e97c0-479">Jotta voisit käyttää tätä tietolähdettä uudelleen, sinun on kuitenkin määritettävä se parametrisoiduksi tietolähteeksi.</span><span class="sxs-lookup"><span data-stu-id="e97c0-479">However, to make this data source reusable, you must then configure it as the parametrized data source.</span></span> <span data-ttu-id="e97c0-480">Katso lisätietoja kohdasta [Lasketun kentän muotoisten sähköisen raportoinnin tietolähteiden parametrisoitujen kutsujen tukeminen](er-calculated-field-type.md).</span><span class="sxs-lookup"><span data-stu-id="e97c0-480">For more information, see [Support parameterized calls of ER data sources of the Calculated field type](er-calculated-field-type.md).</span></span>

1. <span data-ttu-id="e97c0-481">Valitse **Mallin määrityksen suunnittelu** -sivun **Tietolähdetyypit**-ruudusta **Yleiset\\Tyhjä säilö**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-481">On the **Model mapping designer** page, in the **Data source types** pane, select **General\\Empty container**.</span></span>
2. <span data-ttu-id="e97c0-482">Lisää uusi säilötietolähde:</span><span class="sxs-lookup"><span data-stu-id="e97c0-482">Add a new container data source:</span></span>

    1. <span data-ttu-id="e97c0-483">Valitse **Tietolähteet**-ruudussa **Lisää juuri**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-483">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="e97c0-484">Kirjoita valintaikkunan **Nimi**-kentässä **Avustaja**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-484">In the dialog box, in the **Name** field, enter **Helper**.</span></span>
    3. <span data-ttu-id="e97c0-485">Lisää uusi säilötietolähde valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-485">Select **OK** to add the new container data source.</span></span>

3. <span data-ttu-id="e97c0-486">Valitse **Tietolähdetyypit**-ruudusta **Toiminnot\\Laskettu kenttä**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-486">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="e97c0-487">Uuden tietolähteen lisääminen:</span><span class="sxs-lookup"><span data-stu-id="e97c0-487">Add a new data source:</span></span>

    1. <span data-ttu-id="e97c0-488">Valitse **Tietolähteet**-ruudussa **Avustaja**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-488">In the **Data sources** pane, select **Helper**.</span></span>
    2. <span data-ttu-id="e97c0-489">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-489">Select **Add**.</span></span>
    3. <span data-ttu-id="e97c0-490">Kirjoita valintaikkunan **Nimi**-kenttään **NoYesEnumToString**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-490">In the dialog box, in the **Name** field, enter **NoYesEnumToString**.</span></span>
    4. <span data-ttu-id="e97c0-491">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-491">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="e97c0-492">Valitse kaavaeditorissa **Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-492">In the formula editor, select **Parameters**.</span></span>
    6. <span data-ttu-id="e97c0-493">Voit määrittää parametrit määritetylle lausekkeelle noudattamalla seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="e97c0-493">Follow these steps to specify parameters for the configured expression:</span></span>

        1. <span data-ttu-id="e97c0-494">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-494">Select **New**.</span></span>
        2. <span data-ttu-id="e97c0-495">Kirjoita valintaikkunan **Nimi**-kenttään **Argumentti**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-495">In the dialog box, in the **Name** field, enter **Argument**.</span></span>
        3. <span data-ttu-id="e97c0-496">Valitse **Tyyppi**-kentässä **Totuusarvo**-tietotyyppi.</span><span class="sxs-lookup"><span data-stu-id="e97c0-496">In the **Type** field, select the **Boolean** data type.</span></span>
        4. <span data-ttu-id="e97c0-497">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-497">Select **OK**.</span></span>

    7. <span data-ttu-id="e97c0-498">Kirjoita **Kaava**-kenttään **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")**, jos haluat, että oikean varoitusetiketin teksti palautetaan sen mukaan, mikä on suorituskontekstin kieli ja määritetyn parametrin arvo.</span><span class="sxs-lookup"><span data-stu-id="e97c0-498">In the **Formula** field, enter **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** to return the text of the appropriate ER label, depending on the language of the execution context and value of the specified parameter.</span></span>
    8. <span data-ttu-id="e97c0-499">Valitse **Tallenna** ja sulje kaavaeditori.</span><span class="sxs-lookup"><span data-stu-id="e97c0-499">Select **Save**, and close the formula editor.</span></span>
    9. <span data-ttu-id="e97c0-500">Lisää uusi tietolähde valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-500">Select **OK** to add the new data source.</span></span>

![Konfiguroitu mallin määritys ER-tietomallin määrityksen suunnittelussa](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a><span data-ttu-id="e97c0-502">Tietolähteen sitominen tietomallikenttiin</span><span class="sxs-lookup"><span data-stu-id="e97c0-502">Bind data sources to data model fields</span></span>

<span data-ttu-id="e97c0-503">Sinun on sidottava määritetyt tietolähteet tietomallin kenttiin, jotta voit määrittää, miten tietomalli täytetään sovellustiedoilla suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="e97c0-503">You must bind the configured data sources to the fields of the data model to specify how the data model will by filled in with application data at runtime.</span></span>

1. <span data-ttu-id="e97c0-504">Valitse **Mallin määrityksen suunnittelu** -sivun **Tietomalli**-ruudusta **CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-504">On the **Model mapping designer** page, in the **Data model** pane, select **CompanyName**.</span></span>
2. <span data-ttu-id="e97c0-505">Laajenna **Tietolähteet**-ruudussa **CompanyInfo** ja toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e97c0-505">In the **Data sources** pane, expand **CompanyInfo**, and then follow these steps:</span></span>

    1. <span data-ttu-id="e97c0-506">Laajenna **CompanyInfo.find()**-solmu, joka vastaa CompanyInfo-taulukon **find()**-menetelmää.</span><span class="sxs-lookup"><span data-stu-id="e97c0-506">Expand the **CompanyInfo.find()** node that represents the **find()** method of the CompanyInfo table.</span></span>
    2. <span data-ttu-id="e97c0-507">Valitse **CompanyInfo.find().Name**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-507">Select **CompanyInfo.find().Name**.</span></span>
    3. <span data-ttu-id="e97c0-508">Valitse **sido**, jos haluat täyttää sen yrityksen nimen, jota konfiguroitu mallin määritys kutsuu suorituksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-508">Select **Bind** to fill in the name of the company that the configured model mapping is called in the context of at runtime.</span></span>

3. <span data-ttu-id="e97c0-509">Valitse **Tietomalli**-ruudussa **Kyselylomake**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-509">In the **Data model** pane, select **Questionnaire**.</span></span>
4. <span data-ttu-id="e97c0-510">Valitse **Tietolähteet**-ruudussa **Kyselylomake** ja valitse sitten **Sido** täyttääksesi kyselytietueet.</span><span class="sxs-lookup"><span data-stu-id="e97c0-510">In the **Data sources** pane, select **Questionnaire**, and then select **Bind** to fill in questionnaire records.</span></span>
5. <span data-ttu-id="e97c0-511">Laajenna **Tietomalli**-ruudussa **Kyselylomake** ja toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e97c0-511">In the **Data model** pane, expand **Questionnaire**, and then follow these steps:</span></span>

    1. <span data-ttu-id="e97c0-512">Valitse **Tietomalli**-ruudussa **Aktiivinen**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-512">In the **Data model** pane, select **Active**.</span></span>
    2. <span data-ttu-id="e97c0-513">Valitse **Tietomalli**-ruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-513">In the **Data model** pane, select **Edit**.</span></span>
    3. <span data-ttu-id="e97c0-514">Kirjoita **Kaava**-kenttään **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)**, jos haluat täyttää tekstin ja kielestä riippuvan tuloksen luettelointiarvojen vertailusta.</span><span class="sxs-lookup"><span data-stu-id="e97c0-514">In the **Formula** field, enter **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** to fill the text-dependent and language-dependent result of the comparison between enumeration values.</span></span>

6. <span data-ttu-id="e97c0-515">Jatka tietolähteiden sidontaa tietomallin kenttiin samalla tavalla, kunnes saavutat seuraavan tuloksen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-515">Continue to bind data sources to data model fields in the same manner until you achieve the following result.</span></span>

    | <span data-ttu-id="e97c0-516">Kentän polku</span><span class="sxs-lookup"><span data-stu-id="e97c0-516">Field path</span></span>                                              | <span data-ttu-id="e97c0-517">Tietotyyppi</span><span class="sxs-lookup"><span data-stu-id="e97c0-517">Data type</span></span>   | <span data-ttu-id="e97c0-518">Toimenpide</span><span class="sxs-lookup"><span data-stu-id="e97c0-518">Action</span></span> | <span data-ttu-id="e97c0-519">Sitova lauseke</span><span class="sxs-lookup"><span data-stu-id="e97c0-519">Binding expression</span></span> |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | <span data-ttu-id="e97c0-520">CompanyName</span><span class="sxs-lookup"><span data-stu-id="e97c0-520">CompanyName</span></span>                                             | <span data-ttu-id="e97c0-521">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-521">String</span></span>      | <span data-ttu-id="e97c0-522">Sido</span><span class="sxs-lookup"><span data-stu-id="e97c0-522">Bind</span></span>   | <span data-ttu-id="e97c0-523">CompanyInfo.'find()'.Name</span><span class="sxs-lookup"><span data-stu-id="e97c0-523">CompanyInfo.'find()'.Name</span></span> |
    | <span data-ttu-id="e97c0-524">Kyselylomake</span><span class="sxs-lookup"><span data-stu-id="e97c0-524">Questionnaire</span></span>                                           | <span data-ttu-id="e97c0-525">Tietueluettelo</span><span class="sxs-lookup"><span data-stu-id="e97c0-525">Record list</span></span> | <span data-ttu-id="e97c0-526">Sido</span><span class="sxs-lookup"><span data-stu-id="e97c0-526">Bind</span></span>   | <span data-ttu-id="e97c0-527">Kyselylomake</span><span class="sxs-lookup"><span data-stu-id="e97c0-527">Questionnaire</span></span> |
    | <span data-ttu-id="e97c0-528">Kyselylomake\\Aktiivinen</span><span class="sxs-lookup"><span data-stu-id="e97c0-528">Questionnaire\\Active</span></span>                                   | <span data-ttu-id="e97c0-529">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-529">String</span></span>      | <span data-ttu-id="e97c0-530">Muokkaa</span><span class="sxs-lookup"><span data-stu-id="e97c0-530">Edit</span></span>   | <span data-ttu-id="e97c0-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="e97c0-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="e97c0-532">Kyselylomake\\Koodi</span><span class="sxs-lookup"><span data-stu-id="e97c0-532">Questionnaire\\Code</span></span>                                     | <span data-ttu-id="e97c0-533">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-533">String</span></span>      | <span data-ttu-id="e97c0-534">Sido</span><span class="sxs-lookup"><span data-stu-id="e97c0-534">Bind</span></span>   | <span data-ttu-id="e97c0-535">\@.kmCollectionId</span><span class="sxs-lookup"><span data-stu-id="e97c0-535">\@.kmCollectionId</span></span> |
    | <span data-ttu-id="e97c0-536">Kyselylomake\\Kuvaus</span><span class="sxs-lookup"><span data-stu-id="e97c0-536">Questionnaire\\Description</span></span>                              | <span data-ttu-id="e97c0-537">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-537">String</span></span>      | <span data-ttu-id="e97c0-538">Sido</span><span class="sxs-lookup"><span data-stu-id="e97c0-538">Bind</span></span>   | <span data-ttu-id="e97c0-539">\@.Kuvaus</span><span class="sxs-lookup"><span data-stu-id="e97c0-539">\@.Description</span></span> |
    | <span data-ttu-id="e97c0-540">Kyselylomake\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="e97c0-540">Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="e97c0-541">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-541">String</span></span>      | <span data-ttu-id="e97c0-542">Sido</span><span class="sxs-lookup"><span data-stu-id="e97c0-542">Bind</span></span>   | <span data-ttu-id="e97c0-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span><span class="sxs-lookup"><span data-stu-id="e97c0-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span></span> |
    | <span data-ttu-id="e97c0-544">Kyselylomake\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="e97c0-544">Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="e97c0-545">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-545">String</span></span>      | <span data-ttu-id="e97c0-546">Muokkaa</span><span class="sxs-lookup"><span data-stu-id="e97c0-546">Edit</span></span>   | <span data-ttu-id="e97c0-547">CASE (\@.questionMode,</span><span class="sxs-lookup"><span data-stu-id="e97c0-547">CASE (\@.questionMode,</span></span><br><span data-ttu-id="e97c0-548">EnumAppQuestionOrder.Conditional, "Conditional",</span><span class="sxs-lookup"><span data-stu-id="e97c0-548">EnumAppQuestionOrder.Conditional, "Conditional",</span></span><br><span data-ttu-id="e97c0-549">EnumAppQuestionOrder.Random, "Satunnainen (kyselylomakkeen prosenttiosuus)",</span><span class="sxs-lookup"><span data-stu-id="e97c0-549">EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",</span></span><br><span data-ttu-id="e97c0-550">EnumAppQuestionOrder.RandomGroup, "Satunnainen (vastausryhmien prosenttiosuus)",</span><span class="sxs-lookup"><span data-stu-id="e97c0-550">EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",</span></span><br><span data-ttu-id="e97c0-551">EnumAppQuestionOrder.Sequence, "Sequential",</span><span class="sxs-lookup"><span data-stu-id="e97c0-551">EnumAppQuestionOrder.Sequence, "Sequential",</span></span><br><span data-ttu-id="e97c0-552">"")</span><span class="sxs-lookup"><span data-stu-id="e97c0-552">"")</span></span> |
    | <span data-ttu-id="e97c0-553">Kyselylomake\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="e97c0-553">Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="e97c0-554">Tallenna</span><span class="sxs-lookup"><span data-stu-id="e97c0-554">Record</span></span>      |        | |
    | <span data-ttu-id="e97c0-555">Kyselylomake\\ResultsGroup\\Koodi</span><span class="sxs-lookup"><span data-stu-id="e97c0-555">Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="e97c0-556">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-556">String</span></span>      | <span data-ttu-id="e97c0-557">Sido</span><span class="sxs-lookup"><span data-stu-id="e97c0-557">Bind</span></span>   | <span data-ttu-id="e97c0-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span><span class="sxs-lookup"><span data-stu-id="e97c0-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span></span> |
    | <span data-ttu-id="e97c0-559">Kyselylomake\\ResultsGroup\\Kuvaus</span><span class="sxs-lookup"><span data-stu-id="e97c0-559">Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="e97c0-560">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-560">String</span></span>      | <span data-ttu-id="e97c0-561">Sido</span><span class="sxs-lookup"><span data-stu-id="e97c0-561">Bind</span></span>   | <span data-ttu-id="e97c0-562">\@.'\$ResultGroup'.description</span><span class="sxs-lookup"><span data-stu-id="e97c0-562">\@.'\$ResultGroup'.description</span></span> |
    | <span data-ttu-id="e97c0-563">Kyselylomake\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="e97c0-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="e97c0-564">Reaaliluku</span><span class="sxs-lookup"><span data-stu-id="e97c0-564">Real</span></span>        | <span data-ttu-id="e97c0-565">Sido</span><span class="sxs-lookup"><span data-stu-id="e97c0-565">Bind</span></span>   | <span data-ttu-id="e97c0-566">\@.'\$ResultGroup'.maxPoint</span><span class="sxs-lookup"><span data-stu-id="e97c0-566">\@.'\$ResultGroup'.maxPoint</span></span> |
    | <span data-ttu-id="e97c0-567">Kyselylomake\\Kysymys</span><span class="sxs-lookup"><span data-stu-id="e97c0-567">Questionnaire\\Question</span></span>                                 | <span data-ttu-id="e97c0-568">Tietueluettelo</span><span class="sxs-lookup"><span data-stu-id="e97c0-568">Record list</span></span> | <span data-ttu-id="e97c0-569">Sido</span><span class="sxs-lookup"><span data-stu-id="e97c0-569">Bind</span></span>   | <span data-ttu-id="e97c0-570">\@.'&lt;Relations'.KMCollectionQuestion</span><span class="sxs-lookup"><span data-stu-id="e97c0-570">\@.'&lt;Relations'.KMCollectionQuestion</span></span> |
    | <span data-ttu-id="e97c0-571">Kyselylomake\\Kysymys\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="e97c0-571">Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="e97c0-572">Kokonaisluku</span><span class="sxs-lookup"><span data-stu-id="e97c0-572">Integer</span></span>     | <span data-ttu-id="e97c0-573">Sido</span><span class="sxs-lookup"><span data-stu-id="e97c0-573">Bind</span></span>   | <span data-ttu-id="e97c0-574">\@.answerCollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="e97c0-574">\@.answerCollectionSequenceNumber</span></span> |
    | <span data-ttu-id="e97c0-575">Kyselylomake\\Kysymys\\Tunnus</span><span class="sxs-lookup"><span data-stu-id="e97c0-575">Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="e97c0-576">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-576">String</span></span>      | <span data-ttu-id="e97c0-577">Sido</span><span class="sxs-lookup"><span data-stu-id="e97c0-577">Bind</span></span>   | <span data-ttu-id="e97c0-578">\@.kmQuestionId</span><span class="sxs-lookup"><span data-stu-id="e97c0-578">\@.kmQuestionId</span></span> |
    | <span data-ttu-id="e97c0-579">Kyselylomake\\Kysymys\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="e97c0-579">Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="e97c0-580">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-580">String</span></span>      | <span data-ttu-id="e97c0-581">Muokkaa</span><span class="sxs-lookup"><span data-stu-id="e97c0-581">Edit</span></span>   | <span data-ttu-id="e97c0-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="e97c0-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="e97c0-583">Kyselylomake\\Kysymys\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="e97c0-583">Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="e97c0-584">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-584">String</span></span>      | <span data-ttu-id="e97c0-585">Sido</span><span class="sxs-lookup"><span data-stu-id="e97c0-585">Bind</span></span>   | <span data-ttu-id="e97c0-586">\@.parentQuestionId</span><span class="sxs-lookup"><span data-stu-id="e97c0-586">\@.parentQuestionId</span></span> |
    | <span data-ttu-id="e97c0-587">Kyselylomake\\Kysymys\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="e97c0-587">Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="e97c0-588">Kokonaisluku</span><span class="sxs-lookup"><span data-stu-id="e97c0-588">Integer</span></span>     | <span data-ttu-id="e97c0-589">Sido</span><span class="sxs-lookup"><span data-stu-id="e97c0-589">Bind</span></span>   | <span data-ttu-id="e97c0-590">\@.SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="e97c0-590">\@.SequenceNumber</span></span> |
    | <span data-ttu-id="e97c0-591">Kyselylomake\\Kysymys\\Teksti</span><span class="sxs-lookup"><span data-stu-id="e97c0-591">Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="e97c0-592">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-592">String</span></span>      | <span data-ttu-id="e97c0-593">Sido</span><span class="sxs-lookup"><span data-stu-id="e97c0-593">Bind</span></span>   | <span data-ttu-id="e97c0-594">\@.'\$Question'.text</span><span class="sxs-lookup"><span data-stu-id="e97c0-594">\@.'\$Question'.text</span></span> |
    | <span data-ttu-id="e97c0-595">Kyselylomake\\Kysymys\\Vastaus</span><span class="sxs-lookup"><span data-stu-id="e97c0-595">Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="e97c0-596">Tietueluettelo</span><span class="sxs-lookup"><span data-stu-id="e97c0-596">Record list</span></span> | <span data-ttu-id="e97c0-597">Sido</span><span class="sxs-lookup"><span data-stu-id="e97c0-597">Bind</span></span>   | <span data-ttu-id="e97c0-598">\@.'\$Question'.'\$Answer'</span><span class="sxs-lookup"><span data-stu-id="e97c0-598">\@.'\$Question'.'\$Answer'</span></span> |
    | <span data-ttu-id="e97c0-599">Kyselylomake\\Kysymys\\Vastaus\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="e97c0-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="e97c0-600">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-600">String</span></span>      | <span data-ttu-id="e97c0-601">Muokkaa</span><span class="sxs-lookup"><span data-stu-id="e97c0-601">Edit</span></span>   | <span data-ttu-id="e97c0-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="e97c0-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="e97c0-603">Kyselylomake\\Kysymys\\Vastaus\\Pisteet</span><span class="sxs-lookup"><span data-stu-id="e97c0-603">Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="e97c0-604">Reaaliluku</span><span class="sxs-lookup"><span data-stu-id="e97c0-604">Real</span></span>        | <span data-ttu-id="e97c0-605">Sido</span><span class="sxs-lookup"><span data-stu-id="e97c0-605">Bind</span></span>   | <span data-ttu-id="e97c0-606">\@.point</span><span class="sxs-lookup"><span data-stu-id="e97c0-606">\@.point</span></span> |
    | <span data-ttu-id="e97c0-607">Kyselylomake\\Kysymys\\Vastaus\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="e97c0-607">Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="e97c0-608">Kokonaisluku</span><span class="sxs-lookup"><span data-stu-id="e97c0-608">Integer</span></span>     | <span data-ttu-id="e97c0-609">Sido</span><span class="sxs-lookup"><span data-stu-id="e97c0-609">Bind</span></span>   | <span data-ttu-id="e97c0-610">\@.sequenceNumber</span><span class="sxs-lookup"><span data-stu-id="e97c0-610">\@.sequenceNumber</span></span> |
    | <span data-ttu-id="e97c0-611">Kyselylomake\\Kysymys\\Vastaus\\Teksti</span><span class="sxs-lookup"><span data-stu-id="e97c0-611">Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="e97c0-612">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="e97c0-612">String</span></span>      | <span data-ttu-id="e97c0-613">Sido</span><span class="sxs-lookup"><span data-stu-id="e97c0-613">Bind</span></span>   | <span data-ttu-id="e97c0-614">\@.text</span><span class="sxs-lookup"><span data-stu-id="e97c0-614">\@.text</span></span> |

    <span data-ttu-id="e97c0-615">Seuraavassa kuvassa näkyy **mallikartoituksen suunnittelu** -sivulla määritetyn mallikartoituksen lopullinen tila.</span><span class="sxs-lookup"><span data-stu-id="e97c0-615">The following illustration shows the final state of the configured model mapping on the **Model mapping designer** page.</span></span>

    ![Täysin konfiguroitu mallin määritys ER-tietomallin määrityksen suunnittelussa](./media/er-quick-start1-mapping2.png)

7. <span data-ttu-id="e97c0-617">Tallenna muutokset.</span><span class="sxs-lookup"><span data-stu-id="e97c0-617">Save your changes.</span></span>
8. <span data-ttu-id="e97c0-618">Sulje **Mallimäärityksen sunnittelun** sivu.</span><span class="sxs-lookup"><span data-stu-id="e97c0-618">Close the **Model mapping designer** page.</span></span>

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a><span data-ttu-id="e97c0-619">Mallin määrityksen rakenteen täydentäminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-619">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="e97c0-620">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-620">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e97c0-621">Valitse **Konfiguraatiot**-sivun konfiguraatiopuun kohdasta **Kyselylomakkeen yhdistäminen**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-621">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="e97c0-622">Valitse **Versiot**-pikavälilehdessä konfiguraatioversio, jonka tila on **Luonnos**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-622">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="e97c0-623">Valitse **Muutoksen tila** \> **Viimeistele**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-623">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="e97c0-624">Tämän konfiguraation version 1.1 tila muutetaan **luonnoksesta** **valmiiksi**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-624">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="e97c0-625">Versiota 1.1 ei voi enää muuttaa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-625">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="e97c0-626">Tämä versio sisältää konfiguroidun mallin määrityksen, ja sitä voidaan käyttää muiden ER-konfiguraatioiden pohjana.</span><span class="sxs-lookup"><span data-stu-id="e97c0-626">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="e97c0-627">Tämän konfiguraation versio 1.2 luodaan, ja sen tila on **luonnos**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-627">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="e97c0-628">Voit muokata tätä versiota, jos haluat muuttaa **kyselylomakkeen määrityksen** määritystä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-628">You can edit this version to adjust the **Questionnaire mapping** configuration.</span></span>

![Konfiguraatiosivun muokattavan ER-konfiguraation versiot](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> <span data-ttu-id="e97c0-630">Määritetty mallimääritys on **kyselylomakkeen** liiketoimialuetta edustavan abstraktin tietomallin Finance-kohtainen toteutus.</span><span class="sxs-lookup"><span data-stu-id="e97c0-630">The configured model mapping is your Finance-specific implementation of the abstract data model that represents the **Questionnaire** business domain.</span></span>

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a><span data-ttu-id="e97c0-631">Mukautetun raportin mallin suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-631">Design a template for a custom report</span></span>

<span data-ttu-id="e97c0-632">ER-kehys käyttää ennalta määritettyjä malleja luodakseen tiedostoja Microsoft Office -muodoissa (Excel-työkirjoissa tai Word-asiakirjoissa).</span><span class="sxs-lookup"><span data-stu-id="e97c0-632">The ER framework uses predefined templates to generate reports in Microsoft Office formats (Excel workbooks or Word documents).</span></span> <span data-ttu-id="e97c0-633">Kun tarvittava raportti luodaan, malliin täytetään tarvittavat tiedot määritetyn tietovuomäärityksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e97c0-633">While the required report is being generated, a template is filled in with required data according to the configured dataflow.</span></span> <span data-ttu-id="e97c0-634">Siksi sinun on ensin suunniteltava malli mukautettua raporttia varten.</span><span class="sxs-lookup"><span data-stu-id="e97c0-634">Therefore, you must first design a template for your custom report.</span></span> <span data-ttu-id="e97c0-635">Tämä malli on suunniteltava Excel-työkirjana, jonka rakenne edustaa mukautetun raportin asettelua.</span><span class="sxs-lookup"><span data-stu-id="e97c0-635">This template must be designed as an Excel workbook, the structure of which represents the layout of a custom report.</span></span> <span data-ttu-id="e97c0-636">Sinun on annettava jokaiselle Excel-kohteelle nimi, jonka aiot täyttää vaaditulla tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="e97c0-636">You must name every Excel item that you plan to fill in with required data.</span></span>

1. <span data-ttu-id="e97c0-637">Lataa [kyselylomakkeiden raporttimalli.xslx](https://go.microsoft.com/fwlink/?linkid=851448) -tiedosto ja tallenna se paikalliseen tietokoneeseen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-637">Download the [Questionnaires report template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="e97c0-638">Avaa tiedosto Excelissä ja tarkista työkirjan rakenne.</span><span class="sxs-lookup"><span data-stu-id="e97c0-638">Open the file in Excel, and review the structure of the workbook.</span></span>

<span data-ttu-id="e97c0-639">Kuten seuraavasta kuvasta näkyy, ladattu malli on suunniteltu tulostamaan kyselylomakkeita, joissa esitetään kyselyn kysymykset sekä asianmukaiset vastaukset.</span><span class="sxs-lookup"><span data-stu-id="e97c0-639">As the following illustration shows, the downloaded template has been designed to print specified questionnaires that present a questionnaire's questions together with appropriate answers.</span></span>

![Excel-malli määritettyjen kyselylomakkeiden tulostamista varten](./media/er-quick-start1-template-layout.png)

<span data-ttu-id="e97c0-641">Tähän malliin on lisätty Excel-nimiä kyselylomakkeen tietojen täyttämistä varten.</span><span class="sxs-lookup"><span data-stu-id="e97c0-641">Excel names have been added to this template to fill in the questionnaire details.</span></span> <span data-ttu-id="e97c0-642">Nimien hallinnan avulla voit tarkistaa Excelin nimet.</span><span class="sxs-lookup"><span data-stu-id="e97c0-642">You can use Name Manager to review the Excel names.</span></span>

![Nimen hallinnan käyttäminen Excelin nimien tarkistamiseen annetussa Excel-mallissa](./media/er-quick-start1-template-names.png)

<span data-ttu-id="e97c0-644">Raportin otsikot on lisätty englannin kielellä vakiotekstinä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-644">Report labels have been added as fixed text in the English language.</span></span> <span data-ttu-id="e97c0-645">Voit korvata raportin otsikot uusilla Excelin nimillä, jotka täyttävät otsikot ja kielikohtaiset tekstit, käyttämällä ER-muodon [otsikoita](#AddMmLabels), kuten teit kielikohtaisten lausekkeiden osalta määritetyssä mallin yhdistämismäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-645">You can replace the report labels with new Excel names that fill in the labels with language-dependent text by using the ER format [labels](#AddMmLabels), as you did for language-dependent expressions in the configured model mapping.</span></span> <span data-ttu-id="e97c0-646">Tässä tapauksessa ER-etiketit on lisättävä muokattavaan ER-muotoon.</span><span class="sxs-lookup"><span data-stu-id="e97c0-646">In this case, ER labels must be added in the editable ER format.</span></span>

<span data-ttu-id="e97c0-647">Kuten seuraavasta kuvasta näkyy, mukautetun raportin otsikko on määritetty, jotta Excel voi tehdä sivutustyön.</span><span class="sxs-lookup"><span data-stu-id="e97c0-647">As the following illustration shows, the custom report header has been specified to enable Excel to do paging.</span></span>

![Mukautetun raportin ylätunniste annetussa Excel-mallissa](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a><span data-ttu-id="e97c0-649">Muodon suunnittelu</span><span class="sxs-lookup"><span data-stu-id="e97c0-649">Design a format</span></span>

<span data-ttu-id="e97c0-650">Sähköisen raportoinnin toiminnallinen konsultti -roolin käyttäjänä sinun on luotava uusi ER-konfiguraatio, joka sisältää [muoto](general-electronic-reporting.md#FormatComponentOutbound)-komponentin.</span><span class="sxs-lookup"><span data-stu-id="e97c0-650">As a user in the Electronic Reporting Functional Consultant role, you must create a new ER configuration that contains a [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="e97c0-651">Muotokomponentti on konfiguroitava siten, että se määrittää, miten raporttimalli täytetään vaadituilla tiedoilla suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="e97c0-651">You must configure the format component to specify how a report template will be filled in with required data at runtime.</span></span>

<span data-ttu-id="e97c0-652">Kun [tuot suunnitellun mallinmääritys](#FormatImport) -osan vaiheet, voit tuoda vaaditun muodon mukana olevasta XML-tiedostosta.</span><span class="sxs-lookup"><span data-stu-id="e97c0-652">By completing the steps in the [Import a designed format configuration](#FormatImport) section, you can import the required format from the provided XML file.</span></span> <span data-ttu-id="e97c0-653">Voit myös suorittaa [uuden muodon määrityksen luomisen](#FormatCreate) vaiheet ja suunnitella tämän muodon alusta alkaen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-653">Alternatively, you can complete the steps in the [Create a new format configuration](#FormatCreate) section to design this format from scratch.</span></span>

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a><span data-ttu-id="e97c0-654">Tuo suunniteltu muotokonfiguraatio</span><span class="sxs-lookup"><span data-stu-id="e97c0-654">Import a designed format configuration</span></span>

1. <span data-ttu-id="e97c0-655">Lataa [kyselylomakkeiden muoto.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) -tiedosto ja tallenna se paikalliseen tietokoneeseen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-655">Download the [Questionnaires format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="e97c0-656">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-656">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="e97c0-657">Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-657">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="e97c0-658">Valitse toimintoruudussa **Vaihda** \> **Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-658">On the Action pane, Select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="e97c0-659">Valitse **Selaa** ja etsi ja valitse **kyselylomakkeiden format.version.1.1.xml** -tiedosto.</span><span class="sxs-lookup"><span data-stu-id="e97c0-659">Select **Browse**, and then find and select the **Questionnaires format.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="e97c0-660">Tuo konfigurointi valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-660">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="e97c0-661">Jos haluat jatkaa, ohita seuraavat vaiheet, [Luo uusi muotokonfiguraatio](#FormatCreate).</span><span class="sxs-lookup"><span data-stu-id="e97c0-661">To continue, skip the next procedure, [Create a new format configuration](#FormatCreate).</span></span>

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a><span data-ttu-id="e97c0-662">Uuden muotokonfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="e97c0-662">Create a new format configuration</span></span>
 
1. <span data-ttu-id="e97c0-663">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-663">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e97c0-664">Valitse **Konfiguraatiot**-sivun konfiguraatiopuun kohdasta **Kyselylomakemalli**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-664">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="e97c0-665">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-665">Select **Create configuration**.</span></span>
4. <span data-ttu-id="e97c0-666">Toimi avattavassa valintaikkunassa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e97c0-666">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="e97c0-667">Syötä **Uusi**-kenttään **Tietomallikyselylomakkeisiin perustuva muoto**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-667">In the **New** field, select **Format based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="e97c0-668">Kirjoita **Nimi**-kenttään **Kyselylomakkeen raportti**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-668">In the **Name** field, enter **Questionnaire report**.</span></span>
    3. <span data-ttu-id="e97c0-669">Valitse **Tietomallin määritelmä** -kentässä **1**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-669">In the **Data model version** field, select **1**.</span></span>

        > [!NOTE]
        > - <span data-ttu-id="e97c0-670">Jos valitset perustietomallin jonkin tietyn version, tietomallin vastaavan version rakenne näytetään **Malli**-tietolähteen rakenteena luodussa muodossa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-670">If you select a specific version of the base data model, the structure of the corresponding version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span>
        > - <span data-ttu-id="e97c0-671">Kenttä voidaan jättää tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="e97c0-671">You can leave this field blank.</span></span> <span data-ttu-id="e97c0-672">Tässä tapauksessa tietomallin **Luonnos**-version rakenne esitetään **Malli**-tietolähteen rakenteena luotavan mallin muodossa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-672">In that case, the structure of the **Draft** version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span> <span data-ttu-id="e97c0-673">Tämän jälkeen voit muokata malliasi ja nähdä nämä muutokset heti muodossa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-673">You can then adjust your model and immediately see those adjustments in your format.</span></span> <span data-ttu-id="e97c0-674">Tämä lähestymistapa voi parantaa ER-ratkaisun suunnittelun tehokkuutta, kun määrität tietomallin, mallin yhdistämisen ja muodon samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="e97c0-674">This approach might improve the efficiency of ER solution design when you configure your data model, model mapping, and format simultaneously.</span></span>
        > - <span data-ttu-id="e97c0-675">Jos valitset perustietomallin tietyn version, voit siirtyä käyttämään **Luonnos**-versiota myöhemmin, kun aloitat muodon muokkaamisen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-675">If you select a specific version of the base data model, you can switch to using the **Draft** version later, when you start to edit a format.</span></span>

    4. <span data-ttu-id="e97c0-676">**Valitse tietomallin määritys** -kentässä **Juuri**-määritys.</span><span class="sxs-lookup"><span data-stu-id="e97c0-676">In the **Data model definition** field, select the **Root** definition.</span></span>

5. <span data-ttu-id="e97c0-677">Valitse **Luo konfigurointi** luodaksesi konfiguroinnin.</span><span class="sxs-lookup"><span data-stu-id="e97c0-677">Select **Create configuration** to create the configuration.</span></span>

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a><span data-ttu-id="e97c0-678">Tuo raporttimalli</span><span class="sxs-lookup"><span data-stu-id="e97c0-678">Import a report template</span></span>

1. <span data-ttu-id="e97c0-679">Valitse **Konfiguraatiot**-sivun konfiguraatiopuun kohdasta **Kyselylomakeraportti**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-679">On the **Configurations** page, in the configuration tree, select **Questionnaire report**.</span></span>
2. <span data-ttu-id="e97c0-680">Aloita mukautetun muodon määrittäminen valitsemalla **suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-680">Select **Designer** to start to configure a custom format.</span></span>
3. <span data-ttu-id="e97c0-681">Valitse **Muodon suunnittelija** -sivulla hallintapaneelista **Tuo** \> **Tuo Excelistä**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-681">On the **Format designer** page, on the Action Pane, select **Import** \> **Import from Excel**.</span></span>
4. <span data-ttu-id="e97c0-682">Toimi valintaikkunassa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e97c0-682">In the dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="e97c0-683">Valitse **Lisää malli**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-683">Select **Add template**.</span></span>
    2. <span data-ttu-id="e97c0-684">Etsi ja valitse paikallisesti tallennettu **Kyselylomakkeen raporttimalli.xslx** -tiedosto ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-684">Find and select the locally saved **Questionnaires report template.xslx** file, and then select **Open**.</span></span>
    3. <span data-ttu-id="e97c0-685">Tuo malli valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-685">Select **OK** to import the template.</span></span>

    ![Raporttimallin tuominen](./media/er-quick-start1-template-import.png)

<span data-ttu-id="e97c0-687">**Excel\\Tiedosto**-muotoelementti lisätään automaattisesti muokattavaan muotoon juurielementtinä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-687">The **Excel\\File** format element is automatically added to the editable format as a root element.</span></span> <span data-ttu-id="e97c0-688">Lisäksi **Excel\\Alue**-muotoelementti tai **Excel\\Solu**-muotoelementti lisätään automaattisesti jokaista tunnistettua Excel-mallin nimeä varten.</span><span class="sxs-lookup"><span data-stu-id="e97c0-688">Additionally, either the **Excel\\Range** format element or the **Excel\\Cell** format element is automatically added for every recognized Excel name of the imported template.</span></span> <span data-ttu-id="e97c0-689">**Excel\\Otsikko**-muoto, joka sisältää sisäkkäisen **Merkkijono**- elementin, lisätään automaattisesti tuodun mallin otsikkoasetusten mukaiseksi.</span><span class="sxs-lookup"><span data-stu-id="e97c0-689">The **Excel\\Header** format that has the nested **String** element is automatically added to reflect the header settings of the imported template.</span></span>

![Muotorakenne, joka sisältää automaattisesti lisätyt elementit ER-toiminnon suunnittelussa](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a><span data-ttu-id="e97c0-691">Muodon konfigurointi</span><span class="sxs-lookup"><span data-stu-id="e97c0-691">Configure a format</span></span>

1. <span data-ttu-id="e97c0-692">Valitse **Muotoilun suunnittelu** -sivun muotoilupuusta **Excel**-juurielementti.</span><span class="sxs-lookup"><span data-stu-id="e97c0-692">On the **Format designer** page, in the format tree, select the **Excel** root element.</span></span>
2. <span data-ttu-id="e97c0-693">Kirjoita sivun oikeassa reunassa olevan **Muoto**-välilehden **Nimi**-kenttään <a name="AddFormatRootElement"></a>**Raportti**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-693">On the **Format** tab on the right side of the page, in the **Name** field, enter <a name="AddFormatRootElement"></a>**Report**.</span></span>
3. <span data-ttu-id="e97c0-694">Valitse **Kieliasetus**-kentästä **käyttäjäasetus**, jos haluat suorittaa raportin käyttäjän ensisijaisella kielellä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-694">In the **Language preference** field, select **User preference** to run the report in the user's preferred language.</span></span>
4. <span data-ttu-id="e97c0-695">Valitse **Kulttuuriasetus**-kentästä **käyttäjäasetus**, jos haluat suorittaa raportin käyttäjän ensisijaisessa kulttuurissa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-695">In the **Culture preference** field, select **User preference** to run the report in the user's preferred culture.</span></span>

    <span data-ttu-id="e97c0-696">Lisätietoja ER-prosessin kieli- ja kulttuurikonteksteista on ohjeaiheessa [Monikielisten raporttien suunnitteleminen](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="e97c0-696">For information about how to specify the language and culture contexts for an ER process, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

    ![Suunnitellun raportin kieli- ja kulttuuriasetusten määrittäminen ER-toiminnon suunnittelussa](./media/er-quick-start1-template-format-structure1.png)

5. <span data-ttu-id="e97c0-698">Laajenna pääsolmu muotopuussa ja valitse sitten **ResultsGroup**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-698">In the format tree, expand the root node, and then select **ResultsGroup**.</span></span>
6. <span data-ttu-id="e97c0-699">Valitse **Muoto**-välilehden **Replikointisuunta** -kentästä **Ei replikaatiota**, koska yksittäiselle kyselylomakkeelle ei odoteta olevan useita tulosryhmiä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-699">On the **Format** tab, in the **Replication direction** field, select **No replication**, because you don't expect to have multiple result groups for a single questionnaire.</span></span>

    ![Aluemuotoelementtien replikointisuunnan määrittäminen ER-toiminnon suunnittelussa](./media/er-quick-start1-template-format-structure2.png)

7. <span data-ttu-id="e97c0-701">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-701">Select **Save**.</span></span>

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a><span data-ttu-id="e97c0-702">Raportin otsikon tietojen sidonnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-702">Define the data binding for a report title</span></span>

<span data-ttu-id="e97c0-703">Sinun on määritettävä tietosidontamuoto elementille, jota käytetään luodun raportin otsikon täyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-703">You must specify a data binding for a format element that is used to fill in the title of a generated report.</span></span>

1. <span data-ttu-id="e97c0-704">Valitse **Muodon suunnittelija** -sivun oikealta puolelta **Määritys**-välilehdeltä **Raportti\\ReportTitle**-elementti.</span><span class="sxs-lookup"><span data-stu-id="e97c0-704">On the **Format designer** page, on the **Mapping** tab on the right, select the **Report\\ReportTitle** element.</span></span>
2. <span data-ttu-id="e97c0-705">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-705">Select **Edit formula**.</span></span>
3. <span data-ttu-id="e97c0-706">Valitse kaavaeditorissa **Käännä**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-706">In the formula editor, select **Translate**.</span></span>
4. <span data-ttu-id="e97c0-707">Toimi **Tekstin kääntäminen** -valintaikkunassa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e97c0-707">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="e97c0-708">Kirjoita **Etiketin tunnus**-kenttään **ReportTitle**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-708">In the **Label ID** field, enter **ReportTitle**.</span></span>
    2. <span data-ttu-id="e97c0-709">Kirjoita **Teksti oletuskielellä** -kenttään **Kyselylomakeraportti**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-709">In the **Text in default language** field, enter **Questionnaires report**.</span></span>
    3. <span data-ttu-id="e97c0-710">Valitse ensin **Käännä** ja sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-710">Select **Translate**, and then select **Save**.</span></span>
    4. <span data-ttu-id="e97c0-711">Valitse **Käännä**, jos haluat sulkea **Tekstin kääntäminen** -valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="e97c0-711">Select **Translate** to close the **Text translation** dialog box.</span></span>

5. <span data-ttu-id="e97c0-712">Sulje kaavaeditori.</span><span class="sxs-lookup"><span data-stu-id="e97c0-712">Close the formula editor.</span></span>

    ![Sidonnan määrittäminen täyttämään luodun raportin otsikko](./media/er-quick-start1-add-report-title-label.png)

<span data-ttu-id="e97c0-714">Tämän tekniikan avulla voit tehdä kaikki muut nykyisen mallin kielikohtaiset otsikot.</span><span class="sxs-lookup"><span data-stu-id="e97c0-714">You can use this technique to make all other labels of the current template language-dependent.</span></span> <span data-ttu-id="e97c0-715">Lisätietoja yhden ER-kokoonpanon lisättyjen otsikoiden kääntämisestä kaikille tuetuille kielille on ohjeaiheessa [monikielisten raporttien suunnitteleminen](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="e97c0-715">For information about how the added labels of a single ER configuration can be translated into all supported languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a><span data-ttu-id="e97c0-716">Mallin tietolähteen tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-716">Review model data source</span></span>

1. <span data-ttu-id="e97c0-717">Valitse **Muotoile suunnittelua** -sivun **Yhdistämismääritys**-välilehdessä <a name="ModelDSName"></a>**mallin** tietolähde, joka edustaa tämän ER-muodon perustietomallia.</span><span class="sxs-lookup"><span data-stu-id="e97c0-717">On the **Format designer** page, on the **Mapping** tab, select the <a name="ModelDSName"></a>**model** data source that represents the base data model of this ER format.</span></span>
2. <span data-ttu-id="e97c0-718">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-718">Select **Edit**.</span></span>
3. <span data-ttu-id="e97c0-719">Tarkista **tietolähteen ominaisuudet** -valintaikkunan tiedot.</span><span class="sxs-lookup"><span data-stu-id="e97c0-719">Review the information in the **Data source properties** dialog box.</span></span> <span data-ttu-id="e97c0-720">Tämä tietolähde edustaa **kyselylomakemallin** ER-määrityksissä sijaitsevan **kyselylomakkeen** tietomallikomponentin versiota 1.</span><span class="sxs-lookup"><span data-stu-id="e97c0-720">This data source represents version 1 of the **Questionnaires** data model component that resides in the **Questionnaires model** ER configuration.</span></span>

![ER-toimintojen suunnitteluohjelman mallitietolähteen tiedot](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a><span data-ttu-id="e97c0-722">Muotoelementtien sidonta tietolähdekenttiin</span><span class="sxs-lookup"><span data-stu-id="e97c0-722">Bind format elements to data source fields</span></span>

<span data-ttu-id="e97c0-723">Jos haluat määrittää, miten malli täytetään suorituksen aikana, sinun on sidottava kaikki sopivaan Excel-nimeen liittyvät muotoiluelementit yhteen tämän muodon tietolähteen yksittäiseen kenttään.</span><span class="sxs-lookup"><span data-stu-id="e97c0-723">To specify how a template is filled in at runtime, you must bind every format element that is associated with an appropriate Excel name to a single field of this format's data source.</span></span>

1. <span data-ttu-id="e97c0-724">Valitse **Muotoilun suunnittelu** -sivun muotoilupuusta **Raportti\\CompanyName**-muotoelementti.</span><span class="sxs-lookup"><span data-stu-id="e97c0-724">On the **Format designer** page, in the format tree, select the **Report\\CompanyName** format element.</span></span>
2. <span data-ttu-id="e97c0-725">Valitse **Yhdistämismääritys**-välilehdestä **model.CompanyName**-tietolähdekenttä **merkkijono**-tyypistä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-725">On the **Mapping** tab, select the **model.CompanyName** data source field of the **String** type.</span></span>
3. <span data-ttu-id="e97c0-726">Määritä yrityksen nimi malliin valitsemalla **sido**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-726">Select **Bind** to enter a company name in a template.</span></span>
4. <span data-ttu-id="e97c0-727">Valitse muotopuusta **Raportti\\kyselylomake**-elementti.</span><span class="sxs-lookup"><span data-stu-id="e97c0-727">In the format tree, select the **Report\\Questionnaire** element.</span></span>
5. <span data-ttu-id="e97c0-728">Valitse **Yhdistämismääritys**-välilehdestä **model.Questionnaire**-tietolähdekenttä **Tietueluettelo**-tyypistä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-728">On the **Mapping** tab, select the **model.Questionnaire** data source field of the **Record list** type.</span></span>
6. <span data-ttu-id="e97c0-729">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-729">Select **Bind**.</span></span>
7. <span data-ttu-id="e97c0-730">Valitsemalla **Näytä tiedot** saat näkyviin lisätietoja muotoiluelementeistä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-730">Select **Show details** to see more details for format elements.</span></span>

    <span data-ttu-id="e97c0-731">**Kyselylomakkeen** alueen muotoelementti määritetään pystysuunnassa replikoitavaksi.</span><span class="sxs-lookup"><span data-stu-id="e97c0-731">The **Questionnaire** range format element is configured as vertically replicated.</span></span> <span data-ttu-id="e97c0-732">Kun **tietueluettelo**-tyypin tietolähteeseen on sidottu Excel-mallin asianmukainen **kyselylomake**-alue, se toistetaan sidotun tietolähteen jokaisen tietueen osalta.</span><span class="sxs-lookup"><span data-stu-id="e97c0-732">When it's bound to a data source of the **Record list** type, the appropriate **Questionnaire** range of the Excel template is repeated for every record of the bound data source.</span></span>
 
    ![Kyselylomakkeen aluemuodon elementin sitominen asianmukaisiin tietueluettelon tietolähteisiin ER-toiminnon suunnittelussa](./media/er-quick-start1-bindings1.png)

    <span data-ttu-id="e97c0-734">Koska Excel-mallin **kyselylomakkeen** alue on määritetty rivien 5-14 välillä, nämä rivit toistetaan aina raportoitua kyselylomaketta käyttäen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-734">Because the **Questionnaire** range of the Excel template is defined between rows 5 through 14, these rows are repeated for every reported questionnaire.</span></span>

    ![Excel-mallin rivit, jotka toistetaan muodostettuun raporttiin tietueluettelon tietolähteiden jokaisesta tietueesta](./media/er-quick-start1-template-questionnaire-range.png)

8. <span data-ttu-id="e97c0-736">Määritä muiden muotoelementtien samanlaiset sidonnat seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="e97c0-736">Configure similar bindings for the remaining format elements, as described in the following table.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e97c0-737">Tässä taulukossa "tietolähteen polku" -sarakkeen tiedoilla oletetaan, että [suhteellinen polun](relative-path-data-bindings-er-models-format.md) ER-toiminto on käytössä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-737">In this table, the information in the "Data source path" column assumes that the [relative path](relative-path-data-bindings-er-models-format.md) ER feature is turned on.</span></span>

    | <span data-ttu-id="e97c0-738">Muotoile elementin polku</span><span class="sxs-lookup"><span data-stu-id="e97c0-738">Format element path</span></span>                                      | <span data-ttu-id="e97c0-739">Tietolähteen polku</span><span class="sxs-lookup"><span data-stu-id="e97c0-739">Data source path</span></span> |
    |----------------------------------------------------------|------------------|
    | <span data-ttu-id="e97c0-740">Excel\\ReportTitle</span><span class="sxs-lookup"><span data-stu-id="e97c0-740">Excel\\ReportTitle</span></span>                                       | <span data-ttu-id="e97c0-741">**\@"GER\_LABEL:ReportTitle"**</span><span class="sxs-lookup"><span data-stu-id="e97c0-741">**\@"GER\_LABEL:ReportTitle"**</span></span> |
    | <span data-ttu-id="e97c0-742">Excel\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="e97c0-742">Excel\\CompanyName</span></span>                                       | <span data-ttu-id="e97c0-743">**model.CompanyName**</span><span class="sxs-lookup"><span data-stu-id="e97c0-743">**model.CompanyName**</span></span> |
    | <span data-ttu-id="e97c0-744">Excel\\Kyselylomake</span><span class="sxs-lookup"><span data-stu-id="e97c0-744">Excel\\Questionnaire</span></span>                                     | <span data-ttu-id="e97c0-745">**model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="e97c0-745">**model.Questionnaire**</span></span> |
    | <span data-ttu-id="e97c0-746">Excel\\Kyselylomake\\Aktiivinen</span><span class="sxs-lookup"><span data-stu-id="e97c0-746">Excel\\Questionnaire\\Active</span></span>                             | <span data-ttu-id="e97c0-747">**\@.Active**, where **\@** is **model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="e97c0-747">**\@.Active**, where **\@** is **model.Questionnaire**</span></span> |
    | <span data-ttu-id="e97c0-748">Excel\\Kyselylomake\\Koodi</span><span class="sxs-lookup"><span data-stu-id="e97c0-748">Excel\\Questionnaire\\Code</span></span>                               | <span data-ttu-id="e97c0-749">**\@.Code**</span><span class="sxs-lookup"><span data-stu-id="e97c0-749">**\@.Code**</span></span> |
    | <span data-ttu-id="e97c0-750">Excel\\Kyselylomake\\Kuvaus</span><span class="sxs-lookup"><span data-stu-id="e97c0-750">Excel\\Questionnaire\\Description</span></span>                        | <span data-ttu-id="e97c0-751">**\@.Description**</span><span class="sxs-lookup"><span data-stu-id="e97c0-751">**\@.Description**</span></span> |
    | <span data-ttu-id="e97c0-752">Excel\\Kyselylomake\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="e97c0-752">Excel\\Questionnaire\\QuestionnaireType</span></span>                  | <span data-ttu-id="e97c0-753">**\@.QuestionnaireType**</span><span class="sxs-lookup"><span data-stu-id="e97c0-753">**\@.QuestionnaireType**</span></span> |
    | <span data-ttu-id="e97c0-754">Excel\\Kyselylomake\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="e97c0-754">Excel\\Questionnaire\\QuestionOrder</span></span>                      | <span data-ttu-id="e97c0-755">**\@.QuestionOrder**</span><span class="sxs-lookup"><span data-stu-id="e97c0-755">**\@.QuestionOrder**</span></span> |
    | <span data-ttu-id="e97c0-756">Excel\\Kyselylomake\\ResultsGroup\\Koodi\_</span><span class="sxs-lookup"><span data-stu-id="e97c0-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span></span>               | <span data-ttu-id="e97c0-757">**\@.ResultsGroup.Code**</span><span class="sxs-lookup"><span data-stu-id="e97c0-757">**\@.ResultsGroup.Code**</span></span> |
    | <span data-ttu-id="e97c0-758">Excel\\Kyselylomake\\ResultsGroup\\Kuvaus\_</span><span class="sxs-lookup"><span data-stu-id="e97c0-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span></span>        | <span data-ttu-id="e97c0-759">**\@.ResultsGroup.Description**</span><span class="sxs-lookup"><span data-stu-id="e97c0-759">**\@.ResultsGroup.Description**</span></span> |
    | <span data-ttu-id="e97c0-760">Excel\\Kyselylomake\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="e97c0-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>    | <span data-ttu-id="e97c0-761">**\@.ResultsGroup.MaxNumberOfPoint**</span><span class="sxs-lookup"><span data-stu-id="e97c0-761">**\@.ResultsGroup.MaxNumberOfPoint**</span></span> |
    | <span data-ttu-id="e97c0-762">Excel\\Kyselylomake\\Kysymys</span><span class="sxs-lookup"><span data-stu-id="e97c0-762">Excel\\Questionnaire\\Question</span></span>                           | <span data-ttu-id="e97c0-763">**\@.Question**</span><span class="sxs-lookup"><span data-stu-id="e97c0-763">**\@.Question**</span></span> |
    | <span data-ttu-id="e97c0-764">Excel\\Kyselylomake\\Kysymys\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="e97c0-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span></span> | <span data-ttu-id="e97c0-765">**\@.CollectionSequenceNumber**, where **\@** is **model.Questionnaire.Question**</span><span class="sxs-lookup"><span data-stu-id="e97c0-765">**\@.CollectionSequenceNumber**, where **\@** is **model.Questionnaire.Question**</span></span> |
    | <span data-ttu-id="e97c0-766">Excel\\Kyselylomake\\Kysymys\\Tunnus</span><span class="sxs-lookup"><span data-stu-id="e97c0-766">Excel\\Questionnaire\\Question\\Id</span></span>                       | <span data-ttu-id="e97c0-767">**\@.Id**</span><span class="sxs-lookup"><span data-stu-id="e97c0-767">**\@.Id**</span></span> |
    | <span data-ttu-id="e97c0-768">Excel\\Kyselylomake\\Kysymys\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="e97c0-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span></span>          | <span data-ttu-id="e97c0-769">**\@.MustBeCompleted**</span><span class="sxs-lookup"><span data-stu-id="e97c0-769">**\@.MustBeCompleted**</span></span> |
    | <span data-ttu-id="e97c0-770">Excel\\Kyselylomake\\Kysymys\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="e97c0-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span></span>          | <span data-ttu-id="e97c0-771">**\@.PrimaryQuestion**</span><span class="sxs-lookup"><span data-stu-id="e97c0-771">**\@.PrimaryQuestion**</span></span> |
    | <span data-ttu-id="e97c0-772">Excel\\Kyselylomake\\Kysymys\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="e97c0-772">Excel\\Questionnaire\\Question\\SequenceNumber</span></span>           | <span data-ttu-id="e97c0-773">**\@.SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="e97c0-773">**\@.SequenceNumber**</span></span> |
    | <span data-ttu-id="e97c0-774">Excel\\Kyselylomake\\Kysymys\\Teksti</span><span class="sxs-lookup"><span data-stu-id="e97c0-774">Excel\\Questionnaire\\Question\\Text</span></span>                     | <span data-ttu-id="e97c0-775">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="e97c0-775">**\@.Text**</span></span> |
    | <span data-ttu-id="e97c0-776">Excel\\Kyselylomake\\Kysymys\\Vastaus</span><span class="sxs-lookup"><span data-stu-id="e97c0-776">Excel\\Questionnaire\\Question\\Answer</span></span>                   | <span data-ttu-id="e97c0-777">**\@.Answer**</span><span class="sxs-lookup"><span data-stu-id="e97c0-777">**\@.Answer**</span></span> |
    | <span data-ttu-id="e97c0-778">Excel\\Kyselylomake\\Kysymys\\Vastaus\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="e97c0-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>    | <span data-ttu-id="e97c0-779">**\@.CorrectAnswer**, where **\@** is **model.Questionnaire.Answer**</span><span class="sxs-lookup"><span data-stu-id="e97c0-779">**\@.CorrectAnswer**, where **\@** is **model.Questionnaire.Answer**</span></span> |
    | <span data-ttu-id="e97c0-780">Excel\\Kyselylomake\\Kysymys\\Vastaus\\Pisteet</span><span class="sxs-lookup"><span data-stu-id="e97c0-780">Excel\\Questionnaire\\Question\\Answer\\Points</span></span>           | <span data-ttu-id="e97c0-781">**\@.Points**</span><span class="sxs-lookup"><span data-stu-id="e97c0-781">**\@.Points**</span></span> |
    | <span data-ttu-id="e97c0-782">Excel\\Kyselylomake\\Kysymys\\Vastaus\\Teksti</span><span class="sxs-lookup"><span data-stu-id="e97c0-782">Excel\\Questionnaire\\Question\\Answer\\Text</span></span>             | <span data-ttu-id="e97c0-783">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="e97c0-783">**\@.Text**</span></span> |

9. <span data-ttu-id="e97c0-784">Kun olet valmis, valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-784">When you've finished, select **Save**.</span></span>

<span data-ttu-id="e97c0-785">Seuraavassa kuvassa näkyy **muodon suunnittelu** -sivulla määritetyn tietojen sidonnan lopullinen tila.</span><span class="sxs-lookup"><span data-stu-id="e97c0-785">The following illustration shows the final state of the configured data bindings on the **Format designer** page.</span></span>

![Konfiguroitu tietojen sidonnan ER-toiminnon suunnittelussa](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> <span data-ttu-id="e97c0-787">Koko kokoelma määritettyjä tietolähteitä ja sidoksia edustaa määritetyssä muodossa olevaa muotomäärityskomponenttia.</span><span class="sxs-lookup"><span data-stu-id="e97c0-787">The whole collection of specified data sources and bindings represents a format mapping component of the configured format.</span></span> <span data-ttu-id="e97c0-788">Tätä muotomääritystä kutsutaan, kun raportin luonnin konfiguroitu muoto suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="e97c0-788">This format mapping is called when you run the configured format for report generation.</span></span>

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a><span data-ttu-id="e97c0-789">Suunnitellun muodon suorittaminen ER-muodosta</span><span class="sxs-lookup"><span data-stu-id="e97c0-789">Run a designed format from ER</span></span>

<span data-ttu-id="e97c0-790">Voit nyt suorittaa suunnitellun muodon testausta varten **kokoonpanot**-sivulta.</span><span class="sxs-lookup"><span data-stu-id="e97c0-790">You can now run a designed format for testing purposes from the **Configurations** page.</span></span>

1. <span data-ttu-id="e97c0-791">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-791">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e97c0-792">Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta, laajenna **Kysymyslomakemalli** ja valitse sitten **Kysymyslomakeraportti**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-792">On the **Configuration** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="e97c0-793">Valitse muotoiluversion **suunnitteluohjelma**, jonka tila on **luonnos**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-793">Select **Designer** for the format version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="e97c0-794">Vallitse **Muodon suunnittelu** -sivulla **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-794">On the **Format designer** page, select **Run**.</span></span>
5. <span data-ttu-id="e97c0-795">Määritä **ER-parametrit**-valintaikkunan **sisällytettävät rekisterit** -pikavälilehdessä suodatusvaihtoehto niin, että vain **SBCCrsExam**-kysely on mukana.</span><span class="sxs-lookup"><span data-stu-id="e97c0-795">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
6. <span data-ttu-id="e97c0-796">Vahvista suodatusvaihtoehto valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-796">Select **OK** to confirm the filtering option.</span></span>
7. <span data-ttu-id="e97c0-797">Suorita raportti valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-797">Select **OK** to run the report.</span></span>
8. <span data-ttu-id="e97c0-798">Tarkista aikaansaatu raportti.</span><span class="sxs-lookup"><span data-stu-id="e97c0-798">Review the generated report.</span></span>

<span data-ttu-id="e97c0-799">[Oletusarvon](electronic-reporting-destinations.md#default-behavior) mukaan luotu raportti toimitetaan Excel-tiedostona, jonka voit ladata.</span><span class="sxs-lookup"><span data-stu-id="e97c0-799">By [default](electronic-reporting-destinations.md#default-behavior), a generated report is delivered as an Excel file that you can download.</span></span> <span data-ttu-id="e97c0-800">Seuraavissa kuvissa näkyy kaksi sivua luotua raporttia Excel-muodossa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-800">The following illustrations show two pages of the generated report in Excel format.</span></span>

![Esimerkki luodusta raportista Excel-muodossa, sivu 1](./media/er-quick-start1-report1a.png)

![Esimerkki luodusta raportista Excel-muodossa, sivu 2](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a><span data-ttu-id="e97c0-803">Suunnitellun muodon säätäminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-803">Tune a designed format</span></span>

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a><span data-ttu-id="e97c0-804">Tiedostomuodon muokkaaminen luodun tiedoston nimen muuttamista varten</span><span class="sxs-lookup"><span data-stu-id="e97c0-804">Modify a format to change the name of a generated document</span></span>

<span data-ttu-id="e97c0-805">Oletusarvon mukaan luotu tiedosto nimetään nykyisen käyttäjän aliaksen avulla.</span><span class="sxs-lookup"><span data-stu-id="e97c0-805">By default, a generated document is named by using the alias of the current user.</span></span> <span data-ttu-id="e97c0-806">Muokkaamalla muotoa voit muuttaa tätä toimintoa siten, että luotu tiedosto nimetään mukautetun logiikan mukaan.</span><span class="sxs-lookup"><span data-stu-id="e97c0-806">By modifying the format, you can change this behavior so that a generated document is named based on your custom logic.</span></span> <span data-ttu-id="e97c0-807">Esimerkiksi luodun tiedoston nimi voi perustua nykyiseen istunnon päivämäärään ja kellonaikaan sekä raportin otsikkoon.</span><span class="sxs-lookup"><span data-stu-id="e97c0-807">For example, the name of a generated document can be based on the current session date and time, and on the report's title.</span></span>

1. <span data-ttu-id="e97c0-808">Valitse **Muodon suunnittelu** -sivulla **Raportti**-juurinimike.</span><span class="sxs-lookup"><span data-stu-id="e97c0-808">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="e97c0-809">Valitse **yhdistämismääritys**-välilehdestä **Muokkaa tiedostonimeä**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-809">On the **Mapping** tab, select **Edit file name**.</span></span>
3. <span data-ttu-id="e97c0-810">Kirjoita **kaava**-kenttään **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-810">In the **Formula** field, enter **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span></span>
4. <span data-ttu-id="e97c0-811">Valitse **Tallenna** ja sulje kaavaeditori.</span><span class="sxs-lookup"><span data-stu-id="e97c0-811">Select **Save**, and close the formula editor.</span></span>
5. <span data-ttu-id="e97c0-812">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-812">Select **Save**.</span></span>

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a><span data-ttu-id="e97c0-813">Muodon muokkaaminen muuttamalla kysymysten järjestystä</span><span class="sxs-lookup"><span data-stu-id="e97c0-813">Modify a format to change the order of questions</span></span>

<span data-ttu-id="e97c0-814">Kysymyksiä ei ole tilattu oikein luotavalla raportilla.</span><span class="sxs-lookup"><span data-stu-id="e97c0-814">The questions aren't correctly ordered in a generated report.</span></span> <span data-ttu-id="e97c0-815">Voit muuttaa järjestystä muokkaamalla muotoa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-815">You can change the order by modifying the format.</span></span>

1. <span data-ttu-id="e97c0-816">Valitse **Muodon suunnittelu** -sivulla **Raportti**-juurinimike.</span><span class="sxs-lookup"><span data-stu-id="e97c0-816">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="e97c0-817">Laajenna **Määritys**-välilehden muotopuussa **Raportti\\kyselylomake\\kysymys**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-817">On the **Mapping** tab, in the format tree, expand **Report\\Questionnaire\\Question**.</span></span>

    ![Aluetyypin kysymysmuotoelementti ER-operaation suunnittelijassa](./media/er-quick-start1-bindings3.png)

3. <span data-ttu-id="e97c0-819">Valitse **Yhdistämismääritys**-välilehdestä **model.Questionnaire**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-819">On the **Mapping** tab, select **model.Questionnaire**.</span></span>
4. <span data-ttu-id="e97c0-820">Valitse **Lisää** \> **Funktiot\\laskettu kenttä** ja kirjoita sitten **nimi**-kenttään **OrderedQuestions**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-820">Select **Add** \> **Functions\\Calculated field**, and then, in the **Name** field, enter **OrderedQuestions**.</span></span>
5. <span data-ttu-id="e97c0-821">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-821">Select **Edit formula**.</span></span>
6. <span data-ttu-id="e97c0-822">Kirjoita kaavaeditorin **kaava**-kenttään **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** voidaksesi tilata nykyisen kyselylomakkeen kysymysluettelon järjestysnumeron mukaan.</span><span class="sxs-lookup"><span data-stu-id="e97c0-822">In the formula editor, in the **Formula** field, enter **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** to order the list of questions of the current questionnaire by the sequence order number.</span></span>
7. <span data-ttu-id="e97c0-823">Valitse **Tallenna** ja sulje kaavaeditori.</span><span class="sxs-lookup"><span data-stu-id="e97c0-823">Select **Save**, and close the formula editor.</span></span>
8. <span data-ttu-id="e97c0-824">Viimeistele uuden lasketun kentän syöttö valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-824">Select **OK** to complete the entry of a new calculated field.</span></span>
9. <span data-ttu-id="e97c0-825">Valitse **Yhdistämismääritys**-välilehdestä **model.Questionnaire.OrderedQuestions**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-825">On the **Mapping** tab, select **model.Questionnaire.OrderedQuestions**.</span></span>
10. <span data-ttu-id="e97c0-826">Valitse muotopuussa **Excel\\Kysymyslomake\\Kysymys**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-826">In the format tree, select **Excel\\Questionnaire\\Question**.</span></span>
11. <span data-ttu-id="e97c0-827">Valitse **sido** ja vahvista sitten, että käytössä oleva **model.Questionnaire.Questions**-polku korvataan uudella **model.Questionnaire.OrderedQuestions**-polulla kaikissa sisäkkäisten elementtien sidonnoissa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-827">Select **Bind**, and then confirm that the current **model.Questionnaire.Questions** path is replaced by the new **model.Questionnaire.OrderedQuestions** path in all bindings of nested elements.</span></span>
12. <span data-ttu-id="e97c0-828">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-828">Select **Save**.</span></span>

![Kysymysmuotoelementin sitominen määritettyyn OrderedQuestions-tietolähteeseen ER-toiminnon suunnittelussa](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a><span data-ttu-id="e97c0-830">Muokatun muodon suorittaminen ER-muodosta</span><span class="sxs-lookup"><span data-stu-id="e97c0-830">Run a modified format from ER</span></span>

<span data-ttu-id="e97c0-831">Voit nyt suorittaa muokatun muodon testaustarkoituksessa ER-kehyksestä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-831">You can now run a modified format for testing purposes from the ER framework.</span></span>

1. <span data-ttu-id="e97c0-832">Vallitse **Muodon suunnittelu** -sivulla **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-832">On the **Format designer** page, select **Run**.</span></span>
2. <span data-ttu-id="e97c0-833">Määritä **ER-parametrit**-valintaikkunan **sisällytettävät rekisterit** -pikavälilehdessä suodatusvaihtoehto niin, että vain **SBCCrsExam**-kysely on mukana.</span><span class="sxs-lookup"><span data-stu-id="e97c0-833">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
3. <span data-ttu-id="e97c0-834">Vahvista suodatusvaihtoehto valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-834">Select **OK** to confirm the filtering option.</span></span>
4. <span data-ttu-id="e97c0-835">Suorita raportti valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-835">Select **OK** to run the report.</span></span>
5. <span data-ttu-id="e97c0-836">Tarkista aikaansaatu raportti.</span><span class="sxs-lookup"><span data-stu-id="e97c0-836">Review the generated report.</span></span>

<span data-ttu-id="e97c0-837">Seuraavassa kuvassa näkyy Excel-muodossa luotu raportti, jossa kysymykset on järjestetty oikein.</span><span class="sxs-lookup"><span data-stu-id="e97c0-837">The following illustration shows a generated report in Excel format where the questions are correctly ordered.</span></span>

![Luotu raportti Excel-muodossa, jossa on oikein tilatut kysymykset](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a><span data-ttu-id="e97c0-839">Suunnittele muoto loppuun</span><span class="sxs-lookup"><span data-stu-id="e97c0-839">Complete the format design</span></span>

1. <span data-ttu-id="e97c0-840">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-840">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e97c0-841">Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta, laajenna **Kysymyslomakemalli** ja valitse sitten **Kysymyslomakeraportti**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-841">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="e97c0-842">Valitse **Versiot**-pikavälilehdessä konfiguraatioversio, jonka tila on **Luonnos**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-842">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="e97c0-843">Valitse **Muutoksen tila** \> **Viimeistele**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-843">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="e97c0-844">Tämän konfiguraation version 1.1 tila muutetaan **luonnoksesta** **valmiiksi**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-844">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="e97c0-845">Versiota 1.1 ei voi enää muuttaa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-845">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="e97c0-846">Tämä versio sisältää määritetyn muodon, ja sitä voidaan käyttää mukautetun raportin tulostamiseen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-846">This version contains the configured format and can be used to print your custom report.</span></span> <span data-ttu-id="e97c0-847">Tämän konfiguraation versio 1.2 luodaan, ja sen tila on **luonnos**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-847">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="e97c0-848">Voit muokata tätä versiota, jos haluat muuttaa **kyselylomake**-raporttisi muotoa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-848">You can edit this version to adjust the format of your **Questionnaire** report.</span></span>

![Konfiguraatiosivun muokattavan ER-konfiguraation versiot](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> <span data-ttu-id="e97c0-850">Konfiguroitu muoto on **kyselylomake**-raportin rakenne, eikä se sisällä mitään suhteita rahoitukseen määritettyihin esineisiin.</span><span class="sxs-lookup"><span data-stu-id="e97c0-850">The configured format is your design of the **Questionnaire** report and contains no relations to the Finance-specific artefacts.</span></span>

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a><span data-ttu-id="e97c0-851">Sovelluksen artefaktien laatiminen suunniteltua raporttia varten</span><span class="sxs-lookup"><span data-stu-id="e97c0-851">Develop application artefacts to call the designed report</span></span>

<span data-ttu-id="e97c0-852">Järjestelmänvalvojan roolin käyttäjänä sinun on kehitettävä uusi logiikka niin, että konfiguroitu ER-muoto voidaan kutsua sovelluksen käyttöliittymästä (UI) mukautetun raportin luomista varten.</span><span class="sxs-lookup"><span data-stu-id="e97c0-852">As a user in the System Administrator role, you must develop new logic so that the configured ER format can be called from the application user interface (UI) to generate your custom report.</span></span> <span data-ttu-id="e97c0-853">Tällä hetkellä ER ei tarjoa mitään ominaisuuksia tämäntyyppisen logiikan määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-853">Currently, ER doesn't offer any capability for configuring this type of logic.</span></span> <span data-ttu-id="e97c0-854">Siksi tarvitaan joitakin teknisiä töitä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-854">Therefore, some engineering work is required.</span></span> 

<span data-ttu-id="e97c0-855">Uuden logiikan luontia varten käyttöön on otettava jatkuvaa koontia tukeva topologia.</span><span class="sxs-lookup"><span data-stu-id="e97c0-855">To develop the new logic, you must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="e97c0-856">Lisätietoja on kohdassa [Jatkuvaa koonnin ja testauksen automaatiota tukevien topologioiden käyttöönotto](../perf-test/continuous-build-test-automation.md).</span><span class="sxs-lookup"><span data-stu-id="e97c0-856">For more information, see [Deploy topologies that support continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span> <span data-ttu-id="e97c0-857">Tarvitset myös tämän topologian kehitysympäristön käyttöoikeuden.</span><span class="sxs-lookup"><span data-stu-id="e97c0-857">You must also have access to the development environment for this topology.</span></span> <span data-ttu-id="e97c0-858">Lisätietoja saatavilla olevista ER-ohjelmointirajapinnoista on kohdassa [ER-kehys-API](er-apis-app73.md).</span><span class="sxs-lookup"><span data-stu-id="e97c0-858">For more information about the available ER API, see [ER framework API](er-apis-app73.md).</span></span>

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a><span data-ttu-id="e97c0-859">Lähdekoodin muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-859">Modify source code</span></span>

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a><span data-ttu-id="e97c0-860">Tietosopimusluokan lisääminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-860">Add a data contract class</span></span>

<span data-ttu-id="e97c0-861">Lisää uusi **QuestionnairesErReportContract**-luokka Microsoft Visual Studio -projektiin ja kirjoita koodi, joka määrittää konfiguroitavan ER-muodon suorittamiseen käytettävän tietosopimuksen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-861">Add the new **QuestionnairesErReportContract** class to your Microsoft Visual Studio project, and write code that specifies the data contract that should be used to run the configured ER format.</span></span>

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a><span data-ttu-id="e97c0-862">UI Builder -luokan lisääminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-862">Add a UI builder class</span></span>

<span data-ttu-id="e97c0-863">Lisää uusi **QuestionnairesErReportUIBuilder**-luokka Visual Studio -projektiisi ja kirjoita koodi, kun haluat luoda suorituksenaikaisen valintaikkunan, jota käytetään suoritettavan ER-muodon määritystunnuksen hakemiseen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-863">Add the new **QuestionnairesErReportUIBuilder** class to your Visual Studio project, and write code to generate a runtime dialog box that will be used to look up the format mapping ID of the ER format that must be run.</span></span> <span data-ttu-id="e97c0-864">Annettu koodi hakee vain ER-muotoja, jotka sisältävät **[kyselylomakkeen](#DataModeName)** **tietomalliin** viittaavan tietolähteen **[juuri](#RootDefinitionName)**-määritystä käyttäen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-864">The provided code looks up only ER formats that contain a data source of the **Data model** type that refers to the **[Questionnaires](#DataModeName)** data model by using the **[Root](#RootDefinitionName)** definition.</span></span>

> [!NOTE]
> <span data-ttu-id="e97c0-865">Vaihtoehtoisesti voit suodattaa ER-integrointipisteiden avulla ER-muotoja.</span><span class="sxs-lookup"><span data-stu-id="e97c0-865">Alternatively, you can use ER integration points to filter ER formats.</span></span> <span data-ttu-id="e97c0-866">Lisätietoja on kohdassa [API, joka näyttää muodon yhdistämishaun](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span><span class="sxs-lookup"><span data-stu-id="e97c0-866">For more information, see [API to show a format mapping lookup](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span></span>

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a><span data-ttu-id="e97c0-867">Tietopalveluluokan lisääminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-867">Add a data provider class</span></span>

<span data-ttu-id="e97c0-868">Lisää uusi **QuestionnairesErReportDP**-luokka Microsoft Visual Studio -projektiin ja kirjoita koodi, joka näyttää konfiguroitavan ER-muodon suorittamiseen käytettävän tietopalvelun.</span><span class="sxs-lookup"><span data-stu-id="e97c0-868">Add the new **QuestionnairesErReportDP** class to your Visual Studio project, and write code that introduces the data provider that should used to run the configured ER format.</span></span> <span data-ttu-id="e97c0-869">Annettu koodi sisältää vain tämän tietopalvelun tietosopimuksen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-869">The provided code includes only the data contract for this data provider.</span></span>

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a><span data-ttu-id="e97c0-870">Käyttöliittymätekstitiedoston lisääminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-870">Add a labels file</span></span>

<span data-ttu-id="e97c0-871">Lisää uusi **QuestionnairesErReportLabels\_en-US** -tarratiedosto Visual Studio -projektiisi ja määritä seuraavat uusien käyttöliittymäresurssien otsikot:</span><span class="sxs-lookup"><span data-stu-id="e97c0-871">Add the new **QuestionnairesErReportLabels\_en-US** labels file to your Visual Studio project, and specify the following labels for new UI resources:</span></span>

- <span data-ttu-id="e97c0-872">Uuden valikkovaihtoehdon **\@QuestionnairesReport**-otsikko, joka sisältää seuraavan tekstin Yhdysvalloissa (en-US): **kyselylomakeraportti (palvelun tarjoaa ER)**</span><span class="sxs-lookup"><span data-stu-id="e97c0-872">The **\@QuestionnairesReport** label for a new menu item that contains the following text in US English (en-US): **Questionnaires report (powered by ER)**</span></span>
- <span data-ttu-id="e97c0-873">**\@QuestionnairesReportBatchJobDescription**-etiketti, jos valittu ER-muoto ajoitetaan suoritettavaksi erätyönä</span><span class="sxs-lookup"><span data-stu-id="e97c0-873">The **\@QuestionnairesReportBatchJobDescription** label for a batch job title if a selected ER format is scheduled for execution as a batch job</span></span>

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a><span data-ttu-id="e97c0-874">Raporttipalveluluokan lisääminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-874">Add a report service class</span></span>

<span data-ttu-id="e97c0-875">Lisää uusi **QuestionnairesErReportService**-luokka Visual Studio -projektiisi ja kirjoita koodi, joka kutsuu ER-muotoa, määrittää sen muodon yhdistämistunnuksen avulla ja antaa parametriksi tietosopimuksen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-875">Add the new **QuestionnairesErReportService** class to your Visual Studio project, and write code that calls an ER format, identifies it by a format mapping ID, and provides a data contract as a parameter.</span></span>

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

<span data-ttu-id="e97c0-876">Jos sinun on käytettävä sovellustietoja suorittavaa ER-muotoa, sinun on konfiguroitava **tietomalli**-tyypin tietolähdemuodon yhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="e97c0-876">When you must use an ER format that runs application data, you must configure a data source of the **Data model** type in the format mapping.</span></span> <span data-ttu-id="e97c0-877">Tämä tietolähde viittaa tiettyyn tietyn tietomallin osaan käyttämällä yksittäistä päämääritystä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-877">This data source refers to a specific part of the specified data model by using a single root definition.</span></span> <span data-ttu-id="e97c0-878">Kun ER-muoto suoritetaan, se kutsuu tätä tietolähdettä käyttämään sopivaa ER-mallimääritystä, joka on määritetty tietylle mallille ja päämääritykselle.</span><span class="sxs-lookup"><span data-stu-id="e97c0-878">When the ER format is run, it calls this data source to access the appropriate ER model mapping that is configured for a given model and root definition.</span></span>

<span data-ttu-id="e97c0-879">Kaikki tiedot, jotka voit valmistella lähdekoodissa ja tallentaa osana tietosopimusta, voidaan siirtää käytössä olevaan ER-muotoon käyttämällä tämän tyyppisiä ER-mallimäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-879">All the information that you might prepare in the source code and store as part of the data contract can be passed to the running ER format by using an ER model mapping of this type.</span></span> <span data-ttu-id="e97c0-880">ER-mallin yhdistämismäärityksessä on määritettävä **objekti**-tyypin tietolähde, joka viittaa **[QuestionnairesErReportContract](#DataContractClass)**-luokkaan.</span><span class="sxs-lookup"><span data-stu-id="e97c0-880">In the ER model mapping, you must configure a data source of the **Object** type that refers to the **[QuestionnairesErReportContract](#DataContractClass)** class.</span></span> <span data-ttu-id="e97c0-881">Voit määrittää mallimäärityksen määrittämällä tietolähteen, joka kutsuu tätä mallimääritystä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-881">To identify a model mapping, you must specify a data source that calls this model mapping.</span></span> <span data-ttu-id="e97c0-882">Tässä koodissa on **ERModelDataSourceName**-vakion määrittämä tietolähde, jolla on **[malli](#ModelDSName)**-arvo.</span><span class="sxs-lookup"><span data-stu-id="e97c0-882">In the provided code, this data source specified by the **ERModelDataSourceName** constant that has the **[model](#ModelDSName)** value.</span></span> <span data-ttu-id="e97c0-883">Määritä tietolähteen nimi, kun haluat määrittää, mitä tietolähdettä käytetään, kun tietojen sopimus paljastetaan mallimäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-883">To identify which data source is used to expose the data contract in the model mapping, you must specify a data source name.</span></span> <span data-ttu-id="e97c0-884">Tässä koodissa on **ParametersDataSourceName**-vakion määrittämä nimi, jolla on <a name="DataContractDSName"></a>**RunTimeParameters**-arvo.</span><span class="sxs-lookup"><span data-stu-id="e97c0-884">In the provided code, this name is specified by the **ParametersDataSourceName** constant that has <a name="DataContractDSName"></a>**RunTimeParameters** value.</span></span>

> [!NOTE]
> <span data-ttu-id="e97c0-885">Uudessa ympäristössä ER-metatiedot on ehkä päivitettävä, jotta tämäntyyppinen luokka on käytettävissä ER-mallin yhdistämismäärityksen suunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-885">In a new environment, you might have to refresh the ER metadata so that this type of class is available in the ER model mapping designer.</span></span> <span data-ttu-id="e97c0-886">Lisätietoja on kohdassa [Sähköisen raportoinnin (ER) kehyksen määrittäminen](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="e97c0-886">For more information, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span></span>

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a><span data-ttu-id="e97c0-887">Raportin ohjainluokan lisääminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-887">Add a report controller class</span></span>

<span data-ttu-id="e97c0-888">Lisää uusi **QuestionnairesErReportController**-luokka Visual Studio -projektiisi ja kirjoita koodi, joka suorittaa ER-muodon joko synkronisessa tilassa tai eräajona, kuten haluat, valintaikkunassa, joka perustuu annetun **QuestionnairesErReportUIBuilder**-luokan logiikkaan.</span><span class="sxs-lookup"><span data-stu-id="e97c0-888">Add the new **QuestionnairesErReportController** class to your Visual Studio project, and write code that runs an ER format in either synchronous mode or batch mode, as you prefer, in the dialog box that is built based on the logic of the provided **QuestionnairesErReportUIBuilder** class.</span></span>

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a><span data-ttu-id="e97c0-889">Valikkovaihtoehdon lisääminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-889">Add a menu item</span></span>

<span data-ttu-id="e97c0-890">Lisää uusi **QuestionnairesErRepor**-valikkovaihtoehto Visual Studio -projektiisi.</span><span class="sxs-lookup"><span data-stu-id="e97c0-890">Add the new **QuestionnairesErReport** menu item to your Visual Studio project.</span></span> <span data-ttu-id="e97c0-891">Tämä valikkoaihe viittaa **Objekti**-ominaisuuden **QuestionnairesErReportController**-luokkaan, ja sen avulla määritetään käyttäjän oikeudet valita ja suorittaa ER-muoto.</span><span class="sxs-lookup"><span data-stu-id="e97c0-891">In the **Object** property, this menu item refers to the **QuestionnairesErReportController** class, and it's used to specify a user permission to select and run an ER format.</span></span> <span data-ttu-id="e97c0-892">**Otsikko**-ominaisuudessa tämä valikkoaihe viittaa aiemmin luomaasi **\@QuestionnairesReport**-tarraan, joten oikea teksti esitetään sovelluksen käyttöliittymässä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-892">In the **Label** property, this menu item refers to the **\@QuestionnairesReport** label that you created earlier, so that correct text is presented in the application UI.</span></span>

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a><span data-ttu-id="e97c0-893">Valikkovaihtoehdon lisääminen valikkoon</span><span class="sxs-lookup"><span data-stu-id="e97c0-893">Add a menu item to a menu</span></span>

<span data-ttu-id="e97c0-894">Lisää nykyinen **KM**-valikko Visual Studio -projektiisi.</span><span class="sxs-lookup"><span data-stu-id="e97c0-894">Add the existing **KM** menu to your Visual Studio project.</span></span> <span data-ttu-id="e97c0-895">Tähän valikkoon on lisättävä uusi **QuestionnairesErReport**-nimikkeen **Tuloste**-tyyppi.</span><span class="sxs-lookup"><span data-stu-id="e97c0-895">You must add a new **QuestionnairesErReport** item of the **Output** type to this menu.</span></span> <span data-ttu-id="e97c0-896">Tämän kohteen täytyy viitata edellisessä osassa kuvattuun **QuestionnairesErReport**-valikkokohteeseen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-896">This item must refer to the **QuestionnairesErReport** menu item that is described in the previous section.</span></span>

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a> <span data-ttu-id="e97c0-897">Visual Studio -projektin luominen</span><span class="sxs-lookup"><span data-stu-id="e97c0-897">Build a Visual Studio project</span></span>

<span data-ttu-id="e97c0-898">Luo projekti, jotta uusi valikkovaihtoehto on käyttäjien käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-898">Build your project to make a new menu item available to users.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a><span data-ttu-id="e97c0-899">Muodon suorittaminen sovelluksesta</span><span class="sxs-lookup"><span data-stu-id="e97c0-899">Run a format from the application</span></span>

1. <span data-ttu-id="e97c0-900">Siirry kohtaan **kyselylomake** \> **Suunnittelu** \> **Kyselylomakeraportti (palvelun tarjoaa ER)**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-900">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>

    ![Valitaan Kyselylomakeraportti (palvelun tarjoaa ER) -valikkokohta Kysely-moduulista määritetyn ER-muodon suorittamiseksi](./media/er-quick-start1-application-menu-modified.png)

2. <span data-ttu-id="e97c0-902">Valitse valintaikkunan **muodon määritys** -kentästä **kyselylomakkeiden raportti**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-902">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="e97c0-903">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-903">Select **OK**.</span></span>
4. <span data-ttu-id="e97c0-904">Määritä **Sähköisen raportoinnin parametrit**-valintaikkunan **sisällytettävät rekisterit** -pikavälilehdessä suodatusvaihtoehto niin, että vain **SBCCrsExam**-kysely on mukana.</span><span class="sxs-lookup"><span data-stu-id="e97c0-904">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="e97c0-905">Vahvista suodatusvaihtoehto valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-905">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="e97c0-906">Suorita raportti valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-906">Select **OK** to run the report.</span></span>

    ![Sähköinen raportti -dialogi-ikkunan valintaehtojen määrittäminen](./media/er-quick-start1-report-run-dialog-page.png)

7. <span data-ttu-id="e97c0-908">Tarkista aikaansaatu raportti.</span><span class="sxs-lookup"><span data-stu-id="e97c0-908">Review the generated report.</span></span>

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a><span data-ttu-id="e97c0-909">Suunnitellun ER-ratkaisun säätäminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-909">Tune a designed ER solution</span></span>

<span data-ttu-id="e97c0-910">Voit muokata konfiguroitavaa ER-ratkaisua siten, että se käyttää kehittämääsi tietopalveluluokkaa, jonka avulla voit käyttää käytössä olevan ER-muodon tietoja, ja siten, että se syöttää tämän ER-muodon nimen luotuun raporttiin.</span><span class="sxs-lookup"><span data-stu-id="e97c0-910">You can modify the configured ER solution so that it uses the data provider class that you developed to access details of the running ER format, and so that it enters the name of this ER format in a generated report.</span></span>

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a><span data-ttu-id="e97c0-911">Mallin yhdistämismäärityksen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-911">Modify a model mapping</span></span>

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a><span data-ttu-id="e97c0-912">Tietolähteiden lisääminen tietosopimusobjektien käyttämiseen</span><span class="sxs-lookup"><span data-stu-id="e97c0-912">Add data sources to access a data contract object</span></span>

1. <span data-ttu-id="e97c0-913">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-913">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e97c0-914">Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta, laajenna **Kysymyslomakemalli** ja valitse sitten **Kysymyslomakkeen määritys**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-914">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="e97c0-915">Valitse **Suunnittelija**, jos haluat avata **Malli tietolähteen määritys** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="e97c0-915">Select **Designer** to open the **Model to datasource mapping** page.</span></span>
4. <span data-ttu-id="e97c0-916">Valitse **Suunnittelija**, jos haluat avata valitun yhdistämismäärityksen mallikartoituksen suunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-916">Select **Designer** to open the selected mapping in the model mapping designer.</span></span>
5. <span data-ttu-id="e97c0-917">Valitse **Mallin määrityksen suunnittelu** -sivun **Tietolähdetyypit**-ruudusta **Dynamics 365 for Operations\\Objekti**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-917">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Object**.</span></span>
6. <span data-ttu-id="e97c0-918">Valitse **Tietolähteet**-ruudussa **Lisää juuri**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-918">In the **Data sources** pane, select **Add root**.</span></span>
7. <span data-ttu-id="e97c0-919">Kirjoita valintaikkunan **Nimi**-kenttään **[RunTimeParameters](#DataContractDSName)**, joka on määritetty **QuestionnairesErReportService**-luokan lähdekoodissa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-919">In the dialog box, in the **Name** field, enter **[RunTimeParameters](#DataContractDSName)**, as defined in the source code of the **QuestionnairesErReportService** class.</span></span>
8. <span data-ttu-id="e97c0-920">Kirjoita **luokka**-kenttään **[QuestionnairesErReportContract](#DataContractClass)**, joka on koodattu aiemmin.</span><span class="sxs-lookup"><span data-stu-id="e97c0-920">In the **Class** field, enter **[QuestionnairesErReportContract](#DataContractClass)**, which was coded earlier.</span></span>
9. <span data-ttu-id="e97c0-921">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-921">Select **OK**.</span></span>
10. <span data-ttu-id="e97c0-922">Laajenna **RunTimeParameters**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-922">Expand **RunTimeParameters**.</span></span>

<span data-ttu-id="e97c0-923">Lisätty tietolähde antaa tietoja suoritettavan ER-muodon yhdistämismäärityksen tietuetunnuksesta.</span><span class="sxs-lookup"><span data-stu-id="e97c0-923">The added data source provides information about the record ID of the running ER format mapping.</span></span>

![Lisätty tietolähde ER-mallin määrityssuunnittelijaan](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a><span data-ttu-id="e97c0-925">Tietolähteen lisääminen ER-muotomääritystietueen käyttämiseen</span><span class="sxs-lookup"><span data-stu-id="e97c0-925">Add a data source to access ER format mapping records</span></span>

<span data-ttu-id="e97c0-926">Jatka valitun mallimäärityksen muokkaamista lisäämällä tietolähde, joka käyttää ER-muotomääritystietueita.</span><span class="sxs-lookup"><span data-stu-id="e97c0-926">Continue to edit the selected model mapping by adding a data source to access ER format mapping records.</span></span>

1. <span data-ttu-id="e97c0-927">Valitse **Mallin määrityksen suunnittelu** -sivun **Tietolähdetyypit**-ruudusta **Dynamics 365 for Operations\\Taulukkotiedot**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-927">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="e97c0-928">Valitse **Tietolähteet**-ruudussa **Lisää juuri**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-928">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="e97c0-929">Kirjoita valintaikkunan **Nimi**-kentässä **ER1**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-929">In the dialog box, in the **Name** field, enter **ER1**.</span></span>
4. <span data-ttu-id="e97c0-930">Kirjoita **Taulu**-kenttään **ERFormatMappingTable**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-930">In the **Table** field, enter **ERFormatMappingTable**.</span></span>
5. <span data-ttu-id="e97c0-931">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-931">Select **OK**.</span></span>

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a><span data-ttu-id="e97c0-932">Tietolähteen lisääminen käynnissä olevan ER-muodon muotomääritystietueen käyttämiseen</span><span class="sxs-lookup"><span data-stu-id="e97c0-932">Add a data source to access a format mapping record of a running ER format</span></span>

<span data-ttu-id="e97c0-933">Jatka valitun mallimäärityksen muokkaamista lisäämällä tietolähde, joka käyttää käynnissä olevan ER-muodon muotomääritystietueita.</span><span class="sxs-lookup"><span data-stu-id="e97c0-933">Continue to edit the selected model mapping by adding a data source to access the format mapping record of the running ER format.</span></span>

1. <span data-ttu-id="e97c0-934">Valitse **Mallin määrityksen suunnittelu** -sivun **Tietolähdetyypit**-ruudusta **Toiminnot\\Laskettu kenttä**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-934">On the **Model mapping designer** page, in the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
2. <span data-ttu-id="e97c0-935">Valitse **Tietolähteet**-ruudussa **Lisää juuri**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-935">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="e97c0-936">Kirjoita valintaikkunan **Nimi**-kentässä **ER2**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-936">In the dialog box, in the **Name** field, enter **ER2**.</span></span>
4. <span data-ttu-id="e97c0-937">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-937">Select **Edit formula**.</span></span>
5. <span data-ttu-id="e97c0-938">Kirjoita kaavaeditorin **kaava**-kenttään **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-938">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span></span>
6. <span data-ttu-id="e97c0-939">Valitse **Tallenna** ja sulje kaavaeditori.</span><span class="sxs-lookup"><span data-stu-id="e97c0-939">Select **Save**, and close the formula editor.</span></span>
7. <span data-ttu-id="e97c0-940">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-940">Select **OK**.</span></span>

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a><span data-ttu-id="e97c0-941">Kirjoita suoritettavan ER-muodon nimi tietomalliin</span><span class="sxs-lookup"><span data-stu-id="e97c0-941">Enter the name of the running ER format in the data model</span></span>

<span data-ttu-id="e97c0-942">Jatka valitun mallimäärityksen muokkaamista niin, että käytössä olevan ER-muodon nimi kirjoitetaan tietomalliin.</span><span class="sxs-lookup"><span data-stu-id="e97c0-942">Continue to edit the selected model mapping so that the name of the running ER format is entered in the data model.</span></span>

1. <span data-ttu-id="e97c0-943">Laajenna **Mallin määrityksen suunnittelu** -sivun **Tietomalli**-ruudusta **ExecutionContext** ja valitse sitten **ExecutionContext\\FormatName**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-943">On the **Model mapping designer** page, in the **Data model** pane, expand **ExecutionContext**, and then select **ExecutionContext\\FormatName**.</span></span>
2. <span data-ttu-id="e97c0-944">Määritä tietojen sidonta valitun tietomallin kenttää varten valitsemalla **Tietomalli**-ruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-944">In the **Data model** pane, select **Edit** to configure a data binding for the selected data model's field.</span></span>
3. <span data-ttu-id="e97c0-945">Kirjoita kaavaeditorin **Kaava**-kenttään **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-945">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span></span>
4. <span data-ttu-id="e97c0-946">Valitse **Tallenna** ja sulje kaavaeditori.</span><span class="sxs-lookup"><span data-stu-id="e97c0-946">Select **Save**, and close the formula editor.</span></span>

<span data-ttu-id="e97c0-947">Koska olet käyttänyt **FormatName**-kenttää, konfiguroitu mallikartoitus paljastaa nyt sellaisen ER-muodon nimen, joka kutsuu tätä mallimääritystä suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="e97c0-947">Because you used the **FormatName** field, the configured model mapping now exposes the name of an ER format that calls this model mapping during execution.</span></span>

![Tietomallikentän sitominen ER-mallikartoituksen suunnittelutoimintoon lisätyn tietolähteen tapaan](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a><span data-ttu-id="e97c0-949">Mallin määrityksen rakenteen täydentäminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-949">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="e97c0-950">Valitse **Mallimäärityssuunnittelu**-sivulla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-950">On the **Model mapping designer** page, select **Save**.</span></span>
2. <span data-ttu-id="e97c0-951">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e97c0-951">Close the page.</span></span>
3. <span data-ttu-id="e97c0-952">Sulje mallimääritykset-sivu.</span><span class="sxs-lookup"><span data-stu-id="e97c0-952">Close the model mappings page.</span></span>
4. <span data-ttu-id="e97c0-953">Varmista, että **kyselylomakkeen yhdistämis**-määritys on edelleen valittuna **konfiguraatiot**-sivun konfiguraatiopuussa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-953">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire mapping** configuration is still selected.</span></span> <span data-ttu-id="e97c0-954">Valitse sitten **Versiot**-pikavälilehdessä konfiguraatioversio, jonka tila on **Luonnos**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-954">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
5. <span data-ttu-id="e97c0-955">Valitse **Muutoksen tila** \> **Viimeistele**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-955">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="e97c0-956">Tämän konfiguraation version 1.2 tila muutetaan **luonnoksesta** **valmiiksi**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-956">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="e97c0-957">Versiota 1.2 ei voi enää muuttaa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-957">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="e97c0-958">Tämä versio sisältää konfiguroidun mallin määrityksen, ja sitä voidaan käyttää muiden ER-konfiguraatioiden pohjana.</span><span class="sxs-lookup"><span data-stu-id="e97c0-958">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="e97c0-959">Tämän konfiguraation versio 1.3 luodaan, ja sen tila on **luonnos**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-959">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="e97c0-960">Voit muokata tätä versiota, jos haluat muuttaa **kyselylomakkeen** mallimääritystä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-960">You can edit this version to adjust the **Questionnaire** model mapping.</span></span>

### <a name="modify-a-format"></a><a name="ModifyFormat"></a><span data-ttu-id="e97c0-961">Muodon muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-961">Modify a format</span></span>

<span data-ttu-id="e97c0-962">Voit muokata konfiguroitavan ER-muotoa niin, että sen nimi näkyy sen raportin alatunnisteessa, joka luodaan, kun ER-muoto suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="e97c0-962">You can modify the configured ER format so that its name is shown in the footer of a report that is generated when the ER format is run.</span></span>

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a><span data-ttu-id="e97c0-963">Lisää uusi muotoelementti</span><span class="sxs-lookup"><span data-stu-id="e97c0-963">Add a new format element</span></span>

1. <span data-ttu-id="e97c0-964">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-964">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e97c0-965">Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta, laajenna **Kysymyslomakemalli** ja valitse sitten **Kysymyslomakeraportti**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-965">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="e97c0-966">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-966">Select **Designer**.</span></span>
4. <span data-ttu-id="e97c0-967">Valitse **Muodon suunnittelu** -sivulla **Raportti**-juurinimike.</span><span class="sxs-lookup"><span data-stu-id="e97c0-967">On the **Format designer** page, select the **Report** root item.</span></span>
5. <span data-ttu-id="e97c0-968">Valitse **Lisää**, jos haluat lisätä uuden sisäkkäisen muodon elementin valitulle **raportin** juurikohteelle.</span><span class="sxs-lookup"><span data-stu-id="e97c0-968">Select **Add** to add a new nested format element for the selected **Report** root item.</span></span>
6. <span data-ttu-id="e97c0-969">Valitse **Excel\\alatunniste**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-969">Select **Excel\\Footer**.</span></span>
7. <span data-ttu-id="e97c0-970">Kirjoita **Nimi**-kenttään **Alatunniste**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-970">In the **Name** field, enter **Footer**.</span></span>
8. <span data-ttu-id="e97c0-971">Valitse **Raportti/Alatunniste** ja valitse sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-971">Select **Report\Footer**, and then select **Add**.</span></span>
9. <span data-ttu-id="e97c0-972">Valitse **Teksti\\Merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-972">Select **Text\\String**.</span></span>

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a><span data-ttu-id="e97c0-973">Sido lisätty muotoelementti</span><span class="sxs-lookup"><span data-stu-id="e97c0-973">Bind the added format element</span></span>

1. <span data-ttu-id="e97c0-974">Valitse **Muodon suunnittelija** -sivun **Määritys**-välilehden muotopuussa aktiivisessa **Alatunniste\\Merkkijono**-elementissä **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-974">On the **Format designer** page, on the **Mapping** tab, in the format tree, for the active **Footer\\String** element, select **Edit formula**.</span></span>
2. <span data-ttu-id="e97c0-975">Kirjoita kaavaeditorissa **kaava**-kenttään **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-975">In the formula editor, in the **Formula** field, enter **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span></span>
3. <span data-ttu-id="e97c0-976">Valitse **Tallenna** ja sulje kaavaeditori.</span><span class="sxs-lookup"><span data-stu-id="e97c0-976">Select **Save**, and close the formula editor.</span></span>
4. <span data-ttu-id="e97c0-977">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-977">Select **Save**.</span></span>

<span data-ttu-id="e97c0-978">Konfiguroitumuoto on muokattu siten, että sen nimi lisätään luodun raportin alatunnisteeseen käyttämällä **Alatunniste\\Merkkijono**-elementtiä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-978">The configured format has now been modified so that its name will be entered in the footer of a generated report by using the **Footer\\String** element.</span></span>

![Alatunnisteen muotoiluelementin lisääminen määritettyyn muotoon ER-toiminnon suunnittelussa](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a><span data-ttu-id="e97c0-980">Suunnittele muoto loppuun</span><span class="sxs-lookup"><span data-stu-id="e97c0-980">Complete the format design</span></span>

1. <span data-ttu-id="e97c0-981">Sulje **Muodon suunnittelija** -sivu.</span><span class="sxs-lookup"><span data-stu-id="e97c0-981">Close the **Format designer** page.</span></span>
2. <span data-ttu-id="e97c0-982">Varmista, että **kyselylomakkeen raportti**-määritys on edelleen valittuna **konfiguraatiot**-sivun konfiguraatiopuussa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-982">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire report** configuration is still selected.</span></span> <span data-ttu-id="e97c0-983">Valitse sitten **Versiot**-pikavälilehdessä konfiguraatioversio, jonka tila on **Luonnos**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-983">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
3. <span data-ttu-id="e97c0-984">Valitse **Muutoksen tila** \> **Viimeistele**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-984">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="e97c0-985">Tämän konfiguraation version 1.2 tila muutetaan **luonnoksesta** **valmiiksi**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-985">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="e97c0-986">Versiota 1.2 ei voi enää muuttaa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-986">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="e97c0-987">Tämä versio sisältää konfiguroidun muodon, ja sitä voidaan käyttää muiden ER-konfiguraatioiden pohjana.</span><span class="sxs-lookup"><span data-stu-id="e97c0-987">This version contains the configured format and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="e97c0-988">Tämän konfiguraation versio 1.3 luodaan, ja sen tila on **luonnos**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-988">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="e97c0-989">Voit muokata tätä versiota, jos haluat muuttaa **kyselylomakkeen** raporttia.</span><span class="sxs-lookup"><span data-stu-id="e97c0-989">You can edit this version to adjust the **Questionnaire** report.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a><span data-ttu-id="e97c0-990">Muodon suorittaminen sovelluksesta</span><span class="sxs-lookup"><span data-stu-id="e97c0-990">Run a format from the application</span></span>

1. <span data-ttu-id="e97c0-991">Siirry kohtaan **kyselylomake** \> **Suunnittelu** \> **Kyselylomakeraportti (palvelun tarjoaa ER)**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-991">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="e97c0-992">Valitse valintaikkunan **muodon määritys** -kentästä **kyselylomakkeiden raportti**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-992">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="e97c0-993">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-993">Select **OK**.</span></span>
4. <span data-ttu-id="e97c0-994">Määritä **ER-parametrit**-valintaikkunan **sisällytettävät rekisterit** -pikavälilehdessä suodatusvaihtoehto niin, että vain **SBCCrsExam**-kysely on mukana.</span><span class="sxs-lookup"><span data-stu-id="e97c0-994">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="e97c0-995">Vahvista suodatusvaihtoehto valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-995">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="e97c0-996">Suorita raportti valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-996">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="e97c0-997">Tarkista luotu raportti Excel-muodossa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-997">Review the generated report in Excel format.</span></span>

<span data-ttu-id="e97c0-998">Huomaa, että luodun raportin alatunniste sisältää sen luonnissa käytetyn ER-muodon nimen.</span><span class="sxs-lookup"><span data-stu-id="e97c0-998">Notice that the footer of the generated report contains the name of the ER format that was used to generate it.</span></span>

![Luotu raportti Excel-muodossa](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a><span data-ttu-id="e97c0-1000">Muodon suorittaminen ER-muodosta</span><span class="sxs-lookup"><span data-stu-id="e97c0-1000">Run a format from ER</span></span>

1. <span data-ttu-id="e97c0-1001">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-1001">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e97c0-1002">Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta, laajenna **Kysymyslomakemalli** ja valitse sitten **Kysymyslomakeraportti**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-1002">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="e97c0-1003">Valitse toimintoruudussa **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-1003">On the Action Pane, select **Run**.</span></span>
4. <span data-ttu-id="e97c0-1004">Määritä **Sähköisen raportoinnin parametrit**-valintaikkunan **sisällytettävät rekisterit** -pikavälilehdessä suodatusvaihtoehto niin, että vain **SBCCrsExam**-kysely on mukana.</span><span class="sxs-lookup"><span data-stu-id="e97c0-1004">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="e97c0-1005">Vahvista suodatusvaihtoehto valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-1005">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="e97c0-1006">Suorita raportti valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-1006">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="e97c0-1007">Tarkista luotu raportti Excel-muodossa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-1007">Review the generated report in Excel format.</span></span>

<span data-ttu-id="e97c0-1008">Huomaa, että luodun raportin alatunniste ei sisällä sen luonnissa käytetyn ER-muodon nimeä, koska tietosopimusobjekti ei siirtynyt käynnissä olevaan mallimääritykseen, kun ER-muodossa suoritettava ER-muoto kutsui sitä.</span><span class="sxs-lookup"><span data-stu-id="e97c0-1008">Notice that the footer of the generated report doesn't contain the name of ER format that was used to generate it, because the data contract object wasn't passed to the running model mapping when it was called by the ER format that was run from ER.</span></span>

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a><span data-ttu-id="e97c0-1009">Muotokohteen määrittäminen näytön esikatselua varten</span><span class="sxs-lookup"><span data-stu-id="e97c0-1009">Configure a format destination for on-screen preview</span></span>

1. <span data-ttu-id="e97c0-1010">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Sähköisen raportoinnin kohde**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-1010">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting destination**.</span></span>
2. <span data-ttu-id="e97c0-1011">Lisää **Sähköisen raportoinnin kohde** -sivulla kohdetietue konfiguroidulle **kyselylomakeraportin** ER-muodolle.</span><span class="sxs-lookup"><span data-stu-id="e97c0-1011">On the **Electronic reporting destination** page, add a destination record for the configured **Questionnaire report** ER format.</span></span>
3. <span data-ttu-id="e97c0-1012">Määritä **Tiedoston kohde** -pikavälilehdessä sen **raportti**-muotokomponentin **näyttö-** [kohde](er-destination-type-screen.md), joka on [lisätty](#AddFormatRootElement) määritetyn **kyselylomakeraportin** ER-muodon juurielementiksi.</span><span class="sxs-lookup"><span data-stu-id="e97c0-1012">On the **File destination** FastTab, set up the **Screen** [destination](er-destination-type-screen.md) for the **Report** format component that has been [added](#AddFormatRootElement) as the root element of the configured **Questionnaire report** ER format.</span></span>
4. <span data-ttu-id="e97c0-1013">Määritä **PDF-muuntoasetukset**-pikavälilehdessä kohde, joka muuntaa raportin [PDF-muotoon](electronic-reporting-destinations.md#OutputConversionToPDF), joka käyttää **vaakasuuntaista** sivun suuntaa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-1013">On the **PDF conversion settings** FastTab, configure the destination to convert a report to [PDF format](electronic-reporting-destinations.md#OutputConversionToPDF) that uses the **Landscape** page orientation.</span></span>

![Mukautetun näyttökohteen määrittäminen ER-muodossa sähköisen raportoinnin kohdesivulla](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a><span data-ttu-id="e97c0-1015">Voit esikatsella sitä PDF-tiedostona suorittamalla sovelluksen muodon</span><span class="sxs-lookup"><span data-stu-id="e97c0-1015">Run a format from the application to preview it as a PDF document</span></span>

1. <span data-ttu-id="e97c0-1016">Siirry kohtaan **kyselylomake** \> **Suunnittelu** \> **Kyselylomakeraportti (palvelun tarjoaa ER)**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-1016">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="e97c0-1017">Valitse valintaikkunan **muodon määritys** -kentästä **kyselylomakkeiden raportti**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-1017">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="e97c0-1018">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-1018">Select **OK**.</span></span>
4. <span data-ttu-id="e97c0-1019">Määritä **Sähköisen raportoinnin parametrit**-valintaikkunan **sisällytettävät rekisterit** -pikavälilehdessä suodatusvaihtoehto niin, että vain **SBCCrsExam**-kysely on mukana.</span><span class="sxs-lookup"><span data-stu-id="e97c0-1019">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="e97c0-1020">Vahvista suodatusvaihtoehto valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-1020">Select **OK** to confirm the filtering option.</span></span>

    <span data-ttu-id="e97c0-1021">Huomaa, että **Kohteet**-pikavälilehden **tuloste**-kentän arvoksi on määritetty **Näyttö**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-1021">On the **Destinations** FastTab, notice that the **Output** field is set to **Screen**.</span></span> <span data-ttu-id="e97c0-1022">Jos haluat muuttaa konfiguroituja kohteita, valitse **Muuta**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-1022">If you want to change the configured destination, select **Change**.</span></span>

    ![ER-raportin suorituksenaikainen valintaikkuna, jossa voit muuttaa konfiguroidun kohteen](./media/er-quick-start1-run-settings.png)

6. <span data-ttu-id="e97c0-1024">Suorita raportti valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e97c0-1024">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="e97c0-1025">Tarkista luotu raportti PDF-muodossa.</span><span class="sxs-lookup"><span data-stu-id="e97c0-1025">Review the generated report in PDF format.</span></span>

    ![Luodun raportin esikatselu näytöllä PDF-muodossa](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a><span data-ttu-id="e97c0-1027">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e97c0-1027">Additional resources</span></span>

- [<span data-ttu-id="e97c0-1028">Sähköisen raportoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e97c0-1028">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="e97c0-1029">Sähköisen raportoinnin kaavakieli</span><span class="sxs-lookup"><span data-stu-id="e97c0-1029">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="e97c0-1030">Monikielisten raporttien suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="e97c0-1030">Design multilingual reports</span></span>](er-design-multilingual-reports.md)
- [<span data-ttu-id="e97c0-1031">Sähköisen raportoinnin kehyksen ohjelmointirajapinta</span><span class="sxs-lookup"><span data-stu-id="e97c0-1031">ER framework API</span></span>](er-apis-app73.md)
- [<span data-ttu-id="e97c0-1032">CASE-funktio</span><span class="sxs-lookup"><span data-stu-id="e97c0-1032">CASE function</span></span>](er-functions-logical-case.md)
- [<span data-ttu-id="e97c0-1033">CONCATENATE-funktio</span><span class="sxs-lookup"><span data-stu-id="e97c0-1033">CONCATENATE function</span></span>](er-functions-text-concatenate.md)
- [<span data-ttu-id="e97c0-1034">DATETIMEFORMAT-funktio</span><span class="sxs-lookup"><span data-stu-id="e97c0-1034">DATETIMEFORMAT function</span></span>](er-functions-datetime-datetimeformat.md)
- [<span data-ttu-id="e97c0-1035">FILTER-funktio</span><span class="sxs-lookup"><span data-stu-id="e97c0-1035">FILTER function</span></span>](er-functions-list-filter.md)
- [<span data-ttu-id="e97c0-1036">FIRSTORNULL-funktio</span><span class="sxs-lookup"><span data-stu-id="e97c0-1036">FIRSTORNULL function</span></span>](er-functions-list-firstornull.md)
- [<span data-ttu-id="e97c0-1037">FORMAT-funktio</span><span class="sxs-lookup"><span data-stu-id="e97c0-1037">FORMAT function</span></span>](er-functions-text-format.md)
- [<span data-ttu-id="e97c0-1038">IF-funktio</span><span class="sxs-lookup"><span data-stu-id="e97c0-1038">IF function</span></span>](er-functions-logical-if.md)
- [<span data-ttu-id="e97c0-1039">ORDERBY-funktio</span><span class="sxs-lookup"><span data-stu-id="e97c0-1039">ORDERBY function</span></span>](er-functions-list-orderby.md)
- [<span data-ttu-id="e97c0-1040">SESSIONNOW-funktio</span><span class="sxs-lookup"><span data-stu-id="e97c0-1040">SESSIONNOW function</span></span>](er-functions-datetime-sessionnow.md)
