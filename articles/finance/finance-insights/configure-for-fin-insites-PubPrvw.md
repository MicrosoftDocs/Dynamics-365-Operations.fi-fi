---
title: Finance Insightsin määritys – versio 10.0.20 ja myöhempi
description: Tässä artikkelissa kerrotaan, millaiset määritysvaiheet järjestelmässä on suoritettava, jotta Finance Insightsin version ominaisuuksia voi käyttää (versiossa 10.0.20 ja sitä uudemmissa).
author: ShivamPandey-msft
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex,nofollow
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: d05403113c9b178553134ce1a9066bb2acf59b0f
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068102"
---
# <a name="configuration-for-finance-insights---version-10020-and-later"></a>Finance Insightsin määritys – versio 10.0.20 ja myöhempi

[!include [banner](../includes/banner.md)]



Finance Insights yhdistää Microsoft Dynamics 365 Financen toiminnot Dataversen, Azuren ja AI Builderin kanssa. Yhdessä nämä tarjoavat tehokkaat ennustetyökalut organisaatiolle. Tässä artikkelissa kerrotaan, millaiset määritysvaiheet Dynamics 365 Finance -versiossa 10.0.20 on suoritettava, jotta Finance Insightsin ominaisuuksia voi käyttää.

> [!NOTE]
> Tässä artikkelissa kuvatut konfigurointivaiheet koskevat vain Finance-versiota 10.0.20 ja sitä myöhempiä. Jos haluat määrittää Finance Insightsin versiolle 10.0.19 tai sitä aikaisemmalle versiolle, katso [Finance Insightsin määritys versioon 10.0.19 asti](configure-for-fin-insites.md).

## <a name="deploy-finance"></a>Ota Finance käyttöön

Määritä ympäristöt näiden ohjeiden avulla.

1. Luo tai päivitä Finance-ympäristö Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa. Ympäristö edellyttää talous- ja toimintosovellusten sovellusversiota 10.0.20 tai uudempaa.
2. Ympäristön on oltava korkean käytettävyyden ympäristö eristysympäristössä. (Tämä ympäristötyyppi tunnetaan myös tason 2 ympäristönä.) Lisätietoja on kohdassa [Ympäristön suunnittelu](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. Jos olet konfiguroimassa Finance Insightsia eristysympäristössä, tuotantotiedot on ehkä kopioitava tähän ympäristöön, jotta ennusteet toimisivat. Ennustemallissa käytetään useiden vuosien tietoja ennusteiden luomiseen. Contoso-esittelytiedot eivät sisällä riittävästi historiatietoja ennustemallin kouluttamiseen. 

## <a name="configure-dataverse"></a>Määritä Dataverse

Näitä ohjeita noudattamalla voit määrittää Dataversen Finance Insightsille.

1. Avaa ympäristösivu LCS:ssä ja tarkista, että **Power Platform -integrointi** -osa on jo asennettu.

    - Jos se on jo asennettu, Dataverse-ympäristön nimi, joka on linkitetty Finance-ympäristöön, pitäisi olla luettelossa.
    - Jos sitä ei ole määritetty, noudata seuraavia ohjeita:

        1. Valitse **Määritys** **Power Platform -integrointi** -osasta. Ympäristön määrittäminen voi kestää noin tunnin.
        2. Jos Dataverse-ympäristö on asennettu onnistuneesti, Dataverse-ympäristön nimi, joka on linkitetty Finance-ympäristöön, pitäisi olla luettelossa.

        > [!NOTE]
        > Kun olet suorittanut ympäristöasetukset, **älä** valitse kohtaa **CDS for Apps**. Tätä painiketta ei tarvita Finance Insightsissa. Jos valitset sen, et voi määrittää pakollisia ympäristön lisäosia LCS:ssä.

## <a name="configure-azure"></a>Konfiguroi Azure

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>Finance Insightsin Data Lake -resurssien määrittäminen Azure Cloud Shellin avulla

# <a name="use-a-windows-powershell-script"></a>[Windows PowerShell -komentosarjan käyttäminen](#tab/use-a-powershell-script)

Windows PowerShell -komentosarja on annettu. Voit siis helposti määrittää Azure-resurssit, jotka on esitelty kohdassa [Azure Data Lakeen viennin määrittäminen](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md). Jos haluat määrittää asetuksen manuaalisesti, ohita nämä vaiheet ja suorita [Manuaalinen määritys](#manual-setup) -osan prosessia.

> [!NOTE]
> Suorita Windows PowerShell -komentotiedosto seuraavia ohjeita noudattamalla. Asennus ei ehkä toimi, jos käytät **Kokeile** -valintaa Azure CLI:ssä tai jos suoritat komentosarjan tietokoneessa.

Näiden vaiheiden avulla voit määrittää Azuren käyttämällä Windows PowerShell -komentosarjaa. Tarvitset Azure-resurssiryhmän, Azure-resurssien ja Azure AD -sovelluksen luontioikeudet. Lisätietoja vaadituista käyttöoikeuksista on kohdassa [Azure AD:n käyttöoikeuksien tarkistaminen](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. Siirry [Azure-portaalissa](https://portal.azure.com) Azuren kohdetilaukseen.
2. Valitse **Hae**-kentän oikealla puolella oleva **Cloud Shell** -kohta.
3. Valitse **PowerShell**.
4. Luo tallennustila, jos sinua kehotetaan tekemään niin.
5. Valitse **Azure CLI** -välilehdessä **Kopioi**.
6. Avaa Muistiossa uusi tiedosto ja liitä Windows PowerShell -komentosarja.
7. Tallenna tiedosto nimellä **ConfigureDataLake.ps1**.
8. Lataa Windows PowerShell -komentosarja istuntoon käyttämällä valikkovaihtoehtoa lataamiselle Cloud Shellissä.
9. Suorita komentosarja **.\ConfigureDataLake.ps1**.
10. Suorita komentosarja kehotteen ohjeiden avulla.
11. Käytä komentosarjan tulosten tietoja ja asenna Vie Data Lakeen -apuohjelma LCS:ssä.

### <a name="manual-setup"></a>Manuaalinen määritys

#### <a name="add-applications-to-the-azure-ad-tenant"></a>Sovellusten lisääminen Azure AD -vuokraajaan

1. Siirry [Azure-portaalissa](https://portal.azure.com) **Azure Active Directoryyn**.
2. Valitse **Hallitse \> Yrityssovellukset**.
3. Hae seuraavat sovellukset sovellustunnuksen avulla.

    | Hakemus                              | Sovelluksen tunnus                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP Microservices     | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
    | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    | AI Builderin todennuspalvelu         | ad40333e-9910-4b61-b281-e3aeeb8c3ef3 |

Jos et löydä ainoatakaan edellisistä sovelluksista, kokeile alla mainittuja vaiheita.

1. Valitse paikallisessa tietokoneessa **Käynnistä**-valikko ja hae **powershell**.
2. Valitse ja pidä valittuna (tai valitse hiiren kakkospainikkeella) **Windows PowerShell** ja valitse sitten **Suorita järjestelmänvalvojana**.
3. Suorita seuraava komento, jos haluat asentaa **AzureAD**-moduulin.

    `Install-Module -Name AzureAD`

4. Jos jatkaminen edellyttää, että käytössä on NuGet-palveluntarjoaja, valitse **K** ja asenna se.
5. Jos näyttöön tulee Ei-luotettava säilö -sanoma, jatka valitsemalla **K**.
6. Suorita jokaisen lisättävän sovelluksen kohdalla seuraavat komennot ja lisää sovellus Azure AD:hen. Kun sinua pyydetään kirjautumaan, käytä Azure AD -järjestelmänvalvojan tunnuksia.

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>Azure-resurssien luominen

> [!NOTE]
> Varmista, että luot seuraavat resurssit samassa Azure AD -esiintymässä kuin missä Dataverse -ympäristö on. Et voi käyttää eri Azure AD -esiintymän resursseja.

1. Luo tallennustili seuraavasti:

    1. Luo [Azure-portaalissa](https://portal.azure.com) tallennustili.
    2. Määritä **Luo tallennustili** -valintaikkunassa seuraavat kentät:

        - **Sijainti** – Valitse palvelinkeskus, jossa ympäristö sijaitsee.
        - **Suorituskyky** – Suorituskyvyn arvoksi kannattaa valita **Standardi**.
        - **Tilin tyyppi** – Valitse **TallennustilaV2**.

    3. Valitse **Data Laken tallennustila Gen2** -asetuksen **Lisäasetukset**-valintaikkunassa **Ota käyttöön** **Hierarkkiset nimitilat**-toiminnon alla. Jos et ota tätä toimintoa käyttöön, et voi käyttää talous- ja toimintosovellusten kirjoittamia tietoja käyttämällä palveluita, kuten Power BI:n tietovoita.
    4. Valitse **Tarkista ja luo**. Kun käyttöönotto on valmis, uusi resurssi näkyy Azure-portaalissa.
    5. Siirry luotuun tallennustiliin.
    6. Valitse vasemmanpuoleisessa valikossa **Käyttöoikeusavaimet**.
    7. Kopioi ja tallenna tallennustilin nimi. Tämä arvo on annettava myöhemmin, kun avainsäilön salasana määritetään.

2. Luo avainsäilö seuraavasti:

    1. Luo [Azure-portaalissa](https://portal.azure.com) avainsäilö.
    2. Valitse **Sijainti**-kentän **Luo avainsäilö** -valintaikkunassa palvelinkeskus, jossa ympäristö sijaitsee.
    3. Kun olet luonut avainsäilön, siirry kohtaan **Avainsäilön yhteenveto** ja kopioi ja tallenna DNS-nimi. Tämä arvo on annettava myöhemmin, kun Data Laken lisäosa määritetään.

3. Luo ja rekisteröi Azure AD -sovellus seuraavasti:

    1. Siirry [Azure-portaalissa](https://portal.azure.com) kohtaan **Azure Active Directory** ja valitse **Sovellusten rekisteröinnit**.
    2. Valitse **Uuden sovelluksen rekisteröiminen** ja valitse sitten seuraavat kentät:

        - **Nimi** – Anna sovelluksen nimi.
        - **Sovellustyyppi** – Valitse **Web-ohjelmointirajapinta**.
        - **Uudelleenohjauksen URI:n määritys** – Anna Dynamics 365 -esiintymän URL-osoite, esimerkiksi `https://yourdynamicsinstance.dynamics.com/auth`.

    3. Siirry juuri luotuun sovellukseen. Kopioi ja tallenna sen **sovelluksen (asiakassovelluksen) tunnuksen** arvo. Tämä arvo on annettava myöhemmin, kun avainsäilön salasana määritetään.
    4. Siirry **Ohjelmointirajapinnan käyttöoikeudet** -kohtaan ja suorita seuraavat vaiheet:

        1. Valitse **Lisää käyttöoikeus**.
        2. Valitse **Azure Key Vault**.
        3. Kun olet valinnut delegoidut käyttöoikeudet, valitse **user\_impersonation**.
        4. Valitse **Lisää käyttöoikeudet**.

    5. Valitse sovelluksen valikosta **Sertifikaatit \& salaiset koodit**. Luo sitten avainsäilön salaiset koodit seuraavien vaiheiden avulla:

        1. Valitse **Uusi asiakkaan salainen koodi**.
        2. Syötä **Avaimen kuvaus** -kenttään nimi.
        3. Valitse kesto ja valitse sitten **Lisää**. Salainen koodi luodaan **Arvo**-kentässä.
        4. Kopioi ja tallenna asiakasohjelman salasanan arvo. Tämä arvo on annettava myöhemmin, kun avainsäilön salasana määritetään.

4. Luo avainsäilön salaiset koodit seuraavasti:

    1. Siirry aiemmin luotuun avainsäilöön ja valitse **Salaiset koodit**.
    2. Noudata seuraavia vaiheita kunkin seuraavan taulukon salaisen koodin nimen kohdalla:

        1. Valitse **Luo tai tuo**.
        2. Valitse **Luo salasana** -valintaikkunan **Lataa asetuksia** -kentässä **Manuaalinen**.
        3. Luo salaisen koodin nimi ja arvo taulusta.
        4. Valitse **Käytössä** ja valitse sitten **Luo**. Salainen koodi luodaan ja lisätään avainsäilöön.

        | Salaisen koodin nimi                       | Salaisen koodin arvo                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | sovelluksen tunnus                            | Aiemmin luodun sovelluksen sovellustunnus.                                      |
        | sovelluksen salainen koodi                        | Aiemmin tallennettu asiakkaan salainen koodi.                                                    |
        | tallennustilin nimi              | Aiemmin luodun tallennustilin nimi, kuten **tallennustili1**.       |

5. Anna sovellukselle lupa käyttää avainsäilöä seuraavasti:

    1. Avaa [Azure-portaalissa](https://portal.azure.com) aiemmin luotu avainsäilö.
    2. Valitse käyttöoikeuskäytännöt.
    3. Noudata seuraavia vaiheita kunkin seuraavan taulukon sovelluksen kohdalla:

        1. Luo käyttöoikeuskäytäntö valitsemalla **Lisää käyttöoikeuskäytäntö**.
        2. Valitse **Salaisen koodin käyttöoikeudet** -kentässä käyttöoikeudet taulukosta.
        3. Hae **Valitse päänimi** -kentässä sovelluksen näyttönimi taulukosta.
        4. Valitse **Valitse**.
        5. Valitse **Lisää**.
        6. Valitse **Tallenna**.

        | Hakemus                                              | Käyttöoikeudet |
        |----------------------------------------------------------|-------------|
        | Luodun uuden sovelluksen näyttönimi | Hae, Luettelo   |
        | **Microsoft Dynamics ERP Microservices**                 | Hae, Luettelo   |

6. Määritä seuraavasti roolit, jotka käyttävät tallennustiliä:

    1. Avaa [Azure-portaalissa](https://portal.azure.com) aiemmin luotu tallennustili.
    2. Valitse **Käyttöoikeuksien hallinta (IAM)** ja valitse sitten **Roolimääritykset**.
    3. Valitse **Lisää, Lisää roolimääritys**.
    4. Noudata seuraavia vaiheita kunkin seuraavan taulukon sovelluksen kohdalla:

        1. Valitse rooli taulusta.
        2. Jätä **Delegoi käyttöoikeus** -kentän arvoksi **Azure AD -käyttäjä, -ryhmä tai -palvelun päänimi** -arvo.
        3. Syötä **Valitse**-kenttään sovellus taulukosta.
        4. Valitse **Tallenna**.

        | Hakemus                                              | Rooli                        |
        |----------------------------------------------------------|-----------------------------|
        | Luodun uuden sovelluksen näyttönimi | Omistaja                       |
        | Luodun uuden sovelluksen näyttönimi | Osallistuja                 |
        | Luodun uuden sovelluksen näyttönimi | Tallennustili - osallistuja |
        | Luodun uuden sovelluksen näyttönimi | Tallennustilan blob-objektin tietojen omistaja     |
        | **AI Builderin todennuspalvelu**                     | Tallennustilan blob-objektin tietojen lukija    |

# <a name="azure-cli"></a>[Azure CLI](#tab/azure-azure-cli)

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

## <a name="configure-the-export-to-data-lake-add-in"></a>Data Lake -viennin lisäosan määritys

Voit lisätä Vie Data Lakeen -apuohjelman ympäristöön LCS:n avulla.

1. KIrjaudu sisään LCS:ään ja valitse sivun oikealla olevan ympäristön nimen alta **Täydet tiedot**.
2. Valitse **Ympäristöapuohjelmat**-osassa **Asenna uusi apuohjelma**.
3. Valitse **Vie Data Lakeen** -apuohjelma.
4. Syötä seuraavat arvot.

    | Arvo                                                              | kuvaus |
    |--------------------------------------------------------------------|-------------|
    | Seb Azure-tilauksen vuokraajan tunnus, jossa avainsäilö sijaitsee | Sen vuokraajan tunnus, jossa tallennustili, sovellukset ja avainsäilöt sijaitsevat. Jos haluat hankkia tämän arvon, avaa [Azure-portaali](https://portal.azure.com), siirry **Azure Active Directory** -kohtaan ja kopioi **Vuokraajan tunnus** -kentän arvo. |
    | Anna avainsäilön DNS-nimi                             | Avainsäilön DNS-nimi, esimerkiksi `https://customkeyvault.vault.azure.net/`. |
    | Anna salauskoodi, joka sisältää tallennustilin nimen   | **tallennustilin nimi** |
    | Sen sovelluksen tunnuksen salaisen koodin nimi, jonka avulla Data Lakea käytetään          | **sovelluksen tunnus** |
    | Sovellusasiakkaan salasanan salainen nimi                                  | **sovelluksen salainen koodi** |

5. Hyväksy ehdot ja valitse **Asenna**.

Apuohjelma asennetaan muutamassa minuutissa.

## <a name="configure-the-finance-insights-add-in"></a>Finance Insights -lisäosan määrittäminen

> [!NOTE]
> Jos olet aiemmin asentanut Get insights -lisäosan, poista se ennen seuraavia toimia.

Noudattamalla näitä ohjeita voit asentaa Finance Insights -lisäosan.

1. KIrjaudu sisään LCS:ään ja valitse sivun oikealla olevan ympäristön nimen alta **Täydet tiedot**.
2. Valitse **Ympäristöapuohjelmat**-osassa **Asenna uusi apuohjelma**.
3. Valitse **Finance Insights** -lisäosa.
4. Hyväksy ehdot ja valitse **Asenna**.

Apuohjelman asentaminen voi kestää useita minuutteja.

## <a name="feedback-and-support"></a>Palaute ja tuki

Lähetä sähköpostiviesti [Finance Insights](mailto:fiap@microsoft.com) -tiimille, jos haluat antaa palautetta tai tarvitset tukea.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

