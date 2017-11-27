---
title: Myyntilaskujen otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin
description: "Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin myyntilaskujen otsikot ja rivit synkronoidaan Microsoft Dynamics 365 for Salesiin."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 22ab02555dcac850b18aac9564af41d6c627eade
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="d58d5-103">Myyntilaskujen otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="d58d5-103">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d58d5-104">Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin myyntilaskujen otsikot ja rivit synkronoidaan Microsoft Dynamics 365 for Salesiin.</span><span class="sxs-lookup"><span data-stu-id="d58d5-104">The topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="d58d5-105">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="d58d5-105">Templates and tasks</span></span>

<span data-ttu-id="d58d5-106">Seuraavia malleja ja niiden taustalla olevia tehtäviä käytetään synkronoimaan myyntilaskujen otsikot ja rivit Finance and Operationsista Salesiin:</span><span class="sxs-lookup"><span data-stu-id="d58d5-106">The following templates and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="d58d5-107">**Mallin nimi Tietojen integroinnissa**</span><span class="sxs-lookup"><span data-stu-id="d58d5-107">**Name of the template in Data integration**</span></span> 

     - <span data-ttu-id="d58d5-108">Myyntilaskut (Fin and Opsista Salesiin)</span><span class="sxs-lookup"><span data-stu-id="d58d5-108">Sales Invoices (Fin and Ops to Sales)</span></span>

- <span data-ttu-id="d58d5-109">**Tietojen integrointiprojektin tehtävien nimet**</span><span class="sxs-lookup"><span data-stu-id="d58d5-109">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="d58d5-110">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="d58d5-110">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="d58d5-111">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="d58d5-111">SalesInvoiceLine</span></span>

<span data-ttu-id="d58d5-112">Myyntilaskun otsikon ja rivien synkronointia edeltävät, pakolliset synkronointitehtävät:</span><span class="sxs-lookup"><span data-stu-id="d58d5-112">Sync tasks required prior to Sales invoice header and lines synchronization:</span></span>
-   <span data-ttu-id="d58d5-113">Tuotteet (Fin and Opsista Salesiin)</span><span class="sxs-lookup"><span data-stu-id="d58d5-113">Products (Fin and Ops to Sales)</span></span>
-   <span data-ttu-id="d58d5-114">Tilit (Salesista Fin and Opsiin) (jos käytössä)</span><span class="sxs-lookup"><span data-stu-id="d58d5-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="d58d5-115">Yhteystiedot (Salesista Fin and Opsiin) (jos käytössä)</span><span class="sxs-lookup"><span data-stu-id="d58d5-115">Contacts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="d58d5-116">Myyntitilauksen otsikko ja rivit (Fin and Opsista Salesiin)</span><span class="sxs-lookup"><span data-stu-id="d58d5-116">Sales order header and lines (Fin and Ops to Sales)</span></span>

## <a name="entity-set"></a><span data-ttu-id="d58d5-117">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="d58d5-117">Entity set</span></span>

| <span data-ttu-id="d58d5-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d58d5-118">Finance and Operations</span></span>                               | <span data-ttu-id="d58d5-119">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="d58d5-119">Common Data Service (CDS)</span></span>              | <span data-ttu-id="d58d5-120">Myynti</span><span class="sxs-lookup"><span data-stu-id="d58d5-120">Sales</span></span>          |
|------------------------------------------------------|------------------|----------------|
| <span data-ttu-id="d58d5-121">Ulkoisesti ylläpidettyjen asiakkaiden myyntilaskujen otsikot</span><span class="sxs-lookup"><span data-stu-id="d58d5-121">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="d58d5-122">SalesInvoice</span><span class="sxs-lookup"><span data-stu-id="d58d5-122">SalesInvoice</span></span>     | <span data-ttu-id="d58d5-123">Laskut</span><span class="sxs-lookup"><span data-stu-id="d58d5-123">Invoices</span></span>       |
| <span data-ttu-id="d58d5-124">Ulkoisesti ylläpidettyjen asiakkaiden myyntilaskun rivit</span><span class="sxs-lookup"><span data-stu-id="d58d5-124">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="d58d5-125">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="d58d5-125">SalesInvoiceLine</span></span> | <span data-ttu-id="d58d5-126">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="d58d5-126">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="d58d5-127">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="d58d5-127">Entity flow</span></span>

<span data-ttu-id="d58d5-128">Myyntilaskut luodaan Finance and Operationsissa ja synkronoidaan Salesiin.</span><span class="sxs-lookup"><span data-stu-id="d58d5-128">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="d58d5-129">**Myyntilaskun otsikon** kuluihin liittyviä veroja ei tällä hetkellä synkronoida Finance and Operationsista Salesiin.</span><span class="sxs-lookup"><span data-stu-id="d58d5-129">Tax related to charges on the **Sales invoice header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="d58d5-130">Tämä johtuu siitä, että Sales ei tue verotietoja otsikkotasolla.</span><span class="sxs-lookup"><span data-stu-id="d58d5-130">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="d58d5-131">Rivitason kuluihin liittyvät verot ovat tuettuja.</span><span class="sxs-lookup"><span data-stu-id="d58d5-131">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="d58d5-132">Salesin ratkaisu prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="d58d5-132">Prospect to cash solution for Sales</span></span>

-  <span data-ttu-id="d58d5-133">**Laskun numero -kenttään** lisätään **Lasku**-yksikköön ja se näytetään sivulla.</span><span class="sxs-lookup"><span data-stu-id="d58d5-133">An **Invoice number field** is added to the **Invoice** entity and displayed on the page.</span></span>
 
-  <span data-ttu-id="d58d5-134">**Myyntitilaus**-sivun **Luo lasku** -painike on piilotettu, koska laskut luodaan Finance and Operationsissa, josta ne synkronoidaan Salesiin.</span><span class="sxs-lookup"><span data-stu-id="d58d5-134">The **Create invoice** button on the **Sales order** page is hidden because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="d58d5-135">**Laskusivua** ei voi muokata, sillä laskut synkronoidaan Finance and Operationsista.</span><span class="sxs-lookup"><span data-stu-id="d58d5-135">The **Invoice** page is non-editable because invoices will be synced from Finance and Operations.</span></span>
 
-  <span data-ttu-id="d58d5-136">**Myyntitilauksen tila** muuttuu automaattisesti **Laskutettu**-tilaan, kun liittyvä lasku on synkronoitu Finance and Operationsista Salesiin.</span><span class="sxs-lookup"><span data-stu-id="d58d5-136">The **Sales order status** changes automatically to **Invoiced** when the related invoice from Finance and Operations has been  synchronized to Sales.</span></span> <span data-ttu-id="d58d5-137">Laskun omistajaksi määritetään sen myyntitilauksen omistaja, josta lasku on muodostettu.</span><span class="sxs-lookup"><span data-stu-id="d58d5-137">Also, the owner of the sales order from which the invoice was created is assigned as the owner of the invoice.</span></span> <span data-ttu-id="d58d5-138">Näin myyntitilauksen omistaja voi tarkastella laskua.</span><span class="sxs-lookup"><span data-stu-id="d58d5-138">This gives the owner of the sales order the ability to view the invoice.</span></span>
 
## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="d58d5-139">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="d58d5-139">Preconditions and mapping setup</span></span>

<span data-ttu-id="d58d5-140">Järjestelmiin tulisi päivittää seuraavat asetukset ennen myyntilaskujen synkronointia:</span><span class="sxs-lookup"><span data-stu-id="d58d5-140">Before synchronizing sales invoices, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="d58d5-141">Asetukset Salesissa</span><span class="sxs-lookup"><span data-stu-id="d58d5-141">Setup in Sales</span></span>

- <span data-ttu-id="d58d5-142">Varmista kohdassa **Asetukset** > **Hallinto** > **Järjestelmäasetukset** > **Myynti**, että **Käytä järjestelmän hinnanlaskentajärjestelmää** -asetus on **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="d58d5-142">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="d58d5-143">Varmista kohdassa **Asetukset** > **Hallinto** > **Järjestelmäasetukset** > **Myynti**, että **Alennuksen laskutapa** -asetus on **Rivinimike**.</span><span class="sxs-lookup"><span data-stu-id="d58d5-143">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="d58d5-144">Asetukset tietojen integrointiprojektissa</span><span class="sxs-lookup"><span data-stu-id="d58d5-144">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="d58d5-145">SalesInvoiceHeader -tehtävä</span><span class="sxs-lookup"><span data-stu-id="d58d5-145">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="d58d5-146">Päivitä yhdistämismääritys **CDS-organisaation tunnukselle** kohdassa **Lähde** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="d58d5-146">Update the mapping for **CDS Organization ID** in **Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="d58d5-147">**SalesOrder_Organization_OrganizationId**-oletusmalliarvo on ORG001.</span><span class="sxs-lookup"><span data-stu-id="d58d5-147">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="d58d5-148">**Account_Organization_OrganizationId**-oletusmalliarvo on ORG001.</span><span class="sxs-lookup"><span data-stu-id="d58d5-148">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="d58d5-149">**Organization_OrganizationId**-oletusmalliarvo on ORG001.</span><span class="sxs-lookup"><span data-stu-id="d58d5-149">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="d58d5-150">Varmista, että tarvittava yhdistämismääritys on tehty kohtaan **Lähde** > **CDS for InvoiceCountryRegionId** to **BillingAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="d58d5-150">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId** to **BillingAddress_Country**.</span></span>

    -  <span data-ttu-id="d58d5-151">Mallin arvo on **ValueMap**, johon on yhdistetty maiden määrä.</span><span class="sxs-lookup"><span data-stu-id="d58d5-151">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="d58d5-152">**Hinnasto** on pakollinen laskujen luontiin Salesissa.</span><span class="sxs-lookup"><span data-stu-id="d58d5-152">**Price list** is required to create invoices in Sales.</span></span> <span data-ttu-id="d58d5-153">Päivitä **CDS**:n **ValueMap** -arvo > **Kohde -kohdasta pricelevelid.name [Hinnaston nimi]** arvoon Salesissa käytettävä valuuttakohtainen **Hinnasto**.</span><span class="sxs-lookup"><span data-stu-id="d58d5-153">Update the **ValueMap** in **CDS** > **Destination for pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="d58d5-154">Voit käyttää yhden valuutan oletusarvoista **hinnastoa** tai käyttää **ValueMap**-listaa, jos sinulla on useamman valuutan **hinnasto**.</span><span class="sxs-lookup"><span data-stu-id="d58d5-154">You can either use the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>

    -  <span data-ttu-id="d58d5-155">Mallin arvo **pricelevelid.name [Hinta nimi]** -mallille on **ValueMap**, joka perustuu **valuuttaan**.</span><span class="sxs-lookup"><span data-stu-id="d58d5-155">Template value for **pricelevelid.name [Price List Name]** is **ValueMap** based on **Currency**.</span></span>
    -  <span data-ttu-id="d58d5-156">usd: CRM Service USA (esimerkki).</span><span class="sxs-lookup"><span data-stu-id="d58d5-156">usd: CRM Service USA (sample).</span></span> 

#### <a name="salesinvoiceline-task"></a><span data-ttu-id="d58d5-157">SalesInvoiceLine -tehtävä</span><span class="sxs-lookup"><span data-stu-id="d58d5-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="d58d5-158">Varmista, että tarvittava yhdistämismääritys on luotu kohtaan **Lähde** > **CDS mittayksikölle**.</span><span class="sxs-lookup"><span data-stu-id="d58d5-158">Ensure that the needed mapping exists in **Source** > **CDS for Unit of measure**.</span></span>

- <span data-ttu-id="d58d5-159">Varmista, että tarvittava **ValueMap** kohteelle **SalesUnitSymbol** on määritetty Finance and Operationsin kohdassa **Lähde** > **CDS-yhdistämismääritys**.</span><span class="sxs-lookup"><span data-stu-id="d58d5-159">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span> 
    
    - <span data-ttu-id="d58d5-160">Mallin arvo **ValueMap** on määritetty arvoon **SalesUnitSymbol Quantity_UOM**.</span><span class="sxs-lookup"><span data-stu-id="d58d5-160">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>
    
-  <span data-ttu-id="d58d5-161">Päivitä yhdistämismääritys **CDS-organisaation tunnukselle kohdassa Lähde** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="d58d5-161">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="d58d5-162">**SalesInvoicer_Organization_OrganizationId**-oletusmalliarvo on ORG001.</span><span class="sxs-lookup"><span data-stu-id="d58d5-162">Default template value for **SalesInvoicer_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="d58d5-163">**Product_Organization_OrganizationId**-oletusmalliarvo on ORG001.</span><span class="sxs-lookup"><span data-stu-id="d58d5-163">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>
 
## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="d58d5-164">Mallin yhdistäminen tietojen integrointiohjelmassa</span><span class="sxs-lookup"><span data-stu-id="d58d5-164">Template mapping in Data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="d58d5-165">**Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila** eivät sisälly oletusarvoisiin yhdistämismäärityksiin.</span><span class="sxs-lookup"><span data-stu-id="d58d5-165">**Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** are not part of the default mappings.</span></span> <span data-ttu-id="d58d5-166">Näiden kenttien yhdistäminen edellyttää arvomäärityksen määrittämistä, joka koskee vain niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="d58d5-166">Mapping of these fields requires value mapping to be set up, which is specific to the data in the organizations between which the entity is synchronized.</span></span>

<span data-ttu-id="d58d5-167">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integrointiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="d58d5-167">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="d58d5-172">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="d58d5-172">Related topics</span></span>

[<span data-ttu-id="d58d5-173">Finance and Operationsin tuotteiden synkronointi Salesin tuotteisiin</span><span class="sxs-lookup"><span data-stu-id="d58d5-173">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="d58d5-174">Salesin asiakkaiden synkronointi Finance and Operationsin asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="d58d5-174">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="d58d5-175">Salesin yhteyshenkilöiden synkronointi Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="d58d5-175">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="d58d5-176">Myyntitarjouksien otsikoiden ja rivien synkronointi Salesista Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="d58d5-176">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="d58d5-177">Myyntitilauksien otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="d58d5-177">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)


