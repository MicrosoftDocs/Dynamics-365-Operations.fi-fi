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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 4d0ca1fb4b7a4964194516544686b6bb7d26e76c
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997323"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="aed6f-103">Ongelmien vianmääritys synkronoinnin aikana</span><span class="sxs-lookup"><span data-stu-id="aed6f-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aed6f-104">Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Common Data Servicen välillä.</span><span class="sxs-lookup"><span data-stu-id="aed6f-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="aed6f-105">Erityisesti se tarjoaa tietoa, joiden avulla voit korjata virheitä, joita saattaa ilmetä alkuperäisen synkronoinnin aikana.</span><span class="sxs-lookup"><span data-stu-id="aed6f-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aed6f-106">Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia.</span><span class="sxs-lookup"><span data-stu-id="aed6f-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="aed6f-107">Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.</span><span class="sxs-lookup"><span data-stu-id="aed6f-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="aed6f-108">Finance and Operations -sovelluksen ensimmäisten synkronointivirheiden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="aed6f-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="aed6f-109">Kun otat yhdistämismallit käyttöön, karttojen tilan on oltava **Käytössä**.</span><span class="sxs-lookup"><span data-stu-id="aed6f-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="aed6f-110">Jos tila on **ei käynnissä** , alkuperäisen synkronoinnin aikana ilmeni virheitä.</span><span class="sxs-lookup"><span data-stu-id="aed6f-110">If the status is **Not running** , errors occurred during initial synchronization.</span></span> <span data-ttu-id="aed6f-111">Voit tarkastella virheitä valitsemalla **kaksoiskirjoitus** -sivun **ensimmäiset synkronointitiedot** -välilehden.</span><span class="sxs-lookup"><span data-stu-id="aed6f-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Virhe Alkuperäisen synkronoinnin tiedot -välilehdessä](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="aed6f-113">Alkuperäistä synkronointia ei voi suorittaa loppuun: 400 virheellinen pyyntö</span><span class="sxs-lookup"><span data-stu-id="aed6f-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="aed6f-114">**Ongelman korjaamiseen tarvittava rooli:** Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="aed6f-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="aed6f-115">Näyttöön saattaa tulla seuraava virhesanoma, kun yrität suorittaa yhdistämismääritystä ja alkuperäistä synkronointia:</span><span class="sxs-lookup"><span data-stu-id="aed6f-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="aed6f-116">*(\[Virheellinen pyyntö\], Etäpalvelin palautti virheen: (400) Virheellinen pyyntö.), AX-vienti kohtasi virheen*</span><span class="sxs-lookup"><span data-stu-id="aed6f-116">*(\[Bad Request\], The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="aed6f-117">Esimerkki täydestä virheviestistä.</span><span class="sxs-lookup"><span data-stu-id="aed6f-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="aed6f-118">Jos tämä virhe ilmenee jatkuvasti etkä voi suorittaa alkuperäistä synkronointia loppuun, korjaa ongelma noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="aed6f-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="aed6f-119">Kirjaudu sisään virtuaalikone (VM) Finance and Operationsille -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="aed6f-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="aed6f-120">Avaa Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="aed6f-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="aed6f-121">Varmista **Palvelut** -ruudussa, että Microsoft Dynamics 365 -tietojen tuonnin vientikehyspalvelu on käytössä.</span><span class="sxs-lookup"><span data-stu-id="aed6f-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="aed6f-122">Käynnistä se uudelleen, jos se on pysäytetty, koska ensimmäinen synkronointi edellyttää sitä.</span><span class="sxs-lookup"><span data-stu-id="aed6f-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="aed6f-123">Ensimmäinen synkronointivirhe: 403 kielletty</span><span class="sxs-lookup"><span data-stu-id="aed6f-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="aed6f-124">Seuraava virhesanoma saattaa tulla näyttöön alkuperäisen synkronoinnin aikana:</span><span class="sxs-lookup"><span data-stu-id="aed6f-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="aed6f-125">*(\[Kielletty\], Etäpalvelin palautti virheen: (403) Kielletty.), AX-vienti kohtasi virheen*</span><span class="sxs-lookup"><span data-stu-id="aed6f-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="aed6f-126">Korjaa ongelma seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="aed6f-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="aed6f-127">Kirjautuminen Finance and Operations -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="aed6f-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="aed6f-128">Poista **Azure Active Directory -sovellukset** -sivulla **DtAppID** -asiakasohjelma ja lisää se sitten uudelleen.</span><span class="sxs-lookup"><span data-stu-id="aed6f-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![DtAppID-asiakasohjelma Azure AD -sovellusten luettelossa](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="aed6f-130">Itseensä viittaus- tai kehäviittausvirheet ensimmäisen synkronoinnin aikana</span><span class="sxs-lookup"><span data-stu-id="aed6f-130">Self-reference or circular reference failures during initial synchronization</span></span>

<span data-ttu-id="aed6f-131">Näyttöön saattaa tulla virhesanoma, jos jollakin yhdistämismäärityksistä on omia viittauksia tai kehäviittauksia.</span><span class="sxs-lookup"><span data-stu-id="aed6f-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="aed6f-132">Virheet kuuluvat seuraaviin luokkiin:</span><span class="sxs-lookup"><span data-stu-id="aed6f-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="aed6f-133">Virheet Toimittajat V2 msdyn_vendors -entiteetin yhdistämismäärityksessä</span><span class="sxs-lookup"><span data-stu-id="aed6f-133">Errors in the Vendors V2–to–msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="aed6f-134">Virheet Asiakkaat V3 tileille -entiteetin yhdistämismäärityksessä</span><span class="sxs-lookup"><span data-stu-id="aed6f-134">Errors in the Customers V3–to–Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="aed6f-135">Toimittajat V2 msdyn_vendors -entiteetin yhdistämismäärityksen virheiden ratkaiseminen</span><span class="sxs-lookup"><span data-stu-id="aed6f-135">Resolve errors in the Vendors V2–to–msdyn_vendors entity mapping</span></span>

<span data-ttu-id="aed6f-136">**Toimittajat V2** kohteeseen tapahtuvassa **msdyn\_vendors** yhdistämismäärityksessä voi esiintyä ensimmäisen synkronoinnin virheitä, jos entiteeteissä on aiemmin luotuja tietueita, joiden **PrimaryContactPersonId** - ja **InvoiceVendorAccountNumber** -kentissä on arvo.</span><span class="sxs-lookup"><span data-stu-id="aed6f-136">You might encounter initial synchronization errors for the mapping of **Vendors V2** to **msdyn\_vendors** if the entities have existing records where there are values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="aed6f-137">Nämä virheet johtuvat siitä, että **InvoiceVendorAccountNumber** on itseviittaava kenttä ja **PrimaryContactPersonId** on kehäviittaus toimittajan yhdistämismäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="aed6f-137">These errors occur because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="aed6f-138">Näiden virhesanomien muoto on seuraavanlainen:</span><span class="sxs-lookup"><span data-stu-id="aed6f-138">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="aed6f-139">*Kentän GUID-arvon selvittäminen ei onnistunut: \<field\>. Hakua ei löydy: \<value\>. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="aed6f-139">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="aed6f-140">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="aed6f-140">Here are some examples:</span></span>

- <span data-ttu-id="aed6f-141">*Kentän GUID-arvon selvittäminen ei onnistunut: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Hakua ei löydy: 000056. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="aed6f-141">*Couldn't resolve the guid for the field: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="aed6f-142">*Kentän GUID-arvon selvittäminen ei onnistunut: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Hakua ei löydy:V24-1 . Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span><span class="sxs-lookup"><span data-stu-id="aed6f-142">*Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span></span>

<span data-ttu-id="aed6f-143">Jos toimittajaentiteetin tietueiden **PrimaryContactPersonId** - ja **InvoiceVendorAccountNumber** -kentissä on arvoja, suorita ensimmäinen synkronointi loppuun seuraavien ohjeiden mukaisesti:</span><span class="sxs-lookup"><span data-stu-id="aed6f-143">If any records in the vendor entity have values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields, follow these steps to complete the initial synchronization.</span></span>

1. <span data-ttu-id="aed6f-144">Poista Finance and Operations -sovelluksessa **PrimaryContactPersonId** - ja **InvoiceVendorAccountNumber** -kentät yhdistämismäärityksestä ja tallenna sitten yhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="aed6f-144">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="aed6f-145">Valitse **Toimittajat V2 (msdyn\_vendors)** -kaksoiskirjoituksen määrityssivun **Entiteettien yhdistämismääritykset** -välilehden vasemmassa suodattimessa **Finance and Operations -sovellukset. Toimittajat V2**.</span><span class="sxs-lookup"><span data-stu-id="aed6f-145">On the dual-write mapping page for **Vendors V2 (msdyn\_vendors)** , on the **Entity mappings** tab, in the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="aed6f-146">Valitse oikeanpuoleisesta suodattimesta **Sales.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="aed6f-146">In the right filter, select **Sales.Vendor**.</span></span>
    2. <span data-ttu-id="aed6f-147">Käytä hakusanaa **primarycontactperson** ja etsi **PrimaryContactPersonId** -lähdekenttä.</span><span class="sxs-lookup"><span data-stu-id="aed6f-147">Search for **primarycontactperson** to find the **PrimaryContactPersonId** source field.</span></span>
    3. <span data-ttu-id="aed6f-148">Valitse ensin **Toiminnot** ja sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="aed6f-148">Select **Actions** , and then select **Delete**.</span></span>

        ![PrimaryContactPersonId-kentän poistaminen](media/vend_selfref3.png)

    4. <span data-ttu-id="aed6f-150">Poista **InvoiceVendorAccountNumber** -kenttä samalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="aed6f-150">Repeat these steps to delete the **InvoiceVendorAccountNumber** field.</span></span>

        ![InvoiceVendorAccountNumber-kentän poistaminen](media/vend-selfref4.png)

    5. <span data-ttu-id="aed6f-152">Tallenna yhdistämismäärityksen muutokset.</span><span class="sxs-lookup"><span data-stu-id="aed6f-152">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="aed6f-153">Poista **Toimittajien V2** -entiteetin muutosten seuranta käytöstä.</span><span class="sxs-lookup"><span data-stu-id="aed6f-153">Turn off change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="aed6f-154">Valitse **Tiedonhallinta** -työtilassa **Tietoyksiköt** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="aed6f-154">In the **Data management** workspace, select the **Data entities** tile.</span></span>
    2. <span data-ttu-id="aed6f-155">Valitse **Toimittajat V2** -yksikkö.</span><span class="sxs-lookup"><span data-stu-id="aed6f-155">Select the **Vendors V2** entity.</span></span>
    3. <span data-ttu-id="aed6f-156">Valitse toimintoruudussa **Vaihtoehdot** ja valitse sitten **Muutosten seuranta**.</span><span class="sxs-lookup"><span data-stu-id="aed6f-156">On the Action Pane, select **Options** , and then select **Change tracking**.</span></span>

        ![Muutosten seuranta -vaihtoehdon valitseminen](media/selfref_options.png)

    4. <span data-ttu-id="aed6f-158">Valitse **Poista muutosten seuranta käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="aed6f-158">Select **Disable Change Tracking**.</span></span>

        ![Muutosten seurannan käytöstä poistamisen valinta](media/selfref_tracking.png)

3. <span data-ttu-id="aed6f-160">Suorita **Toimittajat V2 (msdyn\_vendors)** -yhdistämismäärityksen ensimmäinen synkronointi.</span><span class="sxs-lookup"><span data-stu-id="aed6f-160">Run initial synchronization for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="aed6f-161">Ensimmäisen synkronoinnin pitäisi onnistua ilman virheitä.</span><span class="sxs-lookup"><span data-stu-id="aed6f-161">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="aed6f-162">Suorita **CDS-yhteyshenkilöt V2 (yhteyshenkilöt)** -yhdistämismäärityksen ensimmäinen synkronointi.</span><span class="sxs-lookup"><span data-stu-id="aed6f-162">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="aed6f-163">Tämä yhdistämismääritys on synkronoitava, jos haluat synkronoida toimittajanentiteetin ensisijaisen yhteyshenkilökentän, koska ensimmäinen synkronointi on tehtävä myös yhteyshenkilötietueiden osalta.</span><span class="sxs-lookup"><span data-stu-id="aed6f-163">You must sync this mapping if you want to sync the primary contact field on the vendors entity, because initial synchronization must also be done for the contact records.</span></span>
5. <span data-ttu-id="aed6f-164">Lisää **PrimaryContactPersonId** - ja **InvoiceVendorAccountNumber** -kentät takaisin **Toimittajat V2 (msdyn\_vendors)** -yhdistämismääritykseen ja tallenna yhdistämismääritys sitten.</span><span class="sxs-lookup"><span data-stu-id="aed6f-164">Add the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields back to the **Vendors V2 (msdyn\_vendors)** mapping, and then save the mapping.</span></span>
6. <span data-ttu-id="aed6f-165">Suorita **Toimittajat V2 (msdyn\_vendors)** -yhdistämismäärityksen ensimmäinen synkronointi uudelleen.</span><span class="sxs-lookup"><span data-stu-id="aed6f-165">Run initial synchronization again for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="aed6f-166">Koska muutosten seuranta on poistettu käytöstä, kaikki tietueet synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="aed6f-166">Because change tracking is turned off, all the records will be synced.</span></span>
7. <span data-ttu-id="aed6f-167">Ota **Toimittajien V2** -entiteetin muutosten seuranta takaisin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="aed6f-167">Turn change tracking back on for the **Vendors V2** entity.</span></span>

## <a name="resolve-errors-in-the-customers-v3toaccounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="aed6f-168">Asiakkaat V3 tileille -entiteetin yhdistämismäärityksen virheiden ratkaiseminen</span><span class="sxs-lookup"><span data-stu-id="aed6f-168">Resolve errors in the Customers V3–to–Accounts entity mapping</span></span>

<span data-ttu-id="aed6f-169">**Asiakkaat V3** **tileille** - yhdistämismäärityksessä voi esiintyä ensimmäisen synkronoinnin virheitä, jos entiteeteissä on aiemmin luotuja tietueita, joiden **ContactPersonID** - ja **InvoiceAccount** -kentissä on arvo.</span><span class="sxs-lookup"><span data-stu-id="aed6f-169">You might encounter initial synchronization errors for the mapping of **Customers V3** to **Accounts** if the entities have existing records where there are values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="aed6f-170">Näiden virheiden syynä on se, että **InvoiceAccount** on itseviittaava kenttä ja **ContactPersonID** on kehäviittaus toimittajan yhdistämismäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="aed6f-170">These errors occur because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="aed6f-171">Näiden virhesanomien muoto on seuraavanlainen:</span><span class="sxs-lookup"><span data-stu-id="aed6f-171">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="aed6f-172">*Kentän GUID-arvon selvittäminen ei onnistunut: \<field\>. Hakua ei löydy: \<value\>. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="aed6f-172">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="aed6f-173">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="aed6f-173">Here are some examples:</span></span>

- <span data-ttu-id="aed6f-174">*Kentän GUID-arvon selvittäminen ei onnistunut: primarycontactid.msdyn\_contactpersonid. Hakua ei löydy: 000056. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="aed6f-174">*Couldn't resolve the guid for the field: primarycontactid.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="aed6f-175">*Kentän GUID-arvon selvittäminen ei onnistunut: msdyn\_billingaccount.accountnumber. Hakua ei löydy: 1206-1. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span><span class="sxs-lookup"><span data-stu-id="aed6f-175">*Couldn't resolve the guid for the field: msdyn\_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span></span>

<span data-ttu-id="aed6f-176">Jos asiakasentiteetin tietueiden **ContactPersonID** - ja **InvoiceAccount** -kentissä on arvoja, suorita ensimmäinen synkronointi loppuun seuraavien ohjeiden mukaisesti:</span><span class="sxs-lookup"><span data-stu-id="aed6f-176">If any records in the customer entity have values in the **ContactPersonID** and **InvoiceAccount** fields, follow these steps to complete the initial synchronization.</span></span> <span data-ttu-id="aed6f-177">Tämän menetelmän avulla voit käyttää kaikkia tällaisia valmiita entiteettejä, kuten **tilejä** ja **yhteyshenkilöitä**.</span><span class="sxs-lookup"><span data-stu-id="aed6f-177">You can use this approach for any out-of-box entities, such **Accounts** and **Contacts**.</span></span>

1. <span data-ttu-id="aed6f-178">Poista Finance and Operations -sovelluksessa **ContactPersonID** - ja **InvoiceAccount** -kentät **Asiakkaat V3 (tilit)** -yhdistämismäärityksestä ja tallenna sitten yhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="aed6f-178">In the Finance and Operations app, delete the **ContactPersonID** and **InvoiceAccount** fields from the **Customers V3 (accounts)** mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="aed6f-179">Valitse **Asiakkaat V3 (tilit)** -kaksoiskirjoituksen määrityssivun **Entiteettien yhdistämismääritykset** -välilehden vasemmassa suodattimessa **Finance and Operations -sovellukset. Asiakkaat V3**.</span><span class="sxs-lookup"><span data-stu-id="aed6f-179">On the dual-write mapping page for **Customers V3 (accounts)** , on the **Entity mappings** tab, in the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="aed6f-180">Valitse oikeanpuoleisesta suodattimesta **Common Data Service.Account**.</span><span class="sxs-lookup"><span data-stu-id="aed6f-180">In the right filter, select **Common Data Service.Account**.</span></span>
    2. <span data-ttu-id="aed6f-181">Käytä hakusanaa **contactperson** ja etsi **ContactPersonID** lähdekenttä.</span><span class="sxs-lookup"><span data-stu-id="aed6f-181">Search for **contactperson** to find the **ContactPersonID** source field.</span></span>
    3. <span data-ttu-id="aed6f-182">Valitse ensin **Toiminnot** ja sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="aed6f-182">Select **Actions** , and then select **Delete**.</span></span>

        ![ContactPersonID-kentän poistaminen](media/cust_selfref3.png)

    4. <span data-ttu-id="aed6f-184">Poista **InvoiceAccount** -kenttä samalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="aed6f-184">Repeat these steps to delete the **InvoiceAccount** field.</span></span>

        ![InvoiceAccount-kentän poistaminen](media/cust_selfref4.png)

    5. <span data-ttu-id="aed6f-186">Tallenna yhdistämismäärityksen muutokset.</span><span class="sxs-lookup"><span data-stu-id="aed6f-186">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="aed6f-187">Poista **Toimittajien V3** -entiteetin muutosten seuranta käytöstä.</span><span class="sxs-lookup"><span data-stu-id="aed6f-187">Turn off change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="aed6f-188">Valitse **Tiedonhallinta** -työtilassa **Tietoyksiköt** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="aed6f-188">In the **Data management** workspace, select the **Data entities** tile.</span></span>
    2. <span data-ttu-id="aed6f-189">Valitse **Asiakkaat V3** -yksikkö.</span><span class="sxs-lookup"><span data-stu-id="aed6f-189">Select the **Customers V3** entity.</span></span>
    3. <span data-ttu-id="aed6f-190">Valitse toimintoruudussa **Vaihtoehdot** ja valitse sitten **Muutosten seuranta**.</span><span class="sxs-lookup"><span data-stu-id="aed6f-190">On the Action Pane, select **Options** , and then select **Change tracking**.</span></span>

        ![Muutosten seuranta -vaihtoehdon valitseminen](media/selfref_options.png)

    4. <span data-ttu-id="aed6f-192">Valitse **Poista muutosten seuranta käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="aed6f-192">Select **Disable Change Tracking**.</span></span>

        ![Muutosten seurannan käytöstä poistamisen valinta](media/selfref_tracking.png)

3. <span data-ttu-id="aed6f-194">Suorita **Asiakkaat V3 (tilit)** -yhdistämismäärityksen ensimmäinen synkronointi.</span><span class="sxs-lookup"><span data-stu-id="aed6f-194">Run initial synchronization for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="aed6f-195">Ensimmäisen synkronoinnin pitäisi onnistua ilman virheitä.</span><span class="sxs-lookup"><span data-stu-id="aed6f-195">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="aed6f-196">Suorita **CDS-yhteyshenkilöt V2 (yhteyshenkilöt)** -yhdistämismäärityksen ensimmäinen synkronointi.</span><span class="sxs-lookup"><span data-stu-id="aed6f-196">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span>

    > [!NOTE]
    > <span data-ttu-id="aed6f-197">Kahdella yhdistämismäärityksellä on sama nimi.</span><span class="sxs-lookup"><span data-stu-id="aed6f-197">There are two maps that have the same name.</span></span> <span data-ttu-id="aed6f-198">Varmista, että valitse yhdistämismäärityksen, jonka **Tiedot** -välilehdessä on seuraava kuvaus: **Kaksoiskirjoitusmalli synkronointiin FO.CDS Toimittajayhteyshenkilöiden V2 ja CDS.Contacts välillä. Tarvitaan uusi paketti \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="aed6f-198">Be sure to select the map that has the following description on the **Details** tab: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span>

5. <span data-ttu-id="aed6f-199">Lisää **InvoiceAccount** - ja **ContactPersonId** -kentät takaisin **Asiakkaat V3 (tilit)** -yhdistämismääritykseen ja tallenna sitten yhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="aed6f-199">Add the **InvoiceAccount** and **ContactPersonId** fields back to the **Customers V3 (Accounts)** mapping, and then save the mapping.</span></span> <span data-ttu-id="aed6f-200">Sekä **InvoiceAccount** - että **ContactPersonId** -kenttä ovat nyt taas synkronoinnin live-tilan osa.</span><span class="sxs-lookup"><span data-stu-id="aed6f-200">Both the **InvoiceAccount** field and the **ContactPersonId** field are now part of live synchronization mode again.</span></span> <span data-ttu-id="aed6f-201">Seuraavassa vaiheessa tehdään näiden kenttien ensimmäinen synkronointi.</span><span class="sxs-lookup"><span data-stu-id="aed6f-201">In the next step, you will do the initial synchronization for these fields.</span></span>
6. <span data-ttu-id="aed6f-202">Suorita uudelleen **Asiakkaat V3 (tilit)** -yhdistämismäärityksen ensimmäinen synkronointi.</span><span class="sxs-lookup"><span data-stu-id="aed6f-202">Run initial synchronization again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="aed6f-203">Koska muutosten seuranta on poistettu käytöstä, **InvoiceAccount** - ja **ContactPersonId** -tiedot synkronoidaan Finance and Operations -sovelluksesta Common Data Service en.</span><span class="sxs-lookup"><span data-stu-id="aed6f-203">Because change tracking is turned off, the data for **InvoiceAccount** and **ContactPersonId** will be synced from the Finance and Operations app to Common Data Service.</span></span>
7. <span data-ttu-id="aed6f-204">**InvoiceAccount** - ja **ContactPersonId** -tietojen synkronoinnissa Common Data Servicesta Finance and Operations -sovelluksiin on käytettävä tietojen integrointiprojektia.</span><span class="sxs-lookup"><span data-stu-id="aed6f-204">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations app, you must use a data integration project.</span></span>

    1. <span data-ttu-id="aed6f-205">Luo Power Appsissa tietojen integrointiprojekti **Sales.Account** - ja **Finance and Operations apps.Customers V3** -entiteettien välille.</span><span class="sxs-lookup"><span data-stu-id="aed6f-205">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="aed6f-206">Tietojen suunnan on oltava peräisin Common Data Servicestä Finance and Operations -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="aed6f-206">The data direction must be from Common Data Service to the Finance and Operations app.</span></span> <span data-ttu-id="aed6f-207">Koska **InvoiceAccount** on uusi kaksoiskirjoituksen määrite, sen ensimmäinen synkronointi kannattaa ehkä ohittaa.</span><span class="sxs-lookup"><span data-stu-id="aed6f-207">Because **InvoiceAccount** is a new attribute in dual-write, you might want to skip initial synchronization for it.</span></span> <span data-ttu-id="aed6f-208">Lisätietoja on kohdassa [Tietojen integrointi Common Data Service -ratkaisuun](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="aed6f-208">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="aed6f-209">Seuraavassa kuvassa on projekti, joka päivittää **CustomerAccount** - ja **ContactPersonId** -määritteet.</span><span class="sxs-lookup"><span data-stu-id="aed6f-209">The following illustration shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![CustomerAccount- ja ContactPersonId-määritteet päivittävä tietojen integrointiprojekti](media/cust_selfref6.png)

    2. <span data-ttu-id="aed6f-211">Lisää yrityksen ehdot suodattimen Common Data Servicen puolelle, jotta vain suodatusehtoja vastaavat tiedot päivitetään Finance and Operations -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="aed6f-211">Add the company criteria in the filter on the Common Data Service side, so that only records that match the filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="aed6f-212">Lisää suodatin valitsemalla suodatinpainike.</span><span class="sxs-lookup"><span data-stu-id="aed6f-212">To add a filter, select the filter button.</span></span> <span data-ttu-id="aed6f-213">Voit sitten lisätä **Muokkaa kyselytä** -valintaikkunassa suodatinkyselyn, kuten **\_msdyn\_company\_value eq '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="aed6f-213">Then, in the **Edit query** dialog box, you can add a filter query such as **\_msdyn\_company\_value eq '\<guid\>'**.</span></span> 

        > <span data-ttu-id="aed6f-214">[HUOMAUTUS] Jos suodatinpainike ei ole näkyvissä, luo tukipyyntö, jotta tietojen integrointiryhmä voi ottaa suodattimen käyttöön vuokraajassa.</span><span class="sxs-lookup"><span data-stu-id="aed6f-214">[NOTE] If the filter button isn't present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span>

        <span data-ttu-id="aed6f-215">Jos suodatinkyselyä **\_msdyn\_company\_value** ei määritetä, kaikki tietueet synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="aed6f-215">If you don't enter a filter query for **\_msdyn\_company\_value** , all the records will be synced.</span></span>

        ![Suodatinkyselyn lisääminen](media/cust_selfref7.png)

    <span data-ttu-id="aed6f-217">Tietueiden ensimmäinen synkronointi on nyt valmis.</span><span class="sxs-lookup"><span data-stu-id="aed6f-217">The initial synchronization of the records is now completed.</span></span>

8. <span data-ttu-id="aed6f-218">Ota muutosten seuranta taas käyttöön Finance and Operations -sovelluksen **Asiakkaat V3** -entiteetissä.</span><span class="sxs-lookup"><span data-stu-id="aed6f-218">In the Finance and Operations app, turn change tracking back on for the **Customers V3** entity.</span></span>
