---
title: Päivitä osapuolen osoitekirja ja yleinen osoitekirja
description: Tässä ohjeaiheessa kuvataan, kuinka kaksoiskirjoitustiedot päivitetään osapuolen ja globaaliin osoitekirjamalliin.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 90ddbe704ab21d62752b581a813601e8986c2103
ms.sourcegitcommit: 180548e3c10459776cf199989d3753e0c1555912
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2021
ms.locfileid: "6112670"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="d1379-103">Päivitä osapuolen osoitekirja ja yleinen osoitekirja</span><span class="sxs-lookup"><span data-stu-id="d1379-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d1379-104">[Microsoft Azure Data Factory -malli](https://aka.ms/dual-write-gab-adf) auttaa päivittämään aiemmin luodun **Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-taulun tiedot kaksoiskirjoitusmallin osapuolen ja yleisen osoitekirjamallin avulla.</span><span class="sxs-lookup"><span data-stu-id="d1379-104">The [Microsoft Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="d1379-105">Malli täsmäyttää sekä finance and operations- että customer engagement -sovellusten tiedot.</span><span class="sxs-lookup"><span data-stu-id="d1379-105">The template reconciles the data from both finance and operations apps and customer engagement applications.</span></span> <span data-ttu-id="d1379-106">Prosessin lopussa luodaan **osapuolen** tietueiden **osapuoli**- ja **yhteyshenkilö** kentät ja liitetään asiakkaan varaushakemusten **Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-tietueisiin.</span><span class="sxs-lookup"><span data-stu-id="d1379-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="d1379-107">.csv-tiedosto (`FONewParty.csv`) luodaan luomaan uudet **osapuoli**-tietueet finance and operations -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="d1379-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the finance and operations app.</span></span> <span data-ttu-id="d1379-108">Tämä ohjeaihe sisältää Data Factory -mallissa käytettävät ohjeet ja tietojen päivittämisen.</span><span class="sxs-lookup"><span data-stu-id="d1379-108">This topic provides instructions about how to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="d1379-109">Jos mukautuksia ei ole, voit käyttää mallia niin kuin se on.</span><span class="sxs-lookup"><span data-stu-id="d1379-109">If you don’t have any customizations, you can use the template as is.</span></span> <span data-ttu-id="d1379-110">Jos olet muokannut **tiliä**, **yhteyshenkilöä** ja **toimittajaa**, sinun on muokattava mallia seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="d1379-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!NOTE]
> <span data-ttu-id="d1379-111">Malli päivittää vain **osapuolen** tiedot.</span><span class="sxs-lookup"><span data-stu-id="d1379-111">The template only upgrades the **Party** data.</span></span> <span data-ttu-id="d1379-112">Tulevat posti- ja sähköiset osoitteet sisällytetään julkaisuun.</span><span class="sxs-lookup"><span data-stu-id="d1379-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d1379-113">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="d1379-113">Prerequisites</span></span>

<span data-ttu-id="d1379-114">Seuraavien edellytysten on täytyttävä osapuolen ja yleisen osoitekirjamallin päivittämisessä:</span><span class="sxs-lookup"><span data-stu-id="d1379-114">The following prerequisites are required to upgrade to the party and global address book model:</span></span>

+ [<span data-ttu-id="d1379-115">Azure-tilaus</span><span class="sxs-lookup"><span data-stu-id="d1379-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="d1379-116">Mallin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="d1379-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="d1379-117">Sinun tulee olla aiemmin luotu kaksoiskirjoitusasiakas.</span><span class="sxs-lookup"><span data-stu-id="d1379-117">You must be an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="d1379-118">Päivityksen valmistelu</span><span class="sxs-lookup"><span data-stu-id="d1379-118">Prepare for the upgrade</span></span>
<span data-ttu-id="d1379-119">Päivitystä varten tarvitaan seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="d1379-119">The following activities are needed to prepare for the upgrade:</span></span>

+ <span data-ttu-id="d1379-120">**Täysin synkronoitu**: Molemmat ympäristöt ovat täysin synkronoituja **Tilin (Asiakas)**, **Yhteyshenkilön** ja **Toimittajan** kanssa.</span><span class="sxs-lookup"><span data-stu-id="d1379-120">**Fully synced**: Both environments are in a fully synced state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="d1379-121">**Integrointiavaimet**: **Tili (Asiakas)**-, **Yhteyshenkilö**- ja **Toimittaja**-taulut Customer Engagement -sovelluksessa käyttävät valmiita integrointiavaimia.</span><span class="sxs-lookup"><span data-stu-id="d1379-121">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="d1379-122">Jos olet mukauttanut integrointiavaimia, mukauta mallia.</span><span class="sxs-lookup"><span data-stu-id="d1379-122">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="d1379-123">**Osapuolinumero**: Kaikki päivitettävät **Tili (asiakas)**-, **yhteyshenkilö**- ja **toimittaja**-tietueet saavat **osapuoli** numeron.</span><span class="sxs-lookup"><span data-stu-id="d1379-123">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="d1379-124">Tietueet, joissa ei ole **osapuolen** numeroa, ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="d1379-124">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="d1379-125">Jos haluat päivittää nämä tietueet, lisää niille **osapuolen** numero ennen päivitysprosessin käynnistämistä.</span><span class="sxs-lookup"><span data-stu-id="d1379-125">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="d1379-126">**Järjestelmän käyttökomento**: Ota päivitysprosessin aikana sekä finance and operations- että customer engagement -ympäristöt offline-tilaan.</span><span class="sxs-lookup"><span data-stu-id="d1379-126">**System outage**: During the upgrade process, you will have to take both the finance and operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="d1379-127">**Tilannekuva**: Ota tilannekuvia sekä finance and operations- että customer engagement -sovelluksista.</span><span class="sxs-lookup"><span data-stu-id="d1379-127">**Snapshot**: Take snapshots of both the finance and operations apps and customer engagement apps.</span></span> <span data-ttu-id="d1379-128">Voit tarvittaessa palauttaa edellisen tilan tilannekuvasten avulla.</span><span class="sxs-lookup"><span data-stu-id="d1379-128">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="d1379-129">Käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="d1379-129">Deployment</span></span>

1. <span data-ttu-id="d1379-130">Lataa malli [Dynamics-365-FastTrack-käyttöönotto-käyttöomaisuus](https://aka.ms/dual-write-gab-adf) -kentästä.</span><span class="sxs-lookup"><span data-stu-id="d1379-130">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="d1379-131">Kirjaudu [Microsoft Azure -palveluun](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="d1379-131">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="d1379-132">[Resurssiryhmän](/azure/azure-resource-manager/management/manage-resource-groups-portal) luonti.</span><span class="sxs-lookup"><span data-stu-id="d1379-132">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="d1379-133">Luo [tallennustili](/azure/storage/common/storage-account-create?tabs=azure-portal) luomallesi resurssiryhmälle.</span><span class="sxs-lookup"><span data-stu-id="d1379-133">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="d1379-134">Luo [Data Factory](/azure/data-factory/quickstart-create-data-factory-portal) yllä luomallesi resurssiryhmälle.</span><span class="sxs-lookup"><span data-stu-id="d1379-134">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="d1379-135">Avaa Data Factory ja valitse **Tee & valvo** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="d1379-135">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="d1379-136">Valitse **Hallinta**-välilehdestä **ARM-malli**.</span><span class="sxs-lookup"><span data-stu-id="d1379-136">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="d1379-137">Tuo **osapuolen** malli valitsemalla **Tuo ARM -malli**.</span><span class="sxs-lookup"><span data-stu-id="d1379-137">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="d1379-138">Tuo malli data factoryyn.</span><span class="sxs-lookup"><span data-stu-id="d1379-138">Import the template into the data factory.</span></span> <span data-ttu-id="d1379-139">Määritä seuraavat arvot **projektitietoja** ja **esiintymän tietoja** varten.</span><span class="sxs-lookup"><span data-stu-id="d1379-139">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="d1379-140">Kenttä</span><span class="sxs-lookup"><span data-stu-id="d1379-140">Field</span></span> | <span data-ttu-id="d1379-141">Arvo</span><span class="sxs-lookup"><span data-stu-id="d1379-141">Value</span></span>
    ---|---
    <span data-ttu-id="d1379-142">Tilaus</span><span class="sxs-lookup"><span data-stu-id="d1379-142">Subscription</span></span> | <span data-ttu-id="d1379-143">Azure-tilaus</span><span class="sxs-lookup"><span data-stu-id="d1379-143">Azure subscription</span></span>
    <span data-ttu-id="d1379-144">Resurssiryhmä</span><span class="sxs-lookup"><span data-stu-id="d1379-144">Resource group</span></span> | <span data-ttu-id="d1379-145">Anna sama resurssi, jolle tallennustili luodaan.</span><span class="sxs-lookup"><span data-stu-id="d1379-145">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="d1379-146">Alue</span><span class="sxs-lookup"><span data-stu-id="d1379-146">Region</span></span> | <span data-ttu-id="d1379-147">Määritä alue.</span><span class="sxs-lookup"><span data-stu-id="d1379-147">Specify region.</span></span>
    <span data-ttu-id="d1379-148">Tehtaan nimi</span><span class="sxs-lookup"><span data-stu-id="d1379-148">Factory Name</span></span> | <span data-ttu-id="d1379-149">Määritä tehtaan nimi.</span><span class="sxs-lookup"><span data-stu-id="d1379-149">Specify factory name.</span></span>
    <span data-ttu-id="d1379-150">FO-yhdistetyn palvelun pääavain</span><span class="sxs-lookup"><span data-stu-id="d1379-150">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="d1379-151">Määritä sovelluksen avain.</span><span class="sxs-lookup"><span data-stu-id="d1379-151">Specify the application's key.</span></span>
    <span data-ttu-id="d1379-152">Azure Blob-objektisäilön yhteysmerkkijonot</span><span class="sxs-lookup"><span data-stu-id="d1379-152">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="d1379-153">Azure Blob-objektisäilön yhteysmerkkijonot.</span><span class="sxs-lookup"><span data-stu-id="d1379-153">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="d1379-154">Dynamics Crm:n linkitetty palvelusalasana</span><span class="sxs-lookup"><span data-stu-id="d1379-154">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="d1379-155">Käyttäjäksi määritetyn käyttäjätilin salasana.</span><span class="sxs-lookup"><span data-stu-id="d1379-155">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="d1379-156">FO Linked Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="d1379-156">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="d1379-157">FO Linked Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="d1379-157">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="d1379-158">Määritä vuokraajan tiedot (toimialueen nimi tai vuokraajan tunnus), jota hakemuksesi käyttää.</span><span class="sxs-lookup"><span data-stu-id="d1379-158">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="d1379-159">FO Linked Service_properties_type Properties_aad Resource Id</span><span class="sxs-lookup"><span data-stu-id="d1379-159">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="d1379-160">FO Linked Service_properties_type Properties_service Principal Id</span><span class="sxs-lookup"><span data-stu-id="d1379-160">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="d1379-161">Määritä sovelluksen asiakkaan tunnus.</span><span class="sxs-lookup"><span data-stu-id="d1379-161">Specify the application's client ID.</span></span>
    <span data-ttu-id="d1379-162">Dynamics Crm Linked Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="d1379-162">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="d1379-163">Dynamics 365 -yhteyden muodostanut käyttäjänimi.</span><span class="sxs-lookup"><span data-stu-id="d1379-163">The username to connect to Dynamics 365.</span></span>

    <span data-ttu-id="d1379-164">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="d1379-164">For additional information, refer to the following topics:</span></span> 
    
    - [<span data-ttu-id="d1379-165">Resource Manager -mallin manuaalinen luominen kullekin ympäristölle</span><span class="sxs-lookup"><span data-stu-id="d1379-165">Manually promote a Resource Manager template for each environment</span></span>](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [<span data-ttu-id="d1379-166">Linkitetyt huollon ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="d1379-166">Linked service properties</span></span>](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [<span data-ttu-id="d1379-167">Tietojen kopioiminen Azure Data Factoryn avulla</span><span class="sxs-lookup"><span data-stu-id="d1379-167">Copy data using Azure Data Factory</span></span>](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. <span data-ttu-id="d1379-168">Tarkista käyttöönoton jälkeen tietojoukot, tietovuo ja data factoryn linkitetty palvelu.</span><span class="sxs-lookup"><span data-stu-id="d1379-168">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Tietojoukot, tietovuo ja linkitetty palvelu](media/data-factory-validate.png)

11. <span data-ttu-id="d1379-170">Siirry kohtaan **Hallitse**.</span><span class="sxs-lookup"><span data-stu-id="d1379-170">Navigate to **Manage**.</span></span> <span data-ttu-id="d1379-171">Valitse **Yhteydet**-kohdasta **Linkitetty palvelu**.</span><span class="sxs-lookup"><span data-stu-id="d1379-171">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="d1379-172">Valitse **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="d1379-172">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="d1379-173">Syötä **Muokkaa linkitettyä palvelua (Dynamics CRM)** -lomakkeeseen seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="d1379-173">In the **Edit linked service (Dynamics CRM)** form, enter the following values.</span></span>

    <span data-ttu-id="d1379-174">Kenttä</span><span class="sxs-lookup"><span data-stu-id="d1379-174">Field</span></span> | <span data-ttu-id="d1379-175">Arvo</span><span class="sxs-lookup"><span data-stu-id="d1379-175">Value</span></span>
    ---|---
    <span data-ttu-id="d1379-176">Nimi</span><span class="sxs-lookup"><span data-stu-id="d1379-176">Name</span></span> | <span data-ttu-id="d1379-177">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="d1379-177">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="d1379-178">kuvaus</span><span class="sxs-lookup"><span data-stu-id="d1379-178">Description</span></span> | <span data-ttu-id="d1379-179">Linkitetyt palvelut, jotka yhdistetään CRM-instanssiin yksikkötietojen hakemista varten</span><span class="sxs-lookup"><span data-stu-id="d1379-179">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="d1379-180">Yhdistä integroinnin suorituspalvelun kautta</span><span class="sxs-lookup"><span data-stu-id="d1379-180">Connect via integration runtime</span></span> | <span data-ttu-id="d1379-181">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d1379-181">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="d1379-182">Käyttöönottotyyppi</span><span class="sxs-lookup"><span data-stu-id="d1379-182">Deployment type</span></span> | <span data-ttu-id="d1379-183">Yhdistetty</span><span class="sxs-lookup"><span data-stu-id="d1379-183">Online</span></span>
    <span data-ttu-id="d1379-184">Palvelu-Uri</span><span class="sxs-lookup"><span data-stu-id="d1379-184">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="d1379-185">Todennustyyppi</span><span class="sxs-lookup"><span data-stu-id="d1379-185">Authentication type</span></span> | <span data-ttu-id="d1379-186">Office365</span><span class="sxs-lookup"><span data-stu-id="d1379-186">Office365</span></span>
    <span data-ttu-id="d1379-187">Käyttäjänimi</span><span class="sxs-lookup"><span data-stu-id="d1379-187">User name</span></span> |
    <span data-ttu-id="d1379-188">Salasana tai Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="d1379-188">Password or Azure Key Vault</span></span> | <span data-ttu-id="d1379-189">Salasana</span><span class="sxs-lookup"><span data-stu-id="d1379-189">Password</span></span>
    <span data-ttu-id="d1379-190">Salasana</span><span class="sxs-lookup"><span data-stu-id="d1379-190">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="d1379-191">Suorita malli</span><span class="sxs-lookup"><span data-stu-id="d1379-191">Run the template</span></span>

1. <span data-ttu-id="d1379-192">Lopeta Finance and Operations -sovelluksen avulla seuraava **Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-kaksoiskirjoituksen yhdistelmä.</span><span class="sxs-lookup"><span data-stu-id="d1379-192">Stop the following **Account**, **Contact**, and **Vendor** dual-write maps using the Finance and Operations app.</span></span>

    + <span data-ttu-id="d1379-193">Asiakkaat V3 (accounts)</span><span class="sxs-lookup"><span data-stu-id="d1379-193">Customers V3(accounts)</span></span>
    + <span data-ttu-id="d1379-194">Asiakkaat V3 (yhteyshenkilöt)</span><span class="sxs-lookup"><span data-stu-id="d1379-194">Customers V3(contacts)</span></span>
    + <span data-ttu-id="d1379-195">CDS-kontaktit V2 (yhteyshenkilöt)</span><span class="sxs-lookup"><span data-stu-id="d1379-195">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="d1379-196">CDS-kontaktit V2 (yhteyshenkilöt)</span><span class="sxs-lookup"><span data-stu-id="d1379-196">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="d1379-197">Toimittajat V2 (msdyn_vendors)</span><span class="sxs-lookup"><span data-stu-id="d1379-197">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="d1379-198">Varmista, että kartat on poistettu kohteen `msdy_dualwriteruntimeconfig` taulusta Dataversessä.</span><span class="sxs-lookup"><span data-stu-id="d1379-198">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="d1379-199">Asenna [kaksoskirjoituksen osapuoli ja yleisiä osoitekirjaratkaisuja](https://aka.ms/dual-write-gab) AppSourcesta.</span><span class="sxs-lookup"><span data-stu-id="d1379-199">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="d1379-200">Jos seuraavat taulut sisältävät tietoja finance and operations -sovelluksessa, suorita niiden **ensimmäinen synkronointi**.</span><span class="sxs-lookup"><span data-stu-id="d1379-200">In the finance and operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="d1379-201">Tervehdykset</span><span class="sxs-lookup"><span data-stu-id="d1379-201">Salutations</span></span>
    + <span data-ttu-id="d1379-202">Henkilökohtaisten luonteenpiirteiden tyypit</span><span class="sxs-lookup"><span data-stu-id="d1379-202">Personal character types</span></span>
    + <span data-ttu-id="d1379-203">Loppusanat</span><span class="sxs-lookup"><span data-stu-id="d1379-203">Complimentary closing</span></span>
    + <span data-ttu-id="d1379-204">Yhteyshenkilöiden arvonimet</span><span class="sxs-lookup"><span data-stu-id="d1379-204">Contact person titles</span></span>
    + <span data-ttu-id="d1379-205">Päätöksentekoroolit</span><span class="sxs-lookup"><span data-stu-id="d1379-205">Decision making roles</span></span>
    + <span data-ttu-id="d1379-206">Kanta-asiakastasot</span><span class="sxs-lookup"><span data-stu-id="d1379-206">Loyalty levels</span></span>

5. <span data-ttu-id="d1379-207">Poista seuraavat vaiheet käytöstä Customer Engagement -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="d1379-207">In the customer engagement app, disable the following plug-in steps.</span></span>

    + <span data-ttu-id="d1379-208">Tilin päivitys</span><span class="sxs-lookup"><span data-stu-id="d1379-208">Account Update</span></span>
         + <span data-ttu-id="d1379-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span><span class="sxs-lookup"><span data-stu-id="d1379-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="d1379-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span><span class="sxs-lookup"><span data-stu-id="d1379-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="d1379-211">Yhteyshenkilön päivitys</span><span class="sxs-lookup"><span data-stu-id="d1379-211">Contact Update</span></span>
         + <span data-ttu-id="d1379-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span><span class="sxs-lookup"><span data-stu-id="d1379-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="d1379-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span><span class="sxs-lookup"><span data-stu-id="d1379-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="d1379-214">msdyn_party Update</span><span class="sxs-lookup"><span data-stu-id="d1379-214">msdyn_party Update</span></span>
         + <span data-ttu-id="d1379-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span><span class="sxs-lookup"><span data-stu-id="d1379-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="d1379-216">msdyn_vendor Update</span><span class="sxs-lookup"><span data-stu-id="d1379-216">msdyn_vendor Update</span></span>
         + <span data-ttu-id="d1379-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="d1379-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="d1379-218">Poista seuraavat vaiheet käytöstä Customer Engagement -sovelluksen työnkuluissa:</span><span class="sxs-lookup"><span data-stu-id="d1379-218">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="d1379-219">Toimittajien luonti Tilit-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1379-219">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="d1379-220">Toimittajien luonti Tilit-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1379-220">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="d1379-221">Luo henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1379-221">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="d1379-222">Luo henkilötyyppisiä toimittajia Toimittajat-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1379-222">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="d1379-223">Toimittajien päivitys Tilit-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1379-223">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="d1379-224">Toimittajien päivitys Toimittajat-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1379-224">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="d1379-225">Päivitä henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1379-225">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="d1379-226">Päivitä henkilötyyppisiä toimittajia Toimittajat-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1379-226">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="d1379-227">Suorita malli data factoryssä valitsemalla **Käynnistys nyt** seuraavan kuvan mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="d1379-227">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="d1379-228">Tämä prosessi saattaa kestää joitakin tunteja tietojen määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="d1379-228">This process might take a few hours to complete based on the data volume.</span></span>

    ![Käynnistimen suoritus](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="d1379-230">Jos olet muokannut **tiliä**, **yhteyshenkilöä** ja **toimittajaa**, sinun täytyy muokata mallia.</span><span class="sxs-lookup"><span data-stu-id="d1379-230">If you have customizations for **Account**, **Contact**, and **Vendor**, then you need to modify the template.</span></span>

8. <span data-ttu-id="d1379-231">Tuo Finance and Operations -sovelluksen uudet **osapuoli**-tietueet.</span><span class="sxs-lookup"><span data-stu-id="d1379-231">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="d1379-232">Lataa `FONewParty.csv`-tiedosto Azure blob-objektisäilöstä.</span><span class="sxs-lookup"><span data-stu-id="d1379-232">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="d1379-233">Polku on `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="d1379-233">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="d1379-234">Muunna `FONewParty.csv`-tiedosto Excel-tiedostoksi ja tuo Excel-tiedosto finance and operations -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="d1379-234">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the finance and operations app.</span></span> <span data-ttu-id="d1379-235">Jos csv-tuonti toimii sinulle, voit tuoda csv-tiedoston suoraan.</span><span class="sxs-lookup"><span data-stu-id="d1379-235">If the csv import works for you, you can import the csv file directly.</span></span> <span data-ttu-id="d1379-236">Tuonti saattaa kestää muutamia tunteja sen mukaan, mikä tietomäärä on käytössä.</span><span class="sxs-lookup"><span data-stu-id="d1379-236">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="d1379-237">Lisätietoja on kohdassa [Tietojen tuonti- ja vientitöiden yleiskatsaus](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="d1379-237">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![Dataverse-osapuolen tietueiden tuominen](media/data-factory-import-party.png)

9. <span data-ttu-id="d1379-239">Ota seuraavat vaiheet käyttöön Customer Engagement -sovelluksissa:</span><span class="sxs-lookup"><span data-stu-id="d1379-239">In the customer engagement apps, enable the following plug-in steps:</span></span>

    + <span data-ttu-id="d1379-240">Tilin päivitys</span><span class="sxs-lookup"><span data-stu-id="d1379-240">Account Update</span></span>
         + <span data-ttu-id="d1379-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span><span class="sxs-lookup"><span data-stu-id="d1379-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="d1379-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span><span class="sxs-lookup"><span data-stu-id="d1379-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="d1379-243">Yhteyshenkilön päivitys</span><span class="sxs-lookup"><span data-stu-id="d1379-243">Contact Update</span></span>
         + <span data-ttu-id="d1379-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span><span class="sxs-lookup"><span data-stu-id="d1379-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="d1379-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span><span class="sxs-lookup"><span data-stu-id="d1379-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="d1379-246">msdyn_party Update</span><span class="sxs-lookup"><span data-stu-id="d1379-246">msdyn_party Update</span></span>
         + <span data-ttu-id="d1379-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span><span class="sxs-lookup"><span data-stu-id="d1379-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="d1379-248">msdyn_vendor Update</span><span class="sxs-lookup"><span data-stu-id="d1379-248">msdyn_vendor Update</span></span>
         + <span data-ttu-id="d1379-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="d1379-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="d1379-250">Aktivoi seuraavat työnkulut Customer Engagement -sovelluksessa, jos poistat niiden aktivoinnin aiemmissa vaiheissa:</span><span class="sxs-lookup"><span data-stu-id="d1379-250">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="d1379-251">Toimittajien luonti Tilit-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1379-251">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="d1379-252">Toimittajien luonti Tilit-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1379-252">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="d1379-253">Luo henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1379-253">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="d1379-254">Luo henkilötyyppisiä toimittajia Toimittajat-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1379-254">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="d1379-255">Toimittajien päivitys Tilit-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1379-255">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="d1379-256">Toimittajien päivitys Toimittajat-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1379-256">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="d1379-257">Päivitä henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1379-257">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="d1379-258">Päivitä henkilötyyppisiä toimittajia Toimittajat-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1379-258">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="d1379-259">Suorita **osapuoliin** liittyvät kartat [osapuolen ja yleisen osoitekirjan](party-gab.md) ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="d1379-259">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="d1379-260">Vianmääritys</span><span class="sxs-lookup"><span data-stu-id="d1379-260">Troubleshooting</span></span>

1. <span data-ttu-id="d1379-261">Jos prosessi epäonnistuu, käynnistä data factory uudelleen epäonnistuneen tehtävän perusteella.</span><span class="sxs-lookup"><span data-stu-id="d1379-261">If the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="d1379-262">Osa tiedostoista luodaan data factoryssa, jota voit käyttää tietojen oikeellisuustarkistusta varten.</span><span class="sxs-lookup"><span data-stu-id="d1379-262">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="d1379-263">Data factory suoritetaan pilkuilla erotettujen csv-tiedostojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="d1379-263">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="d1379-264">Jos kenttäarvolla on pilkku, se voi sisältää tulokset, mutta ei välttämättä pilkkua.</span><span class="sxs-lookup"><span data-stu-id="d1379-264">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="d1379-265">Poista pilkut.</span><span class="sxs-lookup"><span data-stu-id="d1379-265">You need to remove the commas.</span></span>
4. <span data-ttu-id="d1379-266">**Seuranta**-välilehdessä on tietoja kaikista vaiheista ja käsitellyistä tiedoista.</span><span class="sxs-lookup"><span data-stu-id="d1379-266">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="d1379-267">Valitse tietty virheenkorjausvaihe.</span><span class="sxs-lookup"><span data-stu-id="d1379-267">Select a specific step to debug it.</span></span>

    ![Seuranta-välilehti](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="d1379-269">Lisätietoja mallista</span><span class="sxs-lookup"><span data-stu-id="d1379-269">Learn more about the template</span></span>

<span data-ttu-id="d1379-270">Mallin lisätiedot ovat ohjeaiheessa [Comments for Azure Data Factor -mallin lueminut-tiedosto](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span><span class="sxs-lookup"><span data-stu-id="d1379-270">You can find additional information about the template in [Comments for Azure Data Factory template readme](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span></span>
