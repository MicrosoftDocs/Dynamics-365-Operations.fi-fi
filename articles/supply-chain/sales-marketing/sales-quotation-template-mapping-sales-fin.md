---
title: Myyntitarjouksien otsikoiden ja rivien synkronointi suoraan Salesista Finance and Operationsiin
description: "Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin myyntitarjousten otsikot ja rivit synkronoidaan suoraan Microsoft Dynamics 365 for Finance and Operations, Enterprise editioniin."
author: ChristianRytt
manager: AnnBe
ms.date: 11/14/2017
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
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 8e2b568cdca1390bd9582ec913c1fa84924db9d0
ms.contentlocale: fi-fi
ms.lasthandoff: 01/19/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="6d384-103">Myyntitarjouksien otsikoiden ja rivien synkronointi suoraan Salesista Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="6d384-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6d384-104">Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin myyntitarjousten otsikot ja rivit synkronoidaan suoraan Microsoft Dynamics 365 for Finance and Operations, Enterprise editioniin.</span><span class="sxs-lookup"><span data-stu-id="6d384-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

> [!NOTE]
> <span data-ttu-id="6d384-105">Tutustu [Dynamics 365:n tietojen integrointiin](/common-data-service/entity-reference/dynamics-365-integration), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi.</span><span class="sxs-lookup"><span data-stu-id="6d384-105">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="6d384-106">Malli ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="6d384-106">Template and tasks</span></span>

<span data-ttu-id="6d384-107">Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkrontaessa myyntitarjousten otsikot ja rivit suoraan Salesista Finance and Operationsiin:</span><span class="sxs-lookup"><span data-stu-id="6d384-107">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="6d384-108">**Mallin nimi tietojen integroinnissa:** Myyntitarjoukset (Salesista Fin and Opsiin) – suora</span><span class="sxs-lookup"><span data-stu-id="6d384-108">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="6d384-109">**Tehtävien nimet tietojen integrointiprojektissa:**</span><span class="sxs-lookup"><span data-stu-id="6d384-109">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="6d384-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="6d384-110">QuoteHeader</span></span>
    - <span data-ttu-id="6d384-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="6d384-111">QuoteLine</span></span>

<span data-ttu-id="6d384-112">Seuraavat synkronointitehtävät tarvitaan, ennen kuin myyntitilaukset otsikot ja rivit voidaan synkronoida:</span><span class="sxs-lookup"><span data-stu-id="6d384-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="6d384-113">Tuotteet (Fin and Opsista Salesiin) - suora</span><span class="sxs-lookup"><span data-stu-id="6d384-113">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="6d384-114">Tilit (Salesista Fin and Opsiin) - suora (jos käytössä)</span><span class="sxs-lookup"><span data-stu-id="6d384-114">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="6d384-115">Yhteyshenkilöistä asiakkaisiin (Salesista Fin and Opsiin) - suora (jos käytössä)</span><span class="sxs-lookup"><span data-stu-id="6d384-115">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="6d384-116">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="6d384-116">Entity set</span></span>

| <span data-ttu-id="6d384-117">Myynti</span><span class="sxs-lookup"><span data-stu-id="6d384-117">Sales</span></span>        | <span data-ttu-id="6d384-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6d384-118">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="6d384-119">Tarjoukset</span><span class="sxs-lookup"><span data-stu-id="6d384-119">Quotes</span></span>       | <span data-ttu-id="6d384-120">CDS-myyntitarjouksen otsikko</span><span class="sxs-lookup"><span data-stu-id="6d384-120">CDS sales quotation header</span></span> |
| <span data-ttu-id="6d384-121">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="6d384-121">QuoteDetails</span></span> | <span data-ttu-id="6d384-122">CDS-myyntitarjousrivit</span><span class="sxs-lookup"><span data-stu-id="6d384-122">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="6d384-123">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="6d384-123">Entity flow</span></span>

<span data-ttu-id="6d384-124">Myyntitarjoukset luodaan Salesissa ja synkronoidaan Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="6d384-124">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="6d384-125">Salesin myyntitarjoukset synkronoidaan vain, jos seuraavat ehdot täyttyvät:</span><span class="sxs-lookup"><span data-stu-id="6d384-125">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="6d384-126">Kaikkia myyntitarjouksen tarjoustuotteita ylläpidetään ulkoisesti.</span><span class="sxs-lookup"><span data-stu-id="6d384-126">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="6d384-127">Kun valitset **Aktivoi tarjous**, myyntitarjouksesta tulee aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="6d384-127">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="6d384-128">Salesin ratkaisu prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="6d384-128">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="6d384-129">**Sisältää vain ulkoisesti ylläpidettyjä tuotteita** -kenttä on lisätty **Quote**-yksikköön seuraamaan johdonmukaisesti, koostuuko myyntitarjous kokonaan ulkoisesti ylläpidetyistä tuotteista.</span><span class="sxs-lookup"><span data-stu-id="6d384-129">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="6d384-130">Jos myyntitarjouksessa on vain ulkoisesti ylläpidettyjä tuotteita, tuotteita ylläpidetään Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="6d384-130">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="6d384-131">Tämä auttaa varmistamaan, ettet yritä synkronoida myyntitarjousrivejä sellaisten tuotteiden kanssa, joita Finance and Operations ei tunne.</span><span class="sxs-lookup"><span data-stu-id="6d384-131">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="6d384-132">Kaikki myyntitarjouksen tarjoustuotteet päivitetään myyntitarjouksen otsikon **Sisältää vain ulkoisesti ylläpidettyjä tuotteita** -tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="6d384-132">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="6d384-133">Nämä tiedot sijaitsevat **QuoteDetails**-yksikön **Tarjous sisältää vain ulkoisesti ylläpidettyjä tuotteita** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="6d384-133">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="6d384-134">Alennus lisätään tarjoustuotteeseen ja se synkronoidaan Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="6d384-134">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="6d384-135">Otsikon **Alennus**-, **Veloitukset**- ja **Vero**-kenttien hallinta perustuu Finance and Operationsin määrityksiin.</span><span class="sxs-lookup"><span data-stu-id="6d384-135">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="6d384-136">Tämä määritys ei tue tällä hetkellä integrointimääritystä.</span><span class="sxs-lookup"><span data-stu-id="6d384-136">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="6d384-137">Nykyisessä versiossa **Hinta**-, **Alennus**-, **Veloitus**- ja **Vero**-kenttiä ylläpidetään Finance and Operationsissa, jossa niitä myös käsitellään.</span><span class="sxs-lookup"><span data-stu-id="6d384-137">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="6d384-138">Seuraavat kentät ovat Salesissa vain luku -muotoisia, koska arvoja ei synkronoida Finance and Operationsiin:</span><span class="sxs-lookup"><span data-stu-id="6d384-138">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="6d384-139">Myyntitarjouksen otsikon vain luku -kentät: **Alennusprosentti**, **Alennus** ja **Rahdin summa**</span><span class="sxs-lookup"><span data-stu-id="6d384-139">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="6d384-140">Tarjoustuotteiden vain luku -kentät: **Vero**</span><span class="sxs-lookup"><span data-stu-id="6d384-140">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="6d384-141">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="6d384-141">Preconditions and mapping setup</span></span>

<span data-ttu-id="6d384-142">Seuraavat asetukset tulee päivittää ennen myyntitarjousten synkronointia.</span><span class="sxs-lookup"><span data-stu-id="6d384-142">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="6d384-143">Asetukset Salesissa</span><span class="sxs-lookup"><span data-stu-id="6d384-143">Setup in Sales</span></span>

- <span data-ttu-id="6d384-144">Varmista, että sen käyttäjän ryhmän käyttöoikeudet on määritetty, jolle Salesissa asetettu yhteys on määritetty.</span><span class="sxs-lookup"><span data-stu-id="6d384-144">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="6d384-145">Jos käytät esittelytietoja, käyttäjällä on usein järjestelmänvalvojan käyttöoikeudet, mutta ryhmällä ei.</span><span class="sxs-lookup"><span data-stu-id="6d384-145">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="6d384-146">Jos ryhmällä ei ole järjestelmänvalvojan käyttöoikeuksia, kun suoritat projektin tietojen integrointiohjelmasta, saat virheilmoituksen, jossa kerrotaan ensisijaisen ryhmän puuttumisesta.</span><span class="sxs-lookup"><span data-stu-id="6d384-146">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="6d384-147">Voit määrittää ryhmän käyttöoikeudet siirtymällä kohtaan **Asetukset** &gt; **Suojaus** &gt; **Ryhmät**. Valitse sitten haluamasi ryhmä.</span><span class="sxs-lookup"><span data-stu-id="6d384-147">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="6d384-148">Valitse **Roolien hallinta** ja valitse sitten rooli, jolla on halutut käyttöoikeudet, kuten **järjestelmänvalvoja**.</span><span class="sxs-lookup"><span data-stu-id="6d384-148">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="6d384-149">Siirry kohtaan **Asetukset** &gt; **Hallinto** &gt; **Järjestelmäasetukset** &gt; **Sales** ja varmista, että käytössä ovat seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="6d384-149">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="6d384-150">**Käytä järjestelmän hinnanlaskentajärjestelmää** -asetuksen arvoksi on määritetty **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="6d384-150">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="6d384-151">**Alennuksen laskutapa** -kentän arvoksi on määritetty **Rivinimike**.</span><span class="sxs-lookup"><span data-stu-id="6d384-151">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="6d384-152">Asetukset tietojen integrointiprojektissa</span><span class="sxs-lookup"><span data-stu-id="6d384-152">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="6d384-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="6d384-153">QuoteHeader</span></span>

- <span data-ttu-id="6d384-154">Varmista, että **Shipto\_country**- ja **DeliveryAddressCountryRegionISOCode**-kohdan välinen yhdistämismääritys on tehty.</span><span class="sxs-lookup"><span data-stu-id="6d384-154">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="6d384-155">Voit määrittää arvomäärityksessä oletusarvon, jota käytetään, jos kohta on jätetty tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="6d384-155">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="6d384-156">Voit vain jättää vasemman puolen tyhjäksi ja määrittää oikean puolen arvoksi halutun maan tai alueen.</span><span class="sxs-lookup"><span data-stu-id="6d384-156">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="6d384-157">Tällöin kansallisiin tilauksiin ei tarvitse kirjoittaa maata tai aluetta.</span><span class="sxs-lookup"><span data-stu-id="6d384-157">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="6d384-158">Malliarvo on arvomääritys, jossa on yhdistetty useita maita tai alueita. Jos kohta jätetään tyhjäksi, arvo on **US**.</span><span class="sxs-lookup"><span data-stu-id="6d384-158">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="6d384-159">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="6d384-159">QuoteLine</span></span>

- <span data-ttu-id="6d384-160">Varmista, että Finance and Operationsin **SalesUnitSymbol**-kohdassa on vaadittu arvomääritys.</span><span class="sxs-lookup"><span data-stu-id="6d384-160">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="6d384-161">Varmista, että Salesissa on määritetty pakolliset yksiköt.</span><span class="sxs-lookup"><span data-stu-id="6d384-161">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="6d384-162">**oumid.name**-kohdan malliarvoksi, jolla on arvomääritys, on määritetty **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="6d384-162">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="6d384-163">Valinnainen: Kun lisäät seuraavat yhdistämismääritykset, voit varmistaa, että myyntitarjouksen rivit tuodaan Finance and Operationsiin, jos asiakkaalla tai tuotteella ei ole oletustietoja:</span><span class="sxs-lookup"><span data-stu-id="6d384-163">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="6d384-164">**SiteId** – Toimipaikka on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan luoda Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="6d384-164">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="6d384-165">**SiteId**-oletusmalliarvoa ei ole.</span><span class="sxs-lookup"><span data-stu-id="6d384-165">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="6d384-166">**WarehouseId** – Varasto on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan käsitellä Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="6d384-166">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="6d384-167">**WarehouseId**-oletusmalliarvoa ei ole.</span><span class="sxs-lookup"><span data-stu-id="6d384-167">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="6d384-168">Mallin yhdistäminen tietojen integrointiohjelmassa</span><span class="sxs-lookup"><span data-stu-id="6d384-168">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="6d384-169">**Alennus**-, **Veloitukset**- ja **Vero**-kenttien hallinta perustuu monimutkaisiin Finance and Operationsin määrityksiin.</span><span class="sxs-lookup"><span data-stu-id="6d384-169">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="6d384-170">Tämä määritys ei tue tällä hetkellä integrointimääritystä.</span><span class="sxs-lookup"><span data-stu-id="6d384-170">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="6d384-171">Nykyisessä versiossa **Hinta**-, **Alennus**-, **Veloitus**- ja **Vero**-kenttiä käsitellään Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="6d384-171">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="6d384-172">**Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-kentät eivät sisälly oletusarvoisiin yhdistämismäärityksiin.</span><span class="sxs-lookup"><span data-stu-id="6d384-172">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="6d384-173">Näiden kenttien määrittämistä varten on määritettävä arvomääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="6d384-173">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="6d384-174">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integrointiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="6d384-174">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="6d384-175">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="6d384-175">QuoteHeader</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="6d384-177">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="6d384-177">QuoteLine</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="6d384-179">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="6d384-179">Related topics</span></span>

[<span data-ttu-id="6d384-180">Prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="6d384-180">Prospect to cash</span></span>](prospect-to-cash.md)


