---
title: Common Data Service -virtuaaliyksiköiden määrittäminen
description: Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin virtuaaliyksiköiden määrittämistä. Virtuaaliyksiköiden luominen ja aiemmin luotujen päivittäminen sekä luotujen ja käytettävissä olevien yksiköiden analysoiminen.
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0848b7556100fba38fcab0aa2a1a109e2e055fc9
ms.sourcegitcommit: b89baab13e530b5b1f079231619c628309a4742d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/05/2020
ms.locfileid: "3959572"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="10141-104">Common Data Service -virtuaaliyksiköiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="10141-104">Configure Common Data Service virtual entities</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="10141-105">Dynamics 365 Human Resources on Common Data Servicen virtuaalinen tietolähde.</span><span class="sxs-lookup"><span data-stu-id="10141-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="10141-106">Se sisältää Common Data Servicen ja Microsoft Power Platformin täydet CRUD (luonti, luku, päivitys ja poisto) -toiminnot.</span><span class="sxs-lookup"><span data-stu-id="10141-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="10141-107">Virtuaaliyksiköiden tietoja ei tallenneta Common Data Serviceen vaan sovelluksen tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="10141-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="10141-108">Jos haluat ottaa Common Data Servicen Human Resources -yksiköiden CRUD-toiminnot käyttää, yksiköiden on oltava käytettävissä virtuaaliyksikköinä Common Data Servicessa.</span><span class="sxs-lookup"><span data-stu-id="10141-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="10141-109">Voit suorittaa tällä tavoin Common Data Servicen ja Microsoft Power Platformin CRUD-toimintoja Human Resourcesin tiedoissa.</span><span class="sxs-lookup"><span data-stu-id="10141-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="10141-110">Toiminnot tukevat myös Human Resourcesin liiketoimintalogiikan tarkistuksia, joilla varmistetaan tietojen eheys kirjoitettaessa tietoja yksiköihin.</span><span class="sxs-lookup"><span data-stu-id="10141-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="10141-111">Human Resourcesin käytettävissä olevat virtuaaliyksiköt</span><span class="sxs-lookup"><span data-stu-id="10141-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="10141-112">Kaikki Human Resourcesin OData (Open Data Protocol) -yksiköt ovat käytettävissä virtuaaliyksikköinä Common Data Servicessa.</span><span class="sxs-lookup"><span data-stu-id="10141-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="10141-113">Ne ovat käytettävissä myös Power Platformissa.</span><span class="sxs-lookup"><span data-stu-id="10141-113">They're also available in Power Platform.</span></span> <span data-ttu-id="10141-114">Voit nyt muodostaa sovelluksia ja kokemuksia käyttämällä tietoja suoraan Human Resourcesissa CRUD-ominaisuuksien avulla ilman, että tiedot kopioitava ja synkronoitava Common Data Serviceen.</span><span class="sxs-lookup"><span data-stu-id="10141-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="10141-115">Voit muodostaa Power Apps -portaalien avulla ulkoisia sivustoja, joiden avulla voidaan toteuttaa liiketoimintaprosessien yhteistyöskenaarioita Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="10141-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="10141-116">Voit tarkastella ympäristössä käyttöönotettujen virtuaaliyksiköiden luetteloa ja aloittaa [Power Appsin](https://make.powerapps.com) yksiköiden käyttämisen **Dynamics 365 HR -virtuaaliyksiköiden** ratkaisussa.</span><span class="sxs-lookup"><span data-stu-id="10141-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Dynamics 365 HR -virtuaaliyksiköt Power Appsissa](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="10141-118">Virtuaaliyksiköiden ja tavallisten yksiköiden vertailu</span><span class="sxs-lookup"><span data-stu-id="10141-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="10141-119">Human Resourcesin virtuaaliyksiköt eivät ole samoja kuin Human Resourcesin luodut Common Data Servicen yksiköt.</span><span class="sxs-lookup"><span data-stu-id="10141-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="10141-120">Human Resourcesin tavalliset yksiköt luodaan erikseen ja niitä ylläpidetään HCM Common -ratkaisussa Common Data Servicessa.</span><span class="sxs-lookup"><span data-stu-id="10141-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="10141-121">Tavallisissa yksiköissä tiedot tallennetaan Common Data Servicessa, ja ne on synkronoitava Human Resourcesin sovellustietokannassa.</span><span class="sxs-lookup"><span data-stu-id="10141-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="10141-122">Tavallisten Human Resourcesin Common Data Service -yksiköiden luettelo on kohdassa [Common Data Service -yksiköt](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="10141-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="10141-123">Luo perustiedot</span><span class="sxs-lookup"><span data-stu-id="10141-123">Setup</span></span>

<span data-ttu-id="10141-124">Ota virtuaaliyksiköt käyttöön ympäristössä tekemällä seuraavat määritykset.</span><span class="sxs-lookup"><span data-stu-id="10141-124">Follow these setup steps to enable virtual entities in your environment.</span></span> 

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="10141-125">Sovelluksen rekisteröinti Microsoft Azuressa</span><span class="sxs-lookup"><span data-stu-id="10141-125">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="10141-126">Sovellus on rekisteröitävä ensin Azure-portaalissa, jotta Microsoftin käyttäjätietoympäristö voi toimittaa todennus- ja valtuutuspalvelut sovellukselle ja käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="10141-126">First, you need to register the app in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="10141-127">Lisätietoja sovellusten rekisteröinnistä Azuressa on kohdassa [Pika-aloitus: Sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristöön](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="10141-127">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="10141-128">Avaa [Microsoft Azure -portaali](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="10141-128">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="10141-129">Valitse Azure-palveluluettelossa **Sovelluksen rekisteröinnit**.</span><span class="sxs-lookup"><span data-stu-id="10141-129">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="10141-130">Valitse **Uusi rekisteröinti**.</span><span class="sxs-lookup"><span data-stu-id="10141-130">Select **New registration**.</span></span>

4. <span data-ttu-id="10141-131">Kirjoita **Nimi**-kenttään sovellusta kuvaava nimi.</span><span class="sxs-lookup"><span data-stu-id="10141-131">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="10141-132">Esimerkki: **Dynamics 365 Human Resourcesin virtuaaliyksiköt**.</span><span class="sxs-lookup"><span data-stu-id="10141-132">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="10141-133">Anna **Uudelleenohjauksen URI** -kenttään Human Resources -esiintymän nimitilan URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="10141-133">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="10141-134">Valitse **Rekisteröi**.</span><span class="sxs-lookup"><span data-stu-id="10141-134">Select **Register**.</span></span>

7. <span data-ttu-id="10141-135">Kun rekisteröinti valmistuu, Azure-portaali näyttää sovelluksen rekisteröinnin **Yleiskatsaus**-ruudussa, joka sisältää myös sen **sovelluksen (asiakasohjelman) tunnuksen**.</span><span class="sxs-lookup"><span data-stu-id="10141-135">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="10141-136">Kirjoita muistiin tämä **sovelluksen (asiakasohjelman) tunnus**.</span><span class="sxs-lookup"><span data-stu-id="10141-136">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="10141-137">Nämä tiedot annetaan, kun [määrität virtuaaliyksikön tietolähteen](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="10141-137">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="10141-138">Valitse vasemmassa siirtymisruudussa **Varmenteet ja salaiset koodit**.</span><span class="sxs-lookup"><span data-stu-id="10141-138">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="10141-139">Valitse sivun **Asiakasohjelman salasana** -osassa **Uusi asiakasohjelman salasana**.</span><span class="sxs-lookup"><span data-stu-id="10141-139">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="10141-140">Anna kuvaus, valitse kesto ja valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="10141-140">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="10141-141">Kirjaa salaisen koodin arvo muistiin.</span><span class="sxs-lookup"><span data-stu-id="10141-141">Record the secret's value.</span></span> <span data-ttu-id="10141-142">Nämä tiedot annetaan, kun [määrität virtuaaliyksikön tietolähteen](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="10141-142">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="10141-143">Muista kirjoittaa salaisen koodin arvo muistiin tässä vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="10141-143">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="10141-144">Salaista koodi ei näytetä sen jälkeen, kun poistut sivulta.</span><span class="sxs-lookup"><span data-stu-id="10141-144">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="10141-145">Dynamics 365 HR Virtual Entity -sovelluksen asentaminen</span><span class="sxs-lookup"><span data-stu-id="10141-145">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="10141-146">Asenna Dynamics 365 HR Virtual Entity -sovellus Power Apps -ympäristöön ottamaan virtuaaliyksikön ratkaisupaketti käyttöön Common Data Servicessa.</span><span class="sxs-lookup"><span data-stu-id="10141-146">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="10141-147">Avaa [Power Platform -hallintakeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="10141-147">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="10141-148">Valitse **Ympäristöt**-luettelossa Human Resources -esiintymään liitetty Power Apps -ympäristö.</span><span class="sxs-lookup"><span data-stu-id="10141-148">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="10141-149">Valitse sivun **Resurssit**-osassa **Dynamics 365 -sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="10141-149">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="10141-150">Valitse **Asenna sovellus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="10141-150">Select the **Install app** action.</span></span>

5. <span data-ttu-id="10141-151">Valitse ensin **Dynamics 365 HR Virtual Entity** ja valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="10141-151">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="10141-152">Tutustu palvelun käyttöehtoihin ja merkitse ne hyväksytyiksi.</span><span class="sxs-lookup"><span data-stu-id="10141-152">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="10141-153">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="10141-153">Select **Install**.</span></span>

<span data-ttu-id="10141-154">Asennus kestää muutaman minuutin.</span><span class="sxs-lookup"><span data-stu-id="10141-154">The install takes a few minutes.</span></span> <span data-ttu-id="10141-155">Kun asennus valmistuu, jatka seuraaviin vaiheisiin.</span><span class="sxs-lookup"><span data-stu-id="10141-155">When it completes, continue to the next steps.</span></span>

![Dynamics 365 HR Virtual Entity -sovelluksen asentaminen Power Platform -hallintakeskuksessa](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="10141-157">Virtuaaliyksikön tietolähteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="10141-157">Configure the virtual entity data source</span></span> 

<span data-ttu-id="10141-158">Seuraavaksi määritetään virtuaaliyksikön tietolähde Power Apps -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="10141-158">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="10141-159">Avaa [Power Platform -hallintakeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="10141-159">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="10141-160">Valitse **Ympäristöt**-luettelossa Human Resources -esiintymään liitetty Power Apps -ympäristö.</span><span class="sxs-lookup"><span data-stu-id="10141-160">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="10141-161">Valitse **Ympäristön URL-osoite** sivun **Tiedot**-osassa.</span><span class="sxs-lookup"><span data-stu-id="10141-161">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="10141-162">Valitse **Ratkaisun kunnon keskus** -kohdassa **Erikoishaku**-kuvake sovellussivun oikeassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="10141-162">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="10141-163">Valitse **Erikoishaku**-sivun avattavassa **Etsi**-luettelossa **Finance and Operations -virtuaalitietolähteen määritykset**.</span><span class="sxs-lookup"><span data-stu-id="10141-163">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="10141-164">Valitse **Tulokset**.</span><span class="sxs-lookup"><span data-stu-id="10141-164">Select **Results**.</span></span>

7. <span data-ttu-id="10141-165">Valitse **Microsoft HR -tietolähde** -tietue.</span><span class="sxs-lookup"><span data-stu-id="10141-165">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="10141-166">Anna tietolähteen määrityksessä tarvittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="10141-166">Enter the required information for the data source configuration.</span></span>

   - <span data-ttu-id="10141-167">**Kohde-URL**: Human Resources -nimitilan URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="10141-167">**Target URL**: The URL of your Human Resources namespace.</span></span>
   - <span data-ttu-id="10141-168">**Vuokraajan tunnus**: Azure Active Directory (Azure AD) -vuokraajan tunnus.</span><span class="sxs-lookup"><span data-stu-id="10141-168">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>
   - <span data-ttu-id="10141-169">**AAD-sovelluksen tunnus**: Microsoft Azure -portaalissa rekisteröidylle sovellukselle luotu sovelluksen (asiakaspalvelijan) tunnus.</span><span class="sxs-lookup"><span data-stu-id="10141-169">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="10141-170">Saint nämä tiedot aiemman [Sovelluksen rekisteröinti Microsoft Azuressa](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) -vaiheen aikana.</span><span class="sxs-lookup"><span data-stu-id="10141-170">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>
   - <span data-ttu-id="10141-171">**AAD-sovelluksen salainen koodi**: Microsoft Azure -portaalissa rekisteröidylle sovellukselle luotu asiakasohjelman salasana.</span><span class="sxs-lookup"><span data-stu-id="10141-171">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="10141-172">Saint nämä tiedot aiemman [Sovelluksen rekisteröinti Microsoft Azuressa](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) -vaiheen aikana.</span><span class="sxs-lookup"><span data-stu-id="10141-172">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

9. <span data-ttu-id="10141-173">Valitse **Tallenna ja sulje**.</span><span class="sxs-lookup"><span data-stu-id="10141-173">Select **Save & Close**.</span></span>

   ![Microsoft HR -tietolähde](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="10141-175">Sovelluksen oikeuksien myöntäminen Human Resourcesissa</span><span class="sxs-lookup"><span data-stu-id="10141-175">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="10141-176">Myönnä kahden Azure AD -sovelluksen oikeudet Human Resourcesissa:</span><span class="sxs-lookup"><span data-stu-id="10141-176">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="10141-177">Vuokraajalle Microsoft Azure -portaalissa luotu sovellus</span><span class="sxs-lookup"><span data-stu-id="10141-177">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="10141-178">Power Apps -ympäristössä asennettu Dynamics 365 HR Virtual Entity -sovellus</span><span class="sxs-lookup"><span data-stu-id="10141-178">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="10141-179">Avaa Human Resourcesissa **Azure Active Directory -sovellukset** -sivu.</span><span class="sxs-lookup"><span data-stu-id="10141-179">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="10141-180">Luo uusi sovellustietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="10141-180">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="10141-181">Anna **Asiakastunnus**-kentässä Microsoft Azure -portaalissa rekisteröidyn sovelluksen asiakastunnus.</span><span class="sxs-lookup"><span data-stu-id="10141-181">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="10141-182">Anna **Nimi**-kentässä Microsoft Azure -portaalissa rekisteröidyn sovelluksen nimi.</span><span class="sxs-lookup"><span data-stu-id="10141-182">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="10141-183">Valitse **Käyttäjätunnus**-kentässä sellaisen käyttäjän käyttäjätunnus, jolla on Human Resources- ja Power Apps -ympäristön järjestelmänvalvojan käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="10141-183">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="10141-184">Luo toinen sovellustietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="10141-184">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="10141-185">**Asiakastunnus**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="10141-185">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="10141-186">**Nimi**: Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="10141-186">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="10141-187">Valitse **Käyttäjätunnus**-kentässä sellaisen käyttäjän käyttäjätunnus, jolla on Human Resources- ja Power Apps -ympäristön järjestelmänvalvojan käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="10141-187">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="10141-188">Virtuaaliyksiköiden luominen</span><span class="sxs-lookup"><span data-stu-id="10141-188">Generate virtual entities</span></span>

<span data-ttu-id="10141-189">Voit valita asennuksen valmistumisen jälkeen virtuaaliyksiköt, jotka haluat luoda ja ottaa käyttöön Common Data Service -esiintymässä.</span><span class="sxs-lookup"><span data-stu-id="10141-189">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="10141-190">Avaa [Power Platform -hallintakeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="10141-190">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="10141-191">Valitse **Ympäristöt**-luettelossa Human Resources -esiintymään liitetty Power Apps -ympäristö.</span><span class="sxs-lookup"><span data-stu-id="10141-191">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="10141-192">Valitse **Ympäristön URL-osoite** sivun **Tiedot**-osassa.</span><span class="sxs-lookup"><span data-stu-id="10141-192">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="10141-193">Valitse **Ratkaisun kunnon keskus** -kohdassa **Erikoishaku**-kuvake sivun oikeassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="10141-193">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the page.</span></span>

5. <span data-ttu-id="10141-194">Valitse **Erikoishaku**-sivun avattavassa **Etsi**-luettelossa **Käytettävissä olevat HR-yksiköt**.</span><span class="sxs-lookup"><span data-stu-id="10141-194">On the **Advanced Find** page, in the **Look for** dropdown list, select **Available HR Entities**.</span></span>

6. <span data-ttu-id="10141-195">Etsi käyttöönotettavat yksiköt suodatinasetuksilla.</span><span class="sxs-lookup"><span data-stu-id="10141-195">Use the filter options to find the entity or entities you want to enable.</span></span>

7. <span data-ttu-id="10141-196">Valitse yksikkö luettelossa.</span><span class="sxs-lookup"><span data-stu-id="10141-196">Select an entity from the list.</span></span>

8. <span data-ttu-id="10141-197">Muuta yksikkösivulla yksikön **On luotu** -ominaisuudeksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="10141-197">On the entity page, change the **Has Been Generated** property to **Yes** for the entity.</span></span>

9. <span data-ttu-id="10141-198">Tallenna ja sulje yksikkösivu.</span><span class="sxs-lookup"><span data-stu-id="10141-198">Save and close the entity page.</span></span>

> [!NOTE]
> <span data-ttu-id="10141-199">Voit luoda useita virtuaaliyksikköjä samanaikaisesti **Muuta useita tietueita** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="10141-199">You can generate multiple virtual entities at once by using the **Change Multiple Records** page.</span></span> <span data-ttu-id="10141-200">Valitse sivulla ensin useita tietueita ja valitse sitten valintanauhassa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="10141-200">Select multiple records on the page, and select **Edit** on the ribbon.</span></span> <span data-ttu-id="10141-201">Voit sitten muuttaa kaikkien valittujen tietueiden **On luotu** -ominaisuuden.</span><span class="sxs-lookup"><span data-stu-id="10141-201">You can then change the **Has Been Generated** property for all selected records.</span></span>

![Käytettävissä olevat HR-yksiköt](./media/hr-admin-integration-virtual-entities-available.jpg)

> [!NOTE]
> <span data-ttu-id="10141-203">Virtuaaliyksiköiden luontiprosessia yksinkertaistetaan tulevissa versioissa siten, että prosessi tapahtuu Human Resourcesin sivulla.</span><span class="sxs-lookup"><span data-stu-id="10141-203">To streamline the process of generating virtual entities in future releases, the process will occur in a page in Human Resources.</span></span>

## <a name="see-also"></a><span data-ttu-id="10141-204">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="10141-204">See also</span></span>

[<span data-ttu-id="10141-205">Mikä on Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="10141-205">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="10141-206">Yksikön yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="10141-206">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="10141-207">Yksikkösuhteiden yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="10141-207">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="10141-208">Ulkoisten tietolähteiden tietoja sisältävien virtuaaliyksiköiden luominen ja muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="10141-208">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="10141-209">Mitä Power Apps -portaalit ovat?</span><span class="sxs-lookup"><span data-stu-id="10141-209">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="10141-210">Yleiskatsaus sovellusten luonnista Power Appsissa</span><span class="sxs-lookup"><span data-stu-id="10141-210">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
