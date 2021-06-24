---
title: Finance Insightsin konfigurointi – julkinen esiversio (esiversio) - versio 10.0.20 ja sitä myöhemmät
description: Tässä ohjeaiheessa kerrotaan, millaiset määritysvaiheet järjestelmässä on suoritettava, jotta Finance Insightsin julkisen esiversion ominaisuuksia voi käyttää (versiossa 10.0.20 ja sitä uudemmissa).
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 613bd4816e2f0c4fbb56cf79779a08c6a09592bd
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222609"
---
# <a name="configuration-for-finance-insights-for-public-preview-preview---version-10020-and-later"></a><span data-ttu-id="b759b-103">Finance Insightsin konfigurointi – julkinen esiversio (esiversio) - versio 10.0.20 ja sitä myöhemmät</span><span class="sxs-lookup"><span data-stu-id="b759b-103">Configuration for Finance insights for public preview (preview) - version 10.0.20 and later</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b759b-104">Finance Insights yhdistää Microsoft Dynamics 365 Financen toiminnot Dataversen, Azuren ja AI Builderin kanssa. Yhdessä nämä tarjoavat tehokkaat ennustetyökalut organisaatiolle.</span><span class="sxs-lookup"><span data-stu-id="b759b-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="b759b-105">Tässä ohjeaiheessa kerrotaan, millaiset määritysvaiheet Dynamics 365 Finance -versiossa 10.0.20 on suoritettava, jotta Finance Insightsin julkisen esiversion ominaisuuksia voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="b759b-105">This topic explains how to configure Dynamics 365 Finance version 10.0.20 so that your system can use the capabilities that are available in Finance insights public preview.</span></span>

> [!NOTE]
> <span data-ttu-id="b759b-106">Tässä ohjeaiheessa kuvatut konfigurointivaiheet koskevat vain Finance-versiota 10.0.20 ja sitä myöhempiä.</span><span class="sxs-lookup"><span data-stu-id="b759b-106">The configuration steps that are described in this topic apply only to Finance version 10.0.20 and later.</span></span> <span data-ttu-id="b759b-107">Jos haluat määrittää Finance Insightsin versiolle 10.0.19 tai sitä aikaisemmalle versiolle, katso [Finance Insightsin määritys versioon 10.0.18 asti](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="b759b-107">'To set up Finance insights on version 10.0.19 and earlier, see [Configuration for Finance insights - versions up to 10.0.18](configure-for-fin-insites.md).</span></span>

## <a name="deploy-finance"></a><span data-ttu-id="b759b-108">Ota Finance käyttöön</span><span class="sxs-lookup"><span data-stu-id="b759b-108">Deploy Finance</span></span>

<span data-ttu-id="b759b-109">Määritä ympäristöt näiden ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="b759b-109">Follow these steps to deploy the environments.</span></span>

1. <span data-ttu-id="b759b-110">Luo tai päivitä Finance-ympäristö Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="b759b-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Finance environment.</span></span> <span data-ttu-id="b759b-111">Ympäristö edellyttää, että käytössä on Finance and Operations -sovellusten versio 10.0.20 tai sitä uudempi.</span><span class="sxs-lookup"><span data-stu-id="b759b-111">The environment requires app version 10.0.20 or later of Finance and Operations apps.</span></span>
2. <span data-ttu-id="b759b-112">Ympäristön on oltava korkean käytettävyyden ympäristö eristysympäristössä.</span><span class="sxs-lookup"><span data-stu-id="b759b-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="b759b-113">(Tämä ympäristötyyppi tunnetaan myös tason 2 ympäristönä.) Lisätietoja on kohdassa [Ympäristön suunnittelu](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="b759b-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="b759b-114">Jos olet konfiguroimassa Finance Insightsia eristysympäristössä, tuotantotiedot on ehkä kopioitava tähän ympäristöön, jotta ennusteet toimisivat.</span><span class="sxs-lookup"><span data-stu-id="b759b-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="b759b-115">Ennustemallissa käytetään useiden vuosien tietoja ennusteiden luomiseen.</span><span class="sxs-lookup"><span data-stu-id="b759b-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="b759b-116">Contoso-demotiedot eivät sisällä tarpeeksi historiatietoja ennustemallin kouluttamista varten.</span><span class="sxs-lookup"><span data-stu-id="b759b-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="b759b-117">Määritä Dataverse</span><span class="sxs-lookup"><span data-stu-id="b759b-117">Configure Dataverse</span></span>

<span data-ttu-id="b759b-118">Näitä ohjeita noudattamalla voit määrittää Dataversen Finance Insightsille.</span><span class="sxs-lookup"><span data-stu-id="b759b-118">Follow these steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="b759b-119">Avaa ympäristösivu LCS:ssä ja tarkista, että **Power Platform -integrointi** -osa on jo asennettu.</span><span class="sxs-lookup"><span data-stu-id="b759b-119">In LCS, open the environment page, and verify that the **Power Platform Integration** section is already set up.</span></span>

    - <span data-ttu-id="b759b-120">Jos se on jo asennettu, Dataverse-ympäristön nimi, joka on linkitetty Finance-ympäristöön, pitäisi olla luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b759b-120">If it's already set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>
    - <span data-ttu-id="b759b-121">Jos sitä ei ole määritetty, noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="b759b-121">If it isn't yet set up, follow these steps:</span></span>

        1. <span data-ttu-id="b759b-122">Valitse **Määritys** **Power Platform -integrointi** -osasta.</span><span class="sxs-lookup"><span data-stu-id="b759b-122">In the **Power Platform Integration** section, select **Setup**.</span></span> <span data-ttu-id="b759b-123">Ympäristön määrittäminen voi kestää noin tunnin.</span><span class="sxs-lookup"><span data-stu-id="b759b-123">Setup of the environment might take up to an hour.</span></span>
        2. <span data-ttu-id="b759b-124">Jos Dataverse-ympäristö on asennettu onnistuneesti, Dataverse-ympäristön nimi, joka on linkitetty Finance-ympäristöön, pitäisi olla luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b759b-124">If the Dataverse environment is successfully set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>

        > [!NOTE]
        > <span data-ttu-id="b759b-125">Kun olet suorittanut ympäristöasetukset, **älä** valitse kohtaa **CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="b759b-125">After you complete the environment setup, do **not** select **Link to CDS for Apps**.</span></span> <span data-ttu-id="b759b-126">Tätä painiketta ei tarvita Finance Insightsissa.</span><span class="sxs-lookup"><span data-stu-id="b759b-126">This button isn't required for Finance insights.</span></span> <span data-ttu-id="b759b-127">Jos valitset sen, et voi määrittää pakollisia ympäristön lisäosia LCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="b759b-127">If you select it, you won't be able to configure the required environment add-ins in LCS.</span></span>

## <a name="configure-azure"></a><span data-ttu-id="b759b-128">Konfiguroi Azure</span><span class="sxs-lookup"><span data-stu-id="b759b-128">Configure Azure</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="b759b-129">Finance Insightsin Data Lake -resurssien määrittäminen Azure Cloud Shellin avulla</span><span class="sxs-lookup"><span data-stu-id="b759b-129">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="b759b-130">Windows PowerShell -komentosarjan käyttäminen</span><span class="sxs-lookup"><span data-stu-id="b759b-130">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="b759b-131">Windows PowerShell -komentosarja on annettu. Voit siis helposti määrittää Azure-resurssit, jotka on esitelty kohdassa [Azure Data Lakeen viennin määrittäminen](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="b759b-131">A Windows PowerShell script has been provided so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="b759b-132">Jos haluat määrittää asetuksen manuaalisesti, ohita nämä vaiheet ja suorita [Manuaalinen määritys](#manual-setup) -osan prosessia.</span><span class="sxs-lookup"><span data-stu-id="b759b-132">If you prefer to do the setup manually, skip this procedure, and complete the procedure in the [Manual setup](#manual-setup) section instead.</span></span>

> [!NOTE]
> <span data-ttu-id="b759b-133">Suorita Windows PowerShell -komentotiedosto seuraavia ohjeita noudattamalla.</span><span class="sxs-lookup"><span data-stu-id="b759b-133">Use the following procedure to run the Windows PowerShell script.</span></span> <span data-ttu-id="b759b-134">Asennus ei ehkä toimi, jos käytät **Kokeile** -valintaa Azure CLI:ssä tai jos suoritat komentosarjan tietokoneessa.</span><span class="sxs-lookup"><span data-stu-id="b759b-134">The setup might not work if you use the **Try it** option in Azure CLI or if you run the script on your computer.</span></span>

<span data-ttu-id="b759b-135">Näiden vaiheiden avulla voit määrittää Azuren käyttämällä Windows PowerShell -komentosarjaa.</span><span class="sxs-lookup"><span data-stu-id="b759b-135">Follow these steps to use the Windows PowerShell script to configure Azure.</span></span> <span data-ttu-id="b759b-136">Tarvitset Azure-resurssiryhmän, Azure-resurssien ja Azure AD -sovelluksen luontioikeudet.</span><span class="sxs-lookup"><span data-stu-id="b759b-136">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="b759b-137">Lisätietoja vaadituista käyttöoikeuksista on kohdassa [Azure AD:n käyttöoikeuksien tarkistaminen](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="b759b-137">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="b759b-138">Siirry [Azure-portaalissa](https://portal.azure.com) Azuren kohdetilaukseen.</span><span class="sxs-lookup"><span data-stu-id="b759b-138">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span>
2. <span data-ttu-id="b759b-139">Valitse **Hae**-kentän oikealla puolella oleva **Cloud Shell** -kohta.</span><span class="sxs-lookup"><span data-stu-id="b759b-139">Select **Cloud Shell** to the right of the **Search** field.</span></span>
3. <span data-ttu-id="b759b-140">Valitse **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="b759b-140">Select **PowerShell**.</span></span>
4. <span data-ttu-id="b759b-141">Luo tallennustila, jos sinua kehotetaan tekemään niin.</span><span class="sxs-lookup"><span data-stu-id="b759b-141">Create storage if you're prompted to create it.</span></span>
5. <span data-ttu-id="b759b-142">Valitse **Azure CLI** -välilehdessä **Kopioi**.</span><span class="sxs-lookup"><span data-stu-id="b759b-142">On the **Azure CLI** tab, select **Copy**.</span></span>
6. <span data-ttu-id="b759b-143">Avaa Muistiossa uusi tiedosto ja liitä Windows PowerShell -komentosarja.</span><span class="sxs-lookup"><span data-stu-id="b759b-143">In Notepad, open a new file, and paste in the Windows PowerShell script.</span></span>
7. <span data-ttu-id="b759b-144">Tallenna tiedosto nimellä **ConfigureDataLake.ps1**.</span><span class="sxs-lookup"><span data-stu-id="b759b-144">Save the file as **ConfigureDataLake.ps1**.</span></span>
8. <span data-ttu-id="b759b-145">Lataa Windows PowerShell -komentosarja istuntoon käyttämällä valikkovaihtoehtoa lataamiselle Cloud Shellissä.</span><span class="sxs-lookup"><span data-stu-id="b759b-145">Upload the Windows PowerShell script to the session by using the menu option for upload in Cloud Shell.</span></span>
9. <span data-ttu-id="b759b-146">Suorita komentosarja **.\ConfigureDataLake.ps1**.</span><span class="sxs-lookup"><span data-stu-id="b759b-146">Run the **.\ConfigureDataLake.ps1** script.</span></span>
10. <span data-ttu-id="b759b-147">Suorita komentosarja kehotteen ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="b759b-147">Follow the prompts to run the script.</span></span>
11. <span data-ttu-id="b759b-148">Käytä komentosarjan tulosten tietoja ja asenna Vie Data Lakeen -apuohjelma LCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="b759b-148">Use the information from the script output to install the Export to Data Lake add-in in LCS.</span></span>

### <a name="manual-setup"></a><span data-ttu-id="b759b-149">Manuaalinen määritys</span><span class="sxs-lookup"><span data-stu-id="b759b-149">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="b759b-150">Sovellusten lisääminen Azure AD -vuokraajaan</span><span class="sxs-lookup"><span data-stu-id="b759b-150">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="b759b-151">Siirry [Azure-portaalissa](https://portal.azure.com) **Azure Active Directoryyn**.</span><span class="sxs-lookup"><span data-stu-id="b759b-151">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="b759b-152">Valitse **Hallitse \> Yrityssovellukset**.</span><span class="sxs-lookup"><span data-stu-id="b759b-152">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="b759b-153">Hae seuraavat sovellukset sovellustunnuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="b759b-153">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="b759b-154">Hakemus</span><span class="sxs-lookup"><span data-stu-id="b759b-154">Application</span></span>                              | <span data-ttu-id="b759b-155">Sovelluksen tunnus</span><span class="sxs-lookup"><span data-stu-id="b759b-155">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="b759b-156">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="b759b-156">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="b759b-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="b759b-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="b759b-158">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="b759b-158">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="b759b-159">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="b759b-159">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="b759b-160">AI Builderin todennuspalvelu</span><span class="sxs-lookup"><span data-stu-id="b759b-160">AI Builder Authorization Service</span></span>         | <span data-ttu-id="b759b-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="b759b-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="b759b-162">Jos et löydä ainoatakaan edellisistä sovelluksista, kokeile alla mainittuja vaiheita.</span><span class="sxs-lookup"><span data-stu-id="b759b-162">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="b759b-163">Valitse paikallisessa tietokoneessa **Käynnistä**-valikko ja hae **powershell**.</span><span class="sxs-lookup"><span data-stu-id="b759b-163">On your local computer, on the **Start** menu, search for **powershell**.</span></span>
2. <span data-ttu-id="b759b-164">Valitse ja pidä valittuna (tai valitse hiiren kakkospainikkeella) **Windows PowerShell** ja valitse sitten **Suorita järjestelmänvalvojana**.</span><span class="sxs-lookup"><span data-stu-id="b759b-164">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="b759b-165">Suorita seuraava komento, jos haluat asentaa **AzureAD**-moduulin.</span><span class="sxs-lookup"><span data-stu-id="b759b-165">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="b759b-166">Jos jatkaminen edellyttää, että käytössä on NuGet-palveluntarjoaja, valitse **K** ja asenna se.</span><span class="sxs-lookup"><span data-stu-id="b759b-166">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="b759b-167">Jos näyttöön tulee Ei-luotettava säilö -sanoma, jatka valitsemalla **K**.</span><span class="sxs-lookup"><span data-stu-id="b759b-167">If you receive an "Untrusted repository" message, select **Y** to continue.</span></span>
6. <span data-ttu-id="b759b-168">Suorita jokaisen lisättävän sovelluksen kohdalla seuraavat komennot ja lisää sovellus Azure AD:hen.</span><span class="sxs-lookup"><span data-stu-id="b759b-168">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="b759b-169">Kun sinua pyydetään kirjautumaan, käytä Azure AD -järjestelmänvalvojan tunnuksia.</span><span class="sxs-lookup"><span data-stu-id="b759b-169">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="b759b-170">Azure-resurssien luominen</span><span class="sxs-lookup"><span data-stu-id="b759b-170">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="b759b-171">Varmista, että luot seuraavat resurssit samassa Azure AD -esiintymässä kuin missä Dataverse -ympäristö on.</span><span class="sxs-lookup"><span data-stu-id="b759b-171">Make sure that you create the following resources in the same Azure AD instance that the Dataverse environment is in.</span></span> <span data-ttu-id="b759b-172">Et voi käyttää eri Azure AD -esiintymän resursseja.</span><span class="sxs-lookup"><span data-stu-id="b759b-172">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="b759b-173">Luo tallennustili seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="b759b-173">Create a storage account:</span></span>

    1. <span data-ttu-id="b759b-174">Luo [Azure-portaalissa](https://portal.azure.com) tallennustili.</span><span class="sxs-lookup"><span data-stu-id="b759b-174">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="b759b-175">Määritä **Luo tallennustili** -valintaikkunassa seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="b759b-175">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="b759b-176">**Sijainti** – Valitse palvelinkeskus, jossa ympäristö sijaitsee.</span><span class="sxs-lookup"><span data-stu-id="b759b-176">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="b759b-177">**Suorituskyky** – Suorituskyvyn arvoksi kannattaa valita **Standardi**.</span><span class="sxs-lookup"><span data-stu-id="b759b-177">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="b759b-178">**Tilin tyyppi** – Valitse **TallennustilaV2**.</span><span class="sxs-lookup"><span data-stu-id="b759b-178">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="b759b-179">Valitse **Data Laken tallennustila Gen2** -asetuksen **Lisäasetukset**-valintaikkunassa **Ota käyttöön** **Hierarkkiset nimitilat**-toiminnon alla.</span><span class="sxs-lookup"><span data-stu-id="b759b-179">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="b759b-180">Jos et ota tätä toimintoa käyttöön, et voi käyttää Finance and Operations -sovellusten kirjoittamia tietoja käyttämällä palveluita, kuten Power BI:n tiedonkulkuja.</span><span class="sxs-lookup"><span data-stu-id="b759b-180">If you don't enable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="b759b-181">Valitse **Tarkista ja luo**.</span><span class="sxs-lookup"><span data-stu-id="b759b-181">Select **Review and create**.</span></span> <span data-ttu-id="b759b-182">Kun käyttöönotto on valmis, uusi resurssi näkyy Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="b759b-182">When the deployment is completed, the new resource is shown in the Azure portal.</span></span>
    5. <span data-ttu-id="b759b-183">Siirry luotuun tallennustiliin.</span><span class="sxs-lookup"><span data-stu-id="b759b-183">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="b759b-184">Valitse vasemmanpuoleisessa valikossa **Käyttöoikeusavaimet**.</span><span class="sxs-lookup"><span data-stu-id="b759b-184">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="b759b-185">Kopioi ja tallenna tallennustilin nimi.</span><span class="sxs-lookup"><span data-stu-id="b759b-185">Copy and save the name of the storage account.</span></span> <span data-ttu-id="b759b-186">Tämä arvo on annettava myöhemmin, kun avainsäilön salasana määritetään.</span><span class="sxs-lookup"><span data-stu-id="b759b-186">You will have to provide this value later, when you set up key vault secrets.</span></span>

2. <span data-ttu-id="b759b-187">Luo avainsäilö seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="b759b-187">Create a key vault:</span></span>

    1. <span data-ttu-id="b759b-188">Luo [Azure-portaalissa](https://portal.azure.com) avainsäilö.</span><span class="sxs-lookup"><span data-stu-id="b759b-188">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="b759b-189">Valitse **Sijainti**-kentän **Luo avainsäilö** -valintaikkunassa palvelinkeskus, jossa ympäristö sijaitsee.</span><span class="sxs-lookup"><span data-stu-id="b759b-189">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="b759b-190">Kun olet luonut avainsäilön, siirry kohtaan **Avainsäilön yhteenveto** ja kopioi ja tallenna DNS-nimi.</span><span class="sxs-lookup"><span data-stu-id="b759b-190">After key vault is created, go to **Key Vault Overview**, and copy and save the DNS name.</span></span> <span data-ttu-id="b759b-191">Tämä arvo on annettava myöhemmin, kun Data Laken lisäosa määritetään.</span><span class="sxs-lookup"><span data-stu-id="b759b-191">You will have to provide this value later, when you set up the Data Lake add-in.</span></span>

3. <span data-ttu-id="b759b-192">Luo ja rekisteröi Azure AD -sovellus seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="b759b-192">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="b759b-193">Siirry [Azure-portaalissa](https://portal.azure.com) kohtaan **Azure Active Directory** ja valitse **Sovellusten rekisteröinnit**.</span><span class="sxs-lookup"><span data-stu-id="b759b-193">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="b759b-194">Valitse **Uuden sovelluksen rekisteröiminen** ja valitse sitten seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="b759b-194">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="b759b-195">**Nimi** – Anna sovelluksen nimi.</span><span class="sxs-lookup"><span data-stu-id="b759b-195">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="b759b-196">**Sovellustyyppi** – Valitse **Web-ohjelmointirajapinta**.</span><span class="sxs-lookup"><span data-stu-id="b759b-196">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="b759b-197">**Uudelleenohjauksen URI:n määritys** – Anna Dynamics 365 -esiintymän URL-osoite, esimerkiksi `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="b759b-197">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="b759b-198">Siirry juuri luotuun sovellukseen. Kopioi ja tallenna sen **sovelluksen (asiakassovelluksen) tunnuksen** arvo.</span><span class="sxs-lookup"><span data-stu-id="b759b-198">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="b759b-199">Tämä arvo on annettava myöhemmin, kun avainsäilön salasana määritetään.</span><span class="sxs-lookup"><span data-stu-id="b759b-199">You will have to provide this value later, when you set up key vault secrets.</span></span>
    4. <span data-ttu-id="b759b-200">Siirry **Ohjelmointirajapinnan käyttöoikeudet** -kohtaan ja suorita seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="b759b-200">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="b759b-201">Valitse **Lisää käyttöoikeus**.</span><span class="sxs-lookup"><span data-stu-id="b759b-201">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="b759b-202">Valitse **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="b759b-202">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="b759b-203">Kun olet valinnut delegoidut käyttöoikeudet, valitse **user\_impersonation**.</span><span class="sxs-lookup"><span data-stu-id="b759b-203">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="b759b-204">Valitse **Lisää käyttöoikeudet**.</span><span class="sxs-lookup"><span data-stu-id="b759b-204">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="b759b-205">Valitse sovelluksen valikosta **Sertifikaatit \& salaiset koodit**. Luo sitten avainsäilön salaiset koodit seuraavien vaiheiden avulla:</span><span class="sxs-lookup"><span data-stu-id="b759b-205">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="b759b-206">Valitse **Uusi asiakkaan salainen koodi**.</span><span class="sxs-lookup"><span data-stu-id="b759b-206">Select **New client secret**.</span></span>
        2. <span data-ttu-id="b759b-207">Syötä **Avaimen kuvaus** -kenttään nimi.</span><span class="sxs-lookup"><span data-stu-id="b759b-207">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="b759b-208">Valitse kesto ja valitse sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="b759b-208">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="b759b-209">Salainen koodi luodaan **Arvo**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b759b-209">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="b759b-210">Kopioi ja tallenna asiakasohjelman salasanan arvo.</span><span class="sxs-lookup"><span data-stu-id="b759b-210">Copy and save the client secret value.</span></span> <span data-ttu-id="b759b-211">Tämä arvo on annettava myöhemmin, kun avainsäilön salasana määritetään.</span><span class="sxs-lookup"><span data-stu-id="b759b-211">You will have to provide this value later, when you set up key vault secrets.</span></span>

4. <span data-ttu-id="b759b-212">Luo avainsäilön salaiset koodit seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="b759b-212">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="b759b-213">Siirry aiemmin luotuun avainsäilöön ja valitse **Salaiset koodit**.</span><span class="sxs-lookup"><span data-stu-id="b759b-213">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="b759b-214">Noudata seuraavia vaiheita kunkin seuraavan taulukon salaisen koodin nimen kohdalla:</span><span class="sxs-lookup"><span data-stu-id="b759b-214">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="b759b-215">Valitse **Luo tai tuo**.</span><span class="sxs-lookup"><span data-stu-id="b759b-215">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="b759b-216">Valitse **Luo salasana** -valintaikkunan **Lataa asetuksia** -kentässä **Manuaalinen**.</span><span class="sxs-lookup"><span data-stu-id="b759b-216">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="b759b-217">Luo salaisen koodin nimi ja arvo taulusta.</span><span class="sxs-lookup"><span data-stu-id="b759b-217">Create the secret name and value from the table.</span></span>
        4. <span data-ttu-id="b759b-218">Valitse **Käytössä** ja valitse sitten **Luo**.</span><span class="sxs-lookup"><span data-stu-id="b759b-218">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="b759b-219">Salainen koodi luodaan ja lisätään avainsäilöön.</span><span class="sxs-lookup"><span data-stu-id="b759b-219">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="b759b-220">Salaisen koodin nimi</span><span class="sxs-lookup"><span data-stu-id="b759b-220">Secret name</span></span>                       | <span data-ttu-id="b759b-221">Salaisen koodin arvo</span><span class="sxs-lookup"><span data-stu-id="b759b-221">Secret value</span></span>                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | <span data-ttu-id="b759b-222">sovelluksen tunnus</span><span class="sxs-lookup"><span data-stu-id="b759b-222">app-id</span></span>                            | <span data-ttu-id="b759b-223">Aiemmin luodun sovelluksen sovellustunnus.</span><span class="sxs-lookup"><span data-stu-id="b759b-223">The app ID of the application that you created earlier.</span></span>                                      |
        | <span data-ttu-id="b759b-224">sovelluksen salainen koodi</span><span class="sxs-lookup"><span data-stu-id="b759b-224">app-secret</span></span>                        | <span data-ttu-id="b759b-225">Aiemmin tallennettu asiakkaan salainen koodi.</span><span class="sxs-lookup"><span data-stu-id="b759b-225">The client secret that you saved earlier.</span></span>                                                    |
        | <span data-ttu-id="b759b-226">tallennustilin nimi</span><span class="sxs-lookup"><span data-stu-id="b759b-226">storage-account-name</span></span>              | <span data-ttu-id="b759b-227">Aiemmin luodun tallennustilin nimi, kuten **tallennustili1**.</span><span class="sxs-lookup"><span data-stu-id="b759b-227">The name of the storage account that you created earlier, such as **storageaccount1**.</span></span>       |

5. <span data-ttu-id="b759b-228">Anna sovellukselle lupa käyttää avainsäilöä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="b759b-228">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="b759b-229">Avaa [Azure-portaalissa](https://portal.azure.com) aiemmin luotu avainsäilö.</span><span class="sxs-lookup"><span data-stu-id="b759b-229">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="b759b-230">Valitse käyttöoikeuskäytännöt.</span><span class="sxs-lookup"><span data-stu-id="b759b-230">Select the access policies.</span></span>
    3. <span data-ttu-id="b759b-231">Noudata seuraavia vaiheita kunkin seuraavan taulukon sovelluksen kohdalla:</span><span class="sxs-lookup"><span data-stu-id="b759b-231">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="b759b-232">Luo käyttöoikeuskäytäntö valitsemalla **Lisää käyttöoikeuskäytäntö**.</span><span class="sxs-lookup"><span data-stu-id="b759b-232">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="b759b-233">Valitse **Salaisen koodin käyttöoikeudet** -kentässä käyttöoikeudet taulukosta.</span><span class="sxs-lookup"><span data-stu-id="b759b-233">In the **Secret permissions** field, select the permissions from the table.</span></span>
        3. <span data-ttu-id="b759b-234">Hae **Valitse päänimi** -kentässä sovelluksen näyttönimi taulukosta.</span><span class="sxs-lookup"><span data-stu-id="b759b-234">In the **Select principal** field, search for the application display name from the table.</span></span>
        4. <span data-ttu-id="b759b-235">Valitse **Valitse**.</span><span class="sxs-lookup"><span data-stu-id="b759b-235">Select **Select**.</span></span>
        5. <span data-ttu-id="b759b-236">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="b759b-236">Select **Add**.</span></span>
        6. <span data-ttu-id="b759b-237">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b759b-237">Select **Save**.</span></span>

        | <span data-ttu-id="b759b-238">Hakemus</span><span class="sxs-lookup"><span data-stu-id="b759b-238">Application</span></span>                                              | <span data-ttu-id="b759b-239">Käyttöoikeudet</span><span class="sxs-lookup"><span data-stu-id="b759b-239">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="b759b-240">Luodun uuden sovelluksen näyttönimi</span><span class="sxs-lookup"><span data-stu-id="b759b-240">The display name of the new application that you created</span></span> | <span data-ttu-id="b759b-241">Hae, Luettelo</span><span class="sxs-lookup"><span data-stu-id="b759b-241">Get, List</span></span>   |
        | <span data-ttu-id="b759b-242">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="b759b-242">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="b759b-243">Hae, Luettelo</span><span class="sxs-lookup"><span data-stu-id="b759b-243">Get, List</span></span>   |

6. <span data-ttu-id="b759b-244">Määritä seuraavasti roolit, jotka käyttävät tallennustiliä:</span><span class="sxs-lookup"><span data-stu-id="b759b-244">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="b759b-245">Avaa [Azure-portaalissa](https://portal.azure.com) aiemmin luotu tallennustili.</span><span class="sxs-lookup"><span data-stu-id="b759b-245">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="b759b-246">Valitse **Käyttöoikeuksien hallinta (IAM)** ja valitse sitten **Roolimääritykset**.</span><span class="sxs-lookup"><span data-stu-id="b759b-246">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="b759b-247">Valitse **Lisää, Lisää roolimääritys**.</span><span class="sxs-lookup"><span data-stu-id="b759b-247">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="b759b-248">Noudata seuraavia vaiheita kunkin seuraavan taulukon sovelluksen kohdalla:</span><span class="sxs-lookup"><span data-stu-id="b759b-248">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="b759b-249">Valitse rooli taulusta.</span><span class="sxs-lookup"><span data-stu-id="b759b-249">Select the role from the table.</span></span>
        2. <span data-ttu-id="b759b-250">Jätä **Delegoi käyttöoikeus** -kentän arvoksi **Azure AD -käyttäjä, -ryhmä tai -palvelun päänimi** -arvo.</span><span class="sxs-lookup"><span data-stu-id="b759b-250">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="b759b-251">Syötä **Valitse**-kenttään sovellus taulukosta.</span><span class="sxs-lookup"><span data-stu-id="b759b-251">In the **Select** field, enter the application from the table.</span></span>
        4. <span data-ttu-id="b759b-252">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b759b-252">Select **Save**.</span></span>

        | <span data-ttu-id="b759b-253">Hakemus</span><span class="sxs-lookup"><span data-stu-id="b759b-253">Application</span></span>                                              | <span data-ttu-id="b759b-254">Rooli</span><span class="sxs-lookup"><span data-stu-id="b759b-254">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="b759b-255">Luodun uuden sovelluksen näyttönimi</span><span class="sxs-lookup"><span data-stu-id="b759b-255">The display name of the new application that you created</span></span> | <span data-ttu-id="b759b-256">Omistaja</span><span class="sxs-lookup"><span data-stu-id="b759b-256">Owner</span></span>                       |
        | <span data-ttu-id="b759b-257">Luodun uuden sovelluksen näyttönimi</span><span class="sxs-lookup"><span data-stu-id="b759b-257">The display name of the new application that you created</span></span> | <span data-ttu-id="b759b-258">Osallistuja</span><span class="sxs-lookup"><span data-stu-id="b759b-258">Contributor</span></span>                 |
        | <span data-ttu-id="b759b-259">Luodun uuden sovelluksen näyttönimi</span><span class="sxs-lookup"><span data-stu-id="b759b-259">The display name of the new application that you created</span></span> | <span data-ttu-id="b759b-260">Tallennustili - osallistuja</span><span class="sxs-lookup"><span data-stu-id="b759b-260">Storage Account Contributor</span></span> |
        | <span data-ttu-id="b759b-261">Luodun uuden sovelluksen näyttönimi</span><span class="sxs-lookup"><span data-stu-id="b759b-261">The display name of the new application that you created</span></span> | <span data-ttu-id="b759b-262">Tallennustilan blob-objektin tietojen omistaja</span><span class="sxs-lookup"><span data-stu-id="b759b-262">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="b759b-263">**AI Builderin todennuspalvelu**</span><span class="sxs-lookup"><span data-stu-id="b759b-263">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="b759b-264">Tallennustilan blob-objektin tietojen lukija</span><span class="sxs-lookup"><span data-stu-id="b759b-264">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="b759b-265">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="b759b-265">Azure CLI</span></span>](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    Assert-ScriptSetup

    $ClientAppName = 'Finance Data Lake Application'
    $DefaultSecretExpiryInYear = 1
    $MicrosoftDynamicsERPMicroservicesAppId = '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    $MicrosoftDynamicsERPMicroservicesCDSAppId = '703e2651-d3fc-48f5-942c-74274233dba8'
    $AIBuilderAuthorizationServiceAppId = 'ad40333e-9910-4b61-b281-e3aeeb8c3ef3'
    $KeyVaultServicePrincipalAppId = 'cfa8b339-82a2-471a-a3c9-0fc0be7a4093'
    $GraphServicePrincipalAppId = '00000003-0000-0000-c000-000000000000'

    Import-Module AzureAD.Standard.Preview
    $connectAzureADParameters = @{ 'Identity' = $true; 'TenantId' = $env:ACC_TID }
    $azContext = AzureAD.Standard.Preview\Connect-AzureAD @connectAzureADParameters
    $userContext = ConvertFrom-Json ((az ad signed-in-user show) -join '')
    $user = Get-AzureADUser -Filter ("UserPrincipalName eq '" + $userContext.UserPrincipalName + "'")

    Set-AzureSubscription
    
    $resourceGroup = $null
    $ResourceGroupName = 'D365FinanceInsightsDataLake'
    $ResourceGroupNameSuffix = ''
    $FullResourceGroupName = ''
    Write-Output ("The default Azure Resource Group name is '{0}'" -f $ResourceGroupName)
    while (-not ($resourceGroup)) {
        $ResourceGroupNameSuffix = (Read-Host -Prompt "Enter optional Azure Resource Group name suffix: (leave blank for no suffix)")
        if ([string]::IsNullOrWhitespace($ResourceGroupNameSuffix))
        {
            $FullResourceGroupName = $ResourceGroupName
        }
        else
        {
            if ($ResourceGroupNameSuffix -notmatch "^[A-Za-z0-9]+$") {
                Write-Warning "The Azure Resource Group name suffix can only include alphanumeric characters."
                continue
            }

            if ($ResourceGroupNameSuffix.Length -gt 60) {
                Write-Warning "The Azure Resource Group name suffix cannot be longer than 60 characters."
                continue
            }

            $FullResourceGroupName = $ResourceGroupName + $ResourceGroupNameSuffix
        }
        
        $resourceGroup = Get-AzResourceGroup -Name $FullResourceGroupName -ErrorAction SilentlyContinue

        if (-not ($resourceGroup)) {
            Write-Output ("Your new Azure Resource Group name is '{0}'" -f $FullResourceGroupName)
            $resourceLocation = ''
            $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
            while ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations))) {
                $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
                if ($resourceLocation -eq 'help') {
                    Write-Output ("List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
                elseif ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations)))
                {
                    Write-Warning ("The provided location is not available for resource group. List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
            }
            $resourceGroup = New-AzResourceGroup -Name $FullResourceGroupName -Location $resourceLocation
            Write-Output ("Created Azure Resource Group '{0}'" -f $resourceGroup.ResourceGroupName)
        }
        else {
            Write-Output ("Found Azure Resource Group '{0}'" -f ($resourceGroup.ResourceGroupName))
        }
    }

    Write-Output '================================================================================='
    $MicrosoftDynamicsERPMicroservicesAppObjectId = Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId
    Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Out-Null
    $aibuilderAuthorizationServiceObjectId = Create-ADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId
    Write-Output ('=================================================================================')

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $ClientAppName + "'")
    if (-not ($clientAppSPN)) {
        $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        if (-not $keyVaultPrincipal)
        {
            New-AzureADServicePrincipal -AppId $KeyVaultServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Key Vault principal to AAD"
            $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        }
        $keyVaultAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $keyVaultAccess.ResourceAppId = $keyVaultPrincipal.AppId
        $keyVaultAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $keyVaultPrincipal.Oauth2Permissions.Id, "Scope")

        $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        if (-not $graphPrincipal)
        {
            New-AzureADServicePrincipal -AppId $GraphServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Graph principal to AAD"
            $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        }
        $userRead = $graphPrincipal.Oauth2Permissions | Where-Object { $_.Type -eq "User" -and $_.Value -eq "User.Read" }
        $graphAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $graphAccess.ResourceAppId = $graphPrincipal.AppId
        $graphAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $userRead.Id, "Scope")

        $clientApp = New-AzureADApplication -DisplayName $ClientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($ClientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $ClientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($DefaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    try {
        $deployment = New-AzResourceGroupDeployment -ResourceGroupName $FullResourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId -Force -ErrorAction Stop
    }
    catch {
        $ErrorMessage = $_.Exception.Message
        if ($ErrorMessage.Contains("not allowed to be updated"))
        {
            Write-Error ($ErrorMessage)
            Write-Warning "Some items in the existing resource group $FullResourceGroupName could not be updated. To resolve the issue, remove the existing resource group $FullResourceGroupName and run the script again."
        }
        else {
            throw
        }

    }
    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
        
        $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
        $tenantId = (Get-AzContext).Tenant.Id

        Write-Output "Values for LCS Data Lake Add-In:"
        Write-Output ("  Tenant ID:                         " + $tenantId)
        Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
        Write-Output "  Storage account secret name:       storage-account-name"
        Write-Output "  Application ID secret name:        app-id"
        Write-Output "  Application Secret secret name:    app-secret"
        Write-Warning "Copy this information for the LCS Add-in for easy access. Azure Cloud Shell will eventually time out and close."

        Write-Output '================================================================================='
        Write-Output "Values for System parameters > Data connections:"
        Write-Output ("  Application ID:                    " + $clientAppId)
        Write-Output ("  Application Secret:                " + $ClientAppSecret)
        Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
        Write-Output "  Secret name:                       storage-account-connection-string"
        Write-Warning "Copy this information for the System parameters for easy access. Azure Cloud Shell will eventually time out and close."
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $FullResourceGroupName)
    }
}

function Assert-ScriptSetup {
    if ($PSVersionTable.PSEdition -ne 'Core' -or -not $env:ACC_TID) { 
        throw "This script needs to be uploaded and run from Azure Cloud Shell (PowerShell)." 
    }
    
    if ((Get-AzContext) -eq $null -and (Connect-AzAccount) -eq $null) {
        throw 'Unable to connect to Azure account.'
    }
}

function Set-AzureSubscription {
    $azSubscription = $null
    while (-not ($azSubscription)) {
        $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (leave blank for default)")
        if ([string]::IsNullOrWhitespace($subscriptionId)){
            break
        }
        elseif (-not [guid]::TryParse($subscriptionId, $([ref][guid]::Empty))) {
                Write-Warning "Azure Subscription ID must be a valid GUID."
                continue
        }

        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }
}

function Create-ADServicePrincipal {
    param (
        [string] $AppId
    )

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AppId | Out-Null
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
        Write-Host ("Added AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }
    else {
        Write-Host ("Found AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }

    return $service.ObjectId
}

$azureTemplate = @"
{
    "contentVersion": "1.0.0.0",
    "parameters": {
      "aibuilderAppObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of the AI Builder application."
        }
      },
      "clientAppId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the application ID of client application."
        }
      },
      "clientAppSecret": {
        "type": "String",
        "metadata": {
          "description": "Specifies the Azure App ID client secret to in azure key vault."
        }
      },
      "clientAppSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of a client application service principal."
        }
      },
      "userSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of tenant admin service principal."
        }
      },
      "microserviceSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of Microsoft Dynamics ERP Microservices service principal."
        }
      },
      "storageAccountType": {
        "type": "string",
        "defaultValue": "Standard_LRS",
        "allowedValues": [
          "Standard_LRS",
          "Standard_GRS",
          "Standard_ZRS",
          "Premium_LRS"
        ],
        "metadata": {
          "description": "Storage Account type"
        }
      }
    },
    "variables": {
      "storageAccountApiVersion": "2019-06-01",
      "keyVaultApiVersion": "2018-02-14",
      "secretsPermissions": [
        "list",
        "get"
      ],
      "location": "[resourceGroup().location]",
      "storageAccountName": "[concat('store', uniquestring(resourceGroup().id))]",
      "keyVaultName": "[concat('keyvault', uniquestring(resourceGroup().id))]",
      "owner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '8e3af657-a8ff-443c-a75c-2fe8c4bcb635')]",
      "contributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b24988ac-6180-42a0-ab88-20f7382dd24c')]",
      "storageAccountContributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '17d1049b-9a84-46fb-8f53-869881c3d3ab')]",
      "storageBlobDataOwner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b7e6dc6d-f1e8-4753-8033-0f276bb0955b')]",
      "storageBlobDataReader": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '2a2b9908-6ea1-4ae2-8e65-a410df84e7d1')]"
    },
    "resources": [
      {
        "type": "Microsoft.Storage/storageAccounts",
        "apiVersion": "[variables('storageAccountApiVersion')]",
        "name": "[variables('storageAccountName')]",
        "location": "[variables('location')]",
        "sku": {
          "name": "[parameters('storageAccountType')]"
        },
        "kind": "StorageV2",
        "properties": {
          "accessTier": "Hot",
          "supportsHttpsTrafficOnly": true,
          "isHnsEnabled": true
        },
        "resources": [
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'1')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('owner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'2')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('contributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'3')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageAccountContributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'4')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataOwner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'5')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataReader')]",
              "principalId": "[parameters('aibuilderAppObjectId')]"
            }
          }
        ]
      },
      {
        "type": "Microsoft.KeyVault/vaults",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "name": "[variables('keyVaultName')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName'))]"
        ],
        "tags": {
        },
        "properties": {
          "enabledForDeployment": false,
          "enabledForTemplateDeployment": false,
          "enabledForDiskEncryption": false,
          "enableRbacAuthorization": false,
          "accessPolicies": [
            {
              "objectId": "[parameters('clientAppSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('microserviceSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('userSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            }
          ],
          "tenantId": "[subscription().tenantId]",
          "sku": {
            "name": "Standard",
            "family": "A"
          },
          "enableSoftDelete": false,
          "networkAcls": {
            "defaultAction": "Allow",
            "bypass": "AzureServices"
          }
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-id')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppId')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-secret')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppSecret')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-name')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[variables('storageAccountName')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-connection-string')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[concat('DefaultEndpointsProtocol=https;AccountName=', variables('storageAccountName'), ';AccountKey=', listKeys(resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName')), variables('storageAccountApiVersion')).keys[0].value, ';EndpointSuffix=core.windows.net')]"
        }
      }
    ],
    "outputs": {
      "storageAccountName": {
        "type": "string",
        "value": "[variables('storageAccountName')]"
      },
      "keyVaultName": {
        "type": "string",
        "value": "[variables('keyVaultName')]"
      }
    }
  }
"@

try {
  Start-Transcript -path (Join-Path $HOME Provision-FinInsights-Azure.log)
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message

  if ($PSItem.Exception.StackTrace -ne $null)
  {
      Write-Warning $_.Exception.StackTrace
  }

  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}
finally {
  Stop-Transcript
}
```
---

## <a name="configure-the-export-to-data-lake-add-in"></a><span data-ttu-id="b759b-266">Data Lake -viennin lisäosan määritys</span><span class="sxs-lookup"><span data-stu-id="b759b-266">Configure the Export to Data Lake add-in</span></span>

<span data-ttu-id="b759b-267">Voit lisätä Vie Data Lakeen -apuohjelman ympäristöön LCS:n avulla.</span><span class="sxs-lookup"><span data-stu-id="b759b-267">Follow these steps to use LCS to add the Export to Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="b759b-268">KIrjaudu sisään LCS:ään ja valitse sivun oikealla olevan ympäristön nimen alta **Täydet tiedot**.</span><span class="sxs-lookup"><span data-stu-id="b759b-268">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="b759b-269">Valitse **Ympäristöapuohjelmat**-osassa **Asenna uusi apuohjelma**.</span><span class="sxs-lookup"><span data-stu-id="b759b-269">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="b759b-270">Valitse **Vie Data Lakeen** -apuohjelma.</span><span class="sxs-lookup"><span data-stu-id="b759b-270">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="b759b-271">Syötä seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="b759b-271">Enter the following values.</span></span>

    | <span data-ttu-id="b759b-272">Arvo</span><span class="sxs-lookup"><span data-stu-id="b759b-272">Value</span></span>                                                              | <span data-ttu-id="b759b-273">kuvaus</span><span class="sxs-lookup"><span data-stu-id="b759b-273">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="b759b-274">Seb Azure-tilauksen vuokraajan tunnus, jossa avainsäilö sijaitsee</span><span class="sxs-lookup"><span data-stu-id="b759b-274">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="b759b-275">Sen vuokraajan tunnus, jossa tallennustili, sovellukset ja avainsäilöt sijaitsevat.</span><span class="sxs-lookup"><span data-stu-id="b759b-275">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="b759b-276">Jos haluat hankkia tämän arvon, avaa [Azure-portaali](https://portal.azure.com), siirry **Azure Active Directory** -kohtaan ja kopioi **Vuokraajan tunnus** -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="b759b-276">To obtain this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="b759b-277">Anna avainsäilön DNS-nimi</span><span class="sxs-lookup"><span data-stu-id="b759b-277">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="b759b-278">Avainsäilön DNS-nimi, esimerkiksi `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="b759b-278">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> |
    | <span data-ttu-id="b759b-279">Anna salauskoodi, joka sisältää tallennustilin nimen</span><span class="sxs-lookup"><span data-stu-id="b759b-279">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="b759b-280">**tallennustilin nimi**</span><span class="sxs-lookup"><span data-stu-id="b759b-280">**storage-account-name**</span></span> |
    | <span data-ttu-id="b759b-281">Sen sovelluksen tunnuksen salaisen koodin nimi, jonka avulla Data Lakea käytetään</span><span class="sxs-lookup"><span data-stu-id="b759b-281">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="b759b-282">**sovelluksen tunnus**</span><span class="sxs-lookup"><span data-stu-id="b759b-282">**app-id**</span></span> |
    | <span data-ttu-id="b759b-283">Sovellusasiakkaan salasanan salainen nimi</span><span class="sxs-lookup"><span data-stu-id="b759b-283">Secret name for App client secret</span></span>                                  | <span data-ttu-id="b759b-284">**sovelluksen salainen koodi**</span><span class="sxs-lookup"><span data-stu-id="b759b-284">**app-secret**</span></span> |

5. <span data-ttu-id="b759b-285">Hyväksy ehdot ja valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="b759b-285">Agree to the terms, and then select **Install**.</span></span>

<span data-ttu-id="b759b-286">Apuohjelma asennetaan muutamassa minuutissa.</span><span class="sxs-lookup"><span data-stu-id="b759b-286">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-the-finance-insights-add-in"></a><span data-ttu-id="b759b-287">Finance Insights -lisäosan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b759b-287">Configure the Finance insights add-in</span></span>

> [!NOTE]
> <span data-ttu-id="b759b-288">Jos olet aiemmin asentanut Get insights -lisäosan, poista se ennen seuraavia toimia.</span><span class="sxs-lookup"><span data-stu-id="b759b-288">If you previously installed the Get insights add-in, uninstall it before you complete the following procedure.</span></span>

<span data-ttu-id="b759b-289">Noudattamalla näitä ohjeita voit asentaa Finance Insights -lisäosan.</span><span class="sxs-lookup"><span data-stu-id="b759b-289">Follow these steps to install the Finance insights add-in.</span></span>

1. <span data-ttu-id="b759b-290">KIrjaudu sisään LCS:ään ja valitse sivun oikealla olevan ympäristön nimen alta **Täydet tiedot**.</span><span class="sxs-lookup"><span data-stu-id="b759b-290">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="b759b-291">Valitse **Ympäristöapuohjelmat**-osassa **Asenna uusi apuohjelma**.</span><span class="sxs-lookup"><span data-stu-id="b759b-291">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="b759b-292">Valitse **Finance Insights** -lisäosa.</span><span class="sxs-lookup"><span data-stu-id="b759b-292">Select the **Finance insights** add-in.</span></span>
4. <span data-ttu-id="b759b-293">Hyväksy ehdot ja valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="b759b-293">Agree to the terms, and then select **Install**.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="b759b-294">Palaute ja tuki</span><span class="sxs-lookup"><span data-stu-id="b759b-294">Feedback and support</span></span>

<span data-ttu-id="b759b-295">Lähetä sähköpostiviesti [Finance Insights (esiversio) -tiimille](mailto:fiap@microsoft.com), jos haluat antaa palautetta tai tarvitset tukea.</span><span class="sxs-lookup"><span data-stu-id="b759b-295">If you're interested in providing feedback, or if you require support, send an email to [Finance insights (Preview)](mailto:fiap@microsoft.com).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
