---
title: Myyntitarjousten otsikoiden ja rivien synkronointi suoraan Salesista Supply Chain Managementiin
description: Tässä ohjeaiheessa käsitellään malleja ja niiden taustalla olevia tehtäviä, joita käytetään synkronoimaan myyntitarjousten otsikot ja rivit suoraan Dynamics 365 Salesista Dynamics 365 Supply Chain Managementiin.
author: ChristianRytt
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: bdca4d63fbe04a01cf1bbf2ccd7b095d4718a115
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910302"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a><span data-ttu-id="09574-103">Myyntitarjousten otsikoiden ja rivien synkronointi suoraan Salesista Supply Chain Managementiin</span><span class="sxs-lookup"><span data-stu-id="09574-103">Synchronize sales quotation headers and lines directly from Sales to Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="09574-104">Tässä ohjeaiheessa käsitellään malleja ja niiden taustalla olevia tehtäviä, joita käytetään synkronoimaan myyntitarjousten otsikot ja rivit suoraan Dynamics 365 Salesista Dynamics 365 Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="09574-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

> [!NOTE]
> <span data-ttu-id="09574-105">Tutustu [Microsoft Dataverse for Appsin tietojen integrointiin](/powerapps/administrator/data-integrator), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi.</span><span class="sxs-lookup"><span data-stu-id="09574-105">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator).</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="09574-106">Prospektista käteiseksi -ratkaisun tiedonkulku</span><span class="sxs-lookup"><span data-stu-id="09574-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="09574-107">Prospektista käteiseksi -ratkaisu käyttää tietojen integrointitoimintoa Supply Chain Managementin and Salesin esiintymien tietojen synkronoinnissa.</span><span class="sxs-lookup"><span data-stu-id="09574-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="09574-108">Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Supply Chain Managementin ja Salesin välillä.</span><span class="sxs-lookup"><span data-stu-id="09574-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="09574-109">Seuraava kuva näyttää, miten tiedot synkronoidaan Supply Chain Managementin ja Salesin välillä.</span><span class="sxs-lookup"><span data-stu-id="09574-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="09574-110">[![Prospektista käteiseksi -ratkaisun tiedonkulku](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="09574-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="09574-111">Malli ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="09574-111">Template and tasks</span></span>

<span data-ttu-id="09574-112">Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoitaessa myyntitarjousten otsikot ja rivit suoraan Salesista Supply Chain Managementiin:</span><span class="sxs-lookup"><span data-stu-id="09574-112">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="09574-113">**Mallin nimi tietojen integroinnissa:** Myyntitarjoukset (Salesista Supply Chain Managementiin) – suora</span><span class="sxs-lookup"><span data-stu-id="09574-113">**Name of the template in Data integration:** Sales Quotes (Sales to Supply Chain Management) - Direct</span></span>
- <span data-ttu-id="09574-114">**Tehtävien nimet tietojen integrointiprojektissa:**</span><span class="sxs-lookup"><span data-stu-id="09574-114">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="09574-115">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="09574-115">QuoteHeader</span></span>
    - <span data-ttu-id="09574-116">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="09574-116">QuoteLine</span></span>

<span data-ttu-id="09574-117">Seuraavat synkronointitehtävät tarvitaan, ennen kuin myyntitilaukset otsikot ja rivit voidaan synkronoida:</span><span class="sxs-lookup"><span data-stu-id="09574-117">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="09574-118">Tuotteet (Supply Chain Managementista Salesiin) - suora</span><span class="sxs-lookup"><span data-stu-id="09574-118">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="09574-119">Tilit (Salesista Supply Chain Managementiin) - Suora (jos käytössä)</span><span class="sxs-lookup"><span data-stu-id="09574-119">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="09574-120">Yhteyshenkilöistä asiakkaisiin (Salesista Supply Chain Managementiin) - Suora (jos käytössä)</span><span class="sxs-lookup"><span data-stu-id="09574-120">Contacts to Customers (Sales to Supply Chain Management) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="09574-121">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="09574-121">Entity set</span></span>

| <span data-ttu-id="09574-122">Myynti</span><span class="sxs-lookup"><span data-stu-id="09574-122">Sales</span></span>        | <span data-ttu-id="09574-123">Toimitusketjun hallinta</span><span class="sxs-lookup"><span data-stu-id="09574-123">Supply Chain Management</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="09574-124">Tarjoukset</span><span class="sxs-lookup"><span data-stu-id="09574-124">Quotes</span></span>       | <span data-ttu-id="09574-125">Dataversen myyntitarjouksen otsikko</span><span class="sxs-lookup"><span data-stu-id="09574-125">Dataverse sales quotation header</span></span> |
| <span data-ttu-id="09574-126">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="09574-126">QuoteDetails</span></span> | <span data-ttu-id="09574-127">Dataversen myyntitarjousrivit</span><span class="sxs-lookup"><span data-stu-id="09574-127">Dataverse sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="09574-128">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="09574-128">Entity flow</span></span>

<span data-ttu-id="09574-129">Myyntitarjoukset luodaan Salesissa ja synkronoidaan Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="09574-129">Sales quotations are created in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="09574-130">Salesin myyntitarjoukset synkronoidaan vain, jos seuraavat ehdot täyttyvät:</span><span class="sxs-lookup"><span data-stu-id="09574-130">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="09574-131">Kaikkia myyntitarjouksen tarjoustuotteita ylläpidetään ulkoisesti.</span><span class="sxs-lookup"><span data-stu-id="09574-131">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="09574-132">Kun valitset **Aktivoi tarjous**, myyntitarjouksesta tulee aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="09574-132">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="09574-133">Salesin ratkaisu prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="09574-133">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="09574-134">**Sisältää vain ulkoisesti ylläpidettyjä tuotteita** -kenttä on lisätty **Quote**-yksikköön seuraamaan johdonmukaisesti, koostuuko myyntitarjous kokonaan ulkoisesti ylläpidetyistä tuotteista.</span><span class="sxs-lookup"><span data-stu-id="09574-134">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="09574-135">Jos myyntitarjouksessa on vain ulkoisesti ylläpidettyjä tuotteita, tuotteita ylläpidetään Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="09574-135">If a sales quotation has only externally maintained products, the products are maintained in Supply Chain Management.</span></span> <span data-ttu-id="09574-136">Tämä auttaa varmistamaan, ettet yritä synkronoida myyntitarjousrivejä sellaisten tuotteiden kanssa, joita Supply Chain Management ei tunne.</span><span class="sxs-lookup"><span data-stu-id="09574-136">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Supply Chain Management.</span></span>

<span data-ttu-id="09574-137">Kaikki myyntitarjouksen tarjoustuotteet päivitetään myyntitarjouksen otsikon **Sisältää vain ulkoisesti ylläpidettyjä tuotteita** -tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="09574-137">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="09574-138">Nämä tiedot sijaitsevat **QuoteDetails**-yksikön **Tarjous sisältää vain ulkoisesti ylläpidettyjä tuotteita** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="09574-138">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="09574-139">Alennus lisätään tarjoustuotteeseen ja se synkronoidaan Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="09574-139">A discount can be added to the quote product and will be synchronized to Supply Chain Management.</span></span> <span data-ttu-id="09574-140">Otsikon **Alennus**-, **Veloitukset**- ja **Vero**-kenttien hallinta perustuu Supply Chain Managementin määrityksiin.</span><span class="sxs-lookup"><span data-stu-id="09574-140">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Supply Chain Management.</span></span> <span data-ttu-id="09574-141">Tämä määritys ei tue tällä hetkellä integrointimääritystä.</span><span class="sxs-lookup"><span data-stu-id="09574-141">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="09574-142">Nykyisessä versiossa **Hinta**-, **Alennus**-, **Veloitus**- ja **Vero**-kenttiä ylläpidetään Supply Chain Managementissa, jossa niitä myös käsitellään.</span><span class="sxs-lookup"><span data-stu-id="09574-142">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in FSupply Chain Management.</span></span>

<span data-ttu-id="09574-143">Seuraavat kentät ovat Salesissa vain luku -muotoisia, koska arvoja ei synkronoida Supply Chain Managementiin:</span><span class="sxs-lookup"><span data-stu-id="09574-143">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Supply Chain Management:</span></span>

- <span data-ttu-id="09574-144">Myyntitarjouksen otsikon vain luku -kentät: **Alennusprosentti**, **Alennus** ja **Rahdin summa**</span><span class="sxs-lookup"><span data-stu-id="09574-144">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="09574-145">Tarjoustuotteiden vain luku -kentät: **Vero**</span><span class="sxs-lookup"><span data-stu-id="09574-145">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="09574-146">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="09574-146">Preconditions and mapping setup</span></span>

<span data-ttu-id="09574-147">Seuraavat asetukset tulee päivittää ennen myyntitarjousten synkronointia.</span><span class="sxs-lookup"><span data-stu-id="09574-147">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="09574-148">Asetukset Salesissa</span><span class="sxs-lookup"><span data-stu-id="09574-148">Setup in Sales</span></span>

- <span data-ttu-id="09574-149">Varmista, että sen käyttäjän ryhmän käyttöoikeudet on määritetty, jolle Salesissa asetettu yhteys on määritetty.</span><span class="sxs-lookup"><span data-stu-id="09574-149">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="09574-150">Jos käytät esittelytietoja, käyttäjällä on usein järjestelmänvalvojan käyttöoikeudet, mutta ryhmällä ei.</span><span class="sxs-lookup"><span data-stu-id="09574-150">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="09574-151">Jos ryhmällä ei ole järjestelmänvalvojan käyttöoikeuksia, kun suoritat projektin tietojen integrointiohjelmasta, saat virheilmoituksen, jossa kerrotaan ensisijaisen ryhmän puuttumisesta.</span><span class="sxs-lookup"><span data-stu-id="09574-151">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="09574-152">Voit määrittää ryhmän käyttöoikeudet siirtymällä kohtaan **Asetukset** &gt; **Suojaus** &gt; **Ryhmät**. Valitse sitten haluamasi ryhmä.</span><span class="sxs-lookup"><span data-stu-id="09574-152">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="09574-153">Valitse **Roolien hallinta** ja valitse sitten rooli, jolla on halutut käyttöoikeudet, kuten **järjestelmänvalvoja**.</span><span class="sxs-lookup"><span data-stu-id="09574-153">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="09574-154">Siirry kohtaan **Asetukset** &gt; **Hallinto** &gt; **Järjestelmäasetukset** &gt; **Sales** ja varmista, että käytössä ovat seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="09574-154">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="09574-155">**Käytä järjestelmän hinnanlaskentajärjestelmää** -asetuksen arvoksi on määritetty **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="09574-155">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="09574-156">**Alennuksen laskutapa** -kentän arvoksi on määritetty **Rivinimike**.</span><span class="sxs-lookup"><span data-stu-id="09574-156">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="09574-157">Asetukset tietojen integrointiprojektissa</span><span class="sxs-lookup"><span data-stu-id="09574-157">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="09574-158">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="09574-158">QuoteHeader</span></span>

- <span data-ttu-id="09574-159">Varmista, että **Shipto\_country**- ja **DeliveryAddressCountryRegionISOCode**-kohdan välinen yhdistämismääritys on tehty.</span><span class="sxs-lookup"><span data-stu-id="09574-159">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="09574-160">Voit määrittää arvomäärityksessä oletusarvon, jota käytetään, jos kohta on jätetty tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="09574-160">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="09574-161">Voit vain jättää vasemman puolen tyhjäksi ja määrittää oikean puolen arvoksi halutun maan tai alueen.</span><span class="sxs-lookup"><span data-stu-id="09574-161">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="09574-162">Tällöin kansallisiin tilauksiin ei tarvitse kirjoittaa maata tai aluetta.</span><span class="sxs-lookup"><span data-stu-id="09574-162">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="09574-163">Malliarvo on arvomääritys, jossa on yhdistetty useita maita tai alueita. Jos kohta jätetään tyhjäksi, arvo on **US**.</span><span class="sxs-lookup"><span data-stu-id="09574-163">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="09574-164">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="09574-164">QuoteLine</span></span>

- <span data-ttu-id="09574-165">Varmista, että Supply Chain Managementin **SalesUnitSymbol**-kohdassa on vaadittu arvomääritys.</span><span class="sxs-lookup"><span data-stu-id="09574-165">Make sure that the required value map exists for **SalesUnitSymbol** in Supply Chain Management.</span></span>
- <span data-ttu-id="09574-166">Varmista, että Salesissa on määritetty pakolliset yksiköt.</span><span class="sxs-lookup"><span data-stu-id="09574-166">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="09574-167">**oumid.name**-kohdan malliarvoksi, jolla on arvomääritys, on määritetty **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="09574-167">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="09574-168">Valinnainen: Kun lisäät seuraavat yhdistämismääritykset, voit varmistaa, että myyntitarjouksen rivit tuodaan Supply Chain Managementiin, jos asiakkaalla tai tuotteella ei ole oletustietoja:</span><span class="sxs-lookup"><span data-stu-id="09574-168">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Supply Chain Management if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="09574-169">**SiteId** – Toimipaikka on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan luoda Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="09574-169">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="09574-170">**SiteId**-oletusmalliarvoa ei ole.</span><span class="sxs-lookup"><span data-stu-id="09574-170">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="09574-171">**WarehouseId** – Varasto on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan käsitellä Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="09574-171">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="09574-172">**WarehouseId**-oletusmalliarvoa ei ole.</span><span class="sxs-lookup"><span data-stu-id="09574-172">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="09574-173">Mallin yhdistäminen tietojen integrointiohjelmassa</span><span class="sxs-lookup"><span data-stu-id="09574-173">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="09574-174">**Alennus**-, **Veloitukset**- ja **Vero**-kenttien hallinta perustuu Supply Chain Managementin monimutkaisiin määrityksiin.</span><span class="sxs-lookup"><span data-stu-id="09574-174">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Supply Chain Management.</span></span> <span data-ttu-id="09574-175">Tämä määritys ei tue tällä hetkellä integrointimääritystä.</span><span class="sxs-lookup"><span data-stu-id="09574-175">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="09574-176">Nykyisessä versiossa **Hinta**-, **Alennus**-, **Veloitus**- ja **Vero**-kenttiä käsitellään Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="09574-176">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Supply Chain Management.</span></span>
> - <span data-ttu-id="09574-177">**Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-kentät eivät sisälly oletusarvoisiin yhdistämismäärityksiin.</span><span class="sxs-lookup"><span data-stu-id="09574-177">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="09574-178">Näiden kenttien määrittämistä varten on määritettävä arvomääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="09574-178">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="09574-179">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integrointiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="09574-179">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="09574-180">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="09574-180">QuoteHeader</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="09574-182">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="09574-182">QuoteLine</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="09574-184">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="09574-184">Related topics</span></span>

[<span data-ttu-id="09574-185">Prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="09574-185">Prospect to cash</span></span>](prospect-to-cash.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]