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
ms.openlocfilehash: 95472a00d34ba939ac89b4e2484f34d50bee3088
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018309"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="d1f63-103">Päivitä osapuolen osoitekirja ja yleinen osoitekirja</span><span class="sxs-lookup"><span data-stu-id="d1f63-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d1f63-104">[Azure Data Factory -malli](https://aka.ms/dual-write-gab-adf) auttaa päivittämään aiemmin luodun **Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-taulun tiedot kaksoiskirjoitusmallin osapuolen ja yleisen osoitekirjamallin avulla.</span><span class="sxs-lookup"><span data-stu-id="d1f63-104">The [Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="d1f63-105">Malli täsmäyttää sekä Finance and Operations- että customer engagement -sovellusten tiedot.</span><span class="sxs-lookup"><span data-stu-id="d1f63-105">The template reconciles the data from both Finance and Operations apps and customer engagement applications.</span></span> <span data-ttu-id="d1f63-106">Prosessin lopussa luodaan **osapuolen** tietueiden **osapuoli**- ja **yhteyshenkilö** kentät ja liitetään asiakkaan varaushakemusten **Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-tietueisiin.</span><span class="sxs-lookup"><span data-stu-id="d1f63-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="d1f63-107">.csv-tiedosto (`FONewParty.csv`) luodaan luomaan uudet **osapuoli** tietueet Finance and Operations -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="d1f63-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the Finance and Operations app.</span></span> <span data-ttu-id="d1f63-108">Tämä ohjeaihe sisältää Data Factory -mallissa käytettävät ohjeet ja tietojen päivittämisen.</span><span class="sxs-lookup"><span data-stu-id="d1f63-108">This topic provides the instructions to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="d1f63-109">Jos mukautuksia ei ole, voit käyttää mallia niin kuin se on.</span><span class="sxs-lookup"><span data-stu-id="d1f63-109">If you don’t have any customizations, you can use the template as-is.</span></span> <span data-ttu-id="d1f63-110">Jos olet muokannut **tiliä**, **yhteyshenkilöä** ja **toimittajaa**, sinun on muokattava mallia seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="d1f63-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!Note]
> <span data-ttu-id="d1f63-111">Mallin avulla voit päivittää vain **osapuolen** tiedot.</span><span class="sxs-lookup"><span data-stu-id="d1f63-111">The template helps to upgrade only the **Party** data.</span></span> <span data-ttu-id="d1f63-112">Tulevat posti- ja sähköiset osoitteet sisällytetään julkaisuun.</span><span class="sxs-lookup"><span data-stu-id="d1f63-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d1f63-113">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="d1f63-113">Prerequisites</span></span>

<span data-ttu-id="d1f63-114">Nämä edellytykset vaaditaan:</span><span class="sxs-lookup"><span data-stu-id="d1f63-114">These prerequisites are required:</span></span>

+ [<span data-ttu-id="d1f63-115">Azure-tilaus</span><span class="sxs-lookup"><span data-stu-id="d1f63-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="d1f63-116">Mallin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="d1f63-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="d1f63-117">Olet aiemmin luotu kaksoiskirjoitusasiakas.</span><span class="sxs-lookup"><span data-stu-id="d1f63-117">You are an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="d1f63-118">Päivityksen valmistelu</span><span class="sxs-lookup"><span data-stu-id="d1f63-118">Prepare for the upgrade</span></span>

+ <span data-ttu-id="d1f63-119">**Täysin synkronoitu**: Molemmat ympäristöt ovat täysin synkronoituja **Tilin (Asiakas)**, **Yhteyshenkilön** ja **Toimittajan** kanssa.</span><span class="sxs-lookup"><span data-stu-id="d1f63-119">**Fully synched**: Both environments are fully synched state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="d1f63-120">**Integrointiavaimet**: **Tili (Asiakas)**-, **Yhteyshenkilö**- ja **Toimittaja**-taulut Customer Engagement -sovelluksessa käyttävät valmiita integrointiavaimia.</span><span class="sxs-lookup"><span data-stu-id="d1f63-120">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="d1f63-121">Jos olet mukauttanut integrointiavaimia, mukauta mallia.</span><span class="sxs-lookup"><span data-stu-id="d1f63-121">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="d1f63-122">**Osapuolinumero**: Kaikki päivitettävät **Tili (asiakas)**-, **yhteyshenkilö**- ja **toimittaja**-tietueet saavat **osapuoli** numeron.</span><span class="sxs-lookup"><span data-stu-id="d1f63-122">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="d1f63-123">Tietueet, joissa ei ole **osapuolen** numeroa, ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="d1f63-123">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="d1f63-124">Jos haluat päivittää nämä tietueet, lisää niille **osapuolen** numero ennen päivitysprosessin käynnistämistä.</span><span class="sxs-lookup"><span data-stu-id="d1f63-124">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="d1f63-125">**Järjestelmän käyttökomento**: Ota päivitysprosessin aikana sekä Finance and Operations- että customer engagement -ympäristöt offline-tilaan.</span><span class="sxs-lookup"><span data-stu-id="d1f63-125">**System outage**: During the upgrade process, you will have to take both the Finance and Operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="d1f63-126">**Tilannekuva**: Ota tilannekuvia sekä Finance and Operations- että customer engagement -sovelluksista.</span><span class="sxs-lookup"><span data-stu-id="d1f63-126">**Snapshot**: Take snapshots of both the Finance and Operations and customer engagement apps.</span></span> <span data-ttu-id="d1f63-127">Voit tarvittaessa palauttaa edellisen tilan tilannekuvasten avulla.</span><span class="sxs-lookup"><span data-stu-id="d1f63-127">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="d1f63-128">Käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="d1f63-128">Deployment</span></span>

1. <span data-ttu-id="d1f63-129">Lataa malli [Dynamics-365-FastTrack-käyttöönotto-käyttöomaisuus](https://aka.ms/dual-write-gab-adf) -kentästä.</span><span class="sxs-lookup"><span data-stu-id="d1f63-129">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="d1f63-130">Kirjaudu [Microsoft Azure -palveluun](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="d1f63-130">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="d1f63-131">[Resurssiryhmän](/azure/azure-resource-manager/management/manage-resource-groups-portal) luonti.</span><span class="sxs-lookup"><span data-stu-id="d1f63-131">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="d1f63-132">Luo [tallennustili](/azure/storage/common/storage-account-create?tabs=azure-portal) luomallesi resurssiryhmälle.</span><span class="sxs-lookup"><span data-stu-id="d1f63-132">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="d1f63-133">Luo [Data Factory](/azure/data-factory/quickstart-create-data-factory-portal) yllä luomallesi resurssiryhmälle.</span><span class="sxs-lookup"><span data-stu-id="d1f63-133">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="d1f63-134">Avaa Data Factory ja valitse **Tee & valvo** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="d1f63-134">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="d1f63-135">Valitse **Hallinta**-välilehdestä **ARM-malli**.</span><span class="sxs-lookup"><span data-stu-id="d1f63-135">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="d1f63-136">Tuo **osapuolen** malli valitsemalla **Tuo ARM -malli**.</span><span class="sxs-lookup"><span data-stu-id="d1f63-136">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="d1f63-137">Tuo malli data factoryyn.</span><span class="sxs-lookup"><span data-stu-id="d1f63-137">Import the template into the data factory.</span></span> <span data-ttu-id="d1f63-138">Määritä seuraavat arvot **projektitietoja** ja **esiintymän tietoja** varten.</span><span class="sxs-lookup"><span data-stu-id="d1f63-138">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="d1f63-139">Kenttä</span><span class="sxs-lookup"><span data-stu-id="d1f63-139">Field</span></span> | <span data-ttu-id="d1f63-140">Arvo</span><span class="sxs-lookup"><span data-stu-id="d1f63-140">Value</span></span>
    ---|---
    <span data-ttu-id="d1f63-141">Tilaus</span><span class="sxs-lookup"><span data-stu-id="d1f63-141">Subscription</span></span> | <span data-ttu-id="d1f63-142">Azure-tilaus</span><span class="sxs-lookup"><span data-stu-id="d1f63-142">Azure subscription</span></span>
    <span data-ttu-id="d1f63-143">Resurssiryhmä</span><span class="sxs-lookup"><span data-stu-id="d1f63-143">Resource group</span></span> | <span data-ttu-id="d1f63-144">Anna sama resurssi, jolle tallennustili luodaan.</span><span class="sxs-lookup"><span data-stu-id="d1f63-144">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="d1f63-145">Alue</span><span class="sxs-lookup"><span data-stu-id="d1f63-145">Region</span></span> | <span data-ttu-id="d1f63-146">Määritä alue.</span><span class="sxs-lookup"><span data-stu-id="d1f63-146">Specify region.</span></span>
    <span data-ttu-id="d1f63-147">Tehtaan nimi</span><span class="sxs-lookup"><span data-stu-id="d1f63-147">Factory Name</span></span> | <span data-ttu-id="d1f63-148">Määritä tehtaan nimi.</span><span class="sxs-lookup"><span data-stu-id="d1f63-148">Specify factory name.</span></span>
    <span data-ttu-id="d1f63-149">FO-yhdistetyn palvelun pääavain</span><span class="sxs-lookup"><span data-stu-id="d1f63-149">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="d1f63-150">Määritä sovelluksen avain.</span><span class="sxs-lookup"><span data-stu-id="d1f63-150">Specify the application's key.</span></span>
    <span data-ttu-id="d1f63-151">Azure Blob-objektisäilön yhteysmerkkijonot</span><span class="sxs-lookup"><span data-stu-id="d1f63-151">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="d1f63-152">Azure Blob-objektisäilön yhteysmerkkijonot.</span><span class="sxs-lookup"><span data-stu-id="d1f63-152">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="d1f63-153">Dynamics Crm:n linkitetty palvelusalasana</span><span class="sxs-lookup"><span data-stu-id="d1f63-153">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="d1f63-154">Käyttäjäksi määritetyn käyttäjätilin salasana.</span><span class="sxs-lookup"><span data-stu-id="d1f63-154">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="d1f63-155">FO Linked Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="d1f63-155">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="d1f63-156">FO Linked Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="d1f63-156">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="d1f63-157">Määritä vuokraajan tiedot (toimialueen nimi tai vuokraajan tunnus), jota hakemuksesi käyttää.</span><span class="sxs-lookup"><span data-stu-id="d1f63-157">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="d1f63-158">FO Linked Service_properties_type Properties_aad Resource Id</span><span class="sxs-lookup"><span data-stu-id="d1f63-158">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="d1f63-159">FO Linked Service_properties_type Properties_service Principal Id</span><span class="sxs-lookup"><span data-stu-id="d1f63-159">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="d1f63-160">Määritä sovelluksen asiakkaan tunnus.</span><span class="sxs-lookup"><span data-stu-id="d1f63-160">Specify the application's client ID.</span></span>
    <span data-ttu-id="d1f63-161">Dynamics Crm Linked Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="d1f63-161">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="d1f63-162">Dynamics-yhteyden muodostanut käyttäjänimi.</span><span class="sxs-lookup"><span data-stu-id="d1f63-162">The username to connect to Dynamics.</span></span>

    <span data-ttu-id="d1f63-163">Lisätietoja on ohjeaiheessa [Resource Manager -mallin manuaalinen luominen jokaiselle ympäristölle](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [linkitetyt palvelun ominaisuudet](/azure/data-factory/connector-dynamics-ax#linked-service-properties) ja [tietojen kopioiminen Azure Data Factoryn avulla](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span><span class="sxs-lookup"><span data-stu-id="d1f63-163">For more information, see [Manually promote a Resource Manager template for each environment](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Linked service properties](/azure/data-factory/connector-dynamics-ax#linked-service-properties), and [Copy data using Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span></span>

10. <span data-ttu-id="d1f63-164">Tarkista käyttöönoton jälkeen tietojoukot, tietovuo ja data factoryn linkitetty palvelu.</span><span class="sxs-lookup"><span data-stu-id="d1f63-164">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Tietojoukot, tietovuo ja linkitetty palvelu](media/data-factory-validate.png)

11. <span data-ttu-id="d1f63-166">Siirry kohtaan **Hallitse**.</span><span class="sxs-lookup"><span data-stu-id="d1f63-166">Navigate to **Manage**.</span></span> <span data-ttu-id="d1f63-167">Valitse **Yhteydet**-kohdasta **Linkitetty palvelu**.</span><span class="sxs-lookup"><span data-stu-id="d1f63-167">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="d1f63-168">Valitse **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="d1f63-168">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="d1f63-169">Syötä **Muokkaa linkitettyä palvelua (Dynamics CRM)** -lomakkeeseen seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="d1f63-169">In the **Edit linked service (Dynamics CRM)** form, enter the following values:</span></span>

    <span data-ttu-id="d1f63-170">Kenttä</span><span class="sxs-lookup"><span data-stu-id="d1f63-170">Field</span></span> | <span data-ttu-id="d1f63-171">Arvo</span><span class="sxs-lookup"><span data-stu-id="d1f63-171">Value</span></span>
    ---|---
    <span data-ttu-id="d1f63-172">Nimi</span><span class="sxs-lookup"><span data-stu-id="d1f63-172">Name</span></span> | <span data-ttu-id="d1f63-173">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="d1f63-173">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="d1f63-174">kuvaus</span><span class="sxs-lookup"><span data-stu-id="d1f63-174">Description</span></span> | <span data-ttu-id="d1f63-175">Linkitetyt palvelut, jotka yhdistetään CRM-instanssiin yksikkötietojen hakemista varten</span><span class="sxs-lookup"><span data-stu-id="d1f63-175">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="d1f63-176">Yhdistä integroinnin suorituspalvelun kautta</span><span class="sxs-lookup"><span data-stu-id="d1f63-176">Connect via integration runtime</span></span> | <span data-ttu-id="d1f63-177">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d1f63-177">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="d1f63-178">Käyttöönottotyyppi</span><span class="sxs-lookup"><span data-stu-id="d1f63-178">Deployment type</span></span> | <span data-ttu-id="d1f63-179">Yhdistetty</span><span class="sxs-lookup"><span data-stu-id="d1f63-179">Online</span></span>
    <span data-ttu-id="d1f63-180">Palvelu-Uri</span><span class="sxs-lookup"><span data-stu-id="d1f63-180">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="d1f63-181">Todennustyyppi</span><span class="sxs-lookup"><span data-stu-id="d1f63-181">Authentication type</span></span> | <span data-ttu-id="d1f63-182">Office365</span><span class="sxs-lookup"><span data-stu-id="d1f63-182">Office365</span></span>
    <span data-ttu-id="d1f63-183">Käyttäjänimi</span><span class="sxs-lookup"><span data-stu-id="d1f63-183">User name</span></span> |
    <span data-ttu-id="d1f63-184">Salasana tai Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="d1f63-184">Password or Azure Key Vault</span></span> | <span data-ttu-id="d1f63-185">Salasana</span><span class="sxs-lookup"><span data-stu-id="d1f63-185">Password</span></span>
    <span data-ttu-id="d1f63-186">Salasana</span><span class="sxs-lookup"><span data-stu-id="d1f63-186">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="d1f63-187">Suorita malli</span><span class="sxs-lookup"><span data-stu-id="d1f63-187">Run the template</span></span>

1. <span data-ttu-id="d1f63-188">Lopeta Finance and Operations -sovelluksen avulla seuraava **Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-kaksoiskirjoitus.</span><span class="sxs-lookup"><span data-stu-id="d1f63-188">Stop the following **Account**, **Contact**, and **Vendor** dual-write using the Finance and Operations app.</span></span>

    + <span data-ttu-id="d1f63-189">Asiakkaat V3 (accounts)</span><span class="sxs-lookup"><span data-stu-id="d1f63-189">Customers V3(accounts)</span></span>
    + <span data-ttu-id="d1f63-190">Asiakkaat V3 (yhteyshenkilöt)</span><span class="sxs-lookup"><span data-stu-id="d1f63-190">Customers V3(contacts)</span></span>
    + <span data-ttu-id="d1f63-191">CDS-kontaktit V2 (yhteyshenkilöt)</span><span class="sxs-lookup"><span data-stu-id="d1f63-191">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="d1f63-192">CDS-kontaktit V2 (yhteyshenkilöt)</span><span class="sxs-lookup"><span data-stu-id="d1f63-192">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="d1f63-193">Toimittajat V2 (msdyn_vendors)</span><span class="sxs-lookup"><span data-stu-id="d1f63-193">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="d1f63-194">Varmista, että kartat on poistettu kohteen `msdy_dualwriteruntimeconfig` taulusta Dataversessä.</span><span class="sxs-lookup"><span data-stu-id="d1f63-194">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="d1f63-195">Asenna [kaksoskirjoituksen osapuoli ja yleisiä osoitekirjaratkaisuja](https://aka.ms/dual-write-gab) AppSourcesta.</span><span class="sxs-lookup"><span data-stu-id="d1f63-195">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="d1f63-196">Jos seuraavat taulut sisältävät tietoja Finance and Operations -sovelluksessa, suorita niiden **ensimmäinen synkronointi**.</span><span class="sxs-lookup"><span data-stu-id="d1f63-196">In the Finance and Operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="d1f63-197">Tervehdykset</span><span class="sxs-lookup"><span data-stu-id="d1f63-197">Salutations</span></span>
    + <span data-ttu-id="d1f63-198">Henkilökohtaisten luonteenpiirteiden tyypit</span><span class="sxs-lookup"><span data-stu-id="d1f63-198">Personal character types</span></span>
    + <span data-ttu-id="d1f63-199">Loppusanat</span><span class="sxs-lookup"><span data-stu-id="d1f63-199">Complimentary closing</span></span>
    + <span data-ttu-id="d1f63-200">Yhteyshenkilöiden arvonimet</span><span class="sxs-lookup"><span data-stu-id="d1f63-200">Contact person titles</span></span>
    + <span data-ttu-id="d1f63-201">Päätöksentekoroolit</span><span class="sxs-lookup"><span data-stu-id="d1f63-201">Decision making roles</span></span>
    + <span data-ttu-id="d1f63-202">Kanta-asiakastasot</span><span class="sxs-lookup"><span data-stu-id="d1f63-202">Loyalty levels</span></span>

5. <span data-ttu-id="d1f63-203">Poista seuraavat vaiheet käytöstä Customer Engagement -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="d1f63-203">In the customer engagement app, disable the following plugin steps.</span></span>

    + <span data-ttu-id="d1f63-204">Tilin päivitys</span><span class="sxs-lookup"><span data-stu-id="d1f63-204">Account Update</span></span>
         + <span data-ttu-id="d1f63-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span><span class="sxs-lookup"><span data-stu-id="d1f63-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="d1f63-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span><span class="sxs-lookup"><span data-stu-id="d1f63-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="d1f63-207">Yhteyshenkilön päivitys</span><span class="sxs-lookup"><span data-stu-id="d1f63-207">Contact Update</span></span>
         + <span data-ttu-id="d1f63-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span><span class="sxs-lookup"><span data-stu-id="d1f63-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="d1f63-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span><span class="sxs-lookup"><span data-stu-id="d1f63-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="d1f63-210">msdyn_party Update</span><span class="sxs-lookup"><span data-stu-id="d1f63-210">msdyn_party Update</span></span>
         + <span data-ttu-id="d1f63-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span><span class="sxs-lookup"><span data-stu-id="d1f63-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="d1f63-212">msdyn_vendor Update</span><span class="sxs-lookup"><span data-stu-id="d1f63-212">msdyn_vendor Update</span></span>
         + <span data-ttu-id="d1f63-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="d1f63-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="d1f63-214">Poista seuraavat vaiheet käytöstä Customer Engagement -sovelluksen työnkuluissa:</span><span class="sxs-lookup"><span data-stu-id="d1f63-214">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="d1f63-215">Toimittajien luonti Tilit-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1f63-215">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="d1f63-216">Toimittajien luonti Tilit-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1f63-216">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="d1f63-217">Luo henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1f63-217">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="d1f63-218">Luo henkilötyyppisiä toimittajia Toimittajat-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1f63-218">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="d1f63-219">Toimittajien päivitys Tilit-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1f63-219">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="d1f63-220">Toimittajien päivitys Toimittajat-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1f63-220">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="d1f63-221">Päivitä henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1f63-221">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="d1f63-222">Päivitä henkilötyyppisiä toimittajia Toimittajat-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1f63-222">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="d1f63-223">Suorita malli data factoryssä valitsemalla **Käynnistys nyt** seuraavan kuvan mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="d1f63-223">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="d1f63-224">Tämä prosessi saattaa kestää joitakin tunteja tietojen määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="d1f63-224">This process might take a few hours to complete based on the data volume.</span></span>

    ![Käynnistimen suoritus](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="d1f63-226">Jos olet muokannut **tiliä**, **yhteyshenkilöä** ja **toimittajaa**, sinun on muokattava mallia.</span><span class="sxs-lookup"><span data-stu-id="d1f63-226">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template.</span></span>

8. <span data-ttu-id="d1f63-227">Tuo Finance and Operations -sovelluksen uudet **osapuoli**-tietueet.</span><span class="sxs-lookup"><span data-stu-id="d1f63-227">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="d1f63-228">Lataa `FONewParty.csv`-tiedosto Azure blob-objektisäilöstä.</span><span class="sxs-lookup"><span data-stu-id="d1f63-228">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="d1f63-229">Polku on `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="d1f63-229">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="d1f63-230">Muunna `FONewParty.csv`-tiedosto Excel-tiedostoksi ja tuo Excel-tiedosto Finance and Operations -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="d1f63-230">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the Finance and Operations app.</span></span>  <span data-ttu-id="d1f63-231">Jos csv-tuonti toimii sinulle, voit tuoda csv-tiedoston suoraan.</span><span class="sxs-lookup"><span data-stu-id="d1f63-231">If the csv import works for you, you can import csv file directly.</span></span> <span data-ttu-id="d1f63-232">Tuonti saattaa kestää muutamia tunteja sen mukaan, mikä tietomäärä on käytössä.</span><span class="sxs-lookup"><span data-stu-id="d1f63-232">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="d1f63-233">Lisätietoja on kohdassa [Tietojen tuonti- ja vientitöiden yleiskatsaus](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="d1f63-233">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![Dataverse-osapuolen tietueiden tuominen](media/data-factory-import-party.png)

9. <span data-ttu-id="d1f63-235">Ota seuraavat vaiheet käyttöön Customer Engagement -sovelluksissa:</span><span class="sxs-lookup"><span data-stu-id="d1f63-235">In the customer engagement apps, enable the following plugin steps:</span></span>

    + <span data-ttu-id="d1f63-236">Tilin päivitys</span><span class="sxs-lookup"><span data-stu-id="d1f63-236">Account Update</span></span>
         + <span data-ttu-id="d1f63-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span><span class="sxs-lookup"><span data-stu-id="d1f63-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="d1f63-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span><span class="sxs-lookup"><span data-stu-id="d1f63-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="d1f63-239">Yhteyshenkilön päivitys</span><span class="sxs-lookup"><span data-stu-id="d1f63-239">Contact Update</span></span>
         + <span data-ttu-id="d1f63-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span><span class="sxs-lookup"><span data-stu-id="d1f63-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="d1f63-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span><span class="sxs-lookup"><span data-stu-id="d1f63-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="d1f63-242">msdyn_party Update</span><span class="sxs-lookup"><span data-stu-id="d1f63-242">msdyn_party Update</span></span>
         + <span data-ttu-id="d1f63-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span><span class="sxs-lookup"><span data-stu-id="d1f63-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="d1f63-244">msdyn_vendor Update</span><span class="sxs-lookup"><span data-stu-id="d1f63-244">msdyn_vendor Update</span></span>
         + <span data-ttu-id="d1f63-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="d1f63-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="d1f63-246">Aktivoi seuraavat työnkulut Customer Engagement -sovelluksessa, jos poistat niiden aktivoinnin aiemmissa vaiheissa:</span><span class="sxs-lookup"><span data-stu-id="d1f63-246">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="d1f63-247">Toimittajien luonti Tilit-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1f63-247">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="d1f63-248">Toimittajien luonti Tilit-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1f63-248">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="d1f63-249">Luo henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1f63-249">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="d1f63-250">Luo henkilötyyppisiä toimittajia Toimittajat-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1f63-250">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="d1f63-251">Toimittajien päivitys Tilit-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1f63-251">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="d1f63-252">Toimittajien päivitys Toimittajat-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1f63-252">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="d1f63-253">Päivitä henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1f63-253">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="d1f63-254">Päivitä henkilötyyppisiä toimittajia Toimittajat-taulussa</span><span class="sxs-lookup"><span data-stu-id="d1f63-254">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="d1f63-255">Suorita **osapuoliin** liittyvät kartat [osapuolen ja yleisen osoitekirjan](party-gab.md) ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="d1f63-255">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="d1f63-256">Vianmääritys</span><span class="sxs-lookup"><span data-stu-id="d1f63-256">Troubleshooting</span></span>

1. <span data-ttu-id="d1f63-257">Jos prosessi epäonnistuu, käynnistä data factory uudelleen epäonnistuneen tehtävän perusteella.</span><span class="sxs-lookup"><span data-stu-id="d1f63-257">In the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="d1f63-258">Osa tiedostoista luodaan data factoryssa, jota voit käyttää tietojen oikeellisuustarkistusta varten.</span><span class="sxs-lookup"><span data-stu-id="d1f63-258">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="d1f63-259">Data factory suoritetaan pilkuilla erotettujen csv-tiedostojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="d1f63-259">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="d1f63-260">Jos kenttäarvolla on pilkku, se voi sisältää tulokset, mutta ei välttämättä pilkkua.</span><span class="sxs-lookup"><span data-stu-id="d1f63-260">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="d1f63-261">Poista pilkut.</span><span class="sxs-lookup"><span data-stu-id="d1f63-261">You need to remove the commas.</span></span>
4. <span data-ttu-id="d1f63-262">**Seuranta**-välilehdessä on tietoja kaikista vaiheista ja käsitellyistä tiedoista.</span><span class="sxs-lookup"><span data-stu-id="d1f63-262">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="d1f63-263">Valitse tietty virheenkorjausvaihe.</span><span class="sxs-lookup"><span data-stu-id="d1f63-263">Select a specific step to debug it.</span></span>

    ![Seuranta-välilehti](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="d1f63-265">Lisätietoja mallista</span><span class="sxs-lookup"><span data-stu-id="d1f63-265">Learn more about the template</span></span>

<span data-ttu-id="d1f63-266">Malliin lisättyjä kommentteja löydät [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md)-tiedostosta.</span><span class="sxs-lookup"><span data-stu-id="d1f63-266">You can find comments for the template the [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) file.</span></span>