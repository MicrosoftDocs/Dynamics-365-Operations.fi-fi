---
title: Finance Insightsin määritys – versiot 10.0.19 asti
description: Tässä ohjeaiheessa kerrotaan, millaiset määritysvaiheet järjestelmässä on suoritettava, jotta Finance Insightsin ominaisuuksia voi käyttää (versioon 10.0.19 asti).
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
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 6ad06bb6d041fc060b3a99538f6d4d0af333180f
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186417"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="da4fc-103">Finance Insightsin määritys (esiversio)</span><span class="sxs-lookup"><span data-stu-id="da4fc-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="da4fc-104">Seuraavat Finance Insightsin määrittämisen menetelmät ovat voimassa Microsoft Dynamics 365 Financelle versioon 10.0.19 asti.</span><span class="sxs-lookup"><span data-stu-id="da4fc-104">The following procedures for setting up Finance insights are valid for Microsoft Dynamics 365 Finance versions up to 10.0.19.</span></span> <span data-ttu-id="da4fc-105">Jos haluat määrittää Finance Insightsin versiolle 10.0.20 tai sitä myöhemmälle versiolle, katso [Finance Insightsin (esiversio) määritys versiosta 10.0.20 eteenpäin](configure-for-fin-insites-PubPrvw.md).</span><span class="sxs-lookup"><span data-stu-id="da4fc-105">To set up Finance insights on version 10.0.20 and later, see [Configuration for Finance Insights (preview) - versions 10.0.20 and beyond](configure-for-fin-insites-PubPrvw.md).</span></span>

<span data-ttu-id="da4fc-106">Finance Insights yhdistää Microsoft Dynamics 365 Financen toiminnot Microsoft Dataversen, Azuren ja AI Builderin kanssa. Yhdessä nämä tarjoavat tehokkaat ennustetyökalut organisaatiolle.</span><span class="sxs-lookup"><span data-stu-id="da4fc-106">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="da4fc-107">Tässä ohjeaiheessa kerrotaan, millaiset määritysvaiheet järjestelmässä on suoritettava, jotta Finance Insightsin ominaisuuksia voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="da4fc-107">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="da4fc-108">Dynamics 365 Financen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="da4fc-108">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="da4fc-109">Ota ympäristöt käyttöön näiden ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="da4fc-109">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="da4fc-110">Luo tai päivitä Dynamics 365 Finance -ympäristö Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="da4fc-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="da4fc-111">Ympäristö edellyttää, että käytössä on sovellusversio 10.0.11/Platform update 35 -päivitys tai uudempi päivitys.</span><span class="sxs-lookup"><span data-stu-id="da4fc-111">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="da4fc-112">Ympäristön on oltava korkean käytettävyyden ympäristö eristysympäristössä.</span><span class="sxs-lookup"><span data-stu-id="da4fc-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="da4fc-113">(Tämä ympäristötyyppi tunnetaan myös tason 2 ympäristönä.) Lisätietoja on kohdassa [Ympäristön suunnittelu](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="da4fc-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="da4fc-114">Jos olet konfiguroimassa Finance Insightsia eristysympäristössä, tuotantotiedot on ehkä kopioitava tähän ympäristöön, jotta ennusteet toimisivat.</span><span class="sxs-lookup"><span data-stu-id="da4fc-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="da4fc-115">Ennustemallissa käytetään useiden vuosien tietoja ennusteiden luomiseen.</span><span class="sxs-lookup"><span data-stu-id="da4fc-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="da4fc-116">Contoso-demotiedot eivät sisällä tarpeeksi historiatietoja ennustemallin kouluttamista varten.</span><span class="sxs-lookup"><span data-stu-id="da4fc-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="da4fc-117">Määritä Dataverse</span><span class="sxs-lookup"><span data-stu-id="da4fc-117">Configure Dataverse</span></span>

<span data-ttu-id="da4fc-118">Seuraavia ohjeita noudattamalla voit määrittää Dataversen Finance Insightsille.</span><span class="sxs-lookup"><span data-stu-id="da4fc-118">Use the following steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="da4fc-119">Avaa ympäristösivu LCS:ssä ja tarkista, että **Power Platform Integrointi** -osa on jo asennettu.</span><span class="sxs-lookup"><span data-stu-id="da4fc-119">Open the environment page in LCS and verify that the **Power Platform Integration** section is already setup.</span></span>
    1. <span data-ttu-id="da4fc-120">Jos se on jo asennettu, Dataverse-ympäristön nimi, joka on linkitetty Dynamics 365 Finance -ympäristöön, pitäisi olla luettelossa.</span><span class="sxs-lookup"><span data-stu-id="da4fc-120">If it is already set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="da4fc-121">Kopioi Dataverse-ympäristön nimi.</span><span class="sxs-lookup"><span data-stu-id="da4fc-121">Copy the Dataverse environment name.</span></span>
    2. <span data-ttu-id="da4fc-122">Jos sitä ei ole määritetty, noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="da4fc-122">If it is not set up, follow these steps:</span></span>
        1. <span data-ttu-id="da4fc-123">Valitse **Asetukset**-painike Power Platform Integrointi -osasta.</span><span class="sxs-lookup"><span data-stu-id="da4fc-123">Select the **Setup** button in the Power Platform Integration section.</span></span> <span data-ttu-id="da4fc-124">Ympäristön määrittäminen voi viedä noin tunnin.</span><span class="sxs-lookup"><span data-stu-id="da4fc-124">It may take up to an hour for the environment to be set up.</span></span>
        2. <span data-ttu-id="da4fc-125">Jos Dataverse-ympäristö on asennettu onnistuneesti, Dataverse-ympäristön nimi, joka on linkitetty Dynamics 365 Finance -ympäristöön, pitäisi olla luettelossa.</span><span class="sxs-lookup"><span data-stu-id="da4fc-125">If the Dataverse environment is successfully set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="da4fc-126">Kopioi Dataverse-ympäristön nimi.</span><span class="sxs-lookup"><span data-stu-id="da4fc-126">Copy the Dataverse environment name.</span></span>
> [!NOTE]
> <span data-ttu-id="da4fc-127">Kun ympäristön määritys on valmis, **ÄLÄ** valitse **Linkitä CDS for Apps** -painiketta.</span><span class="sxs-lookup"><span data-stu-id="da4fc-127">After completing the environment set up, **DO NOT** select the **Link to CDS for Apps** button.</span></span> <span data-ttu-id="da4fc-128">Tätä ei tarvita Finance Insightsissa, ja se poistaa kyvyn suorittaa tarvittavat ympäristön lisäosat LCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="da4fc-128">This is not needed for Finance Insights and will disable the ability to complete the required Environment Add-ins in LCS.</span></span>

2. <span data-ttu-id="da4fc-129">Avaa [Power Platformin hallintakeskus](https://admin.powerplatform.microsoft.com/) ja luo uusi Dataverse -ympäristö samaan Active Directory -vuokraajaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="da4fc-129">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="da4fc-130">Avaa **Ympäristöt**-sivu.</span><span class="sxs-lookup"><span data-stu-id="da4fc-130">Open the **Environments** page.</span></span>

        <span data-ttu-id="da4fc-131">[![Ympäristöt-sivu](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="da4fc-131">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="da4fc-132">Valitse yllä luotu Dataverse-ympäristö ja valitse sitten **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-132">Select the Dataverse environment created above and then select **Settings**.</span></span>
    3. <span data-ttu-id="da4fc-133">Valitse **Resurssit \> Kaikki vanhat asetukset**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-133">Select **Resources \> All Legacy Settings**.</span></span>
    4. <span data-ttu-id="da4fc-134">Valitse yläreunan siirtymispalkissa **Asetukset** ja valitse sitten **Mukautukset**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-134">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    5. <span data-ttu-id="da4fc-135">Valitse **Kehittäjän resurssit**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-135">Select **Developer Resources**.</span></span>
    6. <span data-ttu-id="da4fc-136">Kopioi **Dataverse-organisaation tunnuksen** arvo.</span><span class="sxs-lookup"><span data-stu-id="da4fc-136">Copy the **Dataverse organization ID** value.</span></span>
    7. <span data-ttu-id="da4fc-137">Kirjoita selaimen osoitepalkkiin Dataverse -organisaation URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="da4fc-137">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="da4fc-138">URL-osoite voi olla esimerkiksi `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="da4fc-138">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

3. <span data-ttu-id="da4fc-139">Jos aiot käyttää kassavirtaennusteiden tai budjettiennusteiden toimintoa, päivitä organsaation huomautusten rajaksi vähintään 50 megatavua (Mt) seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="da4fc-139">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="da4fc-140">Avaa [Power Apps -portaali](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="da4fc-140">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="da4fc-141">Valitse juuri luotu ympäristö ja valitse sitten **Lisäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-141">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="da4fc-142">Valitse **Asetukset \> Sähköpostimääritykset**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-142">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="da4fc-143">Muuta **Tiedoston enimmäiskoko** -kentän arvoksi **51 200**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-143">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="da4fc-144">(Arvo ilmoitetaan kilotavuina \[Kt\].)</span><span class="sxs-lookup"><span data-stu-id="da4fc-144">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="da4fc-145">Tallenna muutokset valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-145">Select **OK** to save your changes.</span></span>

## <a name="configure-the-azure-setup"></a><span data-ttu-id="da4fc-146">Azure-asetuksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="da4fc-146">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="da4fc-147">Syötä Dataverse -hakemiston tunnus ja käyttäjän Azure AD -objektin tunnus</span><span class="sxs-lookup"><span data-stu-id="da4fc-147">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="da4fc-148">Syötä Dataverse -hakemiston tunnus seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="da4fc-148">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="da4fc-149">Avaa [Azure-portaali](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="da4fc-149">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="da4fc-150">Kirjaudu sisään käyttämällä käyttäjätunnusta, jota käytettiin Dataverse -ympäristön luomisessa.</span><span class="sxs-lookup"><span data-stu-id="da4fc-150">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="da4fc-151">Siirry osoitteeseen **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-151">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="da4fc-152">Kopioi **Vuokraajan tunnus** -arvo.</span><span class="sxs-lookup"><span data-stu-id="da4fc-152">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="da4fc-153">Syötä Azure Active Directory (Azure AD) -objektin tunnus seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="da4fc-153">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="da4fc-154">Siirry [Azure-portaalissa](https://portal.azure.com) **Käyttäjät**-kohtaan ja hae käyttäjää sähköpostiosoitteen avulla.</span><span class="sxs-lookup"><span data-stu-id="da4fc-154">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="da4fc-155">Valitse käyttäjän nimi.</span><span class="sxs-lookup"><span data-stu-id="da4fc-155">Select the user's name.</span></span>
    3. <span data-ttu-id="da4fc-156">Kopioi **Objektin tunnus** -arvo.</span><span class="sxs-lookup"><span data-stu-id="da4fc-156">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="da4fc-157">Finance Insightsin Data Lake -resurssien määrittäminen Azure Cloud Shellin avulla</span><span class="sxs-lookup"><span data-stu-id="da4fc-157">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="da4fc-158">Windows PowerShell -komentosarjan käyttäminen</span><span class="sxs-lookup"><span data-stu-id="da4fc-158">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="da4fc-159">Windows PowerShell -komentosarja on annettu. Voit siis helposti määrittää Azure-resurssit, jotka on esitelty kohdassa [Azure Data Lakeen viennin määrittäminen](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="da4fc-159">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="da4fc-160">Jos haluat määrittää asetuksen manuaalisesti, ohita nämä vaiheet ja jatka [Manuaalinen määritys](#manual-setup) -osan toimintojen avulla.</span><span class="sxs-lookup"><span data-stu-id="da4fc-160">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="da4fc-161">Suorita PowerShell -komentosarja alla olevien vaiheiden avulla.</span><span class="sxs-lookup"><span data-stu-id="da4fc-161">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="da4fc-162">Azure CLI:n Kokeile-vaihtoehto tai komentosarjan suorittaminen tietokoneella eivät ehkä toimi.</span><span class="sxs-lookup"><span data-stu-id="da4fc-162">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="da4fc-163">Näiden vaiheiden avulla voit määrittää Azuren käyttämällä Windows PowerShell -komentosarjaa.</span><span class="sxs-lookup"><span data-stu-id="da4fc-163">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="da4fc-164">Tarvitset Azure-resurssiryhmän, Azure-resurssien ja Azure AD -sovelluksen luontioikeudet.</span><span class="sxs-lookup"><span data-stu-id="da4fc-164">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="da4fc-165">Lisätietoja vaadituista käyttöoikeuksista on kohdassa [Azure AD:n käyttöoikeuksien tarkistaminen](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="da4fc-165">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="da4fc-166">Siirry [Azure-portaalissa](https://portal.azure.com) Azuren kohdetilaukseen.</span><span class="sxs-lookup"><span data-stu-id="da4fc-166">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="da4fc-167">Valitse **Hae**-kentän oikealla puolella oleva **Cloud Shell** -painike.</span><span class="sxs-lookup"><span data-stu-id="da4fc-167">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="da4fc-168">Valitse **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-168">Select **PowerShell**.</span></span>
3. <span data-ttu-id="da4fc-169">Luo tallennustila, jos sinua kehotetaan tekemään niin.</span><span class="sxs-lookup"><span data-stu-id="da4fc-169">Create storage if you're prompted to do so.</span></span>
4. <span data-ttu-id="da4fc-170">Siirry **Azure CLI** -välilehteen ja valitse **Kopioi**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-170">Go to the **Azure CLI** tab and select **Copy**.</span></span>  
5. <span data-ttu-id="da4fc-171">Avaa Notepad ja liitä PowerShell-komentosarja.</span><span class="sxs-lookup"><span data-stu-id="da4fc-171">Open Notepad and paste the PowerShell script.</span></span> <span data-ttu-id="da4fc-172">Tallenna tiedosto nimellä ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="da4fc-172">Save the file as ConfigureDataLake.ps1.</span></span>
6. <span data-ttu-id="da4fc-173">Lataa Windows PowerShell -komentosarja istuntoon käyttämällä valikkovaihtoehtoa lataamiselle Cloud Shellissä.</span><span class="sxs-lookup"><span data-stu-id="da4fc-173">Upload the Windows PowerShell script to the session using the menu option for upload in Cloud Shell.</span></span>
7. <span data-ttu-id="da4fc-174">Suorita komentosarja .\ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="da4fc-174">Run the script .\ConfigureDataLake.ps1.</span></span>
8. <span data-ttu-id="da4fc-175">Suorita komentosarja kehotteen ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="da4fc-175">Follow the prompts to run the script.</span></span>
9. <span data-ttu-id="da4fc-176">Käytä komentosarjan tulosten tietoja ja asenna **Vie Data Lakeen** -apuohjelma LCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="da4fc-176">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
10. <span data-ttu-id="da4fc-177">Käytä komentosarjan tulosteen tietoja ja ota käyttöön yksikkösäilö Financen **Tietoyhteydet**-sivulla (**Järjestelmän hallinta \> Järjestelmäparametrit \> Tietoyhteydet**).</span><span class="sxs-lookup"><span data-stu-id="da4fc-177">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="da4fc-178">Manuaalinen määritys</span><span class="sxs-lookup"><span data-stu-id="da4fc-178">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="da4fc-179">Sovellusten lisääminen Azure AD -vuokraajaan</span><span class="sxs-lookup"><span data-stu-id="da4fc-179">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="da4fc-180">Siirry [Azure-portaalissa](https://portal.azure.com) **Azure Active Directoryyn**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-180">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="da4fc-181">Valitse **Hallitse \> Yrityssovellukset**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-181">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="da4fc-182">Hae seuraavat sovellukset sovellustunnuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="da4fc-182">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="da4fc-183">Hakemus</span><span class="sxs-lookup"><span data-stu-id="da4fc-183">Application</span></span>                              | <span data-ttu-id="da4fc-184">Sovelluksen tunnus</span><span class="sxs-lookup"><span data-stu-id="da4fc-184">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="da4fc-185">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="da4fc-185">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="da4fc-186">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="da4fc-186">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="da4fc-187">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="da4fc-187">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="da4fc-188">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="da4fc-188">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="da4fc-189">AI Builderin todennuspalvelu</span><span class="sxs-lookup"><span data-stu-id="da4fc-189">AI Builder Authorization Service</span></span>         | <span data-ttu-id="da4fc-190">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="da4fc-190">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="da4fc-191">Jos et löydä ainoatakaan edellisistä sovelluksista, kokeile alla mainittuja vaiheita.</span><span class="sxs-lookup"><span data-stu-id="da4fc-191">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="da4fc-192">Valitse paikallisessa koneessa **Käynnistä**-valikko ja hae **powershell**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-192">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="da4fc-193">Valitse ja pidä valittuna (tai valitse hiiren kakkospainikkeella) **Windows PowerShell** ja valitse sitten **Suorita järjestelmänvalvojana**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-193">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="da4fc-194">Suorita seuraava komento, jos haluat asentaa **AzureAD**-moduulin.</span><span class="sxs-lookup"><span data-stu-id="da4fc-194">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="da4fc-195">Jos jatkaminen edellyttää, että käytössä on NuGet-palveluntarjoaja, valitse **K** ja asenna se.</span><span class="sxs-lookup"><span data-stu-id="da4fc-195">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="da4fc-196">Jos näyttöön tulee Ei-luotettava säilö -sanoma, jatka valitsemalla **K**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-196">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="da4fc-197">Suorita jokaisen lisättävän sovelluksen kohdalla seuraavat komennot ja lisää sovellus Azure AD:hen.</span><span class="sxs-lookup"><span data-stu-id="da4fc-197">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="da4fc-198">Kun sinua pyydetään kirjautumaan, käytä Azure AD -järjestelmänvalvojan tunnuksia.</span><span class="sxs-lookup"><span data-stu-id="da4fc-198">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="da4fc-199">Azure-resurssien luominen</span><span class="sxs-lookup"><span data-stu-id="da4fc-199">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="da4fc-200">Varmista, että luot seuraavat resurssit samassa Azure AD -esiintymässä kuin Dataverse -ympäristön.</span><span class="sxs-lookup"><span data-stu-id="da4fc-200">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="da4fc-201">Et voi käyttää eri Azure AD -esiintymän resursseja.</span><span class="sxs-lookup"><span data-stu-id="da4fc-201">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="da4fc-202">Luo uusi tallennustili seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="da4fc-202">Create a new storage account:</span></span>

    1. <span data-ttu-id="da4fc-203">Luo [Azure-portaalissa](https://portal.azure.com) tallennustili.</span><span class="sxs-lookup"><span data-stu-id="da4fc-203">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="da4fc-204">Määritä **Luo tallennustili** -valintaikkunassa seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="da4fc-204">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="da4fc-205">**Sijainti** – Valitse palvelinkeskus, jossa ympäristö sijaitsee.</span><span class="sxs-lookup"><span data-stu-id="da4fc-205">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="da4fc-206">**Suorituskyky** – Suorituskyvyn arvoksi kannattaa valita **Standardi**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-206">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="da4fc-207">**Tilin tyyppi** – Valitse **TallennustilaV2**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-207">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="da4fc-208">Valitse **Data Laken tallennustila Gen2** -asetuksen **Lisäasetukset**-valintaikkunassa **Ota käyttöön** **Hierarkkiset nimitilat**-toiminnon alla.</span><span class="sxs-lookup"><span data-stu-id="da4fc-208">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="da4fc-209">Jos poistat tämän toiminnon käytöstä, et voi käyttää Finance and Operations -sovellusten kirjoittamia tietoja käyttämällä palveluita, kuten Power BI:n tiedonkulkuja.</span><span class="sxs-lookup"><span data-stu-id="da4fc-209">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="da4fc-210">Valitse **Tarkista ja luo**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-210">Select **Review and create**.</span></span> <span data-ttu-id="da4fc-211">Kun käyttöönotto on valmis, uusi resurssi näkyy Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="da4fc-211">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="da4fc-212">Siirry luotuun tallennustiliin.</span><span class="sxs-lookup"><span data-stu-id="da4fc-212">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="da4fc-213">Valitse vasemmanpuoleisessa valikossa **Käyttöoikeusavaimet**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-213">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="da4fc-214">Kopioi ja tallenna **Avain1**-tai **Avain2**-kohdan yhteysmerkkijono.</span><span class="sxs-lookup"><span data-stu-id="da4fc-214">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="da4fc-215">Kopioi ja tallenna tallennustilin nimi.</span><span class="sxs-lookup"><span data-stu-id="da4fc-215">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="da4fc-216">Luo uusi avainsäilö seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="da4fc-216">Create a new key vault:</span></span>

    1. <span data-ttu-id="da4fc-217">Luo [Azure-portaalissa](https://portal.azure.com) avainsäilö.</span><span class="sxs-lookup"><span data-stu-id="da4fc-217">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="da4fc-218">Valitse **Sijainti**-kentän **Luo avainsäilö** -valintaikkunassa palvelinkeskus, jossa ympäristö sijaitsee.</span><span class="sxs-lookup"><span data-stu-id="da4fc-218">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="da4fc-219">Kun avainsäilö on luotu, valitse se luettelosta ja valitse sitten **Salaiset koodit**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-219">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="da4fc-220">Valitse **Luo tai tuo**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-220">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="da4fc-221">Valitse **Luo salasana** -valintaikkunan **Lataa asetuksia** -kentässä **Manuaalinen**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-221">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="da4fc-222">Kirjoita salaisen koodin nimi.</span><span class="sxs-lookup"><span data-stu-id="da4fc-222">Enter a name for the secret.</span></span> <span data-ttu-id="da4fc-223">Kirjoita nimi muistiin, sillä sinun on annettava se myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="da4fc-223">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="da4fc-224">Syötä **Arvo**-kenttään yhteysmerkkijono, jonka olet hankkinut edellisen vaiheen tallennustilistä.</span><span class="sxs-lookup"><span data-stu-id="da4fc-224">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="da4fc-225">Valitse **Käytössä** ja valitse sitten **Luo**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-225">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="da4fc-226">Salainen koodi luodaan ja lisätään avainsäilöön.</span><span class="sxs-lookup"><span data-stu-id="da4fc-226">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="da4fc-227">Siirry **Avainsäilön yleiskatsaus** -kohtaan ja merkitse DNS-nimi muistiin.</span><span class="sxs-lookup"><span data-stu-id="da4fc-227">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="da4fc-228">Luo ja rekisteröi Azure AD -sovellus seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="da4fc-228">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="da4fc-229">Siirry [Azure-portaalissa](https://portal.azure.com) kohtaan **Azure Active Directory** ja valitse **Sovellusten rekisteröinnit**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-229">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="da4fc-230">Valitse **Uuden sovelluksen rekisteröiminen** ja valitse sitten seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="da4fc-230">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="da4fc-231">**Nimi** – Anna sovelluksen nimi.</span><span class="sxs-lookup"><span data-stu-id="da4fc-231">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="da4fc-232">**Sovellustyyppi** – Valitse **Web-ohjelmointirajapinta**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-232">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="da4fc-233">**Uudelleenohjauksen URI:n määritys** – Anna Dynamics 365 -esiintymän URL-osoite, esimerkiksi `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="da4fc-233">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="da4fc-234">Siirry juuri luotuun sovellukseen. Kopioi ja tallenna sen **sovelluksen (asiakassovelluksen) tunnuksen** arvo.</span><span class="sxs-lookup"><span data-stu-id="da4fc-234">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="da4fc-235">Tämä arvo on annettava myöhemmin, kun avainsäilö määritetään.</span><span class="sxs-lookup"><span data-stu-id="da4fc-235">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="da4fc-236">Siirry **Ohjelmointirajapinnan käyttöoikeudet** -kohtaan ja suorita seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="da4fc-236">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="da4fc-237">Valitse **Lisää käyttöoikeus**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-237">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="da4fc-238">Valitse **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-238">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="da4fc-239">Kun olet valinnut delegoidut käyttöoikeudet, valitse **user\_impersonation**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-239">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="da4fc-240">Valitse **Lisää käyttöoikeudet**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-240">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="da4fc-241">Valitse sovelluksen valikosta **Sertifikaatit \& salaiset koodit**. Luo sitten avainsäilön salaiset koodit seuraavien vaiheiden avulla:</span><span class="sxs-lookup"><span data-stu-id="da4fc-241">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="da4fc-242">Valitse **Uusi asiakkaan salainen koodi**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-242">Select **New client secret**.</span></span>
        2. <span data-ttu-id="da4fc-243">Syötä **Avaimen kuvaus** -kenttään nimi.</span><span class="sxs-lookup"><span data-stu-id="da4fc-243">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="da4fc-244">Valitse kesto ja valitse sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-244">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="da4fc-245">Salainen koodi luodaan **Arvo**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="da4fc-245">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="da4fc-246">Kopioi ja tallenna salaisen koodin arvo.</span><span class="sxs-lookup"><span data-stu-id="da4fc-246">Copy and save the secret value.</span></span>

4. <span data-ttu-id="da4fc-247">Luo avainsäilön salaiset koodit seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="da4fc-247">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="da4fc-248">Siirry aiemmin luotuun avainsäilöön ja valitse **Salaiset koodit**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-248">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="da4fc-249">Noudata seuraavia vaiheita kunkin seuraavan taulukon salaisen koodin nimen kohdalla:</span><span class="sxs-lookup"><span data-stu-id="da4fc-249">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="da4fc-250">Valitse **Luo tai tuo**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-250">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="da4fc-251">Valitse **Luo salasana** -valintaikkunan **Lataa asetuksia** -kentässä **Manuaalinen**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-251">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="da4fc-252">Luo salaisen koodin nimi ja arvo seuraavasta taulusta.</span><span class="sxs-lookup"><span data-stu-id="da4fc-252">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="da4fc-253">Valitse **Käytössä** ja valitse sitten **Luo**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-253">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="da4fc-254">Salainen koodi luodaan ja lisätään avainsäilöön.</span><span class="sxs-lookup"><span data-stu-id="da4fc-254">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="da4fc-255">Salaisen koodin nimi</span><span class="sxs-lookup"><span data-stu-id="da4fc-255">Secret name</span></span>                       | <span data-ttu-id="da4fc-256">Salaisen koodin arvo</span><span class="sxs-lookup"><span data-stu-id="da4fc-256">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="da4fc-257">sovelluksen tunnus</span><span class="sxs-lookup"><span data-stu-id="da4fc-257">app-id</span></span>                            | <span data-ttu-id="da4fc-258">Aiemmin luodun sovelluksen sovellustunnus</span><span class="sxs-lookup"><span data-stu-id="da4fc-258">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="da4fc-259">sovelluksen salainen koodi</span><span class="sxs-lookup"><span data-stu-id="da4fc-259">app-secret</span></span>                        | <span data-ttu-id="da4fc-260">Aiemmin tallennettu asiakkaan salainen koodi</span><span class="sxs-lookup"><span data-stu-id="da4fc-260">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="da4fc-261">tallennustilin nimi</span><span class="sxs-lookup"><span data-stu-id="da4fc-261">storage-account-name</span></span>              | <span data-ttu-id="da4fc-262">Aiemmin luodun tallennustilin nimi, kuten **tallennustili1**</span><span class="sxs-lookup"><span data-stu-id="da4fc-262">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="da4fc-263">tallennustilin yhteysmerkkijono</span><span class="sxs-lookup"><span data-stu-id="da4fc-263">storage-account-connection-string</span></span> | <span data-ttu-id="da4fc-264">Tallennustilin **Käyttöoikeusavaimet**-sivulta kopioitu yhteysmerkkijono</span><span class="sxs-lookup"><span data-stu-id="da4fc-264">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="da4fc-265">Anna sovellukselle lupa käyttää avainsäilöä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="da4fc-265">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="da4fc-266">Avaa [Azure-portaalissa](https://portal.azure.com) aiemmin luotu avainsäilö.</span><span class="sxs-lookup"><span data-stu-id="da4fc-266">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="da4fc-267">Valitse käyttöoikeuskäytännöt.</span><span class="sxs-lookup"><span data-stu-id="da4fc-267">Select the access policies.</span></span>
    3. <span data-ttu-id="da4fc-268">Noudata seuraavia vaiheita kunkin seuraavan taulukon sovelluksen kohdalla:</span><span class="sxs-lookup"><span data-stu-id="da4fc-268">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="da4fc-269">Luo käyttöoikeuskäytäntö valitsemalla **Lisää käyttöoikeuskäytäntö**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-269">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="da4fc-270">Valitse **Salaisen koodin käyttöoikeudet** -kentässä käyttöoikeudet seuraavasta taulukosta.</span><span class="sxs-lookup"><span data-stu-id="da4fc-270">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="da4fc-271">Hae **Valitse päänimi** -kentässä sovelluksen näyttönimi seuraavasta taulukosta.</span><span class="sxs-lookup"><span data-stu-id="da4fc-271">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="da4fc-272">Valitse **Valitse**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-272">Select **Select**.</span></span>
        5. <span data-ttu-id="da4fc-273">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-273">Select **Add**.</span></span>
        6. <span data-ttu-id="da4fc-274">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-274">Select **Save**.</span></span>

        | <span data-ttu-id="da4fc-275">Hakemus</span><span class="sxs-lookup"><span data-stu-id="da4fc-275">Application</span></span>                                              | <span data-ttu-id="da4fc-276">Käyttöoikeudet</span><span class="sxs-lookup"><span data-stu-id="da4fc-276">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="da4fc-277">Luodun uuden sovelluksen näyttönimi</span><span class="sxs-lookup"><span data-stu-id="da4fc-277">The display name of the new application that you created</span></span> | <span data-ttu-id="da4fc-278">Hae, Luettelo</span><span class="sxs-lookup"><span data-stu-id="da4fc-278">Get, List</span></span>   |
        | <span data-ttu-id="da4fc-279">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="da4fc-279">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="da4fc-280">Hae, Luettelo</span><span class="sxs-lookup"><span data-stu-id="da4fc-280">Get, List</span></span>   |

6. <span data-ttu-id="da4fc-281">Määritä seuraavasti roolit, jotka käyttävät tallennustiliä:</span><span class="sxs-lookup"><span data-stu-id="da4fc-281">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="da4fc-282">Avaa [Azure-portaalissa](https://portal.azure.com) aiemmin luotu tallennustili.</span><span class="sxs-lookup"><span data-stu-id="da4fc-282">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="da4fc-283">Valitse **Käyttöoikeuksien hallinta (IAM)** ja valitse sitten **Roolimääritykset**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-283">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="da4fc-284">Valitse **Lisää, Lisää roolimääritys**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-284">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="da4fc-285">Noudata seuraavia vaiheita kunkin seuraavan taulukon sovelluksen kohdalla:</span><span class="sxs-lookup"><span data-stu-id="da4fc-285">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="da4fc-286">Valitse rooli seuraavasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="da4fc-286">Select the role from the following table.</span></span>
        2. <span data-ttu-id="da4fc-287">Jätä **Delegoi käyttöoikeus** -kentän arvoksi **Azure AD -käyttäjä, -ryhmä tai -palvelun päänimi** -arvo.</span><span class="sxs-lookup"><span data-stu-id="da4fc-287">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="da4fc-288">Syötä **Valitse**-kenttään sovellus seuraavasta taulukosta.</span><span class="sxs-lookup"><span data-stu-id="da4fc-288">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="da4fc-289">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-289">Select **Save**.</span></span>

        | <span data-ttu-id="da4fc-290">Hakemus</span><span class="sxs-lookup"><span data-stu-id="da4fc-290">Application</span></span>                                              | <span data-ttu-id="da4fc-291">Rooli</span><span class="sxs-lookup"><span data-stu-id="da4fc-291">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="da4fc-292">Luodun uuden sovelluksen näyttönimi</span><span class="sxs-lookup"><span data-stu-id="da4fc-292">The display name of the new application that you created</span></span> | <span data-ttu-id="da4fc-293">Omistaja</span><span class="sxs-lookup"><span data-stu-id="da4fc-293">Owner</span></span>                       |
        | <span data-ttu-id="da4fc-294">Luodun uuden sovelluksen näyttönimi</span><span class="sxs-lookup"><span data-stu-id="da4fc-294">The display name of the new application that you created</span></span> | <span data-ttu-id="da4fc-295">Osallistuja</span><span class="sxs-lookup"><span data-stu-id="da4fc-295">Contributor</span></span>                 |
        | <span data-ttu-id="da4fc-296">Luodun uuden sovelluksen näyttönimi</span><span class="sxs-lookup"><span data-stu-id="da4fc-296">The display name of the new application that you created</span></span> | <span data-ttu-id="da4fc-297">Tallennustili - osallistuja</span><span class="sxs-lookup"><span data-stu-id="da4fc-297">Storage Account Contributor</span></span> |
        | <span data-ttu-id="da4fc-298">Luodun uuden sovelluksen näyttönimi</span><span class="sxs-lookup"><span data-stu-id="da4fc-298">The display name of the new application that you created</span></span> | <span data-ttu-id="da4fc-299">Tallennustilan blob-objektin tietojen omistaja</span><span class="sxs-lookup"><span data-stu-id="da4fc-299">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="da4fc-300">**AI Builderin todennuspalvelu**</span><span class="sxs-lookup"><span data-stu-id="da4fc-300">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="da4fc-301">Tallennustilan blob-objektin tietojen lukija</span><span class="sxs-lookup"><span data-stu-id="da4fc-301">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="da4fc-302">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="da4fc-302">Azure CLI</span></span>](#tab/azure-azure-cli)

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



## <a name="configure-the-data-lake"></a><span data-ttu-id="da4fc-303">Data Laken määrittäminen</span><span class="sxs-lookup"><span data-stu-id="da4fc-303">Configure the data lake</span></span>

<span data-ttu-id="da4fc-304">Voit lisätä Azure Data Laken apuohjelman ympäristöön LCS:n avulla.</span><span class="sxs-lookup"><span data-stu-id="da4fc-304">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="da4fc-305">KIrjaudu sisään LCS:ään ja valitse sivun oikealla olevan ympäristön nimen alta **Täydet tiedot**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-305">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="da4fc-306">Valitse **Ympäristöapuohjelmat**-osassa **Asenna uusi apuohjelma**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-306">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="da4fc-307">Valitse **Vie Data Lakeen** -apuohjelma.</span><span class="sxs-lookup"><span data-stu-id="da4fc-307">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="da4fc-308">Syötä seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="da4fc-308">Enter the following values.</span></span>

    | <span data-ttu-id="da4fc-309">Arvo</span><span class="sxs-lookup"><span data-stu-id="da4fc-309">Value</span></span>                                                              | <span data-ttu-id="da4fc-310">kuvaus</span><span class="sxs-lookup"><span data-stu-id="da4fc-310">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="da4fc-311">Seb Azure-tilauksen vuokraajan tunnus, jossa avainsäilö sijaitsee</span><span class="sxs-lookup"><span data-stu-id="da4fc-311">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="da4fc-312">Sen vuokraajan tunnus, jossa tallennustili, sovellukset ja avainsäilöt sijaitsevat.</span><span class="sxs-lookup"><span data-stu-id="da4fc-312">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="da4fc-313">Jos haluat etsiä tämän arvon, avaa [Azure-portaali](https://portal.azure.com), siirry **Azure Active Directory** -kohtaan ja kopioi **Vuokraajan tunnus** -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="da4fc-313">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="da4fc-314">Anna avainsäilön DNS-nimi</span><span class="sxs-lookup"><span data-stu-id="da4fc-314">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="da4fc-315">Avainsäilön DNS-nimi, esimerkiksi `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="da4fc-315">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="da4fc-316">(Tämä arvo vastaa DNS-nimeä, jota käytetään yksikkösäilössä.)</span><span class="sxs-lookup"><span data-stu-id="da4fc-316">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="da4fc-317">Anna salauskoodi, joka sisältää tallennustilin nimen</span><span class="sxs-lookup"><span data-stu-id="da4fc-317">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="da4fc-318">**tallennustilin nimi**</span><span class="sxs-lookup"><span data-stu-id="da4fc-318">**storage-account-name**</span></span> |
    | <span data-ttu-id="da4fc-319">Sen sovelluksen tunnuksen salaisen koodin nimi, jonka avulla Data Lakea käytetään</span><span class="sxs-lookup"><span data-stu-id="da4fc-319">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="da4fc-320">**sovelluksen tunnus**</span><span class="sxs-lookup"><span data-stu-id="da4fc-320">**app-id**</span></span> |
    | <span data-ttu-id="da4fc-321">Sovelluksen tunnuksen kanssa käytettävä salaisen koodin nimi</span><span class="sxs-lookup"><span data-stu-id="da4fc-321">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="da4fc-322">**sovelluksen salainen koodi**</span><span class="sxs-lookup"><span data-stu-id="da4fc-322">**app-secret**</span></span> |

5. <span data-ttu-id="da4fc-323">Hyväksy ehdot ja valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-323">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="da4fc-324">Apuohjelma asennetaan muutamassa minuutissa.</span><span class="sxs-lookup"><span data-stu-id="da4fc-324">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="da4fc-325">AI Builderin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="da4fc-325">Configure AI Builder</span></span>

1. <span data-ttu-id="da4fc-326">Kirjaudu sisään LCS:ään ja avaa **Ympäristön tiedot** -sivu.</span><span class="sxs-lookup"><span data-stu-id="da4fc-326">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="da4fc-327">Vieritä **Ympäristön lisäosat** -osaan.</span><span class="sxs-lookup"><span data-stu-id="da4fc-327">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="da4fc-328">Näkyvissä tulisi olla tähän ympäristöön jo asennetut apuohjelmat.</span><span class="sxs-lookup"><span data-stu-id="da4fc-328">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="da4fc-329">Jos **Vie Data Lakeen** -apuohjelma ei ole näkyvissä, määritä se.</span><span class="sxs-lookup"><span data-stu-id="da4fc-329">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="da4fc-330">Valitse **Hae tiedot** -apuohjelma.</span><span class="sxs-lookup"><span data-stu-id="da4fc-330">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="da4fc-331">Syötä **Hae tiedot** -apuohjelman tietojen sivulla seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="da4fc-331">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="da4fc-332">Arvo</span><span class="sxs-lookup"><span data-stu-id="da4fc-332">Value</span></span>                                                    | <span data-ttu-id="da4fc-333">kuvaus</span><span class="sxs-lookup"><span data-stu-id="da4fc-333">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="da4fc-334">CDS-organisaation URL-osoite</span><span class="sxs-lookup"><span data-stu-id="da4fc-334">CDS Organization URL</span></span>                                     | <span data-ttu-id="da4fc-335">Dataverse-organisaation URL-osoite, joka on kopioitu yllä olevasta kohteesta.</span><span class="sxs-lookup"><span data-stu-id="da4fc-335">The Dataverse organization URL copied from above.</span></span> |
    | <span data-ttu-id="da4fc-336">CDS-organisaation tunnus</span><span class="sxs-lookup"><span data-stu-id="da4fc-336">CDS Org ID</span></span>                                               | <span data-ttu-id="da4fc-337">Dataverse-organisaation tunnus, joka on kopioitu yllä olevasta kohteesta.</span><span class="sxs-lookup"><span data-stu-id="da4fc-337">The Dataverse organization ID copied from above.</span></span> |
5. <span data-ttu-id="da4fc-338">Ota käyttöön **Onko tämä oletusympäristö vuokralaiselle**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-338">Enable **Is this the default environment for you Tenant**.</span></span>
    
## <a name="configure-the-entity-store"></a><span data-ttu-id="da4fc-339">Yksikkösäilön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="da4fc-339">Configure the entity store</span></span>

<span data-ttu-id="da4fc-340">Näiden vaiheiden avulla voit määrittää Finance-ympäristön yksikkösäilön.</span><span class="sxs-lookup"><span data-stu-id="da4fc-340">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="da4fc-341">Siirry kohtaan **Järjestelmän hallinta \> Asetukset \> Järjestelmän parametrit \> Tietoyhteydet**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-341">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="da4fc-342">Määritä seuraavat avainsäilön kentät:</span><span class="sxs-lookup"><span data-stu-id="da4fc-342">Set the following key vault fields:</span></span>

    - <span data-ttu-id="da4fc-343">**Sovelluksen (asiakkaan) tunnus** – Anna aiemmin luotu sovelluksen asiakastunnus.</span><span class="sxs-lookup"><span data-stu-id="da4fc-343">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="da4fc-344">**Sovelluksen salainen koodi** – Syötä aiemmin luotu sovellukselle tallennettu salainen koodi.</span><span class="sxs-lookup"><span data-stu-id="da4fc-344">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="da4fc-345">**DNS-nimi** – DNS (Domain Name System) -nimi löytyy aiemmin luodun sovelluksen sovellustietojen sivulta.</span><span class="sxs-lookup"><span data-stu-id="da4fc-345">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="da4fc-346">**Salainen koodi** – Syötä **Tallennustilin yhteysmerkkijono**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-346">**Secret name** – Enter **storage-account-connection-string**.</span></span>
3. <span data-ttu-id="da4fc-347">Ota käyttöön **Ota Data Lake -integrointi käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="da4fc-347">Enable **Enable Data Lake integration**.</span></span>
4. <span data-ttu-id="da4fc-348">Valitse **Testaa Azure Key Vault** ja tarkista, ettei siinä ole virheitä.</span><span class="sxs-lookup"><span data-stu-id="da4fc-348">Select **Test Azure Key Vault** and verify there are no errors.</span></span>
5. <span data-ttu-id="da4fc-349">Valitse **Testaa Azure-tallennustila** ja tarkista, ettei siinä ole virheitä.</span><span class="sxs-lookup"><span data-stu-id="da4fc-349">Select **Test Azure storage** and verify there are no errors.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="da4fc-350">Palaute ja tuki</span><span class="sxs-lookup"><span data-stu-id="da4fc-350">Feedback and support</span></span>

<span data-ttu-id="da4fc-351">Lähetä sähköpostiviesti [Asiakasmaksujen tiedot (esiversio) -kohteeseen](mailto:fiap@microsoft.com), jos haluat antaa palautetta tai tarvitset tukea.</span><span class="sxs-lookup"><span data-stu-id="da4fc-351">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="da4fc-352">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="da4fc-352">Privacy notice</span></span>

<span data-ttu-id="da4fc-353">Esiversiot (1) voivat käyttää vähemmän tietosuojaa ja suojaustoimenpiteitä kuin Dynamics 365 Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) niitä ei ole tarkoitettu henkilötietojen tai muiden sellaisten tietojen käsittelemiseen, joihin liittyy lainsäädännön tai määräysten vaatimustenmukaisuusvaatimuksia ja (4) niillä on rajoitettu tuki.</span><span class="sxs-lookup"><span data-stu-id="da4fc-353">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
