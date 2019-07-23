---
title: Regression Suite Automation Tool -oppaan määrittäminen ja asentaminen
description: Tämä ohjeaihe on opas, joka käsittelee Regression Suite Automation Tool (RSAT) -työkalun määrittämistä ja asentamista.
author: kfend
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: ab81e95c2e31adfefd4e5c4367a61baa7c251c43
ms.sourcegitcommit: f6581bab16225a027f4fbfad25fdef45bd286489
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/27/2019
ms.locfileid: "1703826"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="ef075-103">Regression Suite Automation Tool -oppaan määrittäminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="ef075-103">Set up and install Regression suite automation tool tutorial</span></span>
<span data-ttu-id="ef075-104">Tämä opas auttaa RSAT-työkalun asennuksessa sekä RSAT-työkalun ja sen käyttöön liittyvien työkalujen käytön aloittamisessa.</span><span class="sxs-lookup"><span data-stu-id="ef075-104">This topic is a tutorial that helps you get setup and get started with RSAT and the tools associated with using RSAT.</span></span> 

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="ef075-105">Lataa ja tallenna tämä tiedosto selaimen työkaluilla PDF-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="ef075-105">Use your internet browser tools to download and save this page in PDF format.</span></span> 

## <a name="key-concepts"></a><span data-ttu-id="ef075-106">Avainkäsitteet</span><span class="sxs-lookup"><span data-stu-id="ef075-106">Key concepts</span></span>

- <span data-ttu-id="ef075-107">Tietoja Regression Suite Automation Tool (RSAT) -työkalua tukevien erilaisten sovellusten asennuksesta ja pakollisista määrityksistä.</span><span class="sxs-lookup"><span data-stu-id="ef075-107">Understand the installation and prerequisite setup that are required for the various applications that support Regression suite automation tool (RSAT).</span></span>
- <span data-ttu-id="ef075-108">Tietoja tavasta, jolla Microsoft Dynamics 365 for Finance and Operationsin tehtävien tallennustoiminnolla yhdessä Microsoft Dynamics Lifecycle Servicesin (LCS) ja Microsoft Azure DevOpsin avulla voi luoda, määrittää, suorittaa, tutkia ja raportoida testitapauksia.</span><span class="sxs-lookup"><span data-stu-id="ef075-108">Understand how the Task recorder feature in Microsoft Dynamics 365 for Finance and Operations, together with Microsoft Dynamics Lifecycle Services (LCS) and Microsoft Azure DevOps, let you create, configure, run, investigate, and report on test cases.</span></span>
- <span data-ttu-id="ef075-109">Toimintokäyttäjille annetaan mahdollisuudet tallentaa liiketoimintatehtäviä Finance and Operationsin tehtävien tallennustoiminnolla ja muuntaa sitten tehtävätallenteet automatisoiduiksi testeiksi – ilman lähdekoodin kirjoittamista.</span><span class="sxs-lookup"><span data-stu-id="ef075-109">Empower functional users to record business tasks by using Task recorder in Finance and Operations, and then convert the task recordings into a suite of automated tests, without having to write source code.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="ef075-110">Ennen aloittamista</span><span class="sxs-lookup"><span data-stu-id="ef075-110">Before you begin</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ef075-111">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="ef075-111">Prerequisites</span></span>

- <span data-ttu-id="ef075-112">Oppaan käyttöä varten tarvitaan Finance and Operations -ympäristö, jossa on käytössä Microsoft Dynamics 365 for Finance and Operations -versio 10.0 (huhtikuu 2019) tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="ef075-112">A Finance and Operations environment that runs Microsoft Dynamics 365 for Finance and Operations version 10.0 (April 2019) or later is required for this tutorial.</span></span> <span data-ttu-id="ef075-113">Lisäksi tuetaan asiakkaita, joiden käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, Platform update 20 (PU20) tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="ef075-113">For customers who are using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, Platform update 20 (PU20) or later is also supported.</span></span>
- <span data-ttu-id="ef075-114">Käyttäjällä on oltava Finance and Operations -ympäristön järjestelmänvalvojan oikeudet.</span><span class="sxs-lookup"><span data-stu-id="ef075-114">The user must have admin rights to the Finance and Operations environment.</span></span>
- <span data-ttu-id="ef075-115">Asiakkaan vuokraajan LCS:n ja Azure DevOpsin (entinen Microsoft Visual Studio Team Services \[VSTS\]) käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="ef075-115">You must have access to the customer tenant LCS and Azure DevOps (previously known as Microsoft Visual Studio Team Services \[VSTS\]).</span></span>
- <span data-ttu-id="ef075-116">Testipaketteja luovalla ja hallitsevalla käyttäjällä on oltava Azure DevOps Test Plans- tai Test Manager -käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="ef075-116">The user that is creating and managing tests suites must have an Azure DevOps Test Plans or Test Manager license.</span></span> <span data-ttu-id="ef075-117">Test Plans -käyttö on mahdollista seuraavilla käyttöoikeuksilla:</span><span class="sxs-lookup"><span data-stu-id="ef075-117">The following licenses will also give you access to Test Plans:</span></span>
    - <span data-ttu-id="ef075-118">Visual Studio Enterprise -käyttöoikeus</span><span class="sxs-lookup"><span data-stu-id="ef075-118">Visual Studio Enterprise license</span></span>
    - <span data-ttu-id="ef075-119">Visual Studio Test Professional -käyttöoikeus</span><span class="sxs-lookup"><span data-stu-id="ef075-119">Visual Studio Test Professional license</span></span>
    - <span data-ttu-id="ef075-120">MSDN Platforms -tilaajan käyttöoikeus</span><span class="sxs-lookup"><span data-stu-id="ef075-120">MSDN Platforms subscriber license</span></span>
- <span data-ttu-id="ef075-121">RSAT-työkalua on voitava käyttää testiympäristössä selaimen kautta.</span><span class="sxs-lookup"><span data-stu-id="ef075-121">RSAT must have access to the test environment via a web browser.</span></span>
- <span data-ttu-id="ef075-122">Microsoft Excel on oltava asennettuna testiparametrien luontia ja muokkausta varten.</span><span class="sxs-lookup"><span data-stu-id="ef075-122">To generate and edit test parameters, you must have Microsoft Excel installed.</span></span>

## <a name="configure-azure-devops"></a><span data-ttu-id="ef075-123">Konfiguroi Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="ef075-123">Configure Azure DevOps</span></span>

### <a name="user-eligibility"></a><span data-ttu-id="ef075-124">Käyttäjien kelpoisuus</span><span class="sxs-lookup"><span data-stu-id="ef075-124">User eligibility</span></span>

<span data-ttu-id="ef075-125">Varmista, että käyttäjä on luotu Azure DevOpsissa ja että tilauksen taso mahdollistaa Azure Test Plans -käytön.</span><span class="sxs-lookup"><span data-stu-id="ef075-125">Make sure that the user is created in Azure DevOps and has a subscription level that provides access to Azure Test Plans.</span></span> <span data-ttu-id="ef075-126">Azure DevOps Test Plans -käyttöoikeus tarvitaan vain, jos käyttäjä luo ja hallitsee testitapauksia. (Toisin sanoen kaikki RSAT-käyttäjät eivät tarvitse tätä käyttöoikeutta.)</span><span class="sxs-lookup"><span data-stu-id="ef075-126">An Azure DevOps Test Plans license is required only if the user will create and manage test cases (that is, not all RSAT users require this license).</span></span> <span data-ttu-id="ef075-127">Lisätietoja vaadittavista käyttöoikeuksista on kohdassa [Vaadittavat käyttöoikeudet](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).</span><span class="sxs-lookup"><span data-stu-id="ef075-127">For information about the license requirements, see [License requirements](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).</span></span>

### <a name="create-a-new-azure-devops-project"></a><span data-ttu-id="ef075-128">Uuden Azure DevOps -projektin luominen</span><span class="sxs-lookup"><span data-stu-id="ef075-128">Create a new Azure DevOps project</span></span>
<span data-ttu-id="ef075-129">RSAT käyttää Azure DevOpsia testitapausten ja testipakettien hallintaan, raportointiin ja suoritettuihin testituloksiin perehtymiseen.</span><span class="sxs-lookup"><span data-stu-id="ef075-129">RSAT uses Azure Devops for test case and test suite management, reporting, and investigating test run results.</span></span> 

> [!NOTE]
> <span data-ttu-id="ef075-130">Voit käyttää aiemmin luotua Azure DevOps -projektia.</span><span class="sxs-lookup"><span data-stu-id="ef075-130">You can use an existing Azure DevOps project.</span></span> <span data-ttu-id="ef075-131">Jos aiemmin luotuun Azure DevOps -projektiin on kuitenkin määritetty mukautettu malli, saat Epäonnistuneet VSTS-synkronoinnit -virheilmoituksen, kun synkronoit testitapauksia liiketoimintaprosessien mallintajasta (BPM) Azure DevOpsiin. (Lisätietoja on osassa [Synkronoinnin testaus liiketoimintaprosessien mallintajasta Azure DevOpsiin](#test-the-synchronization-from-bpm-to-azure-devops).)</span><span class="sxs-lookup"><span data-stu-id="ef075-131">However, if your existing Azure DevOps project is set up so that it has a custom template, you will receive a "VSTS Sync Failure" error when you sync test cases from Business process modeler (BPM) to Azure DevOps (see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section).</span></span> <span data-ttu-id="ef075-132">Jos mukautetussa mallissa on käytetty seuraavia parhaita käytäntöjä, testitapaukset voidaan synkronoida Azure DevOpsiin.</span><span class="sxs-lookup"><span data-stu-id="ef075-132">If the following best practices have been followed for the custom template, you will be able to sync the test cases to Azure DevOps.</span></span> <span data-ttu-id="ef075-133">(Nämä parhaat käytännöt on mainittu virheilmoituksessa.)</span><span class="sxs-lookup"><span data-stu-id="ef075-133">(These best practices are listed in the error message.)</span></span>

- <span data-ttu-id="ef075-134">Älä poista mitään työnimiketyyppejä tai valmiita kenttiä.</span><span class="sxs-lookup"><span data-stu-id="ef075-134">Do not delete any work item types or out-of-the-box fields.</span></span>
- <span data-ttu-id="ef075-135">Älä poista mitään työnimiketyyppien tiloja.</span><span class="sxs-lookup"><span data-stu-id="ef075-135">Do not delete any state of a work item type.</span></span>
- <span data-ttu-id="ef075-136">Älä lisää mitään pakollisia kenttiä työnimiketyyppiin.</span><span class="sxs-lookup"><span data-stu-id="ef075-136">Do not add any required fields to a work item type.</span></span>

![Virheilmoitus ja parhaiden käytäntöjen luettelo](./media/setup_rsa_tool_02.png)

<span data-ttu-id="ef075-138">Muussa tapauksessa tässä oppaassa suositellaan uuden Azure DevOps -projektin luomista.</span><span class="sxs-lookup"><span data-stu-id="ef075-138">Otherwise, for this tutorial, we recommend that you create a new Azure DevOps project.</span></span> <span data-ttu-id="ef075-139">Lisätietoja on kohdassa [Ongelmat synkronoitaessa liiketoimintaprosessien mallintajaan mukautetulla Azure DevOps (VSTS) -prosessimallilla](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span><span class="sxs-lookup"><span data-stu-id="ef075-139">For more information, see [Issues when syncing to BPM using a custom Azure DevOps (VSTS) process template](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span></span>

1. <span data-ttu-id="ef075-140">Avaa Azure DevOpsin URL-osoite (`https://dev.azure.com/<Azure DevOps Name>`).</span><span class="sxs-lookup"><span data-stu-id="ef075-140">Open the Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`).</span></span>
2. <span data-ttu-id="ef075-141">Valitse Azure DevOps -sivu oikeassa yläkulmassa **Luo projekti**.</span><span class="sxs-lookup"><span data-stu-id="ef075-141">Select **Create project** in the upper-right corner of the Azure DevOps page.</span></span>

    ![Luo projekti -painike](./media/setup_rsa_tool_03.png)

3. <span data-ttu-id="ef075-143">Täytä seuraavat kentät ja valitse **Luo**:</span><span class="sxs-lookup"><span data-stu-id="ef075-143">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="ef075-144">**Projektinimi**</span><span class="sxs-lookup"><span data-stu-id="ef075-144">**Project name**</span></span>
    - <span data-ttu-id="ef075-145">**Versionhallinta** – Valitse **Team Foundation Version Control**.</span><span class="sxs-lookup"><span data-stu-id="ef075-145">**Version control** – Select **Team Foundation Version Control**.</span></span> <span data-ttu-id="ef075-146">Huomaa, että oletusvaihtoehtoa **Git** ei tueta.</span><span class="sxs-lookup"><span data-stu-id="ef075-146">Note that the default option, **Git**, isn't supported.</span></span>
    - <span data-ttu-id="ef075-147">**Työnimikeprosessi**</span><span class="sxs-lookup"><span data-stu-id="ef075-147">**Work item process**</span></span>

    ![Luo uusi projekti -valintaikkuna](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a><span data-ttu-id="ef075-149">Henkilökohtaisen käyttöoikeustunnuksen luominen</span><span class="sxs-lookup"><span data-stu-id="ef075-149">Create a personal access token</span></span>

<span data-ttu-id="ef075-150">Tässä oppaassa testitapauskirjasto luodaan ja testitapaukset synkronoidaan Azure DevOpsin kanssa LCS:n liiketoimintaprosessien mallintajan (BPM) avulla.</span><span class="sxs-lookup"><span data-stu-id="ef075-150">In this tutorial, you will use the LCS Business Process Modeler (BPM) to create a test case library and synchronize your test cases with Azure DevOps.</span></span> <span data-ttu-id="ef075-151">Tarvitset henkilökohtaisen käyttöoikeustunnuksen liiketoimintaprosessien mallintajan ja Azure DevOpsin synkronointiin.</span><span class="sxs-lookup"><span data-stu-id="ef075-151">You will need a personal access token to sync BPM with Azure DevOps.</span></span>

1. <span data-ttu-id="ef075-152">Valitse Azure DevOps -projektisivun oikeassa yläkulmassa profiilikuvake ja valitse sitten **Suojaus**.</span><span class="sxs-lookup"><span data-stu-id="ef075-152">Select the profile icon in the upper-right corner of the page for your Azure DevOps project, and then select **Security**.</span></span>

    ![Suojaus-komento](./media/setup_rsa_tool_05.png)

2. <span data-ttu-id="ef075-154">Valitse vasemman ruudun **Suojaus**-kohdassa **Henkilökohtaiset käyttöoikeustunnukset**.</span><span class="sxs-lookup"><span data-stu-id="ef075-154">In the left pane, under **Security**, select **Personal access tokens**.</span></span> <span data-ttu-id="ef075-155">Valitse sitten **Uusi tunnus**.</span><span class="sxs-lookup"><span data-stu-id="ef075-155">Then select **New Token**.</span></span>

    ![Uusi tunnus -painike käyttäjän asetusten Henkilökohtaiset käyttöoikeustunnukset -välilehdessä.](./media/setup_rsa_tool_06.png)

3. <span data-ttu-id="ef075-157">Täytä seuraavat kentät ja valitse **Luo**:</span><span class="sxs-lookup"><span data-stu-id="ef075-157">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="ef075-158">**Nimi**</span><span class="sxs-lookup"><span data-stu-id="ef075-158">**Name**</span></span>
    - <span data-ttu-id="ef075-159">**Vanhentuminen (UTC)** – valitse ensin **Mukautettu määritys** ja valitse sitten päivämäärävalitsimella viimeinen päivämäärä, jolloin tunnus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="ef075-159">**Expiration (UTC)** – Select **Custom defined**, and then use the date picker to select the last available date.</span></span>
    - <span data-ttu-id="ef075-160">**Vaikutusalueet** – valitse **Täydet käyttöoikeudet** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="ef075-160">**Scopes** – Select the **Full access** option.</span></span>

    ![Luo uusi henkilökohtainen käyttöoikeustunnus -valintaikkuna](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > <span data-ttu-id="ef075-162">Kirjoita luotu henkilökohtainen käyttöoikeustunnus muistiin.</span><span class="sxs-lookup"><span data-stu-id="ef075-162">Make a note of the personal access token that is created.</span></span> <span data-ttu-id="ef075-163">Tarvitset sitä myöhemmin RSAT-määrityksiä tehtäessä.</span><span class="sxs-lookup"><span data-stu-id="ef075-163">You will need it later when you set up the RSAT configuration.</span></span>

    ![Henkilökohtainen käyttöoikeustunnus](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a><span data-ttu-id="ef075-165">LCS-projektin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ef075-165">Configure the LCS project</span></span>

<span data-ttu-id="ef075-166">Päätestikirjastoa varten tarvitaan Lifecycle Services (LCS) -projekti.</span><span class="sxs-lookup"><span data-stu-id="ef075-166">You need a Lifecycle Services (LCS) project for your master test library.</span></span> <span data-ttu-id="ef075-167">LCS:n liiketoimintaprosessien mallintajaa (BPM) käytetään testitapausten pääkirjastona.</span><span class="sxs-lookup"><span data-stu-id="ef075-167">The LCS Business Process Modeler (BPM) is used as the master library for your test cases.</span></span> <span data-ttu-id="ef075-168">Liiketoimintaprosessien mallintajan avulla hallitaan ja jaetaan LCS-projektien kirjastoja.</span><span class="sxs-lookup"><span data-stu-id="ef075-168">BPM is used to manage and distribute test libraries across LCS projects.</span></span> <span data-ttu-id="ef075-169">Esimerkiksi testikirjastoja muodostava Microsoftin kumppani tai riippumaton ohjelmistotoimittaja (ISV) julkaisee testitapaukset BPM-kirjastoina.</span><span class="sxs-lookup"><span data-stu-id="ef075-169">For example, a Microsoft partner or independent software vendor (ISV) building test libraries will release test cases in the form of BPM libraries.</span></span> <span data-ttu-id="ef075-170">Liiketoimintaprosessien mallintajassa testitapaukset on järjestetty liiketoimintaprosessien perusteella.</span><span class="sxs-lookup"><span data-stu-id="ef075-170">In BPM, test cases are organized by business process.</span></span> <span data-ttu-id="ef075-171">Liiketoimintaprosessien mallintaja ei määritä suoritusjärjestystä eikä testausvälejä.</span><span class="sxs-lookup"><span data-stu-id="ef075-171">BPM doesn't define the execution order or frequency of your test pass.</span></span> <span data-ttu-id="ef075-172">Näitä tietoja hallitaan Azure DevOpsissa myöhemmin tässä ohjeaiheessa käsiteltävällä tavalla.</span><span class="sxs-lookup"><span data-stu-id="ef075-172">These details are managed in Azure DevOps, as described later in this topic.</span></span>  

<span data-ttu-id="ef075-173">LCS-projektissa voidaan käyttää asiakkaan nykyistä käyttöönottoa tai kumppanin projektia.</span><span class="sxs-lookup"><span data-stu-id="ef075-173">For your LCS project, you can use an existing customer implementation or partner project.</span></span>

### <a name="update-the-lcs-language"></a><span data-ttu-id="ef075-174">LCS-kielen päivittäminen</span><span class="sxs-lookup"><span data-stu-id="ef075-174">Update the LCS language</span></span>

> [!NOTE]
> <span data-ttu-id="ef075-175">Liiketoimintaprosessit näkyvät käyttöliittymässä oikein vain, LCS:n ensisijaiseksi kieleksi on määritetty **Englanti (Yhdysvallat)**.</span><span class="sxs-lookup"><span data-stu-id="ef075-175">For the user interface (UI) to correctly show business processes, the LCS preferred language must be set to **English (United States)**.</span></span>

1. <span data-ttu-id="ef075-176">Siirry LCS-käyttöönottoprojektiin.</span><span class="sxs-lookup"><span data-stu-id="ef075-176">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="ef075-177">Valitse **Asetukset**-painike (rataskuvake) oikeassa yläkulmassa ja valitse sitten **Kieliasetus**.</span><span class="sxs-lookup"><span data-stu-id="ef075-177">Select the **Settings** button (the gear symbol) in the upper-right corner, and then select **Language preference**.</span></span>

    ![Asetusvalikon komennot](./media/setup_rsa_tool_09.png)

3. <span data-ttu-id="ef075-179">Valitse **Ensisijainen kieli** -kentässä **Englanti (Yhdysvallat)** ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ef075-179">In the **Preferred language** field, select **English (United States)**, and then select **Save**.</span></span>

    ![Käyttäjäasetusten Kieliasetus-välilehti](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a><span data-ttu-id="ef075-181">LCS:n määrittäminen muodostamaan yhteys Azure DevOps -projektiin</span><span class="sxs-lookup"><span data-stu-id="ef075-181">Configure LCS to connect to the Azure DevOps project</span></span>

<span data-ttu-id="ef075-182">Jos loit aiemmin uuden Azure DevOps-projektin, määritä LCS-projekti muodostamaan siihen yhteys.</span><span class="sxs-lookup"><span data-stu-id="ef075-182">If you created a new Azure DevOps project earlier, configure the LCS project to connect to it.</span></span> <span data-ttu-id="ef075-183">Jos LCS-projekti on kuitenkin jo yhdistetty Azure DevOps-projektiin, voit jatkaa seuraavaan osaan.</span><span class="sxs-lookup"><span data-stu-id="ef075-183">Otherwise, if your LCS project is already connected to your Azure DevOps project, you can continue to the next section.</span></span>

1. <span data-ttu-id="ef075-184">Siirry LCS-käyttöönottoprojektiin.</span><span class="sxs-lookup"><span data-stu-id="ef075-184">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="ef075-185">Valitse ensin **Valikko**-painike ja sitten **Projektiasetukset**.</span><span class="sxs-lookup"><span data-stu-id="ef075-185">Select the **Menu** button, and then select **Project settings**.</span></span>

    ![Projektiasetukset-komento](./media/setup_rsa_tool_11.png)

3. <span data-ttu-id="ef075-187">Valitse vasemmassa ruudussa ensin **Visual Studio Team Services** ja sitten **Määritä Visual Studio Team Services**.</span><span class="sxs-lookup"><span data-stu-id="ef075-187">In the left pane, select **Visual Studio Team Services**, and then select **Setup Visual Studio Team Services**.</span></span>

    ![Projektiasetusten Visual Studio Team Services -välilehti:](./media/setup_rsa_tool_12.png)

4. <span data-ttu-id="ef075-189">Anna **Azure DevOps -sivuston URL-osoite** -kentässä Azure DevOps-sivuston URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="ef075-189">In the **Azure DevOps site URL** field, enter the URL of the Azure DevOps site.</span></span> <span data-ttu-id="ef075-190">Anna **Henkilökohtainen käyttöoikeustunnus** -kentässä aiemmin luotu henkilökohtainen käyttöoikeustunnus.</span><span class="sxs-lookup"><span data-stu-id="ef075-190">In the **Personal access token** field, enter the personal access token that was created earlier.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef075-191">Vaikka VSTS on nykyään Azure DevOps, käytä vanhaa URL-osoitetta, kun yhdistät LCS:n Azure DevOps-projektiin.</span><span class="sxs-lookup"><span data-stu-id="ef075-191">Although VSTS is now known as Azure DevOps, to connect LCS to your Azure DevOps project, use the old URL.</span></span> <span data-ttu-id="ef075-192">Esimerkiksi tässä oppaassa käytetään seuraavaa Azure DevOpsin URL-osoitetta: `https://dev.azure.com/D365FOFastTrack/`.</span><span class="sxs-lookup"><span data-stu-id="ef075-192">For example, the Azure DevOps URL that is used in this tutorial is `https://dev.azure.com/D365FOFastTrack/`.</span></span> <span data-ttu-id="ef075-193">Seuraavassa kuvassa se on kuitenkin on muodossa `https://D365FOFastTrack.visualstudio.com/`.</span><span class="sxs-lookup"><span data-stu-id="ef075-193">However, in the following illustration, it's entered as `https://D365FOFastTrack.visualstudio.com/`.</span></span>

    ![Visual Studio Team Servicesin määrittämisen vaihe 1](./media/setup_rsa_tool_13.png)

5. <span data-ttu-id="ef075-195">Valitse **Jatka**.</span><span class="sxs-lookup"><span data-stu-id="ef075-195">Select **Continue**.</span></span>
6. <span data-ttu-id="ef075-196">Valitse **Visual Studio Team Services -projekti** -kentässä valitun sivuston VSTS-projekti, joka yhdistetään LCS-projektiin.</span><span class="sxs-lookup"><span data-stu-id="ef075-196">In the **Visual Studio Team Services project** field, select the VSTS project on the selected site to link with the LCS project.</span></span> <span data-ttu-id="ef075-197">**Prosessimalli**-kentän asetuksena on oletusarvoisesti **Ketterä**.</span><span class="sxs-lookup"><span data-stu-id="ef075-197">The **Process template** field is set to **Agile** by default.</span></span> <span data-ttu-id="ef075-198">Tutustu mukautetun mallin parhaita käytäntöjä koskeviin ohjeisiin osassa [Uuden Azure DevOps-projektin luominen](#create-a-new-azure-devops-project).</span><span class="sxs-lookup"><span data-stu-id="ef075-198">For a custom template, review the best practice guidance in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span> <span data-ttu-id="ef075-199">Valitse sitten **Jatka**.</span><span class="sxs-lookup"><span data-stu-id="ef075-199">Then select **Continue**.</span></span>

    ![Visual Studio Team Servicesin määrittämisen vaihe 2](./media/setup_rsa_tool_14.png)

7. <span data-ttu-id="ef075-201">Tarkista asetukset ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ef075-201">Review your settings, and then select **Save**.</span></span>

    ![Visual Studio Team Servicesin määrittämisen vaihe 3](./media/setup_rsa_tool_15.png)

8. <span data-ttu-id="ef075-203">Valitse **Valtuuta**. LCS on nyt valtuutettu käyttämään määritettyä Azure DevOps -sivustoa puolestasi ja ottamaan VSTS:n kanssa integroituvat toiminnot käyttöön.</span><span class="sxs-lookup"><span data-stu-id="ef075-203">Select **Authorize** to authorize LCS to access the configured Azure DevOps site on your behalf and to turn on features that integrate with VSTS.</span></span>

    ![Valtuuta-painike](./media/setup_rsa_tool_16.png)

9. <span data-ttu-id="ef075-205">Avautuvassa viestiruudussa on seuraava ilmoitus: Sinut ohjataan ulkoiselle sivustolle, jossa voit valtuuttaa Lifecycle Servicesin muodostamaan yhteyden Visual Studio Team Services -palveluun puolestasi.</span><span class="sxs-lookup"><span data-stu-id="ef075-205">A message box appears that states, "You are about to be redirected to an eternal site to authorize LCS to connect to Visual Studio Team Services on your behalf.</span></span> <span data-ttu-id="ef075-206">Jatketaanko?</span><span class="sxs-lookup"><span data-stu-id="ef075-206">Proceed?"</span></span> <span data-ttu-id="ef075-207">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="ef075-207">Select **Yes**.</span></span>

    ![Viestiruutu](./media/setup_rsa_tool_17.png)

10. <span data-ttu-id="ef075-209">Valitse **Hyväksy**.</span><span class="sxs-lookup"><span data-stu-id="ef075-209">Select **Accept**.</span></span>

    ![Käytön valtuuttaminen](./media/setup_rsa_tool_18.png)

11. <span data-ttu-id="ef075-211">Jos sinut valtuutetaan käyttäjäksi, käyttöliittymän pitäisi palautua LCS-projektin asetussivulle.</span><span class="sxs-lookup"><span data-stu-id="ef075-211">If you're authorized as a user, the UI should you return to the LCS project settings page.</span></span>

    ![Valtuutettu käyttäjä](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a><span data-ttu-id="ef075-213">Uuden BPM-kirjaston luominen</span><span class="sxs-lookup"><span data-stu-id="ef075-213">Create a new BPM library</span></span>

1. <span data-ttu-id="ef075-214">Siirry LCS-käyttöönottoprojektiin.</span><span class="sxs-lookup"><span data-stu-id="ef075-214">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="ef075-215">Valitse ensin **Valikko**-painike ja sitten **Liiketoimintaprosessien mallintaja**.</span><span class="sxs-lookup"><span data-stu-id="ef075-215">Select the **Menu** button, and then select **Business process modeler**.</span></span>

    ![Liiketoimintaprosessien mallintaja -komento](./media/setup_rsa_tool_20.png)

3. <span data-ttu-id="ef075-217">Valitse **Uusi kirjasto**.</span><span class="sxs-lookup"><span data-stu-id="ef075-217">Select **New library**.</span></span>

    ![Uusi kirjasto -painike](./media/setup_rsa_tool_21.png)

4. <span data-ttu-id="ef075-219">Anna **Kirjaston nimi** -kentässä nimi ja valitse sitten **Luo**.</span><span class="sxs-lookup"><span data-stu-id="ef075-219">In the **Library name** field, enter a name, and then select **Create**.</span></span> <span data-ttu-id="ef075-220">Tässä oppaassa BPM-kirjaston nimeksi annetaan **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="ef075-220">For this tutorial, name the BPM library **RSAT**.</span></span>

    ![Luo uusi kirjasto -valintaikkuna](./media/setup_rsa_tool_22.png)

5. <span data-ttu-id="ef075-222">Avaa uusi **RSAT**-BPM-kirjasto.</span><span class="sxs-lookup"><span data-stu-id="ef075-222">Open the new **RSAT** BPM library.</span></span>
6. <span data-ttu-id="ef075-223">Valitse **Ydinliiketoimintaprosessin malli** -prosessi ja valitse sitten oikealla **Muokkaustila**.</span><span class="sxs-lookup"><span data-stu-id="ef075-223">Select the **Sample Core Business Process** process, and then, on the right, select **Edit mode**.</span></span>

    ![Muokkaustila-painike](./media/setup_rsa_tool_23.png)

7. <span data-ttu-id="ef075-225">Vaihda sekä **Nimi**- että **Kuvaus**-kentän nimeksi **Luo tuote**.</span><span class="sxs-lookup"><span data-stu-id="ef075-225">Change the value of both the **Name** field and the **Description** field to **Create a product**.</span></span> <span data-ttu-id="ef075-226">Valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ef075-226">Then select **Save**.</span></span>

    ![Nimi- ja Kuvaus-kentät](./media/setup_rsa_tool_24.png)

## <a name="finance-and-operations-environment"></a><span data-ttu-id="ef075-228">Finance and Operations -ympäristö</span><span class="sxs-lookup"><span data-stu-id="ef075-228">Finance and Operations environment</span></span>

### <a name="version-requirement"></a><span data-ttu-id="ef075-229">Version vaatimus</span><span class="sxs-lookup"><span data-stu-id="ef075-229">Version requirement</span></span>

<span data-ttu-id="ef075-230">Edellytyksenä Finance and Operationsin testi- tai eristysympäristö, jossa käytössä versio 10.</span><span class="sxs-lookup"><span data-stu-id="ef075-230">A Finance and Operations test or sandbox environment that runs version 10 is required.</span></span> <span data-ttu-id="ef075-231">Lisäksi tuetaan asiakkaita, joiden käytössä on versio7.3, Platform update 20 tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="ef075-231">For customers that are using version 7.3, Platform update 20 or later is also supported.</span></span>

> [!NOTE]
> <span data-ttu-id="ef075-232">RSAT-työkalua on voitava käyttää Finance and Operationsin testiympäristössä selaimen kautta.</span><span class="sxs-lookup"><span data-stu-id="ef075-232">RSAT must have access to your Finance and Operations test environment via a web browser.</span></span>

### <a name="user-criteria"></a><span data-ttu-id="ef075-233">Käyttäjän vaatimukset</span><span class="sxs-lookup"><span data-stu-id="ef075-233">User criteria</span></span>

<span data-ttu-id="ef075-234">Käyttäjällä on oltava ympäristön järjestelmänvalvojan oikeudet.</span><span class="sxs-lookup"><span data-stu-id="ef075-234">The user must have admin rights to this environment.</span></span>

### <a name="set-up-help-settings-to-connect-with-lcs"></a><span data-ttu-id="ef075-235">LCS:n yhdistämisen ohjeasetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ef075-235">Set up Help settings to connect with LCS</span></span>

<span data-ttu-id="ef075-236">Tämä vaihe on välttämätön muodostettaessa yhteyttä LCS:ään, sillä sen avulla tehtävätallenteet voidaan tallentaa sopivaan LCS:n BPM-kirjastoon Finance and Operations -asiakasohjelman avulla.</span><span class="sxs-lookup"><span data-stu-id="ef075-236">This step is required in order to connect with LCS so that task recordings can be saved to the appropriate BPM library in LCS through the Finance and Operations client.</span></span>

1. <span data-ttu-id="ef075-237">Avaa Finance and Operations -asiakasohjelma.</span><span class="sxs-lookup"><span data-stu-id="ef075-237">Open the Finance and Operations client.</span></span>
2. <span data-ttu-id="ef075-238">Valitse **Järjestelmän hallinta \> Asetukset \> Järjestelmän parametrit**.</span><span class="sxs-lookup"><span data-stu-id="ef075-238">Go to **System Administration \> Setup \> System parameters**.</span></span>
3. <span data-ttu-id="ef075-239">Valitse **Ohje**-välilehden **Lifecycle Services -palvelun ohjeiden konfiguraatio** -kentässä soveltuva LCS-projekti (tässä oppaassa se on **RSAT**).</span><span class="sxs-lookup"><span data-stu-id="ef075-239">On the **Help** tab, in the **Lifecycle Services help configuration** field, select the relevant LCS project (**RSAT** for this tutorial).</span></span>

    ![Lifecycle Services -palvelun ohjeiden konfiguraatio -kenttä Ohje-välilehdessä](./media/setup_rsa_tool_25.png)

    <span data-ttu-id="ef075-241">Soveltuvan LCS-projektin BPM-kirjastot täytetään.</span><span class="sxs-lookup"><span data-stu-id="ef075-241">BPM libraries are filled in under the appropriate LCS project.</span></span>

4. <span data-ttu-id="ef075-242">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ef075-242">Select **Save**.</span></span>
5. <span data-ttu-id="ef075-243">Selain on ehkä päivitettävä, ennen kuin päivitetty Ohje-sisältö tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="ef075-243">You might have to refresh the browser to see the updated Help content.</span></span>

    ![Ilmoitus selaimen päivittämisestä](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a><span data-ttu-id="ef075-245">Tehtävätallenteet</span><span class="sxs-lookup"><span data-stu-id="ef075-245">Task recordings</span></span>

> [!NOTE]
> <span data-ttu-id="ef075-246">Varmista, että kaikki tehtävätallenteet käynnistyvät Finance and Operationsin pääkoontinäytöstä.</span><span class="sxs-lookup"><span data-stu-id="ef075-246">Make sure that all your task recordings start on the main dashboard of Finance and Operations.</span></span> <span data-ttu-id="ef075-247">Yksittäiset tallenteet kannattaa pitää lyhyinä ja niissä kannattaa keskittyä yhteen liiketoimintatehtävään, kuten myyntitilauksen luontiin.</span><span class="sxs-lookup"><span data-stu-id="ef075-247">Keep individual recordings short, and focus on one business task, such as creating a sales order.</span></span>

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a><span data-ttu-id="ef075-248">Tehtävätallenteen luominen ja tallentaminen BPM-kirjastoon</span><span class="sxs-lookup"><span data-stu-id="ef075-248">Create a task recording and save it to the BPM library</span></span>

<span data-ttu-id="ef075-249">Luo vastaava tehtävätallenne, jonka voit liittää uuteen BPM-kirjastoon luotuun yksinkertaiseen liiketoimintaprosessiin.</span><span class="sxs-lookup"><span data-stu-id="ef075-249">Create a corresponding task recording that you can attach to the simple business process that was created in the new BPM library.</span></span>

1. <span data-ttu-id="ef075-250">Avaa Finance and Operations -asiakasohjelma.</span><span class="sxs-lookup"><span data-stu-id="ef075-250">Open the Finance and Operations client.</span></span>
2. <span data-ttu-id="ef075-251">Valitse pääkoontinäytössä **Asetukset**-painike (rataskuvake) ja valitse sitten **Tehtävän tallennustoiminto**.</span><span class="sxs-lookup"><span data-stu-id="ef075-251">On the main dashboard, select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>

    ![Asetusvalikon komennot](./media/setup_rsa_tool_27.png)

3. <span data-ttu-id="ef075-253">Valitse **Luo tallenne**.</span><span class="sxs-lookup"><span data-stu-id="ef075-253">Select **Create recording**.</span></span>

    ![Luo tallenne -painike](./media/setup_rsa_tool_28.png)

4. <span data-ttu-id="ef075-255">Täytä **Tallenteen nimi**- ja **Tallenteen kuvaus** -kentät ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ef075-255">Fill in the **Recording name** and **Recording description** fields, and then select **Start**.</span></span>

    ![Tallenteen nimi- ja Tallenteen kuvaus -kentät](./media/setup_rsa_tool_29.png)

5. <span data-ttu-id="ef075-257">Tallenna tuotteen luontivaiheet.</span><span class="sxs-lookup"><span data-stu-id="ef075-257">Record the steps for creating a product.</span></span> <span data-ttu-id="ef075-258">Kun olet valmis, lopeta tallennus valitsemalla **Pysäytä**.</span><span class="sxs-lookup"><span data-stu-id="ef075-258">When you've finished, select **Stop** to stop recording.</span></span>

    ![Tuotteen luontiohjeet](./media/setup_rsa_tool_30.png)

6. <span data-ttu-id="ef075-260">Valitse **Tallenna Lifecycle Servicesiin**.</span><span class="sxs-lookup"><span data-stu-id="ef075-260">Select **Save to Lifecycle Services**.</span></span>

    ![Tallennusasetukset](./media/setup_rsa_tool_31.png)

    <span data-ttu-id="ef075-262">Kirjaston tiedot ladataan LCS:stä.</span><span class="sxs-lookup"><span data-stu-id="ef075-262">Library information is loaded from LCS.</span></span>

    ![Tilanneilmaisin](./media/setup_rsa_tool_32.png)

7. <span data-ttu-id="ef075-264">Valitse tehtävätallenteeseen liitettävä BPM-kirjasto.</span><span class="sxs-lookup"><span data-stu-id="ef075-264">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="ef075-265">Tässä oppaassa valitaan aiemmin luotu **RSAT**-BPM-kirjasto ja siinä oleva **Luo tuote** -liiketoimintaprosessi.</span><span class="sxs-lookup"><span data-stu-id="ef075-265">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Create a product** business process under it.</span></span> <span data-ttu-id="ef075-266">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef075-266">Then select **OK**.</span></span>

    ![Tehtävätallenteen liittäminen BPM-kirjastoon ja liiketoimintaprosessiin](./media/setup_rsa_tool_33.png)

    <span data-ttu-id="ef075-268">Tallennus Lifecycle Servicesiin onnistui -sanoma avautuu.</span><span class="sxs-lookup"><span data-stu-id="ef075-268">A "Saving to Lifecycle Services was successful" message appears.</span></span>

    ![Sanoma onnistuneesta LCS-tallennuksesta](./media/setup_rsa_tool_34.png)

8. <span data-ttu-id="ef075-270">Jos haluat tallentaa tehtävätallenteen paikallisesti ja ladata sen sitten liiketoimintaprosessien mallintajaan LCS:n kautta, toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="ef075-270">If you want to save the task recording locally and then upload it to BPM through LCS, follow these steps:</span></span>

    1. <span data-ttu-id="ef075-271">Kun tallenne on valmis, valitse **Tallenna tälle tietokoneelle**.</span><span class="sxs-lookup"><span data-stu-id="ef075-271">After the recording is completed, select **Save to this PC**.</span></span>

        ![Tallennusasetukset](./media/setup_rsa_tool_35.png)

    2. <span data-ttu-id="ef075-273">Tallenna tiedosto paikallisesti tietokoneeseen valitsemalla selaimen ilmoituspalkissa **Tallenna** tai **Tallenna nimellä**.</span><span class="sxs-lookup"><span data-stu-id="ef075-273">In the browser's Notification bar, select **Save** or **Save As** to save the file on your local computer.</span></span>

        ![Ilmoituspalkki](./media/setup_rsa_tool_36.png)

    3. <span data-ttu-id="ef075-275">Siirry **RSAT**-BPM-kirjasto ja valitse liiketoimintaprosessi, jonka tehtävätallenne tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="ef075-275">Go to the **RSAT** BPM library, and select the business process to save the task recording against.</span></span>
    4. <span data-ttu-id="ef075-276">Valitse **Yleiskuvaus**-välilehdessä **Lataa palvelimeen**.</span><span class="sxs-lookup"><span data-stu-id="ef075-276">On the **Overview** tab, select **Upload**.</span></span>

        ![Lataa palvelimeen -painike](./media/setup_rsa_tool_37.png)

    5. <span data-ttu-id="ef075-278">Valitse ensin **Selaa** ja sitten aiemmin tallennettu .axtr-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="ef075-278">Select **Browse**, and select the .axtr file that you saved earlier.</span></span> <span data-ttu-id="ef075-279">Valitse sitten **Lataa palvelimeen**.</span><span class="sxs-lookup"><span data-stu-id="ef075-279">Then select **Upload**.</span></span>

        ![Palvelimeen ladattavan. axtr-tiedoston valitseminen](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a><span data-ttu-id="ef075-281">Liiketoimintaprosessien mallintajasta Azure DevOpsiin tapahtuvan synkronoinnin testaaminen</span><span class="sxs-lookup"><span data-stu-id="ef075-281">Test the synchronization from BPM to Azure DevOps</span></span>

<span data-ttu-id="ef075-282">Nyt kun tehtävätallenne on liitetty liiketoimintaprosessiin, sinun on tarkistettava, että kyseinen liiketoimintaprosessi ja liitetty tehtävätallenne voidaan synkronoida Azure DevOpsiin ominaisuutena ja testitapauksena käyttämällä VSTS:n synkronointiominaisuutta LCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="ef075-282">Now that a task recording is attached to the business process, you must validate that the business process and the associated task recording can be synced to Azure DevOps as a feature and a test case (respectively) by using the VSTS sync feature in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="ef075-283">Azure DevOpsissa luotava vastaava työnimiketyyppi vaihtelee sen prosessimallin mukaan, joka valittiin, kun LCS-projekti määritettiin Azure DevOpsin kanssa osassa [Uuden Azure DevOps -projektin luominen](#create-a-new-azure-devops-project) kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="ef075-283">The corresponding work item type that is created in Azure DevOps will vary, depending on the process template that you selected when you configured the LCS project with Azure DevOps, as described in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span>

1. <span data-ttu-id="ef075-284">Siirry BPM-kirjastoon ja avaa aiemmin luotu **RSAT**-kirjastoon.</span><span class="sxs-lookup"><span data-stu-id="ef075-284">Go to the BPM library, and open the **RSAT** library that you created earlier.</span></span>
2. <span data-ttu-id="ef075-285">Valitse ensin kolme pistettä -painike (**...**) ja sitten **VSTS-synkronointi**.</span><span class="sxs-lookup"><span data-stu-id="ef075-285">Select the ellipsis button (**...**), and select **VSTS sync**.</span></span>

    ![Kolme pistettä -valikon VSTS-synkronointikomento](./media/setup_rsa_tool_39.png)

    <span data-ttu-id="ef075-287">Kun VSTS-synkronointi on valmis, vasemmalle avautuu **Tarpeet**-välilehti, jossa on vastaava Azure DevOps-työnimike.</span><span class="sxs-lookup"><span data-stu-id="ef075-287">After VSTS sync is completed, a **Requirements** tab appears on the left side and includes the corresponding Azure DevOps work item.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef075-288">Azure DevOpsissa luodussa työnimikkeessä BPM-kirjaston nimi on otsikon etuliitteenä.</span><span class="sxs-lookup"><span data-stu-id="ef075-288">The work item that is created in Azure DevOps will have the BPM library name as the title prefix.</span></span>

    ![Tarpeet-välilehti](./media/setup_rsa_tool_40.png)

3. <span data-ttu-id="ef075-290">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="ef075-290">Refresh the page.</span></span>
4. <span data-ttu-id="ef075-291">Valitse kolme pistettä (**...**) -painike. Näkyviin tulee lisäasetus **Synkronoi testitapaukset**.</span><span class="sxs-lookup"><span data-stu-id="ef075-291">Select the ellipsis button (**...**). You will see an additional option, **Sync test cases**.</span></span> <span data-ttu-id="ef075-292">Valitse tämä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="ef075-292">Select this option.</span></span>

    ![Kolme pistettä -valikon Synkronoi testitapaukset -komento](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > <span data-ttu-id="ef075-294">Jos **Synkronoi testitapaukset** -vaihtoehto ei ole valittavissa sivun päivityksen jälkeen, siirry liiketoimintaprosessien mallintajan pääsivulle ja valitse koko kirjaston **Synkronoi testitapaukset**.</span><span class="sxs-lookup"><span data-stu-id="ef075-294">If the **Sync test cases** option isn't available after you refresh the page, go to main page for BPM, and select **Sync test cases** for the whole library itself.</span></span> <span data-ttu-id="ef075-295">Tällä tavoin voit pakottaa tehokkaasti koko kirjaston synkronoinnin.</span><span class="sxs-lookup"><span data-stu-id="ef075-295">In this way, you effectively force a synchronization for the whole library.</span></span>
    > 
    > ![Koko kirjaston Synkronoi testitapaukset -asetuksen valitseminen](./media/setup_rsa_tool_42.png)

    <span data-ttu-id="ef075-297">Kun Synkronoi testitapaukset on valmis, **Tarpeet**-välilehteen luodaan uusi testitapaus.</span><span class="sxs-lookup"><span data-stu-id="ef075-297">After Sync test cases is completed, a new test case is created on the **Requirements** tab.</span></span>

    ![Uusi testitapaus Tarpeet-välilehdessä](./media/setup_rsa_tool_43.png)

5. <span data-ttu-id="ef075-299">Siirry Azure DevOps -projektiin ja valitse **Taulut \> Työnimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="ef075-299">Go to your Azure DevOps project, and select **Boards \> Work Items**.</span></span>

    ![Taulujen Työnimikkeet-komento](./media/setup_rsa_tool_44.png)

6. <span data-ttu-id="ef075-301">Tarkista, että BPM-synkronoinnilla luotu työnimike ja testitapaus ovat olemassa.</span><span class="sxs-lookup"><span data-stu-id="ef075-301">Validate that the work item and test case that you created through BPM synchronization exist.</span></span>

    ![Työnimike ja testitapaus](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a><span data-ttu-id="ef075-303">RSAT-työkalun määrittäminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="ef075-303">Install and Configure RSAT</span></span>

<span data-ttu-id="ef075-304">RSAT voidaan asentaa mihin tahansa tietokoneeseen, jossa on Windows 10 ja joka voidaan yhdistää Finance and Operations -ympäristöön selaimella (Internet Explorer tai Google Chrome).</span><span class="sxs-lookup"><span data-stu-id="ef075-304">RSAT can be installed on any computer that runs Windows 10 and that can connect to the Finance and Operations environment via a web browser (Internet Explorer or Google Chrome).</span></span>

> [!NOTE]
> <span data-ttu-id="ef075-305">Työkalun aiemman version asennus kannattaa poistaa ennen uuden version asentamista.</span><span class="sxs-lookup"><span data-stu-id="ef075-305">Before you install a new version of the tool, we recommend that you uninstall the previous version.</span></span>

### <a name="install-an-authentication-certificate"></a><span data-ttu-id="ef075-306">Todennuksen varmenteen asentaminen</span><span class="sxs-lookup"><span data-stu-id="ef075-306">Install an authentication certificate</span></span>

<span data-ttu-id="ef075-307">Todenteen käyttöönottaminen edellyttää, että varmenne luodaan ja asennetaan siihen tietokoneeseen, jossa RSAT-työkalua käytetään.</span><span class="sxs-lookup"><span data-stu-id="ef075-307">To enable authentication, you must generate and install a certificate on the same computer that RSAT is running on.</span></span>

#### <a name="generate-a-certificate"></a><span data-ttu-id="ef075-308">Uuden varmenteen luominen</span><span class="sxs-lookup"><span data-stu-id="ef075-308">Generate a certificate</span></span>

1. <span data-ttu-id="ef075-309">Luo varmennetiedosto avaamalla Microsoft Windowsin PowerShell-ikkuna järjestelmänvalvojana ja suorittamalla seuraava komento.</span><span class="sxs-lookup"><span data-stu-id="ef075-309">To generate a certificate file, open a Microsoft Windows PowerShell window as an admin, and run the following command.</span></span>

    ```
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. <span data-ttu-id="ef075-310">Avaa varmenteiden hallinta kirjoittamalla **certlm.msc** **Suorita**-valintaikkunaan ja vahvistamalla, että **Automaattinen D365-testausvarmenne** on luotu, valitsemalla **Henkilökohtainen \> Varmenteet**.</span><span class="sxs-lookup"><span data-stu-id="ef075-310">Open certificate manager by entering **certlm.msc** in the **Run** dialog box, and confirm that the **D365 Automated testing certificate** certificate is created under **Personal \> Certificates**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef075-311">Varmista, että olet kirjoittanut **certlm.msc** eikä **certmgr.msc**, sillä varmenteet on tallennettu paikallisesti tietokoneeseen.</span><span class="sxs-lookup"><span data-stu-id="ef075-311">Be sure to enter **certlm.msc**, not **certmgr.msc**, because the certificates are stored on the local computer.</span></span>

    ![Automatisoitu D365-testausvarmenne](./media/setup_rsa_tool_46.png)

3. <span data-ttu-id="ef075-313">Napsauta varmennetta hiiren kakkospainikkeella ja valitse sitten **Kopioi**.</span><span class="sxs-lookup"><span data-stu-id="ef075-313">Right-click the certificate, and then select **Copy**.</span></span>
4. <span data-ttu-id="ef075-314">Valitse **Luotetut varmenteiden päämyöntäjät \> Varmenteet**.</span><span class="sxs-lookup"><span data-stu-id="ef075-314">Go to **Trusted Root Certification Authorities \> Certificates**.</span></span>

    ![Luotetut varmenteiden päämyöntäjät -kansiossa oleva Varmenteet-kansio](./media/setup_rsa_tool_47.png)

5. <span data-ttu-id="ef075-316">Valitse **Toiminto**-valikossa **Liitä**. Varmenne kopioidaan nyt **Luotetut varmenteiden päämyöntäjät** -sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="ef075-316">On the **Action** menu, select **Paste** to copy the certificate to the **Trusted Root Certification Authorities** location.</span></span>

    ![Toimintovalikon Liitä-komento](./media/setup_rsa_tool_48.png)

6. <span data-ttu-id="ef075-318">Saat asennetun varmenteen allekirjoituksen ilman välilyöntejä ja erikoismerkkejä avaamalla Windows PowerShell -ikkunan järjestelmänvalvojana ja suorittamalla seuraavat komennot.</span><span class="sxs-lookup"><span data-stu-id="ef075-318">To get the thumbprint of the installed certificate, but without spaces or special characters, open a Windows PowerShell window as an admin, and run the following commands.</span></span>

    ```
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > <span data-ttu-id="ef075-319">Tallenna allekirjoitus, koska tarvitset sitä myöhemmin, kun päivität AOS-palvelimen .wif-tiedostot ja määrität RSAT-määritykset.</span><span class="sxs-lookup"><span data-stu-id="ef075-319">Save the thumbprint, because you will need it later when you update the .wif files for Application Object Server (AOS) and set up the RSAT configuration.</span></span>

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a><span data-ttu-id="ef075-320">AOS-tietokoneen määrittäminen luottamaan yhteyteen</span><span class="sxs-lookup"><span data-stu-id="ef075-320">Configure the AOS computer to trust the connection</span></span>

> [!NOTE]
> <span data-ttu-id="ef075-321">Jos Finance and Operations -ympäristö taso 2+ -ympäristö, **kaikkien** ympäristön AOS-tietokoneiden varmenteen allekirjoitus on päivitettävä wif.config-tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="ef075-321">If the Finance and Operations environment is a Tier 2+ environment, the certificate thumbprint must be updated in the wif.config file for **all** AOS computers for the environment.</span></span>

1. <span data-ttu-id="ef075-322">Muodosta RDP-etäkäyttöprotokollayhteys AOS-tietokoneeseen.</span><span class="sxs-lookup"><span data-stu-id="ef075-322">Establish a Remote Desktop Protocol (RDP) connection to the AOS computer.</span></span> <span data-ttu-id="ef075-323">Kirjautumistiedot ovat LCS:n ympäristön tietojen sivulla.</span><span class="sxs-lookup"><span data-stu-id="ef075-323">Sign-in details are available on the environment details page in LCS.</span></span>
2. <span data-ttu-id="ef075-324">Avaa Microsoft Internet Information Services (IIS) ja etsi **AOSService** sivustoluettelossa.</span><span class="sxs-lookup"><span data-stu-id="ef075-324">Open Microsoft Internet Information Services (IIS), and find **AOSService** in the list of sites.</span></span>

    ![AOSService sivustoluettelossa](./media/setup_rsa_tool_49.png)

3. <span data-ttu-id="ef075-326">Avaa **\<Asema\>: \\AosService\\WebRoot**-kansio valitsemalla hiiren kakkospainikkeella **Selaa**.</span><span class="sxs-lookup"><span data-stu-id="ef075-326">Right-click **Explore** to open the **\<Drive\>: \\AosService\\WebRoot** folder.</span></span> <span data-ttu-id="ef075-327">Etsi **wif.config**-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="ef075-327">Find the **wif.config** file.</span></span>

    ![Wif.config-tiedosto WebRoot-kansiossa](./media/setup_rsa_tool_50.png)

4. <span data-ttu-id="ef075-329">Päivitä **wif.config**-tiedosto lisäämällä varmenteen ja myöntäjän nimeen uusi myöntäjä, kuten seuraavassa esimerkissä.</span><span class="sxs-lookup"><span data-stu-id="ef075-329">Update the **wif.config** file by adding a new authority entry for your certificate and authority name, as shown in the following example.</span></span>

    ```
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > <span data-ttu-id="ef075-330">Jos samalla Finance and Operations -sovelluksella on useita käyttäjiä, kunkin käyttäjän on luotava erillinen allekirjoitus ja kaikki nämä allekirjoitukset on lisättävä **\<keys\>**-osaan.</span><span class="sxs-lookup"><span data-stu-id="ef075-330">If multiple users are using the same Finance and Operations application, each user must generate separate thumbprints, and each of those thumbprints must be added in the **\<keys\>** section.</span></span>

5. <span data-ttu-id="ef075-331">Jos AOS-tietokonetta on useita, toista vaiheet 3–4 kussakin tietokoneessa.</span><span class="sxs-lookup"><span data-stu-id="ef075-331">If there is more than one AOS computer, repeat steps 3 through 4 for each additional computer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef075-332">Vanhoista tason 2 ympäristöistä poiketen, uudet tason 2 ympäristöt otetaan käyttöön kahdessa AOS-esiintymässä.</span><span class="sxs-lookup"><span data-stu-id="ef075-332">Unlike older Tier 2 environments, new Tier 2 environments are deployed with two AOS instances.</span></span>

6. <span data-ttu-id="ef075-333">Suorita **iisreset** kaikissa AOS-tietokoneissa.</span><span class="sxs-lookup"><span data-stu-id="ef075-333">Run **iisreset** on all the AOS computers.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef075-334">Jos sinulla ei ole tarvittavia järjestelmänvalvojan oikeuksia **iisreset**-komennon suorittamiseen tason 1 tietokoneessa, valitse LCS:n Ympäristön tiedot -sivulla Ylläpidä > Käynnistä palvelut uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ef075-334">If you don't have admin rights to run **iisreset** on a Tier 1 computer, on the Environment details page in LCS, select Maintain > Restart services.</span></span>

#### <a name="tier-2-environment"></a><span data-ttu-id="ef075-335">Tason 2+ ympäristö</span><span class="sxs-lookup"><span data-stu-id="ef075-335">Tier 2+ environment</span></span>

<span data-ttu-id="ef075-336">Jos käytössä on tason 2+ (Standard-hyväksyntätestaus-eritysympäristö tai uudempi) Finance and Operations -ympäristö, varmista tai määritä seuraava rekisteriasetus siinä tietokoneessa, johon RSAT on asennettu.</span><span class="sxs-lookup"><span data-stu-id="ef075-336">If a Tier 2+ (Standard Acceptance Test sandbox or higher) Finance and Operations environment is used, verify or set the following registry setting on the computer where RSAT is installed.</span></span> <span data-ttu-id="ef075-337">Tämä vaihe on pakollinen, koska sen avulla vältetään todennus- tai RSAT-yhteysvirheet.</span><span class="sxs-lookup"><span data-stu-id="ef075-337">This step is required because it helps you avoid authentication or RSAT connection errors.</span></span>

```
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a><span data-ttu-id="ef075-338">RSAT-työkalun asentaminen</span><span class="sxs-lookup"><span data-stu-id="ef075-338">Install RSAT</span></span>

1. <span data-ttu-id="ef075-339">Siirry sivustoon <https://www.microsoft.com/download/details.aspx?id=57357> ja valitse **Lataa**.</span><span class="sxs-lookup"><span data-stu-id="ef075-339">Go to <https://www.microsoft.com/download/details.aspx?id=57357>, and select **Download**.</span></span>
2. <span data-ttu-id="ef075-340">Valitse ensin kaikki tiedostot ja valitse sitten **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="ef075-340">Select all the files, and then select **Next**.</span></span>

    ![Kaikkien tiedostojen valitseminen](./media/setup_rsa_tool_51.png)

3. <span data-ttu-id="ef075-342">Suorita asennusohjelmalla kaksoisnapsauttamalla .msi-pakettia.</span><span class="sxs-lookup"><span data-stu-id="ef075-342">Double-click the .msi package to run the installer.</span></span> <span data-ttu-id="ef075-343">Valitse asennuksen valmistumisen jälkeen **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="ef075-343">Then, when the installation is completed, select **Finish**.</span></span>

    ![RSAT-asennusohjelmatiedosto](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a><span data-ttu-id="ef075-345">Seleniumin ja selainohjaimien asentaminen</span><span class="sxs-lookup"><span data-stu-id="ef075-345">Install Selenium and browser drivers</span></span>

<span data-ttu-id="ef075-346">RSAT-työkalun vanhoissa versioissa oli asennettava Selenium ja selaimen ohjaimet.</span><span class="sxs-lookup"><span data-stu-id="ef075-346">In older versions of RSAT, you had to install Selenium and browser drivers.</span></span> <span data-ttu-id="ef075-347">Näitä ohjaimia ei enää tarvitse asentaa, sillä ne asennetaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="ef075-347">You no longer have to install these drivers because they are automatically installed.</span></span>

1. <span data-ttu-id="ef075-348">Kun avaat RSAT-työkalun ensimmäisen kerran, sinulla pyydetään automaattisesti lataamaan ja asentamaan Selenium.</span><span class="sxs-lookup"><span data-stu-id="ef075-348">The first time that you open RSAT, you're prompted to automatically download and install Selenium.</span></span> <span data-ttu-id="ef075-349">Lisätietoja on osassa [RSAT-työkalun määrittäminen](#configure-rsat).</span><span class="sxs-lookup"><span data-stu-id="ef075-349">For more information, see the [Configure RSAT](#configure-rsat) section.</span></span>
2. <span data-ttu-id="ef075-350">Ennen kuin voit suorittaa testitapauksen, sinua pyydetään lataamaan ja asentamaan automaattisesti RSAT-määrityksissä valittua oletusselainta vastaava selaimen ohjain.</span><span class="sxs-lookup"><span data-stu-id="ef075-350">Before you can run a test case, you're prompted to automatically download and install the browser driver that corresponds to the default browser that is selected in the RSAT configuration.</span></span> <span data-ttu-id="ef075-351">Lisätietoja on osassa [Testitapausten lataaminen ja suorittaminen](#load-and-run-test-cases).</span><span class="sxs-lookup"><span data-stu-id="ef075-351">For more information, see the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

## <a name="get-started-with-rsat"></a><span data-ttu-id="ef075-352">RSAT-työkalun käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="ef075-352">Get started with RSAT</span></span>

### <a name="create-a-test-plan-and-test-suites"></a><span data-ttu-id="ef075-353">Testisuunnitelman ja testipakettien luominen</span><span class="sxs-lookup"><span data-stu-id="ef075-353">Create a test plan and test suites</span></span>

1. <span data-ttu-id="ef075-354">Siirry Azure DevOps -projektiin ja valitse **Testisuunnitelmat**.</span><span class="sxs-lookup"><span data-stu-id="ef075-354">Go to the Azure DevOps project, and select **Test Plans**.</span></span>

    ![Testisuunnitelmat-komento](./media/setup_rsa_tool_53.png)

2. <span data-ttu-id="ef075-356">Valitse **Uusi testisuunnitelma**.</span><span class="sxs-lookup"><span data-stu-id="ef075-356">Select **New Test Plan**.</span></span>

    ![Uusi testisuunnitelma -painike](./media/setup_rsa_tool_54.png)

3. <span data-ttu-id="ef075-358">Täytä **Nimi**-kenttä ja valitse sitten **Luo**.</span><span class="sxs-lookup"><span data-stu-id="ef075-358">Fill in the **Name** field, and then select **Create**.</span></span> <span data-ttu-id="ef075-359">Anna tässä oppaassa testisuunnitelman nimeksi **RSAT-testisuunnitelma**.</span><span class="sxs-lookup"><span data-stu-id="ef075-359">For this tutorial, name the test plan **RSAT Test Plan**.</span></span>

    ![Uusi testisuunnitelma -valintaikkuna](./media/setup_rsa_tool_55.png)

4. <span data-ttu-id="ef075-361">Luo uuteen testisuunnitelmaan staattinen sarja valitsemalla ensin plus-merkki (**+**) ja sitten **Staattinen sarja**.</span><span class="sxs-lookup"><span data-stu-id="ef075-361">Select the plus sign (**+**), and then select **Static suite** to create a static suite under the new test plan.</span></span> <span data-ttu-id="ef075-362">Annan uuden testisarjan nimeksi **T01 – Valmistus varastoon**.</span><span class="sxs-lookup"><span data-stu-id="ef075-362">Name the new test suite **T01 – Make to Stock**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef075-363">Voit luoda myös kyselypohjaisen sarjan, jos haluat, että uudet liiketoimintaprosessien mallintajan uudet testitapaukset noudetaan automaattisesti RSAT-testisarjaan.</span><span class="sxs-lookup"><span data-stu-id="ef075-363">You can also create a query-based suite, if you want the new test cases from BPM to be automatically pulled into the RSAT test suite.</span></span>

    ![Staattisen sarjan luominen](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a><span data-ttu-id="ef075-365">Testitapausten liittäminen testisarjoihin</span><span class="sxs-lookup"><span data-stu-id="ef075-365">Attach test cases to test suites</span></span>

1. <span data-ttu-id="ef075-366">Lisää aiemmin luodut testitapaukset testisaraan valitsemalla oikealla puolella **Lisää aiemmin luotu**.</span><span class="sxs-lookup"><span data-stu-id="ef075-366">Select **Add existing** on the right side to add existing test cases to the test suite.</span></span>

    ![Lisää aiemmin luotu -painike](./media/setup_rsa_tool_57.png)

2. <span data-ttu-id="ef075-368">Valitse **Lisää testitapaukset sarjaan** -sivulla **Tee kysely** ja valitse sitten testisarjaan lisättävä testitapaus.</span><span class="sxs-lookup"><span data-stu-id="ef075-368">On the **Add test cases to suite** page, select **Run query**, and then select the test case to add to the test suite.</span></span> <span data-ttu-id="ef075-369">Valitse tässä oppaassa **Luo uusi tuote** -testitapaus.</span><span class="sxs-lookup"><span data-stu-id="ef075-369">For this tutorial, select the **Create a new product** test case.</span></span> <span data-ttu-id="ef075-370">Valitse sitten **Lisää testitapauksia** sivun oikeassa alakulmassa (tämä painike ei näy seuraavassa kuvassa).</span><span class="sxs-lookup"><span data-stu-id="ef075-370">Then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Tee kysely -painike](./media/setup_rsa_tool_58.png)

    <span data-ttu-id="ef075-372">Testitapaus lisätään **T01–Valmista varastoon** -testisarjaan.</span><span class="sxs-lookup"><span data-stu-id="ef075-372">The test case is added to the **T01-Make to Stock** test suite.</span></span>

    ![Testisarjaan lisätty testitapaus](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a><span data-ttu-id="ef075-374">Konfiguroi RSAT</span><span class="sxs-lookup"><span data-stu-id="ef075-374">Configure RSAT</span></span>

1. <span data-ttu-id="ef075-375">Avaa RSAT.</span><span class="sxs-lookup"><span data-stu-id="ef075-375">Open RSAT.</span></span>

    ![RSTA-kuvake](./media/setup_rsa_tool_60.png)

2. <span data-ttu-id="ef075-377">Saat varoitussanoman, jonka mukaan Regression Suite Automation Tool tarvitsee Seleniumia. Lisäksi sinulta kysytään, haluatko ladata ja asentaa sen nyt automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="ef075-377">You receive a warning message that states, "The Regression Suite Automation Tool requires Selenium, do you want to automatically download and install it now?"</span></span> <span data-ttu-id="ef075-378">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="ef075-378">Select **Yes**.</span></span>

    ![Varoitussanoma](./media/setup_rsa_tool_61.png)

3. <span data-ttu-id="ef075-380">Valitse oikeassa yläkulmassa **Asetukset**-painike (rataskuvake) ja täytä sitten seuraavat kentät avautuvassa valintaikkunassa:</span><span class="sxs-lookup"><span data-stu-id="ef075-380">Select the **Settings** button (the gear symbol) in the upper-right corner, and then, in the dialog box that appears, fill in the following fields:</span></span>

    - <span data-ttu-id="ef075-381">**Azure DevOps -URL-osoite** – anna Azure DevOps -projektin URL-osoite, kuten `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span><span class="sxs-lookup"><span data-stu-id="ef075-381">**Azure DevOps Url** – Enter the URL of your Azure DevOps project, such as `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span></span>
    - <span data-ttu-id="ef075-382">**Käyttöoikeustunnus** – Anna käyttöoikeustunnus, jonka avulla työkalu voi muodostaa yhteyden Azure DevOpsiin.</span><span class="sxs-lookup"><span data-stu-id="ef075-382">**Access Token** – Enter the access token that lets the tool connect to Azure DevOps.</span></span> <span data-ttu-id="ef075-383">Käytä aiemmin tässä oppaassa luotua henkilökohtaista käyttöoikeustunnusta.</span><span class="sxs-lookup"><span data-stu-id="ef075-383">Use the personal access token that you created earlier in this tutorial.</span></span> <span data-ttu-id="ef075-384">Lisätietoja on kohdassa [Käytön todentaminen henkilökohtaisilla käyttöoikeustunnuksilla](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span><span class="sxs-lookup"><span data-stu-id="ef075-384">For more information, see [Authenticate access with personal access tokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span></span>
    - <span data-ttu-id="ef075-385">**Projektin nimi** – valitse Azure DevOps -projektin nimi.</span><span class="sxs-lookup"><span data-stu-id="ef075-385">**Project Name** – Select the name of your Azure DevOps project.</span></span>
    - <span data-ttu-id="ef075-386">**Testisuunnitelma** – Valitse testitapaukset sisältävä Azure DevOps -testisuunnitelma.</span><span class="sxs-lookup"><span data-stu-id="ef075-386">**Test Plan** – Select the Azure DevOps test plan that contains your test cases.</span></span> <span data-ttu-id="ef075-387">Lisätietoja on kohdassa [Testisuunnitelmien ja -sarjojen luominen](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span><span class="sxs-lookup"><span data-stu-id="ef075-387">For more information, see [Create test plans and test suites](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span></span> <span data-ttu-id="ef075-388">Kun olet valinnut testisuunnitelman, testaa Azure DevOps -yhteys valitsemalla **Testaa yhteyttä**.</span><span class="sxs-lookup"><span data-stu-id="ef075-388">After you select a test plan, select **Test Connection** to test your connection to Azure DevOps.</span></span>
    - <span data-ttu-id="ef075-389">**Isäntänimi** – Anna Finance and Operations -testiympäristön isäntänimi, kuten **\<myaos\>.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="ef075-389">**Hostname** – Enter the host name of the Finance and Operations test environment, such as **\<myaos\>.cloudax.dynamics.com**.</span></span> <span data-ttu-id="ef075-390">Älä käytä **https://**- tai **http://**-etuliitettä.</span><span class="sxs-lookup"><span data-stu-id="ef075-390">Don't include the **https://** or **http://** prefix.</span></span>
    - <span data-ttu-id="ef075-391">**SOAP-isäntänimi** – Anna Finance and Operations -testiympäristön SOAP-isäntänimi.</span><span class="sxs-lookup"><span data-stu-id="ef075-391">**SOAP Hostname** – Enter the SOAP host name of the Finance and Operations test environment.</span></span> <span data-ttu-id="ef075-392">SOAP-isäntänimi on yleensä sama kuin isäntänimi, mutta siinä on **soap**-pääte.</span><span class="sxs-lookup"><span data-stu-id="ef075-392">Typically, the SOAP host name is the same as the host name, but it has a **soap** suffix.</span></span> <span data-ttu-id="ef075-393">Esimerkki: **\<myaos\>soap.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="ef075-393">Here is an example: **\<myaos\>soap.cloudax.dynamics.com**.</span></span> <span data-ttu-id="ef075-394">Älä käytä **https://**- tai **http://**-etuliitettä.</span><span class="sxs-lookup"><span data-stu-id="ef075-394">Don't include the **https://** or **http://** prefix.</span></span>

        > [!NOTE]
        > <span data-ttu-id="ef075-395">Voit etsiä isäntänimien ja SOAP-isäntänimen avaamalla IIS-palvelun hallinnan sekä valitsemalla hiiren kakkospainikkeella ensin **Sivustot \> AOSService** ja sitten **Muokkaa sidontoja**.</span><span class="sxs-lookup"><span data-stu-id="ef075-395">To find the host name and SOAP host name, open IIS Manager, right-click **Sites \> AOSService**, and then select **Edit bindings**.</span></span> <span data-ttu-id="ef075-396">Saat isännän ja SOAP-isännän nimen **Isäntänimi**-sarakkeen arvoista. (SOAP-isännän nimessä on **soap**-pääte URL-osoitteessa.)</span><span class="sxs-lookup"><span data-stu-id="ef075-396">The values in the **Host Name** column give you the host name and SOAP host name (the SOAP host name has the suffix **soap** in the URL).</span></span>

        ![Isännän a SOAP-isännän nimi Isäntänimi-sarakkeessa](./media/setup_rsa_tool_63.png)

    - <span data-ttu-id="ef075-398">**Järjestelmänvalvojakäyttäjän nimi** – anna Finance and Operations -testiympäristön järjestelmävalvojakäyttäjän sähköpostiosoite.</span><span class="sxs-lookup"><span data-stu-id="ef075-398">**Admin user name** – Enter the email address of an admin user in the Finance and Operations test environment.</span></span>
    - <span data-ttu-id="ef075-399">**Allekirjoitus** – anna todennusvarmenteen allekirjoitus aiemmin tässä oppaassa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="ef075-399">**Thumbprint** – Enter the thumbprint of the authentication certificate, as described earlier in this tutorial.</span></span>
    - <span data-ttu-id="ef075-400">**Työhakemisto** – Määritä testin automaatiotiedostojen, kuten Excelin tietotiedostojen, tallennuskansion sijainti.</span><span class="sxs-lookup"><span data-stu-id="ef075-400">**Working directory** – Specify the folder location for storing test automation files, such as Excel test data files.</span></span> <span data-ttu-id="ef075-401">Kirjoita tai valitse esimerkiksi **C:\\Temp\\RegressionTool**.</span><span class="sxs-lookup"><span data-stu-id="ef075-401">For example, enter or select **C:\\Temp\\RegressionTool**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="ef075-402">Jos kansion nimessä on välilyöntejä, suorittaminen ei onnistu, sillä kansiota ei löydetä.</span><span class="sxs-lookup"><span data-stu-id="ef075-402">If the name of the folder has spaces, execution will fail because the folder can't be found.</span></span> <span data-ttu-id="ef075-403">Tämä on tunnettu ongelma ja sen pitäisi olla korjattu työkalun uusimmassa versiossa.</span><span class="sxs-lookup"><span data-stu-id="ef075-403">This issue is a known issue and should be fixed in the latest version of the tool.</span></span>

    - <span data-ttu-id="ef075-404">**Oletusselain** – Valitse joko **Internet Explorer** tai **Google Chrome**.</span><span class="sxs-lookup"><span data-stu-id="ef075-404">**Default browser** – Select either **Internet Explorer** or **Google Chrome**.</span></span> <span data-ttu-id="ef075-405">Varmista, että tarvittavat selainohjaimet on asennettu.</span><span class="sxs-lookup"><span data-stu-id="ef075-405">Make sure that the appropriate browser drivers have been installed.</span></span>
    - <span data-ttu-id="ef075-406">**Testiajon aikakatkaisu** – Määritä testiajojen aikakatkaisuaika minuutteina.</span><span class="sxs-lookup"><span data-stu-id="ef075-406">**Test run timeout** – Specify the time-out period, in minutes, for test runs.</span></span> <span data-ttu-id="ef075-407">Kun aikakatkaisuaika päättyy, kaikki aktiiviset ikkunat suljetaan ja odottavat testitapaukset epäonnistuvat.</span><span class="sxs-lookup"><span data-stu-id="ef075-407">When the time-out period elapses, all active windows are closed, and pending test cases fail.</span></span>
    - <span data-ttu-id="ef075-408">**Testitoiminnon aikakatkaisu** – Tämä kenttä ohjaa Finance and Operation -ympäristön palvelinpyyntöjen aikakatkaisuaikaa minuutteina.</span><span class="sxs-lookup"><span data-stu-id="ef075-408">**Test action timeout** – This field controls the time-out period, in minutes, for Finance and Operation environment server requests.</span></span> <span data-ttu-id="ef075-409">Oletusarvo (2 minuuttia) on yleensä riittävä.</span><span class="sxs-lookup"><span data-stu-id="ef075-409">Usually, the default value (2 minutes) should be enough.</span></span> <span data-ttu-id="ef075-410">Hitaissa ympäristöissä tätä arvo on kuitenkin ehkä suurennettava, jos aikakatkaisuihin liittyviä virheitä tapahtuu.</span><span class="sxs-lookup"><span data-stu-id="ef075-410">However, for slower environments, you might want to increase the value if errors that are related to time-outs occur.</span></span>
    - <span data-ttu-id="ef075-411">**Yrityksen nimi** – Anna sen yrityksen nimi, jota käytetään Finance and Operationsin oletusyrityksenä Excelin parametritiedostoja luotaessa.</span><span class="sxs-lookup"><span data-stu-id="ef075-411">**Company name** – Enter the company name to use as your default Finance and Operations company when Excel parameter files are created.</span></span> <span data-ttu-id="ef075-412">Voit muuttaa yritystä myöhemmin muokkaamalla Excelin parametritiedostoa.</span><span class="sxs-lookup"><span data-stu-id="ef075-412">You can change the company later by editing the Excel parameter file.</span></span>

    ![Asetukset-valintaikkuna](./media/setup_rsa_tool_62.png)

4. <span data-ttu-id="ef075-414">Ota asetukset käyttöön ja tallenna ne valitsemalla **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="ef075-414">Select **Apply** to apply and save your settings.</span></span>

    <span data-ttu-id="ef075-415">Voit tallentaa nykyiset asetukset määritystiedostoon omassa tietokoneessa valitsemalla **Tallenna nimellä**.</span><span class="sxs-lookup"><span data-stu-id="ef075-415">To save your current settings to a configuration file on your computer, select **Save as**.</span></span> <span data-ttu-id="ef075-416">Voit palauttaa asetukset omassa tietokoneessa olevasta määritystiedostosta valitsemalla **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="ef075-416">To restore your settings from a configuration file on your computer, select **Open**.</span></span>

5. <span data-ttu-id="ef075-417">Sulje valintaikkuna valitsemalla **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="ef075-417">Select **Close** to close the dialog box.</span></span>

### <a name="load-and-run-test-cases"></a><span data-ttu-id="ef075-418">Testitapausten lataaminen ja suorittaminen</span><span class="sxs-lookup"><span data-stu-id="ef075-418">Load and run test cases</span></span>

1. <span data-ttu-id="ef075-419">Lataa **RSAT-testisuunnitelma** Azure DevOps-projektista valitsemalla **Lataa**.</span><span class="sxs-lookup"><span data-stu-id="ef075-419">Select **Load** to load the **RSAT Test Plan** test plan from the Azure DevOps project.</span></span>

    ![Lataa-painike](./media/setup_rsa_tool_64.png)

2. <span data-ttu-id="ef075-421">Valitse testisarjasta **Luo uusi tuote** -testitapaus ja valitse sitten **Uusi \> Luo testin suoritus- ja parametritiedostot**.</span><span class="sxs-lookup"><span data-stu-id="ef075-421">Select the **Create a new product** test case from the test suite, and then select **New \> Generate Test Execution and Parameter files**.</span></span>

    ![Uusi-valikon Luo testin suoritus -ja parametritiedostot -komento](./media/setup_rsa_tool_65.png)

    <span data-ttu-id="ef075-423">Excelin parametritiedostot luodaan RSAT-määrityksissä määritetyssä paikallisessa kansiossa (kuten **C:\\Temp\\RegressionTool**).</span><span class="sxs-lookup"><span data-stu-id="ef075-423">The Excel parameter file is created in the local folder that you specified in the RSAT configuration (for example, **C:\\Temp\\RegressionTool**).</span></span>

    ![Luotu Excelin parametritiedosto](./media/setup_rsa_tool_66.png)

3. <span data-ttu-id="ef075-425">Jos haluat tallentaa parametritiedostot, valitse **Lataa palvelimeen**.</span><span class="sxs-lookup"><span data-stu-id="ef075-425">If you want to save the parameter files, select **Upload**.</span></span> <span data-ttu-id="ef075-426">Valittujen testitapausten testin automaatiotiedostot ladataan Azure DevOpsiin tulevaa käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="ef075-426">Test automation files of all selected test cases are uploaded to Azure DevOps for future use.</span></span> <span data-ttu-id="ef075-427">(Nämä tiedostot sisältävät Excelin testiparametritiedostot.)</span><span class="sxs-lookup"><span data-stu-id="ef075-427">(These files include Excel test parameter files.)</span></span>

    <span data-ttu-id="ef075-428">Tällä tavoin ladata testitapauksen parametritiedostot (ja automaatiotiedostot) suoraan Azure DevOpsista valitsemalla **Lataa**.</span><span class="sxs-lookup"><span data-stu-id="ef075-428">In this way, you can select **Load** to load the parameter files (and automation files) from the test case directly from Azure DevOps.</span></span> <span data-ttu-id="ef075-429">Parametritiedostoja ei siis tarvitse luoda uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ef075-429">You don't have to regenerate the parameter files.</span></span> <span data-ttu-id="ef075-430">Tämä menettelytapa osoittautuu tärkeäksi myöhemmin, kun haluat säilyttää parametritiedoston muokkaukset etkä halua, että ne korvataan.</span><span class="sxs-lookup"><span data-stu-id="ef075-430">This approach will become important later, when you want to keep the modifications in the parameter file and don't want them to be overwritten.</span></span>

4. <span data-ttu-id="ef075-431">Voit tarkistaa, että automaatio- ja parametritiedostot on tallennettu Azure DevOpsiin, siirtymällä Azure DevOps -projektiin, valitsemalla **Taulut \> Työnimikkeet** ja valitsemalla lopuksi **Luo uusi tuote** -testitapauksen.</span><span class="sxs-lookup"><span data-stu-id="ef075-431">To verify that the automation files and parameter files are saved to Azure DevOps, go to the Azure DevOps project, select **Boards \> Work Items**, and select the **Create a new product** test case.</span></span> <span data-ttu-id="ef075-432">**Liitteet**-välilehdessä pitäisi olla neljä tiedostoa:</span><span class="sxs-lookup"><span data-stu-id="ef075-432">On the **Attachments** tab, you should see four files:</span></span>

    - <span data-ttu-id="ef075-433">**.cs** – C\#-automaatiotiedosto</span><span class="sxs-lookup"><span data-stu-id="ef075-433">**.cs** – C\# automation file</span></span>
    - <span data-ttu-id="ef075-434">**.dll** – käännetty automaatiotiedosto koottuna</span><span class="sxs-lookup"><span data-stu-id="ef075-434">**.dll** – Compiled automation file as an assembly</span></span>
    - <span data-ttu-id="ef075-435">**.xlsx** – Excelin parametritiedosto</span><span class="sxs-lookup"><span data-stu-id="ef075-435">**.xlsx** – Excel parameter file</span></span>
    - <span data-ttu-id="ef075-436">**.xml** – tallennetiedosto</span><span class="sxs-lookup"><span data-stu-id="ef075-436">**.xml** – Recording file</span></span>

    ![Liitteet-välilehden tiedostot](./media/setup_rsa_tool_67.png)

5. <span data-ttu-id="ef075-438">Valitse ensin suoritettava testitapaus ja sitten **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="ef075-438">Select the test case to run, and then select **Run**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef075-439">Jos käytät selaimena Internet Exploreria, varmista ennen testitapausten suorittamista, että työpöydän tarkkuudeksi on valittu **100 %**. Voit tehdä tämän valitsemalla **Windowsin näyttöasetukset\> Skaalaus ja asettelu**.</span><span class="sxs-lookup"><span data-stu-id="ef075-439">Before you run test cases, if you're using Internet Explorer as the browser, make sure that your desktop resolution is set to **100%** at **Windows Display settings \> Scale and layout**.</span></span> <span data-ttu-id="ef075-440">Jos voi muuttaa tätä asetusta virtuaalikoneessa (VM), muuta se siinä asiakasohjelmassa (kannettava), josta yrität käyttää virtuaalikonetta.</span><span class="sxs-lookup"><span data-stu-id="ef075-440">If you can't change this setting on a virtual machine (VM), change it on the client (laptop) that you're trying to access the VM from.</span></span> <span data-ttu-id="ef075-441">Virtuaalikoneen näyttöasetukset perivät sitten tarkkuusasetukset.</span><span class="sxs-lookup"><span data-stu-id="ef075-441">The resolution settings will then be inherited by the VM display settings.</span></span>

    ![Työpöydän tarkkuudeksi on määritetty 100 %](./media/setup_rsa_tool_68.png)

6. <span data-ttu-id="ef075-443">Jos selainohjaimia ei ole asennettu järjestelmään, näyttöön avautuva varoitussanoma ilmoittaa, että toiminto edellyttää selaimen \<selaimen nimi\> ohjainta ja kysyy</span><span class="sxs-lookup"><span data-stu-id="ef075-443">If the browser drivers aren't installed in the system, you receive a warning message that states, "This operation requires the \<browser name\> driver.</span></span> <span data-ttu-id="ef075-444">haluatko ladata ja asentaa sen nyt automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="ef075-444">Do you want to automatically downloads and install it now?"</span></span> <span data-ttu-id="ef075-445">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="ef075-445">Select **Yes**.</span></span>

    ![Internet Explorerin varoitussanoma](./media/setup_rsa_tool_69.png)

    ![Chromen varoitussanoma](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > <span data-ttu-id="ef075-448">Jos selaimena Chrome selaimena ja avautuva virhesanoma ilmoittaa, että istuntoa ei luotu virheellinen Chrome-version vuoksi, lataa uusin Chrome-ohjain osoitteesta <http://chromedriver.chromium.org/downloads> kansioon **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium**.</span><span class="sxs-lookup"><span data-stu-id="ef075-448">If you're using Chrome as the browser and receive an error message that states that the session wasn't created because the Chrome version isn't correct, download the latest Chrome driver from <http://chromedriver.chromium.org/downloads> to the **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** folder.</span></span>

    ![Chromen virhesanoma](./media/setup_rsa_tool_71.png)

    <span data-ttu-id="ef075-450">Testitapaus suoritetaan ja **Tulos**-kenttä päivitetään.</span><span class="sxs-lookup"><span data-stu-id="ef075-450">The test case is run, and the **Result** field is updated.</span></span>

    ![Tilanneilmaisin](./media/setup_rsa_tool_72.png)

    <span data-ttu-id="ef075-452">Jos olet toiminut oppaan ohjeiden mukaisesti, **Luo uusi tuote** -testitapaus epäonnistuu, koska tuotteen luonnin tehtävätallenne tallensi tuotenimen pysyväiskoodattuna arvona.</span><span class="sxs-lookup"><span data-stu-id="ef075-452">If you've followed this tutorial as it's written, the **Create a new product** test case will fail, because the task recording for creating a product saved the product name as a hard-coded value.</span></span> <span data-ttu-id="ef075-453">Jos suoritat saman testitapauksen uudelleen, näyttöön pitäisi tulla virhesanoma, koska tuote on luotu jo aiemmin.</span><span class="sxs-lookup"><span data-stu-id="ef075-453">If you rerun the same test case, you should receive an error message, because the product already exists.</span></span>

    ![Tulos-kentän asetukseksi on määritetty Epäonnistui](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a><span data-ttu-id="ef075-455">Testitulosten näyttäminen</span><span class="sxs-lookup"><span data-stu-id="ef075-455">View the test results</span></span>

1. <span data-ttu-id="ef075-456">Kaksoisnapsauta epäonnistunutta testitapausta.</span><span class="sxs-lookup"><span data-stu-id="ef075-456">Double-click the failed test case.</span></span>

    <span data-ttu-id="ef075-457">Näyttöön avautuu virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="ef075-457">You receive an error message.</span></span>

    ![Virhesanoma](./media/setup_rsa_tool_73.png)

2. <span data-ttu-id="ef075-459">Voit näyttää koko virhesanoman valitsemalla **Tiedot**.</span><span class="sxs-lookup"><span data-stu-id="ef075-459">Select **Details** to view the whole error message.</span></span>

    ![Koko virhesanoma](./media/setup_rsa_tool_74.png)

3. <span data-ttu-id="ef075-461">Voit näyttää virhesanoman yksityiskohtaisen version Azure DevOpsissa valitsemalla **Avaa Azure DevOpsissa**.</span><span class="sxs-lookup"><span data-stu-id="ef075-461">To view a detailed version of the error message in Azure DevOps, select **Open in Azure DevOps**.</span></span> <span data-ttu-id="ef075-462">Voit näyttää testitapauksen tilan ja yksityiskohtaisen virhesanoman Azure DevOpsissa.</span><span class="sxs-lookup"><span data-stu-id="ef075-462">In Azure DevOps, you can view the status of the test case and the detailed error message.</span></span>

    ![Yksityiskohtainen virhesanoma Azure DevOpsissa](./media/setup_rsa_tool_75.png)

4. <span data-ttu-id="ef075-464">Voit näyttää testitulokset suoraan Azure DevOps -projektissa valitsemalla **Testisuunnitelmat \> Testisuunnitelmat \> Ajot**.</span><span class="sxs-lookup"><span data-stu-id="ef075-464">To view the test results directly in the Azure DevOps project, go to **Test Plans \> Test Plans \> Runs**.</span></span> <span data-ttu-id="ef075-465">Kaksoisnapsauta sitä testiajoa, jonka tiedot haluat nähdä.</span><span class="sxs-lookup"><span data-stu-id="ef075-465">Double-click the test run that you want to see more details for.</span></span>

    ![Testiajoluettelo Azure DevOpsissa](./media/setup_rsa_tool_76.png)

5. <span data-ttu-id="ef075-467">**Suorita yhteenveto** -välilehti ilmaisee, että testitapaus epäonnistui. Varsinainen virhesanoma ei kuitenkaan ole saatavana.</span><span class="sxs-lookup"><span data-stu-id="ef075-467">The **Run summary** tab indicates that the test case failed, but it doesn't provide the actual error message.</span></span> <span data-ttu-id="ef075-468">Voit näyttää virhesanoman tarkat tiedot valitsemalla **Testin tulokset** -välilehden.</span><span class="sxs-lookup"><span data-stu-id="ef075-468">To view the detailed error message, select the **Test results** tab.</span></span>

    ![Suorita yhteenveto -välilehti](./media/setup_rsa_tool_77.png)

    <span data-ttu-id="ef075-470">**Testin tulokset** -välilehdessä on testitapauksen tiedot sekä tulos ja virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="ef075-470">The **Test results** tab provides the test case information, together with the outcome and the error message.</span></span>

    ![Testin tulokset -välilehti](./media/setup_rsa_tool_78.png)

6. <span data-ttu-id="ef075-472">Voit näyttää yksityiskohtaisen virhesanoman kaksoisnapsauttamalla kyseistä tietuetta.</span><span class="sxs-lookup"><span data-stu-id="ef075-472">Double-click the relevant record to view the detailed error message.</span></span>

    ![Yksityiskohtainen virhesanoma](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > <span data-ttu-id="ef075-474">Kaikki virhesanomat ovat saatavana myös paikallisesti kansiossa **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span><span class="sxs-lookup"><span data-stu-id="ef075-474">All error messages are also available locally in **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span></span>

7. <span data-ttu-id="ef075-475">Voit myös viedä testiajon tulokset testisuunnitelmatasolta valitsemalla **Vie**.</span><span class="sxs-lookup"><span data-stu-id="ef075-475">You can also export the test run results from the test plan level by selecting **Export**.</span></span>

    ![Testisuunnitelman vieminen](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a><span data-ttu-id="ef075-477">Excelin parametritiedoston muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="ef075-477">Modify the Excel parameter file</span></span>

1. <span data-ttu-id="ef075-478">Avaa RSAT.</span><span class="sxs-lookup"><span data-stu-id="ef075-478">Open RSAT.</span></span>
2. <span data-ttu-id="ef075-479">Valitse ensin testitapaus ja avaa sitten Excelin parametritiedosto valitsemalla **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="ef075-479">Select the test case, and then select **Edit** to open the Excel parameter file.</span></span>

    <span data-ttu-id="ef075-480">Huomaa, että **EcoResProductCreate**-taulukon **Tuotenumero**-kentän arvo on pysyväiskoodattu.</span><span class="sxs-lookup"><span data-stu-id="ef075-480">On the **EcoResProductCreate** sheet, notice that the value of the **Product number** field is hard-coded.</span></span> <span data-ttu-id="ef075-481">Tähän kenttään on päivitettävä uusi tuotenumero ennen testitapauksen suorittamista uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ef075-481">You must update this field to a new product number before you run the test case again.</span></span>

3. <span data-ttu-id="ef075-482">Käyttämällä seuraavaa Excel-kaavaa voit luoda yksilöivän tuotenumeron jokaiselle ajolle ilman Excelin parametritiedoston avaamista ja tuotenumeron manuaalista päivittämistä joka kerta erikseen.</span><span class="sxs-lookup"><span data-stu-id="ef075-482">To generate a unique product number for each run without having to reopen the Excel parameter file and manually update the product number every time, use the following Excel formula.</span></span>

    ```
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > <span data-ttu-id="ef075-483">**Yleiset**-välilehden lisäksi Excelin parametritiedostossa on tietovälilehti jokaiselle Finance and Operations -lomakesivulle, jota testitapaus käyttää.</span><span class="sxs-lookup"><span data-stu-id="ef075-483">In addition to the **General** tab, the Excel parameter file contains a data tab for every Finance and Operations form page the test case visits.</span></span>

    ![Tuotenumero-kenttä](./media/setup_rsa_tool_81.png)

4. <span data-ttu-id="ef075-485">Valitse **Tallenna** ja sulje sitten Excel-työkirja.</span><span class="sxs-lookup"><span data-stu-id="ef075-485">Select **Save**, and then close the Excel workbook.</span></span>
5. <span data-ttu-id="ef075-486">Tallenna Excelin parametritiedosto Azure DevOpsiin valitsemalla **Lataa palvelimeen**.</span><span class="sxs-lookup"><span data-stu-id="ef075-486">Select **Upload** to save the Excel parameter file to Azure DevOps.</span></span>

    ![Sanoma onnistuneesta latauksesta](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > <span data-ttu-id="ef075-488">Jos haluat suorittaa testitapaukset tietyssä käyttäjäkontekstissa, anna käyttäjän sähköpostitunnus Excelin parametritiedoston **Yleiset**-välilehden **Testikäyttäjä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ef075-488">To run test cases in a specific user context, enter the user's email ID in the **Test User** field on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="ef075-489">Excelin parametritiedoston kenttien asettelu on päivitetty uusimmassa RSAT-versiossa, perusidea on edelleen sama.</span><span class="sxs-lookup"><span data-stu-id="ef075-489">In the latest version of RSAT, the layout of the fields in the Excel parameter file has been updated, but the concept remains the same.</span></span>
    >
    > ![Testikäyttäjä-kenttä](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a><span data-ttu-id="ef075-491">Tulosten tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="ef075-491">Validate the results</span></span>

- <span data-ttu-id="ef075-492">Suorita testitapaus uudelleen valitsemalla **Suorita** ja tarkista, että testitapaus on suoritettu hyväksytysti.</span><span class="sxs-lookup"><span data-stu-id="ef075-492">Select **Run** to rerun the test case, and verify that the test case has passed.</span></span> <span data-ttu-id="ef075-493">Voit näyttää testitulokset osassa [Testitulosten näyttäminen](#view-the-test-results) kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="ef075-493">You can view the test results as described in the [View the test results](#view-the-test-results) section.</span></span>

    ![Tulos-kentän asetukseksi on määritetty Hyväksytty](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a><span data-ttu-id="ef075-495">Testitapausten ketjuttaminen</span><span class="sxs-lookup"><span data-stu-id="ef075-495">Chaining of test cases</span></span>

<span data-ttu-id="ef075-496">Yksi RSAT-työkalun keskeisistä ominaisuuksista on testitapausten ketjuttaminen (jolloin testi voi siirtää arvot toisiin testeihin).</span><span class="sxs-lookup"><span data-stu-id="ef075-496">One key feature of RSAT is the chaining of test cases (that is, the capability of a test to pass values to other tests).</span></span> <span data-ttu-id="ef075-497">Testitapaukset suoritetaan Azure DevOps -testisuunnitelmassa määritetyssä järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="ef075-497">Test cases are run according to their defined order in the Azure DevOps test plan.</span></span> <span data-ttu-id="ef075-498">(Tämä järjestys voidaan päivittää myös itse testityökalussa.) Niinpä jos haluat välittää muuttujia testitapauksesta toiseen, on erittäin tärkeää, että testit ovat oikeassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="ef075-498">(This order can also be updated in the test tool itself.) Therefore, if you want to pass variables from one test case to another, it's very important that the tests be in the correct order.</span></span>

<span data-ttu-id="ef075-499">Tässä osassa luodaan tallennettu muuttuja ensimmäisessä testitapauksessa, sen jälkeen luodaan toinen testitapaus ja ensimmäisen testitapauksen tallennettu muuttuja välitetään toiseen testitapaukseen.</span><span class="sxs-lookup"><span data-stu-id="ef075-499">In this section, you will create a saved variable in the first test case, create a second test case, and pass the saved variable from the first test case to the second test case.</span></span> <span data-ttu-id="ef075-500">Sen jälkeen testitapaukset suoritetaan ketjutettuna testitapauksena RSAT-työkalussa.</span><span class="sxs-lookup"><span data-stu-id="ef075-500">You will then run the test cases as a chained test case in RSAT.</span></span>

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a><span data-ttu-id="ef075-501">Tallennetun muuttujan luominen muokkaamalla aiemmin luotua tehtävätallennetta</span><span class="sxs-lookup"><span data-stu-id="ef075-501">Modify an existing task recording to create a saved variable</span></span>

1. <span data-ttu-id="ef075-502">Avaa Finance and Operations -asiakasohjelma.</span><span class="sxs-lookup"><span data-stu-id="ef075-502">Open the Finance and Operations client.</span></span>
2. <span data-ttu-id="ef075-503">Valitse ensin **Asetukset**-painike (rataskuvake) ja sitten **Tehtävän tallennustoiminto**.</span><span class="sxs-lookup"><span data-stu-id="ef075-503">Select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>
3. <span data-ttu-id="ef075-504">Valitse **Muokkaa tallennetta**.</span><span class="sxs-lookup"><span data-stu-id="ef075-504">Select **Edit Recording**.</span></span>

    ![Muokkaa tallennetta -painike](./media/setup_rsa_tool_85.png)

4. <span data-ttu-id="ef075-506">Valitse **Avaa Lifecycle Services -palveluista**.</span><span class="sxs-lookup"><span data-stu-id="ef075-506">Select **Open from Lifecycle Services**.</span></span>

    ![Avaa Lifecycle Services -palveluista -painike](./media/setup_rsa_tool_86.png)

5. <span data-ttu-id="ef075-508">Valitse **Valitse Lifecycle Services -kirjasto**.</span><span class="sxs-lookup"><span data-stu-id="ef075-508">Select **Select the Lifecycle Services library**.</span></span>

    ![Valitse Lifecycle Services -kirjasto -painike](./media/setup_rsa_tool_87.png)

    <span data-ttu-id="ef075-510">BPM-kirjastot ladataan LCS:tä.</span><span class="sxs-lookup"><span data-stu-id="ef075-510">BPM libraries are loaded from LCS.</span></span>

    ![Tilanneilmaisin](./media/setup_rsa_tool_88.png)

6. <span data-ttu-id="ef075-512">Kun BPM-kirjastot on ladattu LCS:stä, valitse **RSAT**-BPM-kirjasto ja **Luo uusi tuote** -liiketoimintaprosessi, johon tehtävätallenne on liitetty.</span><span class="sxs-lookup"><span data-stu-id="ef075-512">After the BPM libraries are loaded from LCS, select the **RSAT** BPM library and the **Create a new product** business process that the task recording was associated with.</span></span> <span data-ttu-id="ef075-513">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef075-513">Then select **OK**.</span></span>

    ![BPM-kirjaston ja liiketoimintaprosessin valitseminen](./media/setup_rsa_tool_89.png)

7. <span data-ttu-id="ef075-515">Sopivan tehtävätallenteen nimi annetaan **Tallenteen nimi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="ef075-515">The name of the appropriate task recording is entered in the **Recording name** field.</span></span> <span data-ttu-id="ef075-516">Valitse **Aloita**.</span><span class="sxs-lookup"><span data-stu-id="ef075-516">Select **Start**.</span></span>

    ![Tehtävätallenteen nimi Tallenteen nimi -kentässä](./media/setup_rsa_tool_90.png)

8. <span data-ttu-id="ef075-518">Avaa sivu, jossa alkuperäinen tehtävätallenne, **Luo tuote**, tallennettiin valitsemalla ensin **Tuotetietojen hallinta \> Tuotteet** ja sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ef075-518">Go to **Product information management \> Products**, and select **New** to open the page where the original task recording, **Create a product**, was recorded.</span></span>
9. <span data-ttu-id="ef075-519">Valitse **Lisää vaihe**.</span><span class="sxs-lookup"><span data-stu-id="ef075-519">Select **Insert step**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef075-520">Uusi vaihe lisätään ruudussa valitun vaiheen **jälkeen**.</span><span class="sxs-lookup"><span data-stu-id="ef075-520">The new step is inserted **after** the step that you selected in the pane.</span></span>

    ![Lisää vaihe -painike](./media/setup_rsa_tool_91.png)

10. <span data-ttu-id="ef075-522">Napsauta hiiren kakkospainikkeella **Tuotenumero**-kenttää ja valitse sitten **Tehtävän tallennustoiminto \> Kopioi**.</span><span class="sxs-lookup"><span data-stu-id="ef075-522">Right-click the **Product number** field, and then select **Task recorder \> Copy**.</span></span>

    ![Kopioi-komento](./media/setup_rsa_tool_92.png)

11. <span data-ttu-id="ef075-524">Uusi vaihe on lisätty ruutuun.</span><span class="sxs-lookup"><span data-stu-id="ef075-524">A new step is added in the pane.</span></span> <span data-ttu-id="ef075-525">Kirjaa **Tuotenumero**-kentän arvo muistiin, sillä tarvitset sitä myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="ef075-525">Make a note of the value in the **Product number** field, because you will need it later.</span></span>

    ![Uusi vaihe lisätty](./media/setup_rsa_tool_93.png)

12. <span data-ttu-id="ef075-527">Valitse **Muokkaus valmis**.</span><span class="sxs-lookup"><span data-stu-id="ef075-527">Select **Done editing**.</span></span>
13. <span data-ttu-id="ef075-528">Valitse **Tallenna Lifecycle Servicesiin** ja liitä uusi tehtävätallenne samaan BPM-kirjastoon ja liiketoimintaprosessiin, johon alkuperäinen tehtävätallenne on liitetty.</span><span class="sxs-lookup"><span data-stu-id="ef075-528">Select **Save to Lifecycle Services**, and associate the new task recording with the same BPM library and business process that the original task recording was associated with.</span></span> <span data-ttu-id="ef075-529">Lisätietoja on osassa [Tehtävätallenteen luominen ja tallentaminen BPM-kirjastoon](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="ef075-529">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>
14. <span data-ttu-id="ef075-530">Siirtymällä BPM-kirjastoon ja valitsemalla **Synkronoi testitapaukset** voit korvata testitapaukseen Azure DevOpsissa liitetyn tehtävätallenteen osassa [Liiketoimintaprosessien mallintajasta Azure DevOpsiin tapahtuvan synkronoinnin testaaminen](#test-the-synchronization-from-bpm-to-azure-devops) kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="ef075-530">Go to the BPM library, and select **Sync testcases** to overwrite the task recording that is attached to the test case in Azure DevOps, as described in the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>
15. <span data-ttu-id="ef075-531">Avaa RSAT ja lataa kaikki testisarjan testitapaukset uudelleen valitsemalla **Lataa**.</span><span class="sxs-lookup"><span data-stu-id="ef075-531">Open RSAT, and select **Load** to reload all the test cases in the test suite.</span></span> <span data-ttu-id="ef075-532">Sopivan testitapauksen automaatio- ja parametritiedostot on luotava uudelleen valitsemalla ensin testitapaus ja sitten **Uusi \> Luo testin suoritus -ja parametritiedostot** osassa [Testitapausten lataaminen ja suorittaminen](#load-and-run-test-cases) kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="ef075-532">You must regenerate the automation and parameter files for the appropriate test case by selecting the test case and then selecting **New \> Generate Test Execution and Parameter files**, as described in the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef075-533">Jos Excelin parametritiedosto on jätetty auki, uudelleenluonti epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="ef075-533">If the Excel parameter file was left open, regeneration will fail.</span></span> <span data-ttu-id="ef075-534">Varmista tämän vuoksi, että testitapauksen Excelin parametritiedosto on suljettu, ennen kuin luot uuden Excelin parametritiedoston.</span><span class="sxs-lookup"><span data-stu-id="ef075-534">Therefore, make sure that the Excel parameter file for the test case is closed before you generate the new Excel parameter file.</span></span>

16. <span data-ttu-id="ef075-535">Avaa uusi Excelin parametritiedosto valitsemalla **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="ef075-535">Select **Edit** to open the new Excel parameter file.</span></span> <span data-ttu-id="ef075-536">Uusi **Tallennettu muuttuja** -merkintä näkyy rivillä 9.</span><span class="sxs-lookup"><span data-stu-id="ef075-536">You will see a new **Saved variable** entry on line 9.</span></span> <span data-ttu-id="ef075-537">Tämä muuttuja, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, tallennetaan tehtävätallenteen XML-tiedostoon, ja sitä voidaan käyttää seuraavissa testeissä.</span><span class="sxs-lookup"><span data-stu-id="ef075-537">This variable, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, is saved in the task recording's XML file and can be used in subsequent tests.</span></span>

    ![Tallennettu muuttuja -merkintä](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a><span data-ttu-id="ef075-539">Uuden testitapauksen luominen</span><span class="sxs-lookup"><span data-stu-id="ef075-539">Create a new test case</span></span>

1. <span data-ttu-id="ef075-540">Siirry **RSAT**-BPM-kirjastoon.</span><span class="sxs-lookup"><span data-stu-id="ef075-540">Go to the **RSAT** BPM library.</span></span>
2. <span data-ttu-id="ef075-541">Valitse **Tuen liiketoimintaprosessin malli** -prosessi ja valitse sitten oikealla **Muokkaustila**.</span><span class="sxs-lookup"><span data-stu-id="ef075-541">Select the **Sample Support Business Process** process, and then, on the right, select **Edit mode**.</span></span>
3. <span data-ttu-id="ef075-542">Vaihda sekä **Nimi**- että **Kuvaus**-kentän nimeksi **Vapauta tuote**.</span><span class="sxs-lookup"><span data-stu-id="ef075-542">Change the value of both the **Name** field and the **Description** field to **Release a product**.</span></span> <span data-ttu-id="ef075-543">Valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ef075-543">Then select **Save**.</span></span>

    ![Nimeksi ja kuvaukseksi on muutettu Vapauta tuote](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a><span data-ttu-id="ef075-545">Uuden tarkistustoiminnon sisältävän tehtävätallenteen luominen</span><span class="sxs-lookup"><span data-stu-id="ef075-545">Create a new task recording that has a Validate function</span></span>

- <span data-ttu-id="ef075-546">Luo tehtävätallenne, jolla vapautetaan aiemmin luotu tuote USRT-yritykseen.</span><span class="sxs-lookup"><span data-stu-id="ef075-546">Create a task recording to release the product that was created earlier to the USRT legal entity.</span></span> <span data-ttu-id="ef075-547">Lisätietoja on osassa [Tehtävätallenteen luominen ja tallentaminen BPM-kirjastoon](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="ef075-547">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef075-548">Ketjutettujen testitapausten osalta suositellaan aina, että tarvittava tallenne etsitään tai suodatetaan *kirjoittamalla kentän arvo manuaalisesti kenttään*.</span><span class="sxs-lookup"><span data-stu-id="ef075-548">For chained test cases, we always recommend that you find or filter for the record that you require by *manually typing the value of the field*.</span></span> <span data-ttu-id="ef075-549">Työkalu määrittää tällä tavoin tallenteen, jossa toiminto tehdään seuraavassa testitapauksessa.</span><span class="sxs-lookup"><span data-stu-id="ef075-549">In that way, the tool can determine the record that the action must be taken against in the subsequent test case.</span></span>

    ![Tarkistustoiminnon sisältävä uusi tehtävätallenne](./media/setup_rsa_tool_96.png)

    <span data-ttu-id="ef075-551">Edellinen kuva osoitti, miten sen jälkeen, kun tuote on löydetty pikasuodattimella mutta ennen **Vapauta tuotteet** -vaihtoehdon valitsemista, **Tuotenumero**-kentän arvo tarkistetaan. Tällä tavoin voidaan varmistaa, että tuotenumero on aiemmin luotu tuotenumero.</span><span class="sxs-lookup"><span data-stu-id="ef075-551">As the preceding illustration shows, after the product is found by using the Quick Filter, but before you select **Release products**, you validate the value of the **Product number** field to make sure that the product ID is the product ID that was created earlier.</span></span> <span data-ttu-id="ef075-552">Voit tarkistaa arvon napsauttamalla hiiren kakkospainikkeella **Tuotenumero**-kenttää ja valitsemalla sitten **Tehtävän tallennustoiminto \> Tarkista \> Nykyinen arvo**.</span><span class="sxs-lookup"><span data-stu-id="ef075-552">To validate the value, right-click the **Product number** field, and then select **Task recorder \> Validate \> Current Value**.</span></span>

    ![Nykyisen arvon tarkistaminen](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a><span data-ttu-id="ef075-554">Tehtävätallenteen tallentaminen liiketoimintaprosessien mallintajaan</span><span class="sxs-lookup"><span data-stu-id="ef075-554">Save the task recording to BPM</span></span>

1. <span data-ttu-id="ef075-555">Kun tehtävätallenne on valmis, valitse **Tallenna Lifecycle Servicesiin**.</span><span class="sxs-lookup"><span data-stu-id="ef075-555">After the task recording is completed, select **Save to Lifecycle Services**.</span></span>

    ![Tallennusasetukset](./media/setup_rsa_tool_98.png)

2. <span data-ttu-id="ef075-557">Kirjaston tiedot ladataan LCS:stä.</span><span class="sxs-lookup"><span data-stu-id="ef075-557">Library information is loaded from LCS.</span></span>

    ![Tilanneilmaisin](./media/setup_rsa_tool_99.png)

3. <span data-ttu-id="ef075-559">Valitse tehtävätallenteeseen liitettävä BPM-kirjasto.</span><span class="sxs-lookup"><span data-stu-id="ef075-559">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="ef075-560">Tässä oppaassa valitaan aiemmin luotu **RSAT**-BPM-kirjasto ja siinä oleva **Vapauta tuote** -liiketoimintaprosessi.</span><span class="sxs-lookup"><span data-stu-id="ef075-560">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Release a product** business process under it.</span></span> <span data-ttu-id="ef075-561">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef075-561">Then select **OK**.</span></span>

#### <a name="sync-bpm-to-azure-devops"></a><span data-ttu-id="ef075-562">Liiketoimintaprosessien synkronointi Azure DevOpsiin</span><span class="sxs-lookup"><span data-stu-id="ef075-562">Sync BPM to Azure DevOps</span></span>

1. <span data-ttu-id="ef075-563">Siirry BPM-kirjastoon ja avaa **RSAT**-kirjasto.</span><span class="sxs-lookup"><span data-stu-id="ef075-563">Go to the BPM library, and open the **RSAT** library.</span></span>
2. <span data-ttu-id="ef075-564">Valitse ensin **VSTS-synkronointi** ja sitten **Synkronoi testitapaukset**.</span><span class="sxs-lookup"><span data-stu-id="ef075-564">Select **VSTS sync** and then **Sync test cases**.</span></span> <span data-ttu-id="ef075-565">Lisätietoja on osassa [Liiketoimintaprosessien mallintajasta Azure DevOpsiin tapahtuvan synkronoinnin testaaminen](#test-the-synchronization-from-bpm-to-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="ef075-565">For more information, see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>

    <span data-ttu-id="ef075-566">Kun synkronointi on valmis, uusi työnimike ja vastaava **Vapauta tuote** -liiketoimintaprosessin testitapaus näkyvät Azure DevOpsissa kohdassa **Taulut \> Työnimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="ef075-566">After the synchronization is completed, the new work item and the corresponding test case for the **Release a product** business process appear in Azure DevOps at **Boards \> Work Items**.</span></span>

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a><span data-ttu-id="ef075-567">Uuden testitapauksen lisääminen aiemmin luotuun testisarjaan</span><span class="sxs-lookup"><span data-stu-id="ef075-567">Add the new test case to the existing test suite</span></span>

1. <span data-ttu-id="ef075-568">Valitse ensin **Testisuunnitelmat \> Testisuunnitelmat** ja sitten **RSAT-testisuunnitelma**.</span><span class="sxs-lookup"><span data-stu-id="ef075-568">Go to **Test plans \> Test plans**, and select the **RSAT Test Plan** plan.</span></span>
2. <span data-ttu-id="ef075-569">Valitse **Lisää aiemmin luotu**.</span><span class="sxs-lookup"><span data-stu-id="ef075-569">Select **Add existing**.</span></span>
3. <span data-ttu-id="ef075-570">Valitse **Lisää testitapaukset sarjaan** -sivulla **Suorita kysely**.</span><span class="sxs-lookup"><span data-stu-id="ef075-570">On the **Add test cases to suite** page, select **Run query**.</span></span>
4. <span data-ttu-id="ef075-571">Valitse uusi **Vapauta tuote** -prosessia varten luotu testitapaus. Valitse sitten sivun oikeassa alakulmassa **Lisää testitapaukset** (tämä painike ei näy seuraavassa kuvassa).</span><span class="sxs-lookup"><span data-stu-id="ef075-571">Select the new test case that was created for **Release a product**, and then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Lisää testitapaukset sarjaan -sivu](./media/setup_rsa_tool_100.png)

    <span data-ttu-id="ef075-573">Testisarjassa on nyt kaksi testitapausta.</span><span class="sxs-lookup"><span data-stu-id="ef075-573">The test suite now has two test cases.</span></span>

    ![Testisarjan kaksi testitapausta](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a><span data-ttu-id="ef075-575">Testitapausten lataaminen RSAT-työkaluun</span><span class="sxs-lookup"><span data-stu-id="ef075-575">Load test cases into RSAT</span></span>

1. <span data-ttu-id="ef075-576">Avaa RSAT ja valitse **Lataa**.</span><span class="sxs-lookup"><span data-stu-id="ef075-576">Open RSAT, and select **Load**.</span></span>
2. <span data-ttu-id="ef075-577">Testitapaukset ladataan, ja saat varoituksen, jonka mukaan toiminto korvaa Excelin testidatatiedostot ja paikalliset muutokset menetetään ja sinulta kysytään,</span><span class="sxs-lookup"><span data-stu-id="ef075-577">The test cases are loaded, and you receive a warning that states, "This action will overwrite Excel test data files, local changes will be lost.</span></span> <span data-ttu-id="ef075-578">haluatko jatkaa.</span><span class="sxs-lookup"><span data-stu-id="ef075-578">Do you want to proceed?"</span></span> <span data-ttu-id="ef075-579">**Kyllä**-vaihtoehdon valinta päivittää paikallisessa järjestelmässä olevat Excelin parametritiedostot mutta ei Azure DevOpsiin ladattujen Excelin parametritiedostoja.</span><span class="sxs-lookup"><span data-stu-id="ef075-579">Select **Yes** to update the Excel parameter files in the local system but not the Excel parameter files that were uploaded to Azure DevOps.</span></span>

    ![Varoitussanoma](./media/setup_rsa_tool_102.png)

    <span data-ttu-id="ef075-581">Molemmat testitapaukset on ladattu yhdessä ensimmäisen testitapauksen Excelin parametritiedoston kanssa.</span><span class="sxs-lookup"><span data-stu-id="ef075-581">Both the test cases are loaded, together with the Excel parameter file for the first test case.</span></span> <span data-ttu-id="ef075-582">Koska valitse viimeisessä ajossa **Lataa palvelimeen**, parametritiedosto haetaan Azure DevOpsiin.</span><span class="sxs-lookup"><span data-stu-id="ef075-582">Because you selected **Upload** in the last run, the parameter files are pulled from Azure DevOps.</span></span>

    ![Ladatut testitapaukset](./media/setup_rsa_tool_103.png)

3. <span data-ttu-id="ef075-584">Valitse vain toinen testitapaus ja valitse sitten **Uusi \> Luo testin suoritus -ja parametritiedostot**.</span><span class="sxs-lookup"><span data-stu-id="ef075-584">Select only the second test case, and then select **New \> Generate test execution and parameter files**.</span></span>

#### <a name="edit-the-excel-parameter-file"></a><span data-ttu-id="ef075-585">Excelin parametritiedoston muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="ef075-585">Edit the Excel parameter file</span></span>

1. <span data-ttu-id="ef075-586">Valitse vain toinen testitapaus ja avaa sitten vastaava Excelin parametritiedosto valitsemalla **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="ef075-586">Select only the second test case, and then select **Edit** to open the corresponding Excel parameter file.</span></span>
2. <span data-ttu-id="ef075-587">Kopioi tallennettu muuttuja **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** ensimmäisestä testitapauksesta kaikkiin kenttiin, joissa tuotenumeroa käytetään. (Lisätietoja on osassa [Tallennetun muuttujan luominen muokkaamalla aiemmin luotua tehtävätallennetta](#modify-an-existing-task-recording-to-create-a-saved-variable).)</span><span class="sxs-lookup"><span data-stu-id="ef075-587">Copy the **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** saved variable (see the [Modify an existing task recording to create a saved variable](#modify-an-existing-task-recording-to-create-a-saved-variable) section) from the first test case into all the fields where the product number is used.</span></span> <span data-ttu-id="ef075-588">Tässä tapauksessa muuttuja kopioidaan **Tuotenumero**- ja **Tarkista tuotenumero** -kenttiin **EcoResProductListPage**-taulukossa.</span><span class="sxs-lookup"><span data-stu-id="ef075-588">In this case, you copy the variable into the **Product number** and **Validate Product number** fields on the **EcoResProductListPage** sheet.</span></span>

    ![Tuotenumero- ja Tarkista tuotenumero -kentät](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > <span data-ttu-id="ef075-590">Muuttujia voidaan siirtää testien välillä vain saman testiajon aikana.</span><span class="sxs-lookup"><span data-stu-id="ef075-590">Variables can be passed between tests only during the same test run.</span></span> <span data-ttu-id="ef075-591">Muuttujien nimien on oltava täsmälleen samat.</span><span class="sxs-lookup"><span data-stu-id="ef075-591">The names of the variables must match exactly.</span></span>

3. <span data-ttu-id="ef075-592">Valitse **Tallenna** ja sulje sitten Excel-työkirja.</span><span class="sxs-lookup"><span data-stu-id="ef075-592">Select **Save**, and then close the Excel workbook.</span></span>
4. <span data-ttu-id="ef075-593">Tallenna Excelin parametritiedostoon tehdyt muutokset valitsemalla **Lataa palvelimeen**.</span><span class="sxs-lookup"><span data-stu-id="ef075-593">Select **Upload** to save the changes that you made to the Excel parameter file.</span></span>

#### <a name="run-the-chained-test-cases"></a><span data-ttu-id="ef075-594">Ketjutettujen testitapausten suorittaminen</span><span class="sxs-lookup"><span data-stu-id="ef075-594">Run the chained test cases</span></span>

1. <span data-ttu-id="ef075-595">Valitse ensin molemmat testitapaukset ja sitten **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="ef075-595">Select both the test cases, and then select **Run**.</span></span>
2. <span data-ttu-id="ef075-596">Tarkista, että molemmat testitapaukset on hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="ef075-596">Verify that both test cases have passed.</span></span>

    ![Kummankin testitapauksen hyväksytyksi määritetty Tulos-kenttä](./media/setup_rsa_tool_105.png)
