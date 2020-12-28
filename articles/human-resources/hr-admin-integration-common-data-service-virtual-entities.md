---
title: Common Data Service -virtuaaliyksiköiden määrittäminen
description: Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin virtuaaliyksiköiden määrittämistä. Virtuaaliyksiköiden luominen ja aiemmin luotujen päivittäminen sekä luotujen ja käytettävissä olevien yksiköiden analysoiminen.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
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
ms.openlocfilehash: 2b590faeab600d04c9d5303693ec1e9ac682250d
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645598"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="c9d67-104">Common Data Service -virtuaaliyksiköiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c9d67-104">Configure Common Data Service virtual entities</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c9d67-105">Dynamics 365 Human Resources on Common Data Servicen virtuaalinen tietolähde.</span><span class="sxs-lookup"><span data-stu-id="c9d67-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="c9d67-106">Se sisältää Common Data Servicen ja Microsoft Power Platformin täydet CRUD (luonti, luku, päivitys ja poisto) -toiminnot.</span><span class="sxs-lookup"><span data-stu-id="c9d67-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="c9d67-107">Virtuaaliyksiköiden tietoja ei tallenneta Common Data Serviceen vaan sovelluksen tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="c9d67-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="c9d67-108">Jos haluat ottaa Common Data Servicen Human Resources -yksiköiden CRUD-toiminnot käyttää, yksiköiden on oltava käytettävissä virtuaaliyksikköinä Common Data Servicessa.</span><span class="sxs-lookup"><span data-stu-id="c9d67-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="c9d67-109">Voit suorittaa tällä tavoin Common Data Servicen ja Microsoft Power Platformin CRUD-toimintoja Human Resourcesin tiedoissa.</span><span class="sxs-lookup"><span data-stu-id="c9d67-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="c9d67-110">Toiminnot tukevat myös Human Resourcesin liiketoimintalogiikan tarkistuksia, joilla varmistetaan tietojen eheys kirjoitettaessa tietoja yksiköihin.</span><span class="sxs-lookup"><span data-stu-id="c9d67-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="c9d67-111">Human Resourcesin käytettävissä olevat virtuaaliyksiköt</span><span class="sxs-lookup"><span data-stu-id="c9d67-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="c9d67-112">Kaikki Human Resourcesin OData (Open Data Protocol) -yksiköt ovat käytettävissä virtuaaliyksikköinä Common Data Servicessa.</span><span class="sxs-lookup"><span data-stu-id="c9d67-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="c9d67-113">Ne ovat käytettävissä myös Power Platformissa.</span><span class="sxs-lookup"><span data-stu-id="c9d67-113">They're also available in Power Platform.</span></span> <span data-ttu-id="c9d67-114">Voit nyt muodostaa sovelluksia ja kokemuksia käyttämällä tietoja suoraan Human Resourcesissa CRUD-ominaisuuksien avulla ilman, että tiedot kopioitava ja synkronoitava Common Data Serviceen.</span><span class="sxs-lookup"><span data-stu-id="c9d67-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="c9d67-115">Voit muodostaa Power Apps -portaalien avulla ulkoisia sivustoja, joiden avulla voidaan toteuttaa liiketoimintaprosessien yhteistyöskenaarioita Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="c9d67-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="c9d67-116">Voit tarkastella ympäristössä käyttöönotettujen virtuaaliyksiköiden luetteloa ja aloittaa [Power Appsin](https://make.powerapps.com) yksiköiden käyttämisen **Dynamics 365 HR -virtuaaliyksiköiden** ratkaisussa.</span><span class="sxs-lookup"><span data-stu-id="c9d67-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Dynamics 365 HR -virtuaaliyksiköt Power Appsissa](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="c9d67-118">Virtuaaliyksiköiden ja tavallisten yksiköiden vertailu</span><span class="sxs-lookup"><span data-stu-id="c9d67-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="c9d67-119">Human Resourcesin virtuaaliyksiköt eivät ole samoja kuin Human Resourcesin luodut Common Data Servicen yksiköt.</span><span class="sxs-lookup"><span data-stu-id="c9d67-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="c9d67-120">Human Resourcesin tavalliset yksiköt luodaan erikseen ja niitä ylläpidetään HCM Common -ratkaisussa Common Data Servicessa.</span><span class="sxs-lookup"><span data-stu-id="c9d67-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="c9d67-121">Tavallisissa yksiköissä tiedot tallennetaan Common Data Servicessa, ja ne on synkronoitava Human Resourcesin sovellustietokannassa.</span><span class="sxs-lookup"><span data-stu-id="c9d67-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="c9d67-122">Tavallisten Human Resourcesin Common Data Service -yksiköiden luettelo on kohdassa [Common Data Service -yksiköt](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="c9d67-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="c9d67-123">Luo perustiedot</span><span class="sxs-lookup"><span data-stu-id="c9d67-123">Setup</span></span>

<span data-ttu-id="c9d67-124">Ota virtuaaliyksiköt käyttöön ympäristössä tekemällä seuraavat määritykset.</span><span class="sxs-lookup"><span data-stu-id="c9d67-124">Follow these setup steps to enable virtual entities in your environment.</span></span>

### <a name="enable-virtual-entities-in-human-resources"></a><span data-ttu-id="c9d67-125">Human Resourcesin virtuaaliyksiköiden käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="c9d67-125">Enable virtual entities in Human Resources</span></span>

<span data-ttu-id="c9d67-126">Ensin on otettava käyttöön virtuaaliyksiköt **Ominaisuuksien hallinta** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="c9d67-126">First, you must enable virtual entities in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="c9d67-127">Valitse Human Resourcesissa **Järjestelmän hallinta**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-127">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="c9d67-128">Valitse **Ominaisuuksien hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="c9d67-128">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="c9d67-129">Valitse **HR/CDS:n virtuaaliyksikön tuki** ja valitse sitten **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-129">Select **Virtual Entity support in HR/CDS**, and then select **Enable**.</span></span>

<span data-ttu-id="c9d67-130">Lisätietoja ominaisuuksien ottamisesta käyttöön ja poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="c9d67-130">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="c9d67-131">Sovelluksen rekisteröinti Microsoft Azuressa</span><span class="sxs-lookup"><span data-stu-id="c9d67-131">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="c9d67-132">Human Resources -esiintymä on rekisteröitävä Azure-portaalissa, jotta Microsoftin käyttäjätietoympäristö voi toimittaa todennus- ja valtuutuspalvelut sovellukselle ja käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="c9d67-132">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="c9d67-133">Lisätietoja sovellusten rekisteröinnistä Azuressa on kohdassa [Pika-aloitus: Sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristöön](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="c9d67-133">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="c9d67-134">Avaa [Microsoft Azure -portaali](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="c9d67-134">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="c9d67-135">Valitse Azure-palveluluettelossa **Sovelluksen rekisteröinnit**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-135">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="c9d67-136">Valitse **Uusi rekisteröinti**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-136">Select **New registration**.</span></span>

4. <span data-ttu-id="c9d67-137">Kirjoita **Nimi**-kenttään sovellusta kuvaava nimi.</span><span class="sxs-lookup"><span data-stu-id="c9d67-137">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="c9d67-138">Esimerkki: **Dynamics 365 Human Resourcesin virtuaaliyksiköt**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-138">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="c9d67-139">Anna **Uudelleenohjauksen URI** -kenttään Human Resources -esiintymän nimitilan URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="c9d67-139">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="c9d67-140">Valitse **Rekisteröi**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-140">Select **Register**.</span></span>

7. <span data-ttu-id="c9d67-141">Kun rekisteröinti valmistuu, Azure-portaali näyttää sovelluksen rekisteröinnin **Yleiskatsaus**-ruudussa, joka sisältää myös sen **sovelluksen (asiakasohjelman) tunnuksen**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-141">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="c9d67-142">Kirjoita muistiin tämä **sovelluksen (asiakasohjelman) tunnus**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-142">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="c9d67-143">Nämä tiedot annetaan, kun [määrität virtuaaliyksikön tietolähteen](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="c9d67-143">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="c9d67-144">Valitse vasemmassa siirtymisruudussa **Varmenteet ja salaiset koodit**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-144">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="c9d67-145">Valitse sivun **Asiakasohjelman salasana** -osassa **Uusi asiakasohjelman salasana**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-145">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="c9d67-146">Anna kuvaus, valitse kesto ja valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-146">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="c9d67-147">Kirjaa salaisen koodin arvo muistiin.</span><span class="sxs-lookup"><span data-stu-id="c9d67-147">Record the secret's value.</span></span> <span data-ttu-id="c9d67-148">Nämä tiedot annetaan, kun [määrität virtuaaliyksikön tietolähteen](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="c9d67-148">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="c9d67-149">Muista kirjoittaa salaisen koodin arvo muistiin tässä vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="c9d67-149">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="c9d67-150">Salaista koodi ei näytetä sen jälkeen, kun poistut sivulta.</span><span class="sxs-lookup"><span data-stu-id="c9d67-150">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="c9d67-151">Dynamics 365 HR Virtual Entity -sovelluksen asentaminen</span><span class="sxs-lookup"><span data-stu-id="c9d67-151">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="c9d67-152">Asenna Dynamics 365 HR Virtual Entity -sovellus Power Apps -ympäristöön ottamaan virtuaaliyksikön ratkaisupaketti käyttöön Common Data Servicessa.</span><span class="sxs-lookup"><span data-stu-id="c9d67-152">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="c9d67-153">Avaa [Power Platform -hallintakeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="c9d67-153">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="c9d67-154">Valitse **Ympäristöt**-luettelossa Human Resources -esiintymään liitetty Power Apps -ympäristö.</span><span class="sxs-lookup"><span data-stu-id="c9d67-154">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="c9d67-155">Valitse sivun **Resurssit**-osassa **Dynamics 365 -sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-155">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="c9d67-156">Valitse **Asenna sovellus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="c9d67-156">Select the **Install app** action.</span></span>

5. <span data-ttu-id="c9d67-157">Valitse ensin **Dynamics 365 HR Virtual Entity** ja valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-157">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="c9d67-158">Tutustu palvelun käyttöehtoihin ja merkitse ne hyväksytyiksi.</span><span class="sxs-lookup"><span data-stu-id="c9d67-158">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="c9d67-159">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-159">Select **Install**.</span></span>

<span data-ttu-id="c9d67-160">Asennus kestää muutaman minuutin.</span><span class="sxs-lookup"><span data-stu-id="c9d67-160">The install takes a few minutes.</span></span> <span data-ttu-id="c9d67-161">Kun asennus valmistuu, jatka seuraaviin vaiheisiin.</span><span class="sxs-lookup"><span data-stu-id="c9d67-161">When it completes, continue to the next steps.</span></span>

![Dynamics 365 HR Virtual Entity -sovelluksen asentaminen Power Platform -hallintakeskuksessa](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="c9d67-163">Virtuaaliyksikön tietolähteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c9d67-163">Configure the virtual entity data source</span></span> 

<span data-ttu-id="c9d67-164">Seuraavaksi määritetään virtuaaliyksikön tietolähde Power Apps -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="c9d67-164">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="c9d67-165">Avaa [Power Platform -hallintakeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="c9d67-165">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="c9d67-166">Valitse **Ympäristöt**-luettelossa Human Resources -esiintymään liitetty Power Apps -ympäristö.</span><span class="sxs-lookup"><span data-stu-id="c9d67-166">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="c9d67-167">Valitse **Ympäristön URL-osoite** sivun **Tiedot**-osassa.</span><span class="sxs-lookup"><span data-stu-id="c9d67-167">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="c9d67-168">Valitse **Ratkaisun kunnon keskus** -kohdassa **Erikoishaku**-kuvake sovellussivun oikeassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="c9d67-168">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="c9d67-169">Valitse **Erikoishaku**-sivun avattavassa **Etsi**-luettelossa **Finance and Operations -virtuaalitietolähteen määritykset**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-169">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="c9d67-170">Valitse **Tulokset**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-170">Select **Results**.</span></span>

7. <span data-ttu-id="c9d67-171">Valitse **Microsoft HR -tietolähde** -tietue.</span><span class="sxs-lookup"><span data-stu-id="c9d67-171">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="c9d67-172">Anna tietolähteen määrityksessä seuraavat tarvittavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="c9d67-172">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="c9d67-173">**Kohde-URL**: Human Resources -nimitilan URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="c9d67-173">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="c9d67-174">Kohde-URL-osoitteen muoto on seuraava:</span><span class="sxs-lookup"><span data-stu-id="c9d67-174">The format of the target URL is:</span></span>
     
     <span data-ttu-id="c9d67-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="c9d67-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="c9d67-176">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="c9d67-176">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="c9d67-177">Virheiden välttämiseksi varmista, että URL-osoittee lopussa on merkki **/**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-177">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="c9d67-178">**Vuokraajan tunnus**: Azure Active Directory (Azure AD) -vuokraajan tunnus.</span><span class="sxs-lookup"><span data-stu-id="c9d67-178">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="c9d67-179">**AAD-sovelluksen tunnus**: Microsoft Azure -portaalissa rekisteröidylle sovellukselle luotu sovelluksen (asiakaspalvelijan) tunnus.</span><span class="sxs-lookup"><span data-stu-id="c9d67-179">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="c9d67-180">Saint nämä tiedot aiemman [Sovelluksen rekisteröinti Microsoft Azuressa](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) -vaiheen aikana.</span><span class="sxs-lookup"><span data-stu-id="c9d67-180">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="c9d67-181">**AAD-sovelluksen salainen koodi**: Microsoft Azure -portaalissa rekisteröidylle sovellukselle luotu asiakasohjelman salasana.</span><span class="sxs-lookup"><span data-stu-id="c9d67-181">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="c9d67-182">Saint nämä tiedot aiemman [Sovelluksen rekisteröinti Microsoft Azuressa](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) -vaiheen aikana.</span><span class="sxs-lookup"><span data-stu-id="c9d67-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Microsoft HR -tietolähde](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="c9d67-184">Valitse **Tallenna ja sulje**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-184">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="c9d67-185">Sovelluksen oikeuksien myöntäminen Human Resourcesissa</span><span class="sxs-lookup"><span data-stu-id="c9d67-185">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="c9d67-186">Myönnä kahden Azure AD -sovelluksen oikeudet Human Resourcesissa:</span><span class="sxs-lookup"><span data-stu-id="c9d67-186">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="c9d67-187">Vuokraajalle Microsoft Azure -portaalissa luotu sovellus</span><span class="sxs-lookup"><span data-stu-id="c9d67-187">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="c9d67-188">Power Apps -ympäristössä asennettu Dynamics 365 HR Virtual Entity -sovellus</span><span class="sxs-lookup"><span data-stu-id="c9d67-188">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="c9d67-189">Avaa Human Resourcesissa **Azure Active Directory -sovellukset** -sivu.</span><span class="sxs-lookup"><span data-stu-id="c9d67-189">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="c9d67-190">Luo uusi sovellustietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-190">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="c9d67-191">Anna **Asiakastunnus**-kentässä Microsoft Azure -portaalissa rekisteröidyn sovelluksen asiakastunnus.</span><span class="sxs-lookup"><span data-stu-id="c9d67-191">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="c9d67-192">Anna **Nimi**-kentässä Microsoft Azure -portaalissa rekisteröidyn sovelluksen nimi.</span><span class="sxs-lookup"><span data-stu-id="c9d67-192">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="c9d67-193">Valitse **Käyttäjätunnus**-kentässä sellaisen käyttäjän käyttäjätunnus, jolla on Human Resources- ja Power Apps -ympäristön järjestelmänvalvojan käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="c9d67-193">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="c9d67-194">Luo toinen sovellustietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-194">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="c9d67-195">**Asiakastunnus**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="c9d67-195">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="c9d67-196">**Nimi**: Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="c9d67-196">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="c9d67-197">Valitse **Käyttäjätunnus**-kentässä sellaisen käyttäjän käyttäjätunnus, jolla on Human Resources- ja Power Apps -ympäristön järjestelmänvalvojan käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="c9d67-197">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="c9d67-198">Virtuaaliyksiköiden luominen</span><span class="sxs-lookup"><span data-stu-id="c9d67-198">Generate virtual entities</span></span>

<span data-ttu-id="c9d67-199">Voit valita asennuksen valmistumisen jälkeen virtuaaliyksiköt, jotka haluat luoda ja ottaa käyttöön Common Data Service -esiintymässä.</span><span class="sxs-lookup"><span data-stu-id="c9d67-199">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="c9d67-200">Avaa Human Resourcesissa **Common Data Service (CDS) -integraatio** -sivu.</span><span class="sxs-lookup"><span data-stu-id="c9d67-200">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="c9d67-201">Valitse **Virtuaaliyksiköt**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="c9d67-201">Select the **Virtual entities** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="c9d67-202">**Ota virtuaaliyksikkö käyttöön** -tilanvaihtopainike on automaattisesti **Kyllä**-asennossa, kun kaikki tarvittavat määritykset on tehty.</span><span class="sxs-lookup"><span data-stu-id="c9d67-202">The **Enable the virtual entity** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="c9d67-203">Jos tilanvaihtopainike on **Ei**-asennossa, tarkista tämä asiakirjan edellisten osien vaiheet ja varmista, että kaikki edellytettävät asetukset on määritetty.</span><span class="sxs-lookup"><span data-stu-id="c9d67-203">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="c9d67-204">Valitse Common Data Servicessa luotavat yksiköt.</span><span class="sxs-lookup"><span data-stu-id="c9d67-204">Select the entity or entities you want to generate in Common Data Service.</span></span>

4. <span data-ttu-id="c9d67-205">Valitse **Luo/päivitä**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-205">Select **Generate/refresh**.</span></span>

![Common Data Service -integraatio](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a><span data-ttu-id="c9d67-207">Yksikön luontitilan tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="c9d67-207">Check entity generation status</span></span>

<span data-ttu-id="c9d67-208">Virtuaaliyksiköt luodaan Common Data Servicessa asynkronisena taustaprosessina.</span><span class="sxs-lookup"><span data-stu-id="c9d67-208">Virtual entities are generated in Common Data Service through an asynchronous background process.</span></span> <span data-ttu-id="c9d67-209">Prosessin päivitykset näkyvät toimintokeskuksessa.</span><span class="sxs-lookup"><span data-stu-id="c9d67-209">Updates on the process display in the action center.</span></span> <span data-ttu-id="c9d67-210">Prosessin tiedot, kuten virhelokit, näkyvät **Prosessin automatisoinnit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c9d67-210">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="c9d67-211">Avaa Human Resourcesissa **Prosessin automatisoinnit** -sivu.</span><span class="sxs-lookup"><span data-stu-id="c9d67-211">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="c9d67-212">Valitse **Taustaprosessit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="c9d67-212">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="c9d67-213">Valitse **Virtuaaliyksikön kyselyn asynkroninen toiminnon taustaprosessi**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-213">Select **Virtual entity poll async operation background process**.</span></span>

4. <span data-ttu-id="c9d67-214">Valitse **Näytä viimeisimmät tulokset**.</span><span class="sxs-lookup"><span data-stu-id="c9d67-214">Select **View most recent results**.</span></span>

<span data-ttu-id="c9d67-215">Esiin tulevassa ruudussa näkyy prosessin viimeksi suoritetut tulokset.</span><span class="sxs-lookup"><span data-stu-id="c9d67-215">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="c9d67-216">Voit tarkastella prosessin lokia, mukaan lukien mahdollisia Common Data Servicen palauttamia virheitä.</span><span class="sxs-lookup"><span data-stu-id="c9d67-216">You can view the log for the process, including any errors returned from Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="c9d67-217">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="c9d67-217">See also</span></span>

[<span data-ttu-id="c9d67-218">Mikä on Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="c9d67-218">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="c9d67-219">Yksikön yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="c9d67-219">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="c9d67-220">Yksikkösuhteiden yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="c9d67-220">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="c9d67-221">Ulkoisten tietolähteiden tietoja sisältävien virtuaaliyksiköiden luominen ja muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="c9d67-221">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="c9d67-222">Mitä Power Apps -portaalit ovat?</span><span class="sxs-lookup"><span data-stu-id="c9d67-222">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="c9d67-223">Yleiskatsaus sovellusten luonnista Power Appsissa</span><span class="sxs-lookup"><span data-stu-id="c9d67-223">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
