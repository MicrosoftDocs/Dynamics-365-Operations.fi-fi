---
title: Ongelmien vianmääritys synkronoinnin aikana
description: Tässä ohjeaiheessa on vianmääritys tietoja, joiden avulla voit korjata, joita saattaa ilmetä alkuperäisen synkronoinnin aikana.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: c716707140c85b06ad2f084c10c4b2d0ecfea82e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754011"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="f7fb3-103">Ongelmien vianmääritys synkronoinnin aikana</span><span class="sxs-lookup"><span data-stu-id="f7fb3-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f7fb3-104">Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Dataversen välillä.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="f7fb3-105">Erityisesti se tarjoaa tietoa, joiden avulla voit korjata virheitä, joita saattaa ilmetä alkuperäisen synkronoinnin aikana.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f7fb3-106">Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="f7fb3-107">Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="f7fb3-108">Finance and Operations -sovelluksen ensimmäisten synkronointivirheiden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="f7fb3-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="f7fb3-109">Kun otat yhdistämismallit käyttöön, karttojen tilan on oltava **Käytössä**.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="f7fb3-110">Jos tila on **ei käynnissä**, alkuperäisen synkronoinnin aikana ilmeni virheitä.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="f7fb3-111">Voit tarkastella virheitä valitsemalla **kaksoiskirjoitus**-sivun **ensimmäiset synkronointitiedot**-välilehden.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Virhe Alkuperäisen synkronoinnin tiedot -välilehdessä](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="f7fb3-113">Alkuperäistä synkronointia ei voi suorittaa loppuun: 400 virheellinen pyyntö</span><span class="sxs-lookup"><span data-stu-id="f7fb3-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="f7fb3-114">**Ongelman korjaamiseen tarvittava rooli:** Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="f7fb3-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="f7fb3-115">Näyttöön saattaa tulla seuraava virhesanoma, kun yrität suorittaa yhdistämismääritystä ja alkuperäistä synkronointia:</span><span class="sxs-lookup"><span data-stu-id="f7fb3-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="f7fb3-116">*(\[Virheellinen pyyntö\], Etäpalvelin palautti virheen: (400) Virheellinen pyyntö.), AX-vienti kohtasi virheen*</span><span class="sxs-lookup"><span data-stu-id="f7fb3-116">*(\[Bad Request\], The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="f7fb3-117">Esimerkki täydestä virheviestistä.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="f7fb3-118">Jos tämä virhe ilmenee jatkuvasti etkä voi suorittaa alkuperäistä synkronointia loppuun, korjaa ongelma noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="f7fb3-119">Kirjaudu sisään virtuaalikone (VM) Finance and Operationsille -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="f7fb3-120">Avaa Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="f7fb3-121">Varmista **Palvelut**-ruudussa, että Microsoft Dynamics 365 -tietojen tuonnin vientikehyspalvelu on käytössä.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="f7fb3-122">Käynnistä se uudelleen, jos se on pysäytetty, koska ensimmäinen synkronointi edellyttää sitä.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="f7fb3-123">Ensimmäinen synkronointivirhe: 403 kielletty</span><span class="sxs-lookup"><span data-stu-id="f7fb3-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="f7fb3-124">Seuraava virhesanoma saattaa tulla näyttöön alkuperäisen synkronoinnin aikana:</span><span class="sxs-lookup"><span data-stu-id="f7fb3-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="f7fb3-125">*(\[Kielletty\], Etäpalvelin palautti virheen: (403) Kielletty.), AX-vienti kohtasi virheen*</span><span class="sxs-lookup"><span data-stu-id="f7fb3-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="f7fb3-126">Korjaa ongelma seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="f7fb3-127">Kirjautuminen Finance and Operations -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="f7fb3-128">Poista **Azure Active Directory -sovellukset** -sivulla **DtAppID**-asiakasohjelma ja lisää se sitten uudelleen.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![DtAppID-asiakasohjelma Azure AD -sovellusten luettelossa](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="f7fb3-130">Itseensä viittaus- tai kehäviittausvirheet ensimmäisen synkronoinnin aikana</span><span class="sxs-lookup"><span data-stu-id="f7fb3-130">Self-reference or circular reference failures during initial synchronization</span></span>

<span data-ttu-id="f7fb3-131">Näyttöön saattaa tulla virhesanoma, jos jollakin yhdistämismäärityksistä on omia viittauksia tai kehäviittauksia.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="f7fb3-132">Virheet kuuluvat seuraaviin luokkiin:</span><span class="sxs-lookup"><span data-stu-id="f7fb3-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="f7fb3-133">Virheet Toimittajat V2 msdyn_vendors -taulun yhdistämismäärityksessä</span><span class="sxs-lookup"><span data-stu-id="f7fb3-133">Errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="f7fb3-134">Virheet Asiakkaat V3 tileille -taulun yhdistämismäärityksessä</span><span class="sxs-lookup"><span data-stu-id="f7fb3-134">Errors in the Customers V3–to–Accounts table mapping</span></span>](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="f7fb3-135">Toimittajat V2 msdyn_vendors -taulun yhdistämismäärityksen virheiden ratkaiseminen</span><span class="sxs-lookup"><span data-stu-id="f7fb3-135">Resolve errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>

<span data-ttu-id="f7fb3-136">**Toimittajat V2** kohteeseen tapahtuvassa **msdyn\_vendors** yhdistämismäärityksessä voi esiintyä ensimmäisen synkronoinnin virheitä, jos tauluissa on aiemmin luotuja rivejä, joiden **PrimaryContactPersonId**- ja **InvoiceVendorAccountNumber**-sarakkeissa on arvo.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-136">You might encounter initial synchronization errors for the mapping of **Vendors V2** to **msdyn\_vendors** if the tables have existing rows where there are values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns.</span></span> <span data-ttu-id="f7fb3-137">Nämä virheet johtuvat siitä, että **InvoiceVendorAccountNumber** on itseviittaava sarake ja **PrimaryContactPersonId** on kehäviittaus toimittajan yhdistämismäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-137">These errors occur because **InvoiceVendorAccountNumber** is a self-referencing column, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="f7fb3-138">Näiden virhesanomien muoto on seuraavanlainen:</span><span class="sxs-lookup"><span data-stu-id="f7fb3-138">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="f7fb3-139">*Kentän GUID-arvon selvittäminen ei onnistunut: \<field\>. Hakua ei löydy: \<value\>. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="f7fb3-139">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="f7fb3-140">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="f7fb3-140">Here are some examples:</span></span>

- <span data-ttu-id="f7fb3-141">*Kentän GUID-arvon selvittäminen ei onnistunut: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Hakua ei löydy: 000056. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="f7fb3-141">*Couldn't resolve the guid for the field: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="f7fb3-142">*Kentän GUID-arvon selvittäminen ei onnistunut: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Hakua ei löydy:V24-1 . Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span><span class="sxs-lookup"><span data-stu-id="f7fb3-142">*Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span></span>

<span data-ttu-id="f7fb3-143">Jos toimittajataulun rivien **PrimaryContactPersonId**- ja **InvoiceVendorAccountNumber**-sarakkeissa on arvoja, suorita ensimmäinen synkronointi loppuun seuraavien ohjeiden mukaisesti:</span><span class="sxs-lookup"><span data-stu-id="f7fb3-143">If any rows in the vendor table have values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns, follow these steps to complete the initial synchronization.</span></span>

1. <span data-ttu-id="f7fb3-144">Poista Finance and Operations -sovelluksessa **PrimaryContactPersonId**- ja **InvoiceVendorAccountNumber**-sarakkeet yhdistämismäärityksestä ja tallenna sitten yhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-144">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns from the mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="f7fb3-145">Valitse **Toimittajat V2 (msdyn\_vendors)** -kaksoiskirjoituksen määrityssivun **Taulujen yhdistämismääritykset** -välilehden vasemmassa suodattimessa **Finance and Operations -sovellukset Toimittajat V2**.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-145">On the dual-write mapping page for **Vendors V2 (msdyn\_vendors)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="f7fb3-146">Valitse oikeanpuoleisesta suodattimesta **Sales.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-146">In the right filter, select **Sales.Vendor**.</span></span>
    2. <span data-ttu-id="f7fb3-147">Käytä hakusanaa **primarycontactperson** ja etsi **PrimaryContactPersonId**-lähdesarake.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-147">Search for **primarycontactperson** to find the **PrimaryContactPersonId** source column.</span></span>
    3. <span data-ttu-id="f7fb3-148">Valitse ensin **Toiminnot** ja sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-148">Select **Actions**, and then select **Delete**.</span></span>

        ![PrimaryContactPersonId-sarakkeen poistaminen](media/vend_selfref3.png)

    4. <span data-ttu-id="f7fb3-150">Poista **InvoiceVendorAccountNumber**-sarake samalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-150">Repeat these steps to delete the **InvoiceVendorAccountNumber** column.</span></span>

        ![InvoiceVendorAccountNumber-sarakkeen poistaminen](media/vend-selfref4.png)

    5. <span data-ttu-id="f7fb3-152">Tallenna yhdistämismäärityksen muutokset.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-152">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="f7fb3-153">Poista **Toimittajien V2** -taulun muutosten seuranta käytöstä.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-153">Turn off change tracking for the **Vendors V2** table.</span></span>

    1. <span data-ttu-id="f7fb3-154">Valitse **Tiedonhallinta**-työtilassa **Tietotaulut**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-154">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="f7fb3-155">Valitse **Toimittajat V2**-taulu.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-155">Select the **Vendors V2** table.</span></span>
    3. <span data-ttu-id="f7fb3-156">Valitse toimintoruudussa **Vaihtoehdot** ja valitse sitten **Muutosten seuranta**.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-156">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Muutosten seuranta -vaihtoehdon valitseminen](media/selfref_options.png)

    4. <span data-ttu-id="f7fb3-158">Valitse **Poista muutosten seuranta käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-158">Select **Disable Change Tracking**.</span></span>

        ![Muutosten seurannan käytöstä poistamisen valinta](media/selfref_tracking.png)

3. <span data-ttu-id="f7fb3-160">Suorita **Toimittajat V2 (msdyn\_vendors)** -yhdistämismäärityksen ensimmäinen synkronointi.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-160">Run initial synchronization for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="f7fb3-161">Ensimmäisen synkronoinnin pitäisi onnistua ilman virheitä.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-161">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="f7fb3-162">Suorita **CDS-yhteyshenkilöt V2 (yhteyshenkilöt)** -yhdistämismäärityksen ensimmäinen synkronointi.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-162">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="f7fb3-163">Tämä yhdistämismääritys on synkronoitava, jos haluat synkronoida toimittajataulun ensisijaisen yhteyshenkilösarakkeen, koska ensimmäinen synkronointi on tehtävä myös yhteyshenkilörivien osalta.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-163">You must sync this mapping if you want to sync the primary contact column on the vendors table, because initial synchronization must also be done for the contact rows.</span></span>
5. <span data-ttu-id="f7fb3-164">Lisää **PrimaryContactPersonId**- ja **InvoiceVendorAccountNumber**-sarakkeet takaisin **Toimittajat V2 (msdyn\_vendors)** -yhdistämismääritykseen ja tallenna yhdistämismääritys sitten.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-164">Add the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns back to the **Vendors V2 (msdyn\_vendors)** mapping, and then save the mapping.</span></span>
6. <span data-ttu-id="f7fb3-165">Suorita **Toimittajat V2 (msdyn\_vendors)** -yhdistämismäärityksen ensimmäinen synkronointi uudelleen.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-165">Run initial synchronization again for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="f7fb3-166">Koska muutosten seuranta on poistettu käytöstä, kaikki taulut synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-166">Because change tracking is turned off, all the rows will be synced.</span></span>
7. <span data-ttu-id="f7fb3-167">Ota **Toimittajien V2** -taulun muutosten seuranta takaisin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-167">Turn change tracking back on for the **Vendors V2** table.</span></span>

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="f7fb3-168">Asiakkaat V3 tileille -taulun yhdistämismäärityksen virheiden ratkaiseminen</span><span class="sxs-lookup"><span data-stu-id="f7fb3-168">Resolve errors in the Customers V3–to–Accounts table mapping</span></span>

<span data-ttu-id="f7fb3-169">**Asiakkaat V3** **tileille** -yhdistämismäärityksessä voi esiintyä ensimmäisen synkronoinnin virheitä, jos tauluissa on aiemmin luotuja rivejä, joiden **ContactPersonID**- ja **InvoiceAccount**-sarakkeissa on arvo.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-169">You might encounter initial synchronization errors for the mapping of **Customers V3** to **Accounts** if the tables have existing rows where there are values in the **ContactPersonID** and **InvoiceAccount** columns.</span></span> <span data-ttu-id="f7fb3-170">Näiden virheiden syynä on se, että **InvoiceAccount** on itseviittaava sarake ja **ContactPersonID** on kehäviittaus toimittajan yhdistämismäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-170">These errors occur because **InvoiceAccount** is a self-referencing column, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="f7fb3-171">Näiden virhesanomien muoto on seuraavanlainen:</span><span class="sxs-lookup"><span data-stu-id="f7fb3-171">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="f7fb3-172">*Kentän GUID-arvon selvittäminen ei onnistunut: \<field\>. Hakua ei löydy: \<value\>. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="f7fb3-172">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="f7fb3-173">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="f7fb3-173">Here are some examples:</span></span>

- <span data-ttu-id="f7fb3-174">*Kentän GUID-arvon selvittäminen ei onnistunut: primarycontactid.msdyn\_contactpersonid. Hakua ei löydy: 000056. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="f7fb3-174">*Couldn't resolve the guid for the field: primarycontactid.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="f7fb3-175">*Kentän GUID-arvon selvittäminen ei onnistunut: msdyn\_billingaccount.accountnumber. Hakua ei löydy: 1206-1. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span><span class="sxs-lookup"><span data-stu-id="f7fb3-175">*Couldn't resolve the guid for the field: msdyn\_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span></span>

<span data-ttu-id="f7fb3-176">Jos asiakastaulun rivien **ContactPersonID**- ja **InvoiceAccount**-sarakkeissa on arvoja, suorita ensimmäinen synkronointi loppuun seuraavien ohjeiden mukaisesti:</span><span class="sxs-lookup"><span data-stu-id="f7fb3-176">If any rows in the customer table have values in the **ContactPersonID** and **InvoiceAccount** columns, follow these steps to complete the initial synchronization.</span></span> <span data-ttu-id="f7fb3-177">Tämän menetelmän avulla voit käyttää kaikkia valmiita tauluja, kuten **Tilejä** ja **Yhteyshenkilöitä**.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-177">You can use this approach for any out-of-box tables, such **Accounts** and **Contacts**.</span></span>

1. <span data-ttu-id="f7fb3-178">Poista Finance and Operations -sovelluksessa **ContactPersonID**- ja **InvoiceAccount** -sarakkeissa **Asiakkaat V3 (tilit)** -yhdistämismäärityksestä ja tallenna sitten yhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-178">In the Finance and Operations app, delete the **ContactPersonID** and **InvoiceAccount** columns from the **Customers V3 (accounts)** mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="f7fb3-179">Valitse **Asiakkaat V3 (tilit)** -kaksoiskirjoituksen määrityssivun **Taulujen yhdistämismääritykset** -välilehden vasemmassa suodattimessa **Finance and Operations -sovellukset. Asiakkaat V3**.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-179">On the dual-write mapping page for **Customers V3 (accounts)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="f7fb3-180">Valitse oikeanpuoleisesta suodattimesta **Dataverse.Account**.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-180">In the right filter, select **Dataverse.Account**.</span></span>
    2. <span data-ttu-id="f7fb3-181">Käytä hakusanaa **contactperson** ja etsi **ContactPersonID** lähdesarake.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-181">Search for **contactperson** to find the **ContactPersonID** source column.</span></span>
    3. <span data-ttu-id="f7fb3-182">Valitse ensin **Toiminnot** ja sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-182">Select **Actions**, and then select **Delete**.</span></span>

        ![ContactPersonID-sarakkeen poistaminen](media/cust_selfref3.png)

    4. <span data-ttu-id="f7fb3-184">Poista **InvoiceAccount**-sarake samalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-184">Repeat these steps to delete the **InvoiceAccount** column.</span></span>

        ![InvoiceAccount-sarakkeen poistaminen](media/cust_selfref4.png)

    5. <span data-ttu-id="f7fb3-186">Tallenna yhdistämismäärityksen muutokset.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-186">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="f7fb3-187">Poista **Toimittajien V3** -taulun muutosten seuranta käytöstä.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-187">Turn off change tracking for the **Customers V3** table.</span></span>

    1. <span data-ttu-id="f7fb3-188">Valitse **Tiedonhallinta**-työtilassa **Tietotaulut**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-188">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="f7fb3-189">Valitse **Asiakkaat V3** -taulu.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-189">Select the **Customers V3** table.</span></span>
    3. <span data-ttu-id="f7fb3-190">Valitse toimintoruudussa **Vaihtoehdot** ja valitse sitten **Muutosten seuranta**.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-190">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Muutosten seuranta -vaihtoehdon valitseminen](media/selfref_options.png)

    4. <span data-ttu-id="f7fb3-192">Valitse **Poista muutosten seuranta käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-192">Select **Disable Change Tracking**.</span></span>

        ![Muutosten seurannan käytöstä poistamisen valinta](media/selfref_tracking.png)

3. <span data-ttu-id="f7fb3-194">Suorita **Asiakkaat V3 (tilit)** -yhdistämismäärityksen ensimmäinen synkronointi.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-194">Run initial synchronization for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="f7fb3-195">Ensimmäisen synkronoinnin pitäisi onnistua ilman virheitä.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-195">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="f7fb3-196">Suorita **CDS-yhteyshenkilöt V2 (yhteyshenkilöt)** -yhdistämismäärityksen ensimmäinen synkronointi.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-196">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f7fb3-197">Kahdella yhdistämismäärityksellä on sama nimi.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-197">There are two maps that have the same name.</span></span> <span data-ttu-id="f7fb3-198">Varmista, että valitse yhdistämismäärityksen, jonka **Tiedot**-välilehdessä on seuraava kuvaus: **Kaksoiskirjoitusmalli synkronointiin FO.CDS Toimittajayhteyshenkilöiden V2 ja CDS.Contacts välillä. Tarvitaan uusi paketti \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="f7fb3-198">Be sure to select the map that has the following description on the **Details** tab: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span>

5. <span data-ttu-id="f7fb3-199">Lisää **InvoiceAccount**- ja **ContactPersonId** -sarakkeet takaisin **Asiakkaat V3 (tilit)** -yhdistämismääritykseen ja tallenna sitten yhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-199">Add the **InvoiceAccount** and **ContactPersonId** columns back to the **Customers V3 (Accounts)** mapping, and then save the mapping.</span></span> <span data-ttu-id="f7fb3-200">Sekä **InvoiceAccount**- että **ContactPersonId**-sarakkeet ovat nyt taas synkronoinnin live-tilan osa.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-200">Both the **InvoiceAccount** column and the **ContactPersonId** column are now part of live synchronization mode again.</span></span> <span data-ttu-id="f7fb3-201">Seuraavassa vaiheessa tehdään näiden sarakkeiden ensimmäinen synkronointi.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-201">In the next step, you will do the initial synchronization for these columns.</span></span>
6. <span data-ttu-id="f7fb3-202">Suorita uudelleen **Asiakkaat V3 (tilit)** -yhdistämismäärityksen ensimmäinen synkronointi.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-202">Run initial synchronization again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="f7fb3-203">Koska muutosten seuranta on poistettu käytöstä, **InvoiceAccount**- ja **ContactPersonId** -tiedot synkronoidaan Finance and Operations -sovelluksesta Dataverse en.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-203">Because change tracking is turned off, the data for **InvoiceAccount** and **ContactPersonId** will be synced from the Finance and Operations app to Dataverse.</span></span>
7. <span data-ttu-id="f7fb3-204">**InvoiceAccount**- ja **ContactPersonId** -tietojen synkronoinnissa Dataversesta Finance and Operations -sovelluksiin on käytettävä tietojen integrointiprojektia.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-204">To sync the data for **InvoiceAccount** and **ContactPersonId** from Dataverse to the Finance and Operations app, you must use a data integration project.</span></span>

    1. <span data-ttu-id="f7fb3-205">Luo Power Appsissa tietojen integrointiprojekti **Sales.Account**- ja **Finance and Operations apps.Customers V3** -taulujen välille.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-205">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** tables.</span></span> <span data-ttu-id="f7fb3-206">Tietojen suunnan on oltava peräisin Dataversestä Finance and Operations -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-206">The data direction must be from Dataverse to the Finance and Operations app.</span></span> <span data-ttu-id="f7fb3-207">Koska **InvoiceAccount** on uusi kaksoiskirjoituksen määrite, sen ensimmäinen synkronointi kannattaa ehkä ohittaa.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-207">Because **InvoiceAccount** is a new attribute in dual-write, you might want to skip initial synchronization for it.</span></span> <span data-ttu-id="f7fb3-208">Lisätietoja on kohdassa [Tietojen integrointi Dataverse -ratkaisuun](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="f7fb3-208">For more information, see [Integrate data into Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="f7fb3-209">Seuraavassa kuvassa on projekti, joka päivittää **CustomerAccount**- ja **ContactPersonId**-määritteet.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-209">The following illustration shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![CustomerAccount- ja ContactPersonId-määritteet päivittävä tietojen integrointiprojekti](media/cust_selfref6.png)

    2. <span data-ttu-id="f7fb3-211">Lisää yrityksen ehdot suodattimen Dataversen puolelle, jotta vain suodatusehtoja vastaavat rivit päivitetään Finance and Operations -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-211">Add the company criteria in the filter on the Dataverse side, so that only rows that match the filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="f7fb3-212">Lisää suodatin valitsemalla suodatinpainike.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-212">To add a filter, select the filter button.</span></span> <span data-ttu-id="f7fb3-213">Voit sitten lisätä **Muokkaa kyselytä** -valintaikkunassa suodatinkyselyn, kuten **\_msdyn\_company\_value eq '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-213">Then, in the **Edit query** dialog box, you can add a filter query such as **\_msdyn\_company\_value eq '\<guid\>'**.</span></span> 

        > <span data-ttu-id="f7fb3-214">[HUOMAUTUS] Jos suodatinpainike ei ole näkyvissä, luo tukipyyntö, jotta tietojen integrointiryhmä voi ottaa suodattimen käyttöön vuokraajassa.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-214">[NOTE] If the filter button isn't present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span>

        <span data-ttu-id="f7fb3-215">Jos suodatinkyselyä **\_msdyn\_company\_value** ei määritetä, kaikki rivit synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-215">If you don't enter a filter query for **\_msdyn\_company\_value**, all the rows will be synced.</span></span>

        ![Suodatinkyselyn lisääminen](media/cust_selfref7.png)

    <span data-ttu-id="f7fb3-217">Rivien ensimmäinen synkronointi on nyt valmis.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-217">The initial synchronization of the rows is now completed.</span></span>

8. <span data-ttu-id="f7fb3-218">Ota muutosten seuranta taas käyttöön Finance and Operations -sovelluksen **Asiakkaat V3** -taulussa.</span><span class="sxs-lookup"><span data-stu-id="f7fb3-218">In the Finance and Operations app, turn change tracking back on for the **Customers V3** table.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]