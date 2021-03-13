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
ms.openlocfilehash: 4e6f7e0a3978bbf7e520f8cbcfd27c4cfe507777
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114667"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="bcfc4-103">Varaston näkyvyyden apuohjelma</span><span class="sxs-lookup"><span data-stu-id="bcfc4-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="bcfc4-104">Varaston näkyvyyden apuohjelma on itsenäinen ja erittäin skaalautuva mikropalvelu, joka mahdollistaa reaaliaikaisen käytettävissä olevan varaston seurannan ja antaa tällä tavoin yleisen näkymän varaston näkyvyyteen.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="bcfc4-105">Kaikki käytettävissä olevaan varastoon liittyvät tiedot viedään palveluun lähes reaaliaikaisesti käyttämällä matala-asteista SQL-integraatiota.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="bcfc4-106">Ulkoiset palvelut käyttävät palvelut tekevät RESTful API -ohjelmointirajapinnoilla käytettävissä olevien tietojen kyselyjä annetuissa dimensioissa ja saavat tällä tavoin luettelon käytettävissä olevista paikoista.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="bcfc4-107">Varaston näkyvyys on Microsoft Dataverseen perustuva mikropalvelu, joten sitä voi laajentaa muodostamalla Power Apps -sovelluksia ja käyttämällä Power BI:ta tuottamaan liiketoiminnan tarpeita vastaavia mukautettuja toimintoja.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="bcfc4-108">Indeksi voidaan lisäksi päivittää tekemään varastokyselyjä.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="bcfc4-109">Varaston näkyvyydessä on määritysvaihtoehtoja, joiden avulla sen voi integroida useiden kolmannen osapuolen järjestelmien kanssa.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="bcfc4-110">Se tukee standardoitua varastodimensiota, mukautettua laajennettavuutta ja standardoituja, määritettäviä laskettuja määriä.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="bcfc4-111">Tässä aiheessa käsitellään Dynamics 365 Supply Chain Managementin varaston näkyvyyden apuohjelman asentamista ja määrittämistä sekä sen ohjelmointirajapinnan käyttöä.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="bcfc4-112">Varaston näkyvyyden lisäapuohjelman asentaminen</span><span class="sxs-lookup"><span data-stu-id="bcfc4-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="bcfc4-113">Varaston näkyvyyden lisäapuohjelman asentamiseen on käytettävä Microsoft Dynamics Lifecycle Servicesiä (LCS).</span><span class="sxs-lookup"><span data-stu-id="bcfc4-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="bcfc4-114">LCS on yhteistyöportaali, jonka muodostamassa ympäristössä ja jonka säännöllisesti päivitetyillä palveluilla voi hallita Dynamics 365 Finance and Operations -sovellusten elinkaarta.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="bcfc4-115">Lisätietoja on kohdassa [Lifecycle Services -resurssit](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="bcfc4-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="bcfc4-116">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="bcfc4-116">Prerequisites</span></span>

<span data-ttu-id="bcfc4-117">Ennen varaston näkyvyyden apuohjelman asentamista:</span><span class="sxs-lookup"><span data-stu-id="bcfc4-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="bcfc4-118">Hanki LCS-toteutusprojekti, jossa on otettu käyttöön vähintään yksi ympäristö.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="bcfc4-119">Luo tarjoomalle beeta-avaimet LCS:ssa.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-119">Generate the beta keys for your offering in LCS.</span></span>
- <span data-ttu-id="bcfc4-120">Ota tarjooman beeta-avaimet käyttöön käyttäjälle LCS:ssa.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-120">Enable the beta keys for your offering for your user in LCS.</span></span>
- <span data-ttu-id="bcfc4-121">Ota yhteys Microsoftin varaston näkyvyyden tuotetiimiin and ympäristötunnus, jossa haluat ottaa varaston näkyvyyden apuohjelman käyttöön.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-121">Contact the Microsoft Inventory Visibility product team and provide an environment ID where you want to deploy the Inventory Visibility Add-in.</span></span>

<span data-ttu-id="bcfc4-122">Jos sinulla on näitä edellytyksiä koskevia kysymyksiä, ota yhteys varaston näkyvyyden tuotetiimiin.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-122">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="bcfc4-123">Lisäosan asentaminen</span><span class="sxs-lookup"><span data-stu-id="bcfc4-123">Install the add-in</span></span>

<span data-ttu-id="bcfc4-124">Varaston näkyvyyden apuohjelman asentaminen:</span><span class="sxs-lookup"><span data-stu-id="bcfc4-124">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="bcfc4-125">Kirjaudu [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) -portaaliin.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-125">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="bcfc4-126">Valitse aloitussivulla projekti, jossa ympäristö on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-126">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="bcfc4-127">Valitse projektisivulla ympäristö, johon haluat asentaa apuohjelman.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-127">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="bcfc4-128">Vieritä ympäristösivulla **Ympäristöapuohjelmat** -osaan.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-128">On the environment page, scroll down until you see the **Environment add-ins** section.</span></span> <span data-ttu-id="bcfc4-129">Jos osa ei ole näkyvissä, varmista, että edellytyksissä mainitut beeta-avaimet on käsitelty kokonaisuudessaan.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-129">If the section isn't visible, make sure the prerequisite beta keys have been fully processed.</span></span>
1. <span data-ttu-id="bcfc4-130">Valitse **Ympäristöapuohjelmat**-osassa **Asenna uusi apuohjelma**.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-130">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
    <span data-ttu-id="bcfc4-131">![Ympäristösivu LCS:ssa](media/inventory-visibility-environment.png "Ympäristösivu LCS:ssa")</span><span class="sxs-lookup"><span data-stu-id="bcfc4-131">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>
1. <span data-ttu-id="bcfc4-132">Valitse **Asenna uusi apuohjelma** -linkki.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-132">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="bcfc4-133">Käytettävissä olevien apuohjelmien luettelo avautuu.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-133">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="bcfc4-134">Valitse luettelossa **Varastopalvelu**.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-134">Select **Inventory service** from the list.</span></span> <span data-ttu-id="bcfc4-135">(Huomaa, että sen nimi voi olla nyt **Dynamics 365 Supply Chain Managementin varaston näkyvyyden apuohjelma**.)</span><span class="sxs-lookup"><span data-stu-id="bcfc4-135">(Note, this may now be listed as **Inventory Visibility Add-in for Dynamics 365 Supply Chain Management**.)</span></span>
1. <span data-ttu-id="bcfc4-136">Anna arvot seuraavissa ympäristön kentissä:</span><span class="sxs-lookup"><span data-stu-id="bcfc4-136">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="bcfc4-137">**AAD-sovelluksen tunnus**</span><span class="sxs-lookup"><span data-stu-id="bcfc4-137">**AAD application ID**</span></span>
    - <span data-ttu-id="bcfc4-138">**AAD-vuokraajan tunnus**</span><span class="sxs-lookup"><span data-stu-id="bcfc4-138">**AAD tenant ID**</span></span>

    <span data-ttu-id="bcfc4-139">![Apuohjelman määrityssivu](media/inventory-visibility-setup.png "Apuohjelman määrityssivu")</span><span class="sxs-lookup"><span data-stu-id="bcfc4-139">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="bcfc4-140">Hyväksy käyttöehdot valitsemalla **Käyttöehdot**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-140">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="bcfc4-141">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-141">Select **Install**.</span></span> <span data-ttu-id="bcfc4-142">Apuohjelman tilana näkyy nyt **Asennetaan**.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-142">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="bcfc4-143">Se on valmis, päivitä sivu, jonka jälkeen tilana on **Asennettu**.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-143">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="get-a-security-service-token"></a><span data-ttu-id="bcfc4-144">Palvelun suojaustunnuksen hankkiminen</span><span class="sxs-lookup"><span data-stu-id="bcfc4-144">Get a security service token</span></span>

<span data-ttu-id="bcfc4-145">Palvelun suojaustunnus haetaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="bcfc4-145">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="bcfc4-146">Kirjaudu Azure-portaaliin ja etsi sen avulla Supply Chain Management -sovelluksen `clientId` ja `clientSecret`.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-146">Sign in to Azure Portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="bcfc4-147">Nouda Azure Active Directory -tunnus (`aadToken`) lähettämällä HTTP-pyyntö, jossa on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="bcfc4-147">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="bcfc4-148">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="bcfc4-148">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="bcfc4-149">**Tapa** - `GET`</span><span class="sxs-lookup"><span data-stu-id="bcfc4-149">**Method** - `GET`</span></span>
    - <span data-ttu-id="bcfc4-150">**Tekstisisältö (lomaketiedot)**:</span><span class="sxs-lookup"><span data-stu-id="bcfc4-150">**Body content (form data)**:</span></span>

        | <span data-ttu-id="bcfc4-151">avain</span><span class="sxs-lookup"><span data-stu-id="bcfc4-151">key</span></span> | <span data-ttu-id="bcfc4-152">arvo</span><span class="sxs-lookup"><span data-stu-id="bcfc4-152">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="bcfc4-153">client_id</span><span class="sxs-lookup"><span data-stu-id="bcfc4-153">client_id</span></span> | <span data-ttu-id="bcfc4-154">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="bcfc4-154">${aadAppId}</span></span> |
        | <span data-ttu-id="bcfc4-155">client_secret</span><span class="sxs-lookup"><span data-stu-id="bcfc4-155">client_secret</span></span> | <span data-ttu-id="bcfc4-156">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="bcfc4-156">${aadAppSecret}</span></span> |
        | <span data-ttu-id="bcfc4-157">grant_type</span><span class="sxs-lookup"><span data-stu-id="bcfc4-157">grant_type</span></span> | <span data-ttu-id="bcfc4-158">client_credentials</span><span class="sxs-lookup"><span data-stu-id="bcfc4-158">client_credentials</span></span> |
        | <span data-ttu-id="bcfc4-159">resurssi</span><span class="sxs-lookup"><span data-stu-id="bcfc4-159">resource</span></span> | <span data-ttu-id="bcfc4-160">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="bcfc4-160">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="bcfc4-161">Vastauksena pitäisi olla `aadToken` , joka muistuttaa seuraavaa esimerkkiä.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-161">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="bcfc4-162">Muodosta seuraavankaltainen JSON-pyyntö:</span><span class="sxs-lookup"><span data-stu-id="bcfc4-162">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="bcfc4-163">Jossa:</span><span class="sxs-lookup"><span data-stu-id="bcfc4-163">Where:</span></span>
    - <span data-ttu-id="bcfc4-164">`client_assertion`-arvon on oltava edellisessä vaiheessa vastaanotettu `aadToken`.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-164">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="bcfc4-165">`context`-arvon on oltava ympäristötunnus, jossa apuohjelma halutaan ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-165">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="bcfc4-166">Kaikki muut arvot määritetään samoiksi kuin esimerkissä.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-166">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="bcfc4-167">Lähetä HTTP-pyyntö, jossa on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="bcfc4-167">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="bcfc4-168">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="bcfc4-168">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="bcfc4-169">**Tapa** - `POST`</span><span class="sxs-lookup"><span data-stu-id="bcfc4-169">**Method** - `POST`</span></span>
    - <span data-ttu-id="bcfc4-170">**HTTP-otsikko** - sisällytä ohjelmointirajapinnan versio (avain on `Api-Version` ja arvo `1.0`)</span><span class="sxs-lookup"><span data-stu-id="bcfc4-170">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="bcfc4-171">**Tekstisisältö** - sisällytä edellisessä vaiheessa luotu JSON-pyyntö.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-171">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="bcfc4-172">`access_token` saadaan vastauksessa.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-172">You will get an `access_token` in response.</span></span> <span data-ttu-id="bcfc4-173">Sitä tarvitaan haltijatunnuksena, jolla varastoin näkyvyyden ohjelmointirajapintaa kutsutaan.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-173">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="bcfc4-174">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="bcfc4-174">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a><span data-ttu-id="bcfc4-175">Lisäosan asennuksen poistaminen</span><span class="sxs-lookup"><span data-stu-id="bcfc4-175">Uninstall the add-in</span></span>

<span data-ttu-id="bcfc4-176">Poista apuohjelman asennus valitsemalla **Poista asennus**.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-176">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="bcfc4-177">Päivitä LCS, ja varaston näkyvyyden apuohjelma poistetaan.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-177">Refresh LCS and the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="bcfc4-178">Asennuksen poistoprosessi poistaa apuohjelman rekisteröinnin sekä käynnistää kaikkien palveluun tallennettujen liiketoimintatietojen puhdistustyön.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-178">The uninstall process will remove the add-in registration and also start a job to clean up all of the business data stored in the service.</span></span>

## <a name="inventory-visibility-add-in-public-api"></a><span data-ttu-id="bcfc4-179">Varaston näkyvyyden apuohjelman julkinen ohjelmointirajapinta</span><span class="sxs-lookup"><span data-stu-id="bcfc4-179">Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="bcfc4-180">Varaston näkyvyyden apuohjelman julkinen REST API sisältää useita nimenomaisia integroinnin päätepisteitä.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-180">The public REST API of the of the Inventory Visibility Add-in presents several specific endpoints of integration.</span></span> <span data-ttu-id="bcfc4-181">Se tukee kolmea pääasiallista vuorovaikutustyyppiä:</span><span class="sxs-lookup"><span data-stu-id="bcfc4-181">It supports three main interaction types:</span></span>

- <span data-ttu-id="bcfc4-182">Varastosaldon määrän muutosten kirjaaminen apuohjelmaan ulkoisesta järjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-182">Posting on-hand changes to the add-in from an external system.</span></span>
- <span data-ttu-id="bcfc4-183">Nykyisten käytettävissä olevien määrien kysely ulkoisesta järjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-183">Querying current on-hand quantities from an external system.</span></span>
- <span data-ttu-id="bcfc4-184">Automaattinen synkronointi Supply Chain Managementin käytettävissä olevan varaston kanssa.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-184">Automatic synchronization with Supply Chain Management on-hand.</span></span>

<span data-ttu-id="bcfc4-185">Automaattinen synkronointi ei sisälly julkiseen ohjelmointirajapintaan, vaan se käsitellään taustalla ympäristöissä, joissa varaston näkyvyyden apuohjelma on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-185">The automatic synchronization isn't part of the public API but is instead handled in the background for environments that have enabled the Inventory Visibility Add-in.</span></span>

### <a name="authentication"></a><span data-ttu-id="bcfc4-186">Todennus</span><span class="sxs-lookup"><span data-stu-id="bcfc4-186">Authentication</span></span>

<span data-ttu-id="bcfc4-187">Ympäristön suojaustunnusta käytetään varaston näkyvyyden apuohjelman kutsumiseen, joten Azure Active Directory -tunnus on luotava Azure Active Directory -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-187">The platform security token is used to call the Inventory Visibility Add-in, so you must generate an Azure Active Directory token using your Azure Active Directory application.</span></span>

<span data-ttu-id="bcfc4-188">Lisätietoja suojaustunnuksen hakemista on kohdassa [Varaston näkyvyyden apuohjelman asentaminen](#install-add-in).</span><span class="sxs-lookup"><span data-stu-id="bcfc4-188">For more information about how to get the security token, see [Install the Inventory Visibility Add-in](#install-add-in).</span></span>

### <a name="configure-the-inventory-visibility-api"></a><span data-ttu-id="bcfc4-189">Varaston näkyvyyden ohjelmointirajapinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bcfc4-189">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="bcfc4-190">Ennen palvelun käyttöä on tehtävä valmiiksi seuraavissa aliosissa käsiteltävät määritykset.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-190">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="bcfc4-191">Määritykset voivat vaihdella ympäristön tietojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-191">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="bcfc4-192">Siinä pääasiallisesti neljä osaa:</span><span class="sxs-lookup"><span data-stu-id="bcfc4-192">It primarily includes four parts:</span></span>

- [<span data-ttu-id="bcfc4-193">Osiointi</span><span class="sxs-lookup"><span data-stu-id="bcfc4-193">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="bcfc4-194">Dimensiomääritykset</span><span class="sxs-lookup"><span data-stu-id="bcfc4-194">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="bcfc4-195">Indeksointi</span><span class="sxs-lookup"><span data-stu-id="bcfc4-195">Indexing</span></span>](#indexing)
- [<span data-ttu-id="bcfc4-196">Mukautettu mitta</span><span class="sxs-lookup"><span data-stu-id="bcfc4-196">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="bcfc4-197">Osiointi</span><span class="sxs-lookup"><span data-stu-id="bcfc4-197">Partitioning</span></span>

<span data-ttu-id="bcfc4-198">Osiointi voi vaikuttaa merkittävästi varaston näkyvyyden ohjelmointirajapinnan toimintaan.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-198">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="bcfc4-199">Niinpä kannattaakin määrittää rakenne, jossa voidaan ryhmitellä tietoja pienissä osissa siten, että merkitykselliset tietokyselyt ovat mahdollisia.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-199">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="bcfc4-200">`organizationId` (Supply Chain Managementissa `dataAreaId`) sisältyy aina osiointiin, ja varaston näkyvyys osioidaan oletusarvoisesti dimensioiden perusteella, kuten *Toimipaikka + sijainti*.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-200">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="bcfc4-201">Tämän vuoksi palveluissa tehtävissä kyselyissä on aina käytettävä suodattimissa määritettyjä dimensioita.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-201">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="bcfc4-202">*Toimipaikka* ja *sijainti* ovat kaksi varaston näkyvyyden yleistä oletusdimensiota.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-202">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="bcfc4-203">Supply Chain Managementin näiden dimensioiden nimet ovat *toimipaikka* (`InventSiteId`) ja *varasto* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="bcfc4-203">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="bcfc4-204">Dimensiomääritykset</span><span class="sxs-lookup"><span data-stu-id="bcfc4-204">Dimension configurations</span></span>

<span data-ttu-id="bcfc4-205">Varaston näkyvyyden yleisten oletusdimensioiden luettelon ansiosta usein lähdejärjestelmien integrointi on mahdollista.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-205">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="bcfc4-206">Seuraavassa taulukossa on varastodimensiot, jotka tulevat varaston näkyvyyden oletusdimensionimiksi.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-206">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="bcfc4-207">Dimensiotyyppi</span><span class="sxs-lookup"><span data-stu-id="bcfc4-207">Dimension type</span></span> | <span data-ttu-id="bcfc4-208">Dimension nimi</span><span class="sxs-lookup"><span data-stu-id="bcfc4-208">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="bcfc4-209">Tuote</span><span class="sxs-lookup"><span data-stu-id="bcfc4-209">Product</span></span> | `ColorId` |
| <span data-ttu-id="bcfc4-210">Tuote</span><span class="sxs-lookup"><span data-stu-id="bcfc4-210">Product</span></span> | `SizeId` |
| <span data-ttu-id="bcfc4-211">Tuote</span><span class="sxs-lookup"><span data-stu-id="bcfc4-211">Product</span></span> | `StyleId` |
| <span data-ttu-id="bcfc4-212">Tuote</span><span class="sxs-lookup"><span data-stu-id="bcfc4-212">Product</span></span> | `ConfigId` |
| <span data-ttu-id="bcfc4-213">Seuranta</span><span class="sxs-lookup"><span data-stu-id="bcfc4-213">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="bcfc4-214">Seuranta</span><span class="sxs-lookup"><span data-stu-id="bcfc4-214">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="bcfc4-215">Toimipaikka</span><span class="sxs-lookup"><span data-stu-id="bcfc4-215">Location</span></span> | `LocationId` |
| <span data-ttu-id="bcfc4-216">Toimipaikka</span><span class="sxs-lookup"><span data-stu-id="bcfc4-216">Location</span></span> | `SiteId` |
| <span data-ttu-id="bcfc4-217">Varaston tila</span><span class="sxs-lookup"><span data-stu-id="bcfc4-217">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="bcfc4-218">Varastokohtainen</span><span class="sxs-lookup"><span data-stu-id="bcfc4-218">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="bcfc4-219">Varastokohtainen</span><span class="sxs-lookup"><span data-stu-id="bcfc4-219">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="bcfc4-220">Varastokohtainen</span><span class="sxs-lookup"><span data-stu-id="bcfc4-220">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="bcfc4-221">Edellisessä taulukossa mainittu dimensiotyyppi on tarkoitettu vain tiedoksi.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-221">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="bcfc4-222">Dimensiotyyppiä ei tarvitse määrittää varaston näkyvyydessä.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-222">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="bcfc4-223">Jos mukautettu dimensio on luotu ja sen on siirryttävä oletusarvoon, kun varaston näkyvyys käyttää sitä, **mukautetun dimension** nimi voidaan määrittää varaston näkyvyydessä.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-223">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="bcfc4-224">Ulkoiset järjestelmät käyttävät varaston näkyvyyttä RESTful API -ohjelmointirajapinnoilla, jotka ottavat käytettävissä olevat tiedot käyttöön annetuissa dimensiojoukoissa, joissa kyselyt tehdään.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-224">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="bcfc4-225">Integroinnin osalta varaston näkyvyydessä voidaan määrittää *ulkoinen kanavan tietolähde* ja *kohdedimensioiden* lähdedimensio varaston näkyvyydessä.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-225">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="bcfc4-226">Kohdedimensioiden on oltava jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="bcfc4-226">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="bcfc4-227">Varaston näkyvyyden oletusdimensiot</span><span class="sxs-lookup"><span data-stu-id="bcfc4-227">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="bcfc4-228">Mukautetut dimensiot</span><span class="sxs-lookup"><span data-stu-id="bcfc4-228">Custom dimensions</span></span>

<span data-ttu-id="bcfc4-229">Dimensiomääritysten tarkoitus on standardoida monen järjestelmän integrointi dimensiokyselyitä ja tapahtuman dimensioihin kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-229">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="bcfc4-230">Indeksointi</span><span class="sxs-lookup"><span data-stu-id="bcfc4-230">Indexing</span></span>

<span data-ttu-id="bcfc4-231">Käytettävissä olevan varaston kysely ei ole useimmiten korkeimmalla kokonaistasolla, vaan tulokset halutaan ehkä nähdä varastodimensioiden mukaan koostettuina.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-231">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="bcfc4-232">Varaston näkyvyys on joustava, sillä siinä voidaan määrittää dimensioon tai dimensioyhdistelmiin perustuvia indeksejä.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-232">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="bcfc4-233">Tällä hetkellä indeksejä voi määrittään enintään viisi.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-233">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="bcfc4-234">Käytettävää dimensiota tai dimensioyhdistelmää on harkittava huolellisesti ennen toteutusta, sillä näin voidaan varmistaa, että se todella vastaa liiketoiminnan tarpeita.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-234">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="bcfc4-235">Tuotekysely voidaan haluta tehdä esimerkiksi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="bcfc4-235">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="bcfc4-236">Kyselynä käytettävissä oleva koostetuote *väri*- ja *koko*-dimension mukaan.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-236">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="bcfc4-237">Joissakin tapauksissa kyselyn kohteena voi olla tuote kokonaisuudessaan.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-237">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="bcfc4-238">Kaksi indeksiä määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="bcfc4-238">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="bcfc4-239">Tyhjä hakasulje tekee koosteen osiossa olevan tuotetunnuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-239">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="bcfc4-240">Indeksointi määrittää, miten tulokset ryhmitellään `groupBy`-kyselyasetuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-240">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="bcfc4-241">Jos tässä tapauksessa ei määritetä `groupBy`-arvoja, tuloksena on `productid`-kohtainen kokonaismäärä.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-241">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="bcfc4-242">Jos `groupBy`-määrityksenä on sen sijaan `groupBy=ColorId&groupBy=SizeId`, tuloksena on useita rivejä, jotka perustuvat järjestelmässä oleviin väri- ja kokoyhdistelmiin.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-242">Otherwise if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="bcfc4-243">Kyselyehdot voidaan asettaa pyynnön tekstiosaan.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-243">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="bcfc4-244">Seuraavassa esimerkissä on väri- ja kokoyhdistelmää käyttävä tuotekysely.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-244">Here is a sample query on the product with color and size combination.</span></span>

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

#### <a name="custom-measurement"></a><span data-ttu-id="bcfc4-245">Mukautettu mitta</span><span class="sxs-lookup"><span data-stu-id="bcfc4-245">Custom measurement</span></span>

<span data-ttu-id="bcfc4-246">Vaikka oletusarvoiset mittamäärät linkitetään Supply Chain Managementiin, myös oletusmittamäärien yhdistelmistä koostuva määrä on mahdollinen.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-246">The default measurement quantities are linked to Supply Chain Management, however you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="bcfc4-247">Sitä varten on määritettävä mukautettuja määritä, jotka lisätään käytettävissä olevan määrän tulosteisiin.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-247">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="bcfc4-248">Toiminnon antaa yksinkertaisesti mahdollisuuden määrittää lisättävän ja/tai vähennettävän mittajoukon, joiden avulla voidaan muodostaa mukautettu mitta.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-248">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="bcfc4-249">Esimerkiksi seuraavalla kyselyehdolla määritetään mukautetun mitan määräksi `MyCustomAvailableforReservation`, jonka kulutusjärjestelmä käyttää.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-249">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="bcfc4-250">Kulutusjärjestelmä</span><span class="sxs-lookup"><span data-stu-id="bcfc4-250">Consumption system</span></span> | <span data-ttu-id="bcfc4-251">Lasketut mitat</span><span class="sxs-lookup"><span data-stu-id="bcfc4-251">Calculated measurers</span></span> | <span data-ttu-id="bcfc4-252">Tietolähde</span><span class="sxs-lookup"><span data-stu-id="bcfc4-252">Data source</span></span> | <span data-ttu-id="bcfc4-253">Määre</span><span class="sxs-lookup"><span data-stu-id="bcfc4-253">Modifier</span></span> | <span data-ttu-id="bcfc4-254">Määreen laskentatyyppi</span><span class="sxs-lookup"><span data-stu-id="bcfc4-254">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="bcfc4-255">Lisäys</span><span class="sxs-lookup"><span data-stu-id="bcfc4-255">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="bcfc4-256">Lisäys</span><span class="sxs-lookup"><span data-stu-id="bcfc4-256">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="bcfc4-257">Vähennyslasku</span><span class="sxs-lookup"><span data-stu-id="bcfc4-257">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="bcfc4-258">Lisäys</span><span class="sxs-lookup"><span data-stu-id="bcfc4-258">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="bcfc4-259">Vähennyslasku</span><span class="sxs-lookup"><span data-stu-id="bcfc4-259">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="bcfc4-260">Lisäys</span><span class="sxs-lookup"><span data-stu-id="bcfc4-260">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="bcfc4-261">Lisäys</span><span class="sxs-lookup"><span data-stu-id="bcfc4-261">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="bcfc4-262">Vähennyslasku</span><span class="sxs-lookup"><span data-stu-id="bcfc4-262">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="bcfc4-263">Vähennyslasku</span><span class="sxs-lookup"><span data-stu-id="bcfc4-263">Subtraction</span></span> |

<span data-ttu-id="bcfc4-264">Mukautetun mittamäärän kysely palauttaa sitten seuraavan tuloksen.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-264">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="bcfc4-265">`MyCustomAvailableforReservation`-tulos perustuu seuraavaan mukautettujen mittojen laskenta-asetukseen:</span><span class="sxs-lookup"><span data-stu-id="bcfc4-265">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="bcfc4-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="bcfc4-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="bcfc4-267">Varastosaldon muutosten kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="bcfc4-267">Posting on-hand changes</span></span>

<span data-ttu-id="bcfc4-268">Tarkka URL-osoite, johon tapahtuma kirjataan, määräytyy maantieteellisen alueen mukaan.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-268">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="bcfc4-269">Sen muoto on seuraava:</span><span class="sxs-lookup"><span data-stu-id="bcfc4-269">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="bcfc4-270">Tätä URL-osoitetta käytetään todennuksessa HTTP `POST` -menetelmän ohella lähettämään varastosaldon muutostapahtumat palveluun.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-270">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="bcfc4-271">Dynamics 365 -palvelun kanssa HTTP-pyyntöjen avulla tapahtuvassa viestinnässä käytetään erityisotsikko, joka ilmaisee sen Supply Chain Management -esiintymän ympäristötunnuksen, johon tiedot on linkitetty.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-271">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="bcfc4-272">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="bcfc4-272">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="bcfc4-273">Varastosaldon muutosten kirjaamisen kyselyesimerkki 1</span><span class="sxs-lookup"><span data-stu-id="bcfc4-273">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="bcfc4-274">Tässä esimerkissä on skenaario, jossa dimensiomääritys määritetään Power Appsissa.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-274">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="bcfc4-275">Määritä dimension yhdistämismääritys Power Appsissa käyttämällä seuraavaa kyselyä:</span><span class="sxs-lookup"><span data-stu-id="bcfc4-275">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="bcfc4-276">Voit nyt tehdä `dimensionDataSource`-määrityksen ja käyttää mukautettuja dimensioita kyselyissä.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-276">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="bcfc4-277">Järjestelmä muuntaa mukautetut dimensiot automaattisesti perusdimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-277">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="bcfc4-278">Varastosaldon muutosten kirjaamisen kyselyesimerkki 2</span><span class="sxs-lookup"><span data-stu-id="bcfc4-278">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="bcfc4-279">Tässä esimerkissä on skenaario, jossa yhtään dimensiomäärityksen yhdistämismääritystä ei määritetä Power Appsissa, joten myös kirjaamisessa on käytettävä perusdimensioita.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-279">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="bcfc4-280">Kaikkien dimensioiden on oltava perusdimensioita, kun `dimensionDataSource`-kentässä on tyhjäarvo, se on tyhjä tai siinä on välilyönti.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-280">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="bcfc4-281">JSON-tiedostokentän ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="bcfc4-281">JSON document field properties</span></span>

<span data-ttu-id="bcfc4-282">Aiemmin käsitellyissä JSON-kyselyesimerkkien kentissä oli seuraavassa taulukossa olevia ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-282">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="bcfc4-283">Kentän tunnus</span><span class="sxs-lookup"><span data-stu-id="bcfc4-283">Field ID</span></span> | <span data-ttu-id="bcfc4-284">kuvaus</span><span class="sxs-lookup"><span data-stu-id="bcfc4-284">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="bcfc4-285">Tietyn muutostapahtuman yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-285">A unique ID for the specific change event.</span></span> <span data-ttu-id="bcfc4-286">Tämän tunnuksen avulla varmistetaan, että jos viestintä palveluun epäonnistuu kirjauksen aikana, tapahtuman lähettäminen uudelleen ei aiheuta saman tapahtuman laskemista kahdesti järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-286">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="bcfc4-287">Tapahtumaan linkitetyn organisaation tunnus.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-287">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="bcfc4-288">Tämä yhdistetään Supply Chain Management -organisaatioihin tai tietoalueen tunnuksiin.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-288">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="bcfc4-289">Kyseisen tuotteen tunniste.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-289">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="bcfc4-290">Määrä, jolla varastosaldoa on muutettava.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-290">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="bcfc4-291">Jos hyllylle esimerkiksi lisättiin 10 uutta sämpylää, tämä arvo 10.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-291">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="bcfc4-292">Jos 3 sämpylää sitten poistettiin hyllystä tai myyntiin, tämä arvo on -3.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-292">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="bcfc4-293">Muutostapahtuman kirjauksessa ja kyselyssä käytettävien dimensioiden tietolähde.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-293">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="bcfc4-294">Jos tietolähde määritetään, määritetyn tietolähteen mukautettuja dimensioita voidaan käyttää.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-294">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="bcfc4-295">Dimensiomääritysten ansiosta varaston näkyvyys voi yhdistää mukautetut dimensiot yleisiin oletusdimensioihin.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-295">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="bcfc4-296">Jos `dimensionDataSource` ei ole määritetty, kyselyissä voi käyttää vain yleisiä oletusdimensioita.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-296">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="bcfc4-297">Dynaaminen avain- ja arvoparisäilö.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-297">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="bcfc4-298">Ne yhdistetään joihinkin Supply Chain Managementin dimensioihin, minkä lisäksi voidaan lisätä mukautettuja dimensioita (kuten *Lähde*), jotka voivat ilmaista, saapuuko tapahtuma Supply Chain Managementista vai ulkoisesta järjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-298">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="bcfc4-299">Kyselyt nykyisessä varastosaldossa</span><span class="sxs-lookup"><span data-stu-id="bcfc4-299">Querying current on-hand</span></span>

<span data-ttu-id="bcfc4-300">Nykyisen varastosaldon kyselyjen päätepisteessä on samankaltainen URL-osoite:</span><span class="sxs-lookup"><span data-stu-id="bcfc4-300">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="bcfc4-301">Kysely siinä tehdään HTTP `POST` -menetelmällä.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-301">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="bcfc4-302">Nykyisen varastosaldon kyselyesimerkki 1</span><span class="sxs-lookup"><span data-stu-id="bcfc4-302">Current on-hand query example 1</span></span>

<span data-ttu-id="bcfc4-303">Tässä esimerkissä on skenaario, jossa Power Appsissa on jo valmis dimensiomääritys.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-303">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="bcfc4-304">Määritä dimension yhdistämismääritys Power Appsissa käyttämällä seuraavaa kyselyä:</span><span class="sxs-lookup"><span data-stu-id="bcfc4-304">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="bcfc4-305">Voit nyt tehdä `dimensionDataSource`-määrityksen ja käyttää mukautettuja dimensioita kyselyissä.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-305">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="bcfc4-306">Järjestelmä muuntaa mukautetut dimensiot automaattisesti perusdimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-306">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="bcfc4-307">`DimensionDataSource` voidaan määrittää `filters`-kohdassa ja mukautetut dimensiot vodaan määrittää sekä `filters`- että `groupByValues`-kohdissa.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-307">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="bcfc4-308">Järjestelmä muuntaa mukautetut dimensiot automaattisesti perusdimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-308">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="bcfc4-309">Nykyisen varastosaldon kyselyesimerkki 2</span><span class="sxs-lookup"><span data-stu-id="bcfc4-309">Current on-hand query example 2</span></span>

<span data-ttu-id="bcfc4-310">Tässä esimerkissä on skenaario, jossa yhtään dimensiomäärityksen yhdistämismääritystä ei määritetä Power Appsissa, joten myös kirjaamisessa on käytettävä perusdimensioita.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-310">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="bcfc4-311">Kaikkien dimensioiden on oltava perusdimensioita, kun `filters`-kohdan `dimensionDataSource`-kentässä on tyhjäarvo, se on tyhjä tai siinä on välilyönti.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-311">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="bcfc4-312">Palautetun tuloksen esimerkki</span><span class="sxs-lookup"><span data-stu-id="bcfc4-312">Example return result</span></span>

<span data-ttu-id="bcfc4-313">Edellisten esimerkkien kyselyissä voitiin palauttaa seuraavankaltainen tulos.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-313">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="bcfc4-314">Huomaa, että määräkentät on jäsennelty mittahakemistoksi ja niihin liittyviksi arvoiksi.</span><span class="sxs-lookup"><span data-stu-id="bcfc4-314">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>
