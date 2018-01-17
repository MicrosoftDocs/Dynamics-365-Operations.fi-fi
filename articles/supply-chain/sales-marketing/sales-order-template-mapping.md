---
title: Myyntitilauksien otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin
description: "Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin myyntitilausten otsikot ja rivit synkronoidaan Microsoft Dynamics 365 for Salesiin."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: d7e4c435a3344f6a5d66e1889b633d80cda085eb
ms.contentlocale: fi-fi
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="cd63d-103">Myyntitilauksien otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="cd63d-103">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cd63d-104">Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin myyntitilausten otsikot ja rivit synkronoidaan Microsoft Dynamics 365 for Salesiin.</span><span class="sxs-lookup"><span data-stu-id="cd63d-104">The topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="cd63d-105">Malli ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="cd63d-105">Template and tasks</span></span>

<span data-ttu-id="cd63d-106">Seuraavia malleja ja niiden taustalla olevia tehtäviä käytetään synkronoimaan myyntitilausten otsikot ja rivit Finance and Operationsista Salesiin:</span><span class="sxs-lookup"><span data-stu-id="cd63d-106">The following templates and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="cd63d-107">**Mallin nimi Tietojen integroinnissa**</span><span class="sxs-lookup"><span data-stu-id="cd63d-107">**Name of template in Data integration**</span></span> 

    - <span data-ttu-id="cd63d-108">Myyntitilaukset (Fin and Opsista Salesiin)</span><span class="sxs-lookup"><span data-stu-id="cd63d-108">Sales Orders (Fin and Ops to Sales)</span></span>
    
- <span data-ttu-id="cd63d-109">**Tietojen integrointiprojektin tehtävien nimet**</span><span class="sxs-lookup"><span data-stu-id="cd63d-109">**Names of tasks in Data integration project**</span></span>

    - <span data-ttu-id="cd63d-110">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="cd63d-110">OrderHeader</span></span>
    - <span data-ttu-id="cd63d-111">OrderLine</span><span class="sxs-lookup"><span data-stu-id="cd63d-111">OrderLine</span></span>

<span data-ttu-id="cd63d-112">Myyntilaskun otsikon ja rivien synkronointia edeltävät, pakolliset synkronointitehtävät:</span><span class="sxs-lookup"><span data-stu-id="cd63d-112">Sync tasks required prior to Sales invoice header and lines sync:</span></span>

- <span data-ttu-id="cd63d-113">Tuotteet (Fin and Opsista Salesiin)</span><span class="sxs-lookup"><span data-stu-id="cd63d-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="cd63d-114">Tilit (Salesista Fin and Opsiin) (jos käytössä)</span><span class="sxs-lookup"><span data-stu-id="cd63d-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="cd63d-115">Yhteyshenkilöstä asiakkaisiin (Salesista Fin and Opsiin) (jos käytössä)</span><span class="sxs-lookup"><span data-stu-id="cd63d-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="cd63d-116">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="cd63d-116">Entity set</span></span>

| <span data-ttu-id="cd63d-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cd63d-117">Finance and Operations</span></span> |    <span data-ttu-id="cd63d-118">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="cd63d-118">Common Data Service (CDS)</span></span>         |     <span data-ttu-id="cd63d-119">Myynti</span><span class="sxs-lookup"><span data-stu-id="cd63d-119">Sales</span></span>      |
|------------------------|----------------|----------------|
| <span data-ttu-id="cd63d-120">CDS myyntitilauksen otsikot</span><span class="sxs-lookup"><span data-stu-id="cd63d-120">CDS sales order headers</span></span>| <span data-ttu-id="cd63d-121">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="cd63d-121">SalesOrder</span></span>     | <span data-ttu-id="cd63d-122">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="cd63d-122">SalesOrders</span></span> |
| <span data-ttu-id="cd63d-123">CDS-myyntitilausrivit</span><span class="sxs-lookup"><span data-stu-id="cd63d-123">CDS sales order lines</span></span>  | <span data-ttu-id="cd63d-124">SalesOrderLine</span><span class="sxs-lookup"><span data-stu-id="cd63d-124">SalesOrderLine</span></span> | <span data-ttu-id="cd63d-125">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="cd63d-125">SalesOrderDetails</span></span>|

## <a name="entity-flow"></a><span data-ttu-id="cd63d-126">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="cd63d-126">Entity flow</span></span>

<span data-ttu-id="cd63d-127">Myyntitilaukset luodaan Finance and Operationsissa ja synkronoidaan Salesiin.</span><span class="sxs-lookup"><span data-stu-id="cd63d-127">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="cd63d-128">Mallin suodattimen varmistavat, että vain asiaankuuluvat myyntitilaukset synkronoidaan:</span><span class="sxs-lookup"><span data-stu-id="cd63d-128">Filters in the template ensure that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="cd63d-129">Salesista synkronoitavaan myyntitilaukseen sisältyvät niin tilaava kuin laskuttava asiakas.</span><span class="sxs-lookup"><span data-stu-id="cd63d-129">Both ordering and invoicing customer on the sales order that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="cd63d-130">Finance and Operationsin kenttiä **OrderingCustomerIsExternallyMaintained** ja **InvoiceCustomerIsExternallyMaintained** käytetään tietoyksiköiden synkronointien seurantaan.</span><span class="sxs-lookup"><span data-stu-id="cd63d-130">In Finance and Operations, the fields **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** are used to track the synchronization in the data entities.</span></span>

- <span data-ttu-id="cd63d-131">**Myyntitilaus** on vahvistettava Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="cd63d-131">The **Sales order** in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="cd63d-132">Salesiin synkronoidaan vain vahvistetut myyntitilaukset, tai tilaukset joilla on ylempi käsittelytila, kuten Toimitettu tai Laskutettu.</span><span class="sxs-lookup"><span data-stu-id="cd63d-132">Only the confirmed sales orders or sales orders with higher processing status, for example, Shipped or Invoiced status, are synchronized to Sales.</span></span>

- <span data-ttu-id="cd63d-133">Luotuasi tai muokattuasi myyntitilauksen, aja **Laske kokonaismyynti** -eräajo Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="cd63d-133">After creating or modifying a sales order, the batch job **Calculate sales totals** in Finance and Operations must be executed.</span></span> <span data-ttu-id="cd63d-134">CDS:ään ja Salesiin synkronoidaan ainoastaan myyntitilaukset, joiden kokonaismyynti on laskettu.</span><span class="sxs-lookup"><span data-stu-id="cd63d-134">Only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="cd63d-135">**Myyntitilauksen otsikon** kuluihin liittyviä veroja ei tällä hetkellä synkronoida Finance and Operationsista Salesiin.</span><span class="sxs-lookup"><span data-stu-id="cd63d-135">Tax related to charges on the **Sales order header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="cd63d-136">Tämä johtuu siitä, että Sales ei tue verotietoja otsikkotasolla.</span><span class="sxs-lookup"><span data-stu-id="cd63d-136">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="cd63d-137">Rivitason kuluihin liittyvät verot ovat tuettuja.</span><span class="sxs-lookup"><span data-stu-id="cd63d-137">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="cd63d-138">Salesin ratkaisu prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="cd63d-138">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="cd63d-139">**Tilaus**-yksikköön on lisätty uusia kenttiä, jotka näkyvät sivulla:</span><span class="sxs-lookup"><span data-stu-id="cd63d-139">New fields are added to the **Order** entity and displayed on the page:</span></span>

- <span data-ttu-id="cd63d-140">**Ulkoisesti ylläpidetty** - aseta arvoksi **Kyllä**, kun tilaus on peräisin Finance and Operationsista.</span><span class="sxs-lookup"><span data-stu-id="cd63d-140">**Is Maintained Externally** - Set to **Yes** when the order is coming from Finance and Operations.</span></span>

- <span data-ttu-id="cd63d-141">**Käsittelytila** - näyttää tilauksen käsittelytilan Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="cd63d-141">**Processing status** - Used to show the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="cd63d-142">Arvoja ovat</span><span class="sxs-lookup"><span data-stu-id="cd63d-142">Values are:</span></span>

    - <span data-ttu-id="cd63d-143">Aktiivinen</span><span class="sxs-lookup"><span data-stu-id="cd63d-143">Active</span></span>
    - <span data-ttu-id="cd63d-144">Vahvistettu</span><span class="sxs-lookup"><span data-stu-id="cd63d-144">Confirmed</span></span>
    - <span data-ttu-id="cd63d-145">Pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="cd63d-145">Packing Slip</span></span>
    - <span data-ttu-id="cd63d-146">Laskutettu</span><span class="sxs-lookup"><span data-stu-id="cd63d-146">Invoiced</span></span>
    - <span data-ttu-id="cd63d-147">Keräilty</span><span class="sxs-lookup"><span data-stu-id="cd63d-147">Picked</span></span>
    - <span data-ttu-id="cd63d-148">Osittain keräilty</span><span class="sxs-lookup"><span data-stu-id="cd63d-148">Partially Picked</span></span>
    - <span data-ttu-id="cd63d-149">Osittain pakattu</span><span class="sxs-lookup"><span data-stu-id="cd63d-149">Partially Packed</span></span>
    - <span data-ttu-id="cd63d-150">Lähetetty</span><span class="sxs-lookup"><span data-stu-id="cd63d-150">Shipped</span></span>
    - <span data-ttu-id="cd63d-151">Osittain lähetetty</span><span class="sxs-lookup"><span data-stu-id="cd63d-151">Partially Shipped</span></span>
    - <span data-ttu-id="cd63d-152">Osittain laskutettu</span><span class="sxs-lookup"><span data-stu-id="cd63d-152">Partially Invoiced</span></span>
    - <span data-ttu-id="cd63d-153">Peruutettu</span><span class="sxs-lookup"><span data-stu-id="cd63d-153">Cancelled</span></span>

<span data-ttu-id="cd63d-154">**Vain ulkoisesti ylläpidettyjä tuotteita** -asetusta käytetään muissa myyntitilausskenaarioissa (synkronointi Salesista Finance and Operationsiin), jotta järjestelmä voi seurata, koostuuko myyntitilaus täysin **ulkoisesti ylläpidetyistä tuotteista**, jolloin tuotteita ylläpidetään Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="cd63d-154">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (from Sales to Finance and Operation sync) to consistently keep track of whether the sales order is made up entirely of **Externally Maintained Products**, in which case products are maintained in Finance and Operations.</span></span> <span data-ttu-id="cd63d-155">Tämä varmistaa, ettet yritä synkronoida myyntitilausrivejä sellaisten tuotteiden kanssa, joita Finance and Operations ei tunne.</span><span class="sxs-lookup"><span data-stu-id="cd63d-155">This ensures that you don't try to sync sales order lines with products that are unknown to Finance and Operations.</span></span>
 
<span data-ttu-id="cd63d-156">**Myyntitilaus**-sivun **Luo lasku**, **Peruuta tilaus**, **Laske uudelleen**, **Hae tuotteet** ja **Hae osoite** -painikkeet on piilotettu ulkoisesti ylläpidetyissä tilauksissa, koska laskut luodaan Finance and Operationsissa, josta ne synkronoidaan Salesiin.</span><span class="sxs-lookup"><span data-stu-id="cd63d-156">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products** and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="cd63d-157">Tilaussivua ei voi muokata, sillä myyntitilaustiedot synkronoidaan Finance and Operationsista.</span><span class="sxs-lookup"><span data-stu-id="cd63d-157">The order page is non-editable because sales order information will be synced from Finance and Operations.</span></span>
 
<span data-ttu-id="cd63d-158">**Myyntitilauksen tila** pysyy aktiivisena, jotta muutokset Finance and Operationsista siirtyvät Salesin **myyntitilaukseen**.</span><span class="sxs-lookup"><span data-stu-id="cd63d-158">The **Sales order status** will remain active to ensure that changes from Finance and Operations can flow to the **Sales order** in Sales.</span></span> <span data-ttu-id="cd63d-159">Tämä määräytyy asettamalla **Tilakoodi [Status]** -oletusarvoksi **Aktiivinen** tietojen integrointiprojektissa.</span><span class="sxs-lookup"><span data-stu-id="cd63d-159">This is controlled by setting the default **Statecode [Status]** to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="cd63d-160">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="cd63d-160">Preconditions and mapping setup</span></span> 

<span data-ttu-id="cd63d-161">Järjestelmiin tulisi päivittää seuraavat asetukset ennen myyntitilausten synkronointia:</span><span class="sxs-lookup"><span data-stu-id="cd63d-161">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="cd63d-162">Asetukset Salesissa</span><span class="sxs-lookup"><span data-stu-id="cd63d-162">Setup in Sales</span></span>

- <span data-ttu-id="cd63d-163">Varmista, että käyttäjän ryhmän käyttöoikeudet (Salesin **Yhteysasetus**) on liitetty.</span><span class="sxs-lookup"><span data-stu-id="cd63d-163">Ensure permissions for the team that the user (from your Sales **Connection set**) is assigned to.</span></span> <span data-ttu-id="cd63d-164">Jos käytät esittelytietoja, käyttäjällä on usein järjestelmänvalvojan käyttöoikeudet, mutta ryhmällä ei.</span><span class="sxs-lookup"><span data-stu-id="cd63d-164">If you are using demo data, usually the user has admin access, but not the team.</span></span> <span data-ttu-id="cd63d-165">Ilman tätä asetusta näyttöön tulee virhe, Ensisijainen ryhmä puuttuu, kun projekti suoritetaan tietojen integrointitoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="cd63d-165">Without this you will get an error that Principal team is missing when running the project from Data integrator.</span></span> 

    - <span data-ttu-id="cd63d-166">Valitse **Asetukset** > **Suojaus** > **Ryhmät** ja sitten haluamasi ryhmän, valitse **Roolien hallinta** ja sitten rooli ja halutut käyttöoikeudet, esim. Järjestelmänvalvoja.</span><span class="sxs-lookup"><span data-stu-id="cd63d-166">Under **Settings** > **Security** > **Teams**, select the relevant team, click **Manage Roles** and select a role with the desired permissions e.g. System Administrator.</span></span>

- <span data-ttu-id="cd63d-167">Varmista kohdassa **Asetukset** > **Hallinto** > **Järjestelmäasetukset** > **Myynti**, että **Käytä järjestelmän hinnanlaskentajärjestelmää** -asetus on **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="cd63d-167">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="cd63d-168">Varmista kohdassa **Asetukset** > **Hallinto** > **Järjestelmäasetukset** > **Myynti**, että **Alennuksen laskutapa** -asetus on **Rivinimike**.</span><span class="sxs-lookup"><span data-stu-id="cd63d-168">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="cd63d-169">Asetukset Finance and Operationsissa</span><span class="sxs-lookup"><span data-stu-id="cd63d-169">Setup in Finance and Operations</span></span>

<span data-ttu-id="cd63d-170">Määritä **Myynti ja markkinointi** > **Kausittaiset tehtävät** > **Laske kokonaismyynti** suoritettavaksi erätyönä, jonka **Laske myyntitilausten loppusummat** -asetukseksi on määritetty **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="cd63d-170">Set **Sales and marketing** > **Periodic tasks** > **Calculate sales totals** to run as a batch job, with **Calculate totals for sales orders** set to **Yes**.</span></span> <span data-ttu-id="cd63d-171">Tämä on tärkeää, sillä CDS:ään ja Salesiin synkronoidaan ainoastaan myyntitilaukset, joiden kokonaismyynti on laskettu.</span><span class="sxs-lookup"><span data-stu-id="cd63d-171">This is important because only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span> <span data-ttu-id="cd63d-172">Erätyön toistovälin tulee olla sama kuin myyntitilausten toistoväli.</span><span class="sxs-lookup"><span data-stu-id="cd63d-172">The frequency of the batch job should be alligned with the frequency of the sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="cd63d-173">Asetukset tietojen integrointiprojektissa</span><span class="sxs-lookup"><span data-stu-id="cd63d-173">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="cd63d-174">SalesHeader -tehtävä</span><span class="sxs-lookup"><span data-stu-id="cd63d-174">SalesHeader task</span></span>

- <span data-ttu-id="cd63d-175">Päivitä yhdistämismääritys **CDS-organisaation tunnukselle kohdassa Lähde** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="cd63d-175">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span>

    - <span data-ttu-id="cd63d-176">**Account_Organization_OrganizationId**-oletusmalliarvo on ORG001.</span><span class="sxs-lookup"><span data-stu-id="cd63d-176">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="cd63d-177">**InvoiceAccount_Organization_OrganizationId**-oletusmalliarvo on ORG001.</span><span class="sxs-lookup"><span data-stu-id="cd63d-177">Default template value for **InvoiceAccount_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="cd63d-178">**Organization_OrganizationId**-oletusmalliarvo on ORG001.</span><span class="sxs-lookup"><span data-stu-id="cd63d-178">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="cd63d-179">Varmista, että tarvittavat yhdistämismääritykset on tehty kohtiin **Lähde** > **CDS for InvoiceCountryRegionId to BillingAddress_Country** ja **DeliveryCountryRegionId to DeliveryAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="cd63d-179">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId to BillingAddress_Country** and for **DeliveryCountryRegionId to DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="cd63d-180">Mallin arvo on **ValueMap**, johon on yhdistetty maiden määrä.</span><span class="sxs-lookup"><span data-stu-id="cd63d-180">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="cd63d-181">**Hinnasto** on pakollinen tilausten luontiin Salesissa.</span><span class="sxs-lookup"><span data-stu-id="cd63d-181">**Price list** is required to create orders in Sales.</span></span> <span data-ttu-id="cd63d-182">Päivitä **CDS**:n **ValueMap** -arvo > **Kohde** -kohdasta **pricelevelid.name [Hinnaston nimi]** arvoon Salesissa käytettävä valuuttakohtainen **Hinnasto**.</span><span class="sxs-lookup"><span data-stu-id="cd63d-182">Update the **ValueMap** in **CDS** > **Destination** for **pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="cd63d-183">Voit käyttää yhden valuutan oletusarvoista **hinnastoa** tai käyttää **ValueMap**-listaa, jos sinulla on useamman valuutan **hinnasto**.</span><span class="sxs-lookup"><span data-stu-id="cd63d-183">You can either used the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>
    
    - <span data-ttu-id="cd63d-184">Mallin **pricelevelid.name [Hinnaston nimi]** oletusarvo on CRM Service USA (sample).</span><span class="sxs-lookup"><span data-stu-id="cd63d-184">Default template value for **pricelevelid.name [Price List Name]** is CRM Service USA (sample).</span></span> 

#### <a name="salesline-task"></a><span data-ttu-id="cd63d-185">SalesLine -tehtävä</span><span class="sxs-lookup"><span data-stu-id="cd63d-185">SalesLine task</span></span>

- <span data-ttu-id="cd63d-186">Päivitä yhdistämismääritys **CDS-organisaation tunnukselle kohdassa Lähde** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="cd63d-186">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 
    
    - <span data-ttu-id="cd63d-187">**SalesOrder_Organization_OrganizationId**-oletusmalliarvo on ORG001.</span><span class="sxs-lookup"><span data-stu-id="cd63d-187">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="cd63d-188">**Product_Organization_OrganizationId**-oletusmalliarvo on ORG001.</span><span class="sxs-lookup"><span data-stu-id="cd63d-188">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="cd63d-189">Varmista, että tarvittava yhdistämismääritys on tehty kohtaan **Lähde** > **CDS** for **DeliveryCountryRegionId** to **DeliveryAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="cd63d-189">Ensure that the needed mapping exists in **Source** > **CDS** for **DeliveryCountryRegionId** to **DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="cd63d-190">Mallin arvo on **ValueMap**, johon on yhdistetty maiden määrä.</span><span class="sxs-lookup"><span data-stu-id="cd63d-190">Template value is **ValueMap** with a number of countries mapped.</span></span>
    
- <span data-ttu-id="cd63d-191">Varmista, että tarvittava **ValueMap** kohteelle **SalesUnitSymbol** on määritetty Finance and Operationsin kohdassa **Lähde** > **CDS-yhdistämismääritys**.</span><span class="sxs-lookup"><span data-stu-id="cd63d-191">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span>

    - <span data-ttu-id="cd63d-192">Mallin arvo **ValueMap** on määritetty arvoon **SalesUnitSymbol Quantity_UOM**.</span><span class="sxs-lookup"><span data-stu-id="cd63d-192">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="cd63d-193">Mallin yhdistäminen tietojen integrointiohjelmassa</span><span class="sxs-lookup"><span data-stu-id="cd63d-193">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="cd63d-194">**Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-kentät eivät sisälly oletusarvoisiin yhdistämismäärityksiin.</span><span class="sxs-lookup"><span data-stu-id="cd63d-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="cd63d-195">Näiden kenttien määrittämistä varten on määritettävä arvomääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="cd63d-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="cd63d-196">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integrointiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="cd63d-196">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="orderheader"></a><span data-ttu-id="cd63d-197">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="cd63d-197">OrderHeader</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-order-template-mapping-data-integrator-1.png)

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a><span data-ttu-id="cd63d-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="cd63d-200">OrderLine</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-order-template-mapping-data-integrator-3.png)

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="cd63d-203">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="cd63d-203">Related topics</span></span>

[<span data-ttu-id="cd63d-204">Finance and Operationsin tuotteiden synkronointi Salesin tuotteisiin</span><span class="sxs-lookup"><span data-stu-id="cd63d-204">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="cd63d-205">Salesin asiakkaiden synkronointi Finance and Operationsin asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="cd63d-205">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="cd63d-206">Salesin yhteyshenkilöiden synkronointi Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="cd63d-206">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="cd63d-207">Myyntitarjouksien otsikoiden ja rivien synkronointi Salesista Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="cd63d-207">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="cd63d-208">Myyntilaskujen otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="cd63d-208">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


