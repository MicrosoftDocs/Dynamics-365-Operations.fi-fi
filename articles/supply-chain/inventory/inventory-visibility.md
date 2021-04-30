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
ms.openlocfilehash: d09c7be5de75511b10d7a69d4b8ac12917b0dbe8
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910422"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="1a984-103">Varaston näkyvyyden apuohjelma</span><span class="sxs-lookup"><span data-stu-id="1a984-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="1a984-104">Varaston näkyvyyden apuohjelma on itsenäinen ja erittäin skaalautuva mikropalvelu, joka mahdollistaa reaaliaikaisen käytettävissä olevan varaston seurannan ja antaa tällä tavoin yleisen näkymän varaston näkyvyyteen.</span><span class="sxs-lookup"><span data-stu-id="1a984-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="1a984-105">Kaikki käytettävissä olevaan varastoon liittyvät tiedot viedään palveluun lähes reaaliaikaisesti käyttämällä matala-asteista SQL-integraatiota.</span><span class="sxs-lookup"><span data-stu-id="1a984-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="1a984-106">Ulkoiset palvelut käyttävät palvelut tekevät RESTful API -ohjelmointirajapinnoilla käytettävissä olevien tietojen kyselyjä annetuissa dimensioissa ja saavat tällä tavoin luettelon käytettävissä olevista paikoista.</span><span class="sxs-lookup"><span data-stu-id="1a984-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="1a984-107">Varaston näkyvyys on Microsoft Dataverseen perustuva mikropalvelu, joten sitä voi laajentaa muodostamalla Power Apps -sovelluksia ja käyttämällä Power BI:ta tuottamaan liiketoiminnan tarpeita vastaavia mukautettuja toimintoja.</span><span class="sxs-lookup"><span data-stu-id="1a984-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="1a984-108">Indeksi voidaan lisäksi päivittää tekemään varastokyselyjä.</span><span class="sxs-lookup"><span data-stu-id="1a984-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="1a984-109">Varaston näkyvyydessä on määritysvaihtoehtoja, joiden avulla sen voi integroida useiden kolmannen osapuolen järjestelmien kanssa.</span><span class="sxs-lookup"><span data-stu-id="1a984-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="1a984-110">Se tukee standardoitua varastodimensiota, mukautettua laajennettavuutta ja standardoituja, määritettäviä laskettuja määriä.</span><span class="sxs-lookup"><span data-stu-id="1a984-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="1a984-111">Tässä aiheessa käsitellään Dynamics 365 Supply Chain Managementin varaston näkyvyyden apuohjelman asentamista ja määrittämistä sekä sen ohjelmointirajapinnan käyttöä.</span><span class="sxs-lookup"><span data-stu-id="1a984-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="1a984-112">Varaston näkyvyyden lisäapuohjelman asentaminen</span><span class="sxs-lookup"><span data-stu-id="1a984-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="1a984-113">Varaston näkyvyyden lisäapuohjelman asentamiseen on käytettävä Microsoft Dynamics Lifecycle Servicesiä (LCS).</span><span class="sxs-lookup"><span data-stu-id="1a984-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="1a984-114">LCS on yhteistyöportaali, jonka muodostamassa ympäristössä ja jonka säännöllisesti päivitetyillä palveluilla voi hallita Dynamics 365 Finance and Operations -sovellusten elinkaarta.</span><span class="sxs-lookup"><span data-stu-id="1a984-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="1a984-115">Lisätietoja on kohdassa [Lifecycle Services -resurssit](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span><span class="sxs-lookup"><span data-stu-id="1a984-115">For more information, see [Lifecycle Services resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="1a984-116">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="1a984-116">Prerequisites</span></span>

<span data-ttu-id="1a984-117">Ennen varaston näkyvyyden apuohjelman asentamista:</span><span class="sxs-lookup"><span data-stu-id="1a984-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="1a984-118">Hanki LCS-toteutusprojekti, jossa on otettu käyttöön vähintään yksi ympäristö.</span><span class="sxs-lookup"><span data-stu-id="1a984-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="1a984-119">Varmista, että kohdassa [Lisäosien yleiskatsaus](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) annetut edellytykset lisäosien määrittämiselle on täytetty.</span><span class="sxs-lookup"><span data-stu-id="1a984-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="1a984-120">Varaston näkyvyys ei edellytä kaksoiskirjoituslinkitystä.</span><span class="sxs-lookup"><span data-stu-id="1a984-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="1a984-121">Ota yhteyttä varaston näkyvyyden tiimiin [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), jotta saat seuraavat kolme vaadittua tiedostoa:</span><span class="sxs-lookup"><span data-stu-id="1a984-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>
    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="1a984-122">`Inventory Visibility Integration.zip` (jos käynnissä ollut Supply Chain Managementin versio on aiempi kuin 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="1a984-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>
- <span data-ttu-id="1a984-123">Noudata seuraavassa annettuja ohjeita: [Pikaopas: Rekisteröi hakemus Microsoft identity Platformiin](/azure/active-directory/develop/quickstart-register-app) sovelluksen rekisteröimiseksi ja asiakkaan lisäämiseksi AAD:lle ylläpitosopimuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="1a984-123">Follow the instructions given in [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register an application and add a client secret to AAD under your azure subscription.</span></span>
    - [<span data-ttu-id="1a984-124">Sovelluksen rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="1a984-124">Register an application</span></span>](/azure/active-directory/develop/quickstart-register-app)
    - [<span data-ttu-id="1a984-125">Lisää asiakasohjelman salasana</span><span class="sxs-lookup"><span data-stu-id="1a984-125">Add a client secret</span></span>](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
    - <span data-ttu-id="1a984-126">**Sovelluksen (asiakas) tunnuksen**, **asiakasohjelman salasanan** ja **vuokraajan tunnuksen** avulla voidaan tehdä seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="1a984-126">The **Application(Client) Id**, **Client Secret** and **Tenant ID** will be used in the following steps.</span></span>

> [!NOTE]
> <span data-ttu-id="1a984-127">Tällä hetkellä tuettuja maita ja alueita ovat Kanada, Yhdysvallat ja Euroopan unioni (EU).</span><span class="sxs-lookup"><span data-stu-id="1a984-127">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="1a984-128">Jos sinulla on näitä edellytyksiä koskevia kysymyksiä, ota yhteys varaston näkyvyyden tuotetiimiin.</span><span class="sxs-lookup"><span data-stu-id="1a984-128">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="1a984-129">Määritys Dataverse</span><span class="sxs-lookup"><span data-stu-id="1a984-129">Set up Dataverse</span></span>

<span data-ttu-id="1a984-130">Määritä Dataverse noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="1a984-130">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="1a984-131">Lisää palveluperiaate vuokraajaan:</span><span class="sxs-lookup"><span data-stu-id="1a984-131">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="1a984-132">Asenna Azure AD PowerShell Module v2, kuten kuvattu kohdassa [Asenna Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="1a984-132">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="1a984-133">Suorita seuraava PowerShell-komento.</span><span class="sxs-lookup"><span data-stu-id="1a984-133">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="1a984-134">Luo sovelluskäyttäjä varaston näkyvyydelle Dataversessä:</span><span class="sxs-lookup"><span data-stu-id="1a984-134">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="1a984-135">Avaa Dataverse-ympäristön URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="1a984-135">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="1a984-136">Valitse **Lisäasetukset \> Järjestelmä \> Suojaus \> Käyttäjät** ja luo sovelluskäyttäjä.</span><span class="sxs-lookup"><span data-stu-id="1a984-136">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="1a984-137">Vaihda sivunäkymäksi **Sovelluskäyttäjät** näkymävalikossa.</span><span class="sxs-lookup"><span data-stu-id="1a984-137">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="1a984-138">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="1a984-138">Select **New**.</span></span> <span data-ttu-id="1a984-139">Aseta sovellustunnukseksi *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="1a984-139">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="1a984-140">(Objektin tunnus ladataan automaattisesti, kun tallennat muutokset.) Voit mukauttaa nimeä.</span><span class="sxs-lookup"><span data-stu-id="1a984-140">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="1a984-141">Voit muuttaa sen esimerkiksi nimeksi *Varaston näkyvyys*.</span><span class="sxs-lookup"><span data-stu-id="1a984-141">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="1a984-142">Kun olet valmis, valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="1a984-142">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="1a984-143">Valitse **Määritä rooli** ja valitse sitten **Järjestelmänvalvoja**.</span><span class="sxs-lookup"><span data-stu-id="1a984-143">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="1a984-144">Jos saatavana on rooli nimeltä **Common Data Service -käyttäjä**, valitse myös se.</span><span class="sxs-lookup"><span data-stu-id="1a984-144">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="1a984-145">Lisätietoja on kohdassa [Sovelluskäyttäjän luominen](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="1a984-145">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="1a984-146">Jos oletuskieli ei Dataversessäsi ole **englanti**:</span><span class="sxs-lookup"><span data-stu-id="1a984-146">If the default language of your Dataverse is not **English**:</span></span>

    1. <span data-ttu-id="1a984-147">Siirry kohtaan **Lisäasetukset \> Hallinta \> Kielet**,</span><span class="sxs-lookup"><span data-stu-id="1a984-147">Go to **Advanced Setting \> Administration \> Languages**,</span></span>
    1. <span data-ttu-id="1a984-148">Valitse **englanti (LanguageCode=1033)** ja valitse **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="1a984-148">Select **English (LanguageCode=1033)** and select **Apply**.</span></span>

1. <span data-ttu-id="1a984-149">Tuo `Inventory Visibility Dataverse Solution.zip` -tiedosto, joka sisältää Dataverse-konfiguraatioon liittyvät entiteetit ja Power Apps -sovellukset:</span><span class="sxs-lookup"><span data-stu-id="1a984-149">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="1a984-150">Siirry **Ratkaisut**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="1a984-150">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="1a984-151">Valitse **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="1a984-151">Select **Import**.</span></span>

1. <span data-ttu-id="1a984-152">Tuo konfiguraation päivityksen käynnistimen työnkulku:</span><span class="sxs-lookup"><span data-stu-id="1a984-152">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="1a984-153">Siirry Microsoft Flow -sivulle.</span><span class="sxs-lookup"><span data-stu-id="1a984-153">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="1a984-154">Varmista, että yhteys nimeltä *Dataverse (vanha)* on olemassa.</span><span class="sxs-lookup"><span data-stu-id="1a984-154">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="1a984-155">(Jos sitä ei ole olemassa, luo se.)</span><span class="sxs-lookup"><span data-stu-id="1a984-155">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="1a984-156">Tuo `Inventory Visibility Configuration Trigger.zip` -tiedosto.</span><span class="sxs-lookup"><span data-stu-id="1a984-156">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="1a984-157">Kun käynnistys on tuotu, se näkyy **Omat työnkulut** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="1a984-157">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="1a984-158">Alusta seuraavat neljä muuttujaa ympäristön tietojen perusteella:</span><span class="sxs-lookup"><span data-stu-id="1a984-158">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="1a984-159">Azure-vuokraajan tunnus</span><span class="sxs-lookup"><span data-stu-id="1a984-159">Azure Tenant ID</span></span>
        - <span data-ttu-id="1a984-160">Azure-sovelluksen asiakastunnus</span><span class="sxs-lookup"><span data-stu-id="1a984-160">Azure Application Client ID</span></span>
        - <span data-ttu-id="1a984-161">Azure-sovelluksen asiakasohjelman salasana</span><span class="sxs-lookup"><span data-stu-id="1a984-161">Azure Application Client Secret</span></span>
        - <span data-ttu-id="1a984-162">Varaston näkyvyyden päätepiste</span><span class="sxs-lookup"><span data-stu-id="1a984-162">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="1a984-163">Lisätietoja tästä muuttujasta on jäljempänä tässä ohjeaiheessa kohdassa [Varaston näkyvyyden integraation määrittäminen](#setup-inventory-visibility-integration).</span><span class="sxs-lookup"><span data-stu-id="1a984-163">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="1a984-164">![Määrityksen käynnistin](media/configuration-trigger.png "Määrityksen käynnistin")</span><span class="sxs-lookup"><span data-stu-id="1a984-164">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="1a984-165">Valitse **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="1a984-165">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="1a984-166">Lisäosan asentaminen</span><span class="sxs-lookup"><span data-stu-id="1a984-166">Install the add-in</span></span>

<span data-ttu-id="1a984-167">Varaston näkyvyyden apuohjelman asentaminen:</span><span class="sxs-lookup"><span data-stu-id="1a984-167">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="1a984-168">Kirjaudu [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) -portaaliin.</span><span class="sxs-lookup"><span data-stu-id="1a984-168">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="1a984-169">Valitse aloitussivulla projekti, jossa ympäristö on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="1a984-169">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="1a984-170">Valitse projektisivulla ympäristö, johon haluat asentaa apuohjelman.</span><span class="sxs-lookup"><span data-stu-id="1a984-170">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="1a984-171">Siirry ympäristösivulla alaspäin, kunnes näet **Ympäristön lisäosat** -kohdan **Power Platform -integraatio** -kohdassa, josta löytyy Dataverse-ympäristön nimi.</span><span class="sxs-lookup"><span data-stu-id="1a984-171">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="1a984-172">Valitse **Ympäristöapuohjelmat**-osassa **Asenna uusi apuohjelma**.</span><span class="sxs-lookup"><span data-stu-id="1a984-172">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="1a984-173">![Ympäristösivu LCS:ssa](media/inventory-visibility-environment.png "Ympäristösivu LCS:ssa")</span><span class="sxs-lookup"><span data-stu-id="1a984-173">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="1a984-174">Valitse **Asenna uusi apuohjelma** -linkki.</span><span class="sxs-lookup"><span data-stu-id="1a984-174">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="1a984-175">Käytettävissä olevien apuohjelmien luettelo avautuu.</span><span class="sxs-lookup"><span data-stu-id="1a984-175">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="1a984-176">Valitse luettelosta **Vataston näkyvyys**.</span><span class="sxs-lookup"><span data-stu-id="1a984-176">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="1a984-177">Anna arvot seuraavissa ympäristön kentissä:</span><span class="sxs-lookup"><span data-stu-id="1a984-177">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="1a984-178">**AAD-sovelluksen (asiakasohjelman) tunnus**</span><span class="sxs-lookup"><span data-stu-id="1a984-178">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="1a984-179">**AAD-vuokraajan tunnus**</span><span class="sxs-lookup"><span data-stu-id="1a984-179">**AAD tenant ID**</span></span>

    <span data-ttu-id="1a984-180">![Apuohjelman määrityssivu](media/inventory-visibility-setup.png "Apuohjelman määrityssivu")</span><span class="sxs-lookup"><span data-stu-id="1a984-180">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="1a984-181">Hyväksy käyttöehdot valitsemalla **Käyttöehdot**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="1a984-181">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="1a984-182">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="1a984-182">Select **Install**.</span></span> <span data-ttu-id="1a984-183">Apuohjelman tilana näkyy nyt **Asennetaan**.</span><span class="sxs-lookup"><span data-stu-id="1a984-183">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="1a984-184">Se on valmis, päivitä sivu, jonka jälkeen tilana on **Asennettu**.</span><span class="sxs-lookup"><span data-stu-id="1a984-184">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="1a984-185">Lisäosan asennuksen poistaminen</span><span class="sxs-lookup"><span data-stu-id="1a984-185">Uninstall the add-in</span></span>

<span data-ttu-id="1a984-186">Poista apuohjelman asennus valitsemalla **Poista asennus**.</span><span class="sxs-lookup"><span data-stu-id="1a984-186">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="1a984-187">Kun päivität LCS:n, varaston näkyvyyden apuohjelma poistetaan.</span><span class="sxs-lookup"><span data-stu-id="1a984-187">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="1a984-188">Asennuksen poistoprosessi poistaa apuohjelman rekisteröinnin sekä käynnistää kaikkien palveluun tallennettujen liiketoimintatietojen puhdistustyön.</span><span class="sxs-lookup"><span data-stu-id="1a984-188">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="1a984-189">Käytettävissä olevan varaston tietojen käyttäminen Supply Chain Managementista</span><span class="sxs-lookup"><span data-stu-id="1a984-189">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="1a984-190">Varaston näkyvyyden integrointipaketin käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="1a984-190">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="1a984-191">Jos käytössäsi on Supply Chain Management -versio 10.0.17 tai aiempi, ota yhteyttä varaston näkyvyyden tukihenkilöstöön osoitteessa [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) saadaksesi pakettitiedoston.</span><span class="sxs-lookup"><span data-stu-id="1a984-191">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="1a984-192">Ota sitten paketti käyttöön LCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="1a984-192">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="1a984-193">Jos käyttöönoton aikana ilmenee version vastaavuusvirhe, X++-projekti on tuotava manuaalisesti kehitysympäristöön.</span><span class="sxs-lookup"><span data-stu-id="1a984-193">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="1a984-194">Luo sitten käyttöön otettava paketti kehitysympäristössä ja ota se käyttöön tuotantoympäristössä.</span><span class="sxs-lookup"><span data-stu-id="1a984-194">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="1a984-195">Koodi sisältyy Supply Chain Management -versioon 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="1a984-195">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="1a984-196">Jos käytössä on tämä versio tai myöhempi versio, käyttöönottoa ei tarvita.</span><span class="sxs-lookup"><span data-stu-id="1a984-196">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="1a984-197">Varmista, että seuraavat ominaisuudet on otettu käyttöön Supply Chain Management -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="1a984-197">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="1a984-198">(Oletusarvon mukaan ne ovat käytössä.)</span><span class="sxs-lookup"><span data-stu-id="1a984-198">(By default, they are turned on.)</span></span>

| <span data-ttu-id="1a984-199">Toiminnon kuvaus</span><span class="sxs-lookup"><span data-stu-id="1a984-199">Feature description</span></span> | <span data-ttu-id="1a984-200">Koodiversio</span><span class="sxs-lookup"><span data-stu-id="1a984-200">Code version</span></span> | <span data-ttu-id="1a984-201">Vaihda luokka</span><span class="sxs-lookup"><span data-stu-id="1a984-201">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="1a984-202">Varastodimensioiden ottaminen käyttöön InventSum-taulussa tai poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="1a984-202">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="1a984-203">10.0.11</span><span class="sxs-lookup"><span data-stu-id="1a984-203">10.0.11</span></span> | <span data-ttu-id="1a984-204">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="1a984-204">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="1a984-205">Varastodimensioiden ottaminen käyttöön InventSumDelta-taulussa tai poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="1a984-205">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="1a984-206">10.0.12</span><span class="sxs-lookup"><span data-stu-id="1a984-206">10.0.12</span></span> | <span data-ttu-id="1a984-207">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="1a984-207">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="1a984-208">Määritä Varaston näkyvyyden integrointi</span><span class="sxs-lookup"><span data-stu-id="1a984-208">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="1a984-209">Avaa Supply Chain Managementissa **[Ominaisuuden hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** -työtila ja ota käyttöön **Varaston näkyvyyden integraatio** -ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="1a984-209">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="1a984-210">Siirry kohtaan **Varastonhallinta \> Määritys \> Varaston näkyvyyden integraation parametrit** ja kirjoita sen ympäristön URL-osoite, jossa varaston näkyvyys on käytössä.</span><span class="sxs-lookup"><span data-stu-id="1a984-210">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="1a984-211">Etsi LCS-ympäristösi Azure-alue ja kirjoita sitten URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="1a984-211">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="1a984-212">URL-osoitteessa on seuraava muoto:</span><span class="sxs-lookup"><span data-stu-id="1a984-212">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="1a984-213">Esimerkiksi Euroopassa ympäristössäsi on jokin seuraavista URL-osoitteista:</span><span class="sxs-lookup"><span data-stu-id="1a984-213">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="1a984-214">Seuraavat alueet ovat käytettävissä tällä hetkellä.</span><span class="sxs-lookup"><span data-stu-id="1a984-214">The following regions are currently available.</span></span>

    | <span data-ttu-id="1a984-215">Azure-alue</span><span class="sxs-lookup"><span data-stu-id="1a984-215">Azure region</span></span> | <span data-ttu-id="1a984-216">Alueen lyhyt nimi</span><span class="sxs-lookup"><span data-stu-id="1a984-216">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="1a984-217">Itä-Australia</span><span class="sxs-lookup"><span data-stu-id="1a984-217">Australia east</span></span> | <span data-ttu-id="1a984-218">eau</span><span class="sxs-lookup"><span data-stu-id="1a984-218">eau</span></span> |
    | <span data-ttu-id="1a984-219">Kaakkois-Australia</span><span class="sxs-lookup"><span data-stu-id="1a984-219">Australia southeast</span></span> | <span data-ttu-id="1a984-220">seau</span><span class="sxs-lookup"><span data-stu-id="1a984-220">seau</span></span> |
    | <span data-ttu-id="1a984-221">Kanada, keskinen</span><span class="sxs-lookup"><span data-stu-id="1a984-221">Canada central</span></span> | <span data-ttu-id="1a984-222">cca</span><span class="sxs-lookup"><span data-stu-id="1a984-222">cca</span></span> |
    | <span data-ttu-id="1a984-223">Kanada, itäinen</span><span class="sxs-lookup"><span data-stu-id="1a984-223">Canada east</span></span> | <span data-ttu-id="1a984-224">eca</span><span class="sxs-lookup"><span data-stu-id="1a984-224">eca</span></span> |
    | <span data-ttu-id="1a984-225">Pohjois-Eurooppa</span><span class="sxs-lookup"><span data-stu-id="1a984-225">North Europe</span></span> | <span data-ttu-id="1a984-226">neu</span><span class="sxs-lookup"><span data-stu-id="1a984-226">neu</span></span> |
    | <span data-ttu-id="1a984-227">Länsi-Eurooppa</span><span class="sxs-lookup"><span data-stu-id="1a984-227">West Europe</span></span> | <span data-ttu-id="1a984-228">weu</span><span class="sxs-lookup"><span data-stu-id="1a984-228">weu</span></span> |
    | <span data-ttu-id="1a984-229">Itä-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="1a984-229">East US</span></span> | <span data-ttu-id="1a984-230">eus</span><span class="sxs-lookup"><span data-stu-id="1a984-230">eus</span></span> |
    | <span data-ttu-id="1a984-231">Länsi-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="1a984-231">West US</span></span> | <span data-ttu-id="1a984-232">wus</span><span class="sxs-lookup"><span data-stu-id="1a984-232">wus</span></span> |

1. <span data-ttu-id="1a984-233">Valitse **Varastonhallinta \> Kausittainen \> Varaston näkyvyyden integraatio** ja ota työ käyttöön.</span><span class="sxs-lookup"><span data-stu-id="1a984-233">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="1a984-234">Kaikki Supply Chain Managementin varastomuutostapahtumat kirjataan nyt varaston näkyvyyteen.</span><span class="sxs-lookup"><span data-stu-id="1a984-234">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="1a984-235">Varaston näkyvyyden apuohjelman julkinen ohjelmointirajapinta</span><span class="sxs-lookup"><span data-stu-id="1a984-235">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="1a984-236">Varaston näkyvyyden apuohjelman julkinen REST API sisältää useita nimenomaisia integroinnin päätepisteitä.</span><span class="sxs-lookup"><span data-stu-id="1a984-236">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="1a984-237">Se tukee kolmea pääasiallista vuorovaikutustyyppiä:</span><span class="sxs-lookup"><span data-stu-id="1a984-237">It supports three main interaction types:</span></span>

- <span data-ttu-id="1a984-238">Varastosaldon määrän muutosten kirjaaminen apuohjelmaan ulkoisesta järjestelmästä</span><span class="sxs-lookup"><span data-stu-id="1a984-238">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="1a984-239">Nykyisten käytettävissä olevien määrien kysely ulkoisesta järjestelmästä</span><span class="sxs-lookup"><span data-stu-id="1a984-239">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="1a984-240">Automaattinen synkronointi Supply Chain Managementin käytettävissä olevan varaston kanssa</span><span class="sxs-lookup"><span data-stu-id="1a984-240">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="1a984-241">Automaattinen synkronointi ei kuulu julkiseen ohjelmointirajapintaan.</span><span class="sxs-lookup"><span data-stu-id="1a984-241">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="1a984-242">Sen sijaan sitä käsitellään niiden ympäristöjen taustalla, joissa varaston näkyvyyden apuohjelma on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="1a984-242">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="1a984-243">Todennus</span><span class="sxs-lookup"><span data-stu-id="1a984-243">Authentication</span></span>

<span data-ttu-id="1a984-244">Ympäristön suojaustunnuksen avulla kutsutaan varaston näkyvyyden apuohjelmaa.</span><span class="sxs-lookup"><span data-stu-id="1a984-244">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="1a984-245">Siksi sinun on luotava *Azure Active Directory (Azure AD) -tunnus* Azure AD -sovelluksen avulla.</span><span class="sxs-lookup"><span data-stu-id="1a984-245">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="1a984-246">Tämän jälkeen Azure AD -tunnuksen avulla saat *käyttöoikeustunnuksen* suojauspalvelusta.</span><span class="sxs-lookup"><span data-stu-id="1a984-246">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="1a984-247">Palvelun suojaustunnus haetaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="1a984-247">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="1a984-248">Kirjaudu Azure-portaaliin ja etsi sen avulla Supply Chain Management -sovelluksen `clientId` ja `clientSecret`.</span><span class="sxs-lookup"><span data-stu-id="1a984-248">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="1a984-249">Nouda Azure Active Directory -tunnus (`aadToken`) lähettämällä HTTP-pyyntö, jossa on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="1a984-249">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="1a984-250">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="1a984-250">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="1a984-251">**Tapa** - `GET`</span><span class="sxs-lookup"><span data-stu-id="1a984-251">**Method** - `GET`</span></span>
    - <span data-ttu-id="1a984-252">**Tekstisisältö (lomaketiedot)**:</span><span class="sxs-lookup"><span data-stu-id="1a984-252">**Body content (form data)**:</span></span>

        | <span data-ttu-id="1a984-253">avain</span><span class="sxs-lookup"><span data-stu-id="1a984-253">key</span></span> | <span data-ttu-id="1a984-254">arvo</span><span class="sxs-lookup"><span data-stu-id="1a984-254">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="1a984-255">client_id</span><span class="sxs-lookup"><span data-stu-id="1a984-255">client_id</span></span> | <span data-ttu-id="1a984-256">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="1a984-256">${aadAppId}</span></span> |
        | <span data-ttu-id="1a984-257">client_secret</span><span class="sxs-lookup"><span data-stu-id="1a984-257">client_secret</span></span> | <span data-ttu-id="1a984-258">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="1a984-258">${aadAppSecret}</span></span> |
        | <span data-ttu-id="1a984-259">grant_type</span><span class="sxs-lookup"><span data-stu-id="1a984-259">grant_type</span></span> | <span data-ttu-id="1a984-260">client_credentials</span><span class="sxs-lookup"><span data-stu-id="1a984-260">client_credentials</span></span> |
        | <span data-ttu-id="1a984-261">resurssi</span><span class="sxs-lookup"><span data-stu-id="1a984-261">resource</span></span> | <span data-ttu-id="1a984-262">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="1a984-262">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="1a984-263">Vastauksena pitäisi olla `aadToken` , joka muistuttaa seuraavaa esimerkkiä.</span><span class="sxs-lookup"><span data-stu-id="1a984-263">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="1a984-264">Muodosta seuraavankaltainen JSON-pyyntö:</span><span class="sxs-lookup"><span data-stu-id="1a984-264">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="1a984-265">Jossa:</span><span class="sxs-lookup"><span data-stu-id="1a984-265">Where:</span></span>
    - <span data-ttu-id="1a984-266">`client_assertion`-arvon on oltava edellisessä vaiheessa vastaanotettu `aadToken`.</span><span class="sxs-lookup"><span data-stu-id="1a984-266">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="1a984-267">`context`-arvon on oltava ympäristötunnus, jossa apuohjelma halutaan ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="1a984-267">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="1a984-268">Kaikki muut arvot määritetään samoiksi kuin esimerkissä.</span><span class="sxs-lookup"><span data-stu-id="1a984-268">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="1a984-269">Lähetä HTTP-pyyntö, jossa on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="1a984-269">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="1a984-270">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="1a984-270">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="1a984-271">**Tapa** - `POST`</span><span class="sxs-lookup"><span data-stu-id="1a984-271">**Method** - `POST`</span></span>
    - <span data-ttu-id="1a984-272">**HTTP-otsikko** - sisällytä ohjelmointirajapinnan versio (avain on `Api-Version` ja arvo `1.0`)</span><span class="sxs-lookup"><span data-stu-id="1a984-272">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="1a984-273">**Tekstisisältö** - sisällytä edellisessä vaiheessa luotu JSON-pyyntö.</span><span class="sxs-lookup"><span data-stu-id="1a984-273">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="1a984-274">`access_token` saadaan vastauksessa.</span><span class="sxs-lookup"><span data-stu-id="1a984-274">You will get an `access_token` in response.</span></span> <span data-ttu-id="1a984-275">Sitä tarvitaan haltijatunnuksena, jolla varastoin näkyvyyden ohjelmointirajapintaa kutsutaan.</span><span class="sxs-lookup"><span data-stu-id="1a984-275">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="1a984-276">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="1a984-276">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a><span data-ttu-id="1a984-277">Mallipyyntö</span><span class="sxs-lookup"><span data-stu-id="1a984-277">Sample Request</span></span>

<span data-ttu-id="1a984-278">Tässä on esimerkki http-pyynnöstä. Voit käyttää mitä tahansa työkaluja tai koodauskieltä lähettääksesi pyynnön, esimerkiksi ``Postman``.</span><span class="sxs-lookup"><span data-stu-id="1a984-278">For your reference, here is a sample http request, you can use any tools or coding language to send this request, such as  ``Postman``.</span></span>

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

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="1a984-279">Varaston näkyvyyden ohjelmointirajapinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1a984-279">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="1a984-280">Ennen palvelun käyttöä on tehtävä valmiiksi seuraavissa aliosissa käsiteltävät määritykset.</span><span class="sxs-lookup"><span data-stu-id="1a984-280">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="1a984-281">Määritykset voivat vaihdella ympäristön tietojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="1a984-281">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="1a984-282">Siinä pääasiallisesti neljä osaa:</span><span class="sxs-lookup"><span data-stu-id="1a984-282">It primarily includes four parts:</span></span>

- [<span data-ttu-id="1a984-283">Osiointi</span><span class="sxs-lookup"><span data-stu-id="1a984-283">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="1a984-284">Dimensiomääritykset</span><span class="sxs-lookup"><span data-stu-id="1a984-284">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="1a984-285">Indeksointi</span><span class="sxs-lookup"><span data-stu-id="1a984-285">Indexing</span></span>](#indexing)
- [<span data-ttu-id="1a984-286">Mukautettu mitta</span><span class="sxs-lookup"><span data-stu-id="1a984-286">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="1a984-287">Osiointi</span><span class="sxs-lookup"><span data-stu-id="1a984-287">Partitioning</span></span>

<span data-ttu-id="1a984-288">Osiointi voi vaikuttaa merkittävästi varaston näkyvyyden ohjelmointirajapinnan toimintaan.</span><span class="sxs-lookup"><span data-stu-id="1a984-288">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="1a984-289">Niinpä kannattaakin määrittää rakenne, jossa voidaan ryhmitellä tietoja pienissä osissa siten, että merkitykselliset tietokyselyt ovat mahdollisia.</span><span class="sxs-lookup"><span data-stu-id="1a984-289">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="1a984-290">`organizationId` (Supply Chain Managementissa `dataAreaId`) sisältyy aina osiointiin, ja varaston näkyvyys osioidaan oletusarvoisesti dimensioiden perusteella, kuten *Toimipaikka + sijainti*.</span><span class="sxs-lookup"><span data-stu-id="1a984-290">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="1a984-291">Tämän vuoksi palveluissa tehtävissä kyselyissä on aina käytettävä suodattimissa määritettyjä dimensioita.</span><span class="sxs-lookup"><span data-stu-id="1a984-291">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="1a984-292">*Toimipaikka* ja *sijainti* ovat kaksi varaston näkyvyyden yleistä oletusdimensiota.</span><span class="sxs-lookup"><span data-stu-id="1a984-292">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="1a984-293">Supply Chain Managementin näiden dimensioiden nimet ovat *toimipaikka* (`InventSiteId`) ja *varasto* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="1a984-293">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="1a984-294">Dimensiomääritykset</span><span class="sxs-lookup"><span data-stu-id="1a984-294">Dimension configurations</span></span>

<span data-ttu-id="1a984-295">Varaston näkyvyyden yleisten oletusdimensioiden luettelon ansiosta usein lähdejärjestelmien integrointi on mahdollista.</span><span class="sxs-lookup"><span data-stu-id="1a984-295">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="1a984-296">Seuraavassa taulukossa on varastodimensiot, jotka tulevat varaston näkyvyyden oletusdimensionimiksi.</span><span class="sxs-lookup"><span data-stu-id="1a984-296">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="1a984-297">Dimensiotyyppi</span><span class="sxs-lookup"><span data-stu-id="1a984-297">Dimension type</span></span> | <span data-ttu-id="1a984-298">Dimension nimi</span><span class="sxs-lookup"><span data-stu-id="1a984-298">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="1a984-299">Tuote</span><span class="sxs-lookup"><span data-stu-id="1a984-299">Product</span></span> | `ColorId` |
| <span data-ttu-id="1a984-300">Tuote</span><span class="sxs-lookup"><span data-stu-id="1a984-300">Product</span></span> | `SizeId` |
| <span data-ttu-id="1a984-301">Tuote</span><span class="sxs-lookup"><span data-stu-id="1a984-301">Product</span></span> | `StyleId` |
| <span data-ttu-id="1a984-302">Tuote</span><span class="sxs-lookup"><span data-stu-id="1a984-302">Product</span></span> | `ConfigId` |
| <span data-ttu-id="1a984-303">Seuranta</span><span class="sxs-lookup"><span data-stu-id="1a984-303">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="1a984-304">Seuranta</span><span class="sxs-lookup"><span data-stu-id="1a984-304">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="1a984-305">Toimipaikka</span><span class="sxs-lookup"><span data-stu-id="1a984-305">Location</span></span> | `LocationId` |
| <span data-ttu-id="1a984-306">Toimipaikka</span><span class="sxs-lookup"><span data-stu-id="1a984-306">Location</span></span> | `SiteId` |
| <span data-ttu-id="1a984-307">Varaston tila</span><span class="sxs-lookup"><span data-stu-id="1a984-307">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="1a984-308">Varastokohtainen</span><span class="sxs-lookup"><span data-stu-id="1a984-308">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="1a984-309">Varastokohtainen</span><span class="sxs-lookup"><span data-stu-id="1a984-309">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="1a984-310">Varastokohtainen</span><span class="sxs-lookup"><span data-stu-id="1a984-310">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="1a984-311">Edellisessä taulukossa mainittu dimensiotyyppi on tarkoitettu vain tiedoksi.</span><span class="sxs-lookup"><span data-stu-id="1a984-311">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="1a984-312">Dimensiotyyppiä ei tarvitse määrittää varaston näkyvyydessä.</span><span class="sxs-lookup"><span data-stu-id="1a984-312">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="1a984-313">Jos mukautettu dimensio on luotu ja sen on siirryttävä oletusarvoon, kun varaston näkyvyys käyttää sitä, **mukautetun dimension** nimi voidaan määrittää varaston näkyvyydessä.</span><span class="sxs-lookup"><span data-stu-id="1a984-313">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="1a984-314">Ulkoiset järjestelmät käyttävät varaston näkyvyyttä RESTful API -ohjelmointirajapinnoilla, jotka ottavat käytettävissä olevat tiedot käyttöön annetuissa dimensiojoukoissa, joissa kyselyt tehdään.</span><span class="sxs-lookup"><span data-stu-id="1a984-314">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="1a984-315">Integroinnin osalta varaston näkyvyydessä voidaan määrittää *ulkoinen kanavan tietolähde* ja *kohdedimensioiden* lähdedimensio varaston näkyvyydessä.</span><span class="sxs-lookup"><span data-stu-id="1a984-315">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="1a984-316">Kohdedimensioiden on oltava jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="1a984-316">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="1a984-317">Varaston näkyvyyden oletusdimensiot</span><span class="sxs-lookup"><span data-stu-id="1a984-317">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="1a984-318">Mukautetut dimensiot</span><span class="sxs-lookup"><span data-stu-id="1a984-318">Custom dimensions</span></span>

<span data-ttu-id="1a984-319">Dimensiomääritysten tarkoitus on standardoida monen järjestelmän integrointi dimensiokyselyitä ja tapahtuman dimensioihin kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="1a984-319">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="1a984-320">Indeksointi</span><span class="sxs-lookup"><span data-stu-id="1a984-320">Indexing</span></span>

<span data-ttu-id="1a984-321">Käytettävissä olevan varaston kysely ei ole useimmiten korkeimmalla kokonaistasolla, vaan tulokset halutaan ehkä nähdä varastodimensioiden mukaan koostettuina.</span><span class="sxs-lookup"><span data-stu-id="1a984-321">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="1a984-322">Varaston näkyvyys on joustava, sillä siinä voidaan määrittää dimensioon tai dimensioyhdistelmiin perustuvia indeksejä.</span><span class="sxs-lookup"><span data-stu-id="1a984-322">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="1a984-323">Tällä hetkellä indeksejä voi määrittään enintään viisi.</span><span class="sxs-lookup"><span data-stu-id="1a984-323">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="1a984-324">Käytettävää dimensiota tai dimensioyhdistelmää on harkittava huolellisesti ennen toteutusta, sillä näin voidaan varmistaa, että se todella vastaa liiketoiminnan tarpeita.</span><span class="sxs-lookup"><span data-stu-id="1a984-324">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="1a984-325">Tuotekysely voidaan haluta tehdä esimerkiksi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="1a984-325">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="1a984-326">Kyselynä käytettävissä oleva koostetuote *väri*- ja *koko*-dimension mukaan.</span><span class="sxs-lookup"><span data-stu-id="1a984-326">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="1a984-327">Joissakin tapauksissa kyselyn kohteena voi olla tuote kokonaisuudessaan.</span><span class="sxs-lookup"><span data-stu-id="1a984-327">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="1a984-328">Kaksi indeksiä määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="1a984-328">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="1a984-329">Tyhjä hakasulje tekee koosteen osiossa olevan tuotetunnuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="1a984-329">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="1a984-330">Indeksointi määrittää, miten tulokset ryhmitellään `groupBy`-kyselyasetuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="1a984-330">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="1a984-331">Jos tässä tapauksessa ei määritetä `groupBy`-arvoja, tuloksena on `productid`-kohtainen kokonaismäärä.</span><span class="sxs-lookup"><span data-stu-id="1a984-331">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="1a984-332">Jos `groupBy`-määrityksenä on sen sijaan `groupBy=ColorId&groupBy=SizeId`, tuloksena on useita rivejä, jotka perustuvat järjestelmässä oleviin väri- ja kokoyhdistelmiin.</span><span class="sxs-lookup"><span data-stu-id="1a984-332">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="1a984-333">Kyselyehdot voidaan asettaa pyynnön tekstiosaan.</span><span class="sxs-lookup"><span data-stu-id="1a984-333">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="1a984-334">Seuraavassa esimerkissä on väri- ja kokoyhdistelmää käyttävä tuotekysely.</span><span class="sxs-lookup"><span data-stu-id="1a984-334">Here is a sample query on the product with color and size combination.</span></span>

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

<span data-ttu-id="1a984-335">`filters`-kenttää varten vain `ProductId` tukee tällä hetkellä useita arvoja.</span><span class="sxs-lookup"><span data-stu-id="1a984-335">For the `filters` field, currently only `ProductId` supports multiple values.</span></span> <span data-ttu-id="1a984-336">Jos `ProductId` on tyhjä matriisi, kaikkia tuotteita kysellään.</span><span class="sxs-lookup"><span data-stu-id="1a984-336">If the `ProductId` is an empty array, all products will be queried.</span></span>

#### <a name="custom-measurement"></a><span data-ttu-id="1a984-337">Mukautettu mitta</span><span class="sxs-lookup"><span data-stu-id="1a984-337">Custom measurement</span></span>

<span data-ttu-id="1a984-338">Oletusmittamäärät linkitetään Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="1a984-338">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="1a984-339">Haluat ehkä kuitenkin määrän, joka koostuu oletusmitoista.</span><span class="sxs-lookup"><span data-stu-id="1a984-339">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="1a984-340">Sitä varten on määritettävä mukautettuja määritä, jotka lisätään käytettävissä olevan määrän tulosteisiin.</span><span class="sxs-lookup"><span data-stu-id="1a984-340">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="1a984-341">Toiminnon antaa yksinkertaisesti mahdollisuuden määrittää lisättävän ja/tai vähennettävän mittajoukon, joiden avulla voidaan muodostaa mukautettu mitta.</span><span class="sxs-lookup"><span data-stu-id="1a984-341">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="1a984-342">Esimerkiksi seuraavalla kyselyehdolla määritetään mukautetun mitan määräksi `MyCustomAvailableforReservation`, jonka kulutusjärjestelmä käyttää.</span><span class="sxs-lookup"><span data-stu-id="1a984-342">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="1a984-343">Kulutusjärjestelmä</span><span class="sxs-lookup"><span data-stu-id="1a984-343">Consumption system</span></span> | <span data-ttu-id="1a984-344">Lasketut mitat</span><span class="sxs-lookup"><span data-stu-id="1a984-344">Calculated measurers</span></span> | <span data-ttu-id="1a984-345">Tietolähde</span><span class="sxs-lookup"><span data-stu-id="1a984-345">Data source</span></span> | <span data-ttu-id="1a984-346">Määre</span><span class="sxs-lookup"><span data-stu-id="1a984-346">Modifier</span></span> | <span data-ttu-id="1a984-347">Määreen laskentatyyppi</span><span class="sxs-lookup"><span data-stu-id="1a984-347">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="1a984-348">Lisäys</span><span class="sxs-lookup"><span data-stu-id="1a984-348">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="1a984-349">Lisäys</span><span class="sxs-lookup"><span data-stu-id="1a984-349">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="1a984-350">Vähennyslasku</span><span class="sxs-lookup"><span data-stu-id="1a984-350">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="1a984-351">Lisäys</span><span class="sxs-lookup"><span data-stu-id="1a984-351">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="1a984-352">Vähennyslasku</span><span class="sxs-lookup"><span data-stu-id="1a984-352">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="1a984-353">Lisäys</span><span class="sxs-lookup"><span data-stu-id="1a984-353">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="1a984-354">Lisäys</span><span class="sxs-lookup"><span data-stu-id="1a984-354">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="1a984-355">Vähennyslasku</span><span class="sxs-lookup"><span data-stu-id="1a984-355">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="1a984-356">Vähennyslasku</span><span class="sxs-lookup"><span data-stu-id="1a984-356">Subtraction</span></span> |

<span data-ttu-id="1a984-357">Mukautetun mittamäärän kysely palauttaa sitten seuraavan tuloksen.</span><span class="sxs-lookup"><span data-stu-id="1a984-357">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="1a984-358">`MyCustomAvailableforReservation`-tulos perustuu seuraavaan mukautettujen mittojen laskenta-asetukseen:</span><span class="sxs-lookup"><span data-stu-id="1a984-358">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="1a984-359">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="1a984-359">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="1a984-360">Varastosaldon muutosten kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="1a984-360">Posting on-hand changes</span></span>

<span data-ttu-id="1a984-361">Tarkka URL-osoite, johon tapahtuma kirjataan, määräytyy maantieteellisen alueen mukaan.</span><span class="sxs-lookup"><span data-stu-id="1a984-361">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="1a984-362">Sen muoto on seuraava:</span><span class="sxs-lookup"><span data-stu-id="1a984-362">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="1a984-363">Tätä URL-osoitetta käytetään todennuksessa HTTP `POST` -menetelmän ohella lähettämään varastosaldon muutostapahtumat palveluun.</span><span class="sxs-lookup"><span data-stu-id="1a984-363">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="1a984-364">Dynamics 365 -palvelun kanssa HTTP-pyyntöjen avulla tapahtuvassa viestinnässä käytetään erityisotsikko, joka ilmaisee sen Supply Chain Management -esiintymän ympäristötunnuksen, johon tiedot on linkitetty.</span><span class="sxs-lookup"><span data-stu-id="1a984-364">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="1a984-365">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="1a984-365">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="1a984-366">Varastosaldon muutosten kirjaamisen kyselyesimerkki 1</span><span class="sxs-lookup"><span data-stu-id="1a984-366">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="1a984-367">Tässä esimerkissä on skenaario, jossa dimensiomääritys määritetään Power Appsissa.</span><span class="sxs-lookup"><span data-stu-id="1a984-367">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="1a984-368">Määritä dimension yhdistämismääritys Power Appsissa käyttämällä seuraavaa kyselyä:</span><span class="sxs-lookup"><span data-stu-id="1a984-368">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="1a984-369">Voit nyt tehdä `dimensionDataSource`-määrityksen ja käyttää mukautettuja dimensioita kyselyissä.</span><span class="sxs-lookup"><span data-stu-id="1a984-369">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="1a984-370">Järjestelmä muuntaa mukautetut dimensiot automaattisesti perusdimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="1a984-370">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="1a984-371">Varastosaldon muutosten kirjaamisen kyselyesimerkki 2</span><span class="sxs-lookup"><span data-stu-id="1a984-371">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="1a984-372">Tässä esimerkissä on skenaario, jossa yhtään dimensiomäärityksen yhdistämismääritystä ei määritetä Power Appsissa, joten myös kirjaamisessa on käytettävä perusdimensioita.</span><span class="sxs-lookup"><span data-stu-id="1a984-372">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="1a984-373">Kaikkien dimensioiden on oltava perusdimensioita, kun `dimensionDataSource`-kentässä on tyhjäarvo, se on tyhjä tai siinä on välilyönti.</span><span class="sxs-lookup"><span data-stu-id="1a984-373">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="1a984-374">JSON-tiedostokentän ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="1a984-374">JSON document field properties</span></span>

<span data-ttu-id="1a984-375">Aiemmin käsitellyissä JSON-kyselyesimerkkien kentissä oli seuraavassa taulukossa olevia ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="1a984-375">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="1a984-376">Kentän tunnus</span><span class="sxs-lookup"><span data-stu-id="1a984-376">Field ID</span></span> | <span data-ttu-id="1a984-377">kuvaus</span><span class="sxs-lookup"><span data-stu-id="1a984-377">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="1a984-378">Tietyn muutostapahtuman yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="1a984-378">A unique ID for the specific change event.</span></span> <span data-ttu-id="1a984-379">Tämän tunnuksen avulla varmistetaan, että jos viestintä palveluun epäonnistuu kirjauksen aikana, tapahtuman lähettäminen uudelleen ei aiheuta saman tapahtuman laskemista kahdesti järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="1a984-379">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="1a984-380">Tapahtumaan linkitetyn organisaation tunnus.</span><span class="sxs-lookup"><span data-stu-id="1a984-380">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="1a984-381">Tämä yhdistetään Supply Chain Management -organisaatioihin tai tietoalueen tunnuksiin.</span><span class="sxs-lookup"><span data-stu-id="1a984-381">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="1a984-382">Kyseisen tuotteen tunniste.</span><span class="sxs-lookup"><span data-stu-id="1a984-382">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="1a984-383">Määrä, jolla varastosaldoa on muutettava.</span><span class="sxs-lookup"><span data-stu-id="1a984-383">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="1a984-384">Jos hyllylle esimerkiksi lisättiin 10 uutta sämpylää, tämä arvo 10.</span><span class="sxs-lookup"><span data-stu-id="1a984-384">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="1a984-385">Jos 3 sämpylää sitten poistettiin hyllystä tai myyntiin, tämä arvo on -3.</span><span class="sxs-lookup"><span data-stu-id="1a984-385">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="1a984-386">Muutostapahtuman kirjauksessa ja kyselyssä käytettävien dimensioiden tietolähde.</span><span class="sxs-lookup"><span data-stu-id="1a984-386">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="1a984-387">Jos tietolähde määritetään, määritetyn tietolähteen mukautettuja dimensioita voidaan käyttää.</span><span class="sxs-lookup"><span data-stu-id="1a984-387">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="1a984-388">Dimensiomääritysten ansiosta varaston näkyvyys voi yhdistää mukautetut dimensiot yleisiin oletusdimensioihin.</span><span class="sxs-lookup"><span data-stu-id="1a984-388">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="1a984-389">Jos `dimensionDataSource` ei ole määritetty, kyselyissä voi käyttää vain yleisiä oletusdimensioita.</span><span class="sxs-lookup"><span data-stu-id="1a984-389">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="1a984-390">Dynaaminen avain- ja arvoparisäilö.</span><span class="sxs-lookup"><span data-stu-id="1a984-390">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="1a984-391">Ne yhdistetään joihinkin Supply Chain Managementin dimensioihin, minkä lisäksi voidaan lisätä mukautettuja dimensioita (kuten *Lähde*), jotka voivat ilmaista, saapuuko tapahtuma Supply Chain Managementista vai ulkoisesta järjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="1a984-391">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="1a984-392">Kyselyt nykyisessä varastosaldossa</span><span class="sxs-lookup"><span data-stu-id="1a984-392">Querying current on-hand</span></span>

<span data-ttu-id="1a984-393">Nykyisen varastosaldon kyselyjen päätepisteessä on samankaltainen URL-osoite:</span><span class="sxs-lookup"><span data-stu-id="1a984-393">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="1a984-394">Kysely siinä tehdään HTTP `POST` -menetelmällä.</span><span class="sxs-lookup"><span data-stu-id="1a984-394">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="1a984-395">Nykyisen varastosaldon kyselyesimerkki 1</span><span class="sxs-lookup"><span data-stu-id="1a984-395">Current on-hand query example 1</span></span>

<span data-ttu-id="1a984-396">Tässä esimerkissä on skenaario, jossa Power Appsissa on jo valmis dimensiomääritys.</span><span class="sxs-lookup"><span data-stu-id="1a984-396">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="1a984-397">Määritä dimension yhdistämismääritys Power Appsissa käyttämällä seuraavaa kyselyä:</span><span class="sxs-lookup"><span data-stu-id="1a984-397">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="1a984-398">Voit nyt tehdä `dimensionDataSource`-määrityksen ja käyttää mukautettuja dimensioita kyselyissä.</span><span class="sxs-lookup"><span data-stu-id="1a984-398">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="1a984-399">Järjestelmä muuntaa mukautetut dimensiot automaattisesti perusdimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="1a984-399">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="1a984-400">`DimensionDataSource` voidaan määrittää `filters`-kohdassa ja mukautetut dimensiot vodaan määrittää sekä `filters`- että `groupByValues`-kohdissa.</span><span class="sxs-lookup"><span data-stu-id="1a984-400">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="1a984-401">Järjestelmä muuntaa mukautetut dimensiot automaattisesti perusdimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="1a984-401">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="1a984-402">Nykyisen varastosaldon kyselyesimerkki 2</span><span class="sxs-lookup"><span data-stu-id="1a984-402">Current on-hand query example 2</span></span>

<span data-ttu-id="1a984-403">Tässä esimerkissä on skenaario, jossa yhtään dimensiomäärityksen yhdistämismääritystä ei määritetä Power Appsissa, joten myös kirjaamisessa on käytettävä perusdimensioita.</span><span class="sxs-lookup"><span data-stu-id="1a984-403">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="1a984-404">Kaikkien dimensioiden on oltava perusdimensioita, kun `filters`-kohdan `dimensionDataSource`-kentässä on tyhjäarvo, se on tyhjä tai siinä on välilyönti.</span><span class="sxs-lookup"><span data-stu-id="1a984-404">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="1a984-405">Palautetun tuloksen esimerkki</span><span class="sxs-lookup"><span data-stu-id="1a984-405">Example return result</span></span>

<span data-ttu-id="1a984-406">Edellisten esimerkkien kyselyissä voitiin palauttaa seuraavankaltainen tulos.</span><span class="sxs-lookup"><span data-stu-id="1a984-406">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="1a984-407">Huomaa, että määräkentät on jäsennelty mittahakemistoksi ja niihin liittyviksi arvoiksi.</span><span class="sxs-lookup"><span data-stu-id="1a984-407">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]