---
title: Myyntilaskujen otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin
description: "Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operationsin myyntilaskujen otsikot ja rivit synkronoidaan suoraan Microsoft Dynamics 365 for Salesiin."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 70fc842463254b02d812447f93970a9da676057d
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="846e4-103">Myyntilaskujen otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="846e4-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="846e4-104">Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operationsin myyntilaskujen otsikot ja rivit synkronoidaan suoraan Microsoft Dynamics 365 for Salesiin.</span><span class="sxs-lookup"><span data-stu-id="846e4-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="846e4-105">Prospektista käteiseksi -ratkaisun tiedonkulku</span><span class="sxs-lookup"><span data-stu-id="846e4-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="846e4-106">Prospektista käteiseksi -ratkaisu käyttää tietojen integrointitoimintoa Finance and Operations and Sales -esiintymien tietojen synkronoinnissa.</span><span class="sxs-lookup"><span data-stu-id="846e4-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="846e4-107">Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Finance and Operationsin ja Salesin välillä.</span><span class="sxs-lookup"><span data-stu-id="846e4-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="846e4-108">Seuraavassa kuvassa kerrotaan, miten tiedot synkronoidaan Finance and Operations- ja Sales-sovelluksen välillä.</span><span class="sxs-lookup"><span data-stu-id="846e4-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="846e4-109">[![Prospektista käteiseksi -ratkaisun tiedonkulku](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="846e4-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="846e4-110">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="846e4-110">Templates and tasks</span></span>

<span data-ttu-id="846e4-111">Näet käytettävissä olevat mallit avaamalla [PowerApps-hallintakeskuksen](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="846e4-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="846e4-112">Valitse **Projektit** ja valitse sitten julkisia malleja oikeassa yläkulmassa olevan **Uusi projekti** -kohdan avulla.</span><span class="sxs-lookup"><span data-stu-id="846e4-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="846e4-113">Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan myyntilaskujen otsikot ja rivit Finance and Operationsista Salesiin:</span><span class="sxs-lookup"><span data-stu-id="846e4-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="846e4-114">**Mallin nimi tietojen integroinnissa:** Myyntilaskut (Fin and Opsista Salesiin) – suora</span><span class="sxs-lookup"><span data-stu-id="846e4-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="846e4-115">**Tehtävien nimet tietojen integrointiprojektissa:**</span><span class="sxs-lookup"><span data-stu-id="846e4-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="846e4-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="846e4-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="846e4-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="846e4-117">SalesInvoiceLine</span></span>

<span data-ttu-id="846e4-118">Seuraavat synkronointitehtävät tarvitaan, ennen kuin myyntilaskujen otsikot ja rivit voidaan synkronoida:</span><span class="sxs-lookup"><span data-stu-id="846e4-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="846e4-119">Tuotteet (Fin and Opsista Salesiin) - suora</span><span class="sxs-lookup"><span data-stu-id="846e4-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="846e4-120">Tilit (Salesista Fin and Opsiin) - suora (jos käytössä)</span><span class="sxs-lookup"><span data-stu-id="846e4-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="846e4-121">Yhteyshenkilöt (Salesista Fin and Opsiin) - suora (jos käytössä)</span><span class="sxs-lookup"><span data-stu-id="846e4-121">Contacts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="846e4-122">Myyntitilauksen otsikko ja rivit (Fin and Opsista Salesiin) - suora</span><span class="sxs-lookup"><span data-stu-id="846e4-122">Sales order header and lines (Fin and Ops to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="846e4-123">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="846e4-123">Entity set</span></span>

| <span data-ttu-id="846e4-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="846e4-124">Finance and Operations</span></span>                               | <span data-ttu-id="846e4-125">Myynti</span><span class="sxs-lookup"><span data-stu-id="846e4-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="846e4-126">Ulkoisesti ylläpidettyjen asiakkaiden myyntilaskujen otsikot</span><span class="sxs-lookup"><span data-stu-id="846e4-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="846e4-127">Laskut</span><span class="sxs-lookup"><span data-stu-id="846e4-127">Invoices</span></span>       |
| <span data-ttu-id="846e4-128">Ulkoisesti ylläpidettyjen asiakkaiden myyntilaskun rivit</span><span class="sxs-lookup"><span data-stu-id="846e4-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="846e4-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="846e4-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="846e4-130">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="846e4-130">Entity flow</span></span>

<span data-ttu-id="846e4-131">Myyntilaskut luodaan Finance and Operationsissa ja synkronoidaan Salesiin.</span><span class="sxs-lookup"><span data-stu-id="846e4-131">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="846e4-132">Tällä hetkellä myyntilaskun otsikon kuluihin liittyviä veroja ei synkronoida Finance and Operationsista Salesiin.</span><span class="sxs-lookup"><span data-stu-id="846e4-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="846e4-133">Sales ei tue verotietoja otsikkotasolla.</span><span class="sxs-lookup"><span data-stu-id="846e4-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="846e4-134">Sen sijaan rivitason kuluihin liittyvä vero sisällytetään synkronointiin.</span><span class="sxs-lookup"><span data-stu-id="846e4-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="846e4-135">Salesin ratkaisu prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="846e4-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="846e4-136">**Laskun numero** -kenttä on lisätty **Lasku**-yksikköön. Se näkyy sivulla.</span><span class="sxs-lookup"><span data-stu-id="846e4-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="846e4-137">**Myyntitilaus**-sivun **Luo lasku** -painike on piilotettu, koska laskut luodaan Finance and Operationsissa, josta ne synkronoidaan Salesiin.</span><span class="sxs-lookup"><span data-stu-id="846e4-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="846e4-138">**Lasku**-sivua ei voi muokata, sillä laskut synkronoidaan Finance and Operationsista.</span><span class="sxs-lookup"><span data-stu-id="846e4-138">The **Invoice** page can't be edited, because invoices will be synchronized from Finance and Operations.</span></span>
- <span data-ttu-id="846e4-139">**Myyntitilauksen tila** -arvo muuttuu automaattisesti **Laskutettu**-tilaksi, kun liittyvä lasku on synkronoitu Finance and Operationsista Salesiin.</span><span class="sxs-lookup"><span data-stu-id="846e4-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Finance and Operations has been synchronized to Sales.</span></span> <span data-ttu-id="846e4-140">Lisäksi laskun omistajaksi määritetään sen myyntitilauksen omistaja, josta lasku on muodostettu.</span><span class="sxs-lookup"><span data-stu-id="846e4-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="846e4-141">Tämän vuoksi myyntitilauksen omistaja voi tarkastella laskua.</span><span class="sxs-lookup"><span data-stu-id="846e4-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="846e4-142">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="846e4-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="846e4-143">Seuraavat asetukset tulee päivittää järjestelmissä ennen myyntilaskujen synkronointia.</span><span class="sxs-lookup"><span data-stu-id="846e4-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="846e4-144">Asetukset Salesissa</span><span class="sxs-lookup"><span data-stu-id="846e4-144">Setup in Sales</span></span>

<span data-ttu-id="846e4-145">Siirry kohtaan **Asetukset** > **Hallinto** > **Järjestelmäasetukset** > **Sales** ja varmista, että käytössä ovat seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="846e4-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="846e4-146">**Käytä järjestelmän hinnanlaskentajärjestelmää** -asetuksen arvoksi on määritetty **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="846e4-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="846e4-147">**Alennuksen laskutapa** -kentän arvoksi on määritetty **Rivinimike**.</span><span class="sxs-lookup"><span data-stu-id="846e4-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="846e4-148">Asetukset tietojen integrointiprojektissa</span><span class="sxs-lookup"><span data-stu-id="846e4-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="846e4-149">SalesInvoiceHeader -tehtävä</span><span class="sxs-lookup"><span data-stu-id="846e4-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="846e4-150">Varmista, että **InvoiceCountryRegionId**- ja **BillingAddress\_Country** -kohdan välinen yhdistämismääritys on tehty.</span><span class="sxs-lookup"><span data-stu-id="846e4-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="846e4-151">Malliarvo on arvomääritys, jossa on yhdistetty useita maita tai alueita.</span><span class="sxs-lookup"><span data-stu-id="846e4-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="846e4-152">Hinnasto on pakollinen Salesissa, jotta laskuja voidaan luoda.</span><span class="sxs-lookup"><span data-stu-id="846e4-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="846e4-153">Päivitä **pricelevelid.name \[hinnaston nimi\]**-kohdan arvomääritykseksi Salesissa käytettävä hinnasto.</span><span class="sxs-lookup"><span data-stu-id="846e4-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="846e4-154">Yhdelle valuutalle voit käyttää oletushinnastoa.</span><span class="sxs-lookup"><span data-stu-id="846e4-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="846e4-155">Vaihtoehtoisesti voit käyttää arvomääritystä, jos hinnastossa on useita valuuttoja.</span><span class="sxs-lookup"><span data-stu-id="846e4-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="846e4-156">**pricelevelid.name \[Price list name\]**-kohdan mallin arvo on arvomääritys, joka perustuu USD-valuuttaan = CRM Service USA (esimerkki).</span><span class="sxs-lookup"><span data-stu-id="846e4-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="846e4-157">SalesInvoiceLine -tehtävä</span><span class="sxs-lookup"><span data-stu-id="846e4-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="846e4-158">Varmista, että **Mittayksikkö**-kohdalla on pakollinen yhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="846e4-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="846e4-159">Varmista, että Finance and Operationsin **SalesUnitSymbol**-kohdassa on vaadittu arvomääritys.</span><span class="sxs-lookup"><span data-stu-id="846e4-159">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="846e4-160">**SalesUnitSymbol**-kohdan malliarvoksi, jolla on arvomääritys, on määritetty **Quantity\_UOM**.</span><span class="sxs-lookup"><span data-stu-id="846e4-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="846e4-161">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="846e4-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="846e4-162">**Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-kentät eivät sisälly oletusarvoisiin yhdistämismäärityksiin.</span><span class="sxs-lookup"><span data-stu-id="846e4-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="846e4-163">Näiden kenttien määrittämistä varten on määritettävä arvomääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="846e4-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="846e4-164">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="846e4-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="846e4-165">Yhdistämismääritys osoittaa, minkä kentän tiedot synkronoidaan Salesista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="846e4-165">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="846e4-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="846e4-166">SalesInvoiceHeader</span></span>

![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="846e4-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="846e4-168">SalesInvoiceLine</span></span>

![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="846e4-170">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="846e4-170">Related topics</span></span>

[<span data-ttu-id="846e4-171">Prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="846e4-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="846e4-172">Sales-asiakkaiden synkronointi suoraan Finance and Operations -asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="846e4-172">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="846e4-173">Finance and Operationsin tuotteiden synkronointi suoraan Salesin tuotteisiin</span><span class="sxs-lookup"><span data-stu-id="846e4-173">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="846e4-174">Salesin yhteyshenkilöiden synkronointi suoraan Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="846e4-174">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="846e4-175">Myyntitilauksien otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="846e4-175">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)







