---
title: Finance Insightsin määritys (esiversio)
description: Tässä ohjeaiheessa kerrotaan, millaiset määritysvaiheet järjestelmässä on suoritettava, jotta Finance Insightsin ominaisuuksia voi käyttää.
author: ShivamPandey-msft
ms.date: 11/25/2020
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
ms.openlocfilehash: 2443bb057a8b7fe280ed26ecae4e50f671b5e082
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818796"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="4d451-103">Finance Insightsin määritys (esiversio)</span><span class="sxs-lookup"><span data-stu-id="4d451-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4d451-104">Finance Insights yhdistää Microsoft Dynamics 365 Financen toiminnot Microsoft Dataversen, Azuren ja AI Builderin kanssa. Yhdessä nämä tarjoavat tehokkaat ennustetyökalut organisaatiolle.</span><span class="sxs-lookup"><span data-stu-id="4d451-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="4d451-105">Tässä ohjeaiheessa kerrotaan, millaiset määritysvaiheet järjestelmässä on suoritettava, jotta Finance Insightsin ominaisuuksia voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="4d451-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="4d451-106">Dynamics 365 Financen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="4d451-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="4d451-107">Ota ympäristöt käyttöön näiden ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="4d451-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="4d451-108">Luo tai päivitä Dynamics 365 Finance -ympäristö Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="4d451-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="4d451-109">Ympäristö edellyttää, että käytössä on sovellusversio 10.0.11/Platform update 35 -päivitys tai uudempi päivitys.</span><span class="sxs-lookup"><span data-stu-id="4d451-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="4d451-110">Ympäristön on oltava korkean käytettävyyden ympäristö eristysympäristössä.</span><span class="sxs-lookup"><span data-stu-id="4d451-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="4d451-111">(Tämä ympäristötyyppi tunnetaan myös tason 2 ympäristönä.) Lisätietoja on kohdassa [Ympäristön suunnittelu](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="4d451-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="4d451-112">Jos käytössä ovat Contoso-esittelytiedot, asiakkaan maksuennusteiden, kassavirtaennusteiden ja budjettiennusteiden ominaisuuksien käyttäminen edellyttää lisämallitietoja.</span><span class="sxs-lookup"><span data-stu-id="4d451-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="4d451-113">Määritä Dataverse</span><span class="sxs-lookup"><span data-stu-id="4d451-113">Configure Dataverse</span></span>

<span data-ttu-id="4d451-114">Voit tehdä seuraavat manuaaliset määritysvaiheet valmiiksi tai voit nopeuttaa määritysprosessia käyttämällä tarjolla olevaa Windows PowerShell -komentosarjaa.</span><span class="sxs-lookup"><span data-stu-id="4d451-114">You can complete the manual configuration steps that follow, or you can speed up the configuration process by using the Windows PowerShell script that is provided.</span></span> <span data-ttu-id="4d451-115">Kun PowerShell-komentosarja on suoritettu, käytettävissä ovat Finance Insightsin määrityksessä käytettävät arvot.</span><span class="sxs-lookup"><span data-stu-id="4d451-115">When the PowerShell script has finished running, it will give you values to use to configure Finance insights.</span></span> 

> [!NOTE]
> <span data-ttu-id="4d451-116">Suorita komentosarja avaamalla tietokoneen PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4d451-116">Open PowerShell on your PC to run the script.</span></span> <span data-ttu-id="4d451-117">Saatat tarvita PowerShellin version 5.</span><span class="sxs-lookup"><span data-stu-id="4d451-117">You may need PowerShell version 5.</span></span> <span data-ttu-id="4d451-118">Microsoft Azuren CLI:n Kokeile-vaihtoehto ei ehkä toimi.</span><span class="sxs-lookup"><span data-stu-id="4d451-118">The Microsoft Azure CLI "Try it" option may not work.</span></span>

# <a name="manual-configuration-steps"></a>[<span data-ttu-id="4d451-119">Manuaaliset määritysvaiheet</span><span class="sxs-lookup"><span data-stu-id="4d451-119">Manual configuration steps</span></span>](#tab/configuration-steps)

1. <span data-ttu-id="4d451-120">Avaa [Power Platformin hallintakeskus](https://admin.powerplatform.microsoft.com/) ja luo uusi Dataverse -ympäristö samaan Active Directory -vuokraajaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4d451-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="4d451-121">Avaa **Ympäristöt**-sivu.</span><span class="sxs-lookup"><span data-stu-id="4d451-121">Open the **Environments** page.</span></span>

        <span data-ttu-id="4d451-122">[![Ympäristöt-sivu](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="4d451-122">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="4d451-123">Valitse **Uusi ympäristö**.</span><span class="sxs-lookup"><span data-stu-id="4d451-123">Select **New environment**.</span></span>
    3. <span data-ttu-id="4d451-124">Valitse **Tyyppi**-kentässä **Eristys**.</span><span class="sxs-lookup"><span data-stu-id="4d451-124">In the **Type** field, select **Sandbox**.</span></span>
    4. <span data-ttu-id="4d451-125">Määritä **Luo tietokanta** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="4d451-125">Set the **Create Database** option to **Yes**.</span></span>
    5. <span data-ttu-id="4d451-126">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="4d451-126">Select **Next**.</span></span>
    6. <span data-ttu-id="4d451-127">Valitse organisaation kieli ja valuutta.</span><span class="sxs-lookup"><span data-stu-id="4d451-127">Select the language and currency for your organization.</span></span>
    7. <span data-ttu-id="4d451-128">Hyväksy muiden kenttien oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="4d451-128">Accept the default values for the other fields.</span></span>
    8. <span data-ttu-id="4d451-129">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4d451-129">Select **Save**.</span></span>
    9. <span data-ttu-id="4d451-130">Päivitä **Ympäristöt**-sivu.</span><span class="sxs-lookup"><span data-stu-id="4d451-130">Refresh the **Environments** page.</span></span>
    10. <span data-ttu-id="4d451-131">Odota, kunnes **Osavaltio**-kentän arvoksi päivitetään **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="4d451-131">Wait until the value of the **State** field is updated to **Ready**.</span></span>
    11. <span data-ttu-id="4d451-132">Kirjoita Dataverse -organisaation tunnus muistiin.</span><span class="sxs-lookup"><span data-stu-id="4d451-132">Make a note of the Dataverse organization ID.</span></span>
    12. <span data-ttu-id="4d451-133">Valitse ympäristö ja valitse sitten **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="4d451-133">Select the environment, and then select **Settings**.</span></span>
    13. <span data-ttu-id="4d451-134">Valitse **Resurssit \> Kaikki vanhat asetukset**.</span><span class="sxs-lookup"><span data-stu-id="4d451-134">Select **Resources \> All Legacy Settings**.</span></span>
    14. <span data-ttu-id="4d451-135">Valitse yläreunan siirtymispalkissa **Asetukset** ja valitse sitten **Mukautukset**.</span><span class="sxs-lookup"><span data-stu-id="4d451-135">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    15. <span data-ttu-id="4d451-136">Valitse **Kehittäjän resurssit**.</span><span class="sxs-lookup"><span data-stu-id="4d451-136">Select **Developer Resources**.</span></span>
    16. <span data-ttu-id="4d451-137">Määritä **Esiintymän viitetietojen tunnus** -kentän arvoksi sen Dataverse -organisaation tunnuksen arvo, jonka merkitsit muistiin aiemmin.</span><span class="sxs-lookup"><span data-stu-id="4d451-137">Set the **Instance Reference Information ID** field to the Dataverse organization ID value that you made a note of earlier.</span></span>
    17. <span data-ttu-id="4d451-138">Kirjoita selaimen osoitepalkkiin Dataverse -organisaation URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="4d451-138">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="4d451-139">URL-osoite voi olla esimerkiksi `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="4d451-139">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

2. <span data-ttu-id="4d451-140">Jos aiot käyttää kassavirtaennusteiden tai budjettiennusteiden toimintoa, päivitä organsaation huomautusten rajaksi vähintään 50 megatavua (Mt) seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4d451-140">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="4d451-141">Avaa [Power Apps -portaali](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="4d451-141">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="4d451-142">Valitse juuri luotu ympäristö ja valitse sitten **Lisäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="4d451-142">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="4d451-143">Valitse **Asetukset \> Sähköpostimääritykset**.</span><span class="sxs-lookup"><span data-stu-id="4d451-143">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="4d451-144">Muuta **Tiedoston enimmäiskoko** -kentän arvoksi **51 200**.</span><span class="sxs-lookup"><span data-stu-id="4d451-144">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="4d451-145">(Arvo ilmoitetaan kilotavuina \[Kt\].)</span><span class="sxs-lookup"><span data-stu-id="4d451-145">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="4d451-146">Tallenna muutokset valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d451-146">Select **OK** to save your changes.</span></span>

# <a name="windows-powershell-configuration-script"></a>[<span data-ttu-id="4d451-147">Windows PowerShell -määrityskomentosarja</span><span class="sxs-lookup"><span data-stu-id="4d451-147">Windows PowerShell configuration script</span></span>](#tab/powershell-configuration-script)

```azurecli-interactive
Write-Output 'The following modules need to be present for execution of this script:'
Write-Output '  Microsoft.PowerApps.Administration.PowerShell'
Write-Output '  Microsoft.PowerApps.PowerShell'
Write-Output '  Microsoft.Xrm.Tooling.CrmConnector.PowerShell'

try {
    $moduleConsent = Read-Host 'Is it ok to install or update these modules as needed? (yes/no)'
    if ($moduleConsent -ne 'yes' -and $moduleConsent -ne 'y') {
        Write-Warning 'User declined to install required modules.'
        return
    }

    $module = 'Microsoft.PowerApps.Administration.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '2.0.61' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '2.0.61' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.PowerApps.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '1.0.9' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '1.0.9' -AllowClobber -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.Xrm.Tooling.CrmConnector.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '3.3.0.892' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '3.3.0.892' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    Write-Output '================================================================================='

    $useMfa = $false
    $useMfaPrompt = Read-Host "Does your organization require the use of multi-factor authentication? (yes/no)"
    if ($useMfaPrompt -eq 'yes' -or $useMfaPrompt -eq 'y') {
        $useMfa = $true
    }
    if(-not $useMfa) {
        $credential = Get-Credential -Message 'Power Apps Credential'
    }

    $orgFriendlyName = Read-Host "Enter the name of the CDS Organization to use or create: (blank for 'FinanceInsightsOrg')"
    if ($orgFriendlyName.Trim() -eq '') {
        $orgFriendlyName = 'FinanceInsightsOrg'
    }

    $isDefaultOrgPrompt = Read-Host ("Is '" + $orgFriendlyName + "' the default organization for your tenant? (yes/no)")
    if ($isDefaultOrgPrompt -eq 'yes' -or $isDefaultOrgPrompt -eq 'y') {
        $isDefaultOrg = $true
    }

    if ($credential) {
        Add-PowerAppsAccount -Username $credential.UserName -Password $credential.Password
    }
    else {
        Add-PowerAppsAccount
    }

    if ($isDefaultOrg) {
        $orgMatch = ('(default)')
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { $_.IsDefault -eq $true })
    }
    else {
        $orgMatch = ('{0} (*)' -f $orgFriendlyName)
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.IsDefault -eq $false -and ($_.DisplayName -eq $orgFriendlyName -or $_.DisplayName -like $orgMatch)) })
    }

    $getCrmOrgParams = @{ 'OnlineType' = 'Office365' }
    if ($credential) {
        $getCrmOrgParams.Credential = $credential
    }

    if ($null -eq $environment) {
        Write-Output '================================================================================='
        Write-Output 'PowerApps environment not found. A new one will be provisioned.'

        $invalid = 'invalid'

        $location = $invalid
        $cdsLocations = (Get-AdminPowerAppEnvironmentLocations | Select-Object LocationName).LocationName
        while (-not ($location -in $cdsLocations)) {
            $location = (Read-Host -Prompt "Enter the location in which to create the new PowerApps environment: ('help' to see values)")
            if ($location -eq 'help') {
                $cdsLocations
            }
        }

        $currency = $invalid
        $cdsCurrencies = (Get-AdminPowerAppCdsDatabaseCurrencies -Location $location | Select-Object CurrencyName).CurrencyName
        while ($currency -ne '' -and -not ($currency -in $cdsCurrencies)) {
            $currency = (Read-Host -Prompt "Enter the currency to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($currency -eq 'help') {
                $cdsCurrencies
            }
        }

        $language = $invalid
        $cdsLanguages = (Get-AdminPowerAppCdsDatabaseLanguages -Location $location | Select-Object LanguageName, LanguageDisplayName)
        while ($language -ne '' -and -not ($language -in $cdsLanguages.LanguageName)) {
            $language = (Read-Host -Prompt "Enter the language name to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($language -eq 'help') {
                $cdsLanguages | Format-Table -Property LanguageName, LanguageDisplayName
            }
        }

        Write-Output 'Provisioning PowerApps environment. This may take several minutes.'

        $sleep = 15

        $envParams = @{ 'DisplayName' = $orgFriendlyName; 'EnvironmentSku' = 'Sandbox'; 'ProvisionDatabase' = $true; 'Location' = $location; 'WaitUntilFinished' = $true }
        if ($language.Trim() -ne '') {
            $envParams.LanguageName = $language
        }
        if ($currency.Trim() -ne '') {
            $envParams.CurrencyName = $currency
        }
        $newEnvResult = New-AdminPowerAppEnvironment @envParams
        if (($null -eq $newEnvResult) -or ($newEnvResult.CommonDataServiceDatabaseProvisioningState -ne 'Succeeded')) {
            Write-Warning 'Failed to create to PowerApps environment'
            if ($null -ne $newEnvResult) {
                $newEnvResult
            }
        }
        else {
            $environment = $null
            $retryCount = 0
            while (($null -eq $environment) -and ($retryCount -lt 5)) {
                Start-Sleep -Seconds $sleep
                $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.DisplayName -like $orgMatch) })
            }
            Write-Output ("Provisioned PowerApps environment with name: '" + $environment.DisplayName + "'")
        }

        Write-Output 'Waiting for CDS organization provisioning. This may take several minutes.'
        if (-not $credential) {
            $sleep = 120
            Write-Output 'You may be prompted for credentials multiple times while checking the status of the provisioning.'
        }

        while ($null -eq $crmOrg) {
            Start-Sleep -Seconds $sleep
            $crmOrg = (Get-CrmOrganizations @getCrmOrgParams) | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }
    else {
        $crmOrgs = Get-CrmOrganizations @getCrmOrgParams
        if ($UseDefaultOrganization -eq $true) {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -match $orgMatch }
        }
        else {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }

    Write-Output '================================================================================='
    Write-Output 'Values for PowerAI LCS Add-In:'
    Write-Output ("  CDS organization url:             " + $crmOrg.WebApplicationUrl)
    Write-Output ("  CDS organization ID:              " + $crmOrg.OrganizationId)
}
catch {
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $_.Exception.InnerException
    while ($null -ne $inner) {
        Write-Output 'Inner Exception:'
        Write-Error $_.Exception.Message
        Write-Warning $_.Exception.StackTrace
        $inner = $inner.InnerException
    }
}
```
---

## <a name="configure-the-azure-setup"></a><span data-ttu-id="4d451-148">Azure-asetuksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4d451-148">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="4d451-149">Syötä Dataverse -hakemiston tunnus ja käyttäjän Azure AD -objektin tunnus</span><span class="sxs-lookup"><span data-stu-id="4d451-149">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="4d451-150">Syötä Dataverse -hakemiston tunnus seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4d451-150">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="4d451-151">Avaa [Azure-portaali](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="4d451-151">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="4d451-152">Kirjaudu sisään käyttämällä käyttäjätunnusta, jota käytettiin Dataverse -ympäristön luomisessa.</span><span class="sxs-lookup"><span data-stu-id="4d451-152">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="4d451-153">Siirry osoitteeseen **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="4d451-153">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="4d451-154">Kopioi **Vuokraajan tunnus** -arvo.</span><span class="sxs-lookup"><span data-stu-id="4d451-154">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="4d451-155">Syötä Azure Active Directory (Azure AD) -objektin tunnus seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4d451-155">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="4d451-156">Siirry [Azure-portaalissa](https://portal.azure.com) **Käyttäjät**-kohtaan ja hae käyttäjää sähköpostiosoitteen avulla.</span><span class="sxs-lookup"><span data-stu-id="4d451-156">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="4d451-157">Valitse käyttäjän nimi.</span><span class="sxs-lookup"><span data-stu-id="4d451-157">Select the user's name.</span></span>
    3. <span data-ttu-id="4d451-158">Kopioi **Objektin tunnus** -arvo.</span><span class="sxs-lookup"><span data-stu-id="4d451-158">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="4d451-159">Finance Insightsin Data Lake -resurssien määrittäminen Azure Cloud Shellin avulla</span><span class="sxs-lookup"><span data-stu-id="4d451-159">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="4d451-160">Windows PowerShell -komentosarjan käyttäminen</span><span class="sxs-lookup"><span data-stu-id="4d451-160">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="4d451-161">Windows PowerShell -komentosarja on annettu. Voit siis helposti määrittää Azure-resurssit, jotka on esitelty kohdassa [Azure Data Lakeen viennin määrittäminen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake).</span><span class="sxs-lookup"><span data-stu-id="4d451-161">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake).</span></span> <span data-ttu-id="4d451-162">Jos haluat määrittää asetuksen manuaalisesti, ohita nämä vaiheet ja jatka [Manuaalinen määritys](#manual-setup) -osan toimintojen avulla.</span><span class="sxs-lookup"><span data-stu-id="4d451-162">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="4d451-163">Suorita PowerShell -komentosarja alla olevien vaiheiden avulla.</span><span class="sxs-lookup"><span data-stu-id="4d451-163">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="4d451-164">Azure CLI:n Kokeile-vaihtoehto tai komentosarjan suorittaminen tietokoneella eivät ehkä toimi.</span><span class="sxs-lookup"><span data-stu-id="4d451-164">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="4d451-165">Näiden vaiheiden avulla voit määrittää Azuren käyttämällä Windows PowerShell -komentosarjaa.</span><span class="sxs-lookup"><span data-stu-id="4d451-165">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="4d451-166">Tarvitset Azure-resurssiryhmän, Azure-resurssien ja Azure AD -sovelluksen luontioikeudet.</span><span class="sxs-lookup"><span data-stu-id="4d451-166">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="4d451-167">Lisätietoja vaadituista käyttöoikeuksista on kohdassa [Azure AD:n käyttöoikeuksien tarkistaminen](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="4d451-167">For information about the required permissions, see [Check Azure AD permissions](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="4d451-168">Siirry [Azure-portaalissa](https://portal.azure.com) Azuren kohdetilaukseen.</span><span class="sxs-lookup"><span data-stu-id="4d451-168">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="4d451-169">Valitse **Hae**-kentän oikealla puolella oleva **Cloud Shell** -painike.</span><span class="sxs-lookup"><span data-stu-id="4d451-169">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="4d451-170">Valitse **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="4d451-170">Select **PowerShell**.</span></span>
3. <span data-ttu-id="4d451-171">Luo tallennustila, jos sinua kehotetaan tekemään niin.</span><span class="sxs-lookup"><span data-stu-id="4d451-171">Create storage, if you're prompted to do so.</span></span> <span data-ttu-id="4d451-172">Lataa sitten Windows PowerShell -komentosarja istuntoon.</span><span class="sxs-lookup"><span data-stu-id="4d451-172">Then upload the Windows PowerShell script to the session.</span></span>
4. <span data-ttu-id="4d451-173">Suorita komentosarja.</span><span class="sxs-lookup"><span data-stu-id="4d451-173">Run the script.</span></span>
5. <span data-ttu-id="4d451-174">Suorita komentosarja kehotteen ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="4d451-174">Follow the prompts to run the script.</span></span>
6. <span data-ttu-id="4d451-175">Käytä komentosarjan tulosten tietoja ja asenna **Vie Data Lakeen** -apuohjelma LCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="4d451-175">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
7. <span data-ttu-id="4d451-176">Käytä komentosarjan tulosteen tietoja ja ota käyttöön yksikkösäilö Financen **Tietoyhteydet**-sivulla (**Järjestelmän hallinta \> Järjestelmäparametrit \> Tietoyhteydet**).</span><span class="sxs-lookup"><span data-stu-id="4d451-176">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="4d451-177">Manuaalinen määritys</span><span class="sxs-lookup"><span data-stu-id="4d451-177">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="4d451-178">Sovellusten lisääminen Azure AD -vuokraajaan</span><span class="sxs-lookup"><span data-stu-id="4d451-178">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="4d451-179">Siirry [Azure-portaalissa](https://portal.azure.com) **Azure Active Directoryyn**.</span><span class="sxs-lookup"><span data-stu-id="4d451-179">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="4d451-180">Valitse **Hallitse \> Yrityssovellukset**.</span><span class="sxs-lookup"><span data-stu-id="4d451-180">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="4d451-181">Hae seuraavat sovellukset sovellustunnuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="4d451-181">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="4d451-182">Hakemus</span><span class="sxs-lookup"><span data-stu-id="4d451-182">Application</span></span>                              | <span data-ttu-id="4d451-183">Sovelluksen tunnus</span><span class="sxs-lookup"><span data-stu-id="4d451-183">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="4d451-184">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="4d451-184">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="4d451-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="4d451-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="4d451-186">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="4d451-186">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="4d451-187">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="4d451-187">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="4d451-188">AI Builderin todennuspalvelu</span><span class="sxs-lookup"><span data-stu-id="4d451-188">AI Builder Authorization Service</span></span>         | <span data-ttu-id="4d451-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="4d451-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="4d451-190">Jos et löydä ainoatakaan edellisistä sovelluksista, kokeile alla mainittuja vaiheita.</span><span class="sxs-lookup"><span data-stu-id="4d451-190">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="4d451-191">Valitse paikallisessa koneessa **Käynnistä**-valikko ja hae **powershell**.</span><span class="sxs-lookup"><span data-stu-id="4d451-191">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="4d451-192">Valitse ja pidä valittuna (tai valitse hiiren kakkospainikkeella) **Windows PowerShell** ja valitse sitten **Suorita järjestelmänvalvojana**.</span><span class="sxs-lookup"><span data-stu-id="4d451-192">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="4d451-193">Suorita seuraava komento, jos haluat asentaa **AzureAD**-moduulin.</span><span class="sxs-lookup"><span data-stu-id="4d451-193">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="4d451-194">Jos jatkaminen edellyttää, että käytössä on NuGet-palveluntarjoaja, valitse **K** ja asenna se.</span><span class="sxs-lookup"><span data-stu-id="4d451-194">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="4d451-195">Jos näyttöön tulee Ei-luotettava säilö -sanoma, jatka valitsemalla **K**.</span><span class="sxs-lookup"><span data-stu-id="4d451-195">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="4d451-196">Suorita jokaisen lisättävän sovelluksen kohdalla seuraavat komennot ja lisää sovellus Azure AD:hen.</span><span class="sxs-lookup"><span data-stu-id="4d451-196">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="4d451-197">Kun sinua pyydetään kirjautumaan, käytä Azure AD -järjestelmänvalvojan tunnuksia.</span><span class="sxs-lookup"><span data-stu-id="4d451-197">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="4d451-198">Azure-resurssien luominen</span><span class="sxs-lookup"><span data-stu-id="4d451-198">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="4d451-199">Varmista, että luot seuraavat resurssit samassa Azure AD -esiintymässä kuin Dataverse -ympäristön.</span><span class="sxs-lookup"><span data-stu-id="4d451-199">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="4d451-200">Et voi käyttää eri Azure AD -esiintymän resursseja.</span><span class="sxs-lookup"><span data-stu-id="4d451-200">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="4d451-201">Luo uusi tallennustili seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4d451-201">Create a new storage account:</span></span>

    1. <span data-ttu-id="4d451-202">Luo [Azure-portaalissa](https://portal.azure.com) tallennustili.</span><span class="sxs-lookup"><span data-stu-id="4d451-202">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="4d451-203">Määritä **Luo tallennustili** -valintaikkunassa seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="4d451-203">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="4d451-204">**Sijainti** – Valitse palvelinkeskus, jossa ympäristö sijaitsee.</span><span class="sxs-lookup"><span data-stu-id="4d451-204">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="4d451-205">**Suorituskyky** – Suorituskyvyn arvoksi kannattaa valita **Standardi**.</span><span class="sxs-lookup"><span data-stu-id="4d451-205">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="4d451-206">**Tilin tyyppi** – Valitse **TallennustilaV2**.</span><span class="sxs-lookup"><span data-stu-id="4d451-206">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="4d451-207">Valitse **Data Laken tallennustila Gen2** -asetuksen **Lisäasetukset**-valintaikkunassa **Ota käyttöön** **Hierarkkiset nimitilat**-toiminnon alla.</span><span class="sxs-lookup"><span data-stu-id="4d451-207">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="4d451-208">Jos poistat tämän toiminnon käytöstä, et voi käyttää Finance and Operations -sovellusten kirjoittamia tietoja käyttämällä palveluita, kuten Power BI:n tiedonkulkuja.</span><span class="sxs-lookup"><span data-stu-id="4d451-208">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="4d451-209">Valitse **Tarkista ja luo**.</span><span class="sxs-lookup"><span data-stu-id="4d451-209">Select **Review and create**.</span></span> <span data-ttu-id="4d451-210">Kun käyttöönotto on valmis, uusi resurssi näkyy Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="4d451-210">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="4d451-211">Siirry luotuun tallennustiliin.</span><span class="sxs-lookup"><span data-stu-id="4d451-211">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="4d451-212">Valitse vasemmanpuoleisessa valikossa **Käyttöoikeusavaimet**.</span><span class="sxs-lookup"><span data-stu-id="4d451-212">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="4d451-213">Kopioi ja tallenna **Avain1**-tai **Avain2**-kohdan yhteysmerkkijono.</span><span class="sxs-lookup"><span data-stu-id="4d451-213">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="4d451-214">Kopioi ja tallenna tallennustilin nimi.</span><span class="sxs-lookup"><span data-stu-id="4d451-214">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="4d451-215">Luo uusi avainsäilö seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4d451-215">Create a new key vault:</span></span>

    1. <span data-ttu-id="4d451-216">Luo [Azure-portaalissa](https://portal.azure.com) avainsäilö.</span><span class="sxs-lookup"><span data-stu-id="4d451-216">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="4d451-217">Valitse **Sijainti**-kentän **Luo avainsäilö** -valintaikkunassa palvelinkeskus, jossa ympäristö sijaitsee.</span><span class="sxs-lookup"><span data-stu-id="4d451-217">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="4d451-218">Kun avainsäilö on luotu, valitse se luettelosta ja valitse sitten **Salaiset koodit**.</span><span class="sxs-lookup"><span data-stu-id="4d451-218">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="4d451-219">Valitse **Luo tai tuo**.</span><span class="sxs-lookup"><span data-stu-id="4d451-219">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="4d451-220">Valitse **Luo salasana** -valintaikkunan **Lataa asetuksia** -kentässä **Manuaalinen**.</span><span class="sxs-lookup"><span data-stu-id="4d451-220">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="4d451-221">Kirjoita salaisen koodin nimi.</span><span class="sxs-lookup"><span data-stu-id="4d451-221">Enter a name for the secret.</span></span> <span data-ttu-id="4d451-222">Kirjoita nimi muistiin, sillä sinun on annettava se myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="4d451-222">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="4d451-223">Syötä **Arvo**-kenttään yhteysmerkkijono, jonka olet hankkinut edellisen vaiheen tallennustilistä.</span><span class="sxs-lookup"><span data-stu-id="4d451-223">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="4d451-224">Valitse **Käytössä** ja valitse sitten **Luo**.</span><span class="sxs-lookup"><span data-stu-id="4d451-224">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="4d451-225">Salainen koodi luodaan ja lisätään avainsäilöön.</span><span class="sxs-lookup"><span data-stu-id="4d451-225">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="4d451-226">Siirry **Avainsäilön yleiskatsaus** -kohtaan ja merkitse DNS-nimi muistiin.</span><span class="sxs-lookup"><span data-stu-id="4d451-226">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="4d451-227">Luo ja rekisteröi Azure AD -sovellus seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4d451-227">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="4d451-228">Siirry [Azure-portaalissa](https://portal.azure.com) kohtaan **Azure Active Directory** ja valitse **Sovellusten rekisteröinnit**.</span><span class="sxs-lookup"><span data-stu-id="4d451-228">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="4d451-229">Valitse **Uuden sovelluksen rekisteröiminen** ja valitse sitten seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="4d451-229">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="4d451-230">**Nimi** – Anna sovelluksen nimi.</span><span class="sxs-lookup"><span data-stu-id="4d451-230">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="4d451-231">**Sovellustyyppi** – Valitse **Web-ohjelmointirajapinta**.</span><span class="sxs-lookup"><span data-stu-id="4d451-231">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="4d451-232">**Uudelleenohjauksen URI:n määritys** – Anna Dynamics 365 -esiintymän URL-osoite, esimerkiksi `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="4d451-232">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="4d451-233">Siirry juuri luotuun sovellukseen. Kopioi ja tallenna sen **sovelluksen (asiakassovelluksen) tunnuksen** arvo.</span><span class="sxs-lookup"><span data-stu-id="4d451-233">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="4d451-234">Tämä arvo on annettava myöhemmin, kun avainsäilö määritetään.</span><span class="sxs-lookup"><span data-stu-id="4d451-234">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="4d451-235">Siirry **Ohjelmointirajapinnan käyttöoikeudet** -kohtaan ja suorita seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="4d451-235">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="4d451-236">Valitse **Lisää käyttöoikeus**.</span><span class="sxs-lookup"><span data-stu-id="4d451-236">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="4d451-237">Valitse **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="4d451-237">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="4d451-238">Kun olet valinnut delegoidut käyttöoikeudet, valitse **user\_impersonation**.</span><span class="sxs-lookup"><span data-stu-id="4d451-238">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="4d451-239">Valitse **Lisää käyttöoikeudet**.</span><span class="sxs-lookup"><span data-stu-id="4d451-239">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="4d451-240">Valitse sovelluksen valikosta **Sertifikaatit \& salaiset koodit**. Luo sitten avainsäilön salaiset koodit seuraavien vaiheiden avulla:</span><span class="sxs-lookup"><span data-stu-id="4d451-240">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="4d451-241">Valitse **Uusi asiakkaan salainen koodi**.</span><span class="sxs-lookup"><span data-stu-id="4d451-241">Select **New client secret**.</span></span>
        2. <span data-ttu-id="4d451-242">Syötä **Avaimen kuvaus** -kenttään nimi.</span><span class="sxs-lookup"><span data-stu-id="4d451-242">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="4d451-243">Valitse kesto ja valitse sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="4d451-243">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="4d451-244">Salainen koodi luodaan **Arvo**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="4d451-244">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="4d451-245">Kopioi ja tallenna salaisen koodin arvo.</span><span class="sxs-lookup"><span data-stu-id="4d451-245">Copy and save the secret value.</span></span>

4. <span data-ttu-id="4d451-246">Luo avainsäilön salaiset koodit seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4d451-246">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="4d451-247">Siirry aiemmin luotuun avainsäilöön ja valitse **Salaiset koodit**.</span><span class="sxs-lookup"><span data-stu-id="4d451-247">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="4d451-248">Noudata seuraavia vaiheita kunkin seuraavan taulukon salaisen koodin nimen kohdalla:</span><span class="sxs-lookup"><span data-stu-id="4d451-248">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="4d451-249">Valitse **Luo tai tuo**.</span><span class="sxs-lookup"><span data-stu-id="4d451-249">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="4d451-250">Valitse **Luo salasana** -valintaikkunan **Lataa asetuksia** -kentässä **Manuaalinen**.</span><span class="sxs-lookup"><span data-stu-id="4d451-250">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="4d451-251">Luo salaisen koodin nimi ja arvo seuraavasta taulusta.</span><span class="sxs-lookup"><span data-stu-id="4d451-251">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="4d451-252">Valitse **Käytössä** ja valitse sitten **Luo**.</span><span class="sxs-lookup"><span data-stu-id="4d451-252">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="4d451-253">Salainen koodi luodaan ja lisätään avainsäilöön.</span><span class="sxs-lookup"><span data-stu-id="4d451-253">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="4d451-254">Salaisen koodin nimi</span><span class="sxs-lookup"><span data-stu-id="4d451-254">Secret name</span></span>                       | <span data-ttu-id="4d451-255">Salaisen koodin arvo</span><span class="sxs-lookup"><span data-stu-id="4d451-255">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="4d451-256">sovelluksen tunnus</span><span class="sxs-lookup"><span data-stu-id="4d451-256">app-id</span></span>                            | <span data-ttu-id="4d451-257">Aiemmin luodun sovelluksen sovellustunnus</span><span class="sxs-lookup"><span data-stu-id="4d451-257">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="4d451-258">sovelluksen salainen koodi</span><span class="sxs-lookup"><span data-stu-id="4d451-258">app-secret</span></span>                        | <span data-ttu-id="4d451-259">Aiemmin tallennettu asiakkaan salainen koodi</span><span class="sxs-lookup"><span data-stu-id="4d451-259">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="4d451-260">tallennustilin nimi</span><span class="sxs-lookup"><span data-stu-id="4d451-260">storage-account-name</span></span>              | <span data-ttu-id="4d451-261">Aiemmin luodun tallennustilin nimi, kuten **tallennustili1**</span><span class="sxs-lookup"><span data-stu-id="4d451-261">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="4d451-262">tallennustilin yhteysmerkkijono</span><span class="sxs-lookup"><span data-stu-id="4d451-262">storage-account-connection-string</span></span> | <span data-ttu-id="4d451-263">Tallennustilin **Käyttöoikeusavaimet**-sivulta kopioitu yhteysmerkkijono</span><span class="sxs-lookup"><span data-stu-id="4d451-263">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="4d451-264">Anna sovellukselle lupa käyttää avainsäilöä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4d451-264">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="4d451-265">Avaa [Azure-portaalissa](https://portal.azure.com) aiemmin luotu avainsäilö.</span><span class="sxs-lookup"><span data-stu-id="4d451-265">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="4d451-266">Valitse käyttöoikeuskäytännöt.</span><span class="sxs-lookup"><span data-stu-id="4d451-266">Select the access policies.</span></span>
    3. <span data-ttu-id="4d451-267">Noudata seuraavia vaiheita kunkin seuraavan taulukon sovelluksen kohdalla:</span><span class="sxs-lookup"><span data-stu-id="4d451-267">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="4d451-268">Luo käyttöoikeuskäytäntö valitsemalla **Lisää käyttöoikeuskäytäntö**.</span><span class="sxs-lookup"><span data-stu-id="4d451-268">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="4d451-269">Valitse **Salaisen koodin käyttöoikeudet** -kentässä käyttöoikeudet seuraavasta taulukosta.</span><span class="sxs-lookup"><span data-stu-id="4d451-269">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="4d451-270">Hae **Valitse päänimi** -kentässä sovelluksen näyttönimi seuraavasta taulukosta.</span><span class="sxs-lookup"><span data-stu-id="4d451-270">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="4d451-271">Valitse **Valitse**.</span><span class="sxs-lookup"><span data-stu-id="4d451-271">Select **Select**.</span></span>
        5. <span data-ttu-id="4d451-272">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="4d451-272">Select **Add**.</span></span>
        6. <span data-ttu-id="4d451-273">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4d451-273">Select **Save**.</span></span>

        | <span data-ttu-id="4d451-274">Hakemus</span><span class="sxs-lookup"><span data-stu-id="4d451-274">Application</span></span>                                              | <span data-ttu-id="4d451-275">Käyttöoikeudet</span><span class="sxs-lookup"><span data-stu-id="4d451-275">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="4d451-276">Luodun uuden sovelluksen näyttönimi</span><span class="sxs-lookup"><span data-stu-id="4d451-276">The display name of the new application that you created</span></span> | <span data-ttu-id="4d451-277">Hae, Luettelo</span><span class="sxs-lookup"><span data-stu-id="4d451-277">Get, List</span></span>   |
        | <span data-ttu-id="4d451-278">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="4d451-278">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="4d451-279">Hae, Luettelo</span><span class="sxs-lookup"><span data-stu-id="4d451-279">Get, List</span></span>   |

6. <span data-ttu-id="4d451-280">Määritä seuraavasti roolit, jotka käyttävät tallennustiliä:</span><span class="sxs-lookup"><span data-stu-id="4d451-280">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="4d451-281">Avaa [Azure-portaalissa](https://portal.azure.com) aiemmin luotu tallennustili.</span><span class="sxs-lookup"><span data-stu-id="4d451-281">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="4d451-282">Valitse **Käyttöoikeuksien hallinta (IAM)** ja valitse sitten **Roolimääritykset**.</span><span class="sxs-lookup"><span data-stu-id="4d451-282">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="4d451-283">Valitse **Lisää, Lisää roolimääritys**.</span><span class="sxs-lookup"><span data-stu-id="4d451-283">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="4d451-284">Noudata seuraavia vaiheita kunkin seuraavan taulukon sovelluksen kohdalla:</span><span class="sxs-lookup"><span data-stu-id="4d451-284">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="4d451-285">Valitse rooli seuraavasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="4d451-285">Select the role from the following table.</span></span>
        2. <span data-ttu-id="4d451-286">Jätä **Delegoi käyttöoikeus** -kentän arvoksi **Azure AD -käyttäjä, -ryhmä tai -palvelun päänimi** -arvo.</span><span class="sxs-lookup"><span data-stu-id="4d451-286">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="4d451-287">Syötä **Valitse**-kenttään sovellus seuraavasta taulukosta.</span><span class="sxs-lookup"><span data-stu-id="4d451-287">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="4d451-288">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4d451-288">Select **Save**.</span></span>

        | <span data-ttu-id="4d451-289">Hakemus</span><span class="sxs-lookup"><span data-stu-id="4d451-289">Application</span></span>                                              | <span data-ttu-id="4d451-290">Rooli</span><span class="sxs-lookup"><span data-stu-id="4d451-290">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="4d451-291">Luodun uuden sovelluksen näyttönimi</span><span class="sxs-lookup"><span data-stu-id="4d451-291">The display name of the new application that you created</span></span> | <span data-ttu-id="4d451-292">Omistaja</span><span class="sxs-lookup"><span data-stu-id="4d451-292">Owner</span></span>                       |
        | <span data-ttu-id="4d451-293">Luodun uuden sovelluksen näyttönimi</span><span class="sxs-lookup"><span data-stu-id="4d451-293">The display name of the new application that you created</span></span> | <span data-ttu-id="4d451-294">Osallistuja</span><span class="sxs-lookup"><span data-stu-id="4d451-294">Contributor</span></span>                 |
        | <span data-ttu-id="4d451-295">Luodun uuden sovelluksen näyttönimi</span><span class="sxs-lookup"><span data-stu-id="4d451-295">The display name of the new application that you created</span></span> | <span data-ttu-id="4d451-296">Tallennustili - osallistuja</span><span class="sxs-lookup"><span data-stu-id="4d451-296">Storage Account Contributor</span></span> |
        | <span data-ttu-id="4d451-297">Luodun uuden sovelluksen näyttönimi</span><span class="sxs-lookup"><span data-stu-id="4d451-297">The display name of the new application that you created</span></span> | <span data-ttu-id="4d451-298">Tallennustilan blob-objektin tietojen omistaja</span><span class="sxs-lookup"><span data-stu-id="4d451-298">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="4d451-299">**AI Builderin todennuspalvelu**</span><span class="sxs-lookup"><span data-stu-id="4d451-299">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="4d451-300">Tallennustilan blob-objektin tietojen lukija</span><span class="sxs-lookup"><span data-stu-id="4d451-300">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="4d451-301">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="4d451-301">Azure CLI</span></span>](#tab/azure-azure-cli)

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

## <a name="configure-the-entity-store"></a><span data-ttu-id="4d451-302">Yksikkösäilön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4d451-302">Configure the entity store</span></span>

<span data-ttu-id="4d451-303">Näiden vaiheiden avulla voit määrittää Finance-ympäristön yksikkösäilön.</span><span class="sxs-lookup"><span data-stu-id="4d451-303">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="4d451-304">Siirry kohtaan **Järjestelmän hallinta \> Asetukset \> Järjestelmän parametrit \> Tietoyhteydet**.</span><span class="sxs-lookup"><span data-stu-id="4d451-304">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="4d451-305">Määritä **Ota Data Lake -integrointi käyttöön** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="4d451-305">Set the **Enable Data Lake integration** option to **Yes**.</span></span>
3. <span data-ttu-id="4d451-306">Määritä seuraavat avainsäilön kentät:</span><span class="sxs-lookup"><span data-stu-id="4d451-306">Set the following Key Vault fields:</span></span>

    - <span data-ttu-id="4d451-307">**Sovelluksen (asiakkaan) tunnus** – Anna aiemmin luotu sovelluksen asiakastunnus.</span><span class="sxs-lookup"><span data-stu-id="4d451-307">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="4d451-308">**Sovelluksen salainen koodi** – Syötä aiemmin luotu sovellukselle tallennettu salainen koodi.</span><span class="sxs-lookup"><span data-stu-id="4d451-308">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="4d451-309">**DNS-nimi** – DNS (Domain Name System) -nimi löytyy aiemmin luodun sovelluksen sovellustietojen sivulta.</span><span class="sxs-lookup"><span data-stu-id="4d451-309">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="4d451-310">**Salainen koodi** – Syötä **Tallennustilin yhteysmerkkijono**.</span><span class="sxs-lookup"><span data-stu-id="4d451-310">**Secret name** – Enter **storage-account-connection-string**.</span></span>

## <a name="configure-the-data-lake"></a><span data-ttu-id="4d451-311">Data Laken määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4d451-311">Configure the data lake</span></span>

<span data-ttu-id="4d451-312">Voit lisätä Azure Data Laken apuohjelman ympäristöön LCS:n avulla.</span><span class="sxs-lookup"><span data-stu-id="4d451-312">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="4d451-313">KIrjaudu sisään LCS:ään ja valitse sivun oikealla olevan ympäristön nimen alta **Täydet tiedot**.</span><span class="sxs-lookup"><span data-stu-id="4d451-313">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="4d451-314">Valitse **Ympäristöapuohjelmat**-osassa **Asenna uusi apuohjelma**.</span><span class="sxs-lookup"><span data-stu-id="4d451-314">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="4d451-315">Valitse **Vie Data Lakeen** -apuohjelma.</span><span class="sxs-lookup"><span data-stu-id="4d451-315">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="4d451-316">Syötä seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="4d451-316">Enter the following values.</span></span>

    | <span data-ttu-id="4d451-317">Arvo</span><span class="sxs-lookup"><span data-stu-id="4d451-317">Value</span></span>                                                              | <span data-ttu-id="4d451-318">kuvaus</span><span class="sxs-lookup"><span data-stu-id="4d451-318">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="4d451-319">Seb Azure-tilauksen vuokraajan tunnus, jossa avainsäilö sijaitsee</span><span class="sxs-lookup"><span data-stu-id="4d451-319">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="4d451-320">Sen vuokraajan tunnus, jossa tallennustili, sovellukset ja avainsäilöt sijaitsevat.</span><span class="sxs-lookup"><span data-stu-id="4d451-320">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="4d451-321">Jos haluat etsiä tämän arvon, avaa [Azure-portaali](https://portal.azure.com), siirry **Azure Active Directory** -kohtaan ja kopioi **Vuokraajan tunnus** -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="4d451-321">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="4d451-322">Anna avainsäilön DNS-nimi</span><span class="sxs-lookup"><span data-stu-id="4d451-322">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="4d451-323">Avainsäilön DNS-nimi, esimerkiksi `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="4d451-323">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="4d451-324">(Tämä arvo vastaa DNS-nimeä, jota käytetään yksikkösäilössä.)</span><span class="sxs-lookup"><span data-stu-id="4d451-324">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="4d451-325">Anna salauskoodi, joka sisältää tallennustilin nimen</span><span class="sxs-lookup"><span data-stu-id="4d451-325">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="4d451-326">**tallennustilin nimi**</span><span class="sxs-lookup"><span data-stu-id="4d451-326">**storage-account-name**</span></span> |
    | <span data-ttu-id="4d451-327">Sen sovelluksen tunnuksen salaisen koodin nimi, jonka avulla Data Lakea käytetään</span><span class="sxs-lookup"><span data-stu-id="4d451-327">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="4d451-328">**sovelluksen tunnus**</span><span class="sxs-lookup"><span data-stu-id="4d451-328">**app-id**</span></span> |
    | <span data-ttu-id="4d451-329">Sovelluksen tunnuksen kanssa käytettävä salaisen koodin nimi</span><span class="sxs-lookup"><span data-stu-id="4d451-329">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="4d451-330">**sovelluksen salainen koodi**</span><span class="sxs-lookup"><span data-stu-id="4d451-330">**app-secret**</span></span> |

5. <span data-ttu-id="4d451-331">Hyväksy ehdot ja valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="4d451-331">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="4d451-332">Apuohjelma asennetaan muutamassa minuutissa.</span><span class="sxs-lookup"><span data-stu-id="4d451-332">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="4d451-333">AI Builderin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4d451-333">Configure AI Builder</span></span>

1. <span data-ttu-id="4d451-334">Kirjaudu sisään LCS:ään ja avaa **Ympäristön tiedot** -sivu.</span><span class="sxs-lookup"><span data-stu-id="4d451-334">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="4d451-335">Vieritä **Ympäristön lisäosat** -osaan.</span><span class="sxs-lookup"><span data-stu-id="4d451-335">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="4d451-336">Näkyvissä tulisi olla tähän ympäristöön jo asennetut apuohjelmat.</span><span class="sxs-lookup"><span data-stu-id="4d451-336">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="4d451-337">Jos **Vie Data Lakeen** -apuohjelma ei ole näkyvissä, määritä se.</span><span class="sxs-lookup"><span data-stu-id="4d451-337">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="4d451-338">Valitse **Hae tiedot** -apuohjelma.</span><span class="sxs-lookup"><span data-stu-id="4d451-338">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="4d451-339">Syötä **Hae tiedot** -apuohjelman tietojen sivulla seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="4d451-339">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="4d451-340">Arvo</span><span class="sxs-lookup"><span data-stu-id="4d451-340">Value</span></span>                                                    | <span data-ttu-id="4d451-341">kuvaus</span><span class="sxs-lookup"><span data-stu-id="4d451-341">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="4d451-342">CDS-organisaation URL-osoite</span><span class="sxs-lookup"><span data-stu-id="4d451-342">CDS Organization URL</span></span>                                     | <span data-ttu-id="4d451-343">Dataverse -esiintymän Dataverse -organisaation URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="4d451-343">The Dataverse organization URL of the Dataverse instance.</span></span> <span data-ttu-id="4d451-344">Jos haluat löytää tämän arvon, avaa [Power Apps -portaali](https://make.powerapps.com) ja valitse oikeassa yläkulmassa oleva **Asetukset**-painike (ratassymboli). Valitse **Lisäasetukset** ja kopioi URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="4d451-344">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Advanced settings**, and copy the URL.</span></span> <span data-ttu-id="4d451-345">(URL-osoitteen lopussa on merkkijono dynamics.com.)</span><span class="sxs-lookup"><span data-stu-id="4d451-345">(The URL ends with "dynamics.com.")</span></span> |
    | <span data-ttu-id="4d451-346">CDS-organisaation tunnus</span><span class="sxs-lookup"><span data-stu-id="4d451-346">CDS Org ID</span></span>                                               | <span data-ttu-id="4d451-347">Dataverse -esiintymän ympäristön tunnus.</span><span class="sxs-lookup"><span data-stu-id="4d451-347">The environment ID of the Dataverse instance.</span></span> <span data-ttu-id="4d451-348">Jos haluat etsiä tämän arvon, avaa [Power Apps -portaali](https://make.powerapps.com) ja valitse oikeassa yläkulmassa oleva **Asetukset**-painike (ratassymboli) . Valitse **Mukautukset \> Kehittäjän resurssit \> Esiintymän viitetiedot** ja kopioi **Tunnus**-kohdan arvo.</span><span class="sxs-lookup"><span data-stu-id="4d451-348">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Customizations \> Developer resources \> Instance Reference Information**, and copy the **ID** value.</span></span> |
    | <span data-ttu-id="4d451-349">CDS-vuokraajan tunnus (AAD:n hakemistotunnus)</span><span class="sxs-lookup"><span data-stu-id="4d451-349">CDS Tenant ID (Directory ID from AAD)</span></span>               | <span data-ttu-id="4d451-350">Dataverse -esiintymän vuokraajan tunnus.</span><span class="sxs-lookup"><span data-stu-id="4d451-350">The tenant ID of the Dataverse instance.</span></span> <span data-ttu-id="4d451-351">Jos haluat etsiä tämän arvon, avaa [Azure-portaali](https://portal.azure.com), siirry **Azure Active Directory** -kohtaan ja kopioi **Vuokraajan tunnus** -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="4d451-351">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="4d451-352">Anna sen käyttäjäobjektin tunnus, jolla on järjestelmänvalvojan rooli</span><span class="sxs-lookup"><span data-stu-id="4d451-352">Provide user object ID who has system administrator role</span></span> | <span data-ttu-id="4d451-353">Dataverse -käyttäjän Azure AD -käyttäjäobjektin tunnus.</span><span class="sxs-lookup"><span data-stu-id="4d451-353">The Azure AD user object ID of the user in Dataverse.</span></span> <span data-ttu-id="4d451-354">Tämän käyttäjän on oltava Dataverse -esiintymän järjestelmänvalvoja.</span><span class="sxs-lookup"><span data-stu-id="4d451-354">This user must be a system administrator of the Dataverse instance.</span></span> <span data-ttu-id="4d451-355">Jos haluat etsiä tämän arvon, avaa [Azure-portaali](https://portal.azure.com) ja siirry kohtaan **Azure Active Directory \> Käyttäjät**. Valitse käyttäjä ja kopioi **Tunnistetiedot**-osassa **Objektin tunnus** -kohdan arvo.</span><span class="sxs-lookup"><span data-stu-id="4d451-355">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory \> Users**, select the user, and then, in the **Identity** section, copy the **Object ID** value.</span></span> |
    | <span data-ttu-id="4d451-356">Onko tämä CDS:n oletusympäristö vuokralaiselle?</span><span class="sxs-lookup"><span data-stu-id="4d451-356">Is this the default CDS environment for the tenant?</span></span>      | <span data-ttu-id="4d451-357">Jos Dataverse -esiintymä oli ensimmäinen luotu tuotantoesiintymä, valitse tämä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="4d451-357">If the Dataverse instance was the first production instance that was created, select this check box.</span></span> <span data-ttu-id="4d451-358">Jos Dataverse -esiintymä on luotu manuaalisesti, poista tämän valintaruudun valinta.</span><span class="sxs-lookup"><span data-stu-id="4d451-358">If the Dataverse instance was manually created, clear this check box.</span></span> |

## <a name="feedback-and-support"></a><span data-ttu-id="4d451-359">Palaute ja tuki</span><span class="sxs-lookup"><span data-stu-id="4d451-359">Feedback and support</span></span>

<span data-ttu-id="4d451-360">Lähetä sähköpostiviesti [Asiakasmaksujen tiedot (esiversio) -kohteeseen](mailto:fiap@microsoft.com), jos haluat antaa palautetta tai tarvitset tukea.</span><span class="sxs-lookup"><span data-stu-id="4d451-360">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="4d451-361">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="4d451-361">Privacy notice</span></span>

<span data-ttu-id="4d451-362">Esiversiot (1) voivat käyttää vähemmän tietosuojaa ja suojaustoimenpiteitä kuin Dynamics 365 Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) niitä ei ole tarkoitettu henkilötietojen tai muiden sellaisten tietojen käsittelemiseen, joihin liittyy lainsäädännön tai määräysten vaatimustenmukaisuusvaatimuksia ja (4) niillä on rajoitettu tuki.</span><span class="sxs-lookup"><span data-stu-id="4d451-362">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]