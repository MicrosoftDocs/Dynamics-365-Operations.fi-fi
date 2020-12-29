---
title: Varaston näkyvyyden apuohjelma
description: Tässä aiheessa käsitellään Dynamics 365 Supply Chain Managementin varaston näkyvyyden apuohjelman asentamista ja määrittämistä.
author: chuzheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 2976153a6a7e4b4130e8f7673ed128945aeabf65
ms.sourcegitcommit: 03c2e1717b31e4c17ee7bb9004d2ba8cf379a036
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/24/2020
ms.locfileid: "4625062"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="e4c61-103">Varaston näkyvyyden apuohjelma</span><span class="sxs-lookup"><span data-stu-id="e4c61-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e4c61-104">Varaston näkyvyyden apuohjelma on itsenäinen ja erittäin skaalautuva mikropalvelu, joka mahdollistaa reaaliaikaisen käytettävissä olevan varaston seurannan ja antaa tällä tavoin yleisen näkymän varaston näkyvyyteen.</span><span class="sxs-lookup"><span data-stu-id="e4c61-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="e4c61-105">Kaikki käytettävissä olevaan varastoon liittyvät tiedot viedään palveluun lähes reaaliaikaisesti käyttämällä matala-asteista SQL-integraatiota.</span><span class="sxs-lookup"><span data-stu-id="e4c61-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="e4c61-106">Ulkoiset palvelut käyttävät palvelut tekevät RESTful API -ohjelmointirajapinnoilla käytettävissä olevien tietojen kyselyjä annetuissa dimensioissa ja saavat tällä tavoin luettelon käytettävissä olevista paikoista.</span><span class="sxs-lookup"><span data-stu-id="e4c61-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="e4c61-107">Varastoin näkyvyys on Common Data Serviceen perustuva mikropalvelu, joten sitä voi laajentaa muodostamalla Power Apps -sovelluksia ja käyttämällä Power BI:ta tuottamaan liiketoiminnan tarpeita vastaavia mukautettuja toimintoja.</span><span class="sxs-lookup"><span data-stu-id="e4c61-107">Inventory Visibility is a microservice built on the Common Data Service, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="e4c61-108">Indeksi voidaan lisäksi päivittää tekemään varastokyselyjä.</span><span class="sxs-lookup"><span data-stu-id="e4c61-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="e4c61-109">Varaston näkyvyydessä on määritysvaihtoehtoja, joiden avulla sen voi integroida useiden kolmannen osapuolen järjestelmien kanssa.</span><span class="sxs-lookup"><span data-stu-id="e4c61-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="e4c61-110">Se tukee standardoitua varastodimensiota, mukautettua laajennettavuutta ja standardoituja, määritettäviä laskettuja määriä.</span><span class="sxs-lookup"><span data-stu-id="e4c61-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="e4c61-111">Tässä aiheessa käsitellään Dynamics 365 Supply Chain Managementin varaston näkyvyyden apuohjelman asentamista ja määrittämistä sekä sen ohjelmointirajapinnan käyttöä.</span><span class="sxs-lookup"><span data-stu-id="e4c61-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="e4c61-112">Varaston näkyvyyden lisäapuohjelman asentaminen</span><span class="sxs-lookup"><span data-stu-id="e4c61-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="e4c61-113">Varaston näkyvyyden lisäapuohjelman asentamiseen on käytettävä Microsoft Dynamics Lifecycle Servicesiä (LCS).</span><span class="sxs-lookup"><span data-stu-id="e4c61-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="e4c61-114">LCS on yhteistyöportaali, jonka muodostamassa ympäristössä ja jonka säännöllisesti päivitetyillä palveluilla voi hallita Dynamics 365 Finance and Operations -sovellusten elinkaarta.</span><span class="sxs-lookup"><span data-stu-id="e4c61-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="e4c61-115">Lisätietoja on kohdassa [Lifecycle Services -resurssit](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="e4c61-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="e4c61-116">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="e4c61-116">Prerequisites</span></span>

<span data-ttu-id="e4c61-117">Ennen varaston näkyvyyden apuohjelman asentamista:</span><span class="sxs-lookup"><span data-stu-id="e4c61-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="e4c61-118">Hanki LCS-toteutusprojekti, jossa on otettu käyttöön vähintään yksi ympäristö.</span><span class="sxs-lookup"><span data-stu-id="e4c61-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="e4c61-119">Luo tarjoomalle beeta-avaimet LCS:ssa.</span><span class="sxs-lookup"><span data-stu-id="e4c61-119">Generate the beta keys for your offering in LCS.</span></span>
- <span data-ttu-id="e4c61-120">Ota tarjooman beeta-avaimet käyttöön käyttäjälle LCS:ssa.</span><span class="sxs-lookup"><span data-stu-id="e4c61-120">Enable the beta keys for your offering for your user in LCS.</span></span>
- <span data-ttu-id="e4c61-121">Ota yhteys Microsoftin varaston näkyvyyden tuotetiimiin and ympäristötunnus, jossa haluat ottaa varaston näkyvyyden apuohjelman käyttöön.</span><span class="sxs-lookup"><span data-stu-id="e4c61-121">Contact the Microsoft Inventory Visibility product team and provide an environment ID where you want to deploy the Inventory Visibility Add-in.</span></span>

<span data-ttu-id="e4c61-122">Jos sinulla on näitä edellytyksiä koskevia kysymyksiä, ota yhteys varaston näkyvyyden tuotetiimiin.</span><span class="sxs-lookup"><span data-stu-id="e4c61-122">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="e4c61-123">Lisäosan asentaminen</span><span class="sxs-lookup"><span data-stu-id="e4c61-123">Install the add-in</span></span>

<span data-ttu-id="e4c61-124">Varaston näkyvyyden apuohjelman asentaminen:</span><span class="sxs-lookup"><span data-stu-id="e4c61-124">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="e4c61-125">Kirjaudu [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) -portaaliin.</span><span class="sxs-lookup"><span data-stu-id="e4c61-125">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="e4c61-126">Valitse aloitussivulla projekti, jossa ympäristö on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="e4c61-126">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="e4c61-127">Valitse projektisivulla ympäristö, johon haluat asentaa apuohjelman.</span><span class="sxs-lookup"><span data-stu-id="e4c61-127">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="e4c61-128">Vieritä ympäristösivulla **Ympäristöapuohjelmat** -osaan.</span><span class="sxs-lookup"><span data-stu-id="e4c61-128">On the environment page, scroll down until you see the **Environment add-ins** section.</span></span> <span data-ttu-id="e4c61-129">Jos osa ei ole näkyvissä, varmista, että edellytyksissä mainitut beeta-avaimet on käsitelty kokonaisuudessaan.</span><span class="sxs-lookup"><span data-stu-id="e4c61-129">If the section isn't visible, make sure the prerequisite beta keys have been fully processed.</span></span>
1. <span data-ttu-id="e4c61-130">Valitse **Ympäristöapuohjelmat**-osassa **Asenna uusi apuohjelma**.</span><span class="sxs-lookup"><span data-stu-id="e4c61-130">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
    <span data-ttu-id="e4c61-131">![Ympäristösivu LCS:ssa](media/inventory-visibility-environment.png "Ympäristösivu LCS:ssa")</span><span class="sxs-lookup"><span data-stu-id="e4c61-131">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>
1. <span data-ttu-id="e4c61-132">Valitse **Asenna uusi apuohjelma** -linkki.</span><span class="sxs-lookup"><span data-stu-id="e4c61-132">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="e4c61-133">Käytettävissä olevien apuohjelmien luettelo avautuu.</span><span class="sxs-lookup"><span data-stu-id="e4c61-133">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="e4c61-134">Valitse luettelossa **Varastopalvelu**.</span><span class="sxs-lookup"><span data-stu-id="e4c61-134">Select **Inventory service** from the list.</span></span> <span data-ttu-id="e4c61-135">(Huomaa, että sen nimi voi olla nyt **Dynamics 365 Supply Chain Managementin varaston näkyvyyden apuohjelma**.)</span><span class="sxs-lookup"><span data-stu-id="e4c61-135">(Note, this may now be listed as **Inventory Visibility Add-in for Dynamics 365 Supply Chain Management**.)</span></span>
1. <span data-ttu-id="e4c61-136">Anna arvot seuraavissa ympäristön kentissä:</span><span class="sxs-lookup"><span data-stu-id="e4c61-136">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="e4c61-137">**AAD-sovelluksen tunnus**</span><span class="sxs-lookup"><span data-stu-id="e4c61-137">**AAD application ID**</span></span>
    - <span data-ttu-id="e4c61-138">**AAD-vuokraajan tunnus**</span><span class="sxs-lookup"><span data-stu-id="e4c61-138">**AAD tenant ID**</span></span>

    <span data-ttu-id="e4c61-139">![Apuohjelman määrityssivu](media/inventory-visibility-setup.png "Apuohjelman määrityssivu")</span><span class="sxs-lookup"><span data-stu-id="e4c61-139">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="e4c61-140">Hyväksy käyttöehdot valitsemalla **Käyttöehdot**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="e4c61-140">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="e4c61-141">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="e4c61-141">Select **Install**.</span></span> <span data-ttu-id="e4c61-142">Apuohjelman tilana näkyy nyt **Asennetaan**.</span><span class="sxs-lookup"><span data-stu-id="e4c61-142">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="e4c61-143">Se on valmis, päivitä sivu, jonka jälkeen tilana on **Asennettu**.</span><span class="sxs-lookup"><span data-stu-id="e4c61-143">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="get-a-security-service-token"></a><span data-ttu-id="e4c61-144">Palvelun suojaustunnuksen hankkiminen</span><span class="sxs-lookup"><span data-stu-id="e4c61-144">Get a security service token</span></span>

<span data-ttu-id="e4c61-145">Palvelun suojaustunnus haetaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e4c61-145">To get a security service token, do the following:</span></span>

1. <span data-ttu-id="e4c61-146">Hanki `aadToken` ja tee päätepistekutsu: https://securityservice.operations365.dynamics.com/token.</span><span class="sxs-lookup"><span data-stu-id="e4c61-146">Get your `aadToken` and call the endpoint: https://securityservice.operations365.dynamics.com/token.</span></span>
1. <span data-ttu-id="e4c61-147">Korvaa `client_assertion` tekstiosassa omalla `aadToken`-tunnuksella.</span><span class="sxs-lookup"><span data-stu-id="e4c61-147">Replace the `client_assertion` in the body with your `aadToken`.</span></span>
1. <span data-ttu-id="e4c61-148">Vaihda tekstiosan kontekstin tilalle ympäristö, jossa haluat ottaa apuohjelman käyttöön.</span><span class="sxs-lookup"><span data-stu-id="e4c61-148">Replace the context in the body with the environment where you want to deploy the add-in.</span></span>
1. <span data-ttu-id="e4c61-149">Vaihda vaikutusalue tekstiosassa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e4c61-149">Replace the scope in the body with the following:</span></span>

    - <span data-ttu-id="e4c61-150">MCK-vaikutusalue – https://inventoryservice.operations365.dynamics.cn/.default</span><span class="sxs-lookup"><span data-stu-id="e4c61-150">Scope for MCK - "https://inventoryservice.operations365.dynamics.cn/.default"</span></span>  
    <span data-ttu-id="e4c61-151">(Azure Active Directory -sovelluksen tunnus ja MCK-vuokraajan tunnus ovat kohdassa `appsettings.mck.json`.)</span><span class="sxs-lookup"><span data-stu-id="e4c61-151">(You can find the Azure Active Directory application ID and tenant ID for MCK in `appsettings.mck.json`.)</span></span>
    - <span data-ttu-id="e4c61-152">PROD-vaikutusalue – https://inventoryservice.operations365.dynamics.com/.default</span><span class="sxs-lookup"><span data-stu-id="e4c61-152">Scope for PROD - "https://inventoryservice.operations365.dynamics.com/.default"</span></span>  
    <span data-ttu-id="e4c61-153">(Azure Active Directory -sovelluksen tunnus ja PROD-vuokraajan tunnus ovat kohdassa `appsettings.prod.json`.)</span><span class="sxs-lookup"><span data-stu-id="e4c61-153">(You can find the Azure Active Directory application ID and tenant ID for PROD in `appsettings.prod.json`.)</span></span>

    <span data-ttu-id="e4c61-154">Tuloksen pitäisi muistuttaa seuraavaa esimerkkiä:</span><span class="sxs-lookup"><span data-stu-id="e4c61-154">The result should resemble the following example.</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{**Your_AADToken**}",
        "scope":"**https://inventoryservice.operations365.dynamics.com/.default**",
        "context": "**5dbf6cc8-255e-4de2-8a25-2101cd5649b4**",
        "context_type": "finops-env"
    }
    ```

1. <span data-ttu-id="e4c61-155">`access_token` saadaan vastauksessa.</span><span class="sxs-lookup"><span data-stu-id="e4c61-155">You will get an `access_token` in response.</span></span> <span data-ttu-id="e4c61-156">Sitä tarvitaan haltijatunnuksena, jolla varastoin näkyvyyden ohjelmointirajapintaa kutsutaan.</span><span class="sxs-lookup"><span data-stu-id="e4c61-156">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="e4c61-157">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="e4c61-157">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a><span data-ttu-id="e4c61-158">Lisäosan asennuksen poistaminen</span><span class="sxs-lookup"><span data-stu-id="e4c61-158">Uninstall the add-in</span></span>

<span data-ttu-id="e4c61-159">Poista apuohjelman asennus valitsemalla **Poista asennus**.</span><span class="sxs-lookup"><span data-stu-id="e4c61-159">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="e4c61-160">Päivitä LCS, ja varaston näkyvyyden apuohjelma poistetaan.</span><span class="sxs-lookup"><span data-stu-id="e4c61-160">Refresh LCS and the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="e4c61-161">Asennuksen poistoprosessi poistaa apuohjelman rekisteröinnin sekä käynnistää kaikkien palveluun tallennettujen liiketoimintatietojen puhdistustyön.</span><span class="sxs-lookup"><span data-stu-id="e4c61-161">The uninstall process will remove the add-in registration and also start a job to clean up all of the business data stored in the service.</span></span>

## <a name="inventory-visibility-add-in-public-api"></a><span data-ttu-id="e4c61-162">Varaston näkyvyyden apuohjelman julkinen ohjelmointirajapinta</span><span class="sxs-lookup"><span data-stu-id="e4c61-162">Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="e4c61-163">Varaston näkyvyyden apuohjelman julkinen REST API sisältää useita nimenomaisia integroinnin päätepisteitä.</span><span class="sxs-lookup"><span data-stu-id="e4c61-163">The public REST API of the of the Inventory Visibility Add-in presents several specific endpoints of integration.</span></span> <span data-ttu-id="e4c61-164">Se tukee kolmea pääasiallista vuorovaikutustyyppiä:</span><span class="sxs-lookup"><span data-stu-id="e4c61-164">It supports three main interaction types:</span></span>

- <span data-ttu-id="e4c61-165">Varastosaldon määrän muutosten kirjaaminen apuohjelmaan ulkoisesta järjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="e4c61-165">Posting on-hand changes to the add-in from an external system.</span></span>
- <span data-ttu-id="e4c61-166">Nykyisten käytettävissä olevien määrien kysely ulkoisesta järjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="e4c61-166">Querying current on-hand quantities from an external system.</span></span>
- <span data-ttu-id="e4c61-167">Automaattinen synkronointi Supply Chain Managementin käytettävissä olevan varaston kanssa.</span><span class="sxs-lookup"><span data-stu-id="e4c61-167">Automatic synchronization with Supply Chain Management on-hand.</span></span>

<span data-ttu-id="e4c61-168">Automaattinen synkronointi ei sisälly julkiseen ohjelmointirajapintaan, vaan se käsitellään taustalla ympäristöissä, joissa varaston näkyvyyden apuohjelma on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="e4c61-168">The automatic synchronization isn't part of the public API but is instead handled in the background for environments that have enabled the Inventory Visibility Add-in.</span></span>

### <a name="authentication"></a><span data-ttu-id="e4c61-169">Todennus</span><span class="sxs-lookup"><span data-stu-id="e4c61-169">Authentication</span></span>

<span data-ttu-id="e4c61-170">Ympäristön suojaustunnusta käytetään varaston näkyvyyden apuohjelman kutsumiseen, joten Azure Active Directory -tunnus on luotava Azure Active Directory -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="e4c61-170">The platform security token is used to call the Inventory Visibility Add-in, so you must generate an Azure Active Directory token using your Azure Active Directory application.</span></span>

<span data-ttu-id="e4c61-171">Lisätietoja suojaustunnuksen hakemista on kohdassa [Varaston näkyvyyden apuohjelman asentaminen](#install-add-in).</span><span class="sxs-lookup"><span data-stu-id="e4c61-171">For more information about how to get the security token, see [Install the Inventory Visibility Add-in](#install-add-in).</span></span>

### <a name="configure-the-inventory-visibility-api"></a><span data-ttu-id="e4c61-172">Varaston näkyvyyden ohjelmointirajapinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e4c61-172">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="e4c61-173">Ennen palvelun käyttöä on tehtävä valmiiksi seuraavissa aliosissa käsiteltävät määritykset.</span><span class="sxs-lookup"><span data-stu-id="e4c61-173">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="e4c61-174">Määritykset voivat vaihdella ympäristön tietojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e4c61-174">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="e4c61-175">Siinä pääasiallisesti neljä osaa:</span><span class="sxs-lookup"><span data-stu-id="e4c61-175">It primarily includes four parts:</span></span>

- [<span data-ttu-id="e4c61-176">Osiointi</span><span class="sxs-lookup"><span data-stu-id="e4c61-176">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="e4c61-177">Dimensiomääritykset</span><span class="sxs-lookup"><span data-stu-id="e4c61-177">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="e4c61-178">Indeksointi</span><span class="sxs-lookup"><span data-stu-id="e4c61-178">Indexing</span></span>](#indexing)
- [<span data-ttu-id="e4c61-179">Mukautettu mitta</span><span class="sxs-lookup"><span data-stu-id="e4c61-179">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="e4c61-180">Osiointi</span><span class="sxs-lookup"><span data-stu-id="e4c61-180">Partitioning</span></span>

<span data-ttu-id="e4c61-181">Osiointi voi vaikuttaa merkittävästi varaston näkyvyyden ohjelmointirajapinnan toimintaan.</span><span class="sxs-lookup"><span data-stu-id="e4c61-181">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="e4c61-182">Niinpä kannattaakin määrittää rakenne, jossa voidaan ryhmitellä tietoja pienissä osissa siten, että merkitykselliset tietokyselyt ovat mahdollisia.</span><span class="sxs-lookup"><span data-stu-id="e4c61-182">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="e4c61-183">`organizationId` (Supply Chain Managementissa `dataAreaId`) sisältyy aina osiointiin, ja varaston näkyvyys osioidaan oletusarvoisesti dimensioiden perusteella, kuten *Toimipaikka + sijainti*.</span><span class="sxs-lookup"><span data-stu-id="e4c61-183">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="e4c61-184">Tämän vuoksi palveluissa tehtävissä kyselyissä on aina käytettävä suodattimissa määritettyjä dimensioita.</span><span class="sxs-lookup"><span data-stu-id="e4c61-184">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="e4c61-185">*Toimipaikka* ja *sijainti* ovat kaksi varaston näkyvyyden yleistä oletusdimensiota.</span><span class="sxs-lookup"><span data-stu-id="e4c61-185">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="e4c61-186">Supply Chain Managementin näiden dimensioiden nimet ovat *toimipaikka* (`InventSiteId`) ja *varasto* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="e4c61-186">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="e4c61-187">Dimensiomääritykset</span><span class="sxs-lookup"><span data-stu-id="e4c61-187">Dimension configurations</span></span>

<span data-ttu-id="e4c61-188">Varaston näkyvyyden yleisten oletusdimensioiden luettelon ansiosta usein lähdejärjestelmien integrointi on mahdollista.</span><span class="sxs-lookup"><span data-stu-id="e4c61-188">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="e4c61-189">Seuraavassa taulukossa on varastodimensiot, jotka tulevat varaston näkyvyyden oletusdimensionimiksi.</span><span class="sxs-lookup"><span data-stu-id="e4c61-189">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="e4c61-190">Dimensiotyyppi</span><span class="sxs-lookup"><span data-stu-id="e4c61-190">Dimension type</span></span> | <span data-ttu-id="e4c61-191">Dimension nimi</span><span class="sxs-lookup"><span data-stu-id="e4c61-191">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="e4c61-192">Tuote</span><span class="sxs-lookup"><span data-stu-id="e4c61-192">Product</span></span> | `ColorId` |
| <span data-ttu-id="e4c61-193">Tuote</span><span class="sxs-lookup"><span data-stu-id="e4c61-193">Product</span></span> | `SizeId` |
| <span data-ttu-id="e4c61-194">Tuote</span><span class="sxs-lookup"><span data-stu-id="e4c61-194">Product</span></span> | `StyleId` |
| <span data-ttu-id="e4c61-195">Tuote</span><span class="sxs-lookup"><span data-stu-id="e4c61-195">Product</span></span> | `ConfigId` |
| <span data-ttu-id="e4c61-196">Seuranta</span><span class="sxs-lookup"><span data-stu-id="e4c61-196">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="e4c61-197">Seuranta</span><span class="sxs-lookup"><span data-stu-id="e4c61-197">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="e4c61-198">Toimipaikka</span><span class="sxs-lookup"><span data-stu-id="e4c61-198">Location</span></span> | `LocationId` |
| <span data-ttu-id="e4c61-199">Toimipaikka</span><span class="sxs-lookup"><span data-stu-id="e4c61-199">Location</span></span> | `SiteId` |
| <span data-ttu-id="e4c61-200">Varaston tila</span><span class="sxs-lookup"><span data-stu-id="e4c61-200">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="e4c61-201">Varastokohtainen</span><span class="sxs-lookup"><span data-stu-id="e4c61-201">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="e4c61-202">Varastokohtainen</span><span class="sxs-lookup"><span data-stu-id="e4c61-202">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="e4c61-203">Varastokohtainen</span><span class="sxs-lookup"><span data-stu-id="e4c61-203">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="e4c61-204">Edellisessä taulukossa mainittu dimensiotyyppi on tarkoitettu vain tiedoksi.</span><span class="sxs-lookup"><span data-stu-id="e4c61-204">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="e4c61-205">Dimensiotyyppiä ei tarvitse määrittää varaston näkyvyydessä.</span><span class="sxs-lookup"><span data-stu-id="e4c61-205">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="e4c61-206">Jos mukautettu dimensio on luotu ja sen on siirryttävä oletusarvoon, kun varaston näkyvyys käyttää sitä, **mukautetun dimension** nimi voidaan määrittää varaston näkyvyydessä.</span><span class="sxs-lookup"><span data-stu-id="e4c61-206">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="e4c61-207">Ulkoiset järjestelmät käyttävät varaston näkyvyyttä RESTful API -ohjelmointirajapinnoilla, jotka ottavat käytettävissä olevat tiedot käyttöön annetuissa dimensiojoukoissa, joissa kyselyt tehdään.</span><span class="sxs-lookup"><span data-stu-id="e4c61-207">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="e4c61-208">Integroinnin osalta varaston näkyvyydessä voidaan määrittää *ulkoinen kanavan tietolähde* ja *kohdedimensioiden* lähdedimensio varaston näkyvyydessä.</span><span class="sxs-lookup"><span data-stu-id="e4c61-208">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="e4c61-209">Kohdedimensioiden on oltava jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="e4c61-209">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="e4c61-210">Varaston näkyvyyden oletusdimensiot</span><span class="sxs-lookup"><span data-stu-id="e4c61-210">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="e4c61-211">Mukautetut dimensiot</span><span class="sxs-lookup"><span data-stu-id="e4c61-211">Custom dimensions</span></span>

<span data-ttu-id="e4c61-212">Dimensiomääritysten tarkoitus on standardoida monen järjestelmän integrointi dimensiokyselyitä ja tapahtuman dimensioihin kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="e4c61-212">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="e4c61-213">Indeksointi</span><span class="sxs-lookup"><span data-stu-id="e4c61-213">Indexing</span></span>

<span data-ttu-id="e4c61-214">Käytettävissä olevan varaston kysely ei ole useimmiten korkeimmalla kokonaistasolla, vaan tulokset halutaan ehkä nähdä varastodimensioiden mukaan koostettuina.</span><span class="sxs-lookup"><span data-stu-id="e4c61-214">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="e4c61-215">Varaston näkyvyys on joustava, sillä siinä voidaan määrittää dimensioon tai dimensioyhdistelmiin perustuvia indeksejä.</span><span class="sxs-lookup"><span data-stu-id="e4c61-215">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="e4c61-216">Tällä hetkellä indeksejä voi määrittään enintään viisi.</span><span class="sxs-lookup"><span data-stu-id="e4c61-216">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="e4c61-217">Käytettävää dimensiota tai dimensioyhdistelmää on harkittava huolellisesti ennen toteutusta, sillä näin voidaan varmistaa, että se todella vastaa liiketoiminnan tarpeita.</span><span class="sxs-lookup"><span data-stu-id="e4c61-217">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="e4c61-218">Tuotekysely voidaan haluta tehdä esimerkiksi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e4c61-218">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="e4c61-219">Kyselynä käytettävissä oleva koostetuote *väri*- ja *koko*-dimension mukaan.</span><span class="sxs-lookup"><span data-stu-id="e4c61-219">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="e4c61-220">Joissakin tapauksissa kyselyn kohteena voi olla tuote kokonaisuudessaan.</span><span class="sxs-lookup"><span data-stu-id="e4c61-220">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="e4c61-221">Kaksi indeksiä määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e4c61-221">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="e4c61-222">Tyhjä hakasulje tekee koosteen osiossa olevan tuotetunnuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="e4c61-222">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="e4c61-223">Indeksointi määrittää, miten tulokset ryhmitellään `groupBy`-kyselyasetuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="e4c61-223">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="e4c61-224">Jos tässä tapauksessa ei määritetä `groupBy`-arvoja, tuloksena on `productid`-kohtainen kokonaismäärä.</span><span class="sxs-lookup"><span data-stu-id="e4c61-224">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="e4c61-225">Jos `groupBy`-määrityksenä on sen sijaan `groupBy=ColorId&groupBy=SizeId`, tuloksena on useita rivejä, jotka perustuvat järjestelmässä oleviin väri- ja kokoyhdistelmiin.</span><span class="sxs-lookup"><span data-stu-id="e4c61-225">Otherwise if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="e4c61-226">Kyselyehdot voidaan asettaa pyynnön tekstiosaan.</span><span class="sxs-lookup"><span data-stu-id="e4c61-226">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="e4c61-227">Seuraavassa esimerkissä on väri- ja kokoyhdistelmää käyttävä tuotekysely.</span><span class="sxs-lookup"><span data-stu-id="e4c61-227">Here is a sample query on the product with color and size combination.</span></span>

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

#### <a name="custom-measurement"></a><span data-ttu-id="e4c61-228">Mukautettu mitta</span><span class="sxs-lookup"><span data-stu-id="e4c61-228">Custom measurement</span></span>

<span data-ttu-id="e4c61-229">Vaikka oletusarvoiset mittamäärät linkitetään Supply Chain Managementiin, myös oletusmittamäärien yhdistelmistä koostuva määrä on mahdollinen.</span><span class="sxs-lookup"><span data-stu-id="e4c61-229">The default measurement quantities are linked to Supply Chain Management, however you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="e4c61-230">Sitä varten on määritettävä mukautettuja määritä, jotka lisätään käytettävissä olevan määrän tulosteisiin.</span><span class="sxs-lookup"><span data-stu-id="e4c61-230">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="e4c61-231">Toiminnon antaa yksinkertaisesti mahdollisuuden määrittää lisättävän ja/tai vähennettävän mittajoukon, joiden avulla voidaan muodostaa mukautettu mitta.</span><span class="sxs-lookup"><span data-stu-id="e4c61-231">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="e4c61-232">Esimerkiksi seuraavalla kyselyehdolla määritetään mukautetun mitan määräksi `MyCustomAvailableforReservation`, jonka kulutusjärjestelmä käyttää.</span><span class="sxs-lookup"><span data-stu-id="e4c61-232">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="e4c61-233">Kulutusjärjestelmä</span><span class="sxs-lookup"><span data-stu-id="e4c61-233">Consumption system</span></span> | <span data-ttu-id="e4c61-234">Lasketut mitat</span><span class="sxs-lookup"><span data-stu-id="e4c61-234">Calculated measurers</span></span> | <span data-ttu-id="e4c61-235">Tietolähde</span><span class="sxs-lookup"><span data-stu-id="e4c61-235">Data source</span></span> | <span data-ttu-id="e4c61-236">Määre</span><span class="sxs-lookup"><span data-stu-id="e4c61-236">Modifier</span></span> | <span data-ttu-id="e4c61-237">Määreen laskentatyyppi</span><span class="sxs-lookup"><span data-stu-id="e4c61-237">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="e4c61-238">Lisäys</span><span class="sxs-lookup"><span data-stu-id="e4c61-238">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="e4c61-239">Lisäys</span><span class="sxs-lookup"><span data-stu-id="e4c61-239">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="e4c61-240">Vähennyslasku</span><span class="sxs-lookup"><span data-stu-id="e4c61-240">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="e4c61-241">Lisäys</span><span class="sxs-lookup"><span data-stu-id="e4c61-241">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="e4c61-242">Vähennyslasku</span><span class="sxs-lookup"><span data-stu-id="e4c61-242">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="e4c61-243">Lisäys</span><span class="sxs-lookup"><span data-stu-id="e4c61-243">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="e4c61-244">Lisäys</span><span class="sxs-lookup"><span data-stu-id="e4c61-244">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="e4c61-245">Vähennyslasku</span><span class="sxs-lookup"><span data-stu-id="e4c61-245">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="e4c61-246">Vähennyslasku</span><span class="sxs-lookup"><span data-stu-id="e4c61-246">Subtraction</span></span> |

<span data-ttu-id="e4c61-247">Mukautetun mittamäärän kysely palauttaa sitten seuraavan tuloksen.</span><span class="sxs-lookup"><span data-stu-id="e4c61-247">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="e4c61-248">`MyCustomAvailableforReservation`-tulos perustuu seuraavaan mukautettujen mittojen laskenta-asetukseen:</span><span class="sxs-lookup"><span data-stu-id="e4c61-248">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="e4c61-249">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="e4c61-249">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="e4c61-250">Varastosaldon muutosten kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="e4c61-250">Posting on-hand changes</span></span>

<span data-ttu-id="e4c61-251">Tarkka URL-osoite, johon tapahtuma kirjataan, määräytyy maantieteellisen alueen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e4c61-251">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="e4c61-252">Sen muoto on seuraava:</span><span class="sxs-lookup"><span data-stu-id="e4c61-252">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="e4c61-253">Tätä URL-osoitetta käytetään todennuksessa HTTP `POST` -menetelmän ohella lähettämään varastosaldon muutostapahtumat palveluun.</span><span class="sxs-lookup"><span data-stu-id="e4c61-253">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="e4c61-254">Dynamics 365 -palvelun kanssa HTTP-pyyntöjen avulla tapahtuvassa viestinnässä käytetään erityisotsikko, joka ilmaisee sen Supply Chain Management -esiintymän ympäristötunnuksen, johon tiedot on linkitetty.</span><span class="sxs-lookup"><span data-stu-id="e4c61-254">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="e4c61-255">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="e4c61-255">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="e4c61-256">Varastosaldon muutosten kirjaamisen kyselyesimerkki 1</span><span class="sxs-lookup"><span data-stu-id="e4c61-256">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="e4c61-257">Tässä esimerkissä on skenaario, jossa dimensiomääritys määritetään Power Appsissa.</span><span class="sxs-lookup"><span data-stu-id="e4c61-257">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="e4c61-258">Määritä dimension yhdistämismääritys Power Appsissa käyttämällä seuraavaa kyselyä:</span><span class="sxs-lookup"><span data-stu-id="e4c61-258">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="e4c61-259">Voit nyt tehdä `dimensionDataSource`-määrityksen ja käyttää mukautettuja dimensioita kyselyissä.</span><span class="sxs-lookup"><span data-stu-id="e4c61-259">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="e4c61-260">Järjestelmä muuntaa mukautetut dimensiot automaattisesti perusdimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="e4c61-260">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="e4c61-261">Varastosaldon muutosten kirjaamisen kyselyesimerkki 2</span><span class="sxs-lookup"><span data-stu-id="e4c61-261">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="e4c61-262">Tässä esimerkissä on skenaario, jossa yhtään dimensiomäärityksen yhdistämismääritystä ei määritetä Power Appsissa, joten myös kirjaamisessa on käytettävä perusdimensioita.</span><span class="sxs-lookup"><span data-stu-id="e4c61-262">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="e4c61-263">Kaikkien dimensioiden on oltava perusdimensioita, kun `dimensionDataSource`-kentässä on tyhjäarvo, se on tyhjä tai siinä on välilyönti.</span><span class="sxs-lookup"><span data-stu-id="e4c61-263">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="e4c61-264">JSON-tiedostokentän ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="e4c61-264">JSON document field properties</span></span>

<span data-ttu-id="e4c61-265">Aiemmin käsitellyissä JSON-kyselyesimerkkien kentissä oli seuraavassa taulukossa olevia ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="e4c61-265">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="e4c61-266">Kentän tunnus</span><span class="sxs-lookup"><span data-stu-id="e4c61-266">Field ID</span></span> | <span data-ttu-id="e4c61-267">kuvaus</span><span class="sxs-lookup"><span data-stu-id="e4c61-267">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="e4c61-268">Tietyn muutostapahtuman yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="e4c61-268">A unique ID for the specific change event.</span></span> <span data-ttu-id="e4c61-269">Tämän tunnuksen avulla varmistetaan, että jos viestintä palveluun epäonnistuu kirjauksen aikana, tapahtuman lähettäminen uudelleen ei aiheuta saman tapahtuman laskemista kahdesti järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="e4c61-269">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="e4c61-270">Tapahtumaan linkitetyn organisaation tunnus.</span><span class="sxs-lookup"><span data-stu-id="e4c61-270">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="e4c61-271">Tämä yhdistetään Supply Chain Management -organisaatioihin tai tietoalueen tunnuksiin.</span><span class="sxs-lookup"><span data-stu-id="e4c61-271">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="e4c61-272">Kyseisen tuotteen tunniste.</span><span class="sxs-lookup"><span data-stu-id="e4c61-272">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="e4c61-273">Määrä, jolla varastosaldoa on muutettava.</span><span class="sxs-lookup"><span data-stu-id="e4c61-273">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="e4c61-274">Jos hyllylle esimerkiksi lisättiin 10 uutta sämpylää, tämä arvo 10.</span><span class="sxs-lookup"><span data-stu-id="e4c61-274">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="e4c61-275">Jos 3 sämpylää sitten poistettiin hyllystä tai myyntiin, tämä arvo on -3.</span><span class="sxs-lookup"><span data-stu-id="e4c61-275">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="e4c61-276">Muutostapahtuman kirjauksessa ja kyselyssä käytettävien dimensioiden tietolähde.</span><span class="sxs-lookup"><span data-stu-id="e4c61-276">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="e4c61-277">Jos tietolähde määritetään, määritetyn tietolähteen mukautettuja dimensioita voidaan käyttää.</span><span class="sxs-lookup"><span data-stu-id="e4c61-277">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="e4c61-278">Dimensiomääritysten ansiosta varaston näkyvyys voi yhdistää mukautetut dimensiot yleisiin oletusdimensioihin.</span><span class="sxs-lookup"><span data-stu-id="e4c61-278">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="e4c61-279">Jos `dimensionDataSource` ei ole määritetty, kyselyissä voi käyttää vain yleisiä oletusdimensioita.</span><span class="sxs-lookup"><span data-stu-id="e4c61-279">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="e4c61-280">Dynaaminen avain- ja arvoparisäilö.</span><span class="sxs-lookup"><span data-stu-id="e4c61-280">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="e4c61-281">Ne yhdistetään joihinkin Supply Chain Managementin dimensioihin, minkä lisäksi voidaan lisätä mukautettuja dimensioita (kuten *Lähde*), jotka voivat ilmaista, saapuuko tapahtuma Supply Chain Managementista vai ulkoisesta järjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="e4c61-281">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="e4c61-282">Kyselyt nykyisessä varastosaldossa</span><span class="sxs-lookup"><span data-stu-id="e4c61-282">Querying current on-hand</span></span>

<span data-ttu-id="e4c61-283">Nykyisen varastosaldon kyselyjen päätepisteessä on samankaltainen URL-osoite:</span><span class="sxs-lookup"><span data-stu-id="e4c61-283">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="e4c61-284">Kysely siinä tehdään HTTP `POST` -menetelmällä.</span><span class="sxs-lookup"><span data-stu-id="e4c61-284">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="e4c61-285">Nykyisen varastosaldon kyselyesimerkki 1</span><span class="sxs-lookup"><span data-stu-id="e4c61-285">Current on-hand query example 1</span></span>

<span data-ttu-id="e4c61-286">Tässä esimerkissä on skenaario, jossa Power Appsissa on jo valmis dimensiomääritys.</span><span class="sxs-lookup"><span data-stu-id="e4c61-286">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="e4c61-287">Määritä dimension yhdistämismääritys Power Appsissa käyttämällä seuraavaa kyselyä:</span><span class="sxs-lookup"><span data-stu-id="e4c61-287">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="e4c61-288">Voit nyt tehdä `dimensionDataSource`-määrityksen ja käyttää mukautettuja dimensioita kyselyissä.</span><span class="sxs-lookup"><span data-stu-id="e4c61-288">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="e4c61-289">Järjestelmä muuntaa mukautetut dimensiot automaattisesti perusdimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="e4c61-289">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="e4c61-290">`DimensionDataSource` voidaan määrittää `filters`-kohdassa ja mukautetut dimensiot vodaan määrittää sekä `filters`- että `groupByValues`-kohdissa.</span><span class="sxs-lookup"><span data-stu-id="e4c61-290">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="e4c61-291">Järjestelmä muuntaa mukautetut dimensiot automaattisesti perusdimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="e4c61-291">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="e4c61-292">Nykyisen varastosaldon kyselyesimerkki 2</span><span class="sxs-lookup"><span data-stu-id="e4c61-292">Current on-hand query example 2</span></span>

<span data-ttu-id="e4c61-293">Tässä esimerkissä on skenaario, jossa yhtään dimensiomäärityksen yhdistämismääritystä ei määritetä Power Appsissa, joten myös kirjaamisessa on käytettävä perusdimensioita.</span><span class="sxs-lookup"><span data-stu-id="e4c61-293">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="e4c61-294">Kaikkien dimensioiden on oltava perusdimensioita, kun `filters`-kohdan `dimensionDataSource`-kentässä on tyhjäarvo, se on tyhjä tai siinä on välilyönti.</span><span class="sxs-lookup"><span data-stu-id="e4c61-294">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="e4c61-295">Palautetun tuloksen esimerkki</span><span class="sxs-lookup"><span data-stu-id="e4c61-295">Example return result</span></span>

<span data-ttu-id="e4c61-296">Edellisten esimerkkien kyselyissä voitiin palauttaa seuraavankaltainen tulos.</span><span class="sxs-lookup"><span data-stu-id="e4c61-296">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="e4c61-297">Huomaa, että määräkentät on jäsennelty mittahakemistoksi ja niihin liittyviksi arvoiksi.</span><span class="sxs-lookup"><span data-stu-id="e4c61-297">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>
