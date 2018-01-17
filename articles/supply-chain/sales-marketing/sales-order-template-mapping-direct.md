---
title: Myyntitilauksien otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin
description: "Tässä ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin myyntitilausten otsikot ja rivit synkronoidaan suoraan Microsoft Dynamics 365 for Salesiin."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.openlocfilehash: e311b0becbb243cebdc265eccf3059eb46217dee
ms.contentlocale: fi-fi
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="29b6c-103">Myyntitilauksien otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="29b6c-103">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="29b6c-104">Tässä ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin myyntitilausten otsikot ja rivit synkronoidaan suoraan Microsoft Dynamics 365 for Salesiin.</span><span class="sxs-lookup"><span data-stu-id="29b6c-104">This topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="29b6c-105">Prospektista käteiseksi -ratkaisun tiedonkulku</span><span class="sxs-lookup"><span data-stu-id="29b6c-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="29b6c-106">Prospektista käteiseksi -ratkaisu käyttää tietojen integrointitoimintoa Finance and Operations and Sales -esiintymien tietojen synkronoinnissa.</span><span class="sxs-lookup"><span data-stu-id="29b6c-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="29b6c-107">Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Finance and Operationsin ja Salesin välillä.</span><span class="sxs-lookup"><span data-stu-id="29b6c-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="29b6c-108">Seuraavassa kuvassa kerrotaan, miten tiedot synkronoidaan Finance and Operations- ja Sales-sovelluksen välillä.</span><span class="sxs-lookup"><span data-stu-id="29b6c-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="29b6c-109">[![Prospektista käteiseksi -ratkaisun tiedonkulku](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="29b6c-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="29b6c-110">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="29b6c-110">Templates and tasks</span></span>

<span data-ttu-id="29b6c-111">Näet käytettävissä olevat mallit avaamalla [PowerApps-hallintakeskuksen](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="29b6c-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="29b6c-112">Valitse **Projektit** ja valitse sitten julkisia malleja oikeassa yläkulmassa olevan **Uusi projekti** -kohdan avulla.</span><span class="sxs-lookup"><span data-stu-id="29b6c-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="29b6c-113">Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan myyntitilausten otsikot ja rivit Finance and Operationsista Salesiin:</span><span class="sxs-lookup"><span data-stu-id="29b6c-113">The following template and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="29b6c-114">**Mallin nimi tietojen integroinnissa:** Myyntitilaukset (Fin and Opsista Salesiin) – suora</span><span class="sxs-lookup"><span data-stu-id="29b6c-114">**Name of the template in Data integration:** Sales Orders (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="29b6c-115">**Tehtävien nimet tietojen integrointiprojektissa:**</span><span class="sxs-lookup"><span data-stu-id="29b6c-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="29b6c-116">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="29b6c-116">OrderHeader</span></span>
    - <span data-ttu-id="29b6c-117">OrderLine</span><span class="sxs-lookup"><span data-stu-id="29b6c-117">OrderLine</span></span>

<span data-ttu-id="29b6c-118">Seuraavat synkronointitehtävät tarvitaan, ennen kuin myyntilaskujen otsikot ja rivit voidaan synkronoida:</span><span class="sxs-lookup"><span data-stu-id="29b6c-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="29b6c-119">Tuotteet (Fin and Opsista Salesiin) - suora</span><span class="sxs-lookup"><span data-stu-id="29b6c-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="29b6c-120">Tilit (Salesista Fin and Opsiin) - suora (jos käytössä)</span><span class="sxs-lookup"><span data-stu-id="29b6c-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="29b6c-121">Yhteyshenkilöistä asiakkaisiin (Salesista Fin and Opsiin) - suora (jos käytössä)</span><span class="sxs-lookup"><span data-stu-id="29b6c-121">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="29b6c-122">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="29b6c-122">Entity set</span></span>

| <span data-ttu-id="29b6c-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="29b6c-123">Finance and Operations</span></span>  | <span data-ttu-id="29b6c-124">Myynti</span><span class="sxs-lookup"><span data-stu-id="29b6c-124">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="29b6c-125">CDS myyntitilauksen otsikot</span><span class="sxs-lookup"><span data-stu-id="29b6c-125">CDS sales order headers</span></span> | <span data-ttu-id="29b6c-126">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="29b6c-126">SalesOrders</span></span>       |
| <span data-ttu-id="29b6c-127">CDS-myyntitilausrivit</span><span class="sxs-lookup"><span data-stu-id="29b6c-127">CDS sales order lines</span></span>   | <span data-ttu-id="29b6c-128">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="29b6c-128">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="29b6c-129">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="29b6c-129">Entity flow</span></span>

<span data-ttu-id="29b6c-130">Myyntitilaukset luodaan Finance and Operationsissa ja synkronoidaan Salesiin.</span><span class="sxs-lookup"><span data-stu-id="29b6c-130">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="29b6c-131">Mallin suodattimen auttavat varmistamaan, että vain asiaankuuluvat myyntitilaukset synkronoidaan:</span><span class="sxs-lookup"><span data-stu-id="29b6c-131">Filters in the template help guarantee that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="29b6c-132">Salesin myyntitilauksen tilaava asiakas ja laskutusasiakas sisällytetään synkronointiin.</span><span class="sxs-lookup"><span data-stu-id="29b6c-132">On the sales order, both the ordering customer and the invoicing customer that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="29b6c-133">Finance and Operations -sovelluksen **OrderingCustomerIsExternallyMaintained**- ja **InvoiceCustomerIsExternallyMaintained**-kenttiä käytetään tietoyksiköiden synkronointien seurantaan.</span><span class="sxs-lookup"><span data-stu-id="29b6c-133">In Finance and Operations, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** fields are used to track the synchronization in the data entities.</span></span>
- <span data-ttu-id="29b6c-134">Myyntitilaus on vahvistettava Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="29b6c-134">The sales order in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="29b6c-135">Salesiin synkronoidaan vain vahvistetut myyntitilaukset tai myyntitilaukset joilla on ylempi käsittelytila, kuten **Lähetetty** tai **Laskutettu**.</span><span class="sxs-lookup"><span data-stu-id="29b6c-135">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="29b6c-136">Kun myyntitilaus on luotu tai kun sitä on muokattu, **Laske kokonaismyynti** -eräajo on suoritettava Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="29b6c-136">After a sales order is created or modified, the **Calculate sales totals** batch job in Finance and Operations must be run.</span></span> <span data-ttu-id="29b6c-137">Salesiin synkronoidaan vain myyntitilaukset, joiden loppusummat on laskettu.</span><span class="sxs-lookup"><span data-stu-id="29b6c-137">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="29b6c-138">Tällä hetkellä myyntitilauksen otsikon kuluihin liittyviä veroja ei synkronoida Finance and Operationsista Salesiin.</span><span class="sxs-lookup"><span data-stu-id="29b6c-138">Currently, tax that is related to charges on the sales order header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="29b6c-139">Sales ei tue verotietoja otsikkotasolla.</span><span class="sxs-lookup"><span data-stu-id="29b6c-139">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="29b6c-140">Sen sijaan rivitason kuluihin liittyvä vero sisällytetään synkronointiin.</span><span class="sxs-lookup"><span data-stu-id="29b6c-140">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="29b6c-141">Salesin ratkaisu prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="29b6c-141">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="29b6c-142">**Tilaus**-yksikköön on lisätty uusia kenttiä, jotka näkyvät sivulla:</span><span class="sxs-lookup"><span data-stu-id="29b6c-142">New fields have been added to the **Order** entity and appear on the page:</span></span>

- <span data-ttu-id="29b6c-143">**Ulkoisesti ylläpidetty** – määritä tämän vaihtoehdon arvoksi **Kyllä**, kun tilaus on peräisin Finance and Operationsista.</span><span class="sxs-lookup"><span data-stu-id="29b6c-143">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Finance and Operations.</span></span>
- <span data-ttu-id="29b6c-144">**Käsittelytila** – tämä kenttä näyttää tilauksen käsittelytilan Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="29b6c-144">**Processing status** – This field shows the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="29b6c-145">Käytettävissä ovat seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="29b6c-145">The following values are available:</span></span>

    - <span data-ttu-id="29b6c-146">Aktiivinen</span><span class="sxs-lookup"><span data-stu-id="29b6c-146">Active</span></span>
    - <span data-ttu-id="29b6c-147">Vahvistettu</span><span class="sxs-lookup"><span data-stu-id="29b6c-147">Confirmed</span></span>
    - <span data-ttu-id="29b6c-148">Pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="29b6c-148">Packing Slip</span></span>
    - <span data-ttu-id="29b6c-149">Laskutettu</span><span class="sxs-lookup"><span data-stu-id="29b6c-149">Invoiced</span></span>
    - <span data-ttu-id="29b6c-150">Keräilty</span><span class="sxs-lookup"><span data-stu-id="29b6c-150">Picked</span></span>
    - <span data-ttu-id="29b6c-151">Osittain keräilty</span><span class="sxs-lookup"><span data-stu-id="29b6c-151">Partially Picked</span></span>
    - <span data-ttu-id="29b6c-152">Osittain pakattu</span><span class="sxs-lookup"><span data-stu-id="29b6c-152">Partially Packed</span></span>
    - <span data-ttu-id="29b6c-153">Lähetetty</span><span class="sxs-lookup"><span data-stu-id="29b6c-153">Shipped</span></span>
    - <span data-ttu-id="29b6c-154">Osittain lähetetty</span><span class="sxs-lookup"><span data-stu-id="29b6c-154">Partially Shipped</span></span>
    - <span data-ttu-id="29b6c-155">Osittain laskutettu</span><span class="sxs-lookup"><span data-stu-id="29b6c-155">Partially Invoiced</span></span>
    - <span data-ttu-id="29b6c-156">Peruutettu</span><span class="sxs-lookup"><span data-stu-id="29b6c-156">Cancelled</span></span>

<span data-ttu-id="29b6c-157">**Sisältää vain ulkoisesti ylläpidettyjä tuotteita** -asetusta käytetään muissa myyntitilausskenaarioissa (esimerkiksi synkronointi Salesista Finance and Operationsiin), jotta järjestelmä voi seurata, koostuuko myyntitilaus täysin ulkoisesti ylläpidetyistä tuotteista.</span><span class="sxs-lookup"><span data-stu-id="29b6c-157">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (for example, synchronization from Sales to Finance and Operation) to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="29b6c-158">Jos myyntitilauksessa on vain ulkoisesti ylläpidettyjä tuotteita, tuotteita ylläpidetään Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="29b6c-158">If a sales order consists entirely of externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="29b6c-159">Tämä asetus auttaa varmistamaan, ettet yritä synkronoida sellaisia myyntitilausrivejä, joissa on tuotteita, joita Finance and Operations ei tunne.</span><span class="sxs-lookup"><span data-stu-id="29b6c-159">This setting helps guarantee that you don't try to synchronize sales order lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="29b6c-160">**Myyntitilaus**-sivun **Luo lasku**, **Peruuta tilaus**, **Laske uudelleen**, **Hae tuotteet** ja **Hae osoite** -painikkeet on piilotettu ulkoisesti ylläpidetyissä tilauksissa, koska laskut luodaan Finance and Operationsissa, josta ne synkronoidaan Salesiin.</span><span class="sxs-lookup"><span data-stu-id="29b6c-160">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="29b6c-161">Tilaussivua ei voi muokata, sillä myyntitilaustiedot synkronoidaan Finance and Operationsista.</span><span class="sxs-lookup"><span data-stu-id="29b6c-161">The order page can't be edited, because sales order information will be synchronized from Finance and Operations.</span></span>

<span data-ttu-id="29b6c-162">Myyntitilauksen tila pysyy **aktiivisena**, jotta muutokset Finance and Operationsista siirtyvät Salesin myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="29b6c-162">The status of a sales order will remain **Active** to help guarantee that changes from Finance and Operations can flow to the sales order in Sales.</span></span> <span data-ttu-id="29b6c-163">Voit ohjata tätä toimintaa määrittämällä **Tilakoodi \[tila\]**-arvoksi **Aktiivinen** tietojen integrointiprojektissa.</span><span class="sxs-lookup"><span data-stu-id="29b6c-163">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="29b6c-164">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="29b6c-164">Preconditions and mapping setup</span></span>

<span data-ttu-id="29b6c-165">Seuraavat asetukset tulee päivittää järjestelmissä ennen myyntitilausten synkronointia.</span><span class="sxs-lookup"><span data-stu-id="29b6c-165">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="29b6c-166">Asetukset Salesissa</span><span class="sxs-lookup"><span data-stu-id="29b6c-166">Setup in Sales</span></span>

- <span data-ttu-id="29b6c-167">Varmista, että sen käyttäjän ryhmän käyttöoikeudet on määritetty, jolle Salesissa asetettu yhteys on määritetty.</span><span class="sxs-lookup"><span data-stu-id="29b6c-167">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="29b6c-168">Jos käytät esittelytietoja, käyttäjällä on usein järjestelmänvalvojan käyttöoikeudet, mutta ryhmällä ei.</span><span class="sxs-lookup"><span data-stu-id="29b6c-168">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="29b6c-169">Jos ryhmällä ei ole myöskään järjestelmänvalvojan käyttöoikeuksia, kun suoritat projektin tietojen integrointiohjelmasta, saat virheilmoituksen, jossa kerrotaan ensisijaisen ryhmän puuttumisesta.</span><span class="sxs-lookup"><span data-stu-id="29b6c-169">If the team doesn't also have admin access, when you run the project from Data integration, you will receive an error message that states that Principal team is missing.</span></span>

    <span data-ttu-id="29b6c-170">Siirry kohtaan **Asetukset** > **Suojaus** > **Ryhmät**ja valitse haluamasi ryhmä. Valitse **Roolien hallinta** ja valitse sitten halutut käyttöoikeudet, kuten **järjestelmänvalvoja**.</span><span class="sxs-lookup"><span data-stu-id="29b6c-170">Go to **Settings** > **Security** > **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="29b6c-171">Siirry kohtaan **Asetukset** > **Hallinto** > **Järjestelmäasetukset** > **Sales** ja varmista, että käytössä ovat seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="29b6c-171">Go to **Settings** > **Administration** > **System settings** > **Sales**, and makes sure that the following settings are used:</span></span>

    - <span data-ttu-id="29b6c-172">**Käytä järjestelmän hinnanlaskentajärjestelmää** -asetuksen arvoksi on määritetty **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="29b6c-172">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="29b6c-173">**Alennuksen laskutapa** -kentän arvoksi on määritetty **Rivinimike**.</span><span class="sxs-lookup"><span data-stu-id="29b6c-173">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="29b6c-174">Asetukset Finance and Operationsissa</span><span class="sxs-lookup"><span data-stu-id="29b6c-174">Setup in Finance and Operations</span></span>

<span data-ttu-id="29b6c-175">Siirry kohtaan **Myynti ja markkinointi** > **Kausittaiset tehtävät** > **Laske kokonaismyynti**. Määritä sitten erätyönä suoritettava työ.</span><span class="sxs-lookup"><span data-stu-id="29b6c-175">Go to **Sales and marketing** > **Periodic tasks** > **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="29b6c-176">Määritä **Laske myyntitilausten loppusummat** -vaihtoehdon arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="29b6c-176">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="29b6c-177">Tämä vaihe on tärkeä, koska Salesiin synkronoidaan vain myyntitilaukset, joiden loppusummat on laskettu.</span><span class="sxs-lookup"><span data-stu-id="29b6c-177">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="29b6c-178">Erätyön toistovälin tulisi olla sama kuin myyntitilausten synkronoinnin toistoväli.</span><span class="sxs-lookup"><span data-stu-id="29b6c-178">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="29b6c-179">Asetukset tietojen integrointiprojektissa</span><span class="sxs-lookup"><span data-stu-id="29b6c-179">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="29b6c-180">SalesHeader -tehtävä</span><span class="sxs-lookup"><span data-stu-id="29b6c-180">SalesHeader task</span></span>

- <span data-ttu-id="29b6c-181">Varmista, että tarvittavat yhdistämismääritykset on tehty **InvoiceCountryRegionId**- ja **BillingAddress\_Country**-kohdalle ja **DeliveryCountryRegionId**- ja **DeliveryAddress\_Country**-kohdalle.</span><span class="sxs-lookup"><span data-stu-id="29b6c-181">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country** and for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="29b6c-182">Malliarvo on arvomääritys, jossa on yhdistetty useita maita tai alueita.</span><span class="sxs-lookup"><span data-stu-id="29b6c-182">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="29b6c-183">Hinnasto on pakollinen Salesissa, jotta tilauksia voidaan luoda.</span><span class="sxs-lookup"><span data-stu-id="29b6c-183">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="29b6c-184">Päivitä **pricelevelid.name \[hinnaston nimi\]**-kohdan arvomääritykseksi Salesissa käytettävä hinnasto.</span><span class="sxs-lookup"><span data-stu-id="29b6c-184">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="29b6c-185">Yhdelle valuutalle voit käyttää oletushinnastoa.</span><span class="sxs-lookup"><span data-stu-id="29b6c-185">You can use the default price list for a single currency.</span></span> <span data-ttu-id="29b6c-186">Vaihtoehtoisesti voit käyttää arvomääritystä, jos hinnastossa on useita valuuttoja.</span><span class="sxs-lookup"><span data-stu-id="29b6c-186">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="29b6c-187">**pricelevelid.name \[hinnaston nimi\]** -kohdan oletusmallin arvo on **CRM Service USA (esimerkki)**.</span><span class="sxs-lookup"><span data-stu-id="29b6c-187">The default template value for **pricelevelid.name \[Price list name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="29b6c-188">SalesLine -tehtävä</span><span class="sxs-lookup"><span data-stu-id="29b6c-188">SalesLine task</span></span>

- <span data-ttu-id="29b6c-189">Varmista, että **DeliveryCountryRegionId**- ja **DeliveryAddress\_Country**-kohdan välinen yhdistämismääritys on tehty.</span><span class="sxs-lookup"><span data-stu-id="29b6c-189">Make sure that the required mapping exists for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="29b6c-190">Malliarvo on arvomääritys, jossa on yhdistetty useita maita tai alueita.</span><span class="sxs-lookup"><span data-stu-id="29b6c-190">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="29b6c-191">Varmista, että Finance and Operationsin **SalesUnitSymbol**-kohdassa on vaadittu arvomääritys.</span><span class="sxs-lookup"><span data-stu-id="29b6c-191">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="29b6c-192">**SalesUnitSymbol**-kohdan malliarvoksi, jolla on arvomääritys, on määritetty **Quantity\_UOM**.</span><span class="sxs-lookup"><span data-stu-id="29b6c-192">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="29b6c-193">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="29b6c-193">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="29b6c-194">**Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-kentät eivät sisälly oletusarvoisiin yhdistämismäärityksiin.</span><span class="sxs-lookup"><span data-stu-id="29b6c-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="29b6c-195">Näiden kenttien määrittämistä varten on määritettävä arvomääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="29b6c-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="29b6c-196">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="29b6c-196">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="29b6c-197">Yhdistämismääritys osoittaa, minkä kentän tiedot synkronoidaan Salesista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="29b6c-197">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="orderheader"></a><span data-ttu-id="29b6c-198">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="29b6c-198">OrderHeader</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a><span data-ttu-id="29b6c-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="29b6c-200">OrderLine</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="29b6c-202">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="29b6c-202">Related topics</span></span>

[<span data-ttu-id="29b6c-203">Prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="29b6c-203">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="29b6c-204">Sales-asiakkaiden synkronointi suoraan Finance and Operations -asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="29b6c-204">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="29b6c-205">Finance and Operationsin tuotteiden synkronointi suoraan Salesin tuotteisiin</span><span class="sxs-lookup"><span data-stu-id="29b6c-205">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="29b6c-206">Salesin yhteyshenkilöiden synkronointi suoraan Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="29b6c-206">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="29b6c-207">Myyntilaskujen otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="29b6c-207">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




