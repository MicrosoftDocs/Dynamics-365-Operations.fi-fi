---
title: Varaston näkyvyyden apuohjelma
description: Tässä aiheessa käsitellään Dynamics 365 Supply Chain Managementin varaston näkyvyyden apuohjelman asentamista ja määrittämistä.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 84f5e949f0c81f840c8a9086d05bbcfc576e42aa
ms.sourcegitcommit: b67665ed689c55df1a67d1a7840947c3977d600c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6017003"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="aeb07-103">Varaston näkyvyyden apuohjelma</span><span class="sxs-lookup"><span data-stu-id="aeb07-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="aeb07-104">Varaston näkyvyyden apuohjelma on itsenäinen ja erittäin skaalautuva mikropalvelu, joka mahdollistaa reaaliaikaisen käytettävissä olevan varaston seurannan ja antaa tällä tavoin yleisen näkymän varaston näkyvyyteen.</span><span class="sxs-lookup"><span data-stu-id="aeb07-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="aeb07-105">Kaikki käytettävissä olevaan varastoon liittyvät tiedot viedään palveluun lähes reaaliaikaisesti käyttämällä matala-asteista SQL-integraatiota.</span><span class="sxs-lookup"><span data-stu-id="aeb07-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="aeb07-106">Ulkoiset palvelut käyttävät palvelut tekevät RESTful API -ohjelmointirajapinnoilla käytettävissä olevien tietojen kyselyjä annetuissa dimensioissa ja saavat tällä tavoin luettelon käytettävissä olevista paikoista.</span><span class="sxs-lookup"><span data-stu-id="aeb07-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="aeb07-107">Varaston näkyvyys on Microsoft Dataverseen perustuva mikropalvelu, joten sitä voi laajentaa muodostamalla Power Apps -sovelluksia ja käyttämällä Power BI:ta tuottamaan liiketoiminnan tarpeita vastaavia mukautettuja toimintoja.</span><span class="sxs-lookup"><span data-stu-id="aeb07-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="aeb07-108">Indeksi voidaan lisäksi päivittää tekemään varastokyselyjä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="aeb07-109">Varaston näkyvyydessä on määritysvaihtoehtoja, joiden avulla sen voi integroida useiden kolmannen osapuolen järjestelmien kanssa.</span><span class="sxs-lookup"><span data-stu-id="aeb07-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="aeb07-110">Se tukee standardoitua varastodimensiota, mukautettua laajennettavuutta ja standardoituja, määritettäviä laskettuja määriä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="aeb07-111">Tässä aiheessa käsitellään Dynamics 365 Supply Chain Managementin varaston näkyvyyden apuohjelman asentamista ja määrittämistä sekä sen ohjelmointirajapinnan käyttöä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="aeb07-112">Varaston näkyvyyden lisäapuohjelman asentaminen</span><span class="sxs-lookup"><span data-stu-id="aeb07-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="aeb07-113">Varaston näkyvyyden lisäapuohjelman asentamiseen on käytettävä Microsoft Dynamics Lifecycle Servicesiä (LCS).</span><span class="sxs-lookup"><span data-stu-id="aeb07-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="aeb07-114">LCS on yhteistyöportaali, jonka muodostamassa ympäristössä ja jonka säännöllisesti päivitetyillä palveluilla voi hallita Dynamics 365 Finance and Operations -sovellusten elinkaarta.</span><span class="sxs-lookup"><span data-stu-id="aeb07-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="aeb07-115">Lisätietoja on kohdassa [Lifecycle Services -resurssit](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span><span class="sxs-lookup"><span data-stu-id="aeb07-115">For more information, see [Lifecycle Services resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span></span>

### <a name="inventory-visibility-add-in-prerequisites"></a><span data-ttu-id="aeb07-116">Varaston näkyvyyden apuohjelman edellytykset</span><span class="sxs-lookup"><span data-stu-id="aeb07-116">Inventory Visibility Add-in prerequisites</span></span>

<span data-ttu-id="aeb07-117">Ennen varaston näkyvyyden apuohjelman asentamista:</span><span class="sxs-lookup"><span data-stu-id="aeb07-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="aeb07-118">Hanki LCS-toteutusprojekti, jossa on otettu käyttöön vähintään yksi ympäristö.</span><span class="sxs-lookup"><span data-stu-id="aeb07-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="aeb07-119">Varmista, että kohdassa [Lisäosien yleiskatsaus](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) annetut edellytykset lisäosien määrittämiselle on täytetty.</span><span class="sxs-lookup"><span data-stu-id="aeb07-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="aeb07-120">Varaston näkyvyys ei edellytä kaksoiskirjoituslinkitystä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="aeb07-121">Ota yhteyttä varaston näkyvyyden tiimiin [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), jotta saat seuraavat kolme vaadittua tiedostoa:</span><span class="sxs-lookup"><span data-stu-id="aeb07-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>
  - `Inventory Visibility Dataverse Solution.zip`
  - `Inventory Visibility Configuration Trigger.zip`
  - <span data-ttu-id="aeb07-122">`Inventory Visibility Integration.zip` (jos käynnissä ollut Supply Chain Managementin versio on aiempi kuin 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="aeb07-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>
- <span data-ttu-id="aeb07-123">Vaihtoehtoisesti ota yhteyttä varaston näkyvyyden tiimiin [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), jotta saat Package Deployer -paketit.</span><span class="sxs-lookup"><span data-stu-id="aeb07-123">Alternatively, contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package deployer packages.</span></span> <span data-ttu-id="aeb07-124">Virallinen Package Deployer -työkalu voi käyttää näitä pakkauksia.</span><span class="sxs-lookup"><span data-stu-id="aeb07-124">These packages can be used by an official package deployer tool.</span></span>
  - `InventoryServiceBase.PackageDeployer.zip`
  - <span data-ttu-id="aeb07-125">`InventoryServiceApplication.PackageDeployer.zip` (tämä paketti sisältää kaikki `InventoryServiceBase`-paketin muutokset sekä muut käyttöliittymäsovelluksen komponentit)</span><span class="sxs-lookup"><span data-stu-id="aeb07-125">`InventoryServiceApplication.PackageDeployer.zip` (this package contains all of the changes in the `InventoryServiceBase` package, plus additional UI application components)</span></span>
- <span data-ttu-id="aeb07-126">Noudata seuraavassa annettuja ohjeita: [Pikaopas: Rekisteröi hakemus Microsoft identity Platformiin](/azure/active-directory/develop/quickstart-register-app) sovelluksen rekisteröimiseksi ja asiakkaan lisäämiseksi AAD:lle ylläpitosopimuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="aeb07-126">Follow the instructions given in [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register an application and add a client secret to AAD under your azure subscription.</span></span>
  - [<span data-ttu-id="aeb07-127">Sovelluksen rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="aeb07-127">Register an application</span></span>](/azure/active-directory/develop/quickstart-register-app)
  - [<span data-ttu-id="aeb07-128">Lisää asiakasohjelman salasana</span><span class="sxs-lookup"><span data-stu-id="aeb07-128">Add a client secret</span></span>](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
  - <span data-ttu-id="aeb07-129">**Sovelluksen (asiakas) tunnuksen**, **asiakasohjelman salasanan** ja **vuokraajan tunnuksen** avulla voidaan tehdä seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="aeb07-129">The **Application(Client) Id**, **Client Secret**, and **Tenant ID** will be used in the following steps.</span></span>

> [!NOTE]
> <span data-ttu-id="aeb07-130">Tällä hetkellä tuettuja maita ja alueita ovat Kanada, Yhdysvallat ja Euroopan unioni (EU).</span><span class="sxs-lookup"><span data-stu-id="aeb07-130">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="aeb07-131">Jos sinulla on näitä edellytyksiä koskevia kysymyksiä, ota yhteys varaston näkyvyyden tuotetiimiin.</span><span class="sxs-lookup"><span data-stu-id="aeb07-131">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="aeb07-132">Määritys Dataverse</span><span class="sxs-lookup"><span data-stu-id="aeb07-132">Set up Dataverse</span></span>

<span data-ttu-id="aeb07-133">Jotta voit määrittää Dataversen käytön varaston näkyvyyden avulla, sinun on ensin valmisteltava edellytykset ja päätettävä, määritetäänkö Dataverse joko Package Deployer -työkalun avulla vai tuomalla ratkaisut manuaalisesti (molempia ei tarvitse tehdä).</span><span class="sxs-lookup"><span data-stu-id="aeb07-133">To set up Dataverse for use with Inventory Visibility, you must first prepare the prerequisites and then decide whether to set up Dataverse using either the package deployer tool or by manually importing the solutions (you don't have to do both).</span></span> <span data-ttu-id="aeb07-134">Asenna sitten Varaston näkyvyyden lisäapuohjelma.</span><span class="sxs-lookup"><span data-stu-id="aeb07-134">Then install the Inventory Visibility Add-in.</span></span> <span data-ttu-id="aeb07-135">Seuraavissa aliosissa kuvataan, kuinka kukin tehtävä viimeistellään.</span><span class="sxs-lookup"><span data-stu-id="aeb07-135">The following subsections describe how to complete each of these tasks.</span></span>

#### <a name="prepare-dataverse-prerequisites"></a><span data-ttu-id="aeb07-136">Dataverse-edellytysten valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="aeb07-136">Prepare Dataverse prerequisites</span></span>

<span data-ttu-id="aeb07-137">Ennen kuin aloitat Dataversen määrittämisen, lisää vuokraajaan huoltoperiaate seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="aeb07-137">Before you start to set up Dataverse, add a service principle to your tenant by doing the following:</span></span>

1. <span data-ttu-id="aeb07-138">Asenna Azure AD PowerShell Module v2, kuten kuvattu kohdassa [Asenna Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="aeb07-138">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>

1. <span data-ttu-id="aeb07-139">Suorita seuraava PowerShell-komento:</span><span class="sxs-lookup"><span data-stu-id="aeb07-139">Run the following PowerShell command:</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)
    
    New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
    ```

#### <a name="set-up-dataverse-using-the-package-deployer-tool"></a><span data-ttu-id="aeb07-140">Dataversen määrittäminen Package Deployer -työkalun avulla</span><span class="sxs-lookup"><span data-stu-id="aeb07-140">Set up Dataverse using the package deployer tool</span></span>

<span data-ttu-id="aeb07-141">Kun olet määrittänyt tarvittavat edellytykset, käytä seuraavaa menettelyä, jos haluat määrittää Dataversen Package Deployer -työkalun avulla.</span><span class="sxs-lookup"><span data-stu-id="aeb07-141">After you have the prerequisites in place, use the following procedure if you prefer to set up Dataverse using the package deployer tool.</span></span> <span data-ttu-id="aeb07-142">Seuraavassa osassa on tietoja ratkaisujen tuonnista manuaalisesti (älä tee molempia).</span><span class="sxs-lookup"><span data-stu-id="aeb07-142">See the next section for details about how to import the solutions manually instead (don't do both).</span></span>

1. <span data-ttu-id="aeb07-143">Asenna kehittäjien työkalut kohdassa [Lataa työkalut kohteesta NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget) kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="aeb07-143">Install developer tools as described in [Download tools from NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).</span></span>

1. <span data-ttu-id="aeb07-144">Liiketoimintavaatimustesi mukaan valitse `InventoryServiceBase`- tai `InventoryServiceApplication`-paketti.</span><span class="sxs-lookup"><span data-stu-id="aeb07-144">Based on your business requirements, choose the `InventoryServiceBase` or `InventoryServiceApplication` package.</span></span>

1. <span data-ttu-id="aeb07-145">Tuo ratkaisut:</span><span class="sxs-lookup"><span data-stu-id="aeb07-145">Import the solutions:</span></span>
    1. <span data-ttu-id="aeb07-146">`InventoryServiceBase`-paketille:</span><span class="sxs-lookup"><span data-stu-id="aeb07-146">For the `InventoryServiceBase` package:</span></span>
        - <span data-ttu-id="aeb07-147">Pura `InventoryServiceBase.PackageDeployer.zip`</span><span class="sxs-lookup"><span data-stu-id="aeb07-147">Unzip `InventoryServiceBase.PackageDeployer.zip`</span></span>
        - <span data-ttu-id="aeb07-148">Etsi kansio `InventoryServiceBase`, tiedosto `[Content_Types].xml`, tiedosto `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll`, tiedosto `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config` ja tiedosto `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`.</span><span class="sxs-lookup"><span data-stu-id="aeb07-148">Find folder `InventoryServiceBase`, file `[Content_Types].xml`, file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll`, file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`, and file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`.</span></span> 
        - <span data-ttu-id="aeb07-149">Kopioi nämä kansiot ja tiedostot `.\Tools\PackageDeployment`-hakemistoon, joka luotiin kehittäjien työkalujen asennuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-149">Copy each of these folders and files to the `.\Tools\PackageDeployment` directory, which was created when you installed the developer tools.</span></span>
    1. <span data-ttu-id="aeb07-150">`InventoryServiceApplication`-paketille:</span><span class="sxs-lookup"><span data-stu-id="aeb07-150">For the `InventoryServiceApplication` package:</span></span>
        - <span data-ttu-id="aeb07-151">Pura `InventoryServiceApplication.PackageDeployer.zip`</span><span class="sxs-lookup"><span data-stu-id="aeb07-151">Unzip `InventoryServiceApplication.PackageDeployer.zip`</span></span>
        - <span data-ttu-id="aeb07-152">Etsi kansio `InventoryServiceApplication`, tiedosto `[Content_Types].xml`, tiedosto `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`, tiedosto `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config` ja tiedosto `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`.</span><span class="sxs-lookup"><span data-stu-id="aeb07-152">Find folder `InventoryServiceApplication`, file `[Content_Types].xml`, file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`, file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`, and file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`.</span></span>
        - <span data-ttu-id="aeb07-153">Kopioi nämä kansiot ja tiedostot `.\Tools\PackageDeployment`-hakemistoon, joka luotiin kehittäjien työkalujen asennuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-153">Copy each of these folders and files to the `.\Tools\PackageDeployment` directory, which was created when you installed the developer tools.</span></span>
    1. <span data-ttu-id="aeb07-154">Suorita `.\Tools\PackageDeployment\PackageDeployer.exe`.</span><span class="sxs-lookup"><span data-stu-id="aeb07-154">Execute `.\Tools\PackageDeployment\PackageDeployer.exe`.</span></span> <span data-ttu-id="aeb07-155">Voit tuoda ratkaisut noudattamalla näytön ohjeita.</span><span class="sxs-lookup"><span data-stu-id="aeb07-155">Follow the instructions on your screen to import the solutions.</span></span>

1. <span data-ttu-id="aeb07-156">Määritä käyttöoikeusroolit sovelluksen käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="aeb07-156">Assign security roles to the application user.</span></span>
    1. <span data-ttu-id="aeb07-157">Avaa Dataverse-ympäristön URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="aeb07-157">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="aeb07-158">Valitse **Lisäasetukset \> Järjestelmä \> Suojaus \> Käyttäjät** ja etsi käyttäjä nimeltä **# InventoryVisibility**.</span><span class="sxs-lookup"><span data-stu-id="aeb07-158">Go to **Advanced Setting \> System \> Security \> Users**, and find user the named **# InventoryVisibility**.</span></span>
    1. <span data-ttu-id="aeb07-159">Valitse **Määritä rooli** ja valitse sitten **Järjestelmänvalvoja**.</span><span class="sxs-lookup"><span data-stu-id="aeb07-159">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="aeb07-160">Jos saatavana on rooli nimeltä **Common Data Service -käyttäjä**, valitse myös se.</span><span class="sxs-lookup"><span data-stu-id="aeb07-160">If there is a role that is named **Common Data Service User**, select it as well.</span></span>

#### <a name="set-up-dataverse-manually-by-importing-solutions"></a><span data-ttu-id="aeb07-161">Määritä Dataverse manuaalisesti tuomalla ratkaisuja</span><span class="sxs-lookup"><span data-stu-id="aeb07-161">Set up Dataverse manually by importing solutions</span></span>

<span data-ttu-id="aeb07-162">Kun olet määrittänyt tarvittavat edellytykset, käytä seuraavaa menettelyä, jos haluat määrittää Dataversen tuomalla ratkaisuja manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="aeb07-162">After you have the prerequisites in place, use the following procedure if you prefer to set up Dataverse by manually importing solutions.</span></span> <span data-ttu-id="aeb07-163">Edellisessä osassa on lisätietoja Package Deployer -työkalun käytöstä sen sijaan (älä tee molempia).</span><span class="sxs-lookup"><span data-stu-id="aeb07-163">See the previous section for details about how to use the package deployer tool instead (don't do both).</span></span>

1. <span data-ttu-id="aeb07-164">Luo sovelluskäyttäjä varaston näkyvyydelle Dataversessä:</span><span class="sxs-lookup"><span data-stu-id="aeb07-164">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="aeb07-165">Avaa Dataverse-ympäristön URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="aeb07-165">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="aeb07-166">Valitse **Lisäasetukset \> Järjestelmä \> Suojaus \> Käyttäjät** ja luo sovelluskäyttäjä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-166">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="aeb07-167">Vaihda sivunäkymäksi **Sovelluskäyttäjät** näkymävalikossa.</span><span class="sxs-lookup"><span data-stu-id="aeb07-167">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="aeb07-168">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="aeb07-168">Select **New**.</span></span> <span data-ttu-id="aeb07-169">Aseta sovellustunnukseksi *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="aeb07-169">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="aeb07-170">(Objektin tunnus ladataan automaattisesti, kun tallennat muutokset.) Voit mukauttaa nimeä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-170">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="aeb07-171">Voit muuttaa sen esimerkiksi nimeksi *Varaston näkyvyys*.</span><span class="sxs-lookup"><span data-stu-id="aeb07-171">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="aeb07-172">Kun olet valmis, valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="aeb07-172">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="aeb07-173">Valitse **Määritä rooli** ja valitse sitten **Järjestelmänvalvoja**.</span><span class="sxs-lookup"><span data-stu-id="aeb07-173">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="aeb07-174">Jos saatavana on rooli nimeltä **Common Data Service -käyttäjä**, valitse myös se.</span><span class="sxs-lookup"><span data-stu-id="aeb07-174">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="aeb07-175">Lisätietoja on kohdassa [Sovelluskäyttäjän luominen](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="aeb07-175">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="aeb07-176">Jos oletuskieli ei Dataversessäsi ole **englanti**:</span><span class="sxs-lookup"><span data-stu-id="aeb07-176">If the default language of your Dataverse is not **English**:</span></span>

    1. <span data-ttu-id="aeb07-177">Siirry kohtaan **Lisäasetukset \> Hallinta \> Kielet**,</span><span class="sxs-lookup"><span data-stu-id="aeb07-177">Go to **Advanced Setting \> Administration \> Languages**,</span></span>
    1. <span data-ttu-id="aeb07-178">Valitse **englanti (LanguageCode=1033)** ja valitse **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="aeb07-178">Select **English (LanguageCode=1033)** and select **Apply**.</span></span>

1. <span data-ttu-id="aeb07-179">Tuo `Inventory Visibility Dataverse Solution.zip` -tiedosto, joka sisältää Dataverse-konfiguraatioon liittyvät entiteetit ja Power Apps -sovellukset:</span><span class="sxs-lookup"><span data-stu-id="aeb07-179">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="aeb07-180">Siirry **Ratkaisut**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="aeb07-180">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="aeb07-181">Valitse **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="aeb07-181">Select **Import**.</span></span>

1. <span data-ttu-id="aeb07-182">Tuo konfiguraation päivityksen käynnistimen työnkulku:</span><span class="sxs-lookup"><span data-stu-id="aeb07-182">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="aeb07-183">Siirry Microsoft Flow -sivulle.</span><span class="sxs-lookup"><span data-stu-id="aeb07-183">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="aeb07-184">Varmista, että yhteys nimeltä *Dataverse (vanha)* on olemassa.</span><span class="sxs-lookup"><span data-stu-id="aeb07-184">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="aeb07-185">(Jos sitä ei ole olemassa, luo se.)</span><span class="sxs-lookup"><span data-stu-id="aeb07-185">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="aeb07-186">Tuo `Inventory Visibility Configuration Trigger.zip` -tiedosto.</span><span class="sxs-lookup"><span data-stu-id="aeb07-186">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="aeb07-187">Kun käynnistys on tuotu, se näkyy **Omat työnkulut** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="aeb07-187">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="aeb07-188">Alusta seuraavat neljä muuttujaa ympäristön tietojen perusteella:</span><span class="sxs-lookup"><span data-stu-id="aeb07-188">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="aeb07-189">Azure-vuokraajan tunnus</span><span class="sxs-lookup"><span data-stu-id="aeb07-189">Azure Tenant ID</span></span>
        - <span data-ttu-id="aeb07-190">Azure-sovelluksen asiakastunnus</span><span class="sxs-lookup"><span data-stu-id="aeb07-190">Azure Application Client ID</span></span>
        - <span data-ttu-id="aeb07-191">Azure-sovelluksen asiakasohjelman salasana</span><span class="sxs-lookup"><span data-stu-id="aeb07-191">Azure Application Client Secret</span></span>
        - <span data-ttu-id="aeb07-192">Varaston näkyvyyden päätepiste</span><span class="sxs-lookup"><span data-stu-id="aeb07-192">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="aeb07-193">Lisätietoja tästä muuttujasta on jäljempänä tässä ohjeaiheessa kohdassa [Varaston näkyvyyden integraation määrittäminen](#setup-inventory-visibility-integration).</span><span class="sxs-lookup"><span data-stu-id="aeb07-193">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="aeb07-194">![Määrityksen käynnistin](media/configuration-trigger.png "Määrityksen käynnistin")</span><span class="sxs-lookup"><span data-stu-id="aeb07-194">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="aeb07-195">Valitse **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="aeb07-195">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="aeb07-196">Lisäosan asentaminen</span><span class="sxs-lookup"><span data-stu-id="aeb07-196">Install the add-in</span></span>

<span data-ttu-id="aeb07-197">Varaston näkyvyyden apuohjelman asentaminen:</span><span class="sxs-lookup"><span data-stu-id="aeb07-197">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="aeb07-198">Kirjaudu [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) -portaaliin.</span><span class="sxs-lookup"><span data-stu-id="aeb07-198">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="aeb07-199">Valitse aloitussivulla projekti, jossa ympäristö on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="aeb07-199">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="aeb07-200">Valitse projektisivulla ympäristö, johon haluat asentaa apuohjelman.</span><span class="sxs-lookup"><span data-stu-id="aeb07-200">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="aeb07-201">Siirry ympäristösivulla alaspäin, kunnes näet **Ympäristön lisäosat** -kohdan **Power Platform -integraatio** -kohdassa, josta löytyy Dataverse-ympäristön nimi.</span><span class="sxs-lookup"><span data-stu-id="aeb07-201">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="aeb07-202">Valitse **Ympäristöapuohjelmat**-osassa **Asenna uusi apuohjelma**.</span><span class="sxs-lookup"><span data-stu-id="aeb07-202">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="aeb07-203">![Ympäristösivu LCS:ssa](media/inventory-visibility-environment.png "Ympäristösivu LCS:ssa")</span><span class="sxs-lookup"><span data-stu-id="aeb07-203">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="aeb07-204">Valitse **Asenna uusi apuohjelma** -linkki.</span><span class="sxs-lookup"><span data-stu-id="aeb07-204">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="aeb07-205">Käytettävissä olevien apuohjelmien luettelo avautuu.</span><span class="sxs-lookup"><span data-stu-id="aeb07-205">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="aeb07-206">Valitse luettelosta **Vataston näkyvyys**.</span><span class="sxs-lookup"><span data-stu-id="aeb07-206">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="aeb07-207">Anna arvot seuraavissa ympäristön kentissä:</span><span class="sxs-lookup"><span data-stu-id="aeb07-207">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="aeb07-208">**AAD-sovelluksen (asiakasohjelman) tunnus**</span><span class="sxs-lookup"><span data-stu-id="aeb07-208">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="aeb07-209">**AAD-vuokraajan tunnus**</span><span class="sxs-lookup"><span data-stu-id="aeb07-209">**AAD tenant ID**</span></span>

    <span data-ttu-id="aeb07-210">![Apuohjelman määrityssivu](media/inventory-visibility-setup.png "Apuohjelman määrityssivu")</span><span class="sxs-lookup"><span data-stu-id="aeb07-210">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="aeb07-211">Hyväksy käyttöehdot valitsemalla **Käyttöehdot**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="aeb07-211">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="aeb07-212">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="aeb07-212">Select **Install**.</span></span> <span data-ttu-id="aeb07-213">Apuohjelman tilana näkyy nyt **Asennetaan**.</span><span class="sxs-lookup"><span data-stu-id="aeb07-213">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="aeb07-214">Se on valmis, päivitä sivu, jonka jälkeen tilana on **Asennettu**.</span><span class="sxs-lookup"><span data-stu-id="aeb07-214">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="aeb07-215">Lisäosan asennuksen poistaminen</span><span class="sxs-lookup"><span data-stu-id="aeb07-215">Uninstall the add-in</span></span>

<span data-ttu-id="aeb07-216">Poista apuohjelman asennus valitsemalla **Poista asennus**.</span><span class="sxs-lookup"><span data-stu-id="aeb07-216">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="aeb07-217">Kun päivität LCS:n, varaston näkyvyyden apuohjelma poistetaan.</span><span class="sxs-lookup"><span data-stu-id="aeb07-217">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="aeb07-218">Asennuksen poistoprosessi poistaa apuohjelman rekisteröinnin sekä käynnistää kaikkien palveluun tallennettujen liiketoimintatietojen puhdistustyön.</span><span class="sxs-lookup"><span data-stu-id="aeb07-218">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="aeb07-219">Käytettävissä olevan varaston tietojen käyttäminen Supply Chain Managementista</span><span class="sxs-lookup"><span data-stu-id="aeb07-219">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="aeb07-220">Varaston näkyvyyden integrointipaketin käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="aeb07-220">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="aeb07-221">Jos käytössäsi on Supply Chain Management -versio 10.0.17 tai aiempi, ota yhteyttä varaston näkyvyyden tukihenkilöstöön osoitteessa [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) saadaksesi pakettitiedoston.</span><span class="sxs-lookup"><span data-stu-id="aeb07-221">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="aeb07-222">Ota sitten paketti käyttöön LCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-222">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="aeb07-223">Jos käyttöönoton aikana ilmenee version vastaavuusvirhe, X++-projekti on tuotava manuaalisesti kehitysympäristöön.</span><span class="sxs-lookup"><span data-stu-id="aeb07-223">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="aeb07-224">Luo sitten käyttöön otettava paketti kehitysympäristössä ja ota se käyttöön tuotantoympäristössä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-224">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="aeb07-225">Koodi sisältyy Supply Chain Management -versioon 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="aeb07-225">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="aeb07-226">Jos käytössä on tämä versio tai myöhempi versio, käyttöönottoa ei tarvita.</span><span class="sxs-lookup"><span data-stu-id="aeb07-226">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="aeb07-227">Varmista, että seuraavat ominaisuudet on otettu käyttöön Supply Chain Management -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-227">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="aeb07-228">(Oletusarvon mukaan ne ovat käytössä.)</span><span class="sxs-lookup"><span data-stu-id="aeb07-228">(By default, they are turned on.)</span></span>

| <span data-ttu-id="aeb07-229">Toiminnon kuvaus</span><span class="sxs-lookup"><span data-stu-id="aeb07-229">Feature description</span></span> | <span data-ttu-id="aeb07-230">Koodiversio</span><span class="sxs-lookup"><span data-stu-id="aeb07-230">Code version</span></span> | <span data-ttu-id="aeb07-231">Vaihda luokka</span><span class="sxs-lookup"><span data-stu-id="aeb07-231">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="aeb07-232">Varastodimensioiden ottaminen käyttöön InventSum-taulussa tai poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="aeb07-232">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="aeb07-233">10.0.11</span><span class="sxs-lookup"><span data-stu-id="aeb07-233">10.0.11</span></span> | <span data-ttu-id="aeb07-234">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="aeb07-234">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="aeb07-235">Varastodimensioiden ottaminen käyttöön InventSumDelta-taulussa tai poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="aeb07-235">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="aeb07-236">10.0.12</span><span class="sxs-lookup"><span data-stu-id="aeb07-236">10.0.12</span></span> | <span data-ttu-id="aeb07-237">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="aeb07-237">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="aeb07-238">Määritä Varaston näkyvyyden integrointi</span><span class="sxs-lookup"><span data-stu-id="aeb07-238">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="aeb07-239">Avaa Supply Chain Managementissa **[Ominaisuuden hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** -työtila ja ota käyttöön **Varaston näkyvyyden integraatio** -ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="aeb07-239">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="aeb07-240">Siirry kohtaan **Varastonhallinta \> Määritys \> Varaston näkyvyyden integraation parametrit** ja kirjoita sen ympäristön URL-osoite, jossa varaston näkyvyys on käytössä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-240">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="aeb07-241">Etsi LCS-ympäristösi Azure-alue ja kirjoita sitten URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="aeb07-241">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="aeb07-242">URL-osoitteessa on seuraava muoto:</span><span class="sxs-lookup"><span data-stu-id="aeb07-242">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="aeb07-243">Esimerkiksi Euroopassa ympäristössäsi on jokin seuraavista URL-osoitteista:</span><span class="sxs-lookup"><span data-stu-id="aeb07-243">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="aeb07-244">Seuraavat alueet ovat käytettävissä tällä hetkellä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-244">The following regions are currently available.</span></span>

    | <span data-ttu-id="aeb07-245">Azure-alue</span><span class="sxs-lookup"><span data-stu-id="aeb07-245">Azure region</span></span> | <span data-ttu-id="aeb07-246">Alueen lyhyt nimi</span><span class="sxs-lookup"><span data-stu-id="aeb07-246">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="aeb07-247">Itä-Australia</span><span class="sxs-lookup"><span data-stu-id="aeb07-247">Australia east</span></span> | <span data-ttu-id="aeb07-248">eau</span><span class="sxs-lookup"><span data-stu-id="aeb07-248">eau</span></span> |
    | <span data-ttu-id="aeb07-249">Kaakkois-Australia</span><span class="sxs-lookup"><span data-stu-id="aeb07-249">Australia southeast</span></span> | <span data-ttu-id="aeb07-250">seau</span><span class="sxs-lookup"><span data-stu-id="aeb07-250">seau</span></span> |
    | <span data-ttu-id="aeb07-251">Kanada, keskinen</span><span class="sxs-lookup"><span data-stu-id="aeb07-251">Canada central</span></span> | <span data-ttu-id="aeb07-252">cca</span><span class="sxs-lookup"><span data-stu-id="aeb07-252">cca</span></span> |
    | <span data-ttu-id="aeb07-253">Kanada, itäinen</span><span class="sxs-lookup"><span data-stu-id="aeb07-253">Canada east</span></span> | <span data-ttu-id="aeb07-254">eca</span><span class="sxs-lookup"><span data-stu-id="aeb07-254">eca</span></span> |
    | <span data-ttu-id="aeb07-255">Pohjois-Eurooppa</span><span class="sxs-lookup"><span data-stu-id="aeb07-255">North Europe</span></span> | <span data-ttu-id="aeb07-256">neu</span><span class="sxs-lookup"><span data-stu-id="aeb07-256">neu</span></span> |
    | <span data-ttu-id="aeb07-257">Länsi-Eurooppa</span><span class="sxs-lookup"><span data-stu-id="aeb07-257">West Europe</span></span> | <span data-ttu-id="aeb07-258">weu</span><span class="sxs-lookup"><span data-stu-id="aeb07-258">weu</span></span> |
    | <span data-ttu-id="aeb07-259">Itä-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="aeb07-259">East US</span></span> | <span data-ttu-id="aeb07-260">eus</span><span class="sxs-lookup"><span data-stu-id="aeb07-260">eus</span></span> |
    | <span data-ttu-id="aeb07-261">Länsi-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="aeb07-261">West US</span></span> | <span data-ttu-id="aeb07-262">wus</span><span class="sxs-lookup"><span data-stu-id="aeb07-262">wus</span></span> |

1. <span data-ttu-id="aeb07-263">Valitse **Varastonhallinta \> Kausittainen \> Varaston näkyvyyden integraatio** ja ota työ käyttöön.</span><span class="sxs-lookup"><span data-stu-id="aeb07-263">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="aeb07-264">Kaikki Supply Chain Managementin varastomuutostapahtumat kirjataan nyt varaston näkyvyyteen.</span><span class="sxs-lookup"><span data-stu-id="aeb07-264">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="aeb07-265">Varaston näkyvyyden apuohjelman julkinen ohjelmointirajapinta</span><span class="sxs-lookup"><span data-stu-id="aeb07-265">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="aeb07-266">Varaston näkyvyyden apuohjelman julkinen REST API sisältää useita nimenomaisia integroinnin päätepisteitä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-266">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="aeb07-267">Se tukee kolmea pääasiallista vuorovaikutustyyppiä:</span><span class="sxs-lookup"><span data-stu-id="aeb07-267">It supports three main interaction types:</span></span>

- <span data-ttu-id="aeb07-268">Varastosaldon määrän muutosten kirjaaminen apuohjelmaan ulkoisesta järjestelmästä</span><span class="sxs-lookup"><span data-stu-id="aeb07-268">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="aeb07-269">Nykyisten käytettävissä olevien määrien kysely ulkoisesta järjestelmästä</span><span class="sxs-lookup"><span data-stu-id="aeb07-269">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="aeb07-270">Automaattinen synkronointi Supply Chain Managementin käytettävissä olevan varaston kanssa</span><span class="sxs-lookup"><span data-stu-id="aeb07-270">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="aeb07-271">Automaattinen synkronointi ei kuulu julkiseen ohjelmointirajapintaan.</span><span class="sxs-lookup"><span data-stu-id="aeb07-271">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="aeb07-272">Sen sijaan sitä käsitellään niiden ympäristöjen taustalla, joissa varaston näkyvyyden apuohjelma on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="aeb07-272">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="aeb07-273">Todennus</span><span class="sxs-lookup"><span data-stu-id="aeb07-273">Authentication</span></span>

<span data-ttu-id="aeb07-274">Ympäristön suojaustunnuksen avulla kutsutaan varaston näkyvyyden apuohjelmaa.</span><span class="sxs-lookup"><span data-stu-id="aeb07-274">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="aeb07-275">Siksi sinun on luotava *Azure Active Directory (Azure AD) -tunnus* Azure AD -sovelluksen avulla.</span><span class="sxs-lookup"><span data-stu-id="aeb07-275">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="aeb07-276">Tämän jälkeen Azure AD -tunnuksen avulla saat *käyttöoikeustunnuksen* suojauspalvelusta.</span><span class="sxs-lookup"><span data-stu-id="aeb07-276">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="aeb07-277">Palvelun suojaustunnus haetaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="aeb07-277">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="aeb07-278">Kirjaudu Azure-portaaliin ja etsi sen avulla Supply Chain Management -sovelluksen `clientId` ja `clientSecret`.</span><span class="sxs-lookup"><span data-stu-id="aeb07-278">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="aeb07-279">Nouda Azure Active Directory -tunnus (`aadToken`) lähettämällä HTTP-pyyntö, jossa on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="aeb07-279">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="aeb07-280">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="aeb07-280">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="aeb07-281">**Tapa** - `GET`</span><span class="sxs-lookup"><span data-stu-id="aeb07-281">**Method** - `GET`</span></span>
    - <span data-ttu-id="aeb07-282">**Tekstisisältö (lomaketiedot)**:</span><span class="sxs-lookup"><span data-stu-id="aeb07-282">**Body content (form data)**:</span></span>

        | <span data-ttu-id="aeb07-283">avain</span><span class="sxs-lookup"><span data-stu-id="aeb07-283">key</span></span> | <span data-ttu-id="aeb07-284">arvo</span><span class="sxs-lookup"><span data-stu-id="aeb07-284">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="aeb07-285">client_id</span><span class="sxs-lookup"><span data-stu-id="aeb07-285">client_id</span></span> | <span data-ttu-id="aeb07-286">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="aeb07-286">${aadAppId}</span></span> |
        | <span data-ttu-id="aeb07-287">client_secret</span><span class="sxs-lookup"><span data-stu-id="aeb07-287">client_secret</span></span> | <span data-ttu-id="aeb07-288">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="aeb07-288">${aadAppSecret}</span></span> |
        | <span data-ttu-id="aeb07-289">grant_type</span><span class="sxs-lookup"><span data-stu-id="aeb07-289">grant_type</span></span> | <span data-ttu-id="aeb07-290">client_credentials</span><span class="sxs-lookup"><span data-stu-id="aeb07-290">client_credentials</span></span> |
        | <span data-ttu-id="aeb07-291">resurssi</span><span class="sxs-lookup"><span data-stu-id="aeb07-291">resource</span></span> | <span data-ttu-id="aeb07-292">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="aeb07-292">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="aeb07-293">Vastauksena pitäisi olla `aadToken` , joka muistuttaa seuraavaa esimerkkiä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-293">You should receive an `aadToken` in response, which resembles the following example.</span></span>

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
        "expires_on": "1610466645",
        "not_before": "1610462745",
        "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
        "access_token": "eyJ0eX...8WQ"
    }
    ```

1. <span data-ttu-id="aeb07-294">Muodosta seuraavankaltainen JSON-pyyntö:</span><span class="sxs-lookup"><span data-stu-id="aeb07-294">Formulate a JSON request that resembles the following:</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    <span data-ttu-id="aeb07-295">Jossa:</span><span class="sxs-lookup"><span data-stu-id="aeb07-295">Where:</span></span>
    - <span data-ttu-id="aeb07-296">`client_assertion`-arvon on oltava edellisessä vaiheessa vastaanotettu `aadToken`.</span><span class="sxs-lookup"><span data-stu-id="aeb07-296">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="aeb07-297">`context`-arvon on oltava ympäristötunnus, jossa apuohjelma halutaan ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="aeb07-297">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="aeb07-298">Kaikki muut arvot määritetään samoiksi kuin esimerkissä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-298">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="aeb07-299">Lähetä HTTP-pyyntö, jossa on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="aeb07-299">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="aeb07-300">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="aeb07-300">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="aeb07-301">**Tapa** - `POST`</span><span class="sxs-lookup"><span data-stu-id="aeb07-301">**Method** - `POST`</span></span>
    - <span data-ttu-id="aeb07-302">**HTTP-otsikko** - sisällytä ohjelmointirajapinnan versio (avain on `Api-Version` ja arvo `1.0`)</span><span class="sxs-lookup"><span data-stu-id="aeb07-302">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="aeb07-303">**Tekstisisältö** - sisällytä edellisessä vaiheessa luotu JSON-pyyntö.</span><span class="sxs-lookup"><span data-stu-id="aeb07-303">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="aeb07-304">`access_token` saadaan vastauksessa.</span><span class="sxs-lookup"><span data-stu-id="aeb07-304">You will get an `access_token` in response.</span></span> <span data-ttu-id="aeb07-305">Sitä tarvitaan haltijatunnuksena, jolla varastoin näkyvyyden ohjelmointirajapintaa kutsutaan.</span><span class="sxs-lookup"><span data-stu-id="aeb07-305">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="aeb07-306">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="aeb07-306">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a><span data-ttu-id="aeb07-307">Mallipyyntö</span><span class="sxs-lookup"><span data-stu-id="aeb07-307">Sample Request</span></span>

<span data-ttu-id="aeb07-308">Tässä on esimerkki http-pyynnöstä. Voit käyttää mitä tahansa työkaluja tai koodauskieltä lähettääksesi pyynnön, esimerkiksi ``Postman``.</span><span class="sxs-lookup"><span data-stu-id="aeb07-308">For your reference, here is a sample http request, you can use any tools or coding language to send this request, such as  ``Postman``.</span></span>

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "quantities": {
        "pos": {
            "inbound": 5
        }  
    },
    "dimensions": {
        "SizeId": "Small",
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    }
}
```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="aeb07-309">Varaston näkyvyyden ohjelmointirajapinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="aeb07-309">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="aeb07-310">Ennen palvelun käyttöä on tehtävä valmiiksi seuraavissa aliosissa käsiteltävät määritykset.</span><span class="sxs-lookup"><span data-stu-id="aeb07-310">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="aeb07-311">Määritykset voivat vaihdella ympäristön tietojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="aeb07-311">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="aeb07-312">Siinä pääasiallisesti neljä osaa:</span><span class="sxs-lookup"><span data-stu-id="aeb07-312">It primarily includes four parts:</span></span>

- [<span data-ttu-id="aeb07-313">Osiointi</span><span class="sxs-lookup"><span data-stu-id="aeb07-313">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="aeb07-314">Dimensiomääritykset</span><span class="sxs-lookup"><span data-stu-id="aeb07-314">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="aeb07-315">Indeksointi</span><span class="sxs-lookup"><span data-stu-id="aeb07-315">Indexing</span></span>](#indexing)
- [<span data-ttu-id="aeb07-316">Mukautettu mitta</span><span class="sxs-lookup"><span data-stu-id="aeb07-316">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="aeb07-317">Osiointi</span><span class="sxs-lookup"><span data-stu-id="aeb07-317">Partitioning</span></span>

<span data-ttu-id="aeb07-318">Osiointi voi vaikuttaa merkittävästi varaston näkyvyyden ohjelmointirajapinnan toimintaan.</span><span class="sxs-lookup"><span data-stu-id="aeb07-318">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="aeb07-319">Niinpä kannattaakin määrittää rakenne, jossa voidaan ryhmitellä tietoja pienissä osissa siten, että merkitykselliset tietokyselyt ovat mahdollisia.</span><span class="sxs-lookup"><span data-stu-id="aeb07-319">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="aeb07-320">`organizationId` (Supply Chain Managementissa `dataAreaId`) sisältyy aina osiointiin, ja varaston näkyvyys osioidaan oletusarvoisesti dimensioiden perusteella, kuten *Toimipaikka + sijainti*.</span><span class="sxs-lookup"><span data-stu-id="aeb07-320">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="aeb07-321">Tämän vuoksi palveluissa tehtävissä kyselyissä on aina käytettävä suodattimissa määritettyjä dimensioita.</span><span class="sxs-lookup"><span data-stu-id="aeb07-321">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="aeb07-322">*Toimipaikka* ja *sijainti* ovat kaksi varaston näkyvyyden yleistä oletusdimensiota.</span><span class="sxs-lookup"><span data-stu-id="aeb07-322">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="aeb07-323">Supply Chain Managementin näiden dimensioiden nimet ovat *toimipaikka* (`InventSiteId`) ja *varasto* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="aeb07-323">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="aeb07-324">Dimensiomääritykset</span><span class="sxs-lookup"><span data-stu-id="aeb07-324">Dimension configurations</span></span>

<span data-ttu-id="aeb07-325">Varaston näkyvyyden yleisten oletusdimensioiden luettelon ansiosta usein lähdejärjestelmien integrointi on mahdollista.</span><span class="sxs-lookup"><span data-stu-id="aeb07-325">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="aeb07-326">Seuraavassa taulukossa on varastodimensiot, jotka tulevat varaston näkyvyyden oletusdimensionimiksi.</span><span class="sxs-lookup"><span data-stu-id="aeb07-326">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="aeb07-327">Dimensiotyyppi</span><span class="sxs-lookup"><span data-stu-id="aeb07-327">Dimension type</span></span> | <span data-ttu-id="aeb07-328">Dimension nimi</span><span class="sxs-lookup"><span data-stu-id="aeb07-328">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="aeb07-329">Tuote</span><span class="sxs-lookup"><span data-stu-id="aeb07-329">Product</span></span> | `ColorId` |
| <span data-ttu-id="aeb07-330">Tuote</span><span class="sxs-lookup"><span data-stu-id="aeb07-330">Product</span></span> | `SizeId` |
| <span data-ttu-id="aeb07-331">Tuote</span><span class="sxs-lookup"><span data-stu-id="aeb07-331">Product</span></span> | `StyleId` |
| <span data-ttu-id="aeb07-332">Tuote</span><span class="sxs-lookup"><span data-stu-id="aeb07-332">Product</span></span> | `ConfigId` |
| <span data-ttu-id="aeb07-333">Seuranta</span><span class="sxs-lookup"><span data-stu-id="aeb07-333">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="aeb07-334">Seuranta</span><span class="sxs-lookup"><span data-stu-id="aeb07-334">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="aeb07-335">Toimipaikka</span><span class="sxs-lookup"><span data-stu-id="aeb07-335">Location</span></span> | `LocationId` |
| <span data-ttu-id="aeb07-336">Toimipaikka</span><span class="sxs-lookup"><span data-stu-id="aeb07-336">Location</span></span> | `SiteId` |
| <span data-ttu-id="aeb07-337">Varaston tila</span><span class="sxs-lookup"><span data-stu-id="aeb07-337">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="aeb07-338">Varastokohtainen</span><span class="sxs-lookup"><span data-stu-id="aeb07-338">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="aeb07-339">Varastokohtainen</span><span class="sxs-lookup"><span data-stu-id="aeb07-339">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="aeb07-340">Varastokohtainen</span><span class="sxs-lookup"><span data-stu-id="aeb07-340">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="aeb07-341">Edellisessä taulukossa mainittu dimensiotyyppi on tarkoitettu vain tiedoksi.</span><span class="sxs-lookup"><span data-stu-id="aeb07-341">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="aeb07-342">Dimensiotyyppiä ei tarvitse määrittää varaston näkyvyydessä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-342">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="aeb07-343">Jos mukautettu dimensio on luotu ja sen on siirryttävä oletusarvoon, kun varaston näkyvyys käyttää sitä, **mukautetun dimension** nimi voidaan määrittää varaston näkyvyydessä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-343">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="aeb07-344">Ulkoiset järjestelmät käyttävät varaston näkyvyyttä RESTful API -ohjelmointirajapinnoilla, jotka ottavat käytettävissä olevat tiedot käyttöön annetuissa dimensiojoukoissa, joissa kyselyt tehdään.</span><span class="sxs-lookup"><span data-stu-id="aeb07-344">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="aeb07-345">Integroinnin osalta varaston näkyvyydessä voidaan määrittää *ulkoinen kanavan tietolähde* ja *kohdedimensioiden* lähdedimensio varaston näkyvyydessä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-345">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="aeb07-346">Kohdedimensioiden on oltava jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="aeb07-346">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="aeb07-347">Varaston näkyvyyden oletusdimensiot</span><span class="sxs-lookup"><span data-stu-id="aeb07-347">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="aeb07-348">Mukautetut dimensiot</span><span class="sxs-lookup"><span data-stu-id="aeb07-348">Custom dimensions</span></span>

<span data-ttu-id="aeb07-349">Dimensiomääritysten tarkoitus on standardoida monen järjestelmän integrointi dimensiokyselyitä ja tapahtuman dimensioihin kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="aeb07-349">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="aeb07-350">Indeksointi</span><span class="sxs-lookup"><span data-stu-id="aeb07-350">Indexing</span></span>

<span data-ttu-id="aeb07-351">Käytettävissä olevan varaston kysely ei ole useimmiten korkeimmalla kokonaistasolla, vaan tulokset halutaan ehkä nähdä varastodimensioiden mukaan koostettuina.</span><span class="sxs-lookup"><span data-stu-id="aeb07-351">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="aeb07-352">Varaston näkyvyys on joustava, sillä siinä voidaan määrittää dimensioon tai dimensioyhdistelmiin perustuvia indeksejä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-352">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="aeb07-353">Tällä hetkellä indeksejä voi määrittään enintään viisi.</span><span class="sxs-lookup"><span data-stu-id="aeb07-353">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="aeb07-354">Käytettävää dimensiota tai dimensioyhdistelmää on harkittava huolellisesti ennen toteutusta, sillä näin voidaan varmistaa, että se todella vastaa liiketoiminnan tarpeita.</span><span class="sxs-lookup"><span data-stu-id="aeb07-354">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="aeb07-355">Tuotekysely voidaan haluta tehdä esimerkiksi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="aeb07-355">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="aeb07-356">Kyselynä käytettävissä oleva koostetuote *väri*- ja *koko*-dimension mukaan.</span><span class="sxs-lookup"><span data-stu-id="aeb07-356">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="aeb07-357">Joissakin tapauksissa kyselyn kohteena voi olla tuote kokonaisuudessaan.</span><span class="sxs-lookup"><span data-stu-id="aeb07-357">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="aeb07-358">Kaksi indeksiä määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="aeb07-358">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="aeb07-359">Tyhjä hakasulje tekee koosteen osiossa olevan tuotetunnuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="aeb07-359">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="aeb07-360">Indeksointi määrittää, miten tulokset ryhmitellään `groupBy`-kyselyasetuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="aeb07-360">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="aeb07-361">Jos tässä tapauksessa ei määritetä `groupBy`-arvoja, tuloksena on `productid`-kohtainen kokonaismäärä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-361">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="aeb07-362">Jos `groupBy`-määrityksenä on sen sijaan `groupBy=ColorId&groupBy=SizeId`, tuloksena on useita rivejä, jotka perustuvat järjestelmässä oleviin väri- ja kokoyhdistelmiin.</span><span class="sxs-lookup"><span data-stu-id="aeb07-362">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="aeb07-363">Kyselyehdot voidaan asettaa pyynnön tekstiosaan.</span><span class="sxs-lookup"><span data-stu-id="aeb07-363">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="aeb07-364">Seuraavassa esimerkissä on väri- ja kokoyhdistelmää käyttävä tuotekysely.</span><span class="sxs-lookup"><span data-stu-id="aeb07-364">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct1", "MyProduct2"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

<span data-ttu-id="aeb07-365">`filters`-kenttää varten vain `ProductId` tukee tällä hetkellä useita arvoja.</span><span class="sxs-lookup"><span data-stu-id="aeb07-365">For the `filters` field, currently only `ProductId` supports multiple values.</span></span> <span data-ttu-id="aeb07-366">Jos `ProductId` on tyhjä matriisi, kaikkia tuotteita kysellään.</span><span class="sxs-lookup"><span data-stu-id="aeb07-366">If the `ProductId` is an empty array, all products will be queried.</span></span>

#### <a name="custom-measurement"></a><span data-ttu-id="aeb07-367">Mukautettu mitta</span><span class="sxs-lookup"><span data-stu-id="aeb07-367">Custom measurement</span></span>

<span data-ttu-id="aeb07-368">Oletusmittamäärät linkitetään Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="aeb07-368">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="aeb07-369">Haluat ehkä kuitenkin määrän, joka koostuu oletusmitoista.</span><span class="sxs-lookup"><span data-stu-id="aeb07-369">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="aeb07-370">Sitä varten on määritettävä mukautettuja määritä, jotka lisätään käytettävissä olevan määrän tulosteisiin.</span><span class="sxs-lookup"><span data-stu-id="aeb07-370">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="aeb07-371">Toiminnon antaa yksinkertaisesti mahdollisuuden määrittää lisättävän ja/tai vähennettävän mittajoukon, joiden avulla voidaan muodostaa mukautettu mitta.</span><span class="sxs-lookup"><span data-stu-id="aeb07-371">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="aeb07-372">Esimerkiksi seuraavalla kyselyehdolla määritetään mukautetun mitan määräksi `MyCustomAvailableforReservation`, jonka kulutusjärjestelmä käyttää.</span><span class="sxs-lookup"><span data-stu-id="aeb07-372">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| <span data-ttu-id="aeb07-373">Kulutusjärjestelmä</span><span class="sxs-lookup"><span data-stu-id="aeb07-373">Consumption system</span></span> | <span data-ttu-id="aeb07-374">Lasketut mitat</span><span class="sxs-lookup"><span data-stu-id="aeb07-374">Calculated measurers</span></span> | <span data-ttu-id="aeb07-375">Tietolähde</span><span class="sxs-lookup"><span data-stu-id="aeb07-375">Data source</span></span> | <span data-ttu-id="aeb07-376">Määre</span><span class="sxs-lookup"><span data-stu-id="aeb07-376">Modifier</span></span> | <span data-ttu-id="aeb07-377">Määreen laskentatyyppi</span><span class="sxs-lookup"><span data-stu-id="aeb07-377">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="aeb07-378">Lisäys</span><span class="sxs-lookup"><span data-stu-id="aeb07-378">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="aeb07-379">Lisäys</span><span class="sxs-lookup"><span data-stu-id="aeb07-379">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="aeb07-380">Vähennyslasku</span><span class="sxs-lookup"><span data-stu-id="aeb07-380">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="aeb07-381">Lisäys</span><span class="sxs-lookup"><span data-stu-id="aeb07-381">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="aeb07-382">Vähennyslasku</span><span class="sxs-lookup"><span data-stu-id="aeb07-382">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="aeb07-383">Lisäys</span><span class="sxs-lookup"><span data-stu-id="aeb07-383">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="aeb07-384">Lisäys</span><span class="sxs-lookup"><span data-stu-id="aeb07-384">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="aeb07-385">Vähennyslasku</span><span class="sxs-lookup"><span data-stu-id="aeb07-385">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="aeb07-386">Vähennyslasku</span><span class="sxs-lookup"><span data-stu-id="aeb07-386">Subtraction</span></span> |

<span data-ttu-id="aeb07-387">Mukautetun mittamäärän kysely palauttaa sitten seuraavan tuloksen.</span><span class="sxs-lookup"><span data-stu-id="aeb07-387">With that, the query on the custom measurement quantity will return the following output.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="aeb07-388">`MyCustomAvailableforReservation`-tulos perustuu seuraavaan mukautettujen mittojen laskenta-asetukseen:</span><span class="sxs-lookup"><span data-stu-id="aeb07-388">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="aeb07-389">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="aeb07-389">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="aeb07-390">Varastosaldon muutosten kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="aeb07-390">Posting on-hand changes</span></span>

<span data-ttu-id="aeb07-391">Tarkka URL-osoite, johon tapahtuma kirjataan, määräytyy maantieteellisen alueen mukaan.</span><span class="sxs-lookup"><span data-stu-id="aeb07-391">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="aeb07-392">Sen muoto on seuraava:</span><span class="sxs-lookup"><span data-stu-id="aeb07-392">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="aeb07-393">Tätä URL-osoitetta käytetään todennuksessa HTTP `POST` -menetelmän ohella lähettämään varastosaldon muutostapahtumat palveluun.</span><span class="sxs-lookup"><span data-stu-id="aeb07-393">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="aeb07-394">Dynamics 365 -palvelun kanssa HTTP-pyyntöjen avulla tapahtuvassa viestinnässä käytetään erityisotsikko, joka ilmaisee sen Supply Chain Management -esiintymän ympäristötunnuksen, johon tiedot on linkitetty.</span><span class="sxs-lookup"><span data-stu-id="aeb07-394">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="aeb07-395">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="aeb07-395">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="aeb07-396">Varastosaldon muutosten kirjaamisen kyselyesimerkki 1</span><span class="sxs-lookup"><span data-stu-id="aeb07-396">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="aeb07-397">Tässä esimerkissä on skenaario, jossa dimensiomääritys määritetään Power Appsissa.</span><span class="sxs-lookup"><span data-stu-id="aeb07-397">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="aeb07-398">Määritä dimension yhdistämismääritys Power Appsissa käyttämällä seuraavaa kyselyä:</span><span class="sxs-lookup"><span data-stu-id="aeb07-398">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="aeb07-399">Voit nyt tehdä `dimensionDataSource`-määrityksen ja käyttää mukautettuja dimensioita kyselyissä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-399">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="aeb07-400">Järjestelmä muuntaa mukautetut dimensiot automaattisesti perusdimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="aeb07-400">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="aeb07-401">Varastosaldon muutosten kirjaamisen kyselyesimerkki 2</span><span class="sxs-lookup"><span data-stu-id="aeb07-401">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="aeb07-402">Tässä esimerkissä on skenaario, jossa yhtään dimensiomäärityksen yhdistämismääritystä ei määritetä Power Appsissa, joten myös kirjaamisessa on käytettävä perusdimensioita.</span><span class="sxs-lookup"><span data-stu-id="aeb07-402">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="aeb07-403">Kaikkien dimensioiden on oltava perusdimensioita, kun `dimensionDataSource`-kentässä on tyhjäarvo, se on tyhjä tai siinä on välilyönti.</span><span class="sxs-lookup"><span data-stu-id="aeb07-403">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a><span data-ttu-id="aeb07-404">JSON-tiedostokentän ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="aeb07-404">JSON document field properties</span></span>

<span data-ttu-id="aeb07-405">Aiemmin käsitellyissä JSON-kyselyesimerkkien kentissä oli seuraavassa taulukossa olevia ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="aeb07-405">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="aeb07-406">Kentän tunnus</span><span class="sxs-lookup"><span data-stu-id="aeb07-406">Field ID</span></span> | <span data-ttu-id="aeb07-407">kuvaus</span><span class="sxs-lookup"><span data-stu-id="aeb07-407">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="aeb07-408">Tietyn muutostapahtuman yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="aeb07-408">A unique ID for the specific change event.</span></span> <span data-ttu-id="aeb07-409">Tämän tunnuksen avulla varmistetaan, että jos viestintä palveluun epäonnistuu kirjauksen aikana, tapahtuman lähettäminen uudelleen ei aiheuta saman tapahtuman laskemista kahdesti järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-409">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="aeb07-410">Tapahtumaan linkitetyn organisaation tunnus.</span><span class="sxs-lookup"><span data-stu-id="aeb07-410">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="aeb07-411">Tämä yhdistetään Supply Chain Management -organisaatioihin tai tietoalueen tunnuksiin.</span><span class="sxs-lookup"><span data-stu-id="aeb07-411">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="aeb07-412">Kyseisen tuotteen tunniste.</span><span class="sxs-lookup"><span data-stu-id="aeb07-412">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="aeb07-413">Määrä, jolla varastosaldoa on muutettava.</span><span class="sxs-lookup"><span data-stu-id="aeb07-413">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="aeb07-414">Jos hyllylle esimerkiksi lisättiin 10 uutta sämpylää, tämä arvo 10.</span><span class="sxs-lookup"><span data-stu-id="aeb07-414">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="aeb07-415">Jos 3 sämpylää sitten poistettiin hyllystä tai myyntiin, tämä arvo on -3.</span><span class="sxs-lookup"><span data-stu-id="aeb07-415">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="aeb07-416">Muutostapahtuman kirjauksessa ja kyselyssä käytettävien dimensioiden tietolähde.</span><span class="sxs-lookup"><span data-stu-id="aeb07-416">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="aeb07-417">Jos tietolähde määritetään, määritetyn tietolähteen mukautettuja dimensioita voidaan käyttää.</span><span class="sxs-lookup"><span data-stu-id="aeb07-417">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="aeb07-418">Dimensiomääritysten ansiosta varaston näkyvyys voi yhdistää mukautetut dimensiot yleisiin oletusdimensioihin.</span><span class="sxs-lookup"><span data-stu-id="aeb07-418">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="aeb07-419">Jos `dimensionDataSource` ei ole määritetty, kyselyissä voi käyttää vain yleisiä oletusdimensioita.</span><span class="sxs-lookup"><span data-stu-id="aeb07-419">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="aeb07-420">Dynaaminen avain- ja arvoparisäilö.</span><span class="sxs-lookup"><span data-stu-id="aeb07-420">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="aeb07-421">Ne yhdistetään joihinkin Supply Chain Managementin dimensioihin, minkä lisäksi voidaan lisätä mukautettuja dimensioita (kuten *Lähde*), jotka voivat ilmaista, saapuuko tapahtuma Supply Chain Managementista vai ulkoisesta järjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-421">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="aeb07-422">Kyselyt nykyisessä varastosaldossa</span><span class="sxs-lookup"><span data-stu-id="aeb07-422">Querying current on-hand</span></span>

<span data-ttu-id="aeb07-423">Nykyisen varastosaldon kyselyjen päätepisteessä on samankaltainen URL-osoite:</span><span class="sxs-lookup"><span data-stu-id="aeb07-423">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="aeb07-424">Kysely siinä tehdään HTTP `POST` -menetelmällä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-424">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="aeb07-425">Nykyisen varastosaldon kyselyesimerkki 1</span><span class="sxs-lookup"><span data-stu-id="aeb07-425">Current on-hand query example 1</span></span>

<span data-ttu-id="aeb07-426">Tässä esimerkissä on skenaario, jossa Power Appsissa on jo valmis dimensiomääritys.</span><span class="sxs-lookup"><span data-stu-id="aeb07-426">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="aeb07-427">Määritä dimension yhdistämismääritys Power Appsissa käyttämällä seuraavaa kyselyä:</span><span class="sxs-lookup"><span data-stu-id="aeb07-427">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="aeb07-428">Voit nyt tehdä `dimensionDataSource`-määrityksen ja käyttää mukautettuja dimensioita kyselyissä.</span><span class="sxs-lookup"><span data-stu-id="aeb07-428">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="aeb07-429">Järjestelmä muuntaa mukautetut dimensiot automaattisesti perusdimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="aeb07-429">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="aeb07-430">`DimensionDataSource` voidaan määrittää `filters`-kohdassa ja mukautetut dimensiot vodaan määrittää sekä `filters`- että `groupByValues`-kohdissa.</span><span class="sxs-lookup"><span data-stu-id="aeb07-430">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="aeb07-431">Järjestelmä muuntaa mukautetut dimensiot automaattisesti perusdimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="aeb07-431">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="aeb07-432">Nykyisen varastosaldon kyselyesimerkki 2</span><span class="sxs-lookup"><span data-stu-id="aeb07-432">Current on-hand query example 2</span></span>

<span data-ttu-id="aeb07-433">Tässä esimerkissä on skenaario, jossa yhtään dimensiomäärityksen yhdistämismääritystä ei määritetä Power Appsissa, joten myös kirjaamisessa on käytettävä perusdimensioita.</span><span class="sxs-lookup"><span data-stu-id="aeb07-433">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="aeb07-434">Kaikkien dimensioiden on oltava perusdimensioita, kun `filters`-kohdan `dimensionDataSource`-kentässä on tyhjäarvo, se on tyhjä tai siinä on välilyönti.</span><span class="sxs-lookup"><span data-stu-id="aeb07-434">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a><span data-ttu-id="aeb07-435">Palautetun tuloksen esimerkki</span><span class="sxs-lookup"><span data-stu-id="aeb07-435">Example return result</span></span>

<span data-ttu-id="aeb07-436">Edellisten esimerkkien kyselyissä voitiin palauttaa seuraavankaltainen tulos.</span><span class="sxs-lookup"><span data-stu-id="aeb07-436">The queries shown in the previous examples could return a result like this.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="aeb07-437">Huomaa, että määräkentät on jäsennelty mittahakemistoksi ja niihin liittyviksi arvoiksi.</span><span class="sxs-lookup"><span data-stu-id="aeb07-437">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
