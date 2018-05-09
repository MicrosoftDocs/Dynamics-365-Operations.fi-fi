---
title: Myyntitarjouksien otsikoiden ja rivien synkronointi suoraan Salesista Finance and Operationsiin
description: "Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin myyntitarjousten otsikot ja rivit synkronoidaan suoraan Microsoft Dynamics 365 for Finance and Operationsiin."
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a18c8f2c335dee723c104648f8c7c1b79ea569d5
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="4e496-103">Myyntitarjouksien otsikoiden ja rivien synkronointi suoraan Salesista Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="4e496-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e496-104">Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin myyntitarjousten otsikot ja rivit synkronoidaan suoraan Microsoft Dynamics 365 for Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="4e496-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="4e496-105">Tutustu [Dynamics 365:n tietojen integrointiin](/common-data-service/entity-reference/dynamics-365-integration), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi.</span><span class="sxs-lookup"><span data-stu-id="4e496-105">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="4e496-106">Malli ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="4e496-106">Template and tasks</span></span>

<span data-ttu-id="4e496-107">Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkrontaessa myyntitarjousten otsikot ja rivit suoraan Salesista Finance and Operationsiin:</span><span class="sxs-lookup"><span data-stu-id="4e496-107">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="4e496-108">**Mallin nimi tietojen integroinnissa:** Myyntitarjoukset (Salesista Fin and Opsiin) – suora</span><span class="sxs-lookup"><span data-stu-id="4e496-108">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="4e496-109">**Tehtävien nimet tietojen integrointiprojektissa:**</span><span class="sxs-lookup"><span data-stu-id="4e496-109">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="4e496-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="4e496-110">QuoteHeader</span></span>
    - <span data-ttu-id="4e496-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="4e496-111">QuoteLine</span></span>

<span data-ttu-id="4e496-112">Seuraavat synkronointitehtävät tarvitaan, ennen kuin myyntitilaukset otsikot ja rivit voidaan synkronoida:</span><span class="sxs-lookup"><span data-stu-id="4e496-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="4e496-113">Tuotteet (Fin and Opsista Salesiin) - suora</span><span class="sxs-lookup"><span data-stu-id="4e496-113">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="4e496-114">Tilit (Salesista Fin and Opsiin) - suora (jos käytössä)</span><span class="sxs-lookup"><span data-stu-id="4e496-114">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="4e496-115">Yhteyshenkilöistä asiakkaisiin (Salesista Fin and Opsiin) - suora (jos käytössä)</span><span class="sxs-lookup"><span data-stu-id="4e496-115">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="4e496-116">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="4e496-116">Entity set</span></span>

| <span data-ttu-id="4e496-117">Myynti</span><span class="sxs-lookup"><span data-stu-id="4e496-117">Sales</span></span>        | <span data-ttu-id="4e496-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4e496-118">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="4e496-119">Tarjoukset</span><span class="sxs-lookup"><span data-stu-id="4e496-119">Quotes</span></span>       | <span data-ttu-id="4e496-120">CDS-myyntitarjouksen otsikko</span><span class="sxs-lookup"><span data-stu-id="4e496-120">CDS sales quotation header</span></span> |
| <span data-ttu-id="4e496-121">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="4e496-121">QuoteDetails</span></span> | <span data-ttu-id="4e496-122">CDS-myyntitarjousrivit</span><span class="sxs-lookup"><span data-stu-id="4e496-122">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="4e496-123">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="4e496-123">Entity flow</span></span>

<span data-ttu-id="4e496-124">Myyntitarjoukset luodaan Salesissa ja synkronoidaan Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="4e496-124">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="4e496-125">Salesin myyntitarjoukset synkronoidaan vain, jos seuraavat ehdot täyttyvät:</span><span class="sxs-lookup"><span data-stu-id="4e496-125">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="4e496-126">Kaikkia myyntitarjouksen tarjoustuotteita ylläpidetään ulkoisesti.</span><span class="sxs-lookup"><span data-stu-id="4e496-126">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="4e496-127">Kun valitset **Aktivoi tarjous**, myyntitarjouksesta tulee aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="4e496-127">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="4e496-128">Salesin ratkaisu prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="4e496-128">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="4e496-129">**Sisältää vain ulkoisesti ylläpidettyjä tuotteita** -kenttä on lisätty **Quote**-yksikköön seuraamaan johdonmukaisesti, koostuuko myyntitarjous kokonaan ulkoisesti ylläpidetyistä tuotteista.</span><span class="sxs-lookup"><span data-stu-id="4e496-129">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="4e496-130">Jos myyntitarjouksessa on vain ulkoisesti ylläpidettyjä tuotteita, tuotteita ylläpidetään Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="4e496-130">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="4e496-131">Tämä auttaa varmistamaan, ettet yritä synkronoida myyntitarjousrivejä sellaisten tuotteiden kanssa, joita Finance and Operations ei tunne.</span><span class="sxs-lookup"><span data-stu-id="4e496-131">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="4e496-132">Kaikki myyntitarjouksen tarjoustuotteet päivitetään myyntitarjouksen otsikon **Sisältää vain ulkoisesti ylläpidettyjä tuotteita** -tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="4e496-132">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="4e496-133">Nämä tiedot sijaitsevat **QuoteDetails**-yksikön **Tarjous sisältää vain ulkoisesti ylläpidettyjä tuotteita** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="4e496-133">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="4e496-134">Alennus lisätään tarjoustuotteeseen ja se synkronoidaan Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="4e496-134">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="4e496-135">Otsikon **Alennus**-, **Veloitukset**- ja **Vero**-kenttien hallinta perustuu Finance and Operationsin määrityksiin.</span><span class="sxs-lookup"><span data-stu-id="4e496-135">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="4e496-136">Tämä määritys ei tue tällä hetkellä integrointimääritystä.</span><span class="sxs-lookup"><span data-stu-id="4e496-136">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="4e496-137">Nykyisessä versiossa **Hinta**-, **Alennus**-, **Veloitus**- ja **Vero**-kenttiä ylläpidetään Finance and Operationsissa, jossa niitä myös käsitellään.</span><span class="sxs-lookup"><span data-stu-id="4e496-137">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="4e496-138">Seuraavat kentät ovat Salesissa vain luku -muotoisia, koska arvoja ei synkronoida Finance and Operationsiin:</span><span class="sxs-lookup"><span data-stu-id="4e496-138">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="4e496-139">Myyntitarjouksen otsikon vain luku -kentät: **Alennusprosentti**, **Alennus** ja **Rahdin summa**</span><span class="sxs-lookup"><span data-stu-id="4e496-139">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="4e496-140">Tarjoustuotteiden vain luku -kentät: **Vero**</span><span class="sxs-lookup"><span data-stu-id="4e496-140">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="4e496-141">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="4e496-141">Preconditions and mapping setup</span></span>

<span data-ttu-id="4e496-142">Seuraavat asetukset tulee päivittää ennen myyntitarjousten synkronointia.</span><span class="sxs-lookup"><span data-stu-id="4e496-142">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="4e496-143">Asetukset Salesissa</span><span class="sxs-lookup"><span data-stu-id="4e496-143">Setup in Sales</span></span>

- <span data-ttu-id="4e496-144">Varmista, että sen käyttäjän ryhmän käyttöoikeudet on määritetty, jolle Salesissa asetettu yhteys on määritetty.</span><span class="sxs-lookup"><span data-stu-id="4e496-144">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="4e496-145">Jos käytät esittelytietoja, käyttäjällä on usein järjestelmänvalvojan käyttöoikeudet, mutta ryhmällä ei.</span><span class="sxs-lookup"><span data-stu-id="4e496-145">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="4e496-146">Jos ryhmällä ei ole järjestelmänvalvojan käyttöoikeuksia, kun suoritat projektin tietojen integrointiohjelmasta, saat virheilmoituksen, jossa kerrotaan ensisijaisen ryhmän puuttumisesta.</span><span class="sxs-lookup"><span data-stu-id="4e496-146">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="4e496-147">Voit määrittää ryhmän käyttöoikeudet siirtymällä kohtaan **Asetukset** &gt; **Suojaus** &gt; **Ryhmät**. Valitse sitten haluamasi ryhmä.</span><span class="sxs-lookup"><span data-stu-id="4e496-147">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="4e496-148">Valitse **Roolien hallinta** ja valitse sitten rooli, jolla on halutut käyttöoikeudet, kuten **järjestelmänvalvoja**.</span><span class="sxs-lookup"><span data-stu-id="4e496-148">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="4e496-149">Siirry kohtaan **Asetukset** &gt; **Hallinto** &gt; **Järjestelmäasetukset** &gt; **Sales** ja varmista, että käytössä ovat seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="4e496-149">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="4e496-150">**Käytä järjestelmän hinnanlaskentajärjestelmää** -asetuksen arvoksi on määritetty **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="4e496-150">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="4e496-151">**Alennuksen laskutapa** -kentän arvoksi on määritetty **Rivinimike**.</span><span class="sxs-lookup"><span data-stu-id="4e496-151">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="4e496-152">Asetukset tietojen integrointiprojektissa</span><span class="sxs-lookup"><span data-stu-id="4e496-152">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="4e496-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="4e496-153">QuoteHeader</span></span>

- <span data-ttu-id="4e496-154">Varmista, että **Shipto\_country**- ja **DeliveryAddressCountryRegionISOCode**-kohdan välinen yhdistämismääritys on tehty.</span><span class="sxs-lookup"><span data-stu-id="4e496-154">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="4e496-155">Voit määrittää arvomäärityksessä oletusarvon, jota käytetään, jos kohta on jätetty tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="4e496-155">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="4e496-156">Voit vain jättää vasemman puolen tyhjäksi ja määrittää oikean puolen arvoksi halutun maan tai alueen.</span><span class="sxs-lookup"><span data-stu-id="4e496-156">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="4e496-157">Tällöin kansallisiin tilauksiin ei tarvitse kirjoittaa maata tai aluetta.</span><span class="sxs-lookup"><span data-stu-id="4e496-157">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="4e496-158">Malliarvo on arvomääritys, jossa on yhdistetty useita maita tai alueita. Jos kohta jätetään tyhjäksi, arvo on **US**.</span><span class="sxs-lookup"><span data-stu-id="4e496-158">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="4e496-159">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="4e496-159">QuoteLine</span></span>

- <span data-ttu-id="4e496-160">Varmista, että Finance and Operationsin **SalesUnitSymbol**-kohdassa on vaadittu arvomääritys.</span><span class="sxs-lookup"><span data-stu-id="4e496-160">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="4e496-161">Varmista, että Salesissa on määritetty pakolliset yksiköt.</span><span class="sxs-lookup"><span data-stu-id="4e496-161">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="4e496-162">**oumid.name**-kohdan malliarvoksi, jolla on arvomääritys, on määritetty **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="4e496-162">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="4e496-163">Valinnainen: Kun lisäät seuraavat yhdistämismääritykset, voit varmistaa, että myyntitarjouksen rivit tuodaan Finance and Operationsiin, jos asiakkaalla tai tuotteella ei ole oletustietoja:</span><span class="sxs-lookup"><span data-stu-id="4e496-163">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="4e496-164">**SiteId** – Toimipaikka on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan luoda Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="4e496-164">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="4e496-165">**SiteId**-oletusmalliarvoa ei ole.</span><span class="sxs-lookup"><span data-stu-id="4e496-165">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="4e496-166">**WarehouseId** – Varasto on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan käsitellä Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="4e496-166">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="4e496-167">**WarehouseId**-oletusmalliarvoa ei ole.</span><span class="sxs-lookup"><span data-stu-id="4e496-167">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="4e496-168">Mallin yhdistäminen tietojen integrointiohjelmassa</span><span class="sxs-lookup"><span data-stu-id="4e496-168">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="4e496-169">**Alennus**-, **Veloitukset**- ja **Vero**-kenttien hallinta perustuu monimutkaisiin Finance and Operationsin määrityksiin.</span><span class="sxs-lookup"><span data-stu-id="4e496-169">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="4e496-170">Tämä määritys ei tue tällä hetkellä integrointimääritystä.</span><span class="sxs-lookup"><span data-stu-id="4e496-170">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="4e496-171">Nykyisessä versiossa **Hinta**-, **Alennus**-, **Veloitus**- ja **Vero**-kenttiä käsitellään Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="4e496-171">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="4e496-172">**Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-kentät eivät sisälly oletusarvoisiin yhdistämismäärityksiin.</span><span class="sxs-lookup"><span data-stu-id="4e496-172">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="4e496-173">Näiden kenttien määrittämistä varten on määritettävä arvomääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="4e496-173">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="4e496-174">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integrointiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="4e496-174">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="4e496-175">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="4e496-175">QuoteHeader</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="4e496-177">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="4e496-177">QuoteLine</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="4e496-179">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="4e496-179">Related topics</span></span>

[<span data-ttu-id="4e496-180">Prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="4e496-180">Prospect to cash</span></span>](prospect-to-cash.md)


