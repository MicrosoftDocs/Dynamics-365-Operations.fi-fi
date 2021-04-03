---
title: Varaston näkyvyyden apuohjelma
description: Tässä aiheessa käsitellään Dynamics 365 Supply Chain Managementin varaston näkyvyyden apuohjelman asentamista ja määrittämistä.
author: sherry-zheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e588be2ac5aae395ca66e3c9a743a67d71db7c0
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574219"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="f7cf0-103">Varaston näkyvyyden apuohjelma</span><span class="sxs-lookup"><span data-stu-id="f7cf0-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="f7cf0-104">Varaston näkyvyyden apuohjelma on itsenäinen ja erittäin skaalautuva mikropalvelu, joka mahdollistaa reaaliaikaisen käytettävissä olevan varaston seurannan ja antaa tällä tavoin yleisen näkymän varaston näkyvyyteen.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="f7cf0-105">Kaikki käytettävissä olevaan varastoon liittyvät tiedot viedään palveluun lähes reaaliaikaisesti käyttämällä matala-asteista SQL-integraatiota.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="f7cf0-106">Ulkoiset palvelut käyttävät palvelut tekevät RESTful API -ohjelmointirajapinnoilla käytettävissä olevien tietojen kyselyjä annetuissa dimensioissa ja saavat tällä tavoin luettelon käytettävissä olevista paikoista.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="f7cf0-107">Varaston näkyvyys on Microsoft Dataverseen perustuva mikropalvelu, joten sitä voi laajentaa muodostamalla Power Apps -sovelluksia ja käyttämällä Power BI:ta tuottamaan liiketoiminnan tarpeita vastaavia mukautettuja toimintoja.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="f7cf0-108">Indeksi voidaan lisäksi päivittää tekemään varastokyselyjä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="f7cf0-109">Varaston näkyvyydessä on määritysvaihtoehtoja, joiden avulla sen voi integroida useiden kolmannen osapuolen järjestelmien kanssa.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="f7cf0-110">Se tukee standardoitua varastodimensiota, mukautettua laajennettavuutta ja standardoituja, määritettäviä laskettuja määriä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="f7cf0-111">Tässä aiheessa käsitellään Dynamics 365 Supply Chain Managementin varaston näkyvyyden apuohjelman asentamista ja määrittämistä sekä sen ohjelmointirajapinnan käyttöä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="f7cf0-112">Varaston näkyvyyden lisäapuohjelman asentaminen</span><span class="sxs-lookup"><span data-stu-id="f7cf0-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="f7cf0-113">Varaston näkyvyyden lisäapuohjelman asentamiseen on käytettävä Microsoft Dynamics Lifecycle Servicesiä (LCS).</span><span class="sxs-lookup"><span data-stu-id="f7cf0-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="f7cf0-114">LCS on yhteistyöportaali, jonka muodostamassa ympäristössä ja jonka säännöllisesti päivitetyillä palveluilla voi hallita Dynamics 365 Finance and Operations -sovellusten elinkaarta.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="f7cf0-115">Lisätietoja on kohdassa [Lifecycle Services -resurssit](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="f7cf0-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="f7cf0-116">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="f7cf0-116">Prerequisites</span></span>

<span data-ttu-id="f7cf0-117">Ennen varaston näkyvyyden apuohjelman asentamista:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="f7cf0-118">Hanki LCS-toteutusprojekti, jossa on otettu käyttöön vähintään yksi ympäristö.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="f7cf0-119">Varmista, että kohdassa [Lisäosien yleiskatsaus](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) annetut edellytykset lisäosien määrittämiselle on täytetty.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="f7cf0-120">Varaston näkyvyys ei edellytä kaksoiskirjoituslinkitystä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="f7cf0-121">Ota yhteyttä varaston näkyvyyden tiimiin [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), jotta saat seuraavat kolme vaadittua tiedostoa:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>

    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="f7cf0-122">`Inventory Visibility Integration.zip` (jos käynnissä ollut Supply Chain Managementin versio on aiempi kuin 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="f7cf0-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>

> [!NOTE]
> <span data-ttu-id="f7cf0-123">Tällä hetkellä tuettuja maita ja alueita ovat Kanada, Yhdysvallat ja Euroopan unioni (EU).</span><span class="sxs-lookup"><span data-stu-id="f7cf0-123">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="f7cf0-124">Jos sinulla on näitä edellytyksiä koskevia kysymyksiä, ota yhteys varaston näkyvyyden tuotetiimiin.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-124">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="f7cf0-125">Määritys Dataverse</span><span class="sxs-lookup"><span data-stu-id="f7cf0-125">Set up Dataverse</span></span>

<span data-ttu-id="f7cf0-126">Määritä Dataverse noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-126">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="f7cf0-127">Lisää palveluperiaate vuokraajaan:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-127">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="f7cf0-128">Asenna Azure AD PowerShell Module v2, kuten kuvattu kohdassa [Asenna Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="f7cf0-128">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="f7cf0-129">Suorita seuraava PowerShell-komento.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-129">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="f7cf0-130">Luo sovelluskäyttäjä varaston näkyvyydelle Dataversessä:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-130">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="f7cf0-131">Avaa Dataverse-ympäristön URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-131">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="f7cf0-132">Valitse **Lisäasetukset \> Järjestelmä \> Suojaus \> Käyttäjät** ja luo sovelluskäyttäjä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-132">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="f7cf0-133">Vaihda sivunäkymäksi **Sovelluskäyttäjät** näkymävalikossa.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-133">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="f7cf0-134">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-134">Select **New**.</span></span> <span data-ttu-id="f7cf0-135">Aseta sovellustunnukseksi *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-135">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="f7cf0-136">(Objektin tunnus ladataan automaattisesti, kun tallennat muutokset.) Voit mukauttaa nimeä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-136">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="f7cf0-137">Voit muuttaa sen esimerkiksi nimeksi *Varaston näkyvyys*.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-137">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="f7cf0-138">Kun olet valmis, valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-138">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="f7cf0-139">Valitse **Määritä rooli** ja valitse sitten **Järjestelmänvalvoja**.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-139">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="f7cf0-140">Jos saatavana on rooli nimeltä **Common Data Service -käyttäjä**, valitse myös se.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-140">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="f7cf0-141">Lisätietoja on kohdassa [Sovelluskäyttäjän luominen](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="f7cf0-141">For more information, see [Create an application user](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="f7cf0-142">Tuo `Inventory Visibility Dataverse Solution.zip` -tiedosto, joka sisältää Dataverse-konfiguraatioon liittyvät entiteetit ja Power Apps -sovellukset:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-142">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="f7cf0-143">Siirry **Ratkaisut**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-143">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="f7cf0-144">Valitse **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-144">Select **Import**.</span></span>

1. <span data-ttu-id="f7cf0-145">Tuo konfiguraation päivityksen käynnistimen työnkulku:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-145">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="f7cf0-146">Siirry Microsoft Flow -sivulle.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-146">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="f7cf0-147">Varmista, että yhteys nimeltä *Dataverse (vanha)* on olemassa.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-147">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="f7cf0-148">(Jos sitä ei ole olemassa, luo se.)</span><span class="sxs-lookup"><span data-stu-id="f7cf0-148">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="f7cf0-149">Tuo `Inventory Visibility Configuration Trigger.zip` -tiedosto.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-149">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="f7cf0-150">Kun käynnistys on tuotu, se näkyy **Omat työnkulut** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-150">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="f7cf0-151">Alusta seuraavat neljä muuttujaa ympäristön tietojen perusteella:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-151">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="f7cf0-152">Azure-vuokraajan tunnus</span><span class="sxs-lookup"><span data-stu-id="f7cf0-152">Azure Tenant ID</span></span>
        - <span data-ttu-id="f7cf0-153">Azure-sovelluksen asiakastunnus</span><span class="sxs-lookup"><span data-stu-id="f7cf0-153">Azure Application Client ID</span></span>
        - <span data-ttu-id="f7cf0-154">Azure-sovelluksen asiakasohjelman salasana</span><span class="sxs-lookup"><span data-stu-id="f7cf0-154">Azure Application Client Secret</span></span>
        - <span data-ttu-id="f7cf0-155">Varaston näkyvyyden päätepiste</span><span class="sxs-lookup"><span data-stu-id="f7cf0-155">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="f7cf0-156">Lisätietoja tästä muuttujasta on jäljempänä tässä ohjeaiheessa kohdassa [Varaston näkyvyyden integraation määrittäminen](#setup-inventory-visibility-integration).</span><span class="sxs-lookup"><span data-stu-id="f7cf0-156">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="f7cf0-157">![Määrityksen käynnistin](media/configuration-trigger.png "Määrityksen käynnistin")</span><span class="sxs-lookup"><span data-stu-id="f7cf0-157">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="f7cf0-158">Valitse **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-158">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="f7cf0-159">Lisäosan asentaminen</span><span class="sxs-lookup"><span data-stu-id="f7cf0-159">Install the add-in</span></span>

<span data-ttu-id="f7cf0-160">Varaston näkyvyyden apuohjelman asentaminen:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-160">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="f7cf0-161">Kirjaudu [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) -portaaliin.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-161">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="f7cf0-162">Valitse aloitussivulla projekti, jossa ympäristö on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-162">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="f7cf0-163">Valitse projektisivulla ympäristö, johon haluat asentaa apuohjelman.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-163">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="f7cf0-164">Siirry ympäristösivulla alaspäin, kunnes näet **Ympäristön lisäosat** -kohdan **Power Platform -integraatio** -kohdassa, josta löytyy Dataverse-ympäristön nimi.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-164">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="f7cf0-165">Valitse **Ympäristöapuohjelmat**-osassa **Asenna uusi apuohjelma**.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-165">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="f7cf0-166">![Ympäristösivu LCS:ssa](media/inventory-visibility-environment.png "Ympäristösivu LCS:ssa")</span><span class="sxs-lookup"><span data-stu-id="f7cf0-166">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="f7cf0-167">Valitse **Asenna uusi apuohjelma** -linkki.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-167">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="f7cf0-168">Käytettävissä olevien apuohjelmien luettelo avautuu.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-168">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="f7cf0-169">Valitse luettelosta **Vataston näkyvyys**.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-169">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="f7cf0-170">Anna arvot seuraavissa ympäristön kentissä:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-170">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="f7cf0-171">**AAD-sovelluksen (asiakasohjelman) tunnus**</span><span class="sxs-lookup"><span data-stu-id="f7cf0-171">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="f7cf0-172">**AAD-vuokraajan tunnus**</span><span class="sxs-lookup"><span data-stu-id="f7cf0-172">**AAD tenant ID**</span></span>

    <span data-ttu-id="f7cf0-173">![Apuohjelman määrityssivu](media/inventory-visibility-setup.png "Apuohjelman määrityssivu")</span><span class="sxs-lookup"><span data-stu-id="f7cf0-173">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="f7cf0-174">Hyväksy käyttöehdot valitsemalla **Käyttöehdot**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-174">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="f7cf0-175">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-175">Select **Install**.</span></span> <span data-ttu-id="f7cf0-176">Apuohjelman tilana näkyy nyt **Asennetaan**.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-176">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="f7cf0-177">Se on valmis, päivitä sivu, jonka jälkeen tilana on **Asennettu**.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-177">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="f7cf0-178">Lisäosan asennuksen poistaminen</span><span class="sxs-lookup"><span data-stu-id="f7cf0-178">Uninstall the add-in</span></span>

<span data-ttu-id="f7cf0-179">Poista apuohjelman asennus valitsemalla **Poista asennus**.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-179">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="f7cf0-180">Kun päivität LCS:n, varaston näkyvyyden apuohjelma poistetaan.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-180">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="f7cf0-181">Asennuksen poistoprosessi poistaa apuohjelman rekisteröinnin sekä käynnistää kaikkien palveluun tallennettujen liiketoimintatietojen puhdistustyön.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-181">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="f7cf0-182">Käytettävissä olevan varaston tietojen käyttäminen Supply Chain Managementista</span><span class="sxs-lookup"><span data-stu-id="f7cf0-182">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="f7cf0-183">Varaston näkyvyyden integrointipaketin käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="f7cf0-183">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="f7cf0-184">Jos käytössäsi on Supply Chain Management -versio 10.0.17 tai aiempi, ota yhteyttä varaston näkyvyyden tukihenkilöstöön osoitteessa [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) saadaksesi pakettitiedoston.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-184">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="f7cf0-185">Ota sitten paketti käyttöön LCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-185">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="f7cf0-186">Jos käyttöönoton aikana ilmenee version vastaavuusvirhe, X++-projekti on tuotava manuaalisesti kehitysympäristöön.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-186">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="f7cf0-187">Luo sitten käyttöön otettava paketti kehitysympäristössä ja ota se käyttöön tuotantoympäristössä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-187">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="f7cf0-188">Koodi sisältyy Supply Chain Management -versioon 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-188">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="f7cf0-189">Jos käytössä on tämä versio tai myöhempi versio, käyttöönottoa ei tarvita.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-189">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="f7cf0-190">Varmista, että seuraavat ominaisuudet on otettu käyttöön Supply Chain Management -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-190">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="f7cf0-191">(Oletusarvon mukaan ne ovat käytössä.)</span><span class="sxs-lookup"><span data-stu-id="f7cf0-191">(By default, they are turned on.)</span></span>

| <span data-ttu-id="f7cf0-192">Toiminnon kuvaus</span><span class="sxs-lookup"><span data-stu-id="f7cf0-192">Feature description</span></span> | <span data-ttu-id="f7cf0-193">Koodiversio</span><span class="sxs-lookup"><span data-stu-id="f7cf0-193">Code version</span></span> | <span data-ttu-id="f7cf0-194">Vaihda luokka</span><span class="sxs-lookup"><span data-stu-id="f7cf0-194">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="f7cf0-195">Varastodimensioiden ottaminen käyttöön InventSum-taulussa tai poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="f7cf0-195">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="f7cf0-196">10.0.11</span><span class="sxs-lookup"><span data-stu-id="f7cf0-196">10.0.11</span></span> | <span data-ttu-id="f7cf0-197">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="f7cf0-197">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="f7cf0-198">Varastodimensioiden ottaminen käyttöön InventSumDelta-taulussa tai poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="f7cf0-198">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="f7cf0-199">10.0.12</span><span class="sxs-lookup"><span data-stu-id="f7cf0-199">10.0.12</span></span> | <span data-ttu-id="f7cf0-200">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="f7cf0-200">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="f7cf0-201">Määritä Varaston näkyvyyden integrointi</span><span class="sxs-lookup"><span data-stu-id="f7cf0-201">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="f7cf0-202">Avaa Supply Chain Managementissa **[Ominaisuuden hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** -työtila ja ota käyttöön **Varaston näkyvyyden integraatio** -ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-202">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="f7cf0-203">Siirry kohtaan **Varastonhallinta \> Määritys \> Varaston näkyvyyden integraation parametrit** ja kirjoita sen ympäristön URL-osoite, jossa varaston näkyvyys on käytössä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-203">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="f7cf0-204">Etsi LCS-ympäristösi Azure-alue ja kirjoita sitten URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-204">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="f7cf0-205">URL-osoitteessa on seuraava muoto:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-205">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="f7cf0-206">Esimerkiksi Euroopassa ympäristössäsi on jokin seuraavista URL-osoitteista:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-206">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com/`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="f7cf0-207">Seuraavat alueet ovat käytettävissä tällä hetkellä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-207">The following regions are currently available.</span></span>

    | <span data-ttu-id="f7cf0-208">Azure-alue</span><span class="sxs-lookup"><span data-stu-id="f7cf0-208">Azure region</span></span> | <span data-ttu-id="f7cf0-209">Alueen lyhyt nimi</span><span class="sxs-lookup"><span data-stu-id="f7cf0-209">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="f7cf0-210">Itä-Australia</span><span class="sxs-lookup"><span data-stu-id="f7cf0-210">Australia east</span></span> | <span data-ttu-id="f7cf0-211">eau</span><span class="sxs-lookup"><span data-stu-id="f7cf0-211">eau</span></span> |
    | <span data-ttu-id="f7cf0-212">Kaakkois-Australia</span><span class="sxs-lookup"><span data-stu-id="f7cf0-212">Australia southeast</span></span> | <span data-ttu-id="f7cf0-213">seau</span><span class="sxs-lookup"><span data-stu-id="f7cf0-213">seau</span></span> |
    | <span data-ttu-id="f7cf0-214">Kanada, keskinen</span><span class="sxs-lookup"><span data-stu-id="f7cf0-214">Canada central</span></span> | <span data-ttu-id="f7cf0-215">cca</span><span class="sxs-lookup"><span data-stu-id="f7cf0-215">cca</span></span> |
    | <span data-ttu-id="f7cf0-216">Kanada, itäinen</span><span class="sxs-lookup"><span data-stu-id="f7cf0-216">Canada east</span></span> | <span data-ttu-id="f7cf0-217">eca</span><span class="sxs-lookup"><span data-stu-id="f7cf0-217">eca</span></span> |
    | <span data-ttu-id="f7cf0-218">Pohjois-Eurooppa</span><span class="sxs-lookup"><span data-stu-id="f7cf0-218">North Europe</span></span> | <span data-ttu-id="f7cf0-219">neu</span><span class="sxs-lookup"><span data-stu-id="f7cf0-219">neu</span></span> |
    | <span data-ttu-id="f7cf0-220">Länsi-Eurooppa</span><span class="sxs-lookup"><span data-stu-id="f7cf0-220">West Europe</span></span> | <span data-ttu-id="f7cf0-221">weu</span><span class="sxs-lookup"><span data-stu-id="f7cf0-221">weu</span></span> |
    | <span data-ttu-id="f7cf0-222">Itä-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="f7cf0-222">East US</span></span> | <span data-ttu-id="f7cf0-223">eus</span><span class="sxs-lookup"><span data-stu-id="f7cf0-223">eus</span></span> |
    | <span data-ttu-id="f7cf0-224">Länsi-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="f7cf0-224">West US</span></span> | <span data-ttu-id="f7cf0-225">wus</span><span class="sxs-lookup"><span data-stu-id="f7cf0-225">wus</span></span> |

1. <span data-ttu-id="f7cf0-226">Valitse **Varastonhallinta \> Kausittainen \> Varaston näkyvyyden integraatio** ja ota työ käyttöön.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-226">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="f7cf0-227">Kaikki Supply Chain Managementin varastomuutostapahtumat kirjataan nyt varaston näkyvyyteen.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-227">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="f7cf0-228">Varaston näkyvyyden apuohjelman julkinen ohjelmointirajapinta</span><span class="sxs-lookup"><span data-stu-id="f7cf0-228">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="f7cf0-229">Varaston näkyvyyden apuohjelman julkinen REST API sisältää useita nimenomaisia integroinnin päätepisteitä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-229">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="f7cf0-230">Se tukee kolmea pääasiallista vuorovaikutustyyppiä:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-230">It supports three main interaction types:</span></span>

- <span data-ttu-id="f7cf0-231">Varastosaldon määrän muutosten kirjaaminen apuohjelmaan ulkoisesta järjestelmästä</span><span class="sxs-lookup"><span data-stu-id="f7cf0-231">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="f7cf0-232">Nykyisten käytettävissä olevien määrien kysely ulkoisesta järjestelmästä</span><span class="sxs-lookup"><span data-stu-id="f7cf0-232">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="f7cf0-233">Automaattinen synkronointi Supply Chain Managementin käytettävissä olevan varaston kanssa</span><span class="sxs-lookup"><span data-stu-id="f7cf0-233">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="f7cf0-234">Automaattinen synkronointi ei kuulu julkiseen ohjelmointirajapintaan.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-234">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="f7cf0-235">Sen sijaan sitä käsitellään niiden ympäristöjen taustalla, joissa varaston näkyvyyden apuohjelma on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-235">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="f7cf0-236">Todennus</span><span class="sxs-lookup"><span data-stu-id="f7cf0-236">Authentication</span></span>

<span data-ttu-id="f7cf0-237">Ympäristön suojaustunnuksen avulla kutsutaan varaston näkyvyyden apuohjelmaa.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-237">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="f7cf0-238">Siksi sinun on luotava *Azure Active Directory (Azure AD) -tunnus* Azure AD -sovelluksen avulla.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-238">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="f7cf0-239">Tämän jälkeen Azure AD -tunnuksen avulla saat *käyttöoikeustunnuksen* suojauspalvelusta.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-239">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="f7cf0-240">Palvelun suojaustunnus haetaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-240">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="f7cf0-241">Kirjaudu Azure-portaaliin ja etsi sen avulla Supply Chain Management -sovelluksen `clientId` ja `clientSecret`.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-241">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="f7cf0-242">Nouda Azure Active Directory -tunnus (`aadToken`) lähettämällä HTTP-pyyntö, jossa on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-242">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="f7cf0-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="f7cf0-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="f7cf0-244">**Tapa** - `GET`</span><span class="sxs-lookup"><span data-stu-id="f7cf0-244">**Method** - `GET`</span></span>
    - <span data-ttu-id="f7cf0-245">**Tekstisisältö (lomaketiedot)**:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-245">**Body content (form data)**:</span></span>

        | <span data-ttu-id="f7cf0-246">avain</span><span class="sxs-lookup"><span data-stu-id="f7cf0-246">key</span></span> | <span data-ttu-id="f7cf0-247">arvo</span><span class="sxs-lookup"><span data-stu-id="f7cf0-247">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="f7cf0-248">client_id</span><span class="sxs-lookup"><span data-stu-id="f7cf0-248">client_id</span></span> | <span data-ttu-id="f7cf0-249">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="f7cf0-249">${aadAppId}</span></span> |
        | <span data-ttu-id="f7cf0-250">client_secret</span><span class="sxs-lookup"><span data-stu-id="f7cf0-250">client_secret</span></span> | <span data-ttu-id="f7cf0-251">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="f7cf0-251">${aadAppSecret}</span></span> |
        | <span data-ttu-id="f7cf0-252">grant_type</span><span class="sxs-lookup"><span data-stu-id="f7cf0-252">grant_type</span></span> | <span data-ttu-id="f7cf0-253">client_credentials</span><span class="sxs-lookup"><span data-stu-id="f7cf0-253">client_credentials</span></span> |
        | <span data-ttu-id="f7cf0-254">resurssi</span><span class="sxs-lookup"><span data-stu-id="f7cf0-254">resource</span></span> | <span data-ttu-id="f7cf0-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="f7cf0-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="f7cf0-256">Vastauksena pitäisi olla `aadToken` , joka muistuttaa seuraavaa esimerkkiä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-256">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="f7cf0-257">Muodosta seuraavankaltainen JSON-pyyntö:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-257">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="f7cf0-258">Jossa:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-258">Where:</span></span>
    - <span data-ttu-id="f7cf0-259">`client_assertion`-arvon on oltava edellisessä vaiheessa vastaanotettu `aadToken`.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-259">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="f7cf0-260">`context`-arvon on oltava ympäristötunnus, jossa apuohjelma halutaan ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-260">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="f7cf0-261">Kaikki muut arvot määritetään samoiksi kuin esimerkissä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-261">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="f7cf0-262">Lähetä HTTP-pyyntö, jossa on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-262">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="f7cf0-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="f7cf0-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="f7cf0-264">**Tapa** - `POST`</span><span class="sxs-lookup"><span data-stu-id="f7cf0-264">**Method** - `POST`</span></span>
    - <span data-ttu-id="f7cf0-265">**HTTP-otsikko** - sisällytä ohjelmointirajapinnan versio (avain on `Api-Version` ja arvo `1.0`)</span><span class="sxs-lookup"><span data-stu-id="f7cf0-265">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="f7cf0-266">**Tekstisisältö** - sisällytä edellisessä vaiheessa luotu JSON-pyyntö.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-266">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="f7cf0-267">`access_token` saadaan vastauksessa.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-267">You will get an `access_token` in response.</span></span> <span data-ttu-id="f7cf0-268">Sitä tarvitaan haltijatunnuksena, jolla varastoin näkyvyyden ohjelmointirajapintaa kutsutaan.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-268">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="f7cf0-269">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-269">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="f7cf0-270">Varaston näkyvyyden ohjelmointirajapinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f7cf0-270">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="f7cf0-271">Ennen palvelun käyttöä on tehtävä valmiiksi seuraavissa aliosissa käsiteltävät määritykset.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-271">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="f7cf0-272">Määritykset voivat vaihdella ympäristön tietojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-272">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="f7cf0-273">Siinä pääasiallisesti neljä osaa:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-273">It primarily includes four parts:</span></span>

- [<span data-ttu-id="f7cf0-274">Osiointi</span><span class="sxs-lookup"><span data-stu-id="f7cf0-274">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="f7cf0-275">Dimensiomääritykset</span><span class="sxs-lookup"><span data-stu-id="f7cf0-275">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="f7cf0-276">Indeksointi</span><span class="sxs-lookup"><span data-stu-id="f7cf0-276">Indexing</span></span>](#indexing)
- [<span data-ttu-id="f7cf0-277">Mukautettu mitta</span><span class="sxs-lookup"><span data-stu-id="f7cf0-277">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="f7cf0-278">Osiointi</span><span class="sxs-lookup"><span data-stu-id="f7cf0-278">Partitioning</span></span>

<span data-ttu-id="f7cf0-279">Osiointi voi vaikuttaa merkittävästi varaston näkyvyyden ohjelmointirajapinnan toimintaan.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-279">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="f7cf0-280">Niinpä kannattaakin määrittää rakenne, jossa voidaan ryhmitellä tietoja pienissä osissa siten, että merkitykselliset tietokyselyt ovat mahdollisia.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-280">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="f7cf0-281">`organizationId` (Supply Chain Managementissa `dataAreaId`) sisältyy aina osiointiin, ja varaston näkyvyys osioidaan oletusarvoisesti dimensioiden perusteella, kuten *Toimipaikka + sijainti*.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-281">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="f7cf0-282">Tämän vuoksi palveluissa tehtävissä kyselyissä on aina käytettävä suodattimissa määritettyjä dimensioita.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-282">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="f7cf0-283">*Toimipaikka* ja *sijainti* ovat kaksi varaston näkyvyyden yleistä oletusdimensiota.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-283">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="f7cf0-284">Supply Chain Managementin näiden dimensioiden nimet ovat *toimipaikka* (`InventSiteId`) ja *varasto* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="f7cf0-284">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="f7cf0-285">Dimensiomääritykset</span><span class="sxs-lookup"><span data-stu-id="f7cf0-285">Dimension configurations</span></span>

<span data-ttu-id="f7cf0-286">Varaston näkyvyyden yleisten oletusdimensioiden luettelon ansiosta usein lähdejärjestelmien integrointi on mahdollista.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-286">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="f7cf0-287">Seuraavassa taulukossa on varastodimensiot, jotka tulevat varaston näkyvyyden oletusdimensionimiksi.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-287">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="f7cf0-288">Dimensiotyyppi</span><span class="sxs-lookup"><span data-stu-id="f7cf0-288">Dimension type</span></span> | <span data-ttu-id="f7cf0-289">Dimension nimi</span><span class="sxs-lookup"><span data-stu-id="f7cf0-289">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="f7cf0-290">Tuote</span><span class="sxs-lookup"><span data-stu-id="f7cf0-290">Product</span></span> | `ColorId` |
| <span data-ttu-id="f7cf0-291">Tuote</span><span class="sxs-lookup"><span data-stu-id="f7cf0-291">Product</span></span> | `SizeId` |
| <span data-ttu-id="f7cf0-292">Tuote</span><span class="sxs-lookup"><span data-stu-id="f7cf0-292">Product</span></span> | `StyleId` |
| <span data-ttu-id="f7cf0-293">Tuote</span><span class="sxs-lookup"><span data-stu-id="f7cf0-293">Product</span></span> | `ConfigId` |
| <span data-ttu-id="f7cf0-294">Seuranta</span><span class="sxs-lookup"><span data-stu-id="f7cf0-294">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="f7cf0-295">Seuranta</span><span class="sxs-lookup"><span data-stu-id="f7cf0-295">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="f7cf0-296">Toimipaikka</span><span class="sxs-lookup"><span data-stu-id="f7cf0-296">Location</span></span> | `LocationId` |
| <span data-ttu-id="f7cf0-297">Toimipaikka</span><span class="sxs-lookup"><span data-stu-id="f7cf0-297">Location</span></span> | `SiteId` |
| <span data-ttu-id="f7cf0-298">Varaston tila</span><span class="sxs-lookup"><span data-stu-id="f7cf0-298">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="f7cf0-299">Varastokohtainen</span><span class="sxs-lookup"><span data-stu-id="f7cf0-299">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="f7cf0-300">Varastokohtainen</span><span class="sxs-lookup"><span data-stu-id="f7cf0-300">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="f7cf0-301">Varastokohtainen</span><span class="sxs-lookup"><span data-stu-id="f7cf0-301">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="f7cf0-302">Edellisessä taulukossa mainittu dimensiotyyppi on tarkoitettu vain tiedoksi.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-302">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="f7cf0-303">Dimensiotyyppiä ei tarvitse määrittää varaston näkyvyydessä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-303">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="f7cf0-304">Jos mukautettu dimensio on luotu ja sen on siirryttävä oletusarvoon, kun varaston näkyvyys käyttää sitä, **mukautetun dimension** nimi voidaan määrittää varaston näkyvyydessä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-304">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="f7cf0-305">Ulkoiset järjestelmät käyttävät varaston näkyvyyttä RESTful API -ohjelmointirajapinnoilla, jotka ottavat käytettävissä olevat tiedot käyttöön annetuissa dimensiojoukoissa, joissa kyselyt tehdään.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-305">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="f7cf0-306">Integroinnin osalta varaston näkyvyydessä voidaan määrittää *ulkoinen kanavan tietolähde* ja *kohdedimensioiden* lähdedimensio varaston näkyvyydessä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-306">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="f7cf0-307">Kohdedimensioiden on oltava jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-307">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="f7cf0-308">Varaston näkyvyyden oletusdimensiot</span><span class="sxs-lookup"><span data-stu-id="f7cf0-308">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="f7cf0-309">Mukautetut dimensiot</span><span class="sxs-lookup"><span data-stu-id="f7cf0-309">Custom dimensions</span></span>

<span data-ttu-id="f7cf0-310">Dimensiomääritysten tarkoitus on standardoida monen järjestelmän integrointi dimensiokyselyitä ja tapahtuman dimensioihin kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-310">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="f7cf0-311">Indeksointi</span><span class="sxs-lookup"><span data-stu-id="f7cf0-311">Indexing</span></span>

<span data-ttu-id="f7cf0-312">Käytettävissä olevan varaston kysely ei ole useimmiten korkeimmalla kokonaistasolla, vaan tulokset halutaan ehkä nähdä varastodimensioiden mukaan koostettuina.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-312">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="f7cf0-313">Varaston näkyvyys on joustava, sillä siinä voidaan määrittää dimensioon tai dimensioyhdistelmiin perustuvia indeksejä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-313">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="f7cf0-314">Tällä hetkellä indeksejä voi määrittään enintään viisi.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-314">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="f7cf0-315">Käytettävää dimensiota tai dimensioyhdistelmää on harkittava huolellisesti ennen toteutusta, sillä näin voidaan varmistaa, että se todella vastaa liiketoiminnan tarpeita.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-315">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="f7cf0-316">Tuotekysely voidaan haluta tehdä esimerkiksi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-316">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="f7cf0-317">Kyselynä käytettävissä oleva koostetuote *väri*- ja *koko*-dimension mukaan.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-317">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="f7cf0-318">Joissakin tapauksissa kyselyn kohteena voi olla tuote kokonaisuudessaan.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-318">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="f7cf0-319">Kaksi indeksiä määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-319">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="f7cf0-320">Tyhjä hakasulje tekee koosteen osiossa olevan tuotetunnuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-320">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="f7cf0-321">Indeksointi määrittää, miten tulokset ryhmitellään `groupBy`-kyselyasetuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-321">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="f7cf0-322">Jos tässä tapauksessa ei määritetä `groupBy`-arvoja, tuloksena on `productid`-kohtainen kokonaismäärä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-322">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="f7cf0-323">Jos `groupBy`-määrityksenä on sen sijaan `groupBy=ColorId&groupBy=SizeId`, tuloksena on useita rivejä, jotka perustuvat järjestelmässä oleviin väri- ja kokoyhdistelmiin.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-323">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="f7cf0-324">Kyselyehdot voidaan asettaa pyynnön tekstiosaan.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-324">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="f7cf0-325">Seuraavassa esimerkissä on väri- ja kokoyhdistelmää käyttävä tuotekysely.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-325">Here is a sample query on the product with color and size combination.</span></span>

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

#### <a name="custom-measurement"></a><span data-ttu-id="f7cf0-326">Mukautettu mitta</span><span class="sxs-lookup"><span data-stu-id="f7cf0-326">Custom measurement</span></span>

<span data-ttu-id="f7cf0-327">Oletusmittamäärät linkitetään Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-327">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="f7cf0-328">Haluat ehkä kuitenkin määrän, joka koostuu oletusmitoista.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-328">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="f7cf0-329">Sitä varten on määritettävä mukautettuja määritä, jotka lisätään käytettävissä olevan määrän tulosteisiin.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-329">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="f7cf0-330">Toiminnon antaa yksinkertaisesti mahdollisuuden määrittää lisättävän ja/tai vähennettävän mittajoukon, joiden avulla voidaan muodostaa mukautettu mitta.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-330">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="f7cf0-331">Esimerkiksi seuraavalla kyselyehdolla määritetään mukautetun mitan määräksi `MyCustomAvailableforReservation`, jonka kulutusjärjestelmä käyttää.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-331">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="f7cf0-332">Kulutusjärjestelmä</span><span class="sxs-lookup"><span data-stu-id="f7cf0-332">Consumption system</span></span> | <span data-ttu-id="f7cf0-333">Lasketut mitat</span><span class="sxs-lookup"><span data-stu-id="f7cf0-333">Calculated measurers</span></span> | <span data-ttu-id="f7cf0-334">Tietolähde</span><span class="sxs-lookup"><span data-stu-id="f7cf0-334">Data source</span></span> | <span data-ttu-id="f7cf0-335">Määre</span><span class="sxs-lookup"><span data-stu-id="f7cf0-335">Modifier</span></span> | <span data-ttu-id="f7cf0-336">Määreen laskentatyyppi</span><span class="sxs-lookup"><span data-stu-id="f7cf0-336">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="f7cf0-337">Lisäys</span><span class="sxs-lookup"><span data-stu-id="f7cf0-337">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="f7cf0-338">Lisäys</span><span class="sxs-lookup"><span data-stu-id="f7cf0-338">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="f7cf0-339">Vähennyslasku</span><span class="sxs-lookup"><span data-stu-id="f7cf0-339">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="f7cf0-340">Lisäys</span><span class="sxs-lookup"><span data-stu-id="f7cf0-340">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="f7cf0-341">Vähennyslasku</span><span class="sxs-lookup"><span data-stu-id="f7cf0-341">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="f7cf0-342">Lisäys</span><span class="sxs-lookup"><span data-stu-id="f7cf0-342">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="f7cf0-343">Lisäys</span><span class="sxs-lookup"><span data-stu-id="f7cf0-343">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="f7cf0-344">Vähennyslasku</span><span class="sxs-lookup"><span data-stu-id="f7cf0-344">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="f7cf0-345">Vähennyslasku</span><span class="sxs-lookup"><span data-stu-id="f7cf0-345">Subtraction</span></span> |

<span data-ttu-id="f7cf0-346">Mukautetun mittamäärän kysely palauttaa sitten seuraavan tuloksen.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-346">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="f7cf0-347">`MyCustomAvailableforReservation`-tulos perustuu seuraavaan mukautettujen mittojen laskenta-asetukseen:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-347">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="f7cf0-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="f7cf0-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="f7cf0-349">Varastosaldon muutosten kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="f7cf0-349">Posting on-hand changes</span></span>

<span data-ttu-id="f7cf0-350">Tarkka URL-osoite, johon tapahtuma kirjataan, määräytyy maantieteellisen alueen mukaan.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-350">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="f7cf0-351">Sen muoto on seuraava:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-351">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="f7cf0-352">Tätä URL-osoitetta käytetään todennuksessa HTTP `POST` -menetelmän ohella lähettämään varastosaldon muutostapahtumat palveluun.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-352">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="f7cf0-353">Dynamics 365 -palvelun kanssa HTTP-pyyntöjen avulla tapahtuvassa viestinnässä käytetään erityisotsikko, joka ilmaisee sen Supply Chain Management -esiintymän ympäristötunnuksen, johon tiedot on linkitetty.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-353">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="f7cf0-354">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-354">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="f7cf0-355">Varastosaldon muutosten kirjaamisen kyselyesimerkki 1</span><span class="sxs-lookup"><span data-stu-id="f7cf0-355">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="f7cf0-356">Tässä esimerkissä on skenaario, jossa dimensiomääritys määritetään Power Appsissa.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-356">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="f7cf0-357">Määritä dimension yhdistämismääritys Power Appsissa käyttämällä seuraavaa kyselyä:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-357">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="f7cf0-358">Voit nyt tehdä `dimensionDataSource`-määrityksen ja käyttää mukautettuja dimensioita kyselyissä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-358">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="f7cf0-359">Järjestelmä muuntaa mukautetut dimensiot automaattisesti perusdimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-359">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="f7cf0-360">Varastosaldon muutosten kirjaamisen kyselyesimerkki 2</span><span class="sxs-lookup"><span data-stu-id="f7cf0-360">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="f7cf0-361">Tässä esimerkissä on skenaario, jossa yhtään dimensiomäärityksen yhdistämismääritystä ei määritetä Power Appsissa, joten myös kirjaamisessa on käytettävä perusdimensioita.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-361">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="f7cf0-362">Kaikkien dimensioiden on oltava perusdimensioita, kun `dimensionDataSource`-kentässä on tyhjäarvo, se on tyhjä tai siinä on välilyönti.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-362">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="f7cf0-363">JSON-tiedostokentän ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="f7cf0-363">JSON document field properties</span></span>

<span data-ttu-id="f7cf0-364">Aiemmin käsitellyissä JSON-kyselyesimerkkien kentissä oli seuraavassa taulukossa olevia ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-364">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="f7cf0-365">Kentän tunnus</span><span class="sxs-lookup"><span data-stu-id="f7cf0-365">Field ID</span></span> | <span data-ttu-id="f7cf0-366">kuvaus</span><span class="sxs-lookup"><span data-stu-id="f7cf0-366">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="f7cf0-367">Tietyn muutostapahtuman yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-367">A unique ID for the specific change event.</span></span> <span data-ttu-id="f7cf0-368">Tämän tunnuksen avulla varmistetaan, että jos viestintä palveluun epäonnistuu kirjauksen aikana, tapahtuman lähettäminen uudelleen ei aiheuta saman tapahtuman laskemista kahdesti järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-368">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="f7cf0-369">Tapahtumaan linkitetyn organisaation tunnus.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-369">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="f7cf0-370">Tämä yhdistetään Supply Chain Management -organisaatioihin tai tietoalueen tunnuksiin.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-370">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="f7cf0-371">Kyseisen tuotteen tunniste.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-371">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="f7cf0-372">Määrä, jolla varastosaldoa on muutettava.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-372">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="f7cf0-373">Jos hyllylle esimerkiksi lisättiin 10 uutta sämpylää, tämä arvo 10.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-373">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="f7cf0-374">Jos 3 sämpylää sitten poistettiin hyllystä tai myyntiin, tämä arvo on -3.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-374">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="f7cf0-375">Muutostapahtuman kirjauksessa ja kyselyssä käytettävien dimensioiden tietolähde.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-375">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="f7cf0-376">Jos tietolähde määritetään, määritetyn tietolähteen mukautettuja dimensioita voidaan käyttää.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-376">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="f7cf0-377">Dimensiomääritysten ansiosta varaston näkyvyys voi yhdistää mukautetut dimensiot yleisiin oletusdimensioihin.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-377">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="f7cf0-378">Jos `dimensionDataSource` ei ole määritetty, kyselyissä voi käyttää vain yleisiä oletusdimensioita.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-378">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="f7cf0-379">Dynaaminen avain- ja arvoparisäilö.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-379">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="f7cf0-380">Ne yhdistetään joihinkin Supply Chain Managementin dimensioihin, minkä lisäksi voidaan lisätä mukautettuja dimensioita (kuten *Lähde*), jotka voivat ilmaista, saapuuko tapahtuma Supply Chain Managementista vai ulkoisesta järjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-380">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="f7cf0-381">Kyselyt nykyisessä varastosaldossa</span><span class="sxs-lookup"><span data-stu-id="f7cf0-381">Querying current on-hand</span></span>

<span data-ttu-id="f7cf0-382">Nykyisen varastosaldon kyselyjen päätepisteessä on samankaltainen URL-osoite:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-382">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="f7cf0-383">Kysely siinä tehdään HTTP `POST` -menetelmällä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-383">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="f7cf0-384">Nykyisen varastosaldon kyselyesimerkki 1</span><span class="sxs-lookup"><span data-stu-id="f7cf0-384">Current on-hand query example 1</span></span>

<span data-ttu-id="f7cf0-385">Tässä esimerkissä on skenaario, jossa Power Appsissa on jo valmis dimensiomääritys.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-385">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="f7cf0-386">Määritä dimension yhdistämismääritys Power Appsissa käyttämällä seuraavaa kyselyä:</span><span class="sxs-lookup"><span data-stu-id="f7cf0-386">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="f7cf0-387">Voit nyt tehdä `dimensionDataSource`-määrityksen ja käyttää mukautettuja dimensioita kyselyissä.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-387">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="f7cf0-388">Järjestelmä muuntaa mukautetut dimensiot automaattisesti perusdimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-388">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="f7cf0-389">`DimensionDataSource` voidaan määrittää `filters`-kohdassa ja mukautetut dimensiot vodaan määrittää sekä `filters`- että `groupByValues`-kohdissa.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-389">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="f7cf0-390">Järjestelmä muuntaa mukautetut dimensiot automaattisesti perusdimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-390">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="f7cf0-391">Nykyisen varastosaldon kyselyesimerkki 2</span><span class="sxs-lookup"><span data-stu-id="f7cf0-391">Current on-hand query example 2</span></span>

<span data-ttu-id="f7cf0-392">Tässä esimerkissä on skenaario, jossa yhtään dimensiomäärityksen yhdistämismääritystä ei määritetä Power Appsissa, joten myös kirjaamisessa on käytettävä perusdimensioita.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-392">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="f7cf0-393">Kaikkien dimensioiden on oltava perusdimensioita, kun `filters`-kohdan `dimensionDataSource`-kentässä on tyhjäarvo, se on tyhjä tai siinä on välilyönti.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-393">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="f7cf0-394">Palautetun tuloksen esimerkki</span><span class="sxs-lookup"><span data-stu-id="f7cf0-394">Example return result</span></span>

<span data-ttu-id="f7cf0-395">Edellisten esimerkkien kyselyissä voitiin palauttaa seuraavankaltainen tulos.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-395">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="f7cf0-396">Huomaa, että määräkentät on jäsennelty mittahakemistoksi ja niihin liittyviksi arvoiksi.</span><span class="sxs-lookup"><span data-stu-id="f7cf0-396">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
