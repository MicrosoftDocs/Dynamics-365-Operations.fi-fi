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
ms.openlocfilehash: 0d6f79ea569a7a9b0d25e73e8666bf9ba19095d0
ms.sourcegitcommit: a8665c47696028d371cdc4671db1fd8fcf9e1088
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/21/2020
ms.locfileid: "4058151"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="4088b-104">Common Data Service -virtuaaliyksiköiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4088b-104">Configure Common Data Service virtual entities</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="4088b-105">Dynamics 365 Human Resources on Common Data Servicen virtuaalinen tietolähde.</span><span class="sxs-lookup"><span data-stu-id="4088b-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="4088b-106">Se sisältää Common Data Servicen ja Microsoft Power Platformin täydet CRUD (luonti, luku, päivitys ja poisto) -toiminnot.</span><span class="sxs-lookup"><span data-stu-id="4088b-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="4088b-107">Virtuaaliyksiköiden tietoja ei tallenneta Common Data Serviceen vaan sovelluksen tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="4088b-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="4088b-108">Jos haluat ottaa Common Data Servicen Human Resources -yksiköiden CRUD-toiminnot käyttää, yksiköiden on oltava käytettävissä virtuaaliyksikköinä Common Data Servicessa.</span><span class="sxs-lookup"><span data-stu-id="4088b-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="4088b-109">Voit suorittaa tällä tavoin Common Data Servicen ja Microsoft Power Platformin CRUD-toimintoja Human Resourcesin tiedoissa.</span><span class="sxs-lookup"><span data-stu-id="4088b-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="4088b-110">Toiminnot tukevat myös Human Resourcesin liiketoimintalogiikan tarkistuksia, joilla varmistetaan tietojen eheys kirjoitettaessa tietoja yksiköihin.</span><span class="sxs-lookup"><span data-stu-id="4088b-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="4088b-111">Human Resourcesin käytettävissä olevat virtuaaliyksiköt</span><span class="sxs-lookup"><span data-stu-id="4088b-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="4088b-112">Kaikki Human Resourcesin OData (Open Data Protocol) -yksiköt ovat käytettävissä virtuaaliyksikköinä Common Data Servicessa.</span><span class="sxs-lookup"><span data-stu-id="4088b-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="4088b-113">Ne ovat käytettävissä myös Power Platformissa.</span><span class="sxs-lookup"><span data-stu-id="4088b-113">They're also available in Power Platform.</span></span> <span data-ttu-id="4088b-114">Voit nyt muodostaa sovelluksia ja kokemuksia käyttämällä tietoja suoraan Human Resourcesissa CRUD-ominaisuuksien avulla ilman, että tiedot kopioitava ja synkronoitava Common Data Serviceen.</span><span class="sxs-lookup"><span data-stu-id="4088b-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="4088b-115">Voit muodostaa Power Apps -portaalien avulla ulkoisia sivustoja, joiden avulla voidaan toteuttaa liiketoimintaprosessien yhteistyöskenaarioita Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="4088b-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="4088b-116">Voit tarkastella ympäristössä käyttöönotettujen virtuaaliyksiköiden luetteloa ja aloittaa [Power Appsin](https://make.powerapps.com) yksiköiden käyttämisen **Dynamics 365 HR -virtuaaliyksiköiden** ratkaisussa.</span><span class="sxs-lookup"><span data-stu-id="4088b-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Dynamics 365 HR -virtuaaliyksiköt Power Appsissa](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="4088b-118">Virtuaaliyksiköiden ja tavallisten yksiköiden vertailu</span><span class="sxs-lookup"><span data-stu-id="4088b-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="4088b-119">Human Resourcesin virtuaaliyksiköt eivät ole samoja kuin Human Resourcesin luodut Common Data Servicen yksiköt.</span><span class="sxs-lookup"><span data-stu-id="4088b-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="4088b-120">Human Resourcesin tavalliset yksiköt luodaan erikseen ja niitä ylläpidetään HCM Common -ratkaisussa Common Data Servicessa.</span><span class="sxs-lookup"><span data-stu-id="4088b-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="4088b-121">Tavallisissa yksiköissä tiedot tallennetaan Common Data Servicessa, ja ne on synkronoitava Human Resourcesin sovellustietokannassa.</span><span class="sxs-lookup"><span data-stu-id="4088b-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="4088b-122">Tavallisten Human Resourcesin Common Data Service -yksiköiden luettelo on kohdassa [Common Data Service -yksiköt](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="4088b-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="4088b-123">Luo perustiedot</span><span class="sxs-lookup"><span data-stu-id="4088b-123">Setup</span></span>

<span data-ttu-id="4088b-124">Ota virtuaaliyksiköt käyttöön ympäristössä tekemällä seuraavat määritykset.</span><span class="sxs-lookup"><span data-stu-id="4088b-124">Follow these setup steps to enable virtual entities in your environment.</span></span> 

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="4088b-125">Sovelluksen rekisteröinti Microsoft Azuressa</span><span class="sxs-lookup"><span data-stu-id="4088b-125">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="4088b-126">Sovellus on rekisteröitävä ensin Azure-portaalissa, jotta Microsoftin käyttäjätietoympäristö voi toimittaa todennus- ja valtuutuspalvelut sovellukselle ja käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="4088b-126">First, you need to register the app in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="4088b-127">Lisätietoja sovellusten rekisteröinnistä Azuressa on kohdassa [Pika-aloitus: Sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristöön](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="4088b-127">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="4088b-128">Avaa [Microsoft Azure -portaali](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="4088b-128">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="4088b-129">Valitse Azure-palveluluettelossa **Sovelluksen rekisteröinnit**.</span><span class="sxs-lookup"><span data-stu-id="4088b-129">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="4088b-130">Valitse **Uusi rekisteröinti**.</span><span class="sxs-lookup"><span data-stu-id="4088b-130">Select **New registration**.</span></span>

4. <span data-ttu-id="4088b-131">Kirjoita **Nimi** -kenttään sovellusta kuvaava nimi.</span><span class="sxs-lookup"><span data-stu-id="4088b-131">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="4088b-132">Esimerkki: **Dynamics 365 Human Resourcesin virtuaaliyksiköt**.</span><span class="sxs-lookup"><span data-stu-id="4088b-132">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="4088b-133">Anna **Uudelleenohjauksen URI** -kenttään Human Resources -esiintymän nimitilan URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="4088b-133">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="4088b-134">Valitse **Rekisteröi**.</span><span class="sxs-lookup"><span data-stu-id="4088b-134">Select **Register**.</span></span>

7. <span data-ttu-id="4088b-135">Kun rekisteröinti valmistuu, Azure-portaali näyttää sovelluksen rekisteröinnin **Yleiskatsaus** -ruudussa, joka sisältää myös sen **sovelluksen (asiakasohjelman) tunnuksen**.</span><span class="sxs-lookup"><span data-stu-id="4088b-135">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="4088b-136">Kirjoita muistiin tämä **sovelluksen (asiakasohjelman) tunnus**.</span><span class="sxs-lookup"><span data-stu-id="4088b-136">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="4088b-137">Nämä tiedot annetaan, kun [määrität virtuaaliyksikön tietolähteen](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="4088b-137">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="4088b-138">Valitse vasemmassa siirtymisruudussa **Varmenteet ja salaiset koodit**.</span><span class="sxs-lookup"><span data-stu-id="4088b-138">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="4088b-139">Valitse sivun **Asiakasohjelman salasana** -osassa **Uusi asiakasohjelman salasana**.</span><span class="sxs-lookup"><span data-stu-id="4088b-139">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="4088b-140">Anna kuvaus, valitse kesto ja valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="4088b-140">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="4088b-141">Kirjaa salaisen koodin arvo muistiin.</span><span class="sxs-lookup"><span data-stu-id="4088b-141">Record the secret's value.</span></span> <span data-ttu-id="4088b-142">Nämä tiedot annetaan, kun [määrität virtuaaliyksikön tietolähteen](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="4088b-142">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="4088b-143">Muista kirjoittaa salaisen koodin arvo muistiin tässä vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="4088b-143">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="4088b-144">Salaista koodi ei näytetä sen jälkeen, kun poistut sivulta.</span><span class="sxs-lookup"><span data-stu-id="4088b-144">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="4088b-145">Dynamics 365 HR Virtual Entity -sovelluksen asentaminen</span><span class="sxs-lookup"><span data-stu-id="4088b-145">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="4088b-146">Asenna Dynamics 365 HR Virtual Entity -sovellus Power Apps -ympäristöön ottamaan virtuaaliyksikön ratkaisupaketti käyttöön Common Data Servicessa.</span><span class="sxs-lookup"><span data-stu-id="4088b-146">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="4088b-147">Avaa [Power Platform -hallintakeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="4088b-147">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="4088b-148">Valitse **Ympäristöt** -luettelossa Human Resources -esiintymään liitetty Power Apps -ympäristö.</span><span class="sxs-lookup"><span data-stu-id="4088b-148">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="4088b-149">Valitse sivun **Resurssit** -osassa **Dynamics 365 -sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="4088b-149">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="4088b-150">Valitse **Asenna sovellus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="4088b-150">Select the **Install app** action.</span></span>

5. <span data-ttu-id="4088b-151">Valitse ensin **Dynamics 365 HR Virtual Entity** ja valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="4088b-151">Select **Dynamics 365 HR Virtual Entity** , and select **Next**.</span></span>

6. <span data-ttu-id="4088b-152">Tutustu palvelun käyttöehtoihin ja merkitse ne hyväksytyiksi.</span><span class="sxs-lookup"><span data-stu-id="4088b-152">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="4088b-153">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="4088b-153">Select **Install**.</span></span>

<span data-ttu-id="4088b-154">Asennus kestää muutaman minuutin.</span><span class="sxs-lookup"><span data-stu-id="4088b-154">The install takes a few minutes.</span></span> <span data-ttu-id="4088b-155">Kun asennus valmistuu, jatka seuraaviin vaiheisiin.</span><span class="sxs-lookup"><span data-stu-id="4088b-155">When it completes, continue to the next steps.</span></span>

![Dynamics 365 HR Virtual Entity -sovelluksen asentaminen Power Platform -hallintakeskuksessa](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="4088b-157">Virtuaaliyksikön tietolähteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4088b-157">Configure the virtual entity data source</span></span> 

<span data-ttu-id="4088b-158">Seuraavaksi määritetään virtuaaliyksikön tietolähde Power Apps -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="4088b-158">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="4088b-159">Avaa [Power Platform -hallintakeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="4088b-159">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="4088b-160">Valitse **Ympäristöt** -luettelossa Human Resources -esiintymään liitetty Power Apps -ympäristö.</span><span class="sxs-lookup"><span data-stu-id="4088b-160">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="4088b-161">Valitse **Ympäristön URL-osoite** sivun **Tiedot** -osassa.</span><span class="sxs-lookup"><span data-stu-id="4088b-161">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="4088b-162">Valitse **Ratkaisun kunnon keskus** -kohdassa **Erikoishaku** -kuvake sovellussivun oikeassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="4088b-162">In the **Solution Health Hub** , select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="4088b-163">Valitse **Erikoishaku** -sivun avattavassa **Etsi** -luettelossa **Finance and Operations -virtuaalitietolähteen määritykset**.</span><span class="sxs-lookup"><span data-stu-id="4088b-163">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="4088b-164">Valitse **Tulokset**.</span><span class="sxs-lookup"><span data-stu-id="4088b-164">Select **Results**.</span></span>

7. <span data-ttu-id="4088b-165">Valitse **Microsoft HR -tietolähde** -tietue.</span><span class="sxs-lookup"><span data-stu-id="4088b-165">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="4088b-166">Anna tietolähteen määrityksessä tarvittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="4088b-166">Enter the required information for the data source configuration.</span></span>

   - <span data-ttu-id="4088b-167">**Kohde-URL** : Human Resources -nimitilan URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="4088b-167">**Target URL** : The URL of your Human Resources namespace.</span></span>
   - <span data-ttu-id="4088b-168">**Vuokraajan tunnus** : Azure Active Directory (Azure AD) -vuokraajan tunnus.</span><span class="sxs-lookup"><span data-stu-id="4088b-168">**Tenant ID** : The Azure Active Directory (Azure AD) tenant ID.</span></span>
   - <span data-ttu-id="4088b-169">**AAD-sovelluksen tunnus** : Microsoft Azure -portaalissa rekisteröidylle sovellukselle luotu sovelluksen (asiakaspalvelijan) tunnus.</span><span class="sxs-lookup"><span data-stu-id="4088b-169">**AAD Application ID** : The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="4088b-170">Saint nämä tiedot aiemman [Sovelluksen rekisteröinti Microsoft Azuressa](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) -vaiheen aikana.</span><span class="sxs-lookup"><span data-stu-id="4088b-170">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>
   - <span data-ttu-id="4088b-171">**AAD-sovelluksen salainen koodi** : Microsoft Azure -portaalissa rekisteröidylle sovellukselle luotu asiakasohjelman salasana.</span><span class="sxs-lookup"><span data-stu-id="4088b-171">**AAD Application Secret** : The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="4088b-172">Saint nämä tiedot aiemman [Sovelluksen rekisteröinti Microsoft Azuressa](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) -vaiheen aikana.</span><span class="sxs-lookup"><span data-stu-id="4088b-172">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

9. <span data-ttu-id="4088b-173">Valitse **Tallenna ja sulje**.</span><span class="sxs-lookup"><span data-stu-id="4088b-173">Select **Save & Close**.</span></span>

   ![Microsoft HR -tietolähde](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="4088b-175">Sovelluksen oikeuksien myöntäminen Human Resourcesissa</span><span class="sxs-lookup"><span data-stu-id="4088b-175">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="4088b-176">Myönnä kahden Azure AD -sovelluksen oikeudet Human Resourcesissa:</span><span class="sxs-lookup"><span data-stu-id="4088b-176">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="4088b-177">Vuokraajalle Microsoft Azure -portaalissa luotu sovellus</span><span class="sxs-lookup"><span data-stu-id="4088b-177">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="4088b-178">Power Apps -ympäristössä asennettu Dynamics 365 HR Virtual Entity -sovellus</span><span class="sxs-lookup"><span data-stu-id="4088b-178">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="4088b-179">Avaa Human Resourcesissa **Azure Active Directory -sovellukset** -sivu.</span><span class="sxs-lookup"><span data-stu-id="4088b-179">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="4088b-180">Luo uusi sovellustietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4088b-180">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="4088b-181">Anna **Asiakastunnus** -kentässä Microsoft Azure -portaalissa rekisteröidyn sovelluksen asiakastunnus.</span><span class="sxs-lookup"><span data-stu-id="4088b-181">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="4088b-182">Anna **Nimi** -kentässä Microsoft Azure -portaalissa rekisteröidyn sovelluksen nimi.</span><span class="sxs-lookup"><span data-stu-id="4088b-182">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="4088b-183">Valitse **Käyttäjätunnus** -kentässä sellaisen käyttäjän käyttäjätunnus, jolla on Human Resources- ja Power Apps -ympäristön järjestelmänvalvojan käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="4088b-183">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="4088b-184">Luo toinen sovellustietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4088b-184">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="4088b-185">**Asiakastunnus** : f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="4088b-185">**Client Id** : f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="4088b-186">**Nimi** : Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="4088b-186">**Name** : Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="4088b-187">Valitse **Käyttäjätunnus** -kentässä sellaisen käyttäjän käyttäjätunnus, jolla on Human Resources- ja Power Apps -ympäristön järjestelmänvalvojan käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="4088b-187">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="4088b-188">Virtuaaliyksiköiden luominen</span><span class="sxs-lookup"><span data-stu-id="4088b-188">Generate virtual entities</span></span>

<span data-ttu-id="4088b-189">Voit valita asennuksen valmistumisen jälkeen virtuaaliyksiköt, jotka haluat luoda ja ottaa käyttöön Common Data Service -esiintymässä.</span><span class="sxs-lookup"><span data-stu-id="4088b-189">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="4088b-190">Avaa Human Resourcesissa **Common Data Service (CDS) -integraatio** -sivu.</span><span class="sxs-lookup"><span data-stu-id="4088b-190">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="4088b-191">Valitse **Virtuaaliyksiköt** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="4088b-191">Select the **Virtual entities** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="4088b-192">**Ota virtuaaliyksikkö käyttöön** -tilanvaihtopainike on automaattisesti **Kyllä** -asennossa, kun kaikki tarvittavat määritykset on tehty.</span><span class="sxs-lookup"><span data-stu-id="4088b-192">The **Enable the virtual entity** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="4088b-193">Jos tilanvaihtopainike on **Ei** -asennossa, tarkista tämä asiakirjan edellisten osien vaiheet ja varmista, että kaikki edellytettävät asetukset on määritetty.</span><span class="sxs-lookup"><span data-stu-id="4088b-193">If the toggle is set to **No** , review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="4088b-194">Valitse Common Data Servicessa luotavat yksiköt.</span><span class="sxs-lookup"><span data-stu-id="4088b-194">Select the entity or entities you want to generate in Common Data Service.</span></span>

4. <span data-ttu-id="4088b-195">Valitse **Luo/päivitä**.</span><span class="sxs-lookup"><span data-stu-id="4088b-195">Select **Generate/refresh**.</span></span>

![Common Data Service -integraatio](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a><span data-ttu-id="4088b-197">Yksikön luontitilan tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="4088b-197">Check entity generation status</span></span>

<span data-ttu-id="4088b-198">Virtuaaliyksiköt luodaan Common Data Servicessa asynkronisena taustaprosessina.</span><span class="sxs-lookup"><span data-stu-id="4088b-198">Virtual entities are generated in Common Data Service through an asynchronous background process.</span></span> <span data-ttu-id="4088b-199">Prosessin päivitykset näkyvät toimintokeskuksessa.</span><span class="sxs-lookup"><span data-stu-id="4088b-199">Updates on the process display in the action center.</span></span> <span data-ttu-id="4088b-200">Prosessin tiedot, kuten virhelokit, näkyvät **Prosessin automatisoinnit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="4088b-200">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="4088b-201">Avaa Human Resourcesissa **Prosessin automatisoinnit** -sivu.</span><span class="sxs-lookup"><span data-stu-id="4088b-201">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="4088b-202">Valitse **Taustaprosessit** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="4088b-202">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="4088b-203">Valitse **Virtuaaliyksikön kyselyn asynkroninen toiminnon taustaprosessi**.</span><span class="sxs-lookup"><span data-stu-id="4088b-203">Select **Virtual entity poll async operation background process**.</span></span>

4. <span data-ttu-id="4088b-204">Valitse **Näytä viimeisimmät tulokset**.</span><span class="sxs-lookup"><span data-stu-id="4088b-204">Select **View most recent results**.</span></span>

<span data-ttu-id="4088b-205">Esiin tulevassa ruudussa näkyy prosessin viimeksi suoritetut tulokset.</span><span class="sxs-lookup"><span data-stu-id="4088b-205">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="4088b-206">Voit tarkastella prosessin lokia, mukaan lukien mahdollisia Common Data Servicen palauttamia virheitä.</span><span class="sxs-lookup"><span data-stu-id="4088b-206">You can view the log for the process, including any errors returned from Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="4088b-207">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="4088b-207">See also</span></span>

[<span data-ttu-id="4088b-208">Mikä on Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="4088b-208">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="4088b-209">Yksikön yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4088b-209">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="4088b-210">Yksikkösuhteiden yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4088b-210">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="4088b-211">Ulkoisten tietolähteiden tietoja sisältävien virtuaaliyksiköiden luominen ja muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="4088b-211">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="4088b-212">Mitä Power Apps -portaalit ovat?</span><span class="sxs-lookup"><span data-stu-id="4088b-212">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="4088b-213">Yleiskatsaus sovellusten luonnista Power Appsissa</span><span class="sxs-lookup"><span data-stu-id="4088b-213">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
