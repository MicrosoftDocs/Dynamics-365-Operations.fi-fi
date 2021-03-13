---
title: Määritä Dataverse -virtuaalitaulukot
description: Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin virtuaalitaulukoiden määrittämistä. Virtuaalitaulukoiden luominen ja aiemmin luotujen päivittäminen sekä luotujen ja käytettävissä olevien taulukoiden analysoiminen.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
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
ms.openlocfilehash: cd299b51e38cc30c3e18f3ef9de1f43fa817b840
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112419"
---
# <a name="configure-dataverse-virtual-tables"></a><span data-ttu-id="f233c-104">Määritä Dataverse -virtuaalitaulukot</span><span class="sxs-lookup"><span data-stu-id="f233c-104">Configure Dataverse virtual tables</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f233c-105">Dynamics 365 Human Resources on Microsoft Dataversen virtuaalinen tietolähde.</span><span class="sxs-lookup"><span data-stu-id="f233c-105">Dynamics 365 Human Resources is a virtual data source in Microsoft Dataverse.</span></span> <span data-ttu-id="f233c-106">Se sisältää Dataversen ja Microsoft Power Platformin täydet CRUD (luonti, luku, päivitys ja poisto) -toiminnot.</span><span class="sxs-lookup"><span data-stu-id="f233c-106">It provides full create, read, update, and delete (CRUD) operations from Dataverse and Microsoft Power Platform.</span></span> <span data-ttu-id="f233c-107">Virtuaalitaulukoiden tietoja ei tallenneta Dataverseen vaan sovelluksen tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="f233c-107">The data for virtual tables isn't stored in Dataverse, but in the application database.</span></span>

<span data-ttu-id="f233c-108">Jos haluat ottaa Dataversen Human Resources -yksiköiden CRUD-toiminnot käyttää, yksiköiden on oltava käytettävissä virtuaalitaulukkoina Dataversessa.</span><span class="sxs-lookup"><span data-stu-id="f233c-108">To enable CRUD operations on Human Resources entities from Dataverse, you must make the entities available as virtual tables in Dataverse.</span></span> <span data-ttu-id="f233c-109">Voit suorittaa tällä tavoin Dataversen ja Microsoft Power Platformin CRUD-toimintoja Human Resourcesin tiedoissa.</span><span class="sxs-lookup"><span data-stu-id="f233c-109">This lets you perform CRUD operations from Dataverse and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="f233c-110">Toiminnot tukevat myös Human Resourcesin liiketoimintalogiikan tarkistuksia, joilla varmistetaan tietojen eheys kirjoitettaessa tietoja yksiköihin.</span><span class="sxs-lookup"><span data-stu-id="f233c-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

> [!NOTE]
> <span data-ttu-id="f233c-111">Human Resources -yksiköt vastaavat Dataverse-tauluja.</span><span class="sxs-lookup"><span data-stu-id="f233c-111">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="f233c-112">Lisätietoja Dataversesta (aiemmin Common Data Service) ja terminologiapäivityksistä on kohdassa [Mikä on Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="f233c-112">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

## <a name="available-virtual-tables-for-human-resources"></a><span data-ttu-id="f233c-113">Human Resourcesin käytettävissä olevat virtuaalitaulukot</span><span class="sxs-lookup"><span data-stu-id="f233c-113">Available virtual tables for Human Resources</span></span>

<span data-ttu-id="f233c-114">Kaikki Human Resourcesin OData (Open Data Protocol) -yksiköt ovat käytettävissä virtuaalitaulukkoina Dataversessa.</span><span class="sxs-lookup"><span data-stu-id="f233c-114">All Open Data Protocol (OData) entities in Human Resources are available as virtual tables in Dataverse.</span></span> <span data-ttu-id="f233c-115">Ne ovat käytettävissä myös Power Platformissa.</span><span class="sxs-lookup"><span data-stu-id="f233c-115">They're also available in Power Platform.</span></span> <span data-ttu-id="f233c-116">Voit nyt muodostaa sovelluksia ja kokemuksia käyttämällä tietoja suoraan Human Resourcesissa CRUD-ominaisuuksien avulla ilman, että tiedot kopioitava ja synkronoitava Dataverseen.</span><span class="sxs-lookup"><span data-stu-id="f233c-116">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Dataverse.</span></span> <span data-ttu-id="f233c-117">Voit muodostaa Power Apps -portaalien avulla ulkoisia sivustoja, joiden avulla voidaan toteuttaa liiketoimintaprosessien yhteistyöskenaarioita Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="f233c-117">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="f233c-118">Voit tarkastella ympäristössä käyttöönotettujen virtuaalitaulukoiden luetteloa ja aloittaa [Power Appsin](https://make.powerapps.com) taulukoiden käyttämisen **Dynamics 365 HR -virtuaalitaulukoiden** ratkaisussa.</span><span class="sxs-lookup"><span data-stu-id="f233c-118">You can view the list of virtual tables enabled in the environment, and begin working with the tables in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Tables** solution.</span></span>

![Dynamics 365 HR -virtuaalitaulukot Power Appsissa](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a><span data-ttu-id="f233c-120">Virtuaalitaulut ja alkuperäiset taulut</span><span class="sxs-lookup"><span data-stu-id="f233c-120">Virtual tables versus native tables</span></span>

<span data-ttu-id="f233c-121">Human Resourcesin virtuaalitaulukot eivät ole samoja kuin Human Resourcesille luodut alkuperäiset Dataversen taulukot.</span><span class="sxs-lookup"><span data-stu-id="f233c-121">Virtual tables for Human Resources aren't the same as the native Dataverse tables created for Human Resources.</span></span> 

<span data-ttu-id="f233c-122">Human Resourcesin alkuperäiset taulukot luodaan erikseen ja niitä ylläpidetään HCM Common -ratkaisussa Dataversessa.</span><span class="sxs-lookup"><span data-stu-id="f233c-122">The native tables for Human Resources are generated separately and maintained in the HCM Common solution in Dataverse.</span></span> <span data-ttu-id="f233c-123">Aluperäisissä taulukoissa tiedot tallennetaan Dataversessa, ja ne on synkronoitava Human Resourcesin sovellustietokannassa.</span><span class="sxs-lookup"><span data-stu-id="f233c-123">With native tables, the data is stored in Dataverse and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="f233c-124">Alkuperäisten Human Resourcesin Dataverse -taulukoiden luettelo on kohdassa [Dataverse-taulukot](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="f233c-124">For a list of the native Dataverse tables for Human Resources, see [Dataverse tables](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="f233c-125">Luo perustiedot</span><span class="sxs-lookup"><span data-stu-id="f233c-125">Setup</span></span>

<span data-ttu-id="f233c-126">Ota virtuaalitaulukot käyttöön ympäristössä tekemällä seuraavat määritykset.</span><span class="sxs-lookup"><span data-stu-id="f233c-126">Follow these setup steps to enable virtual tables in your environment.</span></span>

### <a name="enable-virtual-tables-in-human-resources"></a><span data-ttu-id="f233c-127">Human Resourcesin virtuaalitaulukoiden käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="f233c-127">Enable virtual tables in Human Resources</span></span>

<span data-ttu-id="f233c-128">Ensin on otettava käyttöön virtuaalitaulukot **Ominaisuuksien hallinta** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="f233c-128">First, you must enable virtual tables in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="f233c-129">Valitse Human Resourcesissa **Järjestelmän hallinta**.</span><span class="sxs-lookup"><span data-stu-id="f233c-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="f233c-130">Valitse **Ominaisuuksien hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="f233c-130">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="f233c-131">Valitse **Dataversen virtuaalitaulukon tuki HR:lle** ja valitse sitten **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="f233c-131">Select **Virtual table support for HR in Dataverse**, and then select **Enable**.</span></span>

<span data-ttu-id="f233c-132">Lisätietoja ominaisuuksien ottamisesta käyttöön ja poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="f233c-132">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="f233c-133">Sovelluksen rekisteröinti Microsoft Azuressa</span><span class="sxs-lookup"><span data-stu-id="f233c-133">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="f233c-134">Human Resources -esiintymä on rekisteröitävä Azure-portaalissa, jotta Microsoftin käyttäjätietoympäristö voi toimittaa todennus- ja valtuutuspalvelut sovellukselle ja käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="f233c-134">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="f233c-135">Lisätietoja sovellusten rekisteröinnistä Azuressa on kohdassa [Pika-aloitus: Sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristöön](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="f233c-135">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="f233c-136">Avaa [Microsoft Azure -portaali](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="f233c-136">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="f233c-137">Valitse Azure-palveluluettelossa **Sovelluksen rekisteröinnit**.</span><span class="sxs-lookup"><span data-stu-id="f233c-137">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="f233c-138">Valitse **Uusi rekisteröinti**.</span><span class="sxs-lookup"><span data-stu-id="f233c-138">Select **New registration**.</span></span>

4. <span data-ttu-id="f233c-139">Kirjoita **Nimi**-kenttään sovellusta kuvaava nimi.</span><span class="sxs-lookup"><span data-stu-id="f233c-139">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="f233c-140">Esimerkki: **Dynamics 365 Human Resourcesin virtuaalitaulukot**.</span><span class="sxs-lookup"><span data-stu-id="f233c-140">For example, **Dynamics 365 Human Resources Virtual Tables**.</span></span>

5. <span data-ttu-id="f233c-141">Anna **Uudelleenohjauksen URI** -kenttään Human Resources -esiintymän nimitilan URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="f233c-141">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="f233c-142">Valitse **Rekisteröi**.</span><span class="sxs-lookup"><span data-stu-id="f233c-142">Select **Register**.</span></span>

7. <span data-ttu-id="f233c-143">Kun rekisteröinti valmistuu, Azure-portaali näyttää sovelluksen rekisteröinnin **Yleiskatsaus**-ruudussa, joka sisältää myös sen **sovelluksen (asiakasohjelman) tunnuksen**.</span><span class="sxs-lookup"><span data-stu-id="f233c-143">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="f233c-144">Kirjoita muistiin tämä **sovelluksen (asiakasohjelman) tunnus**.</span><span class="sxs-lookup"><span data-stu-id="f233c-144">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="f233c-145">Nämä tiedot annetaan, kun [määrität virtuaalitaulukon tietolähteen](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="f233c-145">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

8. <span data-ttu-id="f233c-146">Valitse vasemmassa siirtymisruudussa **Varmenteet ja salaiset koodit**.</span><span class="sxs-lookup"><span data-stu-id="f233c-146">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="f233c-147">Valitse sivun **Asiakasohjelman salasana** -osassa **Uusi asiakasohjelman salasana**.</span><span class="sxs-lookup"><span data-stu-id="f233c-147">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="f233c-148">Anna kuvaus, valitse kesto ja valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="f233c-148">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="f233c-149">Kirjaa salaisen koodin arvo muistiin.</span><span class="sxs-lookup"><span data-stu-id="f233c-149">Record the secret's value.</span></span> <span data-ttu-id="f233c-150">Nämä tiedot annetaan, kun [määrität virtuaalitaulukon tietolähteen](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="f233c-150">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="f233c-151">Muista kirjoittaa salaisen koodin arvo muistiin tässä vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="f233c-151">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="f233c-152">Salaista koodi ei näytetä sen jälkeen, kun poistut sivulta.</span><span class="sxs-lookup"><span data-stu-id="f233c-152">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a><span data-ttu-id="f233c-153">Dynamics 365 HR Virtual Table -sovelluksen asentaminen</span><span class="sxs-lookup"><span data-stu-id="f233c-153">Install the Dynamics 365 HR Virtual Table app</span></span>

<span data-ttu-id="f233c-154">Asenna Dynamics 365 HR Virtual Table -sovellus Power Apps -ympäristöön ottamaan virtuaalitaulukon ratkaisupaketti käyttöön Dataversessa.</span><span class="sxs-lookup"><span data-stu-id="f233c-154">Install the Dynamics 365 HR Virtual Table app in your Power Apps environment to deploy the virtual table solution package to Dataverse.</span></span>

1. <span data-ttu-id="f233c-155">Avaa [Power Platform -hallintakeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="f233c-155">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="f233c-156">Valitse **Ympäristöt**-luettelossa Human Resources -esiintymään liitetty Power Apps -ympäristö.</span><span class="sxs-lookup"><span data-stu-id="f233c-156">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="f233c-157">Valitse sivun **Resurssit**-osassa **Dynamics 365 -sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="f233c-157">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="f233c-158">Valitse **Asenna sovellus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f233c-158">Select the **Install app** action.</span></span>

5. <span data-ttu-id="f233c-159">Valitse ensin **Dynamics 365 HR Virtual Table** ja valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="f233c-159">Select **Dynamics 365 HR Virtual Table**, and select **Next**.</span></span>

6. <span data-ttu-id="f233c-160">Tutustu palvelun käyttöehtoihin ja merkitse ne hyväksytyiksi.</span><span class="sxs-lookup"><span data-stu-id="f233c-160">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="f233c-161">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="f233c-161">Select **Install**.</span></span>

<span data-ttu-id="f233c-162">Asennus kestää muutaman minuutin.</span><span class="sxs-lookup"><span data-stu-id="f233c-162">The install takes a few minutes.</span></span> <span data-ttu-id="f233c-163">Kun asennus valmistuu, jatka seuraaviin vaiheisiin.</span><span class="sxs-lookup"><span data-stu-id="f233c-163">When it completes, continue to the next steps.</span></span>

![Dynamics 365 HR Virtual Table -sovelluksen asentaminen Power Platform -hallintakeskuksessa](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-table-data-source"></a><span data-ttu-id="f233c-165">Virtuaalitaulukon tietolähteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f233c-165">Configure the virtual table data source</span></span> 

<span data-ttu-id="f233c-166">Seuraavaksi määritetään virtuaalitaulukon tietolähde Power Apps -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="f233c-166">The next step is to configure the virtual table data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="f233c-167">Avaa [Power Platform -hallintakeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="f233c-167">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="f233c-168">Valitse **Ympäristöt**-luettelossa Human Resources -esiintymään liitetty Power Apps -ympäristö.</span><span class="sxs-lookup"><span data-stu-id="f233c-168">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="f233c-169">Valitse **Ympäristön URL-osoite** sivun **Tiedot**-osassa.</span><span class="sxs-lookup"><span data-stu-id="f233c-169">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="f233c-170">Valitse **Ratkaisun kunnon keskus** -kohdassa **Erikoishaku**-kuvake sovellussivun oikeassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="f233c-170">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="f233c-171">Valitse **Erikoishaku**-sivun avattavassa **Etsi**-luettelossa **Finance and Operations -virtuaalitietolähteen määritykset**.</span><span class="sxs-lookup"><span data-stu-id="f233c-171">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="f233c-172">Valitse **Tulokset**.</span><span class="sxs-lookup"><span data-stu-id="f233c-172">Select **Results**.</span></span>

7. <span data-ttu-id="f233c-173">Valitse **Microsoft HR -tietolähde** -tietue.</span><span class="sxs-lookup"><span data-stu-id="f233c-173">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="f233c-174">Anna tietolähteen määrityksessä seuraavat tarvittavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="f233c-174">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="f233c-175">**Kohde-URL**: Human Resources -nimitilan URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="f233c-175">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="f233c-176">Kohde-URL-osoitteen muoto on seuraava:</span><span class="sxs-lookup"><span data-stu-id="f233c-176">The format of the target URL is:</span></span>
     
     <span data-ttu-id="f233c-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="f233c-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="f233c-178">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="f233c-178">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="f233c-179">Virheiden välttämiseksi varmista, että URL-osoittee lopussa on merkki **/**.</span><span class="sxs-lookup"><span data-stu-id="f233c-179">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="f233c-180">**Vuokraajan tunnus**: Azure Active Directory (Azure AD) -vuokraajan tunnus.</span><span class="sxs-lookup"><span data-stu-id="f233c-180">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="f233c-181">**AAD-sovelluksen tunnus**: Microsoft Azure -portaalissa rekisteröidylle sovellukselle luotu sovelluksen (asiakaspalvelijan) tunnus.</span><span class="sxs-lookup"><span data-stu-id="f233c-181">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="f233c-182">Saint nämä tiedot aiemman [Sovelluksen rekisteröinti Microsoft Azuressa](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) -vaiheen aikana.</span><span class="sxs-lookup"><span data-stu-id="f233c-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="f233c-183">**AAD-sovelluksen salainen koodi**: Microsoft Azure -portaalissa rekisteröidylle sovellukselle luotu asiakasohjelman salasana.</span><span class="sxs-lookup"><span data-stu-id="f233c-183">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="f233c-184">Saint nämä tiedot aiemman [Sovelluksen rekisteröinti Microsoft Azuressa](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) -vaiheen aikana.</span><span class="sxs-lookup"><span data-stu-id="f233c-184">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Microsoft HR -tietolähde](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="f233c-186">Valitse **Tallenna ja sulje**.</span><span class="sxs-lookup"><span data-stu-id="f233c-186">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="f233c-187">Sovelluksen oikeuksien myöntäminen Human Resourcesissa</span><span class="sxs-lookup"><span data-stu-id="f233c-187">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="f233c-188">Myönnä kahden Azure AD -sovelluksen oikeudet Human Resourcesissa:</span><span class="sxs-lookup"><span data-stu-id="f233c-188">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="f233c-189">Vuokraajalle Microsoft Azure -portaalissa luotu sovellus</span><span class="sxs-lookup"><span data-stu-id="f233c-189">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="f233c-190">Power Apps -ympäristössä asennettu Dynamics 365 HR Virtual Table -sovellus</span><span class="sxs-lookup"><span data-stu-id="f233c-190">The Dynamics 365 HR Virtual Table app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="f233c-191">Avaa Human Resourcesissa **Azure Active Directory -sovellukset** -sivu.</span><span class="sxs-lookup"><span data-stu-id="f233c-191">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="f233c-192">Luo uusi sovellustietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f233c-192">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="f233c-193">Anna **Asiakastunnus**-kentässä Microsoft Azure -portaalissa rekisteröidyn sovelluksen asiakastunnus.</span><span class="sxs-lookup"><span data-stu-id="f233c-193">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="f233c-194">Anna **Nimi**-kentässä Microsoft Azure -portaalissa rekisteröidyn sovelluksen nimi.</span><span class="sxs-lookup"><span data-stu-id="f233c-194">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="f233c-195">Valitse **Käyttäjätunnus**-kentässä sellaisen käyttäjän käyttäjätunnus, jolla on Human Resources- ja Power Apps -ympäristön järjestelmänvalvojan käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="f233c-195">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="f233c-196">Luo toinen sovellustietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f233c-196">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="f233c-197">**Asiakastunnus**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="f233c-197">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="f233c-198">**Nimi**: Dynamics 365 HR Virtual Table</span><span class="sxs-lookup"><span data-stu-id="f233c-198">**Name**: Dynamics 365 HR Virtual Table</span></span>
    - <span data-ttu-id="f233c-199">Valitse **Käyttäjätunnus**-kentässä sellaisen käyttäjän käyttäjätunnus, jolla on Human Resources- ja Power Apps -ympäristön järjestelmänvalvojan käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="f233c-199">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-tables"></a><span data-ttu-id="f233c-200">Virtuaalitaulukoiden luominen</span><span class="sxs-lookup"><span data-stu-id="f233c-200">Generate virtual tables</span></span>

<span data-ttu-id="f233c-201">Voit valita asennuksen valmistumisen jälkeen virtuaalitaulukot, jotka haluat luoda ja ottaa käyttöön Dataverse -esiintymässä.</span><span class="sxs-lookup"><span data-stu-id="f233c-201">When setup completes, you can select the virtual tables you want to generate and enable in your Dataverse instance.</span></span>

1. <span data-ttu-id="f233c-202">Avaa Human Resourcesissa **Dataverse-integraatio** -sivu.</span><span class="sxs-lookup"><span data-stu-id="f233c-202">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="f233c-203">Valitse **Virtuaalitaulukot**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="f233c-203">Select the **Virtual tables** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="f233c-204">**Ota virtuaalitaulukot käyttöön** -tilanvaihtopainike on automaattisesti **Kyllä**-asennossa, kun kaikki tarvittavat määritykset on tehty.</span><span class="sxs-lookup"><span data-stu-id="f233c-204">The **Enable virtual tables** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="f233c-205">Jos tilanvaihtopainike on **Ei**-asennossa, tarkista tämä asiakirjan edellisten osien vaiheet ja varmista, että kaikki edellytettävät asetukset on määritetty.</span><span class="sxs-lookup"><span data-stu-id="f233c-205">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="f233c-206">Valitse Dataversessa luotava taulukko tai luotavat taulukot.</span><span class="sxs-lookup"><span data-stu-id="f233c-206">Select the table or tables you want to generate in Dataverse.</span></span>

4. <span data-ttu-id="f233c-207">Valitse **Luo/päivitä**.</span><span class="sxs-lookup"><span data-stu-id="f233c-207">Select **Generate/refresh**.</span></span>

![Dataverse -integraatio](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-table-generation-status"></a><span data-ttu-id="f233c-209">Taulukon luontitilan tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="f233c-209">Check table generation status</span></span>

<span data-ttu-id="f233c-210">Virtuaalitaulukot luodaan Dataversessa asynkronisena taustaprosessina.</span><span class="sxs-lookup"><span data-stu-id="f233c-210">Virtual tables are generated in Dataverse through an asynchronous background process.</span></span> <span data-ttu-id="f233c-211">Prosessin päivitykset näkyvät toimintokeskuksessa.</span><span class="sxs-lookup"><span data-stu-id="f233c-211">Updates on the process display in the action center.</span></span> <span data-ttu-id="f233c-212">Prosessin tiedot, kuten virhelokit, näkyvät **Prosessin automatisoinnit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="f233c-212">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="f233c-213">Avaa Human Resourcesissa **Prosessin automatisoinnit** -sivu.</span><span class="sxs-lookup"><span data-stu-id="f233c-213">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="f233c-214">Valitse **Taustaprosessit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="f233c-214">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="f233c-215">Valitse **Virtuaalitaulukon kyselyn asynkroninen toiminnon taustaprosessi**.</span><span class="sxs-lookup"><span data-stu-id="f233c-215">Select **Virtual table poll async operation background process**.</span></span>

4. <span data-ttu-id="f233c-216">Valitse **Näytä viimeisimmät tulokset**.</span><span class="sxs-lookup"><span data-stu-id="f233c-216">Select **View most recent results**.</span></span>

<span data-ttu-id="f233c-217">Esiin tulevassa ruudussa näkyy prosessin viimeksi suoritetut tulokset.</span><span class="sxs-lookup"><span data-stu-id="f233c-217">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="f233c-218">Voit tarkastella prosessin lokia, mukaan lukien mahdollisia Dataversen palauttamia virheitä.</span><span class="sxs-lookup"><span data-stu-id="f233c-218">You can view the log for the process, including any errors returned from Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="f233c-219">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="f233c-219">See also</span></span>

[<span data-ttu-id="f233c-220">Mikä on Dataverse?</span><span class="sxs-lookup"><span data-stu-id="f233c-220">What is Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="f233c-221">Taulut Dataversessa</span><span class="sxs-lookup"><span data-stu-id="f233c-221">Tables in Dataverse</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="f233c-222">Taulukkosuhteiden yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f233c-222">Table relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="f233c-223">Ulkoisten tietolähteiden tietoja sisältävien virtuaalitaulukoiden luominen ja muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="f233c-223">Create and edit virtual tables that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="f233c-224">Mitä Power Apps -portaalit ovat?</span><span class="sxs-lookup"><span data-stu-id="f233c-224">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="f233c-225">Yleiskatsaus sovellusten luonnista Power Appsissa</span><span class="sxs-lookup"><span data-stu-id="f233c-225">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
