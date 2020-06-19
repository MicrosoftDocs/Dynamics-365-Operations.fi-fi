---
title: Ongelmien vianmääritys synkronoinnin aikana
description: Tässä ohjeaiheessa on vianmääritys tietoja, joiden avulla voit korjata, joita saattaa ilmetä alkuperäisen synkronoinnin aikana.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410078"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="ae941-103">Ongelmien vianmääritys synkronoinnin aikana</span><span class="sxs-lookup"><span data-stu-id="ae941-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ae941-104">Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Common Data Servicen välillä.</span><span class="sxs-lookup"><span data-stu-id="ae941-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="ae941-105">Erityisesti se tarjoaa tietoa, joiden avulla voit korjata virheitä, joita saattaa ilmetä alkuperäisen synkronoinnin aikana.</span><span class="sxs-lookup"><span data-stu-id="ae941-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ae941-106">Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia.</span><span class="sxs-lookup"><span data-stu-id="ae941-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="ae941-107">Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.</span><span class="sxs-lookup"><span data-stu-id="ae941-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="ae941-108">Finance and Operations -sovelluksen ensimmäisten synkronointivirheiden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="ae941-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="ae941-109">Kun otat yhdistämismallit käyttöön, karttojen tilan on oltava **Käytössä**.</span><span class="sxs-lookup"><span data-stu-id="ae941-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="ae941-110">Jos tila on **ei käynnissä**, alkuperäisen synkronoinnin aikana ilmeni virheitä.</span><span class="sxs-lookup"><span data-stu-id="ae941-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="ae941-111">Voit tarkastella virheitä valitsemalla **kaksoiskirjoitus**-sivun **ensimmäiset synkronointitiedot**-välilehden.</span><span class="sxs-lookup"><span data-stu-id="ae941-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Alkuperäisen synkronoinnin tiedot -välilehti](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="ae941-113">Alkuperäistä synkronointia ei voi suorittaa loppuun: 400 virheellinen pyyntö</span><span class="sxs-lookup"><span data-stu-id="ae941-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="ae941-114">**Ongelman korjaamiseen tarvittava rooli:** Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="ae941-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="ae941-115">Näyttöön saattaa tulla seuraava virhesanoma, kun yrität suorittaa yhdistämismääritystä ja alkuperäistä synkronointia:</span><span class="sxs-lookup"><span data-stu-id="ae941-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="ae941-116">*Etäpalvelin palautti virheen: (400) Virheellinen pyyntö.), AX-vienti kohtasi virheen*</span><span class="sxs-lookup"><span data-stu-id="ae941-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="ae941-117">Esimerkki täydestä virheviestistä.</span><span class="sxs-lookup"><span data-stu-id="ae941-117">Here is an example of the full error message.</span></span>

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

<span data-ttu-id="ae941-118">Jos tämä virhe ilmenee jatkuvasti etkä voi suorittaa alkuperäistä synkronointia loppuun, korjaa ongelma noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="ae941-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="ae941-119">Kirjaudu sisään virtuaalikone (VM) Finance and Operationsille -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="ae941-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="ae941-120">Avaa Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="ae941-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="ae941-121">Varmista **Palvelut**-ruudussa, että Microsoft Dynamics 365 -tietojen tuonnin vientikehyspalvelu on käytössä.</span><span class="sxs-lookup"><span data-stu-id="ae941-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="ae941-122">Käynnistä se uudelleen, jos se on pysäytetty, koska ensimmäinen synkronointi edellyttää sitä.</span><span class="sxs-lookup"><span data-stu-id="ae941-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="ae941-123">Ensimmäinen synkronointivirhe: 403 kielletty</span><span class="sxs-lookup"><span data-stu-id="ae941-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="ae941-124">Seuraava virhesanoma saattaa tulla näyttöön alkuperäisen synkronoinnin aikana:</span><span class="sxs-lookup"><span data-stu-id="ae941-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="ae941-125">*(\[Kielletty\], Etäpalvelin palautti virheen: (403) Kielletty.), AX-vienti kohtasi virheen*</span><span class="sxs-lookup"><span data-stu-id="ae941-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="ae941-126">Korjaa ongelma seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="ae941-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="ae941-127">Kirjautuminen Finance and Operations -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="ae941-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="ae941-128">Poista **Azure Active Directory -sovellukset** -sivulla **DtAppID**-asiakasohjelma ja lisää se sitten uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ae941-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Azure AD -sovellusluettelo](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="ae941-130">Itseensä viittaus- tai kehäviittausvirheet alkuperäisen synkronoinnin aikana</span><span class="sxs-lookup"><span data-stu-id="ae941-130">Self-reference or circular-reference failures during initial synchronization</span></span>

<span data-ttu-id="ae941-131">Näyttöön saattaa tulla virhesanoma, jos jollakin yhdistämismäärityksistä on omia viittauksia tai kehäviittauksia.</span><span class="sxs-lookup"><span data-stu-id="ae941-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="ae941-132">Virheet kuuluvat seuraaviin luokkiin:</span><span class="sxs-lookup"><span data-stu-id="ae941-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="ae941-133">Toimittajat V2 – msdyn_vendors yksikön yhdistämismääritys</span><span class="sxs-lookup"><span data-stu-id="ae941-133">Vendors V2 to msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="ae941-134">Asiakkaat V3 tilien yksikkökartoitukseen</span><span class="sxs-lookup"><span data-stu-id="ae941-134">Customers V3 to Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="ae941-135">Ratkaise Toimittajien V2 virhe msdyn_vendors yksikön yhdistämismääritystä varten</span><span class="sxs-lookup"><span data-stu-id="ae941-135">Resolve an error in Vendors V2 to msdyn_vendors entity mapping</span></span>

<span data-ttu-id="ae941-136">Saatat joutua käyttämään seuraavia alkusynkronointivirheitä **Toimittajat V2** - **msdyn_vendors** kartoitukseen, jos entiteeteillä on aiemmin luotuja, **PrimaryContactPersonId**- ja **InvoiceVendorAccountNumber** -kenttien arvoja.</span><span class="sxs-lookup"><span data-stu-id="ae941-136">You might run into the following initial sync errors on the **Vendors V2** to **msdyn_vendors** mapping if the entities have existing records with values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="ae941-137">Tämä johtuu siitä, että **InvoiceVendorAccountNumber** on itseviittaava kenttä ja **PrimaryContactPersonId** on kehäviittaus toimittajan yhdistämismäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="ae941-137">This because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="ae941-138">*Kentän GUID-arvon selvittäminen ei onnistunut: <field>. Hakua ei löydy: <value>. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="ae941-138">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

<span data-ttu-id="ae941-139">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="ae941-139">Here are a couple of examples:</span></span>

- <span data-ttu-id="ae941-140">*Kentän GUID-arvon selvittäminen ei onnistunut: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Hakua ei löydy: 000056. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="ae941-140">*Couldn't resolve the guid for the field: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="ae941-141">*Kentän GUID-arvon selvittäminen ei onnistunut: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. Hakua ei löydy: V24-1. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span><span class="sxs-lookup"><span data-stu-id="ae941-141">*Couldn't resolve the guid for the field: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span></span>

<span data-ttu-id="ae941-142">Jos toimittajakohteen kentissä on arvoja, joiden arvot ovat samat, suorita ensimmäinen synkronointi onnistuneesti noudattamalla alla olevan kohdan ohjeita.</span><span class="sxs-lookup"><span data-stu-id="ae941-142">If you have records with values in these fields in the vendor entity follow the steps in the below section to complete initial sync successfully.</span></span>

1. <span data-ttu-id="ae941-143">Poista Finance and Operations sovelluksessa **PrimaryContactPersonId**- ja **InvoiceVendorAccountNumber**-kentät määrityksestä ja tallenna muutokset.</span><span class="sxs-lookup"><span data-stu-id="ae941-143">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping and save the changes.</span></span>

    1. <span data-ttu-id="ae941-144">Siirry toimittajat-version **Toimittajat V2 (msdyn_vendors)** -kaksoiskirjoitusmääritysten sivulle ja valitse **yksiköiden yhdistämismääritykset** -välilehti. Valitse vasemmanpuoleisesta suodattimesta **Finance and Operations -sovellukset. Toimittajat V2**.</span><span class="sxs-lookup"><span data-stu-id="ae941-144">Navigate to the dual-write mapping page for **Vendors V2 (msdyn_vendors)**, and select the **Entity mappings** tab. In the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="ae941-145">Valitse oikeanpuoleisesta suodattimesta **Sales.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="ae941-145">In the right filter, select **Sales.Vendor**.</span></span>

    2. <span data-ttu-id="ae941-146">Katso **primarycontactperson** ja etsi lähdekenttä **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="ae941-146">Search for **primarycontactperson** to find the source field **PrimaryContactPersonId**.</span></span>
    
    3. <span data-ttu-id="ae941-147">Napsauta **Toiminnot**-painiketta ja valitse **Poista**.</span><span class="sxs-lookup"><span data-stu-id="ae941-147">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![Itsenäinen tai kehäviittaus 3](media/vend_selfref3.png)
    
    4. <span data-ttu-id="ae941-149">Poista uudelleen, jos haluat poistaa **InvoiceVendorAccountNumber**-kentän.</span><span class="sxs-lookup"><span data-stu-id="ae941-149">Repeat to delete the **InvoiceVendorAccountNumber** field.</span></span>
    
        ![Itsenäinen tai kehäviittaus 4](media/vend-selfref4.png)
    
    5. <span data-ttu-id="ae941-151">Tallenna yhdistämismuutokset.</span><span class="sxs-lookup"><span data-stu-id="ae941-151">Save the mapping changes.</span></span>

2. <span data-ttu-id="ae941-152">Poista **Toimittajien V2**-yksikön muutosjäljitys käytöstä.</span><span class="sxs-lookup"><span data-stu-id="ae941-152">Disable the change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="ae941-153">Siirry kohtaan **Tietojen hallinta \> Tietoyksiköt**.</span><span class="sxs-lookup"><span data-stu-id="ae941-153">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="ae941-154">Valitse **Toimittajat V2**-yksikkö.</span><span class="sxs-lookup"><span data-stu-id="ae941-154">Select the **Vendors V2** entity.</span></span>
    
    3. <span data-ttu-id="ae941-155">Valitse valikkoriviltä **Asetukset** ja **Muuta seurantaa**.</span><span class="sxs-lookup"><span data-stu-id="ae941-155">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![itsenäinen tai kehäviittaus 5](media/selfref_options.png)
    
    4. <span data-ttu-id="ae941-157">Valitse **Poista muutosten jäljitys käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="ae941-157">Click **Disable Change Tracking**.</span></span>
    
        ![itsenäinen tai kehäviittaus 6](media/selfref_tracking.png)

3. <span data-ttu-id="ae941-159">Suorita **Toimittajien V2 (msdyn_vendors)** -määrityksen ensimmäinen synkronointi.</span><span class="sxs-lookup"><span data-stu-id="ae941-159">Run the initial sync of **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="ae941-160">Alkuperäisen synkronoinnin pitäisi toimia virheettä.</span><span class="sxs-lookup"><span data-stu-id="ae941-160">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="ae941-161">Suorita **CDS-yhteystiedot V2 (contacts)** -määrityksen ensimmäinen synkronointi.</span><span class="sxs-lookup"><span data-stu-id="ae941-161">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="ae941-162">Tämä yhdistämismääritys on synkronoitava, jos haluat synkronoida toimittajien ensisijaisen yhteystietokentän, koska yhteystietotietueet on myös ensin synkronoitava.</span><span class="sxs-lookup"><span data-stu-id="ae941-162">You must sync this mapping if you want to sync primary contact field on vendors entity as the contacts records also need to be initial synced.</span></span>

5. <span data-ttu-id="ae941-163">Lisää kentät **PrimaryContactPersonId** ja **InvoiceVendorAccountNumber** takaisin **Toimittajat V2 (msdyn_vendors)** -kartoitukseen ja tallenna yhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="ae941-163">Add the fields **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** back to the **Vendors V2 (msdyn_vendors)** mapping and save the mapping.</span></span>

6. <span data-ttu-id="ae941-164">Suorita uudelleen **Toimittajien V2 (msdyn_vendors)** -määrityksen ensimmäinen synkronointi.</span><span class="sxs-lookup"><span data-stu-id="ae941-164">Run the initial sync again for the **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="ae941-165">Kaikki tiedot synkronoidaan, koska muutosten seuranta on poistettu käytöstä.</span><span class="sxs-lookup"><span data-stu-id="ae941-165">All the records will be synced, because change tracking is disabled.</span></span>

7. <span data-ttu-id="ae941-166">Ota **Toimittajien V2** -yksikön muutosjäljitys käyttöön.</span><span class="sxs-lookup"><span data-stu-id="ae941-166">Enable change tracking for the **Vendors V2** entity.</span></span>

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="ae941-167">Asiakasyksikön yhdistämismäärityksen asiakkaiden V3-virheen ratkaiseminen</span><span class="sxs-lookup"><span data-stu-id="ae941-167">Resolve an error in Customers V3 to Accounts entity mapping</span></span>

<span data-ttu-id="ae941-168">Saatat joutua käyttämään seuraavia alkusynkronointivirheitä kohteesta **Asiakkaat V3** kohteen **Tilit**-kartoitukseen, jos entiteeteillä on aiemmin luotuja, **ContactPersonID**- ja **InvoiceAccount** -kenttien arvoja.</span><span class="sxs-lookup"><span data-stu-id="ae941-168">You might run into the following initial sync errors on the **Customers V3** to **Accounts** mapping if the entities have existing records with values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="ae941-169">Tämä johtuu siitä, että **InvoiceAccount** on itseviittaava kenttä ja **ContactPersonID** on kehäviittaus toimittajan yhdistämismäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="ae941-169">This because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="ae941-170">*Kentän GUID-arvon selvittäminen ei onnistunut: <field>. Hakua ei löydy: <value>. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="ae941-170">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

- <span data-ttu-id="ae941-171">*Kentän GUID-arvon selvittäminen ei onnistunut: primarycontactid.msdyn_contactpersonid. Hakua ei löydy: 000056. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="ae941-171">*Couldn't resolve the guid for the field: primarycontactid.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="ae941-172">*Kentän GUID-arvon selvittäminen ei onnistunut: msdyn_billingaccount.accountnumber. Hakua ei löydy: 1206-1. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span><span class="sxs-lookup"><span data-stu-id="ae941-172">*Couldn't resolve the guid for the field: msdyn_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span></span>

<span data-ttu-id="ae941-173">Jos asiakasyksikön kentissä on arvoja, joiden arvot ovat samat, suorita ensimmäinen synkronointi onnistuneesti noudattamalla alla olevan kohdan ohjeita.</span><span class="sxs-lookup"><span data-stu-id="ae941-173">If you have records with values in these fields in the customer entity follow the steps in the below section to complete initial sync successfully.</span></span> <span data-ttu-id="ae941-174">Tämän menetelmän avulla voit käyttää kaikkia tällaisia tilejä ja yhteyshenkilöitä.</span><span class="sxs-lookup"><span data-stu-id="ae941-174">You can use this approach for any out-of-the-box entities such Accounts and Contacts.</span></span>

1. <span data-ttu-id="ae941-175">Poista Finance and Operations -sovelluksessa **ContactPersonID**- ja **InvoiceAccount** -kentät **Asiakkaat V3 (accounts)** -määrityksestä ja tallenna määritys.</span><span class="sxs-lookup"><span data-stu-id="ae941-175">In the Finance and Operations app, delete the fields **ContactPersonID** and **InvoiceAccount** from the **Customers V3 (accounts)** mapping and save the mapping.</span></span>

    1. <span data-ttu-id="ae941-176">Siirry toimittajat-version **Asiakkaat V3 (accounts)** -kaksoiskirjoitusmääritysten sivulle ja valitse **yksiköiden yhdistämismääritykset** -välilehti. Valitse vasemmanpuoleisesta suodattimesta **Finance and Operations -sovellukset. Asiakkaat V3**.</span><span class="sxs-lookup"><span data-stu-id="ae941-176">Navigate to the dual-write mapping page for **Customers V3 (accounts)**, select the **Entity mappings** tab. In the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="ae941-177">Valitse oikeanpuoleisesta suodattimesta **Common Data Service.Account**.</span><span class="sxs-lookup"><span data-stu-id="ae941-177">In the right filter, select **Common Data Service.Account**.</span></span>

    2. <span data-ttu-id="ae941-178">Katso **contactperson** ja etsi lähdekenttä **ContactPersonID**.</span><span class="sxs-lookup"><span data-stu-id="ae941-178">Search for **contactperson** to find the source field **ContactPersonID**.</span></span>
    
    3. <span data-ttu-id="ae941-179">Napsauta **Toiminnot**-painiketta ja valitse **Poista**.</span><span class="sxs-lookup"><span data-stu-id="ae941-179">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![Itsenäinen tai kehäviittaus 3](media/cust_selfref3.png)
    
    4. <span data-ttu-id="ae941-181">Poista uudelleen, jos haluat poistaa **IInvoiceAccount**-kentän.</span><span class="sxs-lookup"><span data-stu-id="ae941-181">Repeat to delete the **InvoiceAccount** field.</span></span>
    
        ![Itsenäinen tai kehäviittaus](media/cust_selfref4.png)
    
    5. <span data-ttu-id="ae941-183">Tallenna yhdistämismuutokset.</span><span class="sxs-lookup"><span data-stu-id="ae941-183">Save the mapping changes.</span></span>

2. <span data-ttu-id="ae941-184">Poista **Asiakkaiden V3**-yksikön muutosjäljitys käytöstä.</span><span class="sxs-lookup"><span data-stu-id="ae941-184">Disable the change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="ae941-185">Siirry kohtaan **Tietojen hallinta \> Tietoyksiköt**.</span><span class="sxs-lookup"><span data-stu-id="ae941-185">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="ae941-186">Valitse **Asiakkaat V3**-yksikkö.</span><span class="sxs-lookup"><span data-stu-id="ae941-186">Select the **Customers V3** entity.</span></span>
    
    3. <span data-ttu-id="ae941-187">Valitse valikkoriviltä **Asetukset** ja **Muuta seurantaa**.</span><span class="sxs-lookup"><span data-stu-id="ae941-187">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![itsenäinen tai kehäviittaus 5](media/selfref_options.png)
    
    4. <span data-ttu-id="ae941-189">Valitse **Poista muutosten jäljitys käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="ae941-189">Click **Disable Change Tracking**.</span></span>
    
        ![itsenäinen tai kehäviittaus 6](media/selfref_tracking.png)

3. <span data-ttu-id="ae941-191">Suorita **Asiakkaat V3 (Accounts)** -määrityksen ensimmäinen synkronointi.</span><span class="sxs-lookup"><span data-stu-id="ae941-191">Run the initial sync for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="ae941-192">Alkuperäisen synkronoinnin pitäisi toimia virheettä.</span><span class="sxs-lookup"><span data-stu-id="ae941-192">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="ae941-193">Suorita **CDS-yhteystiedot V2 (contacts)** -määrityksen ensimmäinen synkronointi.</span><span class="sxs-lookup"><span data-stu-id="ae941-193">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="ae941-194">Samalla nimellä on 2 karttaa.</span><span class="sxs-lookup"><span data-stu-id="ae941-194">There are 2 maps with the same name.</span></span> <span data-ttu-id="ae941-195">Valitse se, jolla on kuvauksen **Kaksoiskirjoitusmalli synkronointiin FO.CDS Toimittajayhteyshenkilöiden V2 ja CDS.Contacts välillä. Vaatii uutta pakettia. \[Dynamics365SupplyChainExtended\] .**</span><span class="sxs-lookup"><span data-stu-id="ae941-195">Select the one with the description **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span> <span data-ttu-id="ae941-196">Kartan **Tiedot**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="ae941-196">on the **Details** tab of the map.</span></span>

5. <span data-ttu-id="ae941-197">Lisää **InvoiceAccount**- ja **ContactPersonId** -kentät **Asiakkaat V3 (accounts)** -määrityksestä ja tallenna määritys.</span><span class="sxs-lookup"><span data-stu-id="ae941-197">Add the fields **InvoiceAccount** and **ContactPersonId** back to the **Customers V3 (Accounts)** mapping and save the mapping.</span></span> <span data-ttu-id="ae941-198">Nyt sekä **InvoiceAccount**-kenttä että **ContactPersonId**-kenttä ovat jälleen osa live sync -tilaa.</span><span class="sxs-lookup"><span data-stu-id="ae941-198">Now, both the **InvoiceAccount** field and the **ContactPersonId** field are again part of live sync mode.</span></span> <span data-ttu-id="ae941-199">Seuraavassa vaiheessa näiden kenttien ensimmäinen synkronointi on valmis.</span><span class="sxs-lookup"><span data-stu-id="ae941-199">In the next step, you complete the initial sync for these fields.</span></span>

6. <span data-ttu-id="ae941-200">Suorita uudelleen **Asiakkaat V3 (Accounts)** -määrityksen ensimmäinen synkronointi.</span><span class="sxs-lookup"><span data-stu-id="ae941-200">Run the initial sync again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="ae941-201">Koska muutosten seuranta on poistettu käytöstä, synkronoinnin suoritus synkronoi **InvoiceAccount**- ja **ContactPersonId** -tiedot Finance and Operations -sovelluksesta Common Data Service -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="ae941-201">Because change tracking is disabled, running the sync will sync the data for **InvoiceAccount** and **ContactPersonId** from the Finance and Operations app to Common Data Service.</span></span>

7. <span data-ttu-id="ae941-202">Voit synkronoida **InvoiceAccount**- ja **ContactPersonId** -tiedot Common Data Service -järjestelmästä Finance and Operationsiin käyttämällä tietojen integrointiprojektia.</span><span class="sxs-lookup"><span data-stu-id="ae941-202">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations, you use a data integration project.</span></span>

    1. <span data-ttu-id="ae941-203">Luo Power Appsissa tietojen integrointiprojekti **Sales.Account**- ja **Finance and Operations apps.Customers V3** -entiteettien välille.</span><span class="sxs-lookup"><span data-stu-id="ae941-203">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="ae941-204">Tietojen suunnan on oltava peräisin Common Data Servicestä Finance and Operations -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="ae941-204">The data direction must be from Common Data Service to the Finance and Operations app.</span></span>  <span data-ttu-id="ae941-205">Koska **InvoiceAccount** on uusi määrite kaksoiskirjoituksessa, tämän määritteen ensimmäinen synkronointi kannattaa ohittaa.</span><span class="sxs-lookup"><span data-stu-id="ae941-205">Because **InvoiceAccount** is a new attribute in dual-write, you may want to skip initial sync for this attribute.</span></span> <span data-ttu-id="ae941-206">Lisätietoja on kohdassa [Tietojen integrointi Common Data Service -ratkaisuun](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="ae941-206">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="ae941-207">Seuraavassa kuvassa näkyy projekti, joka päivittää **CustomerAccount**- ja **ContactPersonId**-tunnukset.</span><span class="sxs-lookup"><span data-stu-id="ae941-207">The following image shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![Itsenäinen tai kehäviittaus](media/cust_selfref6.png)

    2. <span data-ttu-id="ae941-209">Lisää yrityksen ehdot suodattimen Common Data Service -sivulle, koska vain suodatusehtoja vastaavat tiedot päivitetään Finance and Operations -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="ae941-209">Add the company criteria in the filter on Common Data Service side, because only the records that match filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="ae941-210">Voit lisätä suodattimen napsauttamalla suodatinkuvaketta.</span><span class="sxs-lookup"><span data-stu-id="ae941-210">To add a filter, click the filter icon.</span></span> <span data-ttu-id="ae941-211">**Muokkaa kyselyä** -valintaikkunassa voit lisätä suodatinkyselyn, kuten **_msdyn_company_value eq '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="ae941-211">In the **Edit query** dialog, you can add a filter query like **_msdyn_company_value eq '\<guid\>'**.</span></span> <span data-ttu-id="ae941-212">Jos suodatinkuvake ei ole näkyvissä, luo tukipyyntö, jotta tietojen integrointiryhmä voi ottaa suodattimen käyttöön vuokraajalla.</span><span class="sxs-lookup"><span data-stu-id="ae941-212">If the filter icon is not present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span> <span data-ttu-id="ae941-213">Jos et määritä suodatinkyselyä kohteelle **_msdyn_company_value**, kaikki tiedot synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="ae941-213">If you do not enter a filter query for **_msdyn_company_value**, then all the records are synced.</span></span>

        ![Itsenäinen tai kehäviittaus](media/cust_selfref7.png)

        <span data-ttu-id="ae941-215">Tällöin tietueen ensimmäinen synkronointi on valmis.</span><span class="sxs-lookup"><span data-stu-id="ae941-215">This completes the initial sync of the records.</span></span>

8. <span data-ttu-id="ae941-216">Ota käyttöön **Asiakkaiden V3**-yksikön muutosjäljitys Finance and Operations -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="ae941-216">Enable change tracking for the **Customers V3** entity in the Finance and Operations app.</span></span>

